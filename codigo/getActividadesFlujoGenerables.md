### 🏠 [Inicio](../index.md "Inicio")

# getActividadesFlujoGenerables

## Definicion

Este método se encarga de validar las tareas que tengan algún campo parametrizado y en caso de que encuentre al menos un campo le inserta el valor “SI” al TAG de esa actividad en el flujo.

## Método C#

```
public static DataTable getActividadesFlujoGenerables(string tipoMaterial)
{
    string sql = @"SELECT 
                        CASE 
                            WHEN a.codigo = 80 THEN 'TRSOL'
                            WHEN a.codigo = 81 THEN 'TRDPLANB'
                            WHEN a.codigo = 82 THEN 'TRDIMP' 
                            WHEN a.codigo = 83 THEN 'TRPPROD' 
                            WHEN a.codigo = 84 THEN 'TRPCONT' 
                            WHEN a.codigo = 85 THEN 'TRPCOMP' 
                            WHEN a.codigo = 86 THEN 'TRDCAL'
                            WHEN a.codigo = 87 THEN 'TRICOS'
                            WHEN a.codigo = 88 THEN 'TRIVEN'
                            WHEN a.codigo = 89 THEN 'TRIALM'
                        ELSE '' END id, 
                        CASE 
                            WHEN c.requiereCampos > 0 AND a.codigo = 80 THEN 'SI' 
                            WHEN c.requiereCampos > 0 AND a.codigo = 81 THEN 'SI' 
                            WHEN c.requiereCampos > 0 AND a.codigo = 82 THEN 'SI' 
                            WHEN c.requiereCampos > 0 AND a.codigo = 83 THEN 'SI' 
                            WHEN c.requiereCampos > 0 AND a.codigo = 84 THEN 'SI' 
                            WHEN c.requiereCampos > 0 AND a.codigo = 85 THEN 'SI' 
                            WHEN c.requiereCampos > 0 AND a.codigo = 86 THEN 'SI'
                            WHEN c.requiereCampos > 0 AND a.codigo = 87 THEN 'SI'
                            WHEN c.requiereCampos > 0 AND a.codigo = 88 THEN 'SI'
                            WHEN c.requiereCampos > 0 AND a.codigo = 89 THEN 'SI'
                        ELSE 'NO' END valor
                    FROM (
                            SELECT a.asu_id codigo, a.asu_nombre texto
                            FROM asuntos2 a
                            WHERE a.asu_tso_id = 8
                        ) a
                        LEFT JOIN 
                        (
                            SELECT cfc_conceptoBusqueda, SUM(CASE WHEN cfc_requerido > 0 THEN 1 ELSE 0 END) requiereCampos
                            FROM frm_mae_configFormularioCampos
                            GROUP BY cfc_conceptoBusqueda
                        ) c ON c.cfc_conceptoBusqueda = @tipoMaterial + CONVERT(NVARCHAR(10), a.codigo)
                    WHERE a.codigo IN(80,81,82, 83, 84, 85, 86, 87, 88, 89)";

    GenericProvider gp = new GenericProvider(EasyConfigH.getString("ConnectionStrings", "ConnectionString"));
    DataTable result = gp.GetTable(sql, CommandType.Text
                                                , gp.GetDBParameter("@tipoMaterial", tipoMaterial));

    return result;
}
```
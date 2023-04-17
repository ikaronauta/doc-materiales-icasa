# Materiales

- ## 📚 Tabla de Contenido

- [Materiales](#materiales)
  - [↗️ Diagramas](#-diagramas)
    - [Diagrama Flujo](#diagrama-flujo)
    - [Prueba Solicitud](#prueba-solicitud)
    - [Bosquejo](#bosquejo)
    - [Proceso](#proceso)
    - [Actividades](#actividades)
  - [📋 Diligenciamiento Formularios](#-diligenciamiento-formularios)
    - [80 Registrar Solicitud](#80-registrar-solicitud)
    - [81 Registrar Datos Planificación Base](#81-registrar-datos-planificación-base)
    - [82 Registrar Datos de Impuestos](#82-registrar-datos-de-impuestos)
    - [83 Registrar Planificación Producción](#83-registrar-planificación-producción)
    - [84 Registrar Planificación Contabilidad](#84-registrar-planificación-contabilidad)
    - [85 Registrar Planificación Compras](#85-registrar-planificación-compras)
    - [86 Registrar Datos de Calidad](#86-registrar-datos-de-calidad)
    - [87 Registrar Información de Costos](#87-registrar-información-de-costos)
    - [88 Registrar Información de Ventas](#88-registrar-información-de-ventas)
    - [89 Registrar Información de Almacenamiento](#89-registrar-información-de-almacenamiento)
    - [90 Realizar Validación Técnica](#90-realizar-validación-técnica)
    - [91 Revisar y Crear en SAP](#91-revisar-y-crear-en-sap)
    - [92 Aprobación Vicepresidencia o Sociedad](#92-aprobación-vicepresidencia-o-sociedad)
  - [📝 Código](#-código)
    - [getActividadesFlujoGenerables](#getactividadesflujogenerables)
    - [Definicion](#definicion)
    - [Método C#](#método-c)

- ## ↗️ Diagramas

### Diagrama Flujo

![Flujo Materiales](./images/flujo.png "Flujo Materiales")

---

### Prueba Solicitud

```
⚪ Inicio Proceso
      │
      │
5993 Registrar ─┬── 5995 Registrar Datos
Solicitud       │   Planificación Base
                │             │
                │             │
                │             │
                │             │
                │      5996 Registrar Información ────┐
                │      de Costos                      │
                │             │                       │
                │             │                       │
                │      5997 Registrar Información ────┤
                │      de Ventas                      │
                │             │                       ├─── 5999 Realizar      ─── 6000 Revisar y
                │             │                       │    Validación Técnica     Crear en Sap
                │      5998 Registrar Información ────┤                                 │
                │      de Almacenamiento              │                                 │
                │                                     │                                 │
                │                                     │                                 │
                │                                     │                           ⚫Fin Proceso
                │                                     │
                └── 5994 Registrar Datos ─────────────┘
                    de Impuestos
```

---

### Bosquejo

![Bosquejo](./images/bosquejo.png "Bosquejo")

- ## 🎏 Descripción General

### Proceso

Materiales: **8**

---

### Actividades

| Actividad | Detalle                                 | Id sol_plantillas_cliente | Id frm_Formularios | Formulario |
| --------- | --------------------------------------- | ------------------------- | ------------------ | ---------- |
| 80        | Registrar Solicitud                     | 8                         | 80                 | p8_f1      |
| 81        | Registrar Datos Planificación Base      |                           | 81                 | P8_f2      |
| 82        | Registrar Datos de Impuestos            |                           | 82                 | p8_f3      |
| 83        | Registrar Planificación Producción      |                           | 83                 | p8_f4      |
| 84        | Registrar Planificación Contabilidad    |                           | 84                 | p8_f5      |
| 85        | Registrar Planificación Compras         |                           | 85                 | p8_f6      |
| 86        | Registrar Datos de Calidad              |                           | 86                 | p8_f7      |
| 87        | Registrar Información de Costos         |                           | 87                 | p8_f8      |
| 88        | Registrar Información de Ventas         |                           | 88                 | p8_f9      |
| 89        | Registrar Información de Almacenamiento |                           | 89                 | p8_f10     |
| 90        | Realizar Validación Técnica             |                           | 90                 | p8_f11     |
| 91        | Revisar y Crear en SAP                  |                           | 91                 | p8_f12     |
| 92        | Aprobación Vicepresidencia o Sociedad   |                           | 92                 | p8_f17     |


## 📋 Diligenciamiento Formularios

### 80 Registrar Solicitud

- Se debe seleccionar el ***Tipo de Material*** para que se cargue la configuración establecida en el parametrizador de campos para este ese material.

- Se debe seleccionar una ***Vicepresidencia*** para que se filtren las sociedades.

- Se debe seleccionar al menos una ***sociedad***.

- Se debe seleccionar una ***Clave*** para que se pueda generar una descripción.

- Los campos ***Denominación*** y ***Descripción larga*** se cargan de acuerdo a lo registrado al ***Generar la Descripción***.

- Se debe seleccionar al menos un ***Centro*** y ***Generar los Datos de Centro***.

> :information_source:  **Info**  
> _Con los anteriores pasos ya es posible guardar el formulario._
>

### 81 Registrar Datos Planificación Base

- Ingresar datos requeridos en Grid ***"gPlantData"***.

- Marcar una de las opciones del campo ***¿Reasignar solicitud?*** .

> :information_source:  **Info**  
> _Con los anteriores pasos ya es posible guardar el formulario._

---

### 82 Registrar Datos de Impuestos

- Marcar una de las opciones del campo ***¿Reasignar solicitud?*** .

> :information_source:  **Info**  
> _Con los anteriores pasos ya es posible guardar el formulario._

---

### 83 Registrar Planificación Producción

---

### 84 Registrar Planificación Contabilidad

---

### 85 Registrar Planificación Compras

---

### 86 Registrar Datos de Calidad

---

### 87 Registrar Información de Costos

- Ingresar datos requeridos en Grid ***"gPlantData"***.

- Ingresar datos requeridos en Grid ***"gAccountingData"***.

- Marcar una de las opciones del campo ***¿Reasignar solicitud?*** .

> :information_source:  **Info**  
> _Con los anteriores pasos ya es posible guardar el formulario._

---

### 88 Registrar Información de Ventas

- Marcar una de las opciones del campo ***¿Reasignar solicitud?*** .

> :information_source:  **Info**  
> _Con los anteriores pasos ya es posible guardar el formulario._

---

### 89 Registrar Información de Almacenamiento

- Se debe seleccionarl al menos un almacen y ***"Generar Datos de Ubicación de Almacenamiento"***.

- Marcar una de las opciones del campo ***¿Reasignar solicitud?*** .

> :information_source:  **Info**  
> _Con los anteriores pasos ya es posible guardar el formulario._

---

### 90 Realizar Validación Técnica

- Marcar una de las opciones del campo ***Datos correctos*** .

> :information_source:  **Info**  
> _Con los anteriores pasos ya es posible guardar el formulario._

---

### 91 Revisar y Crear en SAP

- Marcar una de las opciones del campo ***Gestionar Datos de material en SAP*** .

> :information_source:  **Info**  
> _Con los anteriores pasos ya es posible guardar el formulario._

---

### 92 Aprobación Vicepresidencia o Sociedad

---


## 📝 Código

### getActividadesFlujoGenerables

### Definicion

Este método se encarga de validar las tareas que tengan algún campo parametrizado y en caso de que encuentre al menos un campo le inserta el valor “SI” al TAG de esa actividad en el flujo.

### Método C#

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



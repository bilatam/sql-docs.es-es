---
title: sys.dm_exec_query_optimizer_info (Transact-SQL) | Microsoft Docs
ms.custom: ''
ms.date: 03/15/2017
ms.prod: sql
ms.prod_service: database-engine, sql-database, sql-data-warehouse, pdw
ms.reviewer: ''
ms.suite: sql
ms.technology: system-objects
ms.tgt_pltfrm: ''
ms.topic: language-reference
f1_keywords:
- dm_exec_query_optimizer_info_TSQL
- dm_exec_query_optimizer_info
- sys.dm_exec_query_optimizer_info_TSQL
- sys.dm_exec_query_optimizer_info
dev_langs:
- TSQL
helpviewer_keywords:
- sys.dm_exec_query_optimizer_info dynamic management view
ms.assetid: 1d72cef1-22d8-4ae0-91db-6694fe918c9e
caps.latest.revision: 30
author: stevestein
ms.author: sstein
manager: craigg
monikerRange: '>=aps-pdw-2016||=azuresqldb-current||=azure-sqldw-latest||>=sql-server-2016||=sqlallproducts-allversions||>=sql-server-linux-2017'
ms.openlocfilehash: 282a55a0594a0d52a89066c997e6392bc8cc0dbb
ms.sourcegitcommit: 4cd008a77f456b35204989bbdd31db352716bbe6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/06/2018
ms.locfileid: "39557405"
---
# <a name="sysdmexecqueryoptimizerinfo-transact-sql"></a>sys.dm_exec_query_optimizer_info (Transact-SQL)
[!INCLUDE[tsql-appliesto-ss2008-all-md](../../includes/tsql-appliesto-ss2008-all-md.md)]

  Devuelve información estadística detallada acerca de la operación del optimizador de consultas de [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)]. Puede usar esta vista al optimizar una carga de trabajo para identificar los problemas o las mejoras de la optimización de consultas. Por ejemplo, puede usar el número total de optimizaciones, el valor de tiempo transcurrido y el valor del costo final para comparar las optimizaciones de las consultas de la carga de trabajo actual y los cambios observados durante el proceso de optimización. Algunos contadores proporcionan datos que sólo es relevantes para [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] uso interno de diagnóstico. Estos contadores se marcan como "Solo para uso interno".  
  
> [!NOTE]  
>  Para llamar a este método desde [!INCLUDE[ssSDWfull](../../includes/sssdwfull-md.md)] o [!INCLUDE[ssPDW](../../includes/sspdw-md.md)], utilice el nombre de **sys.dm_pdw_nodes_exec_query_optimizer_info**.  
  
|Nombre|Tipo de datos|Descripción|  
|----------|---------------|-----------------|  
|**Contador**|**nvarchar(4000)**|Nombre del evento de estadísticas del optimizador.|  
|**aparición**|**bigint**|Número de repeticiones del evento de optimización para este contador.|  
|**Valor**|**float**|Valor promedio de la propiedad por repetición del evento.|  
|**pdw_node_id**|**int**|**Se aplica a**: [!INCLUDE[ssSDWfull](../../includes/sssdwfull-md.md)], [!INCLUDE[ssPDW](../../includes/sspdw-md.md)]<br /><br /> El identificador para el nodo en esta distribución.|  
  
## <a name="permissions"></a>Permisos  

En [!INCLUDE[ssNoVersion_md](../../includes/ssnoversion-md.md)], requiere `VIEW SERVER STATE` permiso.   
En [!INCLUDE[ssSDS_md](../../includes/sssds-md.md)], requiere el `VIEW DATABASE STATE` permiso en la base de datos.   
    
## <a name="remarks"></a>Notas  
 **Sys.dm_exec_query_optimizer_info** contiene las siguientes propiedades (contadores). Todos los valores de repetición son acumulativos y se establecen en 0 cuando se reinicia el sistema. Todos los valores de los campos de valor se establecen en NULL cuando se reinicia el sistema. Todos los valores de columnas de valor que especifican un promedio utilizan el valor de repetición de la misma fila que el denominador en el cálculo del promedio. Todas las optimizaciones de consulta se miden al [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] determina cambios en **dm_exec_query_optimizer_info**, incluyendo ambas consultas generadas por usuario y sistema. Ejecución de un plan en caché ya no modifica valores en **dm_exec_query_optimizer_info**sólo son importantes optimizaciones.  
  
|Contador|Repetición|Valor|  
|-------------|----------------|-----------|  
|optimizations|Número total de optimizaciones.|No aplicable|  
|elapsed time|Número total de optimizaciones.|Tiempo promedio transcurrido por optimización de instrucción individual (consulta), en segundos.|  
|final cost|Número total de optimizaciones.|Costo promedio estimado para un plan optimizado en unidades de costo internas.|  
|trivial plan|Solo para uso interno|Solo para uso interno|  
|tareas|Solo para uso interno|Solo para uso interno|  
|no plan|Solo para uso interno|Solo para uso interno|  
|search 0|Solo para uso interno|Solo para uso interno|  
|search 0 time|Solo para uso interno|Solo para uso interno|  
|search 0 tasks|Solo para uso interno|Solo para uso interno|  
|search 1|Solo para uso interno|Solo para uso interno|  
|search 1 time|Solo para uso interno|Solo para uso interno|  
|search 1 tasks|Solo para uso interno|Solo para uso interno|  
|search 2|Solo para uso interno|Solo para uso interno|  
|search 2 time|Solo para uso interno|Solo para uso interno|  
|search 2 tasks|Solo para uso interno|Solo para uso interno|  
|gain stage 0 to stage 1|Solo para uso interno|Solo para uso interno|  
|gain stage 1 to stage 2|Solo para uso interno|Solo para uso interno|  
|timeout|Solo para uso interno|Solo para uso interno|  
|memory limit exceeded|Solo para uso interno|Solo para uso interno|  
|insert stmt|Número de optimizaciones que son para instrucciones INSERT.|No aplicable|  
|delete stmt|Número de optimizaciones que son para instrucciones DELETE.|No aplicable|  
|update stmt|Número de optimizaciones que son para instrucciones UPDATE.|No aplicable|  
|contains subquery|Número de optimizaciones de una consulta que contiene al menos una subconsulta.|No aplicable|  
|unnest failed|Solo para uso interno|Solo para uso interno|  
|tablas|Número total de optimizaciones.|Número promedio de tablas referenciadas por consulta optimizada.|  
|sugerencias|Número de veces que se ha especificado alguna sugerencia. Las sugerencias contadas incluyen: sugerencias de consulta JOIN, GROUP, UNION y FORCE ORDER, la opción de conjunto FORCE PLAN y las sugerencias de combinación.|No aplicable|  
|order hint|Número de veces que se ha especificado una sugerencia de orden forzada.|No aplicable|  
|join hint|Número de veces que una sugerencia de combinación ha forzado el algoritmo de combinación.|No aplicable|  
|view reference|Número de veces que se ha hecho referencia a una vista en una consulta|No aplicable|  
|remote query|Número de optimizaciones donde la consulta hacía referencia al menos a un origen de datos remoto, como una tabla con un nombre de cuatro partes o una salida de OPENROWSET.|No aplicable|  
|maximum DOP|Número total de optimizaciones.|Valor promedio de MAXDOP efectivo de un plan optimizado. De forma predeterminada, MAXDOP efectivo viene determinado por la **grado máximo de paralelismo** configuración de servidor opción y puede ser reemplazado para una consulta específica por el valor de la sugerencia de consulta MAXDOP.|  
|maximum recursion level|Número de optimizaciones en las que se ha especificado un nivel de MAXRECURSION mayor que 0 con la sugerencia de consulta.|Nivel promedio de MAXRECURSION en optimizaciones donde se ha especificado un nivel máximo de recursividad con la sugerencia de consulta.|  
|indexed views loaded|Solo para uso interno|Solo para uso interno|  
|indexed views matched|Número de optimizaciones donde han coincidido una o más vistas indizadas.|Número promedio de vistas coincidentes.|  
|indexed views used|Número de optimizaciones donde se han utilizado una o más vistas indizadas en el plan de salida después de la coincidencia.|Número promedio de vistas utilizadas.|  
|indexed views updated|Número de optimizaciones de una instrucción DML que producen un plan que mantiene una o más vistas indizadas.|Número promedio de vistas mantenidas.|  
|dynamic cursor request|Número de optimizaciones en las que se ha especificado una solicitud de cursor dinámico.|No aplicable|  
|fast forward cursor request|Número de optimizaciones en las que se ha especificado una solicitud de cursor de avance rápido.|No aplicable|  
|merge stmt|Número de optimizaciones que son para instrucciones MERGE.|No aplicable|  
  
## <a name="examples"></a>Ejemplos  
  
### <a name="a-viewing-statistics-on-optimizer-execution"></a>A. Ver estadísticas de la ejecución del optimizador  
 ¿Cuáles son las estadísticas de ejecución del optimizador actual para esta instancia de [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)]?  
  
```  
SELECT * FROM sys.dm_exec_query_optimizer_info;  
```  
  
### <a name="b-viewing-the-total-number-of-optimizations"></a>B. Ver el número total de optimizaciones  
 ¿Cuántas optimizaciones se realizan?  
  
```  
SELECT occurrence AS Optimizations FROM sys.dm_exec_query_optimizer_info  
WHERE counter = 'optimizations';  
```  
  
### <a name="c-average-elapsed-time-per-optimization"></a>C. Tiempo medio transcurrido por optimización  
 ¿Cuál es el tiempo promedio transcurrido por optimización?  
  
```  
SELECT ISNULL(value,0.0) AS ElapsedTimePerOptimization  
FROM sys.dm_exec_query_optimizer_info WHERE counter = 'elapsed time';  
```  
  
### <a name="d-fraction-of-optimizations-that-involve-subqueries"></a>D. Parte de las optimizaciones que afectan a subconsultas  
 ¿Qué fracción de las consultas optimizadas contenían una subconsulta?  
  
```  
SELECT (SELECT CAST (occurrence AS float) FROM sys.dm_exec_query_optimizer_info WHERE counter = 'contains subquery') /  
       (SELECT CAST (occurrence AS float)   
        FROM sys.dm_exec_query_optimizer_info WHERE counter = 'optimizations')  
        AS ContainsSubqueryFraction;  
```  
  
## <a name="see-also"></a>Vea también  
 [Funciones y vistas de administración dinámica &#40;Transact-SQL&#41;](~/relational-databases/system-dynamic-management-views/system-dynamic-management-views.md)   
 [Funciones y vistas de administración dinámica relacionadas con ejecuciones &#40;Transact-SQL&#41;](../../relational-databases/system-dynamic-management-views/execution-related-dynamic-management-views-and-functions-transact-sql.md)  
  
  



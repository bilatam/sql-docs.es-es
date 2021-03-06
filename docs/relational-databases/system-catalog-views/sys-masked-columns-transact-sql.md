---
title: Sys.masked_columns (Transact-SQL) | Documentos de Microsoft
ms.custom: ''
ms.date: 02/25/2016
ms.prod: sql
ms.prod_service: database-engine, sql-database
ms.component: system-catalog-views
ms.reviewer: ''
ms.suite: sql
ms.technology: system-objects
ms.tgt_pltfrm: ''
ms.topic: language-reference
f1_keywords:
- sys.masked_columns
- masked_columns_tsql
- sys.masked_columns_tsql
- masked_columns
helpviewer_keywords:
- sys.masked_columns catalog view
ms.assetid: 671577e4-d757-4b8d-9aa9-0fc8d51ea9ca
caps.latest.revision: 9
author: edmacauley
ms.author: edmaca
manager: craigg
monikerRange: =azuresqldb-current||>=sql-server-2016||=sqlallproducts-allversions||>=sql-server-linux-2017
ms.openlocfilehash: 64461261b624ace154376250419ec2e9a2f6ac89
ms.sourcegitcommit: 4cd008a77f456b35204989bbdd31db352716bbe6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/06/2018
ms.locfileid: "39558935"
---
# <a name="sysmaskedcolumns-transact-sql"></a>Sys.masked_columns (Transact-SQL)
[!INCLUDE[tsql-appliesto-ss2016-asdb-xxxx-xxx-md](../../includes/tsql-appliesto-ss2016-asdb-xxxx-xxx-md.md)]

  Utilice la **sys.masked_columns** ver para consultar columnas de la tabla que tienen un se les aplica la función de enmascaramiento de datos dinámicos. Esta vista se hereda de la vista **sys.columns** . Devuelve todas las columnas de la vista **sys.columns** , junto con las columnas **is_masked** y **masking_function** . Además, indica si estas están enmascaradas y, en caso afirmativo, qué función de enmascaramiento se ha definido. Esta vista solo muestra las columnas en las que se ha aplicado la función de enmascaramiento.  
  
|Nombre de columna|Tipo de datos|Descripción|  
|-----------------|---------------|-----------------|  
|object_id|**int**|Identificador del objeto al que pertenece esta columna.|  
|NAME|**sysname**|Nombre de la columna. Es único en el objeto.|  
|column_id|**int**|Identificador de la columna. Es único en el objeto.<br /><br /> Los Id. de columna no tienen que ser secuenciales.|  
|**Sys.masked_columns** devuelve muchas más columnas heredadas de **sys.columns**.|varios|Consulte [sys.columns &#40;Transact-SQL&#41; ](../../relational-databases/system-catalog-views/sys-columns-transact-sql.md) para obtener más definiciones de columna.|  
|is_masked|**bit**|Indica si la columna se enmascara. 1 indica enmascarado.|  
|masking_function|**nvarchar(4000)**|La función de enmascaramiento para la columna.|  
  
## <a name="remarks"></a>Notas  
  
## <a name="permissions"></a>Permisos  
 Esta vista devuelve información acerca de las tablas donde el usuario tiene algún tipo de permiso en la tabla o si el usuario tiene el permiso VIEW ANY DEFINITION.  
  
## <a name="example"></a>Ejemplo  
 La siguiente consulta combinaciones **sys.masked_columns** a **sys.tables** devolver información acerca de todos los enmascarados columnas.  
  
```  
SELECT tbl.name as table_name, c.name AS column_name, c.is_masked, c.masking_function  
FROM sys.masked_columns AS c  
JOIN sys.tables AS tbl   
    ON c.object_id = tbl.object_id  
WHERE is_masked = 1;  
```  
  
## <a name="see-also"></a>Vea también  
 [Enmascaramiento de datos dinámicos](../../relational-databases/security/dynamic-data-masking.md)   
 [sys.columns &#40;Transact-SQL&#41;](../../relational-databases/system-catalog-views/sys-columns-transact-sql.md)  
  
  

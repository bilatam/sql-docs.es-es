---
title: "CREAR el catálogo de texto completo (Transact-SQL) | Documentos de Microsoft"
ms.custom: 
ms.date: 03/14/2017
ms.prod: sql-non-specified
ms.reviewer: 
ms.suite: 
ms.technology:
- database-engine
ms.tgt_pltfrm: 
ms.topic: language-reference
f1_keywords:
- CATALOG_TSQL
- CREATE_FULLTEXT_TSQL
- FULLTEXT_TSQL
- FULLTEXT CATALOG
- CREATE FULLTEXT CATALOG
- CREATE_FULLTEXT_CATALOG_TSQL
- CATALOG
- FULLTEXT_CATALOG_TSQL
- CREATE FULLTEXT
- FULLTEXT
dev_langs:
- TSQL
helpviewer_keywords:
- full-text catalogs [SQL Server], creating
- CREATE FULLTEXT CATALOG statement
ms.assetid: d7a8bd93-e2d7-4a40-82ef-39069e65523b
caps.latest.revision: 60
author: BYHAM
ms.author: rickbyh
manager: jhubbard
ms.translationtype: MT
ms.sourcegitcommit: 876522142756bca05416a1afff3cf10467f4c7f1
ms.openlocfilehash: 303908a306661c764b9cd258147fcc911d2d3983
ms.contentlocale: es-es
ms.lasthandoff: 09/01/2017

---
# <a name="create-fulltext-catalog-transact-sql"></a>CREATE FULLTEXT CATALOG (Transact-SQL)
[!INCLUDE[tsql-appliesto-ss2008-asdb-xxxx-xxx_md](../../includes/tsql-appliesto-ss2008-asdb-xxxx-xxx-md.md)]

  Crea un catálogo de texto completo para una base de datos. Un catálogo de texto completo puede tener varios índices de texto completo, pero un índice de texto completo solo puede pertenecer a un catálogo de texto completo. Cada base de datos puede contener varios catálogos de texto completo o ninguno.  
  
 No se puede crear catálogos de texto completo en el **maestro**, **modelo**, o **tempdb** bases de datos.  
  
> [!IMPORTANT]  
>  A partir de [!INCLUDE[ssKatmai](../../includes/sskatmai-md.md)], un catálogo de texto completo es un objeto virtual y no pertenece a ningún grupo de archivos. Un catálogo de texto completo es un concepto lógico que hace referencia a un grupo de índices de texto completo.  
  
 ![Icono de vínculo de tema](../../database-engine/configure-windows/media/topic-link.gif "Icono de vínculo de tema") [Convenciones de sintaxis de Transact-SQL](../../t-sql/language-elements/transact-sql-syntax-conventions-transact-sql.md)  
  
## <a name="syntax"></a>Sintaxis  
  
```  
  
CREATE FULLTEXT CATALOG catalog_name  
     [ON FILEGROUP filegroup ]  
     [IN PATH 'rootpath']  
     [WITH <catalog_option>]  
     [AS DEFAULT]  
     [AUTHORIZATION owner_name ]  
  
<catalog_option>::=  
     ACCENT_SENSITIVITY = {ON|OFF}  
  
```  
  
## <a name="arguments"></a>Argumentos  
 *Catalog_Name*  
 Es el nombre del catálogo nuevo. El nombre del catálogo debe ser único en la base de datos actual. El nombre del archivo que corresponde al catálogo de texto completo (vea ON FILEGROUP) también debe ser único en la base de datos. Si la base de datos ya contiene un catálogo con el mismo nombre, [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] generará un error.  
  
 La longitud del nombre del catálogo no puede superar los 120 caracteres.  
  
 ON FILEGROUP *filegroup*  
 A partir de [!INCLUDE[ssKatmai](../../includes/sskatmai-md.md)], esta cláusula no tiene ningún efecto.  
  
 EN la ruta de acceso **'***ruta_raíz***'**  
 > [!NOTE]  
>  [!INCLUDE[ssNoteDepFutureAvoid](../../includes/ssnotedepfutureavoid-md.md)]  
  
 A partir de [!INCLUDE[ssKatmai](../../includes/sskatmai-md.md)], esta cláusula no tiene ningún efecto.  
  
 ACCENT_SENSITIVITY = {ON|OFF}   
 Especifica si el catálogo distingue los acentos para la indización de texto completo. Cuando se cambia esta propiedad, el índice debe volver a crearse. La opción predeterminada es utilizar la distinción de acentos que se haya especificado en la intercalación de base de datos. Para mostrar la intercalación de base de datos, use la **sys.databases** vista de catálogo.  
  
 Para determinar el valor de propiedad de distinción de acentos actual de un catálogo de texto completo, utilice la función FULLTEXTCATALOGPROPERTY con el **accentsensitivity** valor de propiedad en *catalog_name*. Si el valor devuelto es '1', el catálogo de texto completo distingue acentos; si el valor es '0', el catálogo no distingue acentos.  
  
 AS DEFAULT   
 Especifica que el catálogo es el predeterminado. Cuando se crean índices de texto completo sin especificar de forma explícita un catálogo de texto completo, se utiliza el catálogo predeterminado. Si un catálogo de texto completo existente ya se ha marcado como AS DEFAULT, configurar este nuevo catálogo como AS DEFAULT lo convertirá en el catálogo de texto completo predeterminado.  
  
 AUTORIZACIÓN *owner_name*  
 Establece el propietario del catálogo de texto completo en el nombre de un usuario o un rol de base de datos. Si *owner_name* es un rol, el rol debe ser el nombre de un rol que el usuario actual es un miembro de o el usuario que ejecuta la instrucción debe ser el propietario de la base de datos o el administrador del sistema.  
  
 Si *owner_name* es un nombre de usuario, el nombre de usuario debe ser uno de los siguientes:  
  
-   El nombre del usuario que ejecuta la instrucción.  
  
-   El nombre de un usuario para el que el usuario que está ejecutando el comando tiene permisos de suplantación.  
  
-   O bien, el usuario que ejecuta el comando debe ser el propietario de la base de datos o el administrador del sistema.  
  
 *owner_name* deben concederse el permiso TAKE OWNERSHIP en el catálogo de texto completo especificado.  
  
## <a name="remarks"></a>Comentarios  
 Los identificadores de los catálogos de texto completo comienzan por 00005 y se incrementan en uno con cada catálogo nuevo que se crea.  
  
## <a name="permissions"></a>Permissions  
 Usuario debe tener el permiso CREATE FULLTEXT CATALOG en la base de datos, o ser miembro de la **db_owner**, o **db_ddladmin** funciones fijas de base de datos.  
  
## <a name="examples"></a>Ejemplos  
 En el ejemplo siguiente se crea un catálogo de texto completo y un índice de texto completo.  
  
```  
USE AdventureWorks2012;  
GO  
CREATE FULLTEXT CATALOG ftCatalog AS DEFAULT;  
GO  
CREATE FULLTEXT INDEX ON HumanResources.JobCandidate(Resume) KEY INDEX PK_JobCandidate_JobCandidateID;  
GO  
```  
  
## <a name="see-also"></a>Vea también  
 [Sys.fulltext_catalogs &#40; Transact-SQL &#41;](../../relational-databases/system-catalog-views/sys-fulltext-catalogs-transact-sql.md)   
 [ALTER FULLTEXT CATALOG &#40;Transact-SQL&#41;](../../t-sql/statements/alter-fulltext-catalog-transact-sql.md)   
 [Eliminar catálogo de texto completo &#40; Transact-SQL &#41;](../../t-sql/statements/drop-fulltext-catalog-transact-sql.md)   
 [Búsqueda de texto completo](../../relational-databases/search/full-text-search.md)   
 [Nuevo catálogo de texto completo &#40; Página general &#41;](http://msdn.microsoft.com/library/5ed6f7cd-d9af-4439-9f33-fc935b883d91)  
  
  
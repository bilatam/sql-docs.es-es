---
title: Mostrar la información del espacio ocupado por los datos y el registro de una base de datos | Microsoft Docs
ms.custom: ''
ms.date: 06/13/2017
ms.prod: sql-server-2014
ms.reviewer: ''
ms.suite: ''
ms.technology:
- database-engine
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- logs [SQL Server], space
- status information [SQL Server], space
- displaying space information
- disk space [SQL Server], displaying
- databases [SQL Server], space used
- viewing space information
- space allocation [SQL Server], displaying
- data space [SQL Server]
ms.assetid: c7b99463-4bab-4e9b-9217-fcb0898dc757
caps.latest.revision: 26
author: craigg-msft
ms.author: craigg
manager: jhubbard
ms.openlocfilehash: 402c584681d84b68361800999252e00baa918703
ms.sourcegitcommit: 5dd5cad0c1bbd308471d6c885f516948ad67dfcf
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2018
ms.locfileid: "36106097"
---
# <a name="display-data-and-log-space-information-for-a-database"></a>Mostrar la información del espacio ocupado por los datos y el registro de una base de datos
  En este tema se describe cómo mostrar la información del espacio ocupado por los datos y el registro de una base de datos en [!INCLUDE[ssCurrent](../../includes/sscurrent-md.md)] mediante [!INCLUDE[ssManStudioFull](../../includes/ssmanstudiofull-md.md)] o [!INCLUDE[tsql](../../includes/tsql-md.md)].  
  
 **En este tema**  
  
-   **Antes de empezar:**  
  
     [Seguridad](#Security)  
  
-   **Para mostrar datos y el registro de información del espacio de una base de datos, utilizando:**  
  
     [SQL Server Management Studio](#SSMSProcedure)  
  
     [Transact-SQL](#TsqlProcedure)  
  
##  <a name="BeforeYouBegin"></a> Antes de empezar  
  
###  <a name="Security"></a> Seguridad  
  
####  <a name="Permissions"></a> Permissions  
 El permiso para ejecutar **sp_spaceused** se otorga al rol **public** . Solo los miembros del rol fijo de base de datos **db_owner** pueden especificar el parámetro **@updateusage** .  
  
##  <a name="SSMSProcedure"></a> Usar SQL Server Management Studio  
  
#### <a name="to-display-data-and-log-space-information-for-a-database"></a>Para mostrar la información del espacio ocupado por los datos y el registro de una base de datos  
  
1.  En el Explorador de objetos, conéctese a una instancia de [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] y expándala.  
  
2.  Expanda **Bases de datos**.  
  
3.  Haga clic con el botón derecho en una base de datos, seleccione **Informes**e **Informes estándar**y, luego, haga clic en **Uso de disco**.  
  
##  <a name="TsqlProcedure"></a> Usar Transact-SQL  
  
#### <a name="to-display-data-and-log-space-information-for-a-database-by-using-spspaceused"></a>Para mostrar la información del espacio ocupado por los datos y el registro de una base de datos mediante sp_spaceused  
  
1.  Conéctese con el [!INCLUDE[ssDE](../../includes/ssde-md.md)].  
  
2.  En la barra Estándar, haga clic en **Nueva consulta**.  
  
3.  Copie y pegue el siguiente ejemplo en la ventana de consulta y haga clic en **Ejecutar**. En este ejemplo se usa el procedimiento almacenado del sistema [sp_spaceused](/sql/relational-databases/system-stored-procedures/sp-spaceused-transact-sql) para notificar información de espacio en disco para la tabla `Vendor` y sus índices.  
  
```tsql  
USE AdventureWorks2012;  
GO  
EXEC sp_spaceused N'Purchasing.Vendor';  
GO  
```  
  
#### <a name="to-display-data-and-log-space-information-for-a-database-by-querying-sysdatabasefiles"></a>Para mostrar la información del espacio ocupado por los datos y el registro de una base de datos mediante una consulta a sys.database_files  
  
1.  Conéctese con el [!INCLUDE[ssDE](../../includes/ssde-md.md)].  
  
2.  En la barra Estándar, haga clic en **Nueva consulta**.  
  
3.  Copie y pegue el siguiente ejemplo en la ventana de consulta y haga clic en **Ejecutar**. En este ejemplo se consulta la vista de catálogo [sys.database_files](/sql/relational-databases/system-catalog-views/sys-database-files-transact-sql) para devolver información específica sobre los archivos de datos y de registro de la base de datos [!INCLUDE[ssSampleDBobject](../../includes/sssampledbobject-md.md)] .  
  
```tsql  
USE AdventureWorks2012;  
GO  
SELECT file_id, name, type_desc, physical_name, size, max_size  
FROM sys.database_files ;  
GO  
  
```  
  
## <a name="see-also"></a>Vea también  
 [SELECT &#40;Transact-SQL&#41;](/sql/t-sql/queries/select-transact-sql)   
 [sys.database_files &#40;Transact-SQL&#41;](/sql/relational-databases/system-catalog-views/sys-database-files-transact-sql)   
 [sp_spaceused &#40;Transact-SQL&#41;](/sql/relational-databases/system-stored-procedures/sp-spaceused-transact-sql)   
 [Agregar archivos de datos o de registro a una base de datos](add-data-or-log-files-to-a-database.md)   
 [Eliminar archivos de datos o de registro de una base de datos](delete-data-or-log-files-from-a-database.md)  
  
  
---
title: Creación de una tabla para almacenar datos FILESTREAM | Microsoft Docs
ms.custom: ''
ms.date: 03/14/2017
ms.prod: sql
ms.prod_service: database-engine
ms.reviewer: ''
ms.suite: sql
ms.technology: filestream
ms.tgt_pltfrm: ''
ms.topic: conceptual
helpviewer_keywords:
- FILESTREAM [SQL Server], table storage
ms.assetid: 029c3059-5c83-43e2-a859-9027031b7de1
caps.latest.revision: 16
author: douglaslMS
ms.author: douglasl
manager: craigg
ms.openlocfilehash: 5bcc013fc397d9b512aad37af8bf4aee988780f0
ms.sourcegitcommit: abd71294ebc39695d403e341c4f77829cb4166a8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "36886601"
---
# <a name="create-a-table-for-storing-filestream-data"></a>Crear una tabla para almacenar datos FILESTREAM
[!INCLUDE[appliesto-ss-xxxx-xxxx-xxx-md](../../includes/appliesto-ss-xxxx-xxxx-xxx-md.md)]
  En este tema se muestra cómo crear una tabla para almacenar datos FILESTREAM.  
  
 Cuando la base de datos tiene un grupo de archivos FILESTREAM, es posible crear o modificar tablas para almacenar datos FILESTREAM. Para especificar que una columna contiene datos FILESTREAM, se debe crear una columna **varbinary(max)** y agregar el atributo FILESTREAM.  
  
### <a name="to-create-a-table-to-store-filestream-data"></a>Para crear una tabla para almacenar datos FILESTREAM  
  
1.  En [!INCLUDE[ssManStudioFull](../../includes/ssmanstudiofull-md.md)], haga clic en **Nueva consulta** para mostrar el Editor de consultas.  
  
2.  Copie el código [!INCLUDE[tsql](../../includes/tsql-md.md)] del ejemplo siguiente en el Editor de consultas. Este código [!INCLUDE[tsql](../../includes/tsql-md.md)] crea una tabla habilitada para FILESTREAM denominada Records.  
  
3.  Para crear la tabla, haga clic en **Ejecutar**.  
  
## <a name="example"></a>Ejemplo  
 En el siguiente ejemplo de código se muestra cómo crear una tabla denominada `Records`. La columna `Id` es una columna `ROWGUIDCOL` y es necesaria para usar datos FILESTREAM con las API de Win32. La columna `SerialNumber` es una columna `UNIQUE INTEGER`. La columna `Chart` es una columna `FILESTREAM` y se usa para almacenar `Chart` en el sistema de archivos.  
  
> [!NOTE]  
>  En este ejemplo se hace referencia a la base de datos de archivo que se creó en [Crear una base de datos habilitada para FILESTREAM](../../relational-databases/blob/create-a-filestream-enabled-database.md).  
  
 [!code-sql[FILESTREAM#FS_CreateTable](../../relational-databases/blob/codesnippet/tsql/create-a-table-for-stori_1.sql)]  
  
## <a name="see-also"></a>Ver también  
 [CREATE TABLE &#40;Transact-SQL&#41;](../../t-sql/statements/create-table-transact-sql.md)   
 [ALTER TABLE &#40;Transact-SQL&#41;](../../t-sql/statements/alter-table-transact-sql.md)  
  
  

---
title: Resultados de los mensajes SQL Server | Microsoft Docs
description: resultados de los mensajes de SQL Server
ms.custom: ''
ms.date: 06/14/2018
ms.prod: sql
ms.prod_service: database-engine, sql-database, sql-data-warehouse, pdw
ms.component: oledb|ole-db-errors
ms.reviewer: ''
ms.suite: sql
ms.technology: connectivity
ms.tgt_pltfrm: ''
ms.topic: reference
helpviewer_keywords:
- OLE DB Driver for SQL Server, errors
- errors [OLE DB], SQL Server message results
- OLE DB error handling, SQL Server message results
author: pmasl
ms.author: Pedro.Lopes
manager: craigg
ms.openlocfilehash: 98d04b56c6e1709e629be46ad00fd3f7b8007a5b
ms.sourcegitcommit: 50838d7e767c61dd0b5e677b6833dd5c139552f2
ms.translationtype: MTE75
ms.contentlocale: es-ES
ms.lasthandoff: 07/18/2018
ms.locfileid: "39106001"
---
# <a name="sql-server-message-results"></a>Resultados de los mensajes de SQL Server
[!INCLUDE[appliesto-ss-asdb-asdw-pdw-md](../../../includes/appliesto-ss-asdb-asdw-pdw-md.md)]

[!INCLUDE[Driver_OLEDB_Download](../../../includes/driver_oledb_download.md)]

  Las instrucciones [!INCLUDE[tsql](../../../includes/tsql-md.md)] siguientes no generan conjuntos de filas del controlador OLE DB para SQL Server ni un recuento de filas afectadas al ejecutarse:  
  
-   PRINT  
  
-   RAISERROR con una gravedad de 10 o inferior  
  
-   DBCC  
  
-   SET SHOWPLAN  
  
-   SET STATISTICS  
  
 Estas instrucciones devuelven uno o varios mensajes informativos o hacen que [!INCLUDE[ssNoVersion](../../../includes/ssnoversion-md.md)] devuelva mensajes informativos en lugar de resultados de conjunto de filas o de recuento. En la ejecución correcta, el controlador OLE DB para SQL Server devuelve S_OK y los mensajes están disponibles para el controlador OLE DB para el consumidor de SQL Server.  
  
 El controlador OLE DB para SQL Server devuelve S_OK y tiene uno o más mensajes informativos disponibles después de la ejecución de muchas [!INCLUDE[tsql](../../../includes/tsql-md.md)] instrucciones o la ejecución del consumidor de un controlador de OLE DB para la función de miembro de SQL Server.  
  
 El consumidor del controlador OLE DB para SQL Server que permite la especificación dinámica de texto de consulta debe comprobar las interfaces de error después de cada ejecución de una función de miembro independientemente del valor del código de retorno, la presencia o ausencia de una referencia de interfaz **IRowset** o **IMultipleResults** devuelta o un recuento de filas afectadas.  
  
## <a name="see-also"></a>Ver también  
 [Errores](../../oledb/ole-db-errors/errors.md)  
  
  

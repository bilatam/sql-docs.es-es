---
title: SQLSTATE (códigos de Error ODBC) | Documentos de Microsoft
ms.custom: ''
ms.date: 03/14/2017
ms.prod: sql
ms.prod_service: database-engine, sql-database, sql-data-warehouse, pdw
ms.reviewer: ''
ms.suite: sql
ms.technology: native-client
ms.tgt_pltfrm: ''
ms.topic: reference
helpviewer_keywords:
- SQL Server Native Client ODBC driver, errors
- ODBC error handling, cause information
- messages [ODBC], cause information
- SQLSTATEs
- errors [ODBC], cause information
ms.assetid: 84cce528-edb0-473f-a85f-3eb87fbe2cf3
author: MightyPen
ms.author: genemi
manager: craigg
monikerRange: '>=aps-pdw-2016||=azuresqldb-current||=azure-sqldw-latest||>=sql-server-2016||=sqlallproducts-allversions||>=sql-server-linux-2017'
ms.openlocfilehash: 1f01ebc913c44f1641096dc7dabfc0665711d93a
ms.sourcegitcommit: 4cd008a77f456b35204989bbdd31db352716bbe6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/06/2018
ms.locfileid: "39542045"
---
# <a name="sqlstate-odbc-error-codes"></a>SQLSTATE (códigos de error ODBC)
[!INCLUDE[appliesto-ss-asdb-asdw-pdw-md](../../includes/appliesto-ss-asdb-asdw-pdw-md.md)]
[!INCLUDE[SNAC_Deprecated](../../includes/snac-deprecated.md)]

  SQLSTATE proporciona información detallada sobre la causa de una advertencia o error. Errores que se producen en los datos de origen que detecta y devuelve [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)], el [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] controlador ODBC de Native Client asigna el número de error nativo devuelto al SQLSTATE correspondiente. Si un número de error nativo no tiene un código de error ODBC para asignar a, el [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] controlador ODBC de Native Client devuelve SQLSTATE 42000 ("sintaxis o infracción de acceso"). Para los errores detectados por el controlador, el [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] controlador ODBC de Native Client genera el SQLSTATE correspondiente.  
  
 Para obtener más información sobre los códigos de error de estado, vea los temas siguientes:  
  
-   [Apéndice A: Códigos de error ODBC ](http://go.microsoft.com/fwlink/?LinkId=89356)  
  
-   [Asignaciones SQLSTATE](http://go.microsoft.com/fwlink/?LinkId=89355)  
  
## <a name="see-also"></a>Vea también  
 [Controlar errores y mensajes](../../relational-databases/native-client-odbc-error-messages/handling-errors-and-messages.md)  
  
  

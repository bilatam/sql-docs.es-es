---
title: Usar puntos de retorno | Microsoft Docs
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.suite: sql
ms.technology: connectivity
ms.tgt_pltfrm: ''
ms.topic: conceptual
ms.assetid: 3b48eb13-32ef-4fb3-8e95-dbc9468c9a44
caps.latest.revision: 19
author: MightyPen
ms.author: genemi
manager: craigg
ms.openlocfilehash: 125c15caac95f152c6f5009b1a794bd0fb625a2c
ms.sourcegitcommit: 2f9cafc1d7a3773a121bdb78a095018c8b7c149f
ms.translationtype: MTE75
ms.contentlocale: es-ES
ms.lasthandoff: 08/08/2018
ms.locfileid: "39661867"
---
# <a name="using-savepoints"></a>Usar puntos de retorno

[!INCLUDE[Driver_JDBC_Download](../../includes/driver_jdbc_download.md)]

Los puntos de retorno ofrecen un mecanismo para revertir partes de una transacción. En [!INCLUDE[ssNoVersion](../../includes/ssnoversion_md.md)], puede crear un punto de retorno con la instrucción SAVE TRANSACTION savepoint_name. Más adelante, ejecute una instrucción ROLLBACK TRANSACTION savepoint_name para revertir al punto de retorno en vez de revertir al inicio de la transacción.

Los puntos de retorno son útiles en situaciones en que no es probable que se produzcan errores. El uso de un punto de retorno para revertir parte de una transacción, en caso de producirse un error no frecuente, puede resultar más eficaz que hacer que cada transacción pruebe si una actualización es válida antes de realizarla. Las operaciones de actualización y reversión son costosas, por lo que los puntos de retorno solamente son eficaces si la probabilidad de encontrar un error es baja y el costo de comprobar de antemano la validez de una actualización es relativamente alto.

El [!INCLUDE[jdbcNoVersion](../../includes/jdbcnoversion_md.md)] admite el uso de puntos de retorno mediante el método [setSavepoint](../../connect/jdbc/reference/setsavepoint-method-sqlserverconnection.md) de la clase [SQLServerConnection](../../connect/jdbc/reference/sqlserverconnection-class.md). Con el método setSavepoint, puede crear un punto de retorno con o sin nombre en la transacción actual y el método devolverá un objeto [SQLServerSavepoint](../../connect/jdbc/reference/sqlserversavepoint-class.md). Se pueden crear varios puntos de retorno en una transacción. Para revertir una transacción a un punto de retorno determinado, puede pasar el objeto SQLServerSavepoint al método [rollback (java.sql.Savepoint)](../../connect/jdbc/reference/rollback-method-java-sql-savepoint.md).

En el siguiente ejemplo, se usa un punto de retorno a la vez que se realiza una transacción local consistente en dos instrucciones independientes del bloque `try`. Las instrucciones se ejecutan en la tabla Production.ScrapReason en la base de datos de ejemplo de [!INCLUDE[ssSampleDBnormal](../../includes/sssampledbnormal_md.md)] y se usa un punto de retorno para revertir la segunda instrucción. Como resultado, solo se confirma en la base de datos la primera instrucción.

[!code[JDBC#UsingSavepoints1](../../connect/jdbc/codesnippet/Java/using-savepoints_1.java)]

## <a name="see-also"></a>Ver también

[Realizar transacciones con el controlador JDBC](../../connect/jdbc/performing-transactions-with-the-jdbc-driver.md)

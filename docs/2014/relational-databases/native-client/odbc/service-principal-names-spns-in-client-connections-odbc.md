---
title: Nombres de entidad de servicio (SPN) en conexiones de cliente (ODBC) | Microsoft Docs
ms.custom: ''
ms.date: 06/13/2017
ms.prod: sql-server-2014
ms.reviewer: ''
ms.suite: ''
ms.technology: native-client  - "database-engine" - "docset-sql-devref"
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 1d60cb30-4c46-49b2-89ab-701e77a330a2
caps.latest.revision: 14
author: MightyPen
ms.author: genemi
manager: craigg
ms.openlocfilehash: 92231cca501a2b1d79a3c4a2cdbf15f1310af904
ms.sourcegitcommit: f8ce92a2f935616339965d140e00298b1f8355d7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/03/2018
ms.locfileid: "37423002"
---
# <a name="service-principal-names-spns-in-client-connections-odbc"></a>Nombres de entidad de seguridad del servicio (SPN) en conexiones de cliente (ODBC)
  En este tema se describen las funciones y atributos ODBC que admiten nombres principales de servicio (SPN) en aplicaciones cliente. Para obtener más información acerca de los SPN en aplicaciones cliente, consulte [nombre Principal de servicio &#40;SPN&#41; compatibilidad en las conexiones de cliente](../features/service-principal-name-spn-support-in-client-connections.md) y [obtener la autenticación mutua de Kerberos](../../native-client-odbc-how-to/get-mutual-kerberos-authentication.md).  
  
## <a name="connection-string-keywords"></a>Palabras clave de cadena de conexión  
 Las siguientes palabras clave de cadena de conexión permiten a las aplicaciones cliente especificar un SPN.  
  
|Palabra clave|Valor|  
|-------------|-----------|  
|`ServerSPN`|SPN del servidor. El valor predeterminado es una cadena vacía, que hace que [!INCLUDE[ssNoVersion](../../../includes/ssnoversion-md.md)] Native Client use el valor predeterminado, SPN generado por controlador.|  
|`FailoverPartnerSPN`|SPN del asociado de conmutación por error. El valor predeterminado es una cadena vacía, que hace que [!INCLUDE[ssNoVersion](../../../includes/ssnoversion-md.md)] Native Client use el valor predeterminado, SPN generado por controlador.|  
  
## <a name="connection-attributes"></a>Atributos de conexión  
 Los siguientes atributos de conexión permiten que las aplicaciones cliente especifiquen un SPN y consulten el método de autenticación.  
  
|Nombre|Tipo|Uso|  
|----------|----------|-----------|  
|SQL_COPT_SS_SERVER_SPN<br /><br /> SQL_COPT_SS_FAILOVER_PARTNER_SPN|SQLTCHAR, lectura/escritura|Especifica el SPN del servidor. El valor predeterminado es una cadena vacía, que hace que [!INCLUDE[ssNoVersion](../../../includes/ssnoversion-md.md)] Native Client use el valor predeterminado, SPN generado por controlador.<br /><br /> Este atributo solo podrá consultarse una vez que se haya establecido mediante programación o una vez que se haya abierto una conexión. Si se intenta consultar este atributo en una conexión que no está abierta y el atributo no se ha establecido mediante programación, se devuelve SQL_ERROR y se registra un error de diagnóstico con SQLState 08003 y el mensaje "Conexión no abierta".<br /><br /> Si se intenta establecer este atributo cuando hay una conexión abierta, se devuelve SQL_ERROR y se registra un error de diagnóstico con SQLState HY011 y el mensaje "Operación no válido en este momento".|  
|SQL_COPT_SS_INTEGRATED_AUTHENTICATION_METHOD|SQLTCHAR, solo lectura|Devuelve el método de autenticación que utiliza la conexión. El valor devuelto a la aplicación es el valor que Windows devuelve a [!INCLUDE[ssNoVersion](../../../includes/ssnoversion-md.md)] Native Client. Los valores posibles son:<br /><br /> -"NTLM", que se devuelve cuando se abre una conexión mediante la autenticación NTLM.<br />-"Kerberos", que se devuelve cuando se abre una conexión mediante la autenticación Kerberos.<br /><br /> Este atributo solamente puede leerse para una conexión abierta que use la autenticación de Windows. Si se intenta leer antes de que se haya abierto una conexión, se devuelve SQL_ERROR y se registra un error con SQLState 08003 y el mensaje "Conexión no abierta".<br /><br /> Si este atributo se consulta en una conexión que no utilizó la autenticación de Windows, se devuelve SQL_ERROR y se registra un error con SQLState HY092 y el mensaje "Identificador de opción/atributo no válido (SQL_COPT_SS_INTEGRATED_AUTHENTICATION_METHOD solamente está disponible para conexiones de confianza)".<br /><br /> Si no puede determinarse el método de autenticación, se devuelve SQL_ERROR y se registra un error con SQLState HY000 y el mensaje "Error general".|  
|SQL_COPT_SS_MUTUALLY_AUTHENTICATED|SQLSMALLINT, solo lectura|Devuelve SQL_TRUE si el servidor de la conexión se autenticó mutuamente; de lo contrario, devuelve SQL_FALSE.<br /><br /> Este atributo solamente puede leerse para una conexión abierta. Si se intenta leer antes de que se haya abierto una conexión, se devuelve SQL_ERROR y se registra un error con SQLState 08003 y el mensaje "Conexión no abierta".<br /><br /> Si este atributo se consulta para una conexión que no usó la autenticación de Windows, se devuelve SQL_FALSE.|  
  
## <a name="odbc-function-support-for-specifying-spns"></a>Compatibilidad con la función ODBC para especificar SPN  
 Las siguientes funciones ODBC admiten aplicaciones cliente y SPN:  
  
-   [SQLBrowseConnect](../../native-client-odbc-api/sqlbrowseconnect.md)  
  
-   [SQLConnect](../../native-client-odbc-api/sqlconnect.md)  
  
-   [SQLDriverConnect](../../native-client-odbc-api/sqldriverconnect.md)  
  
-   [SQLGetConnectAttr](../../native-client-odbc-api/sqlgetconnectattr.md)  
  
-   [SQLSetConnectAttr](../../native-client-odbc-api/sqlsetconnectattr.md)  
  
## <a name="see-also"></a>Vea también  
 [SQL Server Native Client &#40;ODBC&#41;](sql-server-native-client-odbc.md)  
  
  

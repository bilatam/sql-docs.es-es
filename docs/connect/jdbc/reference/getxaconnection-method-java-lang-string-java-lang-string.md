---
title: getXAConnection (método) (java.lang.String, java.lang.String) | Documentos de Microsoft
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.suite: sql
ms.technology: connectivity
ms.tgt_pltfrm: ''
ms.topic: conceptual
apiname:
- SQLServerXADataSource.getXAConnection (java.lang.String, java.lang.String)
apilocation:
- sqljdbc.jar
apitype: Assembly
ms.assetid: 276e0093-3d42-4f73-acc4-2b5b98245b40
caps.latest.revision: 9
author: MightyPen
ms.author: genemi
manager: craigg
ms.openlocfilehash: 8aec959822b00c79031226aaccbaf0085f68f79d
ms.sourcegitcommit: 1740f3090b168c0e809611a7aa6fd514075616bf
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/03/2018
ms.locfileid: "32839330"
---
# <a name="getxaconnection-method-javalangstring-javalangstring"></a>Método getXAConnection (java.lang.String, java.lang.String)
[!INCLUDE[Driver_JDBC_Download](../../../includes/driver_jdbc_download.md)]

  Intenta establecer una conexión a bases de datos física mediante el nombre de usuario y contraseña especificados.  
  
## <a name="syntax"></a>Sintaxis  
  
```  
  
public javax.sql.XAConnection getXAConnection(java.lang.String user,  
                                              java.lang.String password)  
```  
  
#### <a name="parameters"></a>Parámetros  
 *user*  
  
 A **cadena** que contiene el nombre de usuario.  
  
 *password*  
  
 A **cadena** que contiene la contraseña.  
  
## <a name="return-value"></a>Valor devuelto  
 Un objeto XAConnection.  
  
## <a name="exceptions"></a>Excepciones  
 java.sql.SQLException  
  
## <a name="remarks"></a>Comentarios  
 Este método getXAConnection especificado por el método getXAConnection en la interfaz javax.sql.XADataSource.  
  
> [!NOTE]  
>  Las implementaciones del grupo de conexiones XA, y no los códigos de aplicación JDBC, llaman normalmente a este método.  
  
## <a name="see-also"></a>Vea también  
 [Método getXAConnection &#40;SQLServerXADataSource&#41;](../../../connect/jdbc/reference/getxaconnection-method-sqlserverxadatasource.md)   
 [Métodos SQLServerXADataSource](../../../connect/jdbc/reference/sqlserverxadatasource-methods.md)   
 [Miembros de SQLServerXADataSource](../../../connect/jdbc/reference/sqlserverxadatasource-members.md)   
 [Clase SQLServerXADataSource](../../../connect/jdbc/reference/sqlserverxadatasource-class.md)  
  
  

---
title: Método (java.io.InputStream) updateAsciiStream | Microsoft Docs
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.suite: sql
ms.technology: connectivity
ms.tgt_pltfrm: ''
ms.topic: conceptual
ms.assetid: 1dcc3d4f-ae30-45c0-afad-a531358807af
caps.latest.revision: 18
author: MightyPen
ms.author: genemi
manager: craigg
ms.openlocfilehash: a98f78397a2bd9b86b788c696ad13c11f5e9dbe9
ms.sourcegitcommit: e77197ec6935e15e2260a7a44587e8054745d5c2
ms.translationtype: MTE75
ms.contentlocale: es-ES
ms.lasthandoff: 07/11/2018
ms.locfileid: "38020163"
---
# <a name="updateasciistream-method-int-javaioinputstream"></a>Método updateAsciiStream (int, java.io.InputStream)
[!INCLUDE[Driver_JDBC_Download](../../../includes/driver_jdbc_download.md)]

  Actualiza la columna designada con un valor de flujo ASCII.  
  
## <a name="syntax"></a>Sintaxis  
  
```  
  
public void updateAsciiStream(int columnIndex,  
                              java.io.InputStream x)  
```  
  
#### <a name="parameters"></a>Parámetros  
 *columnIndex*  
  
 Valor **int** que indica el índice de columna.  
  
 *x*  
  
 Un objeto InputStream.  
  
## <a name="exceptions"></a>Excepciones  
 [SQLServerException](../../../connect/jdbc/reference/sqlserverexception-class.md)  
  
## <a name="remarks"></a>Notas  
 Este método updateAsciiStream especificado por el método updateAsciiStream en la interfaz java.sql.ResultSet.  
  
 Este método pasa caracteres ASCII (bytes) desde un objeto InputStream a las columnas de caracteres convertibles, que son el rango ASCII [0x00 - 0x7F] de Unicode y las páginas de códigos 874, 932, 936, 949, 950 y desde la 1250 a la 1258. Este método realiza una conversión en la página de intercalación de destino. Si se intenta actualizar una columna de destino no convertible se producirá una excepción. Para las columnas binarias, se pasan bytes sin formato.  
  
 Con este método para el **imagen**, **texto**, y **ntext** [!INCLUDE[ssNoVersion](../../../includes/ssnoversion_md.md)] tipos de datos podrían afectar al rendimiento.  
  
## <a name="see-also"></a>Ver también  
 [Método updateAsciiStream &#40;SQLServerResultSet&#41;](../../../connect/jdbc/reference/updateasciistream-method-sqlserverresultset.md)   
 [Miembros SQLServerResultSet](../../../connect/jdbc/reference/sqlserverresultset-members.md)   
 [Clase SQLServerResultSet](../../../connect/jdbc/reference/sqlserverresultset-class.md)  
  
  

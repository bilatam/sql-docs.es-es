---
title: 'Cómo: Recuperar datos binarios como un flujo mediante el controlador SQLSRV | Microsoft Docs'
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.suite: sql
ms.technology: connectivity
ms.tgt_pltfrm: ''
ms.topic: conceptual
helpviewer_keywords:
- retrieving data, as a binary stream
- streaming data
ms.assetid: cd8d6382-abe6-48ee-9d10-4e6c52c0cb9a
caps.latest.revision: 21
author: MightyPen
ms.author: genemi
manager: craigg
ms.openlocfilehash: d10cc259971d2a81177ee8e04844a54b26cf147c
ms.sourcegitcommit: e77197ec6935e15e2260a7a44587e8054745d5c2
ms.translationtype: MTE75
ms.contentlocale: es-ES
ms.lasthandoff: 07/11/2018
ms.locfileid: "37979842"
---
# <a name="how-to-retrieve-binary-data-as-a-stream-using-the-sqlsrv-driver"></a>Cómo recuperar datos binarios como una secuencia mediante el controlador SQLSRV
[!INCLUDE[Driver_PHP_Download](../../includes/driver_php_download.md)]

La recuperación de datos como un flujo solo está disponible en el controlador SQLSRV de [!INCLUDE[ssDriverPHP](../../includes/ssdriverphp_md.md)], pero no en el controlador PDO_SQLSRV.  
  
Los [!INCLUDE[ssDriverPHP](../../includes/ssdriverphp_md.md)] aprovechan las ventajas de las secuencias de PHP para recuperar grandes cantidades de datos binarios del servidor. En este tema se muestra cómo recuperar datos binarios como una secuencia.  
  
Al utilizar las secuencias para recuperar datos binarios, como las imágenes, se evita tener que consumir una gran cantidad de memoria de script, ya que se recuperan los fragmentos de datos en lugar de cargar el objeto entero en la memoria de script.  
  
## <a name="example"></a>Ejemplo  
En el ejemplo siguiente se recuperan datos binarios (en este caso, una imagen) de la tabla *Production.ProductPhoto* de la base de datos de AdventureWorks. La imagen se recupera como una secuencia y se muestra en el explorador.  
  
El proceso de recuperación de los datos de la imagen como una secuencia se realiza utilizando [sqlsrv_fetch](../../connect/php/sqlsrv-fetch.md) y [sqlsrv_get_field](../../connect/php/sqlsrv-get-field.md) con el tipo de valor devuelto como una secuencia binaria. El tipo de valor devuelto se especifica mediante la constante **SQLSRV_PHPTYPE_STREAM**. Para obtener información sobre las constantes **sqlsrv**, vea [Constantes &#40;controladores de Microsoft para PHP para SQL Server&#41;](../../connect/php/constants-microsoft-drivers-for-php-for-sql-server.md).  
  
En el ejemplo se da por hecho que SQL Server y la base de datos [AdventureWorks](https://github.com/Microsoft/sql-server-samples/tree/master/samples/databases/adventure-works) están instalados en el equipo local. Los resultados se agregan al explorador cuando se ejecuta el ejemplo en el explorador.  
  
```  
<?php  
/* Connect to the local server using Windows Authentication and  
specify the AdventureWorks database as the database in use. */  
$serverName = "(local)";  
$connectionInfo = array( "Database"=>"AdventureWorks");  
$conn = sqlsrv_connect( $serverName, $connectionInfo);  
if( $conn === false )  
{  
     echo "Could not connect.\n";  
     die( print_r( sqlsrv_errors(), true));  
}  
  
/* Set up the Transact-SQL query. */  
$tsql = "SELECT LargePhoto   
         FROM Production.ProductPhoto   
         WHERE ProductPhotoID = ?";  
  
/* Set the parameter values and put them in an array. */  
$productPhotoID = 70;  
$params = array( $productPhotoID);  
  
/* Execute the query. */  
$stmt = sqlsrv_query($conn, $tsql, $params);  
if( $stmt === false )  
{  
     echo "Error in statement execution.</br>";  
     die( print_r( sqlsrv_errors(), true));  
}  
  
/* Retrieve and display the data.  
The return data is retrieved as a binary stream. */  
if ( sqlsrv_fetch( $stmt ) )  
{  
   $image = sqlsrv_get_field( $stmt, 0,   
                      SQLSRV_PHPTYPE_STREAM(SQLSRV_ENC_BINARY));  
   header("Content-Type: image/jpg");  
   fpassthru($image);  
}  
else  
{  
     echo "Error in retrieving data.</br>";  
     die(print_r( sqlsrv_errors(), true));  
}  
  
/* Free statement and connection resources. */  
sqlsrv_free_stmt( $stmt);  
sqlsrv_close( $conn);  
?>  
```  
  
Al especificar el tipo de valor devuelto en el ejemplo, se demuestra cómo especificar el tipo de valor devuelto PHP como una secuencia binaria. Técnicamente, no es necesario en el ejemplo, ya que el campo *LargePhoto* tiene el tipo de SQL Server varbinary(max) y, por tanto, se devuelve como un flujo binario de manera predeterminada. Para obtener información sobre los tipos de datos PHP predeterminados, consulte [Default PHP Data Types](../../connect/php/default-php-data-types.md). Para obtener información sobre cómo especificar los tipos de valor devueltos PHP, consulte [How to: Specify PHP Data Types](../../connect/php/how-to-specify-php-data-types.md).  
  
## <a name="see-also"></a>Ver también  
[Recuperación de datos](../../connect/php/retrieving-data.md)

[Recuperación de datos como una secuencia con el controlador SQLSRV](../../connect/php/retrieving-data-as-a-stream-using-the-sqlsrv-driver.md)

[Sobre los ejemplos de código de la documentación](../../connect/php/about-code-examples-in-the-documentation.md)  
  

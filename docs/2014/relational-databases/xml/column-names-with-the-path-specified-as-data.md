---
title: Nombres de columna con la ruta de acceso especificada como data() | Microsoft Docs
ms.custom: ''
ms.date: 06/13/2017
ms.prod: sql-server-2014
ms.reviewer: ''
ms.suite: ''
ms.technology:
- dbe-xml
ms.tgt_pltfrm: ''
ms.topic: conceptual
helpviewer_keywords:
- names [SQL Server], columns with
ms.assetid: 0b738e44-6108-4417-a9a4-abeb7680d899
caps.latest.revision: 9
author: douglaslMS
ms.author: douglasl
manager: craigg
ms.openlocfilehash: 50b13ad0a796107c0786520ee5b4f47bb6856580
ms.sourcegitcommit: c18fadce27f330e1d4f36549414e5c84ba2f46c2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/02/2018
ms.locfileid: "37221045"
---
# <a name="column-names-with-the-path-specified-as-data"></a>Nombres de columna con la ruta de acceso especificada como data()
  Si la ruta de acceso especificada como nombre de la columna es "data()", el valor se tratará como valor atómico en el XML generado. Si el siguiente elemento de la serialización también es un valor atómico, se agregará un carácter de espacio al XML. Esto resulta útil cuando se crean valores de elementos y atributos del tipo lista. La consulta siguiente recupera el Id. del modelo de producto, el nombre del producto y una lista de los productos de ese modelo.  
  
```  
USE AdventureWorks2012;  
GO  
SELECT ProductModelID       AS "@ProductModelID",  
       Name                 AS "@ProductModelName",  
      (SELECT ProductID AS "data()"  
       FROM   Production.Product  
       WHERE  Production.Product.ProductModelID =   
              Production.ProductModel.ProductModelID  
      FOR XML PATH (''))    AS "@ProductIDs"  
FROM  Production.ProductModel  
WHERE ProductModelID= 7   
FOR XML PATH('ProductModelData');  
```  
  
 La instrucción SELECT anidada recupera una lista de Id. de productos. Especificará "data()" como nombre de columna de los Id. de productos. El modo PATH especifica una cadena vacía para el nombre de elemento de fila, por lo que no se generará ningún elemento de fila. En su lugar, se devolverán los valores como asignados a un atributo ProductIDs del elemento de fila <`ProductModelData`> de la instrucción SELECT primaria. El resultado es el siguiente:  
  
 `<ProductModelData ProductModelID="7"`  
  
 `ProductModelName="HL Touring Frame"`  
  
 `ProductIDs="885 887 888 889 890 891 892 893" />`  
  
## <a name="see-also"></a>Vea también  
 [Usar el modo PATH con FOR XML](use-path-mode-with-for-xml.md)  
  
  

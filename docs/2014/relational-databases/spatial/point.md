---
title: Punto | Microsoft Docs
ms.custom: ''
ms.date: 06/13/2017
ms.prod: sql-server-2014
ms.reviewer: ''
ms.suite: ''
ms.technology:
- dbe-spatial
ms.tgt_pltfrm: ''
ms.topic: conceptual
helpviewer_keywords:
- Point geometry subtype [SQL Server]
- geometry data type [SQL Server], spatial data
ms.assetid: 2a596ec4-8b2f-4962-bcb4-e5c8f77edad5
caps.latest.revision: 19
author: douglaslMS
ms.author: douglasl
manager: craigg
ms.openlocfilehash: 6581a93e30e058e909b4e7df2bec7be6b52e4926
ms.sourcegitcommit: c18fadce27f330e1d4f36549414e5c84ba2f46c2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/02/2018
ms.locfileid: "37331259"
---
# <a name="point"></a>Punto
  En [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] datos espaciales, un `Point` es un objeto 0 dimensional que representa una ubicación única y puede contener valores Z (elevación) y M (medida).  
  
## <a name="geography-data-type"></a>Tipo de datos geography  
 El tipo Point para el tipo de datos geography representa una ubicación única donde *Lat* representa la latitud y *Long* la longitud. Los valores de latitud y longitud se miden en grados. Los valores de latitud siempre quedan en el intervalo [-90, 90] y, si se especifican valores fuera de este, se producirá una excepción. Los valores de longitud siempre quedan en el intervalo [-180, 180], y los especificados fuera de este se ajustan para entrar dentro. Por ejemplo, si se especifica 190 para la longitud, se ajustará al valor -170. *SRID* representa el identificador de referencia espacial de la instancia de **geography** que desea devolver.  
  
## <a name="geometry-data-type"></a>Tipo de datos geometry  
 El tipo point del tipo de datos geometry representa una sola ubicación donde *X* representa la coordenada X del punto que se va a generar e *Y* representa la coordenada Y del punto que se va a generar. *SRID* representa el identificador de referencia espacial de la instancia de **geometry** que desea devolver.  
  
## <a name="examples"></a>Ejemplos  
 El ejemplo siguiente crea una instancia de `geometry Point`que representa el punto (3, 4) con un SRID de 0.  
  
```  
DECLARE @g geometry;  
SET @g = geometry::STGeomFromText('POINT (3 4)', 0);  
```  
  
 El ejemplo siguiente crea una instancia de `geometry``Point` que representa el punto (3, 4) con un valor Z (elevación) de 7, un valor M (medida) de 2,5 y el SRID predeterminado de 0.  
  
```  
DECLARE @g geometry;  
SET @g = geometry::Parse('POINT(3 4 7 2.5)');  
```  
  
 El último ejemplo devuelve los valores X, Y, Z y M para la instancia de `geometry``Point` .  
  
```  
SELECT @g.STX;  
SELECT @g.STY;  
SELECT @g.Z;  
SELECT @g.M;  
```  
  
 Los valores Z y M se pueden especificar explícitamente como NULL, como se muestra en el ejemplo siguiente.  
  
```  
DECLARE @g geometry;  
SET @g = geometry::Parse('POINT(3 4 NULL NULL)');  
```  
  
## <a name="see-also"></a>Vea también  
 [MultiPoint](multipoint.md)   
 [STX &#40;tipo de datos geometry&#41;](/sql/t-sql/spatial-geometry/stx-geometry-data-type)   
 [STY &#40;tipo de datos geometry&#41;](/sql/t-sql/spatial-geometry/sty-geometry-data-type)   
 [Datos espaciales &#40;SQL Server&#41;](spatial-data-sql-server.md)  
  
  

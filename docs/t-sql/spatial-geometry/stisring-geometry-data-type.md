---
title: STIsRing (tipo de datos geometry) | Microsoft Docs
ms.custom: ''
ms.date: 08/03/2017
ms.prod: sql
ms.prod_service: database-engine, sql-database
ms.reviewer: ''
ms.suite: sql
ms.technology: t-sql
ms.tgt_pltfrm: ''
ms.topic: language-reference
f1_keywords:
- STIsRing_TSQL
- STIsRing (geometry Data Type)
dev_langs:
- TSQL
helpviewer_keywords:
- STIsRing (geometry Data Type)
ms.assetid: ea0063be-1c74-4cc4-ac6f-b65321ddfa54
caps.latest.revision: 21
author: douglaslMS
ms.author: douglasl
manager: craigg
ms.openlocfilehash: 2cec988e796d6098db81a4022163888a57276f13
ms.sourcegitcommit: e77197ec6935e15e2260a7a44587e8054745d5c2
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 07/11/2018
ms.locfileid: "38048533"
---
# <a name="stisring-geometry-data-type"></a>STIsRing (tipo de datos geometry)
[!INCLUDE[tsql-appliesto-ss2008-asdb-xxxx-xxx-md](../../includes/tsql-appliesto-ss2008-asdb-xxxx-xxx-md.md)]

Devuelve 1 si una instancia de **geometry** cumple los siguientes requisitos:
-   Es una instancia de **LineString**.  
-   Está cerrada.  
-   Es sencilla.  
-   Devuelve 0 si la instancia de **LineString** no cumple los requisitos.  

 Para que una instancia de **geometry** esté cerrada y sea sencilla, [STIsClosed()](../../t-sql/spatial-geometry/stisclosed-geometry-data-type.md) y [STIsSimple()](../../t-sql/spatial-geometry/stissimple-geometry-data-type.md) deben devolver 1 cuando se les invoca desde la instancia. Para determinar el tipo de instancia de una instancia de **geometry**, use [STGeometryType()](../../t-sql/spatial-geometry/stgeometrytype-geometry-data-type.md).  
  
## <a name="syntax"></a>Sintaxis  
  
```  
  
.STIsRing ( )  
```  
  
## <a name="return-types"></a>Tipos devueltos  
 Tipo de valor devuelto de [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)]: **bit**  
  
 Tipo de valor devuelto de CLR: **SqlBoolean**  
  
## <a name="remarks"></a>Notas  
 Este método devuelve NULL si la instancia de **LineString** no es un polígono.  
  
## <a name="examples"></a>Ejemplos  
 En el ejemplo siguiente se crea una instancia de `LineString` y se usa `STIsRing()` para comprobar si la instancia es un anillo.  
  
```  
DECLARE @g geometry;  
SET @g = geometry::STGeomFromText('LINESTRING(0 0, 2 2, 1 0, 0 0)', 0);  
SELECT @g.STIsRing();  
```  
  
## <a name="see-also"></a>Ver también  
 [STIsClosed &#40;tipo de datos geometry&#41;](../../t-sql/spatial-geometry/stisclosed-geometry-data-type.md)   
 [STGeometryType &#40;tipo de datos geometry&#41;](../../t-sql/spatial-geometry/stgeometrytype-geometry-data-type.md)   
 [STIsSimple &#40;tipo de datos geometry&#41;](../../t-sql/spatial-geometry/stissimple-geometry-data-type.md)   
 [Métodos de OGC en instancias de geometry](../../t-sql/spatial-geometry/ogc-methods-on-geometry-instances.md)  
  
  


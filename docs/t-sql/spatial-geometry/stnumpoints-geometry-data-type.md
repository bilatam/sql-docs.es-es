---
title: STNumPoints (tipo de datos geometry) | Microsoft Docs
ms.custom: ''
ms.date: 03/14/2017
ms.prod: sql
ms.prod_service: database-engine, sql-database
ms.reviewer: ''
ms.suite: sql
ms.technology: t-sql
ms.tgt_pltfrm: ''
ms.topic: language-reference
f1_keywords:
- STNumPoints_TSQL
- STNumPoints (geometry Data Type)
dev_langs:
- TSQL
helpviewer_keywords:
- STNumPoints (geometry Data Type)
ms.assetid: a19520fc-7f91-4a2c-856f-4d8b99a7e496
caps.latest.revision: 16
author: douglaslMS
ms.author: douglasl
manager: craigg
ms.openlocfilehash: 668b4f5708e03ccfb5ed19ad4125e7f957a8f03e
ms.sourcegitcommit: a6596c62f607041c4402f7d5b41a232fca257c14
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2018
ms.locfileid: "36255767"
---
# <a name="stnumpoints-geometry-data-type"></a>STNumPoints (tipo de datos geometry)
[!INCLUDE[tsql-appliesto-ss2012-asdb-xxxx-xxx-md](../../includes/tsql-appliesto-ss2012-asdb-xxxx-xxx-md.md)]

  Devuelve la suma del número de puntos de cada una de las figuras de una instancia de **geometry**.  
  
## <a name="syntax"></a>Sintaxis  
  
```  
  
.STNumPoints ( )  
```  
  
## <a name="return-types"></a>Tipos devueltos  
 Tipo de valor devuelto de [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)]: **int**  
  
 Tipo de valor devuelto de CLR: **SqlInt32**  
  
## <a name="remarks"></a>Notas  
 Este método cuenta los puntos de la descripción de una instancia de **geometry**. Los puntos duplicados se cuentan. Si esta instancia es de tipo **collection**, este método devuelve la suma de los puntos de cada uno de sus elementos.  
  
## <a name="examples"></a>Ejemplos  
 En el ejemplo siguiente se crea una instancia de `LineString` y se utiliza `STNumPoints()` para determinar el número de puntos que se utilizaron en la descripción de la instancia.  
  
```  
DECLARE @g geometry;  
SET @g = geometry::STGeomFromText('LINESTRING(0 0, 2 2, 1 0)', 0);  
SELECT @g.STNumPoints();  
```  
  
## <a name="see-also"></a>Ver también  
 [Métodos de OGC en instancias de geometry](../../t-sql/spatial-geometry/ogc-methods-on-geometry-instances.md)  
  
  

---
title: Elemento StorageMode (ASSL) | Microsoft Docs
ms.custom: ''
ms.date: 03/06/2017
ms.prod: sql-server-2014
ms.reviewer: ''
ms.suite: ''
ms.technology:
- analysis-services
- docset-sql-devref
ms.tgt_pltfrm: ''
ms.topic: reference
api_name:
- StorageMode Element
api_location:
- http://schemas.microsoft.com/analysisservices/2003/engine
topic_type:
- apiref
f1_keywords:
- StorageMode
helpviewer_keywords:
- StorageMode element
ms.assetid: 197e8153-1ab6-43ba-a7e9-ae9be19ac511
caps.latest.revision: 39
author: minewiskan
ms.author: owend
manager: craigg
ms.openlocfilehash: 3d61633743b4ce7e7b72f868b280e1bb376f1846
ms.sourcegitcommit: c18fadce27f330e1d4f36549414e5c84ba2f46c2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/02/2018
ms.locfileid: "37299015"
---
# <a name="storagemode-element-assl"></a>Elemento StorageMode (ASSL)
  Determina el modo de almacenamiento para el elemento primario.  
  
## <a name="syntax"></a>Sintaxis  
  
```xml  
  
<Cube> <!-- or Dimension, MeasureGroup, Partition -->  
   ...  
   <StorageMode>...</StorageMode>  
   ...  
</Cube>  
```  
  
## <a name="element-characteristics"></a>Características del elemento  
  
|Característica|Descripción|  
|--------------------|-----------------|  
|Tipo y longitud de los datos|String (enumeración)|  
|Valor predeterminado|*MOLAP*|  
|Cardinalidad|0-1: Elemento opcional que puede aparecer una y solo una vez.|  
  
## <a name="element-relationships"></a>Relaciones del elemento  
  
|Relación|Elemento|  
|------------------|-------------|  
|Elementos primarios|[Elemento de cubo &#40;ASSL&#41;](../objects/cube-element-assl.md), [dimensión elemento &#40;ASSL&#41;](../objects/dimension-element-assl.md), [elemento MeasureGroup &#40;ASSL&#41;](../objects/group-element-assl.md), [partición Elemento &#40;ASSL&#41;](../objects/partition-element-assl.md)|  
|Elementos secundarios|None|  
  
## <a name="remarks"></a>Notas  
 El valor de este elemento se limita a una de las cadenas enumeradas en la tabla siguiente.  
  
|Valor|Descripción|  
|-----------|-----------------|  
|*MOLAP*|El elemento primario usa el almacenamiento OLAP multidimensional (MOLAP).|  
|*ROLAP*|El elemento primario usa el almacenamiento OLAP relacional (ROLAP).|  
|*HOLAP*|El elemento primario usa el almacenamiento OLAP híbrido (HOLAP). **Nota:** este valor no es válido para [dimensión](../objects/dimension-element-assl.md) elementos primarios.|  
|*InMemory*|El elemento primario utiliza el almacenamiento IMBI.|  
  
 La enumeración que corresponde a los valores permitidos para `StorageMode` en el objeto de Analysis Management Objects (AMO) es el modelo <xref:Microsoft.AnalysisServices.StorageMode>.  
  
 Los elementos que corresponden a los elementos primarios de `StorageMode` en el modelo de objetos de Objetos de administración de análisis (AMO) son <xref:Microsoft.AnalysisServices.Cube>, <xref:Microsoft.AnalysisServices.Dimension>, <xref:Microsoft.AnalysisServices.MeasureGroup> y <xref:Microsoft.AnalysisServices.Partition>.  
  
## <a name="see-also"></a>Vea también  
 [Propiedades &#40;ASSL&#41;](properties-assl.md)  
  
  

---
title: Donde el elemento (XMLA) | Microsoft Docs
ms.custom: ''
ms.date: 06/13/2017
ms.prod: sql-server-2014
ms.reviewer: ''
ms.suite: ''
ms.technology:
- analysis-services
- docset-sql-devref
ms.tgt_pltfrm: ''
ms.topic: reference
api_name:
- Where Element
api_location:
- http://schemas.microsoft.com/analysisservices/2003/engine
topic_type:
- apiref
f1_keywords:
- urn:schemas-microsoft-com:xml-analysis#Where
- microsoft.xml.analysis.where
- http://schemas.microsoft.com/analysisservices/2003/engine#Where
helpviewer_keywords:
- Where element
ms.assetid: 81fb4190-3379-4ddf-8795-a0772f3b92bb
caps.latest.revision: 12
author: minewiskan
ms.author: owend
manager: craigg
ms.openlocfilehash: 44d6242d0c815ee8ec150936a5e41ad12de4a59d
ms.sourcegitcommit: c18fadce27f330e1d4f36549414e5c84ba2f46c2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/02/2018
ms.locfileid: "37218075"
---
# <a name="where-element-xmla"></a>Elemento Where (XMLA)
  Define una condición de filtro que usa el comando primario [Drop](../xml-elements-commands/drop-element-xmla.md) o [Update](../xml-elements-commands/update-element-xmla.md).  
  
## <a name="syntax"></a>Sintaxis  
  
```xml  
  
<Drop> <!-- or Update -->  
   ...  
   <Where>  
      <Attributes>...</Attributes>  
   </Where>  
   ...  
</Insert>  
```  
  
## <a name="element-characteristics"></a>Características del elemento  
  
|Característica|Descripción|  
|--------------------|-----------------|  
|Tipo y longitud de los datos|None|  
|Valor predeterminado|None|  
|Cardinalidad|1-1: Elemento necesario que se produce una vez y solo una vez.|  
  
## <a name="element-relationships"></a>Relaciones del elemento  
  
|Relación|Elemento|  
|------------------|-------------|  
|Elementos primarios|[Drop](../xml-elements-commands/drop-element-xmla.md), [Update](../xml-elements-commands/update-element-xmla.md)|  
|Elementos secundarios|[Atributos](attributes-element-xmla.md)|  
  
## <a name="remarks"></a>Notas  
 Para `Drop` comandos, el `Where` elemento, combinado con el [DeleteWithDescendants](deletewithdescendants-element-xmla.md) elemento, identifica el ámbito de miembros de atributo que se puede quitar.  
  
 Para los comandos `Update`, el elemento `Where` identifica el ámbito de los miembros de atributo que se van a actualizar. Es posible actualizar varios miembros de atributo utilizando una combinación de atributos incluidos en la colección `Attributes` del comando primario `Update` y la colección `Attributes` del elemento `Where`.  
  
 Para más información sobre cómo eliminar y actualizar miembros de atributos, vea [Insertar, actualizar y quitar miembros &#40;XMLA&#41;](../../multidimensional-models-scripting-language-assl-xmla/inserting-updating-and-dropping-members-xmla.md).  
  
## <a name="see-also"></a>Vea también  
 [Propiedades &#40;XMLA&#41;](xml-elements-properties.md)  
  
  

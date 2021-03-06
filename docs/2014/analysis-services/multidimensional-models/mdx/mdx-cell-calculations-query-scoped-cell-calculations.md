---
title: Creación de cálculos de celdas del ámbito de consulta (MDX) | Microsoft Docs
ms.custom: ''
ms.date: 06/13/2017
ms.prod: sql-server-2014
ms.reviewer: ''
ms.suite: ''
ms.technology:
- analysis-services
ms.tgt_pltfrm: ''
ms.topic: conceptual
helpviewer_keywords:
- WITH keyword
- query-scoped cell calculations [MDX]
ms.assetid: 45987daa-4400-41e9-add7-2428fd75709b
caps.latest.revision: 30
author: minewiskan
ms.author: owend
manager: craigg
ms.openlocfilehash: 5431862cd1a446a045d910841adc4d78d62d42be
ms.sourcegitcommit: c18fadce27f330e1d4f36549414e5c84ba2f46c2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/02/2018
ms.locfileid: "37159396"
---
# <a name="creating-query-scoped-cell-calculations-mdx"></a>Crear cálculos de celdas del ámbito de consulta (MDX)
  La palabra clave `WITH` en las expresiones multidimensionales (MDX) se usa para describir las celdas calculadas en el contexto de una consulta. El `WITH` palabra clave tiene la siguiente sintaxis:  
  
```  
WITH CELL CALCULATION Cube_Name.CellCalc_Identifier  String_Expression  
```  
  
 El valor `CellCalc_Identifier` es el nombre de las celdas calculadas. El valor `String_Expression` contiene una lista de expresiones de conjunto MDX ortogonales de una sola dimensión. Cada una de estas expresiones de conjunto debe dar como resultado una de las categorías que figuran en la siguiente tabla:  
  
|Categoría|Descripción|  
|--------------|-----------------|  
|Conjunto vacío|Una expresión de conjunto MDX que se resuelve en un conjunto vacío. En este caso, el ámbito de la celda calculada es todo el cubo.|  
|Conjunto de un solo miembro|Una expresión de conjunto MDX que se resuelve en un solo miembro.|  
|Conjunto de miembros de nivel|Una expresión de conjunto MDX que se resuelve en miembros de un solo nivel. Un ejemplo de expresión de conjunto es el *Level_Expression*.`Members` Función MDX. Para incluir los miembros calculados, use el *Level_Expression*.`AllMembers` Función MDX. Para más información, vea [AllMembers &#40;MDX&#41;](/sql/mdx/allmembers-mdx).|  
|Conjunto de descendientes|Una expresión de conjunto MDX que se resuelve en los descendientes de un miembro determinado. Un ejemplo de expresión de conjunto es el `Descendants`(*Member_Expression*, *Level_Expresion*, *Desc_Flag*) función MDX. Para más información, vea [Descendants &#40;MDX&#41;](/sql/mdx/descendants-mdx).|  
  
 Si el argumento `String_Expression` no describe ninguna dimensión, MDX considera que se han incluido todos los miembros para generar el subcubo de cálculo. Por lo tanto, si el argumento `String_Expression` tiene el valor NULL, la definición de las celdas calculadas se aplica a todo el cubo.  
  
 El argumento `MDX_Expression` contiene una expresión MDX que se evalúa como un valor de celda para todas las celdas definidas en el argumento `String_Expression` .  
  
## <a name="additional-considerations"></a>Consideraciones adicionales  
 MDX procesa la condición de cálculo, especificada por la propiedad `CONDITION` solamente una vez. Este único procesamiento proporciona mayor rendimiento para la evaluación de varias definiciones de celdas calculadas, sobre todo con celdas calculadas superpuestas a través de pasos de cubo.  
  
 Este único procesamiento se lleva a cabo dependiendo del ámbito de creación establecido en la definición de las celdas calculadas:  
  
-   Si se crea en un ámbito global, como parte de un cubo, MDX procesa la condición de cálculo al mismo tiempo que el cubo. Si se modifican de alguna manera las celdas del cubo y se incluyen en el subcubo de cálculo de una definición de celdas calculadas, la condición de cálculo puede no ser precisa hasta que el cubo vuelva a procesarse. La modificación de las celdas puede producirse a partir de reescrituras, por ejemplo. La condición de cálculo se vuelve a procesar en el mismo momento que el cubo.  
  
-   Si se creó en un ámbito de sesión, MDX procesa la condición de cálculo cuando la instrucción se emite durante la sesión. Como en definiciones de celdas calculadas creadas globalmente, si se modifican las celdas, la condición de cálculo puede no ser precisa para la definición de celdas calculadas.  
  
-   Si se creó en un ámbito de consulta, MDX procesa la condición de cálculo cuando se ejecuta la consulta. Aquí también se aplica el tema de modificación de las celdas, aunque las cuestiones de latencia de datos son mínimas debido al bajo tiempo de proceso de la ejecución de la consulta MDX.  
  
 Por otro lado, MDX procesa la fórmula de cálculo siempre que se emite una consulta MDX en el cubo y ésta implica celdas incluidas en la definición de celdas calculadas. Este procesamiento se lleva a cabo independientemente del ámbito de creación.  
  
## <a name="see-also"></a>Vea también  
 [Instrucción CREATE CELL CALCULATION &#40;MDX&#41;](/sql/mdx/mdx-data-definition-create-cell-calculation)  
  
  

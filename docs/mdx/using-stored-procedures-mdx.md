---
title: Usar procedimientos almacenados (MDX) | Documentos de Microsoft
ms.date: 06/04/2018
ms.prod: sql
ms.technology: analysis-services
ms.custom: mdx
ms.topic: reference
ms.author: owend
ms.reviewer: owend
author: minewiskan
manager: kfile
ms.openlocfilehash: 2a0ba1b350e59406f04796924385059c323facd6
ms.sourcegitcommit: 97bef3f248abce57422f15530c1685f91392b494
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2018
ms.locfileid: "34743804"
---
# <a name="using-stored-procedures-mdx"></a>Usar procedimientos almacenados (MDX)


  Puede ampliar la funcionalidad de [!INCLUDE[ssASnoversion](../includes/ssasnoversion-md.md)] y MDX (Expresiones Multidimensionales) escribiendo funciones definidas por el usuario o procedimientos almacenados de .NET. Para obtener más información, vea [ADOMD.NET Server Programming](../analysis-services/multidimensional-models-adomd-net-server/adomd-net-server-programming.md)  
  
 Cuando haga referencia o llame a un procedimiento almacenado, especifique el nombre de la función seguido de paréntesis. Dentro de los paréntesis puede especificar expresiones denominadas argumentos, que proporcionan los datos que se van a pasar a los parámetros. Cuando llame una función, debe proporcionar valores de argumentos para todos los parámetros, así como especificar los valores de argumentos en la misma secuencia en la que se definen los parámetros en la función definida por el usuario.  
  
 La consulta de ejemplo siguiente supone que tiene un ensamblado denominado SampleAssembly registrado en su servidor de [!INCLUDE[ssASnoversion](../includes/ssasnoversion-md.md)]:  
  
```  
SELECT SampleAssembly.RandomSample([Geography].[State-Province].Members, 5) on ROWS,   
[Date].[Calendar].[Calendar Year] on COLUMNS  
FROM [Adventure Works]  
WHERE [Measures].[Reseller Freight Cost]  
```  
  
> [!NOTE]  
>  *Procedimiento almacenado* es la terminología utilizada en [!INCLUDE[ssASnoversion](../includes/ssasnoversion-md.md)] para estos tipos de funciones. Las versiones anteriores de [!INCLUDE[ssASnoversion](../includes/ssasnoversion-md.md)] llama a estos tipos de funciones como *funciones definidas por el usuario*.  
  
## <a name="types-of-stored-procedures"></a>Tipos de procedimientos almacenados  
 [!INCLUDE[ssASnoversion](../includes/ssasnoversion-md.md)] es compatible con ambos tipos de ensamblados: COM y CLR. Se recomienda usar los ensamblados CLR porque ofrecen una seguridad mejorada. Si se instala Microsoft Office Excel en el servidor, también se pueden usar funciones de Excel.  
  
> [!NOTE]  
>  Los ensamblados COM de Microsoft Visual Basic para Aplicaciones (VBA) se registran de forma automática.  
  
## <a name="see-also"></a>Vea también  
 [Funciones &#40;sintaxis MDX&#41;](../mdx/functions-mdx-syntax.md)  
  
  

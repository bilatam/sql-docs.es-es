---
title: Antecesores (MDX) | Documentos de Microsoft
ms.date: 06/04/2018
ms.prod: sql
ms.technology: analysis-services
ms.custom: mdx
ms.topic: reference
ms.author: owend
ms.reviewer: owend
author: minewiskan
manager: kfile
ms.openlocfilehash: 0c108ea102e03000481d18bfc69f657e6bd8a0ce
ms.sourcegitcommit: 97bef3f248abce57422f15530c1685f91392b494
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2018
ms.locfileid: "34740054"
---
# <a name="ancestors-mdx"></a>Ancestors (MDX)


  Función que devuelve el conjunto de todos los antecesores de un miembro especificado en un nivel especificado o a una distancia especificada del miembro. Con [!INCLUDE[ssASnoversion](../includes/ssasnoversion-md.md)], el conjunto devuelto siempre constará de un solo miembro - [!INCLUDE[ssASnoversion](../includes/ssasnoversion-md.md)] no es compatible con varios elementos primarios para un solo miembro.  
  
## <a name="syntax"></a>Sintaxis  
  
```  
  
Level syntax  
Ancestors(Member_Expression, Level_Expression)  
  
Numeric syntax  
Ancestors(Member_Expression, Distance)  
```  
  
## <a name="arguments"></a>Argumentos  
 *Expresión_miembro*  
 Expresión MDX válida que devuelve un miembro.  
  
 *Level_Expression*  
 Expresión MDX válida que devuelve un nivel.  
  
 *distancia*  
 Expresión numérica válida que especifica la distancia desde el miembro especificado.  
  
## <a name="remarks"></a>Notas  
 Con el **antecesores** función, se proporciona la función con una expresión de miembro MDX y, a continuación, se proporciona una expresión MDX de un nivel que sea un antecesor de ese miembro o una expresión numérica que representa el número de niveles por encima de ese miembro. Con esta información, el **antecesores** función devuelve el conjunto de miembros (que será un conjunto que consta de un miembro) en ese nivel.  
  
> [!NOTE]  
>  Para devolver un miembro antecesor, en lugar de un conjunto antecesor, use la [antecesor](../mdx/ancestor-mdx.md) función.  
  
 Si se especifica una expresión de nivel, la **antecesores** función devuelve el conjunto de todos los antecesores del miembro especificado en el nivel especificado. Si el miembro especificado no se encuentra en la misma jerarquía que el nivel especificado, la función devuelve un error.  
  
 Si se especifica una distancia, la **antecesores** función devuelve el conjunto de todos los miembros que son el número de pasos especificado hacia arriba en la jerarquía especificada por la expresión de miembro. Un miembro se puede especificar como un miembro de una jerarquía de atributo, una jerarquía definida por el usuario, o, en algunos casos, una jerarquía de elementos primarios y secundarios. El número 1 devuelve el conjunto de miembros en el nivel primario y el número 2 devuelve el conjunto de miembros en el nivel primario de segundo nivel (si existe). El número 0 devuelve el conjunto, incluyendo únicamente al propio miembro.  
  
> [!NOTE]  
>  Utilice este formulario de la **antecesores** función para los casos en que el nivel del elemento primario es desconocido o no se puede llamar.  
  
## <a name="examples"></a>Ejemplos  
 En el ejemplo siguiente se usa el **antecesores** función para devolver la medida Internet Sales Amount para un miembro, su elemento primario y su primario de segundo nivel. Este ejemplo utiliza expresiones de nivel para especificar los niveles que se devolverán. Los niveles están en la misma jerarquía que el miembro especificado en la expresión de miembro.  
  
```  
SELECT {  
    Ancestors([Product].[Product Categories].[Product].[Mountain-100 Silver, 38],[Product].[Product Categories].[Category]),  
    Ancestors([Product].[Product Categories].[Product].[Mountain-100 Silver, 38],[Product].[Product Categories].[Subcategory]),  
    Ancestors([Product].[Product Categories].[Product].[Mountain-100 Silver, 38],[Product].[Product Categories].[Product])  
    } ON 0,  
[Measures].[Internet Sales Amount] ON 1  
FROM [Adventure Works]  
```  
  
 En el ejemplo siguiente se usa el **antecesores** función para devolver la medida Internet Sales Amount para un miembro, su elemento primario y su primario de segundo nivel. Este ejemplo utiliza expresiones numéricas para especificar los niveles que se devuelven. Los niveles están en la misma jerarquía que el miembro especificado en la expresión de miembro.  
  
```  
SELECT {  
   Ancestors(  
      [Product].[Product Categories].[Product].[Mountain-100 Silver, 38],2  
      ),  
   Ancestors(  
      [Product].[Product Categories].[Product].[Mountain-100 Silver, 38],1  
      ),  
   Ancestors(  
      [Product].[Product Categories].[Product].[Mountain-100 Silver, 38],0  
      )  
   } ON 0,  
[Measures].[Internet Sales Amount] ON 1  
FROM  [Adventure Works]  
```  
  
 En el ejemplo siguiente se usa el **antecesores** función para devolver la medida Internet Sales Amount para el elemento primario de un miembro de una jerarquía de atributo. Este ejemplo utiliza una expresión numérica para especificar el nivel que se devuelve. Dado que el miembro de la expresión de miembro forma parte de una jerarquía de atributo, su elemento primario es el nivel [All].  
  
```  
SELECT {  
   Ancestors(  
      [Product].[Product].[Mountain-100 Silver, 38],1  
      )  
   } ON 0,  
[Measures].[Internet Sales Amount] ON 1  
FROM [Adventure Works]  
```  
  
## <a name="see-also"></a>Vea también  
 [Referencia de funciones MDX &#40;MDX&#41;](../mdx/mdx-function-reference-mdx.md)  
  
  

---
title: Dividir (expresión de SSIS) | Microsoft Docs
ms.custom: ''
ms.date: 06/13/2017
ms.prod: sql-server-2014
ms.reviewer: ''
ms.suite: ''
ms.technology:
- integration-services
ms.tgt_pltfrm: ''
ms.topic: conceptual
helpviewer_keywords:
- / (divide)
- divide operator (/)
ms.assetid: 5bde9223-872d-443e-8a27-57735e1d8f3d
caps.latest.revision: 36
author: douglaslMS
ms.author: douglasl
manager: craigg
ms.openlocfilehash: a3dc1c33e2d3239311c14a6e0657a85775dc4e6a
ms.sourcegitcommit: c18fadce27f330e1d4f36549414e5c84ba2f46c2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/02/2018
ms.locfileid: "37182682"
---
# <a name="divide-ssis-expression"></a>Divide (SSIS Expression)
  Divide la primera expresión numérica por la segunda.  
  
## <a name="syntax"></a>Sintaxis  
  
```  
  
dividend / divisor  
  
```  
  
## <a name="arguments"></a>Argumentos  
 *dividend*  
 Es la expresión numérica que se va a dividir. *dividend* puede ser cualquier expresión numérica. Para más información, consulte [Integration Services Data Types](../data-flow/integration-services-data-types.md).  
  
 *divisor*  
 Es la expresión numérica entre la que se va a dividir el dividendo. *divisor* puede ser cualquier expresión numérica excepto cero.  
  
## <a name="result-types"></a>Tipos de resultado  
 Determinados por los tipos de datos de los dos argumentos. Para más información, consulte [Integration Services Data Types in Expressions](integration-services-data-types-in-expressions.md).  
  
## <a name="remarks"></a>Notas  
 Si alguno de los operandos es NULL, el resultado será NULL.  
  
 No se permite dividir por cero. En función de cómo se evalúe la subexpresión *divisor* , se producirá uno de los siguientes errores:  
  
-   Si la subexpresión *divisor* que devuelve cero es una constante, el error aparecerá en tiempo de diseño y hará que no se valide la expresión.  
  
-   Si la subexpresión *divisor* que devuelve cero contiene variables pero no contiene columnas de entrada, el componente al que la expresión pertenece no superará la validación previa a la ejecución del paquete.  
  
-   Si la subexpresión *divisor* que se evalúa como cero contiene columnas de entrada, el error aparecerá en tiempo de ejecución y se controlará en función de las reglas de flujo de errores del componente de flujo de datos.  
  
## <a name="expression-examples"></a>Ejemplos de expresiones  
 Este ejemplo divide dos literales numéricos.  
  
```  
25 / 5  
```  
  
 Este ejemplo divide los valores de la columna **ListPrice** por los valores de la columna **StandardCost** .  
  
```  
ListPrice / StandardCost  
```  
  
## <a name="see-also"></a>Vea también  
 [Precedencia y asociatividad](operator-precedence-and-associativity.md)   
 [Operadores &#40;expresión de SSIS&#41;](operators-ssis-expression.md)  
  
  

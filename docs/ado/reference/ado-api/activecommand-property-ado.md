---
title: Propiedad ActiveCommand (ADO) | Documentos de Microsoft
ms.prod: sql
ms.prod_service: connectivity
ms.technology: connectivity
ms.custom: ''
ms.date: 01/19/2017
ms.reviewer: ''
ms.suite: sql
ms.tgt_pltfrm: ''
ms.topic: conceptual
apitype: COM
f1_keywords:
- Recordset20::ActiveCommand
helpviewer_keywords:
- ActiveCommand property [ADO]
ms.assetid: fb4088d5-5968-42d6-aeaa-3955046bb4da
caps.latest.revision: 11
author: MightyPen
ms.author: genemi
manager: craigg
ms.openlocfilehash: e85286a885ab8edcfb08b029f7a1fd77c8d3f4a0
ms.sourcegitcommit: 62826c291db93c9017ae219f75c3cfeb8140bf06
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "35274970"
---
# <a name="activecommand-property-ado"></a>Propiedad ActiveCommand (ADO)
Indica el [comando](../../../ado/reference/ado-api/command-object-ado.md) objeto creado asociado [Recordset](../../../ado/reference/ado-api/recordset-object-ado.md) objeto.  
  
## <a name="return-value"></a>Valor devuelto  
 Devuelve un **Variant** que contiene un **comando** objeto. Valor predeterminado es una referencia de objeto null.  
  
## <a name="remarks"></a>Notas  
 El **ActiveCommand** propiedad es de solo lectura.  
  
 Si un **comando** no se utilizó para crear el actual objeto **Recordset**, un **Null** se devuelve la referencia de objeto.  
  
 Utilice esta propiedad para encontrar el asociado **comando** objeto cuando se proporcionan solo resultante **Recordset** objeto.  
  
## <a name="applies-to"></a>Se aplica a  
 [Objeto de conjunto de registros (ADO)](../../../ado/reference/ado-api/recordset-object-ado.md)  
  
## <a name="see-also"></a>Vea también  
 [Ejemplo de la propiedad ActiveCommand (VB)](../../../ado/reference/ado-api/activecommand-property-example-vb.md)   
 [Ejemplo de la propiedad ActiveCommand (JScript)](../../../ado/reference/ado-api/activecommand-property-example-jscript.md)   
 [Ejemplo de la propiedad ActiveCommand (VC ++)](../../../ado/reference/ado-api/activecommand-property-example-vc.md)   
 [Objeto Command (ADO)](../../../ado/reference/ado-api/command-object-ado.md)

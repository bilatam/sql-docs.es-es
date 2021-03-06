---
title: InheritTypeEnum | Documentos de Microsoft
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
- InheritTypeEnum
helpviewer_keywords:
- InheritTypeEnum enumeration [ADOX]
ms.assetid: c2f6ce79-c4b3-4d40-ac95-21025208f991
caps.latest.revision: 12
author: MightyPen
ms.author: genemi
manager: craigg
ms.openlocfilehash: b3a167913b23005cf2b78e4acc682ec2af75157c
ms.sourcegitcommit: 62826c291db93c9017ae219f75c3cfeb8140bf06
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "35286654"
---
# <a name="inherittypeenum"></a>InheritTypeEnum
Especifica cómo heredan permisos establecidos con los objetos [SetPermissions](../../../ado/reference/adox-api/setpermissions-method-adox.md).  
  
|Constante|Valor|Descripción|  
|--------------|-----------|-----------------|  
|**adInheritBoth**|3|Objetos y otros contenedores contenidos en el objeto principal heredan la entrada.|  
|**adInheritContainers**|2|Otros contenedores que se encuentran en el objeto principal heredan la entrada.|  
|**adInheritNone**|0|Predeterminado: Se produce ninguna herencia.|  
|**adInheritNoPropagate**|4|El **marcas adInheritObjects** y **adInheritContainers** marcas no se propagan a una entrada heredada.|  
|**marcas adInheritObjects**|1|Objetos de contenedor no en el contenedor heredan los permisos.|  
  
## <a name="applies-to"></a>Se aplica a  
 [SetPermissions (método, ADOX)](../../../ado/reference/adox-api/setpermissions-method-adox.md)

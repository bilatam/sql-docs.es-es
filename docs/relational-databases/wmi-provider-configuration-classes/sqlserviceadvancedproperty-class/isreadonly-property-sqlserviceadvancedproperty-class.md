---
title: Propiedad IsReadOnly (clase SqlServiceAdvancedProperty) | Documentos de Microsoft
ms.custom: ''
ms.date: 03/03/2017
ms.prod: sql
ms.prod_service: database-engine
ms.component: wmi
ms.reviewer: ''
ms.suite: sql
ms.technology:
- database-engine
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IsReadOnly Property (SqlServiceAdvancedProperty Class)
apilocation:
- sqlmgmproviderxpsp2up.mof
apitype: MOFDef
helpviewer_keywords:
- IsReadOnly property
ms.assetid: 9672e70f-1d8c-4133-ac73-3b5733a1c4ee
caps.latest.revision: 32
author: CarlRabeler
ms.author: carlrab
manager: craigg
ms.openlocfilehash: 7ae3861e4f8c4bf44bcadec1c6b5c4f97f20b896
ms.sourcegitcommit: 1740f3090b168c0e809611a7aa6fd514075616bf
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/03/2018
ms.locfileid: "33010882"
---
# <a name="isreadonly-property-sqlserviceadvancedproperty-class"></a>Propiedad IsReadOnly (clase SqlServiceAdvancedProperty)
[!INCLUDE[tsql-appliesto-ss2008-xxxx-xxxx-xxx-md](../../../includes/tsql-appliesto-ss2008-xxxx-xxxx-xxx-md.md)]
  Obtiene o establece la propiedad booleana que especifica si la propiedad avanzada es o no es de solo lectura.  
  
## <a name="syntax"></a>Sintaxis  
  
```  
  
object.IsReadOnly [= value]  
```  
  
## <a name="parts"></a>Partes  
 *objeto*  
 Objeto de la [clase SqlServiceAdvancedProperty](../../../relational-databases/wmi-provider-configuration-classes/sqlserviceadvancedproperty-class/sqlserviceadvancedproperty-class.md) que representa una propiedad avanzada.  
  
## <a name="property-valuereturn-value"></a>Valor de propiedad y valor devuelto  
 Valor booleano que especifica si la propiedad avanzada es o no es de solo lectura: **true** si la propiedad avanzada es de solo lectura o **false** si se puede modificar.  
  
## <a name="remarks"></a>Comentarios  
  
## <a name="see-also"></a>Vea también  
 [Iniciar y detener servicios](http://technet.microsoft.com/library/ms174886\(v=sql.105\).aspx)  
  
  

---
title: Opciones de validación de suscripciones (Suscripciones de mezcla) | Microsoft Docs
ms.custom: ''
ms.date: 06/13/2017
ms.prod: sql-server-2014
ms.reviewer: ''
ms.suite: ''
ms.technology:
- replication
ms.tgt_pltfrm: ''
ms.topic: conceptual
f1_keywords:
- sql12.rep.validate.mergeoptions.f1
helpviewer_keywords:
- Subscription Validation Options dialog box
ms.assetid: 4958c4ab-2025-42ce-b836-6fb4e9e6f24d
caps.latest.revision: 14
author: MashaMSFT
ms.author: mathoma
manager: craigg
ms.openlocfilehash: ba1d468b04ab25ee97cacde6ef582f193d8a1856
ms.sourcegitcommit: c18fadce27f330e1d4f36549414e5c84ba2f46c2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/02/2018
ms.locfileid: "37166756"
---
# <a name="subscription-validation-options-merge-subscriptions"></a>Opciones de validación de suscripciones (Suscripciones de mezcla)
  Use el cuadro de diálogo **Opciones de validación de suscripciones** para especificar si la validación debe utilizar solamente recuento de filas o recuento de filas y suma de comprobación binaria.  
  
## <a name="options"></a>Opciones  
 **Solo comprobar recuentos de filas**  
 Seleccione esta opción para validar si la tabla del suscriptor tiene el mismo número de filas que la tabla del publicador. Este método no valida si el contenido de las filas coincide. La validación del recuento de filas proporciona una idea sobre validación que puede ponerle al corriente de problemas con los datos.  
  
 **Comprobar los recuentos de filas y comparar las sumas de comprobación para comprobar los datos de las filas**  
 Además de llevar a cabo un recuento de filas en el publicador y en el suscriptor, se calcula una suma de comprobación de todos los datos utilizando el algoritmo binario de suma de comprobación. Si el número de filas da un error, no se lleva a cabo la suma de comprobación. Esta opción no es válida para [!INCLUDE[msCoName](../../includes/msconame-md.md)] [!INCLUDE[ssEW](../../includes/ssew-md.md)].  
  
## <a name="see-also"></a>Vea también  
 [Validar datos en el suscriptor](validate-data-at-the-subscriber.md)   
 [Validar datos replicados](validate-replicated-data.md)  
  
  

---
title: La propiedad MarshalOptions (ADO) | Documentos de Microsoft
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
- Recordset15::MarshalOptions
helpviewer_keywords:
- MarshalOptions property [ADO]
ms.assetid: 390c8abf-133e-40da-8b99-8f748a983e4f
caps.latest.revision: 11
author: MightyPen
ms.author: genemi
manager: craigg
ms.openlocfilehash: 8b81646d7d4339f06e5682c1886651cf69ea0dc4
ms.sourcegitcommit: 62826c291db93c9017ae219f75c3cfeb8140bf06
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "35279344"
---
# <a name="marshaloptions-property-ado"></a>Propiedad MarshalOptions (ADO)
Indica que los registros de la [Recordset](../../../ado/reference/ado-api/recordset-object-ado.md) deben calcularse de nuevo hacia el servidor.  
  
## <a name="settings-and-return-values"></a>Configuración y valores devueltos  
 Establece o devuelve un [MarshalOptionsEnum](../../../ado/reference/ado-api/marshaloptionsenum.md) valor. El valor predeterminado es **adMarshalAll**.  
  
## <a name="remarks"></a>Notas  
 Cuando se usa un cliente [Recordset](../../../ado/reference/ado-api/recordset-object-ado.md), los registros que se han modificado en el cliente se reescriben en el nivel intermedio o un servidor Web mediante una técnica denominada ordenamiento, el proceso de empaquetado y envío de método de interfaz parámetros en los límites del proceso o subproceso. Establecer el **MarshalOptions** propiedad puede mejorar el rendimiento cuando se calculan las referencias de los datos remotos modificados para la actualización en el nivel intermedio o un servidor Web.  
  
> [!NOTE]
>  **Uso de servicios de datos remoto** esta propiedad sólo se utiliza en un lado del cliente **conjunto de registros**.  
  
## <a name="applies-to"></a>Se aplica a  
 [Objeto de conjunto de registros (ADO)](../../../ado/reference/ado-api/recordset-object-ado.md)  
  
## <a name="see-also"></a>Vea también  
 [Ejemplo de la propiedad MarshalOptions (VB)](../../../ado/reference/ado-api/marshaloptions-property-example-vb.md)   
 [Ejemplo de la propiedad MarshalOptions (VC ++)](../../../ado/reference/ado-api/marshaloptions-property-example-vc.md)   

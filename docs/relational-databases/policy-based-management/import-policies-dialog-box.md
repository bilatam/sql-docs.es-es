---
title: Importar directivas (cuadro de diálogo) | Microsoft Docs
ms.custom: ''
ms.date: 03/01/2017
ms.prod: sql
ms.prod_service: database-engine
ms.component: performance-monitor
ms.reviewer: ''
ms.suite: sql
ms.technology:
- database-engine
ms.tgt_pltfrm: ''
ms.topic: conceptual
f1_keywords:
- sql13.swb.dmf.importpolicy.f1
ms.assetid: 78ab5f6e-2f13-4788-937e-8892ef4e2345
caps.latest.revision: 22
author: MikeRayMSFT
ms.author: mikeray
manager: craigg
ms.openlocfilehash: 0e672c7cfb95870236e6e6ed4601790fda6d0a87
ms.sourcegitcommit: 1740f3090b168c0e809611a7aa6fd514075616bf
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/03/2018
ms.locfileid: "32955360"
---
# <a name="import-policies-dialog-box"></a>Importar directivas (cuadro de diálogo)
[!INCLUDE[appliesto-ss-xxxx-xxxx-xxx-md](../../includes/appliesto-ss-xxxx-xxxx-xxx-md.md)]
  Utilice este cuadro de diálogo para importar una o varias directivas (y su condición a la que se hace referencia) que se guardaron como archivos XML, en la instancia de [!INCLUDE[ssDEnoversion](../../includes/ssdenoversion-md.md)] actual.  
  
## <a name="options"></a>Opciones  
 **Archivos para importar**  
 Para importar una directiva desde un archivo XML, escriba la ruta de acceso y el nombre del archivo, o use el botón Examinar (**...**).  
  
 **Reemplazar duplicados con elementos importados**  
 Seleccione esta opción para sobrescribir cualquier directiva o condición existente del mismo nombre si ya existe en esta instancia de [!INCLUDE[ssDE](../../includes/ssde-md.md)] . Una condición con una directiva dependiente no se puede sobrescribir a menos que la directiva dependiente se esté sobrescribiendo también. Si no se selecciona esta opción, una condición existente que está utilizando la misma expresión de condición no producirá un error.  
  
 **Estado de directiva**  
 Seleccione el estado que desea para la directiva importada:  
  
-   **Conservar el estado de las directivas al importar**  
  
-   **Habilitar todas las directivas al importar**  
  
-   **Deshabilitar todas las directivas al importar**  
  
## <a name="see-also"></a>Ver también  
 [Administrar servidores mediante administración basada en directivas](../../relational-databases/policy-based-management/administer-servers-by-using-policy-based-management.md)   
 [Importar una directiva de administración basada en directivas](../../relational-databases/policy-based-management/import-a-policy-based-management-policy.md)   
 [Exportar una directiva de administración basada en directivas](../../relational-databases/policy-based-management/export-a-policy-based-management-policy.md)  
  
  

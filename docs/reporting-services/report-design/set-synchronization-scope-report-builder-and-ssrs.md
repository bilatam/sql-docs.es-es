---
title: Establecer el ámbito de sincronización (Generador de informes y SSRS) | Microsoft Docs
ms.custom: ''
ms.date: 03/07/2017
ms.prod: reporting-services
ms.prod_service: reporting-services-sharepoint, reporting-services-native
ms.component: report-design
ms.reviewer: ''
ms.suite: pro-bi
ms.technology: ''
ms.tgt_pltfrm: ''
ms.topic: conceptual
ms.assetid: 6f4a11e6-6151-47be-a43f-e3dbf6c0e737
caps.latest.revision: 8
author: maggiesMSFT
ms.author: maggies
manager: kfile
ms.openlocfilehash: 00b6638849391c64686afd9f9c070bffeb39e539
ms.sourcegitcommit: 1740f3090b168c0e809611a7aa6fd514075616bf
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/03/2018
ms.locfileid: "33023912"
---
# <a name="set-synchronization-scope-report-builder-and-ssrs"></a>Establecer el ámbito de sincronización (Generador de informes y SSRS)
  En un informe paginado de [!INCLUDE[ssRSnoversion_md](../../includes/ssrsnoversion-md.md)] , los indicadores transmiten los valores de datos sincronizando el intervalo de los valores de datos del indicador que están en un ámbito especificado.   
    
  De forma predeterminada, el ámbito es el contenedor primario del indicador, por ejemplo la tabla o matriz que contiene el indicador. Puede cambiar la sincronización del indicador en función del diseño del informe. Por ejemplo, si una región de datos como una tabla tiene un grupo de filas, puede especificar el grupo como el ámbito del indicador. El indicador también puede omitir la sincronización.  
  
 Opciones como las unidades de medida se pueden establecer mediante expresiones. Para más información, vea [Expresiones &#40;Generador de informes y SSRS&#41;](../../reporting-services/report-design/expressions-report-builder-and-ssrs.md).  
  
 Para obtener información general sobre la descripción y el ámbito de configuración de informes, vea [Ámbito de expresión para los totales, agregados y colecciones integradas &#40;Generador de informes y SSRS&#41;](../../reporting-services/report-design/expression-scope-for-totals-aggregates-and-built-in-collections.md).  
  
## <a name="to-change-the-synchronization-scope-of-an-indicator"></a>Para cambiar el ámbito de sincronización de un indicador  
  
1.  Haga clic con el botón derecho en el indicador que quiere cambiar y seleccione **Propiedades de indicador**.  
  
2.  Haga clic en **Valores y estados** en el panel izquierdo.  
  
3.  En la lista **Ámbito de sincronización** , haga clic en el ámbito que desea aplicar.  
  
     La opción **(Ninguno)** , que quita el ámbito de sincronización del indicador, siempre está disponible. Las demás opciones dependen del diseño del informe.  
  
     Si quiere, puede hacer clic en el botón **Expresión** (*fx*) para modificar una expresión que establezca el ámbito.  
  
4.  [!INCLUDE[clickOK](../../includes/clickok-md.md)]  
  
## <a name="see-also"></a>Ver también  
 [Indicadores &#40;Generador de informes y SSRS&#41;](../../reporting-services/report-design/indicators-report-builder-and-ssrs.md)  
  
  

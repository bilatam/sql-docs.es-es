---
title: Gráficos polares (Generador de informes y SSRS) | Microsoft Docs
ms.custom: ''
ms.date: 03/03/2017
ms.prod: reporting-services
ms.prod_service: reporting-services-sharepoint, reporting-services-native
ms.component: report-design
ms.reviewer: ''
ms.suite: pro-bi
ms.technology: ''
ms.tgt_pltfrm: ''
ms.topic: conceptual
ms.assetid: c9402d8f-202a-4cdf-949e-50f5b1d2b885
caps.latest.revision: 7
author: maggiesMSFT
ms.author: maggies
manager: kfile
ms.openlocfilehash: 732243f0680cda998b70ea70dd51d67e310c81d9
ms.sourcegitcommit: 1740f3090b168c0e809611a7aa6fd514075616bf
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/03/2018
ms.locfileid: "33024242"
---
# <a name="polar-charts-report-builder-and-ssrs"></a>Gráficos polares (Generador de informes y SSRS)
  Un gráfico polar muestra una serie como un conjunto de puntos agrupados por categorías en un círculo de 360 grados. Los valores se representan por la longitud de los puntos con relación al centro del círculo. Cuanto más lejos del centro esté el punto, mayor será su valor. Las etiquetas de las categorías se muestran en el perímetro del gráfico. Para obtener más información sobre cómo agregar datos a un gráfico polar, vea [Gráficos &#40;Generador de informes y SSRS&#41;](../../reporting-services/report-design/charts-report-builder-and-ssrs.md).  
  
> [!NOTE]  
>  [!INCLUDE[ssRBRDDup](../../includes/ssrbrddup-md.md)]  
  
## <a name="variations"></a>Variaciones  
  
-   **Gráfico radial**. Un gráfico radial muestra una serie como una línea o un área circular. A diferencia del gráfico polar, el gráfico radial no muestra los datos en función de las coordenadas polares.  
  
## <a name="data-considerations-for-polar-charts"></a>Consideraciones sobre los datos para los gráficos polares  
  
-   El gráfico radial es útil para realizar comparaciones entre varias series de datos de categorías.  
  
-   Los gráficos polares se usan normalmente para representar datos polares, en los que cada punto de datos viene determinado por un ángulo y una distancia.  
  
-   Los gráficos polares no se pueden combinar con ningún otro tipo de gráfico en la misma área de gráfico.  
  
## <a name="example"></a>Ejemplo  
 En el ejemplo siguiente se muestra el uso de un gráfico radial. La tabla siguiente proporciona los datos de ejemplo para el gráfico.  
  
|Nombre|Sales|  
|----------|-----------|  
|Shrubs|61|  
|Seeds|78|  
|Bulbs|60|  
|Trees|38|  
|Flowers|81|  
  
 En este ejemplo, el campo Nombre se sitúa en el área Grupos de categorías. El campo Ventas se coloca en el área Valores. El campo Sales se agrega automáticamente al gráfico al colocarlo. El gráfico radial calcula dónde se deben situar las etiquetas basándose en el número de valores del campo Sales, que contiene cinco valores, y coloca las etiquetas en cinco puntos equidistantes en un círculo. Si el campo Sales incluyese tres valores, las etiquetas se colocarían en tres puntos equidistantes en un círculo.  
  
 En la ilustración siguiente se muestra un ejemplo de un gráfico radial basado en los datos presentados.  
  
 ![Gráfico radial](../../reporting-services/report-design/media/rs-radarchart.gif "Gráfico radial")  
  
## <a name="see-also"></a>Ver también  
 [Gráficos &#40;Generador de informes y SSRS&#41;](../../reporting-services/report-design/charts-report-builder-and-ssrs.md)   
 [Aplicar formato a un gráfico &#40;Generador de informes y SSRS&#41;](../../reporting-services/report-design/formatting-a-chart-report-builder-and-ssrs.md)   
 [Tipos de gráficos &#40;Generador de informes y SSRS&#41;](../../reporting-services/report-design/chart-types-report-builder-and-ssrs.md)   
 [Gráficos de líneas &#40;Generador de informes y SSRS&#41;](../../reporting-services/report-design/line-charts-report-builder-and-ssrs.md)   
 [Puntos de datos vacíos y nulos en los gráficos &#40;Generador de informes y SSRS&#41;](../../reporting-services/report-design/empty-and-null-data-points-in-charts-report-builder-and-ssrs.md)  
  
  

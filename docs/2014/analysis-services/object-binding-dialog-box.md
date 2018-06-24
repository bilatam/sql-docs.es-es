---
title: Objeto de enlace de cuadro de diálogo | Documentos de Microsoft
ms.custom: ''
ms.date: 06/13/2017
ms.prod: sql-server-2014
ms.reviewer: ''
ms.suite: ''
ms.technology:
- analysis-services
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- sql.asvs.dimensiondesigner.dbv.objectbinding.f1
helpviewer_keywords:
- Object Binding dialog box
ms.assetid: 2bb5ad7c-2962-4559-8c95-cf7148bd2e72
caps.latest.revision: 13
author: Minewiskan
ms.author: owend
manager: mblythe
ms.openlocfilehash: 13b0050733b21e99ac7395a26953338f4dbce176
ms.sourcegitcommit: 5dd5cad0c1bbd308471d6c885f516948ad67dfcf
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2018
ms.locfileid: "36109291"
---
# <a name="object-binding-dialog-box"></a>Enlace de objetos (cuadro de diálogo)
  Use el cuadro de diálogo **Enlace de objetos** en [!INCLUDE[ssBIDevStudioFull](../includes/ssbidevstudiofull-md.md)] para definir enlaces entre la propiedad de un objeto de [!INCLUDE[ssASnoversion](../includes/ssasnoversion-md.md)] y una tabla o columna en una vista del origen de datos. Para mostrar el cuadro de diálogo **Enlace de objetos** , seleccione **(nuevo)** en la lista desplegable del valor de las propiedades siguientes de un objeto [!INCLUDE[ssASnoversion](../includes/ssasnoversion-md.md)] en la ventana **Propiedades** de [!INCLUDE[ssBIDevStudioFull](../includes/ssbidevstudiofull-md.md)]:  
  
-   NameColumn  
  
-   ValueColumn  
  
-   CustomRollupColumn  
  
-   CustomRollupPropertiesColumn  
  
-   UnaryOperatorColumn  
  
## <a name="options"></a>Opciones  
 **Tipo de enlace**  
 Seleccione el enlace que utilizará para el objeto [!INCLUDE[ssASnoversion](../includes/ssasnoversion-md.md)] . Se pueden utilizar los siguientes tipos de enlaces:  
  
 Enlace de columna  
 Enlaza el objeto a una tabla y columna existentes en una vista del origen de datos.  
  
 Generar columna  
 Indica que se definirá una nueva columna en la vista del origen de datos y, a continuación, el enlace de columna se asociará a ella.  
  
> [!NOTE]  
>  Si selecciona esta opción, debe ejecutar el **Asistente para generar esquemas** antes de implementar el objeto de [!INCLUDE[ssASnoversion](../includes/ssasnoversion-md.md)] .  
  
 Enlace de fila  
 Enlaza el objeto a una fila de una tabla de hechos y se usa para facilitar medidas de recuento basadas en el número de filas procesadas en la tabla de hechos.  
  
 **Tabla de origen**  
 Muestra una lista de tablas en la vista del origen de datos asociadas con el objeto de [!INCLUDE[ssASnoversion](../includes/ssasnoversion-md.md)] .  
  
 **Columna de origen**  
 Muestra una lista de columnas de la tabla seleccionada en **Tabla de origen**.  
  
## <a name="see-also"></a>Vea también  
 [Diseñadores y cuadros de diálogo de Analysis Services &#40;datos multidimensionales&#41;](analysis-services-designers-and-dialog-boxes-multidimensional-data.md)  
  
  
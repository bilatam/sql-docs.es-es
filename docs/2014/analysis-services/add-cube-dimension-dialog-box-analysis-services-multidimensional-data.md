---
title: Agregar cuadro de diálogo de dimensión de cubo (Analysis Services - datos multidimensionales) | Microsoft Docs
ms.custom: ''
ms.date: 06/13/2017
ms.prod: sql-server-2014
ms.reviewer: ''
ms.suite: ''
ms.technology:
- analysis-services
ms.tgt_pltfrm: ''
ms.topic: conceptual
f1_keywords:
- sql12.asvs.cubeeditor.addcubedimensiondialog.f1
helpviewer_keywords:
- Add Cube Dimension dialog box
ms.assetid: 625a3b1f-183b-445f-9bb7-96945c324767
caps.latest.revision: 23
author: minewiskan
ms.author: owend
manager: craigg
ms.openlocfilehash: 5ab3e91d2571c4186ad6eeb1e858a6fe5f3f2d53
ms.sourcegitcommit: c18fadce27f330e1d4f36549414e5c84ba2f46c2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/02/2018
ms.locfileid: "37232425"
---
# <a name="add-cube-dimension-dialog-box-analysis-services---multidimensional-data"></a>Cuadro de diálogo Agregar dimensión de cubo (Analysis Services - Datos multidimensionales)
  Use el cuadro de diálogo **Agregar dimensión de cubo** en [!INCLUDE[ssBIDevStudioFull](../includes/ssbidevstudiofull-md.md)] para agregar una referencia a una dimensión de base de datos a un cubo. Para visualizar el cuadro de diálogo **Agregar dimensión de cubo** , puede realizar una de estas acciones:  
  
-   Hacer clic en **Agregar dimensión de cubo** en el panel **Barra de herramientas** de la pestaña **Estructura de cubo** o **Uso de dimensiones** del Diseñador de cubos.  
  
-   Hacer clic con el botón derecho en el panel **Dimensiones** de la pestaña **Estructura de cubo** del Diseñador de cubos y seleccionar **Agregar dimensión de cubo** en el menú contextual.  
  
-   Hacer clic con el botón derecho en el panel **Cuadrícula** de la pestaña **Uso de dimensiones** del Diseñador de cubos y seleccionar **Agregar dimensión de cubo** en el menú contextual.  
  
> [!NOTE]  
>  Cada dimensión de cubo puede tener únicamente una relación con un grupo de medida. No obstante, puede crear más de una dimensión de cubo y agregarla al cubo si la dimensión de la base de datos en la cual se basa la dimensión de cubo se relaciona con los grupos de medida a través de más de una relación en la vista del origen de datos. Se hace referencia a estas dimensiones como dimensiones realizadoras de roles y normalmente se producen con dimensiones de tiempo.  
  
## <a name="options"></a>Opciones  
 **Seleccionar dimensión**  
 Seleccione una dimensión de base de datos existente para agregar una dimensión de cubo que se base en ella al cubo seleccionado. Es posible definir varias dimensiones de cubo a partir de la misma dimensión de base de datos.  
  
> [!NOTE]  
>  Si se agrega a un cubo más de una dimensión de cubo basada en la misma dimensión de base de datos, las dimensiones de cubo adicionales se denominan dimensiones realizadoras de roles.  
  
## <a name="see-also"></a>Vea también  
 [Diseñadores y cuadros de diálogo de Analysis Services &#40;datos multidimensionales&#41;](analysis-services-designers-and-dialog-boxes-multidimensional-data.md)  
  
  

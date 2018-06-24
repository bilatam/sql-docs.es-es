---
title: Propiedades (SSAS Tabular) de la tabla | Documentos de Microsoft
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
- sql12.asvs.bidtoolset.tableprop.f1
ms.assetid: 16d3347b-7e43-4a6b-9956-fdd6ede092e6
caps.latest.revision: 8
author: Minewiskan
ms.author: owend
manager: mblythe
ms.openlocfilehash: 85a29563b6e0e0b78c63c771547a57473e3c9f52
ms.sourcegitcommit: 5dd5cad0c1bbd308471d6c885f516948ad67dfcf
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2018
ms.locfileid: "36105216"
---
# <a name="table-properties-ssas-tabular"></a>Propiedades de la tabla (SSAS tabular)
  En este tema se describen las propiedades de la tabla del modelo. Las propiedades que se describen aquí son diferentes de las del cuadro de diálogo Editar propiedades de tabla, que definen qué columnas del origen se importan.  
  
 Secciones de este tema:  
  
-   [Propiedades de tabla](#bkmk_properties)  
  
-   [Para configurar los valores de propiedad de tabla](#bkmk_config_prop)  
  
##  <a name="bkmk_properties"></a> Propiedades de tabla  
 **Basic**  
  
|Property|Valor predeterminado|Descripción|  
|--------------|---------------------|-----------------|  
|**Nombre de conexión**|\<nombre de conexión >|Nombre de la conexión con el origen de datos de la tabla.<br /><br /> Para modificar la conexión, haga clic en el botón.|  
|**Oculto**|False|Especifica si la tabla se oculta en las listas de campos del cliente de informes.|  
|**Particiones**||Las particiones de la tabla no se muestran en la ventana **Propiedades** . Para ver, crear o modificar las particiones, haga clic en el botón para abrir el Administrador de particiones.|  
|**Datos de origen**||El origen de datos de la tabla no se pueden mostrar en la ventana **Propiedades** . Para ver o modificar los datos de origen, haga clic en el botón para abrir el cuadro de diálogo Editar propiedades de tabla.|  
|**Descripción de tabla**||Descripción de la tabla.<br /><br /> En [!INCLUDE[ssGeminiClient](../../includes/ssgeminiclient-md.md)], si un usuario final coloca el cursor sobre esta tabla en la lista de campos, aparece la descripción como una información sobre herramientas.|  
|**Nombre de tabla**|\<nombre descriptivo >|Especifica el nombre descriptivo de la tabla. El nombre de tabla puede especificar cuándo se importa una tabla con el Asistente para la importación de tablas o en cualquier momento después de la importación. El nombre de tabla en el modelo puede ser diferente de la tabla asociada en el origen. El nombre descriptivo de la tabla aparece en la lista de campos de la aplicación cliente de informes como en la base de datos modelo en [!INCLUDE[ssManStudioFull](../../includes/ssmanstudiofull-md.md)].|  
  
 **Propiedades de informes**  
  
 Para obtener descripciones detalladas e información sobre la configuración de propiedades de informes, vea [Propiedades de informes de Vista avanzada &#40;SSAS tabular&#41;](properties-ssas-tabular.md).  
  
|Property|Valor predeterminado|Descripción|  
|--------------|---------------------|-----------------|  
|**Conjunto de campos predeterminado**|||  
|Comportamiento de tabla|||  
  
###  <a name="bkmk_config_prop"></a> Para configurar los valores de propiedad de tabla  
  
1.  En el diseñador de modelos, en la vista de datos, haga clic en una tabla (pestaña), o bien, en la vista de diagramas, haga clic en un encabezado de tabla.  
  
2.  En la ventana **Propiedades** , haga clic en una propiedad y, a continuación, escriba un valor o haga clic en el botón de opciones de configuración adicionales.  
  
  
---
title: Analysis Services ejecutan el Editor de la tarea DDL (página DDL) | Microsoft Docs
ms.custom: ''
ms.date: 03/06/2017
ms.prod: sql-server-2014
ms.reviewer: ''
ms.suite: ''
ms.technology:
- integration-services
ms.tgt_pltfrm: ''
ms.topic: conceptual
f1_keywords:
- sql12.dts.designer.asexecuteddltask.ddl.f1
helpviewer_keywords:
- Analysis Services Execute DDL Task Editor
ms.assetid: f21bf8d0-ec5f-4c18-9de0-8875addb927b
caps.latest.revision: 29
author: douglaslms
ms.author: douglasl
manager: craigg
ms.openlocfilehash: 8693bb66bb848301a739a16f6989537d203eca25
ms.sourcegitcommit: c18fadce27f330e1d4f36549414e5c84ba2f46c2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/02/2018
ms.locfileid: "37269437"
---
# <a name="analysis-services-execute-ddl-task-editor-ddl-page"></a>Editor de la tarea Ejecutar DDL de Analysis Services (página DDL)
  Use la página **DDL** del cuadro de diálogo **Editor de la tarea Ejecutar DDL de Analysis Services** para especificar una conexión a un proyecto de [!INCLUDE[ssASnoversion](../includes/ssasnoversion-md.md)] o una base de datos de [!INCLUDE[ssASnoversion](../includes/ssasnoversion-md.md)] y proporcionar información sobre el origen de las instrucciones del lenguaje de definición de datos (DDL).  
  
 Para obtener información acerca de esta tarea, vea [Analysis Services Execute DDL Task](control-flow/analysis-services-execute-ddl-task.md).  
  
## <a name="static-options"></a>Opciones estáticas  
 **Conexión**  
 Seleccione un proyecto de [!INCLUDE[ssASnoversion](../includes/ssasnoversion-md.md)] o un administrador de conexiones de [!INCLUDE[ssASnoversion](../includes/ssasnoversion-md.md)] en la lista, o bien haga clic en \<**Nueva conexión…**> y use el cuadro de diálogo **Agregar administrador de conexiones de Analysis Services** para crear una conexión.  
  
 **Temas relacionados:** [Referencia de la interfaz de usuario del cuadro de diálogo Agregar administrador de conexiones con Analysis Services](connection-manager/add-analysis-services-connection-manager-dialog-box-ui-reference.md), [Administrador de conexiones de Analysis Services](connection-manager/analysis-services-connection-manager.md)  
  
 **Tipo de origen**  
 Especifique el tipo de origen de las instrucciones de DDL. Esta propiedad presenta las opciones indicadas en la siguiente tabla:  
  
|Valor|Descripción|  
|-----------|-----------------|  
|**Entrada directa**|Establezca en el cuadro de texto **SourceDirect** el origen de la instrucción DDL almacenada. Al seleccionar este valor se muestran las opciones dinámicas de la siguiente sección.|  
|**Conexión de archivos**|Establezca el origen de un archivo que contenga la instrucción DDL. Al seleccionar este valor se muestran las opciones dinámicas de la siguiente sección.|  
|**Variable**|Establezca el origen en una variable. Al seleccionar este valor se muestran las opciones dinámicas de la siguiente sección.|  
  
## <a name="dynamic-options"></a>Opciones dinámicas  
  
### <a name="sourcetype--direct-input"></a>SourceType = Entrada directa  
 **Source**  
 Escriba las instrucciones de DDL, o bien haga clic en el botón de puntos suspensivos **(…)** y, después, escriba las instrucciones en el cuadro de diálogo **Instrucciones de DDL** .  
  
### <a name="sourcetype--file-connection"></a>SourceType = Conexión de archivos  
 **Source**  
 Seleccione una conexión de archivos de la lista, o bien haga clic en \<**Nueva conexión…**> y use el cuadro de diálogo **Administrador de conexiones de archivos** para crear una conexión.  
  
 **Temas relacionados:** [Administrador de conexiones de archivo](connection-manager/file-connection-manager.md)  
  
### <a name="sourcetype--variable"></a>SourceType = Variable  
 **Source**  
 Seleccione una variable de la lista, o bien haga clic en \<**Nueva variable…**> y use el cuadro de diálogo **Agregar variable** para crear una variable.  
  
 **Temas relacionados:** [Variables de Integration Services &#40;SSIS&#41;](integration-services-ssis-variables.md)  
  
## <a name="see-also"></a>Vea también  
 [Referencia de mensajes y Error de Integration Services](../../2014/integration-services/integration-services-error-and-message-reference.md)   
 [Analysis Services Execute DDL Editor de la tarea &#40;página General&#41;](general-page-of-integration-services-designers-options.md)   
 [Página expresiones](expressions/expressions-page.md)   
 [Flujo de control](control-flow/control-flow.md)   
 [Lenguaje de Scripting de Analysis Services &#40;ASSL&#41; referencia](../analysis-services/scripting/analysis-services-scripting-language-assl-for-xmla.md)   
 [XML for Analysis &#40;XMLA&#41; referencia](../analysis-services/xmla/xml-for-analysis-xmla-reference.md)  
  
  

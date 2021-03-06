---
title: Editor de consultas DMX (Analysis Services - minería de datos) | Microsoft Docs
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
- sql12.asvs.sqlserverstudio.startpage.dmx.f1
ms.assetid: 7ac877a1-0f29-46b9-9a51-73b02172bef1
caps.latest.revision: 21
author: minewiskan
ms.author: owend
manager: craigg
ms.openlocfilehash: 1c1efcb4ecef6c311882b471a56535543bcc25b1
ms.sourcegitcommit: c18fadce27f330e1d4f36549414e5c84ba2f46c2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/02/2018
ms.locfileid: "37236065"
---
# <a name="dmx-query-editor-analysis-services---data-mining"></a>Editor de consultas DMX (Analysis Services: minería de datos)
  Use el Editor de consultas DMX para diseñar y ejecutar instrucciones escritas en el lenguaje de Extensiones de minería de datos (DMX).  
  
## <a name="features"></a>Características  
  
-   Escriba los scripts en el panel del editor de consultas del Editor de consultas DMX.  
  
-   Para ejecutar scripts, presione **F5**o haga clic en **Ejecutar** en la barra de herramientas o en el menú **Consulta** . Si se selecciona un fragmento del código, solamente se ejecutará dicho fragmento. Si no se selecciona ningún código, se ejecutará todo el contenido del Editor de consultas DMX.  
  
-   Vea los metadatos para cubos y otros objetos contenidos en una base de datos de [!INCLUDE[ssASnoversion](../includes/ssasnoversion-md.md)] en el panel de metadatos.  
  
-   Para obtener ayuda con la sintaxis de DMX, seleccione una palabra clave en el Editor de consultas DMX y haga clic en **F1**.  
  
-   Para obtener ayuda dinámica con la sintaxis de DMX, en el menú **Ayuda** , haga clic en **Ayuda dinámica** para abrir el componente Ayuda dinámica. En Ayuda dinámica, los temas de ayuda se muestran en la ventana **Ayuda dinámica** al escribir las palabras clave en el Editor de consultas.  
  
## <a name="sql-server-analysis-services-editors-toolbar"></a>Barra de herramientas Editores de SQL Server Analysis Services  
 Al abrir el Editor de consultas DMX, se mostrará la barra de herramientas **Editores de SQL Server Analysis Services** con los botones que se incluyen en la siguiente tabla.  
  
|Término|Definición|  
|----------|----------------|  
|**Conectar**|Abre el cuadro de diálogo **Conectar a servidor** para establecer una conexión a una instancia de Analysis Services.|  
|**Desconectar**|Desconecta el Editor de consultas DMX de una instancia de [!INCLUDE[ssASnoversion](../includes/ssasnoversion-md.md)] .|  
|**Cambiar conexión**|Abre el cuadro de diálogo **Conectar a servidor** para establecer una conexión a una instancia distinta de [!INCLUDE[ssASnoversion](../includes/ssasnoversion-md.md)] .|  
|**Consulta con conexión actual**|Abre una nueva ventana del Editor de consultas DMX y usa la información de conexión de la ventana actual del Editor de consultas DMX.|  
|**Bases de datos disponibles**|Cambia la conexión a una base de datos distinta de [!INCLUDE[ssASnoversion](../includes/ssasnoversion-md.md)] en la misma instancia.|  
|**Ejecutar**|Ejecuta el código seleccionado y, si no se ha seleccionado ningún código, esta opción ejecuta todo el código del Editor de consultas DMX.|  
|**Analizar**|Comprueba la sintaxis del código seleccionado. Si no se selecciona ningún código, esta opción comprueba la sintaxis de toda la ventana del Editor de consultas DMX.|  
|**Cancelar ejecución de la consulta**|Envía una solicitud de cancelación al servidor. Algunas consultas no pueden cancelarse inmediatamente, sino que deben esperar a una condición de cancelación adecuada. Cuando se cancelan consultas, pueden producirse retrasos mientras se revierten las transacciones.|  
  
## <a name="dmx-query-editor-window"></a>Ventana Editor de consultas DMX  
 Las opciones incluidas en la siguiente tabla están disponibles en el Editor de consultas DMX.  
  
|Término|Definición|  
|----------|----------------|  
|**Ventana editor de consultas**|Escriba las instrucciones y los scripts DMX que debe ejecutar el Editor de consultas DMX.<br /><br /> El menú contextual del editor de consultas proporciona las siguientes opciones:<br /><br /> **Cortar**: copia la selección actual en el Portapapeles y quita la selección de la ventana del editor de consultas.<br /><br /> **Copiar**: copia la selección actual en el Portapapeles.<br /><br /> **Pegar**: pega el contenido del Portapapeles en la selección actual.<br /><br /> **Conectar**: abre el cuadro de diálogo **Conectar con el servidor** para establecer una conexión a una instancia de [!INCLUDE[ssASnoversion](../includes/ssasnoversion-md.md)] .<br /><br /> **Desconectar**: desconecta el editor de consultas actual de un [!INCLUDE[ssASnoversion](../includes/ssasnoversion-md.md)] instancia.<br /><br /> **Desconectar todas las consultas**: desconecta todos los editores de consultas abiertos.<br /><br /> **Cambiar conexión**: abre el **conectar al servidor** cuadro de diálogo para establecer una conexión a otro [!INCLUDE[ssASnoversion](../includes/ssasnoversion-md.md)] instancia.<br /><br /> **Abrir servidor en el Explorador de objetos**: abre el [!INCLUDE[ssASnoversion](../includes/ssasnoversion-md.md)] instancia al que está conectado el editor de consultas actual en **Explorador de objetos**.<br /><br /> **Ejecutar**: ejecuta el código seleccionado o, si se selecciona ningún código, ejecuta todo el código en el editor de consultas actual.<br /><br /> **Ventana propiedades**: muestra el **propiedades** ventana en [!INCLUDE[ssManStudioFull](../includes/ssmanstudiofull-md.md)] para la ventana de consulta actual.<br /><br /> **Opciones de consulta**: muestra el **opciones de consulta** cuadro de diálogo.|  
|**Ventana metadatos**|Muestra los metadatos para la base de datos conectada de [!INCLUDE[ssASnoversion](../includes/ssasnoversion-md.md)] .|  
|**Cubo**|Seleccione un cubo en la base de datos conectada de [!INCLUDE[ssASnoversion](../includes/ssasnoversion-md.md)] para mostrar los metadatos asociados al cubo en la pestaña **Metadatos** .|  
|**Metadatos**|Muestra los metadatos para el cubo seleccionado en **Cubo**, incluidos los grupos de medida y las medidas, los indicadores clave de rendimiento, las dimensiones, las jerarquías, los niveles, los miembros y las propiedades de los miembros. Para recuperar la clave completa de un objeto:<br /><br /> Arrastre el objeto desde la pestaña **Metadatos** hasta el panel de consultas.<br /><br /> O bien:<br /><br /> Haga clic con el botón derecho en el objeto y seleccione **Copiar**y, luego, haga clic con el botón derecho en el panel de consultas y seleccione **Pegar**.|  
|**Funciones**|Muestra los metadatos para las funciones DMX disponibles para la base de datos de [!INCLUDE[ssASnoversion](../includes/ssasnoversion-md.md)], una vez recuperados del conjunto de filas de esquema DMSCHEMA_MINING_FUNCTIONS.<br /><br /> Para recuperar la sintaxis de una función:<br /><br /> Arrastre el objeto desde la pestaña **Funciones** hasta el panel de consultas.<br /><br /> O bien:<br /><br /> Haga clic con el botón derecho en la función y seleccione **Copiar**y, luego, haga clic con el botón derecho en el panel de consultas y seleccione **Pegar**.|  
|**Ventana de resultados**|Muestra los resultados de una instrucción DMX en una cuadrícula.|  
|**Ventana de mensajes**|Muestra información sobre cómo se ejecuta una instrucción DMX. Por ejemplo, esta ventana muestra todos los errores encontrados durante la ejecución o el número de celdas recuperadas tras la ejecución.|  
  
## <a name="see-also"></a>Vea también  
 [Diseñadores y cuadros de diálogo de Analysis Services &#40;datos multidimensionales&#41;](analysis-services-designers-and-dialog-boxes-multidimensional-data.md)   
 [Extensiones de minería de datos &#40;DMX&#41; referencia](/sql/dmx/data-mining-extensions-dmx-reference)   
 [Editor de consultas MDX &#40;Analysis Services - datos multidimensionales&#41;](mdx-query-editor-analysis-services-multidimensional-data.md)   
 [Editor de consultas XMLA &#40;Analysis Services - datos multidimensionales&#41;](xmla-query-editor-analysis-services-multidimensional-data.md)   
 [Editores de consultas y texto &#40;SQL Server Management Studio&#41;](../relational-databases/scripting/query-and-text-editors-sql-server-management-studio.md)   
 [Métodos abreviados de teclado SQL Server Management Studio](../ssms/sql-server-management-studio-keyboard-shortcuts.md)   
 [Personalizar menús y teclas de método abreviado](../ssms/customize-menus-and-shortcut-keys.md)   
 [Codificación de colores en el Editor de consultas](../relational-databases/scripting/color-coding-in-query-editors.md)  
  
  

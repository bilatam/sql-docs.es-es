---
title: Ventana Resultados espaciales | Microsoft Docs
ms.custom: ''
ms.date: 03/01/2017
ms.prod: sql
ms.technology: scripting
ms.reviewer: ''
ms.suite: sql
ms.tgt_pltfrm: ''
ms.topic: conceptual
ms.assetid: c2d5a477-6496-4d01-adee-7322ebdfadf3
caps.latest.revision: 8
author: MightyPen
ms.author: genemi
manager: craigg
monikerRange: '>=aps-pdw-2016||=azuresqldb-current||=azure-sqldw-latest||>=sql-server-2016||=sqlallproducts-allversions||>=sql-server-linux-2017'
ms.openlocfilehash: d7563efb7d43e1d122fe193d1ececd8723294cc6
ms.sourcegitcommit: 4cd008a77f456b35204989bbdd31db352716bbe6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/06/2018
ms.locfileid: "39540345"
---
# <a name="spatial-results-window"></a>Ventana Resultados espaciales
[!INCLUDE[appliesto-ss-asdb-asdw-pdw-md](../../includes/appliesto-ss-asdb-asdw-pdw-md.md)]
  La ventana **Resultados espaciales** proporciona herramientas de asignación visual para ver los datos espaciales. Para ver los resultados espaciales, los resultados de la consulta deben incluir una columna espacial con datos de geometría o de geografía.  
  
> [!NOTE]  
>  La ventana **Resultados espaciales** solo está disponible si los resultados se devuelven a una cuadrícula en la ventana **Resultados** . Si especifica que los resultados se deben devolver como texto, esta ventana no está disponible.  
  
## <a name="options"></a>Opciones  
 **Seleccionar columna espacial**  
 Especifique la columna espacial que desea ver en las columnas espaciales de los resultados de la consulta. Solo puede seleccionarse una columna cada vez.  
  
 **Seleccionar columna de etiqueta**  
 Especifique la columna no espacial en las columnas devueltas en los resultados de la consulta para etiquetar los datos espaciales. Solo puede seleccionarse una columna cada vez.  
  
 Esta opción no está disponible si solo se devuelven instancias de punto en una consulta.  
  
 **Seleccionar proyección**  
 Muestre los datos de geografía en una de estas cuatro proyecciones: Equirectangular, Mercator, Robinson o Bonne.  
  
 Esta opción no está disponible para los datos de geometría.  
  
 **Zoom**  
 Ajuste la presentación del mapa en una escala exponencial.  
  
 **Mostrar líneas de cuadrícula**  
 Activa o desactiva las líneas de cuadrícula de coordenadas.  
  
 En las formas de polígono, la etiqueta solo se muestra cuando la forma es lo suficientemente grande como para contener el texto del rótulo. Si desea mostrar las etiquetas para las formas pequeñas, ajuste el zoom.  
  
> [!NOTE]  
>  Las instancias de punto no se pueden etiquetar.  
  
## <a name="see-also"></a>Ver también  
 [Ver datos espaciales en el Explorador de objetos](../../relational-databases/scripting/view-spatial-data-in-object-explorer.md)   
 [Datos espaciales &#40;SQL Server&#41;](../../relational-databases/spatial/spatial-data-sql-server.md)   
 [Editor de consultas del motor de base de datos &#40;SQL Server Management Studio&#41;](../../relational-databases/scripting/database-engine-query-editor-sql-server-management-studio.md)   
 [Editores de consultas y texto &#40;SQL Server Management Studio&#41;](../../relational-databases/scripting/query-and-text-editors-sql-server-management-studio.md)  
  
  

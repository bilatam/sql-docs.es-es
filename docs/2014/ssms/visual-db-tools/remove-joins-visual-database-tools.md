---
title: Quitar combinaciones (Visual Database Tools) | Microsoft Docs
ms.custom: ''
ms.date: 06/13/2017
ms.prod: sql-server-2014
ms.reviewer: ''
ms.suite: ''
ms.technology:
- dbe-cross-instance
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- removing joins
- joins [SQL Server], removing
- deleting joins
ms.assetid: ccc212a1-fd13-48d6-85e5-5ff310c34bbd
caps.latest.revision: 10
author: JennieHubbard
ms.author: jhubbard
manager: jhubbard
ms.openlocfilehash: 75ee172ba9dcdb5761e7dd1eefe5722441c9983a
ms.sourcegitcommit: 5dd5cad0c1bbd308471d6c885f516948ad67dfcf
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2018
ms.locfileid: "36111462"
---
# <a name="remove-joins-visual-database-tools"></a>Quitar combinaciones (Visual Database Tools)
  Si no desea que las tablas se combinen mediante una combinación interna o externa, puede quitar la combinación existente entre ellas. Por ejemplo, puede quitar una combinación que el [Diseñador de consultas y vistas](visual-database-tools.md) haya creado automáticamente entre dos tablas.  
  
> [!NOTE]  
>  Cuando se quita una combinación de una consulta, no se modifica la relación subyacente en la base de datos.  
  
 Si dos tablas combinadas forman parte de la consulta y quita todas las condiciones de combinación que existen entre ellas, la consulta resultante es el producto de ambas tablas, es decir, una instancia CROSS JOIN.  
  
### <a name="to-remove-a-join"></a>Para quitar una combinación  
  
-   En el [panel Diagrama](diagram-pane-visual-database-tools.md), seleccione la línea de combinación de la combinación que desea quitar y, a continuación, presione la tecla SUPR. Puede seleccionar y eliminar varias líneas de combinación al mismo tiempo.  
  
 El Diseñador de consultas y vistas quita la línea de combinación y modifica la instrucción en el [panel SQL](sql-pane-visual-database-tools.md).  
  
## <a name="see-also"></a>Vea también  
 [Combinar tablas automáticamente &#40;Visual Database Tools&#41;](join-tables-automatically-visual-database-tools.md)   
 [Combinar tablas manualmente &#40;Visual Database Tools&#41;](join-tables-manually-visual-database-tools.md)   
 [Realizar consultas con combinaciones &#40;Visual Database Tools&#41;](query-with-joins-visual-database-tools.md)  
  
  
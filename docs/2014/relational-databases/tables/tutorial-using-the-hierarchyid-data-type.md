---
title: 'Tutorial: Uso del tipo de datos hierarchyid| Microsoft Docs'
ms.custom: ''
ms.date: 06/13/2017
ms.prod: sql-server-2014
ms.reviewer: ''
ms.suite: ''
ms.technology:
- database-engine
ms.tgt_pltfrm: ''
ms.topic: conceptual
helpviewer_keywords:
- tutorials [hierarchyid]
- hierarchyid [Database Engine], tutorial
ms.assetid: 5a7f7cfd-7faf-439f-8085-8fd6bf7db355
caps.latest.revision: 15
author: stevestein
ms.author: sstein
manager: craigg
ms.openlocfilehash: 1a9282da58d26e29c3f88a005e72fc431bf1e57a
ms.sourcegitcommit: c18fadce27f330e1d4f36549414e5c84ba2f46c2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/02/2018
ms.locfileid: "37168356"
---
# <a name="tutorial-using-the-hierarchyid-data-type"></a>Tutorial: Uso del tipo de datos hierarchyid
  Este tutorial está destinado a usuarios con experiencia en [!INCLUDE[tsql](../../includes/tsql-md.md)], pero que desconocen los tipos de datos de `hierarchyid`.  
  
## <a name="what-you-will-learn"></a>Aprendizaje  
 El tutorial está compuesto por dos lecciones:  
  
 [Lección 1: Convertir una tabla en una estructura jerárquica](lesson-1-converting-a-table-to-a-hierarchical-structure.md)  
 En esta lección, se toma una tabla de empleado existente, estructurada como una jerarquía de elementos primarios y secundarios, y se mueven los datos a una nueva tabla que representa la jerarquía usando el tipo de datos de `hierarchyid`. Esta lección requiere la base de datos de ejemplo [!INCLUDE[ssSampleDBobject](../../includes/sssampledbobject-md.md)] .  
  
 [Lección 2: Creación y administración de los datos de una tabla jerárquica](lesson-2-creating-and-managing-data-in-a-hierarchical-table.md)  
 En esta lección, se crea una tabla usando el tipo de datos de `hierarchyid` para representar la estructura de jerarquía. A continuación, se manipulan los datos de la tabla usando los métodos jerárquicos.  
  
## <a name="requirements"></a>Requisitos  
 El sistema debe tener instalado lo siguiente:  
  
-   Cualquier edición de [!INCLUDE[ssKatmai](../../includes/sskatmai-md.md)] o posterior.  
  
-   [!INCLUDE[ssManStudioFull](../../includes/ssmanstudiofull-md.md)] o [!INCLUDE[ssManStudio](../../includes/ssmanstudio-md.md)] Express.  
  
-   Internet Explorer versión 6 o posterior.  
  
## <a name="see-also"></a>Vea también  
 [Tutorial: Introducción con el motor de base de datos](../tutorial-getting-started-with-the-database-engine.md)   
 [Tutorial: Escribir instrucciones Transact-SQL](../../t-sql/tutorial-writing-transact-sql-statements.md)   
 [Referencia de los métodos del tipo de datos hierarchyid](/sql/t-sql/data-types/hierarchyid-data-type-method-reference)   
 [Datos jerárquicos &#40;SQL Server&#41;](../hierarchical-data-sql-server.md)   
 [hierarchyid &#40;Transact-SQL&#41;](/sql/t-sql/data-types/hierarchyid-data-type-method-reference)  
  
  

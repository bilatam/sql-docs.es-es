---
title: Solucionadores personalizados basados en COM | Microsoft Docs
ms.custom: ''
ms.date: 06/13/2017
ms.prod: sql-server-2014
ms.reviewer: ''
ms.suite: ''
ms.technology:
- replication
ms.tgt_pltfrm: ''
ms.topic: conceptual
helpviewer_keywords:
- COM-based resolvers [SQL Server replication]
- custom resolvers [SQL Server replication]
ms.assetid: 94195797-ad7a-4962-a8e3-b259cd13aa38
caps.latest.revision: 35
author: MashaMSFT
ms.author: mathoma
manager: craigg
ms.openlocfilehash: 9809787b2a674b176bd7ef21a1091aecdd106d6d
ms.sourcegitcommit: c18fadce27f330e1d4f36549414e5c84ba2f46c2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/02/2018
ms.locfileid: "37271171"
---
# <a name="com-based-custom-resolvers"></a>COM-Based Custom Resolvers
  Los solucionadores personalizados proporcionan más flexibilidad que el mecanismo de resolución predeterminado y pueden implementar la lógica de negocios que necesitan las aplicaciones que utilizan los datos replicados. Un solucionador personalizado para COM es una biblioteca de vínculos dinámicos (DLL) que implementa la interfaz COM **ICustomResolver** , sus métodos y propiedades, y otras interfaces de soporte y definiciones de tipos especialmente diseñadas para la resolución de conflictos.  
  
> [!NOTE]  
>  Se recomienda utilizar un controlador de lógica de negocios en lugar de un solucionador personalizado para COM, si es posible. Para obtener más información sobre los controladores de lógica de negocios, consulte [Ejecutar lógica de negocios durante la sincronización de mezcla](execute-business-logic-during-merge-synchronization.md).  
  
 Para crear un solucionador COM personalizado, puede usar la biblioteca de tipos del archivo replrec.dll; de forma predeterminada, esta biblioteca se instala en [!INCLUDE[ssInstallPath](../../../includes/ssinstallpath-md.md)]COM.  
  
 Antes de escribir un solucionador COM personalizado, debe decidir:  
  
-   Los tipos de cambios de fila que desea solucionar, como actualizaciones, inserciones y eliminaciones, y si el solucionador se invocará durante la carga de cambios de mezcla, la descarga, o ambas. Puede especificar un tipo de cambio, todos los cambios o cualquier combinación. El solucionador de conflictos de mezcla predeterminado controla los conflictos que no cubre un solucionador personalizado.  
  
-   Si se utiliza el seguimiento por columnas al solucionar el conflicto. Cuando está activo el seguimiento por columnas, solo se marcan como conflicto las columnas en las que se producen conflictos; los demás datos se mezclan normalmente. Sin embargo, los conflictos se resuelven del mismo modo que con el seguimiento por filas: el ganador por prioridad sobrescribe toda la fila de datos (pero los datos pueden ser una mezcla de valores del publicador, de los suscriptores o algunos valores alterados que no proceden del publicador ni de los suscriptores). Para más información, consulte [Detect and Resolve Merge Replication Conflicts](advanced-merge-replication-resolve-merge-replication-conflicts.md).  
  
 Para implementar un solucionador de conflictos personalizado para COM, vea [Implement a Custom Conflict Resolver for a Merge Article](../implement-a-custom-conflict-resolver-for-a-merge-article.md).  
  
 Un solucionador personalizado se especifica para un artículo y no para una publicación completa. Puede utilizar el mismo solucionador con más de un artículo, pero la lógica de los solucionadores personalizados es con frecuencia específica para una tabla concreta. Si se modifica la tabla utilizada en el artículo después de crear el solucionador (por ejemplo, si se cambia el nombre de la columna que se utiliza en la resolución de conflictos), es posible que necesite modificar y volver a compilar el solucionador personalizado.  
  
 Para especificar un solucionador personalizado, vea [Specify a Merge Article Resolver](../publish/specify-a-merge-article-resolver.md).  
  
## <a name="see-also"></a>Vea también  
 [Advanced Merge Replication Conflict Detection and Resolution](advanced-merge-replication-conflict-detection-and-resolution.md)   
 [Microsoft COM-Based Resolvers](advanced-merge-replication-conflict-com-based-resolvers.md)  
  
  

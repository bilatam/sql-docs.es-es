---
title: Agregar una tabla (SSAS Tabular) | Microsoft Docs
ms.custom: ''
ms.date: 06/13/2017
ms.prod: sql-server-2014
ms.reviewer: ''
ms.suite: ''
ms.technology:
- analysis-services
ms.tgt_pltfrm: ''
ms.topic: conceptual
ms.assetid: d713c432-db99-4983-acc1-52b0fdd58bd6
caps.latest.revision: 4
author: minewiskan
ms.author: owend
manager: craigg
ms.openlocfilehash: 82167dfaa3de6d9312cb3115849aac7a9beaf07b
ms.sourcegitcommit: c18fadce27f330e1d4f36549414e5c84ba2f46c2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/02/2018
ms.locfileid: "37281901"
---
# <a name="add-a-table-ssas-tabular"></a>Agregar una tabla (SSAS tabular)
  En este tema se describe cómo agregar una tabla de un origen de datos del que ha importado datos previamente en el modelo. Para agregar una tabla del mismo origen de datos, puede usar la conexión de origen de datos existente. Se recomienda usar siempre una conexión única al importar cualquier número de tablas de un origen de datos único.  
  
### <a name="to-add-a-table-from-an-existing-data-source"></a>Para agregar una tabla de un origen de datos existente  
  
1.  En [!INCLUDE[ssBIDevStudioFull](../../includes/ssbidevstudiofull-md.md)], haga clic en el menú **Modelo** y, a continuación, en **Conexiones existentes**.  
  
2.  En la página **Conexiones existentes** , seleccione la conexión al origen de datos que tiene la tabla que desea agregar y haga clic en **Abrir**.  
  
3.  En la página **Seleccionar tablas y vistas** , seleccione la tabla del origen de datos que desea agregar al modelo.  
  
    > [!NOTE]  
    >  En la página **Seleccionar tablas y vistas** no se mostrarán las tablas que se importaron previamente como activadas.  Si selecciona una tabla que se importó previamente con esta conexión y no proporcionó a la tabla un nombre descriptivo diferente, se agrega un 1 al nombre descriptivo. No tiene que volver a seleccionar las tablas que se importaron previamente con esta conexión.  
  
4.  En caso necesario, use **Vista previa y filtro** para seleccionar solo algunas columnas o para aplicar filtros a los datos que se van a importar.  
  
5.  Haga clic en **Finalizar** para importar la nueva tabla.  
  
> [!NOTE]  
>  Cuando se importan varias tablas al mismo tiempo desde un único origen de datos, las relaciones entre dichas tablas en el origen se crean automáticamente en el modelo. Sin embargo, cuando posteriormente agregue una tabla, es posible que tenga que crear las relaciones manualmente en el modelo entre las tablas recién agregadas y las tablas que se importaron previamente.  
  
## <a name="see-also"></a>Vea también  
 [Importar datos &#40;Tabular de SSAS&#41;](../import-data-ssas-tabular.md)   
 [Eliminar una tabla &#40;Tabular de SSAS&#41;](delete-a-table-ssas-tabular.md)  
  
  

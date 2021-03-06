---
title: Instrucciones y limitaciones de DiffGrams en SQLXML | Documentos de Microsoft
ms.custom: ''
ms.date: 03/16/2017
ms.prod: sql
ms.prod_service: database-engine, sql-database
ms.component: sqlxml
ms.reviewer: ''
ms.suite: sql
ms.technology: ''
ms.tgt_pltfrm: ''
ms.topic: reference
helpviewer_keywords:
- DiffGrams [SQLXML], about DiffGrams
ms.assetid: cf8689c4-2a63-4d05-b202-21b5ff187d7f
caps.latest.revision: 7
author: douglaslMS
ms.author: douglasl
manager: craigg
monikerRange: =azuresqldb-current||>=sql-server-2016||=sqlallproducts-allversions||>=sql-server-linux-2017
ms.openlocfilehash: d47ff7fb2cfe2cb64a92a17a15b0fff6d4cea1cf
ms.sourcegitcommit: 4cd008a77f456b35204989bbdd31db352716bbe6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/06/2018
ms.locfileid: "39542575"
---
# <a name="guidelines-and-limitations-of-diffgrams-in-sqlxml"></a>Instrucciones y limitaciones de DiffGrams en SQLXML
[!INCLUDE[appliesto-ss-asdb-xxxx-xxx-md](../../../includes/appliesto-ss-asdb-xxxx-xxx-md.md)]
  Recuerde lo siguiente al usar DiffGrams con SQLXML 4.0:  
  
-   Tipos de objeto binario grande (BLOB) como **texto/ntext** y no se deben usar imágenes en el  **\<diffgr: antes de >** bloquear al trabajar con DiffGrams, porque esto los incluiría para su uso en control de simultaneidad. Esto puede producir problemas con [!INCLUDE[ssNoVersion](../../../includes/ssnoversion-md.md)] debido a las limitaciones en la comparación para los tipos BLOB. Por ejemplo, la palabra clave LIKE se usa en la cláusula WHERE para comparar entre las columnas de la **texto** de tipo de datos; sin embargo, las comparaciones se producirá un error en el caso de los tipos BLOB donde el tamaño de los datos es mayor que 8 KB.  
  
-   Caracteres especiales en **ntext** datos pueden causar problemas con SQLXML 4.0 debido a las limitaciones en la comparación para los tipos de BLOB. Por ejemplo, el uso de "[Serializable]" en el  **\<diffgr: antes de >** bloque de un DiffGram cuando se utiliza en la comprobación de simultaneidad de una columna de **ntext** se producirá un error de tipo con SQLOLEDB siguiente Descripción del error:  
  
    ```  
    Empty update, no updatable rows found   Transaction aborted  
    ```  
  
  

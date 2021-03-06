---
title: Palabras reservadas (Master Data Services) | Microsoft Docs
ms.custom: ''
ms.date: 03/06/2017
ms.prod: sql-server-2014
ms.reviewer: ''
ms.suite: ''
ms.technology:
- master-data-services
ms.tgt_pltfrm: ''
ms.topic: conceptual
helpviewer_keywords:
- reserved words [Master Data Services]
- Master Data Services, reserved words
ms.assetid: 88afd0d0-4362-4394-8357-4e65388fc0fc
caps.latest.revision: 8
author: leolimsft
ms.author: lle
manager: craigg
ms.openlocfilehash: 2aaee670cd89e957a6ad4700963606ffe0d4ef4f
ms.sourcegitcommit: c18fadce27f330e1d4f36549414e5c84ba2f46c2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/02/2018
ms.locfileid: "37221675"
---
# <a name="reserved-words-master-data-services"></a>Palabras reservadas (Master Data Services)
  En [!INCLUDE[ssMDSshort](../includes/ssmdsshort-md.md)], al crear objetos del modelo o miembros, algunas palabras no se pueden usar. Su uso puede producir errores.  
  
> [!NOTE]  
>  También debe limitar el uso de caracteres especiales (símbolos, guiones, etc.).  
  
-   [Modelos](#models)  
  
-   [Entidades](#entities)  
  
-   [Jerarquías explícitas](#exhierarchies)  
  
-   [Atributos](#attributes)  
  
-   [Miembros](#members)  
  
##  <a name="models"></a> Modelos  
 Si crea un modelo con el nombre establecido en **nombre**, no seleccione **crear entidad con el mismo nombre que el modelo** porque **nombre** no se puede usar para el nombre de una entidad.  
  
##  <a name="entities"></a> Entidades  
 Para los nombres de entidad, no puede usar **Name** o **Code**.  
  
##  <a name="exhierarchies"></a> Jerarquías explícitas  
 Para los nombres de jerarquía explícita, no puede utilizar **Name** o **Code**.  
  
##  <a name="attributes"></a> Atributos  
  
-   **ID**  
  
-   **Code**  
  
-   **Nombre**  
  
-   **EnterDTM**  
  
-   **EnterUserID**  
  
-   **EnterUserName**  
  
-   **LastChgDTM**  
  
-   **LastChgUserID**  
  
-   **Status_ID**  
  
-   **ValidationStatus_ID**  
  
-   **Version_ID**  
  
##  <a name="members"></a> Miembros  
 Para los miembros, no puede usar **MDMMemberStatus** o **raíz** para el **código** valor del atributo.  
  
## <a name="see-also"></a>Vea también  
 [Introducción a Master Data Services](master-data-services-overview-mds.md)  
  
  

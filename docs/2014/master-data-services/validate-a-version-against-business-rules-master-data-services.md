---
title: Validar una versión con las reglas de negocios (Master Data Services) | Microsoft Docs
ms.custom: ''
ms.date: 06/14/2017
ms.prod: sql-server-2014
ms.reviewer: ''
ms.suite: ''
ms.technology:
- master-data-services
ms.tgt_pltfrm: ''
ms.topic: conceptual
helpviewer_keywords:
- validating versions [Master Data Services]
- validating versions [Master Data Services], about validating versions
- versions [Master Data Services], validating
- business rules [Master Data Services], applying to all members
ms.assetid: 5aee7901-6d05-41d4-8bbb-c6f26791d1df
caps.latest.revision: 7
author: leolimsft
ms.author: lle
manager: craigg
ms.openlocfilehash: 8b40c03711cea6e6bf840bdb9ce63fa9cf6e302a
ms.sourcegitcommit: c18fadce27f330e1d4f36549414e5c84ba2f46c2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/02/2018
ms.locfileid: "37296545"
---
# <a name="validate-a-version-against-business-rules-master-data-services"></a>Validar una versión con las reglas de negocios (Master Data Services)
  En [!INCLUDE[ssMDSshort](../includes/ssmdsshort-md.md)], valide una versión para aplicar las reglas de negocios a todos los miembros de la versión del modelo.  
  
 En este procedimiento se explica cómo usar la aplicación web de [!INCLUDE[ssMDSmdm](../includes/ssmdsmdm-md.md)] para validar datos. Si tiene permisos en la base de datos de MDS, puede usar un procedimiento almacenado en su lugar. Para obtener más información, consulte [Validation Stored Procedure &#40;Master Data Services&#41;](validation-stored-procedure-master-data-services.md).  
  
> [!NOTE]  
>  Todos los miembros deben superar la validación antes de que se pueda confirmar una versión.  
  
## <a name="prerequisites"></a>Requisitos previos  
 Para realizar este procedimiento:  
  
-   Debe disponer del permiso para tener acceso al área funcional de **Administración de versiones** .  
  
-   Debe ser administrador de modelo. Para obtener más información, vea [Administrators &#40;Master Data Services&#41;](../../2014/master-data-services/administrators-master-data-services.md).  
  
-   El estado de la versión debe ser **Abrir** o **Bloqueado**.  
  
-   En la página **Validar versiones** , los miembros deben existir con un estado que no sea **Validación correcta**.  
  
### <a name="to-validate-a-version"></a>Validar una versión  
  
1.  En [!INCLUDE[ssMDSmdm](../includes/ssmdsmdm-md.md)], haga clic en **Administración de versiones**.  
  
2.  En la página **Administrar versiones** , en la barra de menús, haga clic en **Validar versión**.  
  
3.  En la página **Validar versiones** , seleccione el modelo y la versión que desea validar.  
  
4.  Haga clic en **Validar**.  
  
5.  En el cuadro de diálogo de confirmación, haga clic en **Aceptar**.  
  
    > [!NOTE]  
    >  Cuando ya no se muestre el indicador de progreso, la validación de la versión habrá terminado.  
  
## <a name="next-steps"></a>Pasos siguientes  
  
-   [Bloquear una versión &#40;Master Data Services&#41;](../../2014/master-data-services/lock-a-version-master-data-services.md)  
  
## <a name="see-also"></a>Vea también  
 [Estados de validación &#40;Master Data Services&#41;](../../2014/master-data-services/validation-statuses-master-data-services.md)   
 [Procedimiento almacenado de validación &#40;Master Data Services&#41;](validation-stored-procedure-master-data-services.md)   
 [Las versiones &#40;Master Data Services&#41;](../../2014/master-data-services/versions-master-data-services.md)   
 [Las reglas de negocios &#40;Master Data Services&#41;](../../2014/master-data-services/business-rules-master-data-services.md)   
 [Validar miembros específicos con las reglas de negocios &#40;Master Data Services&#41;](../../2014/master-data-services/validate-specific-members-against-business-rules-master-data-services.md)  
  
  

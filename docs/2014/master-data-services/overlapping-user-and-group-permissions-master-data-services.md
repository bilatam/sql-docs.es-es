---
title: Superponer permisos de usuario y de grupo (Master Data Services) | Microsoft Docs
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
- users [Master Data Services], resolving permissions
- permissions [Master Data Services], user and group overlaps
- groups [Master Data Services], resolving permissions
ms.assetid: 31c3cf7d-17d4-4474-b6a7-ffcb9fc45b37
caps.latest.revision: 5
author: leolimsft
ms.author: lle
manager: craigg
ms.openlocfilehash: 06b8f48e1f2b7c246c1f5e4559bbbba851ccf128
ms.sourcegitcommit: c18fadce27f330e1d4f36549414e5c84ba2f46c2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/02/2018
ms.locfileid: "37264941"
---
# <a name="overlapping-user-and-group-permissions-master-data-services"></a>Superponer permisos de usuario y de grupo (Master Data Services)
  Los permisos de un usuario se basan en:  
  
-   Permisos de las pertenencias a grupos.  
  
-   Permisos asignados explícitamente al usuario.  
  
 Si un usuario es miembro de varios grupos y dichos grupos tienen acceso al Administrador de datos maestros, se aplican las siguientes reglas:  
  
-   **Denegar** invalida al resto de permisos.  
  
-   **Actualización** invalida **de sólo lectura**.  
  
 Estas reglas se aplican a las pestañas **Modelos** y **Miembros de la jerarquía** . Los permisos se resuelven para cada pestaña y, a continuación, se combinan. Para obtener más información, consulte [How Permissions Are Determined &#40;Master Data Services&#41;](how-permissions-are-determined-master-data-services.md).  
  
> [!NOTE]  
>  Puede ver la resolución de los permisos superpuestos de usuario y de grupo en la interfaz de usuario. Las pestañas **Modelos** y **Miembros de la jerarquía** tienen una lista desplegable en la que puede elegir **Vigente** para ver los permisos vigentes.  
  
## <a name="example-1"></a>Ejemplo 1  
 ![mds_conc_user_group_ex_1](../../2014/master-data-services/media/mds-conc-user-group-ex-1.gif "mds_conc_user_group_ex_1")  
  
 El usuario pertenece a Grupo 1 y Grupo 2.  
  
 El usuario tiene **de sólo lectura** permiso para la entidad Product.  
  
 El Grupo 1 tiene el permiso **Actualizar** para la entidad Product.  
  
 Grupo 2 tiene **de sólo lectura** permiso para la entidad Product.  
  
 Resultado: el permiso vigente del usuario para la entidad Product es **Actualizar** .  
  
## <a name="example-2"></a>Ejemplo 2  
 ![mds_conc_user_group_ex_2](../../2014/master-data-services/media/mds-conc-user-group-ex-2.gif "mds_conc_user_group_ex_2")  
  
 El usuario pertenece a Grupo 1 y Grupo 2.  
  
 El usuario tiene **de sólo lectura** permiso para la entidad Product.  
  
 El Grupo 1 tiene el permiso **Actualizar** para la entidad Product.  
  
 El Grupo 2 tiene el permiso **Denegar** para la entidad Product.  
  
 Resultado: el permiso vigente del usuario para la entidad Product es **Denegar** .  
  
## <a name="example-3"></a>Ejemplo 3  
 ![mds_conc_user_group_ex_3](../../2014/master-data-services/media/mds-conc-user-group-ex-3.gif "mds_conc_user_group_ex_3")  
  
 El usuario pertenece a Grupo 1 y Grupo 2.  
  
 El usuario tiene el permiso **Actualizar** para un grupo de miembros en un nodo de jerarquía.  
  
 Grupo 1 tiene **de sólo lectura** permiso a un grupo de miembros en un nodo de jerarquía.  
  
 Grupo 2 tiene **de sólo lectura** permiso a un grupo de miembros en un nodo de jerarquía.  
  
 Resultado: el permiso vigente del usuario para los miembros es **Actualizar** .  
  
## <a name="see-also"></a>Vea también  
 [¿Cómo se determinan los permisos &#40;Master Data Services&#41;](how-permissions-are-determined-master-data-services.md)   
 [Superponer permisos de modelo y de miembro &#40;Master Data Services&#41;](../../2014/master-data-services/overlapping-model-and-member-permissions-master-data-services.md)  
  
  

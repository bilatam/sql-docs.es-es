---
title: Tareas de nivel de sistema | Microsoft Docs
ms.custom: ''
ms.date: 06/13/2017
ms.prod: sql-server-2014
ms.reviewer: ''
ms.suite: ''
ms.technology:
- reporting-services-native
ms.tgt_pltfrm: ''
ms.topic: conceptual
helpviewer_keywords:
- system-level tasks [Reporting Services]
ms.assetid: 7023b388-40b2-4590-b227-115cf380a1e7
caps.latest.revision: 35
author: markingmyname
ms.author: maghan
manager: craigg
ms.openlocfilehash: 284349672feca872e8f9b704314ae070ec687df7
ms.sourcegitcommit: c18fadce27f330e1d4f36549414e5c84ba2f46c2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/02/2018
ms.locfileid: "37229005"
---
# <a name="system-level-tasks"></a>Tareas de nivel de sistema
  Una tarea de nivel de sistema es una colección de permisos relativos a las operaciones correspondientes al sitio del servidor de informes en general. [!INCLUDE[ssRSnoversion](../../includes/ssrsnoversion-md.md)] también incluye tareas de nivel de elemento que corresponden a elementos específicos. Para obtener más información, vea [Tareas de nivel de elemento](tasks-and-permissions-item-level-tasks.md). Para obtener más información sobre las tareas y permisos en general, consulte [tareas y permisos](tasks-and-permissions.md).  
  
> [!NOTE]  
>  Si trabaja con estas tareas mediante programación, debe utilizar métodos que admitan tareas de nivel de sistema. Para obtener más información, vea <xref:ReportService2010.ReportingService2010.ListTasks%2A> y <xref:ReportService2010.ReportingService2010.ListRoles%2A>.  
  
## <a name="permissions-in-system-level-tasks"></a>Permisos en tareas de nivel de sistema  
 La siguiente tabla identifica la colección de permisos para cada tarea del sistema. Los permisos se incluyen con fin informativo únicamente, para proporcionar una descripción más exacta de la funcionalidad disponible con cada tarea.  
  
|Tarea|Permisos|  
|----------|-----------------|  
|Ejecutar definiciones de informe|Ejecutar definiciones de informe (el nombre del permiso y la tarea es el mismo)|  
|Generar eventos|Generar eventos|  
|Administrar trabajos|Leer propiedades del sistema<br /><br /> Actualizar propiedades del sistema|  
|Administrar propiedades del servidor de informes|Leer propiedades del sistema<br /><br /> Actualizar propiedades del sistema|  
|Administrar roles|Crear roles<br /><br /> Eliminar roles<br /><br /> Leer propiedades de roles<br /><br /> Actualizar propiedades de roles|  
|Administrar programaciones compartidas|Crear programaciones|  
|Administrar la seguridad del servidor de informes|Leer directivas de seguridad del sistema<br /><br /> Actualizar directivas de seguridad del sistema|  
|Ver propiedades del servidor de informes|Leer propiedades del sistema|  
|Ver programaciones compartidas|Leer programaciones|  
  
## <a name="see-also"></a>Vea también  
 [Concesión de permisos en un servidor de informes en modo nativo](granting-permissions-on-a-native-mode-report-server.md)  
  
  

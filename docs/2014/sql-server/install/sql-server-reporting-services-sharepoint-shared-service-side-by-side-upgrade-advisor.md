---
title: Microsoft SQL Server Reporting Services servicio compartido de SharePoint está instalado en paralelo (Asesor de actualizaciones) | Microsoft Docs
ms.custom: ''
ms.date: 03/06/2017
ms.prod: sql-server-2014
ms.reviewer: ''
ms.suite: ''
ms.technology:
- database-engine
ms.tgt_pltfrm: ''
ms.topic: conceptual
ms.assetid: 6ae1017e-129b-4702-9ea7-00ac9b024062
caps.latest.revision: 6
author: markingmyname
ms.author: maghan
manager: craigg
ms.openlocfilehash: 97e0345a38148e02e7f7e73852284887b66b2ccc
ms.sourcegitcommit: c18fadce27f330e1d4f36549414e5c84ba2f46c2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/02/2018
ms.locfileid: "37206395"
---
# <a name="microsoft-sql-server-reporting-services-sharepoint-shared-service-is-installed-side-by-side-upgrade-advisor"></a>El servicio compartido de SharePoint de Microsoft SQL Server Reporting Services está instalado en paralelo (Asesor de actualizaciones)
  Asesor de actualizaciones ha detectado [!INCLUDE[msCoName](../../includes/msconame-md.md)] [!INCLUDE[ssRSnoversion](../../includes/ssrsnoversion-md.md)] servicio compartido de SharePoint se instala en paralelo con una versión anterior de [!INCLUDE[ssRSnoversion](../../includes/ssrsnoversion-md.md)].  
  
||  
|-|  
|**[!INCLUDE[applies](../../includes/applies-md.md)]**  [!INCLUDE[ssRSnoversion](../../includes/ssrsnoversion-md.md)] Modo de SharePoint.|  
  
## <a name="component"></a>Componente  
 [!INCLUDE[ssRSnoversion](../../includes/ssrsnoversion-md.md)]  
  
## <a name="description"></a>Descripción  
 Asesor de actualizaciones ha detectado [!INCLUDE[msCoName](../../includes/msconame-md.md)] [!INCLUDE[ssRSnoversion](../../includes/ssrsnoversion-md.md)] servicio compartido de SharePoint se instala en paralelo con una versión anterior de [!INCLUDE[ssRSnoversion](../../includes/ssrsnoversion-md.md)] que no se basa en la arquitectura del servicio compartido de SharePoint. La actualización se ha bloqueado porque en el equipo existen tecnologías antiguas y nuevas relacionadas con SharePoint de [!INCLUDE[ssRSnoversion](../../includes/ssrsnoversion-md.md)] instaladas en paralelo.  
  
## <a name="corrective-action"></a>Acción correctora  
 Para continuar con la actualización, debe desinstalar una de las instalaciones existentes de [!INCLUDE[ssRSnoversion](../../includes/ssrsnoversion-md.md)]. Después de quitar una de las instalaciones de [!INCLUDE[ssRSnoversion](../../includes/ssrsnoversion-md.md)], vuelva a ejecutar el Asesor de actualizaciones para confirmar que no hay ningún otro problema con la actualización.  
  
  

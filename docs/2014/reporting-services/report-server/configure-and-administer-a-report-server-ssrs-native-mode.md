---
title: Configurar y administrar un servidor de informes (modo nativo de SSRS) | Microsoft Docs
ms.custom: ''
ms.date: 08/10/2017
ms.prod: sql-server-2014
ms.reviewer: ''
ms.suite: ''
ms.technology:
- reporting-services-native
ms.tgt_pltfrm: ''
ms.topic: conceptual
helpviewer_keywords:
- Reporting Services, components
- deploying [Reporting Services], component options
- report servers [Reporting Services], component options
- configuration options [Reporting Services]
- administering Reporting Services
- components [Reporting Services], configuring
- configuring servers [Reporting Services]
ms.assetid: cfec012b-56f1-4346-9814-247acf22351c
caps.latest.revision: 50
author: markingmyname
ms.author: maghan
manager: craigg
ms.openlocfilehash: 296bc51f6a3793d0a37e3b730152f4292c799be1
ms.sourcegitcommit: c18fadce27f330e1d4f36549414e5c84ba2f46c2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/02/2018
ms.locfileid: "37295825"
---
# <a name="configure-and-administer-a-report-server-ssrs-native-mode"></a>Configurar y administrar un servidor de informes (modo nativo de SSRS)
  En este tema se resumen los métodos que se pueden usar para configurar [!INCLUDE[ssRSnoversion](../../includes/ssrsnoversion-md.md)]. También se incluye una lista de temas en los que se explica cómo configurar determinados componentes, características o funciones del servidor. Para configurar [!INCLUDE[ssRSnoversion](../../includes/ssrsnoversion-md.md)], puede:  
  
-   Usar el Administrador de configuración de Reporting Services. En muchos de los temas de esta sección se proporciona información acerca de la configuración de determinadas características mediante esta herramienta.  
  
-   Use [!INCLUDE[ssManStudio](../../includes/ssmanstudio-md.md)] para personalizar las propiedades del servidor, habilitar Mis informes, habilitar los registros de seguimiento y establecer los valores predeterminados de todo el sitio. Para obtener más información acerca de la configuración del sitio, consulte [Reporting Services Report Server &#40;modo nativo&#41; ](reporting-services-report-server-native-mode.md) para Management Studio. Tenga en cuenta que se puede crear y ejecutar un script que establece las propiedades del servidor mediante programación. Para obtener más información, consulte [tareas administrativas e implementación de secuencia de comandos](../tools/script-deployment-and-administrative-tasks.md) y [Report Server System Properties](../report-server-web-service/net-framework/reporting-services-properties-report-server-system-properties.md).  
  
-   Use el Administrador de informes para conceder permisos para tener acceso al servidor de informes. Los permisos se conceden a través de las asignaciones de roles que define para cada cuenta de grupo o usuario. Para obtener más información, vea [Roles y permisos &#40;Reporting Services&#41;](../security/roles-and-permissions-reporting-services.md).  
  
-   También puede modificar archivos de configuración para cambiar la configuración de la aplicación. Para obtener más información acerca de cada archivo así como directrices para modificarlos, vea [Reporting Services Configuration Files](reporting-services-configuration-files.md).  
  
## <a name="in-this-section"></a>En esta sección  
 [Configurar las direcciones URL del servidor de informes &#40;Administrador de configuración de SSRS&#41;](../install-windows/configure-report-server-urls-ssrs-configuration-manager.md)  
 Describe cómo definir las direcciones URL que se usan para tener acceso al servidor de informes y al Administrador de informes.  
  
 [Configurar la cuenta de servicio del servidor de informes &#40;Administrador de configuración de SSRS&#41;](../install-windows/configure-the-report-server-service-account-ssrs-configuration-manager.md)  
 Proporciona recomendaciones y pasos sobre cómo modificar la contraseña y la cuenta de servicio.  
  
 [Crear una base de datos del servidor de informes &#40;Administrador de configuración de SSRS&#41;](../../sql-server/install/create-a-report-server-database-ssrs-configuration-manager.md)  
 Describe cómo crear una base de datos del servidor de informes, necesaria para almacenar objetos y metadatos de servidor.  
  
 [Configurar una conexión de base de datos del servidor de informes &#40;Administrador de configuración de SSRS&#41;](../../sql-server/install/configure-a-report-server-database-connection-ssrs-configuration-manager.md)  
 Describe cómo modificar la cadena de conexión que utiliza el servidor de informes para conectarse a la base de datos del servidor de informes.  
  
 [Configurar un servidor de informes para la entrega de correo electrónico &#40;Administrador de configuración de SSRS&#41;](../../sql-server/install/configure-a-report-server-for-e-mail-delivery-ssrs-configuration-manager.md)  
 Describe cómo configurar un servidor de informes para permitir la distribución de informes por correo electrónico.  
  
 [Configurar la cuenta de ejecución desatendida &#40;Administrador de configuración de SSRS&#41;](../install-windows/configure-the-unattended-execution-account-ssrs-configuration-manager.md)  
 Describe cómo configurar una cuenta de usuario para procesar informes en modo desatendido.  
  
## <a name="see-also"></a>Vea también  
 [Configurar el acceso al generador de informes](configure-report-builder-access.md)   
 [Archivos de configuración de Reporting Services](reporting-services-configuration-files.md)   
 [Administrador de configuración de Reporting Services &#40;modo nativo&#41;](../../sql-server/install/reporting-services-configuration-manager-native-mode.md)   
 [Seguridad y protección de Reporting Services](../security/reporting-services-security-and-protection.md)   
 [Servidor de informes de Reporting Services &#40;modo nativo&#41;](reporting-services-report-server-native-mode.md)  
  
  

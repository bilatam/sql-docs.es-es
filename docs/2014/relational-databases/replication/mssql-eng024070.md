---
title: MSSQL_ENG024070 | Microsoft Docs
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
- MSSQL_ENG024070 error
ms.assetid: 23ac7e00-fab6-429b-9f85-2736a322aa65
caps.latest.revision: 12
author: MashaMSFT
ms.author: mathoma
manager: craigg
ms.openlocfilehash: c1d2141f51c0434fb0c03dee6c1a07875b8150f0
ms.sourcegitcommit: c18fadce27f330e1d4f36549414e5c84ba2f46c2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/02/2018
ms.locfileid: "37305415"
---
# <a name="mssqleng024070"></a>MSSQL_ENG024070
    
## <a name="message-details"></a>Detalles del mensaje  
  
|||  
|-|-|  
|Nombre del producto|SQL Server|  
|Identificador del evento|24070|  
|Origen del evento|MSSQLSERVER|  
|Componente|[!INCLUDE[ssDEnoversion](../../includes/ssdenoversion-md.md)]|  
|Nombre simbólico||  
|Texto del mensaje|El cliente no dispone de un privilegio requerido.|  
  
## <a name="explanation"></a>Explicación  
 Se trata de un error general que puede producirse independientemente de que se esté usando replicación o no. Para un servidor de una topología de replicación, el error suele producirse porque la cuenta del servicio del Agente [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] se cambia con el Administrador de control de servicios de [!INCLUDE[msCoName](../../includes/msconame-md.md)] Windows en lugar del Administrador de configuración de [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] . Si intenta ejecutar un trabajo de agente después de cambiar la cuenta de servicio, es posible que el trabajo no progrese y aparezca un mensaje de error similar al siguiente:  
  
 "Ejecutado como usuario: \<cuentaDeUsuario >. Subsistema de instantánea de replicación: agente \<Nombreagente > no se pudo. Ejecutado como usuario: \<cuentaDeUsuario >. El cliente no dispone de un privilegio requerido. Error en el paso. `[SQLSTATE 42000] (Error 14151)`. Error en el paso."  
  
 Este problema se produce porque el Administrador de control de servicios de Windows no puede conceder los permisos necesarios a la nueva cuenta de servicio para el Agente [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] .  
  
## <a name="user-action"></a>Acción del usuario  
 Para evitar este problema en el futuro, utilice siempre el Administrador de configuración de [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] en lugar del Administrador de control de servicios de Windows para cambiar las cuentas de servicio y las contraseñas.  
  
 Para resolver este problema, utilice el Administrador de configuración de [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] para cambiar la cuenta de servicio a la cuenta original. A continuación, use el Administrador de configuración de [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] para cambiar a la nueva cuenta. Al hacer esto, el Administrador de configuración de [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] agrega la nueva cuenta al siguiente grupo de seguridad:  
  
 SQLServer2008SQLAgentUser$ComputerName$InstanceName  
  
 Como miembro de este grupo de seguridad, se conceden a la nueva cuenta los permisos necesarios para ejecutar el trabajo del agente de replicación.  
  
## <a name="see-also"></a>Vea también  
 [Referencia de errores y eventos &#40;replicación&#41;](errors-and-events-reference-replication.md)   
 [Administrar inicios de sesión y contraseñas en la replicación](security/manage-logins-and-passwords-in-replication.md)   
 [Administrador de configuración de SQL Server](../sql-server-configuration-manager.md)  
  
  

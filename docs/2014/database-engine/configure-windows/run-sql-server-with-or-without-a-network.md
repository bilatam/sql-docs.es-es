---
title: Ejecutar SQL Server con o sin red | Microsoft Docs
ms.custom: ''
ms.date: 03/06/2017
ms.prod: sql-server-2014
ms.reviewer: ''
ms.suite: ''
ms.technology:
- database-engine
ms.tgt_pltfrm: ''
ms.topic: conceptual
helpviewer_keywords:
- verifying Server service has been started
- net start [SQL Server]
- command prompt [SQL Server], connections
- SQL Server services, networks
- status information [SQL Server], Server service
- running SQL Server
- networking [SQL Server], SQL Server with or without
- services [SQL Server], networks
- starting Server service
- SQL Server, running
ms.assetid: 54eac961-5c7a-4481-982d-f93a64b5c2f4
caps.latest.revision: 24
author: MikeRayMSFT
ms.author: mikeray
manager: craigg
ms.openlocfilehash: 54718a326946a454d132236964ede6b83811db6a
ms.sourcegitcommit: c18fadce27f330e1d4f36549414e5c84ba2f46c2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/02/2018
ms.locfileid: "37245535"
---
# <a name="run-sql-server-with-or-without-a-network"></a>Ejecutar SQL Server con o sin red
  [!INCLUDE[msCoName](../../includes/msconame-md.md)] [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] se puede ejecutar en una red o puede funcionar sin ella.  
  
## <a name="running-sql-server-on-a-network"></a>Ejecutar SQL Server en una red  
 Para que [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] pueda comunicarse a través de una red, el servicio [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] debe estar en ejecución. De forma predeterminada, [!INCLUDE[msCoName](../../includes/msconame-md.md)] Windows inicia automáticamente el servicio [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] integrado. Para averiguar si se ha iniciado el servicio [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] , en el símbolo del sistema, escriba:  
  
 **net start**  
  
 Si los servicios asociados con [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] se han iniciado, los siguientes servicios aparecerán en la salida del comando **net start** :  
  
-   Analysis Services (MSSQLSERVER)  
  
-   SQL Server (MSSQLSERVER)  
  
-   Agente SQL Server (MSSQLSERVER)  
  
## <a name="running-sql-server-without-a-network"></a>Ejecutar SQL Server sin una red  
 Cuando se ejecuta una instancia de [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] sin una red, no es necesario iniciar el servicio integrado [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] . Puesto que [!INCLUDE[ssManStudioFull](../../includes/ssmanstudiofull-md.md)], el Administrador de configuración de SQL Server y los comandos **net start** y **net stop** funcionan siempre, incluso sin una red, los procedimientos para iniciar y detener una instancia de [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] son los mismos para el funcionamiento independiente o con red.  
  
 Al conectarse a una instancia de un servidor [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] independiente desde un cliente local, por ejemplo **sqlcmd**, se omite la red y se conecta directamente a la instancia de [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] mediante una canalización local. La diferencia entre una canalización local y una canalización de red es que en la primera no se utiliza la red y en la segunda sí. Ambas canalizaciones establecen una conexión con una instancia de [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] mediante la canalización estándar (\\\\.\pipe\sql\query), a menos que se indique otra cosa.  
  
 Cuando se conecta a una instancia de un servidor [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] local sin especificar un nombre de servidor, se utiliza una canalización local. Si se conecta a una instancia de un servidor [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] local y se especifica explícitamente un nombre de servidor, se utiliza una canalización de red u otro mecanismo de comunicación entre procesos (IPC) de red, como IPX/SPX, suponiendo que se haya configurado [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] para utilizar varias redes. Como un servidor [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] independiente no admite canalizaciones de red, debe omitir el argumento **/***<nombre_de_servidor>*, que resulta innecesario, cuando se conecte a la instancia de [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] desde un cliente. Por ejemplo, para conectarse a una instancia independiente de [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] desde **osql**, escriba:  
  
 **osql /Usa /P** *\<saPassword>*  
  
  

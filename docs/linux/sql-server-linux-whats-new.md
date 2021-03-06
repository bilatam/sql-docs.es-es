---
title: Novedades de SQL Server 2017 en Linux | Microsoft Docs
description: Este artículo resalta cuáles son las novedades de SQL Server 2017 en Linux.
author: rothja
ms.author: jroth
manager: craigg
ms.date: 02/20/2018
ms.topic: conceptual
ms.prod: sql
ms.component: ''
ms.suite: sql
ms.custom: sql-linux
ms.technology: linux
ms.assetid: 456b6f31-6b97-4e31-80ab-b40151ec4868
ms.openlocfilehash: c4390990701f95dddf19ca53354ffcb5af241d30
ms.sourcegitcommit: c8f7e9f05043ac10af8a742153e81ab81aa6a3c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/17/2018
ms.locfileid: "39083537"
---
# <a name="whats-new-for-sql-server-2017-on-linux"></a>Novedades de SQL Server 2017 en Linux

[!INCLUDE[appliesto-ss-xxxx-xxxx-xxx-md-linuxonly](../includes/appliesto-ss-xxxx-xxxx-xxx-md-linuxonly.md)]

Este artículo describe las principales características y servicios disponibles para SQL Server 2017 en Linux.

> [!NOTE]
> Además de estas funcionalidades en este artículo, se publican actualizaciones acumulativas a intervalos regulares después del lanzamiento de GA. Estas actualizaciones acumulativas proporcionan muchas mejoras y correcciones. Para obtener información acerca de la versión de la CU más reciente, consulte [ http://aka.ms/sql2017cu ](http://aka.ms/sql2017cu). Para descargar los paquetes y los problemas conocidos, vea el [notas de la versión](sql-server-linux-release-notes.md).

## <a name="sql-server-database-engine"></a>Motor de base de datos de SQL Server

- Habilitar las capacidades del motor de base de datos de SQL Server core.
- Compatibilidad con rutas de acceso nativas de Linux.
- Compatibilidad con IPv6.
- Compatibilidad con archivos de base de datos en NFS.
- Habilitado [seguridad transparente de la capa](sql-server-linux-encrypted-connections.md) cifrado (TLS).
- Habilitado [autenticación de Active Directory](sql-server-linux-active-directory-authentication.md).
- [La funcionalidad de grupos de disponibilidad](sql-server-linux-availability-group-overview.md) para lograr alta disponibilidad.
- [Búsqueda de texto completo](sql-server-linux-setup-full-text-search.md) admite.

## <a name="sql-server-agent"></a>Agente SQL Server

- Habilitado [del Agente SQL Server](sql-server-linux-setup-sql-agent.md) compatibilidad con las siguientes tareas:
  - [Trabajos de Transact-SQL](sql-server-linux-run-sql-server-agent-job.md)
  - [Correo electrónico de base de datos](sql-server-linux-db-mail-sql-agent.md)
  - [Trasvase de registros](sql-server-linux-use-log-shipping.md)

## <a name="sql-server-integration-services-ssis"></a>SQL Server Integration Services (SSIS)

- Capacidad para ejecutar paquetes SSIS en Linux. Para obtener más información, consulte [configurar SQL Server Integration Services en Linux con ssis-conf](sql-server-linux-configure-ssis.md).

## <a name="other-improvements"></a>Otras mejoras

- Herramienta de configuración de línea de comandos, [mssql-conf](sql-server-linux-configure-mssql-conf.md).
- Compatibilidad con la instalación desatendida con [variables de entorno](sql-server-linux-configure-environment-variables.md).
- Multiplataforma [extensión de Visual Studio Code mssql-server](sql-server-linux-develop-use-vscode.md).
- Generador de secuencias de comandos entre plataformas, [mssql scripter](https://github.com/Microsoft/sql-xplat-cli/blob/dev/doc/usage_guide.md).
- Monitor de vista de administración dinámica (DMV) multiplataforma, [herramienta DBFS](https://github.com/Microsoft/dbfs).

## <a name="next-steps"></a>Pasos siguientes

Para instalar a SQL Server en Linux, use uno de los siguientes tutoriales:

- [Instalación en Red Hat Enterprise Linux](quickstart-install-connect-red-hat.md)
- [Instalación en SUSE Linux Enterprise Server](quickstart-install-connect-suse.md)
- [Instalar en Ubuntu](quickstart-install-connect-ubuntu.md)
- [Ejecutar en Docker](quickstart-install-connect-docker.md)
- [Aprovisionar una máquina virtual de SQL en Azure](/azure/virtual-machines/linux/sql/provision-sql-server-linux-virtual-machine?toc=%2fsql%2flinux%2ftoc.json)

Para ver otras mejoras introducidas en SQL Server 2017, consulte [What ' s New in SQL Server 2017](../sql-server/what-s-new-in-sql-server-2017.md).

> [!TIP]
> Para obtener respuestas a las preguntas más frecuentes, consulte el [SQL Server en Linux preguntas más frecuentes sobre](sql-server-linux-faq.md).

[!INCLUDE[get-help-options](../includes/paragraph-content/get-help-options.md)]

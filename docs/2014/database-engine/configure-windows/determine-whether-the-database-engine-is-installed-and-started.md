---
title: Determinar si el motor de base de datos está instalado y se ha iniciado | Microsoft Docs
ms.custom: ''
ms.date: 06/13/2017
ms.prod: sql-server-2014
ms.reviewer: ''
ms.suite: ''
ms.technology:
- database-engine
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- SQL Server, determining if installed
- verifying Database Engine installation
- viewing Database Engine installation
- installed Database Engine verification [SQL Server]
ms.assetid: babb02e4-3521-4b75-b5df-e09205594375
caps.latest.revision: 16
author: craigg-msft
ms.author: craigg
manager: jhubbard
ms.openlocfilehash: fd18e0df83b3492a5880630787cc815c195166b6
ms.sourcegitcommit: 5dd5cad0c1bbd308471d6c885f516948ad67dfcf
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2018
ms.locfileid: "36201874"
---
# <a name="determine-whether-the-database-engine-is-installed-and-started"></a>Determinar si el motor de base de datos está instalado y se ha iniciado
  En una instalación correcta de [!INCLUDE[ssDEnoversion](../../includes/ssdenoversion-md.md)] se instalan archivos en el sistema de archivos, se crean entradas en el Registro y se instalan varias herramientas. En este tema se describe cómo determinar si el [!INCLUDE[ssDE](../../includes/ssde-md.md)] se instala e inicia en [!INCLUDE[ssCurrent](../../includes/sscurrent-md.md)] mediante el Administrador de configuración de [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] .  
  
##  <a name="SSMSProcedure"></a> Usar el Administrador de configuración de SQL Server  
  
#### <a name="how-to-view-and-start-the-database-engine-by-using-sql-server-configuration-manager"></a>Cómo ver e iniciar el motor de base de datos con el Administrador de configuración de SQL Server  
  
1.  En el menú **Inicio**, seleccione **Todos los programas**, **Microsoft SQL Server**, **Herramientas de configuración**y, finalmente, **Administrador de configuración de SQL Server**.  
  
     Si no tiene estas entradas en el menú **Inicio** , [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] no está instalado correctamente. Ejecute el programa de instalación para instalar [!INCLUDE[ssDEnoversion](../../includes/ssdenoversion-md.md)].  
  
2.  En el panel izquierdo del **Administrador de configuración de SQL Server**, haga clic en **Servicios de SQL Server**. En el panel derecho se muestran varios servicios que están relacionados con [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)]. Si [!INCLUDE[ssDE](../../includes/ssde-md.md)] está instalado, el servicio [!INCLUDE[ssDE](../../includes/ssde-md.md)] aparece como **SQL Server (MSSQLSERVER)** si se trata de la instancia predeterminada, o bien como **SQL Server (**\<*nombre_instancia*>**)**, si [!INCLUDE[ssDE](../../includes/ssde-md.md)] está instalado como una instancia con nombre. A menos que se cambie el nombre de la instancia, [!INCLUDE[ssExpress](../../includes/ssexpress-md.md)] se instala como una instancia con nombre y con el nombre **SQLEXPRESS**. Un icono con un triángulo verde indica que [!INCLUDE[ssDE](../../includes/ssde-md.md)] se está ejecutando. Un icono con un cuadrado rojo indica que [!INCLUDE[ssDE](../../includes/ssde-md.md)] está detenido.  
  
3.  Para iniciar [!INCLUDE[ssDE](../../includes/ssde-md.md)], en el panel derecho, haga clic con el botón derecho en [!INCLUDE[ssDE](../../includes/ssde-md.md)]y haga clic en **Iniciar**.  
  
> [!NOTE]  
>  Durante la instalación, el usuario puede seleccionar una ubicación en la que instalar los archivos de programa y de base de datos. Si el usuario acepta la ubicación predeterminada, los archivos se instalan en [!INCLUDE[ssInstallPath](../../includes/ssinstallpath-md.md)] y C:\Archivos de programa\Microsoft SQL Server\MSSQL.*x*, donde *x* es un número.  
  
  
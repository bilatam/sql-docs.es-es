---
title: MSSQLSERVER_948 | Microsoft Docs
ms.custom: ''
ms.date: 03/06/2017
ms.prod: sql-server-2014
ms.reviewer: ''
ms.suite: ''
ms.technology: supportability
ms.tgt_pltfrm: ''
ms.topic: conceptual
f1_keywords:
- "948"
helpviewer_keywords:
- 948 (Database Engine error)
ms.assetid: 95c4ad45-a518-4165-a5c4-6e6b932b0570
caps.latest.revision: 11
author: MashaMSFT
ms.author: mathoma
manager: craigg
ms.openlocfilehash: 45c987dea690125de2784068b42369a454fafd8d
ms.sourcegitcommit: f8ce92a2f935616339965d140e00298b1f8355d7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/03/2018
ms.locfileid: "37426384"
---
# <a name="mssqlserver948"></a>MSSQLSERVER_948
    
## <a name="details"></a>Detalles  
  
|||  
|-|-|  
|Nombre del producto|SQL Server|  
|Identificador del evento|948|  
|Origen del evento|MSSQLSERVER|  
|Componente|SQLEngine|  
|Nombre simbólico|N/D|  
|Texto del mensaje|No se puede abrir la base de datos "%.*ls" por tener la versión %d. Este servidor es compatible con la versión %d y anteriores. No se admite esta ruta de actualización.|  
  
## <a name="explanation"></a>Explicación  
 Algunas características de [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] afectan a la estructura de los archivos de base de datos. Al adjuntar una base de datos a otra instancia de [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)], es posible que el formato de archivo no sea compatible con una versión distinta de [!INCLUDE[ssDE](../../includes/ssde-md.md)].  
  
 Por ejemplo, este error puede deberse al uso del formato de almacenamiento vardecimal en una versión posterior de [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] y a un intento posterior de adjuntar los archivos de base de datos a una versión anterior al Service Pack 2 de [!INCLUDE[ssVersion2005](../../includes/ssversion2005-md.md)].  
  
## <a name="user-action"></a>Acción del usuario  
 Determine la versión de [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] que está ejecutándose en el servidor de origen. En [!INCLUDE[ssManStudioFull](../../includes/ssmanstudiofull-md.md)], haga clic en el servidor y, a continuación, haga clic en **propiedades** o tipo `SELECT @@VERSION` en una ventana de consulta. Abra la base de datos utilizando la versión original de [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)]. Examine las características que están habilitadas en la base de datos original en la instancia de [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)]. Modifique esta configuración para trabajar con la versión de [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] donde se adjuntará la base de datos.  
  
  

---
title: MSSQLSERVER_905 | Microsoft Docs
ms.custom: ''
ms.date: 05/24/2017
ms.prod: sql-server-2014
ms.reviewer: ''
ms.suite: ''
ms.technology: supportability
ms.tgt_pltfrm: ''
ms.topic: conceptual
helpviewer_keywords:
- 905 (Database Engine error)
ms.assetid: c828bb2e-e554-4f81-b76c-2b3740d2b944
caps.latest.revision: 15
author: MashaMSFT
ms.author: mathoma
manager: craigg
ms.openlocfilehash: 67003112253fc8b7b74fa4dd7c232538c9084bba
ms.sourcegitcommit: f8ce92a2f935616339965d140e00298b1f8355d7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/03/2018
ms.locfileid: "37407104"
---
# <a name="mssqlserver905"></a>MSSQLSERVER_905
    
## <a name="details"></a>Detalles  
  
|||  
|-|-|  
|Nombre del producto|SQL Server|  
|Identificador del evento|905|  
|Origen del evento|MSSQLSERVER|  
|Componente|SQLEngine|  
|Nombre simbólico|DBSTARTUP_EE_PARTITIONING|  
|Texto del mensaje|La base de datos '%. * ls' no se puede iniciar en esta edición de SQL Server porque contiene una función de partición '%.\*ls'. Únicamente la edición Enterprise de SQL Server admite particionamiento.|  
  
## <a name="explanation"></a>Explicación  
 La base de datos contiene una o varias tablas o índices con particiones. Esta edición de [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] no puede utilizar particionamiento. En consecuencia, la base de datos no se puede iniciar correctamente. Las tablas e índices con particiones no están disponibles en todas las ediciones de [!INCLUDE[msCoName](../../includes/msconame-md.md)][!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)]. Para obtener una lista de las características admitidas por las ediciones de [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)], vea [Features Supported by the Editions of SQL Server 2014](../../getting-started/features-supported-by-the-editions-of-sql-server-2014.md).  
  
## <a name="user-action"></a>Acción del usuario  
 Separe la base de datos mediante el procedimiento almacenado sp_detach_db. Mueva los archivos si es necesario, y, a continuación, asocie la base de datos a una instancia de una edición [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] utilizando CREATE DATABASE con las opciones FOR ATTACH o FOR ATTACH_REBUILD_LOG. Deshabilite el particionamiento en todas las tablas y quite las funciones de particionamiento. Desasocie la base de datos de nuevo y vuelva a adjuntarla al servidor actual.  
  
  

---
title: MSSQLSERVER_33028 | Microsoft Docs
ms.custom: ''
ms.date: 04/04/2017
ms.prod: sql
ms.reviewer: ''
ms.suite: sql
ms.technology: supportability
ms.tgt_pltfrm: ''
ms.topic: language-reference
helpviewer_keywords:
- 33028 (Database Engine error)
ms.assetid: c5cec0e4-0bcd-4907-826f-e7d835cfcb37
caps.latest.revision: 10
author: MashaMSFT
ms.author: mathoma
manager: craigg
ms.openlocfilehash: 7a53189762bb4eb7782db32d2fa3040549e7ce7b
ms.sourcegitcommit: ee661730fb695774b9c483c3dd0a6c314e17ddf8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/19/2018
ms.locfileid: "34320476"
---
# <a name="mssqlserver33028"></a>MSSQLSERVER_33028
[!INCLUDE[appliesto-ss-xxxx-xxxx-xxx-md](../../includes/appliesto-ss-xxxx-xxxx-xxx-md.md)]
  
## <a name="details"></a>Detalles  
  
|||  
|-|-|  
|Nombre del producto|SQL Server|  
|Identificador del evento|33028|  
|Origen del evento|MSSQLSERVER|  
|Componente|SQLEngine|  
|Nombre simbólico|SEC_CRYPTOPROV_CANTOPENSESSION|  
|Texto del mensaje|No se puede abrir la sesión para %S_MSG '%.*ls'. Código de error de proveedor: %d.|  
  
## <a name="explanation"></a>Explicación  
[!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] no pudo abrir el proveedor de servicios criptográficos enumerado en el mensaje de error. El proveedor de servicios criptográficos proporcionó el código de error enumerado. Puede que tenga que ponerse en contacto con su proveedor de servicios criptográficos para obtener más información sobre el error.  
  
|Código de error|Descripción|  
|--------------|---------------|  
|0|Correcto. Ningún error.|  
|1|Error. Se ha producido un error no especificado o inesperado. No se dispone de información adicional.|  
|2|Búfer insuficiente. No se pudo asignar espacio para el proveedor de servicios criptográficos.|  
|3|No compatible. El proveedor de servicios criptográficos no admite esta versión. Seleccione otro proveedor de servicios criptográficos.|  
|4|No se ha encontrado. El proveedor de servicios criptográficos especificado no está presente o no se tiene autorización para el acceso a los archivos.|  
|5|Error de autorización. Puede ser el resultado de proporcionar un nombre de usuario o una contraseña incorrectos al crear la credencial. Puede producirse si la credencial no existe.|  
|6|Argumento no válido. Se ha pasado un argumento no válido al proveedor de servicios criptográficos.|  
  
## <a name="user-action"></a>Acción del usuario  
Resuelva el error o póngase en contacto con el proveedor de servicios criptográficos para obtener más información.  
  

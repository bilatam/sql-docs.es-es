---
title: El desencadenador AFTER anidado activa incluso cuando el anidamiento de desencadenadores es OFF | Microsoft Docs
ms.custom: ''
ms.date: 06/13/2017
ms.prod: sql-server-2014
ms.reviewer: ''
ms.suite: ''
ms.technology:
- database-engine
ms.tgt_pltfrm: ''
ms.topic: conceptual
helpviewer_keywords:
- DML triggers, nested
- nested triggers option
- triggers [SQL Server], nested
ms.assetid: 94d72960-676e-40d9-81bc-08bffe778110
caps.latest.revision: 21
author: mashamsft
ms.author: mathoma
manager: craigg
ms.openlocfilehash: 683ffcfa3bb4715b25fb912fa12808be3b0873ec
ms.sourcegitcommit: c18fadce27f330e1d4f36549414e5c84ba2f46c2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/02/2018
ms.locfileid: "37247835"
---
# <a name="nested-after-trigger-fires-even-when-trigger-nesting-is-off"></a>El desencadenador AFTER anidado se lanza incluso cuando el anidamiento de desencadenadores está desactivado
  El Asesor de actualizaciones ha detectado un desencadenador AFTER anidad dentro de un desencadenador INSTEAD OF que está definido en una o más tablas. Los desencadenadores AFTER anidados pueden activarse incluso cuando la opción de configuración del servidor de `nested triggers` se establece en 0.  
  
## <a name="component"></a>Componente  
 [!INCLUDE[ssDE](../../includes/ssde-md.md)]  
  
## <a name="description"></a>Descripción  
 El primer desencadenador AFTER anidado que esté dentro de un desencadenador INSTEAD OF se activará si la opción de configuración del servidor `nested triggers` está establecida en 0. Sin embargo, con esta configuración, no se lanzarán los siguientes desencadenadores AFTER.  
  
## <a name="corrective-action"></a>Acción correctora  
 Revise sus aplicaciones en busca de desencadenadores anidados para determinar si las aplicaciones todavía cumplen con sus reglas de negocios en relación con este comportamiento nuevo, siempre que la opción de configuración del servidor `nested triggers` esté establecida en 0 y, a continuación, realiza las modificaciones apropiadas.  
  
## <a name="see-also"></a>Vea también  
 [Problemas de actualización de motor de base de datos](../../../2014/sql-server/install/database-engine-upgrade-issues.md)   
 [Asesor de actualizaciones de SQL Server 2014 &#91;nuevo&#93;](/sql/2014/sql-server/install/sql-server-2014-upgrade-advisor)  
  
  

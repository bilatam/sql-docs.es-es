---
title: Sys.dm_broker_activated_tasks (Transact-SQL) | Documentos de Microsoft
ms.custom: ''
ms.date: 06/10/2016
ms.prod: sql
ms.reviewer: ''
ms.suite: sql
ms.technology: system-objects
ms.tgt_pltfrm: ''
ms.topic: language-reference
f1_keywords:
- sys.dm_broker_activated_tasks
- sys.dm_broker_activated_tasks_TSQL
- dm_broker_activated_tasks
- dm_broker_activated_tasks_TSQL
dev_langs:
- TSQL
helpviewer_keywords:
- sys.dm_broker_activated_tasks dynamic management view
ms.assetid: 17e6f87f-8f56-489d-9aed-216afc8ef310
caps.latest.revision: 22
author: stevestein
ms.author: sstein
manager: craigg
ms.openlocfilehash: c24c9394aa6f05811e93d18e5c67b43278660dfc
ms.sourcegitcommit: 7019ac41524bdf783ea2c129c17b54581951b515
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/23/2018
ms.locfileid: "34463521"
---
# <a name="sysdmbrokeractivatedtasks-transact-sql"></a>sys.dm_broker_activated_tasks (Transact-SQL)
[!INCLUDE[tsql-appliesto-ss2008-xxxx-xxxx-xxx-md](../../includes/tsql-appliesto-ss2008-xxxx-xxxx-xxx-md.md)]

  Devuelve una fila por cada procedimiento almacenado activado por Service Broker.  
 

|Nombre de columna|Tipo de datos|Description|  
|-----------------|---------------|-----------------|  
|**spid**|**int**|Id. de la sesión del procedimiento almacenado activado. ACEPTA VALORES NULL.|  
|**database_id**|**smallint**|Id. de la base de datos en la que se define la cola. ACEPTA VALORES NULL.|  
|**queue_id**|**int**|Id. del objeto de la cola para el que se activó el procedimiento almacenado. ACEPTA VALORES NULL.|  
|**procedure_name**|**nvarchar(650)**|Nombre del procedimiento almacenado activado. ACEPTA VALORES NULL.|  
|**execute_as**|**int**|Id. del usuario con el que se ejecuta el procedimiento almacenado. ACEPTA VALORES NULL.|  
  
## <a name="permissions"></a>Permissions  
 es necesario contar con el permiso VIEW SERVER STATE en el servidor.  
  
## <a name="physical-joins"></a>Combinaciones físicas  
 ![Combinaciones de sys.dm_broker_activated_tasks](../../relational-databases/system-dynamic-management-views/media/join-dm-broker-activated-tasks-1.gif "combinaciones de sys.dm_broker_activated_tasks")  
  
## <a name="relationship-cardinalities"></a>Cardinalidades de relación  
  
|De|En|Relación|  
|----------|--------|------------------|  
|dm_broker_activated_tasks.spid|dm_exec_sessions.session_id|Uno a uno|  
  
## <a name="see-also"></a>Vea también  
 [Funciones y vistas de administración dinámica &#40;Transact-SQL&#41;](~/relational-databases/system-dynamic-management-views/system-dynamic-management-views.md)   
 [Service Broker relacionadas con vistas de administración dinámica & #40; Transact-SQL & #41;](../../relational-databases/system-dynamic-management-views/service-broker-related-dynamic-management-views-transact-sql.md)  
  
  


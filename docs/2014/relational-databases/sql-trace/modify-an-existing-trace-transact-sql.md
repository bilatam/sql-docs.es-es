---
title: Modificación de un seguimiento existente (Transact-SQL) | Microsoft Docs
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
- traces [SQL Server], modifying
- modifying traces
ms.assetid: 8792b43f-2510-44e3-9239-e73ad8227b89
caps.latest.revision: 17
author: MashaMSFT
ms.author: mathoma
manager: craigg
ms.openlocfilehash: 68d98a838fb17360997d7eb4a1db025176e322aa
ms.sourcegitcommit: c18fadce27f330e1d4f36549414e5c84ba2f46c2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/02/2018
ms.locfileid: "37168286"
---
# <a name="modify-an-existing-trace-transact-sql"></a>Modificar un seguimiento existente (Transact-SQL)
  En este tema se describe cómo utilizar procedimientos almacenados para modificar un seguimiento existente.  
  
### <a name="to-modify-an-existing-trace"></a>Para modificar un seguimiento existente  
  
1.  Si el seguimiento ya se está ejecutando, ejecute **sp_trace_setstatus** especificando **@status = 0** para detener el seguimiento.  
  
2.  Para modificar los eventos del seguimiento, ejecute **sp_trace_setevent** , especificando los cambios a través de los parámetros. Los parámetros son, por este orden:  
  
    -   **@traceid** (Id. del seguimiento)  
  
    -   **@eventid** (Id. del evento)  
  
    -   **@columnid** (Id. de columna)  
  
    -   **@on** (ON)  
  
     Al modificar el parámetro **@on** , tenga presente su interacción con el parámetro **@columnid** :  
  
    |ON|Identificador de columna|Resultado|  
    |--------|---------------|------------|  
    |ON (**1**)|NULL|El evento se activa, se establece en ON. Se borran todas las columnas.|  
    ||NOT NULL|La columna se activa, se establece en ON, para el evento especificado.|  
    |OFF (**0**)|NULL|El evento se desactiva, se establece en OFF. Se borran todas las columnas.|  
    ||NOT NULL|La columna se desactiva, se establece en OFF, para el evento especificado.|  
  
> [!IMPORTANT]  
>  A diferencia de los procedimientos almacenados normales, los parámetros de todos los procedimientos almacenados del [!INCLUDE[ssSqlProfiler](../../includes/sssqlprofiler-md.md)] (**sp_trace_* xx***) deben escribirse de forma precisa y no admiten la conversión automática de tipos de datos. Si no se llama a estos parámetros con los tipos de datos de parámetros de entrada correctos, según se especifica en la descripción del argumento, el procedimiento almacenado devuelve un error.  
  
## <a name="see-also"></a>Vea también  
 [sp_trace_setevent &#40;Transact-SQL&#41;](/sql/relational-databases/system-stored-procedures/sp-trace-setevent-transact-sql)   
 [sp_trace_setstatus &#40;Transact-SQL&#41;](/sql/relational-databases/system-stored-procedures/sp-trace-setstatus-transact-sql)   
 [Procedimientos almacenados del sistema &#40;Transact-SQL&#41;](/sql/relational-databases/system-stored-procedures/system-stored-procedures-transact-sql)   
 [Procedimientos almacenados de SQL Server Profiler &#40;Transact-SQL&#41;](/sql/relational-databases/system-stored-procedures/sql-server-profiler-stored-procedures-transact-sql)  
  
  

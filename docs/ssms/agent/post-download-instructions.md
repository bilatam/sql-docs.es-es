---
title: Exponer instrucciones de descarga | Microsoft Docs
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: sql-tools
ms.component: ssms-agent
ms.reviewer: ''
ms.suite: sql
ms.technology: ssms
ms.tgt_pltfrm: ''
ms.topic: conceptual
f1_keywords:
- sql13.ag.target.post.f1
ms.assetid: 11db1efb-8f5b-4284-b17c-04b4bfcef9ed
caps.latest.revision: 3
author: stevestein
ms.author: sstein
manager: craigg
monikerRange: = azuresqldb-mi-current || >= sql-server-2016 || = sqlallproducts-allversions
ms.openlocfilehash: 7c4ebd7c0451e0a8fca7714b7f722613febc5e56
ms.sourcegitcommit: e77197ec6935e15e2260a7a44587e8054745d5c2
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 07/11/2018
ms.locfileid: "38030843"
---
# <a name="post-download-instructions"></a>Exponer instrucciones de descarga
[!INCLUDE[appliesto-ss-asdbmi-xxxx-xxx-md](../../includes/appliesto-ss-asdbmi-xxxx-xxx-md.md)]

> [!IMPORTANT]  
> En [Instancia administrada de Azure SQL Database](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance), la mayoría de las características de agente SQL Server son compatibles actualmente, aunque no todas. Vea [Diferencias de T-SQL en Instancia administrada de Azure SQL Database](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-transact-sql-information#sql-server-agent) para obtener más información.

Utilice esta página para especificar las instrucciones de descarga de un servidor de destino.  
  
## <a name="options"></a>Opciones  
**Tipo de instrucción**  
Especifica el tipo de instrucción de descarga que se debe exponer.  
  
**Descripción**  
Presenta una descripción de la instrucción de descarga.  
  
**Intervalo de sondeo**  
Establece el intervalo de sondeo del servidor de destino. Solo se aplica a la instrucción **Establecer intervalo de sondeo** .  
  
**Todos los servidores de destino**  
Seleccione esta opción para exponer la instrucción de descarga en todos los servidores de destino.  
  
**Estos servidores de destino**  
Seleccione esta opción para exponer la instrucción de descarga en los servidores de destino seleccionados.  
  
**Select**  
Especifica que el servidor de destino reciba la instrucción de descarga.  
  
**Servidor de destino**  
Presenta el nombre del servidor de destino.  
  
**Hora local**  
Muestra la fecha y la hora del servidor de destino en la zona horaria local de dicho servidor.  
  
**Intervalo de sondeo**  
Presenta el intervalo de sondeo actual del servidor de destino.  
  
## <a name="see-also"></a>Ver también  
[Administración automatizada en una empresa](../../ssms/agent/automated-administration-across-an-enterprise.md)  
  

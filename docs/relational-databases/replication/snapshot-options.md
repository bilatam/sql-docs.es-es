---
title: Opciones de instantánea | Microsoft Docs
ms.custom: ''
ms.date: 03/14/2017
ms.prod: sql
ms.prod_service: database-engine
ms.component: replication
ms.reviewer: ''
ms.suite: sql
ms.technology: replication
ms.tgt_pltfrm: ''
ms.topic: conceptual
helpviewer_keywords:
- snapshot replication [SQL Server], options
- snapshots [SQL Server replication], options
ms.assetid: 759fab42-66c7-4541-a7a3-bb6fb868493c
caps.latest.revision: 28
author: MashaMSFT
ms.author: mathoma
manager: craigg
ms.openlocfilehash: c658f7898af62407a2c5458951aa14263ab94e7b
ms.sourcegitcommit: 022d67cfbc4fdadaa65b499aa7a6a8a942bc502d
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 07/03/2018
ms.locfileid: "37353107"
---
# <a name="snapshot-options"></a>Opciones de instantánea
[!INCLUDE[appliesto-ss-xxxx-xxxx-xxx-md](../../includes/appliesto-ss-xxxx-xxxx-xxx-md.md)]
  Hay una serie de opciones disponibles al inicializar una suscripción con una instantánea:  
  
-   Especificar una ubicación alternativa para la carpeta de instantáneas en lugar de, o además de, la predeterminada. Para más información, consulte [Alternate Snapshot Folder Locations](../../relational-databases/replication/alternate-snapshot-folder-locations.md).  
  
-   Comprimir instantáneas para su almacenamiento en medios extraíbles o para su transferencia a través de una red lenta. Para más información, consulte [Compressed Snapshots](../../relational-databases/replication/compressed-snapshots.md).  
  
-   Ejecutar scripts [!INCLUDE[tsql](../../includes/tsql-md.md)] antes o después de aplicar la instantánea. Para obtener más información, consulte [Ejecutar scripts antes y después de aplicar la instantánea](../../relational-databases/replication/execute-scripts-before-and-after-the-snapshot-is-applied.md).  
  
-   Transferir la instantánea mediante el Protocolo de transferencia de archivos (FTP). Para obtener más información, consulte [Transferir instantáneas mediante FTP](../../relational-databases/replication/transfer-snapshots-through-ftp.md).  
  
## <a name="see-also"></a>Ver también  
 [Inicializar una suscripción con una instantánea](../../relational-databases/replication/initialize-a-subscription-with-a-snapshot.md)  
  
  

---
title: Vs regulares. Conexiones de contexto | Microsoft Docs
ms.custom: ''
ms.date: 06/13/2017
ms.prod: sql-server-2014
ms.reviewer: ''
ms.suite: ''
ms.technology: clr
ms.tgt_pltfrm: ''
ms.topic: reference
helpviewer_keywords:
- context connections [CLR integration]
- regular connections [CLR integration]
ms.assetid: a1dead02-be88-4b16-8cb2-db1284856764
caps.latest.revision: 13
author: rothja
ms.author: jroth
manager: craigg
ms.openlocfilehash: 3ba21a813e019b94a51ad6a43e45faf64cd9f7b2
ms.sourcegitcommit: 022d67cfbc4fdadaa65b499aa7a6a8a942bc502d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/03/2018
ms.locfileid: "37352557"
---
# <a name="regular-vs-context-connections"></a>Vs regulares. Conexiones de contexto
  Si se conecta a un servidor remoto, utilice siempre conexiones normales en lugar de conexiones de contexto. Si se debe conectar al mismo servidor donde se está ejecutando el procedimiento almacenado o la función, utilice la conexión de contexto en la mayoría de los casos. Entre las ventajas que esto presenta se encuentran la ejecución en el mismo espacio de la transacción y que no es necesario volver a autenticarse.  
  
 Además, la utilización de la conexión de contexto suele proporciona un mejor rendimiento y menos uso de recursos. La conexión de contexto es una conexión solo en proceso, por lo que puede ponerse en contacto "directamente" con el servidor omitiendo los niveles de transporte y protocolo de red para enviar las instrucciones Transact-SQL y recibir los resultados. También se omite el proceso de autenticación. En la figura siguiente se muestran los componentes principales del proveedor administrado de `SqlClient`, así como la forma en que interactúan los diferentes componentes entre sí al utilizar una conexión normal y al utilizar la conexión de contexto.  
  
 ![Rutas de código de un contexto y una conexión normal. ] (../../../database-engine/dev-guide/media/clrintdataaccess.gif "Código rutas de acceso de un contexto y una conexión normal.")  
  
 La conexión de contexto sigue una ruta de acceso al código más corta e implica menos componentes, de modo que puede esperar que las solicitudes y los resultados se envíen al servidor y de éste más rápido que en una conexión normal. El tiempo de ejecución de consultas en el servidor es el mismo en las conexiones de contexto y normales.  
  
 Hay algunos casos en los que puede necesitar abrir una conexión normal independiente al mismo servidor. Por ejemplo, hay ciertas restricciones sobre el uso de la conexión de contexto, se describe en [restricciones en conexiones de contexto y normales](context-connections-and-regular-connections-restrictions.md).  
  
## <a name="see-also"></a>Vea también  
 [Conexión de contexto](context-connection.md)  
  
  

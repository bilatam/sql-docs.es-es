---
title: Detectar la categoría de eventos de estado del servidor | Microsoft Docs
ms.custom: ''
ms.date: 06/13/2017
ms.prod: sql-server-2014
ms.reviewer: ''
ms.suite: ''
ms.technology:
- analysis-services
ms.tgt_pltfrm: ''
ms.topic: conceptual
helpviewer_keywords:
- Discover Server State event category
- server state events [Analysis Services]
- discover server state events
- event classes [Analysis Services], discover server state
ms.assetid: b62ebf66-d090-4f74-8c83-11ed518b2018
caps.latest.revision: 24
author: minewiskan
ms.author: owend
manager: craigg
ms.openlocfilehash: 3c55d16650e9ef04ae951a9eb0d7f60fbc6c472a
ms.sourcegitcommit: c18fadce27f330e1d4f36549414e5c84ba2f46c2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/02/2018
ms.locfileid: "37197855"
---
# <a name="discover-server-state-event-category"></a>detección de estado del servidor, categoría de eventos
  La categoría de eventos Detección de estado del servidor tiene las clases de eventos que se describen en la siguiente tabla.  
  
|Clase de eventos|Identificador del evento|Descripción|  
|-----------------|--------------|-----------------|  
|Server State Discover Begin|33|Recopila todos los eventos de inicio de detección XMLA de estado de servidor desde que se inició el seguimiento.|  
|Server State Discover Data|34|Recopila todos los eventos de detección XMLA de estado de servidor desde que se inició el seguimiento. Estos eventos capturan el contenido de la respuesta a la solicitud de detección.|  
|Server State Discover End|35|Recopila todos los eventos de fin de detección XMLA de estado de servidor desde que se inició el seguimiento.|  
  
 Para obtener más información acerca de las columnas asociadas a cada una de las clases de evento de Eventos de consultas, vea [Discover Server State Events Data Columns](discover-server-state-events-data-columns.md).  
  
## <a name="see-also"></a>Vea también  
 [Eventos de seguimiento de Analysis Services](analysis-services-trace-events.md)  
  
  

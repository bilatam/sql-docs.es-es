---
title: Información de publicación, Advertencias (Publicación transaccional) | Microsoft Docs
ms.custom: ''
ms.date: 03/07/2017
ms.prod: sql
ms.prod_service: database-engine
ms.component: replication
ms.reviewer: ''
ms.suite: sql
ms.technology: replication
ms.tgt_pltfrm: ''
ms.topic: conceptual
f1_keywords:
- sql13.rep.monitor.publicationinfo.warningsandagents.tran.f1
ms.assetid: 4d4baf1d-d0a1-4d09-bec7-137811f43f09
caps.latest.revision: 30
author: MashaMSFT
ms.author: mathoma
manager: craigg
ms.openlocfilehash: 539d91d6d77d69047433027e9d70d21056c8faaf
ms.sourcegitcommit: 022d67cfbc4fdadaa65b499aa7a6a8a942bc502d
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 07/03/2018
ms.locfileid: "37353617"
---
# <a name="publication-information-warnings-transactional-publication"></a>Información de publicación, Advertencias (Publicación transaccional)
[!INCLUDE[appliesto-ss-xxxx-xxxx-xxx-md](../../includes/appliesto-ss-xxxx-xxxx-xxx-md.md)]
  La pestaña **Advertencias** está disponible para los distribuidores que ejecutan [!INCLUDE[ssVersion2005](../../includes/ssversion2005-md.md)] y versiones posteriores. La pestaña **Advertencias** permite realizar las siguientes tareas para la publicación seleccionada:  
  
-   Habilitar las advertencias para mostrarlas en el Monitor de replicación.  
  
-   Especificar umbrales asociados con las advertencias.  
  
-   Definir alertas asociadas con advertencias.  
  
## <a name="warnings-thresholds-and-alerts"></a>Advertencias, umbrales y alertas  
 De forma predeterminada, el Monitor de replicación muestra advertencias de suscripciones no inicializadas: se muestra el estado **Suscripción no inicializada** como una advertencia en la columna **Estado** de las páginas que incluyen información de la suscripción. En publicaciones transaccionales, puede especificar si esas condiciones adicionales producen advertencias:  
  
-   Expiración inminente de la suscripción.  
  
     Esta condición se corresponde con la opción **Advertir si una suscripción expirará dentro del umbral**. Si se alcanza o se supera el umbral especificado, se muestra el estado de la suscripción como **Con expiración en breve/Expirado** (a menos que tenga que mostrarse un problema con una prioridad superior).  
  
-   Superar la latencia especificada. Es el tiempo que transcurre entre la confirmación de una transacción en el publicador y la confirmación de la transacción correspondiente en el suscriptor.  
  
     Esto se corresponde con la opción **Advertir si la latencia supera el valor de umbral**. Si se alcanza o se supera el umbral especificado, se muestra el estado de la suscripción como **Rendimiento crítico** (a menos que tenga que mostrarse un problema con una prioridad superior). El umbral también se utiliza para proporcionar una clasificación de rendimiento, que se muestra en la columna **Rendimiento** de las páginas que incluyen información de la suscripción. La clasificación de rendimiento tiene uno de los valores siguientes:  
  
    -   Excelente  
  
    -   Bueno  
  
    -   Regular  
  
    -   Insuficiente  
  
    -   Crítico  
  
 Cuando se habilita una advertencia, también se establece un umbral. Por ejemplo, si habilita la advertencia **Advertir si la latencia supera el valor de umbral**, seleccione el tiempo permitido entre que se confirma una transacción en el publicador y la transacción se confirma en el suscriptor.  
  
 Además de mostrar una advertencia en el Monitor de replicación, llegar a un umbral también puede desencadenar una alerta. Para definir alertas, haga clic en **Configurar alertas** y proporcione información en el cuadro de diálogo **Configurar alertas de replicación** .  
  
## <a name="options"></a>Opciones  
 **Habilitado**  
 Seleccione esta opción si desea habilitar una advertencia y especificar un umbral asociado.  
  
 **Advertencia**  
 Descripción de la advertencia asociada al umbral.  
  
 **Umbral**  
 Permite especificar un valor para el umbral.  
  
 **Configurar alertas**  
 Seleccione una fila en la cuadrícula **Advertencias** y haga clic en **Configurar alertas** para abrir el cuadro de diálogo **Configurar alertas de replicación** . El cuadro de diálogo permite definir una alerta que se asociará al umbral y la advertencia seleccionados.  
  
 **Descartar cambios**  
 Haga clic para descartar los cambios realizados en las advertencias y los umbrales.  
  
> [!NOTE]  
>  Hacer clic en **Descartar cambios** no afecta a las alertas definidas en el cuadro de diálogo **Configurar alertas de replicación** .  
  
 **Guardar cambios**  
 Haga clic para guardar los cambios realizados en las advertencias y los umbrales.  
  
## <a name="see-also"></a>Ver también  
 [Iniciar el Monitor de replicación](../../relational-databases/replication/monitor/start-the-replication-monitor.md)   
 [Ver información y realizar tareas para una publicación &#40;Monitor de replicación&#41;](../../relational-databases/replication/monitor/view-information-and-perform-tasks-for-a-publication-replication-monitor.md)   
 [Supervisar el rendimiento con el Monitor de replicación](../../relational-databases/replication/monitor/monitor-performance-with-replication-monitor.md)   
 [Monitoring Replication](../../relational-databases/replication/monitor/monitoring-replication-overview.md)  (Supervisar la replicación)  
 [Establecer umbrales y advertencias en el Monitor de replicación](../../relational-databases/replication/monitor/set-thresholds-and-warnings-in-replication-monitor.md)  
  
  

---
title: Editor de la tarea FTP (página General) | Microsoft Docs
ms.custom: ''
ms.date: 06/13/2017
ms.prod: sql-server-2014
ms.reviewer: ''
ms.suite: ''
ms.technology:
- integration-services
ms.tgt_pltfrm: ''
ms.topic: conceptual
f1_keywords:
- sql12.dts.designer.ftptask.general.f1
helpviewer_keywords:
- File Transfer Protocol Task Editor
ms.assetid: 28b46fdd-b04a-4f97-a99f-883f5735a6d9
caps.latest.revision: 28
author: douglaslms
ms.author: douglasl
manager: craigg
ms.openlocfilehash: 97f8761af335319cbd205eca3c57d4f6874e5829
ms.sourcegitcommit: c18fadce27f330e1d4f36549414e5c84ba2f46c2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/02/2018
ms.locfileid: "37283641"
---
# <a name="ftp-task-editor-general-page"></a>Editor de la tarea FTP (página General)
  Use la página **General** del cuadro de diálogo **Editor de la tarea FTP** para especificar el administrador de conexiones FTP que se conecta al servidor FTP con el que se comunica la tarea. También puede asignar un nombre a la tarea FTP y describirla.  
  
 Para más información sobre esta tarea, vea [Tarea FTP](control-flow/ftp-task.md).  
  
## <a name="options"></a>Opciones  
 **FtpConnection**  
 Seleccione un administrador de conexiones FTP existente o haga clic en \<**Nueva conexión...**> para crear uno nuevo.  
  
> [!IMPORTANT]  
>  El administrador de conexiones FTP solo admite la autenticación anónima y la autenticación básica. No es compatible con la autenticación de Windows.  
  
 **Temas relacionados**: [FTP Connection Manager](connection-manager/ftp-connection-manager.md), [FTP Connection Manager Editor](../../2014/integration-services/ftp-connection-manager-editor.md)  
  
 **StopOnFailure**  
 Indica si la tarea FTP termina si se produce un error en una opción FTP.  
  
 **Nombre**  
 Proporcione un nombre único para la tarea FTP. Este nombre se utiliza como etiqueta en el icono de tarea.  
  
> [!NOTE]  
>  Los nombres de tarea deben ser únicos en un paquete.  
  
 **Descripción**  
 Escriba una descripción de la tarea FTP.  
  
## <a name="see-also"></a>Vea también  
 [Referencia de mensajes y Error de Integration Services](../../2014/integration-services/integration-services-error-and-message-reference.md)   
 [Editor de la tarea FTP &#40;página transferencia de archivos&#41;](../../2014/integration-services/ftp-task-editor-file-transfer-page.md)   
 [Página Expresiones](expressions/expressions-page.md)  
  
  

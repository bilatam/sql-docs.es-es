---
title: Usar la clase Report para una extensión de entrega | Microsoft Docs
ms.custom: ''
ms.date: 04/27/2017
ms.prod: sql-server-2014
ms.reviewer: ''
ms.suite: ''
ms.technology:
- docset-sql-devref
- reporting-services-native
ms.tgt_pltfrm: ''
ms.topic: reference
helpviewer_keywords:
- delivery extensions [Reporting Services], report information
- Report class
ms.assetid: 1145ac63-eafd-452a-82af-16f85b1676dd
caps.latest.revision: 34
author: markingmyname
ms.author: maghan
manager: craigg
ms.openlocfilehash: 42bb83e2f4420419f82489193dcf022a08783e77
ms.sourcegitcommit: c18fadce27f330e1d4f36549414e5c84ba2f46c2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/02/2018
ms.locfileid: "37301705"
---
# <a name="using-the-report-class-for-a-delivery-extension"></a>Usar la clase Report para una extensión de entrega
  La clase <xref:Microsoft.ReportingServices.Interfaces.Report> representa un informe en la base de datos del servidor de informes. Cada suscripción está asociada a un informe concreto. El informe está contenido en la notificación. La extensión de entrega puede utilizar el objeto <xref:Microsoft.ReportingServices.Interfaces.Report> que forma parte de la notificación para representar el informe. El objeto <xref:Microsoft.ReportingServices.Interfaces.Report> también contiene las propiedades específicas del informe, como la dirección URL para el informe en el servidor de informes y el nombre del informe. Todas estas propiedades se pueden utilizar como parte del proveedor de entrega.  
  
 El método <xref:Microsoft.ReportingServices.Interfaces.Report.Render%2A> de la clase <xref:Microsoft.ReportingServices.Interfaces.Report> se puede utilizar para representar un informe. El método <xref:Microsoft.ReportingServices.Interfaces.Report.Render%2A> devuelve una matriz de uno o más objetos <xref:Microsoft.ReportingServices.Interfaces.RenderedOutputFile> que comprenden un único informe representado. El primer objeto <xref:Microsoft.ReportingServices.Interfaces.RenderedOutputFile> es el informe representado. Cualquier otro objeto <xref:Microsoft.ReportingServices.Interfaces.RenderedOutputFile> son los recursos que se deben entregar junto con los datos del informe (por ejemplo, un archivo HTML e imágenes asociadas). Las extensiones de representación que son extensiones de un único flujo (IMAGE, PDF, MHTML y Excel) devuelven solo un objeto <xref:Microsoft.ReportingServices.Interfaces.RenderedOutputFile> en la matriz.  
  
 El objeto <xref:Microsoft.ReportingServices.Interfaces.RenderedOutputFile>, que contiene el flujo del informe, puede estar incluido como parte de una entrega.  
  
 Para ver un ejemplo de cómo utilizar la clase <xref:Microsoft.ReportingServices.Interfaces.Report>, vea [Muestras de productos de SQL Server Reporting Services](http://go.microsoft.com/fwlink/?LinkId=177889).  
  
## <a name="see-also"></a>Vea también  
 [Implementar una extensión de entrega](implementing-a-delivery-extension.md)   
 [Biblioteca de extensiones de Reporting Services](../reporting-services-extension-library.md)   
 [Uso de la clase RenderedOutputFile para una extensión de entrega](using-the-renderedoutputfile-class-for-a-delivery-extension.md)  
  
  

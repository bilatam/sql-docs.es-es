---
title: 'Métodos de modelo: servicio web del servidor de informes | Microsoft Docs'
ms.custom: ''
ms.date: 03/06/2017
ms.prod: reporting-services
ms.prod_service: reporting-services-native
ms.component: report-server-web-service
ms.reviewer: ''
ms.suite: pro-bi
ms.technology: ''
ms.tgt_pltfrm: ''
ms.topic: reference
applies_to:
- SQL Server 2016 Preview
ms.assetid: d3e658c9-bb22-480b-a3d5-bcde8f537ab2
caps.latest.revision: 4
author: markingmyname
ms.author: maghan
manager: kfile
ms.openlocfilehash: bd5f023ba4dd5424e9e5ca270cc24161537d0465
ms.sourcegitcommit: 1740f3090b168c0e809611a7aa6fd514075616bf
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/03/2018
ms.locfileid: "33025402"
---
# <a name="model-methods---report-server-web-service"></a>Métodos de modelo: servicio web del servidor de informes
  Puede utilizar estos métodos para administrar los modelos.  
  
|Método|Acción|  
|------------|------------|  
|<xref:ReportService2010.ReportingService2010.GenerateModel%2A>|Genera un modelo predeterminado encima de un origen de datos compartido.|  
|<xref:ReportService2010.ReportingService2010.GetModelItemPermissions%2A>|Recupera los permisos de usuario que están asociados al elemento de modelo.|  
|<xref:ReportService2010.ReportingService2010.GetModelItemPolicies%2A>|Recupera las directivas que están asociadas a un elemento de modelo.|  
|<xref:ReportService2010.ReportingService2010.GetUserModel%2A>|Devuelve la parte semántica de un modelo para el usuario actual.|  
|<xref:ReportService2010.ReportingService2010.InheritModelItemParentSecurity%2A>|Elimina las directivas que están asociadas a un elemento de modelo y hace que el elemento de modelo herede las directivas de su elemento primario.|  
|<xref:ReportService2010.ReportingService2010.ListModelDrillthroughReports%2A>|Enumera los informes detallados que están asociados a una entidad en un modelo.|  
|<xref:ReportService2010.ReportingService2010.ListModelItemChildren%2A>|Devuelve una matriz de elementos secundarios del elemento de modelo.|  
|<xref:ReportService2010.ReportingService2010.ListModelItemTypes%2A>|Devuelve una lista de los tipos de elemento de modelo admitidos.|  
|<xref:ReportService2010.ReportingService2010.ListModelPerspectives%2A>|Enumera los modelos y perspectivas que están disponibles para el usuario.|  
|<xref:ReportService2010.ReportingService2010.RegenerateModel%2A>|Actualiza un modelo existente según los cambios del esquema del origen de datos.|  
|<xref:ReportService2010.ReportingService2010.RemoveAllModelItemPolicies%2A>|Elimina todas las directivas que están asociadas a los elementos de modelo en el modelo especificado.|  
|<xref:ReportService2010.ReportingService2010.SetModelDrillthroughReports%2A>|Asocia un conjunto de informes detallados junto con un modelo.|  
|<xref:ReportService2010.ReportingService2010.SetModelItemPolicies%2A>|Establece las directivas de seguridad en un elemento de modelo.|  
  
## <a name="see-also"></a>Ver también  
 [Creación de aplicaciones con el servicio web y .NET Framework](../../../reporting-services/report-server-web-service/net-framework/building-applications-using-the-web-service-and-the-net-framework.md)   
 [Servicio web del servidor de informes](../../../reporting-services/report-server-web-service/report-server-web-service.md)   
 [Métodos del servicio web del servidor de informes](../../../reporting-services/report-server-web-service/methods/report-server-web-service-methods.md)   
 [Referencia técnica &#40;SSRS&#41;](../../../reporting-services/technical-reference-ssrs.md)  
  
  

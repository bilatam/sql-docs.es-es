---
title: Datos de informes de Reporting Services móviles | Microsoft Docs
ms.custom: ''
ms.date: 02/08/2016
ms.prod: reporting-services
ms.prod_service: reporting-services-native
ms.component: mobile-reports
ms.reviewer: ''
ms.suite: pro-bi
ms.technology: ''
ms.tgt_pltfrm: ''
ms.topic: conceptual
ms.assetid: 91138ef8-ddb4-4ac5-a1e4-fa4cf1c58dcc
caps.latest.revision: 15
author: maggiesMSFT
ms.author: maggies
manager: kfile
ms.openlocfilehash: b505c769fc86dd62b738a54c20c98adafd69db60
ms.sourcegitcommit: 1740f3090b168c0e809611a7aa6fd514075616bf
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/03/2018
ms.locfileid: "33018272"
---
# <a name="data-for-reporting-services-mobile-reports"></a>Datos de informes de Reporting Services móviles
El modelo de datos del [!INCLUDE[PRODUCT_NAME](../../includes/ss-mobilereptpub-long.md)] es sencillo. Los datos se importan en el [!INCLUDE[PRODUCT_NAME](../../includes/ss-mobilereptpub-short.md)] como una colección de conjuntos de datos. No son necesarias relaciones formales entre conjuntos de datos. Las búsquedas de un conjunto de datos a otro funcionarán siempre que coincidan los valores de clave. Las agregaciones de fecha y hora las controla el tiempo de ejecución de informe móvil y coincidirán entre diferentes conjuntos de datos, incluso si la granularidad de datos de fecha y hora es distinta entre los conjuntos de datos.   
  
Puede importar datos desde dos tipos de orígenes:   
  
* **Archivos de Excel locales**: seleccione un documento de Excel y seleccione las hojas de cálculo para importar. Después de la importación, los datos se almacenan en la definición de informe móvil. Para actualizar los datos del archivo original de Excel, use el comando **Actualizar datos** en la esquina superior derecha de la pestaña [!INCLUDE[PRODUCT_NAME](../../includes/ss-mobilereptpub-short.md)] **Data** tab. Obtenga más información sobre cómo [preparar datos de Excel para informes móviles de SSRS](../../reporting-services/mobile-reports/prepare-excel-data-for-reporting-services-mobile-reports.md).  
  
* **Conjuntos de datos compartidos de [!INCLUDE[PRODUCT_NAME](../../includes/server-product-name.md)]**: examine la lista de conjuntos de datos publicados en el servidor y seleccione los que quiere agregar al informe móvil. Los informes móviles basados en datos de servidor están siempre conectados a los conjuntos de datos de servidor originales y reflejan el estado más reciente de los datos en el servidor. Vea una [lista de orígenes de datos admitidos](https://msdn.microsoft.com/library/ms159219.aspx).   
  
  Obtenga más información sobre cómo [obtener datos de conjuntos de datos compartidos en el Publicador de informes móviles](../../reporting-services/mobile-reports/get-data-from-shared-datasets-in-reporting-services-mobile-reports.md).  
  
Después de importar los datos en el [!INCLUDE[PRODUCT_NAME](../../includes/ss-mobilereptpub-short.md)], el resto de la experiencia de diseño y creación de informes móviles es igual, independientemente de dónde provengan los datos.   
  
## <a name="connect-mobile-report-elements-to-data"></a>Conectar elementos del informe móvil con datos ##  
  
Cada elemento de [!INCLUDE[PRODUCT_NAME](../../includes/short-product-name.md)] contiene una o varias configuraciones de datos. Por ejemplo, el elemento Medidor radial contiene dos configuraciones de datos: valor principal y valor de comparación. Cada una de estas configuraciones apunta a exactamente un campo (columna) en un conjunto de datos específico.   
  
El tiempo de ejecución de informes móviles proporciona valores agregados para el medidor, según las selecciones del usuario. Tenga en cuenta que el valor de comparación de la misma instancia del medidor radial se puede enlazar a un campo de un conjunto de datos diferente.   
  
### <a name="see-also"></a>Vea también  
-  [Preparar datos para informes de Reporting Services móviles](../../reporting-services/mobile-reports/prepare-data-for-reporting-services-mobile-reports.md)
- [Create and publish mobile reports with SQL Server Mobile Report Publisher (Creación y publicación de informes móviles con el Publicador de informes de SQL Server Mobile)](../../reporting-services/mobile-reports/create-mobile-reports-with-sql-server-mobile-report-publisher.md)  
- [Obtener datos de conjuntos de datos compartidos](../../reporting-services/mobile-reports/get-data-from-shared-datasets-in-reporting-services-mobile-reports.md)
- [Conservar el formato de fecha para Analysis Services en los informes móviles](../../reporting-services/mobile-reports/retain-date-formatting-for-analysis-services-in-mobile-reports.md) 
  
  


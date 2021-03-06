---
title: Administrador de conexiones OLE DB | Microsoft Docs
ms.custom: ''
ms.date: 03/06/2017
ms.prod: sql-server-2014
ms.reviewer: ''
ms.suite: ''
ms.technology:
- integration-services
ms.tgt_pltfrm: ''
ms.topic: conceptual
helpviewer_keywords:
- OLE DB connection manager
- data sources [Integration Services], connections
- connection managers [Integration Services], OLE DB
- connections [Integration Services], OLE DB
ms.assetid: 91e3622e-4b1a-439a-80c7-a00b90d66979
caps.latest.revision: 56
author: douglaslMS
ms.author: douglasl
manager: craigg
ms.openlocfilehash: 11b88bd8144651abfed39fb5b68316abc23f09a5
ms.sourcegitcommit: c18fadce27f330e1d4f36549414e5c84ba2f46c2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/02/2018
ms.locfileid: "37295145"
---
# <a name="ole-db-connection-manager"></a>OLE DB, administrador de conexiones
  Un administrador de conexiones OLE DB permite a un paquete conectarse a un origen de datos mediante un proveedor OLE DB. Por ejemplo, un administrador de conexiones OLE DB que se conecta a [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] puede usar el proveedor [!INCLUDE[msCoName](../../includes/msconame-md.md)] OLE DB para [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)].  
  
> [!NOTE]  
>  El proveedor OLE DB de [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] Native Client 11.0 no admite las nuevas palabras clave de cadena de conexión (MultiSubnetFailover=True) para la agrupación en clústeres de conmutación por error de varias subredes. Para obtener más información, consulte el [notas de la versión de SQL Server](http://go.microsoft.com/fwlink/?LinkId=247824) y la entrada de blog, [conmutación por error de AlwaysOn varias subredes y SSIS](http://go.microsoft.com/fwlink/?LinkId=247825), en www.mattmasson.com.  
  
 Varias tareas y componentes de flujo de datos de [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] [!INCLUDE[ssISnoversion](../../includes/ssisnoversion-md.md)] usan un administrador de conexiones OLE DB. Por ejemplo, un origen de OLE DB y un destino de OLE DB usan este administrador de conexiones para extraer y cargar datos, y la tarea Ejecutar SQL puede usar este administrador de conexiones para conectarse a una base de datos de [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] para ejecutar consultas.  
  
 El administrador de conexiones OLE DB también se usa para obtener acceso a orígenes de datos OLE DB en tareas personalizadas escritas en código no administrado que usa un lenguaje como, por ejemplo, C++.  
  
 Cuando se agrega un administrador de conexiones OLE DB a un paquete, [!INCLUDE[ssISnoversion](../../includes/ssisnoversion-md.md)] crea una conexión de administrador que se resuelve como una conexión OLE DB en tiempo de ejecución, Establece las propiedades del Administrador de la conexión y agrega el Administrador de conexiones para el `Connections` colección en el paquete.  
  
 El `ConnectionManagerType` propiedad del Administrador de conexiones se establece en `OLEDB`.  
  
 El administrador de conexiones OLE DB se puede configurar de las maneras siguientes:  
  
-   Proporcionar una cadena de conexión específica configurada para cumplir con los requisitos del proveedor seleccionado.  
  
-   Según el proveedor, incluir el nombre del origen de datos al cual conectarse.  
  
-   Proporcionar credenciales de seguridad según resulte apropiado para el proveedor seleccionado.  
  
-   Indicar si la conexión creada desde el administrador de conexiones se conserva en el tiempo de ejecución.  
  
## <a name="logging"></a>Registro  
 Puede registrar las llamadas realizadas por el administrador de conexiones OLE DB a proveedores de datos externos. Puede utilizar esta capacidad de registro para solucionar problemas relacionados con las conexiones que el administrador de conexiones OLE DB establece con orígenes de datos externos. Para registrar las llamadas que el administrador de conexiones OLE DB realiza a proveedores de datos externos, habilite el registro de paquetes y seleccione el evento **Diagnostic** en el nivel de paquete. Para obtener más información, vea [Herramientas para solucionar problemas con la ejecución de paquetes](../troubleshooting/troubleshooting-tools-for-package-execution.md).  
  
## <a name="configuration-of-the-oledb-connection-manager"></a>Configuración del administrador de conexiones OLE DB  
 Puede establecer propiedades a través del Diseñador de [!INCLUDE[ssIS](../../includes/ssis-md.md)] o mediante programación. Para obtener más información sobre las propiedades que puede configurar en el Diseñador [!INCLUDE[ssIS](../../includes/ssis-md.md)] , vea [Configurar el administrador de conexiones OLE DB](../configure-ole-db-connection-manager.md). Para obtener información acerca de cómo configurar un administrador de conexiones mediante programación, vea la documentación de la clase **T:Microsoft.SqlServer.Dts.Runtime.ConnectionManager** en la Guía del desarrollador.  
  
## <a name="related-content"></a>Contenido relacionado  
  
-   Artículo wiki, sobre [SSIS con conectores Oracle](http://go.microsoft.com/fwlink/?LinkId=220670) en social.technet.microsoft.com.  
  
-   Artículo técnico, sobre [cadenas de conexión para proveedores OLE DB](http://go.microsoft.com/fwlink/?LinkId=220744), en carlprothman.net.  
  
## <a name="see-also"></a>Vea también  
 [Origen de OLE DB](../data-flow/ole-db-source.md)   
 [Destino de OLE DB](../data-flow/ole-db-destination.md)   
 [Tarea Ejecutar SQL](../control-flow/execute-sql-task.md)   
 [Servicios de integración &#40;SSIS&#41; conexiones](integration-services-ssis-connections.md)  
  
  

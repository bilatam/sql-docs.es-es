---
title: 'Cómo: Conectar con una base de datos y examinar objetos existentes | Microsoft Docs'
ms.custom:
- SSDT
ms.date: 02/09/2017
ms.prod: sql
ms.technology: ssdt
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: conceptual
f1_keywords:
- sql.data.tools.connectionpicker.f1
ms.assetid: 9b331800-3806-4459-ac58-88cdc98124d3
caps.latest.revision: 10
author: stevestein
ms.author: sstein
manager: craigg
ms.openlocfilehash: f342f1427b9943d14216fc5b785036036dd57345
ms.sourcegitcommit: c8f7e9f05043ac10af8a742153e81ab81aa6a3c3
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 07/17/2018
ms.locfileid: "39082687"
---
# <a name="how-to-connect-to-a-database-and-browse-existing-objects"></a>Cómo: Conectar con una base de datos y examinar objetos existentes
Una tarea muy frecuente que realizan los administradores y desarrolladores de bases de datos es conectarse a una base de datos activa, diseñar o examinar su esquema y realizar consultas de sus objetos. El Explorador de objetos de SQL Server de Visual Studio contiene ahora un nodo **SQL Server** dedicado bajo el cual están agrupadas todas las instancias conectadas de SQL Server y sus bases de datos, en una jerarquía similar a la de SSMS. Las instancias conectadas de SQL Server pueden ser una instancia local, como un servidor con SQL Server 2008 en ejecución, o una instancia remota de SQL Azure.  
  
En el procedimiento siguiente se da por supuesto que ya ha instalado la base de datos de ejemplo AdventureWorks. Use [CodePlex](http://msftdbprodsamples.codeplex.com/) para encontrar e instalar bases de datos de ejemplo para distintas versiones de SQL Server. Si lo prefiere, también puede seguir los pasos y usar una base de datos existente en su servidor.  
  
### <a name="to-connect-to-a-database-instance"></a>Para conectar con una instancia de base de datos  
  
1.  En Visual Studio, asegúrese de que el **Explorador de objetos de SQL Server** está abierto. Si no lo está, haga clic en el menú **Ver** y seleccione **Explorador de objetos de SQL Server**.  
  
2.  Haga clic con el botón derecho en el nodo **SQL Server** del **Explorador de objetos de SQL Server** y seleccione **Agregar SQL Server**.  
  
3.  En el cuadro de diálogo **Conectar con el servidor** , escriba el **Nombre del servidor** de la instancia de servidor con la que desee conectar, escriba sus credenciales y, a continuación, haga clic en **Conectar**.  
  
4.  En el **Explorador de objetos de SQL Server**, expanda el nodo **Bases de datos** en la instancia de servidor. Verá que todas las bases de datos que residen en esta instancia de servidor se agregan bajo este nodo **Bases de datos** .  
  
5.  Expanda el nodo **AdventureWorks** (u otra base de datos). Observe que todas las entidades de base de datos están organizadas en una jerarquía similar a la de SQL Server Management Studio.  
  

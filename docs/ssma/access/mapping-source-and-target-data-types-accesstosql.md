---
title: Asignación de origen y los tipos de datos de destino (AccessToSQL) | Microsoft Docs
ms.prod: sql
ms.custom: ''
ms.date: 01/19/2017
ms.reviewer: ''
ms.suite: sql
ms.technology: ssma
ms.tgt_pltfrm: ''
ms.topic: conceptual
applies_to:
- Azure SQL Database
- SQL Server
helpviewer_keywords:
- customizing data type mappings
- data types, mapping
- mapping, data types
- source data types
- target data types
ms.assetid: b362a075-16e7-423f-b63f-e1e9f02844a9
caps.latest.revision: 14
author: Shamikg
ms.author: Shamikg
manager: craigg
ms.openlocfilehash: 4868bbe408b96c95a44c82516ce9bb6c9035397e
ms.sourcegitcommit: c7a98ef59b3bc46245b8c3f5643fad85a082debe
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/12/2018
ms.locfileid: "38979607"
---
# <a name="mapping-source-and-target-data-types-accesstosql"></a>Asignación de origen y los tipos de datos de destino (AccessToSQL)
Tipos de base de datos de acceso difieren de [!INCLUDE[ssNoVersion](../../includes/ssnoversion_md.md)] tipos base de datos. Al convertir objetos de base de datos de Access a [!INCLUDE[ssNoVersion](../../includes/ssnoversion_md.md)] objetos, debe especificar cómo se asignan los tipos de datos de acceso a [!INCLUDE[ssNoVersion](../../includes/ssnoversion_md.md)]. Puede aceptar las asignaciones de tipos de datos de forma predeterminada, o puede personalizar las asignaciones como se muestra en los procedimientos siguientes.  
  
## <a name="default-mappings"></a>Asignaciones predeterminadas  
SSMA tiene un conjunto predeterminado de asignaciones de tipos de datos. Para obtener la lista de asignaciones predeterminadas, vea [configuración del proyecto (asignación de tipos)](http://msdn.microsoft.com/b87b9683-abed-4677-8c50-18bdba704655).  
  
## <a name="customizing-data-type-mappings"></a>Personalizar asignaciones de tipos de datos  
Mediante el uso de la **configuración del proyecto** cuadro de diálogo, puede personalizar cómo se asignan los tipos de todas las bases de datos y objetos de base de datos en un proyecto. Las asignaciones de tipos para un proyecto se aplican a todas las bases de datos y objetos de base de datos que no tiene asignaciones de tipos personalizado.  
  
También puede personalizar la asignación de tipos de datos en el nivel de base de datos o tabla.  
  
El siguiente procedimiento muestra cómo asignar tipos de datos en el proyecto, la base de datos o el nivel de objeto de base de datos.  
  
**Para asignar tipos de datos**  
  
1.  Para personalizar la asignación de tipos de datos para todo el proyecto, abra el **configuración del proyecto** cuadro de diálogo:  
  
    1.  En el **herramientas** menú, seleccione **configuración del proyecto**.  
  
    2.  En el panel izquierdo, seleccione **Type Mapping**.  
  
        El gráfico de asignación de tipo y los botones aparecen en el panel derecho.  
  
    O bien, para personalizar la asignación de tipos de datos en el nivel de base de datos o tabla, seleccione la tabla o base de datos en el panel Explorador de metadatos de acceso:  
  
    1.  En el panel Explorador de metadatos de acceso, expanda **acceso de metabase**y, a continuación, expanda **bases de datos**.  
  
    2.  Seleccione la base de datos o una tabla para el que desea personalizar la asignación de tipos de datos.  
  
    3.  En el panel derecho, haga clic en **Type Mapping**.  
  
2.  Para agregar una nueva asignación, realice lo siguiente:  
  
    1.  En el panel de asignación de tipo, haga clic en **agregar**.  
  
    2.  En el **nueva asignación de tipo** cuadro de diálogo **tipo de origen**, seleccione el tipo de datos de acceso para asignar.  
  
    3.  Si el tipo requiere una longitud, especifique las longitudes de datos mínimo y máximo para la asignación seleccionando la **desde** y **a** casillas de verificación y, a continuación, escriba los valores.  
  
        Esto le permite personalizar la asignación de datos para los valores más pequeños y más grandes del mismo tipo de datos.  
  
    4.  En **tipo de destino**, seleccione el destino [!INCLUDE[ssNoVersion](../../includes/ssnoversion_md.md)] tipo de datos.  
  
        Algunos tipos requieren una longitud del tipo de datos de destino. Si es necesario, escriba la nueva longitud de datos en el **reemplazar con** cuadro y, a continuación, haga clic en **Aceptar**.  
  
3.  Para editar una asignación de tipos de datos, realice lo siguiente:  
  
    1.  En el panel de asignación de tipo, haga clic en **editar**.  
  
    2.  En el **lista de asignación de tipo** cuadro de diálogo **tipo de origen**, seleccione el tipo de datos de acceso para asignar.  
  
    3.  Si el tipo requiere una longitud, especifique las longitudes de datos mínimo y máximo para la asignación seleccionando la **desde** y **a** casillas de verificación y, a continuación, escriba los valores.  
  
        Esto le permite personalizar la asignación de datos para los valores más pequeños y más grandes del mismo tipo de datos.  
  
    4.  En **tipo de destino**, seleccione el destino [!INCLUDE[ssNoVersion](../../includes/ssnoversion_md.md)] tipo de datos.  
  
        Algunos tipos requieren una longitud del tipo de datos de destino. Si es necesario, escriba la nueva longitud de datos en el **reemplazar con** cuadro y, a continuación, haga clic en **Aceptar**.  
  
4.  Para quitar una asignación de tipos de datos, realice lo siguiente:  
  
    1.  En el panel de asignación de tipos, seleccione la fila en la lista de asignación de tipo que contiene la asignación de tipos de datos que desea quitar.  
  
    2.  Haga clic en **Quitar**.  
  
## <a name="next-steps"></a>Pasos siguientes  
El siguiente paso del proceso de migración es [convertir objetos de base de datos de acceso a objetos de SQL Server](http://msdn.microsoft.com/e0ef67bf-80a6-4e6c-a82d-5d46e0623c6c)  
  
## <a name="see-also"></a>Vea también  
[Migrar bases de datos de Access a SQL Server](http://msdn.microsoft.com/76a3abcf-2998-4712-9490-fe8d872c89ca)  
  

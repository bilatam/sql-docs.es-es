---
title: Describir los tipos de datos del controlador JDBC
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.suite: sql
ms.technology: connectivity
ms.tgt_pltfrm: ''
ms.topic: conceptual
ms.assetid: 7802328d-4d23-4775-9573-4169b127d258
caps.latest.revision: 27
author: MightyPen
ms.author: genemi
manager: craigg
ms.openlocfilehash: 594e5770335779e0555d0ba9911923e487d5db53
ms.sourcegitcommit: 2f9cafc1d7a3773a121bdb78a095018c8b7c149f
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/08/2018
ms.locfileid: "39661667"
---
# <a name="understanding-the-jdbc-driver-data-types"></a>Describir los tipos de datos del controlador JDBC

[!INCLUDE[Driver_JDBC_Download](../../includes/driver_jdbc_download.md)]

El [!INCLUDE[jdbcNoVersion](../../includes/jdbcnoversion_md.md)] admite el uso de los tipos de datos básicos y avanzados de JDBC dentro de una aplicación Java que use [!INCLUDE[ssNoVersion](../../includes/ssnoversion_md.md)] como base de datos.  
  
El sistema de tipos de JDBC arbitra la conversión entre los tipos de datos de [!INCLUDE[ssNoVersion](../../includes/ssnoversion_md.md)] y los tipos y objetos del lenguaje Java. Los tipos de JDBC se modelan en los tipos SQL-92 y SQL-99. El controlador JDBC sigue la especificación de JDBC y está diseñado para proporcionar un equilibrio correcto derecho entre previsibilidad y flexibilidad.  
  
En los temas de esta sección se describe cómo utilizar los tipos de datos básicos y avanzados, y cómo se pueden convertir en otros tipos de datos.  
  
## <a name="in-this-section"></a>En esta sección  
  
| Tema                                                                                                                                            | Descripción                                                                                                                                                                                                                                                          |
| ------------------------------------------------------------------------------------------------------------------------------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [Usar tipos de datos básicos](../../connect/jdbc/using-basic-data-types.md)                                                                           | Describe los tipos de datos básicos de JDBC. Incluye ejemplos de cómo trabajar con los tipos de datos utilizando conjuntos de resultados, consultas parametrizadas y procedimientos almacenados.                                                                                                        |
| [Configurar el modo en que los valores java.sql.Time se envían al servidor](../../connect/jdbc/configuring-how-java-sql-time-values-are-sent-to-the-server.md) | Describe cómo el controlador JDBC genera fechas.                                                                                                                                                                                                                       |
| [Usar tipos de datos avanzados](../../connect/jdbc/using-advanced-data-types.md)                                                                     | Describe los tipos de datos avanzados de JDBC.                                                                                                                                                                                                                              |
| [Descripción de las diferencias entre los tipos de datos](../../connect/jdbc/understanding-data-type-differences.md)                                                 | Describe las diferencias entre los diversos tipos de datos del controlador JDBC.                                                                                                                                                                                                    |
| [Descripción de las conversiones de tipos de datos](../../connect/jdbc/understanding-data-type-conversions.md)                                                 | Describe cómo se administra la conversión de tipos de datos cuando se usan métodos establecedor y captador.                                                                                                                                                                                  |
| [Compatibilidad con el juego de caracteres nacional](../../connect/jdbc/national-character-set-support.md)                                                           | Describe la compatibilidad con los tipos del juego de caracteres nacionales.                                                                                                                                                                                                          |
| [Compatibilidad con datos XML](../../connect/jdbc/supporting-xml-data.md)                                                                                 | Describe la interfaz SQLXML. También describe cómo leer y escribir datos XML desde y en una base de datos relacional con el tipo de datos Java de **SQLXML**.                                                                                                             |
| [Contenedores e interfaces](../../connect/jdbc/wrappers-and-interfaces.md)                                                                         | Explica las interfaces que tienen los métodos y constantes específicos de [!INCLUDE[jdbcNoVersion](../../includes/jdbcnoversion_md.md)] que permiten que un servidor de aplicaciones cree un proxy de la clase; asimismo, describe la compatibilidad con la interfaz `java.sql.Wrapper`. |
  
## <a name="see-also"></a>Ver también

[Introducción al controlador JDBC](../../connect/jdbc/overview-of-the-jdbc-driver.md)  

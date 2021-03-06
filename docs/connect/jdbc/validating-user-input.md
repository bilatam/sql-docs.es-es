---
title: Validar la entrada del usuario | Microsoft Docs
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.suite: sql
ms.technology: connectivity
ms.tgt_pltfrm: ''
ms.topic: conceptual
ms.assetid: 8aa867b0-e6f0-49eb-93d3-817ae2ed8f77
caps.latest.revision: 11
author: MightyPen
ms.author: genemi
manager: craigg
ms.openlocfilehash: a2320ed83c095d460aa233ac0227f37c15eca88b
ms.sourcegitcommit: 2f9cafc1d7a3773a121bdb78a095018c8b7c149f
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/08/2018
ms.locfileid: "39662317"
---
# <a name="validating-user-input"></a>Validar los datos introducidos por el usuario

[!INCLUDE[Driver_JDBC_Download](../../includes/driver_jdbc_download.md)]

Cuando construya una aplicación que tiene acceso a datos, debería suponer que todos los datos proporcionados por el usuario son malintencionados hasta que se demuestre lo contrario. Si no lo hace, la aplicación puede quedar en una situación de vulnerabilidad frente a ataques. Un tipo de ataque que puede producirse se denomina inyección de SQL y consiste en que se agrega código malintencionado a cadenas que luego se pasan a una instancia de [!INCLUDE[ssNoVersion](../../includes/ssnoversion_md.md)] para analizarse y ejecutarse. Para evitar este tipo de ataque, debería utilizar procedimientos almacenados con parámetros cuando sea posible y validar siempre los datos que proporcione el usuario.

Validar los datos que proporciona el usuario en el código cliente es importante para no malgastar viajes de ida y vuelta al servidor. Es igualmente importante validar los parámetros para los procedimientos almacenados en el servidor con el fin de detectar las entradas que no son válidas y que omiten la validación del lado cliente.

Para obtener más información sobre la inyección de SQL y cómo evitarla, vea "Inyección de código SQL" en Libros en pantalla de [!INCLUDE[ssNoVersion](../../includes/ssnoversion_md.md)]. Para obtener más información sobre cómo validar parámetros de procedimientos almacenados, vea "Procedimientos almacenados ([!INCLUDE[ssDE](../../includes/ssde_md.md)])" y otros temas secundarios en Libros en pantalla de [!INCLUDE[ssNoVersion](../../includes/ssnoversion_md.md)].

## <a name="see-also"></a>Ver también

[Proteger las aplicaciones del controlador JDBC](../../connect/jdbc/securing-jdbc-driver-applications.md)

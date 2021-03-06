---
title: Compatibilidad internacional (controlador ODBC de Visual FoxPro) | Documentos de Microsoft
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.suite: sql
ms.technology: connectivity
ms.tgt_pltfrm: ''
ms.topic: conceptual
helpviewer_keywords:
- double-byte character sets [ODBC]
- FoxPro ODBC driver [ODBC], international support
- DBCS [ODBC]
- international support [ODBC]
- sort order [ODBC]
- collating sequences [ODBC]
- Visual FoxPro ODBC driver [ODBC], international support
ms.assetid: cd3fab32-13f1-4a86-abc4-5e18667669fc
caps.latest.revision: 5
author: MightyPen
ms.author: genemi
manager: craigg
ms.openlocfilehash: 151d3989737d221e46f6771055d0775c69f7e576
ms.sourcegitcommit: 1740f3090b168c0e809611a7aa6fd514075616bf
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/03/2018
ms.locfileid: "32899920"
---
# <a name="international-support-visual-foxpro-odbc-driver"></a>Compatibilidad internacional (controlador ODBC de Visual FoxPro)
Es compatible con el controlador ODBC de Microsoft Visual FoxPro:  
  
-   Juegos de caracteres de doble byte (DBCS)  
  
-   Varias secuencias de intercalación  
  
 Una secuencia de intercalación define el *criterio de ordenación* para los datos almacenados en una tabla de Visual FoxPro o una base de datos. De forma predeterminada, el controlador está configurado para utilizar las secuencias de intercalación que admiten la versión de idioma del sistema operativo.  
  
 Para obtener una lista de secuencias de intercalación admitidas, consulte [establecer COLLATE](../../odbc/microsoft/set-collate-command.md).  
  
## <a name="locale"></a>configuración regional  
 El conjunto de información que corresponde a un determinado idioma y país o región. Una configuración regional indica opciones específicas como separadores decimales, fecha y formatos de hora y orden de clasificación de caracteres.  
  
## <a name="sort-order"></a>criterio de ordenación  
 Criterios de ordenación incorporan las reglas de ordenación de diferentes *configuración regional*s, lo que le permite ordenar los datos en esos idiomas correctamente. En Visual FoxPro, el criterio de ordenación actual determina los resultados de las comparaciones de expresión de caracteres y el orden en que aparecen en los registros de la indización u ordenar tablas.

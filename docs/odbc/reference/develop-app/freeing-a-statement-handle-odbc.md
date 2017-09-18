---
title: "Liberar un identificador de instrucción ODBC | Documentos de Microsoft"
ms.custom: 
ms.date: 01/19/2017
ms.prod: sql-non-specified
ms.reviewer: 
ms.suite: 
ms.technology:
- drivers
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- statement handles [ODBC]
- handles [ODBC], statement
- freeing statement handles [ODBC]
ms.assetid: ee18e2f1-2690-4cc1-9e5c-e20244e5d480
caps.latest.revision: 5
author: MightyPen
ms.author: genemi
manager: jhubbard
ms.translationtype: MT
ms.sourcegitcommit: f7e6274d77a9cdd4de6cbcaef559ca99f77b3608
ms.openlocfilehash: b33d262c846d9ef8a41bf9440802664ac7d4b75f
ms.contentlocale: es-es
ms.lasthandoff: 09/09/2017

---
# <a name="freeing-a-statement-handle-odbc"></a>Liberar un identificador de instrucción ODBC
Como se mencionó anteriormente, es más eficaz volver a usar las instrucciones que to quitarlos y asignar unos nuevos. Antes de ejecutar una nueva instrucción SQL en una instrucción, las aplicaciones deben estar seguro de que la configuración de la instrucción actual es adecuada. Éstos incluyen atributos de instrucción, enlaces de parámetros y enlaces de conjunto de resultados. Por lo general, parámetros y conjuntos de resultados para la instrucción SQL anterior deben ser independiente (mediante una llamada a **SQLFreeStmt** con las opciones SQL_RESET_PARAMS y SQL_UNBIND) y se vuelve a enlazar para la nueva instrucción SQL.  
  
 Cuando la aplicación ha terminado de usar la instrucción, llama al método **SQLFreeHandle** para liberar la instrucción. Después de liberar la instrucción, es un error de programación de aplicaciones para usar el identificador de la instrucción en una llamada a una función ODBC; al hacerlo de modo que tiene consecuencias no definidas, pero probablemente irrecuperables.  
  
 Cuando **SQLFreeHandle** se llama, las versiones de controlador la estructura que se utiliza para almacenar información acerca de la instrucción.  
  
 **SQLDisconnect** libera automáticamente todas las instrucciones de una conexión.
---
title: CREAR las limitaciones de la instrucción de índice | Documentos de Microsoft
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
- CREATE INDEX statement limitations [ODBC]
- ODBC SQL grammar, CREATE INDEX statement limitations
ms.assetid: 832dcda1-e452-48e6-8adb-7fb33c4fb4ff
caps.latest.revision: 5
author: MightyPen
ms.author: genemi
manager: craigg
ms.openlocfilehash: e9501e07fcdb70984153a718eed22be4d5448ec9
ms.sourcegitcommit: 1740f3090b168c0e809611a7aa6fd514075616bf
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/03/2018
---
# <a name="create-index-statement-limitations"></a>CREAR las limitaciones de la instrucción de índice
La instrucción CREATE INDEX no se admite para los controladores de Microsoft Excel o texto.  
  
 Un índice puede definirse en un máximo de 10 columnas. Si más de 10 columnas se incluyen en una instrucción CREATE INDEX, no se reconocerá el índice y la tabla se tratará como si no se crearon ningún índice.  
  
 El controlador de dBASE no puede crear un índice en una columna lógica.  
  
 Cuando se utiliza el controlador dBASE, puede mejorar el tiempo de respuesta en los archivos de gran tamaño mediante la creación de un índice .mdx (o .ndx) en la columna (campo) especificado en las cláusulas WHERE de una instrucción SELECT. Los índices .mdx existentes se aplicarán automáticamente for =, >, \<, > =, = < y entre los operadores en una cláusula WHERE y predicados LIKE, así como en los predicados de combinación.  
  
 Cuando se utiliza el controlador de dBASE, el índice creado por una instrucción CREATE UNIQUE INDEX es realmente no es único, y pueden ser inserten valores duplicados en la columna indizada. Sólo un registro de un conjunto de valores clave idénticos puede agregarse al índice.  
  
 Cuando se utiliza el controlador de Paradox, debe definirse un índice único en un subconjunto de las columnas de una tabla, como la primera columna contiguo. Una tabla no se puede actualizar el controlador de Paradox si un índice único no está definido en la tabla o cuando se usa el controlador de Paradox sin la implementación del motor de base de datos de Borland.

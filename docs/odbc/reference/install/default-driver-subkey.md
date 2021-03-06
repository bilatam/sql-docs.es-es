---
title: Predeterminado subclave Driver | Documentos de Microsoft
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
- default subkey [ODBC]
- registry entries for components [ODBC], default subkey
- subkeys [ODBC], default subkey
- drivers subkey [ODBC]
ms.assetid: 9e58b24f-ebfc-4286-a272-0843b4d6f2d5
caps.latest.revision: 5
author: MightyPen
ms.author: genemi
manager: craigg
ms.openlocfilehash: 6563627087ce8516f74f478b35f0f6a896aa025b
ms.sourcegitcommit: 1740f3090b168c0e809611a7aa6fd514075616bf
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/03/2018
ms.locfileid: "32915740"
---
# <a name="default-driver-subkey"></a>Subclave de controlador predeterminado
La subclave predeterminado contiene un valor único que describe el controlador utilizado por el origen de datos predeterminado. El formato de este valor se muestra en la tabla siguiente.  
  
|Nombre|Tipo de datos|data|  
|----------|---------------|----------|  
|**Controlador**|REG_SZ|*Descripción del controlador predeterminado*|  
  
 El *descripción predeterminada del controlador* nombre es el mismo que el nombre del valor del bajo la subclave de controladores ODBC que describe el controlador.  
  
 Por ejemplo, si el origen de datos predeterminado utiliza el controlador de SQL Server, el valor bajo la subclave predeterminado podría ser:  
  
```  
Driver : REG_SZ : SQL Server  
```  
  
> [!NOTE]  
>  El controlador predeterminado de contenidos en la subclave predeterminado puede hacer referencia a un DSN de usuario predeterminado o un DSN de sistema de forma predeterminada. Si se crearon DSN un DSN de usuario predeterminado y un sistema de forma predeterminada, el controlador predeterminado se determina por el DSN que se creó en último lugar, por lo que quizás no sea una entrada válida para el DSN que creó en primer lugar.

---
title: PI (Transact-SQL) | Microsoft Docs
ms.custom: ''
ms.date: 03/03/2017
ms.prod: sql
ms.prod_service: database-engine, sql-database, sql-data-warehouse, pdw
ms.reviewer: ''
ms.suite: sql
ms.technology: t-sql
ms.tgt_pltfrm: ''
ms.topic: language-reference
f1_keywords:
- PI_TSQL
- PI
dev_langs:
- TSQL
helpviewer_keywords:
- constant value of PI
- PI function
ms.assetid: d7c4575b-ba1c-4ef7-a633-9a379d7f01fd
caps.latest.revision: 31
author: MashaMSFT
ms.author: mathoma
manager: craigg
monikerRange: '>=aps-pdw-2016||=azuresqldb-current||=azure-sqldw-latest||>=sql-server-2016||=sqlallproducts-allversions||>=sql-server-linux-2017'
ms.openlocfilehash: 3f816de1c7a9750199d8c8101d2562b218336f52
ms.sourcegitcommit: e02c28b0b59531bb2e4f361d7f4950b21904fb74
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/02/2018
ms.locfileid: "39451075"
---
# <a name="pi-transact-sql"></a>PI (Transact-SQL)
[!INCLUDE[tsql-appliesto-ss2008-all-md](../../includes/tsql-appliesto-ss2008-all-md.md)]

  Devuelve el valor constante de PI.  
  
 ![Icono de vínculo de tema](../../database-engine/configure-windows/media/topic-link.gif "Icono de vínculo de tema") [Convenciones de sintaxis de Transact-SQL](../../t-sql/language-elements/transact-sql-syntax-conventions-transact-sql.md)  
  
## <a name="syntax"></a>Sintaxis  
  
```  
PI ( )  
```  
  
## <a name="return-types"></a>Tipos devueltos  
 **float**  
  
## <a name="examples"></a>Ejemplos  
 El siguiente ejemplo devuelve el valor de `PI`.  
  
```  
SELECT PI();  
GO  
```  
  
 [!INCLUDE[ssResult](../../includes/ssresult-md.md)]  
  
```  
------------------------  
3.14159265358979  
  
(1 row(s) affected)  
```  
  
## <a name="see-also"></a>Ver también  
 [Funciones matemáticas &#40;Transact-SQL&#41;](../../t-sql/functions/mathematical-functions-transact-sql.md)  
  
  


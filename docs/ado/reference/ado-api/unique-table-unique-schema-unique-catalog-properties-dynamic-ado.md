---
title: Control de cambios en la tabla de Base de conjunto de registros (ADO) | Documentos de Microsoft
ms.prod: sql
ms.prod_service: connectivity
ms.technology: connectivity
ms.custom: ''
ms.date: 01/19/2017
ms.reviewer: ''
ms.suite: sql
ms.tgt_pltfrm: ''
ms.topic: conceptual
apitype: COM
helpviewer_keywords:
- Unique Table property [ADO]
- Unique Schema property [ADO]
- Unique Catalog property [ADO]
ms.assetid: d0e775d8-e353-46a1-ad10-ed4cc240dfaa
caps.latest.revision: 12
author: MightyPen
ms.author: genemi
manager: craigg
ms.openlocfilehash: 8351eb10101219b09450055526f0cb6a47a95b5f
ms.sourcegitcommit: 62826c291db93c9017ae219f75c3cfeb8140bf06
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "35282704"
---
# <a name="unique-table-unique-schema-unique-catalog-properties-dynamic-ado"></a>Tabla única, un esquema únicos, único catálogo dinámicos propiedades (ADO)
Le permite controlar las modificaciones realizadas en una tabla base concreta en un [Recordset](../../../ado/reference/ado-api/recordset-object-ado.md) que estaba formada por una operación JOIN en varias tablas base.  
  
-   **Tabla única** especifica el nombre de la tabla base en la que se permiten actualizaciones, inserciones y eliminaciones.  
  
-   **Esquema único** especifica la *esquema*, o el nombre del propietario de la tabla.  
  
-   **Único catálogo** especifica la *catálogo*, o el nombre de la base de datos que contiene la tabla.  
  
## <a name="settings-and-return-values"></a>Configuración y valores devueltos  
 Establece o devuelve un **cadena** valor que es el nombre de tabla, esquema o catálogo.  
  
## <a name="remarks"></a>Notas  
 La tabla base deseada se identifica por su catálogo, esquema y los nombres de tabla. Cuando el **tabla única** propiedad está establecida, los valores de la **único esquema** o **Unique Catalog** propiedades se utilizan para buscar la tabla base. Se recomienda, aunque no es necesario, que uno o ambos el **único esquema** y **Unique Catalog** propiedades establecerse antes de la **tabla única** se establece la propiedad.  
  
 La clave principal de la **tabla única** se trata como la clave principal de todo el **conjunto de registros**. Se trata de la clave que se usa para cualquier método que requiere una clave principal.  
  
 Mientras **tabla única** se establece, el [eliminar](../../../ado/reference/ado-api/delete-method-ado-recordset.md) método afecta solamente la tabla con nombre. El [AddNew](../../../ado/reference/ado-api/addnew-method-ado.md), [Resync](../../../ado/reference/ado-api/resync-method.md), [actualización](../../../ado/reference/ado-api/update-method.md), y [UpdateBatch](../../../ado/reference/ado-api/updatebatch-method.md) métodos afectan a las tablas base subyacentes adecuadas de la **Conjunto de registros**.  
  
 **Tabla única** debe especificarse antes de realizar cualquier sincronización personalizada. Si **tabla única** no se ha especificado, el [Resync Command](../../../ado/reference/ado-api/resync-command-property-dynamic-ado.md) propiedad no tiene ningún efecto.  
  
 Se produce un error de tiempo de ejecución si no se encuentra una única tabla base.  
  
 Estas propiedades dinámicas se anexan a la **Recordset** objeto [propiedades](../../../ado/reference/ado-api/properties-collection-ado.md) colección cuando la [CursorLocation](../../../ado/reference/ado-api/cursorlocation-property-ado.md) propiedad está establecida en  **adUseClient**.  
  
## <a name="applies-to"></a>Se aplica a  
 [Objeto de conjunto de registros (ADO)](../../../ado/reference/ado-api/recordset-object-ado.md)  
  
## <a name="see-also"></a>Vea también  
 [Objeto de conjunto de registros (ADO)](../../../ado/reference/ado-api/recordset-object-ado.md)

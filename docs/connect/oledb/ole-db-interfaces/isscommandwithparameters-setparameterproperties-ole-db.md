---
title: 'Isscommandwithparameters:: SetParameterProperties (OLE DB) | Microsoft Docs'
description: ISSCommandWithParameters::SetParameterProperties (OLE DB)
ms.custom: ''
ms.date: 06/14/2018
ms.prod: sql
ms.prod_service: database-engine, sql-database, sql-data-warehouse, pdw
ms.component: oledb|ole-db-interfaces
ms.reviewer: ''
ms.suite: sql
ms.technology:
- database-engine
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- ISSCommandWithParameters::SetParameterProperties (OLE DB)
apitype: COM
helpviewer_keywords:
- SetParameterProperties method
author: pmasl
ms.author: Pedro.Lopes
manager: craigg
ms.openlocfilehash: e04c6a678e204b741f4e0a494000b04ae575035f
ms.sourcegitcommit: 50838d7e767c61dd0b5e677b6833dd5c139552f2
ms.translationtype: MTE75
ms.contentlocale: es-ES
ms.lasthandoff: 07/18/2018
ms.locfileid: "39106071"
---
# <a name="isscommandwithparameterssetparameterproperties-ole-db"></a>ISSCommandWithParameters::SetParameterProperties (OLE DB)
[!INCLUDE[appliesto-ss-asdb-asdw-pdw-md](../../../includes/appliesto-ss-asdb-asdw-pdw-md.md)]

[!INCLUDE[Driver_OLEDB_Download](../../../includes/driver_oledb_download.md)]

  Establece las propiedades de los parámetros por cada parámetro por ordinal o establece las propiedades masivas de los parámetro especificando una matriz de estructuras SSPARAMPROPS.  
  
## <a name="syntax"></a>Sintaxis  
  
```  
  
HRESULT SetParameterProperties(  
      DB_UPARAMS cParams,   
      SSPARAMPROPS rgParamProperties[]);  
```  
  
## <a name="arguments"></a>Argumentos  
 *cParams*[in]  
 El número de estructuras SSPARAMPROPS en la matriz *rgParamProperties*. Si este número es cero, **ISSCommandWithParameters::SetParameterProperties** eliminará todas las propiedades que se puedan haber especificado en cualquier parámetro del comando.  
  
 *rgParamProperties*[in]  
 Una matriz de estructuras SSPARAMPROPS que se van a establecer.  
  
## <a name="return-code-values"></a>Valores de código de retorno  
 El método **ISSCommandWithParameters::SetParameterProperties** devuelve los mismos códigos de error que el método **ICommandProperties::SetProperties** de OLE DB básico.  
  
## <a name="remarks"></a>Notas  
 El establecimiento de propiedades de parámetro con este método se permite por parámetro y por ordinal, o bien mediante una única llamada a **ISSCommandWithParameters::SetParameterProperties** después de generar SSPARAMPROPS desde la matriz de propiedades.  
  
 Se debe llamar al método **SetParameterInfo** antes de llamar al método **ISSCommandWithParameters::SetParameterProperties**. La llamada a `SetParameterProperties(0, NULL)` borra todas las propiedades de parámetro especificadas, en tanto que la llamada a `SetParameterInfo(0,NULL,NULL)` borra toda la información de parámetros, incluidas las propiedades que puedan estar asociadas a un parámetro.  
  
 La llamada a **ISSCommandWithParameters::SetParameterProperties** para especificar propiedades de un parámetro que no es de tipo DBTYPE_XML o DBTYPE_UDT devuelve DB_E_ERRORSOCCURRED o DB_S_ERRORSOCCURRED y marca el campo *dwStatus* de todas las DBPROP incluidas en SSPARAMPROPS para ese parámetro con DBPROPSTATUS_NOTSET. Se debe recorrer la matriz DBPROP de cada DBPROPSET incluido en SSPARAMPROPS para detectar a qué parámetro hace referencia DB_E_ERRORSOCCURRED o DB_S_ERRORSOCCURRED.  
  
 Si se llama a **ISSCommandWithParameters::SetParameterProperties** para especificar las propiedades de parámetros cuya información de parámetro todavía no se ha establecido con **SetParameterInfo**, el proveedor devuelve E_UNEXPECTED con el siguiente mensaje de error:  
  
 No se puede llamar al método SetParameterProperties para los parámetros especificados sin llamar primero al método SetParameterInfo. La información de parámetro debe configurarse antes que las propiedades de parámetro.  
  
 Si la llamada a **ISSCommandWithParameters::SetParameterProperties** contiene algunos parámetros donde se ha establecido la información de parámetro y algunos parámetros donde no se ha establecido, las propiedades dwStatus en DBPROPSET del conjunto de propiedades SSPARAMPROPS devolverán DBSTATUS_NOTSET.  
  
 La estructura SSPARAMPROPS se define del siguiente modo:  
  
 `struct SSPARAMPROPS {`  
  
 `DBORDINAL iOrdinal;`  
  
 `ULONG cPropertySets;`  
  
 `DBPROPSET *rgPropertySets;`  
  
 `};`  
  
 Mejoras en el motor de base de datos a partir de [!INCLUDE[ssSQL11](../../../includes/sssql11-md.md)] permitir isscommandwithparameters:: SetParameterProperties obtener descripciones más precisas de los resultados esperados. Estos resultados más precisos pueden diferir de los valores devueltos por isscommandwithparameters:: SetParameterProperties en versiones anteriores de [!INCLUDE[ssNoVersion](../../../includes/ssnoversion-md.md)]. Para obtener más información, vea [Detección de metadatos](../../oledb/features/metadata-discovery.md).  
  
|Miembro|Descripción|  
|------------|-----------------|  
|*iOrdinal*|El ordinal del parámetro que se ha pasado.|  
|*cPropertySets*|El número de estructuras DBPROPSET de *rgPropertySets*.|  
|*rgPropertySets*|Un puntero a la memoria que devuelve una matriz de estructuras DBPROPSET.|  
  
## <a name="see-also"></a>Ver también  
 [ISSCommandWithParameters &#40;OLE DB&#41;](../../oledb/ole-db-interfaces/isscommandwithparameters-ole-db.md)  
  
  

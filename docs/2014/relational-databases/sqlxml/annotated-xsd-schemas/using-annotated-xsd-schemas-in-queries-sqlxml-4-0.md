---
title: Mediante los esquemas XSD en consultas (SQLXML 4.0) anotados | Documentos de Microsoft
ms.custom: ''
ms.date: 03/06/2017
ms.prod: sql-server-2014
ms.reviewer: ''
ms.suite: ''
ms.technology:
- database-engine
- docset-sql-devref
ms.tgt_pltfrm: ''
ms.topic: reference
helpviewer_keywords:
- queries [SQLXML]
- inline schemas [SQLXML]
- XPath queries [SQLXML], annotated XSD schemas in queries
- queries [SQLXML], annotated XSD schemas
- retrieving data
- mapping schema [SQLXML], queries
- multiple inline schemas
- annotated XSD schemas, queries
- XSD schemas [SQLXML], queries
- templates [SQLXML], annotated XSD schemas in queries
ms.assetid: 927a30a2-eae8-420d-851d-551c5f884f3c
caps.latest.revision: 29
author: JennieHubbard
ms.author: jhubbard
manager: jhubbard
ms.openlocfilehash: bfd947684010ed0d71bdce44f329ccc1f0f34917
ms.sourcegitcommit: 5dd5cad0c1bbd308471d6c885f516948ad67dfcf
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2018
ms.locfileid: "36202249"
---
# <a name="using-annotated-xsd-schemas-in-queries-sqlxml-40"></a>Usar esquemas XSD anotados en consultas (SQLXML 4.0)
  Puede especificar consultas en un esquema anotado para recuperar datos de la base de datos especificando consultas XPath en una plantilla en el esquema XSD.  
  
 El  **\<sql:xpath-consulta >** elemento le permite especificar una consulta XPath en la vista XML definida por el esquema anotado. El esquema anotado en el que se ejecutará la consulta XPath se identifica mediante el `mapping-schema` atributo de la  **\<sql:xpath-consulta >** elemento.  
  
 Las plantillas son documentos XML válidos que contienen una o varias consultas. Las consultas FOR XML y XPath devuelven un fragmento de documento. Las plantillas actúan como contenedores para los fragmentos de documento; de esta forma, las plantillas proporcionan un modo de especificar un elemento único de nivel superior.  
  
 En los ejemplos de este tema se usan plantillas para especificar una consulta XPath en un esquema anotado con objeto de recuperar datos de la base de datos.  
  
 Por ejemplo, fíjese este esquema anotado:  
  
```  
<xsd:schema xmlns:xsd="http://www.w3.org/2001/XMLSchema"   
            xmlns:sql="urn:schemas-microsoft-com:mapping-schema">  
  <xsd:element name="Person.Contact" >  
     <xsd:complexType>  
       <xsd:attribute name="ContactID" type="xsd:string" />   
       <xsd:attribute name="FirstName" type="xsd:string" />   
       <xsd:attribute name="LastName"  type="xsd:string" />   
     </xsd:complexType>  
  </xsd:element>  
</xsd:schema>  
```  
  
 Con fines meramente ilustrativos, este esquema XSD se almacena en un archivo denominado Schema2.xml. A continuación, podría incluir una consulta XPath en el esquema anotado especificado en el siguiente archivo de plantilla (Schema2T.xml):  
  
```  
<sql:xpath-query   
     xmlns:sql="urn:schemas-microsoft-com:xmlsql"  
     >  
          Person.Contact[@ContactID="1"]  
</sql:xpath-query>  
```  
  
 Después, puede crear y usar el script de prueba SQLXML 4.0 (Sqlxml4test.vbs) para ejecutar la consulta como parte de un archivo de plantilla. Para obtener más información, consulte [esquemas XDR anotados &#40;desusado en SQLXML 4.0&#41;](annotated-xdr-schemas-deprecated-in-sqlxml-4-0.md).  
  
## <a name="using-inline-mapping-schemas"></a>Usar esquemas de asignación insertados  
 Un esquema anotado puede incluirse directamente en una plantilla y, después, puede especificarse una consulta XPath en la plantilla en el esquema insertado. La plantilla también puede ser un diagrama de actualización.  
  
 Una plantilla puede incluir varios esquemas insertados. Para usar un esquema en línea que se incluye en una plantilla, especifique la **identificador** del atributo con un valor único en el  **\<xsd: schema >** elemento y, a continuación, utilice **#idvalue**para hacer referencia al esquema insertado. El **Id. de** es un comportamiento idéntico al atributo el **SQL: ID** ({urn: schemas-microsoft-com: sql} Id.) utilizados en los esquemas XDR.  
  
 Por ejemplo, la plantilla siguiente especifica dos esquemas anotados insertados:  
  
```  
<ROOT xmlns:sql='urn:schemas-microsoft-com:xml-sql'>  
<xsd:schema xmlns:xsd='http://www.w3.org/2001/XMLSchema'  
        xmlns:ms='urn:schemas-microsoft-com:mapping-schema'  
        id='InLineSchema1' sql:is-mapping-schema='1'>  
  <xsd:element name='Employees' ms:relation='HumanResources.Employee'>  
    <xsd:complexType>  
      <xsd:attribute name='LoginID'   
                     type='xsd:string'/>  
      <xsd:attribute name='Title'   
                     type='xsd:string'/>  
    </xsd:complexType>  
  </xsd:element>  
</xsd:schema>  
  
<xsd:schema xmlns:xsd='http://www.w3.org/2001/XMLSchema'  
        xmlns:ms='urn:schemas-microsoft-com:mapping-schema'  
        id='InLineSchema2' sql:is-mapping-schema='1'>  
  <xsd:element name='Contacts' ms:relation='Person.Contact'>  
    <xsd:complexType>  
  
      <xsd:attribute name='ContactID'   
                     type='xsd:string' />  
      <xsd:attribute name='FirstName'   
                     type='xsd:string' />  
      <xsd:attribute name='LastName'   
                     type='xsd:string' />  
    </xsd:complexType>  
  </xsd:element>  
</xsd:schema>  
  
<sql:xpath-query xmlns:sql='urn:schemas-microsoft-com:xml-sql'   
        mapping-schema='#InLineSchema1'>  
    /Employees[@LoginID='adventure-works\guy1']  
</sql:xpath-query>  
  
<sql:xpath-query xmlns:sql='urn:schemas-microsoft-com:xml-sql'   
        mapping-schema='#InLineSchema2'>  
    /Contacts[@ContactID='1']  
</sql:xpath-query>  
</ROOT>  
```  
  
 La plantilla también especifica dos consultas XPath. Cada uno de los  **\<consulta xpath >** elementos identifica de forma única el esquema de asignación especificando el `mapping-schema` atributo.  
  
 Cuando se especifica un esquema insertado en la plantilla, el `sql:is-mapping-schema` anotación debe especificarse en el  **\<xsd: schema >** elemento. `sql:is-mapping-schema` toma un valor booleano (0=false, 1=true). Un esquema insertado con **sql: is-mapping-schema = "1"** se trata como un esquema anotado insertado y no se devuelve en el documento XML.  
  
 La anotación `sql:is-mapping-schema` pertenece al espacio de nombres de plantilla `urn:schemas-microsoft-com:xml-sql`.  
  
 Para probar este ejemplo, guarde la plantilla (InlineSchemaTemplate.xml) en un directorio local y, a continuación, cree y use el script de prueba SQLXML 4.0 (Sqlxml4test.vbs) para ejecutar la plantilla. Para obtener más información, consulte [utilizar ADO para ejecutar consultas de SQLXML 4.0](../using-ado-to-execute-sqlxml-4-0-queries.md).  
  
 Además de especificar el `mapping-schema` del atributo en el  **\<sql:xpath-consulta >** elemento en una plantilla (cuando hay una consulta XPath) o en  **\<updg:sync >** elemento de un diagrama de actualización, puede hacer lo siguiente:  
  
-   Especifique el `mapping-schema` del atributo en el  **\<raíz >** elemento (declaración global) de la plantilla. Este esquema de asignación se convierte en el esquema predeterminado que utilizarán todos los nodos XPath y de diagrama de actualización que no tengan ninguna anotación `mapping-schema` explícita.  
  
-   Especificar el atributo `mapping schema` mediante el objeto ADO `Command`.  
  
 El `mapping-schema` atributo que se especifica en el  **\<consulta xpath >** o  **\<updg:sync >** elemento tiene la máxima prioridad; ADO `Command` objeto tiene la prioridad más baja.  
  
 Tenga en cuenta que si especifica una consulta XPath en una plantilla y no especifica un esquema de asignación en el que se ejecuta la consulta XPath, la consulta XPath se trata como un **dbobject** consulta de tipo. Por ejemplo, fíjese en esta plantilla:  
  
```  
<sql:xpath-query   
     xmlns:sql="urn:schemas-microsoft-com:xmlsql">  
          Production.ProductPhoto[@ProductPhotoID='100']/@LargePhoto  
</sql:xpath-query>  
```  
  
 La plantilla especifica una consulta XPath, pero no especifica ningún esquema de asignación. Por lo tanto, esta consulta se considera un **dbobject** donde Production.ProductPhoto es el nombre de tabla de consulta de tipo y @ProductPhotoID= '100' es un predicado que busca una fotografía del producto con el valor de identificador de 100. @LargePhoto es la columna desde la que se va a recuperar el valor.  
  
  
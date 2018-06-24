---
title: Sqlerrorlogevent, clase | Documentos de Microsoft
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
- SqlErrorLogEvent class
- SqlErrorLogFile class
ms.assetid: bde6c467-38d0-4766-a7af-d6c9d6302b07
caps.latest.revision: 12
author: JennieHubbard
ms.author: jhubbard
manager: jhubbard
ms.openlocfilehash: 95588b82a36bb5d7d5d520a5f54ca968a9198112
ms.sourcegitcommit: 5dd5cad0c1bbd308471d6c885f516948ad67dfcf
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2018
ms.locfileid: "36108517"
---
# <a name="sqlerrorlogevent-class"></a>SqlErrorLogEvent, clase
  Proporciona las propiedades para ver los eventos en un archivo de registro [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] especificado.  
  
## <a name="syntax"></a>Sintaxis  
  
```  
  
class SQLErrorLogEvent   
{  
   stringFileName;  
   stringInstanceName;  
   datetimeLogDate;  
   stringMessage;  
   stringProcessInfo;  
};  
```  
  
## <a name="properties"></a>Propiedades  
 Sqlerrorlogevent, clase define las siguientes propiedades.  
  
|||  
|-|-|  
|FileName|Tipo de datos: `string`<br /><br /> Tipo de acceso: solo lectura<br /><br /> <br /><br /> El nombre del archivo de registro de errores.|  
|InstanceName|Tipo de datos: `string`<br /><br /> Tipo de acceso: solo lectura<br /><br /> Calificadores: clave<br /><br /> El nombre de la instancia de [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] donde reside el archivo de registro.|  
|LogDate|Tipo de datos: `datetime`<br /><br /> Tipo de acceso: solo lectura<br /><br /> Calificadores: clave<br /><br /> <br /><br /> Fecha y hora en que el evento se grabó en el archivo de registro.|  
|de mensaje|Tipo de datos: `string`<br /><br /> Tipo de acceso: solo lectura<br /><br /> <br /><br /> Mensaje del evento.|  
|ProcessInfo|Tipo de datos: `string`<br /><br /> Tipo de acceso: solo lectura<br /><br /> <br /><br /> Información sobre el identificador del proceso del servidor de origen (SPID) para el evento.|  
  
## <a name="remarks"></a>Notas  
  
|||  
|-|-|  
|MOF|Sqlmgmproviderxpsp2up.mof|  
|DLL|Sqlmgmprovider.dll|  
|Espacio de nombres|\raíz\Microsoft\SqlServer\ComputerManagement10|  
  
## <a name="example"></a>Ejemplo  
 En el siguiente ejemplo se muestra cómo recuperar los valores para todos los eventos anotados en un archivo de registro especificado. Para ejecutar el ejemplo, reemplace \< *Instance_Name*> con el nombre de la instancia de [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)], por ejemplo, 'Instancia1' y reemplace 'File_Name' por el nombre del archivo de registro de errores, como 'ERRORLOG.1'.  
  
```  
on error resume next  
strComputer = "."  
Set objWMIService = GetObject("winmgmts:" _  
    & "{impersonationLevel=impersonate}!\\" _  
    & strComputer & "\root\MICROSOFT\SqlServer\ComputerManagement10")  
set logEvents = objWmiService.ExecQuery("SELECT * FROM SqlErrorLogEvent WHERE InstanceName = '<Instance_Name>' AND FileName = 'File_Name'")  
  
For Each logEvent in logEvents  
WScript.Echo "Instance Name: " & logEvent.InstanceName & vbNewLine _  
    & "Log Date: " & logEvent.LogDate & vbNewLine _  
    & "Log File Name: " & logEvent.FileName & vbNewLine _  
    & "Process Info: " & logEvent.ProcessInfo & vbNewLine _  
    & "Message: " & logEvent.Message & vbNewLine _  
  
Next  
```  
  
## <a name="comments"></a>Comentarios  
 Cuando *nombreDeInstancia* o *FileName* no se proporcionan en la instrucción WQL, la consulta devolverá información para la instancia predeterminada y la actual [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] archivo de registro. Por ejemplo, la siguiente instrucción WQL devolverá todos los eventos de registro desde el archivo de registro actual (ERRORLOG) en la instancia predeterminada (MSSQLSERVER).  
  
```  
"SELECT * FROM SqlErrorLogEvent"  
```  
  
## <a name="security"></a>Seguridad  
 Para conectarse a un [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] archivo de registro a través de WMI, debe tener los permisos siguientes en los equipos locales y remotos:  
  
-   Acceso de lectura a la **Root\Microsoft\SqlServer\ComputerManagement10** espacio de nombres WMI. De forma predeterminada, todos tienen acceso de lectura mediante el permiso Habilitar cuenta.  
  
-   Permiso de lectura a la carpeta que contiene los registros de errores. De forma predeterminada el error registros se encuentran en la ruta de acceso siguiente (donde \< *unidad >* representa la unidad donde se instaló [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] y \< *nombreDeInstancia*> es el nombre de la instancia de [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)]):  
  
     **\<Unidad >: \Program SQL Server\MSSQL12** **.\< NombreDeInstancia > \MSSQL\Log**  
  
 Si se conecta a través de un firewall, asegúrese de que se establece una excepción en el firewall para WMI en los equipos de destino remotos. Para obtener más información, consulte [conectar con WMI de forma remota comenzando con Windows Vista](http://go.microsoft.com/fwlink/?LinkId=178848).  
  
## <a name="see-also"></a>Vea también  
 [Clase SqlErrorLogFile](sqlerrorlogfile-class.md)   
 [Ver archivos del registro sin conexión](../logs/view-offline-log-files.md)  
  
  
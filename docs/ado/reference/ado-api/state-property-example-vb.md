---
title: Estado de ejemplo de la propiedad (VB) | Documentos de Microsoft
ms.prod: sql
ms.prod_service: connectivity
ms.technology: connectivity
ms.custom: ''
ms.date: 01/19/2017
ms.reviewer: ''
ms.suite: sql
ms.tgt_pltfrm: ''
ms.topic: conceptual
dev_langs:
- VB
helpviewer_keywords:
- State property [ADO], Visual Basic example
ms.assetid: 9da6db50-d9bb-47e1-ae8b-be3c9b88cf9a
caps.latest.revision: 11
author: MightyPen
ms.author: genemi
manager: craigg
ms.openlocfilehash: 1f3f7126a9da116dd34ef2c0e99559eeb7dc122e
ms.sourcegitcommit: 62826c291db93c9017ae219f75c3cfeb8140bf06
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "35281924"
---
# <a name="state-property-example-vb"></a>Ejemplo de la propiedad State (VB)
Este ejemplo se utiliza la [estado](../../../ado/reference/ado-api/state-property-ado.md) propiedad para mostrar un mensaje al abrir conexiones asincrónicas y se ejecutan comandos asincrónicos.  
  
```  
'BeginStateVB  
  
    'To integrate this code  
    'replace the data source and initial catalog values  
    'in the connection string  
  
Public Sub Main()  
    On Error GoTo ErrorHandler  
  
    Dim Cnxn1 As ADODB.Connection  
    Dim Cnxn2 As ADODB.Connection  
    Dim cmdChange As ADODB.Command  
    Dim cmdRestore As ADODB.Command  
    Dim strCnxn As String  
    Dim strSQL As String  
  
    ' Open two asynchronous connections, displaying  
    ' a message while connecting  
    Set Cnxn1 = New ADODB.Connection  
    Set Cnxn2 = New ADODB.Connection  
    strCnxn = "Provider='sqloledb';Data Source='MySqlServer';" & _  
        "Initial Catalog='Pubs';Integrated Security='SSPI';"  
  
    Cnxn1.Open strCnxn, , , adAsyncConnect  
    Do Until Cnxn1.State <> adStateConnecting  
       Debug.Print "Opening first connection...."  
    Loop  
  
    Cnxn2.Open strCnxn, , , adAsyncConnect  
    Do Until Cnxn2.State <> adStateConnecting  
       Debug.Print "Opening second connection...."  
    Loop  
  
    ' Create two command objects  
    Set cmdChange = New ADODB.Command  
    cmdChange.ActiveConnection = Cnxn1  
    strSQL = "UPDATE Titles SET type = 'self_help' WHERE type = 'psychology'"  
    cmdChange.CommandText = strSQL  
  
    Set cmdRestore = New ADODB.Command  
    cmdRestore.ActiveConnection = Cnxn2  
    strSQL = "UPDATE Titles SET type = 'psychology' WHERE type = 'self_help'"  
    cmdRestore.CommandText = strSQL  
  
    ' Executing the commands, displaying a message  
    ' while they are executing  
    cmdChange.Execute , , adAsyncExecute  
    Do Until cmdChange.State <> adStateExecuting  
       Debug.Print "Change command executing...."  
    Loop  
  
    cmdRestore.Execute , , adAsyncExecute  
    Do Until cmdRestore.State <> adStateExecuting  
       Debug.Print "Restore command executing...."  
    Loop  
  
    ' clean up  
    Cnxn1.Close  
    Cnxn2.Close  
    Set Cnxn1 = Nothing  
    Set Cnxn2 = Nothing  
    Exit Sub  
  
ErrorHandler:  
    ' clean up  
    If Not Cnxn1 Is Nothing Then  
        If Cnxn1.State = adStateOpen Then Cnxn1.Close  
    End If  
    Set Cnxn1 = Nothing  
  
    If Not Cnxn2 Is Nothing Then  
        If Cnxn2.State = adStateOpen Then Cnxn2.Close  
    End If  
    Set Cnxn2 = Nothing  
  
    If Err <> 0 Then  
        MsgBox Err.Source & "-->" & Err.Description, , "Error"  
    End If  
End Sub  
'EndStateVB  
```  
  
## <a name="see-also"></a>Vea también  
 [Objeto de conjunto de registros (ADO)](../../../ado/reference/ado-api/recordset-object-ado.md)   
 [Propiedad State (ADO)](../../../ado/reference/ado-api/state-property-ado.md)

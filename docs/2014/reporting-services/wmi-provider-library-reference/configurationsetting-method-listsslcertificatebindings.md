---
title: Método ListSSLCertificateBindings (MSReportServer_ConfigurationSetting de WMI) | Microsoft Docs
ms.custom: ''
ms.date: 06/13/2017
ms.prod: sql-server-2014
ms.reviewer: ''
ms.suite: ''
ms.technology:
- reporting-services-native
ms.tgt_pltfrm: ''
ms.topic: conceptual
helpviewer_keywords:
- ListSSLCertificateBindings method
ms.assetid: d12d280c-9b6f-47a8-bcd9-34cde31c8886
caps.latest.revision: 12
author: markingmyname
ms.author: maghan
manager: craigg
ms.openlocfilehash: 66de4c245aeb16af2667381b8ec6a42133a60099
ms.sourcegitcommit: c18fadce27f330e1d4f36549414e5c84ba2f46c2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/02/2018
ms.locfileid: "37166126"
---
# <a name="listsslcertificatebindings-method-wmi-msreportserverconfigurationsetting"></a>Método ListSSLCertificateBindings (WMI MSReportServer_ConfigurationSetting)
  Devuelve una lista de los certificados SSL instalados en el equipo.  
  
## <a name="syntax"></a>Sintaxis  
  
```vb  
Public Sub ListSSLCertificateBindings(ByVal LCID As Int32, ByRef Application() As String, _  
    ByRef CertificateHash() As String, ByRef IPAddresses() As String, ByRef Port() As Int32, _  
    ByRef Errors() As String, ByRef Length As Int32, _  
    ByRef HRESULT As Int32)  
```  
  
```csharp  
public void ListSSLCertificateBindings(Int32 Lcid, out string[] Application,   
    out string[] CertificateHash,out string[] IPAddress,   
    out Int32[] Port, out string Errors,   
    out Int32 length, out Int32 HRESULT);  
```  
  
## <a name="parameters"></a>Parámetros  
 *LCID*  
 Configuración regional que se utilizará para los mensajes de error que se devuelven.  
  
 *Application[]*  
 [out] Aplicaciones que tienen enlaces de certificado.  
  
 *CertificateHash[]*  
 [out] Valores hash para los certificados.  
  
 *IPAddress[]*  
 [out] Dirección IP para las aplicaciones.  
  
 *Port[]*  
 [out] Número de puerto almacenado en el enlace en rsreportserver.config.  
  
 *Errors[]*  
 [out] Descripciones de los errores que se produjeron.  
  
 *Longitud*  
 [out] Longitud de la matriz devuelta por el método.  
  
 *HRESULT*  
 [out] Valor que indica si la llamada se realizó correctamente o no.  
  
## <a name="return-value"></a>Valor devuelto  
 Devuelve *HRESULT* que indica si la llamada al método se realizó correctamente o no. Un valor de 0 indica que la llamada al método se realizó correctamente. Un valor distinto de cero indica que se ha producido un error.  
  
## <a name="remarks"></a>Notas  
  
## <a name="requirements"></a>Requisitos  
 **Espacio de nombres:** [!INCLUDE[ssRSWMInmspcA](../../includes/ssrswminmspca-md.md)]  
  
## <a name="see-also"></a>Vea también  
 [Miembros MSReportServer_ConfigurationSetting](msreportserver-configurationsetting-members.md)  
  
  

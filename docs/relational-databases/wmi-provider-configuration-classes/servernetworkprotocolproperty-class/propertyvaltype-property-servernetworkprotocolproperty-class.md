---
title: Propiedad PropertyValType (clase ServerNetworkProtocolProperty) | Documentos de Microsoft
ms.custom: ''
ms.date: 03/14/2017
ms.prod: sql
ms.prod_service: database-engine
ms.component: wmi
ms.reviewer: ''
ms.suite: sql
ms.technology:
- database-engine
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- PropertyValType Property (ServerNetworkProtocolProperty Class)
apilocation:
- sqlmgmproviderxpsp2up.mof
apitype: MOFDef
helpviewer_keywords:
- PropertyValType property
ms.assetid: fbd42e8e-0642-4a19-b3c8-6ce88345145f
caps.latest.revision: 30
author: CarlRabeler
ms.author: carlrab
manager: craigg
ms.openlocfilehash: 382f8eefd2bdc19021c561edc07aba29eaade38b
ms.sourcegitcommit: 1740f3090b168c0e809611a7aa6fd514075616bf
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/03/2018
---
# <a name="propertyvaltype-property-servernetworkprotocolproperty-class"></a>Propiedad PropertyValType (clase ServerNetworkProtocolProperty)
[!INCLUDE[tsql-appliesto-ss2008-xxxx-xxxx-xxx-md](../../../includes/tsql-appliesto-ss2008-xxxx-xxxx-xxx-md.md)]
  Obtiene el tipo de datos del valor almacenado en la propiedad a la que se hace referencia.  
  
## <a name="syntax"></a>Sintaxis  
  
```  
  
object.PropertyValType [= value]  
```  
  
## <a name="parts"></a>Partes  
 *objeto*  
 A [clase ServerNetworkProtocolProperty](../../../relational-databases/wmi-provider-configuration-classes/servernetworkprotocolproperty-class/servernetworkprotocolproperty-class.md) objeto que representa un atributo del protocolo de red en la instancia de [!INCLUDE[msCoName](../../../includes/msconame-md.md)] [!INCLUDE[ssNoVersion](../../../includes/ssnoversion-md.md)].  
  
## <a name="property-valuereturn-value"></a>Valor de propiedad y valor devuelto  
 A **uint32** valor que especifica el tipo de datos del valor de propiedad. Devuelve 0 para un valor de cadena y 1 para un tipo numérico.  
  
## <a name="remarks"></a>Comentarios  
  
## <a name="see-also"></a>Vea también  
 [Configurar protocolos de red de servidor y bibliotecas de red](http://msdn.microsoft.com/library/ms177485\(v=sql.100\).aspx)  
  
  

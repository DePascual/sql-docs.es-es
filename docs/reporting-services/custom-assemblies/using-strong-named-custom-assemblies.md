---
title: Usar ensamblados personalizados con nombre seguro | Microsoft Docs
ms.custom: ''
ms.date: 03/14/2017
ms.prod: reporting-services
ms.prod_service: reporting-services-native
ms.component: custom-assemblies
ms.reviewer: ''
ms.suite: pro-bi
ms.technology: ''
ms.tgt_pltfrm: ''
ms.topic: reference
applies_to:
- SQL Server 2016 Preview
helpviewer_keywords:
- AllowPartiallyTrustedCallersAttribute attribute
- strong-named custom assemblies [Reporting Services]
- strong names [Reporting Services]
- assemblies [Reporting Services], strong names
- custom assemblies [Reporting Services], strong-named
ms.assetid: ca9f19d7-6e86-46f2-b9ad-9bf807eaa52e
caps.latest.revision: 35
author: markingmyname
ms.author: maghan
manager: kfile
ms.openlocfilehash: 965c75a16e02d6561da2cf326a74f585e5e8be3a
ms.sourcegitcommit: 1740f3090b168c0e809611a7aa6fd514075616bf
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/03/2018
---
# <a name="using-strong-named-custom-assemblies"></a>Usar ensamblados personalizados con nombre seguro
  Un nombre seguro identifica un ensamblado e incluye un nombre para el mismo, un número de versión de cuatro partes, información de la referencia cultural (si se proporciona), una clave pública y una firma digital almacenadas en el manifiesto del ensamblado. Un nombre seguro identifica de forma única un ensamblado para Common Language Runtime (CLR) y se asegura de la integridad binaria.  
  
## <a name="using-allowpartiallytrustedcallersattribute"></a>Usar AllowPartiallyTrustedCallersAttribute  
 Para usar ensamblados con nombre seguro con los informes, debe permitir que el código de confianza parcial llame al ensamblado con nombre seguro con el atributo **AllowPartiallyTrustedCallers** del ensamblado. Puede usar **AllowPartiallyTrustedCallersAttribute** para permitir que el Diseñador de informes o el servidor de informes llamen a los ensamblados con nombre seguro en las expresiones de informe. Para permitir que el código con confianza parcial llame a los ensamblados con nombre seguro, agregue el siguiente atributo de nivel de ensamblado al archivo de atributos de ensamblado.  
  
```vb  
<assembly:AllowPartiallyTrustedCallers>  
```  
  
```csharp  
[assembly:AllowPartiallyTrustedCallers]  
```  
  
 **AllowPartiallyTrustedCallersAttribute** solo es eficaz cuando lo aplica un ensamblado con nombre seguro en el nivel de ensamblado. Para más información sobre cómo aplicar atributos en el nivel de ensamblado, vea "Aplicar atributos" en la documentación del SDK de [!INCLUDE[msCoName](../../includes/msconame-md.md)] [!INCLUDE[dnprdnshort](../../includes/dnprdnshort-md.md)].  
  
> [!CAUTION]  
>  Cuando **AllowPartiallyTrustedCallersAttribute** está presente, se evitan las comprobaciones de seguridad **FullTrustLinkDemand** predeterminadas, con lo que el ensamblado se puede llamar desde cualquier otro ensamblado con confianza parcial. Todas las comprobaciones de seguridad, incluidos los atributos de seguridad declarativos de nivel de clase o de método, se deben indicar explícitamente.  
  
## <a name="see-also"></a>Ver también  
 [Usar ensamblados personalizados con informes](../../reporting-services/custom-assemblies/using-custom-assemblies-with-reports.md)  
  
  

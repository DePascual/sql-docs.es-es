---
title: Type (propiedad) (ADO MD) | Documentos de Microsoft
ms.prod: sql
ms.prod_service: connectivity
ms.component: ado
ms.technology: connectivity
ms.custom: ''
ms.date: 01/19/2017
ms.reviewer: ''
ms.suite: sql
ms.tgt_pltfrm: ''
ms.topic: conceptual
apitype: COM
f1_keywords:
- Member::Type
- Type
helpviewer_keywords:
- Type property [ADO MD]
ms.assetid: 34698910-64b9-41d8-8531-9de12f2b1e32
caps.latest.revision: 12
author: MightyPen
ms.author: genemi
manager: craigg
ms.openlocfilehash: e6d7a6d956b1ba9878b7e3fdfe8db8150a079169
ms.sourcegitcommit: 1740f3090b168c0e809611a7aa6fd514075616bf
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/03/2018
---
# <a name="type-property-ado-md"></a>Tipo (propiedad, ADO MD)
Indica el tipo del elemento actual [miembro](../../../ado/reference/ado-md-api/member-object-ado-md.md).  
  
## <a name="return-values"></a>Valores devueltos  
 Devuelve un [MemberTypeEnum](../../../ado/reference/ado-md-api/membertypeenum.md) valor y es de solo lectura.  
  
## <a name="remarks"></a>Comentarios  
 Esta propiedad solo se admite en [miembro](../../../ado/reference/ado-md-api/member-object-ado-md.md) objetos que pertenecen a un [nivel](../../../ado/reference/ado-md-api/level-object-ado-md.md) objeto. Se produce un error cuando se hace referencia a esta propiedad desde **miembro** objetos que pertenecen a un [posición](../../../ado/reference/ado-md-api/position-object-ado-md.md) objeto.  
  
## <a name="applies-to"></a>Se aplica a  
 [Objeto de miembro (ADO MD)](../../../ado/reference/ado-md-api/member-object-ado-md.md)

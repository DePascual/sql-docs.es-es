---
title: '&gt; (Mayor que) (MDX) | Documentos de Microsoft'
ms.custom: ''
ms.date: 03/02/2016
ms.prod: analysis-services
ms.prod_service: analysis-services
ms.component: ''
ms.reviewer: ''
ms.suite: pro-bi
ms.technology: ''
ms.tgt_pltfrm: ''
ms.topic: language-reference
f1_keywords:
- '>'
dev_langs:
- kbMDX
helpviewer_keywords:
- greater than operator (>)
- '> (greater than operator)'
ms.assetid: 36ba6462-5517-43be-8e7d-a38b7343c5d3
caps.latest.revision: 33
author: Minewiskan
ms.author: owend
manager: erikre
ms.openlocfilehash: 6d82e6fb8d2c10c88ba8e8a7945f93b3278f9656
ms.sourcegitcommit: 1740f3090b168c0e809611a7aa6fd514075616bf
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/03/2018
---
# <a name="gt-greater-than-mdx"></a>&gt; (Mayor que) (MDX)
[!INCLUDE[ssas-appliesto-sqlas](../includes/ssas-appliesto-sqlas.md)]

  Realiza una operación de comparación que determina si el valor de una expresión multidimensional (MDX) es mayor que el valor de otra expresión MDX.  
  
## <a name="syntax"></a>Sintaxis  
  
```  
  
MDX_Expression > MDX_Expression  
```  
  
#### <a name="parameters"></a>Parámetros  
 *MDX_Expression*  
 Una expresión MDX válida.  
  
## <a name="return-value"></a>Valor devuelto  
 Un valor booleano basado en las condiciones siguientes:  
  
-   **True** si ambos parámetros son distintos de null y el primer parámetro tiene un valor que es mayor que el valor del segundo parámetro.  
  
-   **false** si ambos parámetros son distintos de null y el primer parámetro tiene un valor que es igual o menor que el valor del segundo parámetro.  
  
-   valor NULL si uno de los parámetros (o ambos) se evalúa en un valor NULL.  
  
## <a name="examples"></a>Ejemplos  
 En la siguiente consulta de ejemplo se muestra el uso de este operador.  
  
```  
-- This query returns the gross profit margin (GPM)  
-- for Australia where the GPM is more than 50%.  
With Member [Measures].[HighGPM] as  
  IIF(  
      [Measures].[Gross Profit Margin] > .5,  
      [Measures].[Gross Profit Margin],  
      null)  
SELECT   
NON EMPTY [Sales Territory].[Sales Territory Country].[Australia] ON 0,  
    NON EMPTY [Product].[Category].Members ON 1  
FROM  
    [Adventure Works]  
WHERE  
    ([Measures].[HighGPM])  
  
```  
  
## <a name="see-also"></a>Vea también  
 [Referencia de operadores MDX &#40;MDX&#41;](../mdx/mdx-operator-reference-mdx.md)  
  
  

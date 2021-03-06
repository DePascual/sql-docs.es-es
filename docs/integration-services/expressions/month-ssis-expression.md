---
title: MONTH (expresión de SSIS) | Microsoft Docs
ms.custom: ''
ms.date: 03/01/2017
ms.prod: sql
ms.prod_service: integration-services
ms.component: expressions
ms.reviewer: ''
ms.suite: sql
ms.technology:
- integration-services
ms.tgt_pltfrm: ''
ms.topic: conceptual
helpviewer_keywords:
- dates [Integration Services], MONTH
- MONTH function
ms.assetid: b5a47a11-c2ef-49bd-bd70-235632ff7bf6
caps.latest.revision: 38
author: douglaslMS
ms.author: douglasl
manager: craigg
ms.openlocfilehash: c874334334e79b0be48cd474e1cb4fc8faf065b3
ms.sourcegitcommit: 1740f3090b168c0e809611a7aa6fd514075616bf
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/03/2018
---
# <a name="month-ssis-expression"></a>MONTH (expresión de SSIS)
  Devuelve un entero que representa la parte del mes de una fecha.  
  
## <a name="syntax"></a>Sintaxis  
  
```  
  
MONTH(date)  
```  
  
## <a name="arguments"></a>Argumentos  
 *date*  
 Fecha con cualquier formato de fecha.  
  
## <a name="result-types"></a>Tipos de resultado  
 DT_I4  
  
## <a name="remarks"></a>Notas  
 MONTH devuelve un resultado NULL si el valor del argumento es NULL.  
  
 Un literal de tipo fecha debe convertirse explícitamente en uno de los tipos de datos de fecha. Para más información, consulte [Integration Services Data Types](../../integration-services/data-flow/integration-services-data-types.md).  
  
> [!NOTE]  
>  La expresión no puede validarse cuando un literal de fecha se convierte explícitamente en uno de estos tipos de datos de fecha: DT_DBTIMESTAMPOFFSET y DT_DBTIMESTAMP2.  
  
 Utilizar la función MONTH es más sencillo pero equivalente a utilizar la función DATEPART("Month", date).  
  
## <a name="expression-examples"></a>Ejemplos de expresiones  
 Este ejemplo devuelve el número del mes de un literal de fecha. Si la fecha tiene el formato "mm/dd/aaaa", este ejemplo devuelve 11.  
  
```  
MONTH((DT_DBTIMESTAMP)"11/23/2002")  
```  
  
 Este ejemplo devuelve el entero que representa el mes en la columna **ModifiedDate** .  
  
```  
MONTH(ModifiedDate)  
```  
  
 Este ejemplo devuelve el entero que representa el mes de la fecha actual.  
  
```  
MONTH(GETDATE())  
```  
  
## <a name="see-also"></a>Ver también  
 [DATEADD &#40;expresión de SSIS&#41;](../../integration-services/expressions/dateadd-ssis-expression.md)   
 [DATEDIFF &#40;expresión de SSIS&#41;](../../integration-services/expressions/datediff-ssis-expression.md)   
 [DATEPART &#40;expresión de SSIS&#41;](../../integration-services/expressions/datepart-ssis-expression.md)   
 [DAY &#40;expresión de SSIS&#41;](../../integration-services/expressions/day-ssis-expression.md)   
 [YEAR &#40;expresión de SSIS&#41;](../../integration-services/expressions/year-ssis-expression.md)   
 [Funciones &#40;expresión de SSIS&#41;](../../integration-services/expressions/functions-ssis-expression.md)  
  
  

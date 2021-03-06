---
title: SELECT FROM &lt;modelo&gt;. SAMPLE_CASES (DMX) | Documentos de Microsoft
ms.custom: ''
ms.date: 03/02/2016
ms.prod: analysis-services
ms.prod_service: analysis-services
ms.component: data-mining
ms.reviewer: ''
ms.suite: pro-bi
ms.technology: ''
ms.tgt_pltfrm: ''
ms.topic: language-reference
f1_keywords:
- SAMPLE_CASES
- SELECT
- FROM
dev_langs:
- DMX
helpviewer_keywords:
- SELECT FROM <model>.SAMPLE_CASES statement
- mining models [Analysis Services], sample cases
- sample cases [DMX]
- training mining models
ms.assetid: e7a34b9b-3562-4503-bfa7-dd9b12db480a
caps.latest.revision: 39
author: Minewiskan
ms.author: owend
manager: erikre
ms.openlocfilehash: 013b98a8f70d99810ba3032e3c0f3ac65db27acf
ms.sourcegitcommit: 1740f3090b168c0e809611a7aa6fd514075616bf
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/03/2018
---
# <a name="select-from-ltmodelgtsamplecases-dmx"></a>SELECT FROM &lt;modelo&gt;. SAMPLE_CASES (DMX)
[!INCLUDE[ssas-appliesto-sqlas](../includes/ssas-appliesto-sqlas.md)]

  Devuelve ejemplos de casos que son representativos de los casos que se emplean para entrenar el modelo de minería de datos.  
  
 Para poder utilizar esta instrucción, debe habilitar la obtención de detalles al crear el modelo de minería de datos. Para obtener más información acerca de cómo habilitar la obtención de detalles, vea [CREATE MINING MODEL &#40;DMX&#41;](../dmx/create-mining-model-dmx.md), [SELECT INTO &#40;DMX&#41;](../dmx/select-into-dmx.md), y [ALTER MINING STRUCTURE &#40;DMX&#41;](../dmx/alter-mining-structure-dmx.md).  
  
## <a name="syntax"></a>Sintaxis  
  
```  
  
SELECT [FLATTENED] [TOP <n>] <expression list> FROM <model>.SAMPLE_CASES  
[WHERE <condition list>] ORDER BY <expression> [DESC|ASC]]  
```  
  
## <a name="arguments"></a>Argumentos  
 *n*  
 Opcional. Entero que especifica el número de filas que se devuelven.  
  
 *lista de expresiones*  
 Lista delimitada por comas de identificadores de columna relacionados.  
  
 *model*  
 Identificador de modelo.  
  
 *lista de condiciones*  
 Opcional. Condiciones para restringir los valores que devuelve la lista de columnas.  
  
 *expression*  
 Opcional. Expresión que devuelve un valor escalar.  
  
## <a name="remarks"></a>Comentarios  
 Pueden generarse casos de ejemplo que podrían no existir en los datos de entrenamiento. El caso devuelto es representativo del nodo de contenido especificado.  
  
 Aunque la [!INCLUDE[msCoName](../includes/msconame-md.md)] es el único algoritmo de clústeres de secuencia [!INCLUDE[msCoName](../includes/msconame-md.md)] algoritmo que admite el uso de SELECT FROM \<modelo >. SAMPLE_CASES, algoritmos de terceros también podrían admitirlo.  
  
## <a name="examples"></a>Ejemplos  
 En el siguiente ejemplo se devuelven casos de ejemplo que sirven para entrenar el modelo de minería de datos Target Mail. Mediante el [IsInNode &#40;DMX&#41; ](../dmx/isinnode-dmx.md) funcionando en el **donde** cláusula devuelve exclusivamente casos asociados con el nodo '000000003'. La cadena de nodo se encuentra en la columna NODE_UNIQUE_NAME del conjunto de filas de esquema.  
  
```  
Select * from [Sequence Clustering].SAMPLE_Cases  
WHERE IsInNode('000000003')  
```  
  
## <a name="see-also"></a>Vea también  
 [SELECCIONE &AMP;#40;DMX&AMP;#41;](../dmx/select-dmx.md)   
 [Extensiones de minería de datos &#40;DMX&#41; las instrucciones de definición de datos](../dmx/dmx-statements-data-definition.md)   
 [Extensiones de minería de datos &#40;DMX&#41; instrucciones de manipulación de datos](../dmx/dmx-statements-data-manipulation.md)   
 [Extensiones de minería de datos & #40; DMX & #41; Referencia de instrucciones](../dmx/data-mining-extensions-dmx-statements.md)  
  
  

---
title: Parámetros de comandos con los comandos de proceso | Documentos de Microsoft
ms.prod: sql
ms.prod_service: drivers
ms.service: ''
ms.component: ado
ms.technology:
- drivers
ms.custom: ''
ms.date: 01/19/2017
ms.reviewer: ''
ms.suite: sql
ms.tgt_pltfrm: ''
ms.topic: conceptual
helpviewer_keywords:
- data shaping [ADO], parameterized commands
- parameterized commands [ADO]
- APPEND clause [ADO]
- COMPUTE command [ADO]
ms.assetid: 732f624f-8900-4608-9815-194302d22e8b
caps.latest.revision: 10
author: MightyPen
ms.author: genemi
manager: craigg
ms.openlocfilehash: daf3db7f5afba2f70b58023e714b1d79e1de9b22
ms.sourcegitcommit: 2ddc0bfb3ce2f2b160e3638f1c2c237a898263f4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/03/2018
---
# <a name="parameterized-commands-with-intervening-compute-commands"></a>Comandos de proceso de comandos con parámetros con intermedias
Una típica comando shape APPEND parametrizado tiene una cláusula que crea un elemento primario **Recordset** con un comando de consulta y otra cláusula que crea un elemento secundario **Recordset** con un comando de consulta con parámetros: es decir, un comando que contiene un marcador de posición de parámetro (un signo de interrogación "?"). Resultante en forma de **Recordset** tiene dos niveles, en la que el elemento principal ocupa el nivel superior y el elemento secundario ocupa el nivel inferior.  
  
 La cláusula que crea el elemento secundario **Recordset** puede ahora ser un número arbitrario de forma anidada comandos COMPUTE, donde el comando más profundamente anidado contiene la consulta con parámetros. Resultante en forma de **Recordset** tiene varios niveles, en la que el elemento principal ocupa el nivel superior, el elemento secundario ocupa el nivel inferior y un número arbitrario de **Recordset**s generados por el comandos Shape COMPUTE ocupan los niveles intermedios.  
  
 El uso típico de esta característica es invocar la función de agregado y la capacidad de agrupación de shapeCOMPUTE comandos para crear intermedias **Recordset** objetos analíticos información sobre el elemento secundario **conjunto de registros** . Además, dado que se trata de un comando shape parametrizado, cada vez que una columna de capítulo del elemento primario se tiene acceso, un nuevo elemento secundario **Recordset** se pueden recuperar. Dado que los niveles intermedios se derivan del elemento secundario, también se volverá a calcular.  
  
## <a name="see-also"></a>Vea también  
 [Ejemplo de la forma de datos](../../../ado/guide/data/data-shaping-example.md)

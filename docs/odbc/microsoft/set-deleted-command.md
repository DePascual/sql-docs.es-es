---
title: Comando DELETED | Documentos de Microsoft
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.suite: sql
ms.technology: connectivity
ms.tgt_pltfrm: ''
ms.topic: conceptual
helpviewer_keywords:
- SET DELETED command [ODBC]
ms.assetid: 6b5e0086-156d-471d-8e7f-6c5fa9686cd5
caps.latest.revision: 5
author: MightyPen
ms.author: genemi
manager: craigg
ms.openlocfilehash: 74cd0c5752728320acf09768d876bae37b6e193b
ms.sourcegitcommit: 1740f3090b168c0e809611a7aa6fd514075616bf
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/03/2018
---
# <a name="set-deleted-command"></a>Comando de eliminaciones de Set.
Especifica si se procesan los registros marcados para su eliminación y si están disponibles para su uso en otros comandos.  
  
## <a name="syntax"></a>Sintaxis  
  
```  
  
SET DELETED ON | OFF  
```  
  
## <a name="arguments"></a>Argumentos  
 ON  
 (Valor predeterminado para el controlador; el valor predeterminado de Visual FoxPro es OFF). Especifica que los comandos que funcionan en los registros (incluidos los registros en las tablas relacionadas) con un ámbito de pasar por alto los registros marcados para su eliminación.  
  
 OFF  
 Especifica que los registros marcados para su eliminación puede tener acceso a comandos que operan en los registros (incluidos los registros en las tablas relacionadas) con un ámbito.  
  
## <a name="remarks"></a>Comentarios  
 Realiza una consulta que use () DELETED para evaluar el estado de registros puede optimizarse mediante tecnología Rushmore de Visual FoxPro si la tabla está indizada en () eliminado.  
  
> [!IMPORTANT]  
>  SET DELETED se omite si el ámbito predeterminado para el comando es el registro actual o si incluye un ámbito de un único registro. ÍNDICE siempre omite SET DELETED y todos los registros de la tabla de índices.  
  
## <a name="see-also"></a>Vea también  
 [ELIMINAR, comando SQL](../../odbc/microsoft/delete-sql-command.md)

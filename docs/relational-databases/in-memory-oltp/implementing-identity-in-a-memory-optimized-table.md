---
title: Implementar IDENTITY en una tabla con optimización para memoria | Microsoft Docs
ms.custom: ''
ms.date: 03/01/2017
ms.prod: sql
ms.prod_service: database-engine, sql-database
ms.component: in-memory-oltp
ms.reviewer: ''
ms.suite: sql
ms.technology:
- database-engine-imoltp
ms.tgt_pltfrm: ''
ms.topic: conceptual
ms.assetid: c0a704a3-3a31-4c2c-b967-addacda62ef8
caps.latest.revision: 11
author: MightyPen
ms.author: genemi
manager: craigg
monikerRange: = azuresqldb-current || >= sql-server-2016 || = sqlallproducts-allversions
ms.openlocfilehash: ce137e05e473c16dffc4f4eb468bfff3de53bc93
ms.sourcegitcommit: 1740f3090b168c0e809611a7aa6fd514075616bf
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/03/2018
---
# <a name="implementing-identity-in-a-memory-optimized-table"></a>Implementar IDENTITY en una tabla con optimización para memoria
[!INCLUDE[appliesto-ss-asdb-xxxx-xxx-md](../../includes/appliesto-ss-asdb-xxxx-xxx-md.md)]

IDENTITY se admite en una tabla optimizada para memoria siempre y cuando el valor de inicialización y el incremento sean ambos 1 (que es el valor predeterminado). Las columnas de identidad con la definición de IDENTITY(x, y) donde x != 1 o y != 1 no se admiten en las tablas optimizadas para memoria.   
    
Para aumentar el valor de inicialización de IDENTITY, inserte una nueva fila con un valor explícito para la columna de identidad con la opción de sesión `SET IDENTITY_INSERT table_name ON`. Al insertar la fila, el valor de inicialización de IDENTITY se cambia por el valor insertado explícitamente más 1. Por ejemplo, para aumentar el valor de inicialización a 1000, inserte una fila con el valor 999 en la columna de identidad. De esta forma, los valores de identidad que se generen comenzarán a partir de 1000.     
  
## <a name="see-also"></a>Ver también  
 [Migrar a OLTP en memoria](../../relational-databases/in-memory-oltp/migrating-to-in-memory-oltp.md)  
  
  

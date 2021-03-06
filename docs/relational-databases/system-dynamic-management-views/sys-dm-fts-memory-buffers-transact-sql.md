---
title: Sys.dm_fts_memory_buffers (Transact-SQL) | Documentos de Microsoft
ms.custom: ''
ms.date: 03/29/2017
ms.prod: sql
ms.prod_service: database-engine, sql-database
ms.component: dmv's
ms.reviewer: ''
ms.suite: sql
ms.technology: system-objects
ms.tgt_pltfrm: ''
ms.topic: language-reference
f1_keywords:
- sys.dm_fts_memory_buffers
- dm_fts_memory_buffers_TSQL
- dm_fts_memory_buffers
- sys.dm_fts_memory_buffers_TSQL
dev_langs:
- TSQL
helpviewer_keywords:
- sys.dm_fts_memory_buffers dynamic management view
ms.assetid: 56895fe5-e8df-4d75-9adc-c1f7757cdef8
caps.latest.revision: 33
author: douglaslMS
ms.author: douglasl
manager: craigg
monikerRange: = azuresqldb-current || >= sql-server-2016 || = sqlallproducts-allversions
ms.openlocfilehash: 4c2efa81bdc5a0a9403ee36398d28d94117a1313
ms.sourcegitcommit: f1caaa156db2b16e817e0a3884394e7b30fb642f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/04/2018
---
# <a name="sysdmftsmemorybuffers-transact-sql"></a>sys.dm_fts_memory_buffers (Transact-SQL)
[!INCLUDE[tsql-appliesto-ss2008-asdb-xxxx-xxx-md](../../includes/tsql-appliesto-ss2008-asdb-xxxx-xxx-md.md)]

  Devuelve información acerca de los búferes de memoria que pertenecen a un bloque de memoria específico que se utiliza como parte de un rastreo de texto completo o un intervalo de rastreo de texto completo.  
  
> [!NOTE]
> La siguiente columna se quitará en futuras versiones de [!INCLUDE[msCoName](../../includes/msconame-md.md)] [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)]: **row_count**. Evite el uso de esta columna en los nuevos trabajos de desarrollo y piense en modificar las aplicaciones que la usan actualmente.  

  
|Columna|Data type|Description|  
|------------|---------------|-----------------|  
|**pool_id**|**int**|Id. del grupo de memoria asignado.<br /><br /> 0 = Búferes pequeños<br /><br /> 1 = Búferes grandes|  
|**memory_address**|**varbinary (8)**|Dirección del búfer de memoria asignado.|  
|**Nombre**|**nvarchar(4000)**|Nombre del búfer de memoria compartida para el que se ha realizado esta asignación.|  
|**is_free**|**bit**|Estado actual del búfer de memoria.<br /><br /> 0 = Disponible<br /><br /> 1 = Ocupado|  
|**row_count**|**int**|Número de filas que controla actualmente este búfer.|  
|**bytes_used**|**int**|Cantidad, en bytes, de memoria en uso en este búfer.|  
|**percent_used**|**int**|Porcentaje de memoria asignada usada.|  
  
## <a name="permissions"></a>Permissions  

En [!INCLUDE[ssNoVersion_md](../../includes/ssnoversion-md.md)], requiere `VIEW SERVER STATE` permiso.   
En [!INCLUDE[ssSDS_md](../../includes/sssds-md.md)], requiere el `VIEW DATABASE STATE` permiso en la base de datos.   
  
## <a name="physical-joins"></a>Combinaciones físicas  
 ![Combinaciones significativas de esta vista de administración dinámica](../../relational-databases/system-dynamic-management-views/media/join-dm-fts-memory-buffers-1.gif "combinaciones significativas de esta vista de administración dinámica")  
  
## <a name="relationship-cardinalities"></a>Cardinalidades de relación  
  
|De|En|Relación|  
|----------|--------|------------------|  
|dm_fts_memory_buffers.pool_id|dm_fts_memory_pools.pool_id|Varios a uno|  
  
## <a name="see-also"></a>Vea también  
 [Funciones y vistas de administración dinámica &#40;Transact-SQL&#41;](~/relational-databases/system-dynamic-management-views/system-dynamic-management-views.md)   
 [Funciones y vistas de administración dinámica de la búsqueda semántica y búsqueda de texto completo &#40;Transact-SQL&#41;](../../relational-databases/system-dynamic-management-views/full-text-and-semantic-search-dynamic-management-views-functions.md)  
  
  


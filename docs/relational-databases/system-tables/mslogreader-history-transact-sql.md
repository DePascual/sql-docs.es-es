---
title: MSlogreader_history (Transact-SQL) | Documentos de Microsoft
ms.custom: ''
ms.date: 03/03/2017
ms.prod: sql
ms.prod_service: database-engine
ms.component: system-tables
ms.reviewer: ''
ms.suite: sql
ms.technology:
- replication
ms.tgt_pltfrm: ''
ms.topic: language-reference
applies_to:
- SQL Server
f1_keywords:
- MSlogreader_history_TSQL
- MSlogreader_history
dev_langs:
- TSQL
helpviewer_keywords:
- MSlogreader_history system table
ms.assetid: 2e399fa1-3591-4c1c-96b7-7964fe82c7c4
caps.latest.revision: 29
author: edmacauley
ms.author: edmaca
manager: craigg
ms.openlocfilehash: 8041a5c3dfdb216d939ef5b99e22b36c0781eda9
ms.sourcegitcommit: 1740f3090b168c0e809611a7aa6fd514075616bf
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/03/2018
---
# <a name="mslogreaderhistory-transact-sql"></a>MSlogreader_history (Transact-SQL)
[!INCLUDE[tsql-appliesto-ss2008-xxxx-xxxx-xxx-md](../../includes/tsql-appliesto-ss2008-xxxx-xxxx-xxx-md.md)]

  El **MSlogreader_history** tabla contiene filas de historial para los agentes de lector de registro asociados al distribuidor local. Esta tabla se almacena en la base de datos de distribución.  
  
|Nombre de columna|Tipo de datos|Description|  
|-----------------|---------------|-----------------|  
|**agent_id**|**int**|Id. del Agente de registro del LOG.|  
|**runstatus**|**int**|Estado de ejecución:<br /><br /> 1 = Iniciada.<br /><br /> 2 = se realizan correctamente.<br /><br /> 3 = En curso.<br /><br /> 4 = Inactiva.<br /><br /> 5 = Reintentar.<br /><br /> 6 = Error.|  
|**start_time**|**datetime**|Hora a la que comienza la ejecución del trabajo.|  
|**time**|**datetime**|Hora a la que se registra el mensaje.|  
|**duration**|**int**|Duración, en segundos, de la sesión del mensaje.|  
|**Comentarios**|**nvarchar(255)**|El texto del mensaje.|  
|**xact_seqno**|**varbinary (16)**|Número de secuencia de la última transacción procesada.|  
|**delivery_time**|**int**|Se entrega la primera transacción de tiempo.|  
|**delivered_transactions**|**int**|Número total de transacciones entregadas en la sesión.|  
|**delivered_commands**|**int**|El número total de comandos entregados en la sesión.|  
|**average_commands**|**int**|Número promedio de comandos entregados en la sesión.|  
|**delivery_rate**|**float**|Promedio de comandos entregados por segundo.|  
|**delivery_latency**|**int**|Latencia entre la entrada del comando en la base de datos publicada y su entrada en la base de datos de distribución. En milisegundos.|  
|**error_id**|**int**|El identificador del error en la **MSrepl_error** tabla del sistema.|  
|**timestamp**|**timestamp**|La columna de marca de tiempo de esta tabla.|  
|**updateable_row**|**bit**|Establecido en **1** si la fila de historial se puede sobrescribir.|  
  
## <a name="see-also"></a>Vea también  
 [Tablas de replicación &#40;Transact-SQL&#41;](../../relational-databases/system-tables/replication-tables-transact-sql.md)   
 [Vistas de replicación &#40;Transact-SQL&#41;](../../relational-databases/system-views/replication-views-transact-sql.md)  
  
  

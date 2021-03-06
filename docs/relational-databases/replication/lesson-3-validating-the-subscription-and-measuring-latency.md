---
title: 'Lección 3: Validación de la suscripción y medición de la latencia | Microsoft Docs'
ms.custom: ''
ms.date: 03/01/2017
ms.prod: sql-non-specified
ms.prod_service: database-engine
ms.service: ''
ms.component: replication
ms.reviewer: ''
ms.suite: sql
ms.technology:
- replication
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- SQL Server 2016
helpviewer_keywords:
- replication [SQL Server], tutorials
ms.assetid: 147f7b93-1804-4e0b-9e17-57a51d035b2a
caps.latest.revision: 12
author: MashaMSFT
ms.author: mathoma
manager: craigg
ms.workload: Inactive
ms.openlocfilehash: 9ad3fadb0017628fa54a102366f132bbc72b9cfb
ms.sourcegitcommit: d6b1695c8cbc70279b7d85ec4dfb66a4271cdb10
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/10/2018
---
# <a name="lesson-3-validating-the-subscription-and-measuring-latency"></a>Lección 3: Validar la suscripción y medir la latencia
[!INCLUDE[appliesto-ss-xxxx-xxxx-xxx-md](../../includes/appliesto-ss-xxxx-xxxx-xxx-md.md)]
En esta lección, utilizará testigos de seguimiento para comprobar que los cambios se replican en el suscriptor y para determinar la latencia, es decir, el tiempo que se requiere para que un cambio realizado en el publicador aparezca en el suscriptor. Esta lección requiere que haya completado la lección anterior, [Lección 2: Crear una suscripción a la publicación transaccional](../../relational-databases/replication/lesson-2-creating-a-subscription-to-the-transactional-publication.md).  
  
### <a name="to-insert-a-tracer-token-and-view-information-on-the-token"></a>Para insertar un testigo de seguimiento y ver la información del token  
  
1.  Conéctese al publicador en [!INCLUDE[ssManStudioFull](../../includes/ssmanstudiofull-md.md)], expanda el nodo del servidor, haga clic con el botón derecho en la carpeta **Replicación** y luego en **Iniciar el Monitor de replicación**.  
  
    Se inicia el Monitor de replicación.  
  
2.  Expanda un grupo de publicador en el panel izquierdo, expanda una instancia de publicador y, a continuación, haga clic en la publicación **AdvWorksProductTrans** .  
  
3.  Haga clic en la pestaña **Testigos de seguimiento** .  
  
4.  Haga clic en **Insertar seguimiento**.  
  
5.  Vea el tiempo transcurrido para el testigo de seguimiento en las siguientes columnas: **Publicador a distribuidor**, **Distribuidor a suscriptor**y **Latencia total**. El valor **Pendiente** indica que el testigo no ha alcanzado un punto específico.  
  
## <a name="next-steps"></a>Next Steps  
En esta lección, utilizó correctamente los testigos de seguimiento para comprobar que los cambios de datos se replican del publicador al suscriptor. También puede insertar, actualizar o eliminar datos en la tabla **Product** en el publicador y consultar la tabla **Product** en el suscriptor para ver esos cambios, una vez replicados.  
  
Con esto finaliza el tutorial Replicar datos entre servidores conectados de forma continua. Para realizar un tutorial similar que utiliza replicación de mezcla, vea [Tutorial: Replicating Data with Mobile Clients](../../relational-databases/replication/tutorial-replicating-data-with-mobile-clients.md).  
  
## <a name="see-also"></a>Ver también  
[Medir la latencia y validar las conexiones de la replicación transaccional](../../relational-databases/replication/monitor/measure-latency-and-validate-connections-for-transactional-replication.md)  
  
  
  

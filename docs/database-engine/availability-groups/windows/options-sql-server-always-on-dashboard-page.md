---
title: Opciones (SQL Server AlwaysOn, página del panel) | Microsoft Docs
ms.custom: ''
ms.date: 05/17/2016
ms.prod: sql
ms.prod_service: high-availability
ms.reviewer: ''
ms.suite: sql
ms.technology: high-availability
ms.tgt_pltfrm: ''
ms.topic: conceptual
f1_keywords:
- VS.ToolsOptionsPages.Alwayson.Dashboard
ms.assetid: 4369b588-e982-4b57-80a1-beb2e879ce0b
caps.latest.revision: 8
author: MikeRayMSFT
ms.author: mikeray
manager: craigg
ms.openlocfilehash: 6bc9649dd6bd14a0a34005e369285275c7acb0a9
ms.sourcegitcommit: 1740f3090b168c0e809611a7aa6fd514075616bf
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/03/2018
---
# <a name="options-sql-server-always-on-dashboard-page"></a>Opciones (SQL Server AlwaysOn, página del panel)
[!INCLUDE[appliesto-ss-xxxx-xxxx-xxx-md](../../../includes/appliesto-ss-xxxx-xxxx-xxx-md.md)]

  Use la página **Panel AlwaysOn de SQL Server** del cuadro de diálogo **Opciones de [!INCLUDE[ssManStudioFull](../../../includes/ssmanstudiofull-md.md)]** para configurar el panel de AlwaysOn.  
  
 **Para acceder a esta página:**  
  
 En el menú **Herramientas** , haga clic en **Opciones**, expanda la carpeta **SQL Server Always On** y luego haga clic en **Panel**.  
  
## <a name="on-this-page"></a>En esta página  
 **Activar actualización automática.**  
 Haga clic para habilitar la actualización automática. Las opciones son:  
  
-   El campo **Intervalo de actualización (en segundos)** muestra el número de segundos que pasarán antes de cada actualización del panel. El valor predeterminado es 30. Cuando se habilita la actualización automática, se puede editar este campo para cambiar el intervalo de actualización.  
  
-   El **Número de reintentos de conexión** muestra el número de veces que el panel intentará conectarse a una instancia de [!INCLUDE[ssNoVersion](../../../includes/ssnoversion-md.md)] que hospeda una réplica de disponibilidad para un grupo de disponibilidad que el panel está supervisando. El valor predeterminado es 65535. Cuando se habilita la actualización automática, se puede editar este campo para cambiar el número de reintentos de conexión.  
  
 **Habilite la directiva de AlwaysOn definida por el usuario.**  
 Si ha definido su propia directiva de AlwaysOn, haga clic en esta opción para habilitar la directiva.  
  
## <a name="see-also"></a>Ver también  
 [Usar el Panel de AlwaysOn &#40;SQL Server Management Studio&#41;](../../../database-engine/availability-groups/windows/use-the-always-on-dashboard-sql-server-management-studio.md)  
  
  

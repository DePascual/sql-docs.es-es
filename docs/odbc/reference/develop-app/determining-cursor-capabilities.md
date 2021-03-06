---
title: Determinar las capacidades del Cursor | Documentos de Microsoft
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
- scrollable cursors [ODBC]
- cursors [ODBC], capabilities
- cursors [ODBC], scrollable
ms.assetid: 35be486c-8f2d-4cec-beb8-df14151abfef
caps.latest.revision: 5
author: MightyPen
ms.author: genemi
manager: craigg
ms.openlocfilehash: 3974fb30a9151cdcf681a106ddcf3073b63f66b6
ms.sourcegitcommit: 1740f3090b168c0e809611a7aa6fd514075616bf
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/03/2018
---
# <a name="determining-cursor-capabilities"></a>Determinar las capacidades del Cursor
Las siguientes cuatro opciones en **SQLGetInfo** describen qué tipos de cursores se admiten y cuáles son sus capacidades:  
  
-   SQL_CURSOR_SENSITIVITY. Indica si un cursor es sensible a los cambios realizados por otro cursor.  
  
-   SQL_SCROLL_OPTIONS. Enumera los tipos de cursor compatible (solo avance, estáticos, controlado por, dinámicos o mixtos). Todos los orígenes de datos deben admitir cursores de solo avance.  
  
-   SQL_DYNAMIC_CURSOR_ATTRIBUTES1, SQL_FORWARD_ONLY_CURSOR_ATTRIBUTES1, SQL_KEYSET_CURSOR_ATTRIBUTES1 o SQL_STATIC_CURSOR_ATTRIBUTES1 (dependiendo del tipo del cursor). Enumera los tipos de captura compatibles con los cursores desplazables. Los bits del valor devuelto se corresponden con los tipos de captura en **SQLFetchScroll**.  
  
-   SQL_KEYSET_CURSOR_ATTRIBUTES2 o SQL_STATIC_CURSOR_ATTRIBUTES2 (dependiendo del tipo del cursor). Indica si pueden detectar los cursores estáticos y cursores controlados por sus propias actualizaciones, eliminaciones e inserciones.  
  
 Una aplicación puede determinar las capacidades de cursor en tiempo de ejecución mediante una llamada a **SQLGetInfo** con estas opciones. Esto se suele hacer por aplicaciones genéricas. Funciones de cursor también se pueden determinar durante el desarrollo de aplicaciones y su uso codificado de forma rígida en la aplicación. Esto se realiza normalmente por las aplicaciones verticales y personalizadas pero también puede realizarse mediante aplicaciones genéricas que utiliza una implementación de cursor de cliente, como la biblioteca de cursores ODBC.

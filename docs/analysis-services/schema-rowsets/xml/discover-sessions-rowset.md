---
title: Conjunto de filas DISCOVER_SESSIONS | Documentos de Microsoft
ms.date: 05/03/2018
ms.prod: sql
ms.technology: analysis-services
ms.custom: schema-rowsets
ms.topic: reference
ms.author: owend
ms.reviewer: owend
author: minewiskan
manager: kfile
ms.openlocfilehash: 986fe462d5582f86fab56a28751b48475cbeb74e
ms.sourcegitcommit: c12a7416d1996a3bcce3ebf4a3c9abe61b02fb9e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/10/2018
---
# <a name="discoversessions-rowset"></a>DISCOVER_SESSIONS, conjunto de filas
[!INCLUDE[ssas-appliesto-sqlas](../../../includes/ssas-appliesto-sqlas.md)]
  Proporciona información sobre el uso de los recursos y la actividad en las sesiones abiertas actualmente en el servidor.  
  
## <a name="rowset-columns"></a>Columnas del conjunto de filas  
 El conjunto de filas **DISCOVER_SESSIONS** contiene las siguientes columnas.  
  
|Nombre de columna|Indicador de tipo|Longitud|Description|  
|-----------------|--------------------|------------|-----------------|  
|**SESSION_COMMAND_COUNT**|**DBTYPE_I4**||Número de comandos que comenzaron a ejecutarse desde el principio de la sesión.|  
|**SESSION_CONNECTION_ID**|**DBTYPE_I4**||Identificador de conexión de la sesión.|  
|**SESSION_CPU_TIME_MS**|**DBTYPE_UI8**||Tiempo de CPU, en milisegundos, consumido por todas las solicitudes desde el principio de la sesión.|  
|**SESSION_CURRENT_DATABASE**|**DBTYPE_WSTR**||Nombre de la base de datos que utiliza la ejecución del comando actual o de la base de datos que utilizó el último comando ejecutado.|  
|**SESSION_ELAPSED_TIME_MS**|**DBTYPE_UI8**||Tiempo transcurrido, en milisegundos, desde el inicio de la sesión.|  
|**SESSION_ID**|**DBTYPE_WSTR**||Identificador único de la sesión, como un GUID.|  
|**SESSION_IDLE_TIME_MS**|**DBTYPE_UI8**||Tiempo de inactividad, en milisegundos, desde el inicio de la sesión.|  
|**SESSION_LAST_COMMAND**|**DBTYPE_WSTR**||Texto del comando que se está ejecutando actualmente o del último comando ejecutado.|  
|**SESSION_LAST_COMMAND_CPU_TIME_MS**|**DBTYPE_UI8**||Tiempo de CPU, en milisegundos, consumido por **SESSION_LAST_COMMAND**.|  
|**SESSION_LAST_COMMAND_ELAPSED_TIME_MS**|**DBTYPE_UI8**||Tiempo transcurrido, en milisegundos, desde el inicio de **SESSION_LAST_COMMAND**.|  
|**SESSION_LAST_COMMAND_END_TIME**|**DBTYPE_DBTIMESTAMP**||Hora UTC del servidor en el momento en que terminó de ejecutarse el último comando.|  
|**SESSION_LAST_COMMAND_START_TIME**|**DBTYPE_DBTIMESTAMP**||Hora UTC del servidor en el momento en que comenzó a ejecutarse el último comando.|  
|**SESSION_PROPERTIES**|**DBTYPE_WSTR**||Reservado para uso futuro.|  
|**SESSION_READ_KB**|**DBTYPE_UI8**||Valor acumulado de los datos leídos del disco desde el inicio de la sesión, en kilobytes.|  
|**SESSION_READS**|**DBTYPE_UI8**||Número acumulado de lecturas de disco desde el inicio de la sesión.|  
|**SESSION_SPID**|**DBTYPE_I4**||Identificador de la sesión.|  
|**SESSION_START_TIME**|**DBTYPE_DBTIMESTAMP**||Fecha y hora en que se inició la sesión como hora UTC para el servidor.|  
|**SESSION_STATUS**|**DBTYPE_I4**||Estado de actividad de la sesión.<br /><br /> 0 significa "Inactivo": No hay ninguna actividad actual en curso.<br /><br /> 1 significa "Activo": La sesión está ejecutando alguna tarea solicitada.<br /><br /> 2 significa "Bloqueado": La sesión está esperando que algún recurso continúe ejecutando la tarea suspendida.<br /><br /> 3 significa "Cancelado": La sesión se ha etiquetado como cancelada.|  
|**SESSION_USED_MEMORY**|**DBTYPE_I4**||Tamaño actual de la memoria utilizada por la sesión, en kilobytes. El valor notificado es el uso de RAM por SPID, sin distinción entre la memoria reducible y la no reducible. A diferencia de otras DMV que notifican el uso de memoria, DISCOVER_SESSIONS no divide el uso de memoria por categorías.<br /><br /> Tenga en cuenta que SESSION_USED_MEMORY tiende a notificar valores de uso de memoria inferiores a los reales, porque excluye los objetos compartidos entre varias sesiones.  Solo se representan en el cálculo de memoria aquellos objetos que son únicos en la sesión.|  
|**SESSION_USER_NAME**|**DBTYPE_WSTR**||Nombre de usuario de la sesión.|  
|**SESSION_WRITE_KB**|**DBTYPE_UI8**||Valor acumulado de los datos escritos en el disco desde el inicio de la sesión, en kilobytes.|  
|**SESSION_WRITES**|**DBTYPE_UI8**||Número acumulado de escrituras en disco desde el inicio de la sesión.|  
  
 Este conjunto de filas de esquema no está ordenado.  
  
## <a name="restriction-columns"></a>Columnas de restricción  
 El conjunto de filas **DISCOVER_SESSIONS** puede tener restricciones en las columnas que se muestran en la tabla siguiente.  
  
|Nombre de columna|Indicador de tipo|Estado de restricción|  
|-----------------|--------------------|-----------------------|  
|SESSION_ID|DBTYPE_WSTR|Opcional.|  
|SESSION_SPID|DBTYPE_I4|Opcional.|  
|SESSION_CONNECTION_ID|DBTYPE_I4|Opcional.|  
|SESSION_USER_NAME|DBTYPE_WSTR|Opcional.|  
|SESSION_CURRENT_DATABASE|DBTYPE_WSTR|Opcional.|  
|SESSION_ELAPSED_TIME_MS|DBTYPE_UI8|Opcional.|  
|SESSION_CPU_TIME_MS|DBTYPE_UI8|Opcional.|  
|SESSION_IDLE_TIME_MS|DBTYPE_UI8|Opcional.|  
|SESSION_STATUS|DBTYPE_I4|Opcional.|  
  
## <a name="see-also"></a>Vea también  
 [XML para conjuntos de filas de esquema de análisis](../../../analysis-services/schema-rowsets/xml/xml-for-analysis-schema-rowsets.md)  
  
  

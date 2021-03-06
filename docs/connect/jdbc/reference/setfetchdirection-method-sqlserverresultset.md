---
title: Método setFetchDirection (SQLServerResultSet) | Documentos de Microsoft
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.suite: sql
ms.technology: connectivity
ms.tgt_pltfrm: ''
ms.topic: conceptual
apiname:
- SQLServerResultSet.setFetchDirection
apilocation:
- sqljdbc.jar
apitype: Assembly
ms.assetid: 4ee82290-508d-4bff-a5c5-8a56338deef8
caps.latest.revision: 12
author: MightyPen
ms.author: genemi
manager: craigg
ms.openlocfilehash: c1f042804aa21ca91031c56d285bbfb9d0d8e1f0
ms.sourcegitcommit: 1740f3090b168c0e809611a7aa6fd514075616bf
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/03/2018
---
# <a name="setfetchdirection-method-sqlserverresultset"></a>Método setFetchDirection (SQLServerResultSet)
[!INCLUDE[Driver_JDBC_Download](../../../includes/driver_jdbc_download.md)]

  Ofrece una sugerencia sobre la dirección en la que las filas en esta [SQLServerResultSet](../../../connect/jdbc/reference/sqlserverresultset-class.md) se procesará el objeto.  
  
> [!NOTE]  
>  Este método no es compatible actualmente con la [!INCLUDE[jdbcNoVersion](../../../includes/jdbcnoversion_md.md)]. Si utiliza este método, el controlador JDBC recuerda la configuración, pero no emprende ninguna acción con el método por el momento.  
  
## <a name="syntax"></a>Sintaxis  
  
```  
  
public void setFetchDirection(int direction)  
```  
  
#### <a name="parameters"></a>Parámetros  
 *Dirección*  
  
 Un **int** que indica la dirección de recuperación sugerida. Puede ser uno de los siguientes valores:  
  
 ResultSet.FETCH_FORWARD  
  
 ResultSet.FETCH_REVERSE  
  
 ResultSet.FETCH_UNKNOWN  
  
## <a name="exceptions"></a>Excepciones  
 [SQLServerException](../../../connect/jdbc/reference/sqlserverexception-class.md)  
  
## <a name="remarks"></a>Comentarios  
 Este método setFetchDirection especificado por el método setFetchDirection en la interfaz java.sql.ResultSet.  
  
 El valor inicial de este método está determinado por la [SQLServerStatement](../../../connect/jdbc/reference/sqlserverstatement-class.md) objeto que generó este objeto SQLServerResultSet. La dirección de la captura puede cambiar en cualquier momento.  
  
> [!NOTE]  
>  Si se utiliza este método cuando el tipo de cursor es de solo avance, no tendrá efecto alguno.  
  
## <a name="see-also"></a>Vea también  
 [Miembros SQLServerResultSet](../../../connect/jdbc/reference/sqlserverresultset-members.md)   
 [Clase SQLServerResultSet](../../../connect/jdbc/reference/sqlserverresultset-class.md)  
  
  

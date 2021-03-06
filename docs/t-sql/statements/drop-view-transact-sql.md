---
title: DROP VIEW (Transact-SQL) | Microsoft Docs
ms.custom: ''
ms.date: 05/12/2017
ms.prod: sql
ms.prod_service: database-engine, sql-database, sql-data-warehouse, pdw
ms.component: t-sql|statements
ms.reviewer: ''
ms.suite: sql
ms.technology: t-sql
ms.tgt_pltfrm: ''
ms.topic: language-reference
f1_keywords:
- DROP_VIEW_TSQL
- DROP VIEW
dev_langs:
- TSQL
helpviewer_keywords:
- dropping views
- DROP VIEW statement
- deleting views
- indexed views [SQL Server], removing
- views [SQL Server], removing
- removing views
ms.assetid: 03cea355-e39c-46e1-b7db-8832038669dd
caps.latest.revision: 42
author: edmacauley
ms.author: edmaca
manager: craigg
monikerRange: '>= aps-pdw-2016 || = azuresqldb-current || = azure-sqldw-latest || >= sql-server-2016 || = sqlallproducts-allversions'
ms.openlocfilehash: f1b3f55f30ae5c213ccb5373613625c46b105a12
ms.sourcegitcommit: 1740f3090b168c0e809611a7aa6fd514075616bf
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/03/2018
---
# <a name="drop-view-transact-sql"></a>DROP VIEW (Transact-SQL)
[!INCLUDE[tsql-appliesto-ss2008-all-md](../../includes/tsql-appliesto-ss2008-all-md.md)]

  Quita una o más vistas de la base de datos actual. DROP VIEW se puede ejecutar en vistas indizadas.  
  
 ![Icono de vínculo de tema](../../database-engine/configure-windows/media/topic-link.gif "Icono de vínculo de tema") [Convenciones de sintaxis de Transact-SQL](../../t-sql/language-elements/transact-sql-syntax-conventions-transact-sql.md)  
  
## <a name="syntax"></a>Sintaxis  
  
```  
-- Syntax for SQL Server and Azure SQL Database  
  
DROP VIEW [ IF EXISTS ] [ schema_name . ] view_name [ ...,n ] [ ; ]  
```  
  
```  
-- Syntax for Azure SQL Data Warehouse and Parallel Data Warehouse  
  
DROP VIEW [ schema_name . ] view_name   
[;]  
```  
  
## <a name="arguments"></a>Argumentos  
 *IF EXISTS*  
 **Se aplica a**: [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] (desde [!INCLUDE[ssSQL15](../../includes/sssql15-md.md)] hasta la [versión actual](http://go.microsoft.com/fwlink/p/?LinkId=299658), [!INCLUDE[sssds](../../includes/sssds-md.md)]).|  
  
 Quita la vista condicionalmente solo si ya existe.  
  
 *schema_name*  
 Es el nombre del esquema al que pertenece la vista.  
  
 *view_name*  
 Es el nombre de la vista que se va a quitar.  
  
## <a name="remarks"></a>Notas  
 Cuando se quita una vista, la definición y otra información de la vista se elimina del catálogo del sistema. También se eliminan todos los permisos de la vista.  
  
 Las vistas de una tabla que se ha quitado mediante DROP TABLE se deben quitar explícitamente con DROP VIEW.  
  
 Cuando se ejecuta en una vista indizada, DROP VIEW quita automáticamente todos los índices de una vista. Para mostrar todos los índices de una vista, utilice [sp_helpindex](../../relational-databases/system-stored-procedures/sp-helpindex-transact-sql.md).  
  
 Cuando se realiza una consulta a través de una vista, el [!INCLUDE[ssDE](../../includes/ssde-md.md)] se asegura de que todos los objetos de base de datos a los que se hace referencia en la instrucción existen, que son válidos en el contexto de la instrucción y que las instrucciones de modificación de datos no infringen ninguna regla de integridad de los datos. Las comprobaciones que no son correctas devuelven un mensaje de error. Las comprobaciones correctas traducen la acción a una acción con las tablas subyacentes. Si las vistas o tablas subyacentes han cambiado desde que se creó la vista, puede ser útil quitar y volver a crear la vista.  
  
 Para obtener más información sobre cómo determinar las dependencias de un desencadenador específico, consulte [sys.sql_dependencies &#40;Transact-SQL&#41;](../../relational-databases/system-catalog-views/sys-sql-dependencies-transact-sql.md).  
  
 Para obtener más información sobre cómo ver el texto de la vista, consulte [sp_helptext &#40;Transact-SQL&#41;](../../relational-databases/system-stored-procedures/sp-helptext-transact-sql.md).  
  
## <a name="permissions"></a>Permisos  
 Requiere el permiso **CONTROL** en la vista, el permiso **ALTER** en el esquema que contiene la vista o la pertenencia al rol fijo de servidor **db_ddladmin**.  
  
## <a name="examples"></a>Ejemplos  
  
### <a name="a-drop-a-view"></a>A. Quitar una vista  
 En el siguiente ejemplo se quita la vista `Reorder`.  
  
```  
DROP VIEW dbo.Reorder ;  
GO  
```  
  
## <a name="see-also"></a>Ver también  
 [ALTER VIEW &#40;Transact-SQL&#41;](../../t-sql/statements/alter-view-transact-sql.md)   
 [CREATE VIEW &#40;Transact-SQL&#41;](../../t-sql/statements/create-view-transact-sql.md)   
 [EVENTDATA &#40;Transact-SQL&#41;](../../t-sql/functions/eventdata-transact-sql.md)   
 [sys.columns &#40;Transact-SQL&#41;](../../relational-databases/system-catalog-views/sys-columns-transact-sql.md)   
 [sys.objects &#40;Transact-SQL&#41;](../../relational-databases/system-catalog-views/sys-objects-transact-sql.md)   
 [USE &#40;Transact-SQL&#41;](../../t-sql/language-elements/use-transact-sql.md)   
 [sys.sql_expression_dependencies &#40;Transact-SQL&#41;](../../relational-databases/system-catalog-views/sys-sql-expression-dependencies-transact-sql.md)  
 

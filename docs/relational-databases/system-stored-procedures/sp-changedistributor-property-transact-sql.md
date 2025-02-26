---
title: "sp_changedistributor_property (Transact-SQL)"
description: "sp_changedistributor_property (Transact-SQL)"
author: markingmyname
ms.author: maghan
ms.date: "03/06/2017"
ms.service: sql
ms.subservice: replication
ms.topic: "reference"
f1_keywords:
  - "sp_changedistributor_property_TSQL"
  - "sp_changedistributor_property"
helpviewer_keywords:
  - "sp_changedistributor_property"
dev_langs:
  - "TSQL"
---
# sp_changedistributor_property (Transact-SQL)
[!INCLUDE [SQL Server SQL MI](../../includes/applies-to-version/sql-asdbmi.md)]

  Changes the properties of the Distributor. This stored procedure is executed at the Distributor on any database.  
  
 :::image type="icon" source="../../includes/media/topic-link-icon.svg" border="false"::: [Transact-SQL syntax conventions](../../t-sql/language-elements/transact-sql-syntax-conventions-transact-sql.md)  
  
## Syntax  
  
```  
  
sp_changedistributor_property [ [ @property= ] 'property' ]  
    [ , [ @value= ] 'value' ]  
```  
  
## Arguments  
`[ @property = ] 'property'`
 Is the property for a given Distributor. *property* is **sysname**, and can be one of these values.  
  
|Value|Description|  
|-----------|-----------------|  
|**heartbeat_interval**|Maximum number of minutes that an agent can run without logging a progress message.|  
|NULL (default)|All available *property* values are printed.|  
  
`[ @value = ] 'value'`
 Is the value for the given Distributor property. *value* is **varchar(255)**, with a default of NULL.  
  
## Return Code Values  
 **0** (success) or **1** (failure)  
  
## Remarks  
 **sp_changedistributor_property** is used in all types of replication.  
  
## Example  
 [!code-sql[HowTo#sp_changedistributor_property](../../relational-databases/replication/codesnippet/tsql/sp-changedistributor-pro_1.sql)]  
  
## Permissions  
 Only members of the **sysadmin** fixed server role can execute **sp_changedistributor_property**.  
  
## See Also  
 [View and Modify Distributor and Publisher Properties](../../relational-databases/replication/view-and-modify-distributor-and-publisher-properties.md)   
 [sp_adddistributor &#40;Transact-SQL&#41;](../../relational-databases/system-stored-procedures/sp-adddistributor-transact-sql.md)   
 [sp_dropdistributor &#40;Transact-SQL&#41;](../../relational-databases/system-stored-procedures/sp-dropdistributor-transact-sql.md)   
 [sp_helpdistributor &#40;Transact-SQL&#41;](../../relational-databases/system-stored-procedures/sp-helpdistributor-transact-sql.md)   
 [Replication Stored Procedures &#40;Transact-SQL&#41;](../../relational-databases/system-stored-procedures/replication-stored-procedures-transact-sql.md)  
  
  

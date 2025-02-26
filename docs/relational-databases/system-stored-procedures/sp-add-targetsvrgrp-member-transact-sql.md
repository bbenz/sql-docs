---
title: "sp_add_targetsvrgrp_member (Transact-SQL)"
description: "sp_add_targetsvrgrp_member (Transact-SQL)"
author: markingmyname
ms.author: maghan
ms.date: "08/09/2016"
ms.service: sql
ms.subservice: system-objects
ms.topic: "reference"
f1_keywords:
  - "sp_add_targetsvrgrp_member"
  - "sp_add_targetsvrgrp_member_TSQL"
helpviewer_keywords:
  - "sp_add_targetsvrgrp_member"
dev_langs:
  - "TSQL"
---
# sp_add_targetsvrgrp_member (Transact-SQL)
[!INCLUDE [SQL Server](../../includes/applies-to-version/sqlserver.md)]

  Adds the specified target server to the specified target server group.  
   
 :::image type="icon" source="../../includes/media/topic-link-icon.svg" border="false"::: [Transact-SQL syntax conventions](../../t-sql/language-elements/transact-sql-syntax-conventions-transact-sql.md)  
  
## Syntax  
  
```  
  
sp_add_targetsvrgrp_member [ @group_name = ] 'group_name' , [ @server_name = ] 'server_name'   
```  
  
## Arguments  
`[ @group_name = ] 'group_name'`
 The name of the group. *group_name* is **sysname**, with no default.  
  
`[ @server_name = ] 'server_name'`
 The name of the server that should be added to the specified group. *server_name* is **nvarchar(30)**, with no default.  
  
## Return Code Values  
 **0** (success) or **1** (failure)  
  
## Result Sets  
 None  
  
## Remarks  
 A target server can be a member of more than one target server group.  
  
## Permissions  
 Only members of the **sysadmin** fixed server role can execute this procedure.  
  
## Examples  
 The following example adds the group `Servers Maintaining Customer Information` and adds the `LONDON1` server to that group.  
  
```  
USE msdb ;  
GO  
  
EXEC dbo.sp_add_targetsvrgrp_member  
   @group_name = N'Servers Maintaining Customer Information',  
   @server_name = N'LONDON1' ;  
GO  
```  
  
## See Also  
 [sp_delete_targetsvrgrp_member &#40;Transact-SQL&#41;](../../relational-databases/system-stored-procedures/sp-delete-targetsvrgrp-member-transact-sql.md)   
 [System Stored Procedures &#40;Transact-SQL&#41;](../../relational-databases/system-stored-procedures/system-stored-procedures-transact-sql.md)  
  
  

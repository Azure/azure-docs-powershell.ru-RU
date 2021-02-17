---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncMember.md
ms.openlocfilehash: e5bb853d9dd818801298254eac1f120efcc829a4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100212505"
---
# <span data-ttu-id="ddbca-101">Get-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="ddbca-101">Get-AzSqlSyncMember</span></span>

## <span data-ttu-id="ddbca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ddbca-102">SYNOPSIS</span></span>
<span data-ttu-id="ddbca-103">Возвращает сведения об участниками синхронизации баз SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="ddbca-103">Returns information about Azure SQL Database Sync Members.</span></span>

## <span data-ttu-id="ddbca-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ddbca-104">SYNTAX</span></span>

```
Get-AzSqlSyncMember [-Name <String>] [-SyncGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ddbca-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ddbca-105">DESCRIPTION</span></span>
<span data-ttu-id="ddbca-106">Командалет **Get-AzSqlSyncMember** возвращает сведения об одном или SQL участников синхронизации баз данных Azure.</span><span class="sxs-lookup"><span data-stu-id="ddbca-106">The **Get-AzSqlSyncMember** cmdlet returns information about one or more Azure SQL Database Sync Members.</span></span>
<span data-ttu-id="ddbca-107">Укажите имя участника синхронизации, чтобы увидеть сведения только для этого участника.</span><span class="sxs-lookup"><span data-stu-id="ddbca-107">Specify the name of a sync member to see information for only that sync member.</span></span>

## <span data-ttu-id="ddbca-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ddbca-108">EXAMPLES</span></span>

### <span data-ttu-id="ddbca-109">Пример 1. Все экземпляры azure SQL, которые назначены группе синхронизации</span><span class="sxs-lookup"><span data-stu-id="ddbca-109">Example 1: Get all instances of Azure SQL Sync Member assigned to a sync group</span></span>
```
PS C:\> Get-AzSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" | Format-List
ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup01}/syncMembers/{SyncMember01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup01
SyncMemberName              : SyncMember01
SyncDirection               : OneWayMemberToHub
MemberDatabaseType:         : AzureSqlDatabase
SyncAgentId                 : 
SqlServerDatabaseId         : 
MemberServerName            : memberServer01.full.dns.name
MemberDatabaseName          : memberDatabase01
MemberDatabaseUserName      : myAccount
MemberDatabasePassword      : 
SyncState                   : Good 

ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup01}/syncMembers/{SyncMember02}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup01
SyncMemberName              : SyncMember02
SyncDirection               : OneWayMemberToHub
MemberDatabaseType:         : AzureSqlDatabase
SyncAgentId                 : 
SqlServerDatabaseId         : 
MemberServerName            : memberServer01.full.dns.name
MemberDatabaseName          : memberDatabase01
MemberDatabaseUserName      : myAccount
MemberDatabasePassword      :  
SyncState                   : Good
```

<span data-ttu-id="ddbca-110">Эта команда получает сведения обо всех участниках синхронизации SQL Azure, которые назначены группе синхронизации SyncGroup01.</span><span class="sxs-lookup"><span data-stu-id="ddbca-110">This command gets information about all the Azure SQL Database Sync Member assigned to the sync group SyncGroup01.</span></span>

### <span data-ttu-id="ddbca-111">Пример 2. Сведения о члене синхронизации базы данных Azure SQL Azure</span><span class="sxs-lookup"><span data-stu-id="ddbca-111">Example 2: Get information about an Azure SQL Database Sync Member</span></span>
```
PS C:\> Get-AzSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -Name "SyncMember01" | Format-List
ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup01}/syncMembers/{SyncMember01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup01
SyncMemberName              : SyncMember01
SyncDirection               : OneWayMemberToHub
MemberDatabaseType:         : AzureSqlDatabase
SyncAgentId                 : 
SqlServerDatabaseId         : 
MemberServerName            : memberServer01.full.dns.name
MemberDatabaseName          : memberDatabase01
MemberDatabaseUserName      : myAccount
MemberDatabasePassword      : 
SyncState                   : Good
```

<span data-ttu-id="ddbca-112">Эта команда получает сведения о члене синхронизации базы данных Azure SQL с именем SyncMember01.</span><span class="sxs-lookup"><span data-stu-id="ddbca-112">This command gets information about the Azure SQL Database Sync Member with name "SyncMember01"</span></span>

### <span data-ttu-id="ddbca-113">Пример 3. Все экземпляры azure SQL, которые назначены группе синхронизации с помощью фильтрации</span><span class="sxs-lookup"><span data-stu-id="ddbca-113">Example 3: Get all instances of Azure SQL Sync Member assigned to a sync group using filtering</span></span>
```
PS C:\> Get-AzSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -Name "SyncMember*" | Format-List
ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup01}/syncMembers/{SyncMember01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup01
SyncMemberName              : SyncMember01
SyncDirection               : OneWayMemberToHub
MemberDatabaseType:         : AzureSqlDatabase
SyncAgentId                 : 
SqlServerDatabaseId         : 
MemberServerName            : memberServer01.full.dns.name
MemberDatabaseName          : memberDatabase01
MemberDatabaseUserName      : myAccount
MemberDatabasePassword      : 
SyncState                   : Good 

ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup01}/syncMembers/{SyncMember02}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup01
SyncMemberName              : SyncMember02
SyncDirection               : OneWayMemberToHub
MemberDatabaseType:         : AzureSqlDatabase
SyncAgentId                 : 
SqlServerDatabaseId         : 
MemberServerName            : memberServer01.full.dns.name
MemberDatabaseName          : memberDatabase01
MemberDatabaseUserName      : myAccount
MemberDatabasePassword      :  
SyncState                   : Good
```

<span data-ttu-id="ddbca-114">Эта команда получает сведения обо всех участниках синхронизации баз данных Azure SQL, которые назначены группе синхронизации SyncGroup01, которая начинается с "SyncMember".</span><span class="sxs-lookup"><span data-stu-id="ddbca-114">This command gets information about all the Azure SQL Database Sync Member assigned to the sync group SyncGroup01 that start with "SyncMember".</span></span>

## <span data-ttu-id="ddbca-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ddbca-115">PARAMETERS</span></span>

### <span data-ttu-id="ddbca-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ddbca-116">-DatabaseName</span></span>
<span data-ttu-id="ddbca-117">Имя базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="ddbca-117">The name of the Azure SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddbca-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddbca-118">-DefaultProfile</span></span>
<span data-ttu-id="ddbca-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="ddbca-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddbca-120">-Name</span><span class="sxs-lookup"><span data-stu-id="ddbca-120">-Name</span></span>
<span data-ttu-id="ddbca-121">Имя участника синхронизации.</span><span class="sxs-lookup"><span data-stu-id="ddbca-121">The sync member name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncMemberName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddbca-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ddbca-122">-ResourceGroupName</span></span>
<span data-ttu-id="ddbca-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ddbca-123">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddbca-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ddbca-124">-ServerName</span></span>
<span data-ttu-id="ddbca-125">Имя службы Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="ddbca-125">The name of the Azure SQL Server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddbca-126">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="ddbca-126">-SyncGroupName</span></span>
<span data-ttu-id="ddbca-127">Имя группы синхронизации.</span><span class="sxs-lookup"><span data-stu-id="ddbca-127">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddbca-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddbca-128">CommonParameters</span></span>
<span data-ttu-id="ddbca-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ddbca-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddbca-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ddbca-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddbca-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ddbca-131">INPUTS</span></span>

### <span data-ttu-id="ddbca-132">System.String</span><span class="sxs-lookup"><span data-stu-id="ddbca-132">System.String</span></span>

## <span data-ttu-id="ddbca-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ddbca-133">OUTPUTS</span></span>

### <span data-ttu-id="ddbca-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="ddbca-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="ddbca-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ddbca-135">NOTES</span></span>

## <span data-ttu-id="ddbca-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ddbca-136">RELATED LINKS</span></span>

[<span data-ttu-id="ddbca-137">New-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="ddbca-137">New-AzSqlSyncMember</span></span>](./New-AzSqlSyncMember.md)

[<span data-ttu-id="ddbca-138">Update-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="ddbca-138">Update-AzSqlSyncMember</span></span>](./Update-AzSqlSyncMember.md)

[<span data-ttu-id="ddbca-139">Remove-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="ddbca-139">Remove-AzSqlSyncMember</span></span>](./Remove-AzSqlSyncMember.md)


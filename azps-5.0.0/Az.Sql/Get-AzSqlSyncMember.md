---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncMember.md
ms.openlocfilehash: e5bb853d9dd818801298254eac1f120efcc829a4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245667"
---
# <span data-ttu-id="bb4a2-101">Get-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="bb4a2-101">Get-AzSqlSyncMember</span></span>

## <span data-ttu-id="bb4a2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bb4a2-102">SYNOPSIS</span></span>
<span data-ttu-id="bb4a2-103">Возвращает сведения о членах синхронизации базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="bb4a2-103">Returns information about Azure SQL Database Sync Members.</span></span>

## <span data-ttu-id="bb4a2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bb4a2-104">SYNTAX</span></span>

```
Get-AzSqlSyncMember [-Name <String>] [-SyncGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bb4a2-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bb4a2-105">DESCRIPTION</span></span>
<span data-ttu-id="bb4a2-106">Командлет **Get-AzSqlSyncMember** возвращает сведения об одном или нескольких членах синхронизации базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="bb4a2-106">The **Get-AzSqlSyncMember** cmdlet returns information about one or more Azure SQL Database Sync Members.</span></span>
<span data-ttu-id="bb4a2-107">Укажите имя члена синхронизации, чтобы просмотреть сведения только для этого члена синхронизации.</span><span class="sxs-lookup"><span data-stu-id="bb4a2-107">Specify the name of a sync member to see information for only that sync member.</span></span>

## <span data-ttu-id="bb4a2-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bb4a2-108">EXAMPLES</span></span>

### <span data-ttu-id="bb4a2-109">Пример 1: получение всех экземпляров участника Azure SQL Sync, назначенного группе синхронизации</span><span class="sxs-lookup"><span data-stu-id="bb4a2-109">Example 1: Get all instances of Azure SQL Sync Member assigned to a sync group</span></span>
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

<span data-ttu-id="bb4a2-110">Эта команда получает сведения обо всех членах синхронизации базы данных SQL Azure, назначенных группе синхронизации SyncGroup01.</span><span class="sxs-lookup"><span data-stu-id="bb4a2-110">This command gets information about all the Azure SQL Database Sync Member assigned to the sync group SyncGroup01.</span></span>

### <span data-ttu-id="bb4a2-111">Пример 2: получение сведений об элементе синхронизации базы данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="bb4a2-111">Example 2: Get information about an Azure SQL Database Sync Member</span></span>
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

<span data-ttu-id="bb4a2-112">Эта команда получает сведения о члене синхронизации базы данных SQL Azure с именем "SyncMember01".</span><span class="sxs-lookup"><span data-stu-id="bb4a2-112">This command gets information about the Azure SQL Database Sync Member with name "SyncMember01"</span></span>

### <span data-ttu-id="bb4a2-113">Пример 3: получение всех экземпляров пользователя синхронизации Azure SQL Server, назначенного группе синхронизации с помощью фильтрации</span><span class="sxs-lookup"><span data-stu-id="bb4a2-113">Example 3: Get all instances of Azure SQL Sync Member assigned to a sync group using filtering</span></span>
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

<span data-ttu-id="bb4a2-114">Эта команда получает сведения обо всех членах синхронизации базы данных SQL Azure, назначенных группе синхронизации SyncGroup01, которая начинается с "SyncMember".</span><span class="sxs-lookup"><span data-stu-id="bb4a2-114">This command gets information about all the Azure SQL Database Sync Member assigned to the sync group SyncGroup01 that start with "SyncMember".</span></span>

## <span data-ttu-id="bb4a2-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bb4a2-115">PARAMETERS</span></span>

### <span data-ttu-id="bb4a2-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="bb4a2-116">-DatabaseName</span></span>
<span data-ttu-id="bb4a2-117">Имя базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="bb4a2-117">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="bb4a2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb4a2-118">-DefaultProfile</span></span>
<span data-ttu-id="bb4a2-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="bb4a2-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bb4a2-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="bb4a2-120">-Name</span></span>
<span data-ttu-id="bb4a2-121">Имя элемента синхронизации.</span><span class="sxs-lookup"><span data-stu-id="bb4a2-121">The sync member name.</span></span>

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

### <span data-ttu-id="bb4a2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb4a2-122">-ResourceGroupName</span></span>
<span data-ttu-id="bb4a2-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bb4a2-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="bb4a2-124">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="bb4a2-124">-ServerName</span></span>
<span data-ttu-id="bb4a2-125">Имя сервера Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="bb4a2-125">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="bb4a2-126">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="bb4a2-126">-SyncGroupName</span></span>
<span data-ttu-id="bb4a2-127">Имя группы синхронизации.</span><span class="sxs-lookup"><span data-stu-id="bb4a2-127">The sync group name.</span></span>

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

### <span data-ttu-id="bb4a2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb4a2-128">CommonParameters</span></span>
<span data-ttu-id="bb4a2-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bb4a2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb4a2-130">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bb4a2-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb4a2-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bb4a2-131">INPUTS</span></span>

### <span data-ttu-id="bb4a2-132">System. String</span><span class="sxs-lookup"><span data-stu-id="bb4a2-132">System.String</span></span>

## <span data-ttu-id="bb4a2-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bb4a2-133">OUTPUTS</span></span>

### <span data-ttu-id="bb4a2-134">Microsoft. Azure. Commands. SQL. Sync. Model. AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="bb4a2-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="bb4a2-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="bb4a2-135">NOTES</span></span>

## <span data-ttu-id="bb4a2-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bb4a2-136">RELATED LINKS</span></span>

[<span data-ttu-id="bb4a2-137">New-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="bb4a2-137">New-AzSqlSyncMember</span></span>](./New-AzSqlSyncMember.md)

[<span data-ttu-id="bb4a2-138">Update-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="bb4a2-138">Update-AzSqlSyncMember</span></span>](./Update-AzSqlSyncMember.md)

[<span data-ttu-id="bb4a2-139">Remove-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="bb4a2-139">Remove-AzSqlSyncMember</span></span>](./Remove-AzSqlSyncMember.md)


---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncGroup.md
ms.openlocfilehash: d117ef9685a235528cb91c82a148ff0dddb2d96c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100212508"
---
# <span data-ttu-id="924b3-101">Get-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="924b3-101">Get-AzSqlSyncGroup</span></span>

## <span data-ttu-id="924b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="924b3-102">SYNOPSIS</span></span>
<span data-ttu-id="924b3-103">Возвращает сведения о группах синхронизации баз данных Azure SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="924b3-103">Returns information about Azure SQL Database Sync Groups.</span></span>

## <span data-ttu-id="924b3-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="924b3-104">SYNTAX</span></span>

```
Get-AzSqlSyncGroup [[-Name] <String>] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="924b3-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="924b3-105">DESCRIPTION</span></span>
<span data-ttu-id="924b3-106">Командалет **Get-AzSqlSyncGroup** возвращает сведения об одной или несколько группах синхронизации баз данных Azure SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="924b3-106">The **Get-AzSqlSyncGroup** cmdlet returns information about one or more Azure SQL Database Sync Groups.</span></span>
<span data-ttu-id="924b3-107">Укажите имя группы синхронизации, чтобы увидеть сведения только для этой группы.</span><span class="sxs-lookup"><span data-stu-id="924b3-107">Specify the name of a sync group to see information for only that sync group.</span></span>

## <span data-ttu-id="924b3-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="924b3-108">EXAMPLES</span></span>

### <span data-ttu-id="924b3-109">Пример 1. Все экземпляры группы синхронизации Azure SQL, назначенной базе данных Azure SQL</span><span class="sxs-lookup"><span data-stu-id="924b3-109">Example 1: Get all instances of Azure SQL Sync Group assigned to an Azure SQL Database</span></span>
```
PS C:\>Get-AzSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" | Format-List
ResourceId                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup01
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
IntervalInSeconds           : 100
ConflictResolutionPolicy:   : HubWin
HubDatabaseUserName         : myAccount
HubDatabasePassword         : 
SyncState                   : NotReady
LastSyncTime                : 1/1/0001 12:00:00 AM
Schema                      :  

ResourceId                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup02}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup02
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
IntervalInSeconds           : 100
ConflictResolutionPolicy:   : HubWin
HubDatabaseUserName         : myAccount
HubDatabasePassword         : 
SyncState                   : NotReady
LastSyncTime                : 1/1/0001 12:00:00 AM
Schema                      :
```

<span data-ttu-id="924b3-110">Эта команда получает сведения обо всех группах синхронизации баз данных Azure SQL, которые назначены для базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="924b3-110">This command gets information about all the Azure SQL Database Sync Groups assigned to an Azure SQL Database.</span></span>

### <span data-ttu-id="924b3-111">Пример 2. Сведения о группе синхронизации базы данных Azure SQL</span><span class="sxs-lookup"><span data-stu-id="924b3-111">Example 2: Get information about an Azure SQL Database Sync Group</span></span>
```
PS C:\>Get-AzSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -Name "SyncGroup01" | Format-List
ResourceId                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup02}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup02
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
IntervalInSeconds           : 100
ConflictResolutionPolicy:   : HubWin
HubDatabaseUserName         : myAccount
HubDatabasePassword         : 
SyncState                   : NotReady
LastSyncTime                : 1/1/0001 12:00:00 AM
Schema                      :
```

<span data-ttu-id="924b3-112">Эта команда получает сведения о группе синхронизации базы данных Azure SQL с именем SyncGroup01.</span><span class="sxs-lookup"><span data-stu-id="924b3-112">This command gets information about the Azure SQL Database Sync Group with name "SyncGroup01"</span></span>

### <span data-ttu-id="924b3-113">Пример 3. Все экземпляры группы синхронизации Azure SQL, назначенной базе данных Azure SQL с помощью фильтрации</span><span class="sxs-lookup"><span data-stu-id="924b3-113">Example 3: Get all instances of Azure SQL Sync Group assigned to an Azure SQL Database using filtering</span></span>
```
PS C:\>Get-AzSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -Name "SyncGroup*" | Format-List
ResourceId                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup01
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
IntervalInSeconds           : 100
ConflictResolutionPolicy:   : HubWin
HubDatabaseUserName         : myAccount
HubDatabasePassword         : 
SyncState                   : NotReady
LastSyncTime                : 1/1/0001 12:00:00 AM
Schema                      :  

ResourceId                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup02}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup02
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
IntervalInSeconds           : 100
ConflictResolutionPolicy:   : HubWin
HubDatabaseUserName         : myAccount
HubDatabasePassword         : 
SyncState                   : NotReady
LastSyncTime                : 1/1/0001 12:00:00 AM
Schema                      :
```

<span data-ttu-id="924b3-114">Эта команда получает сведения обо всех группах синхронизации баз данных Azure SQL, которые назначены базе данных Azure SQL, которая начинается с "SyncGroup".</span><span class="sxs-lookup"><span data-stu-id="924b3-114">This command gets information about all the Azure SQL Database Sync Groups assigned to an Azure SQL Database that start with "SyncGroup".</span></span>

## <span data-ttu-id="924b3-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="924b3-115">PARAMETERS</span></span>

### <span data-ttu-id="924b3-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="924b3-116">-DatabaseName</span></span>
<span data-ttu-id="924b3-117">Имя базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="924b3-117">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="924b3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="924b3-118">-DefaultProfile</span></span>
<span data-ttu-id="924b3-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="924b3-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="924b3-120">-Name</span><span class="sxs-lookup"><span data-stu-id="924b3-120">-Name</span></span>
<span data-ttu-id="924b3-121">Имя группы синхронизации.</span><span class="sxs-lookup"><span data-stu-id="924b3-121">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncGroupName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="924b3-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="924b3-122">-ResourceGroupName</span></span>
<span data-ttu-id="924b3-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="924b3-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="924b3-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="924b3-124">-ServerName</span></span>
<span data-ttu-id="924b3-125">Имя службы Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="924b3-125">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="924b3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="924b3-126">CommonParameters</span></span>
<span data-ttu-id="924b3-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="924b3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="924b3-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="924b3-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="924b3-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="924b3-129">INPUTS</span></span>

### <span data-ttu-id="924b3-130">System.String</span><span class="sxs-lookup"><span data-stu-id="924b3-130">System.String</span></span>

## <span data-ttu-id="924b3-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="924b3-131">OUTPUTS</span></span>

### <span data-ttu-id="924b3-132">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="924b3-132">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="924b3-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="924b3-133">NOTES</span></span>

## <span data-ttu-id="924b3-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="924b3-134">RELATED LINKS</span></span>

[<span data-ttu-id="924b3-135">New-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="924b3-135">New-AzSqlSyncGroup</span></span>](./New-AzSqlSyncGroup.md)

[<span data-ttu-id="924b3-136">Update-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="924b3-136">Update-AzSqlSyncGroup</span></span>](./Update-AzSqlSyncGroup.md)

[<span data-ttu-id="924b3-137">Remove-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="924b3-137">Remove-AzSqlSyncGroup</span></span>](./Remove-AzSqlSyncGroup.md)


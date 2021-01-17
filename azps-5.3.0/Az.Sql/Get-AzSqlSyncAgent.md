---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlsyncagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncAgent.md
ms.openlocfilehash: 8bb031ffa2924ce0cace8d2c7daf94be97713eec
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98419228"
---
# <span data-ttu-id="cf276-101">Get-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="cf276-101">Get-AzSqlSyncAgent</span></span>

## <span data-ttu-id="cf276-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cf276-102">SYNOPSIS</span></span>
<span data-ttu-id="cf276-103">Возвращает сведения об агентах синхронизации Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="cf276-103">Returns information about Azure SQL Sync Agents.</span></span>

## <span data-ttu-id="cf276-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="cf276-104">SYNTAX</span></span>

```
Get-AzSqlSyncAgent [[-Name] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cf276-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cf276-105">DESCRIPTION</span></span>
<span data-ttu-id="cf276-106">**Cmdlet Get-AzSqlSyncAgent** возвращает сведения об одном или SQL агентов синхронизации Azure.</span><span class="sxs-lookup"><span data-stu-id="cf276-106">The **Get-AzSqlSyncAgent** cmdlet returns information about one or more Azure SQL Sync Agents.</span></span>
<span data-ttu-id="cf276-107">Укажите имя агента синхронизации, чтобы увидеть сведения только для этого агента.</span><span class="sxs-lookup"><span data-stu-id="cf276-107">Specify the name of a sync agent to see information for only that sync agent.</span></span>

## <span data-ttu-id="cf276-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="cf276-108">EXAMPLES</span></span>

### <span data-ttu-id="cf276-109">Пример 1. Получите все экземпляры агента синхронизации Azure SQL, которые назначены azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="cf276-109">Example 1: Get all instances of Azure SQL Sync Agent assigned to an Azure SQL Server</span></span>
```
PS C:\>Get-AzSqlSyncAgent -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Format-List
ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/syncAgents/{SyncAgent01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncAgentName               : SyncAgent01
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
LastAliveTime:              : 6/1/2017 5:08:48 AM
Version                     : 4.3.6348.1
IsUpToDate                  : False
ExpiryTime                  : 
State                       : Online

ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/syncAgents/{SyncAgent02}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncAgentName               : SyncAgent02
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
LastAliveTime:              : 6/1/2017 5:08:48 AM
Version                     : 4.3.6348.1
IsUpToDate                  : False
ExpiryTime                  : 
State                       : Online
```

<span data-ttu-id="cf276-110">Эта команда получает сведения обо всех агентах синхронизации Azure SQL, которые назначены azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="cf276-110">This command gets information about all the Azure SQL Sync Agents assigned to an Azure SQL Server.</span></span>

### <span data-ttu-id="cf276-111">Пример 2. Сведения об агенте синхронизации Azure SQL Azure</span><span class="sxs-lookup"><span data-stu-id="cf276-111">Example 2: Get information about an Azure SQL Sync Agent</span></span>
```
PS C:\>Get-AzSqlSyncAgent -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -Name "SyncAgent01" | Format-List
ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/syncAgents/{SyncAgent01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncAgentName               : SyncAgent01
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
LastAliveTime:              : 6/1/2017 5:08:48 AM
Version                     : 4.3.6348.1
IsUpToDate                  : False
ExpiryTime                  : 
State                       : Online
```

<span data-ttu-id="cf276-112">Эта команда получает сведения об агенте синхронизации базы данных Azure SQL с именем SyncAgent01.</span><span class="sxs-lookup"><span data-stu-id="cf276-112">This command gets information about the Azure SQL Database Sync Agent with name "SyncAgent01"</span></span>

### <span data-ttu-id="cf276-113">Пример 3. Получите все экземпляры агента синхронизации Azure SQL, которые назначены azure SQL Server с помощью фильтрации</span><span class="sxs-lookup"><span data-stu-id="cf276-113">Example 3: Get all instances of Azure SQL Sync Agent assigned to an Azure SQL Server using filtering</span></span>
```
PS C:\>Get-AzSqlSyncAgent -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -Name SyncAgent* | Format-List
ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/syncAgents/{SyncAgent01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncAgentName               : SyncAgent01
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
LastAliveTime:              : 6/1/2017 5:08:48 AM
Version                     : 4.3.6348.1
IsUpToDate                  : False
ExpiryTime                  : 
State                       : Online

ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/syncAgents/{SyncAgent02}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncAgentName               : SyncAgent02
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
LastAliveTime:              : 6/1/2017 5:08:48 AM
Version                     : 4.3.6348.1
IsUpToDate                  : False
ExpiryTime                  : 
State                       : Online
```

<span data-ttu-id="cf276-114">Эта команда получает сведения обо всех агентах синхронизации Azure SQL, которые назначены azure SQL Server, которые начинаются с "SyncAgent".</span><span class="sxs-lookup"><span data-stu-id="cf276-114">This command gets information about all the Azure SQL Sync Agents assigned to an Azure SQL Server that start with "SyncAgent".</span></span>

## <span data-ttu-id="cf276-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cf276-115">PARAMETERS</span></span>

### <span data-ttu-id="cf276-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf276-116">-DefaultProfile</span></span>
<span data-ttu-id="cf276-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="cf276-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cf276-118">-Name</span><span class="sxs-lookup"><span data-stu-id="cf276-118">-Name</span></span>
<span data-ttu-id="cf276-119">Имя агента синхронизации.</span><span class="sxs-lookup"><span data-stu-id="cf276-119">The sync agent name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncAgentName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf276-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf276-120">-ResourceGroupName</span></span>
<span data-ttu-id="cf276-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cf276-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="cf276-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="cf276-122">-ServerName</span></span>
<span data-ttu-id="cf276-123">Имя Azure SQL Server агент синхронизации.</span><span class="sxs-lookup"><span data-stu-id="cf276-123">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="cf276-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf276-124">CommonParameters</span></span>
<span data-ttu-id="cf276-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf276-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf276-126">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cf276-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf276-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cf276-127">INPUTS</span></span>

### <span data-ttu-id="cf276-128">System.String</span><span class="sxs-lookup"><span data-stu-id="cf276-128">System.String</span></span>

## <span data-ttu-id="cf276-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="cf276-129">OUTPUTS</span></span>

### <span data-ttu-id="cf276-130">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span><span class="sxs-lookup"><span data-stu-id="cf276-130">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span></span>

## <span data-ttu-id="cf276-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="cf276-131">NOTES</span></span>

## <span data-ttu-id="cf276-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cf276-132">RELATED LINKS</span></span>

[<span data-ttu-id="cf276-133">Remove-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="cf276-133">Remove-AzSqlSyncAgent</span></span>](./Remove-AzSqlSyncAgent.md)

[<span data-ttu-id="cf276-134">New-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="cf276-134">New-AzSqlSyncAgent</span></span>](./New-AzSqlSyncAgent.md)


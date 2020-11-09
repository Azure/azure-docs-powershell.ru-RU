---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlsyncagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncAgent.md
ms.openlocfilehash: 8bb031ffa2924ce0cace8d2c7daf94be97713eec
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248164"
---
# <span data-ttu-id="e4fd3-101">Get-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="e4fd3-101">Get-AzSqlSyncAgent</span></span>

## <span data-ttu-id="e4fd3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e4fd3-102">SYNOPSIS</span></span>
<span data-ttu-id="e4fd3-103">Возвращает сведения об агентах синхронизации Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="e4fd3-103">Returns information about Azure SQL Sync Agents.</span></span>

## <span data-ttu-id="e4fd3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e4fd3-104">SYNTAX</span></span>

```
Get-AzSqlSyncAgent [[-Name] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e4fd3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e4fd3-105">DESCRIPTION</span></span>
<span data-ttu-id="e4fd3-106">Командлет **Get-AzSqlSyncAgent** возвращает сведения об одном или нескольких агентах синхронизации Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="e4fd3-106">The **Get-AzSqlSyncAgent** cmdlet returns information about one or more Azure SQL Sync Agents.</span></span>
<span data-ttu-id="e4fd3-107">Укажите имя агента синхронизации, чтобы просмотреть сведения только для этого агента синхронизации.</span><span class="sxs-lookup"><span data-stu-id="e4fd3-107">Specify the name of a sync agent to see information for only that sync agent.</span></span>

## <span data-ttu-id="e4fd3-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e4fd3-108">EXAMPLES</span></span>

### <span data-ttu-id="e4fd3-109">Пример 1: получение всех экземпляров агента синхронизации SQL Azure, назначенного для Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="e4fd3-109">Example 1: Get all instances of Azure SQL Sync Agent assigned to an Azure SQL Server</span></span>
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

<span data-ttu-id="e4fd3-110">Эта команда получает сведения обо всех агентах синхронизации SQL для Azure, назначенных серверу Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="e4fd3-110">This command gets information about all the Azure SQL Sync Agents assigned to an Azure SQL Server.</span></span>

### <span data-ttu-id="e4fd3-111">Пример 2: получение сведений об агенте Azure SQL Sync</span><span class="sxs-lookup"><span data-stu-id="e4fd3-111">Example 2: Get information about an Azure SQL Sync Agent</span></span>
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

<span data-ttu-id="e4fd3-112">Эта команда получает сведения об агенте синхронизации базы данных SQL Azure с именем "SyncAgent01".</span><span class="sxs-lookup"><span data-stu-id="e4fd3-112">This command gets information about the Azure SQL Database Sync Agent with name "SyncAgent01"</span></span>

### <span data-ttu-id="e4fd3-113">Пример 3: получение всех экземпляров агента синхронизации SQL Azure, назначенного серверу Azure SQL Server с помощью фильтрации</span><span class="sxs-lookup"><span data-stu-id="e4fd3-113">Example 3: Get all instances of Azure SQL Sync Agent assigned to an Azure SQL Server using filtering</span></span>
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

<span data-ttu-id="e4fd3-114">Эта команда получает сведения обо всех агентах синхронизации SQL для Azure, назначенных серверу Azure SQL Server, который начинается с "SyncAgent".</span><span class="sxs-lookup"><span data-stu-id="e4fd3-114">This command gets information about all the Azure SQL Sync Agents assigned to an Azure SQL Server that start with "SyncAgent".</span></span>

## <span data-ttu-id="e4fd3-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e4fd3-115">PARAMETERS</span></span>

### <span data-ttu-id="e4fd3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4fd3-116">-DefaultProfile</span></span>
<span data-ttu-id="e4fd3-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="e4fd3-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e4fd3-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e4fd3-118">-Name</span></span>
<span data-ttu-id="e4fd3-119">Имя агента синхронизации.</span><span class="sxs-lookup"><span data-stu-id="e4fd3-119">The sync agent name.</span></span>

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

### <span data-ttu-id="e4fd3-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4fd3-120">-ResourceGroupName</span></span>
<span data-ttu-id="e4fd3-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e4fd3-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="e4fd3-122">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="e4fd3-122">-ServerName</span></span>
<span data-ttu-id="e4fd3-123">Имя сервера Azure SQL Server, в котором находится агент синхронизации.</span><span class="sxs-lookup"><span data-stu-id="e4fd3-123">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="e4fd3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4fd3-124">CommonParameters</span></span>
<span data-ttu-id="e4fd3-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e4fd3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4fd3-126">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e4fd3-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4fd3-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e4fd3-127">INPUTS</span></span>

### <span data-ttu-id="e4fd3-128">System. String</span><span class="sxs-lookup"><span data-stu-id="e4fd3-128">System.String</span></span>

## <span data-ttu-id="e4fd3-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e4fd3-129">OUTPUTS</span></span>

### <span data-ttu-id="e4fd3-130">Microsoft. Azure. Commands. SQL. Sync. Model. AzureSqlSyncAgentModel</span><span class="sxs-lookup"><span data-stu-id="e4fd3-130">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span></span>

## <span data-ttu-id="e4fd3-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="e4fd3-131">NOTES</span></span>

## <span data-ttu-id="e4fd3-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e4fd3-132">RELATED LINKS</span></span>

[<span data-ttu-id="e4fd3-133">Remove-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="e4fd3-133">Remove-AzSqlSyncAgent</span></span>](./Remove-AzSqlSyncAgent.md)

[<span data-ttu-id="e4fd3-134">New-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="e4fd3-134">New-AzSqlSyncAgent</span></span>](./New-AzSqlSyncAgent.md)

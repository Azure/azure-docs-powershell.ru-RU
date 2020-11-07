---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlsyncagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncAgent.md
ms.openlocfilehash: f74a031079ab35e1584d8c7e5536e2605ea665ec
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93728920"
---
# <span data-ttu-id="bfb40-101">Get-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="bfb40-101">Get-AzSqlSyncAgent</span></span>

## <span data-ttu-id="bfb40-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bfb40-102">SYNOPSIS</span></span>
<span data-ttu-id="bfb40-103">Возвращает сведения об агентах синхронизации Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="bfb40-103">Returns information about Azure SQL Sync Agents.</span></span>

## <span data-ttu-id="bfb40-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bfb40-104">SYNTAX</span></span>

```
Get-AzSqlSyncAgent [[-Name] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bfb40-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bfb40-105">DESCRIPTION</span></span>
<span data-ttu-id="bfb40-106">Командлет **Get-AzSqlSyncAgent** возвращает сведения об одном или нескольких агентах синхронизации Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="bfb40-106">The **Get-AzSqlSyncAgent** cmdlet returns information about one or more Azure SQL Sync Agents.</span></span>
<span data-ttu-id="bfb40-107">Укажите имя агента синхронизации, чтобы просмотреть сведения только для этого агента синхронизации.</span><span class="sxs-lookup"><span data-stu-id="bfb40-107">Specify the name of a sync agent to see information for only that sync agent.</span></span>

## <span data-ttu-id="bfb40-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bfb40-108">EXAMPLES</span></span>

### <span data-ttu-id="bfb40-109">Пример 1: получение всех экземпляров агента синхронизации SQL Azure, назначенного для Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="bfb40-109">Example 1: Get all instances of Azure SQL Sync Agent assigned to an Azure SQL Server</span></span>
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

<span data-ttu-id="bfb40-110">Эта команда получает сведения обо всех агентах синхронизации SQL для Azure, назначенных серверу Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="bfb40-110">This command gets information about all the Azure SQL Sync Agents assigned to an Azure SQL Server.</span></span>

### <span data-ttu-id="bfb40-111">Пример 2: получение сведений об агенте Azure SQL Sync</span><span class="sxs-lookup"><span data-stu-id="bfb40-111">Example 2: Get information about an Azure SQL Sync Agent</span></span>
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

<span data-ttu-id="bfb40-112">Эта команда получает сведения об агенте синхронизации базы данных SQL Azure с именем "SyncAgent01".</span><span class="sxs-lookup"><span data-stu-id="bfb40-112">This command gets information about the Azure SQL Database Sync Agent with name "SyncAgent01"</span></span>

### <span data-ttu-id="bfb40-113">Пример 3: получение всех экземпляров агента синхронизации SQL Azure, назначенного серверу Azure SQL Server с помощью фильтрации</span><span class="sxs-lookup"><span data-stu-id="bfb40-113">Example 3: Get all instances of Azure SQL Sync Agent assigned to an Azure SQL Server using filtering</span></span>
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

<span data-ttu-id="bfb40-114">Эта команда получает сведения обо всех агентах синхронизации SQL для Azure, назначенных серверу Azure SQL Server, который начинается с "SyncAgent".</span><span class="sxs-lookup"><span data-stu-id="bfb40-114">This command gets information about all the Azure SQL Sync Agents assigned to an Azure SQL Server that start with "SyncAgent".</span></span>

## <span data-ttu-id="bfb40-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bfb40-115">PARAMETERS</span></span>

### <span data-ttu-id="bfb40-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfb40-116">-DefaultProfile</span></span>
<span data-ttu-id="bfb40-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="bfb40-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bfb40-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="bfb40-118">-Name</span></span>
<span data-ttu-id="bfb40-119">Имя агента синхронизации.</span><span class="sxs-lookup"><span data-stu-id="bfb40-119">The sync agent name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncAgentName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="bfb40-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bfb40-120">-ResourceGroupName</span></span>
<span data-ttu-id="bfb40-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bfb40-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="bfb40-122">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="bfb40-122">-ServerName</span></span>
<span data-ttu-id="bfb40-123">Имя сервера Azure SQL Server, в котором находится агент синхронизации.</span><span class="sxs-lookup"><span data-stu-id="bfb40-123">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="bfb40-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfb40-124">CommonParameters</span></span>
<span data-ttu-id="bfb40-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bfb40-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfb40-126">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bfb40-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfb40-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bfb40-127">INPUTS</span></span>

### <span data-ttu-id="bfb40-128">System. String</span><span class="sxs-lookup"><span data-stu-id="bfb40-128">System.String</span></span>

## <span data-ttu-id="bfb40-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bfb40-129">OUTPUTS</span></span>

### <span data-ttu-id="bfb40-130">Microsoft. Azure. Commands. SQL. Sync. Model. AzureSqlSyncAgentModel</span><span class="sxs-lookup"><span data-stu-id="bfb40-130">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span></span>

## <span data-ttu-id="bfb40-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="bfb40-131">NOTES</span></span>

## <span data-ttu-id="bfb40-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bfb40-132">RELATED LINKS</span></span>

[<span data-ttu-id="bfb40-133">Remove-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="bfb40-133">Remove-AzSqlSyncAgent</span></span>](./Remove-AzSqlSyncAgent.md)

[<span data-ttu-id="bfb40-134">New-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="bfb40-134">New-AzSqlSyncAgent</span></span>](./New-AzSqlSyncAgent.md)


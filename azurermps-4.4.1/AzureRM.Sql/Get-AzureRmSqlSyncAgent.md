---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncAgent.md
ms.openlocfilehash: 5aeb6688f33f9a21cfe20ee91043a8db7bd0313c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559472"
---
# <span data-ttu-id="7fa72-101">Get-AzureRmSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="7fa72-101">Get-AzureRmSqlSyncAgent</span></span>

## <span data-ttu-id="7fa72-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7fa72-102">SYNOPSIS</span></span>
<span data-ttu-id="7fa72-103">Возвращает сведения об агентах синхронизации Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="7fa72-103">Returns information about Azure SQL Sync Agents.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7fa72-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7fa72-104">SYNTAX</span></span>

```
Get-AzureRmSqlSyncAgent [[-Name] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7fa72-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7fa72-105">DESCRIPTION</span></span>
<span data-ttu-id="7fa72-106">Командлет **Get-AzureRmSqlSyncAgent** возвращает сведения об одном или нескольких агентах синхронизации Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="7fa72-106">The **Get-AzureRmSqlSyncAgent** cmdlet returns information about one or more Azure SQL Sync Agents.</span></span>
<span data-ttu-id="7fa72-107">Укажите имя агента синхронизации, чтобы просмотреть сведения только для этого агента синхронизации.</span><span class="sxs-lookup"><span data-stu-id="7fa72-107">Specify the name of a sync agent to see information for only that sync agent.</span></span>

## <span data-ttu-id="7fa72-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7fa72-108">EXAMPLES</span></span>

### <span data-ttu-id="7fa72-109">Пример 1: получение всех экземпляров агента синхронизации SQL Azure, назначенного для Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="7fa72-109">Example 1: Get all instances of Azure SQL Sync Agent assigned to an Azure SQL Server</span></span>
```
PS C:\>Get-AzureRmSqlSyncAgent -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Format-List
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

<span data-ttu-id="7fa72-110">Эта команда получает сведения обо всех агентах синхронизации SQL для Azure, назначенных серверу Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="7fa72-110">This command gets information about all the Azure SQL Sync Agents assigned to an Azure SQL Server.</span></span>

### <span data-ttu-id="7fa72-111">Пример 2: получение сведений об агенте Azure SQL Sync</span><span class="sxs-lookup"><span data-stu-id="7fa72-111">Example 2: Get information about an Azure SQL Sync Agent</span></span>
```
PS C:\>Get-AzureRmSqlSyncAgent -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -Name "SyncAgent01" | Format-List
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

<span data-ttu-id="7fa72-112">Эта команда получает сведения об агенте синхронизации базы данных SQL Azure с именем "SyncAgent01".</span><span class="sxs-lookup"><span data-stu-id="7fa72-112">This command gets information about the Azure SQL Database Sync Agent with name "SyncAgent01"</span></span>

## <span data-ttu-id="7fa72-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7fa72-113">PARAMETERS</span></span>

### <span data-ttu-id="7fa72-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7fa72-114">-Name</span></span>
<span data-ttu-id="7fa72-115">Имя агента синхронизации.</span><span class="sxs-lookup"><span data-stu-id="7fa72-115">The sync agent name.</span></span>

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

### <span data-ttu-id="7fa72-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7fa72-116">-ResourceGroupName</span></span>
<span data-ttu-id="7fa72-117">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7fa72-117">The name of the resource group.</span></span>

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

### <span data-ttu-id="7fa72-118">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="7fa72-118">-ServerName</span></span>
<span data-ttu-id="7fa72-119">Имя сервера Azure SQL Server, в котором находится агент синхронизации.</span><span class="sxs-lookup"><span data-stu-id="7fa72-119">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="7fa72-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fa72-120">-DefaultProfile</span></span>
<span data-ttu-id="7fa72-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7fa72-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fa72-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fa72-122">CommonParameters</span></span>
<span data-ttu-id="7fa72-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7fa72-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fa72-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7fa72-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fa72-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7fa72-125">INPUTS</span></span>

## <span data-ttu-id="7fa72-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7fa72-126">OUTPUTS</span></span>

### <span data-ttu-id="7fa72-127">Microsoft. Azure. Commands. SQL. Sync. Model. AzureSqlSyncAgentModel</span><span class="sxs-lookup"><span data-stu-id="7fa72-127">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span></span>

## <span data-ttu-id="7fa72-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="7fa72-128">NOTES</span></span>

## <span data-ttu-id="7fa72-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7fa72-129">RELATED LINKS</span></span>

[<span data-ttu-id="7fa72-130">Remove-AzureRmSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="7fa72-130">Remove-AzureRmSqlSyncAgent</span></span>](./Remove-AzureRmSqlSyncAgent.md)

[<span data-ttu-id="7fa72-131">New-AzureRmSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="7fa72-131">New-AzureRmSqlSyncAgent</span></span>](./New-AzureRmSqlSyncAgent.md)


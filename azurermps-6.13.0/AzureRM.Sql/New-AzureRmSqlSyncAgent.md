---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlsyncagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlSyncAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlSyncAgent.md
ms.openlocfilehash: 51c3807a6c1e93118eaf84dd51fb62cfe30c1a8b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558219"
---
# <span data-ttu-id="de4f7-101">New-AzureRmSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="de4f7-101">New-AzureRmSqlSyncAgent</span></span>

## <span data-ttu-id="de4f7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="de4f7-102">SYNOPSIS</span></span>
<span data-ttu-id="de4f7-103">Создание агента Azure SQL Sync.</span><span class="sxs-lookup"><span data-stu-id="de4f7-103">Creates an Azure SQL Sync Agent.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="de4f7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="de4f7-104">SYNTAX</span></span>

### <span data-ttu-id="de4f7-105">SyncDatabaseComponent (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="de4f7-105">SyncDatabaseComponent (Default)</span></span>
```
New-AzureRmSqlSyncAgent [-Name] <String> -SyncDatabaseName <String> [-SyncDatabaseServerName <String>]
 [-SyncDatabaseResourceGroupName <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de4f7-106">SyncDatabaseResourceID</span><span class="sxs-lookup"><span data-stu-id="de4f7-106">SyncDatabaseResourceID</span></span>
```
New-AzureRmSqlSyncAgent [-Name] <String> -SyncDatabaseResourceID <String> [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="de4f7-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="de4f7-107">DESCRIPTION</span></span>
<span data-ttu-id="de4f7-108">Командлет **New-AzureRmSqlSyncAgent** создает агент синхронизации Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="de4f7-108">The **New-AzureRmSqlSyncAgent** cmdlet creates an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="de4f7-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="de4f7-109">EXAMPLES</span></span>

### <span data-ttu-id="de4f7-110">Пример 1: создание агента синхронизации для Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="de4f7-110">Example 1: Create a sync agent for an Azure SQL server.</span></span>
```
PS C:\> New-AzureRmSqlSyncAgent -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -Name "SyncAgent01" -SyncDatabaseServerName "syncDatabaseServer01" 
-SyncDatabaseName "syncDatabaseName01" -SyncDatabaseResourceGroupName "syncDatabaseResourceGroup01" | Format-List
ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/syncAgents/{SyncAgent01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncAgentName               : SyncAgent01
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
LastAliveTime:              : 
Version                     : 4.2.0.0
IsUpToDate                  : True
ExpiryTime                  : 12/31/9999 11:59:59 PM
State                       : NeverConnected
```

<span data-ttu-id="de4f7-111">Эта команда создает агент синхронизации для Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="de4f7-111">This command creates a sync agent for an Azure SQL server.</span></span>

## <span data-ttu-id="de4f7-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="de4f7-112">PARAMETERS</span></span>

### <span data-ttu-id="de4f7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de4f7-113">-DefaultProfile</span></span>
<span data-ttu-id="de4f7-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="de4f7-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="de4f7-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="de4f7-115">-Name</span></span>
<span data-ttu-id="de4f7-116">Имя агента синхронизации.</span><span class="sxs-lookup"><span data-stu-id="de4f7-116">The sync agent name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncAgentName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de4f7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de4f7-117">-ResourceGroupName</span></span>
<span data-ttu-id="de4f7-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="de4f7-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="de4f7-119">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="de4f7-119">-ServerName</span></span>
<span data-ttu-id="de4f7-120">Имя сервера Azure SQL Server, в котором находится агент синхронизации.</span><span class="sxs-lookup"><span data-stu-id="de4f7-120">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="de4f7-121">-SyncDatabaseName</span><span class="sxs-lookup"><span data-stu-id="de4f7-121">-SyncDatabaseName</span></span>
<span data-ttu-id="de4f7-122">База данных, которая используется для хранения метаданных, связанных с синхронизацией.</span><span class="sxs-lookup"><span data-stu-id="de4f7-122">The database used to store sync related metadata.</span></span>

```yaml
Type: System.String
Parameter Sets: SyncDatabaseComponent
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de4f7-123">-SyncDatabaseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de4f7-123">-SyncDatabaseResourceGroupName</span></span>
<span data-ttu-id="de4f7-124">Группа ресурсов, к которой принадлежит база данных метаданных синхронизации.</span><span class="sxs-lookup"><span data-stu-id="de4f7-124">The resource group the sync metadata database belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: SyncDatabaseComponent
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de4f7-125">-SyncDatabaseResourceID</span><span class="sxs-lookup"><span data-stu-id="de4f7-125">-SyncDatabaseResourceID</span></span>
<span data-ttu-id="de4f7-126">Идентификатор ресурса для базы данных метаданных синхронизации.</span><span class="sxs-lookup"><span data-stu-id="de4f7-126">The resource ID of  the sync metadata database.</span></span>

```yaml
Type: System.String
Parameter Sets: SyncDatabaseResourceID
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de4f7-127">-SyncDatabaseServerName</span><span class="sxs-lookup"><span data-stu-id="de4f7-127">-SyncDatabaseServerName</span></span>
<span data-ttu-id="de4f7-128">Сервер, на котором размещается база данных метаданных синхронизации.</span><span class="sxs-lookup"><span data-stu-id="de4f7-128">The server on which the sync metadata database is hosted.</span></span>

```yaml
Type: System.String
Parameter Sets: SyncDatabaseComponent
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de4f7-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="de4f7-129">-Confirm</span></span>
<span data-ttu-id="de4f7-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="de4f7-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de4f7-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de4f7-131">-WhatIf</span></span>
<span data-ttu-id="de4f7-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="de4f7-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de4f7-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="de4f7-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de4f7-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de4f7-134">CommonParameters</span></span>
<span data-ttu-id="de4f7-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="de4f7-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de4f7-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de4f7-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de4f7-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="de4f7-137">INPUTS</span></span>

### <span data-ttu-id="de4f7-138">System. String</span><span class="sxs-lookup"><span data-stu-id="de4f7-138">System.String</span></span>

## <span data-ttu-id="de4f7-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="de4f7-139">OUTPUTS</span></span>

### <span data-ttu-id="de4f7-140">Microsoft. Azure. Commands. SQL. Sync. Model. AzureSqlSyncAgentModel</span><span class="sxs-lookup"><span data-stu-id="de4f7-140">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span></span>

## <span data-ttu-id="de4f7-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="de4f7-141">NOTES</span></span>

## <span data-ttu-id="de4f7-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="de4f7-142">RELATED LINKS</span></span>

[<span data-ttu-id="de4f7-143">Remove-AzureRmSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="de4f7-143">Remove-AzureRmSqlSyncAgent</span></span>](./Remove-AzureRmSqlSyncAgent.md)

[<span data-ttu-id="de4f7-144">Get-AzureRmSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="de4f7-144">Get-AzureRmSqlSyncAgent</span></span>](./Get-AzureRmSqlSyncAgent.md)


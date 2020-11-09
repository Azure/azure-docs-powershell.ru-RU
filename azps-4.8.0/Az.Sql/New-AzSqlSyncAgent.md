---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlsyncagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncAgent.md
ms.openlocfilehash: 4a4ce99eb30aaa959eabdc9c1385b567aef2b0fc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243910"
---
# <span data-ttu-id="28d99-101">New-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="28d99-101">New-AzSqlSyncAgent</span></span>

## <span data-ttu-id="28d99-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="28d99-102">SYNOPSIS</span></span>
<span data-ttu-id="28d99-103">Создание агента Azure SQL Sync.</span><span class="sxs-lookup"><span data-stu-id="28d99-103">Creates an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="28d99-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="28d99-104">SYNTAX</span></span>

### <span data-ttu-id="28d99-105">SyncDatabaseComponent (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="28d99-105">SyncDatabaseComponent (Default)</span></span>
```
New-AzSqlSyncAgent [-Name] <String> -SyncDatabaseName <String> [-SyncDatabaseServerName <String>]
 [-SyncDatabaseResourceGroupName <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="28d99-106">SyncDatabaseResourceID</span><span class="sxs-lookup"><span data-stu-id="28d99-106">SyncDatabaseResourceID</span></span>
```
New-AzSqlSyncAgent [-Name] <String> -SyncDatabaseResourceID <String> [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="28d99-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="28d99-107">DESCRIPTION</span></span>
<span data-ttu-id="28d99-108">Командлет **New-AzSqlSyncAgent** создает агент синхронизации Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="28d99-108">The **New-AzSqlSyncAgent** cmdlet creates an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="28d99-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="28d99-109">EXAMPLES</span></span>

### <span data-ttu-id="28d99-110">Пример 1: создание агента синхронизации для Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="28d99-110">Example 1: Create a sync agent for an Azure SQL server.</span></span>
```
PS C:\> New-AzSqlSyncAgent -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -Name "SyncAgent01" -SyncDatabaseServerName "syncDatabaseServer01" 
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

<span data-ttu-id="28d99-111">Эта команда создает агент синхронизации для Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="28d99-111">This command creates a sync agent for an Azure SQL server.</span></span>

## <span data-ttu-id="28d99-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="28d99-112">PARAMETERS</span></span>

### <span data-ttu-id="28d99-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28d99-113">-DefaultProfile</span></span>
<span data-ttu-id="28d99-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="28d99-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="28d99-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="28d99-115">-Name</span></span>
<span data-ttu-id="28d99-116">Имя агента синхронизации.</span><span class="sxs-lookup"><span data-stu-id="28d99-116">The sync agent name.</span></span>

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

### <span data-ttu-id="28d99-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28d99-117">-ResourceGroupName</span></span>
<span data-ttu-id="28d99-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="28d99-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="28d99-119">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="28d99-119">-ServerName</span></span>
<span data-ttu-id="28d99-120">Имя сервера Azure SQL Server, в котором находится агент синхронизации.</span><span class="sxs-lookup"><span data-stu-id="28d99-120">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="28d99-121">-SyncDatabaseName</span><span class="sxs-lookup"><span data-stu-id="28d99-121">-SyncDatabaseName</span></span>
<span data-ttu-id="28d99-122">База данных, которая используется для хранения метаданных, связанных с синхронизацией.</span><span class="sxs-lookup"><span data-stu-id="28d99-122">The database used to store sync related metadata.</span></span>

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

### <span data-ttu-id="28d99-123">-SyncDatabaseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28d99-123">-SyncDatabaseResourceGroupName</span></span>
<span data-ttu-id="28d99-124">Группа ресурсов, к которой принадлежит база данных метаданных синхронизации.</span><span class="sxs-lookup"><span data-stu-id="28d99-124">The resource group the sync metadata database belongs to.</span></span>

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

### <span data-ttu-id="28d99-125">-SyncDatabaseResourceID</span><span class="sxs-lookup"><span data-stu-id="28d99-125">-SyncDatabaseResourceID</span></span>
<span data-ttu-id="28d99-126">Идентификатор ресурса для базы данных метаданных синхронизации.</span><span class="sxs-lookup"><span data-stu-id="28d99-126">The resource ID of  the sync metadata database.</span></span>

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

### <span data-ttu-id="28d99-127">-SyncDatabaseServerName</span><span class="sxs-lookup"><span data-stu-id="28d99-127">-SyncDatabaseServerName</span></span>
<span data-ttu-id="28d99-128">Сервер, на котором размещается база данных метаданных синхронизации.</span><span class="sxs-lookup"><span data-stu-id="28d99-128">The server on which the sync metadata database is hosted.</span></span>

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

### <span data-ttu-id="28d99-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="28d99-129">-Confirm</span></span>
<span data-ttu-id="28d99-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="28d99-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28d99-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28d99-131">-WhatIf</span></span>
<span data-ttu-id="28d99-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="28d99-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28d99-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="28d99-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28d99-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28d99-134">CommonParameters</span></span>
<span data-ttu-id="28d99-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="28d99-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28d99-136">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="28d99-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28d99-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="28d99-137">INPUTS</span></span>

### <span data-ttu-id="28d99-138">System. String</span><span class="sxs-lookup"><span data-stu-id="28d99-138">System.String</span></span>

## <span data-ttu-id="28d99-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="28d99-139">OUTPUTS</span></span>

### <span data-ttu-id="28d99-140">Microsoft. Azure. Commands. SQL. Sync. Model. AzureSqlSyncAgentModel</span><span class="sxs-lookup"><span data-stu-id="28d99-140">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span></span>

## <span data-ttu-id="28d99-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="28d99-141">NOTES</span></span>

## <span data-ttu-id="28d99-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="28d99-142">RELATED LINKS</span></span>

[<span data-ttu-id="28d99-143">Remove-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="28d99-143">Remove-AzSqlSyncAgent</span></span>](./Remove-AzSqlSyncAgent.md)

[<span data-ttu-id="28d99-144">Get-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="28d99-144">Get-AzSqlSyncAgent</span></span>](./Get-AzSqlSyncAgent.md)

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlsyncagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncAgent.md
ms.openlocfilehash: ca3ef83fab80e73d687fd11cde418c9ad43f499e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246980"
---
# <span data-ttu-id="6b6bd-101">Remove-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="6b6bd-101">Remove-AzSqlSyncAgent</span></span>

## <span data-ttu-id="6b6bd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6b6bd-102">SYNOPSIS</span></span>
<span data-ttu-id="6b6bd-103">Удаляет агент Azure SQL Sync.</span><span class="sxs-lookup"><span data-stu-id="6b6bd-103">Removes an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="6b6bd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6b6bd-104">SYNTAX</span></span>

```
Remove-AzSqlSyncAgent [-Name] <String> [-Force] [-PassThru] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6b6bd-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6b6bd-105">DESCRIPTION</span></span>
<span data-ttu-id="6b6bd-106">Командлет **Remove-AzSqlSyncAgent** удаляет агент Azure SQL Sync Agent.</span><span class="sxs-lookup"><span data-stu-id="6b6bd-106">The **Remove-AzSqlSyncAgent** cmdlet removes an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="6b6bd-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6b6bd-107">EXAMPLES</span></span>

### <span data-ttu-id="6b6bd-108">Пример 1: Удаление агента синхронизации</span><span class="sxs-lookup"><span data-stu-id="6b6bd-108">Example 1: Remove a sync agent</span></span>
```
PS C:\>Remove-AzSqlSyncAgent -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -Name "syncAgent01"
```

<span data-ttu-id="6b6bd-109">Эта команда удаляет агент Azure SQL Sync Agent с именем syncAgent01.</span><span class="sxs-lookup"><span data-stu-id="6b6bd-109">This command removes the Azure SQL Sync Agent named syncAgent01.</span></span>

## <span data-ttu-id="6b6bd-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6b6bd-110">PARAMETERS</span></span>

### <span data-ttu-id="6b6bd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b6bd-111">-DefaultProfile</span></span>
<span data-ttu-id="6b6bd-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="6b6bd-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6b6bd-113">-Force</span><span class="sxs-lookup"><span data-stu-id="6b6bd-113">-Force</span></span>
<span data-ttu-id="6b6bd-114">Пропустить предупреждающее сообщение для выполнения действия</span><span class="sxs-lookup"><span data-stu-id="6b6bd-114">Skip confirmation message for performing the action</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b6bd-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6b6bd-115">-Name</span></span>
<span data-ttu-id="6b6bd-116">Имя агента синхронизации.</span><span class="sxs-lookup"><span data-stu-id="6b6bd-116">The sync agent name.</span></span>

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

### <span data-ttu-id="6b6bd-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6b6bd-117">-PassThru</span></span>
<span data-ttu-id="6b6bd-118">Определяет, возвращать ли удаленный агент синхронизации</span><span class="sxs-lookup"><span data-stu-id="6b6bd-118">Defines Whether return the removed sync agent</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b6bd-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b6bd-119">-ResourceGroupName</span></span>
<span data-ttu-id="6b6bd-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6b6bd-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="6b6bd-121">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="6b6bd-121">-ServerName</span></span>
<span data-ttu-id="6b6bd-122">Имя сервера Azure SQL Server, в котором находится агент синхронизации.</span><span class="sxs-lookup"><span data-stu-id="6b6bd-122">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="6b6bd-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6b6bd-123">-Confirm</span></span>
<span data-ttu-id="6b6bd-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6b6bd-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b6bd-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b6bd-125">-WhatIf</span></span>
<span data-ttu-id="6b6bd-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6b6bd-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b6bd-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6b6bd-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b6bd-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b6bd-128">CommonParameters</span></span>
<span data-ttu-id="6b6bd-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6b6bd-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b6bd-130">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6b6bd-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b6bd-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6b6bd-131">INPUTS</span></span>

### <span data-ttu-id="6b6bd-132">System. String</span><span class="sxs-lookup"><span data-stu-id="6b6bd-132">System.String</span></span>

## <span data-ttu-id="6b6bd-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6b6bd-133">OUTPUTS</span></span>

### <span data-ttu-id="6b6bd-134">Microsoft. Azure. Commands. SQL. Sync. Model. AzureSqlSyncAgentModel</span><span class="sxs-lookup"><span data-stu-id="6b6bd-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span></span>

## <span data-ttu-id="6b6bd-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="6b6bd-135">NOTES</span></span>

## <span data-ttu-id="6b6bd-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6b6bd-136">RELATED LINKS</span></span>

[<span data-ttu-id="6b6bd-137">New-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="6b6bd-137">New-AzSqlSyncAgent</span></span>](./New-AzSqlSyncAgent.md)

[<span data-ttu-id="6b6bd-138">Get-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="6b6bd-138">Get-AzSqlSyncAgent</span></span>](./Get-AzSqlSyncAgent.md)

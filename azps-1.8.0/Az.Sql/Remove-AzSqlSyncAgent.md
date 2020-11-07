---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlsyncagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncAgent.md
ms.openlocfilehash: 5adb6d79904b617b0ddbeaae28c9c7860c028fb8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93728820"
---
# <span data-ttu-id="05785-101">Remove-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="05785-101">Remove-AzSqlSyncAgent</span></span>

## <span data-ttu-id="05785-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="05785-102">SYNOPSIS</span></span>
<span data-ttu-id="05785-103">Удаляет агент Azure SQL Sync.</span><span class="sxs-lookup"><span data-stu-id="05785-103">Removes an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="05785-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="05785-104">SYNTAX</span></span>

```
Remove-AzSqlSyncAgent [-Name] <String> [-Force] [-PassThru] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="05785-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="05785-105">DESCRIPTION</span></span>
<span data-ttu-id="05785-106">Командлет **Remove-AzSqlSyncAgent** удаляет агент Azure SQL Sync Agent.</span><span class="sxs-lookup"><span data-stu-id="05785-106">The **Remove-AzSqlSyncAgent** cmdlet removes an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="05785-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="05785-107">EXAMPLES</span></span>

### <span data-ttu-id="05785-108">Пример 1: Удаление агента синхронизации</span><span class="sxs-lookup"><span data-stu-id="05785-108">Example 1: Remove a sync agent</span></span>
```
PS C:\>Remove-AzSqlSyncAgent -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -Name "syncAgent01"
```

<span data-ttu-id="05785-109">Эта команда удаляет агент Azure SQL Sync Agent с именем syncAgent01.</span><span class="sxs-lookup"><span data-stu-id="05785-109">This command removes the Azure SQL Sync Agent named syncAgent01.</span></span>

## <span data-ttu-id="05785-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="05785-110">PARAMETERS</span></span>

### <span data-ttu-id="05785-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05785-111">-DefaultProfile</span></span>
<span data-ttu-id="05785-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="05785-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="05785-113">-Force</span><span class="sxs-lookup"><span data-stu-id="05785-113">-Force</span></span>
<span data-ttu-id="05785-114">Пропустить предупреждающее сообщение для выполнения действия</span><span class="sxs-lookup"><span data-stu-id="05785-114">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="05785-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="05785-115">-Name</span></span>
<span data-ttu-id="05785-116">Имя агента синхронизации.</span><span class="sxs-lookup"><span data-stu-id="05785-116">The sync agent name.</span></span>

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

### <span data-ttu-id="05785-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="05785-117">-PassThru</span></span>
<span data-ttu-id="05785-118">Определяет, возвращать ли удаленный агент синхронизации</span><span class="sxs-lookup"><span data-stu-id="05785-118">Defines Whether return the removed sync agent</span></span>

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

### <span data-ttu-id="05785-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05785-119">-ResourceGroupName</span></span>
<span data-ttu-id="05785-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="05785-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="05785-121">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="05785-121">-ServerName</span></span>
<span data-ttu-id="05785-122">Имя сервера Azure SQL Server, в котором находится агент синхронизации.</span><span class="sxs-lookup"><span data-stu-id="05785-122">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="05785-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="05785-123">-Confirm</span></span>
<span data-ttu-id="05785-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="05785-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05785-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05785-125">-WhatIf</span></span>
<span data-ttu-id="05785-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="05785-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05785-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="05785-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05785-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05785-128">CommonParameters</span></span>
<span data-ttu-id="05785-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="05785-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05785-130">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="05785-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05785-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="05785-131">INPUTS</span></span>

### <span data-ttu-id="05785-132">System. String</span><span class="sxs-lookup"><span data-stu-id="05785-132">System.String</span></span>

## <span data-ttu-id="05785-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="05785-133">OUTPUTS</span></span>

### <span data-ttu-id="05785-134">Microsoft. Azure. Commands. SQL. Sync. Model. AzureSqlSyncAgentModel</span><span class="sxs-lookup"><span data-stu-id="05785-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span></span>

## <span data-ttu-id="05785-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="05785-135">NOTES</span></span>

## <span data-ttu-id="05785-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="05785-136">RELATED LINKS</span></span>

[<span data-ttu-id="05785-137">New-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="05785-137">New-AzSqlSyncAgent</span></span>](./New-AzSqlSyncAgent.md)

[<span data-ttu-id="05785-138">Get-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="05785-138">Get-AzSqlSyncAgent</span></span>](./Get-AzSqlSyncAgent.md)


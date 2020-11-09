---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azscheduledqueryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzScheduledQueryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzScheduledQueryRule.md
ms.openlocfilehash: ea7679b2e3214c55463f9f6fd4ccaf2b22d32841
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249901"
---
# <span data-ttu-id="85159-101">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="85159-101">Remove-AzScheduledQueryRule</span></span>

## <span data-ttu-id="85159-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="85159-102">SYNOPSIS</span></span>
<span data-ttu-id="85159-103">Удаление правила оповещения журнала</span><span class="sxs-lookup"><span data-stu-id="85159-103">Removes a Log Alert Rule</span></span>

## <span data-ttu-id="85159-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="85159-104">SYNTAX</span></span>

### <span data-ttu-id="85159-105">ByRuleName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="85159-105">ByRuleName (Default)</span></span>
```
Remove-AzScheduledQueryRule -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85159-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="85159-106">ByInputObject</span></span>
```
Remove-AzScheduledQueryRule -InputObject <PSScheduledQueryRuleResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85159-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="85159-107">ByResourceId</span></span>
```
Remove-AzScheduledQueryRule -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85159-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="85159-108">DESCRIPTION</span></span>
<span data-ttu-id="85159-109">Удаление правила оповещения журнала</span><span class="sxs-lookup"><span data-stu-id="85159-109">Removes a Log Alert Rule</span></span>

## <span data-ttu-id="85159-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="85159-110">EXAMPLES</span></span>

### <span data-ttu-id="85159-111">Пример 1: удаление по имени правила</span><span class="sxs-lookup"><span data-stu-id="85159-111">Example 1: Remove by rule name</span></span>
```powershell
PS C:\> Remove-AzScheduledQueryRule -ResourceGroupName "MyResourceGroup" -Name "LogAlertRule1"
```

### <span data-ttu-id="85159-112">Пример 2: удаление по объекту ввода</span><span class="sxs-lookup"><span data-stu-id="85159-112">Example 2: Remove by input object</span></span>
```powershell
PS C:\> Remove-AzScheduledQueryRule -InputObject $PSScheduledQueryRuleResource
```

### <span data-ttu-id="85159-113">Пример 3: удаление по идентификатору ресурса</span><span class="sxs-lookup"><span data-stu-id="85159-113">Example 3: Remove by resource Id</span></span>
```powershell
PS C:\> Remove-AzScheduledQueryRule -ResourceId "/subscriptions/b67f7fec-69fc-4974-9099-a26bd6ffeda3/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledQueryRules/LogAlertRule1"
```

## <span data-ttu-id="85159-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="85159-114">PARAMETERS</span></span>

### <span data-ttu-id="85159-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85159-115">-DefaultProfile</span></span>
<span data-ttu-id="85159-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="85159-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85159-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="85159-117">-InputObject</span></span>
<span data-ttu-id="85159-118">Запланированный ресурс правила запроса</span><span class="sxs-lookup"><span data-stu-id="85159-118">The Scheduled Query Rule resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="85159-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="85159-119">-Name</span></span>
<span data-ttu-id="85159-120">Имя оповещения</span><span class="sxs-lookup"><span data-stu-id="85159-120">The alert name</span></span>

```yaml
Type: System.String
Parameter Sets: ByRuleName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85159-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="85159-121">-PassThru</span></span>
<span data-ttu-id="85159-122">Возвращает значение, указывающее на успешное выполнение или сбой.</span><span class="sxs-lookup"><span data-stu-id="85159-122">Return a value indicating success or failure.</span></span>
<span data-ttu-id="85159-123">Этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="85159-123">This cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="85159-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85159-124">-ResourceGroupName</span></span>
<span data-ttu-id="85159-125">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="85159-125">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByRuleName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85159-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="85159-126">-ResourceId</span></span>
<span data-ttu-id="85159-127">Идентификатор ресурса</span><span class="sxs-lookup"><span data-stu-id="85159-127">The resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85159-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="85159-128">-Confirm</span></span>
<span data-ttu-id="85159-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="85159-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85159-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85159-130">-WhatIf</span></span>
<span data-ttu-id="85159-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="85159-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85159-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="85159-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85159-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85159-133">CommonParameters</span></span>
<span data-ttu-id="85159-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="85159-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85159-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="85159-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85159-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="85159-136">INPUTS</span></span>

### <span data-ttu-id="85159-137">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="85159-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

### <span data-ttu-id="85159-138">System. String</span><span class="sxs-lookup"><span data-stu-id="85159-138">System.String</span></span>

## <span data-ttu-id="85159-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="85159-139">OUTPUTS</span></span>

### <span data-ttu-id="85159-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="85159-140">System.Boolean</span></span>

## <span data-ttu-id="85159-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="85159-141">NOTES</span></span>

## <span data-ttu-id="85159-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="85159-142">RELATED LINKS</span></span>
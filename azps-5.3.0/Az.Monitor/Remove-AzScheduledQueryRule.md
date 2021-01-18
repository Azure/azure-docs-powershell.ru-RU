---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azscheduledqueryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzScheduledQueryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzScheduledQueryRule.md
ms.openlocfilehash: ea7679b2e3214c55463f9f6fd4ccaf2b22d32841
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98518209"
---
# <span data-ttu-id="d8caa-101">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="d8caa-101">Remove-AzScheduledQueryRule</span></span>

## <span data-ttu-id="d8caa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8caa-102">SYNOPSIS</span></span>
<span data-ttu-id="d8caa-103">Удаление правила оповещения журнала</span><span class="sxs-lookup"><span data-stu-id="d8caa-103">Removes a Log Alert Rule</span></span>

## <span data-ttu-id="d8caa-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d8caa-104">SYNTAX</span></span>

### <span data-ttu-id="d8caa-105">ByRuleName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d8caa-105">ByRuleName (Default)</span></span>
```
Remove-AzScheduledQueryRule -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8caa-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="d8caa-106">ByInputObject</span></span>
```
Remove-AzScheduledQueryRule -InputObject <PSScheduledQueryRuleResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8caa-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d8caa-107">ByResourceId</span></span>
```
Remove-AzScheduledQueryRule -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8caa-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d8caa-108">DESCRIPTION</span></span>
<span data-ttu-id="d8caa-109">Удаление правила оповещения журнала</span><span class="sxs-lookup"><span data-stu-id="d8caa-109">Removes a Log Alert Rule</span></span>

## <span data-ttu-id="d8caa-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d8caa-110">EXAMPLES</span></span>

### <span data-ttu-id="d8caa-111">Пример 1. Удаление по имени правила</span><span class="sxs-lookup"><span data-stu-id="d8caa-111">Example 1: Remove by rule name</span></span>
```powershell
PS C:\> Remove-AzScheduledQueryRule -ResourceGroupName "MyResourceGroup" -Name "LogAlertRule1"
```

### <span data-ttu-id="d8caa-112">Пример 2. Удаление объекта ввода</span><span class="sxs-lookup"><span data-stu-id="d8caa-112">Example 2: Remove by input object</span></span>
```powershell
PS C:\> Remove-AzScheduledQueryRule -InputObject $PSScheduledQueryRuleResource
```

### <span data-ttu-id="d8caa-113">Пример 3. Удаление по ИД ресурса</span><span class="sxs-lookup"><span data-stu-id="d8caa-113">Example 3: Remove by resource Id</span></span>
```powershell
PS C:\> Remove-AzScheduledQueryRule -ResourceId "/subscriptions/b67f7fec-69fc-4974-9099-a26bd6ffeda3/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledQueryRules/LogAlertRule1"
```

## <span data-ttu-id="d8caa-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d8caa-114">PARAMETERS</span></span>

### <span data-ttu-id="d8caa-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8caa-115">-DefaultProfile</span></span>
<span data-ttu-id="d8caa-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d8caa-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8caa-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d8caa-117">-InputObject</span></span>
<span data-ttu-id="d8caa-118">Ресурс "Правило запланированного запроса"</span><span class="sxs-lookup"><span data-stu-id="d8caa-118">The Scheduled Query Rule resource</span></span>

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

### <span data-ttu-id="d8caa-119">-Name</span><span class="sxs-lookup"><span data-stu-id="d8caa-119">-Name</span></span>
<span data-ttu-id="d8caa-120">Имя оповещения</span><span class="sxs-lookup"><span data-stu-id="d8caa-120">The alert name</span></span>

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

### <span data-ttu-id="d8caa-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d8caa-121">-PassThru</span></span>
<span data-ttu-id="d8caa-122">Возвращает значение, указывающее на успех или неудачу.</span><span class="sxs-lookup"><span data-stu-id="d8caa-122">Return a value indicating success or failure.</span></span>
<span data-ttu-id="d8caa-123">Этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="d8caa-123">This cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d8caa-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8caa-124">-ResourceGroupName</span></span>
<span data-ttu-id="d8caa-125">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="d8caa-125">The resource group name</span></span>

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

### <span data-ttu-id="d8caa-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d8caa-126">-ResourceId</span></span>
<span data-ttu-id="d8caa-127">ИД ресурса</span><span class="sxs-lookup"><span data-stu-id="d8caa-127">The resource Id</span></span>

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

### <span data-ttu-id="d8caa-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d8caa-128">-Confirm</span></span>
<span data-ttu-id="d8caa-129">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d8caa-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8caa-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8caa-130">-WhatIf</span></span>
<span data-ttu-id="d8caa-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d8caa-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8caa-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d8caa-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8caa-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8caa-133">CommonParameters</span></span>
<span data-ttu-id="d8caa-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8caa-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8caa-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d8caa-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8caa-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d8caa-136">INPUTS</span></span>

### <span data-ttu-id="d8caa-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="d8caa-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

### <span data-ttu-id="d8caa-138">System.String</span><span class="sxs-lookup"><span data-stu-id="d8caa-138">System.String</span></span>

## <span data-ttu-id="d8caa-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d8caa-139">OUTPUTS</span></span>

### <span data-ttu-id="d8caa-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d8caa-140">System.Boolean</span></span>

## <span data-ttu-id="d8caa-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d8caa-141">NOTES</span></span>

## <span data-ttu-id="d8caa-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d8caa-142">RELATED LINKS</span></span>

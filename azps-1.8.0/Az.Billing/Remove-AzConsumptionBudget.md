---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/remove-azconsumptionbudget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Remove-AzConsumptionBudget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Remove-AzConsumptionBudget.md
ms.openlocfilehash: 138d9d7510331a385246c99e57ce3f460899ad33
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93901486"
---
# <span data-ttu-id="c8bb0-101">Remove-AzConsumptionBudget</span><span class="sxs-lookup"><span data-stu-id="c8bb0-101">Remove-AzConsumptionBudget</span></span>

## <span data-ttu-id="c8bb0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c8bb0-102">SYNOPSIS</span></span>
<span data-ttu-id="c8bb0-103">Удаление бюджета либо в подписке, либо в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c8bb0-103">Remove a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="c8bb0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c8bb0-104">SYNTAX</span></span>

### <span data-ttu-id="c8bb0-105">Подписка (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c8bb0-105">Subscription (Default)</span></span>
```
Remove-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String>
 [-ResourceGroupName <String>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8bb0-106">Трубодержателей</span><span class="sxs-lookup"><span data-stu-id="c8bb0-106">Piping</span></span>
```
Remove-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -InputObject <PSBudget> [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8bb0-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c8bb0-107">DESCRIPTION</span></span>
<span data-ttu-id="c8bb0-108">Командлет Remove-AzConsumptionBudget удаляет бюджет либо в подписке, либо в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c8bb0-108">The Remove-AzConsumptionBudget cmdlet removes a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="c8bb0-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c8bb0-109">EXAMPLES</span></span>

### <span data-ttu-id="c8bb0-110">Пример 1: удаление бюджета с именем бюджета на уровне подписки</span><span class="sxs-lookup"><span data-stu-id="c8bb0-110">Example 1: Remove a budget with a budget name at subscription level</span></span>
```powershell
PS C:\> Remove-AzConsumptionBudget -Name PSBudget -PassThru
True
```

### <span data-ttu-id="c8bb0-111">Пример 2: удаление бюджета с именем бюджета на уровне группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="c8bb0-111">Example 2: Remove a budget with a budget name at resource group level</span></span>
```powershell
PS C:\> Remove-AzConsumptionBudget -ResourceGroupName RGBudgets -Name PSBudgetRG -PassThru
True
```

### <span data-ttu-id="c8bb0-112">Пример 3: удаление бюджета с помощью трубопроводов на уровне подписки</span><span class="sxs-lookup"><span data-stu-id="c8bb0-112">Example 3: Remove a budget through piping at subscription level</span></span>
```powershell
PS C:\> Get-AzConsumptionBudget -Name PSBudget | Remove-AzConsumptionBudget -PassThru
True
```

## <span data-ttu-id="c8bb0-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c8bb0-113">PARAMETERS</span></span>

### <span data-ttu-id="c8bb0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8bb0-114">-DefaultProfile</span></span>
<span data-ttu-id="c8bb0-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c8bb0-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8bb0-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c8bb0-116">-InputObject</span></span>
<span data-ttu-id="c8bb0-117">Объект бюджета.</span><span class="sxs-lookup"><span data-stu-id="c8bb0-117">Budget object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Consumption.Models.PSBudget
Parameter Sets: Piping
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c8bb0-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c8bb0-118">-Name</span></span>
<span data-ttu-id="c8bb0-119">Название бюджета.</span><span class="sxs-lookup"><span data-stu-id="c8bb0-119">Name of a budget.</span></span>

```yaml
Type: System.String
Parameter Sets: Subscription
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8bb0-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c8bb0-120">-PassThru</span></span>
<span data-ttu-id="c8bb0-121">Командлет возвращает значение true, если бюджет был успешно удален.</span><span class="sxs-lookup"><span data-stu-id="c8bb0-121">The Cmdlet returns true if a budget was successfully removed.</span></span>

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

### <span data-ttu-id="c8bb0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8bb0-122">-ResourceGroupName</span></span>
<span data-ttu-id="c8bb0-123">Группа ресурсов бюджета.</span><span class="sxs-lookup"><span data-stu-id="c8bb0-123">Resource Group of a budget.</span></span>

```yaml
Type: System.String
Parameter Sets: Subscription
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8bb0-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c8bb0-124">-Confirm</span></span>
<span data-ttu-id="c8bb0-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c8bb0-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8bb0-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8bb0-126">-WhatIf</span></span>
<span data-ttu-id="c8bb0-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c8bb0-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8bb0-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c8bb0-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8bb0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8bb0-129">CommonParameters</span></span>
<span data-ttu-id="c8bb0-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c8bb0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8bb0-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8bb0-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8bb0-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c8bb0-132">INPUTS</span></span>

### <span data-ttu-id="c8bb0-133">Microsoft. Azure. Commands. потребление. Models. PSBudget</span><span class="sxs-lookup"><span data-stu-id="c8bb0-133">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>

## <span data-ttu-id="c8bb0-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c8bb0-134">OUTPUTS</span></span>

### <span data-ttu-id="c8bb0-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c8bb0-135">System.Boolean</span></span>

## <span data-ttu-id="c8bb0-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="c8bb0-136">NOTES</span></span>

## <span data-ttu-id="c8bb0-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c8bb0-137">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/remove-azconsumptionbudget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Remove-AzConsumptionBudget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Remove-AzConsumptionBudget.md
ms.openlocfilehash: b3ee807f1ae5b1af46fe2369f74da7e13f1882e6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078490"
---
# <span data-ttu-id="64e47-101">Remove-AzConsumptionBudget</span><span class="sxs-lookup"><span data-stu-id="64e47-101">Remove-AzConsumptionBudget</span></span>

## <span data-ttu-id="64e47-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="64e47-102">SYNOPSIS</span></span>
<span data-ttu-id="64e47-103">Удаление бюджета либо в подписке, либо в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="64e47-103">Remove a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="64e47-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="64e47-104">SYNTAX</span></span>

### <span data-ttu-id="64e47-105">Подписка (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="64e47-105">Subscription (Default)</span></span>
```
Remove-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String>
 [-ResourceGroupName <String>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64e47-106">Трубодержателей</span><span class="sxs-lookup"><span data-stu-id="64e47-106">Piping</span></span>
```
Remove-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -InputObject <PSBudget> [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64e47-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="64e47-107">DESCRIPTION</span></span>
<span data-ttu-id="64e47-108">Командлет Remove-AzConsumptionBudget удаляет бюджет либо в подписке, либо в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="64e47-108">The Remove-AzConsumptionBudget cmdlet removes a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="64e47-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="64e47-109">EXAMPLES</span></span>

### <span data-ttu-id="64e47-110">Пример 1: удаление бюджета с именем бюджета на уровне подписки</span><span class="sxs-lookup"><span data-stu-id="64e47-110">Example 1: Remove a budget with a budget name at subscription level</span></span>
```powershell
PS C:\> Remove-AzConsumptionBudget -Name PSBudget -PassThru
True
```

### <span data-ttu-id="64e47-111">Пример 2: удаление бюджета с именем бюджета на уровне группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="64e47-111">Example 2: Remove a budget with a budget name at resource group level</span></span>
```powershell
PS C:\> Remove-AzConsumptionBudget -ResourceGroupName RGBudgets -Name PSBudgetRG -PassThru
True
```

### <span data-ttu-id="64e47-112">Пример 3: удаление бюджета с помощью трубопроводов на уровне подписки</span><span class="sxs-lookup"><span data-stu-id="64e47-112">Example 3: Remove a budget through piping at subscription level</span></span>
```powershell
PS C:\> Get-AzConsumptionBudget -Name PSBudget | Remove-AzConsumptionBudget -PassThru
True
```

## <span data-ttu-id="64e47-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="64e47-113">PARAMETERS</span></span>

### <span data-ttu-id="64e47-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64e47-114">-DefaultProfile</span></span>
<span data-ttu-id="64e47-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="64e47-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="64e47-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="64e47-116">-InputObject</span></span>
<span data-ttu-id="64e47-117">Объект бюджета.</span><span class="sxs-lookup"><span data-stu-id="64e47-117">Budget object.</span></span>

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

### <span data-ttu-id="64e47-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="64e47-118">-Name</span></span>
<span data-ttu-id="64e47-119">Название бюджета.</span><span class="sxs-lookup"><span data-stu-id="64e47-119">Name of a budget.</span></span>

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

### <span data-ttu-id="64e47-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="64e47-120">-PassThru</span></span>
<span data-ttu-id="64e47-121">Командлет возвращает значение true, если бюджет был успешно удален.</span><span class="sxs-lookup"><span data-stu-id="64e47-121">The Cmdlet returns true if a budget was successfully removed.</span></span>

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

### <span data-ttu-id="64e47-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64e47-122">-ResourceGroupName</span></span>
<span data-ttu-id="64e47-123">Группа ресурсов бюджета.</span><span class="sxs-lookup"><span data-stu-id="64e47-123">Resource Group of a budget.</span></span>

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

### <span data-ttu-id="64e47-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="64e47-124">-Confirm</span></span>
<span data-ttu-id="64e47-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="64e47-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64e47-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64e47-126">-WhatIf</span></span>
<span data-ttu-id="64e47-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="64e47-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64e47-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="64e47-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64e47-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64e47-129">CommonParameters</span></span>
<span data-ttu-id="64e47-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="64e47-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64e47-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64e47-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64e47-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="64e47-132">INPUTS</span></span>

### <span data-ttu-id="64e47-133">Microsoft. Azure. Commands. потребление. Models. PSBudget</span><span class="sxs-lookup"><span data-stu-id="64e47-133">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>

## <span data-ttu-id="64e47-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="64e47-134">OUTPUTS</span></span>

### <span data-ttu-id="64e47-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="64e47-135">System.Boolean</span></span>

## <span data-ttu-id="64e47-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="64e47-136">NOTES</span></span>

## <span data-ttu-id="64e47-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="64e47-137">RELATED LINKS</span></span>

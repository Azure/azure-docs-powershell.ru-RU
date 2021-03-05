---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/powershell/module/az.billing/remove-azconsumptionbudget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Remove-AzConsumptionBudget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Remove-AzConsumptionBudget.md
ms.openlocfilehash: 58a4b7be314489a847479692a08f495fcf4c7146
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983427"
---
# <span data-ttu-id="fcb3a-101">Remove-AzConsumptionBudget</span><span class="sxs-lookup"><span data-stu-id="fcb3a-101">Remove-AzConsumptionBudget</span></span>

## <span data-ttu-id="fcb3a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fcb3a-102">SYNOPSIS</span></span>
<span data-ttu-id="fcb3a-103">Удалить бюджет из подписки или группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fcb3a-103">Remove a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="fcb3a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="fcb3a-104">SYNTAX</span></span>

### <span data-ttu-id="fcb3a-105">Подписка (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fcb3a-105">Subscription (Default)</span></span>
```
Remove-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String>
 [-ResourceGroupName <String>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fcb3a-106">Piping</span><span class="sxs-lookup"><span data-stu-id="fcb3a-106">Piping</span></span>
```
Remove-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -InputObject <PSBudget> [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fcb3a-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fcb3a-107">DESCRIPTION</span></span>
<span data-ttu-id="fcb3a-108">С Remove-AzConsumptionBudget или группы ресурсов удаляется бюджет.</span><span class="sxs-lookup"><span data-stu-id="fcb3a-108">The Remove-AzConsumptionBudget cmdlet removes a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="fcb3a-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="fcb3a-109">EXAMPLES</span></span>

### <span data-ttu-id="fcb3a-110">Пример 1. Удаление бюджета с названием бюджета на уровне подписки</span><span class="sxs-lookup"><span data-stu-id="fcb3a-110">Example 1: Remove a budget with a budget name at subscription level</span></span>
```powershell
PS C:\> Remove-AzConsumptionBudget -Name PSBudget -PassThru
True
```

### <span data-ttu-id="fcb3a-111">Пример 2. Удаление бюджета с названием бюджета на уровне группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="fcb3a-111">Example 2: Remove a budget with a budget name at resource group level</span></span>
```powershell
PS C:\> Remove-AzConsumptionBudget -ResourceGroupName RGBudgets -Name PSBudgetRG -PassThru
True
```

### <span data-ttu-id="fcb3a-112">Пример 3. Удаление бюджета с помощью piping на уровне подписки</span><span class="sxs-lookup"><span data-stu-id="fcb3a-112">Example 3: Remove a budget through piping at subscription level</span></span>
```powershell
PS C:\> Get-AzConsumptionBudget -Name PSBudget | Remove-AzConsumptionBudget -PassThru
True
```

## <span data-ttu-id="fcb3a-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fcb3a-113">PARAMETERS</span></span>

### <span data-ttu-id="fcb3a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcb3a-114">-DefaultProfile</span></span>
<span data-ttu-id="fcb3a-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fcb3a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fcb3a-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fcb3a-116">-InputObject</span></span>
<span data-ttu-id="fcb3a-117">Объект «Бюджет».</span><span class="sxs-lookup"><span data-stu-id="fcb3a-117">Budget object.</span></span>

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

### <span data-ttu-id="fcb3a-118">-Name</span><span class="sxs-lookup"><span data-stu-id="fcb3a-118">-Name</span></span>
<span data-ttu-id="fcb3a-119">Имя бюджета.</span><span class="sxs-lookup"><span data-stu-id="fcb3a-119">Name of a budget.</span></span>

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

### <span data-ttu-id="fcb3a-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fcb3a-120">-PassThru</span></span>
<span data-ttu-id="fcb3a-121">Если бюджет успешно удален, возвращается истина.</span><span class="sxs-lookup"><span data-stu-id="fcb3a-121">The Cmdlet returns true if a budget was successfully removed.</span></span>

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

### <span data-ttu-id="fcb3a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fcb3a-122">-ResourceGroupName</span></span>
<span data-ttu-id="fcb3a-123">Группа ресурсов бюджета.</span><span class="sxs-lookup"><span data-stu-id="fcb3a-123">Resource Group of a budget.</span></span>

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

### <span data-ttu-id="fcb3a-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fcb3a-124">-Confirm</span></span>
<span data-ttu-id="fcb3a-125">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="fcb3a-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fcb3a-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fcb3a-126">-WhatIf</span></span>
<span data-ttu-id="fcb3a-127">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fcb3a-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fcb3a-128">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="fcb3a-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fcb3a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcb3a-129">CommonParameters</span></span>
<span data-ttu-id="fcb3a-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fcb3a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcb3a-131">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fcb3a-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcb3a-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fcb3a-132">INPUTS</span></span>

### <span data-ttu-id="fcb3a-133">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span><span class="sxs-lookup"><span data-stu-id="fcb3a-133">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>

## <span data-ttu-id="fcb3a-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="fcb3a-134">OUTPUTS</span></span>

### <span data-ttu-id="fcb3a-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fcb3a-135">System.Boolean</span></span>

## <span data-ttu-id="fcb3a-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="fcb3a-136">NOTES</span></span>

## <span data-ttu-id="fcb3a-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fcb3a-137">RELATED LINKS</span></span>

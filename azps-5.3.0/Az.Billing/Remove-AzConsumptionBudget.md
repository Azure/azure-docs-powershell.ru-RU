---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/remove-azconsumptionbudget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Remove-AzConsumptionBudget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Remove-AzConsumptionBudget.md
ms.openlocfilehash: b3ee807f1ae5b1af46fe2369f74da7e13f1882e6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98519767"
---
# <span data-ttu-id="62127-101">Remove-AzConsumptionBudget</span><span class="sxs-lookup"><span data-stu-id="62127-101">Remove-AzConsumptionBudget</span></span>

## <span data-ttu-id="62127-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62127-102">SYNOPSIS</span></span>
<span data-ttu-id="62127-103">Удалить бюджет из подписки или группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="62127-103">Remove a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="62127-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="62127-104">SYNTAX</span></span>

### <span data-ttu-id="62127-105">Подписка (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="62127-105">Subscription (Default)</span></span>
```
Remove-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String>
 [-ResourceGroupName <String>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62127-106">Piping</span><span class="sxs-lookup"><span data-stu-id="62127-106">Piping</span></span>
```
Remove-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -InputObject <PSBudget> [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62127-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="62127-107">DESCRIPTION</span></span>
<span data-ttu-id="62127-108">С Remove-AzConsumptionBudget или группы ресурсов удаляется бюджет.</span><span class="sxs-lookup"><span data-stu-id="62127-108">The Remove-AzConsumptionBudget cmdlet removes a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="62127-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="62127-109">EXAMPLES</span></span>

### <span data-ttu-id="62127-110">Пример 1. Удаление бюджета с названием бюджета на уровне подписки</span><span class="sxs-lookup"><span data-stu-id="62127-110">Example 1: Remove a budget with a budget name at subscription level</span></span>
```powershell
PS C:\> Remove-AzConsumptionBudget -Name PSBudget -PassThru
True
```

### <span data-ttu-id="62127-111">Пример 2. Удаление бюджета с названием бюджета на уровне группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="62127-111">Example 2: Remove a budget with a budget name at resource group level</span></span>
```powershell
PS C:\> Remove-AzConsumptionBudget -ResourceGroupName RGBudgets -Name PSBudgetRG -PassThru
True
```

### <span data-ttu-id="62127-112">Пример 3. Удаление бюджета с помощью piping на уровне подписки</span><span class="sxs-lookup"><span data-stu-id="62127-112">Example 3: Remove a budget through piping at subscription level</span></span>
```powershell
PS C:\> Get-AzConsumptionBudget -Name PSBudget | Remove-AzConsumptionBudget -PassThru
True
```

## <span data-ttu-id="62127-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="62127-113">PARAMETERS</span></span>

### <span data-ttu-id="62127-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62127-114">-DefaultProfile</span></span>
<span data-ttu-id="62127-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="62127-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62127-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="62127-116">-InputObject</span></span>
<span data-ttu-id="62127-117">Объект «Бюджет».</span><span class="sxs-lookup"><span data-stu-id="62127-117">Budget object.</span></span>

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

### <span data-ttu-id="62127-118">-Name</span><span class="sxs-lookup"><span data-stu-id="62127-118">-Name</span></span>
<span data-ttu-id="62127-119">Имя бюджета.</span><span class="sxs-lookup"><span data-stu-id="62127-119">Name of a budget.</span></span>

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

### <span data-ttu-id="62127-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="62127-120">-PassThru</span></span>
<span data-ttu-id="62127-121">Если бюджет успешно удален, возвращается истина.</span><span class="sxs-lookup"><span data-stu-id="62127-121">The Cmdlet returns true if a budget was successfully removed.</span></span>

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

### <span data-ttu-id="62127-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62127-122">-ResourceGroupName</span></span>
<span data-ttu-id="62127-123">Группа ресурсов бюджета.</span><span class="sxs-lookup"><span data-stu-id="62127-123">Resource Group of a budget.</span></span>

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

### <span data-ttu-id="62127-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="62127-124">-Confirm</span></span>
<span data-ttu-id="62127-125">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="62127-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62127-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62127-126">-WhatIf</span></span>
<span data-ttu-id="62127-127">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="62127-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62127-128">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="62127-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62127-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62127-129">CommonParameters</span></span>
<span data-ttu-id="62127-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62127-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62127-131">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62127-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62127-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="62127-132">INPUTS</span></span>

### <span data-ttu-id="62127-133">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span><span class="sxs-lookup"><span data-stu-id="62127-133">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>

## <span data-ttu-id="62127-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="62127-134">OUTPUTS</span></span>

### <span data-ttu-id="62127-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="62127-135">System.Boolean</span></span>

## <span data-ttu-id="62127-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="62127-136">NOTES</span></span>

## <span data-ttu-id="62127-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="62127-137">RELATED LINKS</span></span>

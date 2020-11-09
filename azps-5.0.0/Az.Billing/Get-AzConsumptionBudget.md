---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azconsumptionbudget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionBudget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionBudget.md
ms.openlocfilehash: dfca3033b5061116882eb68eb18fa2ff3ddd0c53
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248422"
---
# <span data-ttu-id="bc30d-101">Get-AzConsumptionBudget</span><span class="sxs-lookup"><span data-stu-id="bc30d-101">Get-AzConsumptionBudget</span></span>

## <span data-ttu-id="bc30d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bc30d-102">SYNOPSIS</span></span>
<span data-ttu-id="bc30d-103">Получение списка бюджетов либо в подписке, либо в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bc30d-103">Get a list of budgets in either a subscription or a resource group.</span></span>

## <span data-ttu-id="bc30d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bc30d-104">SYNTAX</span></span>

```
Get-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] [-ResourceGroupName <String>]
 [-Name <String>] [<CommonParameters>]
```

## <span data-ttu-id="bc30d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bc30d-105">DESCRIPTION</span></span>
<span data-ttu-id="bc30d-106">Командлет Get-AzConsumptionBudget возвращает список бюджетов либо в подписке, либо в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bc30d-106">The Get-AzConsumptionBudget cmdlet gets a list of budgets in either a subscription or a resource group.</span></span>

## <span data-ttu-id="bc30d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bc30d-107">EXAMPLES</span></span>

### <span data-ttu-id="bc30d-108">Пример 1: получение списка бюджетов на уровне подписки</span><span class="sxs-lookup"><span data-stu-id="bc30d-108">Example 1: Get a list of budgets at subscription level</span></span>
```powershell
PS C:\> Get-AzConsumptionBudget
Amount:  60     
Category:  Cost
CurrentSpend:  null
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Consumption/budgets/PSBudget
Name:  PSBudget
TimeGrain:  Monthly
TimePeriod:  EndDate:  11/1/2018 12:00:00 AM
             StartDate:  6/1/2018 12:00:00 AM
Type:  Microsoft.Consumption/budgets
```

### <span data-ttu-id="bc30d-109">Пример 2: получение списка бюджетов на уровне группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="bc30d-109">Example 2: Get a list of budgets at resource group level</span></span>
```powershell
PS C:\> Get-AzConsumptionBudget -ResourceGroupName RGBudgets
Amount:  60     
Category:  Cost
CurrentSpend:  null
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/resourceGroups/RGBudgets/providers/Microsoft.Consumption/budgets/PSBudgetRG
Name:  PSBudgetRG
TimeGrain:  Monthly
TimePeriod:  EndDate:  11/1/2018 12:00:00 AM
             StartDate:  6/1/2018 12:00:00 AM
Type:  Microsoft.Consumption/budgets
```

### <span data-ttu-id="bc30d-110">Пример 3: получение бюджета с использованием названия бюджета на уровне подписки</span><span class="sxs-lookup"><span data-stu-id="bc30d-110">Example 3: Get a budget with the budget name at subscription level</span></span>
```powershell
PS C:\> Get-AzConsumptionBudget -Name PSBudget
Amount:  60     
Category:  Cost
CurrentSpend:  null
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Consumption/budgets/PSBudget
Name:  PSBudget
TimeGrain:  Monthly
TimePeriod:  EndDate:  11/1/2018 12:00:00 AM
             StartDate:  6/1/2018 12:00:00 AM
Type:  Microsoft.Consumption/budgets
```

### <span data-ttu-id="bc30d-111">Пример 4: получение бюджета с использованием названия бюджета на уровне группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="bc30d-111">Example 4: Get a budget with the budget name at resource group level</span></span>
```powershell
PS C:\> Get-AzConsumptionBudget -ResourceGroupName RGBudgets -Name PSBudgetRG
Amount:  60     
Category:  Cost
CurrentSpend:  null
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/resourceGroups/RGBudgets/providers/Microsoft.Consumption/budgets/PSBudgetRG
Name:  PSBudgetRG
TimeGrain:  Monthly
TimePeriod:  EndDate:  11/1/2018 12:00:00 AM
             StartDate:  6/1/2018 12:00:00 AM
Type:  Microsoft.Consumption/budgets
```

## <span data-ttu-id="bc30d-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bc30d-112">PARAMETERS</span></span>

### <span data-ttu-id="bc30d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc30d-113">-DefaultProfile</span></span>
<span data-ttu-id="bc30d-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bc30d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bc30d-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="bc30d-115">-Name</span></span>
<span data-ttu-id="bc30d-116">Название бюджета.</span><span class="sxs-lookup"><span data-stu-id="bc30d-116">Name of a budget.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc30d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc30d-117">-ResourceGroupName</span></span>
<span data-ttu-id="bc30d-118">Группа ресурсов бюджета.</span><span class="sxs-lookup"><span data-stu-id="bc30d-118">Resource Group of a budget.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc30d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc30d-119">CommonParameters</span></span>
<span data-ttu-id="bc30d-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bc30d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc30d-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc30d-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc30d-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bc30d-122">INPUTS</span></span>

### <span data-ttu-id="bc30d-123">Ничего</span><span class="sxs-lookup"><span data-stu-id="bc30d-123">None</span></span>

## <span data-ttu-id="bc30d-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bc30d-124">OUTPUTS</span></span>

### <span data-ttu-id="bc30d-125">Microsoft. Azure. Commands. потребление. Models. PSBudget</span><span class="sxs-lookup"><span data-stu-id="bc30d-125">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>

## <span data-ttu-id="bc30d-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="bc30d-126">NOTES</span></span>

## <span data-ttu-id="bc30d-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bc30d-127">RELATED LINKS</span></span>
---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/powershell/module/az.billing/get-azconsumptionbudget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionBudget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionBudget.md
ms.openlocfilehash: 70f7f9c43612f1fd1248e019d970d157fadab000
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986208"
---
# <span data-ttu-id="600ec-101">Get-AzConsumptionBudget</span><span class="sxs-lookup"><span data-stu-id="600ec-101">Get-AzConsumptionBudget</span></span>

## <span data-ttu-id="600ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="600ec-102">SYNOPSIS</span></span>
<span data-ttu-id="600ec-103">Получить список бюджетов в подписке или группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="600ec-103">Get a list of budgets in either a subscription or a resource group.</span></span>

## <span data-ttu-id="600ec-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="600ec-104">SYNTAX</span></span>

```
Get-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] [-ResourceGroupName <String>]
 [-Name <String>] [<CommonParameters>]
```

## <span data-ttu-id="600ec-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="600ec-105">DESCRIPTION</span></span>
<span data-ttu-id="600ec-106">С Get-AzConsumptionBudget или группы ресурсов возвращается список бюджетов в подписке или группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="600ec-106">The Get-AzConsumptionBudget cmdlet gets a list of budgets in either a subscription or a resource group.</span></span>

## <span data-ttu-id="600ec-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="600ec-107">EXAMPLES</span></span>

### <span data-ttu-id="600ec-108">Пример 1. Просмотр списка бюджетов на уровне подписки</span><span class="sxs-lookup"><span data-stu-id="600ec-108">Example 1: Get a list of budgets at subscription level</span></span>
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

### <span data-ttu-id="600ec-109">Пример 2. Получить список бюджетов на уровне группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="600ec-109">Example 2: Get a list of budgets at resource group level</span></span>
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

### <span data-ttu-id="600ec-110">Пример 3. Получить бюджет с названием бюджета на уровне подписки</span><span class="sxs-lookup"><span data-stu-id="600ec-110">Example 3: Get a budget with the budget name at subscription level</span></span>
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

### <span data-ttu-id="600ec-111">Пример 4. Получить бюджет с названием бюджета на уровне группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="600ec-111">Example 4: Get a budget with the budget name at resource group level</span></span>
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

## <span data-ttu-id="600ec-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="600ec-112">PARAMETERS</span></span>

### <span data-ttu-id="600ec-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="600ec-113">-DefaultProfile</span></span>
<span data-ttu-id="600ec-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="600ec-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="600ec-115">-Name</span><span class="sxs-lookup"><span data-stu-id="600ec-115">-Name</span></span>
<span data-ttu-id="600ec-116">Имя бюджета.</span><span class="sxs-lookup"><span data-stu-id="600ec-116">Name of a budget.</span></span>

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

### <span data-ttu-id="600ec-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="600ec-117">-ResourceGroupName</span></span>
<span data-ttu-id="600ec-118">Группа ресурсов бюджета.</span><span class="sxs-lookup"><span data-stu-id="600ec-118">Resource Group of a budget.</span></span>

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

### <span data-ttu-id="600ec-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="600ec-119">CommonParameters</span></span>
<span data-ttu-id="600ec-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="600ec-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="600ec-121">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="600ec-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="600ec-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="600ec-122">INPUTS</span></span>

### <span data-ttu-id="600ec-123">Нет</span><span class="sxs-lookup"><span data-stu-id="600ec-123">None</span></span>

## <span data-ttu-id="600ec-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="600ec-124">OUTPUTS</span></span>

### <span data-ttu-id="600ec-125">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span><span class="sxs-lookup"><span data-stu-id="600ec-125">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>

## <span data-ttu-id="600ec-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="600ec-126">NOTES</span></span>

## <span data-ttu-id="600ec-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="600ec-127">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.Commands.Consumption.dll-Help.xml
Module Name: AzureRM.Consumption
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.consumption/get-azurermconsumptionbudget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Consumption/Commands.Consumption/help/Get-AzureRmConsumptionBudget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Consumption/Commands.Consumption/help/Get-AzureRmConsumptionBudget.md
ms.openlocfilehash: 7793dfe2f5d83e0975a5a8c200d19b48d8c4d9f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560988"
---
# <span data-ttu-id="33b31-101">Get-AzureRmConsumptionBudget</span><span class="sxs-lookup"><span data-stu-id="33b31-101">Get-AzureRmConsumptionBudget</span></span>

## <span data-ttu-id="33b31-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="33b31-102">SYNOPSIS</span></span>
<span data-ttu-id="33b31-103">Получение списка бюджетов либо в подписке, либо в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="33b31-103">Get a list of budgets in either a subscription or a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="33b31-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="33b31-104">SYNTAX</span></span>

```
Get-AzureRmConsumptionBudget [-DefaultProfile <IAzureContextContainer>] [-ResourceGroupName <String>]
 [-Name <String>] [<CommonParameters>]
```

## <span data-ttu-id="33b31-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="33b31-105">DESCRIPTION</span></span>
<span data-ttu-id="33b31-106">Командлет Get-AzureRmConsumptionBudget возвращает список бюджетов либо в подписке, либо в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="33b31-106">The Get-AzureRmConsumptionBudget cmdlet gets a list of budgets in either a subscription or a resource group.</span></span>

## <span data-ttu-id="33b31-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="33b31-107">EXAMPLES</span></span>

### <span data-ttu-id="33b31-108">Пример 1: получение списка бюджетов на уровне подписки</span><span class="sxs-lookup"><span data-stu-id="33b31-108">Example 1: Get a list of budgets at subscription level</span></span>
```powershell
PS C:\> Get-AzureRmConsumptionBudget
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

### <span data-ttu-id="33b31-109">Пример 2: получение списка бюджетов на уровне группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="33b31-109">Example 2: Get a list of budgets at resource group level</span></span>
```powershell
PS C:\> Get-AzureRmConsumptionBudget -ResourceGroupName RGBudgets
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

### <span data-ttu-id="33b31-110">Пример 3: получение бюджета с использованием названия бюджета на уровне подписки</span><span class="sxs-lookup"><span data-stu-id="33b31-110">Example 3: Get a budget with the budget name at subscription level</span></span>
```powershell
PS C:\> Get-AzureRmConsumptionBudget -Name PSBudget
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

### <span data-ttu-id="33b31-111">Пример 4: получение бюджета с использованием названия бюджета на уровне группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="33b31-111">Example 4: Get a budget with the budget name at resource group level</span></span>
```powershell
PS C:\> Get-AzureRmConsumptionBudget -ResourceGroupName RGBudgets -Name PSBudgetRG
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

## <span data-ttu-id="33b31-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="33b31-112">PARAMETERS</span></span>

### <span data-ttu-id="33b31-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33b31-113">-DefaultProfile</span></span>
<span data-ttu-id="33b31-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="33b31-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33b31-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="33b31-115">-Name</span></span>
<span data-ttu-id="33b31-116">Название бюджета.</span><span class="sxs-lookup"><span data-stu-id="33b31-116">Name of a budget.</span></span>

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

### <span data-ttu-id="33b31-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33b31-117">-ResourceGroupName</span></span>
<span data-ttu-id="33b31-118">Группа ресурсов бюджета.</span><span class="sxs-lookup"><span data-stu-id="33b31-118">Resource Group of a budget.</span></span>

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

### <span data-ttu-id="33b31-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33b31-119">CommonParameters</span></span>
<span data-ttu-id="33b31-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="33b31-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33b31-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33b31-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33b31-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="33b31-122">INPUTS</span></span>

### <span data-ttu-id="33b31-123">Ничего</span><span class="sxs-lookup"><span data-stu-id="33b31-123">None</span></span>

## <span data-ttu-id="33b31-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="33b31-124">OUTPUTS</span></span>

### <span data-ttu-id="33b31-125">Microsoft. Azure. Commands. потребление. Models. PSBudget</span><span class="sxs-lookup"><span data-stu-id="33b31-125">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>

## <span data-ttu-id="33b31-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="33b31-126">NOTES</span></span>

## <span data-ttu-id="33b31-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="33b31-127">RELATED LINKS</span></span>

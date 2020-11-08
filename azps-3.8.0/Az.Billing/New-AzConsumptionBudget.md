---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/new-azconsumptionbudget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/New-AzConsumptionBudget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/New-AzConsumptionBudget.md
ms.openlocfilehash: 1b6e815a8ccb02fe462393df8a91af9800b425df
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066873"
---
# <span data-ttu-id="4594f-101">New-AzConsumptionBudget</span><span class="sxs-lookup"><span data-stu-id="4594f-101">New-AzConsumptionBudget</span></span>

## <span data-ttu-id="4594f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4594f-102">SYNOPSIS</span></span>
<span data-ttu-id="4594f-103">Создайте бюджет либо в подписке, либо в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4594f-103">Create a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="4594f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4594f-104">SYNTAX</span></span>

### <span data-ttu-id="4594f-105">Подписка (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4594f-105">Subscription (Default)</span></span>
```
New-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String> -Amount <Decimal>
 -Category <String> -TimeGrain <String> -StartDate <DateTime> [-EndDate <DateTime>]
 [-ResourceGroupName <String>] [-MeterFilter <String[]>] [-ResourceFilter <String[]>]
 [-ResourceGroupFilter <String[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4594f-106">Извещен</span><span class="sxs-lookup"><span data-stu-id="4594f-106">Notification</span></span>
```
New-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String> -Amount <Decimal>
 -Category <String> -TimeGrain <String> -StartDate <DateTime> [-EndDate <DateTime>]
 [-ResourceGroupName <String>] [-MeterFilter <String[]>] [-ResourceFilter <String[]>]
 [-ResourceGroupFilter <String[]>] -NotificationKey <String> [-NotificationEnabled]
 -NotificationThreshold <Decimal> -ContactEmail <String[]> [-ContactGroup <String[]>] [-ContactRole <String[]>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4594f-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4594f-107">DESCRIPTION</span></span>
<span data-ttu-id="4594f-108">Командлет New-AzConsumptionBudget создает бюджет либо в подписке, либо в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4594f-108">The New-AzConsumptionBudget cmdlet creates a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="4594f-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4594f-109">EXAMPLES</span></span>

### <span data-ttu-id="4594f-110">Пример 1: создание бюджетных затрат с именем бюджета на уровне подписки</span><span class="sxs-lookup"><span data-stu-id="4594f-110">Example 1: Create a cost budget with a budget name at subscription level</span></span>
```powershell
PS C:\> New-AzConsumptionBudget -Amount 60 -Name PSBudget -Category Cost -StartDate 2018-06-01 -EndDate 2018-11-01 -TimeGrain Monthly
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

### <span data-ttu-id="4594f-111">Пример 2: создание бюджетных затрат с использованием названия бюджета на уровне группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="4594f-111">Example 2: Create a cost budget with a budget name at resource group level</span></span>
```powershell
PS C:\> New-AzConsumptionBudget -ResourceGroupName RGBudgets -Amount 60 -Name PSBudgetRG -Category Cost -StartDate 2018-06-01 -EndDate 2018-11-01 -TimeGrain Monthly
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

## <span data-ttu-id="4594f-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4594f-112">PARAMETERS</span></span>

### <span data-ttu-id="4594f-113">-Сумма</span><span class="sxs-lookup"><span data-stu-id="4594f-113">-Amount</span></span>
<span data-ttu-id="4594f-114">Сумма бюджета.</span><span class="sxs-lookup"><span data-stu-id="4594f-114">Amount of a budget.</span></span>

```yaml
Type: System.Decimal
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4594f-115">-Категория</span><span class="sxs-lookup"><span data-stu-id="4594f-115">-Category</span></span>
<span data-ttu-id="4594f-116">Категория бюджета может представлять собой стоимость или использование.</span><span class="sxs-lookup"><span data-stu-id="4594f-116">Category of the budget can be cost or usage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Cost, Usage

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4594f-117">-ContactEmail</span><span class="sxs-lookup"><span data-stu-id="4594f-117">-ContactEmail</span></span>
<span data-ttu-id="4594f-118">Адреса электронной почты, на которые нужно отправить уведомление о бюджете при превышении порогового значения.</span><span class="sxs-lookup"><span data-stu-id="4594f-118">Email addresses to send the budget notification to when the threshold is exceeded.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Notification
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4594f-119">-ContactGroup</span><span class="sxs-lookup"><span data-stu-id="4594f-119">-ContactGroup</span></span>
<span data-ttu-id="4594f-120">Группы действий для отправки уведомления о бюджете при превышении порогового значения.</span><span class="sxs-lookup"><span data-stu-id="4594f-120">Action groups to send the budget notification to when the threshold is exceeded.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Notification
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4594f-121">-ContactRole</span><span class="sxs-lookup"><span data-stu-id="4594f-121">-ContactRole</span></span>
<span data-ttu-id="4594f-122">Роли контактных лиц для отправки уведомления о бюджете при превышении порогового значения.</span><span class="sxs-lookup"><span data-stu-id="4594f-122">Contact roles to send the budget notification to when the threshold is exceeded.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Notification
Aliases:
Accepted values: Owner, Reader, Contributor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4594f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4594f-123">-DefaultProfile</span></span>
<span data-ttu-id="4594f-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4594f-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4594f-125">-EndDate</span><span class="sxs-lookup"><span data-stu-id="4594f-125">-EndDate</span></span>
<span data-ttu-id="4594f-126">Дата окончания срока действия бюджета (гггг-мм-дд в формате UTC).</span><span class="sxs-lookup"><span data-stu-id="4594f-126">End date (YYYY-MM-DD in UTC) of time period of a budget.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4594f-127">-MeterFilter</span><span class="sxs-lookup"><span data-stu-id="4594f-127">-MeterFilter</span></span>
<span data-ttu-id="4594f-128">Разделенный запятыми список измерительных приборов для фильтрации.</span><span class="sxs-lookup"><span data-stu-id="4594f-128">Comma-separated list of meters to filter on.</span></span>
<span data-ttu-id="4594f-129">Обязательно, если категория является использованием.</span><span class="sxs-lookup"><span data-stu-id="4594f-129">Required if category is usage.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4594f-130">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4594f-130">-Name</span></span>
<span data-ttu-id="4594f-131">Название бюджета.</span><span class="sxs-lookup"><span data-stu-id="4594f-131">Name of a budget.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4594f-132">-NotificationEnabled</span><span class="sxs-lookup"><span data-stu-id="4594f-132">-NotificationEnabled</span></span>
<span data-ttu-id="4594f-133">Уведомления включены или нет.</span><span class="sxs-lookup"><span data-stu-id="4594f-133">The notification is enabled or not.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Notification
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4594f-134">-NotificationKey</span><span class="sxs-lookup"><span data-stu-id="4594f-134">-NotificationKey</span></span>
<span data-ttu-id="4594f-135">Ключ уведомления, связанного с бюджетом, необходимый для создания уведомления с параметром включения уведомлений, порога уведомлений, контактами электронной почты, группами контактов и контактными ролями.</span><span class="sxs-lookup"><span data-stu-id="4594f-135">Key of a notification associated with a budget, required to create a notification with notification enabled switch, notification threshold, contact emails, contact groups, or contact roles.</span></span>

```yaml
Type: System.String
Parameter Sets: Notification
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4594f-136">-NotificationThreshold</span><span class="sxs-lookup"><span data-stu-id="4594f-136">-NotificationThreshold</span></span>
<span data-ttu-id="4594f-137">Пороговое значение, связанное с уведомлением.</span><span class="sxs-lookup"><span data-stu-id="4594f-137">Threshold value associated with a notification.</span></span>
<span data-ttu-id="4594f-138">Уведомление отправляется, когда стоимость или использование превысило пороговое значение.</span><span class="sxs-lookup"><span data-stu-id="4594f-138">Notification is sent when the cost or usage exceeded the threshold.</span></span>
<span data-ttu-id="4594f-139">Он всегда равен проценту и должен находиться в диапазоне от 0 до 1000.</span><span class="sxs-lookup"><span data-stu-id="4594f-139">It is always percent and has to be between 0 and 1000.</span></span>

```yaml
Type: System.Nullable`1[System.Decimal]
Parameter Sets: Notification
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4594f-140">-ResourceFilter</span><span class="sxs-lookup"><span data-stu-id="4594f-140">-ResourceFilter</span></span>
<span data-ttu-id="4594f-141">Список экземпляров ресурсов, разделенных запятыми, по которым нужно выполнить фильтрацию.</span><span class="sxs-lookup"><span data-stu-id="4594f-141">Comma-separated list of resource instances to filter on.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4594f-142">-ResourceGroupFilter</span><span class="sxs-lookup"><span data-stu-id="4594f-142">-ResourceGroupFilter</span></span>
<span data-ttu-id="4594f-143">Список групп ресурсов с разделителями-запятыми, по которому нужно выполнить фильтрацию.</span><span class="sxs-lookup"><span data-stu-id="4594f-143">Comma-separated list of resource groups to filter on.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4594f-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4594f-144">-ResourceGroupName</span></span>
<span data-ttu-id="4594f-145">Группа ресурсов бюджета.</span><span class="sxs-lookup"><span data-stu-id="4594f-145">Resource Group of a budget.</span></span>

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

### <span data-ttu-id="4594f-146">-StartDate</span><span class="sxs-lookup"><span data-stu-id="4594f-146">-StartDate</span></span>
<span data-ttu-id="4594f-147">Дата начала (гггг-мм-дд в формате UTC) периода бюджета.</span><span class="sxs-lookup"><span data-stu-id="4594f-147">Start date (YYYY-MM-DD in UTC) of time period of a budget.</span></span>
<span data-ttu-id="4594f-148">Не до текущего месяца для ежемесячного прокадрового времени.</span><span class="sxs-lookup"><span data-stu-id="4594f-148">Not prior to current month for monthly time grain.</span></span>
<span data-ttu-id="4594f-149">Не более чем за три месяца для квартального интервала времени.</span><span class="sxs-lookup"><span data-stu-id="4594f-149">Not prior to three months for quarterly time grain.</span></span>
<span data-ttu-id="4594f-150">Не более двенадцати месяцев для ежегодных граней.</span><span class="sxs-lookup"><span data-stu-id="4594f-150">Not prior to twelve months for yearly time grain.</span></span>
<span data-ttu-id="4594f-151">Дата начала в будущем не более трех месяцев.</span><span class="sxs-lookup"><span data-stu-id="4594f-151">Future start date not more than three months.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4594f-152">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="4594f-152">-TimeGrain</span></span>
<span data-ttu-id="4594f-153">Временные Гранки бюджета могут быть ежемесячными, ежеквартальными и ежегодно.</span><span class="sxs-lookup"><span data-stu-id="4594f-153">Time grain of the budget can be monthly, quarterly, or annually.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Monthly, Quarterly, Annually

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4594f-154">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4594f-154">-Confirm</span></span>
<span data-ttu-id="4594f-155">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4594f-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4594f-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4594f-156">-WhatIf</span></span>
<span data-ttu-id="4594f-157">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4594f-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4594f-158">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4594f-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4594f-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4594f-159">CommonParameters</span></span>
<span data-ttu-id="4594f-160">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4594f-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4594f-161">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4594f-161">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4594f-162">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4594f-162">INPUTS</span></span>

### <span data-ttu-id="4594f-163">Ничего</span><span class="sxs-lookup"><span data-stu-id="4594f-163">None</span></span>

## <span data-ttu-id="4594f-164">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4594f-164">OUTPUTS</span></span>

### <span data-ttu-id="4594f-165">Microsoft. Azure. Commands. потребление. Models. PSBudget</span><span class="sxs-lookup"><span data-stu-id="4594f-165">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>

## <span data-ttu-id="4594f-166">Пуск</span><span class="sxs-lookup"><span data-stu-id="4594f-166">NOTES</span></span>

## <span data-ttu-id="4594f-167">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4594f-167">RELATED LINKS</span></span>

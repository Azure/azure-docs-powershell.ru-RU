---
external help file: Microsoft.Azure.Commands.Consumption.dll-Help.xml
Module Name: AzureRM.Consumption
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.consumption/new-azurermconsumptionbudget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Consumption/Commands.Consumption/help/New-AzureRmConsumptionBudget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Consumption/Commands.Consumption/help/New-AzureRmConsumptionBudget.md
ms.openlocfilehash: 9c89a4791b4e32637d069a672ddde06862518332
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567790"
---
# <span data-ttu-id="0b031-101">New-AzureRmConsumptionBudget</span><span class="sxs-lookup"><span data-stu-id="0b031-101">New-AzureRmConsumptionBudget</span></span>

## <span data-ttu-id="0b031-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0b031-102">SYNOPSIS</span></span>
<span data-ttu-id="0b031-103">Создайте бюджет либо в подписке, либо в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0b031-103">Create a budget in either a subscription or a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0b031-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0b031-104">SYNTAX</span></span>

### <span data-ttu-id="0b031-105">Подписка (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0b031-105">Subscription (Default)</span></span>
```
New-AzureRmConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String> -Amount <Decimal>
 -Category <String> -TimeGrain <String> -StartDate <DateTime> [-EndDate <DateTime>]
 [-ResourceGroupName <String>] [-MeterFilter <String[]>] [-ResourceFilter <String[]>]
 [-ResourceGroupFilter <String[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b031-106">Извещен</span><span class="sxs-lookup"><span data-stu-id="0b031-106">Notification</span></span>
```
New-AzureRmConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String> -Amount <Decimal>
 -Category <String> -TimeGrain <String> -StartDate <DateTime> [-EndDate <DateTime>]
 [-ResourceGroupName <String>] [-MeterFilter <String[]>] [-ResourceFilter <String[]>]
 [-ResourceGroupFilter <String[]>] -NotificationKey <String> [-NotificationEnabled]
 -NotificationThreshold <Decimal> -ContactEmail <String[]> [-ContactGroup <String[]>] [-ContactRole <String[]>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b031-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0b031-107">DESCRIPTION</span></span>
<span data-ttu-id="0b031-108">Командлет New-AzureRmConsumptionBudget создает бюджет либо в подписке, либо в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0b031-108">The New-AzureRmConsumptionBudget cmdlet creates a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="0b031-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0b031-109">EXAMPLES</span></span>

### <span data-ttu-id="0b031-110">Пример 1: создание бюджетных затрат с именем бюджета на уровне подписки</span><span class="sxs-lookup"><span data-stu-id="0b031-110">Example 1: Create a cost budget with a budget name at subscription level</span></span>
```powershell
PS C:\> New-AzureRmConsumptionBudget -Amount 60 -Name PSBudget -Category Cost -StartDate 2018-06-01 -EndDate 2018-11-01 -TimeGrain Monthly
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

### <span data-ttu-id="0b031-111">Пример 2: создание бюджетных затрат с использованием названия бюджета на уровне группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="0b031-111">Example 2: Create a cost budget with a budget name at resource group level</span></span>
```powershell
PS C:\> New-AzureRmConsumptionBudget -ResourceGroupName RGBudgets -Amount 60 -Name PSBudgetRG -Category Cost -StartDate 2018-06-01 -EndDate 2018-11-01 -TimeGrain Monthly
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

## <span data-ttu-id="0b031-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0b031-112">PARAMETERS</span></span>

### <span data-ttu-id="0b031-113">-Сумма</span><span class="sxs-lookup"><span data-stu-id="0b031-113">-Amount</span></span>
<span data-ttu-id="0b031-114">Сумма бюджета.</span><span class="sxs-lookup"><span data-stu-id="0b031-114">Amount of a budget.</span></span>

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

### <span data-ttu-id="0b031-115">-Категория</span><span class="sxs-lookup"><span data-stu-id="0b031-115">-Category</span></span>
<span data-ttu-id="0b031-116">Категория бюджета может представлять собой стоимость или использование.</span><span class="sxs-lookup"><span data-stu-id="0b031-116">Category of the budget can be cost or usage.</span></span>

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

### <span data-ttu-id="0b031-117">-ContactEmail</span><span class="sxs-lookup"><span data-stu-id="0b031-117">-ContactEmail</span></span>
<span data-ttu-id="0b031-118">Адреса электронной почты, на которые нужно отправить уведомление о бюджете при превышении порогового значения.</span><span class="sxs-lookup"><span data-stu-id="0b031-118">Email addresses to send the budget notification to when the threshold is exceeded.</span></span>

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

### <span data-ttu-id="0b031-119">-ContactGroup</span><span class="sxs-lookup"><span data-stu-id="0b031-119">-ContactGroup</span></span>
<span data-ttu-id="0b031-120">Группы действий для отправки уведомления о бюджете при превышении порогового значения.</span><span class="sxs-lookup"><span data-stu-id="0b031-120">Action groups to send the budget notification to when the threshold is exceeded.</span></span>

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

### <span data-ttu-id="0b031-121">-ContactRole</span><span class="sxs-lookup"><span data-stu-id="0b031-121">-ContactRole</span></span>
<span data-ttu-id="0b031-122">Роли контактных лиц для отправки уведомления о бюджете при превышении порогового значения.</span><span class="sxs-lookup"><span data-stu-id="0b031-122">Contact roles to send the budget notification to when the threshold is exceeded.</span></span>

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

### <span data-ttu-id="0b031-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b031-123">-DefaultProfile</span></span>
<span data-ttu-id="0b031-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0b031-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b031-125">-EndDate</span><span class="sxs-lookup"><span data-stu-id="0b031-125">-EndDate</span></span>
<span data-ttu-id="0b031-126">Дата окончания срока действия бюджета (гггг-мм-дд в формате UTC).</span><span class="sxs-lookup"><span data-stu-id="0b031-126">End date (YYYY-MM-DD in UTC) of time period of a budget.</span></span>

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

### <span data-ttu-id="0b031-127">-MeterFilter</span><span class="sxs-lookup"><span data-stu-id="0b031-127">-MeterFilter</span></span>
<span data-ttu-id="0b031-128">Разделенный запятыми список измерительных приборов для фильтрации.</span><span class="sxs-lookup"><span data-stu-id="0b031-128">Comma-separated list of meters to filter on.</span></span>
<span data-ttu-id="0b031-129">Обязательно, если категория является использованием.</span><span class="sxs-lookup"><span data-stu-id="0b031-129">Required if category is usage.</span></span>

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

### <span data-ttu-id="0b031-130">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0b031-130">-Name</span></span>
<span data-ttu-id="0b031-131">Название бюджета.</span><span class="sxs-lookup"><span data-stu-id="0b031-131">Name of a budget.</span></span>

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

### <span data-ttu-id="0b031-132">-NotificationEnabled</span><span class="sxs-lookup"><span data-stu-id="0b031-132">-NotificationEnabled</span></span>
<span data-ttu-id="0b031-133">Уведомления включены или нет.</span><span class="sxs-lookup"><span data-stu-id="0b031-133">The notification is enabled or not.</span></span>

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

### <span data-ttu-id="0b031-134">-NotificationKey</span><span class="sxs-lookup"><span data-stu-id="0b031-134">-NotificationKey</span></span>
<span data-ttu-id="0b031-135">Ключ уведомления, связанного с бюджетом, необходимый для создания уведомления с параметром включения уведомлений, порога уведомлений, контактами электронной почты, группами контактов и контактными ролями.</span><span class="sxs-lookup"><span data-stu-id="0b031-135">Key of a notification associated with a budget, required to create a notification with notification enabled switch, notification threshold, contact emails, contact groups, or contact roles.</span></span>

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

### <span data-ttu-id="0b031-136">-NotificationThreshold</span><span class="sxs-lookup"><span data-stu-id="0b031-136">-NotificationThreshold</span></span>
<span data-ttu-id="0b031-137">Пороговое значение, связанное с уведомлением.</span><span class="sxs-lookup"><span data-stu-id="0b031-137">Threshold value associated with a notification.</span></span>
<span data-ttu-id="0b031-138">Уведомление отправляется, когда стоимость или использование превысило пороговое значение.</span><span class="sxs-lookup"><span data-stu-id="0b031-138">Notification is sent when the cost or usage exceeded the threshold.</span></span>
<span data-ttu-id="0b031-139">Он всегда равен проценту и должен находиться в диапазоне от 0 до 1000.</span><span class="sxs-lookup"><span data-stu-id="0b031-139">It is always percent and has to be between 0 and 1000.</span></span>

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

### <span data-ttu-id="0b031-140">-ResourceFilter</span><span class="sxs-lookup"><span data-stu-id="0b031-140">-ResourceFilter</span></span>
<span data-ttu-id="0b031-141">Список экземпляров ресурсов, разделенных запятыми, по которым нужно выполнить фильтрацию.</span><span class="sxs-lookup"><span data-stu-id="0b031-141">Comma-separated list of resource instances to filter on.</span></span>

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

### <span data-ttu-id="0b031-142">-ResourceGroupFilter</span><span class="sxs-lookup"><span data-stu-id="0b031-142">-ResourceGroupFilter</span></span>
<span data-ttu-id="0b031-143">Список групп ресурсов с разделителями-запятыми, по которому нужно выполнить фильтрацию.</span><span class="sxs-lookup"><span data-stu-id="0b031-143">Comma-separated list of resource groups to filter on.</span></span>

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

### <span data-ttu-id="0b031-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b031-144">-ResourceGroupName</span></span>
<span data-ttu-id="0b031-145">Группа ресурсов бюджета.</span><span class="sxs-lookup"><span data-stu-id="0b031-145">Resource Group of a budget.</span></span>

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

### <span data-ttu-id="0b031-146">-StartDate</span><span class="sxs-lookup"><span data-stu-id="0b031-146">-StartDate</span></span>
<span data-ttu-id="0b031-147">Дата начала (гггг-мм-дд в формате UTC) периода бюджета.</span><span class="sxs-lookup"><span data-stu-id="0b031-147">Start date (YYYY-MM-DD in UTC) of time period of a budget.</span></span>
<span data-ttu-id="0b031-148">Не до текущего месяца для ежемесячного прокадрового времени.</span><span class="sxs-lookup"><span data-stu-id="0b031-148">Not prior to current month for monthly time grain.</span></span>
<span data-ttu-id="0b031-149">Не более чем за три месяца для квартального интервала времени.</span><span class="sxs-lookup"><span data-stu-id="0b031-149">Not prior to three months for quarterly time grain.</span></span>
<span data-ttu-id="0b031-150">Не более двенадцати месяцев для ежегодных граней.</span><span class="sxs-lookup"><span data-stu-id="0b031-150">Not prior to twelve months for yearly time grain.</span></span>
<span data-ttu-id="0b031-151">Дата начала в будущем не более трех месяцев.</span><span class="sxs-lookup"><span data-stu-id="0b031-151">Future start date not more than three months.</span></span>

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

### <span data-ttu-id="0b031-152">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="0b031-152">-TimeGrain</span></span>
<span data-ttu-id="0b031-153">Временные Гранки бюджета могут быть ежемесячными, ежеквартальными и ежегодно.</span><span class="sxs-lookup"><span data-stu-id="0b031-153">Time grain of the budget can be monthly, quarterly, or annually.</span></span>

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

### <span data-ttu-id="0b031-154">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0b031-154">-Confirm</span></span>
<span data-ttu-id="0b031-155">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0b031-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b031-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b031-156">-WhatIf</span></span>
<span data-ttu-id="0b031-157">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0b031-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b031-158">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0b031-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b031-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b031-159">CommonParameters</span></span>
<span data-ttu-id="0b031-160">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0b031-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b031-161">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b031-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b031-162">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0b031-162">INPUTS</span></span>

### <span data-ttu-id="0b031-163">Ничего</span><span class="sxs-lookup"><span data-stu-id="0b031-163">None</span></span>

## <span data-ttu-id="0b031-164">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0b031-164">OUTPUTS</span></span>

### <span data-ttu-id="0b031-165">Microsoft. Azure. Commands. потребление. Models. PSBudget</span><span class="sxs-lookup"><span data-stu-id="0b031-165">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>

## <span data-ttu-id="0b031-166">Пуск</span><span class="sxs-lookup"><span data-stu-id="0b031-166">NOTES</span></span>

## <span data-ttu-id="0b031-167">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0b031-167">RELATED LINKS</span></span>

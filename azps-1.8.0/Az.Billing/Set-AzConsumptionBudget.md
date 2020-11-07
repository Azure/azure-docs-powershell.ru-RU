---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/set-azconsumptionbudget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Set-AzConsumptionBudget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Set-AzConsumptionBudget.md
ms.openlocfilehash: c159ab71befb52e8131ade0b90e69c4ba8158885
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93731437"
---
# <span data-ttu-id="2838d-101">Set-AzConsumptionBudget</span><span class="sxs-lookup"><span data-stu-id="2838d-101">Set-AzConsumptionBudget</span></span>

## <span data-ttu-id="2838d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2838d-102">SYNOPSIS</span></span>
<span data-ttu-id="2838d-103">Обновление бюджета либо в подписке, либо в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2838d-103">Update a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="2838d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2838d-104">SYNTAX</span></span>

### <span data-ttu-id="2838d-105">Подписка (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2838d-105">Subscription (Default)</span></span>
```
Set-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String> [-Amount <Decimal>]
 [-Category <String>] [-TimeGrain <String>] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-ResourceGroupName <String>] [-MeterFilter <String[]>] [-ResourceFilter <String[]>]
 [-ResourceGroupFilter <String[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2838d-106">Извещен</span><span class="sxs-lookup"><span data-stu-id="2838d-106">Notification</span></span>
```
Set-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String> [-Amount <Decimal>]
 [-Category <String>] [-TimeGrain <String>] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-ResourceGroupName <String>] [-MeterFilter <String[]>] [-ResourceFilter <String[]>]
 [-ResourceGroupFilter <String[]>] -NotificationKey <String> [-NotificationEnabled]
 [-NotificationThreshold <Decimal>] [-ContactEmail <String[]>] [-ContactGroup <String[]>]
 [-ContactRole <String[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2838d-107">Трубодержателей</span><span class="sxs-lookup"><span data-stu-id="2838d-107">Piping</span></span>
```
Set-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -InputObject <PSBudget> [-Amount <Decimal>]
 [-Category <String>] [-TimeGrain <String>] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-MeterFilter <String[]>] [-ResourceFilter <String[]>] [-ResourceGroupFilter <String[]>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2838d-108">Трубопроводов и уведомления</span><span class="sxs-lookup"><span data-stu-id="2838d-108">Piping and Notification</span></span>
```
Set-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -InputObject <PSBudget> [-Amount <Decimal>]
 [-Category <String>] [-TimeGrain <String>] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-MeterFilter <String[]>] [-ResourceFilter <String[]>] [-ResourceGroupFilter <String[]>]
 -NotificationKey <String> [-NotificationEnabled] [-NotificationThreshold <Decimal>] [-ContactEmail <String[]>]
 [-ContactGroup <String[]>] [-ContactRole <String[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2838d-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2838d-109">DESCRIPTION</span></span>
<span data-ttu-id="2838d-110">Командлет Set-AzConsumptionBudget обновляет бюджет либо в подписке, либо в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2838d-110">The Set-AzConsumptionBudget cmdlet updates a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="2838d-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2838d-111">EXAMPLES</span></span>

### <span data-ttu-id="2838d-112">Пример 1: Обновление бюджета на новую сумму с учетом названия бюджета на уровне подписки</span><span class="sxs-lookup"><span data-stu-id="2838d-112">Example 1: Update a budget by a new amount with a budget name at subscription level</span></span>
```powershell
PS C:\> Set-AzConsumptionBudget -Name PSBudget -Amount 75
Amount:  75     
Category:  Cost
CurrentSpend:  null
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Consumption/budgets/PSBudget
Name:  PSBudget
TimeGrain:  Monthly
TimePeriod:  EndDate:  11/1/2018 12:00:00 AM
             StartDate:  6/1/2018 12:00:00 AM
Type:  Microsoft.Consumption/budgets
```

### <span data-ttu-id="2838d-113">Пример 2: Обновление бюджета с уведомлением о том, что стоимость или использование достигает порогового значения 90% от суммы на уровне подписки</span><span class="sxs-lookup"><span data-stu-id="2838d-113">Example 2: Update a budget with a notification when cost or usage reaches a threshold of 90 percent of amount at subscription level</span></span>
```powershell
PS C:\> Set-AzConsumptionBudget -Name PSBudget -NotificationKey notificationKey-ps1234 -NotificationEnabled -NotificationThreshold 90 -ContactEmail johndoe@contoso.com,janesmith@contoso.com -ContactRole Owner,Reader,Contributor
Amount:  75     
Category:  Cost
CurrentSpend:  null
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Consumption/budgets/PSBudget
Name:  PSBudget
Notification:  NotificationKey:  notificationKey-ps1234
               Threshold:  90
               Enabled:  true
               ContactEmail:  johndoe@contoso.com,janesmith@contoso.com
               ContactRole:  Owner,Reader,Contributor
TimeGrain:  Monthly
TimePeriod:  EndDate:  11/1/2018 12:00:00 AM
             StartDate:  6/1/2018 12:00:00 AM
Type:  Microsoft.Consumption/budgets
```

### <span data-ttu-id="2838d-114">Пример 3: Обновление бюджета на новую сумму с использованием названия бюджета на уровне группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="2838d-114">Example 3: Update a budget by a new amount with a budget name at resource group level</span></span>
```powershell
PS C:\> Set-AzConsumptionBudget -ResourceGroupName RGBudgets -Name PSBudgetRG -Amount 75
Amount:  75     
Category:  Cost
CurrentSpend:  null
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/resourceGroups/RGBudgets/providers/Microsoft.Consumption/budgets/PSBudgetRG
Name:  PSBudgetRG
TimeGrain:  Monthly
TimePeriod:  EndDate:  11/1/2018 12:00:00 AM
             StartDate:  6/1/2018 12:00:00 AM
Type:  Microsoft.Consumption/budgets
```

## <span data-ttu-id="2838d-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2838d-115">PARAMETERS</span></span>

### <span data-ttu-id="2838d-116">-Сумма</span><span class="sxs-lookup"><span data-stu-id="2838d-116">-Amount</span></span>
<span data-ttu-id="2838d-117">Сумма бюджета.</span><span class="sxs-lookup"><span data-stu-id="2838d-117">Amount of a budget.</span></span>

```yaml
Type: System.Nullable`1[System.Decimal]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2838d-118">-Категория</span><span class="sxs-lookup"><span data-stu-id="2838d-118">-Category</span></span>
<span data-ttu-id="2838d-119">Категория бюджета может представлять собой стоимость или использование.</span><span class="sxs-lookup"><span data-stu-id="2838d-119">Category of the budget can be cost or usage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Cost, Usage

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2838d-120">-ContactEmail</span><span class="sxs-lookup"><span data-stu-id="2838d-120">-ContactEmail</span></span>
<span data-ttu-id="2838d-121">Адреса электронной почты, на которые нужно отправить уведомление о бюджете при превышении порогового значения.</span><span class="sxs-lookup"><span data-stu-id="2838d-121">Email addresses to send the budget notification to when the threshold is exceeded.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Notification, Piping and Notification
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2838d-122">-ContactGroup</span><span class="sxs-lookup"><span data-stu-id="2838d-122">-ContactGroup</span></span>
<span data-ttu-id="2838d-123">Группы действий для отправки уведомления о бюджете при превышении порогового значения.</span><span class="sxs-lookup"><span data-stu-id="2838d-123">Action groups to send the budget notification to when the threshold is exceeded.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Notification, Piping and Notification
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2838d-124">-ContactRole</span><span class="sxs-lookup"><span data-stu-id="2838d-124">-ContactRole</span></span>
<span data-ttu-id="2838d-125">Роли контактных лиц для отправки уведомления о бюджете при превышении порогового значения.</span><span class="sxs-lookup"><span data-stu-id="2838d-125">Contact roles to send the budget notification to when the threshold is exceeded.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Notification, Piping and Notification
Aliases:
Accepted values: Owner, Reader, Contributor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2838d-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2838d-126">-DefaultProfile</span></span>
<span data-ttu-id="2838d-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2838d-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2838d-128">-EndDate</span><span class="sxs-lookup"><span data-stu-id="2838d-128">-EndDate</span></span>
<span data-ttu-id="2838d-129">Дата окончания срока действия бюджета (гггг-мм-дд в формате UTC).</span><span class="sxs-lookup"><span data-stu-id="2838d-129">End date (YYYY-MM-DD in UTC) of time period of a budget.</span></span>

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

### <span data-ttu-id="2838d-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2838d-130">-InputObject</span></span>
<span data-ttu-id="2838d-131">Объект бюджета.</span><span class="sxs-lookup"><span data-stu-id="2838d-131">Budget object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Consumption.Models.PSBudget
Parameter Sets: Piping, Piping and Notification
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2838d-132">-MeterFilter</span><span class="sxs-lookup"><span data-stu-id="2838d-132">-MeterFilter</span></span>
<span data-ttu-id="2838d-133">Разделенный запятыми список измерительных приборов для фильтрации.</span><span class="sxs-lookup"><span data-stu-id="2838d-133">Comma-separated list of meters to filter on.</span></span>
<span data-ttu-id="2838d-134">Обязательно, если категория является использованием.</span><span class="sxs-lookup"><span data-stu-id="2838d-134">Required if category is usage.</span></span>

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

### <span data-ttu-id="2838d-135">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2838d-135">-Name</span></span>
<span data-ttu-id="2838d-136">Название бюджета.</span><span class="sxs-lookup"><span data-stu-id="2838d-136">Name of a budget.</span></span>

```yaml
Type: System.String
Parameter Sets: Subscription, Notification
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2838d-137">-NotificationEnabled</span><span class="sxs-lookup"><span data-stu-id="2838d-137">-NotificationEnabled</span></span>
<span data-ttu-id="2838d-138">Уведомление включено.</span><span class="sxs-lookup"><span data-stu-id="2838d-138">The notification is enabled.</span></span>
<span data-ttu-id="2838d-139">Если не указано, уведомление отключается по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2838d-139">If not specified, the notification is disabled by default.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Notification, Piping and Notification
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2838d-140">-NotificationKey</span><span class="sxs-lookup"><span data-stu-id="2838d-140">-NotificationKey</span></span>
<span data-ttu-id="2838d-141">Ключ уведомления, связанного с бюджетом, необходимый для создания уведомления с параметром включения уведомлений, порога уведомлений, контактами электронной почты, группами контактов и контактными ролями.</span><span class="sxs-lookup"><span data-stu-id="2838d-141">Key of a notification associated with a budget, required to create a notification with notification enabled switch, notification threshold, contact emails, contact groups, or contact roles.</span></span>

```yaml
Type: System.String
Parameter Sets: Notification, Piping and Notification
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2838d-142">-NotificationThreshold</span><span class="sxs-lookup"><span data-stu-id="2838d-142">-NotificationThreshold</span></span>
<span data-ttu-id="2838d-143">Пороговое значение, связанное с уведомлением.</span><span class="sxs-lookup"><span data-stu-id="2838d-143">Threshold value associated with a notification.</span></span>
<span data-ttu-id="2838d-144">Уведомление отправляется, когда стоимость или использование превысило пороговое значение.</span><span class="sxs-lookup"><span data-stu-id="2838d-144">Notification is sent when the cost or usage exceeded the threshold.</span></span>
<span data-ttu-id="2838d-145">Он всегда равен проценту и должен находиться в диапазоне от 0 до 1000.</span><span class="sxs-lookup"><span data-stu-id="2838d-145">It is always percent and has to be between 0 and 1000.</span></span>

```yaml
Type: System.Nullable`1[System.Decimal]
Parameter Sets: Notification, Piping and Notification
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2838d-146">-ResourceFilter</span><span class="sxs-lookup"><span data-stu-id="2838d-146">-ResourceFilter</span></span>
<span data-ttu-id="2838d-147">Список экземпляров ресурсов, разделенных запятыми, по которым нужно выполнить фильтрацию.</span><span class="sxs-lookup"><span data-stu-id="2838d-147">Comma-separated list of resource instances to filter on.</span></span>

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

### <span data-ttu-id="2838d-148">-ResourceGroupFilter</span><span class="sxs-lookup"><span data-stu-id="2838d-148">-ResourceGroupFilter</span></span>
<span data-ttu-id="2838d-149">Список групп ресурсов с разделителями-запятыми, по которому нужно выполнить фильтрацию.</span><span class="sxs-lookup"><span data-stu-id="2838d-149">Comma-separated list of resource groups to filter on.</span></span>

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

### <span data-ttu-id="2838d-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2838d-150">-ResourceGroupName</span></span>
<span data-ttu-id="2838d-151">Группа ресурсов бюджета.</span><span class="sxs-lookup"><span data-stu-id="2838d-151">Resource Group of a budget.</span></span>

```yaml
Type: System.String
Parameter Sets: Subscription, Notification
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2838d-152">-StartDate</span><span class="sxs-lookup"><span data-stu-id="2838d-152">-StartDate</span></span>
<span data-ttu-id="2838d-153">Дата начала (гггг-мм-дд в формате UTC) периода бюджета.</span><span class="sxs-lookup"><span data-stu-id="2838d-153">Start date (YYYY-MM-DD in UTC) of time period of a budget.</span></span>
<span data-ttu-id="2838d-154">Не до текущего месяца для ежемесячного прокадрового времени.</span><span class="sxs-lookup"><span data-stu-id="2838d-154">Not prior to current month for monthly time grain.</span></span>
<span data-ttu-id="2838d-155">Не более чем за три месяца для квартального интервала времени.</span><span class="sxs-lookup"><span data-stu-id="2838d-155">Not prior to three months for quarterly time grain.</span></span>
<span data-ttu-id="2838d-156">Не более двенадцати месяцев для ежегодных граней.</span><span class="sxs-lookup"><span data-stu-id="2838d-156">Not prior to twelve months for yearly time grain.</span></span>
<span data-ttu-id="2838d-157">Дата начала в будущем не более трех месяцев.</span><span class="sxs-lookup"><span data-stu-id="2838d-157">Future start date not more than three months.</span></span>

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

### <span data-ttu-id="2838d-158">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="2838d-158">-TimeGrain</span></span>
<span data-ttu-id="2838d-159">Временные Гранки бюджета могут быть ежемесячными, ежеквартальными и ежегодно.</span><span class="sxs-lookup"><span data-stu-id="2838d-159">Time grain of the budget can be monthly, quarterly, or annually.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Monthly, Quarterly, Annually

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2838d-160">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2838d-160">-Confirm</span></span>
<span data-ttu-id="2838d-161">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2838d-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2838d-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2838d-162">-WhatIf</span></span>
<span data-ttu-id="2838d-163">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2838d-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2838d-164">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2838d-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2838d-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2838d-165">CommonParameters</span></span>
<span data-ttu-id="2838d-166">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2838d-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2838d-167">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2838d-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2838d-168">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2838d-168">INPUTS</span></span>

### <span data-ttu-id="2838d-169">Microsoft. Azure. Commands. потребление. Models. PSBudget</span><span class="sxs-lookup"><span data-stu-id="2838d-169">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>

## <span data-ttu-id="2838d-170">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2838d-170">OUTPUTS</span></span>

### <span data-ttu-id="2838d-171">Microsoft. Azure. Commands. потребление. Models. PSBudget</span><span class="sxs-lookup"><span data-stu-id="2838d-171">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>

## <span data-ttu-id="2838d-172">Пуск</span><span class="sxs-lookup"><span data-stu-id="2838d-172">NOTES</span></span>

## <span data-ttu-id="2838d-173">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2838d-173">RELATED LINKS</span></span>

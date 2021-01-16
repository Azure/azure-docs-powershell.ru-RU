---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 7436F31F-9DCB-4365-BA6D-41BDB5D7FCB6
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/add-azautoscalesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzAutoscaleSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzAutoscaleSetting.md
ms.openlocfilehash: b2f7410f45a5b60a768d22fe7e66b7d8c1e4ad94
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98409180"
---
# <span data-ttu-id="5ea95-101">Add-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="5ea95-101">Add-AzAutoscaleSetting</span></span>

## <span data-ttu-id="5ea95-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5ea95-102">SYNOPSIS</span></span>
<span data-ttu-id="5ea95-103">Создает параметр автомасштабии.</span><span class="sxs-lookup"><span data-stu-id="5ea95-103">Creates an Autoscale setting.</span></span>

## <span data-ttu-id="5ea95-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5ea95-104">SYNTAX</span></span>

### <span data-ttu-id="5ea95-105">UpdateAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="5ea95-105">UpdateAutoscaleSetting</span></span>
```
Add-AzAutoscaleSetting -InputObject <PSAutoscaleSetting> -ResourceGroupName <String> [-DisableSetting]
 [-AutoscaleProfile <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile]>]
 [-Notification <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ea95-106">CreateAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="5ea95-106">CreateAutoscaleSetting</span></span>
```
Add-AzAutoscaleSetting -Location <String> -Name <String> -ResourceGroupName <String> [-DisableSetting]
 [-AutoscaleProfile <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile]>]
 -TargetResourceId <String>
 [-Notification <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ea95-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5ea95-107">DESCRIPTION</span></span>
<span data-ttu-id="5ea95-108">Для создания параметра автомасштабы с его параметром будет добавлена надстройка **Add-AzAutoscaleSetting.**</span><span class="sxs-lookup"><span data-stu-id="5ea95-108">The **Add-AzAutoscaleSetting** cmdlet creates an Autoscale setting.</span></span>
<span data-ttu-id="5ea95-109">Этот cmdlet реализует шаблон ShouldProcess, то есть может запросить подтверждение у пользователя перед созданием, изменением или удалением ресурса.</span><span class="sxs-lookup"><span data-stu-id="5ea95-109">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="5ea95-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5ea95-110">EXAMPLES</span></span>

### <span data-ttu-id="5ea95-111">Пример 1. Создание параметра авто шкалы</span><span class="sxs-lookup"><span data-stu-id="5ea95-111">Example 1: Create an Autoscale setting</span></span>
```
PS C:\>$Rule1 = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"

PS C:\> $Profile1 = New-AzAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -StartTimeWindow 2015-03-05T14:00:00 -EndTimeWindow 2015-03-05T14:30:00 -TimeWindowTimeZone GMT -Rule $Rule1, $Rule2 -Name "adios"

PS C:\> $Profile2 = New-AzAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rule $Rule1, $Rule2 -Name "SecondProfileName" -RecurrenceFrequency Minute -ScheduleDay "1", "2", "3" -ScheduleHour 5, 10, 15 -ScheduleMinute 15, 30, 45 -ScheduleTimeZone GMT

PS C:\> Add-AzAutoscaleSetting -Location "East US" -Name "MySetting" -ResourceGroupName "Default-Web-EastUS" -TargetResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm" -AutoscaleProfile $Profile1, $Profile2
```

<span data-ttu-id="5ea95-112">Первые две команды используют [команду New-AzAutoscaleRule,](https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azautoscalerule) чтобы создать два правила для $Rule 1 и $Rule 2.</span><span class="sxs-lookup"><span data-stu-id="5ea95-112">The first two commands use [New-AzAutoscaleRule](https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azautoscalerule) to create two Autoscale rules, $Rule1 and $Rule2.</span></span>
<span data-ttu-id="5ea95-113">Третья и четвертая команды используют [new-AzAutoscaleProfile](https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azautoscaleprofile) для создания профилей автомасштабы $Profile 1 и $Profile 2 с помощью $Rule 1 и $Rule 2.</span><span class="sxs-lookup"><span data-stu-id="5ea95-113">The third and fourth commands use [New-AzAutoscaleProfile](https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azautoscaleprofile) to create Autoscale profiles, $Profile1 and $Profile2, using $Rule1 and $Rule2.</span></span>
<span data-ttu-id="5ea95-114">Конечная команда создает параметр авто шкалы с использованием профилей в $Profile 1 и $Profile 2.</span><span class="sxs-lookup"><span data-stu-id="5ea95-114">The final command creates an Autoscale setting using the profiles in $Profile1 and $Profile2.</span></span>

## <span data-ttu-id="5ea95-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5ea95-115">PARAMETERS</span></span>

### <span data-ttu-id="5ea95-116">-AutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="5ea95-116">-AutoscaleProfile</span></span>
<span data-ttu-id="5ea95-117">Список профилей, которые нужно добавить к параметру авто шкалы или $Null без профиля.</span><span class="sxs-lookup"><span data-stu-id="5ea95-117">Specifies a list of profiles to add to the Autoscale setting, or $Null to add no profile.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ea95-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ea95-118">-DefaultProfile</span></span>
<span data-ttu-id="5ea95-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="5ea95-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5ea95-120">-DisableSetting</span><span class="sxs-lookup"><span data-stu-id="5ea95-120">-DisableSetting</span></span>
<span data-ttu-id="5ea95-121">Отключение существующего параметра автомасштабии.</span><span class="sxs-lookup"><span data-stu-id="5ea95-121">Disables an existing Autoscale setting.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ea95-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5ea95-122">-InputObject</span></span>
<span data-ttu-id="5ea95-123">Полная спецификация autoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="5ea95-123">The complete spec of an AutoscaleSetting</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSAutoscaleSetting
Parameter Sets: UpdateAutoscaleSetting
Aliases: SettingSpec

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ea95-124">-Location</span><span class="sxs-lookup"><span data-stu-id="5ea95-124">-Location</span></span>
<span data-ttu-id="5ea95-125">Определяет расположение параметра автомасштабации.</span><span class="sxs-lookup"><span data-stu-id="5ea95-125">Specifies the location of the Autoscale setting.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateAutoscaleSetting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ea95-126">-Name</span><span class="sxs-lookup"><span data-stu-id="5ea95-126">-Name</span></span>
<span data-ttu-id="5ea95-127">Имя создаваемого параметра автомасштабии.</span><span class="sxs-lookup"><span data-stu-id="5ea95-127">Specifies the name of the Autoscale setting to create.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateAutoscaleSetting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ea95-128">-Notification</span><span class="sxs-lookup"><span data-stu-id="5ea95-128">-Notification</span></span>
<span data-ttu-id="5ea95-129">Список уведомлений, разделенных запятой.</span><span class="sxs-lookup"><span data-stu-id="5ea95-129">Specifies a list of comma-separated notifications.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ea95-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ea95-130">-ResourceGroupName</span></span>
<span data-ttu-id="5ea95-131">Имя группы ресурсов для ресурса, связанного с параметром "Автомасштаб".</span><span class="sxs-lookup"><span data-stu-id="5ea95-131">Specifies the name of the resource group for the resource associated with the Autoscale setting.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ea95-132">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="5ea95-132">-TargetResourceId</span></span>
<span data-ttu-id="5ea95-133">Определяет ИД ресурса для автоматической шкалы.</span><span class="sxs-lookup"><span data-stu-id="5ea95-133">Specifies the ID of the resource to autoscale.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateAutoscaleSetting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ea95-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5ea95-134">-Confirm</span></span>
<span data-ttu-id="5ea95-135">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ea95-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ea95-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ea95-136">-WhatIf</span></span>
<span data-ttu-id="5ea95-137">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ea95-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5ea95-138">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="5ea95-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ea95-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ea95-139">CommonParameters</span></span>
<span data-ttu-id="5ea95-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ea95-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ea95-141">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5ea95-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ea95-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5ea95-142">INPUTS</span></span>

### <span data-ttu-id="5ea95-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="5ea95-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSAutoscaleSetting</span></span>

### <span data-ttu-id="5ea95-144">System.String</span><span class="sxs-lookup"><span data-stu-id="5ea95-144">System.String</span></span>

### <span data-ttu-id="5ea95-145">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="5ea95-145">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="5ea95-146">System.Collections.Generic.List'1[[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="5ea95-146">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="5ea95-147">System.Collections.Generic.List'1[[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="5ea95-147">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="5ea95-148">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5ea95-148">OUTPUTS</span></span>

### <span data-ttu-id="5ea95-149">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAutoscaleSettingOperationResponse</span><span class="sxs-lookup"><span data-stu-id="5ea95-149">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAutoscaleSettingOperationResponse</span></span>

## <span data-ttu-id="5ea95-150">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5ea95-150">NOTES</span></span>

## <span data-ttu-id="5ea95-151">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5ea95-151">RELATED LINKS</span></span>

[<span data-ttu-id="5ea95-152">Get-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="5ea95-152">Get-AzAutoscaleSetting</span></span>](./Get-AzAutoscaleSetting.md)

[<span data-ttu-id="5ea95-153">New-AzAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="5ea95-153">New-AzAutoscaleProfile</span></span>](./New-AzAutoscaleProfile.md)

[<span data-ttu-id="5ea95-154">New-AzAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="5ea95-154">New-AzAutoscaleRule</span></span>](./New-AzAutoscaleRule.md)

[<span data-ttu-id="5ea95-155">Remove-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="5ea95-155">Remove-AzAutoscaleSetting</span></span>](./Remove-AzAutoscaleSetting.md)



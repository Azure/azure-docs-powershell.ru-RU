---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 7436F31F-9DCB-4365-BA6D-41BDB5D7FCB6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/add-azurermautoscalesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmAutoscaleSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmAutoscaleSetting.md
ms.openlocfilehash: 08e7558bb357c930749cf4a93bfa428560c64395
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569024"
---
# <span data-ttu-id="c1e35-101">Add-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="c1e35-101">Add-AzureRmAutoscaleSetting</span></span>

## <span data-ttu-id="c1e35-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c1e35-102">SYNOPSIS</span></span>
<span data-ttu-id="c1e35-103">Создание параметра автомасштабирования.</span><span class="sxs-lookup"><span data-stu-id="c1e35-103">Creates an Autoscale setting.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c1e35-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c1e35-104">SYNTAX</span></span>

### <span data-ttu-id="c1e35-105">UpdateAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="c1e35-105">UpdateAutoscaleSetting</span></span>
```
Add-AzureRmAutoscaleSetting -SettingSpec <PSAutoscaleSetting> -ResourceGroupName <String> [-DisableSetting]
 [-AutoscaleProfile <System.Collections.Generic.List`1[Microsoft.Azure.Management.Insights.Models.AutoscaleProfile]>]
 [-Notification <System.Collections.Generic.List`1[Microsoft.Azure.Management.Insights.Models.AutoscaleNotification]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c1e35-106">CreateAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="c1e35-106">CreateAutoscaleSetting</span></span>
```
Add-AzureRmAutoscaleSetting -Location <String> -Name <String> -ResourceGroupName <String> [-DisableSetting]
 [-AutoscaleProfile <System.Collections.Generic.List`1[Microsoft.Azure.Management.Insights.Models.AutoscaleProfile]>]
 -TargetResourceId <String>
 [-Notification <System.Collections.Generic.List`1[Microsoft.Azure.Management.Insights.Models.AutoscaleNotification]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c1e35-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c1e35-107">DESCRIPTION</span></span>
<span data-ttu-id="c1e35-108">Командлет **Add-AzureRmAutoscaleSetting** создает параметр автомасштабирования.</span><span class="sxs-lookup"><span data-stu-id="c1e35-108">The **Add-AzureRmAutoscaleSetting** cmdlet creates an Autoscale setting.</span></span>

<span data-ttu-id="c1e35-109">Этот командлет реализует шаблон ShouldProcess, т. е. может запросить подтверждение от пользователя, прежде чем действительно создать, изменить или удалить ресурс.</span><span class="sxs-lookup"><span data-stu-id="c1e35-109">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="c1e35-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c1e35-110">EXAMPLES</span></span>

### <span data-ttu-id="c1e35-111">Пример 1: Создание параметра автомасштабирования</span><span class="sxs-lookup"><span data-stu-id="c1e35-111">Example 1: Create an Autoscale setting</span></span>
```
PS C:\>$Rule1 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"

PS C:\> $Profile1 = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -StartTimeWindow 2015-03-05T14:00:00 -EndTimeWindow 2015-03-05T14:30:00 -TimeWindowTimeZone GMT -Rules $Rule1, $Rule2 -Name "adios"

PS C:\> $Profile2 = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rules $Rule1, $Rule2 -Name "SecondProfileName" -RecurrenceFrequency Minute -ScheduleDays "1", "2", "3" -ScheduleHours 5, 10, 15 -ScheduleMinutes 15, 30, 45 -ScheduleTimeZone GMT

PS C:\> Add-AzureRmAutoscaleSetting -Location "East US" -Name "MySetting" -ResourceGroupName "Default-Web-EastUS" -TargetResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm" -AutoscaleProfiles $Profile1, $Profile2
```

<span data-ttu-id="c1e35-112">Первые две команды используют New-AzureRmAutoscaleRule для создания двух правил автомасштабирования $Rule 1 и $Rule 2.</span><span class="sxs-lookup"><span data-stu-id="c1e35-112">The first two commands use New-AzureRmAutoscaleRule to create two Autoscale rules, $Rule1 and $Rule2.</span></span>

<span data-ttu-id="c1e35-113">Третья и четвертая команды используют New-AzureRmAutoscaleProfile для создания профилей автомасштабирования $Profile 1 и $Profile 2 с помощью $Rule 1 и $Rule 2.</span><span class="sxs-lookup"><span data-stu-id="c1e35-113">The third and fourth commands use New-AzureRmAutoscaleProfile to create Autoscale profiles, $Profile1 and $Profile2, using $Rule1 and $Rule2.</span></span>

<span data-ttu-id="c1e35-114">Последняя команда создает параметр автомасштабирования с помощью профилей в $Profile 1 и $Profile 2.</span><span class="sxs-lookup"><span data-stu-id="c1e35-114">The final command creates an Autoscale setting using the profiles in $Profile1 and $Profile2.</span></span>

## <span data-ttu-id="c1e35-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c1e35-115">PARAMETERS</span></span>

### <span data-ttu-id="c1e35-116">-AutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="c1e35-116">-AutoscaleProfile</span></span>
<span data-ttu-id="c1e35-117">Задает список профилей, которые нужно добавить к параметру автомасштабирования, или $Null, чтобы добавить профиль без профиля.</span><span class="sxs-lookup"><span data-stu-id="c1e35-117">Specifies a list of profiles to add to the Autoscale setting, or $Null to add no profile.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile]
Parameter Sets: (All)
Aliases: AutoscaleProfiles

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1e35-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1e35-118">-DefaultProfile</span></span>
<span data-ttu-id="c1e35-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="c1e35-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1e35-120">-DisableSetting</span><span class="sxs-lookup"><span data-stu-id="c1e35-120">-DisableSetting</span></span>
<span data-ttu-id="c1e35-121">Отключение существующего параметра автомасштабирования.</span><span class="sxs-lookup"><span data-stu-id="c1e35-121">Disables an existing Autoscale setting.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1e35-122">-Location</span><span class="sxs-lookup"><span data-stu-id="c1e35-122">-Location</span></span>
<span data-ttu-id="c1e35-123">Задает расположение параметра автомасштабирования.</span><span class="sxs-lookup"><span data-stu-id="c1e35-123">Specifies the location of the Autoscale setting.</span></span>

```yaml
Type: String
Parameter Sets: CreateAutoscaleSetting
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1e35-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c1e35-124">-Name</span></span>
<span data-ttu-id="c1e35-125">Задает имя создаваемого параметра автомасштабирования.</span><span class="sxs-lookup"><span data-stu-id="c1e35-125">Specifies the name of the Autoscale setting to create.</span></span>

```yaml
Type: String
Parameter Sets: CreateAutoscaleSetting
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1e35-126">-Уведомление</span><span class="sxs-lookup"><span data-stu-id="c1e35-126">-Notification</span></span>
<span data-ttu-id="c1e35-127">Задает список уведомлений с разделителями-запятыми.</span><span class="sxs-lookup"><span data-stu-id="c1e35-127">Specifies a list of comma-separated notifications.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification]
Parameter Sets: (All)
Aliases: Notifications

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1e35-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1e35-128">-ResourceGroupName</span></span>
<span data-ttu-id="c1e35-129">Указывает имя группы ресурсов для ресурса, связанного с параметром автомасштабирования.</span><span class="sxs-lookup"><span data-stu-id="c1e35-129">Specifies the name of the resource group for the resource associated with the Autoscale setting.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1e35-130">-SettingSpec</span><span class="sxs-lookup"><span data-stu-id="c1e35-130">-SettingSpec</span></span>
<span data-ttu-id="c1e35-131">Указывает объект **AutoscaleSetting** .</span><span class="sxs-lookup"><span data-stu-id="c1e35-131">Specifies an **AutoscaleSetting** object.</span></span>
<span data-ttu-id="c1e35-132">Чтобы получить объект **AutoscaleSetting** , можно использовать командлет Get-AzureRmAutoscaleSetting или создать его в сценарии Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c1e35-132">You can use the Get-AzureRmAutoscaleSetting cmdlet to get an **AutoscaleSetting** object or you can construct one in a Windows PowerShell script.</span></span>

```yaml
Type: PSAutoscaleSetting
Parameter Sets: Parameters for Add-AzureRmAutoscaleSetting cmdlet in the update semantics
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1e35-133">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="c1e35-133">-TargetResourceId</span></span>
<span data-ttu-id="c1e35-134">Указывает идентификатор ресурса для автомасштабирования.</span><span class="sxs-lookup"><span data-stu-id="c1e35-134">Specifies the ID of the resource to autoscale.</span></span>

```yaml
Type: String
Parameter Sets: CreateAutoscaleSetting
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1e35-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1e35-135">CommonParameters</span></span>
<span data-ttu-id="c1e35-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c1e35-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1e35-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1e35-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1e35-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c1e35-138">INPUTS</span></span>

### <span data-ttu-id="c1e35-139">Ничего</span><span class="sxs-lookup"><span data-stu-id="c1e35-139">None</span></span>
<span data-ttu-id="c1e35-140">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="c1e35-140">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c1e35-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c1e35-141">OUTPUTS</span></span>

### <span data-ttu-id="c1e35-142">Microsoft. Azure. Commands. Insights. OutputClasses. PSAddAutoscaleSettingOperationResponse</span><span class="sxs-lookup"><span data-stu-id="c1e35-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAutoscaleSettingOperationResponse</span></span>

## <span data-ttu-id="c1e35-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="c1e35-143">NOTES</span></span>

## <span data-ttu-id="c1e35-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c1e35-144">RELATED LINKS</span></span>

[<span data-ttu-id="c1e35-145">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="c1e35-145">Get-AzureRmAutoscaleSetting</span></span>](./Get-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="c1e35-146">New-AzureRmAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="c1e35-146">New-AzureRmAutoscaleProfile</span></span>](./New-AzureRmAutoscaleProfile.md)

[<span data-ttu-id="c1e35-147">New-AzureRmAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="c1e35-147">New-AzureRmAutoscaleRule</span></span>](./New-AzureRmAutoscaleRule.md)

[<span data-ttu-id="c1e35-148">Remove-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="c1e35-148">Remove-AzureRmAutoscaleSetting</span></span>](./Remove-AzureRmAutoscaleSetting.md)



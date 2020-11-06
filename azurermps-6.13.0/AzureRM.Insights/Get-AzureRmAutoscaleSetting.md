---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 989CE245-FD1D-4E1D-90A2-2D7DA3975D0B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermautoscalesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmAutoscaleSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmAutoscaleSetting.md
ms.openlocfilehash: 6bf59522b09d9a8a5c301860ab175eef8f7537b8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567755"
---
# <span data-ttu-id="1eaaf-101">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="1eaaf-101">Get-AzureRmAutoscaleSetting</span></span>

## <span data-ttu-id="1eaaf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1eaaf-102">SYNOPSIS</span></span>
<span data-ttu-id="1eaaf-103">Получает параметры автомасштабирования.</span><span class="sxs-lookup"><span data-stu-id="1eaaf-103">Gets Autoscale settings.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1eaaf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1eaaf-104">SYNTAX</span></span>

```
Get-AzureRmAutoscaleSetting -ResourceGroupName <String> [-Name <String>] [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1eaaf-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1eaaf-105">DESCRIPTION</span></span>
<span data-ttu-id="1eaaf-106">Командлет **Get-AzureRmAutoscaleSetting** получает все параметры автомасштабирования, связанные с группой ресурсов или с указанным параметром автомасштабирования.</span><span class="sxs-lookup"><span data-stu-id="1eaaf-106">The **Get-AzureRmAutoscaleSetting** cmdlet gets all Autoscale settings associated with a resource group or a specified Autoscale setting.</span></span>

## <span data-ttu-id="1eaaf-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1eaaf-107">EXAMPLES</span></span>

### <span data-ttu-id="1eaaf-108">Пример 1: получение параметров автомасштабирования</span><span class="sxs-lookup"><span data-stu-id="1eaaf-108">Example 1: Get Autoscale settings</span></span>
```
PS C:\>Get-AzureRmAutoscaleSetting -ResourceGroup "Default-Web-EastUS" -DetailedOutput
resourceId : /subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft. 
             insights/autoscalesettings/DefaultServerFarm-Default-Web-EastUS
Location   : East US
Name       : DefaultServerFarm-Default-Web-EastUS
Properties : 
Enabled    : True
Profiles   : 
Capacity   : 
Default    : 1
Minimum    : 3
Maximum    : 1
FixedDate     : 
Name          : No scheduled times
Recurrence    : 
Rules         : 
MetricTrigger : 
MetricName         : CpuPercentage
MetricResourceId   : /subscriptions/a93fb07c-6c93-40be-bf3b-4f0deba10f4
             b/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm
Operator           : GreaterThanOrEqual
Statistic          : Average
Threshold          : 14
TimeAggregation    : Average
TimeGrain          : 00:01:00
TimeWindow         : 00:45:00
ScaleAction        : 
Cooldown   : 00:05:00
Direction  : Increase
Type       : ChangeCount
Value      : 1
MetricTrigger  : 
MetricName         : CpuPercentage
MetricResourceId  : /subscriptions/a93fb07c-6c93-40be-bf3b-4f0deba10f4
             b/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm
Operator           : LessThanOrEqual
Statistic          : Average
Threshold          : 4
TimeAggregation    : Average
TimeGrain          : 00:01:00
TimeWindow         : 00:45:00
ScaleAction  : 
Cooldown   : 02:00:00
Direction  : Decrease
Type       : ChangeCount
Value      : 1

MetricTrigger  : 
MetricName         : BytesReceived
MetricResourceId  : /subscriptions/a93fb07c-6c93-40be-bf3b-4f0deba10f4
             b/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm
Operator           : LessThanOrEqual
Statistic          : Average
Threshold          : 50
TimeAggregation    : Average
TimeGrain          : 00:01:00
TimeWindow         : 00:10:00
ScaleAction    : 
Cooldown   : 00:10:00
Direction  : Decrease
Type       : ChangeCount
Value      : 1
MetricTrigger  : 
MetricName         : BytesReceived
MetricResourceId  : /subscriptions/a93fb07c-6c93-40be-bf3b-4f0deba10f4
             b/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm
Operator           : GreaterThanOrEqual
Statistic          : Average
Threshold          : 100
                                                TimeAggregation    : Average
TimeGrain          : 00:01:00
TimeWindow         : 00:05:00
ScaleAction    : 
Cooldown   : 00:10:00
                                                Direction  : Increase
Type       : ChangeCount
Value      : 1
             TargetResourceId : /subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/
             providers/microsoft.web/serverFarms/DefaultServerFarm
Tags       : {[$type, Microsoft.WindowsAzure.Management.Common.Storage.CasePreservedDictionary, 
             Microsoft.WindowsAzure.Management.Common.Storage], [hidden-link:/subscriptions/a93fb07c-6c93-40be-bf3b-4f0
             deba10f4b/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm, 
             Resource]}
```

<span data-ttu-id="1eaaf-109">Эта команда получает параметры автомасштабирования, назначенные группе ресурсов Default-Web-EastUS.</span><span class="sxs-lookup"><span data-stu-id="1eaaf-109">This command gets the Autoscale settings assigned to the resource group Default-Web-EastUS.</span></span>

### <span data-ttu-id="1eaaf-110">Пример 2: получение параметров автомасштабирования по имени</span><span class="sxs-lookup"><span data-stu-id="1eaaf-110">Example 2: Get an Autoscale setting by name</span></span>
```
PS C:\>Get-AzureRmAutoscaleSetting -ResourceGroupName "Default-Web-EastUS" -Name "DefaultServerFarm-Default-Web-EastUS" -DetailedOutput
resourceId : /subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft. 
             insights/autoscalesettings/DefaultServerFarm-Default-Web-EastUS
Location   : East US
Name       : DefaultServerFarm-Default-Web-EastUS
Properties : 
Enabled    : True
Profiles   : 
Capacity   : 
Default    : 1
Minimum    : 3
Maximum    : 1
FixedDate     : 
Name          : No scheduled times
Recurrence    : 
Rules         : 
MetricTrigger : 
MetricName         : CpuPercentage
MetricResourceId   : /subscriptions/a93fb07c-6c93-40be-bf3b-4f0deba10f4
             b/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm
Operator           : GreaterThanOrEqual
Statistic          : Average
Threshold          : 14
TimeAggregation    : Average
TimeGrain          : 00:01:00
TimeWindow         : 00:45:00
ScaleAction    : 
Cooldown   : 00:05:00
Direction  : Increase
Type       : ChangeCount
Value      : 1
MetricTrigger  : 
MetricName         : CpuPercentage
MetricResourceId  : /subscriptions/a93fb07c-6c93-40be-bf3b-4f0deba10f4
             b/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm
Operator           : LessThanOrEqual
Statistic          : Average
Threshold          : 4
TimeAggregation    : Average
TimeGrain          : 00:01:00
TimeWindow         : 00:45:00
ScaleAction    : 
Cooldown   : 02:00:00
Direction  : Decrease
Type       : ChangeCount
Value      : 1
MetricTrigger  : 
MetricName         : BytesReceived
MetricResourceId  : /subscriptions/a93fb07c-6c93-40be-bf3b-4f0deba10f4
             b/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm
Operator           : LessThanOrEqual
Statistic          : Average
Threshold          : 50
TimeAggregation    : Average
TimeGrain          : 00:01:00
TimeWindow         : 00:10:00
ScaleAction    : 
Cooldown   : 00:10:00
Direction  : Decrease
Type       : ChangeCount
Value      : 1
MetricTrigger  : 
MetricName         : BytesReceived
MetricResourceId  : /subscriptions/a93fb07c-6c93-40be-bf3b-4f0deba10f4
             b/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm
Operator           : GreaterThanOrEqual
Statistic          : Average
Threshold          : 100
TimeAggregation    : Average
TimeGrain          : 00:01:00
TimeWindow         : 00:05:00
ScaleAction    : 
Cooldown   : 00:10:00
Direction  : Increase
Type       : ChangeCount
Value      : 1
TargetResourceId : /subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/
             providers/microsoft.web/serverFarms/DefaultServerFarm
Tags       : {[$type, Microsoft.WindowsAzure.Management.Common.Storage.CasePreservedDictionary, 
             Microsoft.WindowsAzure.Management.Common.Storage], [hidden-link:/subscriptions/a93fb07c-6c93-40be-bf3b-4f0
             deba10f4b/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm, 
             Resource]}
```

<span data-ttu-id="1eaaf-111">Эта команда получает параметр автомасштабирования с именем DefaultServerFarm-Default-Web-EastUS.</span><span class="sxs-lookup"><span data-stu-id="1eaaf-111">This command gets the Autoscale setting named DefaultServerFarm-Default-Web-EastUS.</span></span>

## <span data-ttu-id="1eaaf-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1eaaf-112">PARAMETERS</span></span>

### <span data-ttu-id="1eaaf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1eaaf-113">-DefaultProfile</span></span>
<span data-ttu-id="1eaaf-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="1eaaf-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1eaaf-115">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="1eaaf-115">-DetailedOutput</span></span>
<span data-ttu-id="1eaaf-116">Указывает на то, что эта операция отображает полные сведения в выходных данных.</span><span class="sxs-lookup"><span data-stu-id="1eaaf-116">Indicates that this operation displays full details in the output.</span></span>

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

### <span data-ttu-id="1eaaf-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1eaaf-117">-Name</span></span>
<span data-ttu-id="1eaaf-118">Указывает имя получаемого параметра.</span><span class="sxs-lookup"><span data-stu-id="1eaaf-118">Specifies the name of the setting to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1eaaf-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1eaaf-119">-ResourceGroupName</span></span>
<span data-ttu-id="1eaaf-120">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1eaaf-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="1eaaf-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1eaaf-121">CommonParameters</span></span>
<span data-ttu-id="1eaaf-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1eaaf-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1eaaf-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1eaaf-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1eaaf-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1eaaf-124">INPUTS</span></span>

### <span data-ttu-id="1eaaf-125">System. String</span><span class="sxs-lookup"><span data-stu-id="1eaaf-125">System.String</span></span>

### <span data-ttu-id="1eaaf-126">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="1eaaf-126">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="1eaaf-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1eaaf-127">OUTPUTS</span></span>

### <span data-ttu-id="1eaaf-128">Microsoft. Azure. Commands. Insights. OutputClasses. PSAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="1eaaf-128">Microsoft.Azure.Commands.Insights.OutputClasses.PSAutoscaleSetting</span></span>

## <span data-ttu-id="1eaaf-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="1eaaf-129">NOTES</span></span>

## <span data-ttu-id="1eaaf-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1eaaf-130">RELATED LINKS</span></span>

[<span data-ttu-id="1eaaf-131">Add-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="1eaaf-131">Add-AzureRmAutoscaleSetting</span></span>](./Add-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="1eaaf-132">Remove-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="1eaaf-132">Remove-AzureRmAutoscaleSetting</span></span>](./Remove-AzureRmAutoscaleSetting.md)



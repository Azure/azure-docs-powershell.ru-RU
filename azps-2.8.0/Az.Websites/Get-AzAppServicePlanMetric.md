---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 0AC0C4F9-4138-49EA-88CB-DC220DE7E9F4
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azappserviceplanmetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzAppServicePlanMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzAppServicePlanMetric.md
ms.openlocfilehash: 04f07e435f8656ef18e452538d97b3728179c969
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93907658"
---
# <span data-ttu-id="89a62-101">Get-AzAppServicePlanMetric</span><span class="sxs-lookup"><span data-stu-id="89a62-101">Get-AzAppServicePlanMetric</span></span>

## <span data-ttu-id="89a62-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="89a62-102">SYNOPSIS</span></span>

## <span data-ttu-id="89a62-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="89a62-103">SYNTAX</span></span>

### <span data-ttu-id="89a62-104">Состояний</span><span class="sxs-lookup"><span data-stu-id="89a62-104">S1</span></span>
```
Get-AzAppServicePlanMetric [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="89a62-105">S2</span><span class="sxs-lookup"><span data-stu-id="89a62-105">S2</span></span>
```
Get-AzAppServicePlanMetric [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-AppServicePlan] <PSAppServicePlan>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="89a62-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="89a62-106">DESCRIPTION</span></span>
<span data-ttu-id="89a62-107">**Get-AzAppServicePlanMetric** получает метрики плана служб приложений.</span><span class="sxs-lookup"><span data-stu-id="89a62-107">The **Get-AzAppServicePlanMetric** gets App Service Plan metrics.</span></span>

## <span data-ttu-id="89a62-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="89a62-108">EXAMPLES</span></span>

### <span data-ttu-id="89a62-109">1:</span><span class="sxs-lookup"><span data-stu-id="89a62-109">1:</span></span>
```
PS C:\>Get-AzAppServicePlanMetric -ResourceGroupName "Default-Web-WestUS" -Name "ContosoAppServPlan" -StartTime 2016-11-30T22:00:00Z -EndTime 2016-11-30T22:30:00Z -Granularity PT1M -Metrics "CPU Percentage"
```

<span data-ttu-id="89a62-110">Эта команда возвращает процент ЦП для плана служб приложений в минуту (PT1M — время опроса 1 минута) между StartTime и EndTime.</span><span class="sxs-lookup"><span data-stu-id="89a62-110">This command gets CPU percentage of the App Service Plan per minute(PT1M - Poll Time 1 minute) between StartTime and EndTime</span></span>

## <span data-ttu-id="89a62-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="89a62-111">PARAMETERS</span></span>

### <span data-ttu-id="89a62-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="89a62-112">-AppServicePlan</span></span>
<span data-ttu-id="89a62-113">Объект плана служб приложений</span><span class="sxs-lookup"><span data-stu-id="89a62-113">App Service Plan Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="89a62-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89a62-114">-DefaultProfile</span></span>
<span data-ttu-id="89a62-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="89a62-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="89a62-116">-EndTime</span><span class="sxs-lookup"><span data-stu-id="89a62-116">-EndTime</span></span>
<span data-ttu-id="89a62-117">Время окончания в формате UTC</span><span class="sxs-lookup"><span data-stu-id="89a62-117">End Time in UTC</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89a62-118">-Гранулярность</span><span class="sxs-lookup"><span data-stu-id="89a62-118">-Granularity</span></span>
<span data-ttu-id="89a62-119">Детализации</span><span class="sxs-lookup"><span data-stu-id="89a62-119">Granularity</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PT1M, PT1H, P1D

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89a62-120">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="89a62-120">-InstanceDetails</span></span>
<span data-ttu-id="89a62-121">Сведения об экземпляре</span><span class="sxs-lookup"><span data-stu-id="89a62-121">Instance Details</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89a62-122">-Метрики</span><span class="sxs-lookup"><span data-stu-id="89a62-122">-Metrics</span></span>
<span data-ttu-id="89a62-123">Метрик</span><span class="sxs-lookup"><span data-stu-id="89a62-123">Metrics</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89a62-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="89a62-124">-Name</span></span>
<span data-ttu-id="89a62-125">Имя плана служб приложений</span><span class="sxs-lookup"><span data-stu-id="89a62-125">App Service Plan Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89a62-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89a62-126">-ResourceGroupName</span></span>
<span data-ttu-id="89a62-127">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="89a62-127">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89a62-128">-StartTime</span><span class="sxs-lookup"><span data-stu-id="89a62-128">-StartTime</span></span>
<span data-ttu-id="89a62-129">Время начала в формате UTC</span><span class="sxs-lookup"><span data-stu-id="89a62-129">Start Time in UTC</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89a62-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89a62-130">CommonParameters</span></span>
<span data-ttu-id="89a62-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="89a62-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89a62-132">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="89a62-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89a62-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="89a62-133">INPUTS</span></span>

### <span data-ttu-id="89a62-134">Microsoft. Azure. Commands. Apps. WebApp. PSAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="89a62-134">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="89a62-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="89a62-135">OUTPUTS</span></span>

### <span data-ttu-id="89a62-136">Microsoft. Azure. Management. website. Models. ResourceMetric</span><span class="sxs-lookup"><span data-stu-id="89a62-136">Microsoft.Azure.Management.WebSites.Models.ResourceMetric</span></span>

## <span data-ttu-id="89a62-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="89a62-137">NOTES</span></span>

## <span data-ttu-id="89a62-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="89a62-138">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 0AC0C4F9-4138-49EA-88CB-DC220DE7E9F4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermappserviceplanmetrics
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmAppServicePlanMetrics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmAppServicePlanMetrics.md
ms.openlocfilehash: a8bb330315cfdd43e30ab790afcdeba0b09cef08
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565298"
---
# <span data-ttu-id="c25ca-101">Get-AzureRmAppServicePlanMetrics</span><span class="sxs-lookup"><span data-stu-id="c25ca-101">Get-AzureRmAppServicePlanMetrics</span></span>

## <span data-ttu-id="c25ca-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c25ca-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c25ca-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c25ca-103">SYNTAX</span></span>

### <span data-ttu-id="c25ca-104">Состояний</span><span class="sxs-lookup"><span data-stu-id="c25ca-104">S1</span></span>
```
Get-AzureRmAppServicePlanMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c25ca-105">S2</span><span class="sxs-lookup"><span data-stu-id="c25ca-105">S2</span></span>
```
Get-AzureRmAppServicePlanMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-AppServicePlan] <PSAppServicePlan>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c25ca-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c25ca-106">DESCRIPTION</span></span>
<span data-ttu-id="c25ca-107">**Get-AzureRmAppServicePlanMetrics** получает метрики плана служб приложений.</span><span class="sxs-lookup"><span data-stu-id="c25ca-107">The **Get-AzureRmAppServicePlanMetrics** gets App Service Plan metrics.</span></span>

## <span data-ttu-id="c25ca-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c25ca-108">EXAMPLES</span></span>

### <span data-ttu-id="c25ca-109">1:</span><span class="sxs-lookup"><span data-stu-id="c25ca-109">1:</span></span>
```
PS C:\>Get-AzureRmAppServicePlanMetrics -ResourceGroupName "Default-Web-WestUS" -Name "ContosoAppServPlan" -StartTime 2016-11-30T22:00:00Z -EndTime 2016-11-30T22:30:00Z -Granularity PT1M -Metrics "CPU Percentage"
```

<span data-ttu-id="c25ca-110">Эта команда возвращает процент ЦП для плана служб приложений в минуту (PT1M — время опроса 1 минута) между StartTime и EndTime.</span><span class="sxs-lookup"><span data-stu-id="c25ca-110">This command gets CPU percentage of the App Service Plan per minute(PT1M - Poll Time 1 minute) between StartTime and EndTime</span></span>

## <span data-ttu-id="c25ca-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c25ca-111">PARAMETERS</span></span>

### <span data-ttu-id="c25ca-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="c25ca-112">-AppServicePlan</span></span>
<span data-ttu-id="c25ca-113">Объект плана служб приложений</span><span class="sxs-lookup"><span data-stu-id="c25ca-113">App Service Plan Object</span></span>

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

### <span data-ttu-id="c25ca-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c25ca-114">-DefaultProfile</span></span>
<span data-ttu-id="c25ca-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c25ca-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c25ca-116">-EndTime</span><span class="sxs-lookup"><span data-stu-id="c25ca-116">-EndTime</span></span>
<span data-ttu-id="c25ca-117">Время окончания в формате UTC</span><span class="sxs-lookup"><span data-stu-id="c25ca-117">End Time in UTC</span></span>

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

### <span data-ttu-id="c25ca-118">-Гранулярность</span><span class="sxs-lookup"><span data-stu-id="c25ca-118">-Granularity</span></span>
<span data-ttu-id="c25ca-119">Детализации</span><span class="sxs-lookup"><span data-stu-id="c25ca-119">Granularity</span></span>

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

### <span data-ttu-id="c25ca-120">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="c25ca-120">-InstanceDetails</span></span>
<span data-ttu-id="c25ca-121">Сведения об экземпляре</span><span class="sxs-lookup"><span data-stu-id="c25ca-121">Instance Details</span></span>

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

### <span data-ttu-id="c25ca-122">-Метрики</span><span class="sxs-lookup"><span data-stu-id="c25ca-122">-Metrics</span></span>
<span data-ttu-id="c25ca-123">Метрик</span><span class="sxs-lookup"><span data-stu-id="c25ca-123">Metrics</span></span>

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

### <span data-ttu-id="c25ca-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c25ca-124">-Name</span></span>
<span data-ttu-id="c25ca-125">Имя плана служб приложений</span><span class="sxs-lookup"><span data-stu-id="c25ca-125">App Service Plan Name</span></span>

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

### <span data-ttu-id="c25ca-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c25ca-126">-ResourceGroupName</span></span>
<span data-ttu-id="c25ca-127">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="c25ca-127">Resource Group Name</span></span>

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

### <span data-ttu-id="c25ca-128">-StartTime</span><span class="sxs-lookup"><span data-stu-id="c25ca-128">-StartTime</span></span>
<span data-ttu-id="c25ca-129">Время начала в формате UTC</span><span class="sxs-lookup"><span data-stu-id="c25ca-129">Start Time in UTC</span></span>

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

### <span data-ttu-id="c25ca-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c25ca-130">CommonParameters</span></span>
<span data-ttu-id="c25ca-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c25ca-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c25ca-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c25ca-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c25ca-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c25ca-133">INPUTS</span></span>

### <span data-ttu-id="c25ca-134">Microsoft. Azure. Management. website. Models. AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="c25ca-134">Microsoft.Azure.Management.WebSites.Models.AppServicePlan</span></span>
<span data-ttu-id="c25ca-135">Параметры: AppServicePlan (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c25ca-135">Parameters: AppServicePlan (ByValue)</span></span>

## <span data-ttu-id="c25ca-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c25ca-136">OUTPUTS</span></span>

### <span data-ttu-id="c25ca-137">Microsoft. Azure. Management. website. Models. ResourceMetric</span><span class="sxs-lookup"><span data-stu-id="c25ca-137">Microsoft.Azure.Management.WebSites.Models.ResourceMetric</span></span>

## <span data-ttu-id="c25ca-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="c25ca-138">NOTES</span></span>

## <span data-ttu-id="c25ca-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c25ca-139">RELATED LINKS</span></span>

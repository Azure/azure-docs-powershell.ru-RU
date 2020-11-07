---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 0AC0C4F9-4138-49EA-88CB-DC220DE7E9F4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermappserviceplanmetrics
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmAppServicePlanMetrics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmAppServicePlanMetrics.md
ms.openlocfilehash: f3376f40246640b8de52ffa138912c768486a3dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733529"
---
# <span data-ttu-id="bdec1-101">Get-AzureRmAppServicePlanMetrics</span><span class="sxs-lookup"><span data-stu-id="bdec1-101">Get-AzureRmAppServicePlanMetrics</span></span>

## <span data-ttu-id="bdec1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bdec1-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bdec1-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bdec1-103">SYNTAX</span></span>

### <span data-ttu-id="bdec1-104">Состояний</span><span class="sxs-lookup"><span data-stu-id="bdec1-104">S1</span></span>
```
Get-AzureRmAppServicePlanMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bdec1-105">S2</span><span class="sxs-lookup"><span data-stu-id="bdec1-105">S2</span></span>
```
Get-AzureRmAppServicePlanMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-AppServicePlan] <ServerFarmWithRichSku>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bdec1-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bdec1-106">DESCRIPTION</span></span>
<span data-ttu-id="bdec1-107">**Get-AzureRmAppServicePlanMetrics** получает метрики плана служб приложений.</span><span class="sxs-lookup"><span data-stu-id="bdec1-107">The **Get-AzureRmAppServicePlanMetrics** gets App Service Plan metrics.</span></span>

## <span data-ttu-id="bdec1-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bdec1-108">EXAMPLES</span></span>

### <span data-ttu-id="bdec1-109">1:</span><span class="sxs-lookup"><span data-stu-id="bdec1-109">1:</span></span>
```
PS C:\>Get-AzureRmAppServicePlanMetrics -ResourceGroupName "Default-Web-WestUS" -Name "ContosoAppServPlan" -StartTime 2016-11-30T22:00:00Z -EndTime 2016-11-30T22:30:00Z -Granularity PT1M -Metrics ["CPU Percentage"]
```

<span data-ttu-id="bdec1-110">Эта команда возвращает процент ЦП для плана служб приложений в минуту (PT1M — время опроса 1 минута) между StartTime и EndTime.</span><span class="sxs-lookup"><span data-stu-id="bdec1-110">This command gets CPU percentage of the App Service Plan per minute(PT1M - Poll Time 1 minute) between StartTime and EndTime</span></span>

## <span data-ttu-id="bdec1-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bdec1-111">PARAMETERS</span></span>

### <span data-ttu-id="bdec1-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="bdec1-112">-AppServicePlan</span></span>
<span data-ttu-id="bdec1-113">Объект плана служб приложений</span><span class="sxs-lookup"><span data-stu-id="bdec1-113">App Service Plan Object</span></span>

```yaml
Type: ServerFarmWithRichSku
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bdec1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdec1-114">-DefaultProfile</span></span>
<span data-ttu-id="bdec1-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bdec1-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bdec1-116">-EndTime</span><span class="sxs-lookup"><span data-stu-id="bdec1-116">-EndTime</span></span>
<span data-ttu-id="bdec1-117">Время окончания в формате UTC</span><span class="sxs-lookup"><span data-stu-id="bdec1-117">End Time in UTC</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdec1-118">-Гранулярность</span><span class="sxs-lookup"><span data-stu-id="bdec1-118">-Granularity</span></span>
<span data-ttu-id="bdec1-119">Детализации</span><span class="sxs-lookup"><span data-stu-id="bdec1-119">Granularity</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PT1M, PT1H, P1D

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdec1-120">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="bdec1-120">-InstanceDetails</span></span>
<span data-ttu-id="bdec1-121">Сведения об экземпляре</span><span class="sxs-lookup"><span data-stu-id="bdec1-121">Instance Details</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdec1-122">-Метрики</span><span class="sxs-lookup"><span data-stu-id="bdec1-122">-Metrics</span></span>
<span data-ttu-id="bdec1-123">Метрик</span><span class="sxs-lookup"><span data-stu-id="bdec1-123">Metrics</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdec1-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="bdec1-124">-Name</span></span>
<span data-ttu-id="bdec1-125">Имя плана служб приложений</span><span class="sxs-lookup"><span data-stu-id="bdec1-125">App Service Plan Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdec1-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bdec1-126">-ResourceGroupName</span></span>
<span data-ttu-id="bdec1-127">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="bdec1-127">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdec1-128">-StartTime</span><span class="sxs-lookup"><span data-stu-id="bdec1-128">-StartTime</span></span>
<span data-ttu-id="bdec1-129">Время начала в формате UTC</span><span class="sxs-lookup"><span data-stu-id="bdec1-129">Start Time in UTC</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdec1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdec1-130">CommonParameters</span></span>
<span data-ttu-id="bdec1-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bdec1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdec1-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bdec1-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdec1-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bdec1-133">INPUTS</span></span>

### <span data-ttu-id="bdec1-134">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="bdec1-134">ServerFarmWithRichSku</span></span>
<span data-ttu-id="bdec1-135">Параметр "AppServicePlan" принимает значение типа "ServerFarmWithRichSku" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="bdec1-135">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="bdec1-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bdec1-136">OUTPUTS</span></span>

## <span data-ttu-id="bdec1-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="bdec1-137">NOTES</span></span>

## <span data-ttu-id="bdec1-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bdec1-138">RELATED LINKS</span></span>


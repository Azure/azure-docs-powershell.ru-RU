---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 0AC0C4F9-4138-49EA-88CB-DC220DE7E9F4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermappserviceplanmetrics
schema: 2.0.0
ms.openlocfilehash: 097b4c5ff6a4a9be32889f104c8e2c8fe0058b13
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913254"
---
# <span data-ttu-id="79a4c-101">Get-AzureRmAppServicePlanMetrics</span><span class="sxs-lookup"><span data-stu-id="79a4c-101">Get-AzureRmAppServicePlanMetrics</span></span>

## <span data-ttu-id="79a4c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="79a4c-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="79a4c-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="79a4c-103">SYNTAX</span></span>

### <span data-ttu-id="79a4c-104">Состояний</span><span class="sxs-lookup"><span data-stu-id="79a4c-104">S1</span></span>
```
Get-AzureRmAppServicePlanMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="79a4c-105">S2</span><span class="sxs-lookup"><span data-stu-id="79a4c-105">S2</span></span>
```
Get-AzureRmAppServicePlanMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-AppServicePlan] <AppServicePlan>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="79a4c-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="79a4c-106">DESCRIPTION</span></span>
<span data-ttu-id="79a4c-107">**Get-AzureRmAppServicePlanMetrics** получает метрики плана служб приложений.</span><span class="sxs-lookup"><span data-stu-id="79a4c-107">The **Get-AzureRmAppServicePlanMetrics** gets App Service Plan metrics.</span></span>

## <span data-ttu-id="79a4c-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="79a4c-108">EXAMPLES</span></span>

### <span data-ttu-id="79a4c-109">1:</span><span class="sxs-lookup"><span data-stu-id="79a4c-109">1:</span></span>
```
PS C:\>Get-AzureRmAppServicePlanMetrics -ResourceGroupName "Default-Web-WestUS" -Name "ContosoAppServPlan" -StartTime 2016-11-30T22:00:00Z -EndTime 2016-11-30T22:30:00Z -Granularity PT1M -Metrics ["CPU Percentage"]
```

<span data-ttu-id="79a4c-110">Эта команда возвращает процент ЦП для плана служб приложений в минуту (PT1M — время опроса 1 минута) между StartTime и EndTime.</span><span class="sxs-lookup"><span data-stu-id="79a4c-110">This command gets CPU percentage of the App Service Plan per minute(PT1M - Poll Time 1 minute) between StartTime and EndTime</span></span>

## <span data-ttu-id="79a4c-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="79a4c-111">PARAMETERS</span></span>

### <span data-ttu-id="79a4c-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="79a4c-112">-AppServicePlan</span></span>
<span data-ttu-id="79a4c-113">Объект плана служб приложений</span><span class="sxs-lookup"><span data-stu-id="79a4c-113">App Service Plan Object</span></span>

```yaml
Type: AppServicePlan
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="79a4c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79a4c-114">-DefaultProfile</span></span>
<span data-ttu-id="79a4c-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="79a4c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="79a4c-116">-EndTime</span><span class="sxs-lookup"><span data-stu-id="79a4c-116">-EndTime</span></span>
<span data-ttu-id="79a4c-117">Время окончания в формате UTC</span><span class="sxs-lookup"><span data-stu-id="79a4c-117">End Time in UTC</span></span>

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

### <span data-ttu-id="79a4c-118">-Гранулярность</span><span class="sxs-lookup"><span data-stu-id="79a4c-118">-Granularity</span></span>
<span data-ttu-id="79a4c-119">Детализации</span><span class="sxs-lookup"><span data-stu-id="79a4c-119">Granularity</span></span>

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

### <span data-ttu-id="79a4c-120">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="79a4c-120">-InstanceDetails</span></span>
<span data-ttu-id="79a4c-121">Сведения об экземпляре</span><span class="sxs-lookup"><span data-stu-id="79a4c-121">Instance Details</span></span>

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

### <span data-ttu-id="79a4c-122">-Метрики</span><span class="sxs-lookup"><span data-stu-id="79a4c-122">-Metrics</span></span>
<span data-ttu-id="79a4c-123">Метрик</span><span class="sxs-lookup"><span data-stu-id="79a4c-123">Metrics</span></span>

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

### <span data-ttu-id="79a4c-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="79a4c-124">-Name</span></span>
<span data-ttu-id="79a4c-125">Имя плана служб приложений</span><span class="sxs-lookup"><span data-stu-id="79a4c-125">App Service Plan Name</span></span>

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

### <span data-ttu-id="79a4c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79a4c-126">-ResourceGroupName</span></span>
<span data-ttu-id="79a4c-127">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="79a4c-127">Resource Group Name</span></span>

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

### <span data-ttu-id="79a4c-128">-StartTime</span><span class="sxs-lookup"><span data-stu-id="79a4c-128">-StartTime</span></span>
<span data-ttu-id="79a4c-129">Время начала в формате UTC</span><span class="sxs-lookup"><span data-stu-id="79a4c-129">Start Time in UTC</span></span>

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

### <span data-ttu-id="79a4c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79a4c-130">CommonParameters</span></span>
<span data-ttu-id="79a4c-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="79a4c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79a4c-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79a4c-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79a4c-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="79a4c-133">INPUTS</span></span>

### <span data-ttu-id="79a4c-134">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="79a4c-134">ServerFarmWithRichSku</span></span>
<span data-ttu-id="79a4c-135">Параметр "AppServicePlan" принимает значение типа "ServerFarmWithRichSku" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="79a4c-135">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="79a4c-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="79a4c-136">OUTPUTS</span></span>

## <span data-ttu-id="79a4c-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="79a4c-137">NOTES</span></span>

## <span data-ttu-id="79a4c-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="79a4c-138">RELATED LINKS</span></span>


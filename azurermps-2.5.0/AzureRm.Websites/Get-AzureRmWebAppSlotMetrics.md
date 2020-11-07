---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 3BCEADF3-15DC-4033-A94A-4C8B4F5E7340
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappslotmetrics
schema: 2.0.0
ms.openlocfilehash: 9393a2aebbde94dcb42989e80b2763198576f408
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914345"
---
# <span data-ttu-id="71c91-101">Get-AzureRmWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="71c91-101">Get-AzureRmWebAppSlotMetrics</span></span>

## <span data-ttu-id="71c91-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="71c91-102">SYNOPSIS</span></span>
<span data-ttu-id="71c91-103">Получает метрики для области веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="71c91-103">Gets metrics for an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="71c91-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="71c91-104">SYNTAX</span></span>

### <span data-ttu-id="71c91-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="71c91-105">S1</span></span>
```
Get-AzureRmWebAppSlotMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="71c91-106">S2</span><span class="sxs-lookup"><span data-stu-id="71c91-106">S2</span></span>
```
Get-AzureRmWebAppSlotMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="71c91-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="71c91-107">DESCRIPTION</span></span>
<span data-ttu-id="71c91-108">**Get-AzureRmWebAppSlotMetrics** получает метрики веб-приложения для заданной ячейки.</span><span class="sxs-lookup"><span data-stu-id="71c91-108">The **Get-AzureRmWebAppSlotMetrics** gets Web App metrics for the specified slot.</span></span>

## <span data-ttu-id="71c91-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="71c91-109">EXAMPLES</span></span>

### <span data-ttu-id="71c91-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="71c91-110">Example 1</span></span>
```
PS C:\> Get-AzureRmAppServicePlanMetrics -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StartTime 2016-11-30T22:00:00Z -EndTime 2016-11-30T22:30:00Z -Granularity PT1M -Metrics ["Requests"]
```

<span data-ttu-id="71c91-111">Эта команда получает запрос указанного веб-приложения в минуту (PT1M — время опроса 1 минута) между StartTime и EndTime.</span><span class="sxs-lookup"><span data-stu-id="71c91-111">This command gets Request of the specified Web App per minute(PT1M - Poll Time 1 minute) between StartTime and EndTime</span></span>

## <span data-ttu-id="71c91-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="71c91-112">PARAMETERS</span></span>

### <span data-ttu-id="71c91-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71c91-113">-DefaultProfile</span></span>
<span data-ttu-id="71c91-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="71c91-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="71c91-115">-EndTime</span><span class="sxs-lookup"><span data-stu-id="71c91-115">-EndTime</span></span>
<span data-ttu-id="71c91-116">Время окончания в формате UTC</span><span class="sxs-lookup"><span data-stu-id="71c91-116">End Time in UTC</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71c91-117">-Гранулярность</span><span class="sxs-lookup"><span data-stu-id="71c91-117">-Granularity</span></span>
<span data-ttu-id="71c91-118">Детализации</span><span class="sxs-lookup"><span data-stu-id="71c91-118">Granularity</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71c91-119">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="71c91-119">-InstanceDetails</span></span>
<span data-ttu-id="71c91-120">Сведения об экземпляре</span><span class="sxs-lookup"><span data-stu-id="71c91-120">Instance Details</span></span>

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

### <span data-ttu-id="71c91-121">-Метрики</span><span class="sxs-lookup"><span data-stu-id="71c91-121">-Metrics</span></span>
<span data-ttu-id="71c91-122">Метрик</span><span class="sxs-lookup"><span data-stu-id="71c91-122">Metrics</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71c91-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="71c91-123">-Name</span></span>
<span data-ttu-id="71c91-124">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="71c91-124">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71c91-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71c91-125">-ResourceGroupName</span></span>
<span data-ttu-id="71c91-126">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="71c91-126">Resource Group Name</span></span>

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

### <span data-ttu-id="71c91-127">-Slot</span><span class="sxs-lookup"><span data-stu-id="71c91-127">-Slot</span></span>
<span data-ttu-id="71c91-128">Название гнезда WebApp</span><span class="sxs-lookup"><span data-stu-id="71c91-128">WebApp Slot Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71c91-129">-StartTime</span><span class="sxs-lookup"><span data-stu-id="71c91-129">-StartTime</span></span>
<span data-ttu-id="71c91-130">Время начала в формате UTC</span><span class="sxs-lookup"><span data-stu-id="71c91-130">Start Time in UTC</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71c91-131">-WebApp</span><span class="sxs-lookup"><span data-stu-id="71c91-131">-WebApp</span></span>
<span data-ttu-id="71c91-132">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="71c91-132">WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="71c91-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71c91-133">CommonParameters</span></span>
<span data-ttu-id="71c91-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="71c91-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71c91-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71c91-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71c91-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="71c91-136">INPUTS</span></span>

### <span data-ttu-id="71c91-137">Семейств</span><span class="sxs-lookup"><span data-stu-id="71c91-137">Site</span></span>
<span data-ttu-id="71c91-138">Параметр "WebApp" принимает значение типа "сайт" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="71c91-138">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="71c91-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="71c91-139">OUTPUTS</span></span>

## <span data-ttu-id="71c91-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="71c91-140">NOTES</span></span>

## <span data-ttu-id="71c91-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="71c91-141">RELATED LINKS</span></span>

[<span data-ttu-id="71c91-142">Get-AzureRMAppServicePlanMetrics</span><span class="sxs-lookup"><span data-stu-id="71c91-142">Get-AzureRMAppServicePlanMetrics</span></span>](./Get-AzureRmAppServicePlanMetrics.md)

[<span data-ttu-id="71c91-143">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="71c91-143">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="71c91-144">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="71c91-144">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

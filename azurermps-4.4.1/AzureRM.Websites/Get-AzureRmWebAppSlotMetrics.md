---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 3BCEADF3-15DC-4033-A94A-4C8B4F5E7340
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlotMetrics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlotMetrics.md
ms.openlocfilehash: 93af61d0554435fae4b9d87170b9202026644e49
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568664"
---
# <span data-ttu-id="283ef-101">Get-AzureRmWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="283ef-101">Get-AzureRmWebAppSlotMetrics</span></span>

## <span data-ttu-id="283ef-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="283ef-102">SYNOPSIS</span></span>
<span data-ttu-id="283ef-103">Получает метрики для области веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="283ef-103">Gets metrics for an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="283ef-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="283ef-104">SYNTAX</span></span>

### <span data-ttu-id="283ef-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="283ef-105">S1</span></span>
```
Get-AzureRmWebAppSlotMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="283ef-106">S2</span><span class="sxs-lookup"><span data-stu-id="283ef-106">S2</span></span>
```
Get-AzureRmWebAppSlotMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="283ef-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="283ef-107">DESCRIPTION</span></span>
<span data-ttu-id="283ef-108">**Get-AzureRmWebAppSlotMetrics** получает метрики веб-приложения для заданной ячейки.</span><span class="sxs-lookup"><span data-stu-id="283ef-108">The **Get-AzureRmWebAppSlotMetrics** gets Web App metrics for the specified slot.</span></span>

## <span data-ttu-id="283ef-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="283ef-109">EXAMPLES</span></span>

### <span data-ttu-id="283ef-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="283ef-110">Example 1</span></span>
```
PS C:\> Get-AzureRmAppServicePlanMetrics -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StartTime 2016-11-30T22:00:00Z -EndTime 2016-11-30T22:30:00Z -Granularity PT1M -Metrics ["Requests"]
```

<span data-ttu-id="283ef-111">Эта команда получает запрос указанного веб-приложения в минуту (PT1M — время опроса 1 минута) между StartTime и EndTime.</span><span class="sxs-lookup"><span data-stu-id="283ef-111">This command gets Request of the specified Web App per minute(PT1M - Poll Time 1 minute) between StartTime and EndTime</span></span>

## <span data-ttu-id="283ef-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="283ef-112">PARAMETERS</span></span>

### <span data-ttu-id="283ef-113">-EndTime</span><span class="sxs-lookup"><span data-stu-id="283ef-113">-EndTime</span></span>
<span data-ttu-id="283ef-114">Время окончания в формате UTC</span><span class="sxs-lookup"><span data-stu-id="283ef-114">End Time in UTC</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="283ef-115">-Гранулярность</span><span class="sxs-lookup"><span data-stu-id="283ef-115">-Granularity</span></span>
<span data-ttu-id="283ef-116">Детализации</span><span class="sxs-lookup"><span data-stu-id="283ef-116">Granularity</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="283ef-117">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="283ef-117">-InstanceDetails</span></span>
<span data-ttu-id="283ef-118">Сведения об экземпляре</span><span class="sxs-lookup"><span data-stu-id="283ef-118">Instance Details</span></span>

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

### <span data-ttu-id="283ef-119">-Метрики</span><span class="sxs-lookup"><span data-stu-id="283ef-119">-Metrics</span></span>
<span data-ttu-id="283ef-120">Метрик</span><span class="sxs-lookup"><span data-stu-id="283ef-120">Metrics</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="283ef-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="283ef-121">-Name</span></span>
<span data-ttu-id="283ef-122">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="283ef-122">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="283ef-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="283ef-123">-ResourceGroupName</span></span>
<span data-ttu-id="283ef-124">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="283ef-124">Resource Group Name</span></span>

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

### <span data-ttu-id="283ef-125">-Slot</span><span class="sxs-lookup"><span data-stu-id="283ef-125">-Slot</span></span>
<span data-ttu-id="283ef-126">Название гнезда WebApp</span><span class="sxs-lookup"><span data-stu-id="283ef-126">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="283ef-127">-StartTime</span><span class="sxs-lookup"><span data-stu-id="283ef-127">-StartTime</span></span>
<span data-ttu-id="283ef-128">Время начала в формате UTC</span><span class="sxs-lookup"><span data-stu-id="283ef-128">Start Time in UTC</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="283ef-129">-WebApp</span><span class="sxs-lookup"><span data-stu-id="283ef-129">-WebApp</span></span>
<span data-ttu-id="283ef-130">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="283ef-130">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="283ef-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="283ef-131">-DefaultProfile</span></span>
<span data-ttu-id="283ef-132">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="283ef-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="283ef-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="283ef-133">CommonParameters</span></span>
<span data-ttu-id="283ef-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="283ef-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="283ef-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="283ef-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="283ef-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="283ef-136">INPUTS</span></span>

### <span data-ttu-id="283ef-137">Семейств</span><span class="sxs-lookup"><span data-stu-id="283ef-137">Site</span></span>
<span data-ttu-id="283ef-138">Параметр "WebApp" принимает значение типа "сайт" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="283ef-138">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="283ef-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="283ef-139">OUTPUTS</span></span>

## <span data-ttu-id="283ef-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="283ef-140">NOTES</span></span>

## <span data-ttu-id="283ef-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="283ef-141">RELATED LINKS</span></span>

[<span data-ttu-id="283ef-142">Get-AzureRMAppServicePlanMetrics</span><span class="sxs-lookup"><span data-stu-id="283ef-142">Get-AzureRMAppServicePlanMetrics</span></span>](./Get-AzureRmAppServicePlanMetrics.md)

[<span data-ttu-id="283ef-143">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="283ef-143">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="283ef-144">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="283ef-144">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

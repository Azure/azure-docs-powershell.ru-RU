---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 3BCEADF3-15DC-4033-A94A-4C8B4F5E7340
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappslotmetrics
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlotMetrics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlotMetrics.md
ms.openlocfilehash: 9c336c1bb2c2485c5bef691a5d5560a1b8795360
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93556440"
---
# <span data-ttu-id="53226-101">Get-AzureRmWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="53226-101">Get-AzureRmWebAppSlotMetrics</span></span>

## <span data-ttu-id="53226-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="53226-102">SYNOPSIS</span></span>
<span data-ttu-id="53226-103">Получает метрики для области веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="53226-103">Gets metrics for an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="53226-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="53226-104">SYNTAX</span></span>

### <span data-ttu-id="53226-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="53226-105">S1</span></span>
```
Get-AzureRmWebAppSlotMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="53226-106">S2</span><span class="sxs-lookup"><span data-stu-id="53226-106">S2</span></span>
```
Get-AzureRmWebAppSlotMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="53226-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="53226-107">DESCRIPTION</span></span>
<span data-ttu-id="53226-108">**Get-AzureRmWebAppSlotMetrics** получает метрики веб-приложения для заданной ячейки.</span><span class="sxs-lookup"><span data-stu-id="53226-108">The **Get-AzureRmWebAppSlotMetrics** gets Web App metrics for the specified slot.</span></span>

## <span data-ttu-id="53226-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="53226-109">EXAMPLES</span></span>

### <span data-ttu-id="53226-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="53226-110">Example 1</span></span>
```
PS C:\> Get-AzureRmAppServicePlanMetrics -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StartTime 2016-11-30T22:00:00Z -EndTime 2016-11-30T22:30:00Z -Granularity PT1M -Metrics ["Requests"]
```

<span data-ttu-id="53226-111">Эта команда получает запрос указанного веб-приложения в минуту (PT1M — время опроса 1 минута) между StartTime и EndTime.</span><span class="sxs-lookup"><span data-stu-id="53226-111">This command gets Request of the specified Web App per minute(PT1M - Poll Time 1 minute) between StartTime and EndTime</span></span>

## <span data-ttu-id="53226-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="53226-112">PARAMETERS</span></span>

### <span data-ttu-id="53226-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53226-113">-DefaultProfile</span></span>
<span data-ttu-id="53226-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="53226-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="53226-115">-EndTime</span><span class="sxs-lookup"><span data-stu-id="53226-115">-EndTime</span></span>
<span data-ttu-id="53226-116">Время окончания в формате UTC</span><span class="sxs-lookup"><span data-stu-id="53226-116">End Time in UTC</span></span>

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

### <span data-ttu-id="53226-117">-Гранулярность</span><span class="sxs-lookup"><span data-stu-id="53226-117">-Granularity</span></span>
<span data-ttu-id="53226-118">Детализации</span><span class="sxs-lookup"><span data-stu-id="53226-118">Granularity</span></span>

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

### <span data-ttu-id="53226-119">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="53226-119">-InstanceDetails</span></span>
<span data-ttu-id="53226-120">Сведения об экземпляре</span><span class="sxs-lookup"><span data-stu-id="53226-120">Instance Details</span></span>

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

### <span data-ttu-id="53226-121">-Метрики</span><span class="sxs-lookup"><span data-stu-id="53226-121">-Metrics</span></span>
<span data-ttu-id="53226-122">Метрик</span><span class="sxs-lookup"><span data-stu-id="53226-122">Metrics</span></span>

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

### <span data-ttu-id="53226-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="53226-123">-Name</span></span>
<span data-ttu-id="53226-124">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="53226-124">WebApp Name</span></span>

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

### <span data-ttu-id="53226-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53226-125">-ResourceGroupName</span></span>
<span data-ttu-id="53226-126">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="53226-126">Resource Group Name</span></span>

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

### <span data-ttu-id="53226-127">-Slot</span><span class="sxs-lookup"><span data-stu-id="53226-127">-Slot</span></span>
<span data-ttu-id="53226-128">Название гнезда WebApp</span><span class="sxs-lookup"><span data-stu-id="53226-128">WebApp Slot Name</span></span>

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

### <span data-ttu-id="53226-129">-StartTime</span><span class="sxs-lookup"><span data-stu-id="53226-129">-StartTime</span></span>
<span data-ttu-id="53226-130">Время начала в формате UTC</span><span class="sxs-lookup"><span data-stu-id="53226-130">Start Time in UTC</span></span>

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

### <span data-ttu-id="53226-131">-WebApp</span><span class="sxs-lookup"><span data-stu-id="53226-131">-WebApp</span></span>
<span data-ttu-id="53226-132">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="53226-132">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="53226-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53226-133">CommonParameters</span></span>
<span data-ttu-id="53226-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="53226-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53226-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53226-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53226-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="53226-136">INPUTS</span></span>

### <span data-ttu-id="53226-137">System. String</span><span class="sxs-lookup"><span data-stu-id="53226-137">System.String</span></span>

### <span data-ttu-id="53226-138">Microsoft. Azure. Management. website. Models. site</span><span class="sxs-lookup"><span data-stu-id="53226-138">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="53226-139">Параметры: WebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="53226-139">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="53226-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="53226-140">OUTPUTS</span></span>

### <span data-ttu-id="53226-141">Microsoft. Azure. Management. website. Models. ResourceMetric</span><span class="sxs-lookup"><span data-stu-id="53226-141">Microsoft.Azure.Management.WebSites.Models.ResourceMetric</span></span>

## <span data-ttu-id="53226-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="53226-142">NOTES</span></span>

## <span data-ttu-id="53226-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="53226-143">RELATED LINKS</span></span>

[<span data-ttu-id="53226-144">Get-AzureRMAppServicePlanMetrics</span><span class="sxs-lookup"><span data-stu-id="53226-144">Get-AzureRMAppServicePlanMetrics</span></span>](./Get-AzureRmAppServicePlanMetrics.md)

[<span data-ttu-id="53226-145">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="53226-145">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="53226-146">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="53226-146">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

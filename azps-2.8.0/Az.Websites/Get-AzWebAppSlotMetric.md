---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 3BCEADF3-15DC-4033-A94A-4C8B4F5E7340
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappslotmetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotMetric.md
ms.openlocfilehash: 696332f18074108fd0294248223777c15be0435d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93907757"
---
# <span data-ttu-id="7ee99-101">Get-AzWebAppSlotMetric</span><span class="sxs-lookup"><span data-stu-id="7ee99-101">Get-AzWebAppSlotMetric</span></span>

## <span data-ttu-id="7ee99-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7ee99-102">SYNOPSIS</span></span>
<span data-ttu-id="7ee99-103">Получает метрики для области веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="7ee99-103">Gets metrics for an Azure Web App slot.</span></span>

## <span data-ttu-id="7ee99-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7ee99-104">SYNTAX</span></span>

### <span data-ttu-id="7ee99-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="7ee99-105">S1</span></span>
```
Get-AzWebAppSlotMetric [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7ee99-106">S2</span><span class="sxs-lookup"><span data-stu-id="7ee99-106">S2</span></span>
```
Get-AzWebAppSlotMetric [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7ee99-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7ee99-107">DESCRIPTION</span></span>
<span data-ttu-id="7ee99-108">**Get-AzWebAppSlotMetric** получает метрики веб-приложения для заданной ячейки.</span><span class="sxs-lookup"><span data-stu-id="7ee99-108">The **Get-AzWebAppSlotMetric** gets Web App metrics for the specified slot.</span></span>

## <span data-ttu-id="7ee99-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7ee99-109">EXAMPLES</span></span>

### <span data-ttu-id="7ee99-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7ee99-110">Example 1</span></span>
```
PS C:\> Get-AzWebAppSlotMetric -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StartTime 2016-11-30T22:00:00Z -EndTime 2016-11-30T22:30:00Z -Granularity PT1M -Metrics ["Requests"]
```

<span data-ttu-id="7ee99-111">Эта команда получает запрос указанного веб-приложения в минуту (PT1M — время опроса 1 минута) между StartTime и EndTime.</span><span class="sxs-lookup"><span data-stu-id="7ee99-111">This command gets Request of the specified Web App per minute(PT1M - Poll Time 1 minute) between StartTime and EndTime</span></span>

## <span data-ttu-id="7ee99-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7ee99-112">PARAMETERS</span></span>

### <span data-ttu-id="7ee99-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ee99-113">-DefaultProfile</span></span>
<span data-ttu-id="7ee99-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7ee99-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7ee99-115">-EndTime</span><span class="sxs-lookup"><span data-stu-id="7ee99-115">-EndTime</span></span>
<span data-ttu-id="7ee99-116">Время окончания в формате UTC</span><span class="sxs-lookup"><span data-stu-id="7ee99-116">End Time in UTC</span></span>

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

### <span data-ttu-id="7ee99-117">-Гранулярность</span><span class="sxs-lookup"><span data-stu-id="7ee99-117">-Granularity</span></span>
<span data-ttu-id="7ee99-118">Детализации</span><span class="sxs-lookup"><span data-stu-id="7ee99-118">Granularity</span></span>

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

### <span data-ttu-id="7ee99-119">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="7ee99-119">-InstanceDetails</span></span>
<span data-ttu-id="7ee99-120">Сведения об экземпляре</span><span class="sxs-lookup"><span data-stu-id="7ee99-120">Instance Details</span></span>

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

### <span data-ttu-id="7ee99-121">-Метрики</span><span class="sxs-lookup"><span data-stu-id="7ee99-121">-Metrics</span></span>
<span data-ttu-id="7ee99-122">Метрик</span><span class="sxs-lookup"><span data-stu-id="7ee99-122">Metrics</span></span>

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

### <span data-ttu-id="7ee99-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7ee99-123">-Name</span></span>
<span data-ttu-id="7ee99-124">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="7ee99-124">WebApp Name</span></span>

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

### <span data-ttu-id="7ee99-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ee99-125">-ResourceGroupName</span></span>
<span data-ttu-id="7ee99-126">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="7ee99-126">Resource Group Name</span></span>

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

### <span data-ttu-id="7ee99-127">-Slot</span><span class="sxs-lookup"><span data-stu-id="7ee99-127">-Slot</span></span>
<span data-ttu-id="7ee99-128">Название гнезда WebApp</span><span class="sxs-lookup"><span data-stu-id="7ee99-128">WebApp Slot Name</span></span>

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

### <span data-ttu-id="7ee99-129">-StartTime</span><span class="sxs-lookup"><span data-stu-id="7ee99-129">-StartTime</span></span>
<span data-ttu-id="7ee99-130">Время начала в формате UTC</span><span class="sxs-lookup"><span data-stu-id="7ee99-130">Start Time in UTC</span></span>

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

### <span data-ttu-id="7ee99-131">-WebApp</span><span class="sxs-lookup"><span data-stu-id="7ee99-131">-WebApp</span></span>
<span data-ttu-id="7ee99-132">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="7ee99-132">WebApp Object</span></span>

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

### <span data-ttu-id="7ee99-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ee99-133">CommonParameters</span></span>
<span data-ttu-id="7ee99-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7ee99-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ee99-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7ee99-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ee99-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7ee99-136">INPUTS</span></span>

### <span data-ttu-id="7ee99-137">System. String</span><span class="sxs-lookup"><span data-stu-id="7ee99-137">System.String</span></span>

### <span data-ttu-id="7ee99-138">Microsoft. Azure. Commands. Apps. PSSite</span><span class="sxs-lookup"><span data-stu-id="7ee99-138">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="7ee99-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7ee99-139">OUTPUTS</span></span>

### <span data-ttu-id="7ee99-140">Microsoft. Azure. Management. website. Models. ResourceMetric</span><span class="sxs-lookup"><span data-stu-id="7ee99-140">Microsoft.Azure.Management.WebSites.Models.ResourceMetric</span></span>

## <span data-ttu-id="7ee99-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="7ee99-141">NOTES</span></span>

## <span data-ttu-id="7ee99-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7ee99-142">RELATED LINKS</span></span>

[<span data-ttu-id="7ee99-143">Get-AzAppServicePlanMetric</span><span class="sxs-lookup"><span data-stu-id="7ee99-143">Get-AzAppServicePlanMetric</span></span>](./Get-AzAppServicePlanMetric.md)

[<span data-ttu-id="7ee99-144">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="7ee99-144">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="7ee99-145">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="7ee99-145">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

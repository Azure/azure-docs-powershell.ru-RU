---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 513BE097-EB4A-4C49-9F7F-42A2BED09022
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappmetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppMetric.md
ms.openlocfilehash: 91b5de48805e458b771227ca9c92e9891be170e1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244657"
---
# <span data-ttu-id="d30ab-101">Get-AzWebAppMetric</span><span class="sxs-lookup"><span data-stu-id="d30ab-101">Get-AzWebAppMetric</span></span>

## <span data-ttu-id="d30ab-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d30ab-102">SYNOPSIS</span></span>
<span data-ttu-id="d30ab-103">Получает метрики веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="d30ab-103">Gets Azure Web App metrics.</span></span>

## <span data-ttu-id="d30ab-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d30ab-104">SYNTAX</span></span>

### <span data-ttu-id="d30ab-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="d30ab-105">S1</span></span>
```
Get-AzWebAppMetric [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d30ab-106">S2</span><span class="sxs-lookup"><span data-stu-id="d30ab-106">S2</span></span>
```
Get-AzWebAppMetric [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d30ab-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d30ab-107">DESCRIPTION</span></span>
<span data-ttu-id="d30ab-108">**Get-AzWebAppMetric** получает метрики веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="d30ab-108">The **Get-AzWebAppMetric** gets Web App metrics.</span></span>

## <span data-ttu-id="d30ab-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d30ab-109">EXAMPLES</span></span>

### <span data-ttu-id="d30ab-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d30ab-110">Example 1</span></span>
```
PS C:\> Get-AzAppServicePlanMetric -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StartTime 2016-11-30T22:00:00Z -EndTime 2016-11-30T22:30:00Z -Granularity PT1M -Metrics "Requests"
```

<span data-ttu-id="d30ab-111">Эта команда получает запросы на веб-приложение ContosoWebApp в минуту (PT1M — время опроса 1 минута) между StartTime и EndTime.</span><span class="sxs-lookup"><span data-stu-id="d30ab-111">This command gets Requests of the Web App ContosoWebApp per minute(PT1M - Poll Time 1 minute) between StartTime and EndTime</span></span>

## <span data-ttu-id="d30ab-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d30ab-112">PARAMETERS</span></span>

### <span data-ttu-id="d30ab-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d30ab-113">-DefaultProfile</span></span>
<span data-ttu-id="d30ab-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d30ab-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d30ab-115">-EndTime</span><span class="sxs-lookup"><span data-stu-id="d30ab-115">-EndTime</span></span>
<span data-ttu-id="d30ab-116">Время окончания в формате UTC</span><span class="sxs-lookup"><span data-stu-id="d30ab-116">End Time in UTC</span></span>

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

### <span data-ttu-id="d30ab-117">-Гранулярность</span><span class="sxs-lookup"><span data-stu-id="d30ab-117">-Granularity</span></span>
<span data-ttu-id="d30ab-118">Детализации</span><span class="sxs-lookup"><span data-stu-id="d30ab-118">Granularity</span></span>

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

### <span data-ttu-id="d30ab-119">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="d30ab-119">-InstanceDetails</span></span>
<span data-ttu-id="d30ab-120">Сведения об экземпляре</span><span class="sxs-lookup"><span data-stu-id="d30ab-120">Instance Details</span></span>

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

### <span data-ttu-id="d30ab-121">-Метрики</span><span class="sxs-lookup"><span data-stu-id="d30ab-121">-Metrics</span></span>
<span data-ttu-id="d30ab-122">Метрики в виде массива строк</span><span class="sxs-lookup"><span data-stu-id="d30ab-122">Metrics as a string array</span></span>

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

### <span data-ttu-id="d30ab-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d30ab-123">-Name</span></span>
<span data-ttu-id="d30ab-124">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="d30ab-124">WebApp Name</span></span>

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

### <span data-ttu-id="d30ab-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d30ab-125">-ResourceGroupName</span></span>
<span data-ttu-id="d30ab-126">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="d30ab-126">Resource Group Name</span></span>

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

### <span data-ttu-id="d30ab-127">-StartTime</span><span class="sxs-lookup"><span data-stu-id="d30ab-127">-StartTime</span></span>
<span data-ttu-id="d30ab-128">Время начала в формате UTC</span><span class="sxs-lookup"><span data-stu-id="d30ab-128">Start Time in UTC</span></span>

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

### <span data-ttu-id="d30ab-129">-WebApp</span><span class="sxs-lookup"><span data-stu-id="d30ab-129">-WebApp</span></span>
<span data-ttu-id="d30ab-130">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="d30ab-130">WebApp object</span></span>

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

### <span data-ttu-id="d30ab-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d30ab-131">CommonParameters</span></span>
<span data-ttu-id="d30ab-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d30ab-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d30ab-133">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d30ab-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d30ab-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d30ab-134">INPUTS</span></span>

### <span data-ttu-id="d30ab-135">System. String</span><span class="sxs-lookup"><span data-stu-id="d30ab-135">System.String</span></span>

### <span data-ttu-id="d30ab-136">Microsoft. Azure. Commands. Apps. PSSite</span><span class="sxs-lookup"><span data-stu-id="d30ab-136">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="d30ab-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d30ab-137">OUTPUTS</span></span>

### <span data-ttu-id="d30ab-138">Microsoft. Azure. Management. website. Models. ResourceMetric</span><span class="sxs-lookup"><span data-stu-id="d30ab-138">Microsoft.Azure.Management.WebSites.Models.ResourceMetric</span></span>

## <span data-ttu-id="d30ab-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="d30ab-139">NOTES</span></span>

## <span data-ttu-id="d30ab-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d30ab-140">RELATED LINKS</span></span>

[<span data-ttu-id="d30ab-141">Get-AzWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="d30ab-141">Get-AzWebAppCertificate</span></span>](./Get-AzWebAppCertificate.md)


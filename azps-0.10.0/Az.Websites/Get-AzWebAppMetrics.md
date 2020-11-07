---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 513BE097-EB4A-4C49-9F7F-42A2BED09022
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/get-Azwebappmetrics
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppMetrics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppMetrics.md
ms.openlocfilehash: 9a3aeabc3eb38127b37ca4ab6a12975c51daea5b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910619"
---
# <span data-ttu-id="565b9-101">Get-AzWebAppMetrics</span><span class="sxs-lookup"><span data-stu-id="565b9-101">Get-AzWebAppMetrics</span></span>

## <span data-ttu-id="565b9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="565b9-102">SYNOPSIS</span></span>
<span data-ttu-id="565b9-103">Получает метрики веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="565b9-103">Gets Azure Web App metrics.</span></span>

## <span data-ttu-id="565b9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="565b9-104">SYNTAX</span></span>

### <span data-ttu-id="565b9-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="565b9-105">S1</span></span>
```
Get-AzWebAppMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="565b9-106">S2</span><span class="sxs-lookup"><span data-stu-id="565b9-106">S2</span></span>
```
Get-AzWebAppMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="565b9-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="565b9-107">DESCRIPTION</span></span>
<span data-ttu-id="565b9-108">**Get-AzWebAppMetrics** получает метрики веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="565b9-108">The **Get-AzWebAppMetrics** gets Web App metrics.</span></span>

## <span data-ttu-id="565b9-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="565b9-109">EXAMPLES</span></span>

### <span data-ttu-id="565b9-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="565b9-110">Example 1</span></span>
```
PS C:\> Get-AzAppServicePlanMetrics -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StartTime 2016-11-30T22:00:00Z -EndTime 2016-11-30T22:30:00Z -Granularity PT1M -Metrics ["Requests"]
```

<span data-ttu-id="565b9-111">Эта команда получает запросы на веб-приложение ContosoWebApp в минуту (PT1M — время опроса 1 минута) между StartTime и EndTime.</span><span class="sxs-lookup"><span data-stu-id="565b9-111">This command gets Requests of the Web App ContosoWebApp per minute(PT1M - Poll Time 1 minute) between StartTime and EndTime</span></span>

## <span data-ttu-id="565b9-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="565b9-112">PARAMETERS</span></span>

### <span data-ttu-id="565b9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="565b9-113">-DefaultProfile</span></span>
<span data-ttu-id="565b9-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="565b9-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="565b9-115">-EndTime</span><span class="sxs-lookup"><span data-stu-id="565b9-115">-EndTime</span></span>
<span data-ttu-id="565b9-116">Время окончания в формате UTC</span><span class="sxs-lookup"><span data-stu-id="565b9-116">End Time in UTC</span></span>

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

### <span data-ttu-id="565b9-117">-Гранулярность</span><span class="sxs-lookup"><span data-stu-id="565b9-117">-Granularity</span></span>
<span data-ttu-id="565b9-118">Детализации</span><span class="sxs-lookup"><span data-stu-id="565b9-118">Granularity</span></span>

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

### <span data-ttu-id="565b9-119">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="565b9-119">-InstanceDetails</span></span>
<span data-ttu-id="565b9-120">Сведения об экземпляре</span><span class="sxs-lookup"><span data-stu-id="565b9-120">Instance Details</span></span>

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

### <span data-ttu-id="565b9-121">-Метрики</span><span class="sxs-lookup"><span data-stu-id="565b9-121">-Metrics</span></span>
<span data-ttu-id="565b9-122">Метрики в виде массива строк</span><span class="sxs-lookup"><span data-stu-id="565b9-122">Metrics as a string array</span></span>

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

### <span data-ttu-id="565b9-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="565b9-123">-Name</span></span>
<span data-ttu-id="565b9-124">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="565b9-124">WebApp Name</span></span>

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

### <span data-ttu-id="565b9-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="565b9-125">-ResourceGroupName</span></span>
<span data-ttu-id="565b9-126">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="565b9-126">Resource Group Name</span></span>

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

### <span data-ttu-id="565b9-127">-StartTime</span><span class="sxs-lookup"><span data-stu-id="565b9-127">-StartTime</span></span>
<span data-ttu-id="565b9-128">Время начала в формате UTC</span><span class="sxs-lookup"><span data-stu-id="565b9-128">Start Time in UTC</span></span>

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

### <span data-ttu-id="565b9-129">-WebApp</span><span class="sxs-lookup"><span data-stu-id="565b9-129">-WebApp</span></span>
<span data-ttu-id="565b9-130">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="565b9-130">WebApp object</span></span>

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

### <span data-ttu-id="565b9-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="565b9-131">CommonParameters</span></span>
<span data-ttu-id="565b9-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="565b9-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="565b9-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="565b9-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="565b9-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="565b9-134">INPUTS</span></span>

### <span data-ttu-id="565b9-135">Семейств</span><span class="sxs-lookup"><span data-stu-id="565b9-135">Site</span></span>
<span data-ttu-id="565b9-136">Параметр "WebApp" принимает значение типа "сайт" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="565b9-136">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="565b9-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="565b9-137">OUTPUTS</span></span>

## <span data-ttu-id="565b9-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="565b9-138">NOTES</span></span>

## <span data-ttu-id="565b9-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="565b9-139">RELATED LINKS</span></span>

[<span data-ttu-id="565b9-140">Get-AzWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="565b9-140">Get-AzWebAppCertificate</span></span>](./Get-AzWebAppCertificate.md)


---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 513BE097-EB4A-4C49-9F7F-42A2BED09022
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppMetrics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppMetrics.md
ms.openlocfilehash: 00e8814c72f0e9d52fae2504a41bef3e8e94e7ce
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733070"
---
# <span data-ttu-id="465b6-101">Get-AzureRmWebAppMetrics</span><span class="sxs-lookup"><span data-stu-id="465b6-101">Get-AzureRmWebAppMetrics</span></span>

## <span data-ttu-id="465b6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="465b6-102">SYNOPSIS</span></span>
<span data-ttu-id="465b6-103">Получает метрики веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="465b6-103">Gets Azure Web App metrics.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="465b6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="465b6-104">SYNTAX</span></span>

### <span data-ttu-id="465b6-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="465b6-105">S1</span></span>
```
Get-AzureRmWebAppMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="465b6-106">S2</span><span class="sxs-lookup"><span data-stu-id="465b6-106">S2</span></span>
```
Get-AzureRmWebAppMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="465b6-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="465b6-107">DESCRIPTION</span></span>
<span data-ttu-id="465b6-108">**Get-AzureRmWebAppMetrics** получает метрики веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="465b6-108">The **Get-AzureRmWebAppMetrics** gets Web App metrics.</span></span>

## <span data-ttu-id="465b6-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="465b6-109">EXAMPLES</span></span>

### <span data-ttu-id="465b6-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="465b6-110">Example 1</span></span>
```
PS C:\> Get-AzureRmAppServicePlanMetrics -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StartTime 2016-11-30T22:00:00Z -EndTime 2016-11-30T22:30:00Z -Granularity PT1M -Metrics ["Requests"]
```

<span data-ttu-id="465b6-111">Эта команда получает запросы на веб-приложение ContosoWebApp в минуту (PT1M — время опроса 1 минута) между StartTime и EndTime.</span><span class="sxs-lookup"><span data-stu-id="465b6-111">This command gets Requests of the Web App ContosoWebApp per minute(PT1M - Poll Time 1 minute) between StartTime and EndTime</span></span>

## <span data-ttu-id="465b6-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="465b6-112">PARAMETERS</span></span>

### <span data-ttu-id="465b6-113">-EndTime</span><span class="sxs-lookup"><span data-stu-id="465b6-113">-EndTime</span></span>
<span data-ttu-id="465b6-114">Время окончания в формате UTC</span><span class="sxs-lookup"><span data-stu-id="465b6-114">End Time in UTC</span></span>

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

### <span data-ttu-id="465b6-115">-Гранулярность</span><span class="sxs-lookup"><span data-stu-id="465b6-115">-Granularity</span></span>
<span data-ttu-id="465b6-116">Детализации</span><span class="sxs-lookup"><span data-stu-id="465b6-116">Granularity</span></span>

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

### <span data-ttu-id="465b6-117">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="465b6-117">-InstanceDetails</span></span>
<span data-ttu-id="465b6-118">Сведения об экземпляре</span><span class="sxs-lookup"><span data-stu-id="465b6-118">Instance Details</span></span>

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

### <span data-ttu-id="465b6-119">-Метрики</span><span class="sxs-lookup"><span data-stu-id="465b6-119">-Metrics</span></span>
<span data-ttu-id="465b6-120">Метрики в виде массива строк</span><span class="sxs-lookup"><span data-stu-id="465b6-120">Metrics as a string array</span></span>

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

### <span data-ttu-id="465b6-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="465b6-121">-Name</span></span>
<span data-ttu-id="465b6-122">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="465b6-122">WebApp Name</span></span>

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

### <span data-ttu-id="465b6-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="465b6-123">-ResourceGroupName</span></span>
<span data-ttu-id="465b6-124">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="465b6-124">Resource Group Name</span></span>

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

### <span data-ttu-id="465b6-125">-StartTime</span><span class="sxs-lookup"><span data-stu-id="465b6-125">-StartTime</span></span>
<span data-ttu-id="465b6-126">Время начала в формате UTC</span><span class="sxs-lookup"><span data-stu-id="465b6-126">Start Time in UTC</span></span>

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

### <span data-ttu-id="465b6-127">-WebApp</span><span class="sxs-lookup"><span data-stu-id="465b6-127">-WebApp</span></span>
<span data-ttu-id="465b6-128">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="465b6-128">WebApp object</span></span>

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

### <span data-ttu-id="465b6-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="465b6-129">-DefaultProfile</span></span>
<span data-ttu-id="465b6-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="465b6-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="465b6-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="465b6-131">CommonParameters</span></span>
<span data-ttu-id="465b6-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="465b6-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="465b6-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="465b6-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="465b6-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="465b6-134">INPUTS</span></span>

### <span data-ttu-id="465b6-135">Семейств</span><span class="sxs-lookup"><span data-stu-id="465b6-135">Site</span></span>
<span data-ttu-id="465b6-136">Параметр "WebApp" принимает значение типа "сайт" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="465b6-136">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="465b6-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="465b6-137">OUTPUTS</span></span>

## <span data-ttu-id="465b6-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="465b6-138">NOTES</span></span>

## <span data-ttu-id="465b6-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="465b6-139">RELATED LINKS</span></span>

[<span data-ttu-id="465b6-140">Get-AzureRmWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="465b6-140">Get-AzureRmWebAppCertificate</span></span>](./Get-AzureRmWebAppCertificate.md)


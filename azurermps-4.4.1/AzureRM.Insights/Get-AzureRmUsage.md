---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: CA67985F-C5D5-4CF4-81A4-C35FD769AF0A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmUsage.md
ms.openlocfilehash: 9f02a1c9dfe0c4c41fa1e873201dbeb1d849dd77
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567627"
---
# <span data-ttu-id="ef508-101">Get-AzureRmUsage</span><span class="sxs-lookup"><span data-stu-id="ef508-101">Get-AzureRmUsage</span></span>

## <span data-ttu-id="ef508-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ef508-102">SYNOPSIS</span></span>
<span data-ttu-id="ef508-103">Получает метрики использования для ресурса.</span><span class="sxs-lookup"><span data-stu-id="ef508-103">Gets the usage metrics for a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ef508-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ef508-104">SYNTAX</span></span>

```
Get-AzureRmUsage [-ResourceId] <String> [-ApiVersion <String>] [-StartTime <DateTime>] [-EndTime <DateTime>]
 [-MetricNames <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ef508-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ef508-105">DESCRIPTION</span></span>
<span data-ttu-id="ef508-106">Командлет **Get-AzureRmUsage** получает метрики использования для указанного ресурса.</span><span class="sxs-lookup"><span data-stu-id="ef508-106">The **Get-AzureRmUsage** cmdlet gets the usage metrics for a specified resource.</span></span>

## <span data-ttu-id="ef508-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ef508-107">EXAMPLES</span></span>

### <span data-ttu-id="ef508-108">Пример 1: Получение метрик использования по ИДЕНТИФИКАТОРу ресурса</span><span class="sxs-lookup"><span data-stu-id="ef508-108">Example 1: Get usage metrics by resource ID</span></span>
```
PS C:\>Get-AzureRmUsage -ResourceId "/subscriptions/bcdeb07f-1c43-20be-1f3b-4f0febc10f5b/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/pattifuller"
```

<span data-ttu-id="ef508-109">Эта команда получает метрики использования для указанного веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="ef508-109">This command gets the usage metrics for the specified website.</span></span>

## <span data-ttu-id="ef508-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ef508-110">PARAMETERS</span></span>

### <span data-ttu-id="ef508-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="ef508-111">-ApiVersion</span></span>
<span data-ttu-id="ef508-112">Указывает строку версии API, например 2014-04-01, которая принимается поставщиком ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ef508-112">Specifies an API version string, for example, 2014-04-01, which is accepted by the resource provider.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef508-113">-EndTime</span><span class="sxs-lookup"><span data-stu-id="ef508-113">-EndTime</span></span>
<span data-ttu-id="ef508-114">Указывает дату и время последнего поиска.</span><span class="sxs-lookup"><span data-stu-id="ef508-114">Specifies the latest time and date to search.</span></span>

<span data-ttu-id="ef508-115">Вы можете использовать командлет Get-Date для получения объекта **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="ef508-115">You can use the Get-Date cmdlet to get a **DateTime** object.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef508-116">-MetricNames</span><span class="sxs-lookup"><span data-stu-id="ef508-116">-MetricNames</span></span>
<span data-ttu-id="ef508-117">Указывает массив имен метрик.</span><span class="sxs-lookup"><span data-stu-id="ef508-117">Specifies an array of names of metrics.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef508-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ef508-118">-ResourceId</span></span>
<span data-ttu-id="ef508-119">Указывает идентификатор ресурса для метрики.</span><span class="sxs-lookup"><span data-stu-id="ef508-119">Specifies the ID of the resource for the metric.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef508-120">-StartTime</span><span class="sxs-lookup"><span data-stu-id="ef508-120">-StartTime</span></span>
<span data-ttu-id="ef508-121">Задает самую раннюю дату и время для поиска.</span><span class="sxs-lookup"><span data-stu-id="ef508-121">Specifies the earliest time and date to search.</span></span>

<span data-ttu-id="ef508-122">Вы можете использовать командлет Get-Date для получения объекта **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="ef508-122">You can use the Get-Date cmdlet to get a **DateTime** object.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef508-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef508-123">-DefaultProfile</span></span>
<span data-ttu-id="ef508-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ef508-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ef508-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef508-125">CommonParameters</span></span>
<span data-ttu-id="ef508-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ef508-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef508-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef508-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef508-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ef508-128">INPUTS</span></span>

## <span data-ttu-id="ef508-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ef508-129">OUTPUTS</span></span>

### <span data-ttu-id="ef508-130">Microsoft. Azure. Commands. Insights. OutputClasses. PSUsageMetric []</span><span class="sxs-lookup"><span data-stu-id="ef508-130">Microsoft.Azure.Commands.Insights.OutputClasses.PSUsageMetric[]</span></span>

## <span data-ttu-id="ef508-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="ef508-131">NOTES</span></span>

## <span data-ttu-id="ef508-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ef508-132">RELATED LINKS</span></span>

[<span data-ttu-id="ef508-133">Get-AzureRmMetric</span><span class="sxs-lookup"><span data-stu-id="ef508-133">Get-AzureRmMetric</span></span>](./Get-AzureRmMetric.md)



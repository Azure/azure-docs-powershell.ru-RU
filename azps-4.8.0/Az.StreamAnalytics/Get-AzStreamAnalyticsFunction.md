---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 7F08A880-1FC5-4542-8AB8-927BB999A552
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsFunction.md
ms.openlocfilehash: ceedee89473385202037cfedb23e4373995b6f98
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94080152"
---
# <span data-ttu-id="e0a23-101">Get-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="e0a23-101">Get-AzStreamAnalyticsFunction</span></span>

## <span data-ttu-id="e0a23-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e0a23-102">SYNOPSIS</span></span>
<span data-ttu-id="e0a23-103">Возвращает функции в задании Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="e0a23-103">Gets functions in a Stream Analytics job.</span></span>

## <span data-ttu-id="e0a23-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e0a23-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsFunction [-JobName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e0a23-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e0a23-105">DESCRIPTION</span></span>
<span data-ttu-id="e0a23-106">Командлет **Get-AzStreamAnalyticsFunction** получает список функций, определенных в задании Azure Stream Analytics, или сведения о конкретной функции.</span><span class="sxs-lookup"><span data-stu-id="e0a23-106">The **Get-AzStreamAnalyticsFunction** cmdlet gets a list of the functions that are defined in an Azure Stream Analytics job or information about a specific function.</span></span>

## <span data-ttu-id="e0a23-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e0a23-107">EXAMPLES</span></span>

### <span data-ttu-id="e0a23-108">Пример 1: получение всех функций Stream Analytics</span><span class="sxs-lookup"><span data-stu-id="e0a23-108">Example 1: Get all Stream Analytics functions</span></span>
```
PS C:\>Get-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22"
```

<span data-ttu-id="e0a23-109">Эта команда получает функции, определенные для задания с именем StreamJob22.</span><span class="sxs-lookup"><span data-stu-id="e0a23-109">This command gets the functions defined on the job named StreamJob22.</span></span>

### <span data-ttu-id="e0a23-110">Пример 2: получение специальной функции Stream Analytics</span><span class="sxs-lookup"><span data-stu-id="e0a23-110">Example 2: Get a specific Stream Analytics function</span></span>
```
PS C:\>Get-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

<span data-ttu-id="e0a23-111">Эта команда получает сведения о функции с именем ScoreTweet, определенной в задании с именем StreamJob22.</span><span class="sxs-lookup"><span data-stu-id="e0a23-111">This command gets information about the function named ScoreTweet defined on the job named StreamJob22.</span></span>

## <span data-ttu-id="e0a23-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e0a23-112">PARAMETERS</span></span>

### <span data-ttu-id="e0a23-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0a23-113">-DefaultProfile</span></span>
<span data-ttu-id="e0a23-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e0a23-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e0a23-115">-JobName</span><span class="sxs-lookup"><span data-stu-id="e0a23-115">-JobName</span></span>
<span data-ttu-id="e0a23-116">Указывает имя задания Stream Analytics, к которому относятся функции.</span><span class="sxs-lookup"><span data-stu-id="e0a23-116">Specifies the name of the Stream Analytics job to which functions belong.</span></span>
<span data-ttu-id="e0a23-117">Этот командлет получает функции для задания, которое указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="e0a23-117">This cmdlet gets functions for the job that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0a23-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e0a23-118">-Name</span></span>
<span data-ttu-id="e0a23-119">Указывает имя функции Stream Analytics, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="e0a23-119">Specifies the name of the Stream Analytics function that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0a23-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0a23-120">-ResourceGroupName</span></span>
<span data-ttu-id="e0a23-121">Указывает имя группы ресурсов, к которой относятся функции Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="e0a23-121">Specifies the name of the resource group to which Stream Analytics functions belongs.</span></span>
<span data-ttu-id="e0a23-122">Этот командлет получает функции для группы, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="e0a23-122">This cmdlet gets functions for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="e0a23-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0a23-123">CommonParameters</span></span>
<span data-ttu-id="e0a23-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e0a23-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0a23-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0a23-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0a23-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e0a23-126">INPUTS</span></span>

### <span data-ttu-id="e0a23-127">System. String</span><span class="sxs-lookup"><span data-stu-id="e0a23-127">System.String</span></span>

## <span data-ttu-id="e0a23-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e0a23-128">OUTPUTS</span></span>

### <span data-ttu-id="e0a23-129">Microsoft. Azure. Commands. StreamAnalytics. Models. PSFunction</span><span class="sxs-lookup"><span data-stu-id="e0a23-129">Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction</span></span>

## <span data-ttu-id="e0a23-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="e0a23-130">NOTES</span></span>

## <span data-ttu-id="e0a23-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e0a23-131">RELATED LINKS</span></span>

[<span data-ttu-id="e0a23-132">New-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="e0a23-132">New-AzStreamAnalyticsFunction</span></span>](./New-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="e0a23-133">Remove-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="e0a23-133">Remove-AzStreamAnalyticsFunction</span></span>](./Remove-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="e0a23-134">Test-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="e0a23-134">Test-AzStreamAnalyticsFunction</span></span>](./Test-AzStreamAnalyticsFunction.md)



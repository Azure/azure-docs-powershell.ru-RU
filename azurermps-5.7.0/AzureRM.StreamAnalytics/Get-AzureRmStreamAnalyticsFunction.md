---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM
ms.assetid: 7F08A880-1FC5-4542-8AB8-927BB999A552
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/get-azurermstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsFunction.md
ms.openlocfilehash: dd2a52167a773b241364311ed4e0e00c03ea8459
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563240"
---
# <span data-ttu-id="7f6fa-101">Get-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="7f6fa-101">Get-AzureRmStreamAnalyticsFunction</span></span>

## <span data-ttu-id="7f6fa-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7f6fa-102">SYNOPSIS</span></span>
<span data-ttu-id="7f6fa-103">Возвращает функции в задании Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="7f6fa-103">Gets functions in a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7f6fa-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7f6fa-104">SYNTAX</span></span>

```
Get-AzureRmStreamAnalyticsFunction [-JobName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7f6fa-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7f6fa-105">DESCRIPTION</span></span>
<span data-ttu-id="7f6fa-106">Командлет **Get-AzureRmStreamAnalyticsFunction** получает список функций, определенных в задании Azure Stream Analytics, или сведения о конкретной функции.</span><span class="sxs-lookup"><span data-stu-id="7f6fa-106">The **Get-AzureRmStreamAnalyticsFunction** cmdlet gets a list of the functions that are defined in an Azure Stream Analytics job or information about a specific function.</span></span>

## <span data-ttu-id="7f6fa-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7f6fa-107">EXAMPLES</span></span>

### <span data-ttu-id="7f6fa-108">Пример 1: получение всех функций Stream Analytics</span><span class="sxs-lookup"><span data-stu-id="7f6fa-108">Example 1: Get all Stream Analytics functions</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22"
```

<span data-ttu-id="7f6fa-109">Эта команда получает функции, определенные для задания с именем StreamJob22.</span><span class="sxs-lookup"><span data-stu-id="7f6fa-109">This command gets the functions defined on the job named StreamJob22.</span></span>

### <span data-ttu-id="7f6fa-110">Пример 2: получение специальной функции Stream Analytics</span><span class="sxs-lookup"><span data-stu-id="7f6fa-110">Example 2: Get a specific Stream Analytics function</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

<span data-ttu-id="7f6fa-111">Эта команда получает сведения о функции с именем ScoreTweet, определенной в задании с именем StreamJob22.</span><span class="sxs-lookup"><span data-stu-id="7f6fa-111">This command gets information about the function named ScoreTweet defined on the job named StreamJob22.</span></span>

## <span data-ttu-id="7f6fa-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7f6fa-112">PARAMETERS</span></span>

### <span data-ttu-id="7f6fa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f6fa-113">-DefaultProfile</span></span>
<span data-ttu-id="7f6fa-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7f6fa-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7f6fa-115">-JobName</span><span class="sxs-lookup"><span data-stu-id="7f6fa-115">-JobName</span></span>
<span data-ttu-id="7f6fa-116">Указывает имя задания Stream Analytics, к которому относятся функции.</span><span class="sxs-lookup"><span data-stu-id="7f6fa-116">Specifies the name of the Stream Analytics job to which functions belong.</span></span>
<span data-ttu-id="7f6fa-117">Этот командлет получает функции для задания, которое указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="7f6fa-117">This cmdlet gets functions for the job that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f6fa-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7f6fa-118">-Name</span></span>
<span data-ttu-id="7f6fa-119">Указывает имя функции Stream Analytics, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="7f6fa-119">Specifies the name of the Stream Analytics function that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f6fa-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f6fa-120">-ResourceGroupName</span></span>
<span data-ttu-id="7f6fa-121">Указывает имя группы ресурсов, к которой относятся функции Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="7f6fa-121">Specifies the name of the resource group to which Stream Analytics functions belongs.</span></span>
<span data-ttu-id="7f6fa-122">Этот командлет получает функции для группы, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="7f6fa-122">This cmdlet gets functions for the group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f6fa-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f6fa-123">CommonParameters</span></span>
<span data-ttu-id="7f6fa-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7f6fa-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f6fa-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f6fa-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f6fa-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7f6fa-126">INPUTS</span></span>

### <span data-ttu-id="7f6fa-127">Ничего</span><span class="sxs-lookup"><span data-stu-id="7f6fa-127">None</span></span>
<span data-ttu-id="7f6fa-128">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="7f6fa-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7f6fa-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7f6fa-129">OUTPUTS</span></span>

### <span data-ttu-id="7f6fa-130">System. Collections. Generic. List [Microsoft. Azure. Commands. StreamAnalytics. Models. PSFunction, Microsoft. Azure. Commands. StreamAnalytics], Microsoft. Azure. Commands. StreamAnalytics. Models. PSFunction</span><span class="sxs-lookup"><span data-stu-id="7f6fa-130">System.Collections.Generic.List[Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction, Microsoft.Azure.Commands.StreamAnalytics], Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction</span></span>

## <span data-ttu-id="7f6fa-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="7f6fa-131">NOTES</span></span>

## <span data-ttu-id="7f6fa-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7f6fa-132">RELATED LINKS</span></span>

[<span data-ttu-id="7f6fa-133">New-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="7f6fa-133">New-AzureRmStreamAnalyticsFunction</span></span>](./New-AzureRmStreamAnalyticsFunction.md)

[<span data-ttu-id="7f6fa-134">Remove-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="7f6fa-134">Remove-AzureRmStreamAnalyticsFunction</span></span>](./Remove-AzureRmStreamAnalyticsFunction.md)

[<span data-ttu-id="7f6fa-135">Test-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="7f6fa-135">Test-AzureRmStreamAnalyticsFunction</span></span>](./Test-AzureRmStreamAnalyticsFunction.md)



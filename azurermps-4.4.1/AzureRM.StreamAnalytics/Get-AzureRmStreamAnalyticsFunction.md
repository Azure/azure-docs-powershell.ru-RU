---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 7F08A880-1FC5-4542-8AB8-927BB999A552
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsFunction.md
ms.openlocfilehash: 4a387da5b8f1f4ed9e6f3653a32ff8880ffaa734
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563828"
---
# <span data-ttu-id="a3130-101">Get-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="a3130-101">Get-AzureRmStreamAnalyticsFunction</span></span>

## <span data-ttu-id="a3130-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a3130-102">SYNOPSIS</span></span>
<span data-ttu-id="a3130-103">Возвращает функции в задании Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="a3130-103">Gets functions in a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a3130-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a3130-104">SYNTAX</span></span>

```
Get-AzureRmStreamAnalyticsFunction [-JobName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a3130-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a3130-105">DESCRIPTION</span></span>
<span data-ttu-id="a3130-106">Командлет **Get-AzureRmStreamAnalyticsFunction** получает список функций, определенных в задании Azure Stream Analytics, или сведения о конкретной функции.</span><span class="sxs-lookup"><span data-stu-id="a3130-106">The **Get-AzureRmStreamAnalyticsFunction** cmdlet gets a list of the functions that are defined in an Azure Stream Analytics job or information about a specific function.</span></span>

## <span data-ttu-id="a3130-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a3130-107">EXAMPLES</span></span>

### <span data-ttu-id="a3130-108">Пример 1: получение всех функций Stream Analytics</span><span class="sxs-lookup"><span data-stu-id="a3130-108">Example 1: Get all Stream Analytics functions</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22"
```

<span data-ttu-id="a3130-109">Эта команда получает функции, определенные для задания с именем StreamJob22.</span><span class="sxs-lookup"><span data-stu-id="a3130-109">This command gets the functions defined on the job named StreamJob22.</span></span>

### <span data-ttu-id="a3130-110">Пример 2: получение специальной функции Stream Analytics</span><span class="sxs-lookup"><span data-stu-id="a3130-110">Example 2: Get a specific Stream Analytics function</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

<span data-ttu-id="a3130-111">Эта команда получает сведения о функции с именем ScoreTweet, определенной в задании с именем StreamJob22.</span><span class="sxs-lookup"><span data-stu-id="a3130-111">This command gets information about the function named ScoreTweet defined on the job named StreamJob22.</span></span>

## <span data-ttu-id="a3130-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a3130-112">PARAMETERS</span></span>

### <span data-ttu-id="a3130-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="a3130-113">-JobName</span></span>
<span data-ttu-id="a3130-114">Указывает имя задания Stream Analytics, к которому относятся функции.</span><span class="sxs-lookup"><span data-stu-id="a3130-114">Specifies the name of the Stream Analytics job to which functions belong.</span></span>
<span data-ttu-id="a3130-115">Этот командлет получает функции для задания, которое указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="a3130-115">This cmdlet gets functions for the job that this parameter specifies.</span></span>

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

### <span data-ttu-id="a3130-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a3130-116">-Name</span></span>
<span data-ttu-id="a3130-117">Указывает имя функции Stream Analytics, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="a3130-117">Specifies the name of the Stream Analytics function that this cmdlet gets.</span></span>

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

### <span data-ttu-id="a3130-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3130-118">-ResourceGroupName</span></span>
<span data-ttu-id="a3130-119">Указывает имя группы ресурсов, к которой относятся функции Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="a3130-119">Specifies the name of the resource group to which Stream Analytics functions belongs.</span></span>
<span data-ttu-id="a3130-120">Этот командлет получает функции для группы, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="a3130-120">This cmdlet gets functions for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="a3130-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3130-121">-DefaultProfile</span></span>
<span data-ttu-id="a3130-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a3130-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a3130-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3130-123">CommonParameters</span></span>
<span data-ttu-id="a3130-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a3130-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3130-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3130-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3130-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a3130-126">INPUTS</span></span>

## <span data-ttu-id="a3130-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a3130-127">OUTPUTS</span></span>

### <span data-ttu-id="a3130-128">System. Collections. Generic. List [Microsoft. Azure. Commands. StreamAnalytics. Models. PSFunction, Microsoft. Azure. Commands. StreamAnalytics], Microsoft. Azure. Commands. StreamAnalytics. Models. PSFunction</span><span class="sxs-lookup"><span data-stu-id="a3130-128">System.Collections.Generic.List[Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction, Microsoft.Azure.Commands.StreamAnalytics], Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction</span></span>

## <span data-ttu-id="a3130-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="a3130-129">NOTES</span></span>

## <span data-ttu-id="a3130-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a3130-130">RELATED LINKS</span></span>

[<span data-ttu-id="a3130-131">New-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="a3130-131">New-AzureRmStreamAnalyticsFunction</span></span>](./New-AzureRmStreamAnalyticsFunction.md)

[<span data-ttu-id="a3130-132">Remove-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="a3130-132">Remove-AzureRmStreamAnalyticsFunction</span></span>](./Remove-AzureRmStreamAnalyticsFunction.md)

[<span data-ttu-id="a3130-133">Test-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="a3130-133">Test-AzureRmStreamAnalyticsFunction</span></span>](./Test-AzureRmStreamAnalyticsFunction.md)



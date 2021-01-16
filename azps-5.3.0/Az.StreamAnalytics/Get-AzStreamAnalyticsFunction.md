---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 7F08A880-1FC5-4542-8AB8-927BB999A552
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsFunction.md
ms.openlocfilehash: ceedee89473385202037cfedb23e4373995b6f98
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98424700"
---
# <span data-ttu-id="840a7-101">Get-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="840a7-101">Get-AzStreamAnalyticsFunction</span></span>

## <span data-ttu-id="840a7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="840a7-102">SYNOPSIS</span></span>
<span data-ttu-id="840a7-103">Возвращает функции в задание Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="840a7-103">Gets functions in a Stream Analytics job.</span></span>

## <span data-ttu-id="840a7-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="840a7-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsFunction [-JobName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="840a7-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="840a7-105">DESCRIPTION</span></span>
<span data-ttu-id="840a7-106">Для получения списка функций, определенных в заданиях Azure Stream Analytics, или сведения о конкретной функции, выполняется **cmdlet Get-AzStreamAnalyticsFunction.**</span><span class="sxs-lookup"><span data-stu-id="840a7-106">The **Get-AzStreamAnalyticsFunction** cmdlet gets a list of the functions that are defined in an Azure Stream Analytics job or information about a specific function.</span></span>

## <span data-ttu-id="840a7-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="840a7-107">EXAMPLES</span></span>

### <span data-ttu-id="840a7-108">Пример 1. Получить все функции аналитики Stream</span><span class="sxs-lookup"><span data-stu-id="840a7-108">Example 1: Get all Stream Analytics functions</span></span>
```
PS C:\>Get-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22"
```

<span data-ttu-id="840a7-109">Эта команда получает функции, определенные для задания StreamJob22.</span><span class="sxs-lookup"><span data-stu-id="840a7-109">This command gets the functions defined on the job named StreamJob22.</span></span>

### <span data-ttu-id="840a7-110">Пример 2. Получить определенную функцию Stream Analytics</span><span class="sxs-lookup"><span data-stu-id="840a7-110">Example 2: Get a specific Stream Analytics function</span></span>
```
PS C:\>Get-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

<span data-ttu-id="840a7-111">Эта команда получает сведения о функции ScoreTweet, определенной в заданиях StreamJob22.</span><span class="sxs-lookup"><span data-stu-id="840a7-111">This command gets information about the function named ScoreTweet defined on the job named StreamJob22.</span></span>

## <span data-ttu-id="840a7-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="840a7-112">PARAMETERS</span></span>

### <span data-ttu-id="840a7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="840a7-113">-DefaultProfile</span></span>
<span data-ttu-id="840a7-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="840a7-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="840a7-115">-JobName</span><span class="sxs-lookup"><span data-stu-id="840a7-115">-JobName</span></span>
<span data-ttu-id="840a7-116">Указывает имя задания Stream Analytics, к которому относятся функции.</span><span class="sxs-lookup"><span data-stu-id="840a7-116">Specifies the name of the Stream Analytics job to which functions belong.</span></span>
<span data-ttu-id="840a7-117">Этот cmdlet получает функции для задания, указанного этим параметром.</span><span class="sxs-lookup"><span data-stu-id="840a7-117">This cmdlet gets functions for the job that this parameter specifies.</span></span>

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

### <span data-ttu-id="840a7-118">-Name</span><span class="sxs-lookup"><span data-stu-id="840a7-118">-Name</span></span>
<span data-ttu-id="840a7-119">Указывает имя функции Stream Analytics, которую получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="840a7-119">Specifies the name of the Stream Analytics function that this cmdlet gets.</span></span>

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

### <span data-ttu-id="840a7-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="840a7-120">-ResourceGroupName</span></span>
<span data-ttu-id="840a7-121">Указывает имя группы ресурсов, к которой принадлежат функции Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="840a7-121">Specifies the name of the resource group to which Stream Analytics functions belongs.</span></span>
<span data-ttu-id="840a7-122">Этот cmdlet получает функции для группы, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="840a7-122">This cmdlet gets functions for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="840a7-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="840a7-123">CommonParameters</span></span>
<span data-ttu-id="840a7-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="840a7-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="840a7-125">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="840a7-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="840a7-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="840a7-126">INPUTS</span></span>

### <span data-ttu-id="840a7-127">System.String</span><span class="sxs-lookup"><span data-stu-id="840a7-127">System.String</span></span>

## <span data-ttu-id="840a7-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="840a7-128">OUTPUTS</span></span>

### <span data-ttu-id="840a7-129">Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction</span><span class="sxs-lookup"><span data-stu-id="840a7-129">Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction</span></span>

## <span data-ttu-id="840a7-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="840a7-130">NOTES</span></span>

## <span data-ttu-id="840a7-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="840a7-131">RELATED LINKS</span></span>

[<span data-ttu-id="840a7-132">New-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="840a7-132">New-AzStreamAnalyticsFunction</span></span>](./New-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="840a7-133">Remove-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="840a7-133">Remove-AzStreamAnalyticsFunction</span></span>](./Remove-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="840a7-134">Test-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="840a7-134">Test-AzStreamAnalyticsFunction</span></span>](./Test-AzStreamAnalyticsFunction.md)


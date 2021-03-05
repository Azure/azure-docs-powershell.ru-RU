---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: EF16CE43-1035-4ED0-B9D1-E475DF659ECE
online version: https://docs.microsoft.com/powershell/module/az.streamanalytics/get-azstreamanalyticsdefaultfunctiondefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsDefaultFunctionDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsDefaultFunctionDefinition.md
ms.openlocfilehash: c900973947418ebfb1eba3b503fc40a9f81a68ff
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973971"
---
# <span data-ttu-id="d9ae5-101">Get-AzStreamAnalyticsDefaultFunctionDefinition</span><span class="sxs-lookup"><span data-stu-id="d9ae5-101">Get-AzStreamAnalyticsDefaultFunctionDefinition</span></span>

## <span data-ttu-id="d9ae5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9ae5-102">SYNOPSIS</span></span>
<span data-ttu-id="d9ae5-103">Возвращает стандартное определение функции в Средстве аналитики Stream.</span><span class="sxs-lookup"><span data-stu-id="d9ae5-103">Gets the default definition of a function in Stream Analytics.</span></span>

## <span data-ttu-id="d9ae5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d9ae5-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsDefaultFunctionDefinition [-JobName] <String> [-Name] <String> [-File] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d9ae5-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d9ae5-105">DESCRIPTION</span></span>
<span data-ttu-id="d9ae5-106">Cmdlet **Get-AzStreamAnalyticsDefaultFunctionDefinition** получает стандартное определение функции в Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="d9ae5-106">The **Get-AzStreamAnalyticsDefaultFunctionDefinition** cmdlet gets the default definition of a function in Azure Stream Analytics.</span></span>
<span data-ttu-id="d9ae5-107">Для создания функции можно использовать определение по умолчанию New-AzStreamAnalyticsFunction и его New-AzStreamAnalyticsFunction.</span><span class="sxs-lookup"><span data-stu-id="d9ae5-107">You can use the default definition and the New-AzStreamAnalyticsFunction cmdlet to create a function.</span></span>
<span data-ttu-id="d9ae5-108">Определение по умолчанию можно изменить перед созданием функции.</span><span class="sxs-lookup"><span data-stu-id="d9ae5-108">You can modify the default definition before you create a function.</span></span>

## <span data-ttu-id="d9ae5-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d9ae5-109">EXAMPLES</span></span>

### <span data-ttu-id="d9ae5-110">Пример 1. Определение по умолчанию для функции Stream Analytics</span><span class="sxs-lookup"><span data-stu-id="d9ae5-110">Example 1: Get the default definition of a Stream Analytics function</span></span>
```
PS C:\>Get-AzStreamAnalyticsDefaultFunctionDefinition -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -File "C:\RetrieveDefaultDefinitionRequest.json" -Name "ScoreTweet"
```

<span data-ttu-id="d9ae5-111">Эта команда получает стандартное определение функции "ScoreTweet" с использованием параметров, указанных в RetrieveDefaultDefinitionRequest.jsфайла.</span><span class="sxs-lookup"><span data-stu-id="d9ae5-111">This command gets the default definition of the function named ScoreTweet by using the parameters specified in the RetrieveDefaultDefinitionRequest.json file.</span></span>

## <span data-ttu-id="d9ae5-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d9ae5-112">PARAMETERS</span></span>

### <span data-ttu-id="d9ae5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9ae5-113">-DefaultProfile</span></span>
<span data-ttu-id="d9ae5-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d9ae5-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d9ae5-115">-File</span><span class="sxs-lookup"><span data-stu-id="d9ae5-115">-File</span></span>
<span data-ttu-id="d9ae5-116">Путь к JSON-файлу, который содержит нотацию объектов JavaScript (JSON) для запроса на извлечение запроса определения функции по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d9ae5-116">Specifies the path of a .json file that contains the JavaScript Object Notation (JSON) representation of the request body for the retrieve default function definition request.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9ae5-117">-JobName</span><span class="sxs-lookup"><span data-stu-id="d9ae5-117">-JobName</span></span>
<span data-ttu-id="d9ae5-118">Указывает имя задания Stream Analytics, к которому относятся функции.</span><span class="sxs-lookup"><span data-stu-id="d9ae5-118">Specifies the name of the Stream Analytics job to which functions belong.</span></span>
<span data-ttu-id="d9ae5-119">Этот cmdlet получает определение по умолчанию для функции в заданиях, указанных этим параметром.</span><span class="sxs-lookup"><span data-stu-id="d9ae5-119">This cmdlet gets the default definition for a function in the job that this parameter specifies.</span></span>

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

### <span data-ttu-id="d9ae5-120">-Name</span><span class="sxs-lookup"><span data-stu-id="d9ae5-120">-Name</span></span>
<span data-ttu-id="d9ae5-121">Указывает имя функции Stream Analytics, для которой этот cmdlet получает определение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d9ae5-121">Specifies the name of the Stream Analytics function for which this cmdlet gets the default definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9ae5-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9ae5-122">-ResourceGroupName</span></span>
<span data-ttu-id="d9ae5-123">Указывает имя группы ресурсов, к которой принадлежат функции Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="d9ae5-123">Specifies the name of the resource group to which Stream Analytics functions belongs.</span></span>
<span data-ttu-id="d9ae5-124">Этот cmdlet получает определение функции для группы, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="d9ae5-124">This cmdlet gets a function definition for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="d9ae5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9ae5-125">CommonParameters</span></span>
<span data-ttu-id="d9ae5-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9ae5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9ae5-127">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9ae5-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9ae5-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d9ae5-128">INPUTS</span></span>

### <span data-ttu-id="d9ae5-129">System.String</span><span class="sxs-lookup"><span data-stu-id="d9ae5-129">System.String</span></span>

## <span data-ttu-id="d9ae5-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d9ae5-130">OUTPUTS</span></span>

### <span data-ttu-id="d9ae5-131">Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction</span><span class="sxs-lookup"><span data-stu-id="d9ae5-131">Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction</span></span>

## <span data-ttu-id="d9ae5-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d9ae5-132">NOTES</span></span>

## <span data-ttu-id="d9ae5-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d9ae5-133">RELATED LINKS</span></span>

[<span data-ttu-id="d9ae5-134">New-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="d9ae5-134">New-AzStreamAnalyticsFunction</span></span>](./New-AzStreamAnalyticsFunction.md)



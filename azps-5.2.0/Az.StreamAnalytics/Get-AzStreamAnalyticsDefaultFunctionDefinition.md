---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: EF16CE43-1035-4ED0-B9D1-E475DF659ECE
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticsdefaultfunctiondefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsDefaultFunctionDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsDefaultFunctionDefinition.md
ms.openlocfilehash: 1854c2e060dbbc83ba196043debb0ba08c9a933e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98414471"
---
# <span data-ttu-id="7f7cb-101">Get-AzStreamAnalyticsDefaultFunctionDefinition</span><span class="sxs-lookup"><span data-stu-id="7f7cb-101">Get-AzStreamAnalyticsDefaultFunctionDefinition</span></span>

## <span data-ttu-id="7f7cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f7cb-102">SYNOPSIS</span></span>
<span data-ttu-id="7f7cb-103">Возвращает стандартное определение функции в Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="7f7cb-103">Gets the default definition of a function in Stream Analytics.</span></span>

## <span data-ttu-id="7f7cb-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7f7cb-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsDefaultFunctionDefinition [-JobName] <String> [-Name] <String> [-File] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7f7cb-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7f7cb-105">DESCRIPTION</span></span>
<span data-ttu-id="7f7cb-106">Cmdlet **Get-AzStreamAnalyticsDefaultFunctionDefinition** получает стандартное определение функции в Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="7f7cb-106">The **Get-AzStreamAnalyticsDefaultFunctionDefinition** cmdlet gets the default definition of a function in Azure Stream Analytics.</span></span>
<span data-ttu-id="7f7cb-107">Для создания функции можно использовать определение по умолчанию New-AzStreamAnalyticsFunction и его New-AzStreamAnalyticsFunction.</span><span class="sxs-lookup"><span data-stu-id="7f7cb-107">You can use the default definition and the New-AzStreamAnalyticsFunction cmdlet to create a function.</span></span>
<span data-ttu-id="7f7cb-108">Определение по умолчанию можно изменить перед созданием функции.</span><span class="sxs-lookup"><span data-stu-id="7f7cb-108">You can modify the default definition before you create a function.</span></span>

## <span data-ttu-id="7f7cb-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7f7cb-109">EXAMPLES</span></span>

### <span data-ttu-id="7f7cb-110">Пример 1. Определение по умолчанию для функции Stream Analytics</span><span class="sxs-lookup"><span data-stu-id="7f7cb-110">Example 1: Get the default definition of a Stream Analytics function</span></span>
```
PS C:\>Get-AzStreamAnalyticsDefaultFunctionDefinition -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -File "C:\RetrieveDefaultDefinitionRequest.json" -Name "ScoreTweet"
```

<span data-ttu-id="7f7cb-111">Эта команда получает стандартное определение функции "ScoreTweet" с использованием параметров, указанных в RetrieveDefaultDefinitionRequest.jsфайла.</span><span class="sxs-lookup"><span data-stu-id="7f7cb-111">This command gets the default definition of the function named ScoreTweet by using the parameters specified in the RetrieveDefaultDefinitionRequest.json file.</span></span>

## <span data-ttu-id="7f7cb-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7f7cb-112">PARAMETERS</span></span>

### <span data-ttu-id="7f7cb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f7cb-113">-DefaultProfile</span></span>
<span data-ttu-id="7f7cb-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7f7cb-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7f7cb-115">-File</span><span class="sxs-lookup"><span data-stu-id="7f7cb-115">-File</span></span>
<span data-ttu-id="7f7cb-116">Путь к JSON-файлу, который содержит нотацию объектов JavaScript (JSON) для запроса на извлечение запроса определения функции по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7f7cb-116">Specifies the path of a .json file that contains the JavaScript Object Notation (JSON) representation of the request body for the retrieve default function definition request.</span></span>

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

### <span data-ttu-id="7f7cb-117">-JobName</span><span class="sxs-lookup"><span data-stu-id="7f7cb-117">-JobName</span></span>
<span data-ttu-id="7f7cb-118">Указывает имя задания Stream Analytics, к которому относятся функции.</span><span class="sxs-lookup"><span data-stu-id="7f7cb-118">Specifies the name of the Stream Analytics job to which functions belong.</span></span>
<span data-ttu-id="7f7cb-119">Этот cmdlet получает определение по умолчанию для функции в заданиях, указанных этим параметром.</span><span class="sxs-lookup"><span data-stu-id="7f7cb-119">This cmdlet gets the default definition for a function in the job that this parameter specifies.</span></span>

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

### <span data-ttu-id="7f7cb-120">-Name</span><span class="sxs-lookup"><span data-stu-id="7f7cb-120">-Name</span></span>
<span data-ttu-id="7f7cb-121">Указывает имя функции Stream Analytics, для которой этот cmdlet получает определение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7f7cb-121">Specifies the name of the Stream Analytics function for which this cmdlet gets the default definition.</span></span>

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

### <span data-ttu-id="7f7cb-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f7cb-122">-ResourceGroupName</span></span>
<span data-ttu-id="7f7cb-123">Указывает имя группы ресурсов, к которой принадлежат функции Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="7f7cb-123">Specifies the name of the resource group to which Stream Analytics functions belongs.</span></span>
<span data-ttu-id="7f7cb-124">Этот cmdlet получает определение функции для группы, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="7f7cb-124">This cmdlet gets a function definition for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="7f7cb-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f7cb-125">CommonParameters</span></span>
<span data-ttu-id="7f7cb-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f7cb-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f7cb-127">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f7cb-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f7cb-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7f7cb-128">INPUTS</span></span>

### <span data-ttu-id="7f7cb-129">System.String</span><span class="sxs-lookup"><span data-stu-id="7f7cb-129">System.String</span></span>

## <span data-ttu-id="7f7cb-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7f7cb-130">OUTPUTS</span></span>

### <span data-ttu-id="7f7cb-131">Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction</span><span class="sxs-lookup"><span data-stu-id="7f7cb-131">Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction</span></span>

## <span data-ttu-id="7f7cb-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7f7cb-132">NOTES</span></span>

## <span data-ttu-id="7f7cb-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7f7cb-133">RELATED LINKS</span></span>

[<span data-ttu-id="7f7cb-134">New-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="7f7cb-134">New-AzStreamAnalyticsFunction</span></span>](./New-AzStreamAnalyticsFunction.md)



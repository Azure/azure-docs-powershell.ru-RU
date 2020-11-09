---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: EF16CE43-1035-4ED0-B9D1-E475DF659ECE
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticsdefaultfunctiondefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsDefaultFunctionDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsDefaultFunctionDefinition.md
ms.openlocfilehash: 1854c2e060dbbc83ba196043debb0ba08c9a933e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247981"
---
# <span data-ttu-id="11288-101">Get-AzStreamAnalyticsDefaultFunctionDefinition</span><span class="sxs-lookup"><span data-stu-id="11288-101">Get-AzStreamAnalyticsDefaultFunctionDefinition</span></span>

## <span data-ttu-id="11288-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="11288-102">SYNOPSIS</span></span>
<span data-ttu-id="11288-103">Возвращает определение функции в Stream Analytics, используемое по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="11288-103">Gets the default definition of a function in Stream Analytics.</span></span>

## <span data-ttu-id="11288-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="11288-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsDefaultFunctionDefinition [-JobName] <String> [-Name] <String> [-File] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="11288-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="11288-105">DESCRIPTION</span></span>
<span data-ttu-id="11288-106">Командлет **Get-AzStreamAnalyticsDefaultFunctionDefinition** Возвращает определение функции по умолчанию в Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="11288-106">The **Get-AzStreamAnalyticsDefaultFunctionDefinition** cmdlet gets the default definition of a function in Azure Stream Analytics.</span></span>
<span data-ttu-id="11288-107">Вы можете использовать определение по умолчанию и командлет New-AzStreamAnalyticsFunction для создания функции.</span><span class="sxs-lookup"><span data-stu-id="11288-107">You can use the default definition and the New-AzStreamAnalyticsFunction cmdlet to create a function.</span></span>
<span data-ttu-id="11288-108">Вы можете изменить определение по умолчанию перед созданием функции.</span><span class="sxs-lookup"><span data-stu-id="11288-108">You can modify the default definition before you create a function.</span></span>

## <span data-ttu-id="11288-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="11288-109">EXAMPLES</span></span>

### <span data-ttu-id="11288-110">Пример 1: получение определения по умолчанию функции Stream Analytics</span><span class="sxs-lookup"><span data-stu-id="11288-110">Example 1: Get the default definition of a Stream Analytics function</span></span>
```
PS C:\>Get-AzStreamAnalyticsDefaultFunctionDefinition -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -File "C:\RetrieveDefaultDefinitionRequest.json" -Name "ScoreTweet"
```

<span data-ttu-id="11288-111">Эта команда получает определение по умолчанию для функции с именем ScoreTweet с параметрами, заданными в RetrieveDefaultDefinitionRequest.jsдля файла.</span><span class="sxs-lookup"><span data-stu-id="11288-111">This command gets the default definition of the function named ScoreTweet by using the parameters specified in the RetrieveDefaultDefinitionRequest.json file.</span></span>

## <span data-ttu-id="11288-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="11288-112">PARAMETERS</span></span>

### <span data-ttu-id="11288-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11288-113">-DefaultProfile</span></span>
<span data-ttu-id="11288-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="11288-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="11288-115">-Файл</span><span class="sxs-lookup"><span data-stu-id="11288-115">-File</span></span>
<span data-ttu-id="11288-116">Указывает путь к JSON-файлу, который содержит представление тела запроса для получения определения функции по умолчанию в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="11288-116">Specifies the path of a .json file that contains the JavaScript Object Notation (JSON) representation of the request body for the retrieve default function definition request.</span></span>

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

### <span data-ttu-id="11288-117">-JobName</span><span class="sxs-lookup"><span data-stu-id="11288-117">-JobName</span></span>
<span data-ttu-id="11288-118">Указывает имя задания Stream Analytics, к которому относятся функции.</span><span class="sxs-lookup"><span data-stu-id="11288-118">Specifies the name of the Stream Analytics job to which functions belong.</span></span>
<span data-ttu-id="11288-119">Этот командлет получает определение по умолчанию для функции в задании, которое указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="11288-119">This cmdlet gets the default definition for a function in the job that this parameter specifies.</span></span>

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

### <span data-ttu-id="11288-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="11288-120">-Name</span></span>
<span data-ttu-id="11288-121">Указывает имя функции Stream Analytics, для которой этот командлет получает определение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="11288-121">Specifies the name of the Stream Analytics function for which this cmdlet gets the default definition.</span></span>

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

### <span data-ttu-id="11288-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11288-122">-ResourceGroupName</span></span>
<span data-ttu-id="11288-123">Указывает имя группы ресурсов, к которой относятся функции Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="11288-123">Specifies the name of the resource group to which Stream Analytics functions belongs.</span></span>
<span data-ttu-id="11288-124">Этот командлет получает определение функции для группы, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="11288-124">This cmdlet gets a function definition for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="11288-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11288-125">CommonParameters</span></span>
<span data-ttu-id="11288-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="11288-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11288-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11288-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11288-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="11288-128">INPUTS</span></span>

### <span data-ttu-id="11288-129">System. String</span><span class="sxs-lookup"><span data-stu-id="11288-129">System.String</span></span>

## <span data-ttu-id="11288-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="11288-130">OUTPUTS</span></span>

### <span data-ttu-id="11288-131">Microsoft. Azure. Commands. StreamAnalytics. Models. PSFunction</span><span class="sxs-lookup"><span data-stu-id="11288-131">Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction</span></span>

## <span data-ttu-id="11288-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="11288-132">NOTES</span></span>

## <span data-ttu-id="11288-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="11288-133">RELATED LINKS</span></span>

[<span data-ttu-id="11288-134">New-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="11288-134">New-AzStreamAnalyticsFunction</span></span>](./New-AzStreamAnalyticsFunction.md)


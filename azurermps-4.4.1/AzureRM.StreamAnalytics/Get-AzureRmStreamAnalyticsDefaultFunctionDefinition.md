---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: EF16CE43-1035-4ED0-B9D1-E475DF659ECE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsDefaultFunctionDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsDefaultFunctionDefinition.md
ms.openlocfilehash: 307a07254f61bcbd37127a2a4d15bb41944a3508
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563831"
---
# <span data-ttu-id="6341b-101">Get-AzureRmStreamAnalyticsDefaultFunctionDefinition</span><span class="sxs-lookup"><span data-stu-id="6341b-101">Get-AzureRmStreamAnalyticsDefaultFunctionDefinition</span></span>

## <span data-ttu-id="6341b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6341b-102">SYNOPSIS</span></span>
<span data-ttu-id="6341b-103">Возвращает определение функции в Stream Analytics, используемое по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6341b-103">Gets the default definition of a function in Stream Analytics.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6341b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6341b-104">SYNTAX</span></span>

```
Get-AzureRmStreamAnalyticsDefaultFunctionDefinition [-JobName] <String> [-Name] <String> [-File] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6341b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6341b-105">DESCRIPTION</span></span>
<span data-ttu-id="6341b-106">Командлет **Get-AzureRmStreamAnalyticsDefaultFunctionDefinition** Возвращает определение функции по умолчанию в Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="6341b-106">The **Get-AzureRmStreamAnalyticsDefaultFunctionDefinition** cmdlet gets the default definition of a function in Azure Stream Analytics.</span></span>
<span data-ttu-id="6341b-107">Вы можете использовать определение по умолчанию и командлет New-AzureRmStreamAnalyticsFunction для создания функции.</span><span class="sxs-lookup"><span data-stu-id="6341b-107">You can use the default definition and the New-AzureRmStreamAnalyticsFunction cmdlet to create a function.</span></span>
<span data-ttu-id="6341b-108">Вы можете изменить определение по умолчанию перед созданием функции.</span><span class="sxs-lookup"><span data-stu-id="6341b-108">You can modify the default definition before you create a function.</span></span>

## <span data-ttu-id="6341b-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6341b-109">EXAMPLES</span></span>

### <span data-ttu-id="6341b-110">Пример 1: получение определения по умолчанию функции Stream Analytics</span><span class="sxs-lookup"><span data-stu-id="6341b-110">Example 1: Get the default definition of a Stream Analytics function</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsDefaultFunctionDefinition -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -File "C:\RetrieveDefaultDefinitionRequest.json" -Name "ScoreTweet"
```

<span data-ttu-id="6341b-111">Эта команда получает определение по умолчанию для функции с именем ScoreTweet с параметрами, заданными в RetrieveDefaultDefinitionRequest.jsдля файла.</span><span class="sxs-lookup"><span data-stu-id="6341b-111">This command gets the default definition of the function named ScoreTweet by using the parameters specified in the RetrieveDefaultDefinitionRequest.json file.</span></span>

## <span data-ttu-id="6341b-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6341b-112">PARAMETERS</span></span>

### <span data-ttu-id="6341b-113">-Файл</span><span class="sxs-lookup"><span data-stu-id="6341b-113">-File</span></span>
<span data-ttu-id="6341b-114">Указывает путь к JSON-файлу, который содержит представление тела запроса для получения определения функции по умолчанию в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="6341b-114">Specifies the path of a .json file that contains the JavaScript Object Notation (JSON) representation of the request body for the retrieve default function definition request.</span></span>

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

### <span data-ttu-id="6341b-115">-JobName</span><span class="sxs-lookup"><span data-stu-id="6341b-115">-JobName</span></span>
<span data-ttu-id="6341b-116">Указывает имя задания Stream Analytics, к которому относятся функции.</span><span class="sxs-lookup"><span data-stu-id="6341b-116">Specifies the name of the Stream Analytics job to which functions belong.</span></span>
<span data-ttu-id="6341b-117">Этот командлет получает определение по умолчанию для функции в задании, которое указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="6341b-117">This cmdlet gets the default definition for a function in the job that this parameter specifies.</span></span>

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

### <span data-ttu-id="6341b-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6341b-118">-Name</span></span>
<span data-ttu-id="6341b-119">Указывает имя функции Stream Analytics, для которой этот командлет получает определение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6341b-119">Specifies the name of the Stream Analytics function for which this cmdlet gets the default definition.</span></span>

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

### <span data-ttu-id="6341b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6341b-120">-ResourceGroupName</span></span>
<span data-ttu-id="6341b-121">Указывает имя группы ресурсов, к которой относятся функции Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="6341b-121">Specifies the name of the resource group to which Stream Analytics functions belongs.</span></span>
<span data-ttu-id="6341b-122">Этот командлет получает определение функции для группы, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="6341b-122">This cmdlet gets a function definition for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="6341b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6341b-123">-DefaultProfile</span></span>
<span data-ttu-id="6341b-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6341b-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6341b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6341b-125">CommonParameters</span></span>
<span data-ttu-id="6341b-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6341b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6341b-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6341b-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6341b-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6341b-128">INPUTS</span></span>

## <span data-ttu-id="6341b-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6341b-129">OUTPUTS</span></span>

### <span data-ttu-id="6341b-130">Microsoft. Azure. Commands. StreamAnalytics. Models. PSFunction</span><span class="sxs-lookup"><span data-stu-id="6341b-130">Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction</span></span>

## <span data-ttu-id="6341b-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="6341b-131">NOTES</span></span>

## <span data-ttu-id="6341b-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6341b-132">RELATED LINKS</span></span>

[<span data-ttu-id="6341b-133">New-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="6341b-133">New-AzureRmStreamAnalyticsFunction</span></span>](./New-AzureRmStreamAnalyticsFunction.md)



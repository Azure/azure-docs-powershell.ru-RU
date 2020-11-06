---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM
ms.assetid: F57C53E2-2873-441F-90E6-E6100418D519
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/test-azurermstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Test-AzureRmStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Test-AzureRmStreamAnalyticsOutput.md
ms.openlocfilehash: 5e93638489749702a3da2608927318f794bc4a3b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567362"
---
# <span data-ttu-id="a6048-101">Test-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="a6048-101">Test-AzureRmStreamAnalyticsOutput</span></span>

## <span data-ttu-id="a6048-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a6048-102">SYNOPSIS</span></span>
<span data-ttu-id="a6048-103">Проверяет состояние подключения для вывода.</span><span class="sxs-lookup"><span data-stu-id="a6048-103">Tests the connection status of an output.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a6048-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a6048-104">SYNTAX</span></span>

```
Test-AzureRmStreamAnalyticsOutput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a6048-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a6048-105">DESCRIPTION</span></span>
<span data-ttu-id="a6048-106">Командлет **Test-AzureRmStreamAnalyticsOutput** проверяет способность Stream Analytics подключаться к выходным данным.</span><span class="sxs-lookup"><span data-stu-id="a6048-106">The **Test-AzureRmStreamAnalyticsOutput** cmdlet tests the ability of Stream Analytics to connect to an output.</span></span>

## <span data-ttu-id="a6048-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a6048-107">EXAMPLES</span></span>

### <span data-ttu-id="a6048-108">Пример 1: Проверка состояния подключения вывода</span><span class="sxs-lookup"><span data-stu-id="a6048-108">EXAMPLE 1: Test the connection status of an output</span></span>
```
PS C:\>Test-AzureRmStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="a6048-109">Это проверяет состояние подключения выходного выхода в StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="a6048-109">This tests the connection status of the output Output in StreamingJob.</span></span>

## <span data-ttu-id="a6048-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a6048-110">PARAMETERS</span></span>

### <span data-ttu-id="a6048-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6048-111">-DefaultProfile</span></span>
<span data-ttu-id="a6048-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a6048-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a6048-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="a6048-113">-JobName</span></span>
<span data-ttu-id="a6048-114">Указывает имя задания Azure Stream Analytics, которому принадлежит требуемый выходной файл Azure Streaming Analytics.</span><span class="sxs-lookup"><span data-stu-id="a6048-114">Specifies the name of the Azure Stream Analytics job to which the desired Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="a6048-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a6048-115">-Name</span></span>
<span data-ttu-id="a6048-116">Указывает имя выходных данных Azure Stream Analytics для проверки.</span><span class="sxs-lookup"><span data-stu-id="a6048-116">Specifies the name of the Azure Stream Analytics output to test.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6048-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6048-117">-ResourceGroupName</span></span>
<span data-ttu-id="a6048-118">Указывает имя группы ресурсов, к которой относятся выходные данные Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="a6048-118">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="a6048-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6048-119">CommonParameters</span></span>
<span data-ttu-id="a6048-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a6048-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6048-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6048-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6048-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a6048-122">INPUTS</span></span>

### <span data-ttu-id="a6048-123">Ничего</span><span class="sxs-lookup"><span data-stu-id="a6048-123">None</span></span>
<span data-ttu-id="a6048-124">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="a6048-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a6048-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a6048-125">OUTPUTS</span></span>

### <span data-ttu-id="a6048-126">System. Object</span><span class="sxs-lookup"><span data-stu-id="a6048-126">System.Object</span></span>

## <span data-ttu-id="a6048-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="a6048-127">NOTES</span></span>

## <span data-ttu-id="a6048-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a6048-128">RELATED LINKS</span></span>

[<span data-ttu-id="a6048-129">Get-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="a6048-129">Get-AzureRmStreamAnalyticsOutput</span></span>](./Get-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="a6048-130">New-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="a6048-130">New-AzureRmStreamAnalyticsOutput</span></span>](./New-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="a6048-131">Remove-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="a6048-131">Remove-AzureRmStreamAnalyticsOutput</span></span>](./Remove-AzureRmStreamAnalyticsOutput.md)



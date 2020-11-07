---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: F57C53E2-2873-441F-90E6-E6100418D519
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/test-azstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsOutput.md
ms.openlocfilehash: ba4eee78732e4217a6652fb6770ab5df8de05174
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912313"
---
# <span data-ttu-id="5d248-101">Test-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="5d248-101">Test-AzStreamAnalyticsOutput</span></span>

## <span data-ttu-id="5d248-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5d248-102">SYNOPSIS</span></span>
<span data-ttu-id="5d248-103">Проверяет состояние подключения для вывода.</span><span class="sxs-lookup"><span data-stu-id="5d248-103">Tests the connection status of an output.</span></span>

## <span data-ttu-id="5d248-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5d248-104">SYNTAX</span></span>

```
Test-AzStreamAnalyticsOutput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5d248-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5d248-105">DESCRIPTION</span></span>
<span data-ttu-id="5d248-106">Командлет **Test-AzStreamAnalyticsOutput** проверяет способность Stream Analytics подключаться к выходным данным.</span><span class="sxs-lookup"><span data-stu-id="5d248-106">The **Test-AzStreamAnalyticsOutput** cmdlet tests the ability of Stream Analytics to connect to an output.</span></span>

## <span data-ttu-id="5d248-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5d248-107">EXAMPLES</span></span>

### <span data-ttu-id="5d248-108">Пример 1: Проверка состояния подключения вывода</span><span class="sxs-lookup"><span data-stu-id="5d248-108">EXAMPLE 1: Test the connection status of an output</span></span>
```
PS C:\>Test-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="5d248-109">Это проверяет состояние подключения выходного выхода в StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="5d248-109">This tests the connection status of the output Output in StreamingJob.</span></span>

## <span data-ttu-id="5d248-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5d248-110">PARAMETERS</span></span>

### <span data-ttu-id="5d248-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d248-111">-DefaultProfile</span></span>
<span data-ttu-id="5d248-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5d248-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5d248-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="5d248-113">-JobName</span></span>
<span data-ttu-id="5d248-114">Указывает имя задания Azure Stream Analytics, которому принадлежит требуемый выходной файл Azure Streaming Analytics.</span><span class="sxs-lookup"><span data-stu-id="5d248-114">Specifies the name of the Azure Stream Analytics job to which the desired Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="5d248-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5d248-115">-Name</span></span>
<span data-ttu-id="5d248-116">Указывает имя выходных данных Azure Stream Analytics для проверки.</span><span class="sxs-lookup"><span data-stu-id="5d248-116">Specifies the name of the Azure Stream Analytics output to test.</span></span>

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

### <span data-ttu-id="5d248-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d248-117">-ResourceGroupName</span></span>
<span data-ttu-id="5d248-118">Указывает имя группы ресурсов, к которой относятся выходные данные Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="5d248-118">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="5d248-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d248-119">CommonParameters</span></span>
<span data-ttu-id="5d248-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5d248-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d248-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d248-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d248-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5d248-122">INPUTS</span></span>

### <span data-ttu-id="5d248-123">System. String</span><span class="sxs-lookup"><span data-stu-id="5d248-123">System.String</span></span>

## <span data-ttu-id="5d248-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5d248-124">OUTPUTS</span></span>

### <span data-ttu-id="5d248-125">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5d248-125">System.Boolean</span></span>

## <span data-ttu-id="5d248-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="5d248-126">NOTES</span></span>

## <span data-ttu-id="5d248-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5d248-127">RELATED LINKS</span></span>

[<span data-ttu-id="5d248-128">Get-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="5d248-128">Get-AzStreamAnalyticsOutput</span></span>](./Get-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="5d248-129">New-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="5d248-129">New-AzStreamAnalyticsOutput</span></span>](./New-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="5d248-130">Remove-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="5d248-130">Remove-AzStreamAnalyticsOutput</span></span>](./Remove-AzStreamAnalyticsOutput.md)



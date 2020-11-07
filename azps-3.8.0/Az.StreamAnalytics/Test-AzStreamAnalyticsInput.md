---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: DEAC40AB-D90B-41D8-86AB-A66B60A908BD
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/test-azstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsInput.md
ms.openlocfilehash: 0123392604b9ea0a6d75d70fcf4f2caaff159702
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912407"
---
# <span data-ttu-id="7442f-101">Test-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="7442f-101">Test-AzStreamAnalyticsInput</span></span>

## <span data-ttu-id="7442f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7442f-102">SYNOPSIS</span></span>
<span data-ttu-id="7442f-103">Проверяет состояние подключения входных данных.</span><span class="sxs-lookup"><span data-stu-id="7442f-103">Tests the connection status of an input.</span></span>

## <span data-ttu-id="7442f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7442f-104">SYNTAX</span></span>

```
Test-AzStreamAnalyticsInput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7442f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7442f-105">DESCRIPTION</span></span>
<span data-ttu-id="7442f-106">Командлет **Test-AzStreamAnalyticsInput** проверяет способность Stream Analytics подключаться к входным данным.</span><span class="sxs-lookup"><span data-stu-id="7442f-106">The **Test-AzStreamAnalyticsInput** cmdlet tests the ability of Stream Analytics to connect to an input.</span></span>

## <span data-ttu-id="7442f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7442f-107">EXAMPLES</span></span>

### <span data-ttu-id="7442f-108">Пример 1: Проверка состояния подключения входного потока</span><span class="sxs-lookup"><span data-stu-id="7442f-108">EXAMPLE 1: Test the connection status of an input stream</span></span>
```
PS C:\>Test-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EntryStream"
```

<span data-ttu-id="7442f-109">Это проверяет состояние подключения входных EntryStream в StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="7442f-109">This tests the connection status of the input EntryStream in StreamingJob.</span></span>

## <span data-ttu-id="7442f-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7442f-110">PARAMETERS</span></span>

### <span data-ttu-id="7442f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7442f-111">-DefaultProfile</span></span>
<span data-ttu-id="7442f-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7442f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7442f-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="7442f-113">-JobName</span></span>
<span data-ttu-id="7442f-114">Указывает имя задания Azure Stream Analytics, к которому относятся входные данные Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="7442f-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="7442f-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7442f-115">-Name</span></span>
<span data-ttu-id="7442f-116">Указывает имя входного Аналитическего элемента Azure Stream для проверки.</span><span class="sxs-lookup"><span data-stu-id="7442f-116">Specifies the name of the Azure Stream Analytics input to test.</span></span>

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

### <span data-ttu-id="7442f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7442f-117">-ResourceGroupName</span></span>
<span data-ttu-id="7442f-118">Указывает имя группы ресурсов, к которой относятся входные данные Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="7442f-118">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="7442f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7442f-119">CommonParameters</span></span>
<span data-ttu-id="7442f-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7442f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7442f-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7442f-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7442f-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7442f-122">INPUTS</span></span>

### <span data-ttu-id="7442f-123">System. String</span><span class="sxs-lookup"><span data-stu-id="7442f-123">System.String</span></span>

## <span data-ttu-id="7442f-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7442f-124">OUTPUTS</span></span>

### <span data-ttu-id="7442f-125">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7442f-125">System.Boolean</span></span>

## <span data-ttu-id="7442f-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="7442f-126">NOTES</span></span>

## <span data-ttu-id="7442f-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7442f-127">RELATED LINKS</span></span>

[<span data-ttu-id="7442f-128">Get-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="7442f-128">Get-AzStreamAnalyticsInput</span></span>](./Get-AzStreamAnalyticsInput.md)

[<span data-ttu-id="7442f-129">New-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="7442f-129">New-AzStreamAnalyticsInput</span></span>](./New-AzStreamAnalyticsInput.md)

[<span data-ttu-id="7442f-130">Remove-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="7442f-130">Remove-AzStreamAnalyticsInput</span></span>](./Remove-AzStreamAnalyticsInput.md)



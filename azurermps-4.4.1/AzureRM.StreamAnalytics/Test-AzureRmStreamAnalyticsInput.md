---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: DEAC40AB-D90B-41D8-86AB-A66B60A908BD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Test-AzureRmStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Test-AzureRmStreamAnalyticsInput.md
ms.openlocfilehash: d0357e06257ad1df97b47ea7be59a1797e0f6902
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733084"
---
# <span data-ttu-id="4bbb1-101">Test-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="4bbb1-101">Test-AzureRmStreamAnalyticsInput</span></span>

## <span data-ttu-id="4bbb1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4bbb1-102">SYNOPSIS</span></span>
<span data-ttu-id="4bbb1-103">Проверяет состояние подключения входных данных.</span><span class="sxs-lookup"><span data-stu-id="4bbb1-103">Tests the connection status of an input.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4bbb1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4bbb1-104">SYNTAX</span></span>

```
Test-AzureRmStreamAnalyticsInput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4bbb1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4bbb1-105">DESCRIPTION</span></span>
<span data-ttu-id="4bbb1-106">Командлет **Test-AzureRmStreamAnalyticsInput** проверяет способность Stream Analytics подключаться к входным данным.</span><span class="sxs-lookup"><span data-stu-id="4bbb1-106">The **Test-AzureRmStreamAnalyticsInput** cmdlet tests the ability of Stream Analytics to connect to an input.</span></span>

## <span data-ttu-id="4bbb1-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4bbb1-107">EXAMPLES</span></span>

### <span data-ttu-id="4bbb1-108">Пример 1: Проверка состояния подключения входного потока</span><span class="sxs-lookup"><span data-stu-id="4bbb1-108">EXAMPLE 1: Test the connection status of an input stream</span></span>
```
PS C:\>Test-AzureRmStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EntryStream"
```

<span data-ttu-id="4bbb1-109">Это проверяет состояние подключения входных EntryStream в StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="4bbb1-109">This tests the connection status of the input EntryStream in StreamingJob.</span></span>

## <span data-ttu-id="4bbb1-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4bbb1-110">PARAMETERS</span></span>

### <span data-ttu-id="4bbb1-111">-JobName</span><span class="sxs-lookup"><span data-stu-id="4bbb1-111">-JobName</span></span>
<span data-ttu-id="4bbb1-112">Указывает имя задания Azure Stream Analytics, к которому относятся входные данные Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="4bbb1-112">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="4bbb1-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4bbb1-113">-Name</span></span>
<span data-ttu-id="4bbb1-114">Указывает имя входного Аналитическего элемента Azure Stream для проверки.</span><span class="sxs-lookup"><span data-stu-id="4bbb1-114">Specifies the name of the Azure Stream Analytics input to test.</span></span>

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

### <span data-ttu-id="4bbb1-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4bbb1-115">-ResourceGroupName</span></span>
<span data-ttu-id="4bbb1-116">Указывает имя группы ресурсов, к которой относятся входные данные Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="4bbb1-116">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="4bbb1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bbb1-117">-DefaultProfile</span></span>
<span data-ttu-id="4bbb1-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4bbb1-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4bbb1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bbb1-119">CommonParameters</span></span>
<span data-ttu-id="4bbb1-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4bbb1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bbb1-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4bbb1-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bbb1-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4bbb1-122">INPUTS</span></span>

## <span data-ttu-id="4bbb1-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4bbb1-123">OUTPUTS</span></span>

### <span data-ttu-id="4bbb1-124">System. Object</span><span class="sxs-lookup"><span data-stu-id="4bbb1-124">System.Object</span></span>

## <span data-ttu-id="4bbb1-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="4bbb1-125">NOTES</span></span>

## <span data-ttu-id="4bbb1-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4bbb1-126">RELATED LINKS</span></span>

[<span data-ttu-id="4bbb1-127">Get-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="4bbb1-127">Get-AzureRmStreamAnalyticsInput</span></span>](./Get-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="4bbb1-128">New-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="4bbb1-128">New-AzureRmStreamAnalyticsInput</span></span>](./New-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="4bbb1-129">Remove-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="4bbb1-129">Remove-AzureRmStreamAnalyticsInput</span></span>](./Remove-AzureRmStreamAnalyticsInput.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: E711FBFF-FB6D-4DFD-BAE8-7961EB4FD16B
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/test-azstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsFunction.md
ms.openlocfilehash: 1f2c7e653e96f697a714fef9f7b56c70240f0456
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235205"
---
# <span data-ttu-id="bf2b3-101">Test-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="bf2b3-101">Test-AzStreamAnalyticsFunction</span></span>

## <span data-ttu-id="bf2b3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bf2b3-102">SYNOPSIS</span></span>
<span data-ttu-id="bf2b3-103">Проверяет, может ли Stream Analytics подключаться к функции.</span><span class="sxs-lookup"><span data-stu-id="bf2b3-103">Tests whether Stream Analytics can connect to a function.</span></span>

## <span data-ttu-id="bf2b3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bf2b3-104">SYNTAX</span></span>

```
Test-AzStreamAnalyticsFunction [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bf2b3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bf2b3-105">DESCRIPTION</span></span>
<span data-ttu-id="bf2b3-106">Командлет **Test-AzStreamAnalyticsFunction** проверяет, может ли Azure Stream Analytics подключаться к функции.</span><span class="sxs-lookup"><span data-stu-id="bf2b3-106">The **Test-AzStreamAnalyticsFunction** cmdlet tests whether Azure Stream Analytics can connect to a function.</span></span>

## <span data-ttu-id="bf2b3-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bf2b3-107">EXAMPLES</span></span>

### <span data-ttu-id="bf2b3-108">Пример 1: Проверка функции Stream Analytics</span><span class="sxs-lookup"><span data-stu-id="bf2b3-108">Example 1: Test a Stream Analytics function</span></span>
```
PS C:\>Test-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

<span data-ttu-id="bf2b3-109">Эта команда проверяет состояние подключения функции с именем ScoreTweet в задании с именем StreamJob22.</span><span class="sxs-lookup"><span data-stu-id="bf2b3-109">This command tests the connection status of the function named ScoreTweet in the job named StreamJob22.</span></span>

## <span data-ttu-id="bf2b3-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bf2b3-110">PARAMETERS</span></span>

### <span data-ttu-id="bf2b3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf2b3-111">-DefaultProfile</span></span>
<span data-ttu-id="bf2b3-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bf2b3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bf2b3-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="bf2b3-113">-JobName</span></span>
<span data-ttu-id="bf2b3-114">Указывает имя задания Stream Analytics, к которому относится функция.</span><span class="sxs-lookup"><span data-stu-id="bf2b3-114">Specifies the name of the Stream Analytics job to which a function belongs.</span></span>

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

### <span data-ttu-id="bf2b3-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="bf2b3-115">-Name</span></span>
<span data-ttu-id="bf2b3-116">Указывает имя функции Stream Analytics, которую проверяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="bf2b3-116">Specifies the name of the Stream Analytics function that this cmdlet tests.</span></span>

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

### <span data-ttu-id="bf2b3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf2b3-117">-ResourceGroupName</span></span>
<span data-ttu-id="bf2b3-118">Указывает имя группы ресурсов, к которой относится функция Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="bf2b3-118">Specifies the name of the resource group to which a Stream Analytics function belongs.</span></span>
<span data-ttu-id="bf2b3-119">Этот командлет проверяет функцию в группе ресурсов, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="bf2b3-119">This cmdlet tests a function in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="bf2b3-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf2b3-120">CommonParameters</span></span>
<span data-ttu-id="bf2b3-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bf2b3-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf2b3-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf2b3-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf2b3-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bf2b3-123">INPUTS</span></span>

### <span data-ttu-id="bf2b3-124">System. String</span><span class="sxs-lookup"><span data-stu-id="bf2b3-124">System.String</span></span>

## <span data-ttu-id="bf2b3-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bf2b3-125">OUTPUTS</span></span>

### <span data-ttu-id="bf2b3-126">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bf2b3-126">System.Boolean</span></span>

## <span data-ttu-id="bf2b3-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="bf2b3-127">NOTES</span></span>

## <span data-ttu-id="bf2b3-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bf2b3-128">RELATED LINKS</span></span>

[<span data-ttu-id="bf2b3-129">Get-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="bf2b3-129">Get-AzStreamAnalyticsFunction</span></span>](./Get-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="bf2b3-130">New-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="bf2b3-130">New-AzStreamAnalyticsFunction</span></span>](./New-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="bf2b3-131">Remove-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="bf2b3-131">Remove-AzStreamAnalyticsFunction</span></span>](./Remove-AzStreamAnalyticsFunction.md)


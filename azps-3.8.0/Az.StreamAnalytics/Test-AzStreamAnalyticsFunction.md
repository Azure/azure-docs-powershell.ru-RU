---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: E711FBFF-FB6D-4DFD-BAE8-7961EB4FD16B
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/test-azstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsFunction.md
ms.openlocfilehash: 1f2c7e653e96f697a714fef9f7b56c70240f0456
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912408"
---
# <span data-ttu-id="769ce-101">Test-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="769ce-101">Test-AzStreamAnalyticsFunction</span></span>

## <span data-ttu-id="769ce-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="769ce-102">SYNOPSIS</span></span>
<span data-ttu-id="769ce-103">Проверяет, может ли Stream Analytics подключаться к функции.</span><span class="sxs-lookup"><span data-stu-id="769ce-103">Tests whether Stream Analytics can connect to a function.</span></span>

## <span data-ttu-id="769ce-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="769ce-104">SYNTAX</span></span>

```
Test-AzStreamAnalyticsFunction [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="769ce-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="769ce-105">DESCRIPTION</span></span>
<span data-ttu-id="769ce-106">Командлет **Test-AzStreamAnalyticsFunction** проверяет, может ли Azure Stream Analytics подключаться к функции.</span><span class="sxs-lookup"><span data-stu-id="769ce-106">The **Test-AzStreamAnalyticsFunction** cmdlet tests whether Azure Stream Analytics can connect to a function.</span></span>

## <span data-ttu-id="769ce-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="769ce-107">EXAMPLES</span></span>

### <span data-ttu-id="769ce-108">Пример 1: Проверка функции Stream Analytics</span><span class="sxs-lookup"><span data-stu-id="769ce-108">Example 1: Test a Stream Analytics function</span></span>
```
PS C:\>Test-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

<span data-ttu-id="769ce-109">Эта команда проверяет состояние подключения функции с именем ScoreTweet в задании с именем StreamJob22.</span><span class="sxs-lookup"><span data-stu-id="769ce-109">This command tests the connection status of the function named ScoreTweet in the job named StreamJob22.</span></span>

## <span data-ttu-id="769ce-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="769ce-110">PARAMETERS</span></span>

### <span data-ttu-id="769ce-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="769ce-111">-DefaultProfile</span></span>
<span data-ttu-id="769ce-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="769ce-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="769ce-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="769ce-113">-JobName</span></span>
<span data-ttu-id="769ce-114">Указывает имя задания Stream Analytics, к которому относится функция.</span><span class="sxs-lookup"><span data-stu-id="769ce-114">Specifies the name of the Stream Analytics job to which a function belongs.</span></span>

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

### <span data-ttu-id="769ce-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="769ce-115">-Name</span></span>
<span data-ttu-id="769ce-116">Указывает имя функции Stream Analytics, которую проверяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="769ce-116">Specifies the name of the Stream Analytics function that this cmdlet tests.</span></span>

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

### <span data-ttu-id="769ce-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="769ce-117">-ResourceGroupName</span></span>
<span data-ttu-id="769ce-118">Указывает имя группы ресурсов, к которой относится функция Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="769ce-118">Specifies the name of the resource group to which a Stream Analytics function belongs.</span></span>
<span data-ttu-id="769ce-119">Этот командлет проверяет функцию в группе ресурсов, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="769ce-119">This cmdlet tests a function in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="769ce-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="769ce-120">CommonParameters</span></span>
<span data-ttu-id="769ce-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="769ce-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="769ce-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="769ce-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="769ce-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="769ce-123">INPUTS</span></span>

### <span data-ttu-id="769ce-124">System. String</span><span class="sxs-lookup"><span data-stu-id="769ce-124">System.String</span></span>

## <span data-ttu-id="769ce-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="769ce-125">OUTPUTS</span></span>

### <span data-ttu-id="769ce-126">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="769ce-126">System.Boolean</span></span>

## <span data-ttu-id="769ce-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="769ce-127">NOTES</span></span>

## <span data-ttu-id="769ce-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="769ce-128">RELATED LINKS</span></span>

[<span data-ttu-id="769ce-129">Get-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="769ce-129">Get-AzStreamAnalyticsFunction</span></span>](./Get-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="769ce-130">New-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="769ce-130">New-AzStreamAnalyticsFunction</span></span>](./New-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="769ce-131">Remove-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="769ce-131">Remove-AzStreamAnalyticsFunction</span></span>](./Remove-AzStreamAnalyticsFunction.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: E711FBFF-FB6D-4DFD-BAE8-7961EB4FD16B
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/test-azstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsFunction.md
ms.openlocfilehash: f9139514850fe9d538c58d14813e91d2d24de502
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93728429"
---
# <span data-ttu-id="1cd31-101">Test-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="1cd31-101">Test-AzStreamAnalyticsFunction</span></span>

## <span data-ttu-id="1cd31-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1cd31-102">SYNOPSIS</span></span>
<span data-ttu-id="1cd31-103">Проверяет, может ли Stream Analytics подключаться к функции.</span><span class="sxs-lookup"><span data-stu-id="1cd31-103">Tests whether Stream Analytics can connect to a function.</span></span>

## <span data-ttu-id="1cd31-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1cd31-104">SYNTAX</span></span>

```
Test-AzStreamAnalyticsFunction [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1cd31-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1cd31-105">DESCRIPTION</span></span>
<span data-ttu-id="1cd31-106">Командлет **Test-AzStreamAnalyticsFunction** проверяет, может ли Azure Stream Analytics подключаться к функции.</span><span class="sxs-lookup"><span data-stu-id="1cd31-106">The **Test-AzStreamAnalyticsFunction** cmdlet tests whether Azure Stream Analytics can connect to a function.</span></span>

## <span data-ttu-id="1cd31-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1cd31-107">EXAMPLES</span></span>

### <span data-ttu-id="1cd31-108">Пример 1: Проверка функции Stream Analytics</span><span class="sxs-lookup"><span data-stu-id="1cd31-108">Example 1: Test a Stream Analytics function</span></span>
```
PS C:\>Test-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

<span data-ttu-id="1cd31-109">Эта команда проверяет состояние подключения функции с именем ScoreTweet в задании с именем StreamJob22.</span><span class="sxs-lookup"><span data-stu-id="1cd31-109">This command tests the connection status of the function named ScoreTweet in the job named StreamJob22.</span></span>

## <span data-ttu-id="1cd31-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1cd31-110">PARAMETERS</span></span>

### <span data-ttu-id="1cd31-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cd31-111">-DefaultProfile</span></span>
<span data-ttu-id="1cd31-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1cd31-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1cd31-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="1cd31-113">-JobName</span></span>
<span data-ttu-id="1cd31-114">Указывает имя задания Stream Analytics, к которому относится функция.</span><span class="sxs-lookup"><span data-stu-id="1cd31-114">Specifies the name of the Stream Analytics job to which a function belongs.</span></span>

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

### <span data-ttu-id="1cd31-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1cd31-115">-Name</span></span>
<span data-ttu-id="1cd31-116">Указывает имя функции Stream Analytics, которую проверяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="1cd31-116">Specifies the name of the Stream Analytics function that this cmdlet tests.</span></span>

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

### <span data-ttu-id="1cd31-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1cd31-117">-ResourceGroupName</span></span>
<span data-ttu-id="1cd31-118">Указывает имя группы ресурсов, к которой относится функция Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="1cd31-118">Specifies the name of the resource group to which a Stream Analytics function belongs.</span></span>
<span data-ttu-id="1cd31-119">Этот командлет проверяет функцию в группе ресурсов, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="1cd31-119">This cmdlet tests a function in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="1cd31-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cd31-120">CommonParameters</span></span>
<span data-ttu-id="1cd31-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1cd31-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cd31-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1cd31-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cd31-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1cd31-123">INPUTS</span></span>

### <span data-ttu-id="1cd31-124">System. String</span><span class="sxs-lookup"><span data-stu-id="1cd31-124">System.String</span></span>

## <span data-ttu-id="1cd31-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1cd31-125">OUTPUTS</span></span>

### <span data-ttu-id="1cd31-126">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1cd31-126">System.Boolean</span></span>

## <span data-ttu-id="1cd31-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="1cd31-127">NOTES</span></span>

## <span data-ttu-id="1cd31-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1cd31-128">RELATED LINKS</span></span>

[<span data-ttu-id="1cd31-129">Get-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="1cd31-129">Get-AzStreamAnalyticsFunction</span></span>](./Get-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="1cd31-130">New-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="1cd31-130">New-AzStreamAnalyticsFunction</span></span>](./New-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="1cd31-131">Remove-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="1cd31-131">Remove-AzStreamAnalyticsFunction</span></span>](./Remove-AzStreamAnalyticsFunction.md)



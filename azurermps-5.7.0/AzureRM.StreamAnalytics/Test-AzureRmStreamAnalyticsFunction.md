---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM
ms.assetid: E711FBFF-FB6D-4DFD-BAE8-7961EB4FD16B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/test-azurermstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Test-AzureRmStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Test-AzureRmStreamAnalyticsFunction.md
ms.openlocfilehash: 29002234ac769ffd46aa3ca338e5ce61f0e3b848
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558739"
---
# <span data-ttu-id="56c2c-101">Test-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="56c2c-101">Test-AzureRmStreamAnalyticsFunction</span></span>

## <span data-ttu-id="56c2c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="56c2c-102">SYNOPSIS</span></span>
<span data-ttu-id="56c2c-103">Проверяет, может ли Stream Analytics подключаться к функции.</span><span class="sxs-lookup"><span data-stu-id="56c2c-103">Tests whether Stream Analytics can connect to a function.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="56c2c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="56c2c-104">SYNTAX</span></span>

```
Test-AzureRmStreamAnalyticsFunction [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="56c2c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="56c2c-105">DESCRIPTION</span></span>
<span data-ttu-id="56c2c-106">Командлет **Test-AzureRmStreamAnalyticsFunction** проверяет, может ли Azure Stream Analytics подключаться к функции.</span><span class="sxs-lookup"><span data-stu-id="56c2c-106">The **Test-AzureRmStreamAnalyticsFunction** cmdlet tests whether Azure Stream Analytics can connect to a function.</span></span>

## <span data-ttu-id="56c2c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="56c2c-107">EXAMPLES</span></span>

### <span data-ttu-id="56c2c-108">Пример 1: Проверка функции Stream Analytics</span><span class="sxs-lookup"><span data-stu-id="56c2c-108">Example 1: Test a Stream Analytics function</span></span>
```
PS C:\>Test-AzureRmStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

<span data-ttu-id="56c2c-109">Эта команда проверяет состояние подключения функции с именем ScoreTweet в задании с именем StreamJob22.</span><span class="sxs-lookup"><span data-stu-id="56c2c-109">This command tests the connection status of the function named ScoreTweet in the job named StreamJob22.</span></span>

## <span data-ttu-id="56c2c-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="56c2c-110">PARAMETERS</span></span>

### <span data-ttu-id="56c2c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56c2c-111">-DefaultProfile</span></span>
<span data-ttu-id="56c2c-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="56c2c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="56c2c-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="56c2c-113">-JobName</span></span>
<span data-ttu-id="56c2c-114">Указывает имя задания Stream Analytics, к которому относится функция.</span><span class="sxs-lookup"><span data-stu-id="56c2c-114">Specifies the name of the Stream Analytics job to which a function belongs.</span></span>

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

### <span data-ttu-id="56c2c-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="56c2c-115">-Name</span></span>
<span data-ttu-id="56c2c-116">Указывает имя функции Stream Analytics, которую проверяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="56c2c-116">Specifies the name of the Stream Analytics function that this cmdlet tests.</span></span>

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

### <span data-ttu-id="56c2c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56c2c-117">-ResourceGroupName</span></span>
<span data-ttu-id="56c2c-118">Указывает имя группы ресурсов, к которой относится функция Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="56c2c-118">Specifies the name of the resource group to which a Stream Analytics function belongs.</span></span>
<span data-ttu-id="56c2c-119">Этот командлет проверяет функцию в группе ресурсов, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="56c2c-119">This cmdlet tests a function in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="56c2c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56c2c-120">CommonParameters</span></span>
<span data-ttu-id="56c2c-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="56c2c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56c2c-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56c2c-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56c2c-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="56c2c-123">INPUTS</span></span>

### <span data-ttu-id="56c2c-124">Ничего</span><span class="sxs-lookup"><span data-stu-id="56c2c-124">None</span></span>
<span data-ttu-id="56c2c-125">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="56c2c-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="56c2c-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="56c2c-126">OUTPUTS</span></span>

### <span data-ttu-id="56c2c-127">System. Object</span><span class="sxs-lookup"><span data-stu-id="56c2c-127">System.Object</span></span>

## <span data-ttu-id="56c2c-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="56c2c-128">NOTES</span></span>

## <span data-ttu-id="56c2c-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="56c2c-129">RELATED LINKS</span></span>

[<span data-ttu-id="56c2c-130">Get-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="56c2c-130">Get-AzureRmStreamAnalyticsFunction</span></span>](./Get-AzureRmStreamAnalyticsFunction.md)

[<span data-ttu-id="56c2c-131">New-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="56c2c-131">New-AzureRmStreamAnalyticsFunction</span></span>](./New-AzureRmStreamAnalyticsFunction.md)

[<span data-ttu-id="56c2c-132">Remove-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="56c2c-132">Remove-AzureRmStreamAnalyticsFunction</span></span>](./Remove-AzureRmStreamAnalyticsFunction.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: E711FBFF-FB6D-4DFD-BAE8-7961EB4FD16B
online version: https://docs.microsoft.com/powershell/module/az.streamanalytics/test-azstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsFunction.md
ms.openlocfilehash: d45a46cd0ff38f925a218c2bbab6edf70b97a4ea
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963496"
---
# <span data-ttu-id="2d097-101">Test-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="2d097-101">Test-AzStreamAnalyticsFunction</span></span>

## <span data-ttu-id="2d097-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2d097-102">SYNOPSIS</span></span>
<span data-ttu-id="2d097-103">Проверяет возможность подключения Stream Analytics к функции.</span><span class="sxs-lookup"><span data-stu-id="2d097-103">Tests whether Stream Analytics can connect to a function.</span></span>

## <span data-ttu-id="2d097-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2d097-104">SYNTAX</span></span>

```
Test-AzStreamAnalyticsFunction [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2d097-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2d097-105">DESCRIPTION</span></span>
<span data-ttu-id="2d097-106">**Cmdlet Test-AzStreamAnalyticsFunction** проверяет возможность подключения Azure Stream Analytics к функции.</span><span class="sxs-lookup"><span data-stu-id="2d097-106">The **Test-AzStreamAnalyticsFunction** cmdlet tests whether Azure Stream Analytics can connect to a function.</span></span>

## <span data-ttu-id="2d097-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2d097-107">EXAMPLES</span></span>

### <span data-ttu-id="2d097-108">Пример 1. Проверка функции Stream Analytics</span><span class="sxs-lookup"><span data-stu-id="2d097-108">Example 1: Test a Stream Analytics function</span></span>
```
PS C:\>Test-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

<span data-ttu-id="2d097-109">Эта команда проверяет состояние подключения функции ScoreTweet в заданиях StreamJob22.</span><span class="sxs-lookup"><span data-stu-id="2d097-109">This command tests the connection status of the function named ScoreTweet in the job named StreamJob22.</span></span>

## <span data-ttu-id="2d097-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2d097-110">PARAMETERS</span></span>

### <span data-ttu-id="2d097-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d097-111">-DefaultProfile</span></span>
<span data-ttu-id="2d097-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2d097-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2d097-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="2d097-113">-JobName</span></span>
<span data-ttu-id="2d097-114">Указывает имя задания Stream Analytics, к которому относится функция.</span><span class="sxs-lookup"><span data-stu-id="2d097-114">Specifies the name of the Stream Analytics job to which a function belongs.</span></span>

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

### <span data-ttu-id="2d097-115">-Name</span><span class="sxs-lookup"><span data-stu-id="2d097-115">-Name</span></span>
<span data-ttu-id="2d097-116">Указывает имя функции Stream Analytics, которую проверяет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2d097-116">Specifies the name of the Stream Analytics function that this cmdlet tests.</span></span>

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

### <span data-ttu-id="2d097-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d097-117">-ResourceGroupName</span></span>
<span data-ttu-id="2d097-118">Имя группы ресурсов, к которой относится функция Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="2d097-118">Specifies the name of the resource group to which a Stream Analytics function belongs.</span></span>
<span data-ttu-id="2d097-119">Этот cmdlet проверяет функцию в группе ресурсов, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="2d097-119">This cmdlet tests a function in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="2d097-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d097-120">CommonParameters</span></span>
<span data-ttu-id="2d097-121">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d097-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d097-122">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d097-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d097-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2d097-123">INPUTS</span></span>

### <span data-ttu-id="2d097-124">System.String</span><span class="sxs-lookup"><span data-stu-id="2d097-124">System.String</span></span>

## <span data-ttu-id="2d097-125">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2d097-125">OUTPUTS</span></span>

### <span data-ttu-id="2d097-126">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2d097-126">System.Boolean</span></span>

## <span data-ttu-id="2d097-127">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2d097-127">NOTES</span></span>

## <span data-ttu-id="2d097-128">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2d097-128">RELATED LINKS</span></span>

[<span data-ttu-id="2d097-129">Get-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="2d097-129">Get-AzStreamAnalyticsFunction</span></span>](./Get-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="2d097-130">New-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="2d097-130">New-AzStreamAnalyticsFunction</span></span>](./New-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="2d097-131">Remove-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="2d097-131">Remove-AzStreamAnalyticsFunction</span></span>](./Remove-AzStreamAnalyticsFunction.md)



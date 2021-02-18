---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: E711FBFF-FB6D-4DFD-BAE8-7961EB4FD16B
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/test-azstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsFunction.md
ms.openlocfilehash: 1f2c7e653e96f697a714fef9f7b56c70240f0456
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100216969"
---
# <span data-ttu-id="98718-101">Test-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="98718-101">Test-AzStreamAnalyticsFunction</span></span>

## <span data-ttu-id="98718-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="98718-102">SYNOPSIS</span></span>
<span data-ttu-id="98718-103">Проверяет возможность подключения Stream Analytics к функции.</span><span class="sxs-lookup"><span data-stu-id="98718-103">Tests whether Stream Analytics can connect to a function.</span></span>

## <span data-ttu-id="98718-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="98718-104">SYNTAX</span></span>

```
Test-AzStreamAnalyticsFunction [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="98718-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="98718-105">DESCRIPTION</span></span>
<span data-ttu-id="98718-106">**Cmdlet Test-AzStreamAnalyticsFunction** проверяет возможность подключения Azure Stream Analytics к функции.</span><span class="sxs-lookup"><span data-stu-id="98718-106">The **Test-AzStreamAnalyticsFunction** cmdlet tests whether Azure Stream Analytics can connect to a function.</span></span>

## <span data-ttu-id="98718-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="98718-107">EXAMPLES</span></span>

### <span data-ttu-id="98718-108">Пример 1. Проверка функции Stream Analytics</span><span class="sxs-lookup"><span data-stu-id="98718-108">Example 1: Test a Stream Analytics function</span></span>
```
PS C:\>Test-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

<span data-ttu-id="98718-109">Эта команда проверяет состояние подключения функции ScoreTweet в заданиях StreamJob22.</span><span class="sxs-lookup"><span data-stu-id="98718-109">This command tests the connection status of the function named ScoreTweet in the job named StreamJob22.</span></span>

## <span data-ttu-id="98718-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="98718-110">PARAMETERS</span></span>

### <span data-ttu-id="98718-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98718-111">-DefaultProfile</span></span>
<span data-ttu-id="98718-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="98718-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="98718-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="98718-113">-JobName</span></span>
<span data-ttu-id="98718-114">Указывает имя задания Stream Analytics, к которому относится функция.</span><span class="sxs-lookup"><span data-stu-id="98718-114">Specifies the name of the Stream Analytics job to which a function belongs.</span></span>

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

### <span data-ttu-id="98718-115">-Name</span><span class="sxs-lookup"><span data-stu-id="98718-115">-Name</span></span>
<span data-ttu-id="98718-116">Указывает имя функции Stream Analytics, которую проверяет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="98718-116">Specifies the name of the Stream Analytics function that this cmdlet tests.</span></span>

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

### <span data-ttu-id="98718-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98718-117">-ResourceGroupName</span></span>
<span data-ttu-id="98718-118">Имя группы ресурсов, к которой относится функция Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="98718-118">Specifies the name of the resource group to which a Stream Analytics function belongs.</span></span>
<span data-ttu-id="98718-119">Этот cmdlet проверяет функцию в группе ресурсов, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="98718-119">This cmdlet tests a function in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="98718-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98718-120">CommonParameters</span></span>
<span data-ttu-id="98718-121">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98718-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98718-122">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98718-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98718-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="98718-123">INPUTS</span></span>

### <span data-ttu-id="98718-124">System.String</span><span class="sxs-lookup"><span data-stu-id="98718-124">System.String</span></span>

## <span data-ttu-id="98718-125">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="98718-125">OUTPUTS</span></span>

### <span data-ttu-id="98718-126">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="98718-126">System.Boolean</span></span>

## <span data-ttu-id="98718-127">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="98718-127">NOTES</span></span>

## <span data-ttu-id="98718-128">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="98718-128">RELATED LINKS</span></span>

[<span data-ttu-id="98718-129">Get-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="98718-129">Get-AzStreamAnalyticsFunction</span></span>](./Get-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="98718-130">New-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="98718-130">New-AzStreamAnalyticsFunction</span></span>](./New-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="98718-131">Remove-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="98718-131">Remove-AzStreamAnalyticsFunction</span></span>](./Remove-AzStreamAnalyticsFunction.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: F57C53E2-2873-441F-90E6-E6100418D519
online version: https://docs.microsoft.com/powershell/module/az.streamanalytics/test-azstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsOutput.md
ms.openlocfilehash: 28a595b3e63a01439417ed07f6fd47c1cfc40a79
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981960"
---
# <span data-ttu-id="bdc97-101">Test-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="bdc97-101">Test-AzStreamAnalyticsOutput</span></span>

## <span data-ttu-id="bdc97-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bdc97-102">SYNOPSIS</span></span>
<span data-ttu-id="bdc97-103">Проверяет состояние подключения выходного результата.</span><span class="sxs-lookup"><span data-stu-id="bdc97-103">Tests the connection status of an output.</span></span>

## <span data-ttu-id="bdc97-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="bdc97-104">SYNTAX</span></span>

```
Test-AzStreamAnalyticsOutput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bdc97-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bdc97-105">DESCRIPTION</span></span>
<span data-ttu-id="bdc97-106">**Cmdlet Test-AzStreamAnalyticsOutput** проверяет возможность подключения средства Stream Analytics к выходным данным.</span><span class="sxs-lookup"><span data-stu-id="bdc97-106">The **Test-AzStreamAnalyticsOutput** cmdlet tests the ability of Stream Analytics to connect to an output.</span></span>

## <span data-ttu-id="bdc97-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="bdc97-107">EXAMPLES</span></span>

### <span data-ttu-id="bdc97-108">Пример 1. Проверка состояния подключения для выходных данных</span><span class="sxs-lookup"><span data-stu-id="bdc97-108">Example 1: Test the connection status of an output</span></span>
```powershell
PS C:\>Test-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="bdc97-109">При этом проверяется состояние подключения выходного результата в StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="bdc97-109">This tests the connection status of the output Output in StreamingJob.</span></span>

## <span data-ttu-id="bdc97-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bdc97-110">PARAMETERS</span></span>

### <span data-ttu-id="bdc97-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdc97-111">-DefaultProfile</span></span>
<span data-ttu-id="bdc97-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bdc97-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bdc97-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="bdc97-113">-JobName</span></span>
<span data-ttu-id="bdc97-114">Указывает имя задания Azure Stream Analytics, к которому относится нужный выход Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="bdc97-114">Specifies the name of the Azure Stream Analytics job to which the desired Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="bdc97-115">-Name</span><span class="sxs-lookup"><span data-stu-id="bdc97-115">-Name</span></span>
<span data-ttu-id="bdc97-116">Указывает имя результата Azure Stream Analytics, который нужно проверить.</span><span class="sxs-lookup"><span data-stu-id="bdc97-116">Specifies the name of the Azure Stream Analytics output to test.</span></span>

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

### <span data-ttu-id="bdc97-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bdc97-117">-ResourceGroupName</span></span>
<span data-ttu-id="bdc97-118">Имя группы ресурсов, к которой относится выход Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="bdc97-118">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="bdc97-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdc97-119">CommonParameters</span></span>
<span data-ttu-id="bdc97-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bdc97-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdc97-121">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bdc97-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdc97-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bdc97-122">INPUTS</span></span>

### <span data-ttu-id="bdc97-123">System.String</span><span class="sxs-lookup"><span data-stu-id="bdc97-123">System.String</span></span>

## <span data-ttu-id="bdc97-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="bdc97-124">OUTPUTS</span></span>

### <span data-ttu-id="bdc97-125">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="bdc97-125">System.Boolean</span></span>

## <span data-ttu-id="bdc97-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="bdc97-126">NOTES</span></span>

## <span data-ttu-id="bdc97-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bdc97-127">RELATED LINKS</span></span>

[<span data-ttu-id="bdc97-128">Get-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="bdc97-128">Get-AzStreamAnalyticsOutput</span></span>](./Get-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="bdc97-129">New-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="bdc97-129">New-AzStreamAnalyticsOutput</span></span>](./New-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="bdc97-130">Remove-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="bdc97-130">Remove-AzStreamAnalyticsOutput</span></span>](./Remove-AzStreamAnalyticsOutput.md)



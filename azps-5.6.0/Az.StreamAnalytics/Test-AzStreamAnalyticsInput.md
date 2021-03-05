---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: DEAC40AB-D90B-41D8-86AB-A66B60A908BD
online version: https://docs.microsoft.com/powershell/module/az.streamanalytics/test-azstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsInput.md
ms.openlocfilehash: 09cf95f6fd7feb17053063952ae7110098353c86
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002179"
---
# <span data-ttu-id="42d16-101">Test-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="42d16-101">Test-AzStreamAnalyticsInput</span></span>

## <span data-ttu-id="42d16-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="42d16-102">SYNOPSIS</span></span>
<span data-ttu-id="42d16-103">Проверяет состояние подключения входного данных.</span><span class="sxs-lookup"><span data-stu-id="42d16-103">Tests the connection status of an input.</span></span>

## <span data-ttu-id="42d16-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="42d16-104">SYNTAX</span></span>

```
Test-AzStreamAnalyticsInput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="42d16-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="42d16-105">DESCRIPTION</span></span>
<span data-ttu-id="42d16-106">**Cmdlet Test-AzStreamAnalyticsInput** проверяет возможность подключения средства Stream Analytics к входным данным.</span><span class="sxs-lookup"><span data-stu-id="42d16-106">The **Test-AzStreamAnalyticsInput** cmdlet tests the ability of Stream Analytics to connect to an input.</span></span>

## <span data-ttu-id="42d16-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="42d16-107">EXAMPLES</span></span>

### <span data-ttu-id="42d16-108">Пример 1. Проверка состояния подключения входного потока</span><span class="sxs-lookup"><span data-stu-id="42d16-108">Example 1: Test the connection status of an input stream</span></span>
```powershell
PS C:\>Test-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EntryStream"
```

<span data-ttu-id="42d16-109">При этом проверяется состояние подключения входного потока в StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="42d16-109">This tests the connection status of the input EntryStream in StreamingJob.</span></span>

## <span data-ttu-id="42d16-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="42d16-110">PARAMETERS</span></span>

### <span data-ttu-id="42d16-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42d16-111">-DefaultProfile</span></span>
<span data-ttu-id="42d16-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="42d16-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="42d16-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="42d16-113">-JobName</span></span>
<span data-ttu-id="42d16-114">Указывает имя задания Azure Stream Analytics, к которому относится ввод Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="42d16-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="42d16-115">-Name</span><span class="sxs-lookup"><span data-stu-id="42d16-115">-Name</span></span>
<span data-ttu-id="42d16-116">Указывает имя входных данных azure Stream Analytics, которые нужно проверить.</span><span class="sxs-lookup"><span data-stu-id="42d16-116">Specifies the name of the Azure Stream Analytics input to test.</span></span>

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

### <span data-ttu-id="42d16-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42d16-117">-ResourceGroupName</span></span>
<span data-ttu-id="42d16-118">Имя группы ресурсов, к которой относится ввод Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="42d16-118">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="42d16-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42d16-119">CommonParameters</span></span>
<span data-ttu-id="42d16-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42d16-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42d16-121">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42d16-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42d16-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="42d16-122">INPUTS</span></span>

### <span data-ttu-id="42d16-123">System.String</span><span class="sxs-lookup"><span data-stu-id="42d16-123">System.String</span></span>

## <span data-ttu-id="42d16-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="42d16-124">OUTPUTS</span></span>

### <span data-ttu-id="42d16-125">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="42d16-125">System.Boolean</span></span>

## <span data-ttu-id="42d16-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="42d16-126">NOTES</span></span>

## <span data-ttu-id="42d16-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="42d16-127">RELATED LINKS</span></span>

[<span data-ttu-id="42d16-128">Get-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="42d16-128">Get-AzStreamAnalyticsInput</span></span>](./Get-AzStreamAnalyticsInput.md)

[<span data-ttu-id="42d16-129">New-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="42d16-129">New-AzStreamAnalyticsInput</span></span>](./New-AzStreamAnalyticsInput.md)

[<span data-ttu-id="42d16-130">Remove-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="42d16-130">Remove-AzStreamAnalyticsInput</span></span>](./Remove-AzStreamAnalyticsInput.md)



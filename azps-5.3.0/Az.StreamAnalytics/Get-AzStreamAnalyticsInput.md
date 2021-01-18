---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: F371FD62-D138-4610-84A1-93EDC42D6AAC
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsInput.md
ms.openlocfilehash: 1f83eaf8ff358c211dbe8b83cfb99d986e56c1ed
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98517002"
---
# <span data-ttu-id="36301-101">Get-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="36301-101">Get-AzStreamAnalyticsInput</span></span>

## <span data-ttu-id="36301-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36301-102">SYNOPSIS</span></span>
<span data-ttu-id="36301-103">Получает ввод задания Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="36301-103">Gets Stream Analytics job inputs.</span></span>

## <span data-ttu-id="36301-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="36301-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsInput [-JobName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="36301-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="36301-105">DESCRIPTION</span></span>
<span data-ttu-id="36301-106">В этом проекте на ленте перечислены все входные данные, определенные в заданиях **Аналитики Stream** или вводимые сведения об определенном входе.</span><span class="sxs-lookup"><span data-stu-id="36301-106">The **Get-AzStreamAnalyticsInput** cmdlet lists all of the inputs that are defined in a Stream Analytics job or gets information about a specific input.</span></span>

## <span data-ttu-id="36301-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="36301-107">EXAMPLES</span></span>

### <span data-ttu-id="36301-108">Пример 1. Просмотр сведений о входных данных, определенных в заданиях</span><span class="sxs-lookup"><span data-stu-id="36301-108">Example 1: Get information about the inputs defined on a job</span></span>
```powershell
PS C:\>Get-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob"
```

<span data-ttu-id="36301-109">Эта команда возвращает сведения обо всех входных данных, определенных в командной работе StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="36301-109">This command returns information about all the inputs defined on the job StreamingJob.</span></span>

### <span data-ttu-id="36301-110">Пример 2. Просмотр сведений об определенных данных, определенных в заданиях</span><span class="sxs-lookup"><span data-stu-id="36301-110">Example 2: Get information about a specific input defined on a job</span></span>
```powershell
PS C:\>Get-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EntryStream"
```

<span data-ttu-id="36301-111">Эта команда возвращает сведения о входных данных с именем EntryStream, определенных в задание StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="36301-111">This command returns information about the input named EntryStream defined on the job StreamingJob.</span></span>

## <span data-ttu-id="36301-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="36301-112">PARAMETERS</span></span>

### <span data-ttu-id="36301-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36301-113">-DefaultProfile</span></span>
<span data-ttu-id="36301-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="36301-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="36301-115">-JobName</span><span class="sxs-lookup"><span data-stu-id="36301-115">-JobName</span></span>
<span data-ttu-id="36301-116">Указывает имя задания Azure Stream Analytics, к которому относится ввод Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="36301-116">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="36301-117">-Name</span><span class="sxs-lookup"><span data-stu-id="36301-117">-Name</span></span>
<span data-ttu-id="36301-118">Указывает имя входных данных azure Stream Analytics, которые нужно получить.</span><span class="sxs-lookup"><span data-stu-id="36301-118">Specifies the name of the Azure Stream Analytics input to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36301-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36301-119">-ResourceGroupName</span></span>
<span data-ttu-id="36301-120">Имя группы ресурсов, к которой относится ввод Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="36301-120">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="36301-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36301-121">CommonParameters</span></span>
<span data-ttu-id="36301-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36301-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36301-123">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36301-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36301-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="36301-124">INPUTS</span></span>

### <span data-ttu-id="36301-125">System.String</span><span class="sxs-lookup"><span data-stu-id="36301-125">System.String</span></span>

## <span data-ttu-id="36301-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="36301-126">OUTPUTS</span></span>

### <span data-ttu-id="36301-127">Microsoft.Azure.Commands.StreamAnalytics.Models.PSInput</span><span class="sxs-lookup"><span data-stu-id="36301-127">Microsoft.Azure.Commands.StreamAnalytics.Models.PSInput</span></span>

## <span data-ttu-id="36301-128">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="36301-128">NOTES</span></span>

## <span data-ttu-id="36301-129">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="36301-129">RELATED LINKS</span></span>

[<span data-ttu-id="36301-130">New-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="36301-130">New-AzStreamAnalyticsInput</span></span>](./New-AzStreamAnalyticsInput.md)

[<span data-ttu-id="36301-131">Remove-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="36301-131">Remove-AzStreamAnalyticsInput</span></span>](./Remove-AzStreamAnalyticsInput.md)

[<span data-ttu-id="36301-132">Test-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="36301-132">Test-AzStreamAnalyticsInput</span></span>](./Test-AzStreamAnalyticsInput.md)



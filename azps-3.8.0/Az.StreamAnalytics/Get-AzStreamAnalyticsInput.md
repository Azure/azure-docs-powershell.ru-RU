---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: F371FD62-D138-4610-84A1-93EDC42D6AAC
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsInput.md
ms.openlocfilehash: ba64089da3673957eead10ef1301f5c7c4a59467
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912971"
---
# <span data-ttu-id="3828e-101">Get-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="3828e-101">Get-AzStreamAnalyticsInput</span></span>

## <span data-ttu-id="3828e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3828e-102">SYNOPSIS</span></span>
<span data-ttu-id="3828e-103">Возвращает входные данные для задания Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="3828e-103">Gets Stream Analytics job inputs.</span></span>

## <span data-ttu-id="3828e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3828e-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsInput [-JobName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3828e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3828e-105">DESCRIPTION</span></span>
<span data-ttu-id="3828e-106">Командлет **Get-AzStreamAnalyticsInput** перечисляет все входные данные, определенные в задании Stream Analytics, или получает сведения о конкретных входных данных.</span><span class="sxs-lookup"><span data-stu-id="3828e-106">The **Get-AzStreamAnalyticsInput** cmdlet lists all of the inputs that are defined in a Stream Analytics job or gets information about a specific input.</span></span>

## <span data-ttu-id="3828e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3828e-107">EXAMPLES</span></span>

### <span data-ttu-id="3828e-108">Пример 1: получение сведений о входных данных, определенных для задания</span><span class="sxs-lookup"><span data-stu-id="3828e-108">EXAMPLE 1: Get information about the inputs defined on a job</span></span>
```
PS C:\>Get-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob"
```

<span data-ttu-id="3828e-109">Эта команда возвращает сведения обо всех входных данных, определенных для задания StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="3828e-109">This command returns information about all the inputs defined on the job StreamingJob.</span></span>

### <span data-ttu-id="3828e-110">Пример 2: получение сведений о конкретном вводе, определенном для задания</span><span class="sxs-lookup"><span data-stu-id="3828e-110">EXAMPLE 2: Get information about a specific input defined on a job</span></span>
```
PS C:\>Get-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EntryStream"
```

<span data-ttu-id="3828e-111">Эта команда возвращает сведения о входных данных с именем EntryStream, определенных в задании StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="3828e-111">This command returns information about the input named EntryStream defined on the job StreamingJob.</span></span>

## <span data-ttu-id="3828e-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3828e-112">PARAMETERS</span></span>

### <span data-ttu-id="3828e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3828e-113">-DefaultProfile</span></span>
<span data-ttu-id="3828e-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3828e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3828e-115">-JobName</span><span class="sxs-lookup"><span data-stu-id="3828e-115">-JobName</span></span>
<span data-ttu-id="3828e-116">Указывает имя задания Azure Stream Analytics, к которому относятся входные данные Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="3828e-116">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="3828e-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3828e-117">-Name</span></span>
<span data-ttu-id="3828e-118">Указывает имя входных данных Azure Stream Analytics, которые нужно извлечь.</span><span class="sxs-lookup"><span data-stu-id="3828e-118">Specifies the name of the Azure Stream Analytics input to retrieve.</span></span>

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

### <span data-ttu-id="3828e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3828e-119">-ResourceGroupName</span></span>
<span data-ttu-id="3828e-120">Указывает имя группы ресурсов, к которой относятся входные данные Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="3828e-120">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="3828e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3828e-121">CommonParameters</span></span>
<span data-ttu-id="3828e-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3828e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3828e-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3828e-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3828e-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3828e-124">INPUTS</span></span>

### <span data-ttu-id="3828e-125">System. String</span><span class="sxs-lookup"><span data-stu-id="3828e-125">System.String</span></span>

## <span data-ttu-id="3828e-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3828e-126">OUTPUTS</span></span>

### <span data-ttu-id="3828e-127">Microsoft. Azure. Commands. StreamAnalytics. Models. PSInput</span><span class="sxs-lookup"><span data-stu-id="3828e-127">Microsoft.Azure.Commands.StreamAnalytics.Models.PSInput</span></span>

## <span data-ttu-id="3828e-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="3828e-128">NOTES</span></span>

## <span data-ttu-id="3828e-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3828e-129">RELATED LINKS</span></span>

[<span data-ttu-id="3828e-130">New-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="3828e-130">New-AzStreamAnalyticsInput</span></span>](./New-AzStreamAnalyticsInput.md)

[<span data-ttu-id="3828e-131">Remove-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="3828e-131">Remove-AzStreamAnalyticsInput</span></span>](./Remove-AzStreamAnalyticsInput.md)

[<span data-ttu-id="3828e-132">Test-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="3828e-132">Test-AzStreamAnalyticsInput</span></span>](./Test-AzStreamAnalyticsInput.md)



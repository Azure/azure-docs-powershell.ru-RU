---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: F371FD62-D138-4610-84A1-93EDC42D6AAC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/get-azurermstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsInput.md
ms.openlocfilehash: 8b63dbd497edce422fc4cf70182ca8259721d8d1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93556479"
---
# <span data-ttu-id="87ad2-101">Get-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="87ad2-101">Get-AzureRmStreamAnalyticsInput</span></span>

## <span data-ttu-id="87ad2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="87ad2-102">SYNOPSIS</span></span>
<span data-ttu-id="87ad2-103">Возвращает входные данные для задания Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="87ad2-103">Gets Stream Analytics job inputs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="87ad2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="87ad2-104">SYNTAX</span></span>

```
Get-AzureRmStreamAnalyticsInput [-JobName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="87ad2-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="87ad2-105">DESCRIPTION</span></span>
<span data-ttu-id="87ad2-106">Командлет **Get-AzureRmStreamAnalyticsInput** перечисляет все входные данные, определенные в задании Stream Analytics, или получает сведения о конкретных входных данных.</span><span class="sxs-lookup"><span data-stu-id="87ad2-106">The **Get-AzureRmStreamAnalyticsInput** cmdlet lists all of the inputs that are defined in a Stream Analytics job or gets information about a specific input.</span></span>

## <span data-ttu-id="87ad2-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="87ad2-107">EXAMPLES</span></span>

### <span data-ttu-id="87ad2-108">Пример 1: получение сведений о входных данных, определенных для задания</span><span class="sxs-lookup"><span data-stu-id="87ad2-108">EXAMPLE 1: Get information about the inputs defined on a job</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob"
```

<span data-ttu-id="87ad2-109">Эта команда возвращает сведения обо всех входных данных, определенных для задания StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="87ad2-109">This command returns information about all the inputs defined on the job StreamingJob.</span></span>

### <span data-ttu-id="87ad2-110">Пример 2: получение сведений о конкретном вводе, определенном для задания</span><span class="sxs-lookup"><span data-stu-id="87ad2-110">EXAMPLE 2: Get information about a specific input defined on a job</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EntryStream"
```

<span data-ttu-id="87ad2-111">Эта команда возвращает сведения о входных данных с именем EntryStream, определенных в задании StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="87ad2-111">This command returns information about the input named EntryStream defined on the job StreamingJob.</span></span>

## <span data-ttu-id="87ad2-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="87ad2-112">PARAMETERS</span></span>

### <span data-ttu-id="87ad2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87ad2-113">-DefaultProfile</span></span>
<span data-ttu-id="87ad2-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="87ad2-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87ad2-115">-JobName</span><span class="sxs-lookup"><span data-stu-id="87ad2-115">-JobName</span></span>
<span data-ttu-id="87ad2-116">Указывает имя задания Azure Stream Analytics, к которому относятся входные данные Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="87ad2-116">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="87ad2-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="87ad2-117">-Name</span></span>
<span data-ttu-id="87ad2-118">Указывает имя входных данных Azure Stream Analytics, которые нужно извлечь.</span><span class="sxs-lookup"><span data-stu-id="87ad2-118">Specifies the name of the Azure Stream Analytics input to retrieve.</span></span>

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

### <span data-ttu-id="87ad2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87ad2-119">-ResourceGroupName</span></span>
<span data-ttu-id="87ad2-120">Указывает имя группы ресурсов, к которой относятся входные данные Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="87ad2-120">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="87ad2-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87ad2-121">CommonParameters</span></span>
<span data-ttu-id="87ad2-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="87ad2-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87ad2-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87ad2-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87ad2-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="87ad2-124">INPUTS</span></span>

### <span data-ttu-id="87ad2-125">System. String</span><span class="sxs-lookup"><span data-stu-id="87ad2-125">System.String</span></span>

## <span data-ttu-id="87ad2-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="87ad2-126">OUTPUTS</span></span>

### <span data-ttu-id="87ad2-127">Microsoft. Azure. Commands. StreamAnalytics. Models. PSInput</span><span class="sxs-lookup"><span data-stu-id="87ad2-127">Microsoft.Azure.Commands.StreamAnalytics.Models.PSInput</span></span>

## <span data-ttu-id="87ad2-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="87ad2-128">NOTES</span></span>

## <span data-ttu-id="87ad2-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="87ad2-129">RELATED LINKS</span></span>

[<span data-ttu-id="87ad2-130">New-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="87ad2-130">New-AzureRmStreamAnalyticsInput</span></span>](./New-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="87ad2-131">Remove-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="87ad2-131">Remove-AzureRmStreamAnalyticsInput</span></span>](./Remove-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="87ad2-132">Test-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="87ad2-132">Test-AzureRmStreamAnalyticsInput</span></span>](./Test-AzureRmStreamAnalyticsInput.md)



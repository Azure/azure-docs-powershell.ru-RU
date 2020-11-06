---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM
ms.assetid: F371FD62-D138-4610-84A1-93EDC42D6AAC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/get-azurermstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsInput.md
ms.openlocfilehash: 724441a09ec2714048ec43b781f5792903bce73a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558740"
---
# <span data-ttu-id="44680-101">Get-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="44680-101">Get-AzureRmStreamAnalyticsInput</span></span>

## <span data-ttu-id="44680-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="44680-102">SYNOPSIS</span></span>
<span data-ttu-id="44680-103">Возвращает входные данные для задания Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="44680-103">Gets Stream Analytics job inputs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="44680-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="44680-104">SYNTAX</span></span>

```
Get-AzureRmStreamAnalyticsInput [-JobName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="44680-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="44680-105">DESCRIPTION</span></span>
<span data-ttu-id="44680-106">Командлет **Get-AzureRmStreamAnalyticsInput** перечисляет все входные данные, определенные в задании Stream Analytics, или получает сведения о конкретных входных данных.</span><span class="sxs-lookup"><span data-stu-id="44680-106">The **Get-AzureRmStreamAnalyticsInput** cmdlet lists all of the inputs that are defined in a Stream Analytics job or gets information about a specific input.</span></span>

## <span data-ttu-id="44680-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="44680-107">EXAMPLES</span></span>

### <span data-ttu-id="44680-108">Пример 1: получение сведений о входных данных, определенных для задания</span><span class="sxs-lookup"><span data-stu-id="44680-108">EXAMPLE 1: Get information about the inputs defined on a job</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob"
```

<span data-ttu-id="44680-109">Эта команда возвращает сведения обо всех входных данных, определенных для задания StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="44680-109">This command returns information about all the inputs defined on the job StreamingJob.</span></span>

### <span data-ttu-id="44680-110">Пример 2: получение сведений о конкретном вводе, определенном для задания</span><span class="sxs-lookup"><span data-stu-id="44680-110">EXAMPLE 2: Get information about a specific input defined on a job</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EntryStream"
```

<span data-ttu-id="44680-111">Эта команда возвращает сведения о входных данных с именем EntryStream, определенных в задании StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="44680-111">This command returns information about the input named EntryStream defined on the job StreamingJob.</span></span>

## <span data-ttu-id="44680-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="44680-112">PARAMETERS</span></span>

### <span data-ttu-id="44680-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44680-113">-DefaultProfile</span></span>
<span data-ttu-id="44680-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="44680-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="44680-115">-JobName</span><span class="sxs-lookup"><span data-stu-id="44680-115">-JobName</span></span>
<span data-ttu-id="44680-116">Указывает имя задания Azure Stream Analytics, к которому относятся входные данные Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="44680-116">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="44680-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="44680-117">-Name</span></span>
<span data-ttu-id="44680-118">Указывает имя входных данных Azure Stream Analytics, которые нужно извлечь.</span><span class="sxs-lookup"><span data-stu-id="44680-118">Specifies the name of the Azure Stream Analytics input to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44680-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44680-119">-ResourceGroupName</span></span>
<span data-ttu-id="44680-120">Указывает имя группы ресурсов, к которой относятся входные данные Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="44680-120">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="44680-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44680-121">CommonParameters</span></span>
<span data-ttu-id="44680-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="44680-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44680-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44680-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44680-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="44680-124">INPUTS</span></span>

### <span data-ttu-id="44680-125">Ничего</span><span class="sxs-lookup"><span data-stu-id="44680-125">None</span></span>
<span data-ttu-id="44680-126">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="44680-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="44680-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="44680-127">OUTPUTS</span></span>

### <span data-ttu-id="44680-128">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. StreamAnalytics. Models. PSInput, Microsoft. Azure. Commands. StreamAnalytics]] Microsoft. Azure. Commands. StreamAnalytics. Models. PSInput</span><span class="sxs-lookup"><span data-stu-id="44680-128">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.StreamAnalytics.Models.PSInput, Microsoft.Azure.Commands.StreamAnalytics]]            Microsoft.Azure.Commands.StreamAnalytics.Models.PSInput</span></span>

## <span data-ttu-id="44680-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="44680-129">NOTES</span></span>

## <span data-ttu-id="44680-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="44680-130">RELATED LINKS</span></span>

[<span data-ttu-id="44680-131">New-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="44680-131">New-AzureRmStreamAnalyticsInput</span></span>](./New-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="44680-132">Remove-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="44680-132">Remove-AzureRmStreamAnalyticsInput</span></span>](./Remove-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="44680-133">Test-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="44680-133">Test-AzureRmStreamAnalyticsInput</span></span>](./Test-AzureRmStreamAnalyticsInput.md)



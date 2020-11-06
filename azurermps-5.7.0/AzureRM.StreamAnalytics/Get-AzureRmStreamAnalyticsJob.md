---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 1D10C1EA-632A-4953-85B1-596A45C30B24
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/get-azurermstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsJob.md
ms.openlocfilehash: a2bf5146958e10dc60c656f08a329d2ec01d1eeb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561327"
---
# <span data-ttu-id="5d08e-101">Get-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="5d08e-101">Get-AzureRmStreamAnalyticsJob</span></span>

## <span data-ttu-id="5d08e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5d08e-102">SYNOPSIS</span></span>
<span data-ttu-id="5d08e-103">Возвращает сведения о заданиях Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="5d08e-103">Gets Stream Analytics jobs information.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5d08e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5d08e-104">SYNTAX</span></span>

### <span data-ttu-id="5d08e-105">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5d08e-105">ByResourceGroup</span></span>
```
Get-AzureRmStreamAnalyticsJob [-ResourceGroupName] <String> [[-Name] <String>] [-NoExpand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5d08e-106">BySubscription</span><span class="sxs-lookup"><span data-stu-id="5d08e-106">BySubscription</span></span>
```
Get-AzureRmStreamAnalyticsJob [-NoExpand] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5d08e-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5d08e-107">DESCRIPTION</span></span>
<span data-ttu-id="5d08e-108">Командлет **Get-AzureRmStreamAnalyticsJob** перечисляет все задания Stream Analytics, определенные в подписке Azure или указанной группе ресурсов, или получает сведения о задании для определенного задания в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5d08e-108">The **Get-AzureRmStreamAnalyticsJob** cmdlet lists all Stream Analytics jobs defined in the Azure subscription or specified resource group or gets job information about a specific job within a resource group.</span></span>

## <span data-ttu-id="5d08e-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5d08e-109">EXAMPLES</span></span>

### <span data-ttu-id="5d08e-110">Пример 1: получение сведений обо всех заданиях в подписке</span><span class="sxs-lookup"><span data-stu-id="5d08e-110">EXAMPLE 1: Get information about all jobs in a subscription</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsJob
```

<span data-ttu-id="5d08e-111">Эта команда возвращает сведения обо всех заданиях Stream Analytics в подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="5d08e-111">This command returns information about all the Stream Analytics jobs in the Azure subscription.</span></span>

### <span data-ttu-id="5d08e-112">Пример 2: получение сведений обо всех заданиях в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="5d08e-112">EXAMPLE 2: Get information about all jobs in a resource group</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US"
```

<span data-ttu-id="5d08e-113">Эта команда возвращает сведения обо всех заданиях Stream Analytics в группе ресурсов StreamAnalytics — по умолчанию — Западная часть США.</span><span class="sxs-lookup"><span data-stu-id="5d08e-113">This command returns information about all the Stream Analytics jobs in the resource group StreamAnalytics-Default-West-US.</span></span>

### <span data-ttu-id="5d08e-114">Пример 3: получение сведений о конкретном задании в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="5d08e-114">EXAMPLE 3: Get information about a specific job in a resource group</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="5d08e-115">Эта команда возвращает сведения о задании Stream Analytics StreamingJob в группе ресурсов StreamAnalytics-Default-Западная часть US.</span><span class="sxs-lookup"><span data-stu-id="5d08e-115">This command returns information about the Stream Analytics job StreamingJob in the resource group StreamAnalytics-Default-West-US.</span></span>

## <span data-ttu-id="5d08e-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5d08e-116">PARAMETERS</span></span>

### <span data-ttu-id="5d08e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d08e-117">-DefaultProfile</span></span>
<span data-ttu-id="5d08e-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5d08e-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5d08e-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5d08e-119">-Name</span></span>
<span data-ttu-id="5d08e-120">Указывает имя задания Azure Stream Analytics, которое требуется извлечь.</span><span class="sxs-lookup"><span data-stu-id="5d08e-120">Specifies the name of the Azure Stream Analytics job to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceGroup
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d08e-121">-NOEXPAND</span><span class="sxs-lookup"><span data-stu-id="5d08e-121">-NoExpand</span></span>
<span data-ttu-id="5d08e-122">Указывает, что командлет извлекает задание Azure Stream Analytics, но не возвращает сведения о входных данных, выходах и преобразованиях.</span><span class="sxs-lookup"><span data-stu-id="5d08e-122">Indicates the cmdlet will retrieve the Azure Stream Analytics job, but not return information on its inputs, outputs, and transformation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d08e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d08e-123">-ResourceGroupName</span></span>
<span data-ttu-id="5d08e-124">Указывает имя группы ресурсов, к которой относится задание Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="5d08e-124">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceGroup
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d08e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d08e-125">CommonParameters</span></span>
<span data-ttu-id="5d08e-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5d08e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d08e-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d08e-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d08e-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5d08e-128">INPUTS</span></span>

### <span data-ttu-id="5d08e-129">Ничего</span><span class="sxs-lookup"><span data-stu-id="5d08e-129">None</span></span>
<span data-ttu-id="5d08e-130">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="5d08e-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5d08e-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5d08e-131">OUTPUTS</span></span>

### <span data-ttu-id="5d08e-132">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. StreamAnalytics. Models. PSJob, Microsoft. Azure. Commands. StreamAnalytics]] Microsoft. Azure. Commands. StreamAnalytics. Models. PSJob</span><span class="sxs-lookup"><span data-stu-id="5d08e-132">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.StreamAnalytics.Models.PSJob, Microsoft.Azure.Commands.StreamAnalytics]]            Microsoft.Azure.Commands.StreamAnalytics.Models.PSJob</span></span>

## <span data-ttu-id="5d08e-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="5d08e-133">NOTES</span></span>

## <span data-ttu-id="5d08e-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5d08e-134">RELATED LINKS</span></span>

[<span data-ttu-id="5d08e-135">New-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="5d08e-135">New-AzureRmStreamAnalyticsJob</span></span>](./New-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="5d08e-136">Remove-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="5d08e-136">Remove-AzureRmStreamAnalyticsJob</span></span>](./Remove-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="5d08e-137">Start-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="5d08e-137">Start-AzureRmStreamAnalyticsJob</span></span>](./Start-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="5d08e-138">Остановить-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="5d08e-138">Stop-AzureRmStreamAnalyticsJob</span></span>](./Stop-AzureRmStreamAnalyticsJob.md)



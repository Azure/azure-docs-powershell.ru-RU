---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 1D10C1EA-632A-4953-85B1-596A45C30B24
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsJob.md
ms.openlocfilehash: 826089ca0db48e89138e9df78f0aa483b110ba30
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94077496"
---
# <span data-ttu-id="b5433-101">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="b5433-101">Get-AzStreamAnalyticsJob</span></span>

## <span data-ttu-id="b5433-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b5433-102">SYNOPSIS</span></span>
<span data-ttu-id="b5433-103">Возвращает сведения о заданиях Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="b5433-103">Gets Stream Analytics jobs information.</span></span>

## <span data-ttu-id="b5433-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b5433-104">SYNTAX</span></span>

### <span data-ttu-id="b5433-105">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b5433-105">ByResourceGroup</span></span>
```
Get-AzStreamAnalyticsJob [-ResourceGroupName] <String> [[-Name] <String>] [-NoExpand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b5433-106">BySubscription</span><span class="sxs-lookup"><span data-stu-id="b5433-106">BySubscription</span></span>
```
Get-AzStreamAnalyticsJob [-NoExpand] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b5433-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b5433-107">DESCRIPTION</span></span>
<span data-ttu-id="b5433-108">Командлет **Get-AzStreamAnalyticsJob** перечисляет все задания Stream Analytics, определенные в подписке Azure или указанной группе ресурсов, или получает сведения о задании для определенного задания в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b5433-108">The **Get-AzStreamAnalyticsJob** cmdlet lists all Stream Analytics jobs defined in the Azure subscription or specified resource group or gets job information about a specific job within a resource group.</span></span>

## <span data-ttu-id="b5433-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b5433-109">EXAMPLES</span></span>

### <span data-ttu-id="b5433-110">Пример 1: получение сведений обо всех заданиях в подписке</span><span class="sxs-lookup"><span data-stu-id="b5433-110">EXAMPLE 1: Get information about all jobs in a subscription</span></span>
```
PS C:\>Get-AzStreamAnalyticsJob
```

<span data-ttu-id="b5433-111">Эта команда возвращает сведения обо всех заданиях Stream Analytics в подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="b5433-111">This command returns information about all the Stream Analytics jobs in the Azure subscription.</span></span>

### <span data-ttu-id="b5433-112">Пример 2: получение сведений обо всех заданиях в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="b5433-112">EXAMPLE 2: Get information about all jobs in a resource group</span></span>
```
PS C:\>Get-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US"
```

<span data-ttu-id="b5433-113">Эта команда возвращает сведения обо всех заданиях Stream Analytics в группе ресурсов StreamAnalytics — по умолчанию — Западная часть США.</span><span class="sxs-lookup"><span data-stu-id="b5433-113">This command returns information about all the Stream Analytics jobs in the resource group StreamAnalytics-Default-West-US.</span></span>

### <span data-ttu-id="b5433-114">Пример 3: получение сведений о конкретном задании в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="b5433-114">EXAMPLE 3: Get information about a specific job in a resource group</span></span>
```
PS C:\>Get-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="b5433-115">Эта команда возвращает сведения о задании Stream Analytics StreamingJob в группе ресурсов StreamAnalytics-Default-Западная часть US.</span><span class="sxs-lookup"><span data-stu-id="b5433-115">This command returns information about the Stream Analytics job StreamingJob in the resource group StreamAnalytics-Default-West-US.</span></span>

## <span data-ttu-id="b5433-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b5433-116">PARAMETERS</span></span>

### <span data-ttu-id="b5433-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5433-117">-DefaultProfile</span></span>
<span data-ttu-id="b5433-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b5433-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b5433-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b5433-119">-Name</span></span>
<span data-ttu-id="b5433-120">Указывает имя задания Azure Stream Analytics, которое требуется извлечь.</span><span class="sxs-lookup"><span data-stu-id="b5433-120">Specifies the name of the Azure Stream Analytics job to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5433-121">-NOEXPAND</span><span class="sxs-lookup"><span data-stu-id="b5433-121">-NoExpand</span></span>
<span data-ttu-id="b5433-122">Указывает, что командлет извлекает задание Azure Stream Analytics, но не возвращает сведения о входных данных, выходах и преобразованиях.</span><span class="sxs-lookup"><span data-stu-id="b5433-122">Indicates the cmdlet will retrieve the Azure Stream Analytics job, but not return information on its inputs, outputs, and transformation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5433-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5433-123">-ResourceGroupName</span></span>
<span data-ttu-id="b5433-124">Указывает имя группы ресурсов, к которой относится задание Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="b5433-124">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5433-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5433-125">CommonParameters</span></span>
<span data-ttu-id="b5433-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b5433-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5433-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5433-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5433-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b5433-128">INPUTS</span></span>

### <span data-ttu-id="b5433-129">System. String</span><span class="sxs-lookup"><span data-stu-id="b5433-129">System.String</span></span>

### <span data-ttu-id="b5433-130">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b5433-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b5433-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b5433-131">OUTPUTS</span></span>

### <span data-ttu-id="b5433-132">Microsoft. Azure. Commands. StreamAnalytics. Models. PSJob</span><span class="sxs-lookup"><span data-stu-id="b5433-132">Microsoft.Azure.Commands.StreamAnalytics.Models.PSJob</span></span>

## <span data-ttu-id="b5433-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="b5433-133">NOTES</span></span>

## <span data-ttu-id="b5433-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b5433-134">RELATED LINKS</span></span>

[<span data-ttu-id="b5433-135">New-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="b5433-135">New-AzStreamAnalyticsJob</span></span>](./New-AzStreamAnalyticsJob.md)

[<span data-ttu-id="b5433-136">Remove-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="b5433-136">Remove-AzStreamAnalyticsJob</span></span>](./Remove-AzStreamAnalyticsJob.md)

[<span data-ttu-id="b5433-137">Start-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="b5433-137">Start-AzStreamAnalyticsJob</span></span>](./Start-AzStreamAnalyticsJob.md)

[<span data-ttu-id="b5433-138">Остановить-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="b5433-138">Stop-AzStreamAnalyticsJob</span></span>](./Stop-AzStreamAnalyticsJob.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 1D10C1EA-632A-4953-85B1-596A45C30B24
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsJob.md
ms.openlocfilehash: 630f32bc9dd4542ad022ed7b65ec85f6456367b5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93728463"
---
# <span data-ttu-id="e41eb-101">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="e41eb-101">Get-AzStreamAnalyticsJob</span></span>

## <span data-ttu-id="e41eb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e41eb-102">SYNOPSIS</span></span>
<span data-ttu-id="e41eb-103">Возвращает сведения о заданиях Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="e41eb-103">Gets Stream Analytics jobs information.</span></span>

## <span data-ttu-id="e41eb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e41eb-104">SYNTAX</span></span>

### <span data-ttu-id="e41eb-105">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e41eb-105">ByResourceGroup</span></span>
```
Get-AzStreamAnalyticsJob [-ResourceGroupName] <String> [[-Name] <String>] [-NoExpand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e41eb-106">BySubscription</span><span class="sxs-lookup"><span data-stu-id="e41eb-106">BySubscription</span></span>
```
Get-AzStreamAnalyticsJob [-NoExpand] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e41eb-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e41eb-107">DESCRIPTION</span></span>
<span data-ttu-id="e41eb-108">Командлет **Get-AzStreamAnalyticsJob** перечисляет все задания Stream Analytics, определенные в подписке Azure или указанной группе ресурсов, или получает сведения о задании для определенного задания в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e41eb-108">The **Get-AzStreamAnalyticsJob** cmdlet lists all Stream Analytics jobs defined in the Azure subscription or specified resource group or gets job information about a specific job within a resource group.</span></span>

## <span data-ttu-id="e41eb-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e41eb-109">EXAMPLES</span></span>

### <span data-ttu-id="e41eb-110">Пример 1: получение сведений обо всех заданиях в подписке</span><span class="sxs-lookup"><span data-stu-id="e41eb-110">EXAMPLE 1: Get information about all jobs in a subscription</span></span>
```
PS C:\>Get-AzStreamAnalyticsJob
```

<span data-ttu-id="e41eb-111">Эта команда возвращает сведения обо всех заданиях Stream Analytics в подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="e41eb-111">This command returns information about all the Stream Analytics jobs in the Azure subscription.</span></span>

### <span data-ttu-id="e41eb-112">Пример 2: получение сведений обо всех заданиях в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="e41eb-112">EXAMPLE 2: Get information about all jobs in a resource group</span></span>
```
PS C:\>Get-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US"
```

<span data-ttu-id="e41eb-113">Эта команда возвращает сведения обо всех заданиях Stream Analytics в группе ресурсов StreamAnalytics — по умолчанию — Западная часть США.</span><span class="sxs-lookup"><span data-stu-id="e41eb-113">This command returns information about all the Stream Analytics jobs in the resource group StreamAnalytics-Default-West-US.</span></span>

### <span data-ttu-id="e41eb-114">Пример 3: получение сведений о конкретном задании в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="e41eb-114">EXAMPLE 3: Get information about a specific job in a resource group</span></span>
```
PS C:\>Get-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="e41eb-115">Эта команда возвращает сведения о задании Stream Analytics StreamingJob в группе ресурсов StreamAnalytics-Default-Западная часть US.</span><span class="sxs-lookup"><span data-stu-id="e41eb-115">This command returns information about the Stream Analytics job StreamingJob in the resource group StreamAnalytics-Default-West-US.</span></span>

## <span data-ttu-id="e41eb-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e41eb-116">PARAMETERS</span></span>

### <span data-ttu-id="e41eb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e41eb-117">-DefaultProfile</span></span>
<span data-ttu-id="e41eb-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e41eb-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e41eb-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e41eb-119">-Name</span></span>
<span data-ttu-id="e41eb-120">Указывает имя задания Azure Stream Analytics, которое требуется извлечь.</span><span class="sxs-lookup"><span data-stu-id="e41eb-120">Specifies the name of the Azure Stream Analytics job to retrieve.</span></span>

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

### <span data-ttu-id="e41eb-121">-NOEXPAND</span><span class="sxs-lookup"><span data-stu-id="e41eb-121">-NoExpand</span></span>
<span data-ttu-id="e41eb-122">Указывает, что командлет извлекает задание Azure Stream Analytics, но не возвращает сведения о входных данных, выходах и преобразованиях.</span><span class="sxs-lookup"><span data-stu-id="e41eb-122">Indicates the cmdlet will retrieve the Azure Stream Analytics job, but not return information on its inputs, outputs, and transformation.</span></span>

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

### <span data-ttu-id="e41eb-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e41eb-123">-ResourceGroupName</span></span>
<span data-ttu-id="e41eb-124">Указывает имя группы ресурсов, к которой относится задание Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="e41eb-124">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

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

### <span data-ttu-id="e41eb-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e41eb-125">CommonParameters</span></span>
<span data-ttu-id="e41eb-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e41eb-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e41eb-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e41eb-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e41eb-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e41eb-128">INPUTS</span></span>

### <span data-ttu-id="e41eb-129">System. String</span><span class="sxs-lookup"><span data-stu-id="e41eb-129">System.String</span></span>

### <span data-ttu-id="e41eb-130">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="e41eb-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e41eb-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e41eb-131">OUTPUTS</span></span>

### <span data-ttu-id="e41eb-132">Microsoft. Azure. Commands. StreamAnalytics. Models. PSJob</span><span class="sxs-lookup"><span data-stu-id="e41eb-132">Microsoft.Azure.Commands.StreamAnalytics.Models.PSJob</span></span>

## <span data-ttu-id="e41eb-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="e41eb-133">NOTES</span></span>

## <span data-ttu-id="e41eb-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e41eb-134">RELATED LINKS</span></span>

[<span data-ttu-id="e41eb-135">New-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="e41eb-135">New-AzStreamAnalyticsJob</span></span>](./New-AzStreamAnalyticsJob.md)

[<span data-ttu-id="e41eb-136">Remove-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="e41eb-136">Remove-AzStreamAnalyticsJob</span></span>](./Remove-AzStreamAnalyticsJob.md)

[<span data-ttu-id="e41eb-137">Start-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="e41eb-137">Start-AzStreamAnalyticsJob</span></span>](./Start-AzStreamAnalyticsJob.md)

[<span data-ttu-id="e41eb-138">Остановить-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="e41eb-138">Stop-AzStreamAnalyticsJob</span></span>](./Stop-AzStreamAnalyticsJob.md)



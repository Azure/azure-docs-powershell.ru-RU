---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 1D10C1EA-632A-4953-85B1-596A45C30B24
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsJob.md
ms.openlocfilehash: 826089ca0db48e89138e9df78f0aa483b110ba30
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100217092"
---
# <span data-ttu-id="cdc28-101">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="cdc28-101">Get-AzStreamAnalyticsJob</span></span>

## <span data-ttu-id="cdc28-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cdc28-102">SYNOPSIS</span></span>
<span data-ttu-id="cdc28-103">Получает сведения о заданиях в stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="cdc28-103">Gets Stream Analytics jobs information.</span></span>

## <span data-ttu-id="cdc28-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="cdc28-104">SYNTAX</span></span>

### <span data-ttu-id="cdc28-105">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="cdc28-105">ByResourceGroup</span></span>
```
Get-AzStreamAnalyticsJob [-ResourceGroupName] <String> [[-Name] <String>] [-NoExpand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cdc28-106">BySubscription</span><span class="sxs-lookup"><span data-stu-id="cdc28-106">BySubscription</span></span>
```
Get-AzStreamAnalyticsJob [-NoExpand] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cdc28-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cdc28-107">DESCRIPTION</span></span>
<span data-ttu-id="cdc28-108">В **этом** списке перечислены все задания аналитики Stream, определенные в подписке Azure или указанной группе ресурсов, а также сведения об определенном задании в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cdc28-108">The **Get-AzStreamAnalyticsJob** cmdlet lists all Stream Analytics jobs defined in the Azure subscription or specified resource group or gets job information about a specific job within a resource group.</span></span>

## <span data-ttu-id="cdc28-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="cdc28-109">EXAMPLES</span></span>

### <span data-ttu-id="cdc28-110">ПРИМЕР 1. Просмотр сведений обо всех заданиях в подписке</span><span class="sxs-lookup"><span data-stu-id="cdc28-110">EXAMPLE 1: Get information about all jobs in a subscription</span></span>
```
PS C:\>Get-AzStreamAnalyticsJob
```

<span data-ttu-id="cdc28-111">Эта команда возвращает сведения обо всех заданиях аналитики Stream в подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="cdc28-111">This command returns information about all the Stream Analytics jobs in the Azure subscription.</span></span>

### <span data-ttu-id="cdc28-112">ПРИМЕР 2. Просмотр сведений обо всех заданиях в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="cdc28-112">EXAMPLE 2: Get information about all jobs in a resource group</span></span>
```
PS C:\>Get-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US"
```

<span data-ttu-id="cdc28-113">Эта команда возвращает сведения обо всех заданиях Аналитики StreamAnalytics в группе ресурсов StreamAnalytics-Default-West-US.</span><span class="sxs-lookup"><span data-stu-id="cdc28-113">This command returns information about all the Stream Analytics jobs in the resource group StreamAnalytics-Default-West-US.</span></span>

### <span data-ttu-id="cdc28-114">ПРИМЕР 3. Просмотр сведений об определенном заданиях в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="cdc28-114">EXAMPLE 3: Get information about a specific job in a resource group</span></span>
```
PS C:\>Get-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="cdc28-115">Эта команда возвращает сведения о командной работе Stream Analytics StreamingJob в группе ресурсов StreamAnalytics-Default-West-US.</span><span class="sxs-lookup"><span data-stu-id="cdc28-115">This command returns information about the Stream Analytics job StreamingJob in the resource group StreamAnalytics-Default-West-US.</span></span>

## <span data-ttu-id="cdc28-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cdc28-116">PARAMETERS</span></span>

### <span data-ttu-id="cdc28-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdc28-117">-DefaultProfile</span></span>
<span data-ttu-id="cdc28-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cdc28-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cdc28-119">-Name</span><span class="sxs-lookup"><span data-stu-id="cdc28-119">-Name</span></span>
<span data-ttu-id="cdc28-120">Указывает имя задания аналитики Azure Stream Analytics, которое нужно получить.</span><span class="sxs-lookup"><span data-stu-id="cdc28-120">Specifies the name of the Azure Stream Analytics job to retrieve.</span></span>

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

### <span data-ttu-id="cdc28-121">-NoExpand</span><span class="sxs-lookup"><span data-stu-id="cdc28-121">-NoExpand</span></span>
<span data-ttu-id="cdc28-122">Указывает на то, что он получит задание Azure Stream Analytics, но не возвратит сведения о входных данных, результатах и преобразовании.</span><span class="sxs-lookup"><span data-stu-id="cdc28-122">Indicates the cmdlet will retrieve the Azure Stream Analytics job, but not return information on its inputs, outputs, and transformation.</span></span>

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

### <span data-ttu-id="cdc28-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cdc28-123">-ResourceGroupName</span></span>
<span data-ttu-id="cdc28-124">Имя группы ресурсов, к которой относится задание Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="cdc28-124">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

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

### <span data-ttu-id="cdc28-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdc28-125">CommonParameters</span></span>
<span data-ttu-id="cdc28-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cdc28-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdc28-127">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cdc28-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdc28-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cdc28-128">INPUTS</span></span>

### <span data-ttu-id="cdc28-129">System.String</span><span class="sxs-lookup"><span data-stu-id="cdc28-129">System.String</span></span>

### <span data-ttu-id="cdc28-130">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="cdc28-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="cdc28-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="cdc28-131">OUTPUTS</span></span>

### <span data-ttu-id="cdc28-132">Microsoft.Azure.Commands.StreamAnalytics.Models.PSJob</span><span class="sxs-lookup"><span data-stu-id="cdc28-132">Microsoft.Azure.Commands.StreamAnalytics.Models.PSJob</span></span>

## <span data-ttu-id="cdc28-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="cdc28-133">NOTES</span></span>

## <span data-ttu-id="cdc28-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cdc28-134">RELATED LINKS</span></span>

[<span data-ttu-id="cdc28-135">New-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="cdc28-135">New-AzStreamAnalyticsJob</span></span>](./New-AzStreamAnalyticsJob.md)

[<span data-ttu-id="cdc28-136">Remove-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="cdc28-136">Remove-AzStreamAnalyticsJob</span></span>](./Remove-AzStreamAnalyticsJob.md)

[<span data-ttu-id="cdc28-137">Start-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="cdc28-137">Start-AzStreamAnalyticsJob</span></span>](./Start-AzStreamAnalyticsJob.md)

[<span data-ttu-id="cdc28-138">Stop-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="cdc28-138">Stop-AzStreamAnalyticsJob</span></span>](./Stop-AzStreamAnalyticsJob.md)



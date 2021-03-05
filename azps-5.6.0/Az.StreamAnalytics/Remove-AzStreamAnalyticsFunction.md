---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 75B0776E-32D5-4EE4-B35C-73E13185A4F1
online version: https://docs.microsoft.com/powershell/module/az.streamanalytics/remove-azstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsFunction.md
ms.openlocfilehash: 1a500f883b6896e91767f0f7d560ee28e4bfc9f7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973811"
---
# <span data-ttu-id="0e60a-101">Remove-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="0e60a-101">Remove-AzStreamAnalyticsFunction</span></span>

## <span data-ttu-id="0e60a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0e60a-102">SYNOPSIS</span></span>
<span data-ttu-id="0e60a-103">Удаляет функцию из задания анализа Stream.</span><span class="sxs-lookup"><span data-stu-id="0e60a-103">Deletes a function from a Stream Analytics job.</span></span>

## <span data-ttu-id="0e60a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0e60a-104">SYNTAX</span></span>

```
Remove-AzStreamAnalyticsFunction [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e60a-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0e60a-105">DESCRIPTION</span></span>
<span data-ttu-id="0e60a-106">**Cmdlet Remove-AzStreamAnalyticsFunction** удаляет функцию асинхронно из задания Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="0e60a-106">The **Remove-AzStreamAnalyticsFunction** cmdlet deletes a function asynchronously from an Azure Stream Analytics job.</span></span>

## <span data-ttu-id="0e60a-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0e60a-107">EXAMPLES</span></span>

### <span data-ttu-id="0e60a-108">Пример 1. Удаление функции Stream Analytics</span><span class="sxs-lookup"><span data-stu-id="0e60a-108">Example 1: Remove a Stream Analytics function</span></span>
```
PS C:\>Remove-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

<span data-ttu-id="0e60a-109">Эта команда удаляет функцию ScoreTweet из задания StreamJob22.</span><span class="sxs-lookup"><span data-stu-id="0e60a-109">This command removes the function named ScoreTweet from the job named StreamJob22.</span></span>

## <span data-ttu-id="0e60a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0e60a-110">PARAMETERS</span></span>

### <span data-ttu-id="0e60a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e60a-111">-DefaultProfile</span></span>
<span data-ttu-id="0e60a-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0e60a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0e60a-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="0e60a-113">-JobName</span></span>
<span data-ttu-id="0e60a-114">Указывает имя задания Stream Analytics, к которому относится функция.</span><span class="sxs-lookup"><span data-stu-id="0e60a-114">Specifies the name of the Stream Analytics job to which a function belongs.</span></span>
<span data-ttu-id="0e60a-115">Этот cmdlet удаляет функцию из задания, указанного этим параметром.</span><span class="sxs-lookup"><span data-stu-id="0e60a-115">This cmdlet removes a function from the job that this parameter specifies.</span></span>

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

### <span data-ttu-id="0e60a-116">-Name</span><span class="sxs-lookup"><span data-stu-id="0e60a-116">-Name</span></span>
<span data-ttu-id="0e60a-117">Указывает имя функции Stream Analytics, удаляемой этим cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0e60a-117">Specifies the name of the Stream Analytics function that this cmdlet removes.</span></span>

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

### <span data-ttu-id="0e60a-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e60a-118">-ResourceGroupName</span></span>
<span data-ttu-id="0e60a-119">Имя группы ресурсов, к которой относится функция Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="0e60a-119">Specifies the name of the resource group to which a Stream Analytics function belongs.</span></span>
<span data-ttu-id="0e60a-120">Этот cmdlet удаляет функцию в группе ресурсов, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="0e60a-120">This cmdlet deletes a function in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="0e60a-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0e60a-121">-Confirm</span></span>
<span data-ttu-id="0e60a-122">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="0e60a-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e60a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e60a-123">-WhatIf</span></span>
<span data-ttu-id="0e60a-124">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0e60a-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0e60a-125">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="0e60a-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e60a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e60a-126">CommonParameters</span></span>
<span data-ttu-id="0e60a-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e60a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e60a-128">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e60a-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e60a-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0e60a-129">INPUTS</span></span>

### <span data-ttu-id="0e60a-130">System.String</span><span class="sxs-lookup"><span data-stu-id="0e60a-130">System.String</span></span>

## <span data-ttu-id="0e60a-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0e60a-131">OUTPUTS</span></span>

### <span data-ttu-id="0e60a-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0e60a-132">System.Boolean</span></span>

## <span data-ttu-id="0e60a-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0e60a-133">NOTES</span></span>

## <span data-ttu-id="0e60a-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0e60a-134">RELATED LINKS</span></span>

[<span data-ttu-id="0e60a-135">Get-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="0e60a-135">Get-AzStreamAnalyticsFunction</span></span>](./Get-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="0e60a-136">New-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="0e60a-136">New-AzStreamAnalyticsFunction</span></span>](./New-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="0e60a-137">Test-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="0e60a-137">Test-AzStreamAnalyticsFunction</span></span>](./Test-AzStreamAnalyticsFunction.md)



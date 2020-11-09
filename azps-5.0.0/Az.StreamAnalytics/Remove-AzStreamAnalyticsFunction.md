---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 75B0776E-32D5-4EE4-B35C-73E13185A4F1
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/remove-azstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsFunction.md
ms.openlocfilehash: d481cf5ba28a87e098691d4b3fa5c179670d881d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94318203"
---
# <span data-ttu-id="d18e0-101">Remove-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="d18e0-101">Remove-AzStreamAnalyticsFunction</span></span>

## <span data-ttu-id="d18e0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d18e0-102">SYNOPSIS</span></span>
<span data-ttu-id="d18e0-103">Удаляет функцию из задания Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="d18e0-103">Deletes a function from a Stream Analytics job.</span></span>

## <span data-ttu-id="d18e0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d18e0-104">SYNTAX</span></span>

```
Remove-AzStreamAnalyticsFunction [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d18e0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d18e0-105">DESCRIPTION</span></span>
<span data-ttu-id="d18e0-106">Командлет **Remove-AzStreamAnalyticsFunction** удаляет функцию асинхронно из задания Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="d18e0-106">The **Remove-AzStreamAnalyticsFunction** cmdlet deletes a function asynchronously from an Azure Stream Analytics job.</span></span>

## <span data-ttu-id="d18e0-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d18e0-107">EXAMPLES</span></span>

### <span data-ttu-id="d18e0-108">Пример 1: Удаление функции Stream Analytics</span><span class="sxs-lookup"><span data-stu-id="d18e0-108">Example 1: Remove a Stream Analytics function</span></span>
```
PS C:\>Remove-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

<span data-ttu-id="d18e0-109">Эта команда удаляет функцию с именем ScoreTweet из задания с именем StreamJob22.</span><span class="sxs-lookup"><span data-stu-id="d18e0-109">This command removes the function named ScoreTweet from the job named StreamJob22.</span></span>

## <span data-ttu-id="d18e0-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d18e0-110">PARAMETERS</span></span>

### <span data-ttu-id="d18e0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d18e0-111">-DefaultProfile</span></span>
<span data-ttu-id="d18e0-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d18e0-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d18e0-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="d18e0-113">-JobName</span></span>
<span data-ttu-id="d18e0-114">Указывает имя задания Stream Analytics, к которому относится функция.</span><span class="sxs-lookup"><span data-stu-id="d18e0-114">Specifies the name of the Stream Analytics job to which a function belongs.</span></span>
<span data-ttu-id="d18e0-115">Этот командлет удаляет функцию из задания, для которого указан этот параметр.</span><span class="sxs-lookup"><span data-stu-id="d18e0-115">This cmdlet removes a function from the job that this parameter specifies.</span></span>

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

### <span data-ttu-id="d18e0-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d18e0-116">-Name</span></span>
<span data-ttu-id="d18e0-117">Указывает имя функции Stream Analytics, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="d18e0-117">Specifies the name of the Stream Analytics function that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d18e0-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d18e0-118">-ResourceGroupName</span></span>
<span data-ttu-id="d18e0-119">Указывает имя группы ресурсов, к которой относится функция Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="d18e0-119">Specifies the name of the resource group to which a Stream Analytics function belongs.</span></span>
<span data-ttu-id="d18e0-120">Этот командлет удаляет функцию в группе ресурсов, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="d18e0-120">This cmdlet deletes a function in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="d18e0-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d18e0-121">-Confirm</span></span>
<span data-ttu-id="d18e0-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d18e0-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d18e0-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d18e0-123">-WhatIf</span></span>
<span data-ttu-id="d18e0-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d18e0-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d18e0-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d18e0-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d18e0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d18e0-126">CommonParameters</span></span>
<span data-ttu-id="d18e0-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d18e0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d18e0-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d18e0-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d18e0-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d18e0-129">INPUTS</span></span>

### <span data-ttu-id="d18e0-130">System. String</span><span class="sxs-lookup"><span data-stu-id="d18e0-130">System.String</span></span>

## <span data-ttu-id="d18e0-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d18e0-131">OUTPUTS</span></span>

### <span data-ttu-id="d18e0-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d18e0-132">System.Boolean</span></span>

## <span data-ttu-id="d18e0-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="d18e0-133">NOTES</span></span>

## <span data-ttu-id="d18e0-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d18e0-134">RELATED LINKS</span></span>

[<span data-ttu-id="d18e0-135">Get-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="d18e0-135">Get-AzStreamAnalyticsFunction</span></span>](./Get-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="d18e0-136">New-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="d18e0-136">New-AzStreamAnalyticsFunction</span></span>](./New-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="d18e0-137">Test-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="d18e0-137">Test-AzStreamAnalyticsFunction</span></span>](./Test-AzStreamAnalyticsFunction.md)



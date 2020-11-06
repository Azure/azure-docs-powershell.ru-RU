---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM
ms.assetid: 75B0776E-32D5-4EE4-B35C-73E13185A4F1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/remove-azurermstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsFunction.md
ms.openlocfilehash: d76b1139955490189aeb9c2269cc4e9ede8197be
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566031"
---
# <span data-ttu-id="372d5-101">Remove-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="372d5-101">Remove-AzureRmStreamAnalyticsFunction</span></span>

## <span data-ttu-id="372d5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="372d5-102">SYNOPSIS</span></span>
<span data-ttu-id="372d5-103">Удаляет функцию из задания Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="372d5-103">Deletes a function from a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="372d5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="372d5-104">SYNTAX</span></span>

```
Remove-AzureRmStreamAnalyticsFunction [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="372d5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="372d5-105">DESCRIPTION</span></span>
<span data-ttu-id="372d5-106">Командлет **Remove-AzureRmStreamAnalyticsFunction** удаляет функцию асинхронно из задания Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="372d5-106">The **Remove-AzureRmStreamAnalyticsFunction** cmdlet deletes a function asynchronously from an Azure Stream Analytics job.</span></span>

## <span data-ttu-id="372d5-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="372d5-107">EXAMPLES</span></span>

### <span data-ttu-id="372d5-108">Пример 1: Удаление функции Stream Analytics</span><span class="sxs-lookup"><span data-stu-id="372d5-108">Example 1: Remove a Stream Analytics function</span></span>
```
PS C:\>Remove-AzureRmStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

<span data-ttu-id="372d5-109">Эта команда удаляет функцию с именем ScoreTweet из задания с именем StreamJob22.</span><span class="sxs-lookup"><span data-stu-id="372d5-109">This command removes the function named ScoreTweet from the job named StreamJob22.</span></span>

## <span data-ttu-id="372d5-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="372d5-110">PARAMETERS</span></span>

### <span data-ttu-id="372d5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="372d5-111">-DefaultProfile</span></span>
<span data-ttu-id="372d5-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="372d5-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="372d5-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="372d5-113">-JobName</span></span>
<span data-ttu-id="372d5-114">Указывает имя задания Stream Analytics, к которому относится функция.</span><span class="sxs-lookup"><span data-stu-id="372d5-114">Specifies the name of the Stream Analytics job to which a function belongs.</span></span>
<span data-ttu-id="372d5-115">Этот командлет удаляет функцию из задания, для которого указан этот параметр.</span><span class="sxs-lookup"><span data-stu-id="372d5-115">This cmdlet removes a function from the job that this parameter specifies.</span></span>

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

### <span data-ttu-id="372d5-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="372d5-116">-Name</span></span>
<span data-ttu-id="372d5-117">Указывает имя функции Stream Analytics, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="372d5-117">Specifies the name of the Stream Analytics function that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="372d5-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="372d5-118">-ResourceGroupName</span></span>
<span data-ttu-id="372d5-119">Указывает имя группы ресурсов, к которой относится функция Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="372d5-119">Specifies the name of the resource group to which a Stream Analytics function belongs.</span></span>
<span data-ttu-id="372d5-120">Этот командлет удаляет функцию в группе ресурсов, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="372d5-120">This cmdlet deletes a function in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="372d5-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="372d5-121">-Confirm</span></span>
<span data-ttu-id="372d5-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="372d5-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="372d5-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="372d5-123">-WhatIf</span></span>
<span data-ttu-id="372d5-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="372d5-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="372d5-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="372d5-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="372d5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="372d5-126">CommonParameters</span></span>
<span data-ttu-id="372d5-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="372d5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="372d5-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="372d5-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="372d5-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="372d5-129">INPUTS</span></span>

### <span data-ttu-id="372d5-130">Ничего</span><span class="sxs-lookup"><span data-stu-id="372d5-130">None</span></span>
<span data-ttu-id="372d5-131">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="372d5-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="372d5-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="372d5-132">OUTPUTS</span></span>

### <span data-ttu-id="372d5-133">System. Object</span><span class="sxs-lookup"><span data-stu-id="372d5-133">System.Object</span></span>

## <span data-ttu-id="372d5-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="372d5-134">NOTES</span></span>

## <span data-ttu-id="372d5-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="372d5-135">RELATED LINKS</span></span>

[<span data-ttu-id="372d5-136">Get-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="372d5-136">Get-AzureRmStreamAnalyticsFunction</span></span>](./Get-AzureRmStreamAnalyticsFunction.md)

[<span data-ttu-id="372d5-137">New-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="372d5-137">New-AzureRmStreamAnalyticsFunction</span></span>](./New-AzureRmStreamAnalyticsFunction.md)

[<span data-ttu-id="372d5-138">Test-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="372d5-138">Test-AzureRmStreamAnalyticsFunction</span></span>](./Test-AzureRmStreamAnalyticsFunction.md)



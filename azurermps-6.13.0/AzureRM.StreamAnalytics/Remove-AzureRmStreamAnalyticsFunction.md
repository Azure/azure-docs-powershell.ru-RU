---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 75B0776E-32D5-4EE4-B35C-73E13185A4F1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/remove-azurermstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsFunction.md
ms.openlocfilehash: 4429142b19e64939b9fcc90d56c80f67c5296c15
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732712"
---
# <span data-ttu-id="9aaec-101">Remove-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="9aaec-101">Remove-AzureRmStreamAnalyticsFunction</span></span>

## <span data-ttu-id="9aaec-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9aaec-102">SYNOPSIS</span></span>
<span data-ttu-id="9aaec-103">Удаляет функцию из задания Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="9aaec-103">Deletes a function from a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9aaec-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9aaec-104">SYNTAX</span></span>

```
Remove-AzureRmStreamAnalyticsFunction [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9aaec-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9aaec-105">DESCRIPTION</span></span>
<span data-ttu-id="9aaec-106">Командлет **Remove-AzureRmStreamAnalyticsFunction** удаляет функцию асинхронно из задания Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="9aaec-106">The **Remove-AzureRmStreamAnalyticsFunction** cmdlet deletes a function asynchronously from an Azure Stream Analytics job.</span></span>

## <span data-ttu-id="9aaec-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9aaec-107">EXAMPLES</span></span>

### <span data-ttu-id="9aaec-108">Пример 1: Удаление функции Stream Analytics</span><span class="sxs-lookup"><span data-stu-id="9aaec-108">Example 1: Remove a Stream Analytics function</span></span>
```
PS C:\>Remove-AzureRmStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

<span data-ttu-id="9aaec-109">Эта команда удаляет функцию с именем ScoreTweet из задания с именем StreamJob22.</span><span class="sxs-lookup"><span data-stu-id="9aaec-109">This command removes the function named ScoreTweet from the job named StreamJob22.</span></span>

## <span data-ttu-id="9aaec-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9aaec-110">PARAMETERS</span></span>

### <span data-ttu-id="9aaec-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9aaec-111">-DefaultProfile</span></span>
<span data-ttu-id="9aaec-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9aaec-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9aaec-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="9aaec-113">-JobName</span></span>
<span data-ttu-id="9aaec-114">Указывает имя задания Stream Analytics, к которому относится функция.</span><span class="sxs-lookup"><span data-stu-id="9aaec-114">Specifies the name of the Stream Analytics job to which a function belongs.</span></span>
<span data-ttu-id="9aaec-115">Этот командлет удаляет функцию из задания, для которого указан этот параметр.</span><span class="sxs-lookup"><span data-stu-id="9aaec-115">This cmdlet removes a function from the job that this parameter specifies.</span></span>

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

### <span data-ttu-id="9aaec-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9aaec-116">-Name</span></span>
<span data-ttu-id="9aaec-117">Указывает имя функции Stream Analytics, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="9aaec-117">Specifies the name of the Stream Analytics function that this cmdlet removes.</span></span>

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

### <span data-ttu-id="9aaec-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9aaec-118">-ResourceGroupName</span></span>
<span data-ttu-id="9aaec-119">Указывает имя группы ресурсов, к которой относится функция Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="9aaec-119">Specifies the name of the resource group to which a Stream Analytics function belongs.</span></span>
<span data-ttu-id="9aaec-120">Этот командлет удаляет функцию в группе ресурсов, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="9aaec-120">This cmdlet deletes a function in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="9aaec-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9aaec-121">-Confirm</span></span>
<span data-ttu-id="9aaec-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9aaec-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9aaec-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9aaec-123">-WhatIf</span></span>
<span data-ttu-id="9aaec-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9aaec-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9aaec-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9aaec-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9aaec-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9aaec-126">CommonParameters</span></span>
<span data-ttu-id="9aaec-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9aaec-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9aaec-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9aaec-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9aaec-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9aaec-129">INPUTS</span></span>

### <span data-ttu-id="9aaec-130">System. String</span><span class="sxs-lookup"><span data-stu-id="9aaec-130">System.String</span></span>

## <span data-ttu-id="9aaec-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9aaec-131">OUTPUTS</span></span>

### <span data-ttu-id="9aaec-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9aaec-132">System.Boolean</span></span>

## <span data-ttu-id="9aaec-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="9aaec-133">NOTES</span></span>

## <span data-ttu-id="9aaec-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9aaec-134">RELATED LINKS</span></span>

[<span data-ttu-id="9aaec-135">Get-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="9aaec-135">Get-AzureRmStreamAnalyticsFunction</span></span>](./Get-AzureRmStreamAnalyticsFunction.md)

[<span data-ttu-id="9aaec-136">New-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="9aaec-136">New-AzureRmStreamAnalyticsFunction</span></span>](./New-AzureRmStreamAnalyticsFunction.md)

[<span data-ttu-id="9aaec-137">Test-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="9aaec-137">Test-AzureRmStreamAnalyticsFunction</span></span>](./Test-AzureRmStreamAnalyticsFunction.md)



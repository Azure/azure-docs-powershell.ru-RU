---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM
ms.assetid: EE41BE86-37D4-4A2B-9007-D019CD62BA9D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/remove-azurermstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsOutput.md
ms.openlocfilehash: 03cca81794e190a97ce21b7e9ed8c82392db3e36
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732001"
---
# <span data-ttu-id="b8fa5-101">Remove-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="b8fa5-101">Remove-AzureRmStreamAnalyticsOutput</span></span>

## <span data-ttu-id="b8fa5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b8fa5-102">SYNOPSIS</span></span>
<span data-ttu-id="b8fa5-103">Удаляет вывод из задания Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="b8fa5-103">Deletes an output from a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b8fa5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b8fa5-104">SYNTAX</span></span>

```
Remove-AzureRmStreamAnalyticsOutput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8fa5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b8fa5-105">DESCRIPTION</span></span>
<span data-ttu-id="b8fa5-106">Командлет **Remove-AzureRmStreamAnalyticsOutput** асинхронно удаляет выходные данные из задания Stream Analytics в Azure.</span><span class="sxs-lookup"><span data-stu-id="b8fa5-106">The **Remove-AzureRmStreamAnalyticsOutput** cmdlet asynchronously deletes an output from a Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="b8fa5-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b8fa5-107">EXAMPLES</span></span>

### <span data-ttu-id="b8fa5-108">Пример 1: удаление выхода из задания</span><span class="sxs-lookup"><span data-stu-id="b8fa5-108">EXAMPLE 1: Remove an output from a job</span></span>
```
PS C:\>Remove-AzureRmStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="b8fa5-109">Эта команда удаляет выходные данные в StreamingJob задания.</span><span class="sxs-lookup"><span data-stu-id="b8fa5-109">This command removes the output Output in the job StreamingJob.</span></span>

## <span data-ttu-id="b8fa5-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b8fa5-110">PARAMETERS</span></span>

### <span data-ttu-id="b8fa5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8fa5-111">-DefaultProfile</span></span>
<span data-ttu-id="b8fa5-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b8fa5-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b8fa5-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="b8fa5-113">-JobName</span></span>
<span data-ttu-id="b8fa5-114">Указывает имя задания Azure Stream Analytics, к которому относятся выходные данные Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="b8fa5-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="b8fa5-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b8fa5-115">-Name</span></span>
<span data-ttu-id="b8fa5-116">Указывает имя удаляемого выходных данных Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="b8fa5-116">Specifies the name of the Azure Stream Analytics output to remove.</span></span>

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

### <span data-ttu-id="b8fa5-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8fa5-117">-ResourceGroupName</span></span>
<span data-ttu-id="b8fa5-118">Указывает имя группы ресурсов, к которой относятся выходные данные Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="b8fa5-118">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="b8fa5-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b8fa5-119">-Confirm</span></span>
<span data-ttu-id="b8fa5-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b8fa5-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8fa5-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8fa5-121">-WhatIf</span></span>
<span data-ttu-id="b8fa5-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b8fa5-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8fa5-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b8fa5-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8fa5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8fa5-124">CommonParameters</span></span>
<span data-ttu-id="b8fa5-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b8fa5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8fa5-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8fa5-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8fa5-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b8fa5-127">INPUTS</span></span>

### <span data-ttu-id="b8fa5-128">Ничего</span><span class="sxs-lookup"><span data-stu-id="b8fa5-128">None</span></span>
<span data-ttu-id="b8fa5-129">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="b8fa5-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b8fa5-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b8fa5-130">OUTPUTS</span></span>

### <span data-ttu-id="b8fa5-131">System. Object</span><span class="sxs-lookup"><span data-stu-id="b8fa5-131">System.Object</span></span>

## <span data-ttu-id="b8fa5-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="b8fa5-132">NOTES</span></span>

## <span data-ttu-id="b8fa5-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b8fa5-133">RELATED LINKS</span></span>

[<span data-ttu-id="b8fa5-134">Get-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="b8fa5-134">Get-AzureRmStreamAnalyticsOutput</span></span>](./Get-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="b8fa5-135">New-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="b8fa5-135">New-AzureRmStreamAnalyticsOutput</span></span>](./New-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="b8fa5-136">Test-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="b8fa5-136">Test-AzureRmStreamAnalyticsOutput</span></span>](./Test-AzureRmStreamAnalyticsOutput.md)



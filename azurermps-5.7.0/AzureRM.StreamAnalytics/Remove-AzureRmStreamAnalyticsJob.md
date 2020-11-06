---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM
ms.assetid: 2F3BDDFE-7585-4802-BFA5-D110F846A33E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/remove-azurermstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsJob.md
ms.openlocfilehash: 64ebe431333914a907c515744501f4624a7977ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561324"
---
# <span data-ttu-id="5897e-101">Remove-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="5897e-101">Remove-AzureRmStreamAnalyticsJob</span></span>

## <span data-ttu-id="5897e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5897e-102">SYNOPSIS</span></span>
<span data-ttu-id="5897e-103">Удаляет задание Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="5897e-103">Removes a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5897e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5897e-104">SYNTAX</span></span>

```
Remove-AzureRmStreamAnalyticsJob [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5897e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5897e-105">DESCRIPTION</span></span>
<span data-ttu-id="5897e-106">Командлет **Remove-AzureRmStreamAnalyticsJob** асинхронно удаляет определенное задание Stream Analytics в Azure.</span><span class="sxs-lookup"><span data-stu-id="5897e-106">The **Remove-AzureRmStreamAnalyticsJob** cmdlet asynchronously deletes a specific Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="5897e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5897e-107">EXAMPLES</span></span>

### <span data-ttu-id="5897e-108">Пример 1: удаление задания</span><span class="sxs-lookup"><span data-stu-id="5897e-108">EXAMPLE 1: Remove a job</span></span>
```
PS C:\>Remove-AzureRmStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="5897e-109">Эта команда удаляет задание StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="5897e-109">This command removes the job StreamingJob.</span></span>

## <span data-ttu-id="5897e-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5897e-110">PARAMETERS</span></span>

### <span data-ttu-id="5897e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5897e-111">-DefaultProfile</span></span>
<span data-ttu-id="5897e-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5897e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5897e-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5897e-113">-Name</span></span>
<span data-ttu-id="5897e-114">Указывает имя задания Azure Stream Analytics, которое нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="5897e-114">Specifies the name of the Azure Stream Analytics job to remove.</span></span>

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

### <span data-ttu-id="5897e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5897e-115">-ResourceGroupName</span></span>
<span data-ttu-id="5897e-116">Указывает имя группы ресурсов, к которой относится задание Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="5897e-116">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

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

### <span data-ttu-id="5897e-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5897e-117">-Confirm</span></span>
<span data-ttu-id="5897e-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5897e-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5897e-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5897e-119">-WhatIf</span></span>
<span data-ttu-id="5897e-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5897e-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5897e-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5897e-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5897e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5897e-122">CommonParameters</span></span>
<span data-ttu-id="5897e-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5897e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5897e-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5897e-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5897e-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5897e-125">INPUTS</span></span>

### <span data-ttu-id="5897e-126">Ничего</span><span class="sxs-lookup"><span data-stu-id="5897e-126">None</span></span>
<span data-ttu-id="5897e-127">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="5897e-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5897e-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5897e-128">OUTPUTS</span></span>

### <span data-ttu-id="5897e-129">System. Object</span><span class="sxs-lookup"><span data-stu-id="5897e-129">System.Object</span></span>

## <span data-ttu-id="5897e-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="5897e-130">NOTES</span></span>

## <span data-ttu-id="5897e-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5897e-131">RELATED LINKS</span></span>

[<span data-ttu-id="5897e-132">Get-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="5897e-132">Get-AzureRmStreamAnalyticsJob</span></span>](./Get-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="5897e-133">New-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="5897e-133">New-AzureRmStreamAnalyticsJob</span></span>](./New-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="5897e-134">Start-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="5897e-134">Start-AzureRmStreamAnalyticsJob</span></span>](./Start-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="5897e-135">Остановить-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="5897e-135">Stop-AzureRmStreamAnalyticsJob</span></span>](./Stop-AzureRmStreamAnalyticsJob.md)



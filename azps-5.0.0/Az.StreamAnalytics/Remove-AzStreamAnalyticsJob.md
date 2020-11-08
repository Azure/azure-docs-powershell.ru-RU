---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 2F3BDDFE-7585-4802-BFA5-D110F846A33E
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/remove-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsJob.md
ms.openlocfilehash: 65d0e40fd522d223eed2d0462e5c66beb9e9709a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246167"
---
# <span data-ttu-id="241a8-101">Remove-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="241a8-101">Remove-AzStreamAnalyticsJob</span></span>

## <span data-ttu-id="241a8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="241a8-102">SYNOPSIS</span></span>
<span data-ttu-id="241a8-103">Удаляет задание Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="241a8-103">Removes a Stream Analytics job.</span></span>

## <span data-ttu-id="241a8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="241a8-104">SYNTAX</span></span>

```
Remove-AzStreamAnalyticsJob [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="241a8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="241a8-105">DESCRIPTION</span></span>
<span data-ttu-id="241a8-106">Командлет **Remove-AzStreamAnalyticsJob** асинхронно удаляет определенное задание Stream Analytics в Azure.</span><span class="sxs-lookup"><span data-stu-id="241a8-106">The **Remove-AzStreamAnalyticsJob** cmdlet asynchronously deletes a specific Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="241a8-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="241a8-107">EXAMPLES</span></span>

### <span data-ttu-id="241a8-108">Пример 1: удаление задания</span><span class="sxs-lookup"><span data-stu-id="241a8-108">EXAMPLE 1: Remove a job</span></span>
```
PS C:\>Remove-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="241a8-109">Эта команда удаляет задание StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="241a8-109">This command removes the job StreamingJob.</span></span>

## <span data-ttu-id="241a8-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="241a8-110">PARAMETERS</span></span>

### <span data-ttu-id="241a8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="241a8-111">-DefaultProfile</span></span>
<span data-ttu-id="241a8-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="241a8-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="241a8-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="241a8-113">-Name</span></span>
<span data-ttu-id="241a8-114">Указывает имя задания Azure Stream Analytics, которое нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="241a8-114">Specifies the name of the Azure Stream Analytics job to remove.</span></span>

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

### <span data-ttu-id="241a8-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="241a8-115">-ResourceGroupName</span></span>
<span data-ttu-id="241a8-116">Указывает имя группы ресурсов, к которой относится задание Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="241a8-116">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

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

### <span data-ttu-id="241a8-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="241a8-117">-Confirm</span></span>
<span data-ttu-id="241a8-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="241a8-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="241a8-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="241a8-119">-WhatIf</span></span>
<span data-ttu-id="241a8-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="241a8-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="241a8-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="241a8-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="241a8-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="241a8-122">CommonParameters</span></span>
<span data-ttu-id="241a8-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="241a8-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="241a8-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="241a8-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="241a8-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="241a8-125">INPUTS</span></span>

### <span data-ttu-id="241a8-126">System. String</span><span class="sxs-lookup"><span data-stu-id="241a8-126">System.String</span></span>

## <span data-ttu-id="241a8-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="241a8-127">OUTPUTS</span></span>

### <span data-ttu-id="241a8-128">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="241a8-128">System.Boolean</span></span>

## <span data-ttu-id="241a8-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="241a8-129">NOTES</span></span>

## <span data-ttu-id="241a8-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="241a8-130">RELATED LINKS</span></span>

[<span data-ttu-id="241a8-131">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="241a8-131">Get-AzStreamAnalyticsJob</span></span>](./Get-AzStreamAnalyticsJob.md)

[<span data-ttu-id="241a8-132">New-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="241a8-132">New-AzStreamAnalyticsJob</span></span>](./New-AzStreamAnalyticsJob.md)

[<span data-ttu-id="241a8-133">Start-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="241a8-133">Start-AzStreamAnalyticsJob</span></span>](./Start-AzStreamAnalyticsJob.md)

[<span data-ttu-id="241a8-134">Остановить-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="241a8-134">Stop-AzStreamAnalyticsJob</span></span>](./Stop-AzStreamAnalyticsJob.md)



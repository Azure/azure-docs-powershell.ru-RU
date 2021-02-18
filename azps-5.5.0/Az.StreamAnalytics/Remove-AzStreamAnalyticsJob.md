---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 2F3BDDFE-7585-4802-BFA5-D110F846A33E
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/remove-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsJob.md
ms.openlocfilehash: 65d0e40fd522d223eed2d0462e5c66beb9e9709a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100217001"
---
# <span data-ttu-id="865d9-101">Remove-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="865d9-101">Remove-AzStreamAnalyticsJob</span></span>

## <span data-ttu-id="865d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="865d9-102">SYNOPSIS</span></span>
<span data-ttu-id="865d9-103">Удаляет задание Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="865d9-103">Removes a Stream Analytics job.</span></span>

## <span data-ttu-id="865d9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="865d9-104">SYNTAX</span></span>

```
Remove-AzStreamAnalyticsJob [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="865d9-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="865d9-105">DESCRIPTION</span></span>
<span data-ttu-id="865d9-106">С **его учетом** можно асинхронно удалить определенное задание Анализа Stream в Azure.</span><span class="sxs-lookup"><span data-stu-id="865d9-106">The **Remove-AzStreamAnalyticsJob** cmdlet asynchronously deletes a specific Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="865d9-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="865d9-107">EXAMPLES</span></span>

### <span data-ttu-id="865d9-108">ПРИМЕР 1. Удаление задания</span><span class="sxs-lookup"><span data-stu-id="865d9-108">EXAMPLE 1: Remove a job</span></span>
```
PS C:\>Remove-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="865d9-109">Эта команда удаляет задание StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="865d9-109">This command removes the job StreamingJob.</span></span>

## <span data-ttu-id="865d9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="865d9-110">PARAMETERS</span></span>

### <span data-ttu-id="865d9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="865d9-111">-DefaultProfile</span></span>
<span data-ttu-id="865d9-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="865d9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="865d9-113">-Name</span><span class="sxs-lookup"><span data-stu-id="865d9-113">-Name</span></span>
<span data-ttu-id="865d9-114">Указывает имя задания Azure Stream Analytics, которое нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="865d9-114">Specifies the name of the Azure Stream Analytics job to remove.</span></span>

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

### <span data-ttu-id="865d9-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="865d9-115">-ResourceGroupName</span></span>
<span data-ttu-id="865d9-116">Имя группы ресурсов, к которой относится задание Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="865d9-116">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

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

### <span data-ttu-id="865d9-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="865d9-117">-Confirm</span></span>
<span data-ttu-id="865d9-118">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="865d9-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="865d9-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="865d9-119">-WhatIf</span></span>
<span data-ttu-id="865d9-120">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="865d9-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="865d9-121">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="865d9-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="865d9-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="865d9-122">CommonParameters</span></span>
<span data-ttu-id="865d9-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="865d9-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="865d9-124">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="865d9-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="865d9-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="865d9-125">INPUTS</span></span>

### <span data-ttu-id="865d9-126">System.String</span><span class="sxs-lookup"><span data-stu-id="865d9-126">System.String</span></span>

## <span data-ttu-id="865d9-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="865d9-127">OUTPUTS</span></span>

### <span data-ttu-id="865d9-128">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="865d9-128">System.Boolean</span></span>

## <span data-ttu-id="865d9-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="865d9-129">NOTES</span></span>

## <span data-ttu-id="865d9-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="865d9-130">RELATED LINKS</span></span>

[<span data-ttu-id="865d9-131">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="865d9-131">Get-AzStreamAnalyticsJob</span></span>](./Get-AzStreamAnalyticsJob.md)

[<span data-ttu-id="865d9-132">New-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="865d9-132">New-AzStreamAnalyticsJob</span></span>](./New-AzStreamAnalyticsJob.md)

[<span data-ttu-id="865d9-133">Start-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="865d9-133">Start-AzStreamAnalyticsJob</span></span>](./Start-AzStreamAnalyticsJob.md)

[<span data-ttu-id="865d9-134">Stop-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="865d9-134">Stop-AzStreamAnalyticsJob</span></span>](./Stop-AzStreamAnalyticsJob.md)



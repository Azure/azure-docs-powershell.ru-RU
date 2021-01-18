---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 2F3BDDFE-7585-4802-BFA5-D110F846A33E
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/remove-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsJob.md
ms.openlocfilehash: 65d0e40fd522d223eed2d0462e5c66beb9e9709a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98516978"
---
# <span data-ttu-id="ef4d6-101">Remove-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="ef4d6-101">Remove-AzStreamAnalyticsJob</span></span>

## <span data-ttu-id="ef4d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef4d6-102">SYNOPSIS</span></span>
<span data-ttu-id="ef4d6-103">Удаляет задание Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="ef4d6-103">Removes a Stream Analytics job.</span></span>

## <span data-ttu-id="ef4d6-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ef4d6-104">SYNTAX</span></span>

```
Remove-AzStreamAnalyticsJob [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef4d6-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ef4d6-105">DESCRIPTION</span></span>
<span data-ttu-id="ef4d6-106">С **его учетом** можно асинхронно удалить определенное задание Анализа Stream в Azure.</span><span class="sxs-lookup"><span data-stu-id="ef4d6-106">The **Remove-AzStreamAnalyticsJob** cmdlet asynchronously deletes a specific Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="ef4d6-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ef4d6-107">EXAMPLES</span></span>

### <span data-ttu-id="ef4d6-108">ПРИМЕР 1. Удаление задания</span><span class="sxs-lookup"><span data-stu-id="ef4d6-108">EXAMPLE 1: Remove a job</span></span>
```
PS C:\>Remove-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="ef4d6-109">Эта команда удаляет задание StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="ef4d6-109">This command removes the job StreamingJob.</span></span>

## <span data-ttu-id="ef4d6-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ef4d6-110">PARAMETERS</span></span>

### <span data-ttu-id="ef4d6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef4d6-111">-DefaultProfile</span></span>
<span data-ttu-id="ef4d6-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ef4d6-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ef4d6-113">-Name</span><span class="sxs-lookup"><span data-stu-id="ef4d6-113">-Name</span></span>
<span data-ttu-id="ef4d6-114">Указывает имя задания Azure Stream Analytics, которое нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="ef4d6-114">Specifies the name of the Azure Stream Analytics job to remove.</span></span>

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

### <span data-ttu-id="ef4d6-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef4d6-115">-ResourceGroupName</span></span>
<span data-ttu-id="ef4d6-116">Имя группы ресурсов, к которой относится задание Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="ef4d6-116">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

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

### <span data-ttu-id="ef4d6-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ef4d6-117">-Confirm</span></span>
<span data-ttu-id="ef4d6-118">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ef4d6-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef4d6-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef4d6-119">-WhatIf</span></span>
<span data-ttu-id="ef4d6-120">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ef4d6-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef4d6-121">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ef4d6-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef4d6-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef4d6-122">CommonParameters</span></span>
<span data-ttu-id="ef4d6-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef4d6-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef4d6-124">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef4d6-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef4d6-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ef4d6-125">INPUTS</span></span>

### <span data-ttu-id="ef4d6-126">System.String</span><span class="sxs-lookup"><span data-stu-id="ef4d6-126">System.String</span></span>

## <span data-ttu-id="ef4d6-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ef4d6-127">OUTPUTS</span></span>

### <span data-ttu-id="ef4d6-128">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ef4d6-128">System.Boolean</span></span>

## <span data-ttu-id="ef4d6-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ef4d6-129">NOTES</span></span>

## <span data-ttu-id="ef4d6-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ef4d6-130">RELATED LINKS</span></span>

[<span data-ttu-id="ef4d6-131">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="ef4d6-131">Get-AzStreamAnalyticsJob</span></span>](./Get-AzStreamAnalyticsJob.md)

[<span data-ttu-id="ef4d6-132">New-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="ef4d6-132">New-AzStreamAnalyticsJob</span></span>](./New-AzStreamAnalyticsJob.md)

[<span data-ttu-id="ef4d6-133">Start-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="ef4d6-133">Start-AzStreamAnalyticsJob</span></span>](./Start-AzStreamAnalyticsJob.md)

[<span data-ttu-id="ef4d6-134">Stop-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="ef4d6-134">Stop-AzStreamAnalyticsJob</span></span>](./Stop-AzStreamAnalyticsJob.md)



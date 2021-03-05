---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 2F3BDDFE-7585-4802-BFA5-D110F846A33E
online version: https://docs.microsoft.com/powershell/module/az.streamanalytics/remove-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsJob.md
ms.openlocfilehash: 183aa9dd5cc7da6e0d86c1fa1018bcfe405c0f7e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973763"
---
# <span data-ttu-id="fa355-101">Remove-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="fa355-101">Remove-AzStreamAnalyticsJob</span></span>

## <span data-ttu-id="fa355-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa355-102">SYNOPSIS</span></span>
<span data-ttu-id="fa355-103">Удаляет задание Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="fa355-103">Removes a Stream Analytics job.</span></span>

## <span data-ttu-id="fa355-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="fa355-104">SYNTAX</span></span>

```
Remove-AzStreamAnalyticsJob [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa355-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fa355-105">DESCRIPTION</span></span>
<span data-ttu-id="fa355-106">С **его учетной** записью асинхронно удаляются определенные задания Аналитики Stream в Azure.</span><span class="sxs-lookup"><span data-stu-id="fa355-106">The **Remove-AzStreamAnalyticsJob** cmdlet asynchronously deletes a specific Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="fa355-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="fa355-107">EXAMPLES</span></span>

### <span data-ttu-id="fa355-108">ПРИМЕР 1. Удаление задания</span><span class="sxs-lookup"><span data-stu-id="fa355-108">EXAMPLE 1: Remove a job</span></span>
```
PS C:\>Remove-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="fa355-109">Эта команда удаляет задание StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="fa355-109">This command removes the job StreamingJob.</span></span>

## <span data-ttu-id="fa355-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fa355-110">PARAMETERS</span></span>

### <span data-ttu-id="fa355-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa355-111">-DefaultProfile</span></span>
<span data-ttu-id="fa355-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fa355-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fa355-113">-Name</span><span class="sxs-lookup"><span data-stu-id="fa355-113">-Name</span></span>
<span data-ttu-id="fa355-114">Указывает имя задания Azure Stream Analytics, которое нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="fa355-114">Specifies the name of the Azure Stream Analytics job to remove.</span></span>

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

### <span data-ttu-id="fa355-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa355-115">-ResourceGroupName</span></span>
<span data-ttu-id="fa355-116">Имя группы ресурсов, к которой относится задание Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="fa355-116">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

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

### <span data-ttu-id="fa355-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fa355-117">-Confirm</span></span>
<span data-ttu-id="fa355-118">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fa355-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa355-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa355-119">-WhatIf</span></span>
<span data-ttu-id="fa355-120">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fa355-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa355-121">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="fa355-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa355-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa355-122">CommonParameters</span></span>
<span data-ttu-id="fa355-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa355-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa355-124">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa355-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa355-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fa355-125">INPUTS</span></span>

### <span data-ttu-id="fa355-126">System.String</span><span class="sxs-lookup"><span data-stu-id="fa355-126">System.String</span></span>

## <span data-ttu-id="fa355-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="fa355-127">OUTPUTS</span></span>

### <span data-ttu-id="fa355-128">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fa355-128">System.Boolean</span></span>

## <span data-ttu-id="fa355-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="fa355-129">NOTES</span></span>

## <span data-ttu-id="fa355-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fa355-130">RELATED LINKS</span></span>

[<span data-ttu-id="fa355-131">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="fa355-131">Get-AzStreamAnalyticsJob</span></span>](./Get-AzStreamAnalyticsJob.md)

[<span data-ttu-id="fa355-132">New-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="fa355-132">New-AzStreamAnalyticsJob</span></span>](./New-AzStreamAnalyticsJob.md)

[<span data-ttu-id="fa355-133">Start-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="fa355-133">Start-AzStreamAnalyticsJob</span></span>](./Start-AzStreamAnalyticsJob.md)

[<span data-ttu-id="fa355-134">Stop-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="fa355-134">Stop-AzStreamAnalyticsJob</span></span>](./Stop-AzStreamAnalyticsJob.md)



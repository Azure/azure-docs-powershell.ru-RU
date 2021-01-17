---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: EE41BE86-37D4-4A2B-9007-D019CD62BA9D
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/remove-azstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsOutput.md
ms.openlocfilehash: 23f7c8270f3d5c0073be9705e43086aae3a3e903
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98414359"
---
# <span data-ttu-id="54bac-101">Remove-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="54bac-101">Remove-AzStreamAnalyticsOutput</span></span>

## <span data-ttu-id="54bac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54bac-102">SYNOPSIS</span></span>
<span data-ttu-id="54bac-103">Удаляет выходные данные из задания Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="54bac-103">Deletes an output from a Stream Analytics job.</span></span>

## <span data-ttu-id="54bac-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="54bac-104">SYNTAX</span></span>

```
Remove-AzStreamAnalyticsOutput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54bac-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="54bac-105">DESCRIPTION</span></span>
<span data-ttu-id="54bac-106">Асинхронно удалит выходной результат из задания Stream Analytics в Azure с использованием **cmdlet Remove-AzStreamAnalyticsOutput.**</span><span class="sxs-lookup"><span data-stu-id="54bac-106">The **Remove-AzStreamAnalyticsOutput** cmdlet asynchronously deletes an output from a Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="54bac-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="54bac-107">EXAMPLES</span></span>

### <span data-ttu-id="54bac-108">ПРИМЕР 1. Удаление результата из задания</span><span class="sxs-lookup"><span data-stu-id="54bac-108">EXAMPLE 1: Remove an output from a job</span></span>
```
PS C:\>Remove-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="54bac-109">Эта команда удаляет выходные данные из задания StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="54bac-109">This command removes the output Output in the job StreamingJob.</span></span>

## <span data-ttu-id="54bac-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="54bac-110">PARAMETERS</span></span>

### <span data-ttu-id="54bac-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54bac-111">-DefaultProfile</span></span>
<span data-ttu-id="54bac-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="54bac-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="54bac-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="54bac-113">-JobName</span></span>
<span data-ttu-id="54bac-114">Указывает имя задания Azure Stream Analytics, к которому относится выход Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="54bac-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="54bac-115">-Name</span><span class="sxs-lookup"><span data-stu-id="54bac-115">-Name</span></span>
<span data-ttu-id="54bac-116">Указывает имя выходных данных Azure Stream Analytics, которые нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="54bac-116">Specifies the name of the Azure Stream Analytics output to remove.</span></span>

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

### <span data-ttu-id="54bac-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54bac-117">-ResourceGroupName</span></span>
<span data-ttu-id="54bac-118">Имя группы ресурсов, к которой относится выход Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="54bac-118">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="54bac-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="54bac-119">-Confirm</span></span>
<span data-ttu-id="54bac-120">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="54bac-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54bac-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54bac-121">-WhatIf</span></span>
<span data-ttu-id="54bac-122">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="54bac-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54bac-123">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="54bac-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54bac-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54bac-124">CommonParameters</span></span>
<span data-ttu-id="54bac-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54bac-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54bac-126">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54bac-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54bac-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="54bac-127">INPUTS</span></span>

### <span data-ttu-id="54bac-128">System.String</span><span class="sxs-lookup"><span data-stu-id="54bac-128">System.String</span></span>

## <span data-ttu-id="54bac-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="54bac-129">OUTPUTS</span></span>

### <span data-ttu-id="54bac-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="54bac-130">System.Boolean</span></span>

## <span data-ttu-id="54bac-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="54bac-131">NOTES</span></span>

## <span data-ttu-id="54bac-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="54bac-132">RELATED LINKS</span></span>

[<span data-ttu-id="54bac-133">Get-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="54bac-133">Get-AzStreamAnalyticsOutput</span></span>](./Get-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="54bac-134">New-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="54bac-134">New-AzStreamAnalyticsOutput</span></span>](./New-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="54bac-135">Test-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="54bac-135">Test-AzStreamAnalyticsOutput</span></span>](./Test-AzStreamAnalyticsOutput.md)



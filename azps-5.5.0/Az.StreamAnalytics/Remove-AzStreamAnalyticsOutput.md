---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: EE41BE86-37D4-4A2B-9007-D019CD62BA9D
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/remove-azstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsOutput.md
ms.openlocfilehash: 23f7c8270f3d5c0073be9705e43086aae3a3e903
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100216993"
---
# <span data-ttu-id="010c7-101">Remove-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="010c7-101">Remove-AzStreamAnalyticsOutput</span></span>

## <span data-ttu-id="010c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="010c7-102">SYNOPSIS</span></span>
<span data-ttu-id="010c7-103">Удаляет выходные данные из задания Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="010c7-103">Deletes an output from a Stream Analytics job.</span></span>

## <span data-ttu-id="010c7-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="010c7-104">SYNTAX</span></span>

```
Remove-AzStreamAnalyticsOutput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="010c7-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="010c7-105">DESCRIPTION</span></span>
<span data-ttu-id="010c7-106">С **его учетом** можно асинхронно удалить выходные данные из задания Stream Analytics в Azure.</span><span class="sxs-lookup"><span data-stu-id="010c7-106">The **Remove-AzStreamAnalyticsOutput** cmdlet asynchronously deletes an output from a Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="010c7-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="010c7-107">EXAMPLES</span></span>

### <span data-ttu-id="010c7-108">ПРИМЕР 1. Удаление результата из задания</span><span class="sxs-lookup"><span data-stu-id="010c7-108">EXAMPLE 1: Remove an output from a job</span></span>
```
PS C:\>Remove-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="010c7-109">Эта команда удаляет выходные данные из задания StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="010c7-109">This command removes the output Output in the job StreamingJob.</span></span>

## <span data-ttu-id="010c7-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="010c7-110">PARAMETERS</span></span>

### <span data-ttu-id="010c7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="010c7-111">-DefaultProfile</span></span>
<span data-ttu-id="010c7-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="010c7-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="010c7-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="010c7-113">-JobName</span></span>
<span data-ttu-id="010c7-114">Указывает имя задания Azure Stream Analytics, к которому относится выход Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="010c7-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="010c7-115">-Name</span><span class="sxs-lookup"><span data-stu-id="010c7-115">-Name</span></span>
<span data-ttu-id="010c7-116">Указывает имя выходных данных Azure Stream Analytics, которые нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="010c7-116">Specifies the name of the Azure Stream Analytics output to remove.</span></span>

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

### <span data-ttu-id="010c7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="010c7-117">-ResourceGroupName</span></span>
<span data-ttu-id="010c7-118">Имя группы ресурсов, к которой относится выход Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="010c7-118">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="010c7-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="010c7-119">-Confirm</span></span>
<span data-ttu-id="010c7-120">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="010c7-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="010c7-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="010c7-121">-WhatIf</span></span>
<span data-ttu-id="010c7-122">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="010c7-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="010c7-123">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="010c7-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="010c7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="010c7-124">CommonParameters</span></span>
<span data-ttu-id="010c7-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="010c7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="010c7-126">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="010c7-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="010c7-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="010c7-127">INPUTS</span></span>

### <span data-ttu-id="010c7-128">System.String</span><span class="sxs-lookup"><span data-stu-id="010c7-128">System.String</span></span>

## <span data-ttu-id="010c7-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="010c7-129">OUTPUTS</span></span>

### <span data-ttu-id="010c7-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="010c7-130">System.Boolean</span></span>

## <span data-ttu-id="010c7-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="010c7-131">NOTES</span></span>

## <span data-ttu-id="010c7-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="010c7-132">RELATED LINKS</span></span>

[<span data-ttu-id="010c7-133">Get-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="010c7-133">Get-AzStreamAnalyticsOutput</span></span>](./Get-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="010c7-134">New-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="010c7-134">New-AzStreamAnalyticsOutput</span></span>](./New-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="010c7-135">Test-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="010c7-135">Test-AzStreamAnalyticsOutput</span></span>](./Test-AzStreamAnalyticsOutput.md)



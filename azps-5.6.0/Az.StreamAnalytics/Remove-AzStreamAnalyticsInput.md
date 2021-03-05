---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 1449F64F-A8F9-4E8E-B62B-17DEF3A0FB30
online version: https://docs.microsoft.com/powershell/module/az.streamanalytics/remove-azstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsInput.md
ms.openlocfilehash: 2e0443976d36339c9866c08118ef08c37fafac48
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973816"
---
# <span data-ttu-id="2a46f-101">Remove-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="2a46f-101">Remove-AzStreamAnalyticsInput</span></span>

## <span data-ttu-id="2a46f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a46f-102">SYNOPSIS</span></span>
<span data-ttu-id="2a46f-103">Удаляет данные из задания Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="2a46f-103">Deletes an input from a Stream Analytics job.</span></span>

## <span data-ttu-id="2a46f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2a46f-104">SYNTAX</span></span>

```
Remove-AzStreamAnalyticsInput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a46f-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2a46f-105">DESCRIPTION</span></span>
<span data-ttu-id="2a46f-106">Асинхронно удаляются данные из задания Stream Analytics в Azure с использованием **cmdlet Remove-AzStreamAnalyticsInput.**</span><span class="sxs-lookup"><span data-stu-id="2a46f-106">The **Remove-AzStreamAnalyticsInput** cmdlet asynchronously deletes an input from a Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="2a46f-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2a46f-107">EXAMPLES</span></span>

### <span data-ttu-id="2a46f-108">ПРИМЕР 1. Удаление потока ввода из задания</span><span class="sxs-lookup"><span data-stu-id="2a46f-108">EXAMPLE 1: Remove an input stream from a job</span></span>
```
PS C:\>Remove-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EventStream"
```

<span data-ttu-id="2a46f-109">Эта команда удаляет входные данные EventStream из StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="2a46f-109">This command removes the input EventStream from StreamingJob.</span></span>

## <span data-ttu-id="2a46f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2a46f-110">PARAMETERS</span></span>

### <span data-ttu-id="2a46f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a46f-111">-DefaultProfile</span></span>
<span data-ttu-id="2a46f-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2a46f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2a46f-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="2a46f-113">-JobName</span></span>
<span data-ttu-id="2a46f-114">Указывает имя задания Azure Stream Analytics, к которому относится ввод Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="2a46f-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="2a46f-115">-Name</span><span class="sxs-lookup"><span data-stu-id="2a46f-115">-Name</span></span>
<span data-ttu-id="2a46f-116">Указывает имя входных данных azure Stream Analytics, которые нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="2a46f-116">Specifies the name of the Azure Stream Analytics input to remove.</span></span>

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

### <span data-ttu-id="2a46f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a46f-117">-ResourceGroupName</span></span>
<span data-ttu-id="2a46f-118">Имя группы ресурсов, к которой относится ввод Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="2a46f-118">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="2a46f-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2a46f-119">-Confirm</span></span>
<span data-ttu-id="2a46f-120">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="2a46f-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a46f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a46f-121">-WhatIf</span></span>
<span data-ttu-id="2a46f-122">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a46f-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a46f-123">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="2a46f-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a46f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a46f-124">CommonParameters</span></span>
<span data-ttu-id="2a46f-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a46f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a46f-126">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a46f-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a46f-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2a46f-127">INPUTS</span></span>

### <span data-ttu-id="2a46f-128">System.String</span><span class="sxs-lookup"><span data-stu-id="2a46f-128">System.String</span></span>

## <span data-ttu-id="2a46f-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2a46f-129">OUTPUTS</span></span>

### <span data-ttu-id="2a46f-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2a46f-130">System.Boolean</span></span>

## <span data-ttu-id="2a46f-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2a46f-131">NOTES</span></span>

## <span data-ttu-id="2a46f-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2a46f-132">RELATED LINKS</span></span>

[<span data-ttu-id="2a46f-133">New-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="2a46f-133">New-AzStreamAnalyticsInput</span></span>](./New-AzStreamAnalyticsInput.md)

[<span data-ttu-id="2a46f-134">Get-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="2a46f-134">Get-AzStreamAnalyticsInput</span></span>](./Get-AzStreamAnalyticsInput.md)

[<span data-ttu-id="2a46f-135">Test-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="2a46f-135">Test-AzStreamAnalyticsInput</span></span>](./Test-AzStreamAnalyticsInput.md)



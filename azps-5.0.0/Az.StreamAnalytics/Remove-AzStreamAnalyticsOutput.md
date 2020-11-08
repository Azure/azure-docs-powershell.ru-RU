---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: EE41BE86-37D4-4A2B-9007-D019CD62BA9D
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/remove-azstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsOutput.md
ms.openlocfilehash: 23f7c8270f3d5c0073be9705e43086aae3a3e903
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246328"
---
# <span data-ttu-id="c644d-101">Remove-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="c644d-101">Remove-AzStreamAnalyticsOutput</span></span>

## <span data-ttu-id="c644d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c644d-102">SYNOPSIS</span></span>
<span data-ttu-id="c644d-103">Удаляет вывод из задания Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="c644d-103">Deletes an output from a Stream Analytics job.</span></span>

## <span data-ttu-id="c644d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c644d-104">SYNTAX</span></span>

```
Remove-AzStreamAnalyticsOutput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c644d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c644d-105">DESCRIPTION</span></span>
<span data-ttu-id="c644d-106">Командлет **Remove-AzStreamAnalyticsOutput** асинхронно удаляет выходные данные из задания Stream Analytics в Azure.</span><span class="sxs-lookup"><span data-stu-id="c644d-106">The **Remove-AzStreamAnalyticsOutput** cmdlet asynchronously deletes an output from a Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="c644d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c644d-107">EXAMPLES</span></span>

### <span data-ttu-id="c644d-108">Пример 1: удаление выхода из задания</span><span class="sxs-lookup"><span data-stu-id="c644d-108">EXAMPLE 1: Remove an output from a job</span></span>
```
PS C:\>Remove-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="c644d-109">Эта команда удаляет выходные данные в StreamingJob задания.</span><span class="sxs-lookup"><span data-stu-id="c644d-109">This command removes the output Output in the job StreamingJob.</span></span>

## <span data-ttu-id="c644d-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c644d-110">PARAMETERS</span></span>

### <span data-ttu-id="c644d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c644d-111">-DefaultProfile</span></span>
<span data-ttu-id="c644d-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c644d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c644d-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="c644d-113">-JobName</span></span>
<span data-ttu-id="c644d-114">Указывает имя задания Azure Stream Analytics, к которому относятся выходные данные Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="c644d-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="c644d-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c644d-115">-Name</span></span>
<span data-ttu-id="c644d-116">Указывает имя удаляемого выходных данных Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="c644d-116">Specifies the name of the Azure Stream Analytics output to remove.</span></span>

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

### <span data-ttu-id="c644d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c644d-117">-ResourceGroupName</span></span>
<span data-ttu-id="c644d-118">Указывает имя группы ресурсов, к которой относятся выходные данные Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="c644d-118">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="c644d-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c644d-119">-Confirm</span></span>
<span data-ttu-id="c644d-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c644d-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c644d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c644d-121">-WhatIf</span></span>
<span data-ttu-id="c644d-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c644d-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c644d-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c644d-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c644d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c644d-124">CommonParameters</span></span>
<span data-ttu-id="c644d-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c644d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c644d-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c644d-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c644d-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c644d-127">INPUTS</span></span>

### <span data-ttu-id="c644d-128">System. String</span><span class="sxs-lookup"><span data-stu-id="c644d-128">System.String</span></span>

## <span data-ttu-id="c644d-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c644d-129">OUTPUTS</span></span>

### <span data-ttu-id="c644d-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c644d-130">System.Boolean</span></span>

## <span data-ttu-id="c644d-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="c644d-131">NOTES</span></span>

## <span data-ttu-id="c644d-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c644d-132">RELATED LINKS</span></span>

[<span data-ttu-id="c644d-133">Get-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="c644d-133">Get-AzStreamAnalyticsOutput</span></span>](./Get-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="c644d-134">New-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="c644d-134">New-AzStreamAnalyticsOutput</span></span>](./New-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="c644d-135">Test-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="c644d-135">Test-AzStreamAnalyticsOutput</span></span>](./Test-AzStreamAnalyticsOutput.md)



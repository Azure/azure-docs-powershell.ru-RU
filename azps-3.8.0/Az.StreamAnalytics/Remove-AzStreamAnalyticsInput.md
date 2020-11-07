---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 1449F64F-A8F9-4E8E-B62B-17DEF3A0FB30
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/remove-azstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsInput.md
ms.openlocfilehash: d3c5e578e6921297d7d5edc467e10b9a2b4e9e53
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912413"
---
# <span data-ttu-id="49688-101">Remove-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="49688-101">Remove-AzStreamAnalyticsInput</span></span>

## <span data-ttu-id="49688-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="49688-102">SYNOPSIS</span></span>
<span data-ttu-id="49688-103">Удаляет входные данные из задания Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="49688-103">Deletes an input from a Stream Analytics job.</span></span>

## <span data-ttu-id="49688-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="49688-104">SYNTAX</span></span>

```
Remove-AzStreamAnalyticsInput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49688-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="49688-105">DESCRIPTION</span></span>
<span data-ttu-id="49688-106">Командлет **Remove-AzStreamAnalyticsInput** асинхронно удаляет входные данные из задания Stream Analytics в Azure.</span><span class="sxs-lookup"><span data-stu-id="49688-106">The **Remove-AzStreamAnalyticsInput** cmdlet asynchronously deletes an input from a Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="49688-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="49688-107">EXAMPLES</span></span>

### <span data-ttu-id="49688-108">Пример 1: удаление входного потока из задания</span><span class="sxs-lookup"><span data-stu-id="49688-108">EXAMPLE 1: Remove an input stream from a job</span></span>
```
PS C:\>Remove-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EventStream"
```

<span data-ttu-id="49688-109">Эта команда удаляет входные EventStream из StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="49688-109">This command removes the input EventStream from StreamingJob.</span></span>

## <span data-ttu-id="49688-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="49688-110">PARAMETERS</span></span>

### <span data-ttu-id="49688-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49688-111">-DefaultProfile</span></span>
<span data-ttu-id="49688-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="49688-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="49688-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="49688-113">-JobName</span></span>
<span data-ttu-id="49688-114">Указывает имя задания Azure Stream Analytics, к которому относятся входные данные Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="49688-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="49688-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="49688-115">-Name</span></span>
<span data-ttu-id="49688-116">Указывает имя удаляемого ввода Stream Analytics для Azure.</span><span class="sxs-lookup"><span data-stu-id="49688-116">Specifies the name of the Azure Stream Analytics input to remove.</span></span>

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

### <span data-ttu-id="49688-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49688-117">-ResourceGroupName</span></span>
<span data-ttu-id="49688-118">Указывает имя группы ресурсов, к которой относятся входные данные Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="49688-118">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="49688-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="49688-119">-Confirm</span></span>
<span data-ttu-id="49688-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="49688-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49688-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49688-121">-WhatIf</span></span>
<span data-ttu-id="49688-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="49688-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49688-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="49688-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49688-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49688-124">CommonParameters</span></span>
<span data-ttu-id="49688-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="49688-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49688-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49688-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49688-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="49688-127">INPUTS</span></span>

### <span data-ttu-id="49688-128">System. String</span><span class="sxs-lookup"><span data-stu-id="49688-128">System.String</span></span>

## <span data-ttu-id="49688-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="49688-129">OUTPUTS</span></span>

### <span data-ttu-id="49688-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="49688-130">System.Boolean</span></span>

## <span data-ttu-id="49688-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="49688-131">NOTES</span></span>

## <span data-ttu-id="49688-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="49688-132">RELATED LINKS</span></span>

[<span data-ttu-id="49688-133">New-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="49688-133">New-AzStreamAnalyticsInput</span></span>](./New-AzStreamAnalyticsInput.md)

[<span data-ttu-id="49688-134">Get-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="49688-134">Get-AzStreamAnalyticsInput</span></span>](./Get-AzStreamAnalyticsInput.md)

[<span data-ttu-id="49688-135">Test-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="49688-135">Test-AzStreamAnalyticsInput</span></span>](./Test-AzStreamAnalyticsInput.md)



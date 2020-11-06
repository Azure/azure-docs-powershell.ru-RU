---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 2F3BDDFE-7585-4802-BFA5-D110F846A33E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsJob.md
ms.openlocfilehash: 9ba839bbfc6740d9d62c9a036d233a8b5a1ce0e9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568274"
---
# <span data-ttu-id="a17cd-101">Remove-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="a17cd-101">Remove-AzureRmStreamAnalyticsJob</span></span>

## <span data-ttu-id="a17cd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a17cd-102">SYNOPSIS</span></span>
<span data-ttu-id="a17cd-103">Удаляет задание Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="a17cd-103">Removes a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a17cd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a17cd-104">SYNTAX</span></span>

```
Remove-AzureRmStreamAnalyticsJob [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a17cd-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a17cd-105">DESCRIPTION</span></span>
<span data-ttu-id="a17cd-106">Командлет **Remove-AzureRmStreamAnalyticsJob** асинхронно удаляет определенное задание Stream Analytics в Azure.</span><span class="sxs-lookup"><span data-stu-id="a17cd-106">The **Remove-AzureRmStreamAnalyticsJob** cmdlet asynchronously deletes a specific Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="a17cd-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a17cd-107">EXAMPLES</span></span>

### <span data-ttu-id="a17cd-108">Пример 1: удаление задания</span><span class="sxs-lookup"><span data-stu-id="a17cd-108">EXAMPLE 1: Remove a job</span></span>
```
PS C:\>Remove-AzureRmStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="a17cd-109">Эта команда удаляет задание StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="a17cd-109">This command removes the job StreamingJob.</span></span>

## <span data-ttu-id="a17cd-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a17cd-110">PARAMETERS</span></span>

### <span data-ttu-id="a17cd-111">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a17cd-111">-Name</span></span>
<span data-ttu-id="a17cd-112">Указывает имя задания Azure Stream Analytics, которое нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="a17cd-112">Specifies the name of the Azure Stream Analytics job to remove.</span></span>

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

### <span data-ttu-id="a17cd-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a17cd-113">-ResourceGroupName</span></span>
<span data-ttu-id="a17cd-114">Указывает имя группы ресурсов, к которой относится задание Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="a17cd-114">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

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

### <span data-ttu-id="a17cd-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a17cd-115">-Confirm</span></span>
<span data-ttu-id="a17cd-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a17cd-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a17cd-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a17cd-117">-WhatIf</span></span>
<span data-ttu-id="a17cd-118">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a17cd-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a17cd-119">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a17cd-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a17cd-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a17cd-120">-DefaultProfile</span></span>
<span data-ttu-id="a17cd-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a17cd-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a17cd-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a17cd-122">CommonParameters</span></span>
<span data-ttu-id="a17cd-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a17cd-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a17cd-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a17cd-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a17cd-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a17cd-125">INPUTS</span></span>

## <span data-ttu-id="a17cd-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a17cd-126">OUTPUTS</span></span>

### <span data-ttu-id="a17cd-127">System. Object</span><span class="sxs-lookup"><span data-stu-id="a17cd-127">System.Object</span></span>

## <span data-ttu-id="a17cd-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="a17cd-128">NOTES</span></span>

## <span data-ttu-id="a17cd-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a17cd-129">RELATED LINKS</span></span>

[<span data-ttu-id="a17cd-130">Get-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="a17cd-130">Get-AzureRmStreamAnalyticsJob</span></span>](./Get-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="a17cd-131">New-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="a17cd-131">New-AzureRmStreamAnalyticsJob</span></span>](./New-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="a17cd-132">Start-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="a17cd-132">Start-AzureRmStreamAnalyticsJob</span></span>](./Start-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="a17cd-133">Остановить-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="a17cd-133">Stop-AzureRmStreamAnalyticsJob</span></span>](./Stop-AzureRmStreamAnalyticsJob.md)



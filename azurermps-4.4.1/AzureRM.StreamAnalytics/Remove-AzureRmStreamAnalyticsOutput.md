---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: EE41BE86-37D4-4A2B-9007-D019CD62BA9D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsOutput.md
ms.openlocfilehash: 9904699d95429e029f330e5c3ca3e5957eb4c35e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732183"
---
# <span data-ttu-id="82dac-101">Remove-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="82dac-101">Remove-AzureRmStreamAnalyticsOutput</span></span>

## <span data-ttu-id="82dac-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="82dac-102">SYNOPSIS</span></span>
<span data-ttu-id="82dac-103">Удаляет вывод из задания Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="82dac-103">Deletes an output from a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="82dac-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="82dac-104">SYNTAX</span></span>

```
Remove-AzureRmStreamAnalyticsOutput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="82dac-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="82dac-105">DESCRIPTION</span></span>
<span data-ttu-id="82dac-106">Командлет **Remove-AzureRmStreamAnalyticsOutput** асинхронно удаляет выходные данные из задания Stream Analytics в Azure.</span><span class="sxs-lookup"><span data-stu-id="82dac-106">The **Remove-AzureRmStreamAnalyticsOutput** cmdlet asynchronously deletes an output from a Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="82dac-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="82dac-107">EXAMPLES</span></span>

### <span data-ttu-id="82dac-108">Пример 1: удаление выхода из задания</span><span class="sxs-lookup"><span data-stu-id="82dac-108">EXAMPLE 1: Remove an output from a job</span></span>
```
PS C:\>Remove-AzureRmStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="82dac-109">Эта команда удаляет выходные данные в StreamingJob задания.</span><span class="sxs-lookup"><span data-stu-id="82dac-109">This command removes the output Output in the job StreamingJob.</span></span>

## <span data-ttu-id="82dac-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="82dac-110">PARAMETERS</span></span>

### <span data-ttu-id="82dac-111">-JobName</span><span class="sxs-lookup"><span data-stu-id="82dac-111">-JobName</span></span>
<span data-ttu-id="82dac-112">Указывает имя задания Azure Stream Analytics, к которому относятся выходные данные Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="82dac-112">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="82dac-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="82dac-113">-Name</span></span>
<span data-ttu-id="82dac-114">Указывает имя удаляемого выходных данных Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="82dac-114">Specifies the name of the Azure Stream Analytics output to remove.</span></span>

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

### <span data-ttu-id="82dac-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82dac-115">-ResourceGroupName</span></span>
<span data-ttu-id="82dac-116">Указывает имя группы ресурсов, к которой относятся выходные данные Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="82dac-116">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="82dac-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="82dac-117">-Confirm</span></span>
<span data-ttu-id="82dac-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="82dac-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82dac-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82dac-119">-WhatIf</span></span>
<span data-ttu-id="82dac-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="82dac-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82dac-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="82dac-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="82dac-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82dac-122">-DefaultProfile</span></span>
<span data-ttu-id="82dac-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="82dac-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="82dac-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82dac-124">CommonParameters</span></span>
<span data-ttu-id="82dac-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="82dac-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82dac-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82dac-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82dac-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="82dac-127">INPUTS</span></span>

## <span data-ttu-id="82dac-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="82dac-128">OUTPUTS</span></span>

### <span data-ttu-id="82dac-129">System. Object</span><span class="sxs-lookup"><span data-stu-id="82dac-129">System.Object</span></span>

## <span data-ttu-id="82dac-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="82dac-130">NOTES</span></span>

## <span data-ttu-id="82dac-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="82dac-131">RELATED LINKS</span></span>

[<span data-ttu-id="82dac-132">Get-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="82dac-132">Get-AzureRmStreamAnalyticsOutput</span></span>](./Get-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="82dac-133">New-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="82dac-133">New-AzureRmStreamAnalyticsOutput</span></span>](./New-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="82dac-134">Test-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="82dac-134">Test-AzureRmStreamAnalyticsOutput</span></span>](./Test-AzureRmStreamAnalyticsOutput.md)



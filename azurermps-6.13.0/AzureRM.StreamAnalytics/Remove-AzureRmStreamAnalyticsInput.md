---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 1449F64F-A8F9-4E8E-B62B-17DEF3A0FB30
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/remove-azurermstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsInput.md
ms.openlocfilehash: 8e80162d5efa6aa274617941df218812ae6901a5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565308"
---
# <span data-ttu-id="5e1ca-101">Remove-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="5e1ca-101">Remove-AzureRmStreamAnalyticsInput</span></span>

## <span data-ttu-id="5e1ca-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5e1ca-102">SYNOPSIS</span></span>
<span data-ttu-id="5e1ca-103">Удаляет входные данные из задания Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="5e1ca-103">Deletes an input from a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5e1ca-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5e1ca-104">SYNTAX</span></span>

```
Remove-AzureRmStreamAnalyticsInput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e1ca-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5e1ca-105">DESCRIPTION</span></span>
<span data-ttu-id="5e1ca-106">Командлет **Remove-AzureRmStreamAnalyticsInput** асинхронно удаляет входные данные из задания Stream Analytics в Azure.</span><span class="sxs-lookup"><span data-stu-id="5e1ca-106">The **Remove-AzureRmStreamAnalyticsInput** cmdlet asynchronously deletes an input from a Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="5e1ca-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5e1ca-107">EXAMPLES</span></span>

### <span data-ttu-id="5e1ca-108">Пример 1: удаление входного потока из задания</span><span class="sxs-lookup"><span data-stu-id="5e1ca-108">EXAMPLE 1: Remove an input stream from a job</span></span>
```
PS C:\>Remove-AzureRmStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EventStream"
```

<span data-ttu-id="5e1ca-109">Эта команда удаляет входные EventStream из StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="5e1ca-109">This command removes the input EventStream from StreamingJob.</span></span>

## <span data-ttu-id="5e1ca-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5e1ca-110">PARAMETERS</span></span>

### <span data-ttu-id="5e1ca-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e1ca-111">-DefaultProfile</span></span>
<span data-ttu-id="5e1ca-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5e1ca-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5e1ca-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="5e1ca-113">-JobName</span></span>
<span data-ttu-id="5e1ca-114">Указывает имя задания Azure Stream Analytics, к которому относятся входные данные Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="5e1ca-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="5e1ca-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5e1ca-115">-Name</span></span>
<span data-ttu-id="5e1ca-116">Указывает имя удаляемого ввода Stream Analytics для Azure.</span><span class="sxs-lookup"><span data-stu-id="5e1ca-116">Specifies the name of the Azure Stream Analytics input to remove.</span></span>

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

### <span data-ttu-id="5e1ca-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e1ca-117">-ResourceGroupName</span></span>
<span data-ttu-id="5e1ca-118">Указывает имя группы ресурсов, к которой относятся входные данные Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="5e1ca-118">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="5e1ca-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5e1ca-119">-Confirm</span></span>
<span data-ttu-id="5e1ca-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5e1ca-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e1ca-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e1ca-121">-WhatIf</span></span>
<span data-ttu-id="5e1ca-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5e1ca-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e1ca-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5e1ca-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e1ca-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e1ca-124">CommonParameters</span></span>
<span data-ttu-id="5e1ca-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5e1ca-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e1ca-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e1ca-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e1ca-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5e1ca-127">INPUTS</span></span>

### <span data-ttu-id="5e1ca-128">System. String</span><span class="sxs-lookup"><span data-stu-id="5e1ca-128">System.String</span></span>

## <span data-ttu-id="5e1ca-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5e1ca-129">OUTPUTS</span></span>

### <span data-ttu-id="5e1ca-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5e1ca-130">System.Boolean</span></span>

## <span data-ttu-id="5e1ca-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="5e1ca-131">NOTES</span></span>

## <span data-ttu-id="5e1ca-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5e1ca-132">RELATED LINKS</span></span>

[<span data-ttu-id="5e1ca-133">New-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="5e1ca-133">New-AzureRmStreamAnalyticsInput</span></span>](./New-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="5e1ca-134">Get-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="5e1ca-134">Get-AzureRmStreamAnalyticsInput</span></span>](./Get-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="5e1ca-135">Test-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="5e1ca-135">Test-AzureRmStreamAnalyticsInput</span></span>](./Test-AzureRmStreamAnalyticsInput.md)



---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM
ms.assetid: 1449F64F-A8F9-4E8E-B62B-17DEF3A0FB30
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/remove-azurermstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsInput.md
ms.openlocfilehash: 9e228c2520402f1b8395c6ca4d90909905f6cb0f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732135"
---
# <span data-ttu-id="0940c-101">Remove-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="0940c-101">Remove-AzureRmStreamAnalyticsInput</span></span>

## <span data-ttu-id="0940c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0940c-102">SYNOPSIS</span></span>
<span data-ttu-id="0940c-103">Удаляет входные данные из задания Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="0940c-103">Deletes an input from a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0940c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0940c-104">SYNTAX</span></span>

```
Remove-AzureRmStreamAnalyticsInput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0940c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0940c-105">DESCRIPTION</span></span>
<span data-ttu-id="0940c-106">Командлет **Remove-AzureRmStreamAnalyticsInput** асинхронно удаляет входные данные из задания Stream Analytics в Azure.</span><span class="sxs-lookup"><span data-stu-id="0940c-106">The **Remove-AzureRmStreamAnalyticsInput** cmdlet asynchronously deletes an input from a Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="0940c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0940c-107">EXAMPLES</span></span>

### <span data-ttu-id="0940c-108">Пример 1: удаление входного потока из задания</span><span class="sxs-lookup"><span data-stu-id="0940c-108">EXAMPLE 1: Remove an input stream from a job</span></span>
```
PS C:\>Remove-AzureRmStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EventStream"
```

<span data-ttu-id="0940c-109">Эта команда удаляет входные EventStream из StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="0940c-109">This command removes the input EventStream from StreamingJob.</span></span>

## <span data-ttu-id="0940c-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0940c-110">PARAMETERS</span></span>

### <span data-ttu-id="0940c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0940c-111">-DefaultProfile</span></span>
<span data-ttu-id="0940c-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0940c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0940c-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="0940c-113">-JobName</span></span>
<span data-ttu-id="0940c-114">Указывает имя задания Azure Stream Analytics, к которому относятся входные данные Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="0940c-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0940c-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0940c-115">-Name</span></span>
<span data-ttu-id="0940c-116">Указывает имя удаляемого ввода Stream Analytics для Azure.</span><span class="sxs-lookup"><span data-stu-id="0940c-116">Specifies the name of the Azure Stream Analytics input to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0940c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0940c-117">-ResourceGroupName</span></span>
<span data-ttu-id="0940c-118">Указывает имя группы ресурсов, к которой относятся входные данные Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="0940c-118">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0940c-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0940c-119">-Confirm</span></span>
<span data-ttu-id="0940c-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0940c-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0940c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0940c-121">-WhatIf</span></span>
<span data-ttu-id="0940c-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0940c-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0940c-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0940c-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0940c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0940c-124">CommonParameters</span></span>
<span data-ttu-id="0940c-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0940c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0940c-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0940c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0940c-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0940c-127">INPUTS</span></span>

### <span data-ttu-id="0940c-128">Ничего</span><span class="sxs-lookup"><span data-stu-id="0940c-128">None</span></span>
<span data-ttu-id="0940c-129">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="0940c-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0940c-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0940c-130">OUTPUTS</span></span>

### <span data-ttu-id="0940c-131">System. Object</span><span class="sxs-lookup"><span data-stu-id="0940c-131">System.Object</span></span>

## <span data-ttu-id="0940c-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="0940c-132">NOTES</span></span>

## <span data-ttu-id="0940c-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0940c-133">RELATED LINKS</span></span>

[<span data-ttu-id="0940c-134">New-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="0940c-134">New-AzureRmStreamAnalyticsInput</span></span>](./New-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="0940c-135">Get-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="0940c-135">Get-AzureRmStreamAnalyticsInput</span></span>](./Get-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="0940c-136">Test-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="0940c-136">Test-AzureRmStreamAnalyticsInput</span></span>](./Test-AzureRmStreamAnalyticsInput.md)



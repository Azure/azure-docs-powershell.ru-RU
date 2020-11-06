---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 678e08df94d7ea828b04d55892cb66e1c0a62349
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93555640"
---
# <span data-ttu-id="fd612-101">Enable-AzureRmDataCollection</span><span class="sxs-lookup"><span data-stu-id="fd612-101">Enable-AzureRmDataCollection</span></span>

## <span data-ttu-id="fd612-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fd612-102">SYNOPSIS</span></span>
<span data-ttu-id="fd612-103">Позволяет Azure PowerShell собирать данные, чтобы улучшить взаимодействие с пользователем с помощью командлетов AzurePowerShell.</span><span class="sxs-lookup"><span data-stu-id="fd612-103">Enables Azure PowerShell to collect data to improve the user experience with AzurePowerShell cmdlets.</span></span>
<span data-ttu-id="fd612-104">Выполнение этого командлета наследуется в сборе данных для текущего пользователя на текущем компьютере.</span><span class="sxs-lookup"><span data-stu-id="fd612-104">Executing this cmdlet opts in to data collection for the current user on the current machine.</span></span>
<span data-ttu-id="fd612-105">Никакие данные не собираются, пока не будет явно задействовано.</span><span class="sxs-lookup"><span data-stu-id="fd612-105">No data is collected unless you explicitly opt in.</span></span>

## <span data-ttu-id="fd612-106">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fd612-106">SYNTAX</span></span>

```
Enable-AzureRmDataCollection [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd612-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fd612-107">DESCRIPTION</span></span>
<span data-ttu-id="fd612-108">Вы можете улучшить взаимодействие с использованием Microsoft Cloud и Azure PowerShell, перейдя в коллекцию данных.</span><span class="sxs-lookup"><span data-stu-id="fd612-108">You can improve the experience of using the Microsoft Cloud and Azure PowerShell by opting in to data collection.</span></span>
<span data-ttu-id="fd612-109">Azure PowerShell не собирает данные без согласия пользователя, поэтому вы должны явно присоединиться, выполнив Enable-AzureRmDataCollection или ответив на "Да", когда Azure PowerShell попросит вас собрать данные при первом запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="fd612-109">Azure PowerShell does not collect data without your consent - you must explicitly opt in by executing Enable-AzureRmDataCollection, or by answering yes when Azure PowerShell prompts you about collecting data the first time you execute a cmdlet.</span></span>
<span data-ttu-id="fd612-110">Корпорация Майкрософт собирает собранные данные для выявления закономерностей использования, для выявления распространенных проблем и для повышения эффективности использования Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="fd612-110">Microsoft aggregates collected data to identify patterns of usage, to identify common issues and to improve the experience of using Azure PowerShell.</span></span>
<span data-ttu-id="fd612-111">Microsoft Azure PowerShell не может собирать конфиденциальные данные и любые сведения, которые можно идентифицировать.</span><span class="sxs-lookup"><span data-stu-id="fd612-111">Microsoft Azure PowerShell does not collect any private data, or any personally identifiable information.</span></span>

<span data-ttu-id="fd612-112">Запустите командлет Enable-AzureRMDataCollection, чтобы включить сбор данных для текущего пользователя на этом компьютере.</span><span class="sxs-lookup"><span data-stu-id="fd612-112">Run the Enable-AzureRMDataCollection cmdlet to enable data collection for the current user on the current machine.</span></span>
<span data-ttu-id="fd612-113">Это предотвратит вывод запроса о сборе данных текущим пользователем при первом выполнении командлетов.</span><span class="sxs-lookup"><span data-stu-id="fd612-113">This will prevent the current user from being prompted about data collection the first time cmdlets are executed.</span></span>

<span data-ttu-id="fd612-114">Чтобы отключить сбор данных для текущего пользователя, выполните командлет Disable-AzureRmDataCollection.</span><span class="sxs-lookup"><span data-stu-id="fd612-114">To disable data collection for the current user, run the Disable-AzureRmDataCollection cmdlet.</span></span>

## <span data-ttu-id="fd612-115">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fd612-115">EXAMPLES</span></span>

### <span data-ttu-id="fd612-116">Пример 1: Включение сбора данных для текущего пользователя</span><span class="sxs-lookup"><span data-stu-id="fd612-116">Example 1: Enabling data collection for the current user</span></span>
```
PS C:\> Enable-AzureRmDataCollection
```

<span data-ttu-id="fd612-117">В этом примере показано, как включить сбор данных для текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="fd612-117">This example shows how to enable data collection for the current user.</span></span>

## <span data-ttu-id="fd612-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fd612-118">PARAMETERS</span></span>

### <span data-ttu-id="fd612-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fd612-119">-Confirm</span></span>
<span data-ttu-id="fd612-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="fd612-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd612-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd612-121">-WhatIf</span></span>
<span data-ttu-id="fd612-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="fd612-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fd612-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="fd612-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd612-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd612-124">CommonParameters</span></span>
<span data-ttu-id="fd612-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fd612-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd612-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd612-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd612-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fd612-127">INPUTS</span></span>

## <span data-ttu-id="fd612-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fd612-128">OUTPUTS</span></span>

### <span data-ttu-id="fd612-129">Ничего</span><span class="sxs-lookup"><span data-stu-id="fd612-129">None</span></span>

## <span data-ttu-id="fd612-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="fd612-130">NOTES</span></span>

## <span data-ttu-id="fd612-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fd612-131">RELATED LINKS</span></span>

[<span data-ttu-id="fd612-132">Disable-AzureRmDataCollection</span><span class="sxs-lookup"><span data-stu-id="fd612-132">Disable-AzureRmDataCollection</span></span>]()


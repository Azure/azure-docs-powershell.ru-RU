---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: e233c523e5fd9372b1e7dd86b5b5e73eb3f7091e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93555644"
---
# <span data-ttu-id="48734-101">Disable-AzureRmDataCollection</span><span class="sxs-lookup"><span data-stu-id="48734-101">Disable-AzureRmDataCollection</span></span>

## <span data-ttu-id="48734-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="48734-102">SYNOPSIS</span></span>
<span data-ttu-id="48734-103">Изменяют сбор данных, чтобы улучшить командлеты AzurePowerShell.</span><span class="sxs-lookup"><span data-stu-id="48734-103">Opts out of collecting data to improve the AzurePowerShell cmdlets.</span></span> <span data-ttu-id="48734-104">Данные не собираются, пока не будет явно задействовано.</span><span class="sxs-lookup"><span data-stu-id="48734-104">Data is not collected unless you explicitly opt in.</span></span>

## <span data-ttu-id="48734-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="48734-105">SYNTAX</span></span>

```
Disable-AzureRmDataCollection [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48734-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="48734-106">DESCRIPTION</span></span>
<span data-ttu-id="48734-107">Вы можете улучшить взаимодействие с использованием Microsoft Cloud и Azure PowerShell, перейдя в коллекцию данных.</span><span class="sxs-lookup"><span data-stu-id="48734-107">You can improve the experience of using the Microsoft Cloud and Azure PowerShell by opting in to data collection.</span></span>
<span data-ttu-id="48734-108">Azure PowerShell не собирает данные без согласия пользователя, поэтому вы должны явно присоединиться, выполнив Enable-AzureRmDataCollection или ответив на "Да", когда Azure PowerShell попросит вас собрать данные при первом запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="48734-108">Azure PowerShell does not collect data without your consent - you must explicitly opt in by executing Enable-AzureRmDataCollection, or by answering yes when Azure PowerShell prompts you about collecting data the first time you execute a cmdlet.</span></span>
<span data-ttu-id="48734-109">Корпорация Майкрософт собирает собранные данные для выявления закономерностей использования, для выявления распространенных проблем и для повышения эффективности использования Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="48734-109">Microsoft aggregates collected data to identify patterns of usage, to identify common issues and to improve the experience of using Azure PowerShell.</span></span>
<span data-ttu-id="48734-110">Microsoft Azure PowerShell не может собирать конфиденциальные данные и любые сведения, которые можно идентифицировать.</span><span class="sxs-lookup"><span data-stu-id="48734-110">Microsoft Azure PowerShell does not collect any private data, or any personally identifiable information.</span></span>

<span data-ttu-id="48734-111">Запустите командлет Disable-AzureRMDataCollection, чтобы отключить сбор данных для текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="48734-111">Run the Disable-AzureRMDataCollection cmdlet to disable data collection for the current user.</span></span>
<span data-ttu-id="48734-112">Это предотвратит вывод запроса о сборе данных текущим пользователем при первом выполнении командлетов.</span><span class="sxs-lookup"><span data-stu-id="48734-112">This will prevent the current user from being prompted about data collection the first time cmdlets are executed.</span></span>

<span data-ttu-id="48734-113">Чтобы включить сбор данных для текущего пользователя, выполните командлет Enable-AzureRmDataCollection.</span><span class="sxs-lookup"><span data-stu-id="48734-113">To enable data collection for the current user, run the Enable-AzureRmDataCollection cmdlet.</span></span>

## <span data-ttu-id="48734-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="48734-114">EXAMPLES</span></span>

### <span data-ttu-id="48734-115">Пример 1: Отключение сбора данных для текущего пользователя</span><span class="sxs-lookup"><span data-stu-id="48734-115">Example 1: Disabling data collection for the current user</span></span>
```
PS C:\> Disable-AzureRmDataCollection
```

<span data-ttu-id="48734-116">В этом примере показано, как отключить сбор данных для текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="48734-116">This example shows how to disable data collection for the current user.</span></span> 

## <span data-ttu-id="48734-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="48734-117">PARAMETERS</span></span>

### <span data-ttu-id="48734-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="48734-118">-Confirm</span></span>
<span data-ttu-id="48734-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="48734-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48734-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48734-120">-WhatIf</span></span>
<span data-ttu-id="48734-121">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="48734-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="48734-122">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="48734-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48734-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48734-123">CommonParameters</span></span>
<span data-ttu-id="48734-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="48734-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48734-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48734-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48734-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="48734-126">INPUTS</span></span>

## <span data-ttu-id="48734-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="48734-127">OUTPUTS</span></span>

### <span data-ttu-id="48734-128">Ничего</span><span class="sxs-lookup"><span data-stu-id="48734-128">None</span></span>

## <span data-ttu-id="48734-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="48734-129">NOTES</span></span>

## <span data-ttu-id="48734-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="48734-130">RELATED LINKS</span></span>

[<span data-ttu-id="48734-131">Enable-AzureRmDataCollection</span><span class="sxs-lookup"><span data-stu-id="48734-131">Enable-AzureRmDataCollection</span></span>]()


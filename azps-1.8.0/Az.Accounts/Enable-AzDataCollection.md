---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/enable-azdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzDataCollection.md
ms.openlocfilehash: 1a68b5ca391e6c09673f07f0469035e0f96c1562
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720275"
---
# <span data-ttu-id="ddbee-101">Enable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="ddbee-101">Enable-AzDataCollection</span></span>

## <span data-ttu-id="ddbee-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ddbee-102">SYNOPSIS</span></span>
<span data-ttu-id="ddbee-103">Позволяет Azure PowerShell собирать данные, чтобы улучшить взаимодействие с пользователем с помощью командлетов AzurePowerShell.</span><span class="sxs-lookup"><span data-stu-id="ddbee-103">Enables Azure PowerShell to collect data to improve the user experience with AzurePowerShell cmdlets.</span></span>
<span data-ttu-id="ddbee-104">Выполнение этого командлета наследуется в сборе данных для текущего пользователя на текущем компьютере.</span><span class="sxs-lookup"><span data-stu-id="ddbee-104">Executing this cmdlet opts in to data collection for the current user on the current machine.</span></span>
<span data-ttu-id="ddbee-105">Никакие данные не собираются, пока не будет явно задействовано.</span><span class="sxs-lookup"><span data-stu-id="ddbee-105">No data is collected unless you explicitly opt in.</span></span>

## <span data-ttu-id="ddbee-106">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ddbee-106">SYNTAX</span></span>

```
Enable-AzDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ddbee-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ddbee-107">DESCRIPTION</span></span>
<span data-ttu-id="ddbee-108">Вы можете улучшить взаимодействие с использованием Microsoft Cloud и Azure PowerShell, перейдя в коллекцию данных.</span><span class="sxs-lookup"><span data-stu-id="ddbee-108">You can improve the experience of using the Microsoft Cloud and Azure PowerShell by opting in to data collection.</span></span>
<span data-ttu-id="ddbee-109">Azure PowerShell не собирает данные без согласия пользователя, поэтому вы должны явно присоединиться, выполнив Enable-AzDataCollection или ответив на "Да", когда Azure PowerShell попросит вас собрать данные при первом запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ddbee-109">Azure PowerShell does not collect data without your consent - you must explicitly opt in by executing Enable-AzDataCollection, or by answering yes when Azure PowerShell prompts you about collecting data the first time you execute a cmdlet.</span></span>
<span data-ttu-id="ddbee-110">Корпорация Майкрософт собирает собранные данные для выявления закономерностей использования, для выявления распространенных проблем и для повышения эффективности использования Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ddbee-110">Microsoft aggregates collected data to identify patterns of usage, to identify common issues and to improve the experience of using Azure PowerShell.</span></span>
<span data-ttu-id="ddbee-111">Microsoft Azure PowerShell не может собирать конфиденциальные данные и любые сведения, которые можно идентифицировать.</span><span class="sxs-lookup"><span data-stu-id="ddbee-111">Microsoft Azure PowerShell does not collect any private data, or any personally identifiable information.</span></span>
<span data-ttu-id="ddbee-112">Запустите командлет Enable-AzDataCollection, чтобы включить сбор данных для текущего пользователя на этом компьютере.</span><span class="sxs-lookup"><span data-stu-id="ddbee-112">Run the Enable-AzDataCollection cmdlet to enable data collection for the current user on the current machine.</span></span>
<span data-ttu-id="ddbee-113">Это предотвратит вывод запроса о сборе данных текущим пользователем при первом выполнении командлетов.</span><span class="sxs-lookup"><span data-stu-id="ddbee-113">This will prevent the current user from being prompted about data collection the first time cmdlets are executed.</span></span>
<span data-ttu-id="ddbee-114">Чтобы отключить сбор данных для текущего пользователя, выполните командлет Disable-AzDataCollection.</span><span class="sxs-lookup"><span data-stu-id="ddbee-114">To disable data collection for the current user, run the Disable-AzDataCollection cmdlet.</span></span>

## <span data-ttu-id="ddbee-115">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ddbee-115">EXAMPLES</span></span>

### <span data-ttu-id="ddbee-116">Пример 1: Включение сбора данных для текущего пользователя</span><span class="sxs-lookup"><span data-stu-id="ddbee-116">Example 1: Enabling data collection for the current user</span></span>
```
PS C:\> Enable-AzDataCollection
```

<span data-ttu-id="ddbee-117">В этом примере показано, как включить сбор данных для текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="ddbee-117">This example shows how to enable data collection for the current user.</span></span>

## <span data-ttu-id="ddbee-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ddbee-118">PARAMETERS</span></span>

### <span data-ttu-id="ddbee-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddbee-119">-DefaultProfile</span></span>
<span data-ttu-id="ddbee-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ddbee-120">The credentials, account, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ddbee-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ddbee-121">-Confirm</span></span>
<span data-ttu-id="ddbee-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ddbee-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ddbee-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ddbee-123">-WhatIf</span></span>
<span data-ttu-id="ddbee-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ddbee-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ddbee-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ddbee-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ddbee-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddbee-126">CommonParameters</span></span>
<span data-ttu-id="ddbee-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ddbee-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddbee-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ddbee-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddbee-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ddbee-129">INPUTS</span></span>

### <span data-ttu-id="ddbee-130">Ничего</span><span class="sxs-lookup"><span data-stu-id="ddbee-130">None</span></span>

## <span data-ttu-id="ddbee-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ddbee-131">OUTPUTS</span></span>

### <span data-ttu-id="ddbee-132">System. void</span><span class="sxs-lookup"><span data-stu-id="ddbee-132">System.Void</span></span>

## <span data-ttu-id="ddbee-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="ddbee-133">NOTES</span></span>

## <span data-ttu-id="ddbee-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ddbee-134">RELATED LINKS</span></span>

[<span data-ttu-id="ddbee-135">Disable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="ddbee-135">Disable-AzDataCollection</span></span>](./Disable-AzDataCollection.md)


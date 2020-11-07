---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/disable-azdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Disable-AzDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Disable-AzDataCollection.md
ms.openlocfilehash: 8c168027573c0160519c8600e3e55cac534edeca
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93909441"
---
# <span data-ttu-id="423da-101">Disable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="423da-101">Disable-AzDataCollection</span></span>

## <span data-ttu-id="423da-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="423da-102">SYNOPSIS</span></span>
<span data-ttu-id="423da-103">Изменяют сбор данных, чтобы улучшить командлеты AzurePowerShell.</span><span class="sxs-lookup"><span data-stu-id="423da-103">Opts out of collecting data to improve the AzurePowerShell cmdlets.</span></span> <span data-ttu-id="423da-104">Данные не собираются, пока не будет явно задействовано.</span><span class="sxs-lookup"><span data-stu-id="423da-104">Data is not collected unless you explicitly opt in.</span></span>

## <span data-ttu-id="423da-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="423da-105">SYNTAX</span></span>

```
Disable-AzDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="423da-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="423da-106">DESCRIPTION</span></span>
<span data-ttu-id="423da-107">Вы можете улучшить взаимодействие с использованием Microsoft Cloud и Azure PowerShell, перейдя в коллекцию данных.</span><span class="sxs-lookup"><span data-stu-id="423da-107">You can improve the experience of using the Microsoft Cloud and Azure PowerShell by opting in to data collection.</span></span>
<span data-ttu-id="423da-108">Azure PowerShell не собирает данные без согласия пользователя, поэтому вы должны явно присоединиться, выполнив Enable-AzDataCollection или ответив на "Да", когда Azure PowerShell попросит вас собрать данные при первом запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="423da-108">Azure PowerShell does not collect data without your consent - you must explicitly opt in by executing Enable-AzDataCollection, or by answering yes when Azure PowerShell prompts you about collecting data the first time you execute a cmdlet.</span></span>
<span data-ttu-id="423da-109">Корпорация Майкрософт собирает собранные данные для выявления закономерностей использования, для выявления распространенных проблем и для повышения эффективности использования Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="423da-109">Microsoft aggregates collected data to identify patterns of usage, to identify common issues and to improve the experience of using Azure PowerShell.</span></span>
<span data-ttu-id="423da-110">Microsoft Azure PowerShell не может собирать конфиденциальные данные и любые сведения, которые можно идентифицировать.</span><span class="sxs-lookup"><span data-stu-id="423da-110">Microsoft Azure PowerShell does not collect any private data, or any personally identifiable information.</span></span>
<span data-ttu-id="423da-111">Запустите командлет Disable-AzDataCollection, чтобы отключить сбор данных для текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="423da-111">Run the Disable-AzDataCollection cmdlet to disable data collection for the current user.</span></span>
<span data-ttu-id="423da-112">Это предотвратит вывод запроса о сборе данных текущим пользователем при первом выполнении командлетов.</span><span class="sxs-lookup"><span data-stu-id="423da-112">This will prevent the current user from being prompted about data collection the first time cmdlets are executed.</span></span>
<span data-ttu-id="423da-113">Чтобы включить сбор данных для текущего пользователя, выполните командлет Enable-AzDataCollection.</span><span class="sxs-lookup"><span data-stu-id="423da-113">To enable data collection for the current user, run the Enable-AzDataCollection cmdlet.</span></span>

## <span data-ttu-id="423da-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="423da-114">EXAMPLES</span></span>

### <span data-ttu-id="423da-115">Пример 1: Отключение сбора данных для текущего пользователя</span><span class="sxs-lookup"><span data-stu-id="423da-115">Example 1: Disabling data collection for the current user</span></span>
```
PS C:\> Disable-AzDataCollection
```

<span data-ttu-id="423da-116">В этом примере показано, как отключить сбор данных для текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="423da-116">This example shows how to disable data collection for the current user.</span></span> 

## <span data-ttu-id="423da-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="423da-117">PARAMETERS</span></span>

### <span data-ttu-id="423da-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="423da-118">-DefaultProfile</span></span>
<span data-ttu-id="423da-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="423da-119">The credentials, account, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="423da-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="423da-120">-Confirm</span></span>
<span data-ttu-id="423da-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="423da-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="423da-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="423da-122">-WhatIf</span></span>
<span data-ttu-id="423da-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="423da-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="423da-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="423da-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="423da-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="423da-125">CommonParameters</span></span>
<span data-ttu-id="423da-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="423da-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="423da-127">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="423da-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="423da-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="423da-128">INPUTS</span></span>

### <span data-ttu-id="423da-129">Ничего</span><span class="sxs-lookup"><span data-stu-id="423da-129">None</span></span>

## <span data-ttu-id="423da-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="423da-130">OUTPUTS</span></span>

### <span data-ttu-id="423da-131">System. void</span><span class="sxs-lookup"><span data-stu-id="423da-131">System.Void</span></span>

## <span data-ttu-id="423da-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="423da-132">NOTES</span></span>

## <span data-ttu-id="423da-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="423da-133">RELATED LINKS</span></span>

[<span data-ttu-id="423da-134">Enable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="423da-134">Enable-AzDataCollection</span></span>](./Enable-AzDataCollection.md)


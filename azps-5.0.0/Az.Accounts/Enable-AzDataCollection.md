---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/enable-azdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzDataCollection.md
ms.openlocfilehash: a8087f41c33dc3bb066609393a87986d5016d1ae
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246302"
---
# <span data-ttu-id="4993c-101">Enable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="4993c-101">Enable-AzDataCollection</span></span>

## <span data-ttu-id="4993c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4993c-102">SYNOPSIS</span></span>
<span data-ttu-id="4993c-103">Позволяет Azure PowerShell собирать данные, чтобы улучшить взаимодействие с пользователем с помощью командлетов PowerShell для Azure.</span><span class="sxs-lookup"><span data-stu-id="4993c-103">Enables Azure PowerShell to collect data to improve the user experience with the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="4993c-104">Выполнение этого командлета наследуется в сборе данных для текущего пользователя на текущем компьютере.</span><span class="sxs-lookup"><span data-stu-id="4993c-104">Executing this cmdlet opts in to data collection for the current user on the current machine.</span></span> <span data-ttu-id="4993c-105">Данные собираются по умолчанию, если только вы не выберете явное согласие.</span><span class="sxs-lookup"><span data-stu-id="4993c-105">Data is collected by default unless you explicitly opt out.</span></span>

## <span data-ttu-id="4993c-106">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4993c-106">SYNTAX</span></span>

```
Enable-AzDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4993c-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4993c-107">DESCRIPTION</span></span>

<span data-ttu-id="4993c-108">Этот `Enable-AzDataCollection` командлет используется для выбора коллекции данных.</span><span class="sxs-lookup"><span data-stu-id="4993c-108">The `Enable-AzDataCollection` cmdlet is used to opt in to data collection.</span></span> <span data-ttu-id="4993c-109">Azure PowerShell автоматически собирает данные телеметрии по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="4993c-109">Azure PowerShell automatically collects telemetry data by default.</span></span> <span data-ttu-id="4993c-110">Корпорация Майкрософт собирает собранные данные для выявления закономерностей использования, для выявления распространенных проблем и для улучшения работы Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="4993c-110">Microsoft aggregates collected data to identify patterns of usage, to identify common issues, and to improve the experience of Azure PowerShell.</span></span>
<span data-ttu-id="4993c-111">Microsoft Azure PowerShell не собирают конфиденциальные или личные данные.</span><span class="sxs-lookup"><span data-stu-id="4993c-111">Microsoft Azure PowerShell doesn't collect any private or personal data.</span></span> <span data-ttu-id="4993c-112">Чтобы отключить сбор данных, необходимо явным образом отказаться от выполнения `Disable-AzDataCollection` .</span><span class="sxs-lookup"><span data-stu-id="4993c-112">To disable data collection, you must explicitly opt out by executing `Disable-AzDataCollection`.</span></span>

## <span data-ttu-id="4993c-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4993c-113">EXAMPLES</span></span>

### <span data-ttu-id="4993c-114">Пример 1: Включение сбора данных для текущего пользователя</span><span class="sxs-lookup"><span data-stu-id="4993c-114">Example 1: Enabling data collection for the current user</span></span>

<span data-ttu-id="4993c-115">В следующем примере показано, как включить сбор данных для текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="4993c-115">The following example shows how to enable data collection for the current user.</span></span>

```powershell
Enable-AzDataCollection
```

## <span data-ttu-id="4993c-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4993c-116">PARAMETERS</span></span>

### <span data-ttu-id="4993c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4993c-117">-DefaultProfile</span></span>

<span data-ttu-id="4993c-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4993c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4993c-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4993c-119">-Confirm</span></span>

<span data-ttu-id="4993c-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4993c-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4993c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4993c-121">-WhatIf</span></span>

<span data-ttu-id="4993c-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4993c-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4993c-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4993c-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4993c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4993c-124">CommonParameters</span></span>

<span data-ttu-id="4993c-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4993c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4993c-126">Дополнительные сведения можно найти в разделе [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).</span><span class="sxs-lookup"><span data-stu-id="4993c-126">For more information, see [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).</span></span>

## <span data-ttu-id="4993c-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4993c-127">INPUTS</span></span>

### <span data-ttu-id="4993c-128">Ничего</span><span class="sxs-lookup"><span data-stu-id="4993c-128">None</span></span>

## <span data-ttu-id="4993c-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4993c-129">OUTPUTS</span></span>

### <span data-ttu-id="4993c-130">System. void</span><span class="sxs-lookup"><span data-stu-id="4993c-130">System.Void</span></span>

## <span data-ttu-id="4993c-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="4993c-131">NOTES</span></span>

## <span data-ttu-id="4993c-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4993c-132">RELATED LINKS</span></span>

[<span data-ttu-id="4993c-133">Disable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="4993c-133">Disable-AzDataCollection</span></span>](./Disable-AzDataCollection.md)
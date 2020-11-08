---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/disable-azdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzDataCollection.md
ms.openlocfilehash: 27b3565191d7de110a5ba3a1e37d204fe3301cbf
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/30/2020
ms.locfileid: "94075080"
---
# <span data-ttu-id="6e9dd-101">Disable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="6e9dd-101">Disable-AzDataCollection</span></span>

## <span data-ttu-id="6e9dd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6e9dd-102">SYNOPSIS</span></span>
<span data-ttu-id="6e9dd-103">Изменяют сбор данных для улучшения командлетов PowerShell для Azure.</span><span class="sxs-lookup"><span data-stu-id="6e9dd-103">Opts out of collecting data to improve the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="6e9dd-104">Данные собираются по умолчанию, если только вы не выберете явное согласие.</span><span class="sxs-lookup"><span data-stu-id="6e9dd-104">Data is collected by default unless you explicitly opt out.</span></span>

## <span data-ttu-id="6e9dd-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6e9dd-105">SYNTAX</span></span>

```
Disable-AzDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6e9dd-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6e9dd-106">DESCRIPTION</span></span>

<span data-ttu-id="6e9dd-107">Этот `Disable-AzDataCollection` командлет используется, чтобы отказаться от сбора данных.</span><span class="sxs-lookup"><span data-stu-id="6e9dd-107">The `Disable-AzDataCollection` cmdlet is used to opt out of data collection.</span></span> <span data-ttu-id="6e9dd-108">Azure PowerShell автоматически собирает данные телеметрии по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6e9dd-108">Azure PowerShell automatically collects telemetry data by default.</span></span> <span data-ttu-id="6e9dd-109">Чтобы отключить сбор данных, необходимо явно отказаться от него. Корпорация Майкрософт собирает собранные данные для выявления закономерностей использования, для выявления распространенных проблем и для улучшения работы Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="6e9dd-109">To disable data collection, you must explicitly opt-out. Microsoft aggregates collected data to identify patterns of usage, to identify common issues, and to improve the experience of Azure PowerShell.</span></span> <span data-ttu-id="6e9dd-110">Microsoft Azure PowerShell не собирают конфиденциальные или личные данные.</span><span class="sxs-lookup"><span data-stu-id="6e9dd-110">Microsoft Azure PowerShell doesn't collect any private or personal data.</span></span> <span data-ttu-id="6e9dd-111">Если вы ранее выделились, выполните `Enable-AzDataCollection` командлет, чтобы повторно включить сбор данных для текущего пользователя на текущем компьютере.</span><span class="sxs-lookup"><span data-stu-id="6e9dd-111">If you've previously opted out, run the `Enable-AzDataCollection` cmdlet to re-enable data collection for the current user on the current machine.</span></span>

## <span data-ttu-id="6e9dd-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6e9dd-112">EXAMPLES</span></span>

### <span data-ttu-id="6e9dd-113">Пример 1: Отключение сбора данных для текущего пользователя</span><span class="sxs-lookup"><span data-stu-id="6e9dd-113">Example 1: Disabling data collection for the current user</span></span>

<span data-ttu-id="6e9dd-114">В следующем примере показано, как отключить сбор данных для текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="6e9dd-114">The following example shows how to disable data collection for the current user.</span></span>

```powershell
Disable-AzDataCollection
```

## <span data-ttu-id="6e9dd-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6e9dd-115">PARAMETERS</span></span>

### <span data-ttu-id="6e9dd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e9dd-116">-DefaultProfile</span></span>

<span data-ttu-id="6e9dd-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6e9dd-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e9dd-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6e9dd-118">-Confirm</span></span>

<span data-ttu-id="6e9dd-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6e9dd-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e9dd-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e9dd-120">-WhatIf</span></span>

<span data-ttu-id="6e9dd-121">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6e9dd-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6e9dd-122">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6e9dd-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e9dd-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e9dd-123">CommonParameters</span></span>

<span data-ttu-id="6e9dd-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6e9dd-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e9dd-125">Дополнительные сведения можно найти в разделе [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).</span><span class="sxs-lookup"><span data-stu-id="6e9dd-125">For more information, see [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).</span></span>

## <span data-ttu-id="6e9dd-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6e9dd-126">INPUTS</span></span>

### <span data-ttu-id="6e9dd-127">Ничего</span><span class="sxs-lookup"><span data-stu-id="6e9dd-127">None</span></span>

## <span data-ttu-id="6e9dd-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6e9dd-128">OUTPUTS</span></span>

### <span data-ttu-id="6e9dd-129">System. void</span><span class="sxs-lookup"><span data-stu-id="6e9dd-129">System.Void</span></span>

## <span data-ttu-id="6e9dd-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="6e9dd-130">NOTES</span></span>

## <span data-ttu-id="6e9dd-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6e9dd-131">RELATED LINKS</span></span>

[<span data-ttu-id="6e9dd-132">Enable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="6e9dd-132">Enable-AzDataCollection</span></span>](./Enable-AzDataCollection.md)

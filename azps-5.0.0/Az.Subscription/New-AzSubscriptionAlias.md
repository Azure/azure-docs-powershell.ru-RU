---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Subscription.dll-Help.xml
Module Name: Az.Subscription
online version: https://docs.microsoft.com/en-us/powershell/module/az.subscription/new-azsubscriptionalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/New-AzSubscriptionAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/New-AzSubscriptionAlias.md
ms.openlocfilehash: 2e957f3a149c4aac30ac83c03997611125aa7870
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249297"
---
# <span data-ttu-id="68a69-101">New-AzSubscriptionAlias</span><span class="sxs-lookup"><span data-stu-id="68a69-101">New-AzSubscriptionAlias</span></span>

## <span data-ttu-id="68a69-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="68a69-102">SYNOPSIS</span></span>
<span data-ttu-id="68a69-103">Создание нового псевдонима и подписки</span><span class="sxs-lookup"><span data-stu-id="68a69-103">Creates new alias and subscription</span></span>

## <span data-ttu-id="68a69-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="68a69-104">SYNTAX</span></span>

```
New-AzSubscriptionAlias -AliasName <String> [-BillingScope <String>] [-Workload <String>]
 [-SubscriptionName <String>] [-ResellerId <String>] [-SubscriptionId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68a69-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="68a69-105">DESCRIPTION</span></span>
<span data-ttu-id="68a69-106">Командлет **New-AzSubscriptionAlias** создает новый псевдоним и подписку.</span><span class="sxs-lookup"><span data-stu-id="68a69-106">The **New-AzSubscriptionAlias** cmdlet creates new alias and subscription</span></span>

## <span data-ttu-id="68a69-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="68a69-107">EXAMPLES</span></span>

### <span data-ttu-id="68a69-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="68a69-108">Example 1</span></span>
```powershell
PS C:\> New-AzSubscriptionAlias -AliasName "NewAliasName" -SubscriptionName "SubscriptionName" -BillingScope "BillingScope" -Workload "WorkloadType"
```

<span data-ttu-id="68a69-109">Создание нового псевдонима и подписки</span><span class="sxs-lookup"><span data-stu-id="68a69-109">Creates new alias and subscription</span></span>

## <span data-ttu-id="68a69-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="68a69-110">PARAMETERS</span></span>

### <span data-ttu-id="68a69-111">-AliasName</span><span class="sxs-lookup"><span data-stu-id="68a69-111">-AliasName</span></span>
<span data-ttu-id="68a69-112">Псевдоним для подписки</span><span class="sxs-lookup"><span data-stu-id="68a69-112">Alias for the subscription</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68a69-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="68a69-113">-AsJob</span></span>
<span data-ttu-id="68a69-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="68a69-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68a69-115">-BillingScope</span><span class="sxs-lookup"><span data-stu-id="68a69-115">-BillingScope</span></span>
<span data-ttu-id="68a69-116">Область выставления счетов</span><span class="sxs-lookup"><span data-stu-id="68a69-116">Billing Scope</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68a69-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68a69-117">-DefaultProfile</span></span>
<span data-ttu-id="68a69-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="68a69-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="68a69-119">-ResellerId</span><span class="sxs-lookup"><span data-stu-id="68a69-119">-ResellerId</span></span>
<span data-ttu-id="68a69-120">Идентификатор торгового посредника</span><span class="sxs-lookup"><span data-stu-id="68a69-120">Reseller Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68a69-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="68a69-121">-SubscriptionId</span></span>
<span data-ttu-id="68a69-122">Идентификатор существующей подписки</span><span class="sxs-lookup"><span data-stu-id="68a69-122">Existing Subscription Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68a69-123">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="68a69-123">-SubscriptionName</span></span>
<span data-ttu-id="68a69-124">Имя подписки</span><span class="sxs-lookup"><span data-stu-id="68a69-124">Name of the subscription</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68a69-125">-Рабочая нагрузка</span><span class="sxs-lookup"><span data-stu-id="68a69-125">-Workload</span></span>
<span data-ttu-id="68a69-126">Тип рабочей нагрузки</span><span class="sxs-lookup"><span data-stu-id="68a69-126">Type of Workload</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68a69-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="68a69-127">-Confirm</span></span>
<span data-ttu-id="68a69-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="68a69-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68a69-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68a69-129">-WhatIf</span></span>
<span data-ttu-id="68a69-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="68a69-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68a69-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="68a69-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68a69-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68a69-132">CommonParameters</span></span>
<span data-ttu-id="68a69-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="68a69-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68a69-134">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="68a69-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68a69-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="68a69-135">INPUTS</span></span>

### <span data-ttu-id="68a69-136">Ничего</span><span class="sxs-lookup"><span data-stu-id="68a69-136">None</span></span>

## <span data-ttu-id="68a69-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="68a69-137">OUTPUTS</span></span>

### <span data-ttu-id="68a69-138">Microsoft. Azure. Commands. Subscription. Models. PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="68a69-138">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="68a69-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="68a69-139">NOTES</span></span>

## <span data-ttu-id="68a69-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="68a69-140">RELATED LINKS</span></span>

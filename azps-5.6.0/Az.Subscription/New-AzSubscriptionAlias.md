---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Subscription.dll-Help.xml
Module Name: Az.Subscription
online version: https://docs.microsoft.com/powershell/module/az.subscription/new-azsubscriptionalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/New-AzSubscriptionAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/New-AzSubscriptionAlias.md
ms.openlocfilehash: 30c90d4b04c6c32144946cbdf98c59991133dbf9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015827"
---
# <span data-ttu-id="ec4ae-101">New-AzSubscriptionAlias</span><span class="sxs-lookup"><span data-stu-id="ec4ae-101">New-AzSubscriptionAlias</span></span>

## <span data-ttu-id="ec4ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec4ae-102">SYNOPSIS</span></span>
<span data-ttu-id="ec4ae-103">Создание псевдонима и подписки</span><span class="sxs-lookup"><span data-stu-id="ec4ae-103">Creates new alias and subscription</span></span>

## <span data-ttu-id="ec4ae-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ec4ae-104">SYNTAX</span></span>

```
New-AzSubscriptionAlias -AliasName <String> [-BillingScope <String>] [-Workload <String>]
 [-SubscriptionName <String>] [-ResellerId <String>] [-SubscriptionId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ec4ae-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ec4ae-105">DESCRIPTION</span></span>
<span data-ttu-id="ec4ae-106">Для создания нового псевдонима и подписки будет создаваться новый псевдоним и подписка на **New-AzSubscriptionAlias.**</span><span class="sxs-lookup"><span data-stu-id="ec4ae-106">The **New-AzSubscriptionAlias** cmdlet creates new alias and subscription</span></span>

## <span data-ttu-id="ec4ae-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ec4ae-107">EXAMPLES</span></span>

### <span data-ttu-id="ec4ae-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ec4ae-108">Example 1</span></span>
```powershell
PS C:\> New-AzSubscriptionAlias -AliasName "NewAliasName" -SubscriptionName "SubscriptionName" -BillingScope "BillingScope" -Workload "WorkloadType"
```

<span data-ttu-id="ec4ae-109">Создание псевдонима и подписки</span><span class="sxs-lookup"><span data-stu-id="ec4ae-109">Creates new alias and subscription</span></span>

## <span data-ttu-id="ec4ae-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ec4ae-110">PARAMETERS</span></span>

### <span data-ttu-id="ec4ae-111">-AliasName</span><span class="sxs-lookup"><span data-stu-id="ec4ae-111">-AliasName</span></span>
<span data-ttu-id="ec4ae-112">Псевдоним подписки</span><span class="sxs-lookup"><span data-stu-id="ec4ae-112">Alias for the subscription</span></span>

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

### <span data-ttu-id="ec4ae-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ec4ae-113">-AsJob</span></span>
<span data-ttu-id="ec4ae-114">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="ec4ae-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ec4ae-115">-BillingScope</span><span class="sxs-lookup"><span data-stu-id="ec4ae-115">-BillingScope</span></span>
<span data-ttu-id="ec4ae-116">Область вы выставления счета</span><span class="sxs-lookup"><span data-stu-id="ec4ae-116">Billing Scope</span></span>

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

### <span data-ttu-id="ec4ae-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec4ae-117">-DefaultProfile</span></span>
<span data-ttu-id="ec4ae-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ec4ae-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec4ae-119">-ResellerId</span><span class="sxs-lookup"><span data-stu-id="ec4ae-119">-ResellerId</span></span>
<span data-ttu-id="ec4ae-120">ИД reseller</span><span class="sxs-lookup"><span data-stu-id="ec4ae-120">Reseller Id</span></span>

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

### <span data-ttu-id="ec4ae-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ec4ae-121">-SubscriptionId</span></span>
<span data-ttu-id="ec4ae-122">Существующий ИД подписки</span><span class="sxs-lookup"><span data-stu-id="ec4ae-122">Existing Subscription Id</span></span>

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

### <span data-ttu-id="ec4ae-123">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="ec4ae-123">-SubscriptionName</span></span>
<span data-ttu-id="ec4ae-124">Название подписки</span><span class="sxs-lookup"><span data-stu-id="ec4ae-124">Name of the subscription</span></span>

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

### <span data-ttu-id="ec4ae-125">-Рабочая нагрузка</span><span class="sxs-lookup"><span data-stu-id="ec4ae-125">-Workload</span></span>
<span data-ttu-id="ec4ae-126">Тип рабочей нагрузки</span><span class="sxs-lookup"><span data-stu-id="ec4ae-126">Type of Workload</span></span>

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

### <span data-ttu-id="ec4ae-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ec4ae-127">-Confirm</span></span>
<span data-ttu-id="ec4ae-128">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="ec4ae-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec4ae-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec4ae-129">-WhatIf</span></span>
<span data-ttu-id="ec4ae-130">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ec4ae-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec4ae-131">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ec4ae-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec4ae-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec4ae-132">CommonParameters</span></span>
<span data-ttu-id="ec4ae-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec4ae-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec4ae-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ec4ae-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec4ae-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ec4ae-135">INPUTS</span></span>

### <span data-ttu-id="ec4ae-136">Нет</span><span class="sxs-lookup"><span data-stu-id="ec4ae-136">None</span></span>

## <span data-ttu-id="ec4ae-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ec4ae-137">OUTPUTS</span></span>

### <span data-ttu-id="ec4ae-138">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="ec4ae-138">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="ec4ae-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ec4ae-139">NOTES</span></span>

## <span data-ttu-id="ec4ae-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ec4ae-140">RELATED LINKS</span></span>

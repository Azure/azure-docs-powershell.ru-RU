---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Subscription.dll-Help.xml
Module Name: Az.Subscription
online version: https://docs.microsoft.com/en-us/powershell/module/az.subscription/new-azsubscriptionalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/New-AzSubscriptionAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/New-AzSubscriptionAlias.md
ms.openlocfilehash: 2e957f3a149c4aac30ac83c03997611125aa7870
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98415319"
---
# <span data-ttu-id="91869-101">New-AzSubscriptionAlias</span><span class="sxs-lookup"><span data-stu-id="91869-101">New-AzSubscriptionAlias</span></span>

## <span data-ttu-id="91869-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91869-102">SYNOPSIS</span></span>
<span data-ttu-id="91869-103">Создание псевдонима и подписки</span><span class="sxs-lookup"><span data-stu-id="91869-103">Creates new alias and subscription</span></span>

## <span data-ttu-id="91869-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="91869-104">SYNTAX</span></span>

```
New-AzSubscriptionAlias -AliasName <String> [-BillingScope <String>] [-Workload <String>]
 [-SubscriptionName <String>] [-ResellerId <String>] [-SubscriptionId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91869-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="91869-105">DESCRIPTION</span></span>
<span data-ttu-id="91869-106">Для создания нового псевдонима и подписки будет создаваться новый псевдоним и подписка на **New-AzSubscriptionAlias.**</span><span class="sxs-lookup"><span data-stu-id="91869-106">The **New-AzSubscriptionAlias** cmdlet creates new alias and subscription</span></span>

## <span data-ttu-id="91869-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="91869-107">EXAMPLES</span></span>

### <span data-ttu-id="91869-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="91869-108">Example 1</span></span>
```powershell
PS C:\> New-AzSubscriptionAlias -AliasName "NewAliasName" -SubscriptionName "SubscriptionName" -BillingScope "BillingScope" -Workload "WorkloadType"
```

<span data-ttu-id="91869-109">Создание псевдонима и подписки</span><span class="sxs-lookup"><span data-stu-id="91869-109">Creates new alias and subscription</span></span>

## <span data-ttu-id="91869-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="91869-110">PARAMETERS</span></span>

### <span data-ttu-id="91869-111">-AliasName</span><span class="sxs-lookup"><span data-stu-id="91869-111">-AliasName</span></span>
<span data-ttu-id="91869-112">Псевдоним подписки</span><span class="sxs-lookup"><span data-stu-id="91869-112">Alias for the subscription</span></span>

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

### <span data-ttu-id="91869-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="91869-113">-AsJob</span></span>
<span data-ttu-id="91869-114">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="91869-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="91869-115">-BillingScope</span><span class="sxs-lookup"><span data-stu-id="91869-115">-BillingScope</span></span>
<span data-ttu-id="91869-116">Область вы выставления счета</span><span class="sxs-lookup"><span data-stu-id="91869-116">Billing Scope</span></span>

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

### <span data-ttu-id="91869-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91869-117">-DefaultProfile</span></span>
<span data-ttu-id="91869-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="91869-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91869-119">-ResellerId</span><span class="sxs-lookup"><span data-stu-id="91869-119">-ResellerId</span></span>
<span data-ttu-id="91869-120">ИД reseller</span><span class="sxs-lookup"><span data-stu-id="91869-120">Reseller Id</span></span>

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

### <span data-ttu-id="91869-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="91869-121">-SubscriptionId</span></span>
<span data-ttu-id="91869-122">Существующий ИД подписки</span><span class="sxs-lookup"><span data-stu-id="91869-122">Existing Subscription Id</span></span>

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

### <span data-ttu-id="91869-123">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="91869-123">-SubscriptionName</span></span>
<span data-ttu-id="91869-124">Название подписки</span><span class="sxs-lookup"><span data-stu-id="91869-124">Name of the subscription</span></span>

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

### <span data-ttu-id="91869-125">-Рабочая нагрузка</span><span class="sxs-lookup"><span data-stu-id="91869-125">-Workload</span></span>
<span data-ttu-id="91869-126">Тип рабочей нагрузки</span><span class="sxs-lookup"><span data-stu-id="91869-126">Type of Workload</span></span>

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

### <span data-ttu-id="91869-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="91869-127">-Confirm</span></span>
<span data-ttu-id="91869-128">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="91869-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91869-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91869-129">-WhatIf</span></span>
<span data-ttu-id="91869-130">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="91869-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="91869-131">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="91869-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91869-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91869-132">CommonParameters</span></span>
<span data-ttu-id="91869-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91869-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91869-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="91869-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91869-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="91869-135">INPUTS</span></span>

### <span data-ttu-id="91869-136">Нет</span><span class="sxs-lookup"><span data-stu-id="91869-136">None</span></span>

## <span data-ttu-id="91869-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="91869-137">OUTPUTS</span></span>

### <span data-ttu-id="91869-138">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="91869-138">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="91869-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="91869-139">NOTES</span></span>

## <span data-ttu-id="91869-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="91869-140">RELATED LINKS</span></span>

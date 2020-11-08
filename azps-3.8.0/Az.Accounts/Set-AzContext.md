---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/set-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzContext.md
ms.openlocfilehash: f7d6c1fcfe4a74601a8a27e85bd1520912b26350
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066461"
---
# <span data-ttu-id="c2cbe-101">Set-AzContext</span><span class="sxs-lookup"><span data-stu-id="c2cbe-101">Set-AzContext</span></span>

## <span data-ttu-id="c2cbe-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c2cbe-102">SYNOPSIS</span></span>
<span data-ttu-id="c2cbe-103">Задает клиента, подписку и среду для командлетов, используемых в текущем сеансе.</span><span class="sxs-lookup"><span data-stu-id="c2cbe-103">Sets the tenant, subscription, and environment for cmdlets to use in the current session.</span></span>

## <span data-ttu-id="c2cbe-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c2cbe-104">SYNTAX</span></span>

### <span data-ttu-id="c2cbe-105">Контекст (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c2cbe-105">Context (Default)</span></span>
```
Set-AzContext [-Context] <PSAzureContext>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c2cbe-106">TenantObject</span><span class="sxs-lookup"><span data-stu-id="c2cbe-106">TenantObject</span></span>
```
Set-AzContext [-TenantObject] <PSAzureTenant>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c2cbe-107">SubscriptionObject</span><span class="sxs-lookup"><span data-stu-id="c2cbe-107">SubscriptionObject</span></span>
```
Set-AzContext [-SubscriptionObject] <PSAzureSubscription>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c2cbe-108">Лимит</span><span class="sxs-lookup"><span data-stu-id="c2cbe-108">Subscription</span></span>
```
Set-AzContext [-Tenant <String>] [-Subscription] <String>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c2cbe-109">TenantNameOnly</span><span class="sxs-lookup"><span data-stu-id="c2cbe-109">TenantNameOnly</span></span>
```
Set-AzContext -Tenant <String>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c2cbe-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c2cbe-110">DESCRIPTION</span></span>
<span data-ttu-id="c2cbe-111">Командлет Set-AzContext задает параметры проверки подлинности для командлетов, выполняемых в текущем сеансе.</span><span class="sxs-lookup"><span data-stu-id="c2cbe-111">The Set-AzContext cmdlet sets authentication information for cmdlets that you run in the current session.</span></span>
<span data-ttu-id="c2cbe-112">Контекст включает сведения о клиенте, подписке и среде.</span><span class="sxs-lookup"><span data-stu-id="c2cbe-112">The context includes tenant, subscription, and environment information.</span></span>

## <span data-ttu-id="c2cbe-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c2cbe-113">EXAMPLES</span></span>

### <span data-ttu-id="c2cbe-114">Пример 1: Настройка контекста подписки</span><span class="sxs-lookup"><span data-stu-id="c2cbe-114">Example 1: Set the subscription context</span></span>
```
PS C:\>Set-AzContext -SubscriptionId "xxxx-xxxx-xxxx-xxxx"

Name    Account             SubscriptionName    Environment         TenantId
----    -------             ----------------    -----------         --------
Work    test@outlook.com    Subscription1       AzureCloud          xxxxxxxx-x...
```

<span data-ttu-id="c2cbe-115">Эта команда задает контекст для использования указанной подписки.</span><span class="sxs-lookup"><span data-stu-id="c2cbe-115">This command sets the context to use the specified subscription.</span></span>

## <span data-ttu-id="c2cbe-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c2cbe-116">PARAMETERS</span></span>

### <span data-ttu-id="c2cbe-117">-Context</span><span class="sxs-lookup"><span data-stu-id="c2cbe-117">-Context</span></span>
<span data-ttu-id="c2cbe-118">Задает контекст для текущего сеанса.</span><span class="sxs-lookup"><span data-stu-id="c2cbe-118">Specifies the context for the current session.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext
Parameter Sets: Context
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c2cbe-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2cbe-119">-DefaultProfile</span></span>
<span data-ttu-id="c2cbe-120">Учетные данные, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c2cbe-120">The credentials, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c2cbe-121">-ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="c2cbe-121">-ExtendedProperty</span></span>
<span data-ttu-id="c2cbe-122">Дополнительные свойства контекста</span><span class="sxs-lookup"><span data-stu-id="c2cbe-122">Additional context properties</span></span>

```yaml
Type: System.Collections.Generic.IDictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2cbe-123">-Force</span><span class="sxs-lookup"><span data-stu-id="c2cbe-123">-Force</span></span>
<span data-ttu-id="c2cbe-124">Перезаписать существующий контекст с тем же именем, если таковое имеется.</span><span class="sxs-lookup"><span data-stu-id="c2cbe-124">Overwrite the existing context with the same name, if any.</span></span>

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

### <span data-ttu-id="c2cbe-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c2cbe-125">-Name</span></span>
<span data-ttu-id="c2cbe-126">Имя контекста</span><span class="sxs-lookup"><span data-stu-id="c2cbe-126">Name of the context</span></span>

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

### <span data-ttu-id="c2cbe-127">-Scope</span><span class="sxs-lookup"><span data-stu-id="c2cbe-127">-Scope</span></span>
<span data-ttu-id="c2cbe-128">Определяет область изменений контекста, например, применяются ли изменения только к текущему процессу или ко всем сеансам, запускаемым этим пользователем.</span><span class="sxs-lookup"><span data-stu-id="c2cbe-128">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2cbe-129">-Подписка</span><span class="sxs-lookup"><span data-stu-id="c2cbe-129">-Subscription</span></span>
<span data-ttu-id="c2cbe-130">Имя или идентификатор подписки, для которой должен быть установлен контекст.</span><span class="sxs-lookup"><span data-stu-id="c2cbe-130">The name or id of the subscription that the context should be set to.</span></span> <span data-ttu-id="c2cbe-131">Этот параметр имеет псевдонимы для-SubscriptionName и-SubscriptionId, поэтому при указании имени и идентификатора вместо подписки можно использовать любую из них.</span><span class="sxs-lookup"><span data-stu-id="c2cbe-131">This parameter has aliases to -SubscriptionName and -SubscriptionId, so, for clarity, either of these can be used instead of -Subscription when specifying name and id, respectively.</span></span>

```yaml
Type: System.String
Parameter Sets: Subscription
Aliases: SubscriptionId, SubscriptionName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2cbe-132">-SubscriptionObject</span><span class="sxs-lookup"><span data-stu-id="c2cbe-132">-SubscriptionObject</span></span>
<span data-ttu-id="c2cbe-133">Объект подписки</span><span class="sxs-lookup"><span data-stu-id="c2cbe-133">A subscription object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.PSAzureSubscription
Parameter Sets: SubscriptionObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c2cbe-134">-Клиент</span><span class="sxs-lookup"><span data-stu-id="c2cbe-134">-Tenant</span></span>
<span data-ttu-id="c2cbe-135">Имя или идентификатор клиента</span><span class="sxs-lookup"><span data-stu-id="c2cbe-135">Tenant name or ID</span></span>

```yaml
Type: System.String
Parameter Sets: Subscription
Aliases: Domain, TenantId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: TenantNameOnly
Aliases: Domain, TenantId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2cbe-136">-TenantObject</span><span class="sxs-lookup"><span data-stu-id="c2cbe-136">-TenantObject</span></span>
<span data-ttu-id="c2cbe-137">Объект клиента</span><span class="sxs-lookup"><span data-stu-id="c2cbe-137">A Tenant Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.PSAzureTenant
Parameter Sets: TenantObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c2cbe-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c2cbe-138">-Confirm</span></span>
<span data-ttu-id="c2cbe-139">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c2cbe-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2cbe-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2cbe-140">-WhatIf</span></span>
<span data-ttu-id="c2cbe-141">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c2cbe-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c2cbe-142">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c2cbe-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2cbe-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2cbe-143">CommonParameters</span></span>
<span data-ttu-id="c2cbe-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c2cbe-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2cbe-145">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2cbe-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2cbe-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c2cbe-146">INPUTS</span></span>

### <span data-ttu-id="c2cbe-147">Microsoft. Azure. Commands. Profile. Models. Core. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="c2cbe-147">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

### <span data-ttu-id="c2cbe-148">Microsoft. Azure. Commands. Profile. Models. PSAzureTenant</span><span class="sxs-lookup"><span data-stu-id="c2cbe-148">Microsoft.Azure.Commands.Profile.Models.PSAzureTenant</span></span>

### <span data-ttu-id="c2cbe-149">Microsoft. Azure. Commands. Profile. Models. PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="c2cbe-149">Microsoft.Azure.Commands.Profile.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="c2cbe-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c2cbe-150">OUTPUTS</span></span>

### <span data-ttu-id="c2cbe-151">Microsoft. Azure. Commands. Profile. Models. Core. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="c2cbe-151">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="c2cbe-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="c2cbe-152">NOTES</span></span>

## <span data-ttu-id="c2cbe-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c2cbe-153">RELATED LINKS</span></span>

[<span data-ttu-id="c2cbe-154">Get-AzContext</span><span class="sxs-lookup"><span data-stu-id="c2cbe-154">Get-AzContext</span></span>](./Get-AzContext.md)


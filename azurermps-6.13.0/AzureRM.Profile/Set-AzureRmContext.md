---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/set-azurermcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Set-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Set-AzureRmContext.md
ms.openlocfilehash: 42c7e2b632b175ef12f34e04ff682020d634ef74
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733137"
---
# <span data-ttu-id="60dd3-101">Set-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="60dd3-101">Set-AzureRmContext</span></span>

## <span data-ttu-id="60dd3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="60dd3-102">SYNOPSIS</span></span>
<span data-ttu-id="60dd3-103">Задает клиента, подписку и среду для командлетов, используемых в текущем сеансе.</span><span class="sxs-lookup"><span data-stu-id="60dd3-103">Sets the tenant, subscription, and environment for cmdlets to use in the current session.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="60dd3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="60dd3-104">SYNTAX</span></span>

### <span data-ttu-id="60dd3-105">Контекст (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="60dd3-105">Context (Default)</span></span>
```
Set-AzureRmContext [-Context] <PSAzureContext>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="60dd3-106">TenantObject</span><span class="sxs-lookup"><span data-stu-id="60dd3-106">TenantObject</span></span>
```
Set-AzureRmContext [-TenantObject] <PSAzureTenant>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="60dd3-107">SubscriptionObject</span><span class="sxs-lookup"><span data-stu-id="60dd3-107">SubscriptionObject</span></span>
```
Set-AzureRmContext [-SubscriptionObject] <PSAzureSubscription>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="60dd3-108">Лимит</span><span class="sxs-lookup"><span data-stu-id="60dd3-108">Subscription</span></span>
```
Set-AzureRmContext [-Tenant <String>] [-Subscription] <String>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="60dd3-109">TenantNameOnly</span><span class="sxs-lookup"><span data-stu-id="60dd3-109">TenantNameOnly</span></span>
```
Set-AzureRmContext -Tenant <String>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="60dd3-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="60dd3-110">DESCRIPTION</span></span>
<span data-ttu-id="60dd3-111">Командлет Set-AzureRmContext задает параметры проверки подлинности для командлетов, выполняемых в текущем сеансе.</span><span class="sxs-lookup"><span data-stu-id="60dd3-111">The Set-AzureRmContext cmdlet sets authentication information for cmdlets that you run in the current session.</span></span>
<span data-ttu-id="60dd3-112">Контекст включает сведения о клиенте, подписке и среде.</span><span class="sxs-lookup"><span data-stu-id="60dd3-112">The context includes tenant, subscription, and environment information.</span></span>

## <span data-ttu-id="60dd3-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="60dd3-113">EXAMPLES</span></span>

### <span data-ttu-id="60dd3-114">Пример 1: Настройка контекста подписки</span><span class="sxs-lookup"><span data-stu-id="60dd3-114">Example 1: Set the subscription context</span></span>
```
PS C:\>Set-AzureRmContext -SubscriptionId "xxxx-xxxx-xxxx-xxxx"

Name    Account             SubscriptionName    Environment         TenantId
----    -------             ----------------    -----------         --------
Work    test@outlook.com    Subscription1       AzureCloud          xxxxxxxx-x...
```

<span data-ttu-id="60dd3-115">Эта команда задает контекст для использования указанной подписки.</span><span class="sxs-lookup"><span data-stu-id="60dd3-115">This command sets the context to use the specified subscription.</span></span>

## <span data-ttu-id="60dd3-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="60dd3-116">PARAMETERS</span></span>

### <span data-ttu-id="60dd3-117">-Context</span><span class="sxs-lookup"><span data-stu-id="60dd3-117">-Context</span></span>
<span data-ttu-id="60dd3-118">Задает контекст для текущего сеанса.</span><span class="sxs-lookup"><span data-stu-id="60dd3-118">Specifies the context for the current session.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.PSAzureContext
Parameter Sets: Context
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="60dd3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60dd3-119">-DefaultProfile</span></span>
<span data-ttu-id="60dd3-120">Учетные данные, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="60dd3-120">The credentials, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60dd3-121">-ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="60dd3-121">-ExtendedProperty</span></span>
<span data-ttu-id="60dd3-122">Дополнительные свойства контекста</span><span class="sxs-lookup"><span data-stu-id="60dd3-122">Additional context properties</span></span>

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

### <span data-ttu-id="60dd3-123">-Force</span><span class="sxs-lookup"><span data-stu-id="60dd3-123">-Force</span></span>
<span data-ttu-id="60dd3-124">Перезаписать существующий контекст с тем же именем, если таковое имеется.</span><span class="sxs-lookup"><span data-stu-id="60dd3-124">Overwrite the existing context with the same name, if any.</span></span>

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

### <span data-ttu-id="60dd3-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="60dd3-125">-Name</span></span>
<span data-ttu-id="60dd3-126">Имя контекста</span><span class="sxs-lookup"><span data-stu-id="60dd3-126">Name of the context</span></span>

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

### <span data-ttu-id="60dd3-127">-Scope</span><span class="sxs-lookup"><span data-stu-id="60dd3-127">-Scope</span></span>
<span data-ttu-id="60dd3-128">Определяет область изменений контекста, например, применяются ли изменения только к текущему процессу или ко всем сеансам, запускаемым этим пользователем.</span><span class="sxs-lookup"><span data-stu-id="60dd3-128">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="60dd3-129">-Подписка</span><span class="sxs-lookup"><span data-stu-id="60dd3-129">-Subscription</span></span>
<span data-ttu-id="60dd3-130">Имя или идентификатор подписки, для которой должен быть установлен контекст.</span><span class="sxs-lookup"><span data-stu-id="60dd3-130">The name or id of the subscription that the context should be set to.</span></span> <span data-ttu-id="60dd3-131">Этот параметр имеет псевдонимы для-SubscriptionName и-SubscriptionId, поэтому при указании имени и идентификатора вместо подписки можно использовать любую из них.</span><span class="sxs-lookup"><span data-stu-id="60dd3-131">This parameter has aliases to -SubscriptionName and -SubscriptionId, so, for clarity, either of these can be used instead of -Subscription when specifying name and id, respectively.</span></span>

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

### <span data-ttu-id="60dd3-132">-SubscriptionObject</span><span class="sxs-lookup"><span data-stu-id="60dd3-132">-SubscriptionObject</span></span>
<span data-ttu-id="60dd3-133">Объект подписки</span><span class="sxs-lookup"><span data-stu-id="60dd3-133">A subscription object</span></span>

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

### <span data-ttu-id="60dd3-134">-Клиент</span><span class="sxs-lookup"><span data-stu-id="60dd3-134">-Tenant</span></span>
<span data-ttu-id="60dd3-135">Имя или идентификатор клиента</span><span class="sxs-lookup"><span data-stu-id="60dd3-135">Tenant name or ID</span></span>

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

### <span data-ttu-id="60dd3-136">-TenantObject</span><span class="sxs-lookup"><span data-stu-id="60dd3-136">-TenantObject</span></span>
<span data-ttu-id="60dd3-137">Объект клиента</span><span class="sxs-lookup"><span data-stu-id="60dd3-137">A Tenant Object</span></span>

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

### <span data-ttu-id="60dd3-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="60dd3-138">-Confirm</span></span>
<span data-ttu-id="60dd3-139">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="60dd3-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60dd3-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60dd3-140">-WhatIf</span></span>
<span data-ttu-id="60dd3-141">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="60dd3-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="60dd3-142">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="60dd3-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60dd3-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60dd3-143">CommonParameters</span></span>
<span data-ttu-id="60dd3-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="60dd3-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60dd3-145">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60dd3-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60dd3-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="60dd3-146">INPUTS</span></span>

### <span data-ttu-id="60dd3-147">Microsoft. Azure. Commands. Profile. Models. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="60dd3-147">Microsoft.Azure.Commands.Profile.Models.PSAzureContext</span></span>
<span data-ttu-id="60dd3-148">Параметры: Context (ByValue)</span><span class="sxs-lookup"><span data-stu-id="60dd3-148">Parameters: Context (ByValue)</span></span>

### <span data-ttu-id="60dd3-149">Microsoft. Azure. Commands. Profile. Models. PSAzureTenant</span><span class="sxs-lookup"><span data-stu-id="60dd3-149">Microsoft.Azure.Commands.Profile.Models.PSAzureTenant</span></span>
<span data-ttu-id="60dd3-150">Параметры: TenantObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="60dd3-150">Parameters: TenantObject (ByValue)</span></span>

### <span data-ttu-id="60dd3-151">Microsoft. Azure. Commands. Profile. Models. PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="60dd3-151">Microsoft.Azure.Commands.Profile.Models.PSAzureSubscription</span></span>
<span data-ttu-id="60dd3-152">Параметры: SubscriptionObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="60dd3-152">Parameters: SubscriptionObject (ByValue)</span></span>

## <span data-ttu-id="60dd3-153">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="60dd3-153">OUTPUTS</span></span>

### <span data-ttu-id="60dd3-154">Microsoft. Azure. Commands. Profile. Models. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="60dd3-154">Microsoft.Azure.Commands.Profile.Models.PSAzureContext</span></span>

## <span data-ttu-id="60dd3-155">Пуск</span><span class="sxs-lookup"><span data-stu-id="60dd3-155">NOTES</span></span>

## <span data-ttu-id="60dd3-156">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="60dd3-156">RELATED LINKS</span></span>

[<span data-ttu-id="60dd3-157">Get-AzureRMContext</span><span class="sxs-lookup"><span data-stu-id="60dd3-157">Get-AzureRMContext</span></span>](./Get-AzureRMContext.md)


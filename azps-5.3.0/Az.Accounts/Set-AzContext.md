---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/set-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzContext.md
ms.openlocfilehash: 49805dee2bff967da294fda228b5426e2652e209
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98507012"
---
# <span data-ttu-id="2c4c9-101">Set-AzContext</span><span class="sxs-lookup"><span data-stu-id="2c4c9-101">Set-AzContext</span></span>

## <span data-ttu-id="2c4c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2c4c9-102">SYNOPSIS</span></span>
<span data-ttu-id="2c4c9-103">Настраивает клиент, подписку и среду для использования в текущем сеансе.</span><span class="sxs-lookup"><span data-stu-id="2c4c9-103">Sets the tenant, subscription, and environment for cmdlets to use in the current session.</span></span>

## <span data-ttu-id="2c4c9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2c4c9-104">SYNTAX</span></span>

### <span data-ttu-id="2c4c9-105">Контекст (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2c4c9-105">Context (Default)</span></span>
```
Set-AzContext [-Context] <PSAzureContext>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2c4c9-106">TenantObject</span><span class="sxs-lookup"><span data-stu-id="2c4c9-106">TenantObject</span></span>
```
Set-AzContext [-TenantObject] <PSAzureTenant>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2c4c9-107">SubscriptionObject</span><span class="sxs-lookup"><span data-stu-id="2c4c9-107">SubscriptionObject</span></span>
```
Set-AzContext [-SubscriptionObject] <PSAzureSubscription>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2c4c9-108">Подписка</span><span class="sxs-lookup"><span data-stu-id="2c4c9-108">Subscription</span></span>
```
Set-AzContext [-Tenant <String>] [-Subscription] <String>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2c4c9-109">TenantNameOnly</span><span class="sxs-lookup"><span data-stu-id="2c4c9-109">TenantNameOnly</span></span>
```
Set-AzContext -Tenant <String>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2c4c9-110">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2c4c9-110">DESCRIPTION</span></span>
<span data-ttu-id="2c4c9-111">Этот Set-AzContext задает сведения для проверки подлинности для cmdlets, которые вы запустите в текущем сеансе.</span><span class="sxs-lookup"><span data-stu-id="2c4c9-111">The Set-AzContext cmdlet sets authentication information for cmdlets that you run in the current session.</span></span>
<span data-ttu-id="2c4c9-112">Контекст включает сведения о клиенте, подписке и среде.</span><span class="sxs-lookup"><span data-stu-id="2c4c9-112">The context includes tenant, subscription, and environment information.</span></span>

## <span data-ttu-id="2c4c9-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2c4c9-113">EXAMPLES</span></span>

### <span data-ttu-id="2c4c9-114">Пример 1. Настройка контекста подписки</span><span class="sxs-lookup"><span data-stu-id="2c4c9-114">Example 1: Set the subscription context</span></span>
```
PS C:\>Set-AzContext -Subscription "xxxx-xxxx-xxxx-xxxx"

Name    Account             SubscriptionName    Environment         TenantId
----    -------             ----------------    -----------         --------
Work    test@outlook.com    Subscription1       AzureCloud          xxxxxxxx-x...
```

<span data-ttu-id="2c4c9-115">Эта команда задает контекст для использования указанной подписки.</span><span class="sxs-lookup"><span data-stu-id="2c4c9-115">This command sets the context to use the specified subscription.</span></span>

## <span data-ttu-id="2c4c9-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2c4c9-116">PARAMETERS</span></span>

### <span data-ttu-id="2c4c9-117">-Контекст</span><span class="sxs-lookup"><span data-stu-id="2c4c9-117">-Context</span></span>
<span data-ttu-id="2c4c9-118">Определяет контекст для текущего сеанса.</span><span class="sxs-lookup"><span data-stu-id="2c4c9-118">Specifies the context for the current session.</span></span>

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

### <span data-ttu-id="2c4c9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c4c9-119">-DefaultProfile</span></span>
<span data-ttu-id="2c4c9-120">Учетные данные, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2c4c9-120">The credentials, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2c4c9-121">-ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="2c4c9-121">-ExtendedProperty</span></span>
<span data-ttu-id="2c4c9-122">Дополнительные свойства контекста</span><span class="sxs-lookup"><span data-stu-id="2c4c9-122">Additional context properties</span></span>

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

### <span data-ttu-id="2c4c9-123">-Force</span><span class="sxs-lookup"><span data-stu-id="2c4c9-123">-Force</span></span>
<span data-ttu-id="2c4c9-124">Переописывание существующего контекста с тем же именем (если есть).</span><span class="sxs-lookup"><span data-stu-id="2c4c9-124">Overwrite the existing context with the same name, if any.</span></span>

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

### <span data-ttu-id="2c4c9-125">-Name</span><span class="sxs-lookup"><span data-stu-id="2c4c9-125">-Name</span></span>
<span data-ttu-id="2c4c9-126">Имя контекста</span><span class="sxs-lookup"><span data-stu-id="2c4c9-126">Name of the context</span></span>

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

### <span data-ttu-id="2c4c9-127">-Scope</span><span class="sxs-lookup"><span data-stu-id="2c4c9-127">-Scope</span></span>
<span data-ttu-id="2c4c9-128">Определяет область изменения контекста, например, применяются ли изменения только к текущему процессу или же к всем сеансам, на которые начал пользователь.</span><span class="sxs-lookup"><span data-stu-id="2c4c9-128">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="2c4c9-129">-Подписка</span><span class="sxs-lookup"><span data-stu-id="2c4c9-129">-Subscription</span></span>
<span data-ttu-id="2c4c9-130">Имя или ид подписки, для которого должен быть установлен контекст.</span><span class="sxs-lookup"><span data-stu-id="2c4c9-130">The name or id of the subscription that the context should be set to.</span></span> <span data-ttu-id="2c4c9-131">У этого параметра есть псевдонимы к -SubscriptionName и -SubscriptionId, поэтому для ясности при указании имени и ид можно использовать любой из них вместо -Subscription.</span><span class="sxs-lookup"><span data-stu-id="2c4c9-131">This parameter has aliases to -SubscriptionName and -SubscriptionId, so, for clarity, either of these can be used instead of -Subscription when specifying name and id, respectively.</span></span>

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

### <span data-ttu-id="2c4c9-132">-SubscriptionObject</span><span class="sxs-lookup"><span data-stu-id="2c4c9-132">-SubscriptionObject</span></span>
<span data-ttu-id="2c4c9-133">Объект подписки</span><span class="sxs-lookup"><span data-stu-id="2c4c9-133">A subscription object</span></span>

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

### <span data-ttu-id="2c4c9-134">-Tenant</span><span class="sxs-lookup"><span data-stu-id="2c4c9-134">-Tenant</span></span>
<span data-ttu-id="2c4c9-135">Имя клиента или ИД клиента</span><span class="sxs-lookup"><span data-stu-id="2c4c9-135">Tenant name or ID</span></span>

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

### <span data-ttu-id="2c4c9-136">-TenantObject</span><span class="sxs-lookup"><span data-stu-id="2c4c9-136">-TenantObject</span></span>
<span data-ttu-id="2c4c9-137">Объект клиента</span><span class="sxs-lookup"><span data-stu-id="2c4c9-137">A Tenant Object</span></span>

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

### <span data-ttu-id="2c4c9-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2c4c9-138">-Confirm</span></span>
<span data-ttu-id="2c4c9-139">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2c4c9-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c4c9-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c4c9-140">-WhatIf</span></span>
<span data-ttu-id="2c4c9-141">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2c4c9-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2c4c9-142">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="2c4c9-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c4c9-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c4c9-143">CommonParameters</span></span>
<span data-ttu-id="2c4c9-144">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c4c9-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c4c9-145">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c4c9-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c4c9-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2c4c9-146">INPUTS</span></span>

### <span data-ttu-id="2c4c9-147">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="2c4c9-147">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

### <span data-ttu-id="2c4c9-148">Microsoft.Azure.Commands.Profile.Models.PSAzureTenant</span><span class="sxs-lookup"><span data-stu-id="2c4c9-148">Microsoft.Azure.Commands.Profile.Models.PSAzureTenant</span></span>

### <span data-ttu-id="2c4c9-149">Microsoft.Azure.Commands.Profile.Models.PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="2c4c9-149">Microsoft.Azure.Commands.Profile.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="2c4c9-150">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2c4c9-150">OUTPUTS</span></span>

### <span data-ttu-id="2c4c9-151">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="2c4c9-151">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="2c4c9-152">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2c4c9-152">NOTES</span></span>

## <span data-ttu-id="2c4c9-153">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2c4c9-153">RELATED LINKS</span></span>

[<span data-ttu-id="2c4c9-154">Get-AzContext</span><span class="sxs-lookup"><span data-stu-id="2c4c9-154">Get-AzContext</span></span>](./Get-AzContext.md)


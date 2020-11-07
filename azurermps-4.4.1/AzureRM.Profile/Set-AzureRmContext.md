---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Set-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Set-AzureRmContext.md
ms.openlocfilehash: 99adb0cb38cd5c1e43dbd9f7dd5f81a4bef26beb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733343"
---
# <span data-ttu-id="7d8d4-101">Set-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="7d8d4-101">Set-AzureRmContext</span></span>

## <span data-ttu-id="7d8d4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7d8d4-102">SYNOPSIS</span></span>
<span data-ttu-id="7d8d4-103">Задает клиента, подписку и среду для командлетов, используемых в текущем сеансе.</span><span class="sxs-lookup"><span data-stu-id="7d8d4-103">Sets the tenant, subscription, and environment for cmdlets to use in the current session.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7d8d4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7d8d4-104">SYNTAX</span></span>

### <span data-ttu-id="7d8d4-105">Контекст (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7d8d4-105">Context (Default)</span></span>
```
Set-AzureRmContext [-Context] <PSAzureContext>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7d8d4-106">TenantObject</span><span class="sxs-lookup"><span data-stu-id="7d8d4-106">TenantObject</span></span>
```
Set-AzureRmContext [-TenantObject] <PSAzureTenant>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7d8d4-107">SubscriptionObject</span><span class="sxs-lookup"><span data-stu-id="7d8d4-107">SubscriptionObject</span></span>
```
Set-AzureRmContext [-SubscriptionObject] <PSAzureSubscription>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7d8d4-108">Лимит</span><span class="sxs-lookup"><span data-stu-id="7d8d4-108">Subscription</span></span>
```
Set-AzureRmContext [-Tenant <String>] [-Subscription] <String>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7d8d4-109">TenantNameOnly</span><span class="sxs-lookup"><span data-stu-id="7d8d4-109">TenantNameOnly</span></span>
```
Set-AzureRmContext -Tenant <String>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7d8d4-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7d8d4-110">DESCRIPTION</span></span>
<span data-ttu-id="7d8d4-111">Командлет Set-AzureRmContext задает параметры проверки подлинности для командлетов, выполняемых в текущем сеансе.</span><span class="sxs-lookup"><span data-stu-id="7d8d4-111">The Set-AzureRmContext cmdlet sets authentication information for cmdlets that you run in the current session.</span></span>
<span data-ttu-id="7d8d4-112">Контекст включает сведения о клиенте, подписке и среде.</span><span class="sxs-lookup"><span data-stu-id="7d8d4-112">The context includes tenant, subscription, and environment information.</span></span>

## <span data-ttu-id="7d8d4-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7d8d4-113">EXAMPLES</span></span>

### <span data-ttu-id="7d8d4-114">Пример 1: Настройка контекста подписки</span><span class="sxs-lookup"><span data-stu-id="7d8d4-114">Example 1: Set the subscription context</span></span>
```
PS C:\>Set-AzureRmContext -SubscriptionId "xxxx-xxxx-xxxx-xxxx"

Account      : PFuller@contoso.com
Environment  : AzureCloud
Subscription : xxxx-xxxx-xxxx-xxxx
Tenant       : yyyy-yyyy-yyyy-yyyy
```

<span data-ttu-id="7d8d4-115">Эта команда задает контекст для использования указанной подписки.</span><span class="sxs-lookup"><span data-stu-id="7d8d4-115">This command sets the context to use the specified subscription.</span></span>

## <span data-ttu-id="7d8d4-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7d8d4-116">PARAMETERS</span></span>

### <span data-ttu-id="7d8d4-117">-Context</span><span class="sxs-lookup"><span data-stu-id="7d8d4-117">-Context</span></span>
<span data-ttu-id="7d8d4-118">Задает контекст для текущего сеанса.</span><span class="sxs-lookup"><span data-stu-id="7d8d4-118">Specifies the context for the current session.</span></span>

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

### <span data-ttu-id="7d8d4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d8d4-119">-DefaultProfile</span></span>
<span data-ttu-id="7d8d4-120">Учетные данные, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7d8d4-120">The credentials, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7d8d4-121">-ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="7d8d4-121">-ExtendedProperty</span></span>
<span data-ttu-id="7d8d4-122">Дополнительные свойства контекста</span><span class="sxs-lookup"><span data-stu-id="7d8d4-122">Additional context properties</span></span>

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

### <span data-ttu-id="7d8d4-123">-Force</span><span class="sxs-lookup"><span data-stu-id="7d8d4-123">-Force</span></span>
<span data-ttu-id="7d8d4-124">Перезаписать существующий контекст с тем же именем, если таковое имеется.</span><span class="sxs-lookup"><span data-stu-id="7d8d4-124">Overwrite the existing context with the same name, if any.</span></span>

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

### <span data-ttu-id="7d8d4-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7d8d4-125">-Name</span></span>
<span data-ttu-id="7d8d4-126">Имя контекста</span><span class="sxs-lookup"><span data-stu-id="7d8d4-126">Name of the context</span></span>

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

### <span data-ttu-id="7d8d4-127">-Scope</span><span class="sxs-lookup"><span data-stu-id="7d8d4-127">-Scope</span></span>
<span data-ttu-id="7d8d4-128">Определяет область изменений контекста, например wheher изменения применяются только к процессу cusrrent или ко всем сеансам, запускаемым этим пользователем.</span><span class="sxs-lookup"><span data-stu-id="7d8d4-128">Determines the scope of context changes, for example, wheher changes apply only to the cusrrent process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="7d8d4-129">-Подписка</span><span class="sxs-lookup"><span data-stu-id="7d8d4-129">-Subscription</span></span>
<span data-ttu-id="7d8d4-130">Имя или идентификатор подписки</span><span class="sxs-lookup"><span data-stu-id="7d8d4-130">Subscription Name or Id</span></span>

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

### <span data-ttu-id="7d8d4-131">-SubscriptionObject</span><span class="sxs-lookup"><span data-stu-id="7d8d4-131">-SubscriptionObject</span></span>
<span data-ttu-id="7d8d4-132">Объект подписки</span><span class="sxs-lookup"><span data-stu-id="7d8d4-132">A subscription object</span></span>

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

### <span data-ttu-id="7d8d4-133">-Клиент</span><span class="sxs-lookup"><span data-stu-id="7d8d4-133">-Tenant</span></span>
<span data-ttu-id="7d8d4-134">Имя или идентификатор клиента</span><span class="sxs-lookup"><span data-stu-id="7d8d4-134">Tenant name or ID</span></span>

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

### <span data-ttu-id="7d8d4-135">-TenantObject</span><span class="sxs-lookup"><span data-stu-id="7d8d4-135">-TenantObject</span></span>
<span data-ttu-id="7d8d4-136">Объект клиента</span><span class="sxs-lookup"><span data-stu-id="7d8d4-136">A Tenant Object</span></span>

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

### <span data-ttu-id="7d8d4-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7d8d4-137">-Confirm</span></span>
<span data-ttu-id="7d8d4-138">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7d8d4-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d8d4-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d8d4-139">-WhatIf</span></span>
<span data-ttu-id="7d8d4-140">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7d8d4-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7d8d4-141">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7d8d4-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d8d4-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d8d4-142">CommonParameters</span></span>
<span data-ttu-id="7d8d4-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7d8d4-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d8d4-144">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d8d4-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d8d4-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7d8d4-145">INPUTS</span></span>

### <span data-ttu-id="7d8d4-146">PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="7d8d4-146">PSAzureContext</span></span>
<span data-ttu-id="7d8d4-147">Параметр "Context" принимает значение типа "PSAzureContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="7d8d4-147">Parameter 'Context' accepts value of type 'PSAzureContext' from the pipeline</span></span>

## <span data-ttu-id="7d8d4-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7d8d4-148">OUTPUTS</span></span>

### <span data-ttu-id="7d8d4-149">PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="7d8d4-149">PSAzureContext</span></span>

## <span data-ttu-id="7d8d4-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="7d8d4-150">NOTES</span></span>

## <span data-ttu-id="7d8d4-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7d8d4-151">RELATED LINKS</span></span>

[<span data-ttu-id="7d8d4-152">Get-AzureRMContext</span><span class="sxs-lookup"><span data-stu-id="7d8d4-152">Get-AzureRMContext</span></span>](./Get-AzureRMContext.md)


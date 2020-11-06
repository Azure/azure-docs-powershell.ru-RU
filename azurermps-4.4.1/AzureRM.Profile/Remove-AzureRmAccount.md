---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Remove-AzureRmAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Remove-AzureRmAccount.md
ms.openlocfilehash: d1b401c1ae806d48b9cb9969c36ef72d104076eb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565179"
---
# <span data-ttu-id="d9465-101">Remove-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="d9465-101">Remove-AzureRmAccount</span></span>

## <span data-ttu-id="d9465-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d9465-102">SYNOPSIS</span></span>
<span data-ttu-id="d9465-103">Удаление всех учетных данных и контекстов, связанных с данной учетной записью.</span><span class="sxs-lookup"><span data-stu-id="d9465-103">Remove all credentials and contexts associated with the given account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d9465-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d9465-104">SYNTAX</span></span>

### <span data-ttu-id="d9465-105">ContextName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d9465-105">ContextName (Default)</span></span>
```
Remove-AzureRmAccount [-ContextName <String>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9465-106">Идентификатора пользователя</span><span class="sxs-lookup"><span data-stu-id="d9465-106">UserId</span></span>
```
Remove-AzureRmAccount [-Username] <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9465-107">ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="d9465-107">ServicePrincipal</span></span>
```
Remove-AzureRmAccount -ApplicationId <String> -TenantId <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9465-108">AccountObject</span><span class="sxs-lookup"><span data-stu-id="d9465-108">AccountObject</span></span>
```
Remove-AzureRmAccount [-InputObject] <PSAzureRmAccount> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9465-109">ContextObject</span><span class="sxs-lookup"><span data-stu-id="d9465-109">ContextObject</span></span>
```
Remove-AzureRmAccount [-AzureContext] <PSAzureContext> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9465-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d9465-110">DESCRIPTION</span></span>
<span data-ttu-id="d9465-111">Удалите все учетные данные, а также контекст (сведения о подписке и клиенте), связанные с указанной учетной записью.</span><span class="sxs-lookup"><span data-stu-id="d9465-111">Remove all credentials, and contexts (subscription and tenant information) associated with the given account.</span></span>  <span data-ttu-id="d9465-112">После выполнения этого командлета вам потребуется выполнить вход в систему с помощью Add-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="d9465-112">After executing this cmdlet, you will need to login again using Add-AzureRmAccount</span></span>

## <span data-ttu-id="d9465-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d9465-113">EXAMPLES</span></span>

### <span data-ttu-id="d9465-114">Выход из учетной записи curent</span><span class="sxs-lookup"><span data-stu-id="d9465-114">Log out the curent account</span></span>
```
PS C:\> Remove-AzureRmAccount
```

<span data-ttu-id="d9465-115">Выполнит выход из учетной записи, связанной с текущим контекстом.</span><span class="sxs-lookup"><span data-stu-id="d9465-115">Logs out the account associated with the current context.</span></span>

### <span data-ttu-id="d9465-116">Выход из учетной записи, связанной с определенным контекстом</span><span class="sxs-lookup"><span data-stu-id="d9465-116">Log out the account associated with a particular context</span></span>
```
PS C:\> Get-AzureRmContext "Work" | Remove-AzureRmAccount -Scope CurrentUser
```

<span data-ttu-id="d9465-117">Выход из учетной записи, связанной с указанным контекстом (с именем "трудозатраты").</span><span class="sxs-lookup"><span data-stu-id="d9465-117">Logs out the account associated with the given context (named 'Work').</span></span> <span data-ttu-id="d9465-118">Так как в этом случае используется область "CurrentUser", все учетные данные и контексты удаляются без возможности восстановления.</span><span class="sxs-lookup"><span data-stu-id="d9465-118">Because this uses the 'CurrentUser' scope, all credentials and contexts will be permanently deleted.</span></span>

### <span data-ttu-id="d9465-119">Выход определенного пользователя</span><span class="sxs-lookup"><span data-stu-id="d9465-119">Log out a particular user</span></span>
```
PS C:\> Remove-AzureRmAccount -Username 'user1@contoso.org'
```

<span data-ttu-id="d9465-120">Выход из учетной user1@contoso.org записи "пользователь: все учетные данные и все контексты, связанные с этим пользователем, будут удалены.</span><span class="sxs-lookup"><span data-stu-id="d9465-120">Logs out the 'user1@contoso.org' user - all credentials and all contexts associated with this user will be removed.</span></span>

## <span data-ttu-id="d9465-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d9465-121">PARAMETERS</span></span>

### <span data-ttu-id="d9465-122">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="d9465-122">-ApplicationId</span></span>
<span data-ttu-id="d9465-123">Идентификатор ServicePrincipal (глобальный уникальный идентификатор)</span><span class="sxs-lookup"><span data-stu-id="d9465-123">ServicePrincipal id (globally unique id)</span></span>

```yaml
Type: System.String
Parameter Sets: ServicePrincipal
Aliases: SPN, ServicePrincipal

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9465-124">-AzureContext</span><span class="sxs-lookup"><span data-stu-id="d9465-124">-AzureContext</span></span>
<span data-ttu-id="d9465-125">Context</span><span class="sxs-lookup"><span data-stu-id="d9465-125">Context</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.PSAzureContext
Parameter Sets: ContextObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d9465-126">-ContextName</span><span class="sxs-lookup"><span data-stu-id="d9465-126">-ContextName</span></span>
<span data-ttu-id="d9465-127">Имя контекста для выхода из</span><span class="sxs-lookup"><span data-stu-id="d9465-127">Name of the context to log out of</span></span>

```yaml
Type: System.String
Parameter Sets: ContextName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9465-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9465-128">-DefaultProfile</span></span>
<span data-ttu-id="d9465-129">Учетные данные, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="d9465-129">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d9465-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d9465-130">-InputObject</span></span>
<span data-ttu-id="d9465-131">Удаляемый объект учетной записи</span><span class="sxs-lookup"><span data-stu-id="d9465-131">The account object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.PSAzureRmAccount
Parameter Sets: AccountObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d9465-132">-Scope</span><span class="sxs-lookup"><span data-stu-id="d9465-132">-Scope</span></span>
<span data-ttu-id="d9465-133">Определяет область изменений контекста, например, применяются ли изменения только к текущему процессу или ко всем сеансам, запускаемым этим пользователем.</span><span class="sxs-lookup"><span data-stu-id="d9465-133">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="d9465-134">-TenantId</span><span class="sxs-lookup"><span data-stu-id="d9465-134">-TenantId</span></span>
<span data-ttu-id="d9465-135">Идентификатор клиента (глобальный уникальный идентификатор)</span><span class="sxs-lookup"><span data-stu-id="d9465-135">Tenant id (globally unique id)</span></span>

```yaml
Type: System.String
Parameter Sets: ServicePrincipal
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9465-136">-Username</span><span class="sxs-lookup"><span data-stu-id="d9465-136">-Username</span></span>
<span data-ttu-id="d9465-137">Имя пользователя в форме " user@contoso.org "</span><span class="sxs-lookup"><span data-stu-id="d9465-137">User name of the form 'user@contoso.org'</span></span>

```yaml
Type: System.String
Parameter Sets: UserId
Aliases: Id, UserId

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9465-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d9465-138">-Confirm</span></span>
<span data-ttu-id="d9465-139">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d9465-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9465-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9465-140">-WhatIf</span></span>
<span data-ttu-id="d9465-141">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d9465-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9465-142">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d9465-142">The cmdlet is not executed.</span></span>

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

### <span data-ttu-id="d9465-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9465-143">CommonParameters</span></span>
<span data-ttu-id="d9465-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d9465-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9465-145">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9465-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9465-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d9465-146">INPUTS</span></span>

### <span data-ttu-id="d9465-147">Microsoft. Azure. Commands. Profile. Models. PSAzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="d9465-147">Microsoft.Azure.Commands.Profile.Models.PSAzureRmAccount</span></span>

### <span data-ttu-id="d9465-148">Microsoft. Azure. Commands. Profile. Models. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="d9465-148">Microsoft.Azure.Commands.Profile.Models.PSAzureContext</span></span>

## <span data-ttu-id="d9465-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d9465-149">OUTPUTS</span></span>

### <span data-ttu-id="d9465-150">Microsoft. Azure. Commands. Profile. Models. PSAzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="d9465-150">Microsoft.Azure.Commands.Profile.Models.PSAzureRmAccount</span></span>

## <span data-ttu-id="d9465-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="d9465-151">NOTES</span></span>

## <span data-ttu-id="d9465-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d9465-152">RELATED LINKS</span></span>


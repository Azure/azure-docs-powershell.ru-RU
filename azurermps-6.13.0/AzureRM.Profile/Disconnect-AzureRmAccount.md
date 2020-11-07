---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/remove-azurermaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Disconnect-AzureRmAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Disconnect-AzureRmAccount.md
ms.openlocfilehash: e5fbecea64a15569fbd6319f3f3be5ff4102153e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734597"
---
# <span data-ttu-id="71d50-101">Disconnect-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="71d50-101">Disconnect-AzureRmAccount</span></span>

## <span data-ttu-id="71d50-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="71d50-102">SYNOPSIS</span></span>
<span data-ttu-id="71d50-103">Отключение подключенной учетной записи Azure и удаление всех учетных данных и контекстов, связанных с этой учетной записью.</span><span class="sxs-lookup"><span data-stu-id="71d50-103">Disconnects a connected Azure account and removes all credentials and contexts associated with that account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="71d50-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="71d50-104">SYNTAX</span></span>

### <span data-ttu-id="71d50-105">ContextName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="71d50-105">ContextName (Default)</span></span>
```
Disconnect-AzureRmAccount [-ContextName <String>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71d50-106">Идентификатора пользователя</span><span class="sxs-lookup"><span data-stu-id="71d50-106">UserId</span></span>
```
Disconnect-AzureRmAccount [-Username] <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71d50-107">ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="71d50-107">ServicePrincipal</span></span>
```
Disconnect-AzureRmAccount -ApplicationId <String> -TenantId <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71d50-108">AccountObject</span><span class="sxs-lookup"><span data-stu-id="71d50-108">AccountObject</span></span>
```
Disconnect-AzureRmAccount [-InputObject] <PSAzureRmAccount> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71d50-109">ContextObject</span><span class="sxs-lookup"><span data-stu-id="71d50-109">ContextObject</span></span>
```
Disconnect-AzureRmAccount [-AzureContext] <PSAzureContext> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71d50-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="71d50-110">DESCRIPTION</span></span>
<span data-ttu-id="71d50-111">Командлет Disconnect-AzureRmAccount отключает подключенную учетную запись Azure и удаляет все учетные данные и контексты (сведения о подписке и клиенте), связанные с этой учетной записью.</span><span class="sxs-lookup"><span data-stu-id="71d50-111">The Disconnect-AzureRmAccount cmdlet disconnects a connected Azure account and removes all credentials and contexts (subscription and tenant information) associated with that account.</span></span>
<span data-ttu-id="71d50-112">После выполнения этого командлета вам потребуется снова войти в систему с помощью Connect-AzureRmAccount.</span><span class="sxs-lookup"><span data-stu-id="71d50-112">After executing this cmdlet, you will need to login again using Connect-AzureRmAccount.</span></span>

## <span data-ttu-id="71d50-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="71d50-113">EXAMPLES</span></span>

### <span data-ttu-id="71d50-114">Выход из текущей учетной записи</span><span class="sxs-lookup"><span data-stu-id="71d50-114">Logout of the current account</span></span>
```
PS C:\> Disconnect-AzureRmAccount
```

<span data-ttu-id="71d50-115">Выполнит выход из учетной записи Azure, связанной с текущим контекстом.</span><span class="sxs-lookup"><span data-stu-id="71d50-115">Logs out of the Azure account associated with the current context.</span></span>

### <span data-ttu-id="71d50-116">Выход из учетной записи, связанной с определенным контекстом</span><span class="sxs-lookup"><span data-stu-id="71d50-116">Logout of the account associated with a particular context</span></span>
```
PS C:\> Get-AzureRmContext "Work" | Disconnect-AzureRmAccount -Scope CurrentUser
```

<span data-ttu-id="71d50-117">Выход из учетной записи, связанной с указанным контекстом (с именем "трудозатраты").</span><span class="sxs-lookup"><span data-stu-id="71d50-117">Logs out the account associated with the given context (named 'Work').</span></span> <span data-ttu-id="71d50-118">Так как в этом случае используется область "CurrentUser", все учетные данные и контексты удаляются без возможности восстановления.</span><span class="sxs-lookup"><span data-stu-id="71d50-118">Because this uses the 'CurrentUser' scope, all credentials and contexts will be permanently deleted.</span></span>

### <span data-ttu-id="71d50-119">Выход определенного пользователя</span><span class="sxs-lookup"><span data-stu-id="71d50-119">Log out a particular user</span></span>
```
PS C:\> Disconnect-AzureRmAccount -Username 'user1@contoso.org'
```

<span data-ttu-id="71d50-120">Выход из учетной user1@contoso.org записи "пользователь: все учетные данные и все контексты, связанные с этим пользователем, будут удалены.</span><span class="sxs-lookup"><span data-stu-id="71d50-120">Logs out the 'user1@contoso.org' user - all credentials and all contexts associated with this user will be removed.</span></span>

## <span data-ttu-id="71d50-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="71d50-121">PARAMETERS</span></span>

### <span data-ttu-id="71d50-122">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="71d50-122">-ApplicationId</span></span>
<span data-ttu-id="71d50-123">Идентификатор ServicePrincipal (глобальный уникальный идентификатор)</span><span class="sxs-lookup"><span data-stu-id="71d50-123">ServicePrincipal id (globally unique id)</span></span>

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

### <span data-ttu-id="71d50-124">-AzureContext</span><span class="sxs-lookup"><span data-stu-id="71d50-124">-AzureContext</span></span>
<span data-ttu-id="71d50-125">Context</span><span class="sxs-lookup"><span data-stu-id="71d50-125">Context</span></span>

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

### <span data-ttu-id="71d50-126">-ContextName</span><span class="sxs-lookup"><span data-stu-id="71d50-126">-ContextName</span></span>
<span data-ttu-id="71d50-127">Имя контекста для выхода из</span><span class="sxs-lookup"><span data-stu-id="71d50-127">Name of the context to log out of</span></span>

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

### <span data-ttu-id="71d50-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71d50-128">-DefaultProfile</span></span>
<span data-ttu-id="71d50-129">Учетные данные, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="71d50-129">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="71d50-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="71d50-130">-InputObject</span></span>
<span data-ttu-id="71d50-131">Удаляемый объект учетной записи</span><span class="sxs-lookup"><span data-stu-id="71d50-131">The account object to remove</span></span>

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

### <span data-ttu-id="71d50-132">-Scope</span><span class="sxs-lookup"><span data-stu-id="71d50-132">-Scope</span></span>
<span data-ttu-id="71d50-133">Определяет область изменений контекста, например, применяются ли изменения только к текущему процессу или ко всем сеансам, запускаемым этим пользователем.</span><span class="sxs-lookup"><span data-stu-id="71d50-133">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="71d50-134">-TenantId</span><span class="sxs-lookup"><span data-stu-id="71d50-134">-TenantId</span></span>
<span data-ttu-id="71d50-135">Идентификатор клиента (глобальный уникальный идентификатор)</span><span class="sxs-lookup"><span data-stu-id="71d50-135">Tenant id (globally unique id)</span></span>

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

### <span data-ttu-id="71d50-136">-Username</span><span class="sxs-lookup"><span data-stu-id="71d50-136">-Username</span></span>
<span data-ttu-id="71d50-137">Имя пользователя в форме " user@contoso.org "</span><span class="sxs-lookup"><span data-stu-id="71d50-137">User name of the form 'user@contoso.org'</span></span>

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

### <span data-ttu-id="71d50-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="71d50-138">-Confirm</span></span>
<span data-ttu-id="71d50-139">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="71d50-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71d50-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71d50-140">-WhatIf</span></span>
<span data-ttu-id="71d50-141">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="71d50-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71d50-142">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="71d50-142">The cmdlet is not executed.</span></span>

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

### <span data-ttu-id="71d50-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71d50-143">CommonParameters</span></span>
<span data-ttu-id="71d50-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="71d50-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71d50-145">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71d50-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71d50-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="71d50-146">INPUTS</span></span>

### <span data-ttu-id="71d50-147">Microsoft. Azure. Commands. Profile. Models. PSAzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="71d50-147">Microsoft.Azure.Commands.Profile.Models.PSAzureRmAccount</span></span>
<span data-ttu-id="71d50-148">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="71d50-148">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="71d50-149">Microsoft. Azure. Commands. Profile. Models. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="71d50-149">Microsoft.Azure.Commands.Profile.Models.PSAzureContext</span></span>
<span data-ttu-id="71d50-150">Параметры: AzureContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="71d50-150">Parameters: AzureContext (ByValue)</span></span>

## <span data-ttu-id="71d50-151">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="71d50-151">OUTPUTS</span></span>

### <span data-ttu-id="71d50-152">Microsoft. Azure. Commands. Profile. Models. PSAzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="71d50-152">Microsoft.Azure.Commands.Profile.Models.PSAzureRmAccount</span></span>

## <span data-ttu-id="71d50-153">Пуск</span><span class="sxs-lookup"><span data-stu-id="71d50-153">NOTES</span></span>

## <span data-ttu-id="71d50-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="71d50-154">RELATED LINKS</span></span>

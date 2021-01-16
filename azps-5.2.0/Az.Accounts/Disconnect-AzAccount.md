---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/disconnect-azaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disconnect-AzAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disconnect-AzAccount.md
ms.openlocfilehash: 23689d4e84228d4eaeaae82e2efe53b6450d44f9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98393279"
---
# <span data-ttu-id="e7f9c-101">Disconnect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="e7f9c-101">Disconnect-AzAccount</span></span>

## <span data-ttu-id="e7f9c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7f9c-102">SYNOPSIS</span></span>
<span data-ttu-id="e7f9c-103">Отключает подключенную учетную запись Azure и удаляет все учетные данные и контексты, связанные с ней.</span><span class="sxs-lookup"><span data-stu-id="e7f9c-103">Disconnects a connected Azure account and removes all credentials and contexts associated with that account.</span></span>

## <span data-ttu-id="e7f9c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e7f9c-104">SYNTAX</span></span>

### <span data-ttu-id="e7f9c-105">Имя Контекста (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e7f9c-105">ContextName (Default)</span></span>
```
Disconnect-AzAccount [-ContextName <String>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7f9c-106">UserId</span><span class="sxs-lookup"><span data-stu-id="e7f9c-106">UserId</span></span>
```
Disconnect-AzAccount [-Username] <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7f9c-107">ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="e7f9c-107">ServicePrincipal</span></span>
```
Disconnect-AzAccount -ApplicationId <String> -TenantId <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7f9c-108">AccountObject</span><span class="sxs-lookup"><span data-stu-id="e7f9c-108">AccountObject</span></span>
```
Disconnect-AzAccount [-InputObject] <PSAzureRmAccount> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7f9c-109">ContextObject</span><span class="sxs-lookup"><span data-stu-id="e7f9c-109">ContextObject</span></span>
```
Disconnect-AzAccount [-AzureContext] <PSAzureContext> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7f9c-110">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e7f9c-110">DESCRIPTION</span></span>
<span data-ttu-id="e7f9c-111">Новый Disconnect-AzAccount отключает подключенную учетную запись Azure и удаляет все учетные данные и контексты (сведения о подписке и клиенте), связанные с ней.</span><span class="sxs-lookup"><span data-stu-id="e7f9c-111">The Disconnect-AzAccount cmdlet disconnects a connected Azure account and removes all credentials and contexts (subscription and tenant information) associated with that account.</span></span>
<span data-ttu-id="e7f9c-112">После выполнения этого cmdlet вам потребуется повторно войти с помощью Connect-AzAccount.</span><span class="sxs-lookup"><span data-stu-id="e7f9c-112">After executing this cmdlet, you will need to login again using Connect-AzAccount.</span></span>

## <span data-ttu-id="e7f9c-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e7f9c-113">EXAMPLES</span></span>

### <span data-ttu-id="e7f9c-114">Пример 1. Выйдите из текущей учетной записи</span><span class="sxs-lookup"><span data-stu-id="e7f9c-114">Example 1: Logout of the current account</span></span>
```powershell
PS C:\> Disconnect-AzAccount
```

<span data-ttu-id="e7f9c-115">Выход из учетной записи Azure, связанной с текущим контекстом.</span><span class="sxs-lookup"><span data-stu-id="e7f9c-115">Logs out of the Azure account associated with the current context.</span></span>

### <span data-ttu-id="e7f9c-116">Пример 2. Выйдите из учетной записи, связанной с определенным контекстом</span><span class="sxs-lookup"><span data-stu-id="e7f9c-116">Example 2: Logout of the account associated with a particular context</span></span>
```powershell
PS C:\> Get-AzContext "Work" | Disconnect-AzAccount -Scope CurrentUser
```

<span data-ttu-id="e7f9c-117">Выйдите из учетной записи, связанной с заданным контекстом (с именем "Работа").</span><span class="sxs-lookup"><span data-stu-id="e7f9c-117">Logs out the account associated with the given context (named 'Work').</span></span> <span data-ttu-id="e7f9c-118">Так как используется область CurrentUser, все учетные данные и контексты будут удалены без возможности удаления.</span><span class="sxs-lookup"><span data-stu-id="e7f9c-118">Because this uses the 'CurrentUser' scope, all credentials and contexts will be permanently deleted.</span></span>

### <span data-ttu-id="e7f9c-119">Пример 3. Выход определенного пользователя из учетной записи</span><span class="sxs-lookup"><span data-stu-id="e7f9c-119">Example 3: Log out a particular user</span></span>
```powershell
PS C:\> Disconnect-AzAccount -Username 'user1@contoso.org'
```

<span data-ttu-id="e7f9c-120">Выйдите из учетной записи пользователя ' — все учетные данные и все контексты, связанные с этим пользователем, user1@contoso.org будут удалены.</span><span class="sxs-lookup"><span data-stu-id="e7f9c-120">Logs out the 'user1@contoso.org' user - all credentials and all contexts associated with this user will be removed.</span></span>

## <span data-ttu-id="e7f9c-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e7f9c-121">PARAMETERS</span></span>

### <span data-ttu-id="e7f9c-122">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="e7f9c-122">-ApplicationId</span></span>
<span data-ttu-id="e7f9c-123">ServicePrincipal id (глобальный уникальный id)</span><span class="sxs-lookup"><span data-stu-id="e7f9c-123">ServicePrincipal id (globally unique id)</span></span>

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

### <span data-ttu-id="e7f9c-124">-AzureContext</span><span class="sxs-lookup"><span data-stu-id="e7f9c-124">-AzureContext</span></span>
<span data-ttu-id="e7f9c-125">Контекст</span><span class="sxs-lookup"><span data-stu-id="e7f9c-125">Context</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext
Parameter Sets: ContextObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e7f9c-126">-ContextName</span><span class="sxs-lookup"><span data-stu-id="e7f9c-126">-ContextName</span></span>
<span data-ttu-id="e7f9c-127">Имя контекста, из которого нужно выйти</span><span class="sxs-lookup"><span data-stu-id="e7f9c-127">Name of the context to log out of</span></span>

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

### <span data-ttu-id="e7f9c-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7f9c-128">-DefaultProfile</span></span>
<span data-ttu-id="e7f9c-129">Учетные данные, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="e7f9c-129">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e7f9c-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e7f9c-130">-InputObject</span></span>
<span data-ttu-id="e7f9c-131">Удаляемый объект учетной записи</span><span class="sxs-lookup"><span data-stu-id="e7f9c-131">The account object to remove</span></span>

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

### <span data-ttu-id="e7f9c-132">-Scope</span><span class="sxs-lookup"><span data-stu-id="e7f9c-132">-Scope</span></span>
<span data-ttu-id="e7f9c-133">Определяет область изменения контекста, например, применяются ли изменения только к текущему процессу или же к всем сеансам, на которые начал пользователь.</span><span class="sxs-lookup"><span data-stu-id="e7f9c-133">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="e7f9c-134">-TenantId</span><span class="sxs-lookup"><span data-stu-id="e7f9c-134">-TenantId</span></span>
<span data-ttu-id="e7f9c-135">ИД клиента (глобальный уникальный id)</span><span class="sxs-lookup"><span data-stu-id="e7f9c-135">Tenant id (globally unique id)</span></span>

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

### <span data-ttu-id="e7f9c-136">-Username</span><span class="sxs-lookup"><span data-stu-id="e7f9c-136">-Username</span></span>
<span data-ttu-id="e7f9c-137">Имя пользователя формы user@contoso.org '</span><span class="sxs-lookup"><span data-stu-id="e7f9c-137">User name of the form 'user@contoso.org'</span></span>

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

### <span data-ttu-id="e7f9c-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e7f9c-138">-Confirm</span></span>
<span data-ttu-id="e7f9c-139">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="e7f9c-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7f9c-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7f9c-140">-WhatIf</span></span>
<span data-ttu-id="e7f9c-141">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e7f9c-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7f9c-142">Этот cmdlet не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e7f9c-142">The cmdlet is not executed.</span></span>

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

### <span data-ttu-id="e7f9c-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7f9c-143">CommonParameters</span></span>
<span data-ttu-id="e7f9c-144">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7f9c-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7f9c-145">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7f9c-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7f9c-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e7f9c-146">INPUTS</span></span>

### <span data-ttu-id="e7f9c-147">Microsoft.Azure.Commands.Profile.Models.PSAzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="e7f9c-147">Microsoft.Azure.Commands.Profile.Models.PSAzureRmAccount</span></span>

### <span data-ttu-id="e7f9c-148">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="e7f9c-148">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="e7f9c-149">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e7f9c-149">OUTPUTS</span></span>

### <span data-ttu-id="e7f9c-150">Microsoft.Azure.Commands.Profile.Models.PSAzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="e7f9c-150">Microsoft.Azure.Commands.Profile.Models.PSAzureRmAccount</span></span>

## <span data-ttu-id="e7f9c-151">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e7f9c-151">NOTES</span></span>

## <span data-ttu-id="e7f9c-152">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e7f9c-152">RELATED LINKS</span></span>

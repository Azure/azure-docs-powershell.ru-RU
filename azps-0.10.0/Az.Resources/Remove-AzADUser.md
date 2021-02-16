---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 9F9B2691-BB3F-4644-BD95-6D74777D1E99
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-Azaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzADUser.md
ms.openlocfilehash: e16adfe6db006af0c1f49992d5aff39412d4d4d3
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100398212"
---
# <span data-ttu-id="9a388-101">Remove-AzADUser</span><span class="sxs-lookup"><span data-stu-id="9a388-101">Remove-AzADUser</span></span>

## <span data-ttu-id="9a388-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a388-102">SYNOPSIS</span></span>
<span data-ttu-id="9a388-103">Удаляет активного пользователя каталога.</span><span class="sxs-lookup"><span data-stu-id="9a388-103">Deletes an active directory user.</span></span>

## <span data-ttu-id="9a388-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9a388-104">SYNTAX</span></span>

### <span data-ttu-id="9a388-105">UPNOrObjectIdParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9a388-105">UPNOrObjectIdParameterSet (Default)</span></span>
```
Remove-AzADUser -UPNOrObjectId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a388-106">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a388-106">UPNParameterSet</span></span>
```
Remove-AzADUser -UserPrincipalName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a388-107">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a388-107">ObjectIdParameterSet</span></span>
```
Remove-AzADUser -ObjectId <Guid> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a388-108">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a388-108">DisplayNameParameterSet</span></span>
```
Remove-AzADUser -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a388-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a388-109">InputObjectParameterSet</span></span>
```
Remove-AzADUser -InputObject <PSADUser> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a388-110">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9a388-110">DESCRIPTION</span></span>
<span data-ttu-id="9a388-111">Удаляет пользователя Active Directory (рабочий или учебный аккаунт, также известный как ид организации).</span><span class="sxs-lookup"><span data-stu-id="9a388-111">Deletes an active directory user (work/school account also popularly known as org-id).</span></span>

## <span data-ttu-id="9a388-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9a388-112">EXAMPLES</span></span>

### <span data-ttu-id="9a388-113">Пример 1. Удаление пользователя по имени пользователя</span><span class="sxs-lookup"><span data-stu-id="9a388-113">Example 1 - Remove a user by user principal name</span></span>

```
PS C:\> Remove-AzADUser -UserPrincipalName foo@domain.com
```

<span data-ttu-id="9a388-114">Удаляет пользователя с основным именем пользователя " foo@domain.com из клиента.</span><span class="sxs-lookup"><span data-stu-id="9a388-114">Removes the user with user principal name "foo@domain.com" from the tenant.</span></span>

### <span data-ttu-id="9a388-115">Пример 2. Удаление пользователя по ид объекта</span><span class="sxs-lookup"><span data-stu-id="9a388-115">Example 2 - Remove a user by object id</span></span>

```
PS C:\> Remove-AzADUser -ObjectId 7a9582cf-88c4-4319-842b-7a5d60967a69
```

<span data-ttu-id="9a388-116">Удаляет пользователя с ид объекта '7a9582cf-88c4-4319-842b-7a5d60967a69' из клиента.</span><span class="sxs-lookup"><span data-stu-id="9a388-116">Removes the user with object id '7a9582cf-88c4-4319-842b-7a5d60967a69' from the tenant.</span></span>

### <span data-ttu-id="9a388-117">Пример 3. Удаление пользователя с помощью piping</span><span class="sxs-lookup"><span data-stu-id="9a388-117">Example 3 - Remove a user by piping</span></span>

```
PS C:\> Get-AzADUser -ObjectId 7a9582cf-88c4-4319-842b-7a5d60967a69 | Remove-AzADUser
```

<span data-ttu-id="9a388-118">Возвращает пользователя с объектным ид '7a9582cf-88c4-4319-842b-7a5d60967a69' и каналами, которые можно Remove-AzADUser, чтобы удалить пользователя из клиента.</span><span class="sxs-lookup"><span data-stu-id="9a388-118">Gets the user with object id '7a9582cf-88c4-4319-842b-7a5d60967a69' and pipes that to the Remove-AzADUser cmdlet to remove the user from the tenant.</span></span>

## <span data-ttu-id="9a388-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9a388-119">PARAMETERS</span></span>

### <span data-ttu-id="9a388-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a388-120">-DefaultProfile</span></span>
<span data-ttu-id="9a388-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="9a388-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a388-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="9a388-122">-DisplayName</span></span>
<span data-ttu-id="9a388-123">Отображаемая имя удаляемого пользователя.</span><span class="sxs-lookup"><span data-stu-id="9a388-123">The display name of the user to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a388-124">-Force</span><span class="sxs-lookup"><span data-stu-id="9a388-124">-Force</span></span>
<span data-ttu-id="9a388-125">При этом не запросить подтверждение удаления пользователя.</span><span class="sxs-lookup"><span data-stu-id="9a388-125">If specified, doesn't ask for confirmation for deleting the user.</span></span>

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

### <span data-ttu-id="9a388-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9a388-126">-InputObject</span></span>
<span data-ttu-id="9a388-127">Удаляемый объект пользователя.</span><span class="sxs-lookup"><span data-stu-id="9a388-127">The user object to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9a388-128">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="9a388-128">-ObjectId</span></span>
<span data-ttu-id="9a388-129">ИД объекта пользователя, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="9a388-129">The object id of the user to be deleted.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a388-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9a388-130">-PassThru</span></span>
<span data-ttu-id="9a388-131">Если эта команда была успешной, ее можно указать как истина.</span><span class="sxs-lookup"><span data-stu-id="9a388-131">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="9a388-132">-UPNOrObjectId</span><span class="sxs-lookup"><span data-stu-id="9a388-132">-UPNOrObjectId</span></span>
<span data-ttu-id="9a388-133">Имя пользователя или objectId удаляемого пользователя.</span><span class="sxs-lookup"><span data-stu-id="9a388-133">The user principal name or the objectId of the user to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: UPNOrObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a388-134">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="9a388-134">-UserPrincipalName</span></span>
<span data-ttu-id="9a388-135">Имя пользователя, которого нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="9a388-135">The user principal name of the user to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: UPNParameterSet
Aliases: UPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a388-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9a388-136">-Confirm</span></span>
<span data-ttu-id="9a388-137">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="9a388-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a388-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a388-138">-WhatIf</span></span>
<span data-ttu-id="9a388-139">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9a388-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a388-140">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="9a388-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a388-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a388-141">CommonParameters</span></span>
<span data-ttu-id="9a388-142">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a388-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a388-143">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a388-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a388-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9a388-144">INPUTS</span></span>

### <span data-ttu-id="9a388-145">System.String</span><span class="sxs-lookup"><span data-stu-id="9a388-145">System.String</span></span>

### <span data-ttu-id="9a388-146">System.Guid</span><span class="sxs-lookup"><span data-stu-id="9a388-146">System.Guid</span></span>

### <span data-ttu-id="9a388-147">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span><span class="sxs-lookup"><span data-stu-id="9a388-147">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>
<span data-ttu-id="9a388-148">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="9a388-148">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="9a388-149">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9a388-149">OUTPUTS</span></span>

### <span data-ttu-id="9a388-150">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9a388-150">System.Boolean</span></span>

## <span data-ttu-id="9a388-151">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9a388-151">NOTES</span></span>

## <span data-ttu-id="9a388-152">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9a388-152">RELATED LINKS</span></span>

[<span data-ttu-id="9a388-153">New-AzADUser</span><span class="sxs-lookup"><span data-stu-id="9a388-153">New-AzADUser</span></span>](./New-AzADUser.md)

[<span data-ttu-id="9a388-154">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="9a388-154">Get-AzADUser</span></span>](./Get-AzADUser.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 9F9B2691-BB3F-4644-BD95-6D74777D1E99
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADUser.md
ms.openlocfilehash: 39413c8279b84bb75d3e86bbf41ff40afe05ad06
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100220457"
---
# <span data-ttu-id="4cecd-101">Remove-AzADUser</span><span class="sxs-lookup"><span data-stu-id="4cecd-101">Remove-AzADUser</span></span>

## <span data-ttu-id="4cecd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4cecd-102">SYNOPSIS</span></span>
<span data-ttu-id="4cecd-103">Удаляет активного пользователя каталога.</span><span class="sxs-lookup"><span data-stu-id="4cecd-103">Deletes an active directory user.</span></span>

## <span data-ttu-id="4cecd-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4cecd-104">SYNTAX</span></span>

### <span data-ttu-id="4cecd-105">UPNOrObjectIdParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4cecd-105">UPNOrObjectIdParameterSet (Default)</span></span>
```
Remove-AzADUser -UPNOrObjectId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4cecd-106">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="4cecd-106">UPNParameterSet</span></span>
```
Remove-AzADUser -UserPrincipalName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4cecd-107">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4cecd-107">ObjectIdParameterSet</span></span>
```
Remove-AzADUser -ObjectId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4cecd-108">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="4cecd-108">DisplayNameParameterSet</span></span>
```
Remove-AzADUser -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4cecd-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4cecd-109">InputObjectParameterSet</span></span>
```
Remove-AzADUser -InputObject <PSADUser> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4cecd-110">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4cecd-110">DESCRIPTION</span></span>
<span data-ttu-id="4cecd-111">Удаляет пользователя Active Directory (рабочий или учебный аккаунт, также известный как ид организации).</span><span class="sxs-lookup"><span data-stu-id="4cecd-111">Deletes an active directory user (work/school account also popularly known as org-id).</span></span>

## <span data-ttu-id="4cecd-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4cecd-112">EXAMPLES</span></span>

### <span data-ttu-id="4cecd-113">Пример 1. Удаление пользователя по имени директора-пользователя</span><span class="sxs-lookup"><span data-stu-id="4cecd-113">Example 1: Remove a user by user principal name</span></span>

```powershell
PS C:\> Remove-AzADUser -UserPrincipalName foo@domain.com
```

<span data-ttu-id="4cecd-114">Удаляет пользователя с основным именем пользователя " foo@domain.com из клиента.</span><span class="sxs-lookup"><span data-stu-id="4cecd-114">Removes the user with user principal name "foo@domain.com" from the tenant.</span></span>

### <span data-ttu-id="4cecd-115">Пример 2. Удаление пользователя по ид объекта</span><span class="sxs-lookup"><span data-stu-id="4cecd-115">Example 2: Remove a user by object id</span></span>

```powershell
PS C:\> Remove-AzADUser -ObjectId 7a9582cf-88c4-4319-842b-7a5d60967a69
```

<span data-ttu-id="4cecd-116">Удаляет пользователя с ид объекта '7a9582cf-88c4-4319-842b-7a5d60967a69' из клиента.</span><span class="sxs-lookup"><span data-stu-id="4cecd-116">Removes the user with object id '7a9582cf-88c4-4319-842b-7a5d60967a69' from the tenant.</span></span>

### <span data-ttu-id="4cecd-117">Пример 3. Удаление пользователя с помощью piping</span><span class="sxs-lookup"><span data-stu-id="4cecd-117">Example 3: Remove a user by piping</span></span>

```powershell
PS C:\> Get-AzADUser -ObjectId 7a9582cf-88c4-4319-842b-7a5d60967a69 | Remove-AzADUser
```

<span data-ttu-id="4cecd-118">Возвращает пользователя с объектным ид '7a9582cf-88c4-4319-842b-7a5d60967a69' и каналами, которые Remove-AzADUser к этому Remove-AzADUser, чтобы удалить пользователя из клиента.</span><span class="sxs-lookup"><span data-stu-id="4cecd-118">Gets the user with object id '7a9582cf-88c4-4319-842b-7a5d60967a69' and pipes that to the Remove-AzADUser cmdlet to remove the user from the tenant.</span></span>

## <span data-ttu-id="4cecd-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4cecd-119">PARAMETERS</span></span>

### <span data-ttu-id="4cecd-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cecd-120">-DefaultProfile</span></span>
<span data-ttu-id="4cecd-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="4cecd-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4cecd-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="4cecd-122">-DisplayName</span></span>
<span data-ttu-id="4cecd-123">Отображаемая имя удаляемого пользователя.</span><span class="sxs-lookup"><span data-stu-id="4cecd-123">The display name of the user to be deleted.</span></span>

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

### <span data-ttu-id="4cecd-124">-Force</span><span class="sxs-lookup"><span data-stu-id="4cecd-124">-Force</span></span>
<span data-ttu-id="4cecd-125">При этом не запросить подтверждение удаления пользователя.</span><span class="sxs-lookup"><span data-stu-id="4cecd-125">If specified, doesn't ask for confirmation for deleting the user.</span></span>

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

### <span data-ttu-id="4cecd-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4cecd-126">-InputObject</span></span>
<span data-ttu-id="4cecd-127">Удаляемый объект пользователя.</span><span class="sxs-lookup"><span data-stu-id="4cecd-127">The user object to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADUser
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4cecd-128">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="4cecd-128">-ObjectId</span></span>
<span data-ttu-id="4cecd-129">ИД объекта пользователя, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="4cecd-129">The object id of the user to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4cecd-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4cecd-130">-PassThru</span></span>
<span data-ttu-id="4cecd-131">Если эта команда была успешной, ее можно указать как истина.</span><span class="sxs-lookup"><span data-stu-id="4cecd-131">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="4cecd-132">-UPNOrObjectId</span><span class="sxs-lookup"><span data-stu-id="4cecd-132">-UPNOrObjectId</span></span>
<span data-ttu-id="4cecd-133">Имя пользователя или objectId удаляемого пользователя.</span><span class="sxs-lookup"><span data-stu-id="4cecd-133">The user principal name or the objectId of the user to be deleted.</span></span>

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

### <span data-ttu-id="4cecd-134">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="4cecd-134">-UserPrincipalName</span></span>
<span data-ttu-id="4cecd-135">Имя пользователя, которого нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="4cecd-135">The user principal name of the user to be deleted.</span></span>

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

### <span data-ttu-id="4cecd-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4cecd-136">-Confirm</span></span>
<span data-ttu-id="4cecd-137">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4cecd-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4cecd-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4cecd-138">-WhatIf</span></span>
<span data-ttu-id="4cecd-139">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4cecd-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4cecd-140">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="4cecd-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4cecd-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cecd-141">CommonParameters</span></span>
<span data-ttu-id="4cecd-142">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4cecd-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cecd-143">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4cecd-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cecd-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4cecd-144">INPUTS</span></span>

### <span data-ttu-id="4cecd-145">System.String</span><span class="sxs-lookup"><span data-stu-id="4cecd-145">System.String</span></span>

### <span data-ttu-id="4cecd-146">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span><span class="sxs-lookup"><span data-stu-id="4cecd-146">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="4cecd-147">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4cecd-147">OUTPUTS</span></span>

### <span data-ttu-id="4cecd-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4cecd-148">System.Boolean</span></span>

## <span data-ttu-id="4cecd-149">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4cecd-149">NOTES</span></span>

## <span data-ttu-id="4cecd-150">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4cecd-150">RELATED LINKS</span></span>

[<span data-ttu-id="4cecd-151">New-AzADUser</span><span class="sxs-lookup"><span data-stu-id="4cecd-151">New-AzADUser</span></span>](./New-AzADUser.md)

[<span data-ttu-id="4cecd-152">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="4cecd-152">Get-AzADUser</span></span>](./Get-AzADUser.md)

[<span data-ttu-id="4cecd-153">Update-AzADUser</span><span class="sxs-lookup"><span data-stu-id="4cecd-153">Update-AzADUser</span></span>](./Update-AzADUser.md)


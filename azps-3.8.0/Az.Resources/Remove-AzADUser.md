---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 9F9B2691-BB3F-4644-BD95-6D74777D1E99
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADUser.md
ms.openlocfilehash: f05acfb05e9cd60616e243e36da406477e8d9d03
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912150"
---
# <span data-ttu-id="7fb9a-101">Remove-AzADUser</span><span class="sxs-lookup"><span data-stu-id="7fb9a-101">Remove-AzADUser</span></span>

## <span data-ttu-id="7fb9a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7fb9a-102">SYNOPSIS</span></span>
<span data-ttu-id="7fb9a-103">Удаляет пользователя Active Directory.</span><span class="sxs-lookup"><span data-stu-id="7fb9a-103">Deletes an active directory user.</span></span>

## <span data-ttu-id="7fb9a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7fb9a-104">SYNTAX</span></span>

### <span data-ttu-id="7fb9a-105">UPNOrObjectIdParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7fb9a-105">UPNOrObjectIdParameterSet (Default)</span></span>
```
Remove-AzADUser -UPNOrObjectId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7fb9a-106">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="7fb9a-106">UPNParameterSet</span></span>
```
Remove-AzADUser -UserPrincipalName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7fb9a-107">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7fb9a-107">ObjectIdParameterSet</span></span>
```
Remove-AzADUser -ObjectId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7fb9a-108">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7fb9a-108">DisplayNameParameterSet</span></span>
```
Remove-AzADUser -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7fb9a-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7fb9a-109">InputObjectParameterSet</span></span>
```
Remove-AzADUser -InputObject <PSADUser> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7fb9a-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7fb9a-110">DESCRIPTION</span></span>
<span data-ttu-id="7fb9a-111">Удаление пользователя Active Directory (рабочей или учебной учетной записи, известной как "org-ID").</span><span class="sxs-lookup"><span data-stu-id="7fb9a-111">Deletes an active directory user (work/school account also popularly known as org-id).</span></span>

## <span data-ttu-id="7fb9a-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7fb9a-112">EXAMPLES</span></span>

### <span data-ttu-id="7fb9a-113">Пример 1: Удаление пользователя по имени субъекта-пользователя</span><span class="sxs-lookup"><span data-stu-id="7fb9a-113">Example 1 - Remove a user by user principal name</span></span>

```
PS C:\> Remove-AzADUser -UserPrincipalName foo@domain.com
```

<span data-ttu-id="7fb9a-114">Удаляет пользователя с именем участника-пользователя " foo@domain.com " из клиента.</span><span class="sxs-lookup"><span data-stu-id="7fb9a-114">Removes the user with user principal name "foo@domain.com" from the tenant.</span></span>

### <span data-ttu-id="7fb9a-115">Пример 2: Удаление пользователя по идентификатору объекта</span><span class="sxs-lookup"><span data-stu-id="7fb9a-115">Example 2 - Remove a user by object id</span></span>

```
PS C:\> Remove-AzADUser -ObjectId 7a9582cf-88c4-4319-842b-7a5d60967a69
```

<span data-ttu-id="7fb9a-116">Удаляет пользователя с идентификатором объекта "7a9582cf-88c4-4319-842b-7a5d60967a69" из клиента.</span><span class="sxs-lookup"><span data-stu-id="7fb9a-116">Removes the user with object id '7a9582cf-88c4-4319-842b-7a5d60967a69' from the tenant.</span></span>

### <span data-ttu-id="7fb9a-117">Пример 3. Удаление пользователя с помощью трубопроводов</span><span class="sxs-lookup"><span data-stu-id="7fb9a-117">Example 3 - Remove a user by piping</span></span>

```
PS C:\> Get-AzADUser -ObjectId 7a9582cf-88c4-4319-842b-7a5d60967a69 | Remove-AzADUser
```

<span data-ttu-id="7fb9a-118">Возвращает пользователя с идентификатором объекта "7a9582cf-88c4-4319-842b-7a5d60967a69" и каналами, которые должны быть удалены из клиента с помощью командлета Remove-AzADUser.</span><span class="sxs-lookup"><span data-stu-id="7fb9a-118">Gets the user with object id '7a9582cf-88c4-4319-842b-7a5d60967a69' and pipes that to the Remove-AzADUser cmdlet to remove the user from the tenant.</span></span>

## <span data-ttu-id="7fb9a-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7fb9a-119">PARAMETERS</span></span>

### <span data-ttu-id="7fb9a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fb9a-120">-DefaultProfile</span></span>
<span data-ttu-id="7fb9a-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="7fb9a-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7fb9a-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="7fb9a-122">-DisplayName</span></span>
<span data-ttu-id="7fb9a-123">Отображаемое имя пользователя, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="7fb9a-123">The display name of the user to be deleted.</span></span>

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

### <span data-ttu-id="7fb9a-124">-Force</span><span class="sxs-lookup"><span data-stu-id="7fb9a-124">-Force</span></span>
<span data-ttu-id="7fb9a-125">Если задано, не запрашивает подтверждение удаления пользователя.</span><span class="sxs-lookup"><span data-stu-id="7fb9a-125">If specified, doesn't ask for confirmation for deleting the user.</span></span>

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

### <span data-ttu-id="7fb9a-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7fb9a-126">-InputObject</span></span>
<span data-ttu-id="7fb9a-127">Объект пользователя, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="7fb9a-127">The user object to be deleted.</span></span>

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

### <span data-ttu-id="7fb9a-128">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="7fb9a-128">-ObjectId</span></span>
<span data-ttu-id="7fb9a-129">Идентификатор объекта пользователя, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="7fb9a-129">The object id of the user to be deleted.</span></span>

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

### <span data-ttu-id="7fb9a-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7fb9a-130">-PassThru</span></span>
<span data-ttu-id="7fb9a-131">Если указать это, будет возвращено значение истина, если команда была выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="7fb9a-131">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="7fb9a-132">-UPNOrObjectId</span><span class="sxs-lookup"><span data-stu-id="7fb9a-132">-UPNOrObjectId</span></span>
<span data-ttu-id="7fb9a-133">Имя субъекта-пользователя или ИД объекта пользователя, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="7fb9a-133">The user principal name or the objectId of the user to be deleted.</span></span>

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

### <span data-ttu-id="7fb9a-134">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="7fb9a-134">-UserPrincipalName</span></span>
<span data-ttu-id="7fb9a-135">Имя субъекта-пользователя удаляемого пользователя.</span><span class="sxs-lookup"><span data-stu-id="7fb9a-135">The user principal name of the user to be deleted.</span></span>

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

### <span data-ttu-id="7fb9a-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7fb9a-136">-Confirm</span></span>
<span data-ttu-id="7fb9a-137">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7fb9a-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7fb9a-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7fb9a-138">-WhatIf</span></span>
<span data-ttu-id="7fb9a-139">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7fb9a-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7fb9a-140">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7fb9a-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7fb9a-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fb9a-141">CommonParameters</span></span>
<span data-ttu-id="7fb9a-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7fb9a-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fb9a-143">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7fb9a-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fb9a-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7fb9a-144">INPUTS</span></span>

### <span data-ttu-id="7fb9a-145">System. String</span><span class="sxs-lookup"><span data-stu-id="7fb9a-145">System.String</span></span>

### <span data-ttu-id="7fb9a-146">Microsoft. Azure. Commands. ActiveDirectory. PSADUser</span><span class="sxs-lookup"><span data-stu-id="7fb9a-146">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="7fb9a-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7fb9a-147">OUTPUTS</span></span>

### <span data-ttu-id="7fb9a-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7fb9a-148">System.Boolean</span></span>

## <span data-ttu-id="7fb9a-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="7fb9a-149">NOTES</span></span>

## <span data-ttu-id="7fb9a-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7fb9a-150">RELATED LINKS</span></span>

[<span data-ttu-id="7fb9a-151">New-AzADUser</span><span class="sxs-lookup"><span data-stu-id="7fb9a-151">New-AzADUser</span></span>](./New-AzADUser.md)

[<span data-ttu-id="7fb9a-152">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="7fb9a-152">Get-AzADUser</span></span>](./Get-AzADUser.md)

[<span data-ttu-id="7fb9a-153">Set-AzADUser</span><span class="sxs-lookup"><span data-stu-id="7fb9a-153">Set-AzADUser</span></span>](./Set-AzADUser.md)


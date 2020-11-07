---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 9F9B2691-BB3F-4644-BD95-6D74777D1E99
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADUser.md
ms.openlocfilehash: 1b863b0bc9cb90caca4d7431ec6835cb75836609
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733809"
---
# <span data-ttu-id="61d94-101">Remove-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="61d94-101">Remove-AzureRmADUser</span></span>

## <span data-ttu-id="61d94-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="61d94-102">SYNOPSIS</span></span>
<span data-ttu-id="61d94-103">Удаляет пользователя Active Directory.</span><span class="sxs-lookup"><span data-stu-id="61d94-103">Deletes an active directory user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="61d94-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="61d94-104">SYNTAX</span></span>

### <span data-ttu-id="61d94-105">UPNOrObjectIdParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="61d94-105">UPNOrObjectIdParameterSet (Default)</span></span>
```
Remove-AzureRmADUser -UPNOrObjectId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61d94-106">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="61d94-106">UPNParameterSet</span></span>
```
Remove-AzureRmADUser -UserPrincipalName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61d94-107">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="61d94-107">ObjectIdParameterSet</span></span>
```
Remove-AzureRmADUser -ObjectId <Guid> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61d94-108">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="61d94-108">DisplayNameParameterSet</span></span>
```
Remove-AzureRmADUser -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61d94-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="61d94-109">InputObjectParameterSet</span></span>
```
Remove-AzureRmADUser -InputObject <PSADUser> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61d94-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="61d94-110">DESCRIPTION</span></span>
<span data-ttu-id="61d94-111">Удаление пользователя Active Directory (рабочей или учебной учетной записи, известной как "org-ID").</span><span class="sxs-lookup"><span data-stu-id="61d94-111">Deletes an active directory user (work/school account also popularly known as org-id).</span></span>

## <span data-ttu-id="61d94-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="61d94-112">EXAMPLES</span></span>

### <span data-ttu-id="61d94-113">Пример 1: Удаление пользователя по имени субъекта-пользователя</span><span class="sxs-lookup"><span data-stu-id="61d94-113">Example 1 - Remove a user by user principal name</span></span>

```
PS C:\> Remove-AzureRmADUser -UserPrincipalName foo@domain.com
```

<span data-ttu-id="61d94-114">Удаляет пользователя с именем участника-пользователя " foo@domain.com " из клиента.</span><span class="sxs-lookup"><span data-stu-id="61d94-114">Removes the user with user principal name "foo@domain.com" from the tenant.</span></span>

### <span data-ttu-id="61d94-115">Пример 2: Удаление пользователя по идентификатору объекта</span><span class="sxs-lookup"><span data-stu-id="61d94-115">Example 2 - Remove a user by object id</span></span>

```
PS C:\> Remove-AzureRmADUser -ObjectId 7a9582cf-88c4-4319-842b-7a5d60967a69
```

<span data-ttu-id="61d94-116">Удаляет пользователя с идентификатором объекта "7a9582cf-88c4-4319-842b-7a5d60967a69" из клиента.</span><span class="sxs-lookup"><span data-stu-id="61d94-116">Removes the user with object id '7a9582cf-88c4-4319-842b-7a5d60967a69' from the tenant.</span></span>

### <span data-ttu-id="61d94-117">Пример 3. Удаление пользователя с помощью трубопроводов</span><span class="sxs-lookup"><span data-stu-id="61d94-117">Example 3 - Remove a user by piping</span></span>

```
PS C:\> Get-AzureRmADUser -ObjectId 7a9582cf-88c4-4319-842b-7a5d60967a69 | Remove-AzureRmADUser
```

<span data-ttu-id="61d94-118">Возвращает пользователя с идентификатором объекта "7a9582cf-88c4-4319-842b-7a5d60967a69" и каналами, которые должны быть удалены из клиента с помощью командлета Remove-AzureRmADUser.</span><span class="sxs-lookup"><span data-stu-id="61d94-118">Gets the user with object id '7a9582cf-88c4-4319-842b-7a5d60967a69' and pipes that to the Remove-AzureRmADUser cmdlet to remove the user from the tenant.</span></span>

## <span data-ttu-id="61d94-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="61d94-119">PARAMETERS</span></span>

### <span data-ttu-id="61d94-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61d94-120">-DefaultProfile</span></span>
<span data-ttu-id="61d94-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="61d94-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="61d94-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="61d94-122">-DisplayName</span></span>
<span data-ttu-id="61d94-123">Отображаемое имя пользователя, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="61d94-123">The display name of the user to be deleted.</span></span>

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

### <span data-ttu-id="61d94-124">-Force</span><span class="sxs-lookup"><span data-stu-id="61d94-124">-Force</span></span>
<span data-ttu-id="61d94-125">Если задано, не запрашивает подтверждение удаления пользователя.</span><span class="sxs-lookup"><span data-stu-id="61d94-125">If specified, doesn't ask for confirmation for deleting the user.</span></span>

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

### <span data-ttu-id="61d94-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="61d94-126">-InputObject</span></span>
<span data-ttu-id="61d94-127">Объект пользователя, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="61d94-127">The user object to be deleted.</span></span>

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

### <span data-ttu-id="61d94-128">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="61d94-128">-ObjectId</span></span>
<span data-ttu-id="61d94-129">Идентификатор объекта пользователя, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="61d94-129">The object id of the user to be deleted.</span></span>

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

### <span data-ttu-id="61d94-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="61d94-130">-PassThru</span></span>
<span data-ttu-id="61d94-131">Если указать это, будет возвращено значение истина, если команда была выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="61d94-131">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="61d94-132">-UPNOrObjectId</span><span class="sxs-lookup"><span data-stu-id="61d94-132">-UPNOrObjectId</span></span>
<span data-ttu-id="61d94-133">Имя субъекта-пользователя или ИД объекта пользователя, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="61d94-133">The user principal name or the objectId of the user to be deleted.</span></span>

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

### <span data-ttu-id="61d94-134">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="61d94-134">-UserPrincipalName</span></span>
<span data-ttu-id="61d94-135">Имя субъекта-пользователя удаляемого пользователя.</span><span class="sxs-lookup"><span data-stu-id="61d94-135">The user principal name of the user to be deleted.</span></span>

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

### <span data-ttu-id="61d94-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="61d94-136">-Confirm</span></span>
<span data-ttu-id="61d94-137">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="61d94-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61d94-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61d94-138">-WhatIf</span></span>
<span data-ttu-id="61d94-139">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="61d94-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61d94-140">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="61d94-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61d94-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61d94-141">CommonParameters</span></span>
<span data-ttu-id="61d94-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="61d94-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61d94-143">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61d94-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61d94-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="61d94-144">INPUTS</span></span>

### <span data-ttu-id="61d94-145">System. String</span><span class="sxs-lookup"><span data-stu-id="61d94-145">System.String</span></span>

### <span data-ttu-id="61d94-146">System. GUID</span><span class="sxs-lookup"><span data-stu-id="61d94-146">System.Guid</span></span>

### <span data-ttu-id="61d94-147">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADUser</span><span class="sxs-lookup"><span data-stu-id="61d94-147">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>
<span data-ttu-id="61d94-148">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="61d94-148">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="61d94-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="61d94-149">OUTPUTS</span></span>

### <span data-ttu-id="61d94-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="61d94-150">System.Boolean</span></span>

## <span data-ttu-id="61d94-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="61d94-151">NOTES</span></span>

## <span data-ttu-id="61d94-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="61d94-152">RELATED LINKS</span></span>

[<span data-ttu-id="61d94-153">New-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="61d94-153">New-AzureRmADUser</span></span>](./New-AzureRmADUser.md)

[<span data-ttu-id="61d94-154">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="61d94-154">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)

[<span data-ttu-id="61d94-155">Set-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="61d94-155">Set-AzureRmADUser</span></span>](./Set-AzureRmADUser.md)


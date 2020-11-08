---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/update-azaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADUser.md
ms.openlocfilehash: b765e33479c6178d69fb670a2f18ef0169eadf35
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235869"
---
# <span data-ttu-id="1145d-101">Update-AzADUser</span><span class="sxs-lookup"><span data-stu-id="1145d-101">Update-AzADUser</span></span>

## <span data-ttu-id="1145d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1145d-102">SYNOPSIS</span></span>
<span data-ttu-id="1145d-103">Обновление существующего пользователя Active Directory.</span><span class="sxs-lookup"><span data-stu-id="1145d-103">Updates an existing active directory user.</span></span>

## <span data-ttu-id="1145d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1145d-104">SYNTAX</span></span>

### <span data-ttu-id="1145d-105">UPNOrObjectIdParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1145d-105">UPNOrObjectIdParameterSet (Default)</span></span>
```
Update-AzADUser -UPNOrObjectId <String> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1145d-106">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="1145d-106">UPNParameterSet</span></span>
```
Update-AzADUser -UserPrincipalName <String> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1145d-107">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1145d-107">ObjectIdParameterSet</span></span>
```
Update-AzADUser -ObjectId <String> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1145d-108">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1145d-108">InputObjectParameterSet</span></span>
```
Update-AzADUser -InputObject <PSADUser> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1145d-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1145d-109">DESCRIPTION</span></span>
<span data-ttu-id="1145d-110">Обновление существующего пользователя Active Directory (рабочей или учебной учетной записи, известной как "org-ID").</span><span class="sxs-lookup"><span data-stu-id="1145d-110">Updates an existing active directory user (work/school account also popularly known as org-id).</span></span>
<span data-ttu-id="1145d-111">Дополнительные сведения: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#UpdateUser</span><span class="sxs-lookup"><span data-stu-id="1145d-111">For more information: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#UpdateUser</span></span>

## <span data-ttu-id="1145d-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1145d-112">EXAMPLES</span></span>

### <span data-ttu-id="1145d-113">Пример 1: обновление отображаемого имени пользователя с помощью идентификатора объекта</span><span class="sxs-lookup"><span data-stu-id="1145d-113">Example 1: Update the display name of a user using object id</span></span>

```powershell
PS C:\> Update-AzADUser -ObjectId 155a5c10-93a9-4941-a0df-96d83ab5ab24 -DisplayName MyNewDisplayName
```

<span data-ttu-id="1145d-114">Обновляет отображаемое имя пользователя с идентификатором объекта "155a5c10-93a9-4941-a0df-96d83ab5ab24" и "MyNewDisplayName".</span><span class="sxs-lookup"><span data-stu-id="1145d-114">Updates the display name of the user with object id '155a5c10-93a9-4941-a0df-96d83ab5ab24' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="1145d-115">Пример 2: обновление отображаемого имени пользователя с помощью основного имени пользователя</span><span class="sxs-lookup"><span data-stu-id="1145d-115">Example 2: Update the display name of a user using user principal name</span></span>

```powershell
PS C:\> Update-AzADUser -UserPrincipalName foo@domain.com -DisplayName MyNewDisplayName
```

<span data-ttu-id="1145d-116">Обновляет отображаемое имя пользователя с именем участника-пользователя " foo@domain.com " MyNewDisplayName ".</span><span class="sxs-lookup"><span data-stu-id="1145d-116">Updates the display name of the user with user principal name 'foo@domain.com' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="1145d-117">Пример 3: обновление отображаемого имени пользователя с помощью трубопроводов</span><span class="sxs-lookup"><span data-stu-id="1145d-117">Example 3: Update the display name of a user using piping</span></span>

```powershell
PS C:\> Get-AzADUser -ObjectId 155a5c10-93a9-4941-a0df-96d83ab5ab24 | Update-AzADUser -DisplayName MyNewDisplayName
```

<span data-ttu-id="1145d-118">Возвращает пользователя с идентификатором объекта "155a5c10-93a9-4941-a0df-96d83ab5ab24" и каналами, которые должны использовать командлет Update-AzADUser для обновления отображаемого имени пользователя на "MyNewDisplayName".</span><span class="sxs-lookup"><span data-stu-id="1145d-118">Gets the user with object id '155a5c10-93a9-4941-a0df-96d83ab5ab24' and pipes that to the Update-AzADUser cmdlet to update the display name of that user to 'MyNewDisplayName'.</span></span>

## <span data-ttu-id="1145d-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1145d-119">PARAMETERS</span></span>

### <span data-ttu-id="1145d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1145d-120">-DefaultProfile</span></span>
<span data-ttu-id="1145d-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1145d-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1145d-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="1145d-122">-DisplayName</span></span>
<span data-ttu-id="1145d-123">Новое отображаемое имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="1145d-123">New display name for the user.</span></span>

```yaml
Type: System.String
Parameter Sets: UPNOrObjectIdParameterSet, UPNParameterSet, ObjectIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1145d-124">-EnableAccount</span><span class="sxs-lookup"><span data-stu-id="1145d-124">-EnableAccount</span></span>
<span data-ttu-id="1145d-125">значение true для включения учетной записи; в противном случае — значение false.</span><span class="sxs-lookup"><span data-stu-id="1145d-125">true for enabling the account; otherwise, false.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: UPNOrObjectIdParameterSet, UPNParameterSet, ObjectIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: InputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1145d-126">-ForceChangePasswordNextLogin</span><span class="sxs-lookup"><span data-stu-id="1145d-126">-ForceChangePasswordNextLogin</span></span>
<span data-ttu-id="1145d-127">Он должен быть указан, если пользователь должен сменить пароль при следующем успешном входе.</span><span class="sxs-lookup"><span data-stu-id="1145d-127">It must be specified if the user should change the password on the next successful login.</span></span>
<span data-ttu-id="1145d-128">Только в том случае, если пароль обновлен, в противном случае он будет игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="1145d-128">Only valid if password is updated otherwise it will be ignored.</span></span>

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

### <span data-ttu-id="1145d-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1145d-129">-InputObject</span></span>
<span data-ttu-id="1145d-130">Объект, представляющий пользователя, которого нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="1145d-130">The object representing the user to be updated.</span></span>

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

### <span data-ttu-id="1145d-131">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="1145d-131">-ObjectId</span></span>
<span data-ttu-id="1145d-132">Идентификатор объекта пользователя, который необходимо обновить.</span><span class="sxs-lookup"><span data-stu-id="1145d-132">The object id of the user to be updated.</span></span>

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

### <span data-ttu-id="1145d-133">-Password (пароль)</span><span class="sxs-lookup"><span data-stu-id="1145d-133">-Password</span></span>
<span data-ttu-id="1145d-134">Новый пароль пользователя.</span><span class="sxs-lookup"><span data-stu-id="1145d-134">New password for the user.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: UPNOrObjectIdParameterSet, UPNParameterSet, ObjectIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Security.SecureString
Parameter Sets: InputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1145d-135">-UPNOrObjectId</span><span class="sxs-lookup"><span data-stu-id="1145d-135">-UPNOrObjectId</span></span>
<span data-ttu-id="1145d-136">Имя участника-пользователя или код объекта пользователя, который нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="1145d-136">The user principal name or object id of the user to be updated.</span></span>

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

### <span data-ttu-id="1145d-137">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="1145d-137">-UserPrincipalName</span></span>
<span data-ttu-id="1145d-138">Имя субъекта-пользователя для обновляемого пользователя.</span><span class="sxs-lookup"><span data-stu-id="1145d-138">The user principal name of the user to be updated.</span></span>

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

### <span data-ttu-id="1145d-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1145d-139">-Confirm</span></span>
<span data-ttu-id="1145d-140">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1145d-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1145d-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1145d-141">-WhatIf</span></span>
<span data-ttu-id="1145d-142">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1145d-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1145d-143">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1145d-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1145d-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1145d-144">CommonParameters</span></span>
<span data-ttu-id="1145d-145">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1145d-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1145d-146">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1145d-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1145d-147">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1145d-147">INPUTS</span></span>

### <span data-ttu-id="1145d-148">System. String</span><span class="sxs-lookup"><span data-stu-id="1145d-148">System.String</span></span>

### <span data-ttu-id="1145d-149">Microsoft. Azure. Commands. ActiveDirectory. PSADUser</span><span class="sxs-lookup"><span data-stu-id="1145d-149">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span></span>

### <span data-ttu-id="1145d-150">System. Nullable "1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="1145d-150">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="1145d-151">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="1145d-151">System.Security.SecureString</span></span>

## <span data-ttu-id="1145d-152">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1145d-152">OUTPUTS</span></span>

### <span data-ttu-id="1145d-153">Microsoft. Azure. Commands. ActiveDirectory. PSADUser</span><span class="sxs-lookup"><span data-stu-id="1145d-153">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="1145d-154">Пуск</span><span class="sxs-lookup"><span data-stu-id="1145d-154">NOTES</span></span>

## <span data-ttu-id="1145d-155">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1145d-155">RELATED LINKS</span></span>

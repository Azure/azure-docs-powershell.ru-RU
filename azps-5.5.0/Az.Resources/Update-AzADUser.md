---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/update-azaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADUser.md
ms.openlocfilehash: b765e33479c6178d69fb670a2f18ef0169eadf35
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100240021"
---
# <span data-ttu-id="39fc4-101">Update-AzADUser</span><span class="sxs-lookup"><span data-stu-id="39fc4-101">Update-AzADUser</span></span>

## <span data-ttu-id="39fc4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39fc4-102">SYNOPSIS</span></span>
<span data-ttu-id="39fc4-103">Обновляет существующего пользователя active directory.</span><span class="sxs-lookup"><span data-stu-id="39fc4-103">Updates an existing active directory user.</span></span>

## <span data-ttu-id="39fc4-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="39fc4-104">SYNTAX</span></span>

### <span data-ttu-id="39fc4-105">UPNOrObjectIdParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="39fc4-105">UPNOrObjectIdParameterSet (Default)</span></span>
```
Update-AzADUser -UPNOrObjectId <String> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39fc4-106">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="39fc4-106">UPNParameterSet</span></span>
```
Update-AzADUser -UserPrincipalName <String> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39fc4-107">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="39fc4-107">ObjectIdParameterSet</span></span>
```
Update-AzADUser -ObjectId <String> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39fc4-108">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="39fc4-108">InputObjectParameterSet</span></span>
```
Update-AzADUser -InputObject <PSADUser> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="39fc4-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="39fc4-109">DESCRIPTION</span></span>
<span data-ttu-id="39fc4-110">Обновляет существующего пользователя Active Directory (рабочий или учебный аккаунт, также известный как ид организации).</span><span class="sxs-lookup"><span data-stu-id="39fc4-110">Updates an existing active directory user (work/school account also popularly known as org-id).</span></span>
<span data-ttu-id="39fc4-111">Дополнительные сведения https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#UpdateUser</span><span class="sxs-lookup"><span data-stu-id="39fc4-111">For more information: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#UpdateUser</span></span>

## <span data-ttu-id="39fc4-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="39fc4-112">EXAMPLES</span></span>

### <span data-ttu-id="39fc4-113">Пример 1. Обновление отображаемого имени пользователя с помощью ид объекта</span><span class="sxs-lookup"><span data-stu-id="39fc4-113">Example 1: Update the display name of a user using object id</span></span>

```powershell
PS C:\> Update-AzADUser -ObjectId 155a5c10-93a9-4941-a0df-96d83ab5ab24 -DisplayName MyNewDisplayName
```

<span data-ttu-id="39fc4-114">Отображает имя пользователя с ид объекта "155a5c10-93a9-4941-a0df-96d83ab5ab24" на "MyNewDisplayName".</span><span class="sxs-lookup"><span data-stu-id="39fc4-114">Updates the display name of the user with object id '155a5c10-93a9-4941-a0df-96d83ab5ab24' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="39fc4-115">Пример 2. Обновление отображаемого имени пользователя с помощью имени директора</span><span class="sxs-lookup"><span data-stu-id="39fc4-115">Example 2: Update the display name of a user using user principal name</span></span>

```powershell
PS C:\> Update-AzADUser -UserPrincipalName foo@domain.com -DisplayName MyNewDisplayName
```

<span data-ttu-id="39fc4-116">Отображает имя пользователя с именем основного пользователя foo@domain.com '' на "MyNewDisplayName".</span><span class="sxs-lookup"><span data-stu-id="39fc4-116">Updates the display name of the user with user principal name 'foo@domain.com' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="39fc4-117">Пример 3. Обновление отображаемого имени пользователя с помощью piping</span><span class="sxs-lookup"><span data-stu-id="39fc4-117">Example 3: Update the display name of a user using piping</span></span>

```powershell
PS C:\> Get-AzADUser -ObjectId 155a5c10-93a9-4941-a0df-96d83ab5ab24 | Update-AzADUser -DisplayName MyNewDisplayName
```

<span data-ttu-id="39fc4-118">Возвращает пользователя с ид объекта '155a5c10-93a9-4941-a0df-96d83ab5ab24' и трубами к Update-AzADUser, чтобы обновить отображаемого имени пользователя на "MyNewDisplayName".</span><span class="sxs-lookup"><span data-stu-id="39fc4-118">Gets the user with object id '155a5c10-93a9-4941-a0df-96d83ab5ab24' and pipes that to the Update-AzADUser cmdlet to update the display name of that user to 'MyNewDisplayName'.</span></span>

## <span data-ttu-id="39fc4-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="39fc4-119">PARAMETERS</span></span>

### <span data-ttu-id="39fc4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39fc4-120">-DefaultProfile</span></span>
<span data-ttu-id="39fc4-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="39fc4-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39fc4-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="39fc4-122">-DisplayName</span></span>
<span data-ttu-id="39fc4-123">Новое отображаемая имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="39fc4-123">New display name for the user.</span></span>

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

### <span data-ttu-id="39fc4-124">-EnableAccount</span><span class="sxs-lookup"><span data-stu-id="39fc4-124">-EnableAccount</span></span>
<span data-ttu-id="39fc4-125">для включения учетной записи; в противном случае это будет ложь.</span><span class="sxs-lookup"><span data-stu-id="39fc4-125">true for enabling the account; otherwise, false.</span></span>

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

### <span data-ttu-id="39fc4-126">-ForceChangePasswordNextLogin</span><span class="sxs-lookup"><span data-stu-id="39fc4-126">-ForceChangePasswordNextLogin</span></span>
<span data-ttu-id="39fc4-127">При следующем успешном входе необходимо у указывается, должен ли пользователь сменить пароль.</span><span class="sxs-lookup"><span data-stu-id="39fc4-127">It must be specified if the user should change the password on the next successful login.</span></span>
<span data-ttu-id="39fc4-128">Действует только при обновлении пароля, в противном случае он будет игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="39fc4-128">Only valid if password is updated otherwise it will be ignored.</span></span>

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

### <span data-ttu-id="39fc4-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="39fc4-129">-InputObject</span></span>
<span data-ttu-id="39fc4-130">Объект, представляющий пользователя, который нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="39fc4-130">The object representing the user to be updated.</span></span>

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

### <span data-ttu-id="39fc4-131">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="39fc4-131">-ObjectId</span></span>
<span data-ttu-id="39fc4-132">ИД объекта пользователя, который нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="39fc4-132">The object id of the user to be updated.</span></span>

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

### <span data-ttu-id="39fc4-133">-Password</span><span class="sxs-lookup"><span data-stu-id="39fc4-133">-Password</span></span>
<span data-ttu-id="39fc4-134">Новый пароль пользователя.</span><span class="sxs-lookup"><span data-stu-id="39fc4-134">New password for the user.</span></span>

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

### <span data-ttu-id="39fc4-135">-UPNOrObjectId</span><span class="sxs-lookup"><span data-stu-id="39fc4-135">-UPNOrObjectId</span></span>
<span data-ttu-id="39fc4-136">Имя пользователя или ид объекта пользователя, который нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="39fc4-136">The user principal name or object id of the user to be updated.</span></span>

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

### <span data-ttu-id="39fc4-137">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="39fc4-137">-UserPrincipalName</span></span>
<span data-ttu-id="39fc4-138">Имя пользователя, который нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="39fc4-138">The user principal name of the user to be updated.</span></span>

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

### <span data-ttu-id="39fc4-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="39fc4-139">-Confirm</span></span>
<span data-ttu-id="39fc4-140">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="39fc4-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39fc4-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39fc4-141">-WhatIf</span></span>
<span data-ttu-id="39fc4-142">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="39fc4-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39fc4-143">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="39fc4-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39fc4-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39fc4-144">CommonParameters</span></span>
<span data-ttu-id="39fc4-145">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39fc4-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39fc4-146">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="39fc4-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39fc4-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="39fc4-147">INPUTS</span></span>

### <span data-ttu-id="39fc4-148">System.String</span><span class="sxs-lookup"><span data-stu-id="39fc4-148">System.String</span></span>

### <span data-ttu-id="39fc4-149">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span><span class="sxs-lookup"><span data-stu-id="39fc4-149">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span></span>

### <span data-ttu-id="39fc4-150">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="39fc4-150">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="39fc4-151">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="39fc4-151">System.Security.SecureString</span></span>

## <span data-ttu-id="39fc4-152">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="39fc4-152">OUTPUTS</span></span>

### <span data-ttu-id="39fc4-153">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span><span class="sxs-lookup"><span data-stu-id="39fc4-153">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="39fc4-154">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="39fc4-154">NOTES</span></span>

## <span data-ttu-id="39fc4-155">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="39fc4-155">RELATED LINKS</span></span>

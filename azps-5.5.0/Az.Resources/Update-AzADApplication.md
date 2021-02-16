---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/update-azadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADApplication.md
ms.openlocfilehash: c4754ecf8cae06fd43f57bc50d3b3fbeaf1d5081
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100242437"
---
# <span data-ttu-id="985d4-101">Update-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="985d4-101">Update-AzADApplication</span></span>

## <span data-ttu-id="985d4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="985d4-102">SYNOPSIS</span></span>
<span data-ttu-id="985d4-103">Обновляет существующее приложение Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="985d4-103">Updates an existing azure active directory application.</span></span>

## <span data-ttu-id="985d4-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="985d4-104">SYNTAX</span></span>

### <span data-ttu-id="985d4-105">ApplicationObjectIdWithUpdateParamsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="985d4-105">ApplicationObjectIdWithUpdateParamsParameterSet (Default)</span></span>
```
Update-AzADApplication -ObjectId <String> [-DisplayName <String>] [-HomePage <String>]
 [-IdentifierUri <String[]>] [-ReplyUrl <String[]>] [-AvailableToOtherTenants <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="985d4-106">ApplicationIdWithUpdateParamsParameterSet</span><span class="sxs-lookup"><span data-stu-id="985d4-106">ApplicationIdWithUpdateParamsParameterSet</span></span>
```
Update-AzADApplication -ApplicationId <Guid> [-DisplayName <String>] [-HomePage <String>]
 [-IdentifierUri <String[]>] [-ReplyUrl <String[]>] [-AvailableToOtherTenants <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="985d4-107">InputObjectWithUpdateParamsParameterSet</span><span class="sxs-lookup"><span data-stu-id="985d4-107">InputObjectWithUpdateParamsParameterSet</span></span>
```
Update-AzADApplication -InputObject <PSADApplication> [-DisplayName <String>] [-HomePage <String>]
 [-IdentifierUri <String[]>] [-ReplyUrl <String[]>] [-AvailableToOtherTenants <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="985d4-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="985d4-108">DESCRIPTION</span></span>
<span data-ttu-id="985d4-109">Обновляет существующее приложение Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="985d4-109">Updates an existing azure active directory application.</span></span>
<span data-ttu-id="985d4-110">Чтобы обновить учетные данные, связанные с этим приложением, воспользуйтесь New-AzADAppCredential-New-AzADAppCredential.</span><span class="sxs-lookup"><span data-stu-id="985d4-110">To update the credentials associated with this application, please use the New-AzADAppCredential cmdlet.</span></span>

## <span data-ttu-id="985d4-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="985d4-111">EXAMPLES</span></span>

### <span data-ttu-id="985d4-112">Пример 1. Обновление отображаемого имени приложения</span><span class="sxs-lookup"><span data-stu-id="985d4-112">Example 1 - Update the display name of an application</span></span>

```
PS C:\> Update-AzADApplication -ObjectId fb7b3405-ca44-4b5b-8584-12392f5d96d7 -DisplayName MyNewDisplayName
```

<span data-ttu-id="985d4-113">Отображает имя приложения с ид объекта "fb7b3405-ca44-4b5b-8584-12392f5d96d7" на "MyNewDisplayName".</span><span class="sxs-lookup"><span data-stu-id="985d4-113">Updates the display name of the application with object id 'fb7b3405-ca44-4b5b-8584-12392f5d96d7' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="985d4-114">Пример 2. Обновление всех свойств приложения</span><span class="sxs-lookup"><span data-stu-id="985d4-114">Example 2 - Update all properties of an application</span></span>

```
PS C:\> Update-AzADApplication -ObjectId fb7b3405-ca44-4b5b-8584-12392f5d96d7 -DisplayName MyNewDisplayName -HomePage https://www.microsoft.com -IdentifierUris "https://UpdateAppUri"
```

<span data-ttu-id="985d4-115">Обновляет свойства приложения с помощью ид объекта "fb7b3405-ca44-4b5b-8584-12392f5d96d7".</span><span class="sxs-lookup"><span data-stu-id="985d4-115">Updates the properties of an application with object id 'fb7b3405-ca44-4b5b-8584-12392f5d96d7'.</span></span>

### <span data-ttu-id="985d4-116">Пример 3. Обновление отображаемого имени приложения с помощью piping</span><span class="sxs-lookup"><span data-stu-id="985d4-116">Example 3 - Update the display name of an application using piping</span></span>

```
PS C:\> Get-AzADApplication -ObjectId fb7b3405-ca44-4b5b-8584-12392f5d96d7 | Update-AzADApplication -DisplayName MyNewDisplayName
```

<span data-ttu-id="985d4-117">Получает приложение с объектным идом 'fb7b3405-ca44-4b5b-8584-12392f5d96d7' и каналами, которые до Update-AzADApplication-управления, чтобы обновить отображаемого имени приложения на "MyNewDisplayName".</span><span class="sxs-lookup"><span data-stu-id="985d4-117">Gets the application with object id 'fb7b3405-ca44-4b5b-8584-12392f5d96d7' and pipes that to the Update-AzADApplication cmdlet to update the display name of the application to "MyNewDisplayName".</span></span>

## <span data-ttu-id="985d4-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="985d4-118">PARAMETERS</span></span>

### <span data-ttu-id="985d4-119">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="985d4-119">-ApplicationId</span></span>
<span data-ttu-id="985d4-120">ID приложения, которое нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="985d4-120">The application id of the application to update.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationIdWithUpdateParamsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="985d4-121">-AvailableToOtherTenants</span><span class="sxs-lookup"><span data-stu-id="985d4-121">-AvailableToOtherTenants</span></span>
<span data-ttu-id="985d4-122">Имеет true, если приложение совместно с другими клиентами; в противном случае это будет ложь.</span><span class="sxs-lookup"><span data-stu-id="985d4-122">True if the application is shared with other tenants; otherwise, false.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: ApplicationObjectIdWithUpdateParamsParameterSet, ApplicationIdWithUpdateParamsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Boolean
Parameter Sets: InputObjectWithUpdateParamsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="985d4-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="985d4-123">-DefaultProfile</span></span>
<span data-ttu-id="985d4-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="985d4-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="985d4-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="985d4-125">-DisplayName</span></span>
<span data-ttu-id="985d4-126">Отображаемая версия приложения, которое нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="985d4-126">The display name for the application to update.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdWithUpdateParamsParameterSet, ApplicationIdWithUpdateParamsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InputObjectWithUpdateParamsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="985d4-127">-HomePage</span><span class="sxs-lookup"><span data-stu-id="985d4-127">-HomePage</span></span>
<span data-ttu-id="985d4-128">URL-адрес домашней страницы приложения.</span><span class="sxs-lookup"><span data-stu-id="985d4-128">The URL to the application's homepage.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdWithUpdateParamsParameterSet, ApplicationIdWithUpdateParamsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InputObjectWithUpdateParamsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="985d4-129">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="985d4-129">-IdentifierUri</span></span>
<span data-ttu-id="985d4-130">ЮРИС, определяют приложение.</span><span class="sxs-lookup"><span data-stu-id="985d4-130">The URIs that identify the application.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ApplicationObjectIdWithUpdateParamsParameterSet, ApplicationIdWithUpdateParamsParameterSet
Aliases: IdentifierUris

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: InputObjectWithUpdateParamsParameterSet
Aliases: IdentifierUris

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="985d4-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="985d4-131">-InputObject</span></span>
<span data-ttu-id="985d4-132">Объект, представляющий приложение, которое нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="985d4-132">The object representing the application to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADApplication
Parameter Sets: InputObjectWithUpdateParamsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="985d4-133">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="985d4-133">-ObjectId</span></span>
<span data-ttu-id="985d4-134">ИД объекта приложения, который нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="985d4-134">The object id of the application to update.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdWithUpdateParamsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="985d4-135">-ReplyUrl</span><span class="sxs-lookup"><span data-stu-id="985d4-135">-ReplyUrl</span></span>
<span data-ttu-id="985d4-136">Указывает URL-адреса, на которые отправляются токены пользователей для регистрации, или ЮРИСов перенаправления, в которые отправляются коды авторизации oAuth 2.0 и маркеры доступа.</span><span class="sxs-lookup"><span data-stu-id="985d4-136">Specifies the URLs that user tokens are sent to for sign in, or the redirect URIs that OAuth 2.0 authorization codes and access tokens are sent to.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ApplicationObjectIdWithUpdateParamsParameterSet, ApplicationIdWithUpdateParamsParameterSet
Aliases: ReplyUrls

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: InputObjectWithUpdateParamsParameterSet
Aliases: ReplyUrls

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="985d4-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="985d4-137">-Confirm</span></span>
<span data-ttu-id="985d4-138">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="985d4-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="985d4-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="985d4-139">-WhatIf</span></span>
<span data-ttu-id="985d4-140">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="985d4-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="985d4-141">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="985d4-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="985d4-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="985d4-142">CommonParameters</span></span>
<span data-ttu-id="985d4-143">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="985d4-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="985d4-144">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="985d4-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="985d4-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="985d4-145">INPUTS</span></span>

### <span data-ttu-id="985d4-146">System.String</span><span class="sxs-lookup"><span data-stu-id="985d4-146">System.String</span></span>

### <span data-ttu-id="985d4-147">System.Guid</span><span class="sxs-lookup"><span data-stu-id="985d4-147">System.Guid</span></span>

### <span data-ttu-id="985d4-148">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span><span class="sxs-lookup"><span data-stu-id="985d4-148">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

### <span data-ttu-id="985d4-149">System.String[]</span><span class="sxs-lookup"><span data-stu-id="985d4-149">System.String[]</span></span>

### <span data-ttu-id="985d4-150">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="985d4-150">System.Boolean</span></span>

## <span data-ttu-id="985d4-151">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="985d4-151">OUTPUTS</span></span>

### <span data-ttu-id="985d4-152">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span><span class="sxs-lookup"><span data-stu-id="985d4-152">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="985d4-153">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="985d4-153">NOTES</span></span>

## <span data-ttu-id="985d4-154">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="985d4-154">RELATED LINKS</span></span>

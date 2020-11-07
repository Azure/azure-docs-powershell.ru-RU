---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/update-Azadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Update-AzADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Update-AzADApplication.md
ms.openlocfilehash: 8eb01ccfa16b1d3610468f98117ee650376d4b6c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910804"
---
# <span data-ttu-id="2386e-101">Update-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="2386e-101">Update-AzADApplication</span></span>

## <span data-ttu-id="2386e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2386e-102">SYNOPSIS</span></span>
<span data-ttu-id="2386e-103">Обновляет существующее приложение Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="2386e-103">Updates an existing azure active directory application.</span></span>

## <span data-ttu-id="2386e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2386e-104">SYNTAX</span></span>

### <span data-ttu-id="2386e-105">ApplicationObjectIdWithUpdateParamsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2386e-105">ApplicationObjectIdWithUpdateParamsParameterSet (Default)</span></span>
```
Update-AzADApplication -ObjectId <Guid> [-DisplayName <String>] [-HomePage <String>]
 [-IdentifierUri <String[]>] [-ReplyUrl <String[]>] [-AvailableToOtherTenants <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2386e-106">ApplicationIdWithUpdateParamsParameterSet</span><span class="sxs-lookup"><span data-stu-id="2386e-106">ApplicationIdWithUpdateParamsParameterSet</span></span>
```
Update-AzADApplication -ApplicationId <Guid> [-DisplayName <String>] [-HomePage <String>]
 [-IdentifierUri <String[]>] [-ReplyUrl <String[]>] [-AvailableToOtherTenants <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2386e-107">InputObjectWithUpdateParamsParameterSet</span><span class="sxs-lookup"><span data-stu-id="2386e-107">InputObjectWithUpdateParamsParameterSet</span></span>
```
Update-AzADApplication -InputObject <PSADApplication> [-DisplayName <String>] [-HomePage <String>]
 [-IdentifierUri <String[]>] [-ReplyUrl <String[]>] [-AvailableToOtherTenants <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2386e-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2386e-108">DESCRIPTION</span></span>
<span data-ttu-id="2386e-109">Обновляет существующее приложение Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="2386e-109">Updates an existing azure active directory application.</span></span>
<span data-ttu-id="2386e-110">Чтобы обновить учетные данные, связанные с этим приложением, используйте командлет New-AzADAppCredential.</span><span class="sxs-lookup"><span data-stu-id="2386e-110">To update the credentials associated with this application, please use the New-AzADAppCredential cmdlet.</span></span>

## <span data-ttu-id="2386e-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2386e-111">EXAMPLES</span></span>

### <span data-ttu-id="2386e-112">Пример 1: обновление отображаемого имени приложения</span><span class="sxs-lookup"><span data-stu-id="2386e-112">Example 1 - Update the display name of an application</span></span>

```
PS C:\> Update-AzADApplication -ObjectId fb7b3405-ca44-4b5b-8584-12392f5d96d7 -DisplayName MyNewDisplayName
```

<span data-ttu-id="2386e-113">Обновляет отображаемое имя приложения с помощью идентификатора объекта "fb7b3405-CA44-4b5b-8584-12392f5d96d7" и "MyNewDisplayName".</span><span class="sxs-lookup"><span data-stu-id="2386e-113">Updates the display name of the application with object id 'fb7b3405-ca44-4b5b-8584-12392f5d96d7' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="2386e-114">Пример 2: обновление всех свойств приложения</span><span class="sxs-lookup"><span data-stu-id="2386e-114">Example 2 - Update all properties of an application</span></span>

```
PS C:\> Update-AzADApplication -ObjectId fb7b3405-ca44-4b5b-8584-12392f5d96d7 -DisplayName MyNewDisplayName -HomePage https://www.microsoft.com -IdentifierUris "https://UpdateAppUri"
```

<span data-ttu-id="2386e-115">Обновляет свойства приложения с помощью идентификатора объекта "fb7b3405-CA44-4b5b-8584-12392f5d96d7".</span><span class="sxs-lookup"><span data-stu-id="2386e-115">Updates the properties of an application with object id 'fb7b3405-ca44-4b5b-8584-12392f5d96d7'.</span></span>

### <span data-ttu-id="2386e-116">Пример 3: обновление отображаемого имени приложения с помощью трубопроводов</span><span class="sxs-lookup"><span data-stu-id="2386e-116">Example 3 - Update the display name of an application using piping</span></span>

```
PS C:\> Get-AzADApplication -ObjectId fb7b3405-ca44-4b5b-8584-12392f5d96d7 | Update-AzADApplication -DisplayName MyNewDisplayName
```

<span data-ttu-id="2386e-117">Возвращает приложение с идентификатором объекта "fb7b3405-CA44-4b5b-8584-12392f5d96d7" и каналами, которые должны использовать командлет Update-AzADApplication для обновления отображаемого имени приложения на "MyNewDisplayName".</span><span class="sxs-lookup"><span data-stu-id="2386e-117">Gets the application with object id 'fb7b3405-ca44-4b5b-8584-12392f5d96d7' and pipes that to the Update-AzADApplication cmdlet to update the display name of the application to "MyNewDisplayName".</span></span>

## <span data-ttu-id="2386e-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2386e-118">PARAMETERS</span></span>

### <span data-ttu-id="2386e-119">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="2386e-119">-ApplicationId</span></span>
<span data-ttu-id="2386e-120">Идентификатор приложения, которое необходимо обновить.</span><span class="sxs-lookup"><span data-stu-id="2386e-120">The application id of the application to update.</span></span>

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

### <span data-ttu-id="2386e-121">-AvailableToOtherTenants</span><span class="sxs-lookup"><span data-stu-id="2386e-121">-AvailableToOtherTenants</span></span>
<span data-ttu-id="2386e-122">Значение true, если приложение предоставлено другим клиентам; в противном случае — значение false.</span><span class="sxs-lookup"><span data-stu-id="2386e-122">True if the application is shared with other tenants; otherwise, false.</span></span>

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

### <span data-ttu-id="2386e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2386e-123">-DefaultProfile</span></span>
<span data-ttu-id="2386e-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2386e-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2386e-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="2386e-125">-DisplayName</span></span>
<span data-ttu-id="2386e-126">Отображаемое имя приложения, которое необходимо обновить.</span><span class="sxs-lookup"><span data-stu-id="2386e-126">The display name for the application to update.</span></span>

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

### <span data-ttu-id="2386e-127">-Главная страница</span><span class="sxs-lookup"><span data-stu-id="2386e-127">-HomePage</span></span>
<span data-ttu-id="2386e-128">URL-адрес домашней страницы приложения.</span><span class="sxs-lookup"><span data-stu-id="2386e-128">The URL to the application's homepage.</span></span>

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

### <span data-ttu-id="2386e-129">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="2386e-129">-IdentifierUri</span></span>
<span data-ttu-id="2386e-130">Универсальные коды ресурсов (URI), обозначающие приложение.</span><span class="sxs-lookup"><span data-stu-id="2386e-130">The URIs that identify the application.</span></span>

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

### <span data-ttu-id="2386e-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2386e-131">-InputObject</span></span>
<span data-ttu-id="2386e-132">Объект, представляющий приложение, которое требуется обновить.</span><span class="sxs-lookup"><span data-stu-id="2386e-132">The object representing the application to update.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication
Parameter Sets: InputObjectWithUpdateParamsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2386e-133">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="2386e-133">-ObjectId</span></span>
<span data-ttu-id="2386e-134">Идентификатор объекта обновляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="2386e-134">The object id of the application to update.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationObjectIdWithUpdateParamsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2386e-135">-ReplyUrl</span><span class="sxs-lookup"><span data-stu-id="2386e-135">-ReplyUrl</span></span>
<span data-ttu-id="2386e-136">Указывает URL-адреса, на которые должны отправляться маркеры пользователей для входа, или URI перенаправления, на которые отправляются коды авторизации OAuth 2,0 и маркеры доступа.</span><span class="sxs-lookup"><span data-stu-id="2386e-136">Specifies the URLs that user tokens are sent to for sign in, or the redirect URIs that OAuth 2.0 authorization codes and access tokens are sent to.</span></span>

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

### <span data-ttu-id="2386e-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2386e-137">-Confirm</span></span>
<span data-ttu-id="2386e-138">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2386e-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2386e-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2386e-139">-WhatIf</span></span>
<span data-ttu-id="2386e-140">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2386e-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2386e-141">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2386e-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2386e-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2386e-142">CommonParameters</span></span>
<span data-ttu-id="2386e-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2386e-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2386e-144">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2386e-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2386e-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2386e-145">INPUTS</span></span>

### <span data-ttu-id="2386e-146">System. GUID</span><span class="sxs-lookup"><span data-stu-id="2386e-146">System.Guid</span></span>

### <span data-ttu-id="2386e-147">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="2386e-147">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>
<span data-ttu-id="2386e-148">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2386e-148">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="2386e-149">System. String</span><span class="sxs-lookup"><span data-stu-id="2386e-149">System.String</span></span>

### <span data-ttu-id="2386e-150">System. String []</span><span class="sxs-lookup"><span data-stu-id="2386e-150">System.String[]</span></span>

### <span data-ttu-id="2386e-151">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2386e-151">System.Boolean</span></span>

## <span data-ttu-id="2386e-152">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2386e-152">OUTPUTS</span></span>

### <span data-ttu-id="2386e-153">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="2386e-153">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="2386e-154">Пуск</span><span class="sxs-lookup"><span data-stu-id="2386e-154">NOTES</span></span>

## <span data-ttu-id="2386e-155">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2386e-155">RELATED LINKS</span></span>

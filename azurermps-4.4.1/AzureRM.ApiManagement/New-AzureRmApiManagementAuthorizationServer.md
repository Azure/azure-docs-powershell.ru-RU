---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 45B96AB0-ACE3-4754-B162-88027AC8CA41
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementAuthorizationServer.md
ms.openlocfilehash: cfba050b3ec6e464465d72e5f8d236f3b253fd0e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565744"
---
# <span data-ttu-id="4a5e7-101">New-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="4a5e7-101">New-AzureRmApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="4a5e7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4a5e7-102">SYNOPSIS</span></span>
<span data-ttu-id="4a5e7-103">Создание сервера авторизации.</span><span class="sxs-lookup"><span data-stu-id="4a5e7-103">Creates an authorization server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4a5e7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4a5e7-104">SYNTAX</span></span>

```
New-AzureRmApiManagementAuthorizationServer -Context <PsApiManagementContext> [-ServerId <String>]
 -Name <String> [-Description <String>] -ClientRegistrationPageUrl <String> -AuthorizationEndpointUrl <String>
 -TokenEndpointUrl <String> -ClientId <String> [-ClientSecret <String>]
 [-AuthorizationRequestMethods <PsApiManagementAuthorizationRequestMethod[]>]
 -GrantTypes <PsApiManagementGrantType[]>
 -ClientAuthenticationMethods <PsApiManagementClientAuthenticationMethod[]> [-TokenBodyParameters <Hashtable>]
 [-SupportState <Boolean>] [-DefaultScope <String>]
 -AccessTokenSendingMethods <PsApiManagementAccessTokenSendingMethod[]> [-ResourceOwnerUsername <String>]
 [-ResourceOwnerPassword <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4a5e7-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4a5e7-105">DESCRIPTION</span></span>
<span data-ttu-id="4a5e7-106">Командлет **New-AzureRmApiManagementAuthorizationServer** создает сервер авторизации управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="4a5e7-106">The **New-AzureRmApiManagementAuthorizationServer** cmdlet creates an Azure API Management authorization server.</span></span>

## <span data-ttu-id="4a5e7-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4a5e7-107">EXAMPLES</span></span>

### <span data-ttu-id="4a5e7-108">Пример 1: создание сервера авторизации</span><span class="sxs-lookup"><span data-stu-id="4a5e7-108">Example 1: Create an authorization server</span></span>
```
PS C:\>New-AzureRmApiManagementAuthrizarionServer -Context $ApiMgmtContext -Name "Contoso OAuth2 server" -ClientRegistrationPageUrl "https://contoso/signup" -AuthorizationEndpointUrl "https://contoso/auth" -TokenEndpointUrl "https://contoso/token" -ClientId "clientid" -ClientSecret "e041ed1b660b4eadbad5a29d066e6e88" -AuthorizationRequestMethods @('Get', 'Post') -GrantTypes @( 'AuthorizationCode', 'Implicit', 'ResourceOwnerPassword', 'ClientCredentials') -ClientAuthenticationMethods @('Basic') -TokenBodyParameters @{'par1'='val1'; 'par2'='val2'} -AccessTokenSendingMethods @('AuthorizationHeader', 'Query') -ResourceOwnerUsername "ivan" -ResourceOwnerPassword "qwerty"
```

<span data-ttu-id="4a5e7-109">Эта команда создает сервер авторизации.</span><span class="sxs-lookup"><span data-stu-id="4a5e7-109">This command creates an authorization server.</span></span>

## <span data-ttu-id="4a5e7-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4a5e7-110">PARAMETERS</span></span>

### <span data-ttu-id="4a5e7-111">-AccessTokenSendingMethods</span><span class="sxs-lookup"><span data-stu-id="4a5e7-111">-AccessTokenSendingMethods</span></span>
<span data-ttu-id="4a5e7-112">Указывает массив методов для отправки маркера доступа.</span><span class="sxs-lookup"><span data-stu-id="4a5e7-112">Specifies an array of methods to send an access token.</span></span>
<span data-ttu-id="4a5e7-113">psdx_paramvalues AuthorizationHeader и Query.</span><span class="sxs-lookup"><span data-stu-id="4a5e7-113">psdx_paramvalues AuthorizationHeader and Query.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessTokenSendingMethod[]
Parameter Sets: (All)
Aliases: 
Accepted values: AuthorizationHeader, Query

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a5e7-114">-AuthorizationEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="4a5e7-114">-AuthorizationEndpointUrl</span></span>
<span data-ttu-id="4a5e7-115">Указывает конечную точку авторизации для проверки подлинности владельцев ресурсов и получения разрешений на авторизацию.</span><span class="sxs-lookup"><span data-stu-id="4a5e7-115">Specifies the authorization endpoint to authenticate resource owners and obtain authorization grants.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a5e7-116">-AuthorizationRequestMethods</span><span class="sxs-lookup"><span data-stu-id="4a5e7-116">-AuthorizationRequestMethods</span></span>
<span data-ttu-id="4a5e7-117">Указывает массив методов запроса авторизации.</span><span class="sxs-lookup"><span data-stu-id="4a5e7-117">Specifies an array of authorization request methods.</span></span>
<span data-ttu-id="4a5e7-118">Допустимые значения: GET, POST.</span><span class="sxs-lookup"><span data-stu-id="4a5e7-118">Valid values are: GET, POST.</span></span>
<span data-ttu-id="4a5e7-119">Значением по умолчанию является GET.</span><span class="sxs-lookup"><span data-stu-id="4a5e7-119">The default value is GET.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAuthorizationRequestMethod[]
Parameter Sets: (All)
Aliases: 
Accepted values: Get, Post

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a5e7-120">-ClientAuthenticationMethods</span><span class="sxs-lookup"><span data-stu-id="4a5e7-120">-ClientAuthenticationMethods</span></span>
<span data-ttu-id="4a5e7-121">Задает массив методов проверки подлинности клиента.</span><span class="sxs-lookup"><span data-stu-id="4a5e7-121">Specifies an array of client authentication methods.</span></span>
<span data-ttu-id="4a5e7-122">psdx_paramvalues основного и основного текста.</span><span class="sxs-lookup"><span data-stu-id="4a5e7-122">psdx_paramvalues Basic and Body.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientAuthenticationMethod[]
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Body

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a5e7-123">-ClientId</span><span class="sxs-lookup"><span data-stu-id="4a5e7-123">-ClientId</span></span>
<span data-ttu-id="4a5e7-124">Указывает идентификатор клиента для консоли разработчика, которая является клиентским приложением.</span><span class="sxs-lookup"><span data-stu-id="4a5e7-124">Specifies the client ID of the developer console that is the client application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a5e7-125">-ClientRegistrationPageUrl</span><span class="sxs-lookup"><span data-stu-id="4a5e7-125">-ClientRegistrationPageUrl</span></span>
<span data-ttu-id="4a5e7-126">Задает конечную точку регистрации клиента для регистрации клиентов с помощью сервера авторизации и получения учетных данных клиента.</span><span class="sxs-lookup"><span data-stu-id="4a5e7-126">Specifies the client registration endpoint to register clients with the authorization server and obtain client credentials.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a5e7-127">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="4a5e7-127">-ClientSecret</span></span>
<span data-ttu-id="4a5e7-128">Указывает секретный ключ клиента для консоли разработчика, который является клиентским приложением.</span><span class="sxs-lookup"><span data-stu-id="4a5e7-128">Specifies the client secret of developer console that is the client application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a5e7-129">-Context</span><span class="sxs-lookup"><span data-stu-id="4a5e7-129">-Context</span></span>
<span data-ttu-id="4a5e7-130">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="4a5e7-130">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a5e7-131">-DefaultScope</span><span class="sxs-lookup"><span data-stu-id="4a5e7-131">-DefaultScope</span></span>
<span data-ttu-id="4a5e7-132">Задает область по умолчанию для сервера авторизации.</span><span class="sxs-lookup"><span data-stu-id="4a5e7-132">Specifies the default scope for the authorization server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a5e7-133">-Описание</span><span class="sxs-lookup"><span data-stu-id="4a5e7-133">-Description</span></span>
<span data-ttu-id="4a5e7-134">Задает описание сервера авторизации.</span><span class="sxs-lookup"><span data-stu-id="4a5e7-134">Specifies a description for an authorization server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a5e7-135">-GrantTypes</span><span class="sxs-lookup"><span data-stu-id="4a5e7-135">-GrantTypes</span></span>
<span data-ttu-id="4a5e7-136">Указывает массив типов субсидий.</span><span class="sxs-lookup"><span data-stu-id="4a5e7-136">Specifies an array of grant types.</span></span>
<span data-ttu-id="4a5e7-137">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="4a5e7-137">psdx_paramvalues</span></span>

- <span data-ttu-id="4a5e7-138">AuthorizationCode</span><span class="sxs-lookup"><span data-stu-id="4a5e7-138">AuthorizationCode</span></span>
- <span data-ttu-id="4a5e7-139">ClientCredentials</span><span class="sxs-lookup"><span data-stu-id="4a5e7-139">ClientCredentials</span></span> 
- <span data-ttu-id="4a5e7-140">Согласия</span><span class="sxs-lookup"><span data-stu-id="4a5e7-140">Implicit</span></span> 
- <span data-ttu-id="4a5e7-141">ResourceOwnerPassword</span><span class="sxs-lookup"><span data-stu-id="4a5e7-141">ResourceOwnerPassword</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGrantType[]
Parameter Sets: (All)
Aliases: 
Accepted values: AuthorizationCode, Implicit, ResourceOwnerPassword, ClientCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a5e7-142">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4a5e7-142">-Name</span></span>
<span data-ttu-id="4a5e7-143">Указывает имя сервера авторизации, который нужно создать.</span><span class="sxs-lookup"><span data-stu-id="4a5e7-143">Specifies the name of the authorization server to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a5e7-144">-ResourceOwnerPassword</span><span class="sxs-lookup"><span data-stu-id="4a5e7-144">-ResourceOwnerPassword</span></span>
<span data-ttu-id="4a5e7-145">Указывает пароль владельца ресурса.</span><span class="sxs-lookup"><span data-stu-id="4a5e7-145">Specifies the resource owner password.</span></span>
<span data-ttu-id="4a5e7-146">Если ResourceOwnerPassword указан с помощью параметра *GrantTypes* , необходимо указать этот параметр.</span><span class="sxs-lookup"><span data-stu-id="4a5e7-146">You must specify this parameter is required if ResourceOwnerPassword is specified by the *GrantTypes* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a5e7-147">-ResourceOwnerUsername</span><span class="sxs-lookup"><span data-stu-id="4a5e7-147">-ResourceOwnerUsername</span></span>
<span data-ttu-id="4a5e7-148">Указывает имя пользователя, владеющего ресурсом.</span><span class="sxs-lookup"><span data-stu-id="4a5e7-148">Specifies the resource owner user name.</span></span>
<span data-ttu-id="4a5e7-149">Этот параметр необходимо указывать, если параметр ResourceOwnerPassword указан с помощью параметра *GrantTypes* .</span><span class="sxs-lookup"><span data-stu-id="4a5e7-149">You must specify this parameter if ResourceOwnerPassword is specified by the *GrantTypes* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a5e7-150">-ServerId</span><span class="sxs-lookup"><span data-stu-id="4a5e7-150">-ServerId</span></span>
<span data-ttu-id="4a5e7-151">Указывает идентификатор сервера авторизации, который нужно создать.</span><span class="sxs-lookup"><span data-stu-id="4a5e7-151">Specifies the ID of the authorization server to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a5e7-152">-SupportState</span><span class="sxs-lookup"><span data-stu-id="4a5e7-152">-SupportState</span></span>
<span data-ttu-id="4a5e7-153">Указывает, следует ли поддерживать параметр *State* .</span><span class="sxs-lookup"><span data-stu-id="4a5e7-153">Indicates whether to support the *State* parameter.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a5e7-154">-TokenBodyParameters</span><span class="sxs-lookup"><span data-stu-id="4a5e7-154">-TokenBodyParameters</span></span>
<span data-ttu-id="4a5e7-155">Указывает дополнительные параметры тела, использующие формат **Application/x-www-UrlEncoded** .</span><span class="sxs-lookup"><span data-stu-id="4a5e7-155">Specifies additional body parameters using **application/x-www-form-urlencoded** format.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a5e7-156">-TokenEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="4a5e7-156">-TokenEndpointUrl</span></span>
<span data-ttu-id="4a5e7-157">Указывает URL-адрес конечной точки маркера, который используется клиентами для получения маркеров доступа в Exchange для представления разрешений на предоставление авторизации или обновления маркеров.</span><span class="sxs-lookup"><span data-stu-id="4a5e7-157">Specifies the token endpoint URL that is used by clients to obtain access tokens in exchange for presenting authorization grants or refresh tokens.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a5e7-158">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a5e7-158">-DefaultProfile</span></span>
<span data-ttu-id="4a5e7-159">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4a5e7-159">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4a5e7-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a5e7-160">CommonParameters</span></span>
<span data-ttu-id="4a5e7-161">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4a5e7-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a5e7-162">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a5e7-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a5e7-163">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4a5e7-163">INPUTS</span></span>

## <span data-ttu-id="4a5e7-164">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4a5e7-164">OUTPUTS</span></span>

### <span data-ttu-id="4a5e7-165">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementOAuth2AuthrozationServer</span><span class="sxs-lookup"><span data-stu-id="4a5e7-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthrozationServer</span></span>

## <span data-ttu-id="4a5e7-166">Пуск</span><span class="sxs-lookup"><span data-stu-id="4a5e7-166">NOTES</span></span>

## <span data-ttu-id="4a5e7-167">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4a5e7-167">RELATED LINKS</span></span>


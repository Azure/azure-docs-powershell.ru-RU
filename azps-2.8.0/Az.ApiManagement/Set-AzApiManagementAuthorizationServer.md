---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 93005775-3AB9-43C5-B353-45B82124ADB7
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementAuthorizationServer.md
ms.openlocfilehash: 696db55822242e124f006be233a9c8a8605a360d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93727946"
---
# <span data-ttu-id="4940a-101">Set-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="4940a-101">Set-AzApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="4940a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4940a-102">SYNOPSIS</span></span>
<span data-ttu-id="4940a-103">Изменение сервера авторизации.</span><span class="sxs-lookup"><span data-stu-id="4940a-103">Modifies an authorization server.</span></span>

## <span data-ttu-id="4940a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4940a-104">SYNTAX</span></span>

```
Set-AzApiManagementAuthorizationServer -Context <PsApiManagementContext> -ServerId <String> -Name <String>
 [-Description <String>] -ClientRegistrationPageUrl <String> -AuthorizationEndpointUrl <String>
 -TokenEndpointUrl <String> -ClientId <String> [-ClientSecret <String>]
 [-AuthorizationRequestMethods <PsApiManagementAuthorizationRequestMethod[]>]
 -GrantTypes <PsApiManagementGrantType[]>
 -ClientAuthenticationMethods <PsApiManagementClientAuthenticationMethod[]> [-TokenBodyParameters <Hashtable>]
 [-SupportState <Boolean>] [-DefaultScope <String>]
 -AccessTokenSendingMethods <PsApiManagementAccessTokenSendingMethod[]> [-ResourceOwnerUsername <String>]
 [-ResourceOwnerPassword <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4940a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4940a-105">DESCRIPTION</span></span>
<span data-ttu-id="4940a-106">Командлет **Set-AzApiManagementAuthorizationServer** изменяет сведения о сервере авторизации управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="4940a-106">The **Set-AzApiManagementAuthorizationServer** cmdlet modifies Azure API Management authorization server details.</span></span>

## <span data-ttu-id="4940a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4940a-107">EXAMPLES</span></span>

### <span data-ttu-id="4940a-108">Пример 1: изменение сервера авторизации</span><span class="sxs-lookup"><span data-stu-id="4940a-108">Example 1: Modify an authorization server</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementAuthorizationServer -Context $ApiMgmtContext -ServerId 0123456789 -Name "Contoso OAuth2 server" -ClientRegistrationPageUrl "https://contoso/signupv2" -AuthorizationEndpointUrl "https://contoso/authv2" -TokenEndpointUrl "https://contoso/tokenv2" -ClientId "clientid" -ClientSecret "e041ed1b660b4eadbad5a29d066e6e88" -AuthorizationRequestMethods @('Get') -GrantTypes @( 'AuthorizationCode', 'Implicit', 'ClientCredentials') -ClientAuthenticationMethods @('Basic') -TokenBodyParameters @{'par1'='val1'} -AccessTokenSendingMethods @('AuthorizationHeader')
```

<span data-ttu-id="4940a-109">Эта команда изменяет указанный сервер авторизации управления API.</span><span class="sxs-lookup"><span data-stu-id="4940a-109">This command modifies the specified API Management authorization server.</span></span>

## <span data-ttu-id="4940a-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4940a-110">PARAMETERS</span></span>

### <span data-ttu-id="4940a-111">-AccessTokenSendingMethods</span><span class="sxs-lookup"><span data-stu-id="4940a-111">-AccessTokenSendingMethods</span></span>
<span data-ttu-id="4940a-112">Указывает массив методов для отправки маркера доступа.</span><span class="sxs-lookup"><span data-stu-id="4940a-112">Specifies an array of methods to send an access token.</span></span>
<span data-ttu-id="4940a-113">psdx_paramvalues AuthorizationHeader и Query.</span><span class="sxs-lookup"><span data-stu-id="4940a-113">psdx_paramvalues AuthorizationHeader and Query.</span></span>

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

### <span data-ttu-id="4940a-114">-AuthorizationEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="4940a-114">-AuthorizationEndpointUrl</span></span>
<span data-ttu-id="4940a-115">Указывает конечную точку авторизации для проверки подлинности владельцев ресурсов и получения разрешений на авторизацию.</span><span class="sxs-lookup"><span data-stu-id="4940a-115">Specifies the authorization endpoint to authenticate resource owners and obtain authorization grants.</span></span>

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

### <span data-ttu-id="4940a-116">-AuthorizationRequestMethods</span><span class="sxs-lookup"><span data-stu-id="4940a-116">-AuthorizationRequestMethods</span></span>
<span data-ttu-id="4940a-117">Указывает массив методов запроса авторизации.</span><span class="sxs-lookup"><span data-stu-id="4940a-117">Specifies an array of authorization request methods.</span></span>
<span data-ttu-id="4940a-118">psdx_paramvalues GET и POST.</span><span class="sxs-lookup"><span data-stu-id="4940a-118">psdx_paramvalues GET and POST.</span></span>
<span data-ttu-id="4940a-119">Значением по умолчанию является GET.</span><span class="sxs-lookup"><span data-stu-id="4940a-119">The default value is GET.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAuthorizationRequestMethod[]
Parameter Sets: (All)
Aliases:
Accepted values: Get, Post, Head, Options, Trace, Put, Patch, Delete

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4940a-120">-ClientAuthenticationMethods</span><span class="sxs-lookup"><span data-stu-id="4940a-120">-ClientAuthenticationMethods</span></span>
<span data-ttu-id="4940a-121">Задает массив методов проверки подлинности клиента.</span><span class="sxs-lookup"><span data-stu-id="4940a-121">Specifies an array of client authentication methods.</span></span>
<span data-ttu-id="4940a-122">psdx_paramvalues основного и основного текста.</span><span class="sxs-lookup"><span data-stu-id="4940a-122">psdx_paramvalues Basic and Body.</span></span>

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

### <span data-ttu-id="4940a-123">-ClientId</span><span class="sxs-lookup"><span data-stu-id="4940a-123">-ClientId</span></span>
<span data-ttu-id="4940a-124">Указывает идентификатор клиента для консоли разработчика, которая является клиентским приложением.</span><span class="sxs-lookup"><span data-stu-id="4940a-124">Specifies the client ID of the developer console that is the client application.</span></span>

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

### <span data-ttu-id="4940a-125">-ClientRegistrationPageUrl</span><span class="sxs-lookup"><span data-stu-id="4940a-125">-ClientRegistrationPageUrl</span></span>
<span data-ttu-id="4940a-126">Задает конечную точку регистрации клиента для регистрации клиентов с помощью сервера авторизации и получения учетных данных клиента.</span><span class="sxs-lookup"><span data-stu-id="4940a-126">Specifies the client registration endpoint to register clients with the authorization server and obtain client credentials.</span></span>

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

### <span data-ttu-id="4940a-127">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="4940a-127">-ClientSecret</span></span>
<span data-ttu-id="4940a-128">Указывает секретный ключ клиента для консоли разработчика, которая является клиентским приложением.</span><span class="sxs-lookup"><span data-stu-id="4940a-128">Specifies the client secret of the developer console that is the client application.</span></span>

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

### <span data-ttu-id="4940a-129">-Context</span><span class="sxs-lookup"><span data-stu-id="4940a-129">-Context</span></span>
<span data-ttu-id="4940a-130">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="4940a-130">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4940a-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4940a-131">-DefaultProfile</span></span>
<span data-ttu-id="4940a-132">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4940a-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4940a-133">-DefaultScope</span><span class="sxs-lookup"><span data-stu-id="4940a-133">-DefaultScope</span></span>
<span data-ttu-id="4940a-134">Задает область по умолчанию для сервера авторизации.</span><span class="sxs-lookup"><span data-stu-id="4940a-134">Specifies the default scope for the authorization server.</span></span>

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

### <span data-ttu-id="4940a-135">-Описание</span><span class="sxs-lookup"><span data-stu-id="4940a-135">-Description</span></span>
<span data-ttu-id="4940a-136">Задает описание сервера авторизации.</span><span class="sxs-lookup"><span data-stu-id="4940a-136">Specifies a description for an authorization server.</span></span>

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

### <span data-ttu-id="4940a-137">-GrantTypes</span><span class="sxs-lookup"><span data-stu-id="4940a-137">-GrantTypes</span></span>
<span data-ttu-id="4940a-138">Указывает массив типов субсидий.</span><span class="sxs-lookup"><span data-stu-id="4940a-138">Specifies an array of grant types.</span></span>
<span data-ttu-id="4940a-139">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="4940a-139">psdx_paramvalues</span></span>
- <span data-ttu-id="4940a-140">AuthorizationCode</span><span class="sxs-lookup"><span data-stu-id="4940a-140">AuthorizationCode</span></span>
- <span data-ttu-id="4940a-141">ClientCredentials</span><span class="sxs-lookup"><span data-stu-id="4940a-141">ClientCredentials</span></span> 
- <span data-ttu-id="4940a-142">Согласия</span><span class="sxs-lookup"><span data-stu-id="4940a-142">Implicit</span></span> 
- <span data-ttu-id="4940a-143">ResourceOwnerPassword</span><span class="sxs-lookup"><span data-stu-id="4940a-143">ResourceOwnerPassword</span></span>

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

### <span data-ttu-id="4940a-144">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4940a-144">-Name</span></span>
<span data-ttu-id="4940a-145">Указывает имя сервера авторизации, который нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="4940a-145">Specifies the name of the authorization server to modify.</span></span>

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

### <span data-ttu-id="4940a-146">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4940a-146">-PassThru</span></span>
<span data-ttu-id="4940a-147">PassThru</span><span class="sxs-lookup"><span data-stu-id="4940a-147">passthru</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4940a-148">-ResourceOwnerPassword</span><span class="sxs-lookup"><span data-stu-id="4940a-148">-ResourceOwnerPassword</span></span>
<span data-ttu-id="4940a-149">Указывает пароль владельца ресурса.</span><span class="sxs-lookup"><span data-stu-id="4940a-149">Specifies the resource owner password.</span></span>
<span data-ttu-id="4940a-150">Этот параметр необходимо указывать, если параметр ResourceOwnerPassword указан с помощью параметра *GrantTypes* .</span><span class="sxs-lookup"><span data-stu-id="4940a-150">You must specify this parameter if ResourceOwnerPassword is specified by the *GrantTypes* parameter.</span></span>

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

### <span data-ttu-id="4940a-151">-ResourceOwnerUsername</span><span class="sxs-lookup"><span data-stu-id="4940a-151">-ResourceOwnerUsername</span></span>
<span data-ttu-id="4940a-152">Указывает имя пользователя, владеющего ресурсом.</span><span class="sxs-lookup"><span data-stu-id="4940a-152">Specifies the resource owner user name.</span></span>
<span data-ttu-id="4940a-153">Этот параметр необходимо указывать, если параметр ResourceOwnerPassword указан с помощью параметра *GrantTypes* .</span><span class="sxs-lookup"><span data-stu-id="4940a-153">You must specify this parameter if ResourceOwnerPassword is specified by the *GrantTypes* parameter.</span></span>

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

### <span data-ttu-id="4940a-154">-ServerId</span><span class="sxs-lookup"><span data-stu-id="4940a-154">-ServerId</span></span>
<span data-ttu-id="4940a-155">Указывает идентификатор сервера авторизации, который нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="4940a-155">Specifies the ID of the authorization server to modify.</span></span>

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

### <span data-ttu-id="4940a-156">-SupportState</span><span class="sxs-lookup"><span data-stu-id="4940a-156">-SupportState</span></span>
<span data-ttu-id="4940a-157">Указывает, следует ли поддерживать параметр *State* .</span><span class="sxs-lookup"><span data-stu-id="4940a-157">Indicates whether to support the *State* parameter.</span></span>

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

### <span data-ttu-id="4940a-158">-TokenBodyParameters</span><span class="sxs-lookup"><span data-stu-id="4940a-158">-TokenBodyParameters</span></span>
<span data-ttu-id="4940a-159">Указывает дополнительные параметры тела, использующие формат Application/x-www-UrlEncoded.</span><span class="sxs-lookup"><span data-stu-id="4940a-159">Specifies additional body parameters using application/x-www-form-urlencoded format.</span></span>

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

### <span data-ttu-id="4940a-160">-TokenEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="4940a-160">-TokenEndpointUrl</span></span>
<span data-ttu-id="4940a-161">Задает конечную точку маркера для клиентов, чтобы получить доступ к данным о предоставлении авторизации или обновлении маркеров в Exchange.</span><span class="sxs-lookup"><span data-stu-id="4940a-161">Specifies the token endpoint for clients to obtain access tokens in exchange for presenting authorization grants or refresh tokens.</span></span>

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

### <span data-ttu-id="4940a-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4940a-162">CommonParameters</span></span>
<span data-ttu-id="4940a-163">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4940a-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4940a-164">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4940a-164">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4940a-165">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4940a-165">INPUTS</span></span>

### <span data-ttu-id="4940a-166">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="4940a-166">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="4940a-167">System. String</span><span class="sxs-lookup"><span data-stu-id="4940a-167">System.String</span></span>

### <span data-ttu-id="4940a-168">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementAuthorizationRequestMethod []</span><span class="sxs-lookup"><span data-stu-id="4940a-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAuthorizationRequestMethod[]</span></span>

### <span data-ttu-id="4940a-169">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementGrantType []</span><span class="sxs-lookup"><span data-stu-id="4940a-169">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGrantType[]</span></span>

### <span data-ttu-id="4940a-170">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementClientAuthenticationMethod []</span><span class="sxs-lookup"><span data-stu-id="4940a-170">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientAuthenticationMethod[]</span></span>

### <span data-ttu-id="4940a-171">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="4940a-171">System.Collections.Hashtable</span></span>

### <span data-ttu-id="4940a-172">System. Nullable "1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="4940a-172">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="4940a-173">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementAccessTokenSendingMethod []</span><span class="sxs-lookup"><span data-stu-id="4940a-173">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessTokenSendingMethod[]</span></span>

### <span data-ttu-id="4940a-174">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="4940a-174">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="4940a-175">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4940a-175">OUTPUTS</span></span>

### <span data-ttu-id="4940a-176">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementOAuth2AuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="4940a-176">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthorizationServer</span></span>

## <span data-ttu-id="4940a-177">Пуск</span><span class="sxs-lookup"><span data-stu-id="4940a-177">NOTES</span></span>

## <span data-ttu-id="4940a-178">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4940a-178">RELATED LINKS</span></span>

[<span data-ttu-id="4940a-179">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="4940a-179">Get-AzApiManagementAuthorizationServer</span></span>](./Get-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="4940a-180">New-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="4940a-180">New-AzApiManagementAuthorizationServer</span></span>](./New-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="4940a-181">Remove-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="4940a-181">Remove-AzApiManagementAuthorizationServer</span></span>](./Remove-AzApiManagementAuthorizationServer.md)



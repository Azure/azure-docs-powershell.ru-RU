---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 93005775-3AB9-43C5-B353-45B82124ADB7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementAuthorizationServer.md
ms.openlocfilehash: ed7043746aa5ce59e733737acf8da61bdb44b0a1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734281"
---
# <span data-ttu-id="a01e1-101">Set-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="a01e1-101">Set-AzureRmApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="a01e1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a01e1-102">SYNOPSIS</span></span>
<span data-ttu-id="a01e1-103">Изменение сервера авторизации.</span><span class="sxs-lookup"><span data-stu-id="a01e1-103">Modifies an authorization server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a01e1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a01e1-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementAuthorizationServer -Context <PsApiManagementContext> -ServerId <String> -Name <String>
 [-Description <String>] -ClientRegistrationPageUrl <String> -AuthorizationEndpointUrl <String>
 -TokenEndpointUrl <String> -ClientId <String> [-ClientSecret <String>]
 [-AuthorizationRequestMethods <PsApiManagementAuthorizationRequestMethod[]>]
 -GrantTypes <PsApiManagementGrantType[]>
 -ClientAuthenticationMethods <PsApiManagementClientAuthenticationMethod[]> [-TokenBodyParameters <Hashtable>]
 [-SupportState <Boolean>] [-DefaultScope <String>]
 -AccessTokenSendingMethods <PsApiManagementAccessTokenSendingMethod[]> [-ResourceOwnerUsername <String>]
 [-ResourceOwnerPassword <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a01e1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a01e1-105">DESCRIPTION</span></span>
<span data-ttu-id="a01e1-106">Командлет **Set-AzureRmApiManagementAuthorizationServer** изменяет сведения о сервере авторизации управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="a01e1-106">The **Set-AzureRmApiManagementAuthorizationServer** cmdlet modifies Azure API Management authorization server details.</span></span>

## <span data-ttu-id="a01e1-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a01e1-107">EXAMPLES</span></span>

### <span data-ttu-id="a01e1-108">Пример 1: изменение сервера авторизации</span><span class="sxs-lookup"><span data-stu-id="a01e1-108">Example 1: Modify an authorization server</span></span>
```
PS C:\>Set-AzureRmApiManagementAuthrizarionServer -Context $ApiMgmtContext -ServerId 0123456789 -Name "Contoso OAuth2 server" -ClientRegistrationPageUrl "https://contoso/signupv2" -AuthorizationEndpointUrl "https://contoso/authv2" -TokenEndpointUrl "https://contoso/tokenv2" -ClientId "clientid" -ClientSecret "e041ed1b660b4eadbad5a29d066e6e88" -AuthorizationRequestMethods @('Get') -GrantTypes @( 'AuthorizationCode', 'Implicit', 'ClientCredentials') -ClientAuthenticationMethods @('Basic') -TokenBodyParameters @{'par1'='val1'} -AccessTokenSendingMethods @('AuthorizationHeader')
```

<span data-ttu-id="a01e1-109">Эта команда изменяет указанный сервер авторизации управления API.</span><span class="sxs-lookup"><span data-stu-id="a01e1-109">This command modifies the specified API Management authorization server.</span></span>

## <span data-ttu-id="a01e1-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a01e1-110">PARAMETERS</span></span>

### <span data-ttu-id="a01e1-111">-AccessTokenSendingMethods</span><span class="sxs-lookup"><span data-stu-id="a01e1-111">-AccessTokenSendingMethods</span></span>
<span data-ttu-id="a01e1-112">Указывает массив методов для отправки маркера доступа.</span><span class="sxs-lookup"><span data-stu-id="a01e1-112">Specifies an array of methods to send an access token.</span></span>
<span data-ttu-id="a01e1-113">psdx_paramvalues AuthorizationHeader и Query.</span><span class="sxs-lookup"><span data-stu-id="a01e1-113">psdx_paramvalues AuthorizationHeader and Query.</span></span>

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

### <span data-ttu-id="a01e1-114">-AuthorizationEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="a01e1-114">-AuthorizationEndpointUrl</span></span>
<span data-ttu-id="a01e1-115">Указывает конечную точку авторизации для проверки подлинности владельцев ресурсов и получения разрешений на авторизацию.</span><span class="sxs-lookup"><span data-stu-id="a01e1-115">Specifies the authorization endpoint to authenticate resource owners and obtain authorization grants.</span></span>

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

### <span data-ttu-id="a01e1-116">-AuthorizationRequestMethods</span><span class="sxs-lookup"><span data-stu-id="a01e1-116">-AuthorizationRequestMethods</span></span>
<span data-ttu-id="a01e1-117">Указывает массив методов запроса авторизации.</span><span class="sxs-lookup"><span data-stu-id="a01e1-117">Specifies an array of authorization request methods.</span></span>
<span data-ttu-id="a01e1-118">psdx_paramvalues GET и POST.</span><span class="sxs-lookup"><span data-stu-id="a01e1-118">psdx_paramvalues GET and POST.</span></span>
<span data-ttu-id="a01e1-119">Значением по умолчанию является GET.</span><span class="sxs-lookup"><span data-stu-id="a01e1-119">The default value is GET.</span></span>

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

### <span data-ttu-id="a01e1-120">-ClientAuthenticationMethods</span><span class="sxs-lookup"><span data-stu-id="a01e1-120">-ClientAuthenticationMethods</span></span>
<span data-ttu-id="a01e1-121">Задает массив методов проверки подлинности клиента.</span><span class="sxs-lookup"><span data-stu-id="a01e1-121">Specifies an array of client authentication methods.</span></span>
<span data-ttu-id="a01e1-122">psdx_paramvalues основного и основного текста.</span><span class="sxs-lookup"><span data-stu-id="a01e1-122">psdx_paramvalues Basic and Body.</span></span>

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

### <span data-ttu-id="a01e1-123">-ClientId</span><span class="sxs-lookup"><span data-stu-id="a01e1-123">-ClientId</span></span>
<span data-ttu-id="a01e1-124">Указывает идентификатор клиента для консоли разработчика, которая является клиентским приложением.</span><span class="sxs-lookup"><span data-stu-id="a01e1-124">Specifies the client ID of the developer console that is the client application.</span></span>

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

### <span data-ttu-id="a01e1-125">-ClientRegistrationPageUrl</span><span class="sxs-lookup"><span data-stu-id="a01e1-125">-ClientRegistrationPageUrl</span></span>
<span data-ttu-id="a01e1-126">Задает конечную точку регистрации клиента для регистрации клиентов с помощью сервера авторизации и получения учетных данных клиента.</span><span class="sxs-lookup"><span data-stu-id="a01e1-126">Specifies the client registration endpoint to register clients with the authorization server and obtain client credentials.</span></span>

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

### <span data-ttu-id="a01e1-127">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="a01e1-127">-ClientSecret</span></span>
<span data-ttu-id="a01e1-128">Указывает секретный ключ клиента для консоли разработчика, которая является клиентским приложением.</span><span class="sxs-lookup"><span data-stu-id="a01e1-128">Specifies the client secret of the developer console that is the client application.</span></span>

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

### <span data-ttu-id="a01e1-129">-Context</span><span class="sxs-lookup"><span data-stu-id="a01e1-129">-Context</span></span>
<span data-ttu-id="a01e1-130">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="a01e1-130">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="a01e1-131">-DefaultScope</span><span class="sxs-lookup"><span data-stu-id="a01e1-131">-DefaultScope</span></span>
<span data-ttu-id="a01e1-132">Задает область по умолчанию для сервера авторизации.</span><span class="sxs-lookup"><span data-stu-id="a01e1-132">Specifies the default scope for the authorization server.</span></span>

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

### <span data-ttu-id="a01e1-133">-Описание</span><span class="sxs-lookup"><span data-stu-id="a01e1-133">-Description</span></span>
<span data-ttu-id="a01e1-134">Задает описание сервера авторизации.</span><span class="sxs-lookup"><span data-stu-id="a01e1-134">Specifies a description for an authorization server.</span></span>

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

### <span data-ttu-id="a01e1-135">-GrantTypes</span><span class="sxs-lookup"><span data-stu-id="a01e1-135">-GrantTypes</span></span>
<span data-ttu-id="a01e1-136">Указывает массив типов субсидий.</span><span class="sxs-lookup"><span data-stu-id="a01e1-136">Specifies an array of grant types.</span></span>
<span data-ttu-id="a01e1-137">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="a01e1-137">psdx_paramvalues</span></span>

- <span data-ttu-id="a01e1-138">AuthorizationCode</span><span class="sxs-lookup"><span data-stu-id="a01e1-138">AuthorizationCode</span></span>
- <span data-ttu-id="a01e1-139">ClientCredentials</span><span class="sxs-lookup"><span data-stu-id="a01e1-139">ClientCredentials</span></span> 
- <span data-ttu-id="a01e1-140">Согласия</span><span class="sxs-lookup"><span data-stu-id="a01e1-140">Implicit</span></span> 
- <span data-ttu-id="a01e1-141">ResourceOwnerPassword</span><span class="sxs-lookup"><span data-stu-id="a01e1-141">ResourceOwnerPassword</span></span>

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

### <span data-ttu-id="a01e1-142">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a01e1-142">-Name</span></span>
<span data-ttu-id="a01e1-143">Указывает имя сервера авторизации, который нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="a01e1-143">Specifies the name of the authorization server to modify.</span></span>

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

### <span data-ttu-id="a01e1-144">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a01e1-144">-PassThru</span></span>
<span data-ttu-id="a01e1-145">PassThru</span><span class="sxs-lookup"><span data-stu-id="a01e1-145">passthru</span></span>

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

### <span data-ttu-id="a01e1-146">-ResourceOwnerPassword</span><span class="sxs-lookup"><span data-stu-id="a01e1-146">-ResourceOwnerPassword</span></span>
<span data-ttu-id="a01e1-147">Указывает пароль владельца ресурса.</span><span class="sxs-lookup"><span data-stu-id="a01e1-147">Specifies the resource owner password.</span></span>
<span data-ttu-id="a01e1-148">Этот параметр необходимо указывать, если параметр ResourceOwnerPassword указан с помощью параметра *GrantTypes* .</span><span class="sxs-lookup"><span data-stu-id="a01e1-148">You must specify this parameter if ResourceOwnerPassword is specified by the *GrantTypes* parameter.</span></span>

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

### <span data-ttu-id="a01e1-149">-ResourceOwnerUsername</span><span class="sxs-lookup"><span data-stu-id="a01e1-149">-ResourceOwnerUsername</span></span>
<span data-ttu-id="a01e1-150">Указывает имя пользователя, владеющего ресурсом.</span><span class="sxs-lookup"><span data-stu-id="a01e1-150">Specifies the resource owner user name.</span></span>
<span data-ttu-id="a01e1-151">Этот параметр необходимо указывать, если параметр ResourceOwnerPassword указан с помощью параметра *GrantTypes* .</span><span class="sxs-lookup"><span data-stu-id="a01e1-151">You must specify this parameter if ResourceOwnerPassword is specified by the *GrantTypes* parameter.</span></span>

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

### <span data-ttu-id="a01e1-152">-ServerId</span><span class="sxs-lookup"><span data-stu-id="a01e1-152">-ServerId</span></span>
<span data-ttu-id="a01e1-153">Указывает идентификатор сервера авторизации, который нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="a01e1-153">Specifies the ID of the authorization server to modify.</span></span>

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

### <span data-ttu-id="a01e1-154">-SupportState</span><span class="sxs-lookup"><span data-stu-id="a01e1-154">-SupportState</span></span>
<span data-ttu-id="a01e1-155">Указывает, следует ли поддерживать параметр *State* .</span><span class="sxs-lookup"><span data-stu-id="a01e1-155">Indicates whether to support the *State* parameter.</span></span>

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

### <span data-ttu-id="a01e1-156">-TokenBodyParameters</span><span class="sxs-lookup"><span data-stu-id="a01e1-156">-TokenBodyParameters</span></span>
<span data-ttu-id="a01e1-157">Указывает дополнительные параметры тела, использующие формат Application/x-www-UrlEncoded.</span><span class="sxs-lookup"><span data-stu-id="a01e1-157">Specifies additional body parameters using application/x-www-form-urlencoded format.</span></span>

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

### <span data-ttu-id="a01e1-158">-TokenEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="a01e1-158">-TokenEndpointUrl</span></span>
<span data-ttu-id="a01e1-159">Задает конечную точку маркера для клиентов, чтобы получить доступ к данным о предоставлении авторизации или обновлении маркеров в Exchange.</span><span class="sxs-lookup"><span data-stu-id="a01e1-159">Specifies the token endpoint for clients to obtain access tokens in exchange for presenting authorization grants or refresh tokens.</span></span>

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

### <span data-ttu-id="a01e1-160">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a01e1-160">-DefaultProfile</span></span>
<span data-ttu-id="a01e1-161">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a01e1-161">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a01e1-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a01e1-162">CommonParameters</span></span>
<span data-ttu-id="a01e1-163">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a01e1-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a01e1-164">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a01e1-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a01e1-165">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a01e1-165">INPUTS</span></span>

## <span data-ttu-id="a01e1-166">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a01e1-166">OUTPUTS</span></span>

### <span data-ttu-id="a01e1-167">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementOAuth2AuthrozationServer</span><span class="sxs-lookup"><span data-stu-id="a01e1-167">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthrozationServer</span></span>

## <span data-ttu-id="a01e1-168">Пуск</span><span class="sxs-lookup"><span data-stu-id="a01e1-168">NOTES</span></span>

## <span data-ttu-id="a01e1-169">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a01e1-169">RELATED LINKS</span></span>

[<span data-ttu-id="a01e1-170">Get-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="a01e1-170">Get-AzureRmApiManagementAuthorizationServer</span></span>](./Get-AzureRmApiManagementAuthorizationServer.md)

[<span data-ttu-id="a01e1-171">New-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="a01e1-171">New-AzureRmApiManagementAuthorizationServer</span></span>](./New-AzureRmApiManagementAuthorizationServer.md)

[<span data-ttu-id="a01e1-172">Remove-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="a01e1-172">Remove-AzureRmApiManagementAuthorizationServer</span></span>](./Remove-AzureRmApiManagementAuthorizationServer.md)



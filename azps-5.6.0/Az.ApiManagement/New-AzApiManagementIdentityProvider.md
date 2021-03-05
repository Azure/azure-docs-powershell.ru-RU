---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementIdentityProvider.md
ms.openlocfilehash: 31a635c5965d40cf12e77d556e987c08dfb7175a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993082"
---
# <span data-ttu-id="9b02f-101">New-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="9b02f-101">New-AzApiManagementIdentityProvider</span></span>

## <span data-ttu-id="9b02f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b02f-102">SYNOPSIS</span></span>
<span data-ttu-id="9b02f-103">Создает новую конфигурацию поставщика удостоверений.</span><span class="sxs-lookup"><span data-stu-id="9b02f-103">Creates a new Identity Provider configuration.</span></span>

## <span data-ttu-id="9b02f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9b02f-104">SYNTAX</span></span>

```
New-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> -ClientId <String> -ClientSecret <String>
 [-AllowedTenants <String[]>] [-Authority <String>] [-SignupPolicyName <String>] [-SigninPolicyName <String>]
 [-ProfileEditingPolicyName <String>] [-PasswordResetPolicyName <String>] [-SigninTenant <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b02f-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9b02f-105">DESCRIPTION</span></span>
<span data-ttu-id="9b02f-106">Создает новую конфигурацию поставщика удостоверений.</span><span class="sxs-lookup"><span data-stu-id="9b02f-106">Creates a new Identity Provider configuration.</span></span>

## <span data-ttu-id="9b02f-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9b02f-107">EXAMPLES</span></span>

### <span data-ttu-id="9b02f-108">Пример 1. Настройка Facebook в качестве поставщика удостоверений для входа на портал разработчика</span><span class="sxs-lookup"><span data-stu-id="9b02f-108">Example 1: Configures Facebook as an identity Provider for Developer Portal Logins</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementIdentityProvider -Context $apimContext -Type 'Facebook' -ClientId 'sdfsfwerwerw' -ClientSecret 'sdgsdfgfst43tewfewrf'
```

<span data-ttu-id="9b02f-109">Эта команда настраивает Facebook Identity в качестве поставщика удостоверений, принятого на портале разработчика службы ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="9b02f-109">This command configures Facebook Identity as a accepted Identity Provider on the Developer Portal of the ApiManagement service.</span></span>
<span data-ttu-id="9b02f-110">Он принимает входные данные ClientId и ClientSecret приложения Facebook.</span><span class="sxs-lookup"><span data-stu-id="9b02f-110">This takes as input the ClientId and ClientSecret of the Facebook app.</span></span>

### <span data-ttu-id="9b02f-111">Пример 2. Настройка adB2C в качестве поставщика удостоверений для входа на портал разработчика</span><span class="sxs-lookup"><span data-stu-id="9b02f-111">Example 2: Configures adB2C as an identity Provider for Developer Portal Logins</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementIdentityProvider -Context $context -Type AadB2C -ClientId 6b1fc750-9e68-450c-97d2-ba6acd0fbc20 -ClientSecret "foobar" -AllowedTenants 'samirtestbc.onmicrosoft.com' -SignupPolicyName B2C_1_signup-policy

Type                     : AadB2C
ClientId                 : 6b1fc750-9e68-450c-97d2-ba6acd0fbc20
ClientSecret             : foobar
AllowedTenants           : {samirtestbc.onmicrosoft.com}
Authority                : login.microsoftonline.com
SignupPolicyName         : B2C_1_signup-policy
SigninPolicyName         :
ProfileEditingPolicyName :
PasswordResetPolicyName  :
Id                       : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/identityProviders/AadB2C
ResourceGroupName        : Api-Default-WestUS
ServiceName              : contoso
```

<span data-ttu-id="9b02f-112">Эта команда настраивает Facebook Identity в качестве поставщика удостоверений, принятого на портале разработчика службы ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="9b02f-112">This command configures Facebook Identity as a accepted Identity Provider on the Developer Portal of the ApiManagement service.</span></span>
<span data-ttu-id="9b02f-113">Он принимает входные данные ClientId и ClientSecret приложения Facebook.</span><span class="sxs-lookup"><span data-stu-id="9b02f-113">This takes as input the ClientId and ClientSecret of the Facebook app.</span></span>

## <span data-ttu-id="9b02f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9b02f-114">PARAMETERS</span></span>

### <span data-ttu-id="9b02f-115">-AllowedTenants</span><span class="sxs-lookup"><span data-stu-id="9b02f-115">-AllowedTenants</span></span>
<span data-ttu-id="9b02f-116">Список разрешенных клиентов Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="9b02f-116">List of allowed Azure Active Directory Tenants</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b02f-117">-Authority</span><span class="sxs-lookup"><span data-stu-id="9b02f-117">-Authority</span></span>
<span data-ttu-id="9b02f-118">Имя точки обнаружения OpenID Connect для AAD или AAD B2C.</span><span class="sxs-lookup"><span data-stu-id="9b02f-118">OpenID Connect discovery endpoint hostname for AAD or AAD B2C.</span></span> <span data-ttu-id="9b02f-119">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="9b02f-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="9b02f-120">-ClientId</span><span class="sxs-lookup"><span data-stu-id="9b02f-120">-ClientId</span></span>
<span data-ttu-id="9b02f-121">Идентификатор клиента приложения во внешнем поставщике удостоверений.</span><span class="sxs-lookup"><span data-stu-id="9b02f-121">Client Id of the Application in the external Identity Provider.</span></span>
<span data-ttu-id="9b02f-122">Это ИД приложения для входа в Facebook, ИД клиента для входа Google, ИД приложения для Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="9b02f-122">It is App ID for Facebook login, Client ID for Google login, App ID for Microsoft.</span></span>

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

### <span data-ttu-id="9b02f-123">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="9b02f-123">-ClientSecret</span></span>
<span data-ttu-id="9b02f-124">Секрет клиента приложения во внешнем поставщике удостоверений, используемого для проверки подлинности запроса на вход.</span><span class="sxs-lookup"><span data-stu-id="9b02f-124">Client secret of the Application in external Identity Provider, used to authenticate login request.</span></span>
<span data-ttu-id="9b02f-125">Например, это "Секрет приложения" для входа в Facebook, ключ API для входа в Google, общедоступный ключ для Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="9b02f-125">For example, it is App Secret for Facebook login, API Key for Google login, Public Key for Microsoft.</span></span>

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

### <span data-ttu-id="9b02f-126">-Контекст</span><span class="sxs-lookup"><span data-stu-id="9b02f-126">-Context</span></span>
<span data-ttu-id="9b02f-127">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="9b02f-127">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="9b02f-128">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="9b02f-128">This parameter is required.</span></span>

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

### <span data-ttu-id="9b02f-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b02f-129">-DefaultProfile</span></span>
<span data-ttu-id="9b02f-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9b02f-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9b02f-131">-PasswordResetPolicyName</span><span class="sxs-lookup"><span data-stu-id="9b02f-131">-PasswordResetPolicyName</span></span>
<span data-ttu-id="9b02f-132">Имя политики сброса пароля.</span><span class="sxs-lookup"><span data-stu-id="9b02f-132">Password Reset Policy Name.</span></span> <span data-ttu-id="9b02f-133">Применимо только к поставщику удостоверений AAD B2C.</span><span class="sxs-lookup"><span data-stu-id="9b02f-133">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="9b02f-134">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="9b02f-134">This parameter is optional.</span></span>

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

### <span data-ttu-id="9b02f-135">-ProfileEditingPolicyName</span><span class="sxs-lookup"><span data-stu-id="9b02f-135">-ProfileEditingPolicyName</span></span>
<span data-ttu-id="9b02f-136">Имя политики редактирования профиля.</span><span class="sxs-lookup"><span data-stu-id="9b02f-136">Profile Editing Policy Name.</span></span> <span data-ttu-id="9b02f-137">Применимо только к поставщику удостоверений AAD B2C.</span><span class="sxs-lookup"><span data-stu-id="9b02f-137">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="9b02f-138">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="9b02f-138">This parameter is optional.</span></span>

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

### <span data-ttu-id="9b02f-139">-SigninPolicyName</span><span class="sxs-lookup"><span data-stu-id="9b02f-139">-SigninPolicyName</span></span>
<span data-ttu-id="9b02f-140">Имя политики регистрации.</span><span class="sxs-lookup"><span data-stu-id="9b02f-140">Signin Policy Name.</span></span> <span data-ttu-id="9b02f-141">Применимо только к поставщику удостоверений AAD B2C.</span><span class="sxs-lookup"><span data-stu-id="9b02f-141">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="9b02f-142">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="9b02f-142">This parameter is optional.</span></span>

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

### <span data-ttu-id="9b02f-143">-SigninTenant</span><span class="sxs-lookup"><span data-stu-id="9b02f-143">-SigninTenant</span></span>
<span data-ttu-id="9b02f-144">Переопределения клиента в AAD B2C вместо `common` клиента</span><span class="sxs-lookup"><span data-stu-id="9b02f-144">Signin Tenant to override in AAD B2C instead of the `common` Tenant</span></span>

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

### <span data-ttu-id="9b02f-145">-SignupPolicyName</span><span class="sxs-lookup"><span data-stu-id="9b02f-145">-SignupPolicyName</span></span>
<span data-ttu-id="9b02f-146">Имя политики регистрации.</span><span class="sxs-lookup"><span data-stu-id="9b02f-146">Signup Policy Name.</span></span> <span data-ttu-id="9b02f-147">Применимо только к поставщику удостоверений AAD B2C.</span><span class="sxs-lookup"><span data-stu-id="9b02f-147">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="9b02f-148">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="9b02f-148">This parameter is optional.</span></span>

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

### <span data-ttu-id="9b02f-149">-Type</span><span class="sxs-lookup"><span data-stu-id="9b02f-149">-Type</span></span>
<span data-ttu-id="9b02f-150">Идентификатор поставщика удостоверений.</span><span class="sxs-lookup"><span data-stu-id="9b02f-150">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="9b02f-151">Если он указан, будет пытаться найти конфигурацию поставщика удостоверений по идентификатору.</span><span class="sxs-lookup"><span data-stu-id="9b02f-151">If specified will try to find identity provider configuration by the identifier.</span></span>
<span data-ttu-id="9b02f-152">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="9b02f-152">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType
Parameter Sets: (All)
Aliases:
Accepted values: Facebook, Google, Microsoft, Twitter, Aad, AadB2C

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b02f-153">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9b02f-153">-Confirm</span></span>
<span data-ttu-id="9b02f-154">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="9b02f-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b02f-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b02f-155">-WhatIf</span></span>
<span data-ttu-id="9b02f-156">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9b02f-156">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9b02f-157">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="9b02f-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b02f-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b02f-158">CommonParameters</span></span>
<span data-ttu-id="9b02f-159">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b02f-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b02f-160">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9b02f-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b02f-161">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9b02f-161">INPUTS</span></span>

### <span data-ttu-id="9b02f-162">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="9b02f-162">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="9b02f-163">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="9b02f-163">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

### <span data-ttu-id="9b02f-164">System.String</span><span class="sxs-lookup"><span data-stu-id="9b02f-164">System.String</span></span>

### <span data-ttu-id="9b02f-165">System.String[]</span><span class="sxs-lookup"><span data-stu-id="9b02f-165">System.String[]</span></span>

## <span data-ttu-id="9b02f-166">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9b02f-166">OUTPUTS</span></span>

### <span data-ttu-id="9b02f-167">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="9b02f-167">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="9b02f-168">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9b02f-168">NOTES</span></span>

## <span data-ttu-id="9b02f-169">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9b02f-169">RELATED LINKS</span></span>

[<span data-ttu-id="9b02f-170">Get-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="9b02f-170">Get-AzApiManagementIdentityProvider</span></span>](./Get-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="9b02f-171">Remove-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="9b02f-171">Remove-AzApiManagementIdentityProvider</span></span>](./Remove-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="9b02f-172">Set-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="9b02f-172">Set-AzApiManagementIdentityProvider</span></span>](./Set-AzApiManagementIdentityProvider.md)

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementIdentityProvider.md
ms.openlocfilehash: 61d63a427b7c1e52f95f980dde505c27765dcd39
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066712"
---
# <span data-ttu-id="9b5c1-101">New-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="9b5c1-101">New-AzApiManagementIdentityProvider</span></span>

## <span data-ttu-id="9b5c1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9b5c1-102">SYNOPSIS</span></span>
<span data-ttu-id="9b5c1-103">Создает новую конфигурацию поставщика удостоверений.</span><span class="sxs-lookup"><span data-stu-id="9b5c1-103">Creates a new Identity Provider configuration.</span></span>

## <span data-ttu-id="9b5c1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9b5c1-104">SYNTAX</span></span>

```
New-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> -ClientId <String> -ClientSecret <String>
 [-AllowedTenants <String[]>] [-Authority <String>] [-SignupPolicyName <String>] [-SigninPolicyName <String>]
 [-ProfileEditingPolicyName <String>] [-PasswordResetPolicyName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b5c1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9b5c1-105">DESCRIPTION</span></span>
<span data-ttu-id="9b5c1-106">Создает новую конфигурацию поставщика удостоверений.</span><span class="sxs-lookup"><span data-stu-id="9b5c1-106">Creates a new Identity Provider configuration.</span></span>

## <span data-ttu-id="9b5c1-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9b5c1-107">EXAMPLES</span></span>

### <span data-ttu-id="9b5c1-108">Пример 1: Настройка Facebook в качестве поставщика удостоверений для входа на портал разработчика</span><span class="sxs-lookup"><span data-stu-id="9b5c1-108">Example 1: Configures Facebook as an identity Provider for Developer Portal Logins</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementIdentityProvider -Context $apimContext -Type 'Facebook' -ClientId 'sdfsfwerwerw' -ClientSecret 'sdgsdfgfst43tewfewrf'
```

<span data-ttu-id="9b5c1-109">Эта команда настраивает удостоверение Facebook как одобренного поставщика удостоверений на портале разработчика службы ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="9b5c1-109">This command configures Facebook Identity as a accepted Identity Provider on the Developer Portal of the ApiManagement service.</span></span>
<span data-ttu-id="9b5c1-110">Это берет на себя в качестве входных данных ClientId и ClientSecret приложения Facebook.</span><span class="sxs-lookup"><span data-stu-id="9b5c1-110">This takes as input the ClientId and ClientSecret of the Facebook app.</span></span>

### <span data-ttu-id="9b5c1-111">Пример 2: Настройка adB2C в качестве поставщика удостоверений для входа на портал разработчика</span><span class="sxs-lookup"><span data-stu-id="9b5c1-111">Example 2: Configures adB2C as an identity Provider for Developer Portal Logins</span></span>
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

<span data-ttu-id="9b5c1-112">Эта команда настраивает удостоверение Facebook как одобренного поставщика удостоверений на портале разработчика службы ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="9b5c1-112">This command configures Facebook Identity as a accepted Identity Provider on the Developer Portal of the ApiManagement service.</span></span>
<span data-ttu-id="9b5c1-113">Это берет на себя в качестве входных данных ClientId и ClientSecret приложения Facebook.</span><span class="sxs-lookup"><span data-stu-id="9b5c1-113">This takes as input the ClientId and ClientSecret of the Facebook app.</span></span>

## <span data-ttu-id="9b5c1-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9b5c1-114">PARAMETERS</span></span>

### <span data-ttu-id="9b5c1-115">-AllowedTenants</span><span class="sxs-lookup"><span data-stu-id="9b5c1-115">-AllowedTenants</span></span>
<span data-ttu-id="9b5c1-116">Список разрешенных клиентов Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="9b5c1-116">List of allowed Azure Active Directory Tenants</span></span>

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

### <span data-ttu-id="9b5c1-117">-Authority</span><span class="sxs-lookup"><span data-stu-id="9b5c1-117">-Authority</span></span>
<span data-ttu-id="9b5c1-118">Имя узла конечной точки обнаружения OpenID подключения для AAD или AAD B2C.</span><span class="sxs-lookup"><span data-stu-id="9b5c1-118">OpenID Connect discovery endpoint hostname for AAD or AAD B2C.</span></span> <span data-ttu-id="9b5c1-119">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="9b5c1-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="9b5c1-120">-ClientId</span><span class="sxs-lookup"><span data-stu-id="9b5c1-120">-ClientId</span></span>
<span data-ttu-id="9b5c1-121">Идентификатор клиента приложения в поставщике внешней идентификации.</span><span class="sxs-lookup"><span data-stu-id="9b5c1-121">Client Id of the Application in the external Identity Provider.</span></span>
<span data-ttu-id="9b5c1-122">Это идентификатор приложения для входа в Facebook, идентификатор клиента для входа в Google, идентификатор приложения для Microsoft.</span><span class="sxs-lookup"><span data-stu-id="9b5c1-122">It is App ID for Facebook login, Client ID for Google login, App ID for Microsoft.</span></span>

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

### <span data-ttu-id="9b5c1-123">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="9b5c1-123">-ClientSecret</span></span>
<span data-ttu-id="9b5c1-124">Секретный ключ клиента приложения во внешнем поставщике удостоверений, используемый для проверки подлинности запроса на вход.</span><span class="sxs-lookup"><span data-stu-id="9b5c1-124">Client secret of the Application in external Identity Provider, used to authenticate login request.</span></span>
<span data-ttu-id="9b5c1-125">Например, это конфиденциальное приложение для входа в Facebook, ключ API для входа в Google, Открытый ключ для Microsoft.</span><span class="sxs-lookup"><span data-stu-id="9b5c1-125">For example, it is App Secret for Facebook login, API Key for Google login, Public Key for Microsoft.</span></span>

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

### <span data-ttu-id="9b5c1-126">-Context</span><span class="sxs-lookup"><span data-stu-id="9b5c1-126">-Context</span></span>
<span data-ttu-id="9b5c1-127">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="9b5c1-127">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="9b5c1-128">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="9b5c1-128">This parameter is required.</span></span>

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

### <span data-ttu-id="9b5c1-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b5c1-129">-DefaultProfile</span></span>
<span data-ttu-id="9b5c1-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9b5c1-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9b5c1-131">-PasswordResetPolicyName</span><span class="sxs-lookup"><span data-stu-id="9b5c1-131">-PasswordResetPolicyName</span></span>
<span data-ttu-id="9b5c1-132">Имя политики сброса пароля.</span><span class="sxs-lookup"><span data-stu-id="9b5c1-132">Password Reset Policy Name.</span></span> <span data-ttu-id="9b5c1-133">Применимо только к поставщику удостоверений AAD B2C.</span><span class="sxs-lookup"><span data-stu-id="9b5c1-133">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="9b5c1-134">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="9b5c1-134">This parameter is optional.</span></span>

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

### <span data-ttu-id="9b5c1-135">-ProfileEditingPolicyName</span><span class="sxs-lookup"><span data-stu-id="9b5c1-135">-ProfileEditingPolicyName</span></span>
<span data-ttu-id="9b5c1-136">Имя политики редактирования профиля.</span><span class="sxs-lookup"><span data-stu-id="9b5c1-136">Profile Editing Policy Name.</span></span> <span data-ttu-id="9b5c1-137">Применимо только к поставщику удостоверений AAD B2C.</span><span class="sxs-lookup"><span data-stu-id="9b5c1-137">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="9b5c1-138">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="9b5c1-138">This parameter is optional.</span></span>

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

### <span data-ttu-id="9b5c1-139">-SigninPolicyName</span><span class="sxs-lookup"><span data-stu-id="9b5c1-139">-SigninPolicyName</span></span>
<span data-ttu-id="9b5c1-140">Имя политики входа.</span><span class="sxs-lookup"><span data-stu-id="9b5c1-140">Signin Policy Name.</span></span> <span data-ttu-id="9b5c1-141">Применимо только к поставщику удостоверений AAD B2C.</span><span class="sxs-lookup"><span data-stu-id="9b5c1-141">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="9b5c1-142">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="9b5c1-142">This parameter is optional.</span></span>

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

### <span data-ttu-id="9b5c1-143">-SignupPolicyName</span><span class="sxs-lookup"><span data-stu-id="9b5c1-143">-SignupPolicyName</span></span>
<span data-ttu-id="9b5c1-144">Имя политики регистрации.</span><span class="sxs-lookup"><span data-stu-id="9b5c1-144">Signup Policy Name.</span></span> <span data-ttu-id="9b5c1-145">Применимо только к поставщику удостоверений AAD B2C.</span><span class="sxs-lookup"><span data-stu-id="9b5c1-145">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="9b5c1-146">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="9b5c1-146">This parameter is optional.</span></span>

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

### <span data-ttu-id="9b5c1-147">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="9b5c1-147">-Type</span></span>
<span data-ttu-id="9b5c1-148">Идентификатор поставщика удостоверений.</span><span class="sxs-lookup"><span data-stu-id="9b5c1-148">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="9b5c1-149">Если задано значение, это попытается найти конфигурацию поставщика удостоверений с помощью идентификатора.</span><span class="sxs-lookup"><span data-stu-id="9b5c1-149">If specified will try to find identity provider configuration by the identifier.</span></span>
<span data-ttu-id="9b5c1-150">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="9b5c1-150">This parameter is optional.</span></span>

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

### <span data-ttu-id="9b5c1-151">-SigninTenant</span><span class="sxs-lookup"><span data-stu-id="9b5c1-151">-SigninTenant</span></span>
<span data-ttu-id="9b5c1-152">Переопределение клиента для входа в AAD B2C вместо `common` клиента</span><span class="sxs-lookup"><span data-stu-id="9b5c1-152">Signin Tenant to override in AAD B2C instead of the `common` Tenant</span></span>

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

### <span data-ttu-id="9b5c1-153">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9b5c1-153">-Confirm</span></span>
<span data-ttu-id="9b5c1-154">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9b5c1-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b5c1-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b5c1-155">-WhatIf</span></span>
<span data-ttu-id="9b5c1-156">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9b5c1-156">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9b5c1-157">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9b5c1-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b5c1-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b5c1-158">CommonParameters</span></span>
<span data-ttu-id="9b5c1-159">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9b5c1-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b5c1-160">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9b5c1-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b5c1-161">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9b5c1-161">INPUTS</span></span>

### <span data-ttu-id="9b5c1-162">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="9b5c1-162">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="9b5c1-163">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="9b5c1-163">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

### <span data-ttu-id="9b5c1-164">System. String</span><span class="sxs-lookup"><span data-stu-id="9b5c1-164">System.String</span></span>

### <span data-ttu-id="9b5c1-165">System. String []</span><span class="sxs-lookup"><span data-stu-id="9b5c1-165">System.String[]</span></span>

## <span data-ttu-id="9b5c1-166">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9b5c1-166">OUTPUTS</span></span>

### <span data-ttu-id="9b5c1-167">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="9b5c1-167">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="9b5c1-168">Пуск</span><span class="sxs-lookup"><span data-stu-id="9b5c1-168">NOTES</span></span>

## <span data-ttu-id="9b5c1-169">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9b5c1-169">RELATED LINKS</span></span>

[<span data-ttu-id="9b5c1-170">Get-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="9b5c1-170">Get-AzApiManagementIdentityProvider</span></span>](./Get-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="9b5c1-171">Remove-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="9b5c1-171">Remove-AzApiManagementIdentityProvider</span></span>](./Remove-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="9b5c1-172">Set-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="9b5c1-172">Set-AzApiManagementIdentityProvider</span></span>](./Set-AzApiManagementIdentityProvider.md)

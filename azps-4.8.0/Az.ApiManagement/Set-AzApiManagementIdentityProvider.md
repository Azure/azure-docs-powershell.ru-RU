---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementIdentityProvider.md
ms.openlocfilehash: 05bf93584fcc39f239877e2568cb88b243b1e820
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078536"
---
# <span data-ttu-id="4d0b0-101">Set-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="4d0b0-101">Set-AzApiManagementIdentityProvider</span></span>

## <span data-ttu-id="4d0b0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4d0b0-102">SYNOPSIS</span></span>
<span data-ttu-id="4d0b0-103">Обновляет конфигурацию существующего поставщика удостоверений.</span><span class="sxs-lookup"><span data-stu-id="4d0b0-103">Updates the Configuration of an existing Identity Provider.</span></span>

## <span data-ttu-id="4d0b0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4d0b0-104">SYNTAX</span></span>

### <span data-ttu-id="4d0b0-105">ExpandedParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4d0b0-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-ClientId <String>] [-ClientSecret <String>]
 [-AllowedTenants <String[]>] [-Authority <String>] [-SignupPolicyName <String>] [-SigninPolicyName <String>]
 [-ProfileEditingPolicyName <String>] [-PasswordResetPolicyName <String>] [-SigninTenant <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d0b0-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="4d0b0-106">ByInputObject</span></span>
```
Set-AzApiManagementIdentityProvider -InputObject <PsApiManagementIdentityProvider> [-ClientId <String>]
 [-ClientSecret <String>] [-AllowedTenants <String[]>] [-Authority <String>] [-SignupPolicyName <String>]
 [-SigninPolicyName <String>] [-ProfileEditingPolicyName <String>] [-PasswordResetPolicyName <String>]
 [-SigninTenant <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4d0b0-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4d0b0-107">DESCRIPTION</span></span>
<span data-ttu-id="4d0b0-108">Обновляет конфигурацию существующего поставщика удостоверений.</span><span class="sxs-lookup"><span data-stu-id="4d0b0-108">Updates the Configuration of an existing Identity Provider.</span></span>

## <span data-ttu-id="4d0b0-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4d0b0-109">EXAMPLES</span></span>

### <span data-ttu-id="4d0b0-110">Пример 1: обновление поставщика удостоверений Facebook</span><span class="sxs-lookup"><span data-stu-id="4d0b0-110">Example 1: Update the facebook Identity Provider</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> Set-AzApiManagementIdentityProvider -Context $apimContext -Type Facebook -ClientSecret "updatedSecret" -PassThru
```

<span data-ttu-id="4d0b0-111">Командлет обновляет секретный ключ клиента поставщика удостоверений Facebook;</span><span class="sxs-lookup"><span data-stu-id="4d0b0-111">The cmdlet updates the Client Secret of the Facebook Identity Provider;</span></span>

### <span data-ttu-id="4d0b0-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="4d0b0-112">Example 2</span></span>

<span data-ttu-id="4d0b0-113">Обновляет конфигурацию существующего поставщика удостоверений.</span><span class="sxs-lookup"><span data-stu-id="4d0b0-113">Updates the Configuration of an existing Identity Provider.</span></span> <span data-ttu-id="4d0b0-114">(автоматически сформированные)</span><span class="sxs-lookup"><span data-stu-id="4d0b0-114">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzApiManagementIdentityProvider -AllowedTenants 'samirtestbc.onmicrosoft.com' -Authority <String> -ClientId 'clientid' -ClientSecret 'updatedSecret' -Context <PsApiManagementContext> -PasswordResetPolicyName <String> -ProfileEditingPolicyName <String> -SigninPolicyName <String> -SignupPolicyName B2C_1_signup-policy -Type Facebook
```

## <span data-ttu-id="4d0b0-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4d0b0-115">PARAMETERS</span></span>

### <span data-ttu-id="4d0b0-116">-AllowedTenants</span><span class="sxs-lookup"><span data-stu-id="4d0b0-116">-AllowedTenants</span></span>
<span data-ttu-id="4d0b0-117">Список разрешенных клиентов Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="4d0b0-117">List of allowed Azure Active Directory Tenants.</span></span>

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

### <span data-ttu-id="4d0b0-118">-Authority</span><span class="sxs-lookup"><span data-stu-id="4d0b0-118">-Authority</span></span>
<span data-ttu-id="4d0b0-119">Имя узла конечной точки обнаружения OpenID подключения для AAD или AAD B2C.</span><span class="sxs-lookup"><span data-stu-id="4d0b0-119">OpenID Connect discovery endpoint hostname for AAD or AAD B2C.</span></span> <span data-ttu-id="4d0b0-120">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="4d0b0-120">This parameter is optional.</span></span>

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

### <span data-ttu-id="4d0b0-121">-ClientId</span><span class="sxs-lookup"><span data-stu-id="4d0b0-121">-ClientId</span></span>
<span data-ttu-id="4d0b0-122">Идентификатор клиента приложения в поставщике внешней идентификации.</span><span class="sxs-lookup"><span data-stu-id="4d0b0-122">Client Id of the Application in the external Identity Provider.</span></span>
<span data-ttu-id="4d0b0-123">Это идентификатор приложения для входа в Facebook, идентификатор клиента для входа в Google, идентификатор приложения для Microsoft.</span><span class="sxs-lookup"><span data-stu-id="4d0b0-123">It is App ID for Facebook login, Client ID for Google login, App ID for Microsoft.</span></span>

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

### <span data-ttu-id="4d0b0-124">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="4d0b0-124">-ClientSecret</span></span>
<span data-ttu-id="4d0b0-125">Секретный ключ клиента приложения во внешнем поставщике удостоверений, используемый для проверки подлинности запроса на вход.</span><span class="sxs-lookup"><span data-stu-id="4d0b0-125">Client secret of the Application in external Identity Provider, used to authenticate login request.</span></span>
<span data-ttu-id="4d0b0-126">Например, это конфиденциальное приложение для входа в Facebook, ключ API для входа в Google, Открытый ключ для Microsoft.</span><span class="sxs-lookup"><span data-stu-id="4d0b0-126">For example, it is App Secret for Facebook login, API Key for Google login, Public Key for Microsoft.</span></span>

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

### <span data-ttu-id="4d0b0-127">-Context</span><span class="sxs-lookup"><span data-stu-id="4d0b0-127">-Context</span></span>
<span data-ttu-id="4d0b0-128">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="4d0b0-128">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="4d0b0-129">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="4d0b0-129">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4d0b0-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d0b0-130">-DefaultProfile</span></span>
<span data-ttu-id="4d0b0-131">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4d0b0-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4d0b0-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4d0b0-132">-InputObject</span></span>
<span data-ttu-id="4d0b0-133">Экземпляр PsApiManagementIdentityProvider.</span><span class="sxs-lookup"><span data-stu-id="4d0b0-133">Instance of PsApiManagementIdentityProvider.</span></span> <span data-ttu-id="4d0b0-134">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="4d0b0-134">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4d0b0-135">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4d0b0-135">-PassThru</span></span>
<span data-ttu-id="4d0b0-136">Указывает на то, что этот командлет возвращает  **PsApiManagementIdentityProvider** , который изменяется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="4d0b0-136">Indicates that this cmdlet returns the  **PsApiManagementIdentityProvider** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="4d0b0-137">-PasswordResetPolicyName</span><span class="sxs-lookup"><span data-stu-id="4d0b0-137">-PasswordResetPolicyName</span></span>
<span data-ttu-id="4d0b0-138">Имя политики сброса пароля.</span><span class="sxs-lookup"><span data-stu-id="4d0b0-138">Password Reset Policy Name.</span></span> <span data-ttu-id="4d0b0-139">Применимо только к поставщику удостоверений AAD B2C.</span><span class="sxs-lookup"><span data-stu-id="4d0b0-139">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="4d0b0-140">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="4d0b0-140">This parameter is optional.</span></span>

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

### <span data-ttu-id="4d0b0-141">-ProfileEditingPolicyName</span><span class="sxs-lookup"><span data-stu-id="4d0b0-141">-ProfileEditingPolicyName</span></span>
<span data-ttu-id="4d0b0-142">Имя политики редактирования профиля.</span><span class="sxs-lookup"><span data-stu-id="4d0b0-142">Profile Editing Policy Name.</span></span> <span data-ttu-id="4d0b0-143">Применимо только к поставщику удостоверений AAD B2C.</span><span class="sxs-lookup"><span data-stu-id="4d0b0-143">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="4d0b0-144">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="4d0b0-144">This parameter is optional.</span></span>

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

### <span data-ttu-id="4d0b0-145">-SigninPolicyName</span><span class="sxs-lookup"><span data-stu-id="4d0b0-145">-SigninPolicyName</span></span>
<span data-ttu-id="4d0b0-146">Имя политики входа.</span><span class="sxs-lookup"><span data-stu-id="4d0b0-146">Signin Policy Name.</span></span> <span data-ttu-id="4d0b0-147">Применимо только к поставщику удостоверений AAD B2C.</span><span class="sxs-lookup"><span data-stu-id="4d0b0-147">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="4d0b0-148">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="4d0b0-148">This parameter is optional.</span></span>

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

### <span data-ttu-id="4d0b0-149">-SigninTenant</span><span class="sxs-lookup"><span data-stu-id="4d0b0-149">-SigninTenant</span></span>
<span data-ttu-id="4d0b0-150">Переопределение клиента для входа в AAD B2C вместо `common` клиента</span><span class="sxs-lookup"><span data-stu-id="4d0b0-150">Signin Tenant to override in AAD B2C instead of the `common` Tenant</span></span>

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

### <span data-ttu-id="4d0b0-151">-SignupPolicyName</span><span class="sxs-lookup"><span data-stu-id="4d0b0-151">-SignupPolicyName</span></span>
<span data-ttu-id="4d0b0-152">Имя политики регистрации.</span><span class="sxs-lookup"><span data-stu-id="4d0b0-152">Signup Policy Name.</span></span> <span data-ttu-id="4d0b0-153">Применимо только к поставщику удостоверений AAD B2C.</span><span class="sxs-lookup"><span data-stu-id="4d0b0-153">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="4d0b0-154">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="4d0b0-154">This parameter is optional.</span></span>

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

### <span data-ttu-id="4d0b0-155">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="4d0b0-155">-Type</span></span>
<span data-ttu-id="4d0b0-156">Идентификатор существующего поставщика удостоверений.</span><span class="sxs-lookup"><span data-stu-id="4d0b0-156">Identifier of an existing Identity Provider.</span></span>
<span data-ttu-id="4d0b0-157">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="4d0b0-157">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType
Parameter Sets: ExpandedParameter
Aliases:
Accepted values: Facebook, Google, Microsoft, Twitter, Aad, AadB2C

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d0b0-158">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4d0b0-158">-Confirm</span></span>
<span data-ttu-id="4d0b0-159">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4d0b0-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d0b0-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d0b0-160">-WhatIf</span></span>
<span data-ttu-id="4d0b0-161">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4d0b0-161">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4d0b0-162">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4d0b0-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d0b0-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d0b0-163">CommonParameters</span></span>
<span data-ttu-id="4d0b0-164">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4d0b0-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d0b0-165">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4d0b0-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d0b0-166">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4d0b0-166">INPUTS</span></span>

### <span data-ttu-id="4d0b0-167">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="4d0b0-167">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="4d0b0-168">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="4d0b0-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

### <span data-ttu-id="4d0b0-169">System. String</span><span class="sxs-lookup"><span data-stu-id="4d0b0-169">System.String</span></span>

### <span data-ttu-id="4d0b0-170">System. String []</span><span class="sxs-lookup"><span data-stu-id="4d0b0-170">System.String[]</span></span>

### <span data-ttu-id="4d0b0-171">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="4d0b0-171">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="4d0b0-172">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4d0b0-172">OUTPUTS</span></span>

### <span data-ttu-id="4d0b0-173">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="4d0b0-173">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="4d0b0-174">Пуск</span><span class="sxs-lookup"><span data-stu-id="4d0b0-174">NOTES</span></span>

## <span data-ttu-id="4d0b0-175">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4d0b0-175">RELATED LINKS</span></span>

[<span data-ttu-id="4d0b0-176">New-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="4d0b0-176">New-AzApiManagementIdentityProvider</span></span>](./New-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="4d0b0-177">Get-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="4d0b0-177">Get-AzApiManagementIdentityProvider</span></span>](./Get-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="4d0b0-178">Remove-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="4d0b0-178">Remove-AzApiManagementIdentityProvider</span></span>](./Remove-AzApiManagementIdentityProvider.md)
---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementIdentityProvider.md
ms.openlocfilehash: d2d689c9df73f7cd9bb6df6a5153e9afa71cb39d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93727937"
---
# <span data-ttu-id="272aa-101">Set-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="272aa-101">Set-AzApiManagementIdentityProvider</span></span>

## <span data-ttu-id="272aa-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="272aa-102">SYNOPSIS</span></span>
<span data-ttu-id="272aa-103">Обновляет конфигурацию существующего поставщика удостоверений.</span><span class="sxs-lookup"><span data-stu-id="272aa-103">Updates the Configuration of an existing Identity Provider.</span></span>

## <span data-ttu-id="272aa-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="272aa-104">SYNTAX</span></span>

### <span data-ttu-id="272aa-105">ExpandedParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="272aa-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-ClientId <String>] [-ClientSecret <String>]
 [-AllowedTenants <String[]>] [-Authority <String>] [-SignupPolicyName <String>] [-SigninPolicyName <String>]
 [-ProfileEditingPolicyName <String>] [-PasswordResetPolicyName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="272aa-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="272aa-106">ByInputObject</span></span>
```
Set-AzApiManagementIdentityProvider -InputObject <PsApiManagementIdentityProvider> [-ClientId <String>]
 [-ClientSecret <String>] [-AllowedTenants <String[]>] [-Authority <String>] [-SignupPolicyName <String>]
 [-SigninPolicyName <String>] [-ProfileEditingPolicyName <String>] [-PasswordResetPolicyName <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="272aa-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="272aa-107">DESCRIPTION</span></span>
<span data-ttu-id="272aa-108">Обновляет конфигурацию существующего поставщика удостоверений.</span><span class="sxs-lookup"><span data-stu-id="272aa-108">Updates the Configuration of an existing Identity Provider.</span></span>

## <span data-ttu-id="272aa-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="272aa-109">EXAMPLES</span></span>

### <span data-ttu-id="272aa-110">Пример 1: обновление поставщика удостоверений Facebook</span><span class="sxs-lookup"><span data-stu-id="272aa-110">Example 1 : Update the facebook Identity Provider</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> Set-AzApiManagementIdentityProvider -Context $apimContext -Type Facebook -ClientSecret "updatedSecret" -PassThru
```

<span data-ttu-id="272aa-111">Командлет обновляет секретный ключ клиента поставщика удостоверений Facebook;</span><span class="sxs-lookup"><span data-stu-id="272aa-111">The cmdlet updates the Client Secret of the Facebook Identity Provider;</span></span>

## <span data-ttu-id="272aa-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="272aa-112">PARAMETERS</span></span>

### <span data-ttu-id="272aa-113">-AllowedTenants</span><span class="sxs-lookup"><span data-stu-id="272aa-113">-AllowedTenants</span></span>
<span data-ttu-id="272aa-114">Список разрешенных клиентов Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="272aa-114">List of allowed Azure Active Directory Tenants.</span></span>

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

### <span data-ttu-id="272aa-115">-Authority</span><span class="sxs-lookup"><span data-stu-id="272aa-115">-Authority</span></span>
<span data-ttu-id="272aa-116">Имя узла конечной точки обнаружения OpenID подключения для AAD или AAD B2C.</span><span class="sxs-lookup"><span data-stu-id="272aa-116">OpenID Connect discovery endpoint hostname for AAD or AAD B2C.</span></span> <span data-ttu-id="272aa-117">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="272aa-117">This parameter is optional.</span></span>

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

### <span data-ttu-id="272aa-118">-ClientId</span><span class="sxs-lookup"><span data-stu-id="272aa-118">-ClientId</span></span>
<span data-ttu-id="272aa-119">Идентификатор клиента приложения в поставщике внешней идентификации.</span><span class="sxs-lookup"><span data-stu-id="272aa-119">Client Id of the Application in the external Identity Provider.</span></span>
<span data-ttu-id="272aa-120">Это идентификатор приложения для входа в Facebook, идентификатор клиента для входа в Google, идентификатор приложения для Microsoft.</span><span class="sxs-lookup"><span data-stu-id="272aa-120">It is App ID for Facebook login, Client ID for Google login, App ID for Microsoft.</span></span>

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

### <span data-ttu-id="272aa-121">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="272aa-121">-ClientSecret</span></span>
<span data-ttu-id="272aa-122">Секретный ключ клиента приложения во внешнем поставщике удостоверений, используемый для проверки подлинности запроса на вход.</span><span class="sxs-lookup"><span data-stu-id="272aa-122">Client secret of the Application in external Identity Provider, used to authenticate login request.</span></span>
<span data-ttu-id="272aa-123">Например, это конфиденциальное приложение для входа в Facebook, ключ API для входа в Google, Открытый ключ для Microsoft.</span><span class="sxs-lookup"><span data-stu-id="272aa-123">For example, it is App Secret for Facebook login, API Key for Google login, Public Key for Microsoft.</span></span>

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

### <span data-ttu-id="272aa-124">-Context</span><span class="sxs-lookup"><span data-stu-id="272aa-124">-Context</span></span>
<span data-ttu-id="272aa-125">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="272aa-125">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="272aa-126">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="272aa-126">This parameter is required.</span></span>

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

### <span data-ttu-id="272aa-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="272aa-127">-DefaultProfile</span></span>
<span data-ttu-id="272aa-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="272aa-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="272aa-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="272aa-129">-InputObject</span></span>
<span data-ttu-id="272aa-130">Экземпляр PsApiManagementIdentityProvider.</span><span class="sxs-lookup"><span data-stu-id="272aa-130">Instance of PsApiManagementIdentityProvider.</span></span> <span data-ttu-id="272aa-131">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="272aa-131">This parameter is required.</span></span>

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

### <span data-ttu-id="272aa-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="272aa-132">-PassThru</span></span>
<span data-ttu-id="272aa-133">Указывает на то, что этот командлет возвращает  **PsApiManagementIdentityProvider** , который изменяется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="272aa-133">Indicates that this cmdlet returns the  **PsApiManagementIdentityProvider** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="272aa-134">-PasswordResetPolicyName</span><span class="sxs-lookup"><span data-stu-id="272aa-134">-PasswordResetPolicyName</span></span>
<span data-ttu-id="272aa-135">Имя политики сброса пароля.</span><span class="sxs-lookup"><span data-stu-id="272aa-135">Password Reset Policy Name.</span></span> <span data-ttu-id="272aa-136">Применимо только к поставщику удостоверений AAD B2C.</span><span class="sxs-lookup"><span data-stu-id="272aa-136">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="272aa-137">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="272aa-137">This parameter is optional.</span></span>

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

### <span data-ttu-id="272aa-138">-ProfileEditingPolicyName</span><span class="sxs-lookup"><span data-stu-id="272aa-138">-ProfileEditingPolicyName</span></span>
<span data-ttu-id="272aa-139">Имя политики редактирования профиля.</span><span class="sxs-lookup"><span data-stu-id="272aa-139">Profile Editing Policy Name.</span></span> <span data-ttu-id="272aa-140">Применимо только к поставщику удостоверений AAD B2C.</span><span class="sxs-lookup"><span data-stu-id="272aa-140">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="272aa-141">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="272aa-141">This parameter is optional.</span></span>

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

### <span data-ttu-id="272aa-142">-SigninPolicyName</span><span class="sxs-lookup"><span data-stu-id="272aa-142">-SigninPolicyName</span></span>
<span data-ttu-id="272aa-143">Имя политики входа.</span><span class="sxs-lookup"><span data-stu-id="272aa-143">Signin Policy Name.</span></span> <span data-ttu-id="272aa-144">Применимо только к поставщику удостоверений AAD B2C.</span><span class="sxs-lookup"><span data-stu-id="272aa-144">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="272aa-145">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="272aa-145">This parameter is optional.</span></span>

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

### <span data-ttu-id="272aa-146">-SignupPolicyName</span><span class="sxs-lookup"><span data-stu-id="272aa-146">-SignupPolicyName</span></span>
<span data-ttu-id="272aa-147">Имя политики регистрации.</span><span class="sxs-lookup"><span data-stu-id="272aa-147">Signup Policy Name.</span></span> <span data-ttu-id="272aa-148">Применимо только к поставщику удостоверений AAD B2C.</span><span class="sxs-lookup"><span data-stu-id="272aa-148">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="272aa-149">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="272aa-149">This parameter is optional.</span></span>

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

### <span data-ttu-id="272aa-150">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="272aa-150">-Type</span></span>
<span data-ttu-id="272aa-151">Идентификатор существующего поставщика удостоверений.</span><span class="sxs-lookup"><span data-stu-id="272aa-151">Identifier of an existing Identity Provider.</span></span>
<span data-ttu-id="272aa-152">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="272aa-152">This parameter is required.</span></span>

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

### <span data-ttu-id="272aa-153">-Confirm</span><span class="sxs-lookup"><span data-stu-id="272aa-153">-Confirm</span></span>
<span data-ttu-id="272aa-154">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="272aa-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="272aa-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="272aa-155">-WhatIf</span></span>
<span data-ttu-id="272aa-156">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="272aa-156">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="272aa-157">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="272aa-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="272aa-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="272aa-158">CommonParameters</span></span>
<span data-ttu-id="272aa-159">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="272aa-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="272aa-160">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="272aa-160">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="272aa-161">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="272aa-161">INPUTS</span></span>

### <span data-ttu-id="272aa-162">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="272aa-162">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="272aa-163">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="272aa-163">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

### <span data-ttu-id="272aa-164">System. String</span><span class="sxs-lookup"><span data-stu-id="272aa-164">System.String</span></span>

### <span data-ttu-id="272aa-165">System. String []</span><span class="sxs-lookup"><span data-stu-id="272aa-165">System.String[]</span></span>

### <span data-ttu-id="272aa-166">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="272aa-166">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="272aa-167">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="272aa-167">OUTPUTS</span></span>

### <span data-ttu-id="272aa-168">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="272aa-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="272aa-169">Пуск</span><span class="sxs-lookup"><span data-stu-id="272aa-169">NOTES</span></span>

## <span data-ttu-id="272aa-170">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="272aa-170">RELATED LINKS</span></span>

[<span data-ttu-id="272aa-171">New-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="272aa-171">New-AzApiManagementIdentityProvider</span></span>](./New-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="272aa-172">Get-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="272aa-172">Get-AzApiManagementIdentityProvider</span></span>](./Get-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="272aa-173">Remove-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="272aa-173">Remove-AzApiManagementIdentityProvider</span></span>](./Remove-AzApiManagementIdentityProvider.md)

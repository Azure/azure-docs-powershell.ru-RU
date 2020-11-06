---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Add-AzureRmAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Add-AzureRmAccount.md
ms.openlocfilehash: 11303438a50839bbe05139888cc665198ed09810
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568712"
---
# <span data-ttu-id="acec6-101">Add-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="acec6-101">Add-AzureRmAccount</span></span>

## <span data-ttu-id="acec6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="acec6-102">SYNOPSIS</span></span>
<span data-ttu-id="acec6-103">Добавляет учетную запись с проверкой подлинности, которая используется для запросов командлетов диспетчера ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="acec6-103">Adds an authenticated account to use for Azure Resource Manager cmdlet requests.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="acec6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="acec6-104">SYNTAX</span></span>

### <span data-ttu-id="acec6-105">UserWithSubscriptionId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="acec6-105">UserWithSubscriptionId (Default)</span></span>
```
Add-AzureRmAccount [-Environment <String>] [[-Credential] <PSCredential>] [-TenantId <String>]
 [-Subscription <String>] [-ContextName <String>] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="acec6-106">ServicePrincipalWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="acec6-106">ServicePrincipalWithSubscriptionId</span></span>
```
Add-AzureRmAccount [-Environment <String>] [-Credential] <PSCredential> [-ServicePrincipal] -TenantId <String>
 [-Subscription <String>] [-ContextName <String>] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="acec6-107">ServicePrincipalCertificateWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="acec6-107">ServicePrincipalCertificateWithSubscriptionId</span></span>
```
Add-AzureRmAccount [-Environment <String>] -CertificateThumbprint <String> -ApplicationId <String>
 [-ServicePrincipal] -TenantId <String> [-Subscription <String>] [-ContextName <String>] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="acec6-108">AccessTokenWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="acec6-108">AccessTokenWithSubscriptionId</span></span>
```
Add-AzureRmAccount [-Environment <String>] [-TenantId <String>] -AccessToken <String>
 [-GraphAccessToken <String>] [-KeyVaultAccessToken <String>] -AccountId <String> [-Subscription <String>]
 [-ContextName <String>] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="acec6-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="acec6-109">DESCRIPTION</span></span>
<span data-ttu-id="acec6-110">Командлет Add-AzureRmAcccount добавляет учетную запись Azure, прошедший проверку подлинности, для запросов командлетов Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="acec6-110">The Add-AzureRmAcccount cmdlet adds an authenticated Azure account to use for Azure Resource Manager cmdlet requests.</span></span>

<span data-ttu-id="acec6-111">Вы можете использовать эту учетную запись с проверкой подлинности только для командлетов Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="acec6-111">You can use this authenticated account only with Azure Resource Manager cmdlets.</span></span>
<span data-ttu-id="acec6-112">Чтобы добавить учетную запись, прошедший проверку подлинности, с помощью командлетов управления службами, используйте Add-AzureAccount или Import-AzurePublishSettingsFile.</span><span class="sxs-lookup"><span data-stu-id="acec6-112">To add an authenticated account for use with Service Management cmdlets, use the Add-AzureAccount or the Import-AzurePublishSettingsFile cmdlet.</span></span>

## <span data-ttu-id="acec6-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="acec6-113">EXAMPLES</span></span>

### <span data-ttu-id="acec6-114">Пример 1: Добавление учетной записи, требующей интерактивного входа</span><span class="sxs-lookup"><span data-stu-id="acec6-114">Example 1: Add an account that requires interactive login</span></span>
```
PS C:\>Add-AzureRmAccount
Account: azureuser@contoso.com
Environment: AzureCloud
Subscription: xxxx-xxxx-xxxx-xxxx
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="acec6-115">Эта команда добавляет учетную запись диспетчера ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="acec6-115">This command adds an Azure Resource Manager account.</span></span>

<span data-ttu-id="acec6-116">Чтобы запустить командлеты диспетчера ресурсов Azure с этой учетной записью, необходимо задать учетные данные учетной записи Майкрософт или идентификатора организации в запросе.</span><span class="sxs-lookup"><span data-stu-id="acec6-116">To run Azure Resource Manager cmdlets with this account, you must provide Microsoft account or organizational ID credentials at the prompt.</span></span>

<span data-ttu-id="acec6-117">Если для ваших учетных данных включена многофакторная проверка подлинности, вы должны войти в систему с помощью интерактивного режима или воспользоваться проверкой подлинности субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="acec6-117">If multi-factor authentication is enabled for your credentials, you must log in using the interactive option or use service principal authentication.</span></span>

### <span data-ttu-id="acec6-118">Пример 2: Добавление учетной записи, которая проходит проверку подлинности с учетными данными идентификатора Организации</span><span class="sxs-lookup"><span data-stu-id="acec6-118">Example 2: Add an account that authenticates with organizational ID credentials</span></span>
```
PS C:\>$Credential = Get-Credential
PS C:\> Add-AzureRmAccount -Credential $Credential
Account: azureuser@contoso.com
Environment: AzureChinaCloud
Subscription: xxxx-xxxx-xxxx-xxxx
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="acec6-119">Первая команда получает учетные данные пользователя, а затем сохраняет их в переменной $Credential.</span><span class="sxs-lookup"><span data-stu-id="acec6-119">The first command gets the user credentials, and then stores them in the $Credential variable.</span></span>

<span data-ttu-id="acec6-120">Вторая команда добавляет учетную запись диспетчера ресурсов Azure с учетными данными в $Credential.</span><span class="sxs-lookup"><span data-stu-id="acec6-120">The second command adds an Azure Resource Manager account with the credentials in $Credential.</span></span>

<span data-ttu-id="acec6-121">Эта учетная запись проходит проверку подлинности с помощью диспетчера ресурсов Azure с использованием учетных данных идентификатора организации.</span><span class="sxs-lookup"><span data-stu-id="acec6-121">This account authenticates with Azure Resource Manager using organizational ID credentials.</span></span>
<span data-ttu-id="acec6-122">Для запуска командлетов диспетчера ресурсов Azure с этой учетной записью нельзя использовать многофакторную проверку подлинности или учетные данные учетной записи Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="acec6-122">You cannot use multi-factor authentication or Microsoft account credentials to run Azure Resource Manager cmdlets with this account.</span></span>

### <span data-ttu-id="acec6-123">Пример 3: Добавление учетной записи, которая проходит проверку подлинности с учетными данными субъекта-службы</span><span class="sxs-lookup"><span data-stu-id="acec6-123">Example 3: Add an account that authenticates with service principal credentials</span></span>
```
PS C:\>$Credential = Get-Credential
PS C:\> Add-AzureRmAccount -Credential $Credential -Tenant "xxxx-xxxx-xxxx-xxxx" -ServicePrincipal
Account: xxxx-xxxx-xxxx-xxxx
Environment: AzureCloud
Subscription: yyyy-yyyy-yyyy-yyyy
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="acec6-124">Первая команда получает учетные данные пользователя, а затем сохраняет их в переменной $Credential.</span><span class="sxs-lookup"><span data-stu-id="acec6-124">The first command gets the user credentials, and then stores them in the $Credential variable.</span></span>

<span data-ttu-id="acec6-125">Вторая команда добавляет учетную запись диспетчера ресурсов Azure с учетными данными, хранящимися в $Credential для указанного клиента.</span><span class="sxs-lookup"><span data-stu-id="acec6-125">The second command adds an Azure Resource Manager account with the credentials stored in $Credential for the specified Tenant.</span></span>
<span data-ttu-id="acec6-126">Параметр ключа ServicePrincipal указывает, что учетная запись проходит проверку подлинности субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="acec6-126">The ServicePrincipal switch parameter indicates that the account authenticates as a service principal.</span></span>

### <span data-ttu-id="acec6-127">Пример 4: Добавление учетной записи для определенного клиента и подписки</span><span class="sxs-lookup"><span data-stu-id="acec6-127">Example 4: Add an account for a specific tenant and subscription</span></span>
```
PS C:\>Add-AzureRmAccount -Tenant "xxxx-xxxx-xxxx-xxxx" -SubscriptionId "yyyy-yyyy-yyyy-yyyy"
Account: pfuller@contoso.com
Environment: AzureCloud
Subscription: yyyy-yyyy-yyyy-yyyy
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="acec6-128">Эта команда добавляет учетную запись диспетчера ресурсов Azure для запуска командлетов для указанных клиентов и подписок по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="acec6-128">This command adds an Azure Resource Manager account to run cmdlets for the specified tenant and subscription by default.</span></span>

## <span data-ttu-id="acec6-129">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="acec6-129">PARAMETERS</span></span>

### <span data-ttu-id="acec6-130">-AccessToken</span><span class="sxs-lookup"><span data-stu-id="acec6-130">-AccessToken</span></span>
<span data-ttu-id="acec6-131">Задает маркер доступа.</span><span class="sxs-lookup"><span data-stu-id="acec6-131">Specifies an access token.</span></span>

```yaml
Type: System.String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acec6-132">-AccountId</span><span class="sxs-lookup"><span data-stu-id="acec6-132">-AccountId</span></span>
<span data-ttu-id="acec6-133">Идентификатор учетной записи для маркера доступа</span><span class="sxs-lookup"><span data-stu-id="acec6-133">Account Id for access token</span></span>

```yaml
Type: System.String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acec6-134">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="acec6-134">-ApplicationId</span></span>
<span data-ttu-id="acec6-135">УЧАСТНИКОВ</span><span class="sxs-lookup"><span data-stu-id="acec6-135">SPN</span></span>

```yaml
Type: System.String
Parameter Sets: ServicePrincipalCertificateWithSubscriptionId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acec6-136">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="acec6-136">-CertificateThumbprint</span></span>
<span data-ttu-id="acec6-137">Хэш сертификата (отпечаток)</span><span class="sxs-lookup"><span data-stu-id="acec6-137">Certificate Hash (Thumbprint)</span></span>

```yaml
Type: System.String
Parameter Sets: ServicePrincipalCertificateWithSubscriptionId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acec6-138">-ContextName</span><span class="sxs-lookup"><span data-stu-id="acec6-138">-ContextName</span></span>
<span data-ttu-id="acec6-139">Имя контекста по умолчанию из этого имени входа.</span><span class="sxs-lookup"><span data-stu-id="acec6-139">Name of the default context from this login.</span></span>  <span data-ttu-id="acec6-140">Вы сможете выбрать этот контекст по этому имени после входа.</span><span class="sxs-lookup"><span data-stu-id="acec6-140">You will be able to select this context by this name after login.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acec6-141">-Credential</span><span class="sxs-lookup"><span data-stu-id="acec6-141">-Credential</span></span>
<span data-ttu-id="acec6-142">Указывает объект PSCredential.</span><span class="sxs-lookup"><span data-stu-id="acec6-142">Specifies a PSCredential object.</span></span>
<span data-ttu-id="acec6-143">Для получения дополнительных сведений о объекте PSCredential введите Get-Help Get-credentials.</span><span class="sxs-lookup"><span data-stu-id="acec6-143">For more information about the PSCredential object, type Get-Help Get-Credential.</span></span>

<span data-ttu-id="acec6-144">Объект PSCredential предоставляет идентификатор пользователя и пароль для учетных данных идентификатора организации, а также идентификатор приложения и секрет для учетных данных субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="acec6-144">The PSCredential object provides the user ID and password for organizational ID credentials, or the application ID and secret for service principal credentials.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: UserWithSubscriptionId
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: ServicePrincipalWithSubscriptionId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acec6-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acec6-145">-DefaultProfile</span></span>
<span data-ttu-id="acec6-146">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="acec6-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="acec6-147">-Environment</span><span class="sxs-lookup"><span data-stu-id="acec6-147">-Environment</span></span>
<span data-ttu-id="acec6-148">Среда, содержащая учетную запись, в которую нужно войти</span><span class="sxs-lookup"><span data-stu-id="acec6-148">Environment containing the account to log into</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EnvironmentName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acec6-149">-Force</span><span class="sxs-lookup"><span data-stu-id="acec6-149">-Force</span></span>
<span data-ttu-id="acec6-150">Перезаписать существующий контекст с тем же именем, если таковое имеется.</span><span class="sxs-lookup"><span data-stu-id="acec6-150">Overwrite the existing context with the same name, if any.</span></span>

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

### <span data-ttu-id="acec6-151">-GraphAccessToken</span><span class="sxs-lookup"><span data-stu-id="acec6-151">-GraphAccessToken</span></span>
<span data-ttu-id="acec6-152">AccessToken для службы Graph</span><span class="sxs-lookup"><span data-stu-id="acec6-152">AccessToken for Graph Service</span></span>

```yaml
Type: System.String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acec6-153">-KeyVaultAccessToken</span><span class="sxs-lookup"><span data-stu-id="acec6-153">-KeyVaultAccessToken</span></span>
<span data-ttu-id="acec6-154">Служба AccessToken для KeyVault</span><span class="sxs-lookup"><span data-stu-id="acec6-154">AccessToken for KeyVault Service</span></span>

```yaml
Type: System.String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acec6-155">-Scope</span><span class="sxs-lookup"><span data-stu-id="acec6-155">-Scope</span></span>
<span data-ttu-id="acec6-156">Определяет область изменений контекста, например wheher изменения применяются только к процессу cusrrent или ко всем сеансам, запускаемым этим пользователем.</span><span class="sxs-lookup"><span data-stu-id="acec6-156">Determines the scope of context changes, for example, wheher changes apply only to the cusrrent process, or to all sessions started by this user.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases: 
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acec6-157">-ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="acec6-157">-ServicePrincipal</span></span>
<span data-ttu-id="acec6-158">Указывает, что учетная запись проходит проверку подлинности путем предоставления учетных данных субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="acec6-158">Indicates that this account authenticates by providing service principal credentials.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServicePrincipalWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acec6-159">-Подписка</span><span class="sxs-lookup"><span data-stu-id="acec6-159">-Subscription</span></span>
<span data-ttu-id="acec6-160">Имя или идентификатор подписки</span><span class="sxs-lookup"><span data-stu-id="acec6-160">Subscription Name or ID</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName, SubscriptionId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="acec6-161">-TenantId</span><span class="sxs-lookup"><span data-stu-id="acec6-161">-TenantId</span></span>
<span data-ttu-id="acec6-162">Имя или идентификатор необязательного клиента</span><span class="sxs-lookup"><span data-stu-id="acec6-162">Optional tenant name or ID</span></span>

```yaml
Type: System.String
Parameter Sets: UserWithSubscriptionId, AccessTokenWithSubscriptionId
Aliases: Domain

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ServicePrincipalWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionId
Aliases: Domain

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acec6-163">-Confirm</span><span class="sxs-lookup"><span data-stu-id="acec6-163">-Confirm</span></span>
<span data-ttu-id="acec6-164">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="acec6-164">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acec6-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="acec6-165">-WhatIf</span></span>
<span data-ttu-id="acec6-166">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="acec6-166">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="acec6-167">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="acec6-167">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acec6-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acec6-168">CommonParameters</span></span>
<span data-ttu-id="acec6-169">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="acec6-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acec6-170">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="acec6-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acec6-171">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="acec6-171">INPUTS</span></span>

### <span data-ttu-id="acec6-172">Подстрок</span><span class="sxs-lookup"><span data-stu-id="acec6-172">String</span></span>
<span data-ttu-id="acec6-173">Параметр "SubscriptionId" принимает значение типа String из конвейера.</span><span class="sxs-lookup"><span data-stu-id="acec6-173">Parameter 'SubscriptionId' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="acec6-174">Подстрок</span><span class="sxs-lookup"><span data-stu-id="acec6-174">String</span></span>
<span data-ttu-id="acec6-175">Параметр "SubscriptionName" принимает значение типа String из конвейера.</span><span class="sxs-lookup"><span data-stu-id="acec6-175">Parameter 'SubscriptionName' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="acec6-176">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="acec6-176">OUTPUTS</span></span>

### <span data-ttu-id="acec6-177">PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="acec6-177">PSAzureProfile</span></span>
<span data-ttu-id="acec6-178">Учетные данные, сведения о подписке, учетной записи и клиенте для пользователя, выполнившего вход.</span><span class="sxs-lookup"><span data-stu-id="acec6-178">Credentials, subscription, account, and tenant information for the logged in user.</span></span>

## <span data-ttu-id="acec6-179">Пуск</span><span class="sxs-lookup"><span data-stu-id="acec6-179">NOTES</span></span>

## <span data-ttu-id="acec6-180">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="acec6-180">RELATED LINKS</span></span>


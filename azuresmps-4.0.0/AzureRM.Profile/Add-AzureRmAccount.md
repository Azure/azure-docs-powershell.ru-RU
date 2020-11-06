---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 533982757e4ea953c1f5d07ba67ac70af2161a10
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93555504"
---
# <span data-ttu-id="e5c16-101">Add-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="e5c16-101">Add-AzureRmAccount</span></span>

## <span data-ttu-id="e5c16-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e5c16-102">SYNOPSIS</span></span>
<span data-ttu-id="e5c16-103">Добавляет учетную запись с проверкой подлинности, которая используется для запросов командлетов диспетчера ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="e5c16-103">Adds an authenticated account to use for Azure Resource Manager cmdlet requests.</span></span>

## <span data-ttu-id="e5c16-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e5c16-104">SYNTAX</span></span>

### <span data-ttu-id="e5c16-105">UserWithSubscriptionId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e5c16-105">UserWithSubscriptionId (Default)</span></span>
```
Add-AzureRmAccount [-Environment <String>] [[-Credential] <PSCredential>] [-TenantId <String>]
 [-SubscriptionId <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5c16-106">UserWithSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="e5c16-106">UserWithSubscriptionName</span></span>
```
Add-AzureRmAccount [-Environment <String>] [[-Credential] <PSCredential>] [-TenantId <String>]
 -SubscriptionName <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5c16-107">ServicePrincipalWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e5c16-107">ServicePrincipalWithSubscriptionId</span></span>
```
Add-AzureRmAccount [-Environment <String>] [-Credential] <PSCredential> [-ServicePrincipal] -TenantId <String>
 [-SubscriptionId <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5c16-108">ServicePrincipalWithSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="e5c16-108">ServicePrincipalWithSubscriptionName</span></span>
```
Add-AzureRmAccount [-Environment <String>] [-Credential] <PSCredential> [-ServicePrincipal] -TenantId <String>
 -SubscriptionName <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5c16-109">ServicePrincipalCertificateWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e5c16-109">ServicePrincipalCertificateWithSubscriptionId</span></span>
```
Add-AzureRmAccount [-Environment <String>] -CertificateThumbprint <String> -ApplicationId <String>
 [-ServicePrincipal] -TenantId <String> [-SubscriptionId <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5c16-110">ServicePrincipalCertificateWithSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="e5c16-110">ServicePrincipalCertificateWithSubscriptionName</span></span>
```
Add-AzureRmAccount [-Environment <String>] -CertificateThumbprint <String> -ApplicationId <String>
 [-ServicePrincipal] -TenantId <String> -SubscriptionName <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5c16-111">AccessTokenWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e5c16-111">AccessTokenWithSubscriptionId</span></span>
```
Add-AzureRmAccount [-Environment <String>] [-TenantId <String>] -AccessToken <String> -AccountId <String>
 [-SubscriptionId <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5c16-112">AccessTokenWithSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="e5c16-112">AccessTokenWithSubscriptionName</span></span>
```
Add-AzureRmAccount [-Environment <String>] [-TenantId <String>] -AccessToken <String> -AccountId <String>
 -SubscriptionName <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5c16-113">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e5c16-113">DESCRIPTION</span></span>
<span data-ttu-id="e5c16-114">Командлет Add-AzureRmAcccount добавляет учетную запись Azure, прошедший проверку подлинности, для запросов командлетов Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="e5c16-114">The Add-AzureRmAcccount cmdlet adds an authenticated Azure account to use for Azure Resource Manager cmdlet requests.</span></span>

<span data-ttu-id="e5c16-115">Вы можете использовать эту учетную запись с проверкой подлинности только для командлетов Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="e5c16-115">You can use this authenticated account only with Azure Resource Manager cmdlets.</span></span>
<span data-ttu-id="e5c16-116">Чтобы добавить учетную запись, прошедший проверку подлинности, с помощью командлетов управления службами, используйте Add-AzureAccount или Import-AzurePublishSettingsFile.</span><span class="sxs-lookup"><span data-stu-id="e5c16-116">To add an authenticated account for use with Service Management cmdlets, use the Add-AzureAccount or the Import-AzurePublishSettingsFile cmdlet.</span></span>

## <span data-ttu-id="e5c16-117">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e5c16-117">EXAMPLES</span></span>

### <span data-ttu-id="e5c16-118">Пример 1: Добавление учетной записи, требующей интерактивного входа</span><span class="sxs-lookup"><span data-stu-id="e5c16-118">Example 1: Add an account that requires interactive login</span></span>
```
PS C:\>Add-AzureRmAccount
Account: azureuser@contoso.com
Environment: AzureCloud
Subscription: xxxx-xxxx-xxxx-xxxx
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="e5c16-119">Эта команда добавляет учетную запись диспетчера ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="e5c16-119">This command adds an Azure Resource Manager account.</span></span>

<span data-ttu-id="e5c16-120">Чтобы запустить командлеты диспетчера ресурсов Azure с этой учетной записью, необходимо задать учетные данные учетной записи Майкрософт или идентификатора организации в запросе.</span><span class="sxs-lookup"><span data-stu-id="e5c16-120">To run Azure Resource Manager cmdlets with this account, you must provide Microsoft account or organizational ID credentials at the prompt.</span></span>

<span data-ttu-id="e5c16-121">Если для ваших учетных данных включена многофакторная проверка подлинности, вы должны войти в систему с помощью интерактивного режима или воспользоваться проверкой подлинности субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="e5c16-121">If multi-factor authentication is enabled for your credentials, you must log in using the interactive option or use service principal authentication.</span></span>

### <span data-ttu-id="e5c16-122">Пример 2: Добавление учетной записи, которая проходит проверку подлинности с учетными данными идентификатора Организации</span><span class="sxs-lookup"><span data-stu-id="e5c16-122">Example 2: Add an account that authenticates with organizational ID credentials</span></span>
```
PS C:\>$Credential = Get-Credential
PS C:\> Add-AzureRmAccount -Credential $Credential
Account: azureuser@contoso.com
Environment: AzureChinaCloud
Subscription: xxxx-xxxx-xxxx-xxxx
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="e5c16-123">Первая команда получает учетные данные пользователя, а затем сохраняет их в переменной $Credential.</span><span class="sxs-lookup"><span data-stu-id="e5c16-123">The first command gets the user credentials, and then stores them in the $Credential variable.</span></span>

<span data-ttu-id="e5c16-124">Вторая команда добавляет учетную запись диспетчера ресурсов Azure с учетными данными в $Credential.</span><span class="sxs-lookup"><span data-stu-id="e5c16-124">The second command adds an Azure Resource Manager account with the credentials in $Credential.</span></span>

<span data-ttu-id="e5c16-125">Эта учетная запись проходит проверку подлинности с помощью диспетчера ресурсов Azure с использованием учетных данных идентификатора организации.</span><span class="sxs-lookup"><span data-stu-id="e5c16-125">This account authenticates with Azure Resource Manager using organizational ID credentials.</span></span>
<span data-ttu-id="e5c16-126">Для запуска командлетов диспетчера ресурсов Azure с этой учетной записью нельзя использовать многофакторную проверку подлинности или учетные данные учетной записи Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="e5c16-126">You cannot use multi-factor authentication or Microsoft account credentials to run Azure Resource Manager cmdlets with this account.</span></span>

### <span data-ttu-id="e5c16-127">Пример 3: Добавление учетной записи, которая проходит проверку подлинности с учетными данными субъекта-службы</span><span class="sxs-lookup"><span data-stu-id="e5c16-127">Example 3: Add an account that authenticates with service principal credentials</span></span>
```
PS C:\>$Credential = Get-Credential
PS C:\> Add-AzureRmAccount -Credential $Credential -Tenant "xxxx-xxxx-xxxx-xxxx" -ServicePrincipal
Account: xxxx-xxxx-xxxx-xxxx
Environment: AzureCloud
Subscription: yyyy-yyyy-yyyy-yyyy
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="e5c16-128">Первая команда получает учетные данные пользователя, а затем сохраняет их в переменной $Credential.</span><span class="sxs-lookup"><span data-stu-id="e5c16-128">The first command gets the user credentials, and then stores them in the $Credential variable.</span></span>

<span data-ttu-id="e5c16-129">Вторая команда добавляет учетную запись диспетчера ресурсов Azure с учетными данными, хранящимися в $Credential для указанного клиента.</span><span class="sxs-lookup"><span data-stu-id="e5c16-129">The second command adds an Azure Resource Manager account with the credentials stored in $Credential for the specified Tenant.</span></span>
<span data-ttu-id="e5c16-130">Параметр ключа ServicePrincipal указывает, что учетная запись проходит проверку подлинности субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="e5c16-130">The ServicePrincipal switch parameter indicates that the account authenticates as a service principal.</span></span>

### <span data-ttu-id="e5c16-131">Пример 4: Добавление учетной записи для определенного клиента и подписки</span><span class="sxs-lookup"><span data-stu-id="e5c16-131">Example 4: Add an account for a specific tenant and subscription</span></span>
```
PS C:\>Add-AzureRmAccount -Tenant "xxxx-xxxx-xxxx-xxxx" -SubscriptionId "yyyy-yyyy-yyyy-yyyy"
Account: pfuller@contoso.com
Environment: AzureCloud
Subscription: yyyy-yyyy-yyyy-yyyy
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="e5c16-132">Эта команда добавляет учетную запись диспетчера ресурсов Azure для запуска командлетов для указанных клиентов и подписок по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e5c16-132">This command adds an Azure Resource Manager account to run cmdlets for the specified tenant and subscription by default.</span></span>

## <span data-ttu-id="e5c16-133">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e5c16-133">PARAMETERS</span></span>

### <span data-ttu-id="e5c16-134">-AccessToken</span><span class="sxs-lookup"><span data-stu-id="e5c16-134">-AccessToken</span></span>
<span data-ttu-id="e5c16-135">Задает маркер доступа.</span><span class="sxs-lookup"><span data-stu-id="e5c16-135">Specifies an access token.</span></span>

```yaml
Type: String
Parameter Sets: AccessTokenWithSubscriptionId, AccessTokenWithSubscriptionName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5c16-136">-AccountId</span><span class="sxs-lookup"><span data-stu-id="e5c16-136">-AccountId</span></span>
<span data-ttu-id="e5c16-137">Идентификатор учетной записи для маркера доступа</span><span class="sxs-lookup"><span data-stu-id="e5c16-137">Account Id for access token</span></span>

```yaml
Type: String
Parameter Sets: AccessTokenWithSubscriptionId, AccessTokenWithSubscriptionName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5c16-138">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="e5c16-138">-ApplicationId</span></span>
<span data-ttu-id="e5c16-139">УЧАСТНИКОВ</span><span class="sxs-lookup"><span data-stu-id="e5c16-139">SPN</span></span>

```yaml
Type: String
Parameter Sets: ServicePrincipalCertificateWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5c16-140">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="e5c16-140">-CertificateThumbprint</span></span>
<span data-ttu-id="e5c16-141">Хэш сертификата (отпечаток)</span><span class="sxs-lookup"><span data-stu-id="e5c16-141">Certificate Hash (Thumbprint)</span></span>

```yaml
Type: String
Parameter Sets: ServicePrincipalCertificateWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5c16-142">-Credential</span><span class="sxs-lookup"><span data-stu-id="e5c16-142">-Credential</span></span>
<span data-ttu-id="e5c16-143">Указывает объект PSCredential.</span><span class="sxs-lookup"><span data-stu-id="e5c16-143">Specifies a PSCredential object.</span></span>
<span data-ttu-id="e5c16-144">Для получения дополнительных сведений о объекте PSCredential введите Get-Help Get-credentials.</span><span class="sxs-lookup"><span data-stu-id="e5c16-144">For more information about the PSCredential object, type Get-Help Get-Credential.</span></span>

<span data-ttu-id="e5c16-145">Объект PSCredential предоставляет идентификатор пользователя и пароль для учетных данных идентификатора организации, а также идентификатор приложения и секрет для учетных данных субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="e5c16-145">The PSCredential object provides the user ID and password for organizational ID credentials, or the application ID and secret for service principal credentials.</span></span>

```yaml
Type: PSCredential
Parameter Sets: UserWithSubscriptionId, UserWithSubscriptionName
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: PSCredential
Parameter Sets: ServicePrincipalWithSubscriptionId, ServicePrincipalWithSubscriptionName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5c16-146">-Environment</span><span class="sxs-lookup"><span data-stu-id="e5c16-146">-Environment</span></span>
<span data-ttu-id="e5c16-147">Среда, содержащая учетную запись, в которую нужно войти</span><span class="sxs-lookup"><span data-stu-id="e5c16-147">Environment containing the account to log into</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5c16-148">-ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="e5c16-148">-ServicePrincipal</span></span>
<span data-ttu-id="e5c16-149">Указывает, что учетная запись проходит проверку подлинности путем предоставления учетных данных субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="e5c16-149">Indicates that this account authenticates by providing service principal credentials.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ServicePrincipalWithSubscriptionId, ServicePrincipalWithSubscriptionName, ServicePrincipalCertificateWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5c16-150">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e5c16-150">-SubscriptionId</span></span>
<span data-ttu-id="e5c16-151">Указывает идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="e5c16-151">Specifies the ID of the subscription.</span></span>
<span data-ttu-id="e5c16-152">Если этот параметр не указан, используется первая подписка из списка подписок.</span><span class="sxs-lookup"><span data-stu-id="e5c16-152">If you do not specify this parameter, the first subscription from the subscription list is used.</span></span>

```yaml
Type: String
Parameter Sets: UserWithSubscriptionId, ServicePrincipalWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionId, AccessTokenWithSubscriptionId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e5c16-153">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="e5c16-153">-SubscriptionName</span></span>
<span data-ttu-id="e5c16-154">Название подписки</span><span class="sxs-lookup"><span data-stu-id="e5c16-154">Subscription Name</span></span>

```yaml
Type: String
Parameter Sets: UserWithSubscriptionName, ServicePrincipalWithSubscriptionName, ServicePrincipalCertificateWithSubscriptionName, AccessTokenWithSubscriptionName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e5c16-155">-TenantId</span><span class="sxs-lookup"><span data-stu-id="e5c16-155">-TenantId</span></span>
<span data-ttu-id="e5c16-156">Имя или идентификатор необязательного клиента</span><span class="sxs-lookup"><span data-stu-id="e5c16-156">Optional tenant name or ID</span></span>

```yaml
Type: String
Parameter Sets: UserWithSubscriptionId, UserWithSubscriptionName, AccessTokenWithSubscriptionId, AccessTokenWithSubscriptionName
Aliases: Domain

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ServicePrincipalWithSubscriptionId, ServicePrincipalWithSubscriptionName, ServicePrincipalCertificateWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionName
Aliases: Domain

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5c16-157">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e5c16-157">-Confirm</span></span>
<span data-ttu-id="e5c16-158">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e5c16-158">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5c16-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5c16-159">-WhatIf</span></span>
<span data-ttu-id="e5c16-160">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e5c16-160">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e5c16-161">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e5c16-161">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5c16-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5c16-162">CommonParameters</span></span>
<span data-ttu-id="e5c16-163">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e5c16-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5c16-164">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5c16-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5c16-165">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e5c16-165">INPUTS</span></span>

## <span data-ttu-id="e5c16-166">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e5c16-166">OUTPUTS</span></span>

### <span data-ttu-id="e5c16-167">PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="e5c16-167">PSAzureProfile</span></span>

## <span data-ttu-id="e5c16-168">Пуск</span><span class="sxs-lookup"><span data-stu-id="e5c16-168">NOTES</span></span>

## <span data-ttu-id="e5c16-169">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e5c16-169">RELATED LINKS</span></span>


---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/add-azurermaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Connect-AzureRmAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Connect-AzureRmAccount.md
ms.openlocfilehash: a0f29e666a289faddbfce848b97cb0272ce67d0d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734601"
---
# <span data-ttu-id="d4d59-101">Connect-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="d4d59-101">Connect-AzureRmAccount</span></span>

## <span data-ttu-id="d4d59-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d4d59-102">SYNOPSIS</span></span>
<span data-ttu-id="d4d59-103">Подключитесь к Azure с учетной записью, прошедшим проверку подлинности, для использования с запросом командлетов Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="d4d59-103">Connect to Azure with an authenticated account for use with Azure Resource Manager cmdlet requests.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d4d59-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d4d59-104">SYNTAX</span></span>

### <span data-ttu-id="d4d59-105">UserWithSubscriptionId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d4d59-105">UserWithSubscriptionId (Default)</span></span>
```
Connect-AzureRmAccount [-Environment <String>] [[-Credential] <PSCredential>] [-TenantId <String>]
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d4d59-106">ServicePrincipalWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d4d59-106">ServicePrincipalWithSubscriptionId</span></span>
```
Connect-AzureRmAccount [-Environment <String>] [-Credential] <PSCredential> [-ServicePrincipal]
 -TenantId <String> [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d4d59-107">ServicePrincipalCertificateWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d4d59-107">ServicePrincipalCertificateWithSubscriptionId</span></span>
```
Connect-AzureRmAccount [-Environment <String>] -CertificateThumbprint <String> -ApplicationId <String>
 [-ServicePrincipal] -TenantId <String> [-Subscription <String>] [-ContextName <String>]
 [-SkipContextPopulation] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4d59-108">AccessTokenWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d4d59-108">AccessTokenWithSubscriptionId</span></span>
```
Connect-AzureRmAccount [-Environment <String>] [-TenantId <String>] -AccessToken <String>
 [-GraphAccessToken <String>] [-KeyVaultAccessToken <String>] -AccountId <String> [-Subscription <String>]
 [-ContextName <String>] [-SkipValidation] [-SkipContextPopulation] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d4d59-109">ManagedServiceLogin</span><span class="sxs-lookup"><span data-stu-id="d4d59-109">ManagedServiceLogin</span></span>
```
Connect-AzureRmAccount [-Environment <String>] [-TenantId <String>] [-AccountId <String>] [-Identity]
 [-ManagedServicePort <Int32>] [-ManagedServiceHostName <String>] [-ManagedServiceSecret <SecureString>]
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d4d59-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d4d59-110">DESCRIPTION</span></span>
<span data-ttu-id="d4d59-111">Командлет Connect-AzureRmAccount подключает к Azure учетную запись с проверкой подлинности для использования с запросом командлета диспетчера ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="d4d59-111">The Connect-AzureRmAccount cmdlet connects to Azure with an authenticated account for use with Azure Resource Manager cmdlet requests.</span></span>
<span data-ttu-id="d4d59-112">Вы можете использовать эту учетную запись с проверкой подлинности только для командлетов Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="d4d59-112">You can use this authenticated account only with Azure Resource Manager cmdlets.</span></span>
<span data-ttu-id="d4d59-113">Чтобы добавить учетную запись, прошедший проверку подлинности, с помощью командлетов управления службами, используйте Add-AzureAccount или Import-AzurePublishSettingsFile.</span><span class="sxs-lookup"><span data-stu-id="d4d59-113">To add an authenticated account for use with Service Management cmdlets, use the Add-AzureAccount or the Import-AzurePublishSettingsFile cmdlet.</span></span>
<span data-ttu-id="d4d59-114">Если для текущего пользователя контекст не найден, эта команда заполнит список контекста пользователя, указав контекст для каждой из подписок (первых 25).</span><span class="sxs-lookup"><span data-stu-id="d4d59-114">If no context is found for the current user, this command will populate the user's context list with a context for each of their (first 25) subscriptions.</span></span> <span data-ttu-id="d4d59-115">Список контекстов, созданных для пользователя, можно найти, выполнив "Get-AzureRmContext-ListAvailable".</span><span class="sxs-lookup"><span data-stu-id="d4d59-115">The list of contexts created for the user can be found by running "Get-AzureRmContext -ListAvailable".</span></span> <span data-ttu-id="d4d59-116">Чтобы пропустить это заполнение, вы можете выполнить эту команду с параметром "-SkipContextPopulation".</span><span class="sxs-lookup"><span data-stu-id="d4d59-116">To skip this context population, you can run this command with the "-SkipContextPopulation" switch parameter.</span></span>
<span data-ttu-id="d4d59-117">После выполнения этого командлета вы можете отключиться от учетной записи Azure с помощью команды Disconnect-AzureRmAccount.</span><span class="sxs-lookup"><span data-stu-id="d4d59-117">After executing this cmdlet, you can disconnect from an Azure account using Disconnect-AzureRmAccount.</span></span>

## <span data-ttu-id="d4d59-118">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d4d59-118">EXAMPLES</span></span>

### <span data-ttu-id="d4d59-119">Пример 1: использование интерактивного входа для подключения к учетной записи Azure</span><span class="sxs-lookup"><span data-stu-id="d4d59-119">Example 1: Use an interactive login to connect to an Azure account</span></span>
```powershell
PS C:\> Connect-AzureRmAccount

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="d4d59-120">Эта команда соединяется с учетной записью Azure.</span><span class="sxs-lookup"><span data-stu-id="d4d59-120">This command connects to an Azure account.</span></span>
<span data-ttu-id="d4d59-121">Чтобы запустить командлеты диспетчера ресурсов Azure с этой учетной записью, необходимо задать учетные данные учетной записи Майкрософт или идентификатора организации в запросе.</span><span class="sxs-lookup"><span data-stu-id="d4d59-121">To run Azure Resource Manager cmdlets with this account, you must provide Microsoft account or organizational ID credentials at the prompt.</span></span>
<span data-ttu-id="d4d59-122">Если для ваших учетных данных включена многофакторная проверка подлинности, вы должны войти в систему с помощью интерактивного режима или воспользоваться проверкой подлинности субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="d4d59-122">If multi-factor authentication is enabled for your credentials, you must log in using the interactive option or use service principal authentication.</span></span>

### <span data-ttu-id="d4d59-123">Пример 2: подключение к учетной записи Azure с использованием учетных данных идентификатора Организации</span><span class="sxs-lookup"><span data-stu-id="d4d59-123">Example 2: Connect to an Azure account using organizational ID credentials</span></span>
```powershell
PS C:\> $Credential = Get-Credential
PS C:\> Connect-AzureRmAccount -Credential $Credential

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="d4d59-124">Первая команда предложит ввести учетные данные пользователя (имя пользователя и пароль), а затем сохранит их в переменной $Credential.</span><span class="sxs-lookup"><span data-stu-id="d4d59-124">The first command will prompt for user credentials (username and password), and then stores them in the $Credential variable.</span></span>
<span data-ttu-id="d4d59-125">Вторая команда подключается к учетной записи Azure с использованием учетных данных, которые хранятся в $Credential.</span><span class="sxs-lookup"><span data-stu-id="d4d59-125">The second command connects to an Azure account using the credentials stored in $Credential.</span></span>
<span data-ttu-id="d4d59-126">Эта учетная запись проходит проверку подлинности с помощью диспетчера ресурсов Azure с использованием учетных данных идентификатора организации.</span><span class="sxs-lookup"><span data-stu-id="d4d59-126">This account authenticates with Azure Resource Manager using organizational ID credentials.</span></span>
<span data-ttu-id="d4d59-127">Для запуска командлетов диспетчера ресурсов Azure с этой учетной записью нельзя использовать многофакторную проверку подлинности или учетные данные учетной записи Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="d4d59-127">You cannot use multi-factor authentication or Microsoft account credentials to run Azure Resource Manager cmdlets with this account.</span></span>

### <span data-ttu-id="d4d59-128">Пример 3: подключение к учетной записи субъекта-службы Azure</span><span class="sxs-lookup"><span data-stu-id="d4d59-128">Example 3: Connect to an Azure service principal account</span></span>
```powershell
PS C:\> $Credential = Get-Credential

PS C:\> Connect-AzureRmAccount -Credential $Credential -Tenant "xxxx-xxxx-xxxx-xxxx" -ServicePrincipal
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
xxxx-xxxx-xxxx-xxxx    Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="d4d59-129">Первая команда получает учетные данные субъекта-службы (идентификатор приложения и секретный ключ участника-службы), а затем сохраняет их в переменной $Credential.</span><span class="sxs-lookup"><span data-stu-id="d4d59-129">The first command gets the service principal credentials (application id and service principal secret), and then stores them in the $Credential variable.</span></span>
<span data-ttu-id="d4d59-130">Вторая команда подключается к Azure с использованием учетных данных субъекта-службы, хранящихся в $Credential для указанного клиента.</span><span class="sxs-lookup"><span data-stu-id="d4d59-130">The second command connect to Azure using the service principal credentials stored in $Credential for the specified Tenant.</span></span>
<span data-ttu-id="d4d59-131">Параметр ключа ServicePrincipal указывает, что учетная запись проходит проверку подлинности субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="d4d59-131">The ServicePrincipal switch parameter indicates that the account authenticates as a service principal.</span></span>

### <span data-ttu-id="d4d59-132">Пример 4: использование интерактивного входа для подключения к учетной записи для определенного клиента и подписки</span><span class="sxs-lookup"><span data-stu-id="d4d59-132">Example 4: Use an interactive login to connect to an account for a specific tenant and subscription</span></span>
```powershell
PS C:\> Connect-AzureRmAccount -Tenant "xxxx-xxxx-xxxx-xxxx" -SubscriptionId "yyyy-yyyy-yyyy-yyyy"
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="d4d59-133">Эта команда соединяется с учетной записью Azure и настроила AzureRM PowerShell для запуска командлетов для указанного клиента и подписки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d4d59-133">This command connects to an Azure account and configured AzureRM PowerShell to run cmdlets for the specified tenant and subscription by default.</span></span>

### <span data-ttu-id="d4d59-134">Пример 5: Добавление учетной записи с помощью имени входа для удостоверения управляемой службы</span><span class="sxs-lookup"><span data-stu-id="d4d59-134">Example 5: Add an Account Using Managed Service Identity Login</span></span>
```powershell
PS C:\> Connect-AzureRmAccount -MSI

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
MSI@50342              Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="d4d59-135">Эта команда соединяется с использованием управляемого удостоверения среды хоста (например, если выполняется в VirtualMachine с назначенным идентификатором управляемой службы, это позволит коду войти в систему с помощью этого назначенного удостоверения).</span><span class="sxs-lookup"><span data-stu-id="d4d59-135">This command connects using the managed service identity of the host environment (for example, if executed on a VirtualMachine with an assigned Managed Service Identity, this will allow the code to login using that assigned identity)</span></span>

### <span data-ttu-id="d4d59-136">Пример 6: Добавление учетной записи с помощью сертификатов</span><span class="sxs-lookup"><span data-stu-id="d4d59-136">Example 6: Add an account using certificates</span></span>
```powershell
# For more information on creating a self-signed certificate
# and giving it proper permissions, please see the following:
# https://docs.microsoft.com/en-us/azure/active-directory/develop/howto-authenticate-service-principal-powershell
PS C:\> $Thumbprint = "0SZTNJ34TCCMUJ5MJZGR8XQD3S0RVHJBA33Z8ZXV"
PS C:\> $TenantId = "4cd76576-b611-43d0-8f2b-adcb139531bf"
PS C:\> $ApplicationId = "3794a65a-e4e4-493d-ac1d-f04308d712dd"
PS C:\> Connect-AzureRmAccount -CertificateThumbprint $Thumbprint -ApplicationId $ApplicationId -Tenant $TenantId -ServicePrincipal

Account             SubscriptionName TenantId            Environment
-------             ---------------- --------            -----------
xxxx-xxxx-xxxx-xxxx Subscription1    xxxx-xxxx-xxxx-xxxx AzureCloud

Account          : 3794a65a-e4e4-493d-ac1d-f04308d712dd
SubscriptionName : MyTestSubscription
SubscriptionId   : 85f0f653-1f86-4d2c-a9f1-042efc00085c
TenantId         : 4cd76576-b611-43d0-8f2b-adcb139531bf
Environment      : AzureCloud
```

<span data-ttu-id="d4d59-137">Эта команда используется для подключения к учетной записи Azure с использованием проверки подлинности субъекта-службы на основе сертификатов.</span><span class="sxs-lookup"><span data-stu-id="d4d59-137">This command connects to an Azure account using certificate-based service principal authentication.</span></span> <span data-ttu-id="d4d59-138">Для проверки подлинности был создан Theservice участник, который использовался при использовании этого сертификата.</span><span class="sxs-lookup"><span data-stu-id="d4d59-138">Theservice principal used for authentication should have been created with the given certificate.</span></span>

## <span data-ttu-id="d4d59-139">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d4d59-139">PARAMETERS</span></span>

### <span data-ttu-id="d4d59-140">-AccessToken</span><span class="sxs-lookup"><span data-stu-id="d4d59-140">-AccessToken</span></span>
<span data-ttu-id="d4d59-141">Задает маркер доступа.</span><span class="sxs-lookup"><span data-stu-id="d4d59-141">Specifies an access token.</span></span>

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

### <span data-ttu-id="d4d59-142">-AccountId</span><span class="sxs-lookup"><span data-stu-id="d4d59-142">-AccountId</span></span>
<span data-ttu-id="d4d59-143">Идентификатор учетной записи для маркера доступа</span><span class="sxs-lookup"><span data-stu-id="d4d59-143">Account Id for access token</span></span>

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

```yaml
Type: System.String
Parameter Sets: ManagedServiceLogin
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4d59-144">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="d4d59-144">-ApplicationId</span></span>
<span data-ttu-id="d4d59-145">УЧАСТНИКОВ</span><span class="sxs-lookup"><span data-stu-id="d4d59-145">SPN</span></span>

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

### <span data-ttu-id="d4d59-146">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="d4d59-146">-CertificateThumbprint</span></span>
<span data-ttu-id="d4d59-147">Хэш сертификата (отпечаток)</span><span class="sxs-lookup"><span data-stu-id="d4d59-147">Certificate Hash (Thumbprint)</span></span>

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

### <span data-ttu-id="d4d59-148">-ContextName</span><span class="sxs-lookup"><span data-stu-id="d4d59-148">-ContextName</span></span>
<span data-ttu-id="d4d59-149">Имя контекста по умолчанию из этого имени входа.</span><span class="sxs-lookup"><span data-stu-id="d4d59-149">Name of the default context from this login.</span></span>  <span data-ttu-id="d4d59-150">Вы сможете выбрать этот контекст по этому имени после входа.</span><span class="sxs-lookup"><span data-stu-id="d4d59-150">You will be able to select this context by this name after login.</span></span>

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

### <span data-ttu-id="d4d59-151">-Credential</span><span class="sxs-lookup"><span data-stu-id="d4d59-151">-Credential</span></span>
<span data-ttu-id="d4d59-152">Указывает объект PSCredential.</span><span class="sxs-lookup"><span data-stu-id="d4d59-152">Specifies a PSCredential object.</span></span>
<span data-ttu-id="d4d59-153">Для получения дополнительных сведений о объекте PSCredential введите Get-Help Get-credentials.</span><span class="sxs-lookup"><span data-stu-id="d4d59-153">For more information about the PSCredential object, type Get-Help Get-Credential.</span></span>
<span data-ttu-id="d4d59-154">Объект PSCredential предоставляет идентификатор пользователя и пароль для учетных данных идентификатора организации, а также идентификатор приложения и секрет для учетных данных субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="d4d59-154">The PSCredential object provides the user ID and password for organizational ID credentials, or the application ID and secret for service principal credentials.</span></span>

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

### <span data-ttu-id="d4d59-155">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4d59-155">-DefaultProfile</span></span>
<span data-ttu-id="d4d59-156">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d4d59-156">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d4d59-157">-Environment</span><span class="sxs-lookup"><span data-stu-id="d4d59-157">-Environment</span></span>
<span data-ttu-id="d4d59-158">Среда, содержащая учетную запись, в которую нужно войти</span><span class="sxs-lookup"><span data-stu-id="d4d59-158">Environment containing the account to log into</span></span>

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

### <span data-ttu-id="d4d59-159">-Force</span><span class="sxs-lookup"><span data-stu-id="d4d59-159">-Force</span></span>
<span data-ttu-id="d4d59-160">Перезаписать существующий контекст с тем же именем, если таковое имеется.</span><span class="sxs-lookup"><span data-stu-id="d4d59-160">Overwrite the existing context with the same name, if any.</span></span>

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

### <span data-ttu-id="d4d59-161">-GraphAccessToken</span><span class="sxs-lookup"><span data-stu-id="d4d59-161">-GraphAccessToken</span></span>
<span data-ttu-id="d4d59-162">AccessToken для службы Graph</span><span class="sxs-lookup"><span data-stu-id="d4d59-162">AccessToken for Graph Service</span></span>

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

### <span data-ttu-id="d4d59-163">-Identity</span><span class="sxs-lookup"><span data-stu-id="d4d59-163">-Identity</span></span>
<span data-ttu-id="d4d59-164">Вход с учетной записью управляемой службы в текущем окружении.</span><span class="sxs-lookup"><span data-stu-id="d4d59-164">Login using managed service identity in the current environment.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ManagedServiceLogin
Aliases: MSI, ManagedService

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4d59-165">-KeyVaultAccessToken</span><span class="sxs-lookup"><span data-stu-id="d4d59-165">-KeyVaultAccessToken</span></span>
<span data-ttu-id="d4d59-166">Служба AccessToken для KeyVault</span><span class="sxs-lookup"><span data-stu-id="d4d59-166">AccessToken for KeyVault Service</span></span>

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

### <span data-ttu-id="d4d59-167">-ManagedServiceHostName</span><span class="sxs-lookup"><span data-stu-id="d4d59-167">-ManagedServiceHostName</span></span>
<span data-ttu-id="d4d59-168">Имя узла для логина управляемой службы</span><span class="sxs-lookup"><span data-stu-id="d4d59-168">Host name for managed service login</span></span>

```yaml
Type: System.String
Parameter Sets: ManagedServiceLogin
Aliases:

Required: False
Position: Named
Default value: localhost
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4d59-169">-ManagedServicePort</span><span class="sxs-lookup"><span data-stu-id="d4d59-169">-ManagedServicePort</span></span>
<span data-ttu-id="d4d59-170">Номер порта для логина управляемой службы</span><span class="sxs-lookup"><span data-stu-id="d4d59-170">Port number for managed service login</span></span>

```yaml
Type: System.Int32
Parameter Sets: ManagedServiceLogin
Aliases:

Required: False
Position: Named
Default value: 50342
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4d59-171">-ManagedServiceSecret</span><span class="sxs-lookup"><span data-stu-id="d4d59-171">-ManagedServiceSecret</span></span>
<span data-ttu-id="d4d59-172">Секрет, используемый для некоторых типов входных данных управляемой службы.</span><span class="sxs-lookup"><span data-stu-id="d4d59-172">Secret, used for some kinds of managed service login.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ManagedServiceLogin
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4d59-173">-Scope</span><span class="sxs-lookup"><span data-stu-id="d4d59-173">-Scope</span></span>
<span data-ttu-id="d4d59-174">Определяет область изменений контекста, например, применяются ли изменения только к текущему процессу или ко всем сеансам, запускаемым этим пользователем.</span><span class="sxs-lookup"><span data-stu-id="d4d59-174">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="d4d59-175">-ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="d4d59-175">-ServicePrincipal</span></span>
<span data-ttu-id="d4d59-176">Указывает, что учетная запись проходит проверку подлинности путем предоставления учетных данных субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="d4d59-176">Indicates that this account authenticates by providing service principal credentials.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServicePrincipalCertificateWithSubscriptionId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServicePrincipalWithSubscriptionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4d59-177">-SkipContextPopulation</span><span class="sxs-lookup"><span data-stu-id="d4d59-177">-SkipContextPopulation</span></span>
<span data-ttu-id="d4d59-178">Пропускает заполнение контекста, если контексты не найдены.</span><span class="sxs-lookup"><span data-stu-id="d4d59-178">Skips context population if no contexts are found.</span></span>

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

### <span data-ttu-id="d4d59-179">-SkipValidation</span><span class="sxs-lookup"><span data-stu-id="d4d59-179">-SkipValidation</span></span>
<span data-ttu-id="d4d59-180">Пропуск проверки маркера доступа</span><span class="sxs-lookup"><span data-stu-id="d4d59-180">Skip validation for access token</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AccessTokenWithSubscriptionId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4d59-181">-Подписка</span><span class="sxs-lookup"><span data-stu-id="d4d59-181">-Subscription</span></span>
<span data-ttu-id="d4d59-182">Имя или идентификатор подписки</span><span class="sxs-lookup"><span data-stu-id="d4d59-182">Subscription Name or ID</span></span>

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

### <span data-ttu-id="d4d59-183">-TenantId</span><span class="sxs-lookup"><span data-stu-id="d4d59-183">-TenantId</span></span>
<span data-ttu-id="d4d59-184">Необязательное имя домена или ИД клиента.</span><span class="sxs-lookup"><span data-stu-id="d4d59-184">Optional domain name or tenant ID.</span></span> <span data-ttu-id="d4d59-185">Доменное имя не будет работать во всех случаях входа.</span><span class="sxs-lookup"><span data-stu-id="d4d59-185">Domain name will not work in all sign-in situations.</span></span> <span data-ttu-id="d4d59-186">Для входа в учетную запись поставщика облачных решений (CSP) требуется ИД клиента.</span><span class="sxs-lookup"><span data-stu-id="d4d59-186">For Cloud Solution Provider (CSP) sign-in, tenant ID is required.</span></span>

```yaml
Type: System.String
Parameter Sets: UserWithSubscriptionId, AccessTokenWithSubscriptionId, ManagedServiceLogin
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

### <span data-ttu-id="d4d59-187">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d4d59-187">-Confirm</span></span>
<span data-ttu-id="d4d59-188">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d4d59-188">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4d59-189">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4d59-189">-WhatIf</span></span>
<span data-ttu-id="d4d59-190">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d4d59-190">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d4d59-191">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d4d59-191">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4d59-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4d59-192">CommonParameters</span></span>
<span data-ttu-id="d4d59-193">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d4d59-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4d59-194">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4d59-194">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4d59-195">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d4d59-195">INPUTS</span></span>

### <span data-ttu-id="d4d59-196">System. String</span><span class="sxs-lookup"><span data-stu-id="d4d59-196">System.String</span></span>
<span data-ttu-id="d4d59-197">Параметры: Подписка (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d4d59-197">Parameters: Subscription (ByValue)</span></span>

## <span data-ttu-id="d4d59-198">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d4d59-198">OUTPUTS</span></span>

### <span data-ttu-id="d4d59-199">Microsoft. Azure. Commands. Profile. Models. PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="d4d59-199">Microsoft.Azure.Commands.Profile.Models.PSAzureProfile</span></span>

## <span data-ttu-id="d4d59-200">Пуск</span><span class="sxs-lookup"><span data-stu-id="d4d59-200">NOTES</span></span>

## <span data-ttu-id="d4d59-201">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d4d59-201">RELATED LINKS</span></span>

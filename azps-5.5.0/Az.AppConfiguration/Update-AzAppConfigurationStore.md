---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/update-azappconfigurationstore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Update-AzAppConfigurationStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Update-AzAppConfigurationStore.md
ms.openlocfilehash: 8aea57e0c2bea5dbaa2e3233e886c97bfebe4bd4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100229388"
---
# <span data-ttu-id="32abb-101">Update-AzAppConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="32abb-101">Update-AzAppConfigurationStore</span></span>

## <span data-ttu-id="32abb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32abb-102">SYNOPSIS</span></span>
<span data-ttu-id="32abb-103">Обновляет хранилище конфигураций с указанными параметрами.</span><span class="sxs-lookup"><span data-stu-id="32abb-103">Updates a configuration store with the specified parameters.</span></span>

## <span data-ttu-id="32abb-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="32abb-104">SYNTAX</span></span>

### <span data-ttu-id="32abb-105">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="32abb-105">UpdateExpanded (Default)</span></span>
```
Update-AzAppConfigurationStore -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-EncryptionKeyIdentifier <String>] [-IdentityType <IdentityType>] [-KeyVaultIdentityClientId <String>]
 [-Sku <String>] [-Tag <Hashtable>] [-UserAssignedIdentity <String[]>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="32abb-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="32abb-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzAppConfigurationStore -InputObject <IAppConfigurationIdentity> [-EncryptionKeyIdentifier <String>]
 [-IdentityType <IdentityType>] [-KeyVaultIdentityClientId <String>] [-Sku <String>] [-Tag <Hashtable>]
 [-UserAssignedIdentity <String[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="32abb-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="32abb-107">DESCRIPTION</span></span>
<span data-ttu-id="32abb-108">Обновляет хранилище конфигураций с указанными параметрами.</span><span class="sxs-lookup"><span data-stu-id="32abb-108">Updates a configuration store with the specified parameters.</span></span>

## <span data-ttu-id="32abb-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="32abb-109">EXAMPLES</span></span>

### <span data-ttu-id="32abb-110">Пример 1. Включить шифрование данных в хранилище конфигураций приложения с помощью управляемых удостоверений, которым назначены системы.</span><span class="sxs-lookup"><span data-stu-id="32abb-110">Example 1: Enable data encryption of the app configuration store by system-assigned managed identity</span></span>
```powershell
PS C:\> $key = Add-AzKeyVaultKey -VaultName kv-Name -Name key-Name -Destination 'Software'
PS C:\> $systemAssignedAppStore = New-AzAppConfigurationStore -Name appconfig-test11 -ResourceGroupName azpwsh-manual-test -Location $env.location -Sku 'standard' -IdentityType "SystemAssigned"
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName kv-Name -ObjectId $systemAssignedAppStore.IdentityPrincipalId -PermissionsToKeys get,unwrapKey,wrapKey -PassThru
PS C:\> Update-AzAppConfigurationStore -Name appconfig-test11 -ResourceGroupName azpwsh-manual-test -EncryptionKeyIdentifier $key.Id

Location Name             Type
-------- ----             ----
eastus   appconfig-test01 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="32abb-111">Эта команда позволяет шифровать данные с помощью ключа, храняного в хранилище ключей Azure, с помощью управляемого удостоверения, назначенного системе.</span><span class="sxs-lookup"><span data-stu-id="32abb-111">This command enables data encryption by a key stored in Azure Key Vault using a system-assigned managed identity.</span></span>
<span data-ttu-id="32abb-112">В хранилище должно быть включено soft-delete и purge-protection, а у управляемого удостоверения должны быть такие основные разрешения: get, wrapKey, unw ключkey.</span><span class="sxs-lookup"><span data-stu-id="32abb-112">The vault must have enabled soft-delete and purge-protection, and the managed identity must have these key permissions: get, wrapKey, unwrapKey.</span></span>

### <span data-ttu-id="32abb-113">Пример 2. Включить шифрование данных в хранилище конфигураций приложения с помощью управляемых удостоверений, которым назначены пользователи</span><span class="sxs-lookup"><span data-stu-id="32abb-113">Example 2: Enable data encryption of the app configuration store by user-assigned managed identity</span></span>
```powershell
PS C:\> $key = Add-AzKeyVaultKey -VaultName kv-Name -Name key-Name -Destination 'Software'
PS C:\> $assignedIdentity = New-AzUserAssignedIdentity -ResourceGroupName azpwsh-manual-test -Name assignedIdentity
PS C:\> New-AzAppConfigurationStore -Name appconfig-test11 -ResourceGroupName azpwsh-manual-test -Location $env.location -Sku 'standard' -IdentityType "UserAssigned" -UserAssignedIdentity $assignedIdentity.Id
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName kv-Name -ObjectId $assignedIdentity.PrincipalId -PermissionsToKeys get,unwrapKey,wrapKey -PassThru
PS C:\> Update-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test -Name appconfig-test11 -EncryptionKeyIdentifier $key.Id -KeyVaultIdentityClientId $assignedIdentity.ClientId

Location Name             Type
-------- ----             ----
eastus   appconfig-test10 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="32abb-114">Эта команда позволяет шифровать данные с помощью ключа, храняного в хранилище ключей Azure, с использованием управляемого удостоверения, назначенного пользователем.</span><span class="sxs-lookup"><span data-stu-id="32abb-114">This command enables data encryption by a key stored in Azure Key Vault using a user-assigned managed identity.</span></span>
<span data-ttu-id="32abb-115">Удостоверение, назначенное пользователю, должно быть настроено с `-UserAssignedIdentity` помощью.</span><span class="sxs-lookup"><span data-stu-id="32abb-115">The user-assigned identity must have been set with `-UserAssignedIdentity`.</span></span>
<span data-ttu-id="32abb-116">В хранилище должно быть включено soft-delete и purge-protection, а у управляемого удостоверения должны быть такие основные разрешения: get, wrapKey, unw ключkey.</span><span class="sxs-lookup"><span data-stu-id="32abb-116">The vault must have enabled soft-delete and purge-protection, and the managed identity must have these key permissions: get, wrapKey, unwrapKey.</span></span>

### <span data-ttu-id="32abb-117">Пример 3. Отключение шифрования в хранилище конфигураций приложений.</span><span class="sxs-lookup"><span data-stu-id="32abb-117">Example 3: Disable encryption of an app configuration store.</span></span>
```powershell
PS C:\> $appConf = Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test -Name appconfig-test10 | Update-AzAppConfigurationStore -EncryptionKeyIdentifier $null

Location Name             Type
-------- ----             ----
eastus   appconfig-test10 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="32abb-118">Эта команда отключает шифрование магазина конфигураций приложений.</span><span class="sxs-lookup"><span data-stu-id="32abb-118">This command disables encryption of an app configuration store.</span></span>

### <span data-ttu-id="32abb-119">Пример 3. Обновление SKU и тега для магазина конфигурации приложения по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="32abb-119">Example 3: Update sku and tag of an app configuration store by pipeline.</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test -Name appconfig-test10 | Update-AzAppConfigurationStore -Sku 'standard' -Tag @{'key'='update'}

Location Name             Type
-------- ----             ----
eastus   appconfig-test10 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="32abb-120">Эта команда обновляет SKU и тег магазина конфигурации приложения в конвейере.</span><span class="sxs-lookup"><span data-stu-id="32abb-120">This command updates sku and tag of an app configuration store by pipeline.</span></span>

## <span data-ttu-id="32abb-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="32abb-121">PARAMETERS</span></span>

### <span data-ttu-id="32abb-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="32abb-122">-AsJob</span></span>
<span data-ttu-id="32abb-123">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="32abb-123">Run the command as a job</span></span>

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

### <span data-ttu-id="32abb-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32abb-124">-DefaultProfile</span></span>
<span data-ttu-id="32abb-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="32abb-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32abb-126">-EncryptionKeyIdentifier</span><span class="sxs-lookup"><span data-stu-id="32abb-126">-EncryptionKeyIdentifier</span></span>
<span data-ttu-id="32abb-127">URI ключа хранилища ключа, используемого для шифрования данных.</span><span class="sxs-lookup"><span data-stu-id="32abb-127">The URI of the key vault key used to encrypt data.</span></span>

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

### <span data-ttu-id="32abb-128">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="32abb-128">-IdentityType</span></span>
<span data-ttu-id="32abb-129">Тип используемых управляемых удостоверений.</span><span class="sxs-lookup"><span data-stu-id="32abb-129">The type of managed identity used.</span></span>
<span data-ttu-id="32abb-130">Тип SystemAssignedAndUserAssigned включает неявно созданное удостоверение и набор удостоверений, которые назначены пользователю.</span><span class="sxs-lookup"><span data-stu-id="32abb-130">The type 'SystemAssignedAndUserAssigned' includes both an implicitly created identity and a set of user-assigned identities.</span></span>
<span data-ttu-id="32abb-131">Тип "Нет" удалит все удостоверения.</span><span class="sxs-lookup"><span data-stu-id="32abb-131">The type 'None' will remove any identities.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Support.IdentityType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32abb-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="32abb-132">-InputObject</span></span>
<span data-ttu-id="32abb-133">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="32abb-133">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="32abb-134">-KeyVaultIdentityClientId</span><span class="sxs-lookup"><span data-stu-id="32abb-134">-KeyVaultIdentityClientId</span></span>
<span data-ttu-id="32abb-135">Идентификатор клиента удостоверения, который будет использоваться для доступа к key vault.</span><span class="sxs-lookup"><span data-stu-id="32abb-135">The client id of the identity which will be used to access key vault.</span></span>

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

### <span data-ttu-id="32abb-136">-Name</span><span class="sxs-lookup"><span data-stu-id="32abb-136">-Name</span></span>
<span data-ttu-id="32abb-137">Имя магазина конфигурации.</span><span class="sxs-lookup"><span data-stu-id="32abb-137">The name of the configuration store.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32abb-138">-NoWait</span><span class="sxs-lookup"><span data-stu-id="32abb-138">-NoWait</span></span>
<span data-ttu-id="32abb-139">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="32abb-139">Run the command asynchronously</span></span>

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

### <span data-ttu-id="32abb-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32abb-140">-ResourceGroupName</span></span>
<span data-ttu-id="32abb-141">Имя группы ресурсов, к которой принадлежит реестр контейнера.</span><span class="sxs-lookup"><span data-stu-id="32abb-141">The name of the resource group to which the container registry belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32abb-142">-SKU</span><span class="sxs-lookup"><span data-stu-id="32abb-142">-Sku</span></span>
<span data-ttu-id="32abb-143">Имя SKU магазина конфигурации.</span><span class="sxs-lookup"><span data-stu-id="32abb-143">The SKU name of the configuration store.</span></span>

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

### <span data-ttu-id="32abb-144">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="32abb-144">-SubscriptionId</span></span>
<span data-ttu-id="32abb-145">ИД подписки Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="32abb-145">The Microsoft Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32abb-146">-Tag</span><span class="sxs-lookup"><span data-stu-id="32abb-146">-Tag</span></span>
<span data-ttu-id="32abb-147">Теги ARM ресурсов.</span><span class="sxs-lookup"><span data-stu-id="32abb-147">The ARM resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32abb-148">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="32abb-148">-UserAssignedIdentity</span></span>
<span data-ttu-id="32abb-149">Список удостоверений, связанных с ресурсом.</span><span class="sxs-lookup"><span data-stu-id="32abb-149">The list of user-assigned identities associated with the resource.</span></span>
<span data-ttu-id="32abb-150">В качестве ключей словарей для пользовательских удостоверений будут ARM идентификаторы ресурсов в форме :'/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span><span class="sxs-lookup"><span data-stu-id="32abb-150">The user-assigned identity dictionary keys will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32abb-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="32abb-151">-Confirm</span></span>
<span data-ttu-id="32abb-152">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="32abb-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32abb-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32abb-153">-WhatIf</span></span>
<span data-ttu-id="32abb-154">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="32abb-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32abb-155">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="32abb-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32abb-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32abb-156">CommonParameters</span></span>
<span data-ttu-id="32abb-157">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32abb-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32abb-158">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="32abb-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32abb-159">INPUTS</span><span class="sxs-lookup"><span data-stu-id="32abb-159">INPUTS</span></span>

### <span data-ttu-id="32abb-160">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity</span><span class="sxs-lookup"><span data-stu-id="32abb-160">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity</span></span>

## <span data-ttu-id="32abb-161">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="32abb-161">OUTPUTS</span></span>

### <span data-ttu-id="32abb-162">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="32abb-162">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IConfigurationStore</span></span>

## <span data-ttu-id="32abb-163">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="32abb-163">NOTES</span></span>

<span data-ttu-id="32abb-164">ALIASES</span><span class="sxs-lookup"><span data-stu-id="32abb-164">ALIASES</span></span>

<span data-ttu-id="32abb-165">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="32abb-165">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="32abb-166">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="32abb-166">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="32abb-167">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="32abb-167">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="32abb-168">INPUTOBJECT <IAppConfigurationIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="32abb-168">INPUTOBJECT <IAppConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="32abb-169">`[ConfigStoreName <String>]`: имя магазина конфигурации.</span><span class="sxs-lookup"><span data-stu-id="32abb-169">`[ConfigStoreName <String>]`: The name of the configuration store.</span></span>
  - <span data-ttu-id="32abb-170">`[GroupName <String>]`: Имя закрытой группы ресурсов, связываемой с ресурсом.</span><span class="sxs-lookup"><span data-stu-id="32abb-170">`[GroupName <String>]`: The name of the private link resource group.</span></span>
  - <span data-ttu-id="32abb-171">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="32abb-171">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="32abb-172">`[PrivateEndpointConnectionName <String>]`: имя подключения к закрытой конечной точке</span><span class="sxs-lookup"><span data-stu-id="32abb-172">`[PrivateEndpointConnectionName <String>]`: Private endpoint connection name</span></span>
  - <span data-ttu-id="32abb-173">`[ResourceGroupName <String>]`: Имя группы ресурсов, к которой принадлежит реестр контейнера.</span><span class="sxs-lookup"><span data-stu-id="32abb-173">`[ResourceGroupName <String>]`: The name of the resource group to which the container registry belongs.</span></span>
  - <span data-ttu-id="32abb-174">`[SubscriptionId <String>]`: ИД подписки Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="32abb-174">`[SubscriptionId <String>]`: The Microsoft Azure subscription ID.</span></span>

## <span data-ttu-id="32abb-175">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="32abb-175">RELATED LINKS</span></span>



<span data-ttu-id="32abb-176">[Set-AzKeyVaultAccessPolicy](https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultaccesspolicy?view=azps-4.4.0) 
 [New-AzUserAssignedIdentity](https://docs.microsoft.com/en-us/powershell/module/az.managedserviceidentity/new-azuserassignedidentity?view=azps-4.4.0)</span><span class="sxs-lookup"><span data-stu-id="32abb-176">[Set-AzKeyVaultAccessPolicy](https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultaccesspolicy?view=azps-4.4.0)
[New-AzUserAssignedIdentity](https://docs.microsoft.com/en-us/powershell/module/az.managedserviceidentity/new-azuserassignedidentity?view=azps-4.4.0)</span></span>


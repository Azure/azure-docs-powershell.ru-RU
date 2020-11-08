---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/update-azappconfigurationstore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Update-AzAppConfigurationStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Update-AzAppConfigurationStore.md
ms.openlocfilehash: 944241dc7434646272c7149d81b380996e71db8f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079855"
---
# <span data-ttu-id="05b01-101">Update-AzAppConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="05b01-101">Update-AzAppConfigurationStore</span></span>

## <span data-ttu-id="05b01-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="05b01-102">SYNOPSIS</span></span>
<span data-ttu-id="05b01-103">Обновляет хранилище конфигураций с указанными параметрами.</span><span class="sxs-lookup"><span data-stu-id="05b01-103">Updates a configuration store with the specified parameters.</span></span>

## <span data-ttu-id="05b01-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="05b01-104">SYNTAX</span></span>

### <span data-ttu-id="05b01-105">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="05b01-105">UpdateExpanded (Default)</span></span>
```
Update-AzAppConfigurationStore -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-EncryptionKeyIdentifier <String>] [-IdentityType <IdentityType>] [-KeyVaultIdentityClientId <String>]
 [-Sku <String>] [-Tag <Hashtable>] [-UserAssignedIdentity <String[]>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="05b01-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="05b01-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzAppConfigurationStore -InputObject <IAppConfigurationIdentity> [-EncryptionKeyIdentifier <String>]
 [-IdentityType <IdentityType>] [-KeyVaultIdentityClientId <String>] [-Sku <String>] [-Tag <Hashtable>]
 [-UserAssignedIdentity <String[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="05b01-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="05b01-107">DESCRIPTION</span></span>
<span data-ttu-id="05b01-108">Обновляет хранилище конфигураций с указанными параметрами.</span><span class="sxs-lookup"><span data-stu-id="05b01-108">Updates a configuration store with the specified parameters.</span></span>

## <span data-ttu-id="05b01-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="05b01-109">EXAMPLES</span></span>

### <span data-ttu-id="05b01-110">Пример 1: Включение шифрования данных в conifguration Store по системе, назначенной управляемым удостоверением</span><span class="sxs-lookup"><span data-stu-id="05b01-110">Example 1: Enable data encryption of the app conifguration store by system-assigned managed identity</span></span>
```powershell
PS C:\> $key = Add-AzKeyVaultKey -VaultName kv-Name -Name key-Name -Destination 'Software'
PS C:\> $systemAssignedAppStore = New-AzAppConfigurationStore -Name appconfig-test11 -ResourceGroupName azpwsh-manual-test -Location $env.location -Sku 'standard' -IdentityType "SystemAssigned"
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName kv-Name -ObjectId $systemAssignedAppStore.IdentityPrincipalId -PermissionsToKeys get,unwrapKey,wrapKey -PassThru
PS C:\> Update-AzAppConfigurationStore -Name appconfig-test11 -ResourceGroupName azpwsh-manual-test -EncryptionKeyIdentifier $key.Id

Location Name             Type
-------- ----             ----
eastus   appconfig-test01 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="05b01-111">Эта команда обеспечивает шифрование данных ключом, хранящимся в хранилище ключей Azure, с использованием системного удостоверения, назначенного системой.</span><span class="sxs-lookup"><span data-stu-id="05b01-111">This command enables data encryption by a key stored in Azure Key Vault using a system-assigned managed identity.</span></span>
<span data-ttu-id="05b01-112">Хранилище должно включать функцию "обратимое удаление" и "очистить", а управляемое удостоверение должно иметь следующие ключевые разрешения: Get, wrapKey, unwrapKey.</span><span class="sxs-lookup"><span data-stu-id="05b01-112">The vault must have enabled soft-delete and purge-protection, and the managed identity must have these key permissions: get, wrapKey, unwrapKey.</span></span>

### <span data-ttu-id="05b01-113">Пример 2: Включите шифрование данных в приложении conifguration Store по управляемому идентификатору, назначенному пользователем.</span><span class="sxs-lookup"><span data-stu-id="05b01-113">Example 2: Enable data encryption of the app conifguration store by user-assigned managed identity</span></span>
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

<span data-ttu-id="05b01-114">Эта команда обеспечивает шифрование данных с помощью ключа, хранящегося в хранилище ключей Azure, с использованием управляемого удостоверения, назначенного пользователем.</span><span class="sxs-lookup"><span data-stu-id="05b01-114">This command enables data encryption by a key stored in Azure Key Vault using a user-assigned managed identity.</span></span>
<span data-ttu-id="05b01-115">Для идентификатора, назначенного пользователю, должно быть задано значение `-UserAssignedIdentity` .</span><span class="sxs-lookup"><span data-stu-id="05b01-115">The user-assigned identity must have been set with `-UserAssignedIdentity`.</span></span>
<span data-ttu-id="05b01-116">Хранилище должно включать функцию "обратимое удаление" и "очистить", а управляемое удостоверение должно иметь следующие ключевые разрешения: Get, wrapKey, unwrapKey.</span><span class="sxs-lookup"><span data-stu-id="05b01-116">The vault must have enabled soft-delete and purge-protection, and the managed identity must have these key permissions: get, wrapKey, unwrapKey.</span></span>

### <span data-ttu-id="05b01-117">Пример 3: отключение шифрования для conifguration магазина приложения.</span><span class="sxs-lookup"><span data-stu-id="05b01-117">Example 3: Disable encryption of an app conifguration store.</span></span>
```powershell
PS C:\> $appConf = Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test -Name appconfig-test10 | Update-AzAppConfigurationStore -EncryptionKeyIdentifier $null

Location Name             Type
-------- ----             ----
eastus   appconfig-test10 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="05b01-118">Эта команда отключает шифрование conifguration магазина приложения.</span><span class="sxs-lookup"><span data-stu-id="05b01-118">This command disables encryption of an app conifguration store.</span></span>

### <span data-ttu-id="05b01-119">Пример 3: обновление SKU и тега приложения conifguration магазин по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="05b01-119">Example 3: Update sku and tag of an app conifguration store by pipeline.</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test -Name appconfig-test10 | Update-AzAppConfigurationStore -Sku 'standard' -Tag @{'key'='update'}

Location Name             Type
-------- ----             ----
eastus   appconfig-test10 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="05b01-120">Эта команда обновляет SKU и тег приложения conifguration Store по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="05b01-120">This command updates sku and tag of an app conifguration store by pipeline.</span></span>

## <span data-ttu-id="05b01-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="05b01-121">PARAMETERS</span></span>

### <span data-ttu-id="05b01-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="05b01-122">-AsJob</span></span>
<span data-ttu-id="05b01-123">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="05b01-123">Run the command as a job</span></span>

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

### <span data-ttu-id="05b01-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05b01-124">-DefaultProfile</span></span>
<span data-ttu-id="05b01-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="05b01-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="05b01-126">-EncryptionKeyIdentifier</span><span class="sxs-lookup"><span data-stu-id="05b01-126">-EncryptionKeyIdentifier</span></span>
<span data-ttu-id="05b01-127">URI ключа хранилища ключей, используемого для шифрования данных.</span><span class="sxs-lookup"><span data-stu-id="05b01-127">The URI of the key vault key used to encrypt data.</span></span>

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

### <span data-ttu-id="05b01-128">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="05b01-128">-IdentityType</span></span>
<span data-ttu-id="05b01-129">Тип используемого управляемого удостоверения.</span><span class="sxs-lookup"><span data-stu-id="05b01-129">The type of managed identity used.</span></span>
<span data-ttu-id="05b01-130">Тип "SystemAssignedAndUserAssigned" включает в себя как неявно созданную идентификацию, так и набор идентификаторов, назначенных пользователем.</span><span class="sxs-lookup"><span data-stu-id="05b01-130">The type 'SystemAssignedAndUserAssigned' includes both an implicitly created identity and a set of user-assigned identities.</span></span>
<span data-ttu-id="05b01-131">Тип "нет" приведет к удалению всех удостоверений.</span><span class="sxs-lookup"><span data-stu-id="05b01-131">The type 'None' will remove any identities.</span></span>

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

### <span data-ttu-id="05b01-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="05b01-132">-InputObject</span></span>
<span data-ttu-id="05b01-133">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="05b01-133">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="05b01-134">-KeyVaultIdentityClientId</span><span class="sxs-lookup"><span data-stu-id="05b01-134">-KeyVaultIdentityClientId</span></span>
<span data-ttu-id="05b01-135">Идентификатор клиента для удостоверения, который будет использоваться для доступа к хранилищу ключей.</span><span class="sxs-lookup"><span data-stu-id="05b01-135">The client id of the identity which will be used to access key vault.</span></span>

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

### <span data-ttu-id="05b01-136">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="05b01-136">-Name</span></span>
<span data-ttu-id="05b01-137">Имя хранилища конфигураций.</span><span class="sxs-lookup"><span data-stu-id="05b01-137">The name of the configuration store.</span></span>

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

### <span data-ttu-id="05b01-138">-Wait</span><span class="sxs-lookup"><span data-stu-id="05b01-138">-NoWait</span></span>
<span data-ttu-id="05b01-139">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="05b01-139">Run the command asynchronously</span></span>

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

### <span data-ttu-id="05b01-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05b01-140">-ResourceGroupName</span></span>
<span data-ttu-id="05b01-141">Имя группы ресурсов, к которой принадлежит реестр контейнера.</span><span class="sxs-lookup"><span data-stu-id="05b01-141">The name of the resource group to which the container registry belongs.</span></span>

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

### <span data-ttu-id="05b01-142">-SKU</span><span class="sxs-lookup"><span data-stu-id="05b01-142">-Sku</span></span>
<span data-ttu-id="05b01-143">Имя SKU хранилища конфигураций.</span><span class="sxs-lookup"><span data-stu-id="05b01-143">The SKU name of the configuration store.</span></span>

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

### <span data-ttu-id="05b01-144">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="05b01-144">-SubscriptionId</span></span>
<span data-ttu-id="05b01-145">Идентификатор подписки Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="05b01-145">The Microsoft Azure subscription ID.</span></span>

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

### <span data-ttu-id="05b01-146">-Тег</span><span class="sxs-lookup"><span data-stu-id="05b01-146">-Tag</span></span>
<span data-ttu-id="05b01-147">Теги ресурсов ARM.</span><span class="sxs-lookup"><span data-stu-id="05b01-147">The ARM resource tags.</span></span>

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

### <span data-ttu-id="05b01-148">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="05b01-148">-UserAssignedIdentity</span></span>
<span data-ttu-id="05b01-149">Список назначенных пользователю удостоверений, связанных с ресурсом.</span><span class="sxs-lookup"><span data-stu-id="05b01-149">The list of user-assigned identities associated with the resource.</span></span>
<span data-ttu-id="05b01-150">Назначенные пользователем ключи словаря идентификаторов будут представлять собой идентификаторы ресурсов ARM в форме "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}".</span><span class="sxs-lookup"><span data-stu-id="05b01-150">The user-assigned identity dictionary keys will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span></span>

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

### <span data-ttu-id="05b01-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="05b01-151">-Confirm</span></span>
<span data-ttu-id="05b01-152">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="05b01-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05b01-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05b01-153">-WhatIf</span></span>
<span data-ttu-id="05b01-154">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="05b01-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05b01-155">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="05b01-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05b01-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05b01-156">CommonParameters</span></span>
<span data-ttu-id="05b01-157">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="05b01-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05b01-158">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="05b01-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05b01-159">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="05b01-159">INPUTS</span></span>

### <span data-ttu-id="05b01-160">Microsoft. Azure. PowerShell. командлеты. AppConfiguration. Models. IAppConfigurationIdentity</span><span class="sxs-lookup"><span data-stu-id="05b01-160">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity</span></span>

## <span data-ttu-id="05b01-161">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="05b01-161">OUTPUTS</span></span>

### <span data-ttu-id="05b01-162">Microsoft. Azure. PowerShell. командлеты. AppConfiguration. Models. Api20200601. IConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="05b01-162">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IConfigurationStore</span></span>

## <span data-ttu-id="05b01-163">Пуск</span><span class="sxs-lookup"><span data-stu-id="05b01-163">NOTES</span></span>

<span data-ttu-id="05b01-164">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="05b01-164">ALIASES</span></span>

<span data-ttu-id="05b01-165">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="05b01-165">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="05b01-166">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="05b01-166">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="05b01-167">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="05b01-167">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="05b01-168">INPUTOBJECT <IAppConfigurationIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="05b01-168">INPUTOBJECT <IAppConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="05b01-169">`[ConfigStoreName <String>]`: Имя хранилища конфигураций.</span><span class="sxs-lookup"><span data-stu-id="05b01-169">`[ConfigStoreName <String>]`: The name of the configuration store.</span></span>
  - <span data-ttu-id="05b01-170">`[GroupName <String>]`: Имя группы ресурсов частной ссылки.</span><span class="sxs-lookup"><span data-stu-id="05b01-170">`[GroupName <String>]`: The name of the private link resource group.</span></span>
  - <span data-ttu-id="05b01-171">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="05b01-171">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="05b01-172">`[PrivateEndpointConnectionName <String>]`: Имя частного подключения конечной точки</span><span class="sxs-lookup"><span data-stu-id="05b01-172">`[PrivateEndpointConnectionName <String>]`: Private endpoint connection name</span></span>
  - <span data-ttu-id="05b01-173">`[ResourceGroupName <String>]`: Имя группы ресурсов, к которой принадлежит реестр контейнера.</span><span class="sxs-lookup"><span data-stu-id="05b01-173">`[ResourceGroupName <String>]`: The name of the resource group to which the container registry belongs.</span></span>
  - <span data-ttu-id="05b01-174">`[SubscriptionId <String>]`: Идентификатор подписки Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="05b01-174">`[SubscriptionId <String>]`: The Microsoft Azure subscription ID.</span></span>

## <span data-ttu-id="05b01-175">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="05b01-175">RELATED LINKS</span></span>



<span data-ttu-id="05b01-176">[Set-AzKeyVaultAccessPolicy](https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultaccesspolicy?view=azps-4.4.0) 
 [New-AzUserAssignedIdentity](https://docs.microsoft.com/en-us/powershell/module/az.managedserviceidentity/new-azuserassignedidentity?view=azps-4.4.0)</span><span class="sxs-lookup"><span data-stu-id="05b01-176">[Set-AzKeyVaultAccessPolicy](https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultaccesspolicy?view=azps-4.4.0)
[New-AzUserAssignedIdentity](https://docs.microsoft.com/en-us/powershell/module/az.managedserviceidentity/new-azuserassignedidentity?view=azps-4.4.0)</span></span>


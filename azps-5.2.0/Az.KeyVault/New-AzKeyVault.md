---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 4C40DAC9-5C0B-4AFD-9BDB-D407E0B9F701
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVault.md
ms.openlocfilehash: 0da8ce1e7da509c140e5893240fadb37d7852ad8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98415223"
---
# <span data-ttu-id="72b00-101">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="72b00-101">New-AzKeyVault</span></span>

## <span data-ttu-id="72b00-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="72b00-102">SYNOPSIS</span></span>
<span data-ttu-id="72b00-103">Создание сейфа ключа.</span><span class="sxs-lookup"><span data-stu-id="72b00-103">Creates a key vault.</span></span>

## <span data-ttu-id="72b00-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="72b00-104">SYNTAX</span></span>

```
New-AzKeyVault [-Name] <String> [-ResourceGroupName] <String> [-Location] <String> [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-EnablePurgeProtection]
 [-EnableRbacAuthorization] [-SoftDeleteRetentionInDays <Int32>] [-Sku <String>] [-Tag <Hashtable>]
 [-NetworkRuleSet <PSKeyVaultNetworkRuleSet>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="72b00-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="72b00-105">DESCRIPTION</span></span>
<span data-ttu-id="72b00-106">При **нажатии на AzKeyVault** создается хранилище ключа в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="72b00-106">The **New-AzKeyVault** cmdlet creates a key vault in the specified resource group.</span></span> <span data-ttu-id="72b00-107">Этот cmdlet также предоставляет текущим входя в систему пользователю разрешения на добавление, удаление и секрет списков и секретов в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="72b00-107">This cmdlet also grants permissions to the currently logged on user to add, remove, or list keys and secrets in the key vault.</span></span>
<span data-ttu-id="72b00-108">Примечание. Если при попытке создать новое хранилище ключей подписка не зарегистрирована для использования пространства имен **Microsoft.KeyVault,** запустите **register-AzResourceProvider -ProviderNamespace "Microsoft.KeyVault",** а затем повторно запустите команду **New-AzKeyVault.**</span><span class="sxs-lookup"><span data-stu-id="72b00-108">Note: If you see the error **The subscription is not registered to use namespace 'Microsoft.KeyVault'** when you try to create your new key vault, run **Register-AzResourceProvider -ProviderNamespace "Microsoft.KeyVault"** and then rerun your **New-AzKeyVault** command.</span></span> <span data-ttu-id="72b00-109">Дополнительные сведения см. в register-AzResourceProvider.</span><span class="sxs-lookup"><span data-stu-id="72b00-109">For more information, see Register-AzResourceProvider.</span></span>

## <span data-ttu-id="72b00-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="72b00-110">EXAMPLES</span></span>

### <span data-ttu-id="72b00-111">Пример 1. Создание стандартного хранилища ключей</span><span class="sxs-lookup"><span data-stu-id="72b00-111">Example 1: Create a Standard key vault</span></span>
```powershell
PS C:\> New-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US'

Vault Name                       : contoso03vault
Resource Group Name              : group14
Location                         : East US
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/group14/providers
                                   /Microsoft.KeyVault/vaults/contoso03vault
Vault URI                        : https://contoso03vault.vault.azure.net/
Tenant ID                        : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
SKU                              : Standard
Enabled For Deployment?          : False
Enabled For Template Deployment? : False
Enabled For Disk Encryption?     : False
Soft Delete Enabled?             :
Access Policies                  :
                                   Tenant ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Object ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Application ID                             :
                                   Display Name                               : User Name (username@microsoft.com)
                                   Permissions to Keys                        : get, create, delete, list, update,
                                   import, backup, restore, recover
                                   Permissions to Secrets                     : get, list, set, delete, backup,
                                   restore, recover
                                   Permissions to Certificates                : get, delete, list, create, import,
                                   update, deleteissuers, getissuers, listissuers, managecontacts, manageissuers,
                                   setissuers, recover, backup, restore
                                   Permissions to (Key Vault Managed) Storage : delete, deletesas, get, getsas, list,
                                   listsas, regeneratekey, set, setsas, update, recover, backup, restore

Tags                             :
```

<span data-ttu-id="72b00-112">Эта команда создает хранилище с именем Contoso03Vault в регионе Azure East US.</span><span class="sxs-lookup"><span data-stu-id="72b00-112">This command creates a key vault named Contoso03Vault, in the Azure region East US.</span></span> <span data-ttu-id="72b00-113">Команда добавляет хранилище ключа в группу ресурсов с именем "Группа14".</span><span class="sxs-lookup"><span data-stu-id="72b00-113">The command adds the key vault to the resource group named Group14.</span></span> <span data-ttu-id="72b00-114">Так как команда не указывает значение параметра *SKU,* она создает стандартный сейф ключей.</span><span class="sxs-lookup"><span data-stu-id="72b00-114">Because the command does not specify a value for the *SKU* parameter, it creates a Standard key vault.</span></span>

### <span data-ttu-id="72b00-115">Пример 2. Создание сейфа ключа Premium</span><span class="sxs-lookup"><span data-stu-id="72b00-115">Example 2: Create a Premium key vault</span></span>
```powershell
PS C:\>New-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US' -Sku 'Premium'

Vault Name                       : contoso03vault
Resource Group Name              : group14
Location                         : East US
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/group14/providers
                                   /Microsoft.KeyVault/vaults/contoso03vault
Vault URI                        : https://contoso03vault.vault.azure.net/
Tenant ID                        : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
SKU                              : Premium
Enabled For Deployment?          : False
Enabled For Template Deployment? : False
Enabled For Disk Encryption?     : False
Soft Delete Enabled?             :
Access Policies                  :
                                   Tenant ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Object ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Application ID                             :
                                   Display Name                               : User Name (username@microsoft.com)
                                   Permissions to Keys                        : get, create, delete, list, update,
                                   import, backup, restore, recover
                                   Permissions to Secrets                     : get, list, set, delete, backup,
                                   restore, recover
                                   Permissions to Certificates                : get, delete, list, create, import,
                                   update, deleteissuers, getissuers, listissuers, managecontacts, manageissuers,
                                   setissuers, recover, backup, restore
                                   Permissions to (Key Vault Managed) Storage : delete, deletesas, get, getsas, list,
                                   listsas, regeneratekey, set, setsas, update, recover, backup, restore

Tags                             :
```

<span data-ttu-id="72b00-116">Эта команда создает хранилище ключей, как в предыдущем примере.</span><span class="sxs-lookup"><span data-stu-id="72b00-116">This command creates a key vault, just like the previous example.</span></span> <span data-ttu-id="72b00-117">Однако она указывает значение Premium для параметра *SKU,* чтобы создать хранилище ключей Premium.</span><span class="sxs-lookup"><span data-stu-id="72b00-117">However, it specifies a value of Premium for the *SKU* parameter to create a Premium key vault.</span></span>

### <span data-ttu-id="72b00-118">Пример 3</span><span class="sxs-lookup"><span data-stu-id="72b00-118">Example 3</span></span>
```powershell
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "110.0.1.0/24" -ServiceEndpoint Microsoft.KeyVault
PS C:\> $virtualNetwork = New-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG -Location westus -AddressPrefix "110.0.0.0/16" -Subnet $frontendSubnet
PS C:\> $myNetworkResId = (Get-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG).Subnets[0].Id
PS C:\> $ruleSet = New-AzKeyVaultNetworkRuleSetObject -DefaultAction Allow -Bypass AzureServices -IpAddressRange "110.0.1.0/24" -VirtualNetworkResourceId $myNetworkResId
PS C:\> New-AzKeyVault -ResourceGroupName "myRg" -VaultName "myVault" -NetworkRuleSet $ruleSet
```

<span data-ttu-id="72b00-119">Создание сейфа ключа и определяет правила сети, позволяющие получить доступ к указанному IP-адресу из виртуальной сети, указанной $myNetworkResId.</span><span class="sxs-lookup"><span data-stu-id="72b00-119">Creating a key vault and specifies network rules to allow access to the specified IP address from the virtual network identified by $myNetworkResId.</span></span> <span data-ttu-id="72b00-120">Дополнительные `New-AzKeyVaultNetworkRuleSetObject` сведения см. в этой информации.</span><span class="sxs-lookup"><span data-stu-id="72b00-120">See `New-AzKeyVaultNetworkRuleSetObject` for more information.</span></span>

## <span data-ttu-id="72b00-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="72b00-121">PARAMETERS</span></span>

### <span data-ttu-id="72b00-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72b00-122">-DefaultProfile</span></span>
<span data-ttu-id="72b00-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="72b00-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="72b00-124">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="72b00-124">-EnabledForDeployment</span></span>
<span data-ttu-id="72b00-125">Позволяет поставщику ресурсов Microsoft.Compute извлекать секрет из этого ключевого сейфа, когда на него ссылается создание ресурсов, например при создании виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="72b00-125">Enables the Microsoft.Compute resource provider to retrieve secrets from this key vault when this key vault is referenced in resource creation, for example when creating a virtual machine.</span></span>

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

### <span data-ttu-id="72b00-126">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="72b00-126">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="72b00-127">Позволяет службе шифрования дисков Azure получать секрет и отобирать ключи из этого key vault.</span><span class="sxs-lookup"><span data-stu-id="72b00-127">Enables the Azure disk encryption service to get secrets and unwrap keys from this key vault.</span></span>

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

### <span data-ttu-id="72b00-128">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="72b00-128">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="72b00-129">Позволяет Диспетчеру ресурсов Azure получать секрет из этого сейфа ключа, если на него ссылается развертывание шаблонов.</span><span class="sxs-lookup"><span data-stu-id="72b00-129">Enables Azure Resource Manager to get secrets from this key vault when this key vault is referenced in a template deployment.</span></span>

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

### <span data-ttu-id="72b00-130">-EnablePurgeProtection</span><span class="sxs-lookup"><span data-stu-id="72b00-130">-EnablePurgeProtection</span></span>
<span data-ttu-id="72b00-131">При этом для этого хранилища включена защита от немедленного удаления. требуется также мягкий удаление.</span><span class="sxs-lookup"><span data-stu-id="72b00-131">If specified, protection against immediate deletion is enabled for this vault; requires soft delete to be enabled as well.</span></span>

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

### <span data-ttu-id="72b00-132">-EnableRbacAuthorization</span><span class="sxs-lookup"><span data-stu-id="72b00-132">-EnableRbacAuthorization</span></span>
<span data-ttu-id="72b00-133">Если задан этот вариант, разрешает действия с данными с помощью управления доступом на основе ролей (RBAC), а политики доступа, указанные в свойствах хранилища, будут игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="72b00-133">If specified, enables to authorize data actions by Role Based Access Control (RBAC), and then the access policies specified in vault properties will be ignored.</span></span> <span data-ttu-id="72b00-134">Обратите внимание на то, что действия управления всегда разрешены с помощью RBAC.</span><span class="sxs-lookup"><span data-stu-id="72b00-134">Note that management actions are always authorized with RBAC.</span></span>

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

### <span data-ttu-id="72b00-135">-Location</span><span class="sxs-lookup"><span data-stu-id="72b00-135">-Location</span></span>
<span data-ttu-id="72b00-136">Определяет регион Azure, в котором нужно создать хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="72b00-136">Specifies the Azure region in which to create the key vault.</span></span> <span data-ttu-id="72b00-137">Используйте команду [Get-AzLocation,](https://docs.microsoft.com/powershell/module/Azure/Get-AzLocation) чтобы увидеть ваши варианты.</span><span class="sxs-lookup"><span data-stu-id="72b00-137">Use the command [Get-AzLocation](https://docs.microsoft.com/powershell/module/Azure/Get-AzLocation) to see your choices.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72b00-138">-Name</span><span class="sxs-lookup"><span data-stu-id="72b00-138">-Name</span></span>
<span data-ttu-id="72b00-139">Указывает имя создаемого хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="72b00-139">Specifies a name of the key vault to create.</span></span> <span data-ttu-id="72b00-140">Имя может быть любым сочетанием букв, цифр или дефисов.</span><span class="sxs-lookup"><span data-stu-id="72b00-140">The name can be any combination of letters, digits, or hyphens.</span></span> <span data-ttu-id="72b00-141">Имя должно начинаться с буквы или цифры.</span><span class="sxs-lookup"><span data-stu-id="72b00-141">The name must start and end with a letter or digit.</span></span> <span data-ttu-id="72b00-142">Имя должно быть универсальным.</span><span class="sxs-lookup"><span data-stu-id="72b00-142">The name must be universally unique.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: VaultName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72b00-143">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="72b00-143">-NetworkRuleSet</span></span>
<span data-ttu-id="72b00-144">Набор правил сети для хранилища.</span><span class="sxs-lookup"><span data-stu-id="72b00-144">Specifies the network rule set of the vault.</span></span> <span data-ttu-id="72b00-145">Он регулирует специальные возможности ключного хранилища из определенных сетевых мест.</span><span class="sxs-lookup"><span data-stu-id="72b00-145">It governs the accessibility of the key vault from specific network locations.</span></span> <span data-ttu-id="72b00-146">Создано `New-AzKeyVaultNetworkRuleSetObject` .</span><span class="sxs-lookup"><span data-stu-id="72b00-146">Created by `New-AzKeyVaultNetworkRuleSetObject`.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleSet
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72b00-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72b00-147">-ResourceGroupName</span></span>
<span data-ttu-id="72b00-148">Указывает имя существующей группы ресурсов, в которой нужно создать хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="72b00-148">Specifies the name of an existing resource group in which to create the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72b00-149">-SKU</span><span class="sxs-lookup"><span data-stu-id="72b00-149">-Sku</span></span>
<span data-ttu-id="72b00-150">Указывает SKU экземпляра key vault.</span><span class="sxs-lookup"><span data-stu-id="72b00-150">Specifies the SKU of the key vault instance.</span></span> <span data-ttu-id="72b00-151">Сведения о том, какие возможности доступны для каждого SKU, см. на веб-сайте цены на ключ хранилища Azure ( https://go.microsoft.com/fwlink/?linkid=512521) .</span><span class="sxs-lookup"><span data-stu-id="72b00-151">For information about which features are available for each SKU, see the Azure Key Vault Pricing website (https://go.microsoft.com/fwlink/?linkid=512521).</span></span>

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

### <span data-ttu-id="72b00-152">-SoftDeleteRetentionInDays</span><span class="sxs-lookup"><span data-stu-id="72b00-152">-SoftDeleteRetentionInDays</span></span>
<span data-ttu-id="72b00-153">Определяет время сохранения удаленных ресурсов и время, пока хранилище или объект в удаленном состоянии не будут удалены.</span><span class="sxs-lookup"><span data-stu-id="72b00-153">Specifies how long deleted resources are retained, and how long until a vault or an object in the deleted state can be purged.</span></span> <span data-ttu-id="72b00-154">Значение по умолчанию — 90 дней.</span><span class="sxs-lookup"><span data-stu-id="72b00-154">The default is 90 days.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72b00-155">-Tag</span><span class="sxs-lookup"><span data-stu-id="72b00-155">-Tag</span></span>
<span data-ttu-id="72b00-156">Пары значений ключа в виде hash table.</span><span class="sxs-lookup"><span data-stu-id="72b00-156">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="72b00-157">Например: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="72b00-157">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72b00-158">-Confirm</span><span class="sxs-lookup"><span data-stu-id="72b00-158">-Confirm</span></span>
<span data-ttu-id="72b00-159">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72b00-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72b00-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72b00-160">-WhatIf</span></span>
<span data-ttu-id="72b00-161">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72b00-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72b00-162">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="72b00-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72b00-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72b00-163">CommonParameters</span></span>
<span data-ttu-id="72b00-164">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72b00-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72b00-165">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="72b00-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72b00-166">INPUTS</span><span class="sxs-lookup"><span data-stu-id="72b00-166">INPUTS</span></span>

### <span data-ttu-id="72b00-167">System.String</span><span class="sxs-lookup"><span data-stu-id="72b00-167">System.String</span></span>

### <span data-ttu-id="72b00-168">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="72b00-168">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="72b00-169">Microsoft.Azure.Management.KeyVault.Models.SkuName</span><span class="sxs-lookup"><span data-stu-id="72b00-169">Microsoft.Azure.Management.KeyVault.Models.SkuName</span></span>

### <span data-ttu-id="72b00-170">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="72b00-170">System.Collections.Hashtable</span></span>

## <span data-ttu-id="72b00-171">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="72b00-171">OUTPUTS</span></span>

### <span data-ttu-id="72b00-172">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="72b00-172">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="72b00-173">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="72b00-173">NOTES</span></span>

## <span data-ttu-id="72b00-174">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="72b00-174">RELATED LINKS</span></span>

[<span data-ttu-id="72b00-175">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="72b00-175">Get-AzKeyVault</span></span>](./Get-AzKeyVault.md)

[<span data-ttu-id="72b00-176">Remove-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="72b00-176">Remove-AzKeyVault</span></span>](./Remove-AzKeyVault.md)

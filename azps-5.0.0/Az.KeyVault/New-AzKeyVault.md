---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 4C40DAC9-5C0B-4AFD-9BDB-D407E0B9F701
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVault.md
ms.openlocfilehash: 0da8ce1e7da509c140e5893240fadb37d7852ad8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94250214"
---
# <span data-ttu-id="ddffa-101">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="ddffa-101">New-AzKeyVault</span></span>

## <span data-ttu-id="ddffa-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ddffa-102">SYNOPSIS</span></span>
<span data-ttu-id="ddffa-103">Создание хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="ddffa-103">Creates a key vault.</span></span>

## <span data-ttu-id="ddffa-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ddffa-104">SYNTAX</span></span>

```
New-AzKeyVault [-Name] <String> [-ResourceGroupName] <String> [-Location] <String> [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-EnablePurgeProtection]
 [-EnableRbacAuthorization] [-SoftDeleteRetentionInDays <Int32>] [-Sku <String>] [-Tag <Hashtable>]
 [-NetworkRuleSet <PSKeyVaultNetworkRuleSet>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ddffa-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ddffa-105">DESCRIPTION</span></span>
<span data-ttu-id="ddffa-106">Командлет **New-AzKeyVault** создает хранилище ключей в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ddffa-106">The **New-AzKeyVault** cmdlet creates a key vault in the specified resource group.</span></span> <span data-ttu-id="ddffa-107">Этот командлет также предоставляет пользователям разрешения на добавление, удаление или перечисление ключей и секретных параметров в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="ddffa-107">This cmdlet also grants permissions to the currently logged on user to add, remove, or list keys and secrets in the key vault.</span></span>
<span data-ttu-id="ddffa-108">Примечание. Если вы видите сообщение об ошибке **"не зарегистрирована подписка на использование пространства имен" Microsoft. KeyVault "** при попытке создания нового хранилища ключей, выполните команду **Register-AzResourceProvider-ProviderNamespace" Microsoft. KeyVault "** , а затем снова запустите программу **New-AzKeyVault** .</span><span class="sxs-lookup"><span data-stu-id="ddffa-108">Note: If you see the error **The subscription is not registered to use namespace 'Microsoft.KeyVault'** when you try to create your new key vault, run **Register-AzResourceProvider -ProviderNamespace "Microsoft.KeyVault"** and then rerun your **New-AzKeyVault** command.</span></span> <span data-ttu-id="ddffa-109">Дополнительные сведения можно найти в разделе Register-AzResourceProvider.</span><span class="sxs-lookup"><span data-stu-id="ddffa-109">For more information, see Register-AzResourceProvider.</span></span>

## <span data-ttu-id="ddffa-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ddffa-110">EXAMPLES</span></span>

### <span data-ttu-id="ddffa-111">Пример 1: создание стандартного хранилища ключей</span><span class="sxs-lookup"><span data-stu-id="ddffa-111">Example 1: Create a Standard key vault</span></span>
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

<span data-ttu-id="ddffa-112">Эта команда создает хранилище ключей с именем Contoso03Vault в Azure Region East США.</span><span class="sxs-lookup"><span data-stu-id="ddffa-112">This command creates a key vault named Contoso03Vault, in the Azure region East US.</span></span> <span data-ttu-id="ddffa-113">Команда добавляет хранилище ключей в группу ресурсов с именем Group14.</span><span class="sxs-lookup"><span data-stu-id="ddffa-113">The command adds the key vault to the resource group named Group14.</span></span> <span data-ttu-id="ddffa-114">Поскольку в команде не указано значение параметра *SKU* , создается стандартное хранилище ключа.</span><span class="sxs-lookup"><span data-stu-id="ddffa-114">Because the command does not specify a value for the *SKU* parameter, it creates a Standard key vault.</span></span>

### <span data-ttu-id="ddffa-115">Пример 2: создание хранилища ключей Premium</span><span class="sxs-lookup"><span data-stu-id="ddffa-115">Example 2: Create a Premium key vault</span></span>
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

<span data-ttu-id="ddffa-116">Эта команда создает хранилище ключей, как и в предыдущем примере.</span><span class="sxs-lookup"><span data-stu-id="ddffa-116">This command creates a key vault, just like the previous example.</span></span> <span data-ttu-id="ddffa-117">Тем не менее, он задает значение Premium для параметра *SKU* для создания хранилища ключей Premium.</span><span class="sxs-lookup"><span data-stu-id="ddffa-117">However, it specifies a value of Premium for the *SKU* parameter to create a Premium key vault.</span></span>

### <span data-ttu-id="ddffa-118">Пример 3</span><span class="sxs-lookup"><span data-stu-id="ddffa-118">Example 3</span></span>
```powershell
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "110.0.1.0/24" -ServiceEndpoint Microsoft.KeyVault
PS C:\> $virtualNetwork = New-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG -Location westus -AddressPrefix "110.0.0.0/16" -Subnet $frontendSubnet
PS C:\> $myNetworkResId = (Get-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG).Subnets[0].Id
PS C:\> $ruleSet = New-AzKeyVaultNetworkRuleSetObject -DefaultAction Allow -Bypass AzureServices -IpAddressRange "110.0.1.0/24" -VirtualNetworkResourceId $myNetworkResId
PS C:\> New-AzKeyVault -ResourceGroupName "myRg" -VaultName "myVault" -NetworkRuleSet $ruleSet
```

<span data-ttu-id="ddffa-119">Создайте хранилище ключей и определяет сетевые правила, разрешающие доступ к указанному IP-адресу из виртуальной сети, определенной $myNetworkResId.</span><span class="sxs-lookup"><span data-stu-id="ddffa-119">Creating a key vault and specifies network rules to allow access to the specified IP address from the virtual network identified by $myNetworkResId.</span></span> <span data-ttu-id="ddffa-120">`New-AzKeyVaultNetworkRuleSetObject`Для получения дополнительных сведений ознакомьтесь с дополнительными сведениями.</span><span class="sxs-lookup"><span data-stu-id="ddffa-120">See `New-AzKeyVaultNetworkRuleSetObject` for more information.</span></span>

## <span data-ttu-id="ddffa-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ddffa-121">PARAMETERS</span></span>

### <span data-ttu-id="ddffa-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddffa-122">-DefaultProfile</span></span>
<span data-ttu-id="ddffa-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="ddffa-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ddffa-124">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="ddffa-124">-EnabledForDeployment</span></span>
<span data-ttu-id="ddffa-125">Включает поставщик ресурсов Microsoft. COMPUTE для извлечения секретов из этого ключа, если это временное хранилище ссылается на создание ресурсов (например, при создании виртуальной машины).</span><span class="sxs-lookup"><span data-stu-id="ddffa-125">Enables the Microsoft.Compute resource provider to retrieve secrets from this key vault when this key vault is referenced in resource creation, for example when creating a virtual machine.</span></span>

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

### <span data-ttu-id="ddffa-126">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="ddffa-126">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="ddffa-127">Позволяет службе шифрования дисков Azure получить секретные ключи и их перетекание из этого хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="ddffa-127">Enables the Azure disk encryption service to get secrets and unwrap keys from this key vault.</span></span>

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

### <span data-ttu-id="ddffa-128">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="ddffa-128">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="ddffa-129">Позволяет диспетчеру ресурсов Azure получать секреты из этого хранилища ключей при ссылке на это хранилище ключей в развертывании шаблона.</span><span class="sxs-lookup"><span data-stu-id="ddffa-129">Enables Azure Resource Manager to get secrets from this key vault when this key vault is referenced in a template deployment.</span></span>

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

### <span data-ttu-id="ddffa-130">-EnablePurgeProtection</span><span class="sxs-lookup"><span data-stu-id="ddffa-130">-EnablePurgeProtection</span></span>
<span data-ttu-id="ddffa-131">Если задано, защита от немедленного удаления включена для этого хранилища; требуется также мягкое удаление.</span><span class="sxs-lookup"><span data-stu-id="ddffa-131">If specified, protection against immediate deletion is enabled for this vault; requires soft delete to be enabled as well.</span></span>

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

### <span data-ttu-id="ddffa-132">-EnableRbacAuthorization</span><span class="sxs-lookup"><span data-stu-id="ddffa-132">-EnableRbacAuthorization</span></span>
<span data-ttu-id="ddffa-133">Если задано, разрешает выполнять действия с данными с помощью управления доступом на основе ролей (RBAC), а затем политики доступа, указанные в свойствах хранилища, будут игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="ddffa-133">If specified, enables to authorize data actions by Role Based Access Control (RBAC), and then the access policies specified in vault properties will be ignored.</span></span> <span data-ttu-id="ddffa-134">Обратите внимание, что действия управления всегда разрешены с помощью RBAC.</span><span class="sxs-lookup"><span data-stu-id="ddffa-134">Note that management actions are always authorized with RBAC.</span></span>

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

### <span data-ttu-id="ddffa-135">-Location</span><span class="sxs-lookup"><span data-stu-id="ddffa-135">-Location</span></span>
<span data-ttu-id="ddffa-136">Указывает область Azure, в которой нужно создать хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="ddffa-136">Specifies the Azure region in which to create the key vault.</span></span> <span data-ttu-id="ddffa-137">С помощью команды [Get-AzLocation](https://docs.microsoft.com/powershell/module/Azure/Get-AzLocation) можно просмотреть варианты выбора.</span><span class="sxs-lookup"><span data-stu-id="ddffa-137">Use the command [Get-AzLocation](https://docs.microsoft.com/powershell/module/Azure/Get-AzLocation) to see your choices.</span></span>

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

### <span data-ttu-id="ddffa-138">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ddffa-138">-Name</span></span>
<span data-ttu-id="ddffa-139">Задает имя создаваемого хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="ddffa-139">Specifies a name of the key vault to create.</span></span> <span data-ttu-id="ddffa-140">Имя может представлять собой любую комбинацию букв, цифр или дефисов.</span><span class="sxs-lookup"><span data-stu-id="ddffa-140">The name can be any combination of letters, digits, or hyphens.</span></span> <span data-ttu-id="ddffa-141">Имя должно начинаться и заканчиваться на букву или цифру.</span><span class="sxs-lookup"><span data-stu-id="ddffa-141">The name must start and end with a letter or digit.</span></span> <span data-ttu-id="ddffa-142">Имя должно быть универсальным уникальным.</span><span class="sxs-lookup"><span data-stu-id="ddffa-142">The name must be universally unique.</span></span>

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

### <span data-ttu-id="ddffa-143">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="ddffa-143">-NetworkRuleSet</span></span>
<span data-ttu-id="ddffa-144">Указывает набор сетевых правил хранилища.</span><span class="sxs-lookup"><span data-stu-id="ddffa-144">Specifies the network rule set of the vault.</span></span> <span data-ttu-id="ddffa-145">Он определяет доступность ключа для хранилища с определенными сетевыми адресами.</span><span class="sxs-lookup"><span data-stu-id="ddffa-145">It governs the accessibility of the key vault from specific network locations.</span></span> <span data-ttu-id="ddffa-146">Кем создано `New-AzKeyVaultNetworkRuleSetObject` .</span><span class="sxs-lookup"><span data-stu-id="ddffa-146">Created by `New-AzKeyVaultNetworkRuleSetObject`.</span></span>

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

### <span data-ttu-id="ddffa-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ddffa-147">-ResourceGroupName</span></span>
<span data-ttu-id="ddffa-148">Указывает имя существующей группы ресурсов, в которой нужно создать хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="ddffa-148">Specifies the name of an existing resource group in which to create the key vault.</span></span>

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

### <span data-ttu-id="ddffa-149">-SKU</span><span class="sxs-lookup"><span data-stu-id="ddffa-149">-Sku</span></span>
<span data-ttu-id="ddffa-150">Указывает SKU экземпляра хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="ddffa-150">Specifies the SKU of the key vault instance.</span></span> <span data-ttu-id="ddffa-151">Сведения о том, какие функции доступны для каждого SKU, можно найти на веб-сайте ценообразования для Azure Key Vault ( https://go.microsoft.com/fwlink/?linkid=512521) .</span><span class="sxs-lookup"><span data-stu-id="ddffa-151">For information about which features are available for each SKU, see the Azure Key Vault Pricing website (https://go.microsoft.com/fwlink/?linkid=512521).</span></span>

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

### <span data-ttu-id="ddffa-152">-SoftDeleteRetentionInDays</span><span class="sxs-lookup"><span data-stu-id="ddffa-152">-SoftDeleteRetentionInDays</span></span>
<span data-ttu-id="ddffa-153">Указывает, как долго будут храниться удаленные ресурсы, а также как долго, пока не будет очищено хранилище или объект в удаленном состоянии.</span><span class="sxs-lookup"><span data-stu-id="ddffa-153">Specifies how long deleted resources are retained, and how long until a vault or an object in the deleted state can be purged.</span></span> <span data-ttu-id="ddffa-154">Значение по умолчанию — 90 дней.</span><span class="sxs-lookup"><span data-stu-id="ddffa-154">The default is 90 days.</span></span>

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

### <span data-ttu-id="ddffa-155">-Тег</span><span class="sxs-lookup"><span data-stu-id="ddffa-155">-Tag</span></span>
<span data-ttu-id="ddffa-156">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="ddffa-156">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="ddffa-157">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="ddffa-157">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="ddffa-158">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ddffa-158">-Confirm</span></span>
<span data-ttu-id="ddffa-159">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ddffa-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ddffa-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ddffa-160">-WhatIf</span></span>
<span data-ttu-id="ddffa-161">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ddffa-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ddffa-162">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ddffa-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ddffa-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddffa-163">CommonParameters</span></span>
<span data-ttu-id="ddffa-164">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ddffa-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddffa-165">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ddffa-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddffa-166">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ddffa-166">INPUTS</span></span>

### <span data-ttu-id="ddffa-167">System. String</span><span class="sxs-lookup"><span data-stu-id="ddffa-167">System.String</span></span>

### <span data-ttu-id="ddffa-168">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ddffa-168">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="ddffa-169">Microsoft. Azure. Management. KeyVault. Models. SkuName</span><span class="sxs-lookup"><span data-stu-id="ddffa-169">Microsoft.Azure.Management.KeyVault.Models.SkuName</span></span>

### <span data-ttu-id="ddffa-170">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="ddffa-170">System.Collections.Hashtable</span></span>

## <span data-ttu-id="ddffa-171">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ddffa-171">OUTPUTS</span></span>

### <span data-ttu-id="ddffa-172">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="ddffa-172">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="ddffa-173">Пуск</span><span class="sxs-lookup"><span data-stu-id="ddffa-173">NOTES</span></span>

## <span data-ttu-id="ddffa-174">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ddffa-174">RELATED LINKS</span></span>

[<span data-ttu-id="ddffa-175">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="ddffa-175">Get-AzKeyVault</span></span>](./Get-AzKeyVault.md)

[<span data-ttu-id="ddffa-176">Remove-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="ddffa-176">Remove-AzKeyVault</span></span>](./Remove-AzKeyVault.md)

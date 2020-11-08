---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvaultnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultNetworkRuleSet.md
ms.openlocfilehash: 6d264ff7e2f12777845edbf2d56cae3d8b59ddb0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94250189"
---
# <span data-ttu-id="933de-101">Update-AzKeyVaultNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="933de-101">Update-AzKeyVaultNetworkRuleSet</span></span>

## <span data-ttu-id="933de-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="933de-102">SYNOPSIS</span></span>
<span data-ttu-id="933de-103">Обновляет сетевое правило, установленное в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="933de-103">Updates the network rule set on a key vault.</span></span>

## <span data-ttu-id="933de-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="933de-104">SYNTAX</span></span>

### <span data-ttu-id="933de-105">ByVaultName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="933de-105">ByVaultName (Default)</span></span>
```
Update-AzKeyVaultNetworkRuleSet [-VaultName] <String> [[-ResourceGroupName] <String>]
 [-DefaultAction <PSKeyVaultNetworkRuleDefaultActionEnum>] [-Bypass <PSKeyVaultNetworkRuleBypassEnum>]
 [-IpAddressRange <String[]>] [-VirtualNetworkResourceId <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="933de-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="933de-106">ByInputObject</span></span>
```
Update-AzKeyVaultNetworkRuleSet [-InputObject] <PSKeyVault>
 [-DefaultAction <PSKeyVaultNetworkRuleDefaultActionEnum>] [-Bypass <PSKeyVaultNetworkRuleBypassEnum>]
 [-IpAddressRange <String[]>] [-VirtualNetworkResourceId <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="933de-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="933de-107">ByResourceId</span></span>
```
Update-AzKeyVaultNetworkRuleSet [-ResourceId] <String>
 [-DefaultAction <PSKeyVaultNetworkRuleDefaultActionEnum>] [-Bypass <PSKeyVaultNetworkRuleBypassEnum>]
 [-IpAddressRange <String[]>] [-VirtualNetworkResourceId <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="933de-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="933de-108">DESCRIPTION</span></span>
<span data-ttu-id="933de-109">Команда **Update-AzKeyVaultNetworkRuleSet** обновляет сетевые правила, действующие в указанном хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="933de-109">The **Update-AzKeyVaultNetworkRuleSet** command updates the network rules in effect on the specified key vault.</span></span> 

## <span data-ttu-id="933de-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="933de-110">EXAMPLES</span></span>

### <span data-ttu-id="933de-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="933de-111">Example 1</span></span>
```powershell
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24" -ServiceEndpoint Microsoft.KeyVault 
PS C:\> $virtualNetwork = New-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG -Location westus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
PS C:\> $myNetworkResId = (Get-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG).Subnets[0].Id
PS C:\> Update-AzKeyVaultNetworkRuleSet -VaultName 'myVault' -ResourceGroupName myRG -Bypass AzureServices -IpAddressRange "10.0.1.0/24" -VirtualNetworkResourceId $myNetworkResId -PassThru

Vault Name                       : myVault
Resource Group Name              : myRG
Location                         : West US
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers
                                   /Microsoft.KeyVault/vaults/myvault
Vault URI                        : https://myvault.vault.azure.net/
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


Network Rule Set                 :
                                   Default Action                             : Allow
                                   Bypass                                     : AzureServices
                                   IP Rules                                   : 10.0.1.0/24
                                   Virtual Network Rules                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-
                                   xxxxxxxxxxxxx/resourcegroups/myrg/providers/microsoft.network/virtualnetworks/myvn
                                   et/subnets/frontendsubnet

Tags                             :
```

<span data-ttu-id="933de-112">Эта команда обновляет набор правил сети в хранилище с именем "myVault" для указанного диапазона IP-адресов и виртуальной сети, позволяя пропускать сетевые правила для служб Azure.</span><span class="sxs-lookup"><span data-stu-id="933de-112">This command updates the network ruleset on the vault named 'myVault' for the specified IP range and the virtual network, allowing bypassing of the network rule for Azure services.</span></span>

### <span data-ttu-id="933de-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="933de-113">Example 2</span></span>

<span data-ttu-id="933de-114">Обновляет сетевое правило, установленное в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="933de-114">Updates the network rule set on a key vault.</span></span> <span data-ttu-id="933de-115">(автоматически сформированные)</span><span class="sxs-lookup"><span data-stu-id="933de-115">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Update-AzKeyVaultNetworkRuleSet -DefaultAction Allow -VaultName 'myVault'
```

## <span data-ttu-id="933de-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="933de-116">PARAMETERS</span></span>

### <span data-ttu-id="933de-117">-Обход</span><span class="sxs-lookup"><span data-stu-id="933de-117">-Bypass</span></span>
<span data-ttu-id="933de-118">Указывает обход сетевого правила.</span><span class="sxs-lookup"><span data-stu-id="933de-118">Specifies bypass of network rule.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleBypassEnum]
Parameter Sets: (All)
Aliases:
Accepted values: None, AzureServices

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="933de-119">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="933de-119">-DefaultAction</span></span>
<span data-ttu-id="933de-120">Задает действие по умолчанию для сетевого правила.</span><span class="sxs-lookup"><span data-stu-id="933de-120">Specifies default action of network rule.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleDefaultActionEnum]
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="933de-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="933de-121">-DefaultProfile</span></span>
<span data-ttu-id="933de-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="933de-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="933de-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="933de-123">-InputObject</span></span>
<span data-ttu-id="933de-124">Объект KeyVault</span><span class="sxs-lookup"><span data-stu-id="933de-124">KeyVault object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="933de-125">-IpAddressRange</span><span class="sxs-lookup"><span data-stu-id="933de-125">-IpAddressRange</span></span>
<span data-ttu-id="933de-126">Указывает допустимый диапазон IP-адресов сети сетевого правила.</span><span class="sxs-lookup"><span data-stu-id="933de-126">Specifies allowed network IP address range of network rule.</span></span>

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

### <span data-ttu-id="933de-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="933de-127">-PassThru</span></span>
<span data-ttu-id="933de-128">Этот командлет не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="933de-128">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="933de-129">Если указан этот параметр, возвращается обновленный объект Key Vault.</span><span class="sxs-lookup"><span data-stu-id="933de-129">If this switch is specified, it returns the updated key vault object.</span></span>

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

### <span data-ttu-id="933de-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="933de-130">-ResourceGroupName</span></span>
<span data-ttu-id="933de-131">Указывает имя группы ресурсов, связанной с хранилищем ключей, для которого изменяется сетевое правило.</span><span class="sxs-lookup"><span data-stu-id="933de-131">Specifies the name of the resource group associated with the key vault whose network rule is being modified.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="933de-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="933de-132">-ResourceId</span></span>
<span data-ttu-id="933de-133">Идентификатор ресурса KeyVault</span><span class="sxs-lookup"><span data-stu-id="933de-133">KeyVault Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="933de-134">-VaultName</span><span class="sxs-lookup"><span data-stu-id="933de-134">-VaultName</span></span>
<span data-ttu-id="933de-135">Указывает имя хранилища ключей, сетевое правило которого изменяется.</span><span class="sxs-lookup"><span data-stu-id="933de-135">Specifies the name of a key vault whose network rule is being modified.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="933de-136">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="933de-136">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="933de-137">Указывает допустимый идентификатор ресурса виртуальной сети для сетевого правила.</span><span class="sxs-lookup"><span data-stu-id="933de-137">Specifies allowed virtual network resource identifier of network rule.</span></span>

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

### <span data-ttu-id="933de-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="933de-138">-Confirm</span></span>
<span data-ttu-id="933de-139">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="933de-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="933de-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="933de-140">-WhatIf</span></span>
<span data-ttu-id="933de-141">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="933de-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="933de-142">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="933de-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="933de-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="933de-143">CommonParameters</span></span>
<span data-ttu-id="933de-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="933de-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="933de-145">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="933de-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="933de-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="933de-146">INPUTS</span></span>

### <span data-ttu-id="933de-147">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="933de-147">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="933de-148">System. String</span><span class="sxs-lookup"><span data-stu-id="933de-148">System.String</span></span>

### <span data-ttu-id="933de-149">System. Nullable "1 [[Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultNetworkRuleDefaultActionEnum, Microsoft. Azure. PowerShell. командлеты. KeyVault, Version = 1.0.0.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="933de-149">System.Nullable\`1[[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleDefaultActionEnum, Microsoft.Azure.PowerShell.Cmdlets.KeyVault, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="933de-150">System. Nullable "1 [[Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultNetworkRuleBypassEnum, Microsoft. Azure. PowerShell. командлеты. KeyVault, Version = 1.0.0.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="933de-150">System.Nullable\`1[[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleBypassEnum, Microsoft.Azure.PowerShell.Cmdlets.KeyVault, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="933de-151">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="933de-151">OUTPUTS</span></span>

### <span data-ttu-id="933de-152">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="933de-152">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="933de-153">Пуск</span><span class="sxs-lookup"><span data-stu-id="933de-153">NOTES</span></span>

## <span data-ttu-id="933de-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="933de-154">RELATED LINKS</span></span>

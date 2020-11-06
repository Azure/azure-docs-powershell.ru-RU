---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/update-azurermkeyvaultnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Update-AzureRmKeyVaultNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Update-AzureRmKeyVaultNetworkRuleSet.md
ms.openlocfilehash: b1a0081f24932cf25026bdea4e9064e9dbb5a0cb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562979"
---
# <span data-ttu-id="9071e-101">Update-AzureRmKeyVaultNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="9071e-101">Update-AzureRmKeyVaultNetworkRuleSet</span></span>

## <span data-ttu-id="9071e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9071e-102">SYNOPSIS</span></span>
<span data-ttu-id="9071e-103">Обновляет сетевое правило, установленное в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="9071e-103">Updates the network rule set on a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9071e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9071e-104">SYNTAX</span></span>

### <span data-ttu-id="9071e-105">ByVaultName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9071e-105">ByVaultName (Default)</span></span>
```
Update-AzureRmKeyVaultNetworkRuleSet [-VaultName] <String> [[-ResourceGroupName] <String>]
 [-DefaultAction <PSKeyVaultNetworkRuleDefaultActionEnum>] [-Bypass <PSKeyVaultNetworkRuleBypassEnum>]
 [-IpAddressRange <String[]>] [-VirtualNetworkResourceId <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9071e-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="9071e-106">ByInputObject</span></span>
```
Update-AzureRmKeyVaultNetworkRuleSet [-InputObject] <PSKeyVault>
 [-DefaultAction <PSKeyVaultNetworkRuleDefaultActionEnum>] [-Bypass <PSKeyVaultNetworkRuleBypassEnum>]
 [-IpAddressRange <String[]>] [-VirtualNetworkResourceId <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9071e-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="9071e-107">ByResourceId</span></span>
```
Update-AzureRmKeyVaultNetworkRuleSet [-ResourceId] <String>
 [-DefaultAction <PSKeyVaultNetworkRuleDefaultActionEnum>] [-Bypass <PSKeyVaultNetworkRuleBypassEnum>]
 [-IpAddressRange <String[]>] [-VirtualNetworkResourceId <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9071e-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9071e-108">DESCRIPTION</span></span>
<span data-ttu-id="9071e-109">Команда **Update-AzureRmKeyVaultNetworkRuleSet** обновляет сетевые правила, действующие в указанном хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="9071e-109">The **Update-AzureRmKeyVaultNetworkRuleSet** command updates the network rules in effect on the specified key vault.</span></span> 

## <span data-ttu-id="9071e-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9071e-110">EXAMPLES</span></span>

### <span data-ttu-id="9071e-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9071e-111">Example 1</span></span>
```powershell
PS C:\> $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24" -ServiceEndpoint Microsoft.KeyVault 
PS C:\> $virtualNetwork = New-AzureRmVirtualNetwork -Name myVNet -ResourceGroupName myRG -Location westus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
PS C:\> $myNetworkResId = (Get-AzureRmVirtualNetwork -Name myVNet -ResourceGroupName myRG).Subnets[0].Id
PS C:\> Update-AzureRmKeyVaultNetworkRuleSet -VaultName 'myVault' -ResourceGroupName myRG -Bypass AzureServices -IpAddressRange "10.0.1.0/24" -VirtualNetworkResourceId $myNetworkResId -PassThru

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

<span data-ttu-id="9071e-112">Эта команда обновляет набор правил сети в хранилище с именем "myVault" для указанного диапазона IP-адресов и виртуальной сети, позволяя пропускать сетевые правила для служб Azure.</span><span class="sxs-lookup"><span data-stu-id="9071e-112">This command updates the network ruleset on the vault named 'myVault' for the specified IP range and the virtual network, allowing bypassing of the network rule for Azure services.</span></span>

## <span data-ttu-id="9071e-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9071e-113">PARAMETERS</span></span>

### <span data-ttu-id="9071e-114">-Обход</span><span class="sxs-lookup"><span data-stu-id="9071e-114">-Bypass</span></span>
<span data-ttu-id="9071e-115">Указывает обход сетевого правила.</span><span class="sxs-lookup"><span data-stu-id="9071e-115">Specifies bypass of network rule.</span></span>

```yaml
Type: PSKeyVaultNetworkRuleBypassEnum
Parameter Sets: (All)
Aliases:
Accepted values: None, AzureServices

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9071e-116">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="9071e-116">-DefaultAction</span></span>
<span data-ttu-id="9071e-117">Задает действие по умолчанию для сетевого правила.</span><span class="sxs-lookup"><span data-stu-id="9071e-117">Specifies default action of network rule.</span></span>

```yaml
Type: PSKeyVaultNetworkRuleDefaultActionEnum
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9071e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9071e-118">-DefaultProfile</span></span>
<span data-ttu-id="9071e-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9071e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9071e-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9071e-120">-InputObject</span></span>
<span data-ttu-id="9071e-121">Объект KeyVault</span><span class="sxs-lookup"><span data-stu-id="9071e-121">KeyVault object</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9071e-122">-IpAddressRange</span><span class="sxs-lookup"><span data-stu-id="9071e-122">-IpAddressRange</span></span>
<span data-ttu-id="9071e-123">Указывает допустимый диапазон IP-адресов сети сетевого правила.</span><span class="sxs-lookup"><span data-stu-id="9071e-123">Specifies allowed network IP address range of network rule.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9071e-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9071e-124">-PassThru</span></span>
<span data-ttu-id="9071e-125">Этот командлет не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9071e-125">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="9071e-126">Если указан этот параметр, возвращается обновленный объект Key Vault.</span><span class="sxs-lookup"><span data-stu-id="9071e-126">If this switch is specified, it returns the updated key vault object.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9071e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9071e-127">-ResourceGroupName</span></span>
<span data-ttu-id="9071e-128">Указывает имя группы ресурсов, связанной с хранилищем ключей, для которого изменяется сетевое правило.</span><span class="sxs-lookup"><span data-stu-id="9071e-128">Specifies the name of the resource group associated with the key vault whose network rule is being modified.</span></span>

```yaml
Type: String
Parameter Sets: ByVaultName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9071e-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9071e-129">-ResourceId</span></span>
<span data-ttu-id="9071e-130">Идентификатор ресурса KeyVault</span><span class="sxs-lookup"><span data-stu-id="9071e-130">KeyVault Resource Id</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9071e-131">-VaultName</span><span class="sxs-lookup"><span data-stu-id="9071e-131">-VaultName</span></span>
<span data-ttu-id="9071e-132">Указывает имя хранилища ключей, сетевое правило которого изменяется.</span><span class="sxs-lookup"><span data-stu-id="9071e-132">Specifies the name of a key vault whose network rule is being modified.</span></span>

```yaml
Type: String
Parameter Sets: ByVaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9071e-133">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="9071e-133">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="9071e-134">Указывает допустимый идентификатор ресурса виртуальной сети для сетевого правила.</span><span class="sxs-lookup"><span data-stu-id="9071e-134">Specifies allowed virtual network resource identifier of network rule.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9071e-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9071e-135">-Confirm</span></span>
<span data-ttu-id="9071e-136">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9071e-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9071e-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9071e-137">-WhatIf</span></span>
<span data-ttu-id="9071e-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9071e-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9071e-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9071e-139">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9071e-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9071e-140">CommonParameters</span></span>
<span data-ttu-id="9071e-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9071e-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9071e-142">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9071e-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9071e-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9071e-143">INPUTS</span></span>

### <span data-ttu-id="9071e-144">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="9071e-144">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="9071e-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9071e-145">OUTPUTS</span></span>

### <span data-ttu-id="9071e-146">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="9071e-146">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="9071e-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="9071e-147">NOTES</span></span>

## <span data-ttu-id="9071e-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9071e-148">RELATED LINKS</span></span>

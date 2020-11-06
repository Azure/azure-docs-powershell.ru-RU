---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/add-azurermkeyvaultnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureRmKeyVaultNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureRmKeyVaultNetworkRule.md
ms.openlocfilehash: c99b621a39df1be595ceb873d85f5a3d848abc88
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560171"
---
# <span data-ttu-id="e8677-101">Add-AzureRmKeyVaultNetworkRule</span><span class="sxs-lookup"><span data-stu-id="e8677-101">Add-AzureRmKeyVaultNetworkRule</span></span>

## <span data-ttu-id="e8677-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e8677-102">SYNOPSIS</span></span>
<span data-ttu-id="e8677-103">Добавляет правило, чтобы ограничить доступ к хранилищу ключей на основе Интернет-адреса клиента.</span><span class="sxs-lookup"><span data-stu-id="e8677-103">Adds a rule meant to restrict access to a key vault based on the client's internet address.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e8677-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e8677-104">SYNTAX</span></span>

### <span data-ttu-id="e8677-105">ByVaultName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e8677-105">ByVaultName (Default)</span></span>
```
Add-AzureRmKeyVaultNetworkRule [-VaultName] <String> [[-ResourceGroupName] <String>]
 [-IpAddressRange <String[]>] [-VirtualNetworkResourceId <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8677-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="e8677-106">ByInputObject</span></span>
```
Add-AzureRmKeyVaultNetworkRule [-InputObject] <PSKeyVault> [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8677-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e8677-107">ByResourceId</span></span>
```
Add-AzureRmKeyVaultNetworkRule [-ResourceId] <String> [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8677-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e8677-108">DESCRIPTION</span></span>
<span data-ttu-id="e8677-109">Командлет **Add-AzureRmKeyVaultNetworkRule** предоставляет или ограничивает доступ к хранилищу ключей набору вызывающего абонента, которому назначены их IP-адреса, или виртуальную сеть, к которой они относятся.</span><span class="sxs-lookup"><span data-stu-id="e8677-109">The **Add-AzureRmKeyVaultNetworkRule** cmdlet grants or restricts access to a key vault to a set of caller designated by their IP addresses or the virtual network to which they belong.</span></span> <span data-ttu-id="e8677-110">Правило может ограничивать доступ других пользователей, приложений или групп безопасности, которым предоставлены разрешения с помощью политики доступа.</span><span class="sxs-lookup"><span data-stu-id="e8677-110">The rule has the potential to restrict access for other users, applications, or security groups which have been granted permissions via the access policy.</span></span>

## <span data-ttu-id="e8677-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e8677-111">EXAMPLES</span></span>

### <span data-ttu-id="e8677-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e8677-112">Example 1</span></span>
```powershell
PS C:\> $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24" -ServiceEndpoint Microsoft.KeyVault 
PS C:\> $virtualNetwork = New-AzureRmVirtualNetwork -Name myVNet -ResourceGroupName myRG -Location westus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
PS C:\> $myNetworkResId = (Get-AzureRmVirtualNetwork -Name myVNet -ResourceGroupName myRG).Subnets[0].Id
PS C:\> Add-AzureRmKeyVaultNetworkRule -VaultName myvault -IpAddressRange "10.0.1.0/24" -VirtualNetworkResourceId $myNetworkResId -PassThru

Vault Name                       : myvault
Resource Group Name              : myRG
Location                         : westus
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myRG/providers
                                   /Microsoft.KeyVault/vaults/myvault
Vault URI                        : https://myvault.vault.azure.net/
Tenant ID                        : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
SKU                              : Standard
Enabled For Deployment?          : True
Enabled For Template Deployment? : True
Enabled For Disk Encryption?     : False
Soft Delete Enabled?             : True
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
                                   setissuers, recover
                                   Permissions to (Key Vault Managed) Storage : delete, deletesas, get, getsas, list,
                                   listsas, regeneratekey, set, setsas, update


Network Rule Set                 :
                                   Default Action                             : Allow
                                   Bypass                                     : AzureServices
                                   IP Rules                                   : 10.0.1.0/24
                                   Virtual Network Rules                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-
                                   xxxxxxxxxxxxx/resourcegroups/myRG/providers/microsoft.network/virtualnetworks/myvn
                                   et/subnets/frontendsubnet

Tags                             :
```

<span data-ttu-id="e8677-113">Эта команда добавляет сетевое правило в указанное хранилище, разрешая доступ к указанному IP-адресу из виртуальной сети, определенной $myNetworkResId.</span><span class="sxs-lookup"><span data-stu-id="e8677-113">This command adds a network rule to the specified vault, allowing access to the specified IP address from the virtual network identified by $myNetworkResId.</span></span>

## <span data-ttu-id="e8677-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e8677-114">PARAMETERS</span></span>

### <span data-ttu-id="e8677-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8677-115">-DefaultProfile</span></span>
<span data-ttu-id="e8677-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e8677-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8677-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e8677-117">-InputObject</span></span>
<span data-ttu-id="e8677-118">Объект KeyVault</span><span class="sxs-lookup"><span data-stu-id="e8677-118">KeyVault object</span></span>

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

### <span data-ttu-id="e8677-119">-IpAddressRange</span><span class="sxs-lookup"><span data-stu-id="e8677-119">-IpAddressRange</span></span>
<span data-ttu-id="e8677-120">Указывает допустимый диапазон IP-адресов сети сетевого правила.</span><span class="sxs-lookup"><span data-stu-id="e8677-120">Specifies allowed network IP address range of network rule.</span></span>

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

### <span data-ttu-id="e8677-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e8677-121">-PassThru</span></span>
<span data-ttu-id="e8677-122">Этот командлет не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e8677-122">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="e8677-123">Если указан этот параметр, возвращается обновленный объект Key Vault.</span><span class="sxs-lookup"><span data-stu-id="e8677-123">If this switch is specified, it returns the updated key vault object.</span></span>

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

### <span data-ttu-id="e8677-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8677-124">-ResourceGroupName</span></span>
<span data-ttu-id="e8677-125">Указывает имя группы ресурсов, связанной с хранилищем ключей, для которого изменяется сетевое правило.</span><span class="sxs-lookup"><span data-stu-id="e8677-125">Specifies the name of the resource group associated with the key vault whose network rule is being modified.</span></span>

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

### <span data-ttu-id="e8677-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e8677-126">-ResourceId</span></span>
<span data-ttu-id="e8677-127">Идентификатор ресурса KeyVault</span><span class="sxs-lookup"><span data-stu-id="e8677-127">KeyVault Resource Id</span></span>

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

### <span data-ttu-id="e8677-128">-VaultName</span><span class="sxs-lookup"><span data-stu-id="e8677-128">-VaultName</span></span>
<span data-ttu-id="e8677-129">Указывает имя хранилища ключей, сетевое правило которого изменяется.</span><span class="sxs-lookup"><span data-stu-id="e8677-129">Specifies the name of a key vault whose network rule is being modified.</span></span>

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

### <span data-ttu-id="e8677-130">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="e8677-130">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="e8677-131">Указывает допустимый идентификатор ресурса виртуальной сети для сетевого правила.</span><span class="sxs-lookup"><span data-stu-id="e8677-131">Specifies allowed virtual network resource identifier of network rule.</span></span>

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

### <span data-ttu-id="e8677-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e8677-132">-Confirm</span></span>
<span data-ttu-id="e8677-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e8677-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8677-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8677-134">-WhatIf</span></span>
<span data-ttu-id="e8677-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e8677-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8677-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e8677-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8677-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8677-137">CommonParameters</span></span>
<span data-ttu-id="e8677-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e8677-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8677-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8677-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8677-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e8677-140">INPUTS</span></span>

### <span data-ttu-id="e8677-141">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="e8677-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="e8677-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e8677-142">OUTPUTS</span></span>

### <span data-ttu-id="e8677-143">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="e8677-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="e8677-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="e8677-144">NOTES</span></span>

## <span data-ttu-id="e8677-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e8677-145">RELATED LINKS</span></span>

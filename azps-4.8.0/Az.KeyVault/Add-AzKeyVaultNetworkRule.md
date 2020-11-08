---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultNetworkRule.md
ms.openlocfilehash: 7e9c904d6c03836b2d97ebead98f1675e2ec3cbf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078230"
---
# <span data-ttu-id="41722-101">Add-AzKeyVaultNetworkRule</span><span class="sxs-lookup"><span data-stu-id="41722-101">Add-AzKeyVaultNetworkRule</span></span>

## <span data-ttu-id="41722-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="41722-102">SYNOPSIS</span></span>
<span data-ttu-id="41722-103">Добавляет правило, чтобы ограничить доступ к хранилищу ключей на основе Интернет-адреса клиента.</span><span class="sxs-lookup"><span data-stu-id="41722-103">Adds a rule meant to restrict access to a key vault based on the client's internet address.</span></span>

## <span data-ttu-id="41722-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="41722-104">SYNTAX</span></span>

### <span data-ttu-id="41722-105">ByVaultName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="41722-105">ByVaultName (Default)</span></span>
```
Add-AzKeyVaultNetworkRule [-VaultName] <String> [[-ResourceGroupName] <String>] [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41722-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="41722-106">ByInputObject</span></span>
```
Add-AzKeyVaultNetworkRule [-InputObject] <PSKeyVault> [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41722-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="41722-107">ByResourceId</span></span>
```
Add-AzKeyVaultNetworkRule [-ResourceId] <String> [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41722-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="41722-108">DESCRIPTION</span></span>
<span data-ttu-id="41722-109">Командлет **Add-AzKeyVaultNetworkRule** предоставляет или ограничивает доступ к хранилищу ключей набору вызывающего абонента, которому назначены их IP-адреса, или виртуальную сеть, к которой они относятся.</span><span class="sxs-lookup"><span data-stu-id="41722-109">The **Add-AzKeyVaultNetworkRule** cmdlet grants or restricts access to a key vault to a set of caller designated by their IP addresses or the virtual network to which they belong.</span></span> <span data-ttu-id="41722-110">Правило может ограничивать доступ других пользователей, приложений или групп безопасности, которым предоставлены разрешения с помощью политики доступа.</span><span class="sxs-lookup"><span data-stu-id="41722-110">The rule has the potential to restrict access for other users, applications, or security groups which have been granted permissions via the access policy.</span></span>

<span data-ttu-id="41722-111">Обратите внимание на то, что любой диапазон IP- `10.0.0.0–10.255.255.255` адресов внутри (частный IP-адрес) не может использоваться для добавления сетевых правил.</span><span class="sxs-lookup"><span data-stu-id="41722-111">Please note that any IP range inside `10.0.0.0–10.255.255.255` (private IP addresses) cannot be used to add network rules.</span></span>

## <span data-ttu-id="41722-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="41722-112">EXAMPLES</span></span>

### <span data-ttu-id="41722-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="41722-113">Example 1</span></span>
```powershell
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24" -ServiceEndpoint Microsoft.KeyVault 
PS C:\> $virtualNetwork = New-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG -Location westus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
PS C:\> $myNetworkResId = (Get-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG).Subnets[0].Id
PS C:\> Add-AzKeyVaultNetworkRule -VaultName myvault -IpAddressRange "10.0.1.0/24" -VirtualNetworkResourceId $myNetworkResId -PassThru

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

<span data-ttu-id="41722-114">Эта команда добавляет сетевое правило в указанное хранилище, разрешая доступ к указанному IP-адресу из виртуальной сети, определенной $myNetworkResId.</span><span class="sxs-lookup"><span data-stu-id="41722-114">This command adds a network rule to the specified vault, allowing access to the specified IP address from the virtual network identified by $myNetworkResId.</span></span>

## <span data-ttu-id="41722-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="41722-115">PARAMETERS</span></span>

### <span data-ttu-id="41722-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41722-116">-DefaultProfile</span></span>
<span data-ttu-id="41722-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="41722-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41722-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="41722-118">-InputObject</span></span>
<span data-ttu-id="41722-119">Объект KeyVault</span><span class="sxs-lookup"><span data-stu-id="41722-119">KeyVault object</span></span>

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

### <span data-ttu-id="41722-120">-IpAddressRange</span><span class="sxs-lookup"><span data-stu-id="41722-120">-IpAddressRange</span></span>
<span data-ttu-id="41722-121">Указывает допустимый диапазон IP-адресов сети сетевого правила.</span><span class="sxs-lookup"><span data-stu-id="41722-121">Specifies allowed network IP address range of network rule.</span></span>

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

### <span data-ttu-id="41722-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="41722-122">-PassThru</span></span>
<span data-ttu-id="41722-123">Этот командлет не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="41722-123">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="41722-124">Если указан этот параметр, возвращается обновленный объект Key Vault.</span><span class="sxs-lookup"><span data-stu-id="41722-124">If this switch is specified, it returns the updated key vault object.</span></span>

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

### <span data-ttu-id="41722-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41722-125">-ResourceGroupName</span></span>
<span data-ttu-id="41722-126">Указывает имя группы ресурсов, связанной с хранилищем ключей, для которого изменяется сетевое правило.</span><span class="sxs-lookup"><span data-stu-id="41722-126">Specifies the name of the resource group associated with the key vault whose network rule is being modified.</span></span>

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

### <span data-ttu-id="41722-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="41722-127">-ResourceId</span></span>
<span data-ttu-id="41722-128">Идентификатор ресурса KeyVault</span><span class="sxs-lookup"><span data-stu-id="41722-128">KeyVault Resource Id</span></span>

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

### <span data-ttu-id="41722-129">-VaultName</span><span class="sxs-lookup"><span data-stu-id="41722-129">-VaultName</span></span>
<span data-ttu-id="41722-130">Указывает имя хранилища ключей, сетевое правило которого изменяется.</span><span class="sxs-lookup"><span data-stu-id="41722-130">Specifies the name of a key vault whose network rule is being modified.</span></span>

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

### <span data-ttu-id="41722-131">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="41722-131">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="41722-132">Указывает допустимый идентификатор ресурса виртуальной сети для сетевого правила.</span><span class="sxs-lookup"><span data-stu-id="41722-132">Specifies allowed virtual network resource identifier of network rule.</span></span>

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

### <span data-ttu-id="41722-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="41722-133">-Confirm</span></span>
<span data-ttu-id="41722-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="41722-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41722-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41722-135">-WhatIf</span></span>
<span data-ttu-id="41722-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="41722-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41722-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="41722-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41722-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41722-138">CommonParameters</span></span>
<span data-ttu-id="41722-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="41722-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41722-140">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="41722-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41722-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="41722-141">INPUTS</span></span>

### <span data-ttu-id="41722-142">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="41722-142">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="41722-143">System. String</span><span class="sxs-lookup"><span data-stu-id="41722-143">System.String</span></span>

## <span data-ttu-id="41722-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="41722-144">OUTPUTS</span></span>

### <span data-ttu-id="41722-145">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="41722-145">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="41722-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="41722-146">NOTES</span></span>

## <span data-ttu-id="41722-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="41722-147">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultNetworkRule.md
ms.openlocfilehash: d7b5f3a7a5a4c2f28724214fb026768979fa9028
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720633"
---
# <span data-ttu-id="52f29-101">Remove-AzKeyVaultNetworkRule</span><span class="sxs-lookup"><span data-stu-id="52f29-101">Remove-AzKeyVaultNetworkRule</span></span>

## <span data-ttu-id="52f29-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="52f29-102">SYNOPSIS</span></span>
<span data-ttu-id="52f29-103">Удаляет правило сети из хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="52f29-103">Removes a network rule from a key vault.</span></span>

## <span data-ttu-id="52f29-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="52f29-104">SYNTAX</span></span>

### <span data-ttu-id="52f29-105">ByVaultName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="52f29-105">ByVaultName (Default)</span></span>
```
Remove-AzKeyVaultNetworkRule [-VaultName] <String> [[-ResourceGroupName] <String>] [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52f29-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="52f29-106">ByInputObject</span></span>
```
Remove-AzKeyVaultNetworkRule [-InputObject] <PSKeyVault> [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52f29-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="52f29-107">ByResourceId</span></span>
```
Remove-AzKeyVaultNetworkRule [-ResourceId] <String> [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52f29-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="52f29-108">DESCRIPTION</span></span>
<span data-ttu-id="52f29-109">Удаляет правило сети из хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="52f29-109">Removes a network rule from a key vault.</span></span>

## <span data-ttu-id="52f29-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="52f29-110">EXAMPLES</span></span>

### <span data-ttu-id="52f29-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="52f29-111">Example 1</span></span>
```powershell
PS C:\> $myNetworkResId = (Get-AzVirtualNetwork -Name myVNetName -ResourceGroupName myRG).Subnets[0].Id
PS C:\> Remove-AzKeyVaultNetworkRule -VaultName myVault -IpAddressRange "10.0.0.1/26" -VirtualNetworkResourceId $myNetworkResId -PassThru

Vault Name                       : myVault
Resource Group Name              : myrg
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
                                   IP Rules                                   :
                                   Virtual Network Rules                      :

Tags                             :
```

<span data-ttu-id="52f29-112">Эта команда удаляет сетевое правило из указанного хранилища, при условии, что найдено правило, совпадающее с указанным IP-адресом и идентификатором ресурса виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="52f29-112">This command removes a network rule from the specified vault, provided a rule is found matching the specified IP address and the virtual network resource identifier.</span></span>

## <span data-ttu-id="52f29-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="52f29-113">PARAMETERS</span></span>

### <span data-ttu-id="52f29-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52f29-114">-DefaultProfile</span></span>
<span data-ttu-id="52f29-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="52f29-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52f29-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="52f29-116">-InputObject</span></span>
<span data-ttu-id="52f29-117">Объект KeyVault</span><span class="sxs-lookup"><span data-stu-id="52f29-117">KeyVault object</span></span>

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

### <span data-ttu-id="52f29-118">-IpAddressRange</span><span class="sxs-lookup"><span data-stu-id="52f29-118">-IpAddressRange</span></span>
<span data-ttu-id="52f29-119">Указывает допустимый диапазон IP-адресов сети сетевого правила.</span><span class="sxs-lookup"><span data-stu-id="52f29-119">Specifies allowed network IP address range of network rule.</span></span>

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

### <span data-ttu-id="52f29-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="52f29-120">-PassThru</span></span>
<span data-ttu-id="52f29-121">Этот командлет не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="52f29-121">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="52f29-122">Если указан этот параметр, возвращается обновленный объект Key Vault.</span><span class="sxs-lookup"><span data-stu-id="52f29-122">If this switch is specified, it returns the updated key vault object.</span></span>

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

### <span data-ttu-id="52f29-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52f29-123">-ResourceGroupName</span></span>
<span data-ttu-id="52f29-124">Указывает имя группы ресурсов, связанной с хранилищем ключей, для которого изменяется сетевое правило.</span><span class="sxs-lookup"><span data-stu-id="52f29-124">Specifies the name of the resource group associated with the key vault whose network rule is being modified.</span></span>

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

### <span data-ttu-id="52f29-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="52f29-125">-ResourceId</span></span>
<span data-ttu-id="52f29-126">Идентификатор ресурса KeyVault</span><span class="sxs-lookup"><span data-stu-id="52f29-126">KeyVault Resource Id</span></span>

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

### <span data-ttu-id="52f29-127">-VaultName</span><span class="sxs-lookup"><span data-stu-id="52f29-127">-VaultName</span></span>
<span data-ttu-id="52f29-128">Указывает имя хранилища ключей, сетевое правило которого изменяется.</span><span class="sxs-lookup"><span data-stu-id="52f29-128">Specifies the name of a key vault whose network rule is being modified.</span></span>

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

### <span data-ttu-id="52f29-129">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="52f29-129">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="52f29-130">Указывает допустимый идентификатор ресурса виртуальной сети для сетевого правила.</span><span class="sxs-lookup"><span data-stu-id="52f29-130">Specifies allowed virtual network resource identifier of network rule.</span></span>

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

### <span data-ttu-id="52f29-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="52f29-131">-Confirm</span></span>
<span data-ttu-id="52f29-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="52f29-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52f29-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52f29-133">-WhatIf</span></span>
<span data-ttu-id="52f29-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="52f29-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52f29-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="52f29-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52f29-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52f29-136">CommonParameters</span></span>
<span data-ttu-id="52f29-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="52f29-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52f29-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52f29-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52f29-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="52f29-139">INPUTS</span></span>

### <span data-ttu-id="52f29-140">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="52f29-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="52f29-141">System. String</span><span class="sxs-lookup"><span data-stu-id="52f29-141">System.String</span></span>

## <span data-ttu-id="52f29-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="52f29-142">OUTPUTS</span></span>

### <span data-ttu-id="52f29-143">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="52f29-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="52f29-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="52f29-144">NOTES</span></span>

## <span data-ttu-id="52f29-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="52f29-145">RELATED LINKS</span></span>

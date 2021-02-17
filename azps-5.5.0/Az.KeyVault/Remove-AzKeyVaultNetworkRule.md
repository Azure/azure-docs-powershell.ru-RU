---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultNetworkRule.md
ms.openlocfilehash: b1c0326be98efed91ce53c9cf04cdee6fce658f8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100234049"
---
# <span data-ttu-id="e2947-101">Remove-AzKeyVaultNetworkRule</span><span class="sxs-lookup"><span data-stu-id="e2947-101">Remove-AzKeyVaultNetworkRule</span></span>

## <span data-ttu-id="e2947-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2947-102">SYNOPSIS</span></span>
<span data-ttu-id="e2947-103">Удаляет правило сети из хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="e2947-103">Removes a network rule from a key vault.</span></span>

## <span data-ttu-id="e2947-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e2947-104">SYNTAX</span></span>

### <span data-ttu-id="e2947-105">ByVaultName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e2947-105">ByVaultName (Default)</span></span>
```
Remove-AzKeyVaultNetworkRule [-VaultName] <String> [[-ResourceGroupName] <String>] [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2947-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="e2947-106">ByInputObject</span></span>
```
Remove-AzKeyVaultNetworkRule [-InputObject] <PSKeyVault> [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2947-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e2947-107">ByResourceId</span></span>
```
Remove-AzKeyVaultNetworkRule [-ResourceId] <String> [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2947-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e2947-108">DESCRIPTION</span></span>
<span data-ttu-id="e2947-109">Удаляет правило сети из хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="e2947-109">Removes a network rule from a key vault.</span></span>

## <span data-ttu-id="e2947-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e2947-110">EXAMPLES</span></span>

### <span data-ttu-id="e2947-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e2947-111">Example 1</span></span>
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

<span data-ttu-id="e2947-112">Эта команда удаляет правило сети из указанного хранилища при условии, что найдено правило, совпадающий с указанным IP-адресом и идентификатором виртуального сетевого ресурса.</span><span class="sxs-lookup"><span data-stu-id="e2947-112">This command removes a network rule from the specified vault, provided a rule is found matching the specified IP address and the virtual network resource identifier.</span></span>

## <span data-ttu-id="e2947-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e2947-113">PARAMETERS</span></span>

### <span data-ttu-id="e2947-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2947-114">-DefaultProfile</span></span>
<span data-ttu-id="e2947-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e2947-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2947-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e2947-116">-InputObject</span></span>
<span data-ttu-id="e2947-117">Объект KeyVault</span><span class="sxs-lookup"><span data-stu-id="e2947-117">KeyVault object</span></span>

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

### <span data-ttu-id="e2947-118">-IpAddressRange</span><span class="sxs-lookup"><span data-stu-id="e2947-118">-IpAddressRange</span></span>
<span data-ttu-id="e2947-119">Диапазон разрешенных IP-адресов сети для правила сети.</span><span class="sxs-lookup"><span data-stu-id="e2947-119">Specifies allowed network IP address range of network rule.</span></span>

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

### <span data-ttu-id="e2947-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e2947-120">-PassThru</span></span>
<span data-ttu-id="e2947-121">Этот cmdlet не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e2947-121">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="e2947-122">Если этот ключ задан, он возвращает обновленный объект key vault.</span><span class="sxs-lookup"><span data-stu-id="e2947-122">If this switch is specified, it returns the updated key vault object.</span></span>

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

### <span data-ttu-id="e2947-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2947-123">-ResourceGroupName</span></span>
<span data-ttu-id="e2947-124">Указывает имя группы ресурсов, связанной с хранилищем ключа, сетевое правило которого было изменено.</span><span class="sxs-lookup"><span data-stu-id="e2947-124">Specifies the name of the resource group associated with the key vault whose network rule is being modified.</span></span>

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

### <span data-ttu-id="e2947-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e2947-125">-ResourceId</span></span>
<span data-ttu-id="e2947-126">KeyVault Resource Id</span><span class="sxs-lookup"><span data-stu-id="e2947-126">KeyVault Resource Id</span></span>

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

### <span data-ttu-id="e2947-127">-VaultName</span><span class="sxs-lookup"><span data-stu-id="e2947-127">-VaultName</span></span>
<span data-ttu-id="e2947-128">Указывает имя хранилища ключа, сетевое правило которого будет изменено.</span><span class="sxs-lookup"><span data-stu-id="e2947-128">Specifies the name of a key vault whose network rule is being modified.</span></span>

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

### <span data-ttu-id="e2947-129">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="e2947-129">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="e2947-130">Определяет допустимый идентификатор виртуального сетевого ресурса для правила сети.</span><span class="sxs-lookup"><span data-stu-id="e2947-130">Specifies allowed virtual network resource identifier of network rule.</span></span>

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

### <span data-ttu-id="e2947-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e2947-131">-Confirm</span></span>
<span data-ttu-id="e2947-132">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e2947-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2947-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2947-133">-WhatIf</span></span>
<span data-ttu-id="e2947-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e2947-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2947-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="e2947-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2947-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2947-136">CommonParameters</span></span>
<span data-ttu-id="e2947-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2947-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2947-138">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e2947-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2947-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e2947-139">INPUTS</span></span>

### <span data-ttu-id="e2947-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="e2947-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="e2947-141">System.String</span><span class="sxs-lookup"><span data-stu-id="e2947-141">System.String</span></span>

## <span data-ttu-id="e2947-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e2947-142">OUTPUTS</span></span>

### <span data-ttu-id="e2947-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="e2947-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="e2947-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e2947-144">NOTES</span></span>

## <span data-ttu-id="e2947-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e2947-145">RELATED LINKS</span></span>

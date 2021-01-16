---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/undo-azkeyvaultremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultRemoval.md
ms.openlocfilehash: 98a3a023564c2c61f1398856e8a089276aeae7bc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98394471"
---
# <span data-ttu-id="92df6-101">Undo-AzKeyVaultRemoval</span><span class="sxs-lookup"><span data-stu-id="92df6-101">Undo-AzKeyVaultRemoval</span></span>

## <span data-ttu-id="92df6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92df6-102">SYNOPSIS</span></span>
<span data-ttu-id="92df6-103">Восстановление удаленного сейфа ключа в активном состоянии.</span><span class="sxs-lookup"><span data-stu-id="92df6-103">Recovers a deleted key vault into an active state.</span></span>

## <span data-ttu-id="92df6-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="92df6-104">SYNTAX</span></span>

### <span data-ttu-id="92df6-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="92df6-105">Default (Default)</span></span>
```
Undo-AzKeyVaultRemoval [-VaultName] <String> [-ResourceGroupName] <String> [-Location] <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92df6-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="92df6-106">InputObject</span></span>
```
Undo-AzKeyVaultRemoval [-InputObject] <PSDeletedKeyVault> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="92df6-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="92df6-107">DESCRIPTION</span></span>
<span data-ttu-id="92df6-108">Для восстановления ранее удаленного сейфа ключа будет восстановлен **cmdlet Undo-AzKeyVaultRemoval.**</span><span class="sxs-lookup"><span data-stu-id="92df6-108">The **Undo-AzKeyVaultRemoval** cmdlet will recover a previously deleted key vault.</span></span> <span data-ttu-id="92df6-109">Восстановленный сейф будет активен после восстановления</span><span class="sxs-lookup"><span data-stu-id="92df6-109">The recovered vault will be active after recovery</span></span>

## <span data-ttu-id="92df6-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="92df6-110">EXAMPLES</span></span>

### <span data-ttu-id="92df6-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="92df6-111">Example 1</span></span>
```powershell
PS C:\> Undo-AzKeyVaultRemoval -VaultName 'MyKeyVault' -ResourceGroupName 'MyResourceGroup' -Location 'eastus2' -Tag @{"x"= "y"}

Vault Name                       : MyKeyVault
Resource Group Name              : MyResourceGroup
Location                         : eastus2
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers
                                   /Microsoft.KeyVault/vaults/mykeyvault
Vault URI                        : https://mykeyvault.vault.azure.net/
Tenant ID                        : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
SKU                              : Standard
Enabled For Deployment?          : True
Enabled For Template Deployment? : True
Enabled For Disk Encryption?     : True
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

Tags                             :
                                   Name  Value
                                   ====  =====
                                   x     y
```

<span data-ttu-id="92df6-112">Эта команда восстановит ключевое хранилище MyKeyVault, ранее удаленное из области eastus2 и группы ресурсов MyResourceGroup, в активное и можное состояние.</span><span class="sxs-lookup"><span data-stu-id="92df6-112">This command will recover the key vault 'MyKeyVault' that was previously deleted from eastus2 region and 'MyResourceGroup' resource group, into an active and usable state.</span></span> <span data-ttu-id="92df6-113">Теги также будут заменяться новыми.</span><span class="sxs-lookup"><span data-stu-id="92df6-113">It also replaces the tags with new tag.</span></span>

## <span data-ttu-id="92df6-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="92df6-114">PARAMETERS</span></span>

### <span data-ttu-id="92df6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92df6-115">-DefaultProfile</span></span>
<span data-ttu-id="92df6-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="92df6-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="92df6-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="92df6-117">-InputObject</span></span>
<span data-ttu-id="92df6-118">Удаленный объект сейфа</span><span class="sxs-lookup"><span data-stu-id="92df6-118">Deleted vault object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="92df6-119">-Location</span><span class="sxs-lookup"><span data-stu-id="92df6-119">-Location</span></span>
<span data-ttu-id="92df6-120">Определяет удаленный сейф в исходном регионе Azure.</span><span class="sxs-lookup"><span data-stu-id="92df6-120">Specifies the deleted vault original Azure region.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92df6-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92df6-121">-ResourceGroupName</span></span>
<span data-ttu-id="92df6-122">Указывает имя существующей группы ресурсов, в которой нужно создать хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="92df6-122">Specifies the name of an existing resource group in which to create the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92df6-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="92df6-123">-Tag</span></span>
<span data-ttu-id="92df6-124">Пары значений ключа в виде hash table.</span><span class="sxs-lookup"><span data-stu-id="92df6-124">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="92df6-125">Например: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="92df6-125">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="92df6-126">-VaultName</span><span class="sxs-lookup"><span data-stu-id="92df6-126">-VaultName</span></span>
<span data-ttu-id="92df6-127">Имя сейфа.</span><span class="sxs-lookup"><span data-stu-id="92df6-127">Vault name.</span></span>
<span data-ttu-id="92df6-128">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span><span class="sxs-lookup"><span data-stu-id="92df6-128">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92df6-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="92df6-129">-Confirm</span></span>
<span data-ttu-id="92df6-130">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="92df6-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92df6-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92df6-131">-WhatIf</span></span>
<span data-ttu-id="92df6-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="92df6-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="92df6-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="92df6-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92df6-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92df6-134">CommonParameters</span></span>
<span data-ttu-id="92df6-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92df6-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92df6-136">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="92df6-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92df6-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="92df6-137">INPUTS</span></span>

### <span data-ttu-id="92df6-138">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault</span><span class="sxs-lookup"><span data-stu-id="92df6-138">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault</span></span>

## <span data-ttu-id="92df6-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="92df6-139">OUTPUTS</span></span>

### <span data-ttu-id="92df6-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="92df6-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="92df6-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="92df6-141">NOTES</span></span>

## <span data-ttu-id="92df6-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="92df6-142">RELATED LINKS</span></span>

[<span data-ttu-id="92df6-143">Remove-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="92df6-143">Remove-AzKeyVault</span></span>](./Remove-AzKeyVault.md)

[<span data-ttu-id="92df6-144">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="92df6-144">New-AzKeyVault</span></span>](./New-AzKeyVault.md)

[<span data-ttu-id="92df6-145">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="92df6-145">Get-AzKeyVault</span></span>](./Get-AzKeyVault.md)
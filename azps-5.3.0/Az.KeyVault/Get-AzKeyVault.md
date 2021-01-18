---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: A7C287C4-E9FD-407A-91BD-EFA17C33FC8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVault.md
ms.openlocfilehash: 37ed0c0cb29e69aa2e8018bb193fa4c82b0c3bcb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504724"
---
# <span data-ttu-id="b6673-101">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="b6673-101">Get-AzKeyVault</span></span>

## <span data-ttu-id="b6673-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6673-102">SYNOPSIS</span></span>
<span data-ttu-id="b6673-103">Получает основные сейфы.</span><span class="sxs-lookup"><span data-stu-id="b6673-103">Gets key vaults.</span></span>

## <span data-ttu-id="b6673-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b6673-104">SYNTAX</span></span>

### <span data-ttu-id="b6673-105">GetVaultByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b6673-105">GetVaultByName (Default)</span></span>
```
Get-AzKeyVault [[-VaultName] <String>] [[-ResourceGroupName] <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b6673-106">ByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="b6673-106">ByDeletedVault</span></span>
```
Get-AzKeyVault [-VaultName] <String> [-Location] <String> [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b6673-107">ListAllDeletedVaultsInSubscription</span><span class="sxs-lookup"><span data-stu-id="b6673-107">ListAllDeletedVaultsInSubscription</span></span>
```
Get-AzKeyVault [-InRemovedState] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b6673-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b6673-108">DESCRIPTION</span></span>
<span data-ttu-id="b6673-109">Для получения сведений о ключевых хранилищах в подписке можно получить сведения о **cmdlet Get-AzKeyVault.**</span><span class="sxs-lookup"><span data-stu-id="b6673-109">The **Get-AzKeyVault** cmdlet gets information about the key vaults in a subscription.</span></span> <span data-ttu-id="b6673-110">Вы можете просмотреть все экземпляры ключевых хранилища в подписке или отфильтровать результаты по группе ресурсов или определенному сейфу ключа.</span><span class="sxs-lookup"><span data-stu-id="b6673-110">You can view all key vaults instances in a subscription, or filter your results by a resource group or a particular key vault.</span></span>
<span data-ttu-id="b6673-111">Обратите внимание на то, что хотя при этом не требуется указывать группу ресурсов, при получаете только одно ключевое хранилище, это следует сделать для улучшения производительности.</span><span class="sxs-lookup"><span data-stu-id="b6673-111">Note that although specifying the resource group is optional for this cmdlet when you get a single key vault, you should do so for better performance.</span></span>

## <span data-ttu-id="b6673-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b6673-112">EXAMPLES</span></span>

### <span data-ttu-id="b6673-113">Пример 1. Получить все основные хранилища в текущей подписке</span><span class="sxs-lookup"><span data-stu-id="b6673-113">Example 1: Get all key vaults in your current subscription</span></span>
```powershell
PS C:\> Get-AzKeyVault

Vault Name          : myvault1
Resource Group Name : myrg
Location            : westus
Resource ID         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.Ke
                      yVault/vaults/myvault1
Tags                :


Vault Name          : myvault2
Resource Group Name : myrg1
Location            : westus
Resource ID         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg1/providers/Microsoft.Ke
                      yVault/vaults/myvault2
Tags                :

Vault Name          : myvault3
Resource Group Name : myrg1
Location            : westus
Resource ID         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg1/providers/Microsoft.Ke
                      yVault/vaults/myvault3
Tags                :
```

<span data-ttu-id="b6673-114">Эта команда получает все основные хранилища в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="b6673-114">This command gets all the key vaults in your current subscription.</span></span>

### <span data-ttu-id="b6673-115">Пример 2. Получить определенное хранилище ключей</span><span class="sxs-lookup"><span data-stu-id="b6673-115">Example 2: Get a specific key vault</span></span>
```powershell
PS C:\> Get-AzKeyVault -VaultName 'myvault'

Vault Name                       : myvault
Resource Group Name              : myrg
Location                         : westus
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers
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

Tags                             :
```

<span data-ttu-id="b6673-116">Эта команда получает ключ хранилища myvault в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="b6673-116">This command gets the key vault named myvault in your current subscription.</span></span>

### <span data-ttu-id="b6673-117">Пример 3. Получить основные хранилища в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="b6673-117">Example 3: Get key vaults in a resource group</span></span>
```powershell
PS C:\> Get-AzKeyVault -ResourceGroupName 'myrg1'

Vault Name          : myvault2
Resource Group Name : myrg1
Location            : westus
Resource ID         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg1/providers/Microsoft.Ke
                      yVault/vaults/myvault2
Tags                :

Vault Name          : myvault3
Resource Group Name : myrg1
Location            : westus
Resource ID         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg1/providers/Microsoft.Ke
                      yVault/vaults/myvault3
Tags                :
```

<span data-ttu-id="b6673-118">Эта команда получает все основные хранилища в группе ресурсов ContosoPayRollResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="b6673-118">This command gets all the key vaults in the resource group named ContosoPayRollResourceGroup.</span></span>

### <span data-ttu-id="b6673-119">Пример 4. Все удаленные хранилища ключей в текущей подписке</span><span class="sxs-lookup"><span data-stu-id="b6673-119">Example 4: Get all deleted key vaults in your current subscription</span></span>
```powershell
PS C:\> Get-AzKeyVault -InRemovedState

Vault Name           : myvault4
Location             : westus
Id                   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/providers/Microsoft.KeyVault/locations/westu
                       s/deletedVaults/myvault4
Resource ID          : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.K
                       eyVault/vaults/myvault4
Deletion Date        : 5/24/2018 9:33:24 PM
Scheduled Purge Date : 8/22/2018 9:33:24 PM
Tags                 :
```

<span data-ttu-id="b6673-120">Эта команда получает все удаленные хранилища ключей в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="b6673-120">This command gets all the deleted key vaults in your current subscription.</span></span>

### <span data-ttu-id="b6673-121">Пример 5. Получить удаленное хранилище ключей</span><span class="sxs-lookup"><span data-stu-id="b6673-121">Example 5: Get a deleted key vault</span></span>
```powershell
PS C:\> Get-AzKeyVault -VaultName 'myvault4'  -Location 'westus' -InRemovedState

Vault Name           : myvault4
Location             : westus
Id                   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/providers/Microsoft.KeyVault/locations/westu
                       s/deletedVaults/myvault4
Resource ID          : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.K
                       eyVault/vaults/myvault4
Deletion Date        : 5/24/2018 9:33:24 PM
Scheduled Purge Date : 8/22/2018 9:33:24 PM
Tags                 :
```

<span data-ttu-id="b6673-122">Эта команда получает данные удаленного ключа с именем myvault4 в текущей подписке и на западном регионе.</span><span class="sxs-lookup"><span data-stu-id="b6673-122">This command gets the deleted key vault information named myvault4 in your current subscription and in westus region.</span></span>

### <span data-ttu-id="b6673-123">Пример 6. Использование фильтрации для получения ключевых сейфов</span><span class="sxs-lookup"><span data-stu-id="b6673-123">Example 6: Get key vaults using filtering</span></span>
```powershell
PS C:\> Get-AzKeyVault -VaultName 'myvault*'

Vault Name          : myvault2
Resource Group Name : myrg1
Location            : westus
Resource ID         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg1/providers/Microsoft.Ke
                      yVault/vaults/myvault2
Tags                :

Vault Name          : myvault3
Resource Group Name : myrg1
Location            : westus
Resource ID         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg1/providers/Microsoft.Ke
                      yVault/vaults/myvault3
Tags                :
```

<span data-ttu-id="b6673-124">Эта команда получает все основные хранилища в подписке, которые начинаются с myvault.</span><span class="sxs-lookup"><span data-stu-id="b6673-124">This command gets all the key vaults in the subscription that start with "myvault".</span></span>

## <span data-ttu-id="b6673-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b6673-125">PARAMETERS</span></span>

### <span data-ttu-id="b6673-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6673-126">-DefaultProfile</span></span>
<span data-ttu-id="b6673-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="b6673-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b6673-128">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="b6673-128">-InRemovedState</span></span>
<span data-ttu-id="b6673-129">Указывает, следует ли показывать ранее удаленные хранилища в выходных данных.</span><span class="sxs-lookup"><span data-stu-id="b6673-129">Specifies whether to show the previously deleted vaults in the output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByDeletedVault, ListAllDeletedVaultsInSubscription
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6673-130">-Location</span><span class="sxs-lookup"><span data-stu-id="b6673-130">-Location</span></span>
<span data-ttu-id="b6673-131">Расположение удаленного сейфа.</span><span class="sxs-lookup"><span data-stu-id="b6673-131">The location of the deleted vault.</span></span>

```yaml
Type: System.String
Parameter Sets: ByDeletedVault
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6673-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6673-132">-ResourceGroupName</span></span>
<span data-ttu-id="b6673-133">Указывает имя группы ресурсов, связанной с запрашиваемой key vault или key vaults.</span><span class="sxs-lookup"><span data-stu-id="b6673-133">Specifies the name of the resource group associated with the key vault or key vaults being queried.</span></span>

```yaml
Type: System.String
Parameter Sets: GetVaultByName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="b6673-134">-Tag</span><span class="sxs-lookup"><span data-stu-id="b6673-134">-Tag</span></span>
<span data-ttu-id="b6673-135">Пары значений ключа в виде hash table.</span><span class="sxs-lookup"><span data-stu-id="b6673-135">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="b6673-136">Например: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="b6673-136">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: GetVaultByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6673-137">-VaultName</span><span class="sxs-lookup"><span data-stu-id="b6673-137">-VaultName</span></span>
<span data-ttu-id="b6673-138">Указывает имя сейфа ключа.</span><span class="sxs-lookup"><span data-stu-id="b6673-138">Specifies the name of the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: GetVaultByName
Aliases: Name

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: ByDeletedVault
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="b6673-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6673-139">CommonParameters</span></span>
<span data-ttu-id="b6673-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6673-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6673-141">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b6673-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6673-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b6673-142">INPUTS</span></span>

### <span data-ttu-id="b6673-143">System.String</span><span class="sxs-lookup"><span data-stu-id="b6673-143">System.String</span></span>

### <span data-ttu-id="b6673-144">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="b6673-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="b6673-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b6673-145">OUTPUTS</span></span>

### <span data-ttu-id="b6673-146">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="b6673-146">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="b6673-147">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span><span class="sxs-lookup"><span data-stu-id="b6673-147">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

### <span data-ttu-id="b6673-148">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault</span><span class="sxs-lookup"><span data-stu-id="b6673-148">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault</span></span>

## <span data-ttu-id="b6673-149">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b6673-149">NOTES</span></span>

## <span data-ttu-id="b6673-150">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b6673-150">RELATED LINKS</span></span>

[<span data-ttu-id="b6673-151">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="b6673-151">New-AzKeyVault</span></span>](./New-AzKeyVault.md)

[<span data-ttu-id="b6673-152">Remove-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="b6673-152">Remove-AzKeyVault</span></span>](./Remove-AzKeyVault.md)

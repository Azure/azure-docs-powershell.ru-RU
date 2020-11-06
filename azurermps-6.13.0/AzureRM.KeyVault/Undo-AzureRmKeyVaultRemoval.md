---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/undo-azurermkeyvaultremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureRmKeyVaultRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureRmKeyVaultRemoval.md
ms.openlocfilehash: af6ed0e4db688cdc9ad6da598c0bc240e9b3c958
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564380"
---
# <span data-ttu-id="75660-101">Undo-AzureRmKeyVaultRemoval</span><span class="sxs-lookup"><span data-stu-id="75660-101">Undo-AzureRmKeyVaultRemoval</span></span>

## <span data-ttu-id="75660-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="75660-102">SYNOPSIS</span></span>
<span data-ttu-id="75660-103">Восстановление удаленного хранилища ключей в активном состоянии.</span><span class="sxs-lookup"><span data-stu-id="75660-103">Recovers a deleted key vault into an active state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="75660-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="75660-104">SYNTAX</span></span>

### <span data-ttu-id="75660-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="75660-105">Default (Default)</span></span>
```
Undo-AzureRmKeyVaultRemoval [-VaultName] <String> [-ResourceGroupName] <String> [-Location] <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75660-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="75660-106">InputObject</span></span>
```
Undo-AzureRmKeyVaultRemoval [-InputObject] <PSDeletedKeyVault> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75660-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="75660-107">DESCRIPTION</span></span>
<span data-ttu-id="75660-108">Командлет **Undo-AzureRmKeyVaultRemoval** восстановит ранее удаленное хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="75660-108">The **Undo-AzureRmKeyVaultRemoval** cmdlet will recover a previously deleted key vault.</span></span> <span data-ttu-id="75660-109">Восстановленное хранилище станет активным после восстановления</span><span class="sxs-lookup"><span data-stu-id="75660-109">The recovered vault will be active after recovery</span></span>

## <span data-ttu-id="75660-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="75660-110">EXAMPLES</span></span>

### <span data-ttu-id="75660-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="75660-111">Example 1</span></span>
```powershell
PS C:\> Undo-AzureRmKeyVaultRemoval -VaultName 'MyKeyVault' -ResourceGroupName 'MyResourceGroup' -Location 'eastus2' -Tag @{"x"= "y"}

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

<span data-ttu-id="75660-112">Эта команда восстанавливает активное и пригодное состояние для хранилища ключей "MyKeyVault", который ранее был удален из группы ресурсов eastus2 Region и "MyResourceGroup".</span><span class="sxs-lookup"><span data-stu-id="75660-112">This command will recover the key vault 'MyKeyVault' that was previously deleted from eastus2 region and 'MyResourceGroup' resource group, into an active and usable state.</span></span> <span data-ttu-id="75660-113">Он также заменяет Теги на новый тег.</span><span class="sxs-lookup"><span data-stu-id="75660-113">It also replaces the tags with new tag.</span></span>

## <span data-ttu-id="75660-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="75660-114">PARAMETERS</span></span>

### <span data-ttu-id="75660-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75660-115">-DefaultProfile</span></span>
<span data-ttu-id="75660-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="75660-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75660-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="75660-117">-InputObject</span></span>
<span data-ttu-id="75660-118">Удален объект хранилища</span><span class="sxs-lookup"><span data-stu-id="75660-118">Deleted vault object</span></span>

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

### <span data-ttu-id="75660-119">-Location</span><span class="sxs-lookup"><span data-stu-id="75660-119">-Location</span></span>
<span data-ttu-id="75660-120">Указывает исходный регион для удаленного хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="75660-120">Specifies the deleted vault original Azure region.</span></span>

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

### <span data-ttu-id="75660-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75660-121">-ResourceGroupName</span></span>
<span data-ttu-id="75660-122">Указывает имя существующей группы ресурсов, в которой нужно создать хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="75660-122">Specifies the name of an existing resource group in which to create the key vault.</span></span>

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

### <span data-ttu-id="75660-123">-Тег</span><span class="sxs-lookup"><span data-stu-id="75660-123">-Tag</span></span>
<span data-ttu-id="75660-124">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="75660-124">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="75660-125">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="75660-125">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="75660-126">-VaultName</span><span class="sxs-lookup"><span data-stu-id="75660-126">-VaultName</span></span>
<span data-ttu-id="75660-127">Имя хранилища.</span><span class="sxs-lookup"><span data-stu-id="75660-127">Vault name.</span></span>
<span data-ttu-id="75660-128">Командлет создает полное доменное имя хранилища на основе имени и выбранной в данный момент среды.</span><span class="sxs-lookup"><span data-stu-id="75660-128">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="75660-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="75660-129">-Confirm</span></span>
<span data-ttu-id="75660-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="75660-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75660-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75660-131">-WhatIf</span></span>
<span data-ttu-id="75660-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="75660-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="75660-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="75660-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75660-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75660-134">CommonParameters</span></span>
<span data-ttu-id="75660-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="75660-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75660-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75660-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75660-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="75660-137">INPUTS</span></span>

### <span data-ttu-id="75660-138">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault</span><span class="sxs-lookup"><span data-stu-id="75660-138">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault</span></span>
<span data-ttu-id="75660-139">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="75660-139">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="75660-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="75660-140">OUTPUTS</span></span>

### <span data-ttu-id="75660-141">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="75660-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="75660-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="75660-142">NOTES</span></span>

## <span data-ttu-id="75660-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="75660-143">RELATED LINKS</span></span>

[<span data-ttu-id="75660-144">Remove-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="75660-144">Remove-AzureRmKeyVault</span></span>](./Remove-AzureRmKeyVault.md)

[<span data-ttu-id="75660-145">New-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="75660-145">New-AzureRmKeyVault</span></span>](./New-AzureRmKeyVault.md)

[<span data-ttu-id="75660-146">Get-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="75660-146">Get-AzureRmKeyVault</span></span>](./Get-AzureRmKeyVault.md)

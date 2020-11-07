---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/undo-azkeyvaultremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultRemoval.md
ms.openlocfilehash: 77d8faf49e2ff1c1431986f77d05f5683cfa8eef
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93900090"
---
# <span data-ttu-id="8030f-101">Undo-AzKeyVaultRemoval</span><span class="sxs-lookup"><span data-stu-id="8030f-101">Undo-AzKeyVaultRemoval</span></span>

## <span data-ttu-id="8030f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8030f-102">SYNOPSIS</span></span>
<span data-ttu-id="8030f-103">Восстановление удаленного хранилища ключей в активном состоянии.</span><span class="sxs-lookup"><span data-stu-id="8030f-103">Recovers a deleted key vault into an active state.</span></span>

## <span data-ttu-id="8030f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8030f-104">SYNTAX</span></span>

### <span data-ttu-id="8030f-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8030f-105">Default (Default)</span></span>
```
Undo-AzKeyVaultRemoval [-VaultName] <String> [-ResourceGroupName] <String> [-Location] <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8030f-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="8030f-106">InputObject</span></span>
```
Undo-AzKeyVaultRemoval [-InputObject] <PSDeletedKeyVault> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8030f-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8030f-107">DESCRIPTION</span></span>
<span data-ttu-id="8030f-108">Командлет **Undo-AzKeyVaultRemoval** восстановит ранее удаленное хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="8030f-108">The **Undo-AzKeyVaultRemoval** cmdlet will recover a previously deleted key vault.</span></span> <span data-ttu-id="8030f-109">Восстановленное хранилище станет активным после восстановления</span><span class="sxs-lookup"><span data-stu-id="8030f-109">The recovered vault will be active after recovery</span></span>

## <span data-ttu-id="8030f-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8030f-110">EXAMPLES</span></span>

### <span data-ttu-id="8030f-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8030f-111">Example 1</span></span>
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

<span data-ttu-id="8030f-112">Эта команда восстанавливает активное и пригодное состояние для хранилища ключей "MyKeyVault", который ранее был удален из группы ресурсов eastus2 Region и "MyResourceGroup".</span><span class="sxs-lookup"><span data-stu-id="8030f-112">This command will recover the key vault 'MyKeyVault' that was previously deleted from eastus2 region and 'MyResourceGroup' resource group, into an active and usable state.</span></span> <span data-ttu-id="8030f-113">Он также заменяет Теги на новый тег.</span><span class="sxs-lookup"><span data-stu-id="8030f-113">It also replaces the tags with new tag.</span></span>

## <span data-ttu-id="8030f-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8030f-114">PARAMETERS</span></span>

### <span data-ttu-id="8030f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8030f-115">-DefaultProfile</span></span>
<span data-ttu-id="8030f-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="8030f-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8030f-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8030f-117">-InputObject</span></span>
<span data-ttu-id="8030f-118">Удален объект хранилища</span><span class="sxs-lookup"><span data-stu-id="8030f-118">Deleted vault object</span></span>

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

### <span data-ttu-id="8030f-119">-Location</span><span class="sxs-lookup"><span data-stu-id="8030f-119">-Location</span></span>
<span data-ttu-id="8030f-120">Указывает исходный регион для удаленного хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="8030f-120">Specifies the deleted vault original Azure region.</span></span>

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

### <span data-ttu-id="8030f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8030f-121">-ResourceGroupName</span></span>
<span data-ttu-id="8030f-122">Указывает имя существующей группы ресурсов, в которой нужно создать хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="8030f-122">Specifies the name of an existing resource group in which to create the key vault.</span></span>

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

### <span data-ttu-id="8030f-123">-Тег</span><span class="sxs-lookup"><span data-stu-id="8030f-123">-Tag</span></span>
<span data-ttu-id="8030f-124">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="8030f-124">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="8030f-125">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="8030f-125">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="8030f-126">-VaultName</span><span class="sxs-lookup"><span data-stu-id="8030f-126">-VaultName</span></span>
<span data-ttu-id="8030f-127">Имя хранилища.</span><span class="sxs-lookup"><span data-stu-id="8030f-127">Vault name.</span></span>
<span data-ttu-id="8030f-128">Командлет создает полное доменное имя хранилища на основе имени и выбранной в данный момент среды.</span><span class="sxs-lookup"><span data-stu-id="8030f-128">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="8030f-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8030f-129">-Confirm</span></span>
<span data-ttu-id="8030f-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8030f-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8030f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8030f-131">-WhatIf</span></span>
<span data-ttu-id="8030f-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8030f-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8030f-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8030f-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8030f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8030f-134">CommonParameters</span></span>
<span data-ttu-id="8030f-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8030f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8030f-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8030f-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8030f-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8030f-137">INPUTS</span></span>

### <span data-ttu-id="8030f-138">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault</span><span class="sxs-lookup"><span data-stu-id="8030f-138">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault</span></span>

## <span data-ttu-id="8030f-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8030f-139">OUTPUTS</span></span>

### <span data-ttu-id="8030f-140">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="8030f-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="8030f-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="8030f-141">NOTES</span></span>

## <span data-ttu-id="8030f-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8030f-142">RELATED LINKS</span></span>

[<span data-ttu-id="8030f-143">Remove-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="8030f-143">Remove-AzKeyVault</span></span>](./Remove-AzKeyVault.md)

[<span data-ttu-id="8030f-144">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="8030f-144">New-AzKeyVault</span></span>](./New-AzKeyVault.md)

[<span data-ttu-id="8030f-145">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="8030f-145">Get-AzKeyVault</span></span>](./Get-AzKeyVault.md)

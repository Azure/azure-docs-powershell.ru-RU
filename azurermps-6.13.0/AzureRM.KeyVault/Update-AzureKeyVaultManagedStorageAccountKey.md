---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/update-azurekeyvaultmanagedstorageaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Update-AzureKeyVaultManagedStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Update-AzureKeyVaultManagedStorageAccountKey.md
ms.openlocfilehash: 2e096b04830d50840d6298e7aa8085b0090a347e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567745"
---
# <span data-ttu-id="7124e-101">Update-AzureKeyVaultManagedStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="7124e-101">Update-AzureKeyVaultManagedStorageAccountKey</span></span>

## <span data-ttu-id="7124e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7124e-102">SYNOPSIS</span></span>
<span data-ttu-id="7124e-103">Повторное создание указанного ключа учетной записи хранения для хранилища ключей из управляемого хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="7124e-103">Regenerates the specified key of Key Vault managed Azure Storage Account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7124e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7124e-104">SYNTAX</span></span>

### <span data-ttu-id="7124e-105">ByDefinitionName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7124e-105">ByDefinitionName (Default)</span></span>
```
Update-AzureKeyVaultManagedStorageAccountKey [-VaultName] <String> [-AccountName] <String> [-KeyName] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7124e-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="7124e-106">ByInputObject</span></span>
```
Update-AzureKeyVaultManagedStorageAccountKey [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [-KeyName] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7124e-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7124e-107">DESCRIPTION</span></span>
<span data-ttu-id="7124e-108">Повторное создание указанного ключа учетной записи хранилища для управляемого хранилища Azure и задание ключа в качестве активного ключа.</span><span class="sxs-lookup"><span data-stu-id="7124e-108">Regenerates the specified key of Key Vault managed Azure Storage Account and sets the key as the active key.</span></span> <span data-ttu-id="7124e-109">Прокси-сервер хранилища ключей. вызов в диспетчере ресурсов Azure для повторного создания ключа.</span><span class="sxs-lookup"><span data-stu-id="7124e-109">Key Vault proxies the call to Azure Resource Manager to regenerate the key.</span></span> <span data-ttu-id="7124e-110">Вызывающий объект должен posses разрешения на повторное создание ключей в указанной учетной записи хранения Azure.</span><span class="sxs-lookup"><span data-stu-id="7124e-110">The caller must posses permissions to regenerate keys on given Azure Storage Account.</span></span>

## <span data-ttu-id="7124e-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7124e-111">EXAMPLES</span></span>

### <span data-ttu-id="7124e-112">Пример 1: повторное создание ключа</span><span class="sxs-lookup"><span data-stu-id="7124e-112">Example 1: Regenerate a key</span></span>
```powershell
PS C:\> Update-AzureKeyVaultManagedStorageAccountKey -VaultName 'myvault' -AccountName 'mystorageaccount' -KeyName 'key1'

Id                  : https://myvault.vault.azure.net:443/storage/mystorageaccount
Vault Name          : myvault
AccountName         : mystorageaccount
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/mystorageaccount
Active Key Name     : key1
Auto Regenerate Key : True
Regeneration Period : 90.00:00:00
Enabled             : True
Created             : 5/21/2018 11:55:58 PM
Updated             : 5/21/2018 11:55:58 PM
Tags                :
```

<span data-ttu-id="7124e-113">Повторное создание "key1" учетной записи "mystorageaccount" и установка "key1" в качестве активной учетной записи хранения для хранилища ключей в службе хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="7124e-113">Regenerates 'key1' of account 'mystorageaccount' and sets 'key1' as the active of the Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="7124e-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7124e-114">PARAMETERS</span></span>

### <span data-ttu-id="7124e-115">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="7124e-115">-AccountName</span></span>
<span data-ttu-id="7124e-116">Имя учетной записи хранилища с управляемым хранилищем.</span><span class="sxs-lookup"><span data-stu-id="7124e-116">Key Vault managed storage account name.</span></span> <span data-ttu-id="7124e-117">Командлет создает полное доменное имя управляемой учетной записи хранения из имени хранилища, выбранной в данный момент среды и управляемого имени учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="7124e-117">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefinitionName
Aliases: StorageAccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7124e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7124e-118">-DefaultProfile</span></span>
<span data-ttu-id="7124e-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="7124e-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7124e-120">-Force</span><span class="sxs-lookup"><span data-stu-id="7124e-120">-Force</span></span>
<span data-ttu-id="7124e-121">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="7124e-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="7124e-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7124e-122">-InputObject</span></span>
<span data-ttu-id="7124e-123">Объект ManagedStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="7124e-123">ManagedStorageAccount object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7124e-124">-KeyName</span><span class="sxs-lookup"><span data-stu-id="7124e-124">-KeyName</span></span>
<span data-ttu-id="7124e-125">Имя ключа учетной записи хранения, которое нужно повторно создать и сделать активным.</span><span class="sxs-lookup"><span data-stu-id="7124e-125">Name of storage account key to regenerate and make active.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7124e-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7124e-126">-PassThru</span></span>
<span data-ttu-id="7124e-127">По умолчанию командлет не возвращает объект.</span><span class="sxs-lookup"><span data-stu-id="7124e-127">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="7124e-128">Если этот параметр указан, командлет возвращает управляемую учетную запись хранения, которая была удалена.</span><span class="sxs-lookup"><span data-stu-id="7124e-128">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

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

### <span data-ttu-id="7124e-129">-VaultName</span><span class="sxs-lookup"><span data-stu-id="7124e-129">-VaultName</span></span>
<span data-ttu-id="7124e-130">Имя хранилища.</span><span class="sxs-lookup"><span data-stu-id="7124e-130">Vault name.</span></span>
<span data-ttu-id="7124e-131">Командлет создает полное доменное имя хранилища на основе имени и выбранной в данный момент среды.</span><span class="sxs-lookup"><span data-stu-id="7124e-131">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefinitionName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7124e-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7124e-132">-Confirm</span></span>
<span data-ttu-id="7124e-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7124e-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7124e-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7124e-134">-WhatIf</span></span>
<span data-ttu-id="7124e-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7124e-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7124e-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7124e-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7124e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7124e-137">CommonParameters</span></span>
<span data-ttu-id="7124e-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7124e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7124e-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7124e-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7124e-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7124e-140">INPUTS</span></span>

### <span data-ttu-id="7124e-141">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="7124e-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>
<span data-ttu-id="7124e-142">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7124e-142">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="7124e-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7124e-143">OUTPUTS</span></span>

### <span data-ttu-id="7124e-144">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7124e-144">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="7124e-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="7124e-145">NOTES</span></span>

## <span data-ttu-id="7124e-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7124e-146">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)


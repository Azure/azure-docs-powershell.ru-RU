---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 183618058d6400798dc2af74975fd45a0a397b16
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93900062"
---
# <span data-ttu-id="92b7c-101">Update-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="92b7c-101">Update-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="92b7c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="92b7c-102">SYNOPSIS</span></span>
<span data-ttu-id="92b7c-103">Обновление редактируемых атрибутов хранилища ключей управляемой учетной записи хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="92b7c-103">Update editable attributes of a Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="92b7c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="92b7c-104">SYNTAX</span></span>

### <span data-ttu-id="92b7c-105">ByDefinitionName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="92b7c-105">ByDefinitionName (Default)</span></span>
```
Update-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String> [-ActiveKeyName <String>]
 [-AutoRegenerateKey <Boolean>] [-RegenerationPeriod <TimeSpan>] [-Enable <Boolean>] [-Tag <Hashtable>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92b7c-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="92b7c-106">ByInputObject</span></span>
```
Update-AzKeyVaultManagedStorageAccount [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [-ActiveKeyName <String>] [-AutoRegenerateKey <Boolean>] [-RegenerationPeriod <TimeSpan>] [-Enable <Boolean>]
 [-Tag <Hashtable>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="92b7c-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="92b7c-107">DESCRIPTION</span></span>
<span data-ttu-id="92b7c-108">Обновите редактируемые атрибуты хранилища ключей управляемой учетной записи хранения Azure.</span><span class="sxs-lookup"><span data-stu-id="92b7c-108">Update the editable attributes of a Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="92b7c-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="92b7c-109">EXAMPLES</span></span>

### <span data-ttu-id="92b7c-110">Пример 1: Обновление активного ключа на "key2" в учетной записи хранения для хранилища ключей, управляемой хранилищем Azure.</span><span class="sxs-lookup"><span data-stu-id="92b7c-110">Example 1: Update the active key to 'key2' on a Key Vault managed Azure Storage Account.</span></span>
```powershell
PS C:\> Update-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -ActiveKeyName 'key2'

Id                  : https://myvault.vault.azure.net:443/storage/mystorageaccount
Vault Name          : myvault
AccountName         : mystorageaccount
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/mystorageaccount
Active Key Name     : key2
Auto Regenerate Key : True
Regeneration Period : 90.00:00:00
Enabled             : True
Created             : 5/21/2018 11:55:58 PM
Updated             : 5/21/2018 11:55:58 PM
Tags                :
```

<span data-ttu-id="92b7c-111">Обновление активного ключа учетной записи хранения для управляемого хранилища Azure Key на "key2".</span><span class="sxs-lookup"><span data-stu-id="92b7c-111">Updates the Key Vault managed Azure Storage Account active key to 'key2'.</span></span> <span data-ttu-id="92b7c-112">После этого обновления будет использован "key2" для создания маркеров SAS.</span><span class="sxs-lookup"><span data-stu-id="92b7c-112">'key2' will be used to generate SAS tokens after this update.</span></span>

## <span data-ttu-id="92b7c-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="92b7c-113">PARAMETERS</span></span>

### <span data-ttu-id="92b7c-114">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="92b7c-114">-AccountName</span></span>
<span data-ttu-id="92b7c-115">Имя учетной записи хранилища с управляемым хранилищем.</span><span class="sxs-lookup"><span data-stu-id="92b7c-115">Key Vault managed storage account name.</span></span> <span data-ttu-id="92b7c-116">Командлет создает полное доменное имя управляемой учетной записи хранения из имени хранилища, выбранной в данный момент среды и управляемого имени учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="92b7c-116">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

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

### <span data-ttu-id="92b7c-117">-ActiveKeyName</span><span class="sxs-lookup"><span data-stu-id="92b7c-117">-ActiveKeyName</span></span>
<span data-ttu-id="92b7c-118">Имя активного ключа.</span><span class="sxs-lookup"><span data-stu-id="92b7c-118">Active key name.</span></span>
<span data-ttu-id="92b7c-119">Если не указано, существующее значение активного имени ключа управляемой учетной записи хранения останется прежним.</span><span class="sxs-lookup"><span data-stu-id="92b7c-119">If not specified, the existing value of managed storage account's active key name remains unchanged</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92b7c-120">-AutoRegenerateKey</span><span class="sxs-lookup"><span data-stu-id="92b7c-120">-AutoRegenerateKey</span></span>
<span data-ttu-id="92b7c-121">Автоматическое повторное создание ключа.</span><span class="sxs-lookup"><span data-stu-id="92b7c-121">Auto regenerate key.</span></span>
<span data-ttu-id="92b7c-122">Если не указано, существующее значение автоматического повторного создания ключа для управляемой учетной записи хранения не изменяется</span><span class="sxs-lookup"><span data-stu-id="92b7c-122">If not specified, the existing value of auto regenerate key of managed storage account remains unchanged</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92b7c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92b7c-123">-DefaultProfile</span></span>
<span data-ttu-id="92b7c-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="92b7c-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="92b7c-125">-Enable (включить)</span><span class="sxs-lookup"><span data-stu-id="92b7c-125">-Enable</span></span>
<span data-ttu-id="92b7c-126">Если параметр указан, включает использование управляемого ключа учетной записи хранения для создания маркеров SAS, если значение равно true.</span><span class="sxs-lookup"><span data-stu-id="92b7c-126">If present, enables a use of a managed storage account key for sas token generation if value is true.</span></span> <span data-ttu-id="92b7c-127">Отключение использования управляемого ключа учетной записи хранения для создания маркеров SAS, если значение равно false.</span><span class="sxs-lookup"><span data-stu-id="92b7c-127">Disables use of a managed storage account key for sas token generation if value is false.</span></span> <span data-ttu-id="92b7c-128">Если не указано, существующее значение состояния Enabled и Disabled для учетной записи хранения не будет изменено.</span><span class="sxs-lookup"><span data-stu-id="92b7c-128">If not specified, the existing value of the storage account's enabled/disabled state remains unchanged.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92b7c-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="92b7c-129">-InputObject</span></span>
<span data-ttu-id="92b7c-130">Объект ManagedStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="92b7c-130">ManagedStorageAccount object.</span></span>

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

### <span data-ttu-id="92b7c-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="92b7c-131">-PassThru</span></span>
<span data-ttu-id="92b7c-132">По умолчанию командлет не возвращает объект.</span><span class="sxs-lookup"><span data-stu-id="92b7c-132">Cmdlet does not return object by default.</span></span> <span data-ttu-id="92b7c-133">Если указан этот параметр, возвращают управляемый объект учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="92b7c-133">If this switch is specified, return managed storage account object.</span></span>

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

### <span data-ttu-id="92b7c-134">-RegenerationPeriod</span><span class="sxs-lookup"><span data-stu-id="92b7c-134">-RegenerationPeriod</span></span>
<span data-ttu-id="92b7c-135">Период повторного создания.</span><span class="sxs-lookup"><span data-stu-id="92b7c-135">Regeneration period.</span></span> <span data-ttu-id="92b7c-136">Если включено автоматическое повторное создание ключа, это значение определяет интервал времени, после которого функция автоматического повторного создания keygets для управляемой учетной записи хранилища становится активной клавишей.</span><span class="sxs-lookup"><span data-stu-id="92b7c-136">If auto regenerate key is enabled, this value specifies the timespan after which managed storage account's inactive keygets auto regenerated and becomes the active key.</span></span> <span data-ttu-id="92b7c-137">Если не указано, существующее значение периода повторного создания ключей управляемой учетной записи хранения остается неизменным</span><span class="sxs-lookup"><span data-stu-id="92b7c-137">If not specified, the existing value of regeneration period of keys of managed storage account remains unchanged</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92b7c-138">-Тег</span><span class="sxs-lookup"><span data-stu-id="92b7c-138">-Tag</span></span>
<span data-ttu-id="92b7c-139">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="92b7c-139">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="92b7c-140">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="92b7c-140">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92b7c-141">-VaultName</span><span class="sxs-lookup"><span data-stu-id="92b7c-141">-VaultName</span></span>
<span data-ttu-id="92b7c-142">Имя хранилища.</span><span class="sxs-lookup"><span data-stu-id="92b7c-142">Vault name.</span></span>
<span data-ttu-id="92b7c-143">Командлет создает полное доменное имя хранилища на основе имени и выбранной в данный момент среды.</span><span class="sxs-lookup"><span data-stu-id="92b7c-143">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="92b7c-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="92b7c-144">-Confirm</span></span>
<span data-ttu-id="92b7c-145">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="92b7c-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92b7c-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92b7c-146">-WhatIf</span></span>
<span data-ttu-id="92b7c-147">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="92b7c-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92b7c-148">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="92b7c-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92b7c-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92b7c-149">CommonParameters</span></span>
<span data-ttu-id="92b7c-150">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="92b7c-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92b7c-151">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92b7c-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92b7c-152">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="92b7c-152">INPUTS</span></span>

### <span data-ttu-id="92b7c-153">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="92b7c-153">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="92b7c-154">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="92b7c-154">OUTPUTS</span></span>

### <span data-ttu-id="92b7c-155">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="92b7c-155">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="92b7c-156">Пуск</span><span class="sxs-lookup"><span data-stu-id="92b7c-156">NOTES</span></span>

## <span data-ttu-id="92b7c-157">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="92b7c-157">RELATED LINKS</span></span>

[<span data-ttu-id="92b7c-158">AZ. KeyVault</span><span class="sxs-lookup"><span data-stu-id="92b7c-158">Az.KeyVault</span></span>](/powershell/module/az.keyvault)

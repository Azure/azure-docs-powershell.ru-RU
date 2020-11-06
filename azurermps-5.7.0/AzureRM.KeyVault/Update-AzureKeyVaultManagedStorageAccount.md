---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/update-azurekeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Update-AzureKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Update-AzureKeyVaultManagedStorageAccount.md
ms.openlocfilehash: b16ceeb2409c2709286b970f857fcb9079bf067a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561739"
---
# <span data-ttu-id="2f346-101">Update-AzureKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2f346-101">Update-AzureKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="2f346-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2f346-102">SYNOPSIS</span></span>
<span data-ttu-id="2f346-103">Обновление редактируемых атрибутов хранилища ключей управляемой учетной записи хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="2f346-103">Update editable attributes of a Key Vault managed Azure Storage Account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2f346-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2f346-104">SYNTAX</span></span>

```
Update-AzureKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String>
 [-ActiveKeyName <String>] [-AutoRegenerateKey <Boolean>] [-RegenerationPeriod <TimeSpan>] [-Enable <Boolean>]
 [-Tag <Hashtable>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2f346-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2f346-105">DESCRIPTION</span></span>
<span data-ttu-id="2f346-106">Обновите редактируемые атрибуты хранилища ключей управляемой учетной записи хранения Azure.</span><span class="sxs-lookup"><span data-stu-id="2f346-106">Update the editable attributes of a Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="2f346-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2f346-107">EXAMPLES</span></span>

### <span data-ttu-id="2f346-108">Пример 1: Обновление активного ключа на "key2" в учетной записи хранения для хранилища ключей, управляемой хранилищем Azure.</span><span class="sxs-lookup"><span data-stu-id="2f346-108">Example 1:Update the active key to 'key2' on a Key Vault managed Azure Storage Account.</span></span>
```
PS C:\> Update-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -ActiveKeyName 'key2'
```

<span data-ttu-id="2f346-109">Обновление активного ключа учетной записи хранения для управляемого хранилища Azure Key на "key2".</span><span class="sxs-lookup"><span data-stu-id="2f346-109">Updates the Key Vault managed Azure Storage Account active key to 'key2'.</span></span> <span data-ttu-id="2f346-110">После этого обновления будет использован "key2" для создания маркеров SAS.</span><span class="sxs-lookup"><span data-stu-id="2f346-110">'key2' will be used to generate SAS tokens after this update.</span></span>

## <span data-ttu-id="2f346-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2f346-111">PARAMETERS</span></span>

### <span data-ttu-id="2f346-112">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="2f346-112">-AccountName</span></span>
<span data-ttu-id="2f346-113">Имя учетной записи хранилища с управляемым хранилищем.</span><span class="sxs-lookup"><span data-stu-id="2f346-113">Key Vault managed storage account name.</span></span> <span data-ttu-id="2f346-114">Командлет создает полное доменное имя управляемой учетной записи хранения из имени хранилища, выбранной в данный момент среды и управляемого имени учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="2f346-114">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f346-115">-ActiveKeyName</span><span class="sxs-lookup"><span data-stu-id="2f346-115">-ActiveKeyName</span></span>
<span data-ttu-id="2f346-116">Имя активного ключа.</span><span class="sxs-lookup"><span data-stu-id="2f346-116">Active key name.</span></span>
<span data-ttu-id="2f346-117">Если не указано, существующее значение активного имени ключа управляемой учетной записи хранения останется прежним.</span><span class="sxs-lookup"><span data-stu-id="2f346-117">If not specified, the existing value of managed storage account's active key name remains unchanged</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f346-118">-AutoRegenerateKey</span><span class="sxs-lookup"><span data-stu-id="2f346-118">-AutoRegenerateKey</span></span>
<span data-ttu-id="2f346-119">Автоматическое повторное создание ключа.</span><span class="sxs-lookup"><span data-stu-id="2f346-119">Auto regenerate key.</span></span>
<span data-ttu-id="2f346-120">Если не указано, существующее значение автоматического повторного создания ключа для управляемой учетной записи хранения не изменяется</span><span class="sxs-lookup"><span data-stu-id="2f346-120">If not specified, the existing value of auto regenerate key of managed storage account remains unchanged</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f346-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f346-121">-DefaultProfile</span></span>
<span data-ttu-id="2f346-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="2f346-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2f346-123">-Enable (включить)</span><span class="sxs-lookup"><span data-stu-id="2f346-123">-Enable</span></span>
<span data-ttu-id="2f346-124">Если параметр указан, включает использование управляемого ключа учетной записи хранения для создания маркеров SAS, если значение равно true.</span><span class="sxs-lookup"><span data-stu-id="2f346-124">If present, enables a use of a managed storage account key for sas token generation if value is true.</span></span> <span data-ttu-id="2f346-125">Отключение использования управляемого ключа учетной записи хранения для создания маркеров SAS, если значение равно false.</span><span class="sxs-lookup"><span data-stu-id="2f346-125">Disables use of a managed storage account key for sas token generation if value is false.</span></span> <span data-ttu-id="2f346-126">Если не указано, существующее значение состояния Enabled и Disabled для учетной записи хранения не будет изменено.</span><span class="sxs-lookup"><span data-stu-id="2f346-126">If not specified, the existing value of the storage account's enabled/disabled state remains unchanged.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f346-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2f346-127">-PassThru</span></span>
<span data-ttu-id="2f346-128">По умолчанию командлет не возвращает объект.</span><span class="sxs-lookup"><span data-stu-id="2f346-128">Cmdlet does not return object by default.</span></span> <span data-ttu-id="2f346-129">Если указан этот параметр, возвращают управляемый объект учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="2f346-129">If this switch is specified, return managed storage account object.</span></span>

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

### <span data-ttu-id="2f346-130">-RegenerationPeriod</span><span class="sxs-lookup"><span data-stu-id="2f346-130">-RegenerationPeriod</span></span>
<span data-ttu-id="2f346-131">Период повторного создания.</span><span class="sxs-lookup"><span data-stu-id="2f346-131">Regeneration period.</span></span> <span data-ttu-id="2f346-132">Если включено автоматическое повторное создание ключа, это значение определяет интервал времени, после которого функция автоматического повторного создания keygets для управляемой учетной записи хранилища становится активной клавишей.</span><span class="sxs-lookup"><span data-stu-id="2f346-132">If auto regenerate key is enabled, this value specifies the timespan after which managed storage account's inactive keygets auto regenerated and becomes the active key.</span></span> <span data-ttu-id="2f346-133">Если не указано, существующее значение периода повторного создания ключей управляемой учетной записи хранения остается неизменным</span><span class="sxs-lookup"><span data-stu-id="2f346-133">If not specified, the existing value of regeneration period of keys of managed storage account remains unchanged</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f346-134">-Тег</span><span class="sxs-lookup"><span data-stu-id="2f346-134">-Tag</span></span>
<span data-ttu-id="2f346-135">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="2f346-135">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="2f346-136">Например:</span><span class="sxs-lookup"><span data-stu-id="2f346-136">For example:</span></span>

<span data-ttu-id="2f346-137">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="2f346-137">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f346-138">-VaultName</span><span class="sxs-lookup"><span data-stu-id="2f346-138">-VaultName</span></span>
<span data-ttu-id="2f346-139">Имя хранилища.</span><span class="sxs-lookup"><span data-stu-id="2f346-139">Vault name.</span></span>
<span data-ttu-id="2f346-140">Командлет создает полное доменное имя хранилища на основе имени и выбранной в данный момент среды.</span><span class="sxs-lookup"><span data-stu-id="2f346-140">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f346-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2f346-141">-Confirm</span></span>
<span data-ttu-id="2f346-142">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2f346-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f346-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f346-143">-WhatIf</span></span>
<span data-ttu-id="2f346-144">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2f346-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f346-145">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2f346-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f346-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f346-146">CommonParameters</span></span>
<span data-ttu-id="2f346-147">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2f346-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f346-148">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f346-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f346-149">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2f346-149">INPUTS</span></span>

### <span data-ttu-id="2f346-150">Ничего</span><span class="sxs-lookup"><span data-stu-id="2f346-150">None</span></span>
<span data-ttu-id="2f346-151">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="2f346-151">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2f346-152">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2f346-152">OUTPUTS</span></span>

### <span data-ttu-id="2f346-153">Microsoft. Azure. Commands. KeyVault. Models. ManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2f346-153">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageAccount</span></span>

## <span data-ttu-id="2f346-154">Пуск</span><span class="sxs-lookup"><span data-stu-id="2f346-154">NOTES</span></span>

## <span data-ttu-id="2f346-155">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2f346-155">RELATED LINKS</span></span>

[<span data-ttu-id="2f346-156">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2f346-156">AzureRM.KeyVault</span></span>](/powershell/module/azurerm.keyvault)

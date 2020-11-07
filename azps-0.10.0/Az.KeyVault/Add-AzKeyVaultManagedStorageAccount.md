---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Add-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Add-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 85a0bc0f552688d036dc76ebbc6d15c608ade433
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911177"
---
# <span data-ttu-id="e3a6d-101">Add-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e3a6d-101">Add-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="e3a6d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e3a6d-102">SYNOPSIS</span></span>
<span data-ttu-id="e3a6d-103">Добавляет существующую учетную запись хранилища Azure в заданное хранилище ключей для ключей, управляемых службой хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="e3a6d-103">Adds an existing Azure Storage Account to the specified key vault for its keys to be managed by the Key Vault service.</span></span>

## <span data-ttu-id="e3a6d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e3a6d-104">SYNTAX</span></span>

```
Add-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String>
 [-AccountResourceId] <String> [-ActiveKeyName] <String> [-DisableAutoRegenerateKey]
 [-RegenerationPeriod <TimeSpan>] [-Disable] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3a6d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e3a6d-105">DESCRIPTION</span></span>
<span data-ttu-id="e3a6d-106">Настройка существующей учетной записи хранилища Azure с хранилищем ключей для ключей учетной записи хранения для управления с помощью ключей.</span><span class="sxs-lookup"><span data-stu-id="e3a6d-106">Sets up an existing Azure Storage Account with Key Vault for Storage Account keys to be managed by Key Vault.</span></span> <span data-ttu-id="e3a6d-107">Учетная запись хранения уже должна существовать.</span><span class="sxs-lookup"><span data-stu-id="e3a6d-107">The Storage Account must already exist.</span></span> <span data-ttu-id="e3a6d-108">Ключи хранилища никогда не открываются для вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="e3a6d-108">The Storage Keys are never exposed to caller.</span></span>
<span data-ttu-id="e3a6d-109">Автоматическое повторное создание ключа и переключение активного ключа на основе периода повторного создания.</span><span class="sxs-lookup"><span data-stu-id="e3a6d-109">Key Vault auto regenerates and switches the active key based on the regeneration period.</span></span>

## <span data-ttu-id="e3a6d-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e3a6d-110">EXAMPLES</span></span>

### <span data-ttu-id="e3a6d-111">Пример 1: Настройка учетной записи хранения Azure с помощью ключа Vault для управления ее ключами</span><span class="sxs-lookup"><span data-stu-id="e3a6d-111">Example 1: Set an Azure Storage Account with Key Vault to manage its keys</span></span>
```
PS C:\> $regenerationPeriod = [System.Timespan]::FromDays(90)
PS C:\> Add-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -ResourceId '/subscriptions/<subscription id>/resourceGroups/myresourcegroup/providers/Microsoft.Storage/storageAccounts/mystorageaccount' -ActiveKeyName 'key1' -RegenerationPeriod $regenerationPeriod
```

<span data-ttu-id="e3a6d-112">Задает учетной записи хранения с основным хранилищем ключей для управления с помощью Key Vault.</span><span class="sxs-lookup"><span data-stu-id="e3a6d-112">Sets a Storage Account with Key Vault for its keys to be managed by Key Vault.</span></span> <span data-ttu-id="e3a6d-113">Для активного ключа задано значение "key1".</span><span class="sxs-lookup"><span data-stu-id="e3a6d-113">The active key set is 'key1'.</span></span> <span data-ttu-id="e3a6d-114">Этот ключ будет использоваться для создания маркеров SAS.</span><span class="sxs-lookup"><span data-stu-id="e3a6d-114">This key will be used to generate sas tokens.</span></span> <span data-ttu-id="e3a6d-115">Ключевое приложение получит повторное создание ключа "key2" после периода повторного создания с момента выполнения этой команды и задает его в качестве активного ключа.</span><span class="sxs-lookup"><span data-stu-id="e3a6d-115">Key Vault will regenerate 'key2' key after the regeneration period from the time of this command and set it as the active key.</span></span> <span data-ttu-id="e3a6d-116">Этот процесс автоматического повторного создания продолжится между "key1" и "key2" с пропуском в 90 дней.</span><span class="sxs-lookup"><span data-stu-id="e3a6d-116">This auto regeneration process will continue between 'key1' and 'key2' with a gap of 90 days.</span></span>

### <span data-ttu-id="e3a6d-117">Пример 2: Настройка классической учетной записи хранилища Azure с помощью ключа Vault для управления ее ключами</span><span class="sxs-lookup"><span data-stu-id="e3a6d-117">Example 2: Set a Classic Azure Storage Account with Key Vault to manage its keys</span></span>
```
PS C:\> $regenerationPeriod = [System.Timespan]::FromDays(90)
PS C:\> Add-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -ResourceId '/subscriptions/<subscription id>/resourceGroups/myresourcegroup/providers/Microsoft.ClassicStorage/storageAccounts/mystorageaccount' -ActiveKeyName 'Primary' -RegenerationPeriod $regenerationPeriod
```

<span data-ttu-id="e3a6d-118">Задает классический учетной записи хранилища с основным хранилищем ключей для управления с помощью Key Vault.</span><span class="sxs-lookup"><span data-stu-id="e3a6d-118">Sets a Classic Storage Account with Key Vault for its keys to be managed by Key Vault.</span></span> <span data-ttu-id="e3a6d-119">Активным является параметр "основной".</span><span class="sxs-lookup"><span data-stu-id="e3a6d-119">The active key set is 'Primary'.</span></span> <span data-ttu-id="e3a6d-120">Этот ключ будет использоваться для создания маркеров SAS.</span><span class="sxs-lookup"><span data-stu-id="e3a6d-120">This key will be used to generate sas tokens.</span></span> <span data-ttu-id="e3a6d-121">Ключевое приложение получит повторное создание ключа "дополнительный" после периода повторного создания с момента этой команды и установит его в качестве активного ключа.</span><span class="sxs-lookup"><span data-stu-id="e3a6d-121">Key Vault will regenerate 'Secondary' key after the regeneration period from the time of this command and set it as the active key.</span></span> <span data-ttu-id="e3a6d-122">Этот процесс автоматического повторного создания продолжится между "основным" и "дополнительным" с пропуском в 90 дней.</span><span class="sxs-lookup"><span data-stu-id="e3a6d-122">This auto regeneration process will continue between 'Primary' and 'Secondary' with a gap of 90 days.</span></span>

## <span data-ttu-id="e3a6d-123">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e3a6d-123">PARAMETERS</span></span>

### <span data-ttu-id="e3a6d-124">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="e3a6d-124">-AccountName</span></span>
<span data-ttu-id="e3a6d-125">Имя учетной записи хранилища с управляемым хранилищем.</span><span class="sxs-lookup"><span data-stu-id="e3a6d-125">Key Vault managed storage account name.</span></span> <span data-ttu-id="e3a6d-126">Командлет создает полное доменное имя управляемой учетной записи хранения из имени хранилища, выбранной в данный момент среды и управляемого имени учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="e3a6d-126">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

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

### <span data-ttu-id="e3a6d-127">-AccountResourceId</span><span class="sxs-lookup"><span data-stu-id="e3a6d-127">-AccountResourceId</span></span>
<span data-ttu-id="e3a6d-128">Идентификатор ресурса Azure учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="e3a6d-128">Azure resource id of the storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountResourceId

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3a6d-129">-ActiveKeyName</span><span class="sxs-lookup"><span data-stu-id="e3a6d-129">-ActiveKeyName</span></span>
<span data-ttu-id="e3a6d-130">Имя ключа учетной записи хранения, которое необходимо использовать для создания маркеров SAS.</span><span class="sxs-lookup"><span data-stu-id="e3a6d-130">Name of the storage account key that must be used for generating sas tokens.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3a6d-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3a6d-131">-DefaultProfile</span></span>
<span data-ttu-id="e3a6d-132">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="e3a6d-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3a6d-133">-Отключение</span><span class="sxs-lookup"><span data-stu-id="e3a6d-133">-Disable</span></span>
<span data-ttu-id="e3a6d-134">Отключение использования ключа управляемой учетной записи хранения для создания маркеров SAS.</span><span class="sxs-lookup"><span data-stu-id="e3a6d-134">Disables the use of managed storage account's key for generation of sas tokens.</span></span>

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

### <span data-ttu-id="e3a6d-135">-DisableAutoRegenerateKey</span><span class="sxs-lookup"><span data-stu-id="e3a6d-135">-DisableAutoRegenerateKey</span></span>
<span data-ttu-id="e3a6d-136">Автоматическое повторное создание ключа.</span><span class="sxs-lookup"><span data-stu-id="e3a6d-136">Auto regenerate key.</span></span> <span data-ttu-id="e3a6d-137">Если установлено значение true, неактивный ключ для управляемой учетной записи хранения будет автоматически восстановлен и станет новым активным ключом после периода повторного создания.</span><span class="sxs-lookup"><span data-stu-id="e3a6d-137">If true, then the managed storage account's inactive key gets auto regenerated and becomes the new active key after the regeneration period.</span></span> <span data-ttu-id="e3a6d-138">Если задано значение false, ключи управляемой учетной записи хранения не воссоздаются автоматически.</span><span class="sxs-lookup"><span data-stu-id="e3a6d-138">If false, then the keys of managed storage account are not auto regenerated.</span></span>

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

### <span data-ttu-id="e3a6d-139">-RegenerationPeriod</span><span class="sxs-lookup"><span data-stu-id="e3a6d-139">-RegenerationPeriod</span></span>
<span data-ttu-id="e3a6d-140">Период повторного создания.</span><span class="sxs-lookup"><span data-stu-id="e3a6d-140">Regeneration period.</span></span> <span data-ttu-id="e3a6d-141">Если включено автоматическое повторное создание ключа, это значение определяет интервал времени, после которого функция автоматического повторного создания keygets управляемой учетной записи хранилища становится новым активным ключом.</span><span class="sxs-lookup"><span data-stu-id="e3a6d-141">If auto regenerate key is enabled, this value specifies the timespan after which managed storage account's inactive keygets auto regenerated and becomes the new active key.</span></span>

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

### <span data-ttu-id="e3a6d-142">-Тег</span><span class="sxs-lookup"><span data-stu-id="e3a6d-142">-Tag</span></span>
<span data-ttu-id="e3a6d-143">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="e3a6d-143">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="e3a6d-144">Например:</span><span class="sxs-lookup"><span data-stu-id="e3a6d-144">For example:</span></span>

<span data-ttu-id="e3a6d-145">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="e3a6d-145">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="e3a6d-146">-VaultName</span><span class="sxs-lookup"><span data-stu-id="e3a6d-146">-VaultName</span></span>
<span data-ttu-id="e3a6d-147">Имя хранилища.</span><span class="sxs-lookup"><span data-stu-id="e3a6d-147">Vault name.</span></span>
<span data-ttu-id="e3a6d-148">Командлет создает полное доменное имя хранилища на основе имени и выбранной в данный момент среды.</span><span class="sxs-lookup"><span data-stu-id="e3a6d-148">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="e3a6d-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e3a6d-149">-Confirm</span></span>
<span data-ttu-id="e3a6d-150">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e3a6d-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3a6d-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3a6d-151">-WhatIf</span></span>
<span data-ttu-id="e3a6d-152">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e3a6d-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3a6d-153">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e3a6d-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3a6d-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3a6d-154">CommonParameters</span></span>
<span data-ttu-id="e3a6d-155">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e3a6d-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3a6d-156">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3a6d-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3a6d-157">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e3a6d-157">INPUTS</span></span>

### <span data-ttu-id="e3a6d-158">Ничего</span><span class="sxs-lookup"><span data-stu-id="e3a6d-158">None</span></span>
<span data-ttu-id="e3a6d-159">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="e3a6d-159">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e3a6d-160">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e3a6d-160">OUTPUTS</span></span>

### <span data-ttu-id="e3a6d-161">Microsoft. Azure. Commands. KeyVault. Models. ManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e3a6d-161">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageAccount</span></span>

## <span data-ttu-id="e3a6d-162">Пуск</span><span class="sxs-lookup"><span data-stu-id="e3a6d-162">NOTES</span></span>

## <span data-ttu-id="e3a6d-163">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e3a6d-163">RELATED LINKS</span></span>

[<span data-ttu-id="e3a6d-164">AZ. KeyVault</span><span class="sxs-lookup"><span data-stu-id="e3a6d-164">Az.KeyVault</span></span>](/powershell/module/Az.keyvault)

---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://msdn.microsoft.com/en-us/library/dn868052.aspx
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 820a1c84600a3fb143d2b3c34a81e1f7cedac0d3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93570404"
---
# <span data-ttu-id="bd7e8-101">Add-AzureKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="bd7e8-101">Add-AzureKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="bd7e8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bd7e8-102">SYNOPSIS</span></span>
<span data-ttu-id="bd7e8-103">Добавляет существующую учетную запись хранилища Azure в заданное хранилище ключей для ключей, управляемых службой хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="bd7e8-103">Adds an existing Azure Storage Account to the specified key vault for its keys to be managed by the Key Vault service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bd7e8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bd7e8-104">SYNTAX</span></span>

```
Add-AzureKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String>
 [-AccountResourceId] <String> [-ActiveKeyName] <String> [-DisableAutoRegenerateKey]
 [-RegenerationPeriod <TimeSpan>] [-Disable] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd7e8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bd7e8-105">DESCRIPTION</span></span>
<span data-ttu-id="bd7e8-106">Настройка существующей учетной записи хранилища Azure с хранилищем ключей для ключей учетной записи хранения для управления с помощью ключей.</span><span class="sxs-lookup"><span data-stu-id="bd7e8-106">Sets up an existing Azure Storage Account with Key Vault for Storage Account keys to be managed by Key Vault.</span></span> <span data-ttu-id="bd7e8-107">Учетная запись хранения уже должна существовать.</span><span class="sxs-lookup"><span data-stu-id="bd7e8-107">The Storage Account must already exist.</span></span> <span data-ttu-id="bd7e8-108">Ключи хранилища никогда не открываются для вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="bd7e8-108">The Storage Keys are never exposed to caller.</span></span>
<span data-ttu-id="bd7e8-109">Автоматическое повторное создание ключа и переключение активного ключа на основе периода повторного создания.</span><span class="sxs-lookup"><span data-stu-id="bd7e8-109">Key Vault auto regenerates and switches the active key based on the regeneration period.</span></span>

## <span data-ttu-id="bd7e8-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bd7e8-110">EXAMPLES</span></span>

### <span data-ttu-id="bd7e8-111">Пример 1: Настройка учетной записи хранения Azure с помощью ключа Vault для управления ее ключами</span><span class="sxs-lookup"><span data-stu-id="bd7e8-111">Example 1: Set an Azure Storage Account with Key Vault to manage its keys</span></span>
```
PS C:\> $regenerationPeriod = [System.Timespan]::FromDays(90)
PS C:\> Add-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -ResourceId '/subscriptions/<subscription id>/resourceGroups/myresourcegroup/providers/Microsoft.Storage/storageAccounts/mystorageaccount' -ActiveKeyName 'key1' -RegenerationPeriod $regenerationPeriod
```

<span data-ttu-id="bd7e8-112">Задает учетной записи хранения с основным хранилищем ключей для управления с помощью Key Vault.</span><span class="sxs-lookup"><span data-stu-id="bd7e8-112">Sets a Storage Account with Key Vault for its keys to be managed by Key Vault.</span></span> <span data-ttu-id="bd7e8-113">Для активного ключа задано значение "key1".</span><span class="sxs-lookup"><span data-stu-id="bd7e8-113">The active key set is 'key1'.</span></span> <span data-ttu-id="bd7e8-114">Этот ключ будет использоваться для создания маркеров SAS.</span><span class="sxs-lookup"><span data-stu-id="bd7e8-114">This key will be used to generate sas tokens.</span></span> <span data-ttu-id="bd7e8-115">Ключевое приложение получит повторное создание ключа "key2" после периода повторного создания с момента выполнения этой команды и задает его в качестве активного ключа.</span><span class="sxs-lookup"><span data-stu-id="bd7e8-115">Key Vault will regenerate 'key2' key after the regeneration period from the time of this command and set it as the active key.</span></span> <span data-ttu-id="bd7e8-116">Этот процесс автоматического повторного создания продолжится между "key1" и "key2" с пропуском в 90 дней.</span><span class="sxs-lookup"><span data-stu-id="bd7e8-116">This auto regeneration process will continue between 'key1' and 'key2' with a gap of 90 days.</span></span>

### <span data-ttu-id="bd7e8-117">Пример 2: Настройка классической учетной записи хранилища Azure с помощью ключа Vault для управления ее ключами</span><span class="sxs-lookup"><span data-stu-id="bd7e8-117">Example 2: Set a Classic Azure Storage Account with Key Vault to manage its keys</span></span>
```
PS C:\> $regenerationPeriod = [System.Timespan]::FromDays(90)
PS C:\> Add-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -ResourceId '/subscriptions/<subscription id>/resourceGroups/myresourcegroup/providers/Microsoft.ClassicStorage/storageAccounts/mystorageaccount' -ActiveKeyName 'Primary' -RegenerationPeriod $regenerationPeriod
```

<span data-ttu-id="bd7e8-118">Задает классический учетной записи хранилища с основным хранилищем ключей для управления с помощью Key Vault.</span><span class="sxs-lookup"><span data-stu-id="bd7e8-118">Sets a Classic Storage Account with Key Vault for its keys to be managed by Key Vault.</span></span> <span data-ttu-id="bd7e8-119">Активным является параметр "основной".</span><span class="sxs-lookup"><span data-stu-id="bd7e8-119">The active key set is 'Primary'.</span></span> <span data-ttu-id="bd7e8-120">Этот ключ будет использоваться для создания маркеров SAS.</span><span class="sxs-lookup"><span data-stu-id="bd7e8-120">This key will be used to generate sas tokens.</span></span> <span data-ttu-id="bd7e8-121">Ключевое приложение получит повторное создание ключа "дополнительный" после периода повторного создания с момента этой команды и установит его в качестве активного ключа.</span><span class="sxs-lookup"><span data-stu-id="bd7e8-121">Key Vault will regenerate 'Secondary' key after the regeneration period from the time of this command and set it as the active key.</span></span> <span data-ttu-id="bd7e8-122">Этот процесс автоматического повторного создания продолжится между "основным" и "дополнительным" с пропуском в 90 дней.</span><span class="sxs-lookup"><span data-stu-id="bd7e8-122">This auto regeneration process will continue between 'Primary' and 'Secondary' with a gap of 90 days.</span></span>

## <span data-ttu-id="bd7e8-123">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bd7e8-123">PARAMETERS</span></span>

### <span data-ttu-id="bd7e8-124">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="bd7e8-124">-AccountName</span></span>
<span data-ttu-id="bd7e8-125">Имя учетной записи хранилища с управляемым хранилищем.</span><span class="sxs-lookup"><span data-stu-id="bd7e8-125">Key Vault managed storage account name.</span></span> <span data-ttu-id="bd7e8-126">Командлет создает полное доменное имя управляемой учетной записи хранения из имени хранилища, выбранной в данный момент среды и управляемого имени учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="bd7e8-126">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd7e8-127">-AccountResourceId</span><span class="sxs-lookup"><span data-stu-id="bd7e8-127">-AccountResourceId</span></span>
<span data-ttu-id="bd7e8-128">Идентификатор ресурса Azure учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="bd7e8-128">Azure resource id of the storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountResourceId

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd7e8-129">-ActiveKeyName</span><span class="sxs-lookup"><span data-stu-id="bd7e8-129">-ActiveKeyName</span></span>
<span data-ttu-id="bd7e8-130">Имя ключа учетной записи хранения, которое необходимо использовать для создания маркеров SAS.</span><span class="sxs-lookup"><span data-stu-id="bd7e8-130">Name of the storage account key that must be used for generating sas tokens.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd7e8-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bd7e8-131">-Confirm</span></span>
<span data-ttu-id="bd7e8-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="bd7e8-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd7e8-133">-Отключение</span><span class="sxs-lookup"><span data-stu-id="bd7e8-133">-Disable</span></span>
<span data-ttu-id="bd7e8-134">Отключение использования ключа управляемой учетной записи хранения для создания маркеров SAS.</span><span class="sxs-lookup"><span data-stu-id="bd7e8-134">Disables the use of managed storage account's key for generation of sas tokens.</span></span>

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

### <span data-ttu-id="bd7e8-135">-DisableAutoRegenerateKey</span><span class="sxs-lookup"><span data-stu-id="bd7e8-135">-DisableAutoRegenerateKey</span></span>
<span data-ttu-id="bd7e8-136">Автоматическое повторное создание ключа.</span><span class="sxs-lookup"><span data-stu-id="bd7e8-136">Auto regenerate key.</span></span> <span data-ttu-id="bd7e8-137">Если установлено значение true, неактивный ключ для управляемой учетной записи хранения будет автоматически восстановлен и станет новым активным ключом после периода повторного создания.</span><span class="sxs-lookup"><span data-stu-id="bd7e8-137">If true, then the managed storage account's inactive key gets auto regenerated and becomes the new active key after the regeneration period.</span></span> <span data-ttu-id="bd7e8-138">Если задано значение false, ключи управляемой учетной записи хранения не воссоздаются автоматически.</span><span class="sxs-lookup"><span data-stu-id="bd7e8-138">If false, then the keys of managed storage account are not auto regenerated.</span></span>

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

### <span data-ttu-id="bd7e8-139">-RegenerationPeriod</span><span class="sxs-lookup"><span data-stu-id="bd7e8-139">-RegenerationPeriod</span></span>
<span data-ttu-id="bd7e8-140">Период повторного создания.</span><span class="sxs-lookup"><span data-stu-id="bd7e8-140">Regeneration period.</span></span> <span data-ttu-id="bd7e8-141">Если включено автоматическое повторное создание ключа, это значение определяет интервал времени, после которого функция автоматического повторного создания keygets управляемой учетной записи хранилища становится новым активным ключом.</span><span class="sxs-lookup"><span data-stu-id="bd7e8-141">If auto regenerate key is enabled, this value specifies the timespan after which managed storage account's inactive keygets auto regenerated and becomes the new active key.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd7e8-142">-Тег</span><span class="sxs-lookup"><span data-stu-id="bd7e8-142">-Tag</span></span>
<span data-ttu-id="bd7e8-143">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="bd7e8-143">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="bd7e8-144">Например:</span><span class="sxs-lookup"><span data-stu-id="bd7e8-144">For example:</span></span>

<span data-ttu-id="bd7e8-145">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="bd7e8-145">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd7e8-146">-VaultName</span><span class="sxs-lookup"><span data-stu-id="bd7e8-146">-VaultName</span></span>
<span data-ttu-id="bd7e8-147">Имя хранилища.</span><span class="sxs-lookup"><span data-stu-id="bd7e8-147">Vault name.</span></span>
<span data-ttu-id="bd7e8-148">Командлет создает полное доменное имя хранилища на основе имени и выбранной в данный момент среды.</span><span class="sxs-lookup"><span data-stu-id="bd7e8-148">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd7e8-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd7e8-149">-WhatIf</span></span>
<span data-ttu-id="bd7e8-150">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="bd7e8-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd7e8-151">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="bd7e8-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd7e8-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd7e8-152">-DefaultProfile</span></span>
<span data-ttu-id="bd7e8-153">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bd7e8-153">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bd7e8-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd7e8-154">CommonParameters</span></span>
<span data-ttu-id="bd7e8-155">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bd7e8-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd7e8-156">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd7e8-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd7e8-157">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bd7e8-157">INPUTS</span></span>

## <span data-ttu-id="bd7e8-158">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bd7e8-158">OUTPUTS</span></span>

### <span data-ttu-id="bd7e8-159">Microsoft. Azure. Commands. KeyVault. Models. ManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="bd7e8-159">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageAccount</span></span>

## <span data-ttu-id="bd7e8-160">Пуск</span><span class="sxs-lookup"><span data-stu-id="bd7e8-160">NOTES</span></span>

## <span data-ttu-id="bd7e8-161">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bd7e8-161">RELATED LINKS</span></span>

[<span data-ttu-id="bd7e8-162">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="bd7e8-162">AzureRM.KeyVault</span></span>](/powershell/module/azurerm.keyvault)

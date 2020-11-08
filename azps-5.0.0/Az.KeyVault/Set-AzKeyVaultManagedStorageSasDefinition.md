---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultmanagedstoragesasdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultManagedStorageSasDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultManagedStorageSasDefinition.md
ms.openlocfilehash: ff73d5db0b16d7176b9c49aa6e70bc13fc9f3fba
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245283"
---
# <span data-ttu-id="7804b-101">Set-AzKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="7804b-101">Set-AzKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="7804b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7804b-102">SYNOPSIS</span></span>
<span data-ttu-id="7804b-103">Задает определение сигнатуры общего доступа (SAS) с помощью хранилища ключей для указанной учетной записи хранения для хранилища ключей в управляемом хранилище Azure.</span><span class="sxs-lookup"><span data-stu-id="7804b-103">Sets a Shared Access Signature (SAS) definition with Key Vault for a given Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="7804b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7804b-104">SYNTAX</span></span>

### <span data-ttu-id="7804b-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7804b-105">Default (Default)</span></span>
```
Set-AzKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-TemplateUri] <String> [-SasType] <String> [-Disable] [-Tag <Hashtable>] -ValidityPeriod <TimeSpan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7804b-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="7804b-106">ByInputObject</span></span>
```
Set-AzKeyVaultManagedStorageSasDefinition [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [-Name] <String> [-TemplateUri] <String> [-SasType] <String> [-Disable] [-Tag <Hashtable>]
 -ValidityPeriod <TimeSpan> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7804b-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7804b-107">DESCRIPTION</span></span>
<span data-ttu-id="7804b-108">Задает определение сигнатуры общего доступа (SAS) с учетной записью хранения для управления с помощью данного хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="7804b-108">Sets a Shared Access Signature (SAS) definition with a given Key Vault managed Azure Storage Account.</span></span> <span data-ttu-id="7804b-109">Это также задает секрет, который можно использовать для получения маркера SAS по этому определению SAS.</span><span class="sxs-lookup"><span data-stu-id="7804b-109">This also sets a secret which can be used to get the SAS token per this SAS definition.</span></span>
<span data-ttu-id="7804b-110">Маркер SAS генерируется с использованием этих параметров и активного ключа учетной записи хранения для хранилища ключей в службе хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="7804b-110">SAS token is generated using these parameters and the active key of the Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="7804b-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7804b-111">EXAMPLES</span></span>

### <span data-ttu-id="7804b-112">Пример 1: Настройка определения SAS типа учетной записи и получение на ее основе текущего маркера SAS</span><span class="sxs-lookup"><span data-stu-id="7804b-112">Example 1: Set an account-type SAS definition, and obtain a current SAS token based on it</span></span>
```powershell
PS C:\> $sa = Get-AzStorageAccount -Name mysa -ResourceGroupName myrg
PS C:\> $kv = Get-AzKeyVault -VaultName mykv
PS C:\> Add-AzKeyVaultManagedStorageAccount -VaultName $kv.VaultName -AccountName $sa.StorageAccountName -AccountResourceId $sa.Id -ActiveKeyName key1 -RegenerationPeriod ([System.Timespan]::FromDays(180))
PS C:\> $sctx = New-AzStorageContext -StorageAccountName $sa.StorageAccountName -Protocol Https -StorageAccountKey Key1
PS C:\> $start = [System.DateTime]::Now.AddDays(-1)
PS C:\> $end = [System.DateTime]::Now.AddMonths(1)
PS C:\> $at = New-AzStorageAccountSasToken -Service blob,file,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup" -Protocol HttpsOnly -StartTime $start -ExpiryTime $end -Context $sctx
PS C:\> $sas = Set-AzKeyVaultManagedStorageSasDefinition -AccountName $sa.StorageAccountName -VaultName $kv.VaultName -Name accountsas -TemplateUri $at -SasType 'account' -ValidityPeriod ([System.Timespan]::FromDays(30))
PS C:\> Get-AzKeyVaultSecret -VaultName $kv.VaultName -Name $sas.Sid.Substring($sas.Sid.LastIndexOf('/')+1)
```

<span data-ttu-id="7804b-113">Задает определение SAS учетной записи "accountsas" на KeyVault-управляемой учетной записи хранения "MYSA" в хранилище "mykv".</span><span class="sxs-lookup"><span data-stu-id="7804b-113">Sets an account SAS definition 'accountsas' on a KeyVault-managed storage account 'mysa' in vault 'mykv'.</span></span> <span data-ttu-id="7804b-114">В частности, в приведенной выше последовательности выполняются следующие действия:</span><span class="sxs-lookup"><span data-stu-id="7804b-114">Specifically, the sequence above performs the following:</span></span>
  - <span data-ttu-id="7804b-115">Получает (уже существующую) учетную запись хранения</span><span class="sxs-lookup"><span data-stu-id="7804b-115">gets a (pre-existing) storage account</span></span>
  - <span data-ttu-id="7804b-116">Получает (уже существующее) хранилище ключей</span><span class="sxs-lookup"><span data-stu-id="7804b-116">gets a (pre-existing) key vault</span></span>
  - <span data-ttu-id="7804b-117">Добавляет в хранилище KeyVault учетную запись хранения, задавая значение key1 в качестве активного ключа и с периодом повторного создания в 180 дней.</span><span class="sxs-lookup"><span data-stu-id="7804b-117">adds a KeyVault-managed storage account to the vault, setting Key1 as the active key, and with a regeneration period of 180 days</span></span>
  - <span data-ttu-id="7804b-118">Задает контекст хранения для указанной учетной записи хранения с помощью key1</span><span class="sxs-lookup"><span data-stu-id="7804b-118">sets a storage context for the specified storage account, with Key1</span></span>
  - <span data-ttu-id="7804b-119">Создание маркера SAS учетной записи для BLOB-объектов служб, файла, таблицы и очереди, для службы типов ресурсов, контейнера и объекта, с учетом всех разрешений по протоколу HTTPS и с указанными начальной и конечной датами.</span><span class="sxs-lookup"><span data-stu-id="7804b-119">creates an account SAS token for services Blob, File, Table and Queue, for resource types Service, Container and Object, with all permissions, over https and with the specified start and end dates</span></span>
  - <span data-ttu-id="7804b-120">Задает в хранилище определение SAS хранилища, управляемое по KeyVault, с URI шаблона в качестве созданного выше маркера SAS с типом данных "учетная запись" и действует в течение 30 дней.</span><span class="sxs-lookup"><span data-stu-id="7804b-120">sets a KeyVault-managed storage SAS definition in the vault, with the template uri as the SAS token created above, of SAS type 'account' and valid for 30 days</span></span>
  - <span data-ttu-id="7804b-121">Возвращает реальный маркер доступа из секрета KeyVault, соответствующего определению SAS.</span><span class="sxs-lookup"><span data-stu-id="7804b-121">retrieves the actual access token from the KeyVault secret corresponding to the SAS definition</span></span>

## <span data-ttu-id="7804b-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7804b-122">PARAMETERS</span></span>

### <span data-ttu-id="7804b-123">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="7804b-123">-AccountName</span></span>
<span data-ttu-id="7804b-124">Имя учетной записи хранилища с управляемым хранилищем.</span><span class="sxs-lookup"><span data-stu-id="7804b-124">Key Vault managed storage account name.</span></span> <span data-ttu-id="7804b-125">Командлет создает полное доменное имя управляемой учетной записи хранения из имени хранилища, выбранной в данный момент среды и управляемого имени учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="7804b-125">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: StorageAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7804b-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7804b-126">-DefaultProfile</span></span>
<span data-ttu-id="7804b-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="7804b-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7804b-128">-Отключение</span><span class="sxs-lookup"><span data-stu-id="7804b-128">-Disable</span></span>
<span data-ttu-id="7804b-129">Отключение использования определения SAS для создания маркера SAS.</span><span class="sxs-lookup"><span data-stu-id="7804b-129">Disables the use of sas definition for generation of sas token.</span></span>

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

### <span data-ttu-id="7804b-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7804b-130">-InputObject</span></span>
<span data-ttu-id="7804b-131">Объект ManagedStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="7804b-131">ManagedStorageAccount object.</span></span>

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

### <span data-ttu-id="7804b-132">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7804b-132">-Name</span></span>
<span data-ttu-id="7804b-133">Имя определения SAS хранилища.</span><span class="sxs-lookup"><span data-stu-id="7804b-133">Storage sas definition name.</span></span> <span data-ttu-id="7804b-134">Командлет создает полное доменное имя определения SAS хранилища из имени хранилища, выбранной среды, имени учетной записи хранения и имени определения SAS.</span><span class="sxs-lookup"><span data-stu-id="7804b-134">Cmdlet constructs the FQDN of a storage sas definition from vault name, currently selected environment, storage account name and sas definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SasDefinitionName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7804b-135">-SasType</span><span class="sxs-lookup"><span data-stu-id="7804b-135">-SasType</span></span>
<span data-ttu-id="7804b-136">Тип SAS хранилища.</span><span class="sxs-lookup"><span data-stu-id="7804b-136">Storage SAS type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7804b-137">-Тег</span><span class="sxs-lookup"><span data-stu-id="7804b-137">-Tag</span></span>
<span data-ttu-id="7804b-138">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="7804b-138">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="7804b-139">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="7804b-139">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="7804b-140">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="7804b-140">-TemplateUri</span></span>
<span data-ttu-id="7804b-141">URI шаблона определения SAS хранилища.</span><span class="sxs-lookup"><span data-stu-id="7804b-141">Storage SAS definition template uri.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7804b-142">-ValidityPeriod</span><span class="sxs-lookup"><span data-stu-id="7804b-142">-ValidityPeriod</span></span>
<span data-ttu-id="7804b-143">Срок действия, который будет использоваться для задания срока действия маркера SAS с момента создания.</span><span class="sxs-lookup"><span data-stu-id="7804b-143">Validity period that will get used to set the expiry time of sas token from the time it gets generated</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7804b-144">-VaultName</span><span class="sxs-lookup"><span data-stu-id="7804b-144">-VaultName</span></span>
<span data-ttu-id="7804b-145">Имя хранилища.</span><span class="sxs-lookup"><span data-stu-id="7804b-145">Vault name.</span></span>
<span data-ttu-id="7804b-146">Командлет создает полное доменное имя хранилища на основе имени и выбранной в данный момент среды.</span><span class="sxs-lookup"><span data-stu-id="7804b-146">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="7804b-147">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7804b-147">-Confirm</span></span>
<span data-ttu-id="7804b-148">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7804b-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7804b-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7804b-149">-WhatIf</span></span>
<span data-ttu-id="7804b-150">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7804b-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7804b-151">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7804b-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7804b-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7804b-152">CommonParameters</span></span>
<span data-ttu-id="7804b-153">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7804b-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7804b-154">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7804b-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7804b-155">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7804b-155">INPUTS</span></span>

### <span data-ttu-id="7804b-156">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="7804b-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="7804b-157">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7804b-157">OUTPUTS</span></span>

### <span data-ttu-id="7804b-158">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="7804b-158">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="7804b-159">Пуск</span><span class="sxs-lookup"><span data-stu-id="7804b-159">NOTES</span></span>

## <span data-ttu-id="7804b-160">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7804b-160">RELATED LINKS</span></span>

[<span data-ttu-id="7804b-161">Azureâ € ‹ RM. в € ‹ keyâ € ‹ Vault</span><span class="sxs-lookup"><span data-stu-id="7804b-161">Azureâ€‹RM.â€‹Keyâ€‹Vault</span></span>](/powershell/module/az.keyvault/)

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultmanagedstoragesasdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultManagedStorageSasDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultManagedStorageSasDefinition.md
ms.openlocfilehash: ff73d5db0b16d7176b9c49aa6e70bc13fc9f3fba
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98507187"
---
# <span data-ttu-id="6af80-101">Set-AzKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="6af80-101">Set-AzKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="6af80-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6af80-102">SYNOPSIS</span></span>
<span data-ttu-id="6af80-103">Задает определение подписи ОБЩЕГО доступа (SAS) с хранилищем ключа для заданного ключевого хранилища, управляемой учетной записью хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="6af80-103">Sets a Shared Access Signature (SAS) definition with Key Vault for a given Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="6af80-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6af80-104">SYNTAX</span></span>

### <span data-ttu-id="6af80-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6af80-105">Default (Default)</span></span>
```
Set-AzKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-TemplateUri] <String> [-SasType] <String> [-Disable] [-Tag <Hashtable>] -ValidityPeriod <TimeSpan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6af80-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="6af80-106">ByInputObject</span></span>
```
Set-AzKeyVaultManagedStorageSasDefinition [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [-Name] <String> [-TemplateUri] <String> [-SasType] <String> [-Disable] [-Tag <Hashtable>]
 -ValidityPeriod <TimeSpan> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6af80-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6af80-107">DESCRIPTION</span></span>
<span data-ttu-id="6af80-108">Задает определение подписи общего доступа (SAS) с помощью учетной записи хранилища Azure, управляемой основным хранилищем.</span><span class="sxs-lookup"><span data-stu-id="6af80-108">Sets a Shared Access Signature (SAS) definition with a given Key Vault managed Azure Storage Account.</span></span> <span data-ttu-id="6af80-109">Это также задает секрет, который можно использовать для получения маркера SAS для определения SAS.</span><span class="sxs-lookup"><span data-stu-id="6af80-109">This also sets a secret which can be used to get the SAS token per this SAS definition.</span></span>
<span data-ttu-id="6af80-110">Маркер SAS создается с использованием этих параметров и активного ключа учетной записи хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="6af80-110">SAS token is generated using these parameters and the active key of the Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="6af80-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6af80-111">EXAMPLES</span></span>

### <span data-ttu-id="6af80-112">Пример 1. Настройка определения SAS типа учетной записи и получение текущего маркера SAS на его основе</span><span class="sxs-lookup"><span data-stu-id="6af80-112">Example 1: Set an account-type SAS definition, and obtain a current SAS token based on it</span></span>
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

<span data-ttu-id="6af80-113">Задает определение SAS учетной записи "учетные записи" в учетной записи хранилища, управляемой KeyVault, "mysa" в хранилище mykv.</span><span class="sxs-lookup"><span data-stu-id="6af80-113">Sets an account SAS definition 'accountsas' on a KeyVault-managed storage account 'mysa' in vault 'mykv'.</span></span> <span data-ttu-id="6af80-114">В частности, в следующей последовательности выполняются следующие действия:</span><span class="sxs-lookup"><span data-stu-id="6af80-114">Specifically, the sequence above performs the following:</span></span>
  - <span data-ttu-id="6af80-115">получает (предварительно существующую) учетную запись хранения</span><span class="sxs-lookup"><span data-stu-id="6af80-115">gets a (pre-existing) storage account</span></span>
  - <span data-ttu-id="6af80-116">получает (предварительно существующее) хранилище ключа</span><span class="sxs-lookup"><span data-stu-id="6af80-116">gets a (pre-existing) key vault</span></span>
  - <span data-ttu-id="6af80-117">добавляет учетную запись хранения с управлением KeyVault в хранилище, направив клавишу 1 в качестве активного ключа с периодом в 180 дней</span><span class="sxs-lookup"><span data-stu-id="6af80-117">adds a KeyVault-managed storage account to the vault, setting Key1 as the active key, and with a regeneration period of 180 days</span></span>
  - <span data-ttu-id="6af80-118">задает контекст хранилища для указанной учетной записи хранения с ключом 1</span><span class="sxs-lookup"><span data-stu-id="6af80-118">sets a storage context for the specified storage account, with Key1</span></span>
  - <span data-ttu-id="6af80-119">Создает маркер SAS учетной записи для служб BLOB-объектов, файлов, таблиц и очередей, для типов ресурсов "Служба", "Контейнер" и "Объект" со всеми разрешениями по протоколу https и с указанными датами начала и окончания.</span><span class="sxs-lookup"><span data-stu-id="6af80-119">creates an account SAS token for services Blob, File, Table and Queue, for resource types Service, Container and Object, with all permissions, over https and with the specified start and end dates</span></span>
  - <span data-ttu-id="6af80-120">Задает определение SAS хранилища, управляемого KeyVault, в хранилище, где шаблон uri является токеном SAS, созданным выше, и типом SAS "учетная запись" и действительным в течение 30 дней.</span><span class="sxs-lookup"><span data-stu-id="6af80-120">sets a KeyVault-managed storage SAS definition in the vault, with the template uri as the SAS token created above, of SAS type 'account' and valid for 30 days</span></span>
  - <span data-ttu-id="6af80-121">Извлекает фактический маркер доступа из секретного ключа KeyVault, соответствующего определению SAS.</span><span class="sxs-lookup"><span data-stu-id="6af80-121">retrieves the actual access token from the KeyVault secret corresponding to the SAS definition</span></span>

## <span data-ttu-id="6af80-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6af80-122">PARAMETERS</span></span>

### <span data-ttu-id="6af80-123">-AccountName</span><span class="sxs-lookup"><span data-stu-id="6af80-123">-AccountName</span></span>
<span data-ttu-id="6af80-124">Имя учетной записи, управляемой хранилищем Key Vault.</span><span class="sxs-lookup"><span data-stu-id="6af80-124">Key Vault managed storage account name.</span></span> <span data-ttu-id="6af80-125">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span><span class="sxs-lookup"><span data-stu-id="6af80-125">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

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

### <span data-ttu-id="6af80-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6af80-126">-DefaultProfile</span></span>
<span data-ttu-id="6af80-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="6af80-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6af80-128">-Disable</span><span class="sxs-lookup"><span data-stu-id="6af80-128">-Disable</span></span>
<span data-ttu-id="6af80-129">Отключает использование определения sas для генерации маркера sas.</span><span class="sxs-lookup"><span data-stu-id="6af80-129">Disables the use of sas definition for generation of sas token.</span></span>

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

### <span data-ttu-id="6af80-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6af80-130">-InputObject</span></span>
<span data-ttu-id="6af80-131">Объект ManagedStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="6af80-131">ManagedStorageAccount object.</span></span>

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

### <span data-ttu-id="6af80-132">-Name</span><span class="sxs-lookup"><span data-stu-id="6af80-132">-Name</span></span>
<span data-ttu-id="6af80-133">Имя определения sas хранилища.</span><span class="sxs-lookup"><span data-stu-id="6af80-133">Storage sas definition name.</span></span> <span data-ttu-id="6af80-134">Cmdlet конструировать FQDN определения sas хранилища из имени хранилища, выбранной среды, имени учетной записи хранения и имени определения sas.</span><span class="sxs-lookup"><span data-stu-id="6af80-134">Cmdlet constructs the FQDN of a storage sas definition from vault name, currently selected environment, storage account name and sas definition name.</span></span>

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

### <span data-ttu-id="6af80-135">-SasType</span><span class="sxs-lookup"><span data-stu-id="6af80-135">-SasType</span></span>
<span data-ttu-id="6af80-136">Тип SAS хранилища.</span><span class="sxs-lookup"><span data-stu-id="6af80-136">Storage SAS type.</span></span>

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

### <span data-ttu-id="6af80-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="6af80-137">-Tag</span></span>
<span data-ttu-id="6af80-138">Пары значений ключа в виде hash table.</span><span class="sxs-lookup"><span data-stu-id="6af80-138">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="6af80-139">Например: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="6af80-139">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="6af80-140">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="6af80-140">-TemplateUri</span></span>
<span data-ttu-id="6af80-141">URI шаблона определения SAS хранилища.</span><span class="sxs-lookup"><span data-stu-id="6af80-141">Storage SAS definition template uri.</span></span>

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

### <span data-ttu-id="6af80-142">-ValidityPeriod</span><span class="sxs-lookup"><span data-stu-id="6af80-142">-ValidityPeriod</span></span>
<span data-ttu-id="6af80-143">Срок действия, который будет использоваться для того, чтобы установить срок действия маркера sas с времени его получения</span><span class="sxs-lookup"><span data-stu-id="6af80-143">Validity period that will get used to set the expiry time of sas token from the time it gets generated</span></span>

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

### <span data-ttu-id="6af80-144">-VaultName</span><span class="sxs-lookup"><span data-stu-id="6af80-144">-VaultName</span></span>
<span data-ttu-id="6af80-145">Имя сейфа.</span><span class="sxs-lookup"><span data-stu-id="6af80-145">Vault name.</span></span>
<span data-ttu-id="6af80-146">С его учетом именем и выбранной средой строится FQDN хранилища.</span><span class="sxs-lookup"><span data-stu-id="6af80-146">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="6af80-147">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6af80-147">-Confirm</span></span>
<span data-ttu-id="6af80-148">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6af80-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6af80-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6af80-149">-WhatIf</span></span>
<span data-ttu-id="6af80-150">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6af80-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6af80-151">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="6af80-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6af80-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6af80-152">CommonParameters</span></span>
<span data-ttu-id="6af80-153">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6af80-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6af80-154">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6af80-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6af80-155">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6af80-155">INPUTS</span></span>

### <span data-ttu-id="6af80-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="6af80-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="6af80-157">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6af80-157">OUTPUTS</span></span>

### <span data-ttu-id="6af80-158">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="6af80-158">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="6af80-159">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6af80-159">NOTES</span></span>

## <span data-ttu-id="6af80-160">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6af80-160">RELATED LINKS</span></span>

[<span data-ttu-id="6af80-161">Azureâ€;RM.â€™Keyâ?Vault</span><span class="sxs-lookup"><span data-stu-id="6af80-161">Azureâ€‹RM.â€‹Keyâ€‹Vault</span></span>](/powershell/module/az.keyvault/)

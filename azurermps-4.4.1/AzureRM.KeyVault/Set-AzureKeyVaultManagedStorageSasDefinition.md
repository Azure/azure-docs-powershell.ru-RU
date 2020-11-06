---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://msdn.microsoft.com/en-us/library/dn868052.aspx
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultManagedStorageSasDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultManagedStorageSasDefinition.md
ms.openlocfilehash: e32e57932731e788def7a8e27c85c956795b0c4e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568756"
---
# <span data-ttu-id="e618d-101">Set-AzureKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="e618d-101">Set-AzureKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="e618d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e618d-102">SYNOPSIS</span></span>
<span data-ttu-id="e618d-103">Задает определение сигнатуры общего доступа (SAS) с помощью хранилища ключей для указанной учетной записи хранения для хранилища ключей в управляемом хранилище Azure.</span><span class="sxs-lookup"><span data-stu-id="e618d-103">Sets a Shared Access Signature (SAS) definition with Key Vault for a given Key Vault managed Azure Storage Account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e618d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e618d-104">SYNTAX</span></span>

### <span data-ttu-id="e618d-105">RawSas (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e618d-105">RawSas (Default)</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Parameter] <Hashtable> [-Disable] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e618d-106">AdhocAccountSas</span><span class="sxs-lookup"><span data-stu-id="e618d-106">AdhocAccountSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition -Service <String[]> -ResourceType <String[]>
 [-ApiVersion <String>] [-VaultName] <String> [-AccountName] <String> [-Name] <String> [-Disable]
 [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>] [-IPAddressOrRange <String>]
 -ValidityPeriod <TimeSpan> -Permission <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e618d-107">AdhocServiceBlobSas</span><span class="sxs-lookup"><span data-stu-id="e618d-107">AdhocServiceBlobSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -ValidityPeriod <TimeSpan> -Permission <String[]> -Blob <String>
 -Container <String> [-SharedAccessHeader <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e618d-108">AdhocServiceContainerSas</span><span class="sxs-lookup"><span data-stu-id="e618d-108">AdhocServiceContainerSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -ValidityPeriod <TimeSpan> -Permission <String[]> -Container <String>
 [-SharedAccessHeader <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e618d-109">AdhocServiceFileSas</span><span class="sxs-lookup"><span data-stu-id="e618d-109">AdhocServiceFileSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -ValidityPeriod <TimeSpan> -Permission <String[]>
 [-SharedAccessHeader <String[]>] -Share <String> -Path <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e618d-110">AdhocServiceShareSas</span><span class="sxs-lookup"><span data-stu-id="e618d-110">AdhocServiceShareSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -ValidityPeriod <TimeSpan> -Permission <String[]>
 [-SharedAccessHeader <String[]>] -Share <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e618d-111">AdhocServiceQueueSas</span><span class="sxs-lookup"><span data-stu-id="e618d-111">AdhocServiceQueueSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -ValidityPeriod <TimeSpan> -Permission <String[]> -Queue <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e618d-112">AdhocServiceTableSas</span><span class="sxs-lookup"><span data-stu-id="e618d-112">AdhocServiceTableSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -ValidityPeriod <TimeSpan> -Permission <String[]> -Table <String>
 [-StartPartitionKey <String>] [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e618d-113">StoredPolicyServiceBlobSas</span><span class="sxs-lookup"><span data-stu-id="e618d-113">StoredPolicyServiceBlobSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -Blob <String> -Container <String> -Policy <String>
 [-SharedAccessHeader <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e618d-114">StoredPolicyServiceContainerSas</span><span class="sxs-lookup"><span data-stu-id="e618d-114">StoredPolicyServiceContainerSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -Container <String> -Policy <String> [-SharedAccessHeader <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e618d-115">StoredPolicyServiceFileSas</span><span class="sxs-lookup"><span data-stu-id="e618d-115">StoredPolicyServiceFileSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -Policy <String> [-SharedAccessHeader <String[]>] -Share <String> -Path <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e618d-116">StoredPolicyServiceShareSas</span><span class="sxs-lookup"><span data-stu-id="e618d-116">StoredPolicyServiceShareSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -Policy <String> [-SharedAccessHeader <String[]>] -Share <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e618d-117">StoredPolicyServiceQueueSas</span><span class="sxs-lookup"><span data-stu-id="e618d-117">StoredPolicyServiceQueueSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -Policy <String> -Queue <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e618d-118">StoredPolicyServiceTableSas</span><span class="sxs-lookup"><span data-stu-id="e618d-118">StoredPolicyServiceTableSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -Policy <String> -Table <String> [-StartPartitionKey <String>]
 [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e618d-119">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e618d-119">DESCRIPTION</span></span>
<span data-ttu-id="e618d-120">Задает определение сигнатуры общего доступа (SAS) с учетной записью хранения для управления с помощью данного хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="e618d-120">Sets a Shared Access Signature (SAS) definition with a given Key Vault managed Azure Storage Account.</span></span> <span data-ttu-id="e618d-121">Это также задает секрет, который можно использовать для получения маркера SAS по этому определению SAS.</span><span class="sxs-lookup"><span data-stu-id="e618d-121">This also sets a secret which can be used to get the SAS token per this SAS definition.</span></span>
<span data-ttu-id="e618d-122">Маркер SAS генерируется с использованием этих параметров и активного ключа учетной записи хранения для хранилища ключей в службе хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="e618d-122">SAS token is generated using these parameters and the active key of the Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="e618d-123">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e618d-123">EXAMPLES</span></span>

### <span data-ttu-id="e618d-124">Пример 1: Настройка определения SAS для блоба нерегламентированных служб</span><span class="sxs-lookup"><span data-stu-id="e618d-124">Example 1 : Set an ad hoc service Blob sas definition</span></span>
```
PS C:\> Set-AzureKeyVaultManagedStorageSasDefinition -Blob 'blob1' -Container 'container1' -VaultName 'vault1' -AccountName 'account1' -Name 'sas1' -ValidityPeriod ([System.Timespan]::FromDays(30)) -Permission Read,Add -SharedAccessHeader CacheControl,ContentDisposition -Protocol HttpsOnly -IPAddressOrRange '168.1.5.60-168.1.5.70'
```

<span data-ttu-id="e618d-125">Задает определение сопоставления безопасности BLOB-объектов ad hoc ("sas1") с управляемой учетной записью хранения для хранилища ключей "компьютера1" в хранилище "vault1".</span><span class="sxs-lookup"><span data-stu-id="e618d-125">Sets an ad hoc service blob sas definition 'sas1' with key vault managed storage account 'account1' in vault 'vault1'.</span></span>

### <span data-ttu-id="e618d-126">Пример 2: Настройка определения SAS для учетной записи ad hoc</span><span class="sxs-lookup"><span data-stu-id="e618d-126">Example 2 : Set an ad hoc account sas definition</span></span>
```
PS C:\> Set-AzureKeyVaultManagedStorageSasDefinition -Service Blob,File -ResourceType Container,Service -VaultName 'vault1' -AccountName 'account1' -Name 'sas1' -Protocol HttpsOrHttp -IPAddressOrRange '168.1.5.60' -ValidityPeriod ([System.Timespan]::FromDays(30)) -Permission Read,Add
```

<span data-ttu-id="e618d-127">Задает ad hoc определение SAS "sas1" с управляемой учетной записью хранения для хранилища ключей "компьютера1" в хранилище "vault1".</span><span class="sxs-lookup"><span data-stu-id="e618d-127">Sets an ad hoc blob sas definition 'sas1' with key vault managed storage account 'account1' in vault 'vault1'.</span></span>

### <span data-ttu-id="e618d-128">Пример 3: Настройка определения SAS с помощью хэш-таблицы</span><span class="sxs-lookup"><span data-stu-id="e618d-128">Example 3 : Set a sas definition using a hashtable</span></span>
```
PS C:\> $parameters = @{"sasType"="blob";"signedVersion"="2016-05-31";"signedProtocols"="https";"signedIp"="168.1.5.60-168.1.5.70";"validityPeriod"="P30D";"signedPermissions"="ra";"blobName"="blob1";"containerName"="container1";"rscd"="";"rscc"=""}
PS C:\> Set-AzureKeyVaultManagedStorageSasDefinition -VaultName vault1 -AccountName account1 -Name sas1 -Parameter $parameters
```

<span data-ttu-id="e618d-129">Задает для ad hoc определение SAS "sas1" с управляемой учетной записью хранения для хранилища ключей "компьютера1" в хранилище "vault1" с помощью Hashtable.</span><span class="sxs-lookup"><span data-stu-id="e618d-129">Sets an ad hoc blob sas definition 'sas1' with key vault managed storage account 'account1' in vault 'vault1' using a hashtable.</span></span>

## <span data-ttu-id="e618d-130">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e618d-130">PARAMETERS</span></span>

### <span data-ttu-id="e618d-131">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="e618d-131">-AccountName</span></span>
<span data-ttu-id="e618d-132">Имя учетной записи хранилища с управляемым хранилищем.</span><span class="sxs-lookup"><span data-stu-id="e618d-132">Key Vault managed storage account name.</span></span> <span data-ttu-id="e618d-133">Командлет создает полное доменное имя управляемой учетной записи хранения из имени хранилища, выбранной в данный момент среды и управляемого имени учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="e618d-133">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e618d-134">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="e618d-134">-ApiVersion</span></span>
<span data-ttu-id="e618d-135">Указывает версию службы хранилища, используемую для выполнения запроса, созданного с помощью URI SAS учетной записи.</span><span class="sxs-lookup"><span data-stu-id="e618d-135">Specifies the storage service version to use to execute the request made using the account SAS URI.</span></span>

```yaml
Type: System.String
Parameter Sets: AdhocAccountSas
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e618d-136">-BLOB</span><span class="sxs-lookup"><span data-stu-id="e618d-136">-Blob</span></span>
<span data-ttu-id="e618d-137">Имя BLOB-объекта</span><span class="sxs-lookup"><span data-stu-id="e618d-137">Blob Name</span></span>

```yaml
Type: System.String
Parameter Sets: AdhocServiceBlobSas, StoredPolicyServiceBlobSas
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e618d-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e618d-138">-Confirm</span></span>
<span data-ttu-id="e618d-139">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e618d-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e618d-140">-Container</span><span class="sxs-lookup"><span data-stu-id="e618d-140">-Container</span></span>
<span data-ttu-id="e618d-141">Имя контейнера</span><span class="sxs-lookup"><span data-stu-id="e618d-141">Container Name</span></span>

```yaml
Type: System.String
Parameter Sets: AdhocServiceBlobSas, AdhocServiceContainerSas, StoredPolicyServiceBlobSas, StoredPolicyServiceContainerSas
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e618d-142">-Отключение</span><span class="sxs-lookup"><span data-stu-id="e618d-142">-Disable</span></span>
<span data-ttu-id="e618d-143">Отключение использования определения SAS для создания маркера SAS.</span><span class="sxs-lookup"><span data-stu-id="e618d-143">Disables the use of sas definition for generation of sas token.</span></span>

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

### <span data-ttu-id="e618d-144">-EndPartitionKey</span><span class="sxs-lookup"><span data-stu-id="e618d-144">-EndPartitionKey</span></span>
<span data-ttu-id="e618d-145">Клавиша End Partition</span><span class="sxs-lookup"><span data-stu-id="e618d-145">End Partition Key</span></span>

```yaml
Type: System.String
Parameter Sets: AdhocServiceTableSas, StoredPolicyServiceTableSas
Aliases: endpk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e618d-146">-EndRowKey</span><span class="sxs-lookup"><span data-stu-id="e618d-146">-EndRowKey</span></span>
<span data-ttu-id="e618d-147">Клавиша "конец строки"</span><span class="sxs-lookup"><span data-stu-id="e618d-147">End Row Key</span></span>

```yaml
Type: System.String
Parameter Sets: AdhocServiceTableSas, StoredPolicyServiceTableSas
Aliases: endrk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e618d-148">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="e618d-148">-IPAddressOrRange</span></span>
<span data-ttu-id="e618d-149">IP-адрес или ACL диапазона IP-адресов (список управления доступом) для запроса, который будет принят службой хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="e618d-149">IP, or IP range ACL (access control list) of the request that would be accepted by Azure Storage.</span></span>

```yaml
Type: System.String
Parameter Sets: AdhocAccountSas, AdhocServiceBlobSas, AdhocServiceContainerSas, AdhocServiceFileSas, AdhocServiceShareSas, AdhocServiceQueueSas, AdhocServiceTableSas, StoredPolicyServiceBlobSas, StoredPolicyServiceContainerSas, StoredPolicyServiceFileSas, StoredPolicyServiceShareSas, StoredPolicyServiceQueueSas, StoredPolicyServiceTableSas
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e618d-150">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e618d-150">-Name</span></span>
<span data-ttu-id="e618d-151">Имя определения SAS хранилища.</span><span class="sxs-lookup"><span data-stu-id="e618d-151">Storage sas definition name.</span></span> <span data-ttu-id="e618d-152">Командлет создает полное доменное имя определения SAS хранилища из имени хранилища, выбранной среды, имени учетной записи хранения и имени определения SAS.</span><span class="sxs-lookup"><span data-stu-id="e618d-152">Cmdlet constructs the FQDN of a storage sas definition from vault name, currently selected environment, storage account name and sas definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SasDefinitionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e618d-153">-Параметр</span><span class="sxs-lookup"><span data-stu-id="e618d-153">-Parameter</span></span>
<span data-ttu-id="e618d-154">Параметры определения SAS, которые будут использоваться для создания маркера SAS.</span><span class="sxs-lookup"><span data-stu-id="e618d-154">Sas definition parameters that will be used to create the sas token.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: RawSas
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e618d-155">-Path</span><span class="sxs-lookup"><span data-stu-id="e618d-155">-Path</span></span>
<span data-ttu-id="e618d-156">Путь к облачному файлу для создания маркера SAS.</span><span class="sxs-lookup"><span data-stu-id="e618d-156">Path to the cloud file to generate sas token against.</span></span>

```yaml
Type: System.String
Parameter Sets: AdhocServiceFileSas, StoredPolicyServiceFileSas
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e618d-157">-Разрешения</span><span class="sxs-lookup"><span data-stu-id="e618d-157">-Permission</span></span>
<span data-ttu-id="e618d-158">PermissionSet.</span><span class="sxs-lookup"><span data-stu-id="e618d-158">Permission.</span></span> <span data-ttu-id="e618d-159">Значения: "запрос", "Добавить", "Обновить", "процесс"</span><span class="sxs-lookup"><span data-stu-id="e618d-159">Values include 'Query','Add','Update','Process'</span></span>

```yaml
Type: System.String[]
Parameter Sets: AdhocAccountSas, AdhocServiceBlobSas, AdhocServiceContainerSas, AdhocServiceFileSas, AdhocServiceShareSas, AdhocServiceQueueSas, AdhocServiceTableSas
Aliases: 
Accepted values: Add, Create, Delete, List, Process, Read, Query, Update, Write

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e618d-160">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="e618d-160">-Policy</span></span>
<span data-ttu-id="e618d-161">Идентификатор политики</span><span class="sxs-lookup"><span data-stu-id="e618d-161">Policy Identifier</span></span>

```yaml
Type: System.String
Parameter Sets: StoredPolicyServiceBlobSas, StoredPolicyServiceContainerSas, StoredPolicyServiceFileSas, StoredPolicyServiceShareSas, StoredPolicyServiceQueueSas, StoredPolicyServiceTableSas
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e618d-162">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="e618d-162">-Protocol</span></span>
<span data-ttu-id="e618d-163">Протокол можно использовать в запросе с маркером SAS.</span><span class="sxs-lookup"><span data-stu-id="e618d-163">Protocol can be used in the request with the SAS token.</span></span>

```yaml
Type: System.String
Parameter Sets: AdhocAccountSas, AdhocServiceBlobSas, AdhocServiceContainerSas, AdhocServiceFileSas, AdhocServiceShareSas, AdhocServiceQueueSas, AdhocServiceTableSas, StoredPolicyServiceBlobSas, StoredPolicyServiceContainerSas, StoredPolicyServiceFileSas, StoredPolicyServiceShareSas, StoredPolicyServiceQueueSas, StoredPolicyServiceTableSas
Aliases: 
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e618d-164">-Очередь</span><span class="sxs-lookup"><span data-stu-id="e618d-164">-Queue</span></span>
<span data-ttu-id="e618d-165">Имя очереди</span><span class="sxs-lookup"><span data-stu-id="e618d-165">Queue Name</span></span>

```yaml
Type: System.String
Parameter Sets: AdhocServiceQueueSas, StoredPolicyServiceQueueSas
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e618d-166">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="e618d-166">-ResourceType</span></span>
<span data-ttu-id="e618d-167">Типы ресурсов, к которым относится этот маркер SAS.</span><span class="sxs-lookup"><span data-stu-id="e618d-167">Resource types that this SAS token applies to.</span></span> <span data-ttu-id="e618d-168">Значения включают "Service", "Container", "Object"</span><span class="sxs-lookup"><span data-stu-id="e618d-168">Values include 'Service','Container','Object'</span></span>

```yaml
Type: System.String[]
Parameter Sets: AdhocAccountSas
Aliases: 
Accepted values: Service, Container, Object

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e618d-169">-Служба</span><span class="sxs-lookup"><span data-stu-id="e618d-169">-Service</span></span>
<span data-ttu-id="e618d-170">Типы служб, к которым применяется этот маркер SAS.</span><span class="sxs-lookup"><span data-stu-id="e618d-170">Service types that this SAS token applies to.</span></span> <span data-ttu-id="e618d-171">Значения включают "BLOB", "файл", "очередь", "Таблица"</span><span class="sxs-lookup"><span data-stu-id="e618d-171">Values include 'Blob','File','Queue','Table'</span></span>

```yaml
Type: System.String[]
Parameter Sets: AdhocAccountSas
Aliases: 
Accepted values: Blob, File, Queue, Table

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e618d-172">-Общий доступ</span><span class="sxs-lookup"><span data-stu-id="e618d-172">-Share</span></span>
<span data-ttu-id="e618d-173">Имя общего доступа</span><span class="sxs-lookup"><span data-stu-id="e618d-173">Share Name</span></span>

```yaml
Type: System.String
Parameter Sets: AdhocServiceFileSas, AdhocServiceShareSas, StoredPolicyServiceFileSas, StoredPolicyServiceShareSas
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e618d-174">-SharedAccessHeader</span><span class="sxs-lookup"><span data-stu-id="e618d-174">-SharedAccessHeader</span></span>
<span data-ttu-id="e618d-175">Задает параметры запроса для переопределения заголовков ответа.</span><span class="sxs-lookup"><span data-stu-id="e618d-175">Specifies the query parameters to override response headers.</span></span>

```yaml
Type: System.String[]
Parameter Sets: AdhocServiceBlobSas, AdhocServiceContainerSas, AdhocServiceFileSas, AdhocServiceShareSas, StoredPolicyServiceBlobSas, StoredPolicyServiceContainerSas, StoredPolicyServiceFileSas, StoredPolicyServiceShareSas
Aliases: 
Accepted values: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentType

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e618d-176">-StartPartitionKey</span><span class="sxs-lookup"><span data-stu-id="e618d-176">-StartPartitionKey</span></span>
<span data-ttu-id="e618d-177">Начало раздела</span><span class="sxs-lookup"><span data-stu-id="e618d-177">Start Partition Key</span></span>

```yaml
Type: System.String
Parameter Sets: AdhocServiceTableSas, StoredPolicyServiceTableSas
Aliases: startpk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e618d-178">-StartRowKey</span><span class="sxs-lookup"><span data-stu-id="e618d-178">-StartRowKey</span></span>
<span data-ttu-id="e618d-179">Клавиша "Пуск строки"</span><span class="sxs-lookup"><span data-stu-id="e618d-179">Start Row Key</span></span>

```yaml
Type: System.String
Parameter Sets: AdhocServiceTableSas, StoredPolicyServiceTableSas
Aliases: startrk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e618d-180">-Таблица</span><span class="sxs-lookup"><span data-stu-id="e618d-180">-Table</span></span>
<span data-ttu-id="e618d-181">Имя таблицы</span><span class="sxs-lookup"><span data-stu-id="e618d-181">Table Name</span></span>

```yaml
Type: System.String
Parameter Sets: AdhocServiceTableSas, StoredPolicyServiceTableSas
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e618d-182">-Тег</span><span class="sxs-lookup"><span data-stu-id="e618d-182">-Tag</span></span>
<span data-ttu-id="e618d-183">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="e618d-183">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="e618d-184">Например:</span><span class="sxs-lookup"><span data-stu-id="e618d-184">For example:</span></span>

<span data-ttu-id="e618d-185">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="e618d-185">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="e618d-186">-TargetStorageVersion</span><span class="sxs-lookup"><span data-stu-id="e618d-186">-TargetStorageVersion</span></span>
<span data-ttu-id="e618d-187">Указывает используемую версию службы хранилища для проверки подлинности запросов, выполненных с маркером SAS.</span><span class="sxs-lookup"><span data-stu-id="e618d-187">Specifies the signed storage service version to use to authenticate requests made with the SAS token.</span></span>

```yaml
Type: System.String
Parameter Sets: AdhocAccountSas, AdhocServiceBlobSas, AdhocServiceContainerSas, AdhocServiceFileSas, AdhocServiceShareSas, AdhocServiceQueueSas, AdhocServiceTableSas, StoredPolicyServiceBlobSas, StoredPolicyServiceContainerSas, StoredPolicyServiceFileSas, StoredPolicyServiceShareSas, StoredPolicyServiceQueueSas, StoredPolicyServiceTableSas
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e618d-188">-ValidityPeriod</span><span class="sxs-lookup"><span data-stu-id="e618d-188">-ValidityPeriod</span></span>
<span data-ttu-id="e618d-189">Срок действия, который будет использоваться для задания срока действия маркера SAS с момента создания.</span><span class="sxs-lookup"><span data-stu-id="e618d-189">Validity period that will get used to set the expiry time of sas token from the time it gets generated</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: AdhocAccountSas, AdhocServiceBlobSas, AdhocServiceContainerSas, AdhocServiceFileSas, AdhocServiceShareSas, AdhocServiceQueueSas, AdhocServiceTableSas
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e618d-190">-VaultName</span><span class="sxs-lookup"><span data-stu-id="e618d-190">-VaultName</span></span>
<span data-ttu-id="e618d-191">Имя хранилища.</span><span class="sxs-lookup"><span data-stu-id="e618d-191">Vault name.</span></span>
<span data-ttu-id="e618d-192">Командлет создает полное доменное имя хранилища на основе имени и выбранной в данный момент среды.</span><span class="sxs-lookup"><span data-stu-id="e618d-192">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="e618d-193">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e618d-193">-WhatIf</span></span>
<span data-ttu-id="e618d-194">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e618d-194">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e618d-195">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e618d-195">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e618d-196">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e618d-196">-DefaultProfile</span></span>
<span data-ttu-id="e618d-197">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e618d-197">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e618d-198">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e618d-198">CommonParameters</span></span>
<span data-ttu-id="e618d-199">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e618d-199">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e618d-200">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e618d-200">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e618d-201">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e618d-201">INPUTS</span></span>

## <span data-ttu-id="e618d-202">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e618d-202">OUTPUTS</span></span>

### <span data-ttu-id="e618d-203">Microsoft. Azure. Commands. KeyVault. Models. ManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="e618d-203">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageSasDefinition</span></span>

## <span data-ttu-id="e618d-204">Пуск</span><span class="sxs-lookup"><span data-stu-id="e618d-204">NOTES</span></span>

## <span data-ttu-id="e618d-205">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e618d-205">RELATED LINKS</span></span>

[<span data-ttu-id="e618d-206">Azureâ € ‹ RM. в € ‹ keyâ € ‹ Vault</span><span class="sxs-lookup"><span data-stu-id="e618d-206">Azureâ€‹RM.â€‹Keyâ€‹Vault</span></span>](/powershell/module/azurerm.keyvault/)

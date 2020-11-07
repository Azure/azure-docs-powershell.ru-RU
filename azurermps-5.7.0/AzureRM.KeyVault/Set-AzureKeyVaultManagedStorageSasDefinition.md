---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultmanagedstoragesasdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultManagedStorageSasDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultManagedStorageSasDefinition.md
ms.openlocfilehash: 5a4c1effd1cbda4399e06f3b6db606cff87d8955
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734707"
---
# <span data-ttu-id="fd191-101">Set-AzureKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="fd191-101">Set-AzureKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="fd191-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fd191-102">SYNOPSIS</span></span>
<span data-ttu-id="fd191-103">Задает определение сигнатуры общего доступа (SAS) с помощью хранилища ключей для указанной учетной записи хранения для хранилища ключей в управляемом хранилище Azure.</span><span class="sxs-lookup"><span data-stu-id="fd191-103">Sets a Shared Access Signature (SAS) definition with Key Vault for a given Key Vault managed Azure Storage Account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fd191-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fd191-104">SYNTAX</span></span>

### <span data-ttu-id="fd191-105">RawSas (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fd191-105">RawSas (Default)</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Parameter] <Hashtable> [-Disable] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd191-106">AdhocAccountSas</span><span class="sxs-lookup"><span data-stu-id="fd191-106">AdhocAccountSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition -Service <String[]> -ResourceType <String[]>
 [-ApiVersion <String>] [-VaultName] <String> [-AccountName] <String> [-Name] <String> [-Disable]
 [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>] [-IPAddressOrRange <String>]
 -ValidityPeriod <TimeSpan> -Permission <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd191-107">AdhocServiceBlobSas</span><span class="sxs-lookup"><span data-stu-id="fd191-107">AdhocServiceBlobSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -ValidityPeriod <TimeSpan> -Permission <String[]> -Blob <String>
 -Container <String> [-SharedAccessHeader <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd191-108">AdhocServiceContainerSas</span><span class="sxs-lookup"><span data-stu-id="fd191-108">AdhocServiceContainerSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -ValidityPeriod <TimeSpan> -Permission <String[]> -Container <String>
 [-SharedAccessHeader <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fd191-109">AdhocServiceFileSas</span><span class="sxs-lookup"><span data-stu-id="fd191-109">AdhocServiceFileSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -ValidityPeriod <TimeSpan> -Permission <String[]>
 [-SharedAccessHeader <String[]>] -Share <String> -Path <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd191-110">AdhocServiceShareSas</span><span class="sxs-lookup"><span data-stu-id="fd191-110">AdhocServiceShareSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -ValidityPeriod <TimeSpan> -Permission <String[]>
 [-SharedAccessHeader <String[]>] -Share <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd191-111">AdhocServiceQueueSas</span><span class="sxs-lookup"><span data-stu-id="fd191-111">AdhocServiceQueueSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -ValidityPeriod <TimeSpan> -Permission <String[]> -Queue <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd191-112">AdhocServiceTableSas</span><span class="sxs-lookup"><span data-stu-id="fd191-112">AdhocServiceTableSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -ValidityPeriod <TimeSpan> -Permission <String[]> -Table <String>
 [-StartPartitionKey <String>] [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd191-113">StoredPolicyServiceBlobSas</span><span class="sxs-lookup"><span data-stu-id="fd191-113">StoredPolicyServiceBlobSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -Blob <String> -Container <String> -Policy <String>
 [-SharedAccessHeader <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fd191-114">StoredPolicyServiceContainerSas</span><span class="sxs-lookup"><span data-stu-id="fd191-114">StoredPolicyServiceContainerSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -Container <String> -Policy <String> [-SharedAccessHeader <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd191-115">StoredPolicyServiceFileSas</span><span class="sxs-lookup"><span data-stu-id="fd191-115">StoredPolicyServiceFileSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -Policy <String> [-SharedAccessHeader <String[]>] -Share <String> -Path <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd191-116">StoredPolicyServiceShareSas</span><span class="sxs-lookup"><span data-stu-id="fd191-116">StoredPolicyServiceShareSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -Policy <String> [-SharedAccessHeader <String[]>] -Share <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd191-117">StoredPolicyServiceQueueSas</span><span class="sxs-lookup"><span data-stu-id="fd191-117">StoredPolicyServiceQueueSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -Policy <String> -Queue <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd191-118">StoredPolicyServiceTableSas</span><span class="sxs-lookup"><span data-stu-id="fd191-118">StoredPolicyServiceTableSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -Policy <String> -Table <String> [-StartPartitionKey <String>]
 [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd191-119">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fd191-119">DESCRIPTION</span></span>
<span data-ttu-id="fd191-120">Задает определение сигнатуры общего доступа (SAS) с учетной записью хранения для управления с помощью данного хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="fd191-120">Sets a Shared Access Signature (SAS) definition with a given Key Vault managed Azure Storage Account.</span></span> <span data-ttu-id="fd191-121">Это также задает секрет, который можно использовать для получения маркера SAS по этому определению SAS.</span><span class="sxs-lookup"><span data-stu-id="fd191-121">This also sets a secret which can be used to get the SAS token per this SAS definition.</span></span>
<span data-ttu-id="fd191-122">Маркер SAS генерируется с использованием этих параметров и активного ключа учетной записи хранения для хранилища ключей в службе хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="fd191-122">SAS token is generated using these parameters and the active key of the Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="fd191-123">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fd191-123">EXAMPLES</span></span>

### <span data-ttu-id="fd191-124">Пример 1: Настройка определения SAS для блоба нерегламентированных служб</span><span class="sxs-lookup"><span data-stu-id="fd191-124">Example 1 : Set an ad hoc service Blob sas definition</span></span>
```
PS C:\> Set-AzureKeyVaultManagedStorageSasDefinition -Blob 'blob1' -Container 'container1' -VaultName 'vault1' -AccountName 'account1' -Name 'sas1' -ValidityPeriod ([System.Timespan]::FromDays(30)) -Permission Read,Add -SharedAccessHeader CacheControl,ContentDisposition -Protocol HttpsOnly -IPAddressOrRange '168.1.5.60-168.1.5.70'
```

<span data-ttu-id="fd191-125">Задает определение сопоставления безопасности BLOB-объектов ad hoc ("sas1") с управляемой учетной записью хранения для хранилища ключей "компьютера1" в хранилище "vault1".</span><span class="sxs-lookup"><span data-stu-id="fd191-125">Sets an ad hoc service blob sas definition 'sas1' with key vault managed storage account 'account1' in vault 'vault1'.</span></span>

### <span data-ttu-id="fd191-126">Пример 2: Настройка определения SAS для учетной записи ad hoc</span><span class="sxs-lookup"><span data-stu-id="fd191-126">Example 2 : Set an ad hoc account sas definition</span></span>
```
PS C:\> Set-AzureKeyVaultManagedStorageSasDefinition -Service Blob,File -ResourceType Container,Service -VaultName 'vault1' -AccountName 'account1' -Name 'sas1' -Protocol HttpsOrHttp -IPAddressOrRange '168.1.5.60' -ValidityPeriod ([System.Timespan]::FromDays(30)) -Permission Read,Add
```

<span data-ttu-id="fd191-127">Задает ad hoc определение SAS "sas1" с управляемой учетной записью хранения для хранилища ключей "компьютера1" в хранилище "vault1".</span><span class="sxs-lookup"><span data-stu-id="fd191-127">Sets an ad hoc blob sas definition 'sas1' with key vault managed storage account 'account1' in vault 'vault1'.</span></span>

### <span data-ttu-id="fd191-128">Пример 3: Настройка определения SAS с помощью хэш-таблицы</span><span class="sxs-lookup"><span data-stu-id="fd191-128">Example 3 : Set a sas definition using a hashtable</span></span>
```
PS C:\> $parameters = @{"sasType"="blob";"signedVersion"="2016-05-31";"signedProtocols"="https";"signedIp"="168.1.5.60-168.1.5.70";"validityPeriod"="P30D";"signedPermissions"="ra";"blobName"="blob1";"containerName"="container1";"rscd"="";"rscc"=""}
PS C:\> Set-AzureKeyVaultManagedStorageSasDefinition -VaultName vault1 -AccountName account1 -Name sas1 -Parameter $parameters
```

<span data-ttu-id="fd191-129">Задает для ad hoc определение SAS "sas1" с управляемой учетной записью хранения для хранилища ключей "компьютера1" в хранилище "vault1" с помощью Hashtable.</span><span class="sxs-lookup"><span data-stu-id="fd191-129">Sets an ad hoc blob sas definition 'sas1' with key vault managed storage account 'account1' in vault 'vault1' using a hashtable.</span></span>

## <span data-ttu-id="fd191-130">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fd191-130">PARAMETERS</span></span>

### <span data-ttu-id="fd191-131">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="fd191-131">-AccountName</span></span>
<span data-ttu-id="fd191-132">Имя учетной записи хранилища с управляемым хранилищем.</span><span class="sxs-lookup"><span data-stu-id="fd191-132">Key Vault managed storage account name.</span></span> <span data-ttu-id="fd191-133">Командлет создает полное доменное имя управляемой учетной записи хранения из имени хранилища, выбранной в данный момент среды и управляемого имени учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="fd191-133">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd191-134">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="fd191-134">-ApiVersion</span></span>
<span data-ttu-id="fd191-135">Указывает версию службы хранилища, используемую для выполнения запроса, созданного с помощью URI SAS учетной записи.</span><span class="sxs-lookup"><span data-stu-id="fd191-135">Specifies the storage service version to use to execute the request made using the account SAS URI.</span></span>

```yaml
Type: String
Parameter Sets: AdhocAccountSas
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd191-136">-BLOB</span><span class="sxs-lookup"><span data-stu-id="fd191-136">-Blob</span></span>
<span data-ttu-id="fd191-137">Имя BLOB-объекта</span><span class="sxs-lookup"><span data-stu-id="fd191-137">Blob Name</span></span>

```yaml
Type: String
Parameter Sets: AdhocServiceBlobSas, StoredPolicyServiceBlobSas
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd191-138">-Container</span><span class="sxs-lookup"><span data-stu-id="fd191-138">-Container</span></span>
<span data-ttu-id="fd191-139">Имя контейнера</span><span class="sxs-lookup"><span data-stu-id="fd191-139">Container Name</span></span>

```yaml
Type: String
Parameter Sets: AdhocServiceBlobSas, AdhocServiceContainerSas, StoredPolicyServiceBlobSas, StoredPolicyServiceContainerSas
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd191-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd191-140">-DefaultProfile</span></span>
<span data-ttu-id="fd191-141">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="fd191-141">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fd191-142">-Отключение</span><span class="sxs-lookup"><span data-stu-id="fd191-142">-Disable</span></span>
<span data-ttu-id="fd191-143">Отключение использования определения SAS для создания маркера SAS.</span><span class="sxs-lookup"><span data-stu-id="fd191-143">Disables the use of sas definition for generation of sas token.</span></span>

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

### <span data-ttu-id="fd191-144">-EndPartitionKey</span><span class="sxs-lookup"><span data-stu-id="fd191-144">-EndPartitionKey</span></span>
<span data-ttu-id="fd191-145">Клавиша End Partition</span><span class="sxs-lookup"><span data-stu-id="fd191-145">End Partition Key</span></span>

```yaml
Type: String
Parameter Sets: AdhocServiceTableSas, StoredPolicyServiceTableSas
Aliases: endpk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd191-146">-EndRowKey</span><span class="sxs-lookup"><span data-stu-id="fd191-146">-EndRowKey</span></span>
<span data-ttu-id="fd191-147">Клавиша "конец строки"</span><span class="sxs-lookup"><span data-stu-id="fd191-147">End Row Key</span></span>

```yaml
Type: String
Parameter Sets: AdhocServiceTableSas, StoredPolicyServiceTableSas
Aliases: endrk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd191-148">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="fd191-148">-IPAddressOrRange</span></span>
<span data-ttu-id="fd191-149">IP-адрес или ACL диапазона IP-адресов (список управления доступом) для запроса, который будет принят службой хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="fd191-149">IP, or IP range ACL (access control list) of the request that would be accepted by Azure Storage.</span></span>

```yaml
Type: String
Parameter Sets: AdhocAccountSas, AdhocServiceBlobSas, AdhocServiceContainerSas, AdhocServiceFileSas, AdhocServiceShareSas, AdhocServiceQueueSas, AdhocServiceTableSas, StoredPolicyServiceBlobSas, StoredPolicyServiceContainerSas, StoredPolicyServiceFileSas, StoredPolicyServiceShareSas, StoredPolicyServiceQueueSas, StoredPolicyServiceTableSas
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd191-150">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="fd191-150">-Name</span></span>
<span data-ttu-id="fd191-151">Имя определения SAS хранилища.</span><span class="sxs-lookup"><span data-stu-id="fd191-151">Storage sas definition name.</span></span> <span data-ttu-id="fd191-152">Командлет создает полное доменное имя определения SAS хранилища из имени хранилища, выбранной среды, имени учетной записи хранения и имени определения SAS.</span><span class="sxs-lookup"><span data-stu-id="fd191-152">Cmdlet constructs the FQDN of a storage sas definition from vault name, currently selected environment, storage account name and sas definition name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SasDefinitionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd191-153">-Параметр</span><span class="sxs-lookup"><span data-stu-id="fd191-153">-Parameter</span></span>
<span data-ttu-id="fd191-154">Параметры определения SAS, которые будут использоваться для создания маркера SAS.</span><span class="sxs-lookup"><span data-stu-id="fd191-154">Sas definition parameters that will be used to create the sas token.</span></span>

```yaml
Type: Hashtable
Parameter Sets: RawSas
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd191-155">-Path</span><span class="sxs-lookup"><span data-stu-id="fd191-155">-Path</span></span>
<span data-ttu-id="fd191-156">Путь к облачному файлу для создания маркера SAS.</span><span class="sxs-lookup"><span data-stu-id="fd191-156">Path to the cloud file to generate sas token against.</span></span>

```yaml
Type: String
Parameter Sets: AdhocServiceFileSas, StoredPolicyServiceFileSas
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd191-157">-Разрешения</span><span class="sxs-lookup"><span data-stu-id="fd191-157">-Permission</span></span>
<span data-ttu-id="fd191-158">PermissionSet.</span><span class="sxs-lookup"><span data-stu-id="fd191-158">Permission.</span></span> <span data-ttu-id="fd191-159">Значения: "запрос", "Добавить", "Обновить", "процесс"</span><span class="sxs-lookup"><span data-stu-id="fd191-159">Values include 'Query','Add','Update','Process'</span></span>

```yaml
Type: String[]
Parameter Sets: AdhocAccountSas, AdhocServiceBlobSas, AdhocServiceContainerSas, AdhocServiceFileSas, AdhocServiceShareSas, AdhocServiceQueueSas, AdhocServiceTableSas
Aliases:
Accepted values: Add, Create, Delete, List, Process, Read, Query, Update, Write

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd191-160">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="fd191-160">-Policy</span></span>
<span data-ttu-id="fd191-161">Идентификатор политики</span><span class="sxs-lookup"><span data-stu-id="fd191-161">Policy Identifier</span></span>

```yaml
Type: String
Parameter Sets: StoredPolicyServiceBlobSas, StoredPolicyServiceContainerSas, StoredPolicyServiceFileSas, StoredPolicyServiceShareSas, StoredPolicyServiceQueueSas, StoredPolicyServiceTableSas
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd191-162">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="fd191-162">-Protocol</span></span>
<span data-ttu-id="fd191-163">Протокол можно использовать в запросе с маркером SAS.</span><span class="sxs-lookup"><span data-stu-id="fd191-163">Protocol can be used in the request with the SAS token.</span></span>

```yaml
Type: String
Parameter Sets: AdhocAccountSas, AdhocServiceBlobSas, AdhocServiceContainerSas, AdhocServiceFileSas, AdhocServiceShareSas, AdhocServiceQueueSas, AdhocServiceTableSas, StoredPolicyServiceBlobSas, StoredPolicyServiceContainerSas, StoredPolicyServiceFileSas, StoredPolicyServiceShareSas, StoredPolicyServiceQueueSas, StoredPolicyServiceTableSas
Aliases:
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd191-164">-Очередь</span><span class="sxs-lookup"><span data-stu-id="fd191-164">-Queue</span></span>
<span data-ttu-id="fd191-165">Имя очереди</span><span class="sxs-lookup"><span data-stu-id="fd191-165">Queue Name</span></span>

```yaml
Type: String
Parameter Sets: AdhocServiceQueueSas, StoredPolicyServiceQueueSas
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd191-166">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="fd191-166">-ResourceType</span></span>
<span data-ttu-id="fd191-167">Типы ресурсов, к которым относится этот маркер SAS.</span><span class="sxs-lookup"><span data-stu-id="fd191-167">Resource types that this SAS token applies to.</span></span> <span data-ttu-id="fd191-168">Значения включают "Service", "Container", "Object"</span><span class="sxs-lookup"><span data-stu-id="fd191-168">Values include 'Service','Container','Object'</span></span>

```yaml
Type: String[]
Parameter Sets: AdhocAccountSas
Aliases:
Accepted values: Service, Container, Object

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd191-169">-Служба</span><span class="sxs-lookup"><span data-stu-id="fd191-169">-Service</span></span>
<span data-ttu-id="fd191-170">Типы служб, к которым применяется этот маркер SAS.</span><span class="sxs-lookup"><span data-stu-id="fd191-170">Service types that this SAS token applies to.</span></span> <span data-ttu-id="fd191-171">Значения включают "BLOB", "файл", "очередь", "Таблица"</span><span class="sxs-lookup"><span data-stu-id="fd191-171">Values include 'Blob','File','Queue','Table'</span></span>

```yaml
Type: String[]
Parameter Sets: AdhocAccountSas
Aliases:
Accepted values: Blob, File, Queue, Table

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd191-172">-Общий доступ</span><span class="sxs-lookup"><span data-stu-id="fd191-172">-Share</span></span>
<span data-ttu-id="fd191-173">Имя общего доступа</span><span class="sxs-lookup"><span data-stu-id="fd191-173">Share Name</span></span>

```yaml
Type: String
Parameter Sets: AdhocServiceFileSas, AdhocServiceShareSas, StoredPolicyServiceFileSas, StoredPolicyServiceShareSas
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd191-174">-SharedAccessHeader</span><span class="sxs-lookup"><span data-stu-id="fd191-174">-SharedAccessHeader</span></span>
<span data-ttu-id="fd191-175">Задает параметры запроса для переопределения заголовков ответа.</span><span class="sxs-lookup"><span data-stu-id="fd191-175">Specifies the query parameters to override response headers.</span></span>

```yaml
Type: String[]
Parameter Sets: AdhocServiceBlobSas, AdhocServiceContainerSas, AdhocServiceFileSas, AdhocServiceShareSas, StoredPolicyServiceBlobSas, StoredPolicyServiceContainerSas, StoredPolicyServiceFileSas, StoredPolicyServiceShareSas
Aliases:
Accepted values: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentType

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd191-176">-StartPartitionKey</span><span class="sxs-lookup"><span data-stu-id="fd191-176">-StartPartitionKey</span></span>
<span data-ttu-id="fd191-177">Начало раздела</span><span class="sxs-lookup"><span data-stu-id="fd191-177">Start Partition Key</span></span>

```yaml
Type: String
Parameter Sets: AdhocServiceTableSas, StoredPolicyServiceTableSas
Aliases: startpk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd191-178">-StartRowKey</span><span class="sxs-lookup"><span data-stu-id="fd191-178">-StartRowKey</span></span>
<span data-ttu-id="fd191-179">Клавиша "Пуск строки"</span><span class="sxs-lookup"><span data-stu-id="fd191-179">Start Row Key</span></span>

```yaml
Type: String
Parameter Sets: AdhocServiceTableSas, StoredPolicyServiceTableSas
Aliases: startrk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd191-180">-Таблица</span><span class="sxs-lookup"><span data-stu-id="fd191-180">-Table</span></span>
<span data-ttu-id="fd191-181">Имя таблицы</span><span class="sxs-lookup"><span data-stu-id="fd191-181">Table Name</span></span>

```yaml
Type: String
Parameter Sets: AdhocServiceTableSas, StoredPolicyServiceTableSas
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd191-182">-Тег</span><span class="sxs-lookup"><span data-stu-id="fd191-182">-Tag</span></span>
<span data-ttu-id="fd191-183">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="fd191-183">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="fd191-184">Например:</span><span class="sxs-lookup"><span data-stu-id="fd191-184">For example:</span></span>

<span data-ttu-id="fd191-185">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="fd191-185">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="fd191-186">-TargetStorageVersion</span><span class="sxs-lookup"><span data-stu-id="fd191-186">-TargetStorageVersion</span></span>
<span data-ttu-id="fd191-187">Указывает используемую версию службы хранилища для проверки подлинности запросов, выполненных с маркером SAS.</span><span class="sxs-lookup"><span data-stu-id="fd191-187">Specifies the signed storage service version to use to authenticate requests made with the SAS token.</span></span>

```yaml
Type: String
Parameter Sets: AdhocAccountSas, AdhocServiceBlobSas, AdhocServiceContainerSas, AdhocServiceFileSas, AdhocServiceShareSas, AdhocServiceQueueSas, AdhocServiceTableSas, StoredPolicyServiceBlobSas, StoredPolicyServiceContainerSas, StoredPolicyServiceFileSas, StoredPolicyServiceShareSas, StoredPolicyServiceQueueSas, StoredPolicyServiceTableSas
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd191-188">-ValidityPeriod</span><span class="sxs-lookup"><span data-stu-id="fd191-188">-ValidityPeriod</span></span>
<span data-ttu-id="fd191-189">Срок действия, который будет использоваться для задания срока действия маркера SAS с момента создания.</span><span class="sxs-lookup"><span data-stu-id="fd191-189">Validity period that will get used to set the expiry time of sas token from the time it gets generated</span></span>

```yaml
Type: TimeSpan
Parameter Sets: AdhocAccountSas, AdhocServiceBlobSas, AdhocServiceContainerSas, AdhocServiceFileSas, AdhocServiceShareSas, AdhocServiceQueueSas, AdhocServiceTableSas
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd191-190">-VaultName</span><span class="sxs-lookup"><span data-stu-id="fd191-190">-VaultName</span></span>
<span data-ttu-id="fd191-191">Имя хранилища.</span><span class="sxs-lookup"><span data-stu-id="fd191-191">Vault name.</span></span>
<span data-ttu-id="fd191-192">Командлет создает полное доменное имя хранилища на основе имени и выбранной в данный момент среды.</span><span class="sxs-lookup"><span data-stu-id="fd191-192">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="fd191-193">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fd191-193">-Confirm</span></span>
<span data-ttu-id="fd191-194">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="fd191-194">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd191-195">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd191-195">-WhatIf</span></span>
<span data-ttu-id="fd191-196">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="fd191-196">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd191-197">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="fd191-197">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd191-198">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd191-198">CommonParameters</span></span>
<span data-ttu-id="fd191-199">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fd191-199">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd191-200">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd191-200">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd191-201">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fd191-201">INPUTS</span></span>

### <span data-ttu-id="fd191-202">Ничего</span><span class="sxs-lookup"><span data-stu-id="fd191-202">None</span></span>
<span data-ttu-id="fd191-203">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="fd191-203">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fd191-204">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fd191-204">OUTPUTS</span></span>

### <span data-ttu-id="fd191-205">Microsoft. Azure. Commands. KeyVault. Models. ManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="fd191-205">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageSasDefinition</span></span>

## <span data-ttu-id="fd191-206">Пуск</span><span class="sxs-lookup"><span data-stu-id="fd191-206">NOTES</span></span>

## <span data-ttu-id="fd191-207">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fd191-207">RELATED LINKS</span></span>

[<span data-ttu-id="fd191-208">Azureâ € ‹ RM. в € ‹ keyâ € ‹ Vault</span><span class="sxs-lookup"><span data-stu-id="fd191-208">Azureâ€‹RM.â€‹Keyâ€‹Vault</span></span>](/powershell/module/azurerm.keyvault/)

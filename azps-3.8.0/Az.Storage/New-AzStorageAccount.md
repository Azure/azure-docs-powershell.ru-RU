---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A3DA1205-B8FB-4B4C-9C40-AD303D038EDF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
ms.openlocfilehash: c88e56a485f9e42daf229667ab4c07d7a7464578
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073146"
---
# <span data-ttu-id="c3c7d-101">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c3c7d-101">New-AzStorageAccount</span></span>

## <span data-ttu-id="c3c7d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c3c7d-102">SYNOPSIS</span></span>
<span data-ttu-id="c3c7d-103">Создание учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="c3c7d-103">Creates a Storage account.</span></span>

## <span data-ttu-id="c3c7d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c3c7d-104">SYNTAX</span></span>

```
New-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Location] <String>
 [-Kind <String>] [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>]
 [-Tag <Hashtable>] [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-EnableHierarchicalNamespace <Boolean>] [-EnableAzureActiveDirectoryDomainServicesForFile <Boolean>]
 [-EnableLargeFileShare] [-AsJob] [-EncryptionKeyTypeForTable <String>] [-EncryptionKeyTypeForQueue <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c3c7d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c3c7d-105">DESCRIPTION</span></span>
<span data-ttu-id="c3c7d-106">Командлет **New-AzStorageAccount** создает учетную запись хранения Azure.</span><span class="sxs-lookup"><span data-stu-id="c3c7d-106">The **New-AzStorageAccount** cmdlet creates an Azure Storage account.</span></span>

## <span data-ttu-id="c3c7d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c3c7d-107">EXAMPLES</span></span>

### <span data-ttu-id="c3c7d-108">Пример 1: создание учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="c3c7d-108">Example 1: Create a Storage account</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS
```

<span data-ttu-id="c3c7d-109">Эта команда создает учетную запись хранения для имени группы ресурсов MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="c3c7d-109">This command creates a Storage account for the resource group name MyResourceGroup.</span></span>

### <span data-ttu-id="c3c7d-110">Пример 2: создание учетной записи хранения BLOB-данных с BlobStorageным и горячим AccessTier</span><span class="sxs-lookup"><span data-stu-id="c3c7d-110">Example 2: Create a Blob Storage account with BlobStorage Kind and hot AccessTier</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind BlobStorage -AccessTier Hot
```

<span data-ttu-id="c3c7d-111">Эта команда создает учетную запись хранилища BLOB-объектов, которая имеет BlobStorage и горячий AccessTier</span><span class="sxs-lookup"><span data-stu-id="c3c7d-111">This command creates a Blob Storage account that with BlobStorage Kind and hot AccessTier</span></span>

### <span data-ttu-id="c3c7d-112">Пример 3: создание учетной записи хранения с помощью StorageV2, создание и назначение удостоверения для Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="c3c7d-112">Example 3: Create a Storage account with Kind StorageV2, and Generate and Assign an Identity for Azure KeyVault.</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind StorageV2 -AssignIdentity
```

<span data-ttu-id="c3c7d-113">Эта команда создает учетную запись хранения с StorageV2.</span><span class="sxs-lookup"><span data-stu-id="c3c7d-113">This command creates a Storage account with Kind StorageV2.</span></span>  <span data-ttu-id="c3c7d-114">Кроме того, она генерирует и назначает удостоверение, которое можно использовать для управления ключами учетной записи через Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="c3c7d-114">It also generates and assigns an identity that can be used to manage account keys through Azure KeyVault.</span></span>

### <span data-ttu-id="c3c7d-115">Пример 4: создание учетной записи хранения с помощью NetworkRuleSet из JSON</span><span class="sxs-lookup"><span data-stu-id="c3c7d-115">Example 4: Create a Storage account with NetworkRuleSet from JSON</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -Type Standard_LRS -NetworkRuleSet (@{bypass="Logging,Metrics";
    ipRules=(@{IPAddressOrRange="20.11.0.0/16";Action="allow"},
            @{IPAddressOrRange="10.0.0.0/7";Action="allow"});
    virtualNetworkRules=(@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},
                        @{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2";Action="allow"});
    defaultAction="Deny"})
```

<span data-ttu-id="c3c7d-116">Эта команда создает учетную запись хранения, которая имеет свойство NetworkRuleSet из JSON.</span><span class="sxs-lookup"><span data-stu-id="c3c7d-116">This command creates a Storage account that has NetworkRuleSet property from JSON</span></span>

### <span data-ttu-id="c3c7d-117">Пример 5: создание учетной записи хранения с включенным иерархическое пространством имен.</span><span class="sxs-lookup"><span data-stu-id="c3c7d-117">Example 5: Create a Storage account with Hierarchical Namespace enabled.</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "US West" -SkuName "Standard_GRS" -Kind StorageV2  -EnableHierarchicalNamespace $true
```

<span data-ttu-id="c3c7d-118">Эта команда создает учетную запись хранения, для которой включено иерархическое пространство имен.</span><span class="sxs-lookup"><span data-stu-id="c3c7d-118">This command creates a Storage account with Hierarchical Namespace enabled.</span></span>

### <span data-ttu-id="c3c7d-119">Пример 6: создание учетной записи хранения для файлов Azure проверка подлинности в DS и включение больших файловых ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c3c7d-119">Example 6: Create a Storage account with Azure Files AAD DS Authentication, and enable large file share.</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EnableAzureActiveDirectoryDomainServicesForFile $true -EnableLargeFileShare
```

<span data-ttu-id="c3c7d-120">Эта команда создает учетную запись хранения с помощью Azure Files Authentication DS и включает большие общие файлы..</span><span class="sxs-lookup"><span data-stu-id="c3c7d-120">This command creates a Storage account with Azure Files AAD DS Authentication, and enable large file share..</span></span>

### <span data-ttu-id="c3c7d-121">Пример 8. Создание учетной записи хранения с помощью очереди и службы таблиц. Используйте ключ шифрования для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="c3c7d-121">Example 8: Create a Storage account with Queue and Table Service use account-scoped encryption key.</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EncryptionKeyTypeForTable Account -EncryptionKeyTypeForQueue Account

PS C:\>$account = get-AzStorageAccount -ResourceGroupName $rgname -StorageAccountName $accountName

PS C:\>$account.Encryption.Services.Queue

Enabled LastEnabledTime     KeyType
------- ---------------     -------
   True 1/9/2020 6:09:11 AM Account

PS C:\>$account.Encryption.Services.Table

Enabled LastEnabledTime     KeyType
------- ---------------     -------
   True 1/9/2020 6:09:11 AM Account
```

<span data-ttu-id="c3c7d-122">Эта команда создает учетную запись хранилища, в которой служба очереди и таблица использует ключ шифрования для учетной записи, поэтому очередь и таблица будут использовать один и тот же ключ шифрования с BLOB-объектом и службой файлов.</span><span class="sxs-lookup"><span data-stu-id="c3c7d-122">This command creates a Storage account with Queue and Table Service use account-scoped encryption key, so Queue and Table will use same encryption key with Blob and File service.</span></span> <span data-ttu-id="c3c7d-123">Затем получите доступ к свойствам учетной записи хранения и просмотрите набор шифрования для службы очереди и таблицы.</span><span class="sxs-lookup"><span data-stu-id="c3c7d-123">Then get the Storage account properties, and view the encryption keytype of Queue and Table Service.</span></span>

## <span data-ttu-id="c3c7d-124">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c3c7d-124">PARAMETERS</span></span>

### <span data-ttu-id="c3c7d-125">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="c3c7d-125">-AccessTier</span></span>
<span data-ttu-id="c3c7d-126">Указывает уровень доступа учетной записи хранения, созданной этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="c3c7d-126">Specifies the access tier of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="c3c7d-127">Допустимые значения этого параметра: горячий и крутой.</span><span class="sxs-lookup"><span data-stu-id="c3c7d-127">The acceptable values for this parameter are: Hot and Cool.</span></span>
<span data-ttu-id="c3c7d-128">Если указать значение BlobStorage для параметра *вида* , необходимо указать значение параметра *AccessTier* .</span><span class="sxs-lookup"><span data-stu-id="c3c7d-128">If you specify a value of BlobStorage for the *Kind* parameter, you must specify a value for the *AccessTier* parameter.</span></span> <span data-ttu-id="c3c7d-129">Если для этого параметра *типа* задано значение хранилища, не указывайте параметр *AccessTier* .</span><span class="sxs-lookup"><span data-stu-id="c3c7d-129">If you specify a value of Storage for this *Kind* parameter, do not specify the *AccessTier* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Hot, Cool

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3c7d-130">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c3c7d-130">-AsJob</span></span>
<span data-ttu-id="c3c7d-131">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="c3c7d-131">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c3c7d-132">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="c3c7d-132">-AssignIdentity</span></span>
<span data-ttu-id="c3c7d-133">Создание и назначение нового удостоверения учетной записи хранения для этой учетной записи хранения для использования со службами управления ключами, такими как Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="c3c7d-133">Generate and assign a new Storage account Identity for this Storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="c3c7d-134">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="c3c7d-134">-CustomDomainName</span></span>
<span data-ttu-id="c3c7d-135">Указывает имя настраиваемого домена учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="c3c7d-135">Specifies the name of the custom domain of the Storage account.</span></span>
<span data-ttu-id="c3c7d-136">По умолчанию используется значение Storage.</span><span class="sxs-lookup"><span data-stu-id="c3c7d-136">The default value is Storage.</span></span>

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

### <span data-ttu-id="c3c7d-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3c7d-137">-DefaultProfile</span></span>
<span data-ttu-id="c3c7d-138">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c3c7d-138">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3c7d-139">-EnableAzureActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="c3c7d-139">-EnableAzureActiveDirectoryDomainServicesForFile</span></span>
<span data-ttu-id="c3c7d-140">Включите проверку подлинности доменных служб Azure Active Directory для учетной записи хранения в Azure Files.</span><span class="sxs-lookup"><span data-stu-id="c3c7d-140">Enable Azure Files Azure Active Directory Domain Service Authentication for the storage account.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3c7d-141">-EnableHierarchicalNamespace</span><span class="sxs-lookup"><span data-stu-id="c3c7d-141">-EnableHierarchicalNamespace</span></span>
<span data-ttu-id="c3c7d-142">Указывает, включено ли в учетной записи хранения иерархическое пространство имен.</span><span class="sxs-lookup"><span data-stu-id="c3c7d-142">Indicates whether or not the Storage account enables Hierarchical Namespace.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3c7d-143">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="c3c7d-143">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="c3c7d-144">Указывает, разрешено ли учетной записи хранения только трафик HTTPS.</span><span class="sxs-lookup"><span data-stu-id="c3c7d-144">Indicates whether or not the Storage account only enables HTTPS traffic.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3c7d-145">-EnableLargeFileShare</span><span class="sxs-lookup"><span data-stu-id="c3c7d-145">-EnableLargeFileShare</span></span>
<span data-ttu-id="c3c7d-146">Указывает, может ли учетная запись хранения поддерживать большие файловые ресурсы размером более 5 TiB.</span><span class="sxs-lookup"><span data-stu-id="c3c7d-146">Indicates whether or not the storage account can support large file shares with more than 5 TiB capacity.</span></span> <span data-ttu-id="c3c7d-147">После включения учетной записи эту функцию нельзя отключить.</span><span class="sxs-lookup"><span data-stu-id="c3c7d-147">Once the account is enabled, the feature cannot be disabled.</span></span> <span data-ttu-id="c3c7d-148">В настоящее время поддерживается только для типов репликации LRS и ZRS, поэтому преобразование учетной записи в геоизбыточные учетные записи будет невозможно.</span><span class="sxs-lookup"><span data-stu-id="c3c7d-148">Currently only supported for LRS and ZRS replication types, hence account conversions to geo-redundant accounts would not be possible.</span></span> <span data-ttu-id="c3c7d-149">Дополнительные сведения https://go.microsoft.com/fwlink/?linkid=2086047</span><span class="sxs-lookup"><span data-stu-id="c3c7d-149">Learn more in https://go.microsoft.com/fwlink/?linkid=2086047</span></span>

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

### <span data-ttu-id="c3c7d-150">-EncryptionKeyTypeForQueue</span><span class="sxs-lookup"><span data-stu-id="c3c7d-150">-EncryptionKeyTypeForQueue</span></span>
<span data-ttu-id="c3c7d-151">Установка KeyType для шифрования в очереди.</span><span class="sxs-lookup"><span data-stu-id="c3c7d-151">Set the Encryption KeyType for Queue.</span></span> <span data-ttu-id="c3c7d-152">По умолчанию используется значение Service.</span><span class="sxs-lookup"><span data-stu-id="c3c7d-152">The default value is Service.</span></span>
<span data-ttu-id="c3c7d-153">-Account: очередь будет зашифрована с использованием ключа шифрования с областью действия для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="c3c7d-153">-Account: Queue will be encrypted with account-scoped encryption key.</span></span> <span data-ttu-id="c3c7d-154">-Service: очередь всегда будет шифроваться с помощью Service-Managed клавиш.</span><span class="sxs-lookup"><span data-stu-id="c3c7d-154">-Service: Queue will always be encrypted with Service-Managed keys.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Service, Account

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3c7d-155">-EncryptionKeyTypeForTable</span><span class="sxs-lookup"><span data-stu-id="c3c7d-155">-EncryptionKeyTypeForTable</span></span>
<span data-ttu-id="c3c7d-156">Задайте для свойства KeyType для таблицы ключ шифрования.</span><span class="sxs-lookup"><span data-stu-id="c3c7d-156">Set the Encryption KeyType for Table.</span></span> <span data-ttu-id="c3c7d-157">По умолчанию используется значение Service.</span><span class="sxs-lookup"><span data-stu-id="c3c7d-157">The default value is Service.</span></span>
- <span data-ttu-id="c3c7d-158">Учетная запись: таблица будет зашифрована с использованием ключа шифрования уровня учетной записи.</span><span class="sxs-lookup"><span data-stu-id="c3c7d-158">Account: Table will be encrypted with account-scoped encryption key.</span></span> 
- <span data-ttu-id="c3c7d-159">Служба: таблица всегда будет шифроваться с помощью Service-Managed клавиш.</span><span class="sxs-lookup"><span data-stu-id="c3c7d-159">Service: Table will always be encrypted with Service-Managed keys.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Service, Account

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3c7d-160">-Видах</span><span class="sxs-lookup"><span data-stu-id="c3c7d-160">-Kind</span></span>
<span data-ttu-id="c3c7d-161">Указывает вариант учетной записи хранения, создаваемой этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="c3c7d-161">Specifies the kind of Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="c3c7d-162">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="c3c7d-162">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c3c7d-163">Склад.</span><span class="sxs-lookup"><span data-stu-id="c3c7d-163">Storage.</span></span> <span data-ttu-id="c3c7d-164">Общая цель учетной записи хранения, которая поддерживает хранение больших двоичных объектов, таблиц, очередей, файлов и дисков.</span><span class="sxs-lookup"><span data-stu-id="c3c7d-164">General purpose Storage account that supports storage of Blobs, Tables, Queues, Files and Disks.</span></span>
- <span data-ttu-id="c3c7d-165">StorageV2.</span><span class="sxs-lookup"><span data-stu-id="c3c7d-165">StorageV2.</span></span> <span data-ttu-id="c3c7d-166">Учетная запись хранения общего назначения версии 2 (GPv2), поддерживающая большие двоичные объекты, таблицы, очереди, файлы и диски, с дополнительными возможностями, такими как уровни данных.</span><span class="sxs-lookup"><span data-stu-id="c3c7d-166">General Purpose Version 2 (GPv2) Storage account that supports Blobs, Tables, Queues, Files, and Disks, with advanced features like data tiering.</span></span>
- <span data-ttu-id="c3c7d-167">BlobStorage.</span><span class="sxs-lookup"><span data-stu-id="c3c7d-167">BlobStorage.</span></span> <span data-ttu-id="c3c7d-168">Учетная запись хранилища BLOB-объектов, поддерживающая только хранение больших двоичных объектов.</span><span class="sxs-lookup"><span data-stu-id="c3c7d-168">Blob Storage account which supports storage of Blobs only.</span></span>
- <span data-ttu-id="c3c7d-169">BlockBlobStorage.</span><span class="sxs-lookup"><span data-stu-id="c3c7d-169">BlockBlobStorage.</span></span> <span data-ttu-id="c3c7d-170">Блокировка учетной записи хранения BLOB-объектов, которая поддерживает хранение блочных больших двоичных объектов.</span><span class="sxs-lookup"><span data-stu-id="c3c7d-170">Block Blob Storage account which supports storage of Block Blobs only.</span></span>
- <span data-ttu-id="c3c7d-171">FileStorage.</span><span class="sxs-lookup"><span data-stu-id="c3c7d-171">FileStorage.</span></span> <span data-ttu-id="c3c7d-172">Учетная запись хранилища файлов, поддерживающая хранение только файлов.</span><span class="sxs-lookup"><span data-stu-id="c3c7d-172">File Storage account which supports storage of Files only.</span></span>
<span data-ttu-id="c3c7d-173">Значением по умолчанию является StorageV2.</span><span class="sxs-lookup"><span data-stu-id="c3c7d-173">The default value is StorageV2.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Storage, StorageV2, BlobStorage, BlockBlobStorage, FileStorage

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3c7d-174">-Location</span><span class="sxs-lookup"><span data-stu-id="c3c7d-174">-Location</span></span>
<span data-ttu-id="c3c7d-175">Указывает расположение учетной записи хранения, которую нужно создать.</span><span class="sxs-lookup"><span data-stu-id="c3c7d-175">Specifies the location of the Storage account to create.</span></span>

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

### <span data-ttu-id="c3c7d-176">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c3c7d-176">-Name</span></span>
<span data-ttu-id="c3c7d-177">Указывает имя учетной записи хранения, которую нужно создать.</span><span class="sxs-lookup"><span data-stu-id="c3c7d-177">Specifies the name of the Storage account to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3c7d-178">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="c3c7d-178">-NetworkRuleSet</span></span>
<span data-ttu-id="c3c7d-179">NetworkRuleSet используется для определения набора правил конфигурации для брандмауэров и виртуальных сетей, а также для задания значений свойств сети, таких как службы, которые могут обойти правила и обрабатывать запросы, не соответствующие ни одному из заданных правил.</span><span class="sxs-lookup"><span data-stu-id="c3c7d-179">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as services allowed to bypass the rules and how to handle requests that don't match any of the defined rules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3c7d-180">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3c7d-180">-ResourceGroupName</span></span>
<span data-ttu-id="c3c7d-181">Указывает имя группы ресурсов, в которую нужно добавить учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="c3c7d-181">Specifies the name of the resource group in which to add the Storage account.</span></span>

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

### <span data-ttu-id="c3c7d-182">-SkuName</span><span class="sxs-lookup"><span data-stu-id="c3c7d-182">-SkuName</span></span>
<span data-ttu-id="c3c7d-183">Указывает имя SKU учетной записи хранения, созданной этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="c3c7d-183">Specifies the SKU name of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="c3c7d-184">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="c3c7d-184">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c3c7d-185">Standard_LRS.</span><span class="sxs-lookup"><span data-stu-id="c3c7d-185">Standard_LRS.</span></span> <span data-ttu-id="c3c7d-186">Локально избыточное хранилище.</span><span class="sxs-lookup"><span data-stu-id="c3c7d-186">Locally-redundant storage.</span></span>
- <span data-ttu-id="c3c7d-187">Standard_ZRS.</span><span class="sxs-lookup"><span data-stu-id="c3c7d-187">Standard_ZRS.</span></span> <span data-ttu-id="c3c7d-188">Зона — избыточное хранилище.</span><span class="sxs-lookup"><span data-stu-id="c3c7d-188">Zone-redundant storage.</span></span>
- <span data-ttu-id="c3c7d-189">Standard_GRS.</span><span class="sxs-lookup"><span data-stu-id="c3c7d-189">Standard_GRS.</span></span> <span data-ttu-id="c3c7d-190">Геоизбыточное хранилище.</span><span class="sxs-lookup"><span data-stu-id="c3c7d-190">Geo-redundant storage.</span></span>
- <span data-ttu-id="c3c7d-191">Standard_RAGRS.</span><span class="sxs-lookup"><span data-stu-id="c3c7d-191">Standard_RAGRS.</span></span> <span data-ttu-id="c3c7d-192">Доступное для чтения геоизбыточное хранилище.</span><span class="sxs-lookup"><span data-stu-id="c3c7d-192">Read access geo-redundant storage.</span></span>
- <span data-ttu-id="c3c7d-193">Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="c3c7d-193">Premium_LRS.</span></span> <span data-ttu-id="c3c7d-194">Локально — избыточное хранилище Premium.</span><span class="sxs-lookup"><span data-stu-id="c3c7d-194">Premium locally-redundant storage.</span></span>
- <span data-ttu-id="c3c7d-195">Premium_ZRS.</span><span class="sxs-lookup"><span data-stu-id="c3c7d-195">Premium_ZRS.</span></span> <span data-ttu-id="c3c7d-196">Расширенная зона — избыточное хранилище.</span><span class="sxs-lookup"><span data-stu-id="c3c7d-196">Premium zone-redundant storage.</span></span>
- <span data-ttu-id="c3c7d-197">Standard_GZRS геоизбыточной зоны (избыточное хранилище).</span><span class="sxs-lookup"><span data-stu-id="c3c7d-197">Standard_GZRS - Geo-redundant zone-redundant storage.</span></span>
- <span data-ttu-id="c3c7d-198">Standard_RAGZRS-для чтения с геоизбыточной зоны (избыточное хранилище).</span><span class="sxs-lookup"><span data-stu-id="c3c7d-198">Standard_RAGZRS - Read access geo-redundant zone-redundant storage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountType, AccountType, Type
Accepted values: Standard_LRS, Standard_ZRS, Standard_GRS, Standard_RAGRS, Premium_LRS, Premium_ZRS, Standard_GZRS, Standard_RAGZRS

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3c7d-199">-Тег</span><span class="sxs-lookup"><span data-stu-id="c3c7d-199">-Tag</span></span>
<span data-ttu-id="c3c7d-200">Пары "ключ-значение" в виде хэш-таблицы, установленной в качестве тегов на сервере.</span><span class="sxs-lookup"><span data-stu-id="c3c7d-200">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="c3c7d-201">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="c3c7d-201">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="c3c7d-202">-UseSubDomain</span><span class="sxs-lookup"><span data-stu-id="c3c7d-202">-UseSubDomain</span></span>
<span data-ttu-id="c3c7d-203">Указывает, нужно ли включить косвенную проверку CName.</span><span class="sxs-lookup"><span data-stu-id="c3c7d-203">Indicates whether to enable indirect CName validation.</span></span>

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

### <span data-ttu-id="c3c7d-204">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3c7d-204">CommonParameters</span></span>
<span data-ttu-id="c3c7d-205">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c3c7d-205">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3c7d-206">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c3c7d-206">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3c7d-207">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c3c7d-207">INPUTS</span></span>

### <span data-ttu-id="c3c7d-208">System. String</span><span class="sxs-lookup"><span data-stu-id="c3c7d-208">System.String</span></span>

## <span data-ttu-id="c3c7d-209">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c3c7d-209">OUTPUTS</span></span>

### <span data-ttu-id="c3c7d-210">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c3c7d-210">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="c3c7d-211">Пуск</span><span class="sxs-lookup"><span data-stu-id="c3c7d-211">NOTES</span></span>

## <span data-ttu-id="c3c7d-212">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c3c7d-212">RELATED LINKS</span></span>

[<span data-ttu-id="c3c7d-213">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c3c7d-213">Get-AzStorageAccount</span></span>](./Get-AzStorageAccount.md)

[<span data-ttu-id="c3c7d-214">Remove-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c3c7d-214">Remove-AzStorageAccount</span></span>](./Remove-AzStorageAccount.md)

[<span data-ttu-id="c3c7d-215">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c3c7d-215">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)

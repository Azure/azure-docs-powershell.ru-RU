---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A3DA1205-B8FB-4B4C-9C40-AD303D038EDF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
ms.openlocfilehash: c8ac7139c44adc8bd748eef9a6c762a71c3a777f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93907277"
---
# <span data-ttu-id="7ba12-101">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7ba12-101">New-AzStorageAccount</span></span>

## <span data-ttu-id="7ba12-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7ba12-102">SYNOPSIS</span></span>
<span data-ttu-id="7ba12-103">Создание учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="7ba12-103">Creates a Storage account.</span></span>

## <span data-ttu-id="7ba12-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7ba12-104">SYNTAX</span></span>

```
New-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Location] <String>
 [-Kind <String>] [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>]
 [-Tag <Hashtable>] [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-EnableHierarchicalNamespace <Boolean>] [-EnableAzureActiveDirectoryDomainServicesForFile <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7ba12-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7ba12-105">DESCRIPTION</span></span>
<span data-ttu-id="7ba12-106">Командлет **New-AzStorageAccount** создает учетную запись хранения Azure.</span><span class="sxs-lookup"><span data-stu-id="7ba12-106">The **New-AzStorageAccount** cmdlet creates an Azure Storage account.</span></span>

## <span data-ttu-id="7ba12-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7ba12-107">EXAMPLES</span></span>

### <span data-ttu-id="7ba12-108">Пример 1: создание учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="7ba12-108">Example 1: Create a Storage account</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS
```

<span data-ttu-id="7ba12-109">Эта команда создает учетную запись хранения для имени группы ресурсов MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="7ba12-109">This command creates a Storage account for the resource group name MyResourceGroup.</span></span>

### <span data-ttu-id="7ba12-110">Пример 2: создание учетной записи хранения BLOB-данных с BlobStorageным и горячим AccessTier</span><span class="sxs-lookup"><span data-stu-id="7ba12-110">Example 2: Create a Blob Storage account with BlobStorage Kind and hot AccessTier</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind BlobStorage -AccessTier Hot
```

<span data-ttu-id="7ba12-111">Эта команда создает учетную запись хранилища BLOB-объектов, которая имеет BlobStorage и горячий AccessTier</span><span class="sxs-lookup"><span data-stu-id="7ba12-111">This command creates a Blob Storage account that with BlobStorage Kind and hot AccessTier</span></span>

### <span data-ttu-id="7ba12-112">Пример 3: создание учетной записи хранения с помощью StorageV2, создание и назначение удостоверения для Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="7ba12-112">Example 3: Create a Storage account with Kind StorageV2, and Generate and Assign an Identity for Azure KeyVault.</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind StorageV2 -AssignIdentity
```

<span data-ttu-id="7ba12-113">Эта команда создает учетную запись хранения с StorageV2.</span><span class="sxs-lookup"><span data-stu-id="7ba12-113">This command creates a Storage account with Kind StorageV2.</span></span>  <span data-ttu-id="7ba12-114">Кроме того, она генерирует и назначает удостоверение, которое можно использовать для управления ключами учетной записи через Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="7ba12-114">It also generates and assigns an identity that can be used to manage account keys through Azure KeyVault.</span></span>

### <span data-ttu-id="7ba12-115">Пример 4: создание учетной записи хранения с помощью NetworkRuleSet из JSON</span><span class="sxs-lookup"><span data-stu-id="7ba12-115">Example 4: Create a Storage account with NetworkRuleSet from JSON</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -Type Standard_LRS -NetworkRuleSet (@{bypass="Logging,Metrics";
    ipRules=(@{IPAddressOrRange="20.11.0.0/16";Action="allow"},
            @{IPAddressOrRange="10.0.0.0/7";Action="allow"});
    virtualNetworkRules=(@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},
                        @{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2";Action="allow"});
    defaultAction="Deny"})
```

<span data-ttu-id="7ba12-116">Эта команда создает учетную запись хранения, которая имеет свойство NetworkRuleSet из JSON.</span><span class="sxs-lookup"><span data-stu-id="7ba12-116">This command creates a Storage account that has NetworkRuleSet property from JSON</span></span>

### <span data-ttu-id="7ba12-117">Пример 5: создание учетной записи хранения с включенным иерархическое пространством имен.</span><span class="sxs-lookup"><span data-stu-id="7ba12-117">Example 5: Create a Storage account with Hierarchical Namespace enabled.</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "US West" -SkuName "Standard_GRS" -Kind StorageV2  -EnableHierarchicalNamespace $true
```

<span data-ttu-id="7ba12-118">Эта команда создает учетную запись хранения, для которой включено иерархическое пространство имен.</span><span class="sxs-lookup"><span data-stu-id="7ba12-118">This command creates a Storage account with Hierarchical Namespace enabled.</span></span>

### <span data-ttu-id="7ba12-119">Пример 6: создание учетной записи хранения с помощью Azure Files аутентификация в доменных службах AAD.</span><span class="sxs-lookup"><span data-stu-id="7ba12-119">Example 6: Create a Storage account with Azure Files AAD DS Authentication.</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EnableAzureActiveDirectoryDomainServicesForFile $true
```

<span data-ttu-id="7ba12-120">Эта команда создает учетную запись хранения с проверкой подлинности в службе каталогов AAD DS.</span><span class="sxs-lookup"><span data-stu-id="7ba12-120">This command creates a Storage account with Azure Files AAD DS Authentication.</span></span>

## <span data-ttu-id="7ba12-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7ba12-121">PARAMETERS</span></span>

### <span data-ttu-id="7ba12-122">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="7ba12-122">-AccessTier</span></span>
<span data-ttu-id="7ba12-123">Указывает уровень доступа учетной записи хранения, созданной этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="7ba12-123">Specifies the access tier of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="7ba12-124">Допустимые значения этого параметра: горячий и крутой.</span><span class="sxs-lookup"><span data-stu-id="7ba12-124">The acceptable values for this parameter are: Hot and Cool.</span></span>
<span data-ttu-id="7ba12-125">Если указать значение BlobStorage для параметра *вида* , необходимо указать значение параметра *AccessTier* .</span><span class="sxs-lookup"><span data-stu-id="7ba12-125">If you specify a value of BlobStorage for the *Kind* parameter, you must specify a value for the *AccessTier* parameter.</span></span> <span data-ttu-id="7ba12-126">Если для этого параметра *типа* задано значение хранилища, не указывайте параметр *AccessTier* .</span><span class="sxs-lookup"><span data-stu-id="7ba12-126">If you specify a value of Storage for this *Kind* parameter, do not specify the *AccessTier* parameter.</span></span>

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

### <span data-ttu-id="7ba12-127">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7ba12-127">-AsJob</span></span>
<span data-ttu-id="7ba12-128">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="7ba12-128">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7ba12-129">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="7ba12-129">-AssignIdentity</span></span>
<span data-ttu-id="7ba12-130">Создание и назначение нового удостоверения учетной записи хранения для этой учетной записи хранения для использования со службами управления ключами, такими как Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="7ba12-130">Generate and assign a new Storage account Identity for this Storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="7ba12-131">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="7ba12-131">-CustomDomainName</span></span>
<span data-ttu-id="7ba12-132">Указывает имя настраиваемого домена учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="7ba12-132">Specifies the name of the custom domain of the Storage account.</span></span>
<span data-ttu-id="7ba12-133">По умолчанию используется значение Storage.</span><span class="sxs-lookup"><span data-stu-id="7ba12-133">The default value is Storage.</span></span>

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

### <span data-ttu-id="7ba12-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ba12-134">-DefaultProfile</span></span>
<span data-ttu-id="7ba12-135">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7ba12-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ba12-136">-EnableAzureActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="7ba12-136">-EnableAzureActiveDirectoryDomainServicesForFile</span></span>
<span data-ttu-id="7ba12-137">Включите проверку подлинности доменных служб Azure Active Directory для учетной записи хранения в Azure Files.</span><span class="sxs-lookup"><span data-stu-id="7ba12-137">Enable Azure Files Azure Active Directory Domain Service Authentication for the storage account.</span></span>

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

### <span data-ttu-id="7ba12-138">-EnableHierarchicalNamespace</span><span class="sxs-lookup"><span data-stu-id="7ba12-138">-EnableHierarchicalNamespace</span></span>
<span data-ttu-id="7ba12-139">Указывает, включено ли в учетной записи хранения иерархическое пространство имен.</span><span class="sxs-lookup"><span data-stu-id="7ba12-139">Indicates whether or not the Storage account enables Hierarchical Namespace.</span></span>

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

### <span data-ttu-id="7ba12-140">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="7ba12-140">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="7ba12-141">Указывает, разрешено ли учетной записи хранения только трафик HTTPS.</span><span class="sxs-lookup"><span data-stu-id="7ba12-141">Indicates whether or not the Storage account only enables HTTPS traffic.</span></span>

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

### <span data-ttu-id="7ba12-142">-Видах</span><span class="sxs-lookup"><span data-stu-id="7ba12-142">-Kind</span></span>
<span data-ttu-id="7ba12-143">Указывает вариант учетной записи хранения, создаваемой этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="7ba12-143">Specifies the kind of Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="7ba12-144">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="7ba12-144">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7ba12-145">Склад.</span><span class="sxs-lookup"><span data-stu-id="7ba12-145">Storage.</span></span> <span data-ttu-id="7ba12-146">Общая цель учетной записи хранения, которая поддерживает хранение больших двоичных объектов, таблиц, очередей, файлов и дисков.</span><span class="sxs-lookup"><span data-stu-id="7ba12-146">General purpose Storage account that supports storage of Blobs, Tables, Queues, Files and Disks.</span></span>
- <span data-ttu-id="7ba12-147">StorageV2.</span><span class="sxs-lookup"><span data-stu-id="7ba12-147">StorageV2.</span></span> <span data-ttu-id="7ba12-148">Учетная запись хранения общего назначения версии 2 (GPv2), поддерживающая большие двоичные объекты, таблицы, очереди, файлы и диски, с дополнительными возможностями, такими как уровни данных.</span><span class="sxs-lookup"><span data-stu-id="7ba12-148">General Purpose Version 2 (GPv2) Storage account that supports Blobs, Tables, Queues, Files, and Disks, with advanced features like data tiering.</span></span>
- <span data-ttu-id="7ba12-149">BlobStorage.</span><span class="sxs-lookup"><span data-stu-id="7ba12-149">BlobStorage.</span></span> <span data-ttu-id="7ba12-150">Учетная запись хранилища BLOB-объектов, поддерживающая только хранение больших двоичных объектов.</span><span class="sxs-lookup"><span data-stu-id="7ba12-150">Blob Storage account which supports storage of Blobs only.</span></span>
- <span data-ttu-id="7ba12-151">BlockBlobStorage.</span><span class="sxs-lookup"><span data-stu-id="7ba12-151">BlockBlobStorage.</span></span> <span data-ttu-id="7ba12-152">Блокировка учетной записи хранения BLOB-объектов, которая поддерживает хранение блочных больших двоичных объектов.</span><span class="sxs-lookup"><span data-stu-id="7ba12-152">Block Blob Storage account which supports storage of Block Blobs only.</span></span>
- <span data-ttu-id="7ba12-153">FileStorage.</span><span class="sxs-lookup"><span data-stu-id="7ba12-153">FileStorage.</span></span> <span data-ttu-id="7ba12-154">Учетная запись хранилища файлов, поддерживающая хранение только файлов.</span><span class="sxs-lookup"><span data-stu-id="7ba12-154">File Storage account which supports storage of Files only.</span></span>
<span data-ttu-id="7ba12-155">Значением по умолчанию является StorageV2.</span><span class="sxs-lookup"><span data-stu-id="7ba12-155">The default value is StorageV2.</span></span>

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

### <span data-ttu-id="7ba12-156">-Location</span><span class="sxs-lookup"><span data-stu-id="7ba12-156">-Location</span></span>
<span data-ttu-id="7ba12-157">Указывает расположение учетной записи хранения, которую нужно создать.</span><span class="sxs-lookup"><span data-stu-id="7ba12-157">Specifies the location of the Storage account to create.</span></span>

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

### <span data-ttu-id="7ba12-158">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7ba12-158">-Name</span></span>
<span data-ttu-id="7ba12-159">Указывает имя учетной записи хранения, которую нужно создать.</span><span class="sxs-lookup"><span data-stu-id="7ba12-159">Specifies the name of the Storage account to create.</span></span>

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

### <span data-ttu-id="7ba12-160">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="7ba12-160">-NetworkRuleSet</span></span>
<span data-ttu-id="7ba12-161">NetworkRuleSet используется для определения набора правил конфигурации для брандмауэров и виртуальных сетей, а также для задания значений свойств сети, таких как службы, которые могут обойти правила и обрабатывать запросы, не соответствующие ни одному из заданных правил.</span><span class="sxs-lookup"><span data-stu-id="7ba12-161">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as services allowed to bypass the rules and how to handle requests that don't match any of the defined rules.</span></span>

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

### <span data-ttu-id="7ba12-162">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ba12-162">-ResourceGroupName</span></span>
<span data-ttu-id="7ba12-163">Указывает имя группы ресурсов, в которую нужно добавить учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="7ba12-163">Specifies the name of the resource group in which to add the Storage account.</span></span>

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

### <span data-ttu-id="7ba12-164">-SkuName</span><span class="sxs-lookup"><span data-stu-id="7ba12-164">-SkuName</span></span>
<span data-ttu-id="7ba12-165">Указывает имя SKU учетной записи хранения, созданной этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="7ba12-165">Specifies the SKU name of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="7ba12-166">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="7ba12-166">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7ba12-167">Standard_LRS.</span><span class="sxs-lookup"><span data-stu-id="7ba12-167">Standard_LRS.</span></span> <span data-ttu-id="7ba12-168">Локально избыточное хранилище.</span><span class="sxs-lookup"><span data-stu-id="7ba12-168">Locally-redundant storage.</span></span>
- <span data-ttu-id="7ba12-169">Standard_ZRS.</span><span class="sxs-lookup"><span data-stu-id="7ba12-169">Standard_ZRS.</span></span> <span data-ttu-id="7ba12-170">Зона — избыточное хранилище.</span><span class="sxs-lookup"><span data-stu-id="7ba12-170">Zone-redundant storage.</span></span>
- <span data-ttu-id="7ba12-171">Standard_GRS.</span><span class="sxs-lookup"><span data-stu-id="7ba12-171">Standard_GRS.</span></span> <span data-ttu-id="7ba12-172">Геоизбыточное хранилище.</span><span class="sxs-lookup"><span data-stu-id="7ba12-172">Geo-redundant storage.</span></span>
- <span data-ttu-id="7ba12-173">Standard_RAGRS.</span><span class="sxs-lookup"><span data-stu-id="7ba12-173">Standard_RAGRS.</span></span> <span data-ttu-id="7ba12-174">Доступное для чтения геоизбыточное хранилище.</span><span class="sxs-lookup"><span data-stu-id="7ba12-174">Read access geo-redundant storage.</span></span>
- <span data-ttu-id="7ba12-175">Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="7ba12-175">Premium_LRS.</span></span> <span data-ttu-id="7ba12-176">Локально — избыточное хранилище Premium.</span><span class="sxs-lookup"><span data-stu-id="7ba12-176">Premium locally-redundant storage.</span></span>
- <span data-ttu-id="7ba12-177">Premium_ZRS.</span><span class="sxs-lookup"><span data-stu-id="7ba12-177">Premium_ZRS.</span></span> <span data-ttu-id="7ba12-178">Расширенная зона — избыточное хранилище.</span><span class="sxs-lookup"><span data-stu-id="7ba12-178">Premium zone-redundant storage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountType, AccountType, Type
Accepted values: Standard_LRS, Standard_ZRS, Standard_GRS, Standard_RAGRS, Premium_LRS, Premium_ZRS

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ba12-179">-Тег</span><span class="sxs-lookup"><span data-stu-id="7ba12-179">-Tag</span></span>
<span data-ttu-id="7ba12-180">Пары "ключ-значение" в виде хэш-таблицы, установленной в качестве тегов на сервере.</span><span class="sxs-lookup"><span data-stu-id="7ba12-180">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="7ba12-181">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="7ba12-181">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="7ba12-182">-UseSubDomain</span><span class="sxs-lookup"><span data-stu-id="7ba12-182">-UseSubDomain</span></span>
<span data-ttu-id="7ba12-183">Указывает, нужно ли включить косвенную проверку CName.</span><span class="sxs-lookup"><span data-stu-id="7ba12-183">Indicates whether to enable indirect CName validation.</span></span>

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

### <span data-ttu-id="7ba12-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ba12-184">CommonParameters</span></span>
<span data-ttu-id="7ba12-185">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7ba12-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ba12-186">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ba12-186">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ba12-187">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7ba12-187">INPUTS</span></span>

### <span data-ttu-id="7ba12-188">System. String</span><span class="sxs-lookup"><span data-stu-id="7ba12-188">System.String</span></span>

## <span data-ttu-id="7ba12-189">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7ba12-189">OUTPUTS</span></span>

### <span data-ttu-id="7ba12-190">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7ba12-190">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="7ba12-191">Пуск</span><span class="sxs-lookup"><span data-stu-id="7ba12-191">NOTES</span></span>

## <span data-ttu-id="7ba12-192">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7ba12-192">RELATED LINKS</span></span>

[<span data-ttu-id="7ba12-193">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7ba12-193">Get-AzStorageAccount</span></span>](./Get-AzStorageAccount.md)

[<span data-ttu-id="7ba12-194">Remove-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7ba12-194">Remove-AzStorageAccount</span></span>](./Remove-AzStorageAccount.md)

[<span data-ttu-id="7ba12-195">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7ba12-195">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)

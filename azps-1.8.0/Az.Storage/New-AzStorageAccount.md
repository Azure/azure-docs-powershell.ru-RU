---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A3DA1205-B8FB-4B4C-9C40-AD303D038EDF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
ms.openlocfilehash: 316bcbd8efa101a53dc36ede5e56e2b9379f02e7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93728631"
---
# <span data-ttu-id="9b409-101">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="9b409-101">New-AzStorageAccount</span></span>

## <span data-ttu-id="9b409-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9b409-102">SYNOPSIS</span></span>
<span data-ttu-id="9b409-103">Создание учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="9b409-103">Creates a Storage account.</span></span>

## <span data-ttu-id="9b409-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9b409-104">SYNTAX</span></span>

```
New-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Location] <String>
 [-Kind <String>] [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>]
 [-Tag <Hashtable>] [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-EnableHierarchicalNamespace <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9b409-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9b409-105">DESCRIPTION</span></span>
<span data-ttu-id="9b409-106">Командлет **New-AzStorageAccount** создает учетную запись хранения Azure.</span><span class="sxs-lookup"><span data-stu-id="9b409-106">The **New-AzStorageAccount** cmdlet creates an Azure Storage account.</span></span>

## <span data-ttu-id="9b409-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9b409-107">EXAMPLES</span></span>

### <span data-ttu-id="9b409-108">Пример 1: создание учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="9b409-108">Example 1: Create a Storage account</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS
```

<span data-ttu-id="9b409-109">Эта команда создает учетную запись хранения для имени группы ресурсов MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="9b409-109">This command creates a Storage account for the resource group name MyResourceGroup.</span></span>

### <span data-ttu-id="9b409-110">Пример 2: создание учетной записи хранения BLOB-данных с BlobStorageным и горячим AccessTier</span><span class="sxs-lookup"><span data-stu-id="9b409-110">Example 2: Create a Blob Storage account with BlobStorage Kind and hot AccessTier</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind BlobStorage -AccessTier Hot
```

<span data-ttu-id="9b409-111">Эта команда создает учетную запись хранилища BLOB-объектов, которая имеет BlobStorage и горячий AccessTier</span><span class="sxs-lookup"><span data-stu-id="9b409-111">This command creates a Blob Storage account that with BlobStorage Kind and hot AccessTier</span></span>

### <span data-ttu-id="9b409-112">Пример 3: создание учетной записи хранения с помощью StorageV2, создание и назначение удостоверения для Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="9b409-112">Example 3: Create a Storage account with Kind StorageV2, and Generate and Assign an Identity for Azure KeyVault.</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind StorageV2 -AssignIdentity
```

<span data-ttu-id="9b409-113">Эта команда создает учетную запись хранения с StorageV2.</span><span class="sxs-lookup"><span data-stu-id="9b409-113">This command creates a Storage account with Kind StorageV2.</span></span>  <span data-ttu-id="9b409-114">Кроме того, она генерирует и назначает удостоверение, которое можно использовать для управления ключами учетной записи через Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="9b409-114">It also generates and assigns an identity that can be used to manage account keys through Azure KeyVault.</span></span>

### <span data-ttu-id="9b409-115">Пример 4: создание учетной записи хранения с помощью NetworkRuleSet из JSON</span><span class="sxs-lookup"><span data-stu-id="9b409-115">Example 4: Create a Storage account with NetworkRuleSet from JSON</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -Type Standard_LRS -NetworkRuleSet (@{bypass="Logging,Metrics";
    ipRules=(@{IPAddressOrRange="20.11.0.0/16";Action="allow"},
            @{IPAddressOrRange="10.0.0.0/7";Action="allow"});
    virtualNetworkRules=(@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},
                        @{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2";Action="allow"});
    defaultAction="Deny"})
```

<span data-ttu-id="9b409-116">Эта команда создает учетную запись хранения, которая имеет свойство NetworkRuleSet из JSON.</span><span class="sxs-lookup"><span data-stu-id="9b409-116">This command creates a Storage account that has NetworkRuleSet property from JSON</span></span>

### <span data-ttu-id="9b409-117">Пример 5: создание учетной записи хранения с включенным иерархическое пространством имен.</span><span class="sxs-lookup"><span data-stu-id="9b409-117">Example 5: Create a Storage account with Hierarchical Namespace enabled.</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "US West" -SkuName "Standard_GRS" -Kind StorageV2  -EnableHierarchicalNamespace $true
```

<span data-ttu-id="9b409-118">Эта команда создает учетную запись хранения, для которой включено иерархическое пространство имен.</span><span class="sxs-lookup"><span data-stu-id="9b409-118">This command creates a Storage account with Hierarchical Namespace enabled.</span></span>

## <span data-ttu-id="9b409-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9b409-119">PARAMETERS</span></span>

### <span data-ttu-id="9b409-120">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="9b409-120">-AccessTier</span></span>
<span data-ttu-id="9b409-121">Указывает уровень доступа учетной записи хранения, созданной этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="9b409-121">Specifies the access tier of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="9b409-122">Допустимые значения этого параметра: горячий и крутой.</span><span class="sxs-lookup"><span data-stu-id="9b409-122">The acceptable values for this parameter are: Hot and Cool.</span></span>
<span data-ttu-id="9b409-123">Если указать значение BlobStorage для параметра *вида* , необходимо указать значение параметра *AccessTier* .</span><span class="sxs-lookup"><span data-stu-id="9b409-123">If you specify a value of BlobStorage for the *Kind* parameter, you must specify a value for the *AccessTier* parameter.</span></span> <span data-ttu-id="9b409-124">Если для этого параметра *типа* задано значение хранилища, не указывайте параметр *AccessTier* .</span><span class="sxs-lookup"><span data-stu-id="9b409-124">If you specify a value of Storage for this *Kind* parameter, do not specify the *AccessTier* parameter.</span></span>

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

### <span data-ttu-id="9b409-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9b409-125">-AsJob</span></span>
<span data-ttu-id="9b409-126">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="9b409-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9b409-127">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="9b409-127">-AssignIdentity</span></span>
<span data-ttu-id="9b409-128">Создание и назначение нового удостоверения учетной записи хранения для этой учетной записи хранения для использования со службами управления ключами, такими как Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="9b409-128">Generate and assign a new Storage account Identity for this Storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="9b409-129">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="9b409-129">-CustomDomainName</span></span>
<span data-ttu-id="9b409-130">Указывает имя настраиваемого домена учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="9b409-130">Specifies the name of the custom domain of the Storage account.</span></span>
<span data-ttu-id="9b409-131">По умолчанию используется значение Storage.</span><span class="sxs-lookup"><span data-stu-id="9b409-131">The default value is Storage.</span></span>

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

### <span data-ttu-id="9b409-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b409-132">-DefaultProfile</span></span>
<span data-ttu-id="9b409-133">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9b409-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b409-134">-EnableHierarchicalNamespace</span><span class="sxs-lookup"><span data-stu-id="9b409-134">-EnableHierarchicalNamespace</span></span>
<span data-ttu-id="9b409-135">Указывает, включено ли в учетной записи хранения иерархическое пространство имен.</span><span class="sxs-lookup"><span data-stu-id="9b409-135">Indicates whether or not the Storage account enables Hierarchical Namespace.</span></span>

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

### <span data-ttu-id="9b409-136">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="9b409-136">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="9b409-137">Указывает, разрешено ли учетной записи хранения только трафик HTTPS.</span><span class="sxs-lookup"><span data-stu-id="9b409-137">Indicates whether or not the Storage account only enables HTTPS traffic.</span></span>

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

### <span data-ttu-id="9b409-138">-Видах</span><span class="sxs-lookup"><span data-stu-id="9b409-138">-Kind</span></span>
<span data-ttu-id="9b409-139">Указывает вариант учетной записи хранения, создаваемой этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="9b409-139">Specifies the kind of Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="9b409-140">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="9b409-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9b409-141">Склад.</span><span class="sxs-lookup"><span data-stu-id="9b409-141">Storage.</span></span> <span data-ttu-id="9b409-142">Общая цель учетной записи хранения, которая поддерживает хранение больших двоичных объектов, таблиц, очередей, файлов и дисков.</span><span class="sxs-lookup"><span data-stu-id="9b409-142">General purpose Storage account that supports storage of Blobs, Tables, Queues, Files and Disks.</span></span>
- <span data-ttu-id="9b409-143">StorageV2.</span><span class="sxs-lookup"><span data-stu-id="9b409-143">StorageV2.</span></span> <span data-ttu-id="9b409-144">Учетная запись хранения общего назначения версии 2 (GPv2), поддерживающая большие двоичные объекты, таблицы, очереди, файлы и диски, с дополнительными возможностями, такими как уровни данных.</span><span class="sxs-lookup"><span data-stu-id="9b409-144">General Purpose Version 2 (GPv2) Storage account that supports Blobs, Tables, Queues, Files, and Disks, with advanced features like data tiering.</span></span>
- <span data-ttu-id="9b409-145">BlobStorage.</span><span class="sxs-lookup"><span data-stu-id="9b409-145">BlobStorage.</span></span> <span data-ttu-id="9b409-146">Учетная запись хранилища BLOB-объектов, поддерживающая только хранение больших двоичных объектов.</span><span class="sxs-lookup"><span data-stu-id="9b409-146">Blob Storage account which supports storage of Blobs only.</span></span>
<span data-ttu-id="9b409-147">По умолчанию используется значение Storage.</span><span class="sxs-lookup"><span data-stu-id="9b409-147">The default value is Storage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Storage, StorageV2, BlobStorage, BlockBlobStorage

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b409-148">-Location</span><span class="sxs-lookup"><span data-stu-id="9b409-148">-Location</span></span>
<span data-ttu-id="9b409-149">Указывает расположение учетной записи хранения, которую нужно создать.</span><span class="sxs-lookup"><span data-stu-id="9b409-149">Specifies the location of the Storage account to create.</span></span>

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

### <span data-ttu-id="9b409-150">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9b409-150">-Name</span></span>
<span data-ttu-id="9b409-151">Указывает имя учетной записи хранения, которую нужно создать.</span><span class="sxs-lookup"><span data-stu-id="9b409-151">Specifies the name of the Storage account to create.</span></span>

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

### <span data-ttu-id="9b409-152">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="9b409-152">-NetworkRuleSet</span></span>
<span data-ttu-id="9b409-153">NetworkRuleSet используется для определения набора правил конфигурации для брандмауэров и виртуальных сетей, а также для задания значений свойств сети, таких как службы, которые могут обойти правила и обрабатывать запросы, не соответствующие ни одному из заданных правил.</span><span class="sxs-lookup"><span data-stu-id="9b409-153">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as services allowed to bypass the rules and how to handle requests that don't match any of the defined rules.</span></span>

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

### <span data-ttu-id="9b409-154">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b409-154">-ResourceGroupName</span></span>
<span data-ttu-id="9b409-155">Указывает имя группы ресурсов, в которую нужно добавить учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="9b409-155">Specifies the name of the resource group in which to add the Storage account.</span></span>

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

### <span data-ttu-id="9b409-156">-SkuName</span><span class="sxs-lookup"><span data-stu-id="9b409-156">-SkuName</span></span>
<span data-ttu-id="9b409-157">Указывает имя SKU учетной записи хранения, созданной этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="9b409-157">Specifies the SKU name of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="9b409-158">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="9b409-158">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9b409-159">Standard_LRS.</span><span class="sxs-lookup"><span data-stu-id="9b409-159">Standard_LRS.</span></span> <span data-ttu-id="9b409-160">Локально избыточное хранилище.</span><span class="sxs-lookup"><span data-stu-id="9b409-160">Locally-redundant storage.</span></span>
- <span data-ttu-id="9b409-161">Standard_ZRS.</span><span class="sxs-lookup"><span data-stu-id="9b409-161">Standard_ZRS.</span></span> <span data-ttu-id="9b409-162">Зона — избыточное хранилище.</span><span class="sxs-lookup"><span data-stu-id="9b409-162">Zone-redundant storage.</span></span>
- <span data-ttu-id="9b409-163">Standard_GRS.</span><span class="sxs-lookup"><span data-stu-id="9b409-163">Standard_GRS.</span></span> <span data-ttu-id="9b409-164">Геоизбыточное хранилище.</span><span class="sxs-lookup"><span data-stu-id="9b409-164">Geo-redundant storage.</span></span>
- <span data-ttu-id="9b409-165">Standard_RAGRS.</span><span class="sxs-lookup"><span data-stu-id="9b409-165">Standard_RAGRS.</span></span> <span data-ttu-id="9b409-166">Доступное для чтения геоизбыточное хранилище.</span><span class="sxs-lookup"><span data-stu-id="9b409-166">Read access geo-redundant storage.</span></span>
- <span data-ttu-id="9b409-167">Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="9b409-167">Premium_LRS.</span></span> <span data-ttu-id="9b409-168">Локально — избыточное хранилище Premium.</span><span class="sxs-lookup"><span data-stu-id="9b409-168">Premium locally-redundant storage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountType, AccountType, Type
Accepted values: Standard_LRS, Standard_ZRS, Standard_GRS, Standard_RAGRS, Premium_LRS

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b409-169">-Тег</span><span class="sxs-lookup"><span data-stu-id="9b409-169">-Tag</span></span>
<span data-ttu-id="9b409-170">Пары "ключ-значение" в виде хэш-таблицы, установленной в качестве тегов на сервере.</span><span class="sxs-lookup"><span data-stu-id="9b409-170">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="9b409-171">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="9b409-171">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="9b409-172">-UseSubDomain</span><span class="sxs-lookup"><span data-stu-id="9b409-172">-UseSubDomain</span></span>
<span data-ttu-id="9b409-173">Указывает, нужно ли включить косвенную проверку CName.</span><span class="sxs-lookup"><span data-stu-id="9b409-173">Indicates whether to enable indirect CName validation.</span></span>

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

### <span data-ttu-id="9b409-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b409-174">CommonParameters</span></span>
<span data-ttu-id="9b409-175">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9b409-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b409-176">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b409-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b409-177">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9b409-177">INPUTS</span></span>

### <span data-ttu-id="9b409-178">System. String</span><span class="sxs-lookup"><span data-stu-id="9b409-178">System.String</span></span>

## <span data-ttu-id="9b409-179">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9b409-179">OUTPUTS</span></span>

### <span data-ttu-id="9b409-180">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="9b409-180">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="9b409-181">Пуск</span><span class="sxs-lookup"><span data-stu-id="9b409-181">NOTES</span></span>

## <span data-ttu-id="9b409-182">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9b409-182">RELATED LINKS</span></span>

[<span data-ttu-id="9b409-183">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="9b409-183">Get-AzStorageAccount</span></span>](./Get-AzStorageAccount.md)

[<span data-ttu-id="9b409-184">Remove-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="9b409-184">Remove-AzStorageAccount</span></span>](./Remove-AzStorageAccount.md)

[<span data-ttu-id="9b409-185">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="9b409-185">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)

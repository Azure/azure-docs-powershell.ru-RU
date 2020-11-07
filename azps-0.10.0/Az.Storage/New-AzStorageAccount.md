---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A3DA1205-B8FB-4B4C-9C40-AD303D038EDF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/New-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/New-AzStorageAccount.md
ms.openlocfilehash: 3ded950659546b6ec2a25271bc09718c937d401b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910742"
---
# <span data-ttu-id="91287-101">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="91287-101">New-AzStorageAccount</span></span>

## <span data-ttu-id="91287-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="91287-102">SYNOPSIS</span></span>
<span data-ttu-id="91287-103">Создание учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="91287-103">Creates a Storage account.</span></span>

## <span data-ttu-id="91287-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="91287-104">SYNTAX</span></span>

```
New-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String>
 [-Location] <String> [-Kind <String>] [-AccessTier <String>] [-CustomDomainName <String>]
 [-UseSubDomain <Boolean>] [-Tag <Hashtable>] [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="91287-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="91287-105">DESCRIPTION</span></span>
<span data-ttu-id="91287-106">Командлет **New-AzStorageAccount** создает учетную запись хранения Azure.</span><span class="sxs-lookup"><span data-stu-id="91287-106">The **New-AzStorageAccount** cmdlet creates an Azure Storage account.</span></span>

## <span data-ttu-id="91287-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="91287-107">EXAMPLES</span></span>

### <span data-ttu-id="91287-108">Пример 1: создание учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="91287-108">Example 1: Create a Storage account</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS
```

<span data-ttu-id="91287-109">Эта команда создает учетную запись хранения для имени группы ресурсов MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="91287-109">This command creates a Storage account for the resource group name MyResourceGroup.</span></span>

### <span data-ttu-id="91287-110">Пример 2: создание учетной записи хранения BLOB-данных с BlobStorageным и горячим AccessTier</span><span class="sxs-lookup"><span data-stu-id="91287-110">Example 2: Create a Blob Storage account with BlobStorage Kind and hot AccessTier</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind BlobStorage -AccessTier Hot
```

<span data-ttu-id="91287-111">Эта команда создает учетную запись хранилища BLOB-объектов, которая имеет BlobStorage и горячий AccessTier</span><span class="sxs-lookup"><span data-stu-id="91287-111">This command creates a Blob Storage account that with BlobStorage Kind and hot AccessTier</span></span>

### <span data-ttu-id="91287-112">Пример 3: создание учетной записи хранения с помощью StorageV2, создание и назначение удостоверения для Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="91287-112">Example 3: Create a Storage account with Kind StorageV2, and Generate and Assign an Identity for Azure KeyVault.</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind StorageV2 -AssignIdentity
```

<span data-ttu-id="91287-113">Эта команда создает учетную запись хранения с StorageV2.</span><span class="sxs-lookup"><span data-stu-id="91287-113">This command creates a Storage account with Kind StorageV2.</span></span>  <span data-ttu-id="91287-114">Кроме того, она генерирует и назначает удостоверение, которое можно использовать для управления ключами учетной записи через Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="91287-114">It also generates and assigns an identity that can be used to manage account keys through Azure KeyVault.</span></span>

### <span data-ttu-id="91287-115">Пример 4: создание учетной записи хранения с помощью NetworkRuleSet из JSON</span><span class="sxs-lookup"><span data-stu-id="91287-115">Example 4: Create a Storage account with NetworkRuleSet from JSON</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -Type Standard_LRS -NetworkRuleSet (@{bypass="Logging,Metrics";
    ipRules=(@{IPAddressOrRange="20.11.0.0/16";Action="allow"},
            @{IPAddressOrRange="10.0.0.0/7";Action="allow"});
    virtualNetworkRules=(@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},
                        @{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2";Action="allow"});
    defaultAction="Deny"})
```

<span data-ttu-id="91287-116">Эта команда создает учетную запись хранения, которая имеет свойство NetworkRuleSet из JSON.</span><span class="sxs-lookup"><span data-stu-id="91287-116">This command creates a Storage account that has NetworkRuleSet property from JSON</span></span>

## <span data-ttu-id="91287-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="91287-117">PARAMETERS</span></span>

### <span data-ttu-id="91287-118">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="91287-118">-AccessTier</span></span>
<span data-ttu-id="91287-119">Указывает уровень доступа учетной записи хранения, созданной этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="91287-119">Specifies the access tier of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="91287-120">Допустимые значения этого параметра: горячий и крутой.</span><span class="sxs-lookup"><span data-stu-id="91287-120">The acceptable values for this parameter are: Hot and Cool.</span></span>
<span data-ttu-id="91287-121">Если указать значение BlobStorage для параметра *вида* , необходимо указать значение параметра *AccessTier* .</span><span class="sxs-lookup"><span data-stu-id="91287-121">If you specify a value of BlobStorage for the *Kind* parameter, you must specify a value for the *AccessTier* parameter.</span></span> <span data-ttu-id="91287-122">Если для этого параметра *типа* задано значение хранилища, не указывайте параметр *AccessTier* .</span><span class="sxs-lookup"><span data-stu-id="91287-122">If you specify a value of Storage for this *Kind* parameter, do not specify the *AccessTier* parameter.</span></span>

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

### <span data-ttu-id="91287-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="91287-123">-AsJob</span></span>
<span data-ttu-id="91287-124">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="91287-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="91287-125">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="91287-125">-AssignIdentity</span></span>
<span data-ttu-id="91287-126">Создание и назначение нового удостоверения учетной записи хранения для этой учетной записи хранения для использования со службами управления ключами, такими как Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="91287-126">Generate and assign a new Storage account Identity for this Storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="91287-127">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="91287-127">-CustomDomainName</span></span>
<span data-ttu-id="91287-128">Указывает имя настраиваемого домена учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="91287-128">Specifies the name of the custom domain of the Storage account.</span></span>
<span data-ttu-id="91287-129">По умолчанию используется значение Storage.</span><span class="sxs-lookup"><span data-stu-id="91287-129">The default value is Storage.</span></span>

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

### <span data-ttu-id="91287-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91287-130">-DefaultProfile</span></span>
<span data-ttu-id="91287-131">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="91287-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91287-132">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="91287-132">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="91287-133">Указывает, разрешено ли учетной записи хранения только трафик HTTPS.</span><span class="sxs-lookup"><span data-stu-id="91287-133">Indicates whether or not the Storage account only enables HTTPS traffic.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91287-134">-Видах</span><span class="sxs-lookup"><span data-stu-id="91287-134">-Kind</span></span>
<span data-ttu-id="91287-135">Указывает вариант учетной записи хранения, создаваемой этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="91287-135">Specifies the kind of Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="91287-136">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="91287-136">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="91287-137">Склад.</span><span class="sxs-lookup"><span data-stu-id="91287-137">Storage.</span></span> <span data-ttu-id="91287-138">Общая цель учетной записи хранения, которая поддерживает хранение больших двоичных объектов, таблиц, очередей, файлов и дисков.</span><span class="sxs-lookup"><span data-stu-id="91287-138">General purpose Storage account that supports storage of Blobs, Tables, Queues, Files and Disks.</span></span>
- <span data-ttu-id="91287-139">StorageV2.</span><span class="sxs-lookup"><span data-stu-id="91287-139">StorageV2.</span></span> <span data-ttu-id="91287-140">Учетная запись хранения общего назначения версии 2 (GPv2), поддерживающая большие двоичные объекты, таблицы, очереди, файлы и диски, с дополнительными возможностями, такими как уровни данных.</span><span class="sxs-lookup"><span data-stu-id="91287-140">General Purpose Version 2 (GPv2) Storage account that supports Blobs, Tables, Queues, Files, and Disks, with advanced features like data tiering.</span></span>
- <span data-ttu-id="91287-141">BlobStorage.</span><span class="sxs-lookup"><span data-stu-id="91287-141">BlobStorage.</span></span> <span data-ttu-id="91287-142">Учетная запись хранилища BLOB-объектов, поддерживающая только хранение больших двоичных объектов.</span><span class="sxs-lookup"><span data-stu-id="91287-142">Blob Storage account which supports storage of Blobs only.</span></span>
<span data-ttu-id="91287-143">По умолчанию используется значение Storage.</span><span class="sxs-lookup"><span data-stu-id="91287-143">The default value is Storage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Storage, StorageV2, BlobStorage

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91287-144">-Location</span><span class="sxs-lookup"><span data-stu-id="91287-144">-Location</span></span>
<span data-ttu-id="91287-145">Указывает расположение учетной записи хранения, которую нужно создать.</span><span class="sxs-lookup"><span data-stu-id="91287-145">Specifies the location of the Storage account to create.</span></span>

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

### <span data-ttu-id="91287-146">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="91287-146">-Name</span></span>
<span data-ttu-id="91287-147">Указывает имя учетной записи хранения, которую нужно создать.</span><span class="sxs-lookup"><span data-stu-id="91287-147">Specifies the name of the Storage account to create.</span></span>

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

### <span data-ttu-id="91287-148">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="91287-148">-NetworkRuleSet</span></span>
<span data-ttu-id="91287-149">NetworkRuleSet используется для определения набора правил конфигурации для брандмауэров и виртуальных сетей, а также для задания значений свойств сети, таких как службы, которые могут обойти правила и обрабатывать запросы, не соответствующие ни одному из заданных правил.</span><span class="sxs-lookup"><span data-stu-id="91287-149">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as services allowed to bypass the rules and how to handle requests that don't match any of the defined rules.</span></span>

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

### <span data-ttu-id="91287-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91287-150">-ResourceGroupName</span></span>
<span data-ttu-id="91287-151">Указывает имя группы ресурсов, в которую нужно добавить учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="91287-151">Specifies the name of the resource group in which to add the Storage account.</span></span>

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

### <span data-ttu-id="91287-152">-SkuName</span><span class="sxs-lookup"><span data-stu-id="91287-152">-SkuName</span></span>
<span data-ttu-id="91287-153">Указывает имя SKU учетной записи хранения, созданной этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="91287-153">Specifies the SKU name of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="91287-154">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="91287-154">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="91287-155">Standard_LRS.</span><span class="sxs-lookup"><span data-stu-id="91287-155">Standard_LRS.</span></span> <span data-ttu-id="91287-156">Локально избыточное хранилище.</span><span class="sxs-lookup"><span data-stu-id="91287-156">Locally-redundant storage.</span></span>
- <span data-ttu-id="91287-157">Standard_ZRS.</span><span class="sxs-lookup"><span data-stu-id="91287-157">Standard_ZRS.</span></span> <span data-ttu-id="91287-158">Зона — избыточное хранилище.</span><span class="sxs-lookup"><span data-stu-id="91287-158">Zone-redundant storage.</span></span>
- <span data-ttu-id="91287-159">Standard_GRS.</span><span class="sxs-lookup"><span data-stu-id="91287-159">Standard_GRS.</span></span> <span data-ttu-id="91287-160">Геоизбыточное хранилище.</span><span class="sxs-lookup"><span data-stu-id="91287-160">Geo-redundant storage.</span></span>
- <span data-ttu-id="91287-161">Standard_RAGRS.</span><span class="sxs-lookup"><span data-stu-id="91287-161">Standard_RAGRS.</span></span> <span data-ttu-id="91287-162">Доступное для чтения геоизбыточное хранилище.</span><span class="sxs-lookup"><span data-stu-id="91287-162">Read access geo-redundant storage.</span></span>
- <span data-ttu-id="91287-163">Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="91287-163">Premium_LRS.</span></span> <span data-ttu-id="91287-164">Локально — избыточное хранилище Premium.</span><span class="sxs-lookup"><span data-stu-id="91287-164">Premium locally-redundant storage.</span></span>

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

### <span data-ttu-id="91287-165">-Тег</span><span class="sxs-lookup"><span data-stu-id="91287-165">-Tag</span></span>
<span data-ttu-id="91287-166">Пары "ключ-значение" в виде хэш-таблицы, установленной в качестве тегов на сервере.</span><span class="sxs-lookup"><span data-stu-id="91287-166">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="91287-167">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="91287-167">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="91287-168">-UseSubDomain</span><span class="sxs-lookup"><span data-stu-id="91287-168">-UseSubDomain</span></span>
<span data-ttu-id="91287-169">Указывает, нужно ли включить косвенную проверку CName.</span><span class="sxs-lookup"><span data-stu-id="91287-169">Indicates whether to enable indirect CName validation.</span></span>

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

### <span data-ttu-id="91287-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91287-170">CommonParameters</span></span>
<span data-ttu-id="91287-171">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="91287-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91287-172">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91287-172">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91287-173">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="91287-173">INPUTS</span></span>

### <span data-ttu-id="91287-174">System. String</span><span class="sxs-lookup"><span data-stu-id="91287-174">System.String</span></span>

### <span data-ttu-id="91287-175">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="91287-175">System.Boolean</span></span>

## <span data-ttu-id="91287-176">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="91287-176">OUTPUTS</span></span>

### <span data-ttu-id="91287-177">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="91287-177">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="91287-178">Пуск</span><span class="sxs-lookup"><span data-stu-id="91287-178">NOTES</span></span>

## <span data-ttu-id="91287-179">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="91287-179">RELATED LINKS</span></span>

[<span data-ttu-id="91287-180">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="91287-180">Get-AzStorageAccount</span></span>](./Get-AzStorageAccount.md)

[<span data-ttu-id="91287-181">Remove-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="91287-181">Remove-AzStorageAccount</span></span>](./Remove-AzStorageAccount.md)

[<span data-ttu-id="91287-182">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="91287-182">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)

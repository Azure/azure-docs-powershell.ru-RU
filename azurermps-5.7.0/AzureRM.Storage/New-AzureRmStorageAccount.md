---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
ms.assetid: A3DA1205-B8FB-4B4C-9C40-AD303D038EDF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/New-AzureRmStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/New-AzureRmStorageAccount.md
ms.openlocfilehash: 1b00930332d9f3f5a78e4cfe8ab7478a5dc5fa19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567864"
---
# <span data-ttu-id="6f864-101">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6f864-101">New-AzureRmStorageAccount</span></span>

## <span data-ttu-id="6f864-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6f864-102">SYNOPSIS</span></span>
<span data-ttu-id="6f864-103">Создание учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="6f864-103">Creates a Storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6f864-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6f864-104">SYNTAX</span></span>

```
New-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String>
 [-Location] <String> [[-Kind] <String>] [[-AccessTier] <String>] [[-CustomDomainName] <String>]
 [[-UseSubDomain] <Boolean>] [[-EnableEncryptionService] <EncryptionSupportServiceEnum>] [[-Tag] <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="6f864-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6f864-105">DESCRIPTION</span></span>
<span data-ttu-id="6f864-106">Командлет **New-AzureRmStorageAccount** создает учетную запись хранения Azure.</span><span class="sxs-lookup"><span data-stu-id="6f864-106">The **New-AzureRmStorageAccount** cmdlet creates an Azure Storage account.</span></span>

## <span data-ttu-id="6f864-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6f864-107">EXAMPLES</span></span>

### <span data-ttu-id="6f864-108">Пример 1: создание учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="6f864-108">Example 1: Create a Storage Account</span></span>
```
PS C:\>New-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -Location "West US" -SkuName "Standard_GRS"
```

<span data-ttu-id="6f864-109">Эта команда создает учетную запись хранения для имени группы ресурсов MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="6f864-109">This command creates a Storage account for the resource group name MyResourceGroup.</span></span>

### <span data-ttu-id="6f864-110">Пример 2: создание учетной записи хранилища BLOB-объектов, использующей шифрование службы хранилища</span><span class="sxs-lookup"><span data-stu-id="6f864-110">Example 2: Create a Blob Storage account that uses Storage Service Encryption</span></span>
```
PS C:\>New-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -Location "West US" -SkuName "Standard_GRS" -EnableEncryptionService Blob -Kind "BlobStorage" -AccessTier Hot
```

<span data-ttu-id="6f864-111">Эта команда создает учетную запись хранилища BLOB-объектов, которая использует тип горячего доступа.</span><span class="sxs-lookup"><span data-stu-id="6f864-111">This command creates a Blob Storage account that uses the hot access type.</span></span>
<span data-ttu-id="6f864-112">Учетная запись включила шифрование службы хранилища в службе больших двоичных объектов.</span><span class="sxs-lookup"><span data-stu-id="6f864-112">The account has enabled Storage Service encryption on Blob Service.</span></span>

### <span data-ttu-id="6f864-113">Пример 3: создание учетной записи хранения, которая обеспечивает шифрование службы хранилища для BLOB-объектов и файловых служб, а затем создает и назначает удостоверение для Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="6f864-113">Example 3: Create a Storage Account that Enables Storage Service Encryption on Blob and File Services, and Generate and Assign an Identity for Azure KeyVault.</span></span>
```
PS C:\>New-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -Location "West US" -SkuName "Standard_GRS" -EnableEncryptionService "Blob,File" -AssignIdentity
```

<span data-ttu-id="6f864-114">Эта команда создает учетную запись хранения, которая включила шифрование службы хранилища для BLOB-объектов и файловых служб.</span><span class="sxs-lookup"><span data-stu-id="6f864-114">This command creates a Storage account that enabled Storage Service encryption on Blob and File Services.</span></span>  <span data-ttu-id="6f864-115">Кроме того, она генерирует и назначает удостоверение, которое можно использовать для управления ключами учетной записи через Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="6f864-115">It also generates and assigns an identity that can be used to manage account keys through Azure KeyVault.</span></span>

## <span data-ttu-id="6f864-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6f864-116">PARAMETERS</span></span>

### <span data-ttu-id="6f864-117">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="6f864-117">-AccessTier</span></span>
<span data-ttu-id="6f864-118">Указывает уровень доступа учетной записи хранения, созданной этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="6f864-118">Specifies the access tier of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="6f864-119">Допустимые значения этого параметра: горячий и крутой.</span><span class="sxs-lookup"><span data-stu-id="6f864-119">The acceptable values for this parameter are: Hot and Cool.</span></span>

<span data-ttu-id="6f864-120">Если указать значение BlobStorage для параметра *вида* , необходимо указать значение параметра *AccessTier* .</span><span class="sxs-lookup"><span data-stu-id="6f864-120">If you specify a value of BlobStorage for the *Kind* parameter, you must specify a value for the *AccessTier* parameter.</span></span>

<span data-ttu-id="6f864-121">Если для этого параметра *типа* задано значение хранилища, не указывайте параметр *AccessTier* .</span><span class="sxs-lookup"><span data-stu-id="6f864-121">If you specify a value of Storage for this *Kind* parameter, do not specify the *AccessTier* parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f864-122">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="6f864-122">-AssignIdentity</span></span>
<span data-ttu-id="6f864-123">Создание и назначение нового удостоверения учетной записи хранения для этой учетной записи хранения для использования со службами управления ключами, такими как Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="6f864-123">Generate and assign a new Storage Account Identity for this storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="6f864-124">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="6f864-124">-CustomDomainName</span></span>
<span data-ttu-id="6f864-125">Указывает имя настраиваемого домена учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="6f864-125">Specifies the name of the custom domain of the Storage account.</span></span>
<span data-ttu-id="6f864-126">По умолчанию используется значение Storage.</span><span class="sxs-lookup"><span data-stu-id="6f864-126">The default value is Storage.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f864-127">-EnableEncryptionService</span><span class="sxs-lookup"><span data-stu-id="6f864-127">-EnableEncryptionService</span></span>
<span data-ttu-id="6f864-128">Указывает, включает ли этот командлет шифрование службы хранилища для службы хранилища.</span><span class="sxs-lookup"><span data-stu-id="6f864-128">Indicates whether this cmdlet enables Storage Service encryption on the Storage Service.</span></span>
<span data-ttu-id="6f864-129">Поддерживаются двоичные файлы и службы Azure.</span><span class="sxs-lookup"><span data-stu-id="6f864-129">Azure Blob and Azure File Services are supported.</span></span>

```yaml
Type: EncryptionSupportServiceEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f864-130">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="6f864-130">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="6f864-131">Указывает, следует ли учетной записи хранения включать трафик HTTPS.</span><span class="sxs-lookup"><span data-stu-id="6f864-131">Indicates whether or not the Storage Account only enable https traffic.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f864-132">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="6f864-132">-InformationAction</span></span>
<span data-ttu-id="6f864-133">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="6f864-133">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="6f864-134">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="6f864-134">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6f864-135">Продолжал</span><span class="sxs-lookup"><span data-stu-id="6f864-135">Continue</span></span>
- <span data-ttu-id="6f864-136">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="6f864-136">Ignore</span></span>
- <span data-ttu-id="6f864-137">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="6f864-137">Inquire</span></span>
- <span data-ttu-id="6f864-138">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="6f864-138">SilentlyContinue</span></span>
- <span data-ttu-id="6f864-139">Остановить</span><span class="sxs-lookup"><span data-stu-id="6f864-139">Stop</span></span>
- <span data-ttu-id="6f864-140">Рвать</span><span class="sxs-lookup"><span data-stu-id="6f864-140">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f864-141">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="6f864-141">-InformationVariable</span></span>
<span data-ttu-id="6f864-142">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="6f864-142">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f864-143">-Видах</span><span class="sxs-lookup"><span data-stu-id="6f864-143">-Kind</span></span>
<span data-ttu-id="6f864-144">Указывает вариант учетной записи хранения, создаваемой этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="6f864-144">Specifies the kind of Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="6f864-145">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="6f864-145">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6f864-146">Склад.</span><span class="sxs-lookup"><span data-stu-id="6f864-146">Storage.</span></span>
<span data-ttu-id="6f864-147">Общая цель учетной записи хранения, которая поддерживает хранение больших двоичных объектов, таблиц, очередей, файлов и дисков.</span><span class="sxs-lookup"><span data-stu-id="6f864-147">General purpose storage account that supports storage of Blobs, Tables, Queues, Files and Disks.</span></span>

- <span data-ttu-id="6f864-148">BlobStorage.</span><span class="sxs-lookup"><span data-stu-id="6f864-148">BlobStorage.</span></span>
<span data-ttu-id="6f864-149">Учетная запись хранилища BLOB-объектов, поддерживающая только хранение больших двоичных объектов.</span><span class="sxs-lookup"><span data-stu-id="6f864-149">Blob storage account which supports storage of Blobs only.</span></span>


<span data-ttu-id="6f864-150">По умолчанию используется значение Storage.</span><span class="sxs-lookup"><span data-stu-id="6f864-150">The default value is Storage.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f864-151">-Location</span><span class="sxs-lookup"><span data-stu-id="6f864-151">-Location</span></span>
<span data-ttu-id="6f864-152">Указывает расположение учетной записи хранения, которую нужно создать.</span><span class="sxs-lookup"><span data-stu-id="6f864-152">Specifies the location of the Storage account to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f864-153">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6f864-153">-Name</span></span>
<span data-ttu-id="6f864-154">Указывает имя учетной записи хранения, которую нужно создать.</span><span class="sxs-lookup"><span data-stu-id="6f864-154">Specifies the name of the Storage account to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f864-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f864-155">-ResourceGroupName</span></span>
<span data-ttu-id="6f864-156">Указывает имя группы ресурсов, в которую нужно добавить учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="6f864-156">Specifies the name of the resource group in which to add the Storage account.</span></span>

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

### <span data-ttu-id="6f864-157">-SkuName</span><span class="sxs-lookup"><span data-stu-id="6f864-157">-SkuName</span></span>
<span data-ttu-id="6f864-158">Указывает имя SKU учетной записи хранения, созданной этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="6f864-158">Specifies the SKU name of the storage account that this cmdlet creates.</span></span>
<span data-ttu-id="6f864-159">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="6f864-159">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6f864-160">Standard_LRS.</span><span class="sxs-lookup"><span data-stu-id="6f864-160">Standard_LRS.</span></span>
<span data-ttu-id="6f864-161">Локально избыточное хранилище.</span><span class="sxs-lookup"><span data-stu-id="6f864-161">Locally-redundant storage.</span></span>
- <span data-ttu-id="6f864-162">Standard_ZRS.</span><span class="sxs-lookup"><span data-stu-id="6f864-162">Standard_ZRS.</span></span>
<span data-ttu-id="6f864-163">Зона — избыточное хранилище.</span><span class="sxs-lookup"><span data-stu-id="6f864-163">Zone-redundant storage.</span></span>
- <span data-ttu-id="6f864-164">Standard_GRS.</span><span class="sxs-lookup"><span data-stu-id="6f864-164">Standard_GRS.</span></span>
<span data-ttu-id="6f864-165">Геоизбыточное хранилище.</span><span class="sxs-lookup"><span data-stu-id="6f864-165">Geo-redundant storage.</span></span>
- <span data-ttu-id="6f864-166">Standard_RAGRS.</span><span class="sxs-lookup"><span data-stu-id="6f864-166">Standard_RAGRS.</span></span>
<span data-ttu-id="6f864-167">Доступное для чтения геоизбыточное хранилище.</span><span class="sxs-lookup"><span data-stu-id="6f864-167">Read access geo-redundant storage.</span></span>
- <span data-ttu-id="6f864-168">Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="6f864-168">Premium_LRS.</span></span>
<span data-ttu-id="6f864-169">Локально — избыточное хранилище Premium.</span><span class="sxs-lookup"><span data-stu-id="6f864-169">Premium locally-redundant storage.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountType, AccountType, Type

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f864-170">-Тег</span><span class="sxs-lookup"><span data-stu-id="6f864-170">-Tag</span></span>
<span data-ttu-id="6f864-171">Если указать значение BlobStorage для параметра *вида* , необходимо указать значение параметра *AccessTier* .</span><span class="sxs-lookup"><span data-stu-id="6f864-171">If you specify a value of BlobStorage for the *Kind* parameter, you must specify a value for the *AccessTier* parameter.</span></span>

<span data-ttu-id="6f864-172">Если для этого параметра *типа* задано значение хранилища, не указывайте параметр *AccessTier* .</span><span class="sxs-lookup"><span data-stu-id="6f864-172">If you specify a value of Storage for this *Kind* parameter, do not specify the *AccessTier* parameter.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f864-173">-UseSubDomain</span><span class="sxs-lookup"><span data-stu-id="6f864-173">-UseSubDomain</span></span>
<span data-ttu-id="6f864-174">Указывает, нужно ли включить косвенную проверку CName.</span><span class="sxs-lookup"><span data-stu-id="6f864-174">Indicates whether to enable indirect CName validation.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f864-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f864-175">CommonParameters</span></span>
<span data-ttu-id="6f864-176">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6f864-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f864-177">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f864-177">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f864-178">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6f864-178">INPUTS</span></span>

### <span data-ttu-id="6f864-179">Ничего</span><span class="sxs-lookup"><span data-stu-id="6f864-179">None</span></span>
<span data-ttu-id="6f864-180">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="6f864-180">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6f864-181">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6f864-181">OUTPUTS</span></span>

## <span data-ttu-id="6f864-182">Пуск</span><span class="sxs-lookup"><span data-stu-id="6f864-182">NOTES</span></span>

## <span data-ttu-id="6f864-183">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6f864-183">RELATED LINKS</span></span>

[<span data-ttu-id="6f864-184">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6f864-184">Get-AzureRmStorageAccount</span></span>](./Get-AzureRmStorageAccount.md)

[<span data-ttu-id="6f864-185">Remove-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6f864-185">Remove-AzureRmStorageAccount</span></span>](./Remove-AzureRmStorageAccount.md)

[<span data-ttu-id="6f864-186">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6f864-186">Set-AzureRmStorageAccount</span></span>](./Set-AzureRmStorageAccount.md)

---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: A3DA1205-B8FB-4B4C-9C40-AD303D038EDF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/New-AzureRmStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/New-AzureRmStorageAccount.md
ms.openlocfilehash: 50384630658f7626ee02ca1dee223e82bf122ef1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93735024"
---
# <span data-ttu-id="eb3d6-101">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="eb3d6-101">New-AzureRmStorageAccount</span></span>

## <span data-ttu-id="eb3d6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="eb3d6-102">SYNOPSIS</span></span>
<span data-ttu-id="eb3d6-103">Создание учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="eb3d6-103">Creates a Storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eb3d6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="eb3d6-104">SYNTAX</span></span>

```
New-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String>
 [-Location] <String> [[-Kind] <String>] [[-AccessTier] <String>] [[-CustomDomainName] <String>]
 [[-UseSubDomain] <Boolean>] [[-EnableEncryptionService] <EncryptionSupportServiceEnum>] [[-Tag] <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="eb3d6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="eb3d6-105">DESCRIPTION</span></span>
<span data-ttu-id="eb3d6-106">Командлет **New-AzureRmStorageAccount** создает учетную запись хранения Azure.</span><span class="sxs-lookup"><span data-stu-id="eb3d6-106">The **New-AzureRmStorageAccount** cmdlet creates an Azure Storage account.</span></span>

## <span data-ttu-id="eb3d6-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="eb3d6-107">EXAMPLES</span></span>

### <span data-ttu-id="eb3d6-108">Пример 1: создание учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="eb3d6-108">Example 1: Create a Storage Account</span></span>
```
PS C:\>New-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -Location "US West" -SkuName "Standard_GRS"
```

<span data-ttu-id="eb3d6-109">Эта команда создает учетную запись хранения для имени группы ресурсов MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="eb3d6-109">This command creates a Storage account for the resource group name MyResourceGroup.</span></span>

### <span data-ttu-id="eb3d6-110">Пример 2: создание учетной записи хранилища BLOB-объектов, использующей шифрование службы хранилища</span><span class="sxs-lookup"><span data-stu-id="eb3d6-110">Example 2: Create a Blob Storage account that uses Storage Service Encryption</span></span>
```
PS C:\>New-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -Location "US West" -SkuName "Standard_GRS" -EnableEncryptionService Blob -Kind "BlobStorage" -AccessTier Hot
```

<span data-ttu-id="eb3d6-111">Эта команда создает учетную запись хранилища BLOB-объектов, которая использует тип горячего доступа.</span><span class="sxs-lookup"><span data-stu-id="eb3d6-111">This command creates a Blob Storage account that uses the hot access type.</span></span>
<span data-ttu-id="eb3d6-112">Учетная запись включила шифрование службы хранилища в службе больших двоичных объектов.</span><span class="sxs-lookup"><span data-stu-id="eb3d6-112">The account has enabled Storage Service encryption on Blob Service.</span></span>

### <span data-ttu-id="eb3d6-113">Пример 3: создание учетной записи хранения, которая обеспечивает шифрование службы хранилища для BLOB-объектов и файловых служб, а затем создает и назначает удостоверение для Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="eb3d6-113">Example 3: Create a Storage Account that Enables Storage Service Encryption on Blob and File Services, and Generate and Assign an Identity for Azure KeyVault.</span></span>
```
PS C:\>New-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -Location "US West" -SkuName "Standard_GRS" -EnableEncryptionService "Blob,File" -AssignIdentity
```

<span data-ttu-id="eb3d6-114">Эта команда создает учетную запись хранения, которая включила шифрование службы хранилища для BLOB-объектов и файловых служб.</span><span class="sxs-lookup"><span data-stu-id="eb3d6-114">This command creates a Storage account that enabled Storage Service encryption on Blob and File Services.</span></span>  <span data-ttu-id="eb3d6-115">Кроме того, она генерирует и назначает удостоверение, которое можно использовать для управления ключами учетной записи через Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="eb3d6-115">It also generates and assigns an identity that can be used to manage account keys through Azure KeyVault.</span></span>

## <span data-ttu-id="eb3d6-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="eb3d6-116">PARAMETERS</span></span>

### <span data-ttu-id="eb3d6-117">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="eb3d6-117">-AccessTier</span></span>
<span data-ttu-id="eb3d6-118">Указывает уровень доступа учетной записи хранения, созданной этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="eb3d6-118">Specifies the access tier of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="eb3d6-119">Допустимые значения этого параметра: горячий и крутой.</span><span class="sxs-lookup"><span data-stu-id="eb3d6-119">The acceptable values for this parameter are: Hot and Cool.</span></span>

<span data-ttu-id="eb3d6-120">Если указать значение BlobStorage для параметра *вида* , необходимо указать значение параметра *AccessTier* .</span><span class="sxs-lookup"><span data-stu-id="eb3d6-120">If you specify a value of BlobStorage for the *Kind* parameter, you must specify a value for the *AccessTier* parameter.</span></span>

<span data-ttu-id="eb3d6-121">Если для этого параметра *типа* задано значение хранилища, не указывайте параметр *AccessTier* .</span><span class="sxs-lookup"><span data-stu-id="eb3d6-121">If you specify a value of Storage for this *Kind* parameter, do not specify the *AccessTier* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb3d6-122">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="eb3d6-122">-AssignIdentity</span></span>
<span data-ttu-id="eb3d6-123">Создание и назначение нового удостоверения учетной записи хранения для этой учетной записи хранения для использования со службами управления ключами, такими как Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="eb3d6-123">Generate and assign a new Storage Account Identity for this storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="eb3d6-124">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="eb3d6-124">-CustomDomainName</span></span>
<span data-ttu-id="eb3d6-125">Указывает имя настраиваемого домена учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="eb3d6-125">Specifies the name of the custom domain of the Storage account.</span></span>
<span data-ttu-id="eb3d6-126">По умолчанию используется значение Storage.</span><span class="sxs-lookup"><span data-stu-id="eb3d6-126">The default value is Storage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb3d6-127">-EnableEncryptionService</span><span class="sxs-lookup"><span data-stu-id="eb3d6-127">-EnableEncryptionService</span></span>
<span data-ttu-id="eb3d6-128">Указывает, включает ли этот командлет шифрование службы хранилища для службы хранилища.</span><span class="sxs-lookup"><span data-stu-id="eb3d6-128">Indicates whether this cmdlet enables Storage Service encryption on the Storage Service.</span></span>
<span data-ttu-id="eb3d6-129">Поддерживаются двоичные файлы и службы Azure.</span><span class="sxs-lookup"><span data-stu-id="eb3d6-129">Azure Blob and Azure File Services are supported.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Management.Storage.StorageAccountBaseCmdlet+EncryptionSupportServiceEnum]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb3d6-130">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="eb3d6-130">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="eb3d6-131">Указывает, следует ли учетной записи хранения включать трафик HTTPS.</span><span class="sxs-lookup"><span data-stu-id="eb3d6-131">Indicates whether or not the Storage Account only enable https traffic.</span></span>

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

### <span data-ttu-id="eb3d6-132">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="eb3d6-132">-InformationAction</span></span>
<span data-ttu-id="eb3d6-133">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="eb3d6-133">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="eb3d6-134">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="eb3d6-134">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="eb3d6-135">Продолжал</span><span class="sxs-lookup"><span data-stu-id="eb3d6-135">Continue</span></span>
- <span data-ttu-id="eb3d6-136">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="eb3d6-136">Ignore</span></span>
- <span data-ttu-id="eb3d6-137">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="eb3d6-137">Inquire</span></span>
- <span data-ttu-id="eb3d6-138">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="eb3d6-138">SilentlyContinue</span></span>
- <span data-ttu-id="eb3d6-139">Остановить</span><span class="sxs-lookup"><span data-stu-id="eb3d6-139">Stop</span></span>
- <span data-ttu-id="eb3d6-140">Рвать</span><span class="sxs-lookup"><span data-stu-id="eb3d6-140">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb3d6-141">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="eb3d6-141">-InformationVariable</span></span>
<span data-ttu-id="eb3d6-142">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="eb3d6-142">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb3d6-143">-Видах</span><span class="sxs-lookup"><span data-stu-id="eb3d6-143">-Kind</span></span>
<span data-ttu-id="eb3d6-144">Указывает вариант учетной записи хранения, создаваемой этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="eb3d6-144">Specifies the kind of Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="eb3d6-145">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="eb3d6-145">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="eb3d6-146">Склад.</span><span class="sxs-lookup"><span data-stu-id="eb3d6-146">Storage.</span></span>
<span data-ttu-id="eb3d6-147">Общая цель учетной записи хранения, которая поддерживает хранение больших двоичных объектов, таблиц, очередей, файлов и дисков.</span><span class="sxs-lookup"><span data-stu-id="eb3d6-147">General purpose storage account that supports storage of Blobs, Tables, Queues, Files and Disks.</span></span>
 
- <span data-ttu-id="eb3d6-148">BlobStorage.</span><span class="sxs-lookup"><span data-stu-id="eb3d6-148">BlobStorage.</span></span>
<span data-ttu-id="eb3d6-149">Учетная запись хранилища BLOB-объектов, поддерживающая только хранение больших двоичных объектов.</span><span class="sxs-lookup"><span data-stu-id="eb3d6-149">Blob storage account which supports storage of Blobs only.</span></span>
 

<span data-ttu-id="eb3d6-150">По умолчанию используется значение Storage.</span><span class="sxs-lookup"><span data-stu-id="eb3d6-150">The default value is Storage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb3d6-151">-Location</span><span class="sxs-lookup"><span data-stu-id="eb3d6-151">-Location</span></span>
<span data-ttu-id="eb3d6-152">Указывает расположение учетной записи хранения, которую нужно создать.</span><span class="sxs-lookup"><span data-stu-id="eb3d6-152">Specifies the location of the Storage account to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb3d6-153">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="eb3d6-153">-Name</span></span>
<span data-ttu-id="eb3d6-154">Указывает имя учетной записи хранения, которую нужно создать.</span><span class="sxs-lookup"><span data-stu-id="eb3d6-154">Specifies the name of the Storage account to create.</span></span>

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

### <span data-ttu-id="eb3d6-155">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="eb3d6-155">-NetworkRuleSet</span></span>
<span data-ttu-id="eb3d6-156">NetworkRuleSet учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="eb3d6-156">Storage Account NetworkRuleSet</span></span>

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

### <span data-ttu-id="eb3d6-157">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb3d6-157">-ResourceGroupName</span></span>
<span data-ttu-id="eb3d6-158">Указывает имя группы ресурсов, в которую нужно добавить учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="eb3d6-158">Specifies the name of the resource group in which to add the Storage account.</span></span>

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

### <span data-ttu-id="eb3d6-159">-SkuName</span><span class="sxs-lookup"><span data-stu-id="eb3d6-159">-SkuName</span></span>
<span data-ttu-id="eb3d6-160">Указывает имя SKU учетной записи хранения, созданной этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="eb3d6-160">Specifies the SKU name of the storage account that this cmdlet creates.</span></span>
<span data-ttu-id="eb3d6-161">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="eb3d6-161">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="eb3d6-162">Standard_LRS.</span><span class="sxs-lookup"><span data-stu-id="eb3d6-162">Standard_LRS.</span></span>
<span data-ttu-id="eb3d6-163">Локально избыточное хранилище.</span><span class="sxs-lookup"><span data-stu-id="eb3d6-163">Locally-redundant storage.</span></span> 
- <span data-ttu-id="eb3d6-164">Standard_ZRS.</span><span class="sxs-lookup"><span data-stu-id="eb3d6-164">Standard_ZRS.</span></span>
<span data-ttu-id="eb3d6-165">Зона — избыточное хранилище.</span><span class="sxs-lookup"><span data-stu-id="eb3d6-165">Zone-redundant storage.</span></span>
- <span data-ttu-id="eb3d6-166">Standard_GRS.</span><span class="sxs-lookup"><span data-stu-id="eb3d6-166">Standard_GRS.</span></span>
<span data-ttu-id="eb3d6-167">Геоизбыточное хранилище.</span><span class="sxs-lookup"><span data-stu-id="eb3d6-167">Geo-redundant storage.</span></span> 
- <span data-ttu-id="eb3d6-168">Standard_RAGRS.</span><span class="sxs-lookup"><span data-stu-id="eb3d6-168">Standard_RAGRS.</span></span>
<span data-ttu-id="eb3d6-169">Доступное для чтения геоизбыточное хранилище.</span><span class="sxs-lookup"><span data-stu-id="eb3d6-169">Read access geo-redundant storage.</span></span> 
- <span data-ttu-id="eb3d6-170">Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="eb3d6-170">Premium_LRS.</span></span>
<span data-ttu-id="eb3d6-171">Локально — избыточное хранилище Premium.</span><span class="sxs-lookup"><span data-stu-id="eb3d6-171">Premium locally-redundant storage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountType, AccountType, Type

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb3d6-172">-Тег</span><span class="sxs-lookup"><span data-stu-id="eb3d6-172">-Tag</span></span>
<span data-ttu-id="eb3d6-173">Если указать значение BlobStorage для параметра *вида* , необходимо указать значение параметра *AccessTier* .</span><span class="sxs-lookup"><span data-stu-id="eb3d6-173">If you specify a value of BlobStorage for the *Kind* parameter, you must specify a value for the *AccessTier* parameter.</span></span>

<span data-ttu-id="eb3d6-174">Если для этого параметра *типа* задано значение хранилища, не указывайте параметр *AccessTier* .</span><span class="sxs-lookup"><span data-stu-id="eb3d6-174">If you specify a value of Storage for this *Kind* parameter, do not specify the *AccessTier* parameter.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb3d6-175">-UseSubDomain</span><span class="sxs-lookup"><span data-stu-id="eb3d6-175">-UseSubDomain</span></span>
<span data-ttu-id="eb3d6-176">Указывает, нужно ли включить косвенную проверку CName.</span><span class="sxs-lookup"><span data-stu-id="eb3d6-176">Indicates whether to enable indirect CName validation.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb3d6-177">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb3d6-177">-DefaultProfile</span></span>
<span data-ttu-id="eb3d6-178">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="eb3d6-178">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eb3d6-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb3d6-179">CommonParameters</span></span>
<span data-ttu-id="eb3d6-180">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="eb3d6-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb3d6-181">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb3d6-181">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb3d6-182">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="eb3d6-182">INPUTS</span></span>

## <span data-ttu-id="eb3d6-183">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="eb3d6-183">OUTPUTS</span></span>

## <span data-ttu-id="eb3d6-184">Пуск</span><span class="sxs-lookup"><span data-stu-id="eb3d6-184">NOTES</span></span>

## <span data-ttu-id="eb3d6-185">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="eb3d6-185">RELATED LINKS</span></span>

[<span data-ttu-id="eb3d6-186">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="eb3d6-186">Get-AzureRmStorageAccount</span></span>](./Get-AzureRmStorageAccount.md)

[<span data-ttu-id="eb3d6-187">Remove-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="eb3d6-187">Remove-AzureRmStorageAccount</span></span>](./Remove-AzureRmStorageAccount.md)

[<span data-ttu-id="eb3d6-188">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="eb3d6-188">Set-AzureRmStorageAccount</span></span>](./Set-AzureRmStorageAccount.md)



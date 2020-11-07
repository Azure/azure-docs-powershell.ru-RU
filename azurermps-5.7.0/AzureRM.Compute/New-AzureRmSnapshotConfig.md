---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmSnapshotConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmSnapshotConfig.md
ms.openlocfilehash: ee3dd849a8f3877ac19ce86a7257d28fc18575c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732755"
---
# <span data-ttu-id="343e4-101">New-AzureRmSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="343e4-101">New-AzureRmSnapshotConfig</span></span>

## <span data-ttu-id="343e4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="343e4-102">SYNOPSIS</span></span>
<span data-ttu-id="343e4-103">Создание настраиваемого объекта снимка.</span><span class="sxs-lookup"><span data-stu-id="343e4-103">Creates a configurable snapshot object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="343e4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="343e4-104">SYNTAX</span></span>

```
New-AzureRmSnapshotConfig [-SkuName <StorageAccountTypes>] [[-OsType] <OperatingSystemTypes>]
 [[-DiskSizeGB] <Int32>] [[-Location] <String>] [-Tag <Hashtable>] [-CreateOption <DiskCreateOption>]
 [-StorageAccountId <String>] [-ImageReference <ImageDiskReference>] [-SourceUri <String>]
 [-SourceResourceId <String>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="343e4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="343e4-105">DESCRIPTION</span></span>
<span data-ttu-id="343e4-106">Командлет **New-AzureRmSnapshotConfig** создает настраиваемый объект снимка.</span><span class="sxs-lookup"><span data-stu-id="343e4-106">The **New-AzureRmSnapshotConfig** cmdlet creates a configurable snapshot object.</span></span>

## <span data-ttu-id="343e4-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="343e4-107">EXAMPLES</span></span>

### <span data-ttu-id="343e4-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="343e4-108">Example 1</span></span>
```
PS C:\> $snapshotconfig = New-AzureRmSnapshotConfig -Location 'Central US' -DiskSizeGB 5 -AccountType StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $snapshotconfig = Set-AzureRmSnapshotDiskEncryptionKey -Snapshot $snapshotconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $snapshotconfig = Set-AzureRmSnapshotKeyEncryptionKey -Snapshot $snapshotconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshotconfig;
```

<span data-ttu-id="343e4-109">В первой команде создается локальный пустой объект Snapshot с размером 5GB в Standard_LRS типе учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="343e4-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="343e4-110">Она также задает тип операционной системы Windows и включает параметры шифрования.</span><span class="sxs-lookup"><span data-stu-id="343e4-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="343e4-111">Вторая и третья команды устанавливают параметры ключа шифрования диска и ключа шифрования для объекта snapshot.</span><span class="sxs-lookup"><span data-stu-id="343e4-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="343e4-112">Последняя команда принимает объект snapshot и создает моментальный снимок с именем "Snapshot01" в группе ресурсов "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="343e4-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="343e4-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="343e4-113">PARAMETERS</span></span>

### <span data-ttu-id="343e4-114">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="343e4-114">-CreateOption</span></span>
<span data-ttu-id="343e4-115">Указывает, создает ли этот командлет диск на виртуальной машине из платформы или пользовательского образа, создает пустой диск или прикрепляет существующий диск.</span><span class="sxs-lookup"><span data-stu-id="343e4-115">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

```yaml
Type: DiskCreateOption
Parameter Sets: (All)
Aliases: 
Accepted values: Empty, Attach, FromImage, Import, Copy, Restore

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="343e4-116">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="343e4-116">-DiskEncryptionKey</span></span>
<span data-ttu-id="343e4-117">Задает объект ключа шифрования диска для снимка.</span><span class="sxs-lookup"><span data-stu-id="343e4-117">Specifies the disk encryption key object on a snapshot.</span></span>

```yaml
Type: KeyVaultAndSecretReference
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="343e4-118">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="343e4-118">-DiskSizeGB</span></span>
<span data-ttu-id="343e4-119">Задает размер диска в ГБ.</span><span class="sxs-lookup"><span data-stu-id="343e4-119">Specifies the size of the disk in GB.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="343e4-120">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="343e4-120">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="343e4-121">Включите параметры шифрования.</span><span class="sxs-lookup"><span data-stu-id="343e4-121">Enable encryption settings.</span></span>

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

### <span data-ttu-id="343e4-122">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="343e4-122">-ImageReference</span></span>
<span data-ttu-id="343e4-123">Указывает ссылку на изображение в снимке.</span><span class="sxs-lookup"><span data-stu-id="343e4-123">Specifies the image reference on a snapshot.</span></span>

```yaml
Type: ImageDiskReference
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="343e4-124">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="343e4-124">-KeyEncryptionKey</span></span>
<span data-ttu-id="343e4-125">Задает ключ шифрования ключа для снимка.</span><span class="sxs-lookup"><span data-stu-id="343e4-125">Specifies the Key encryption key on a snapshot.</span></span>

```yaml
Type: KeyVaultAndKeyReference
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="343e4-126">-Location</span><span class="sxs-lookup"><span data-stu-id="343e4-126">-Location</span></span>
<span data-ttu-id="343e4-127">Задает расположение.</span><span class="sxs-lookup"><span data-stu-id="343e4-127">Specifies a location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="343e4-128">-OsType</span><span class="sxs-lookup"><span data-stu-id="343e4-128">-OsType</span></span>
<span data-ttu-id="343e4-129">Указывает тип операционной системы.</span><span class="sxs-lookup"><span data-stu-id="343e4-129">Specifies the OS type.</span></span>

```yaml
Type: OperatingSystemTypes
Parameter Sets: (All)
Aliases: 
Accepted values: Windows, Linux

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="343e4-130">-SkuName</span><span class="sxs-lookup"><span data-stu-id="343e4-130">-SkuName</span></span>
<span data-ttu-id="343e4-131">Указывает имя SKU учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="343e4-131">Specifies the Sku name of the storage account.</span></span>

```yaml
Type: StorageAccountTypes
Parameter Sets: (All)
Aliases: AccountType

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="343e4-132">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="343e4-132">-SourceResourceId</span></span>
<span data-ttu-id="343e4-133">Указывает исходный идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="343e4-133">Specifies the source resource ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="343e4-134">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="343e4-134">-SourceUri</span></span>
<span data-ttu-id="343e4-135">Указывает универсальный код ресурса (URI) источника.</span><span class="sxs-lookup"><span data-stu-id="343e4-135">Specifies the source Uri.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="343e4-136">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="343e4-136">-StorageAccountId</span></span>
<span data-ttu-id="343e4-137">Указывает идентификатор учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="343e4-137">Specifies the storage account ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="343e4-138">-Тег</span><span class="sxs-lookup"><span data-stu-id="343e4-138">-Tag</span></span>
<span data-ttu-id="343e4-139">Указывает, что ресурсы и группы ресурсов можно пометить с помощью набора пар "имя-значение".</span><span class="sxs-lookup"><span data-stu-id="343e4-139">Specifies that resources and resource groups can be tagged with a set of name-value pairs.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="343e4-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="343e4-140">-Confirm</span></span>
<span data-ttu-id="343e4-141">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="343e4-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="343e4-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="343e4-142">-WhatIf</span></span>
<span data-ttu-id="343e4-143">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="343e4-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="343e4-144">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="343e4-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="343e4-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="343e4-145">CommonParameters</span></span>
<span data-ttu-id="343e4-146">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="343e4-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="343e4-147">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="343e4-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="343e4-148">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="343e4-148">INPUTS</span></span>

### <span data-ttu-id="343e4-149">System. Nullable "1 [[Microsoft. Azure. Management. COMPUTE. Model. StorageAccountTypes, Microsoft. Azure. Management. COMPUTE, Version = 14.0.0.0, культура =" нейтрально ", PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="343e4-149">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.StorageAccountTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>
<span data-ttu-id="343e4-150">System. Nullable `1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable` 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]] System. String System. Nullable. Hashtable System. null `1[[Microsoft.Azure.Management.Compute.Models.DiskCreateOption, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
Microsoft.Azure.Management.Compute.Models.ImageDiskReference
System.Nullable` 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]] Microsoft. Azure. Management. COMPUTE. Models. KeyVaultAndSecretReference Microsoft. Azure. Management. Recompute. моделирует. KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="343e4-150">System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]] System.String System.Collections.Hashtable System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.DiskCreateOption, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
Microsoft.Azure.Management.Compute.Models.ImageDiskReference
System.Nullable`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]] Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="343e4-151">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="343e4-151">OUTPUTS</span></span>

### <span data-ttu-id="343e4-152">Microsoft. Azure. Management. COMPUTE. Models. Snapshot</span><span class="sxs-lookup"><span data-stu-id="343e4-152">Microsoft.Azure.Management.Compute.Models.Snapshot</span></span>

## <span data-ttu-id="343e4-153">Пуск</span><span class="sxs-lookup"><span data-stu-id="343e4-153">NOTES</span></span>

## <span data-ttu-id="343e4-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="343e4-154">RELATED LINKS</span></span>


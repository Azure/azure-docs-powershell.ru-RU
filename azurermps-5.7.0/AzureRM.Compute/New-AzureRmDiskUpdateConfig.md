---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmDiskUpdateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmDiskUpdateConfig.md
ms.openlocfilehash: 68a6e53e6ad024411c0775a21bbdbb0d0b8c75f2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563696"
---
# <span data-ttu-id="2febe-101">New-AzureRmDiskUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="2febe-101">New-AzureRmDiskUpdateConfig</span></span>

## <span data-ttu-id="2febe-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2febe-102">SYNOPSIS</span></span>
<span data-ttu-id="2febe-103">Создание настраиваемого объекта обновления диска.</span><span class="sxs-lookup"><span data-stu-id="2febe-103">Creates a configurable disk update object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2febe-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2febe-104">SYNTAX</span></span>

```
New-AzureRmDiskUpdateConfig [-SkuName <StorageAccountTypes>] [[-OsType] <OperatingSystemTypes>]
 [[-DiskSizeGB] <Int32>] [[-Tag] <Hashtable>] [-CreateOption <DiskCreateOption>] [-StorageAccountId <String>]
 [-ImageReference <ImageDiskReference>] [-SourceUri <String>] [-SourceResourceId <String>]
 [-EncryptionSettingsEnabled <Boolean>] [-DiskEncryptionKey <KeyVaultAndSecretReference>]
 [-KeyEncryptionKey <KeyVaultAndKeyReference>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2febe-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2febe-105">DESCRIPTION</span></span>
<span data-ttu-id="2febe-106">Командлет **New-AzureRmDiskUpdateConfig** создает настраиваемый объект обновления диска.</span><span class="sxs-lookup"><span data-stu-id="2febe-106">The **New-AzureRmDiskUpdateConfig** cmdlet creates a configurable disk update object.</span></span>

## <span data-ttu-id="2febe-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2febe-107">EXAMPLES</span></span>

### <span data-ttu-id="2febe-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2febe-108">Example 1</span></span>
```
PS C:\> $diskupdateconfig = New-AzureRmDiskUpdateConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskupdateconfig = Set-AzureRmDiskUpdateDiskEncryptionKey -DiskUpdate $diskupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskupdateconfig = Set-AzureRmDiskUpdateKeyEncryptionKey -DiskUpdate $diskupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -DiskUpdate $diskupdateconfig;
```

<span data-ttu-id="2febe-109">Первая команда создает локальный пустой объект обновления диска с размером 10 ГБ в Premium_LRS тип учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="2febe-109">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="2febe-110">Она также задает тип операционной системы Windows и включает параметры шифрования.</span><span class="sxs-lookup"><span data-stu-id="2febe-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="2febe-111">Вторая и третья команды устанавливают параметры ключа шифрования диска и ключа шифрования для объекта обновления диска.</span><span class="sxs-lookup"><span data-stu-id="2febe-111">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="2febe-112">Последняя команда принимает объект обновления диска и обновляет существующий диск с именем "Disk01" в группе ресурсов "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="2febe-112">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="2febe-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="2febe-113">Example 2</span></span>
```
PS C:\> New-AzureRmDiskUpdateConfig -DiskSizeGB 10 | Update-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01';
```

<span data-ttu-id="2febe-114">Эта команда обновляет существующий диск с именем "Disk01" в группе ресурсов "ResourceGroup01" на диск размером 10 ГБ.</span><span class="sxs-lookup"><span data-stu-id="2febe-114">This command updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="2febe-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2febe-115">PARAMETERS</span></span>

### <span data-ttu-id="2febe-116">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="2febe-116">-CreateOption</span></span>
<span data-ttu-id="2febe-117">Указывает, создает ли этот командлет диск на виртуальной машине из платформы или пользовательского образа, создает пустой диск или прикрепляет существующий диск.</span><span class="sxs-lookup"><span data-stu-id="2febe-117">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

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

### <span data-ttu-id="2febe-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="2febe-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="2febe-119">Указывает объект ключа шифрования диска на диске.</span><span class="sxs-lookup"><span data-stu-id="2febe-119">Specifies the disk encryption key object on a disk.</span></span>

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

### <span data-ttu-id="2febe-120">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="2febe-120">-DiskSizeGB</span></span>
<span data-ttu-id="2febe-121">Задает размер диска в ГБ.</span><span class="sxs-lookup"><span data-stu-id="2febe-121">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="2febe-122">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="2febe-122">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="2febe-123">Включите параметры шифрования.</span><span class="sxs-lookup"><span data-stu-id="2febe-123">Enable encryption settings.</span></span>

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

### <span data-ttu-id="2febe-124">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="2febe-124">-ImageReference</span></span>
<span data-ttu-id="2febe-125">Указывает ссылку на изображение на диске.</span><span class="sxs-lookup"><span data-stu-id="2febe-125">Specifies the image reference on a disk.</span></span>

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

### <span data-ttu-id="2febe-126">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="2febe-126">-KeyEncryptionKey</span></span>
<span data-ttu-id="2febe-127">Задает ключ шифрования ключа на диске.</span><span class="sxs-lookup"><span data-stu-id="2febe-127">Specifies the Key encryption key on a disk.</span></span>

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

### <span data-ttu-id="2febe-128">-OsType</span><span class="sxs-lookup"><span data-stu-id="2febe-128">-OsType</span></span>
<span data-ttu-id="2febe-129">Указывает тип операционной системы.</span><span class="sxs-lookup"><span data-stu-id="2febe-129">Specifies the OS type.</span></span>

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

### <span data-ttu-id="2febe-130">-SkuName</span><span class="sxs-lookup"><span data-stu-id="2febe-130">-SkuName</span></span>
<span data-ttu-id="2febe-131">Указывает имя SKU учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="2febe-131">Specifies the Sku name of the storage account.</span></span>

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

### <span data-ttu-id="2febe-132">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="2febe-132">-SourceResourceId</span></span>
<span data-ttu-id="2febe-133">Указывает исходный идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="2febe-133">Specifies the source resource ID.</span></span>

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

### <span data-ttu-id="2febe-134">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="2febe-134">-SourceUri</span></span>
<span data-ttu-id="2febe-135">Указывает универсальный код ресурса (URI) источника.</span><span class="sxs-lookup"><span data-stu-id="2febe-135">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="2febe-136">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="2febe-136">-StorageAccountId</span></span>
<span data-ttu-id="2febe-137">Указывает идентификатор учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="2febe-137">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="2febe-138">-Тег</span><span class="sxs-lookup"><span data-stu-id="2febe-138">-Tag</span></span>
<span data-ttu-id="2febe-139">Указывает, что ресурсы и группы ресурсов можно пометить с помощью набора пар "имя-значение".</span><span class="sxs-lookup"><span data-stu-id="2febe-139">Specifies that resources and resource groups can be tagged with a set of name-value pairs.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2febe-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2febe-140">-Confirm</span></span>
<span data-ttu-id="2febe-141">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2febe-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2febe-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2febe-142">-WhatIf</span></span>
<span data-ttu-id="2febe-143">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2febe-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2febe-144">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2febe-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2febe-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2febe-145">CommonParameters</span></span>
<span data-ttu-id="2febe-146">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2febe-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2febe-147">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2febe-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2febe-148">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2febe-148">INPUTS</span></span>

### <span data-ttu-id="2febe-149">System. Nullable "1 [[Microsoft. Azure. Management. COMPUTE. Model. StorageAccountTypes, Microsoft. Azure. Management. COMPUTE, Version = 14.0.0.0, культура =" нейтрально ", PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="2febe-149">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.StorageAccountTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>
<span data-ttu-id="2febe-150">System. Nullable `1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable` 1 [[System. Int32, mscorlib, Version = 4.0.0.0, культура = нейтраль, PublicKeyToken = b77a5c561934e089]] System. Collections. Hashtable. Nullable `1[[Microsoft.Azure.Management.Compute.Models.DiskCreateOption, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.String
Microsoft.Azure.Management.Compute.Models.ImageDiskReference
System.Nullable` 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, культура = нейтраль, PublicKeyToken = b77a5c561934e089]] Microsoft. Azure. Management. COMPUTE. Models. KeyVaultAndSecretReference Microsoft. Azure. System. COMPUTE. Models. KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="2febe-150">System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]] System.Collections.Hashtable System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.DiskCreateOption, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.String
Microsoft.Azure.Management.Compute.Models.ImageDiskReference
System.Nullable`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]] Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="2febe-151">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2febe-151">OUTPUTS</span></span>

### <span data-ttu-id="2febe-152">Microsoft. Azure. Management. COMPUTE. Models. DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="2febe-152">Microsoft.Azure.Management.Compute.Models.DiskUpdate</span></span>

## <span data-ttu-id="2febe-153">Пуск</span><span class="sxs-lookup"><span data-stu-id="2febe-153">NOTES</span></span>

## <span data-ttu-id="2febe-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2febe-154">RELATED LINKS</span></span>


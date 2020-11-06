---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmDiskConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmDiskConfig.md
ms.openlocfilehash: 70ee169903ca70b539e8eda2043ffcd0fd2928c1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93570083"
---
# <span data-ttu-id="d9574-101">New-AzureRmDiskConfig</span><span class="sxs-lookup"><span data-stu-id="d9574-101">New-AzureRmDiskConfig</span></span>

## <span data-ttu-id="d9574-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d9574-102">SYNOPSIS</span></span>
<span data-ttu-id="d9574-103">Создание настраиваемого объекта диска.</span><span class="sxs-lookup"><span data-stu-id="d9574-103">Creates a configurable disk object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d9574-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d9574-104">SYNTAX</span></span>

```
New-AzureRmDiskConfig [[-SkuName] <StorageAccountTypes>] [[-OsType] <OperatingSystemTypes>]
 [[-DiskSizeGB] <Int32>] [[-Location] <String>] [-Zone <String[]>] [-Tag <Hashtable>]
 [-CreateOption <DiskCreateOption>] [-StorageAccountId <String>] [-ImageReference <ImageDiskReference>]
 [-SourceUri <String>] [-SourceResourceId <String>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9574-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d9574-105">DESCRIPTION</span></span>
<span data-ttu-id="d9574-106">Командлет **New-AzureRmDiskConfig** создает настраиваемый объект диска.</span><span class="sxs-lookup"><span data-stu-id="d9574-106">The **New-AzureRmDiskConfig** cmdlet creates a configurable disk object.</span></span>

## <span data-ttu-id="d9574-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d9574-107">EXAMPLES</span></span>

### <span data-ttu-id="d9574-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d9574-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzureRmDiskConfig -Location 'Central US' -DiskSizeGB 5 -AccountType StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskconfig = Set-AzureRmDiskDiskEncryptionKey -Disk $diskconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskconfig = Set-AzureRmDiskKeyEncryptionKey -Disk $diskconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="d9574-109">Первая команда создает локальный пустой объект диска с размером 5GB в Standard_LRS типе учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="d9574-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="d9574-110">Она также задает тип операционной системы Windows и включает параметры шифрования.</span><span class="sxs-lookup"><span data-stu-id="d9574-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="d9574-111">Вторая и третья команды устанавливают параметры ключа шифрования диска и ключа шифрования для объекта диска.</span><span class="sxs-lookup"><span data-stu-id="d9574-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span>
<span data-ttu-id="d9574-112">Последняя команда принимает объект диска и создает диск с именем "Disk01" в группе ресурсов "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="d9574-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="d9574-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d9574-113">PARAMETERS</span></span>

### <span data-ttu-id="d9574-114">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="d9574-114">-CreateOption</span></span>
<span data-ttu-id="d9574-115">Указывает, создает ли этот командлет диск на виртуальной машине из платформы или пользовательского образа, создает пустой диск или прикрепляет существующий диск.</span><span class="sxs-lookup"><span data-stu-id="d9574-115">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.DiskCreateOption]
Parameter Sets: (All)
Aliases: 
Accepted values: Empty, Attach, FromImage, Import, Copy

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9574-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9574-116">-DefaultProfile</span></span>
<span data-ttu-id="d9574-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d9574-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d9574-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="d9574-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="d9574-119">Указывает объект ключа шифрования диска на диске.</span><span class="sxs-lookup"><span data-stu-id="d9574-119">Specifies the disk encryption key object on a disk.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9574-120">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="d9574-120">-DiskSizeGB</span></span>
<span data-ttu-id="d9574-121">Задает размер диска в ГБ.</span><span class="sxs-lookup"><span data-stu-id="d9574-121">Specifies the size of the disk in GB.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9574-122">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="d9574-122">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="d9574-123">Включите параметры шифрования.</span><span class="sxs-lookup"><span data-stu-id="d9574-123">Enable encryption settings.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9574-124">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="d9574-124">-ImageReference</span></span>
<span data-ttu-id="d9574-125">Указывает ссылку на изображение на диске.</span><span class="sxs-lookup"><span data-stu-id="d9574-125">Specifies the image reference on a disk.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.ImageDiskReference
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9574-126">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="d9574-126">-KeyEncryptionKey</span></span>
<span data-ttu-id="d9574-127">Задает ключ шифрования ключа на диске.</span><span class="sxs-lookup"><span data-stu-id="d9574-127">Specifies the Key encryption key on a disk.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9574-128">-Location</span><span class="sxs-lookup"><span data-stu-id="d9574-128">-Location</span></span>
<span data-ttu-id="d9574-129">Задает расположение.</span><span class="sxs-lookup"><span data-stu-id="d9574-129">Specifies a location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9574-130">-OsType</span><span class="sxs-lookup"><span data-stu-id="d9574-130">-OsType</span></span>
<span data-ttu-id="d9574-131">Указывает тип операционной системы.</span><span class="sxs-lookup"><span data-stu-id="d9574-131">Specifies the OS type.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes]
Parameter Sets: (All)
Aliases: 
Accepted values: Windows, Linux

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9574-132">-SkuName</span><span class="sxs-lookup"><span data-stu-id="d9574-132">-SkuName</span></span>
<span data-ttu-id="d9574-133">Указывает имя SKU учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="d9574-133">Specifies the Sku name of the storage account.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.StorageAccountTypes]
Parameter Sets: (All)
Aliases: AccountType
Accepted values: StandardLRS, PremiumLRS

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9574-134">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="d9574-134">-SourceResourceId</span></span>
<span data-ttu-id="d9574-135">Указывает исходный идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="d9574-135">Specifies the  source resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9574-136">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="d9574-136">-SourceUri</span></span>
<span data-ttu-id="d9574-137">Указывает универсальный код ресурса (URI) источника.</span><span class="sxs-lookup"><span data-stu-id="d9574-137">Specifies the source Uri.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9574-138">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="d9574-138">-StorageAccountId</span></span>
<span data-ttu-id="d9574-139">Указывает идентификатор учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="d9574-139">Specifies the storage account ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9574-140">-Тег</span><span class="sxs-lookup"><span data-stu-id="d9574-140">-Tag</span></span>
<span data-ttu-id="d9574-141">Указывает, что ресурсы и группы ресурсов можно пометить с помощью набора пар "имя-значение".</span><span class="sxs-lookup"><span data-stu-id="d9574-141">Specifies that resources and resource groups can be tagged with a set of name-value pairs.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9574-142">-Zone</span><span class="sxs-lookup"><span data-stu-id="d9574-142">-Zone</span></span>
<span data-ttu-id="d9574-143">Указывает список логических зон для диска.</span><span class="sxs-lookup"><span data-stu-id="d9574-143">Specifies the logical zone list for Disk.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9574-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d9574-144">-Confirm</span></span>
<span data-ttu-id="d9574-145">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d9574-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9574-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9574-146">-WhatIf</span></span>
<span data-ttu-id="d9574-147">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d9574-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d9574-148">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d9574-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9574-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9574-149">CommonParameters</span></span>
<span data-ttu-id="d9574-150">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d9574-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9574-151">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9574-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9574-152">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d9574-152">INPUTS</span></span>

### <span data-ttu-id="d9574-153">System. Nullable "1 [[Microsoft. Azure. Management. COMPUTE. Model. StorageAccountTypes, Microsoft. Azure. Management. COMPUTE, Version = 14.0.0.0, культура =" нейтрально ", PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="d9574-153">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.StorageAccountTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>
<span data-ttu-id="d9574-154">System. Nullable `1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable` 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]] System. String System. Nullable. Hashtable System. null `1[[Microsoft.Azure.Management.Compute.Models.DiskCreateOption, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
Microsoft.Azure.Management.Compute.Models.ImageDiskReference
System.Nullable` 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]] Microsoft. Azure. Management. COMPUTE. Models. KeyVaultAndSecretReference Microsoft. Azure. Management. Recompute. моделирует. KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="d9574-154">System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]] System.String System.Collections.Hashtable System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.DiskCreateOption, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
Microsoft.Azure.Management.Compute.Models.ImageDiskReference
System.Nullable`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]] Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="d9574-155">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d9574-155">OUTPUTS</span></span>

### <span data-ttu-id="d9574-156">Microsoft. Azure. Management. COMPUTE. Models.</span><span class="sxs-lookup"><span data-stu-id="d9574-156">Microsoft.Azure.Management.Compute.Models.Disk</span></span>

## <span data-ttu-id="d9574-157">Пуск</span><span class="sxs-lookup"><span data-stu-id="d9574-157">NOTES</span></span>

## <span data-ttu-id="d9574-158">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d9574-158">RELATED LINKS</span></span>


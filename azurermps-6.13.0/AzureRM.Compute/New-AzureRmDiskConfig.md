---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermdiskconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmDiskConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmDiskConfig.md
ms.openlocfilehash: 693d121bac5a618c5ad588cf4d34f63d8c6d0fd4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733003"
---
# <span data-ttu-id="84180-101">New-AzureRmDiskConfig</span><span class="sxs-lookup"><span data-stu-id="84180-101">New-AzureRmDiskConfig</span></span>

## <span data-ttu-id="84180-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="84180-102">SYNOPSIS</span></span>
<span data-ttu-id="84180-103">Создание настраиваемого объекта диска.</span><span class="sxs-lookup"><span data-stu-id="84180-103">Creates a configurable disk object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="84180-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="84180-104">SYNTAX</span></span>

```
New-AzureRmDiskConfig [[-SkuName] <String>] [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>]
 [[-Location] <String>] [-Zone <String[]>] [-DiskIOPSReadWrite <Int32>] [-DiskMBpsReadWrite <Int32>]
 [-Tag <Hashtable>] [-CreateOption <String>] [-StorageAccountId <String>]
 [-ImageReference <ImageDiskReference>] [-SourceUri <String>] [-SourceResourceId <String>]
 [-EncryptionSettingsEnabled <Boolean>] [-DiskEncryptionKey <KeyVaultAndSecretReference>]
 [-KeyEncryptionKey <KeyVaultAndKeyReference>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="84180-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="84180-105">DESCRIPTION</span></span>
<span data-ttu-id="84180-106">Командлет **New-AzureRmDiskConfig** создает настраиваемый объект диска.</span><span class="sxs-lookup"><span data-stu-id="84180-106">The **New-AzureRmDiskConfig** cmdlet creates a configurable disk object.</span></span>

## <span data-ttu-id="84180-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="84180-107">EXAMPLES</span></span>

### <span data-ttu-id="84180-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="84180-108">Example 1</span></span>
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

<span data-ttu-id="84180-109">Первая команда создает локальный пустой объект диска с размером 5GB в Standard_LRS типе учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="84180-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span> <span data-ttu-id="84180-110">Она также задает тип операционной системы Windows и включает параметры шифрования.</span><span class="sxs-lookup"><span data-stu-id="84180-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="84180-111">Вторая и третья команды устанавливают параметры ключа шифрования диска и ключа шифрования для объекта диска.</span><span class="sxs-lookup"><span data-stu-id="84180-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span> <span data-ttu-id="84180-112">Последняя команда принимает объект диска и создает диск с именем "Disk01" в группе ресурсов "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="84180-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="84180-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="84180-113">PARAMETERS</span></span>

### <span data-ttu-id="84180-114">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="84180-114">-CreateOption</span></span>
<span data-ttu-id="84180-115">Указывает, создает ли этот командлет диск на виртуальной машине из платформы или пользовательского образа, создает пустой диск или прикрепляет существующий диск.</span><span class="sxs-lookup"><span data-stu-id="84180-115">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

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

### <span data-ttu-id="84180-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84180-116">-DefaultProfile</span></span>
<span data-ttu-id="84180-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="84180-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="84180-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="84180-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="84180-119">Указывает объект ключа шифрования диска на диске.</span><span class="sxs-lookup"><span data-stu-id="84180-119">Specifies the disk encryption key object on a disk.</span></span>

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

### <span data-ttu-id="84180-120">-DiskIOPSReadWrite</span><span class="sxs-lookup"><span data-stu-id="84180-120">-DiskIOPSReadWrite</span></span>
<span data-ttu-id="84180-121">Количество операций ввода/вывода, разрешенных для этого диска; только устанавливаемые для UltraSSD дисков.</span><span class="sxs-lookup"><span data-stu-id="84180-121">The number of IOPS allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="84180-122">Одна операция может переключаться между 4 КБ и 256 Кбайт.</span><span class="sxs-lookup"><span data-stu-id="84180-122">One operation can transfer between 4k and 256k bytes.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84180-123">-DiskMBpsReadWrite</span><span class="sxs-lookup"><span data-stu-id="84180-123">-DiskMBpsReadWrite</span></span>
<span data-ttu-id="84180-124">Пропускная способность, разрешенная для этого диска; только устанавливаемые для UltraSSD дисков.</span><span class="sxs-lookup"><span data-stu-id="84180-124">The bandwidth allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="84180-125">Мбит/с — миллионные байты в секунду – используется нотация ISO с числом степеней 10.</span><span class="sxs-lookup"><span data-stu-id="84180-125">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84180-126">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="84180-126">-DiskSizeGB</span></span>
<span data-ttu-id="84180-127">Задает размер диска в ГБ.</span><span class="sxs-lookup"><span data-stu-id="84180-127">Specifies the size of the disk in GB.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84180-128">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="84180-128">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="84180-129">Включите параметры шифрования.</span><span class="sxs-lookup"><span data-stu-id="84180-129">Enable encryption settings.</span></span>

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

### <span data-ttu-id="84180-130">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="84180-130">-ImageReference</span></span>
<span data-ttu-id="84180-131">Указывает ссылку на изображение на диске.</span><span class="sxs-lookup"><span data-stu-id="84180-131">Specifies the image reference on a disk.</span></span>

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

### <span data-ttu-id="84180-132">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="84180-132">-KeyEncryptionKey</span></span>
<span data-ttu-id="84180-133">Задает ключ шифрования ключа на диске.</span><span class="sxs-lookup"><span data-stu-id="84180-133">Specifies the Key encryption key on a disk.</span></span>

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

### <span data-ttu-id="84180-134">-Location</span><span class="sxs-lookup"><span data-stu-id="84180-134">-Location</span></span>
<span data-ttu-id="84180-135">Задает расположение.</span><span class="sxs-lookup"><span data-stu-id="84180-135">Specifies a location.</span></span>

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

### <span data-ttu-id="84180-136">-OsType</span><span class="sxs-lookup"><span data-stu-id="84180-136">-OsType</span></span>
<span data-ttu-id="84180-137">Указывает тип операционной системы.</span><span class="sxs-lookup"><span data-stu-id="84180-137">Specifies the OS type.</span></span>

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

### <span data-ttu-id="84180-138">-SkuName</span><span class="sxs-lookup"><span data-stu-id="84180-138">-SkuName</span></span>
<span data-ttu-id="84180-139">Указывает имя SKU учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="84180-139">Specifies the Sku name of the storage account.</span></span>  <span data-ttu-id="84180-140">Доступные значения: Standard_LRS, Premium_LRS, StandardSSD_LRS и UltraSSD_LRS.</span><span class="sxs-lookup"><span data-stu-id="84180-140">Available values are Standard_LRS, Premium_LRS, StandardSSD_LRS, and UltraSSD_LRS.</span></span>  <span data-ttu-id="84180-141">UltraSSD_LRS можно использовать только с пустым значением для параметра CreateOption.</span><span class="sxs-lookup"><span data-stu-id="84180-141">UltraSSD_LRS can only be used with Empty value for CreateOption parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountType

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84180-142">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="84180-142">-SourceResourceId</span></span>
<span data-ttu-id="84180-143">Указывает исходный идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="84180-143">Specifies the  source resource ID.</span></span>

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

### <span data-ttu-id="84180-144">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="84180-144">-SourceUri</span></span>
<span data-ttu-id="84180-145">Указывает универсальный код ресурса (URI) источника.</span><span class="sxs-lookup"><span data-stu-id="84180-145">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="84180-146">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="84180-146">-StorageAccountId</span></span>
<span data-ttu-id="84180-147">Указывает идентификатор учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="84180-147">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="84180-148">-Тег</span><span class="sxs-lookup"><span data-stu-id="84180-148">-Tag</span></span>
<span data-ttu-id="84180-149">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="84180-149">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="84180-150">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="84180-150">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="84180-151">-Zone</span><span class="sxs-lookup"><span data-stu-id="84180-151">-Zone</span></span>
<span data-ttu-id="84180-152">Указывает список логических зон для диска.</span><span class="sxs-lookup"><span data-stu-id="84180-152">Specifies the logical zone list for Disk.</span></span>

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

### <span data-ttu-id="84180-153">-Confirm</span><span class="sxs-lookup"><span data-stu-id="84180-153">-Confirm</span></span>
<span data-ttu-id="84180-154">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="84180-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84180-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84180-155">-WhatIf</span></span>
<span data-ttu-id="84180-156">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="84180-156">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="84180-157">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="84180-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84180-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84180-158">CommonParameters</span></span>
<span data-ttu-id="84180-159">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="84180-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84180-160">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84180-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84180-161">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="84180-161">INPUTS</span></span>

### <span data-ttu-id="84180-162">System. String</span><span class="sxs-lookup"><span data-stu-id="84180-162">System.String</span></span>

### <span data-ttu-id="84180-163">System. Nullable "1 [[Microsoft. Azure. Management. COMPUTE. Model. OperatingSystemTypes, Microsoft. Azure. Management. COMPUTE, Version = 21.0.0.0, культура =" нейтрально ", PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="84180-163">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=21.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="84180-164">System. Int32</span><span class="sxs-lookup"><span data-stu-id="84180-164">System.Int32</span></span>

### <span data-ttu-id="84180-165">System. String []</span><span class="sxs-lookup"><span data-stu-id="84180-165">System.String[]</span></span>

### <span data-ttu-id="84180-166">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="84180-166">System.Collections.Hashtable</span></span>

### <span data-ttu-id="84180-167">Microsoft. Azure. Management. COMPUTE. Models. ImageDiskReference</span><span class="sxs-lookup"><span data-stu-id="84180-167">Microsoft.Azure.Management.Compute.Models.ImageDiskReference</span></span>

### <span data-ttu-id="84180-168">System. Nullable "1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="84180-168">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="84180-169">Microsoft. Azure. Management. COMPUTE. Models. KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="84180-169">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="84180-170">Microsoft. Azure. Management. COMPUTE. Models. KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="84180-170">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="84180-171">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="84180-171">OUTPUTS</span></span>

### <span data-ttu-id="84180-172">Microsoft.Azure.Commands.Compute.Automation.Models.PSDISK</span><span class="sxs-lookup"><span data-stu-id="84180-172">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="84180-173">Пуск</span><span class="sxs-lookup"><span data-stu-id="84180-173">NOTES</span></span>

## <span data-ttu-id="84180-174">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="84180-174">RELATED LINKS</span></span>

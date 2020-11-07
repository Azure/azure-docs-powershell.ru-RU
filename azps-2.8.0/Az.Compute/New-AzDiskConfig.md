---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azdiskconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskConfig.md
ms.openlocfilehash: c37ed947441789951d8523f38e7950ad6d9d2066
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721855"
---
# <span data-ttu-id="3ba4d-101">New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="3ba4d-101">New-AzDiskConfig</span></span>

## <span data-ttu-id="3ba4d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3ba4d-102">SYNOPSIS</span></span>
<span data-ttu-id="3ba4d-103">Создание настраиваемого объекта диска.</span><span class="sxs-lookup"><span data-stu-id="3ba4d-103">Creates a configurable disk object.</span></span>

## <span data-ttu-id="3ba4d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3ba4d-104">SYNTAX</span></span>

```
New-AzDiskConfig [[-SkuName] <String>] [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>]
 [[-Location] <String>] [-Zone <String[]>] [-HyperVGeneration <String>] [-DiskIOPSReadWrite <Int32>]
 [-DiskMBpsReadWrite <Int32>] [-Tag <Hashtable>] [-CreateOption <String>] [-StorageAccountId <String>]
 [-ImageReference <ImageDiskReference>] [-SourceUri <String>] [-SourceResourceId <String>]
 [-UploadSizeInBytes <Int64>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ba4d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3ba4d-105">DESCRIPTION</span></span>
<span data-ttu-id="3ba4d-106">Командлет **New-AzDiskConfig** создает настраиваемый объект диска.</span><span class="sxs-lookup"><span data-stu-id="3ba4d-106">The **New-AzDiskConfig** cmdlet creates a configurable disk object.</span></span>

## <span data-ttu-id="3ba4d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3ba4d-107">EXAMPLES</span></span>

### <span data-ttu-id="3ba4d-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3ba4d-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzDiskConfig -Location 'Central US' -DiskSizeGB 5 -AccountType Standard_LRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskconfig = Set-AzDiskDiskEncryptionKey -Disk $diskconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskconfig = Set-AzDiskKeyEncryptionKey -Disk $diskconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="3ba4d-109">Первая команда создает локальный пустой объект диска с размером 5GB в Standard_LRS типе учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="3ba4d-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span> <span data-ttu-id="3ba4d-110">Она также задает тип операционной системы Windows и включает параметры шифрования.</span><span class="sxs-lookup"><span data-stu-id="3ba4d-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="3ba4d-111">Вторая и третья команды устанавливают параметры ключа шифрования диска и ключа шифрования для объекта диска.</span><span class="sxs-lookup"><span data-stu-id="3ba4d-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span> <span data-ttu-id="3ba4d-112">Последняя команда принимает объект диска и создает диск с именем "Disk01" в группе ресурсов "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="3ba4d-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="3ba4d-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="3ba4d-113">Example 2</span></span>
```
PS C:\> $diskconfig = New-AzDiskConfig -Location 'Central US' -DiskSizeGB 1023 -SkuName Standard_LRS -OsType Windows -CreateOption Upload -DiskIOPSReadWrite 500 -DiskMBpsReadWrite 8;
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
PS C:\> $diskSas = Grant-AzDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -DurationInSecond 86400 -Access 'Write'
PS C:\> $disk = Get-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
# $disk.DiskState == 'ReadyToUpload'
PS C:\> AzCopy /Source:https://myaccount.blob.core.windows.net/mycontainer1 /Dest:$diskSas
PS C:\> $disk = Get-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
# $disk.DiskState == 'ActiveUpload'
PS C:\> Revoke-AzDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
```

<span data-ttu-id="3ba4d-114">В первой команде создается объект локального диска для отправки.</span><span class="sxs-lookup"><span data-stu-id="3ba4d-114">The first command creates a local disk object for Upload.</span></span>
<span data-ttu-id="3ba4d-115">Вторая команда принимает объект диска и создает диск с именем "Disk01" в группе ресурсов "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="3ba4d-115">The second command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>
<span data-ttu-id="3ba4d-116">Третья команда получает URL-адрес SAS для диска.</span><span class="sxs-lookup"><span data-stu-id="3ba4d-116">The third command gets SAS Url for the disk.</span></span>
<span data-ttu-id="3ba4d-117">Четвертая команда получает состояние диска.</span><span class="sxs-lookup"><span data-stu-id="3ba4d-117">The fourth command gets the state of the disk.</span></span>
<span data-ttu-id="3ba4d-118">Если состояние диска — "ReadyToUpload", пользователь может отправить диск из хранилища BLOB-данных на диск с помощью AzCopy.</span><span class="sxs-lookup"><span data-stu-id="3ba4d-118">If the disk state is 'ReadyToUpload', a user can upload a disk from blob storage to the disk SAS Url using AzCopy.</span></span>
<span data-ttu-id="3ba4d-119">Во время передачи состояние диска изменится на "ActiveUpload".</span><span class="sxs-lookup"><span data-stu-id="3ba4d-119">During uploading, the disk state is changed to 'ActiveUpload'.</span></span>
<span data-ttu-id="3ba4d-120">Последняя команда отзывает доступ к диску по URL-адресу SAS.</span><span class="sxs-lookup"><span data-stu-id="3ba4d-120">The last command revokes the disk access for the SAS Url.</span></span>

## <span data-ttu-id="3ba4d-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3ba4d-121">PARAMETERS</span></span>

### <span data-ttu-id="3ba4d-122">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="3ba4d-122">-CreateOption</span></span>
<span data-ttu-id="3ba4d-123">Указывает, создает ли этот командлет диск на виртуальной машине из платформы или пользовательского образа, создает пустой диск или прикрепляет существующий диск.</span><span class="sxs-lookup"><span data-stu-id="3ba4d-123">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

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

### <span data-ttu-id="3ba4d-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ba4d-124">-DefaultProfile</span></span>
<span data-ttu-id="3ba4d-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3ba4d-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3ba4d-126">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="3ba4d-126">-DiskEncryptionKey</span></span>
<span data-ttu-id="3ba4d-127">Указывает объект ключа шифрования диска на диске.</span><span class="sxs-lookup"><span data-stu-id="3ba4d-127">Specifies the disk encryption key object on a disk.</span></span>

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

### <span data-ttu-id="3ba4d-128">-DiskIOPSReadWrite</span><span class="sxs-lookup"><span data-stu-id="3ba4d-128">-DiskIOPSReadWrite</span></span>
<span data-ttu-id="3ba4d-129">Количество операций ввода/вывода, разрешенных для этого диска; только устанавливаемые для UltraSSD дисков.</span><span class="sxs-lookup"><span data-stu-id="3ba4d-129">The number of IOPS allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="3ba4d-130">Одна операция может переключаться между 4 КБ и 256 Кбайт.</span><span class="sxs-lookup"><span data-stu-id="3ba4d-130">One operation can transfer between 4k and 256k bytes.</span></span>

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

### <span data-ttu-id="3ba4d-131">-DiskMBpsReadWrite</span><span class="sxs-lookup"><span data-stu-id="3ba4d-131">-DiskMBpsReadWrite</span></span>
<span data-ttu-id="3ba4d-132">Пропускная способность, разрешенная для этого диска; только устанавливаемые для UltraSSD дисков.</span><span class="sxs-lookup"><span data-stu-id="3ba4d-132">The bandwidth allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="3ba4d-133">Мбит/с — миллионные байты в секунду – используется нотация ISO с числом степеней 10.</span><span class="sxs-lookup"><span data-stu-id="3ba4d-133">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

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

### <span data-ttu-id="3ba4d-134">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="3ba4d-134">-DiskSizeGB</span></span>
<span data-ttu-id="3ba4d-135">Задает размер диска в ГБ.</span><span class="sxs-lookup"><span data-stu-id="3ba4d-135">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="3ba4d-136">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="3ba4d-136">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="3ba4d-137">Включите параметры шифрования.</span><span class="sxs-lookup"><span data-stu-id="3ba4d-137">Enable encryption settings.</span></span>

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

### <span data-ttu-id="3ba4d-138">-HyperVGeneration</span><span class="sxs-lookup"><span data-stu-id="3ba4d-138">-HyperVGeneration</span></span>
<span data-ttu-id="3ba4d-139">Создание гипервизора виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="3ba4d-139">The hypervisor generation of the Virtual Machine.</span></span> <span data-ttu-id="3ba4d-140">Применимо только к дискам ОС.</span><span class="sxs-lookup"><span data-stu-id="3ba4d-140">Applicable to OS disks only.</span></span>  <span data-ttu-id="3ba4d-141">Допустимые значения: v1 и v2.</span><span class="sxs-lookup"><span data-stu-id="3ba4d-141">Allowed values are V1 and V2.</span></span>

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

### <span data-ttu-id="3ba4d-142">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="3ba4d-142">-ImageReference</span></span>
<span data-ttu-id="3ba4d-143">Указывает ссылку на изображение на диске.</span><span class="sxs-lookup"><span data-stu-id="3ba4d-143">Specifies the image reference on a disk.</span></span>

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

### <span data-ttu-id="3ba4d-144">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="3ba4d-144">-KeyEncryptionKey</span></span>
<span data-ttu-id="3ba4d-145">Задает ключ шифрования ключа на диске.</span><span class="sxs-lookup"><span data-stu-id="3ba4d-145">Specifies the Key encryption key on a disk.</span></span>

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

### <span data-ttu-id="3ba4d-146">-Location</span><span class="sxs-lookup"><span data-stu-id="3ba4d-146">-Location</span></span>
<span data-ttu-id="3ba4d-147">Задает расположение.</span><span class="sxs-lookup"><span data-stu-id="3ba4d-147">Specifies a location.</span></span>

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

### <span data-ttu-id="3ba4d-148">-OsType</span><span class="sxs-lookup"><span data-stu-id="3ba4d-148">-OsType</span></span>
<span data-ttu-id="3ba4d-149">Указывает тип операционной системы.</span><span class="sxs-lookup"><span data-stu-id="3ba4d-149">Specifies the OS type.</span></span>

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

### <span data-ttu-id="3ba4d-150">-SkuName</span><span class="sxs-lookup"><span data-stu-id="3ba4d-150">-SkuName</span></span>
<span data-ttu-id="3ba4d-151">Указывает имя SKU учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="3ba4d-151">Specifies the Sku name of the storage account.</span></span>  <span data-ttu-id="3ba4d-152">Доступные значения: Standard_LRS, Premium_LRS, StandardSSD_LRS и UltraSSD_LRS.</span><span class="sxs-lookup"><span data-stu-id="3ba4d-152">Available values are Standard_LRS, Premium_LRS, StandardSSD_LRS, and UltraSSD_LRS.</span></span>  <span data-ttu-id="3ba4d-153">UltraSSD_LRS можно использовать только с пустым значением для параметра CreateOption.</span><span class="sxs-lookup"><span data-stu-id="3ba4d-153">UltraSSD_LRS can only be used with Empty value for CreateOption parameter.</span></span>

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

### <span data-ttu-id="3ba4d-154">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="3ba4d-154">-SourceResourceId</span></span>
<span data-ttu-id="3ba4d-155">Указывает исходный идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="3ba4d-155">Specifies the  source resource ID.</span></span>

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

### <span data-ttu-id="3ba4d-156">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="3ba4d-156">-SourceUri</span></span>
<span data-ttu-id="3ba4d-157">Указывает универсальный код ресурса (URI) источника.</span><span class="sxs-lookup"><span data-stu-id="3ba4d-157">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="3ba4d-158">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="3ba4d-158">-StorageAccountId</span></span>
<span data-ttu-id="3ba4d-159">Указывает идентификатор учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="3ba4d-159">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="3ba4d-160">-Тег</span><span class="sxs-lookup"><span data-stu-id="3ba4d-160">-Tag</span></span>
<span data-ttu-id="3ba4d-161">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="3ba4d-161">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="3ba4d-162">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="3ba4d-162">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="3ba4d-163">-UploadSizeInBytes</span><span class="sxs-lookup"><span data-stu-id="3ba4d-163">-UploadSizeInBytes</span></span>
<span data-ttu-id="3ba4d-164">Указывает размер содержимого отправки, включая нижний колонтитул виртуального жесткого диска при отправке CreateOption.</span><span class="sxs-lookup"><span data-stu-id="3ba4d-164">Specifies the size of the contents of the upload including the VHD footer when CreateOption is Upload.</span></span>  <span data-ttu-id="3ba4d-165">Это значение должно быть между 20972032 (20 MiB + 512 байт для нижнего колонтитула VHD) и 35183298347520 байт (32 TiB + 512 байт для нижнего колонтитула VHD).</span><span class="sxs-lookup"><span data-stu-id="3ba4d-165">This value should be between 20972032 (20 MiB + 512 bytes for the VHD footer) and 35183298347520 bytes (32 TiB + 512 bytes for the VHD footer).</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ba4d-166">-Zone</span><span class="sxs-lookup"><span data-stu-id="3ba4d-166">-Zone</span></span>
<span data-ttu-id="3ba4d-167">Указывает список логических зон для диска.</span><span class="sxs-lookup"><span data-stu-id="3ba4d-167">Specifies the logical zone list for Disk.</span></span>

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

### <span data-ttu-id="3ba4d-168">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3ba4d-168">-Confirm</span></span>
<span data-ttu-id="3ba4d-169">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3ba4d-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ba4d-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ba4d-170">-WhatIf</span></span>
<span data-ttu-id="3ba4d-171">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3ba4d-171">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3ba4d-172">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3ba4d-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ba4d-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ba4d-173">CommonParameters</span></span>
<span data-ttu-id="3ba4d-174">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3ba4d-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ba4d-175">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3ba4d-175">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ba4d-176">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3ba4d-176">INPUTS</span></span>

### <span data-ttu-id="3ba4d-177">System. String</span><span class="sxs-lookup"><span data-stu-id="3ba4d-177">System.String</span></span>

### <span data-ttu-id="3ba4d-178">System. Nullable "1 [[Microsoft. Azure. Management. COMPUTE. Model. OperatingSystemTypes, Microsoft. Azure. Management. COMPUTE, Version = 23.0.0.0, культура =" нейтрально ", PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="3ba4d-178">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="3ba4d-179">System. Int32</span><span class="sxs-lookup"><span data-stu-id="3ba4d-179">System.Int32</span></span>

### <span data-ttu-id="3ba4d-180">System. String []</span><span class="sxs-lookup"><span data-stu-id="3ba4d-180">System.String[]</span></span>

### <span data-ttu-id="3ba4d-181">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="3ba4d-181">System.Collections.Hashtable</span></span>

### <span data-ttu-id="3ba4d-182">Microsoft. Azure. Management. COMPUTE. Models. ImageDiskReference</span><span class="sxs-lookup"><span data-stu-id="3ba4d-182">Microsoft.Azure.Management.Compute.Models.ImageDiskReference</span></span>

### <span data-ttu-id="3ba4d-183">System. Nullable "1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="3ba4d-183">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="3ba4d-184">Microsoft. Azure. Management. COMPUTE. Models. KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="3ba4d-184">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="3ba4d-185">Microsoft. Azure. Management. COMPUTE. Models. KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="3ba4d-185">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="3ba4d-186">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3ba4d-186">OUTPUTS</span></span>

### <span data-ttu-id="3ba4d-187">Microsoft.Azure.Commands.Compute.Automation.Models.PSDISK</span><span class="sxs-lookup"><span data-stu-id="3ba4d-187">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="3ba4d-188">Пуск</span><span class="sxs-lookup"><span data-stu-id="3ba4d-188">NOTES</span></span>

## <span data-ttu-id="3ba4d-189">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3ba4d-189">RELATED LINKS</span></span>

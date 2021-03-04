---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azdiskconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskConfig.md
ms.openlocfilehash: 34caab92645f610ed6ed71d907639060cf0c456a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957619"
---
# <span data-ttu-id="bc0ee-101">New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="bc0ee-101">New-AzDiskConfig</span></span>

## <span data-ttu-id="bc0ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc0ee-102">SYNOPSIS</span></span>
<span data-ttu-id="bc0ee-103">Создает настраиваемый объект диска.</span><span class="sxs-lookup"><span data-stu-id="bc0ee-103">Creates a configurable disk object.</span></span>

## <span data-ttu-id="bc0ee-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="bc0ee-104">SYNTAX</span></span>

```
New-AzDiskConfig [[-SkuName] <String>] [-Tier <String>] [-LogicalSectorSize <Int32>]
 [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>] [[-Location] <String>]
 [-Zone <String[]>] [-HyperVGeneration <String>] [-DiskIOPSReadWrite <Int64>] [-DiskMBpsReadWrite <Int64>]
 [-DiskIOPSReadOnly <Int64>] [-DiskMBpsReadOnly <Int64>] [-MaxSharesCount <Int32>] [-Tag <Hashtable>]
 [-CreateOption <String>] [-StorageAccountId <String>] [-ImageReference <ImageDiskReference>]
 [-GalleryImageReference <ImageDiskReference>] [-SourceUri <String>] [-SourceResourceId <String>]
 [-UploadSizeInBytes <Int64>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DiskEncryptionSetId <String>] [-EncryptionType <String>] [-DiskAccessId <String>]
 [-NetworkAccessPolicy <String>] [-BurstingEnabled <Boolean>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bc0ee-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bc0ee-105">DESCRIPTION</span></span>
<span data-ttu-id="bc0ee-106">Для создания настраиваемого диска создается объект диска **New-AzDiskConfig.**</span><span class="sxs-lookup"><span data-stu-id="bc0ee-106">The **New-AzDiskConfig** cmdlet creates a configurable disk object.</span></span>

## <span data-ttu-id="bc0ee-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="bc0ee-107">EXAMPLES</span></span>

### <span data-ttu-id="bc0ee-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="bc0ee-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzDiskConfig -Location 'Central US' -DiskSizeGB 5 -SkuName Standard_LRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskconfig = Set-AzDiskDiskEncryptionKey -Disk $diskconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskconfig = Set-AzDiskKeyEncryptionKey -Disk $diskconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="bc0ee-109">Первая команда создает локальный пустой диск с размером 5 ГБ Standard_LRS типа учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="bc0ee-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span> <span data-ttu-id="bc0ee-110">Она также задает тип ос Windows и включает параметры шифрования.</span><span class="sxs-lookup"><span data-stu-id="bc0ee-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="bc0ee-111">Вторая и третья команды устанавливают параметры ключа шифрования диска и ключа шифрования для объекта диска.</span><span class="sxs-lookup"><span data-stu-id="bc0ee-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span> <span data-ttu-id="bc0ee-112">Последняя команда принимает объект диска и создает диск с именем "Диск01" в группе ресурсов "Группа ресурсов01".</span><span class="sxs-lookup"><span data-stu-id="bc0ee-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="bc0ee-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="bc0ee-113">Example 2</span></span>
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

<span data-ttu-id="bc0ee-114">Первая команда создает объект локального диска для отправки.</span><span class="sxs-lookup"><span data-stu-id="bc0ee-114">The first command creates a local disk object for Upload.</span></span>
<span data-ttu-id="bc0ee-115">Вторая команда принимает объект диска и создает диск с именем "Диск01" в группе ресурсов "Группа ресурсов01".</span><span class="sxs-lookup"><span data-stu-id="bc0ee-115">The second command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>
<span data-ttu-id="bc0ee-116">Третья команда получает URL-адрес SAS для диска.</span><span class="sxs-lookup"><span data-stu-id="bc0ee-116">The third command gets SAS Url for the disk.</span></span>
<span data-ttu-id="bc0ee-117">Четвертая команда получает состояние диска.</span><span class="sxs-lookup"><span data-stu-id="bc0ee-117">The fourth command gets the state of the disk.</span></span>
<span data-ttu-id="bc0ee-118">Если состояние диска — ReadyToUpload, пользователь может отправить диск из хранилища BLOB-дисков в URL-адрес SAS диска с помощью AzCopy.</span><span class="sxs-lookup"><span data-stu-id="bc0ee-118">If the disk state is 'ReadyToUpload', a user can upload a disk from blob storage to the disk SAS Url using AzCopy.</span></span>
<span data-ttu-id="bc0ee-119">Во время отправки состояние диска меняется на "ActiveUpload".</span><span class="sxs-lookup"><span data-stu-id="bc0ee-119">During uploading, the disk state is changed to 'ActiveUpload'.</span></span>
<span data-ttu-id="bc0ee-120">Последняя команда отменяет доступ к диску URL-адреса SAS.</span><span class="sxs-lookup"><span data-stu-id="bc0ee-120">The last command revokes the disk access for the SAS Url.</span></span>

### <span data-ttu-id="bc0ee-121">Пример 3</span><span class="sxs-lookup"><span data-stu-id="bc0ee-121">Example 3</span></span>
```
PS C:\> $galleryImageReference = @{Id = '/subscriptions/0296790d-427c-48ca-b204-8b729bbd8670/resourceGroups/swaggertests/providers/Microsoft.Compute/galleries/swaggergallery/images/swaggerimagedef/versions/1.0.0'; Lun=1}
PS C:\> $diskConfig = New-AzDiskConfig -Location 'West US' -CreateOption 'FromImage' -GalleryImageReference $galleryImageReference;
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskConfig
```

<span data-ttu-id="bc0ee-122">Создайте диск из общей коллекции изображений.</span><span class="sxs-lookup"><span data-stu-id="bc0ee-122">Create a disk from a Shared Gallery Image Version.</span></span>  <span data-ttu-id="bc0ee-123">ИД — это id версии изображения коллекции.</span><span class="sxs-lookup"><span data-stu-id="bc0ee-123">Id is the id of the shared gallery image version.</span></span> <span data-ttu-id="bc0ee-124">Lun требуется только в том случае, если источником является диск данных.</span><span class="sxs-lookup"><span data-stu-id="bc0ee-124">Lun is needed only if the source is a data disk.</span></span>

## <span data-ttu-id="bc0ee-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bc0ee-125">PARAMETERS</span></span>

### <span data-ttu-id="bc0ee-126">-BurstingEnabled</span><span class="sxs-lookup"><span data-stu-id="bc0ee-126">-BurstingEnabled</span></span>
<span data-ttu-id="bc0ee-127">Включает вспышки, которые выходят за пределы предварительно заского целевого показателя производительности диска.</span><span class="sxs-lookup"><span data-stu-id="bc0ee-127">Enables bursting beyond the provisioned performance target of the disk.</span></span> <span data-ttu-id="bc0ee-128">По умолчанию вспышки отключены.</span><span class="sxs-lookup"><span data-stu-id="bc0ee-128">Bursting is disabled by default.</span></span> <span data-ttu-id="bc0ee-129">Не относится к дискам Ultra.</span><span class="sxs-lookup"><span data-stu-id="bc0ee-129">Does not apply to Ultra disks.</span></span>

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

### <span data-ttu-id="bc0ee-130">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="bc0ee-130">-CreateOption</span></span>
<span data-ttu-id="bc0ee-131">Указывает, создает ли этот cmdlet диск в виртуальной машине из платформы или изображения пользователя, создает пустой диск или влог существующий диск.</span><span class="sxs-lookup"><span data-stu-id="bc0ee-131">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

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

### <span data-ttu-id="bc0ee-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc0ee-132">-DefaultProfile</span></span>
<span data-ttu-id="bc0ee-133">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bc0ee-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bc0ee-134">-DiskAccessId</span><span class="sxs-lookup"><span data-stu-id="bc0ee-134">-DiskAccessId</span></span>
<span data-ttu-id="bc0ee-135">Возвращает или ARM ИД ресурса DiskAccess для использования частных конечных точек.</span><span class="sxs-lookup"><span data-stu-id="bc0ee-135">Gets or sets ARM ID of the DiskAccess resource for using private endpoints on.</span></span>


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

### <span data-ttu-id="bc0ee-136">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="bc0ee-136">-DiskEncryptionKey</span></span>
<span data-ttu-id="bc0ee-137">Определяет объект ключа шифрования диска на диске.</span><span class="sxs-lookup"><span data-stu-id="bc0ee-137">Specifies the disk encryption key object on a disk.</span></span>

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

### <span data-ttu-id="bc0ee-138">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="bc0ee-138">-DiskEncryptionSetId</span></span>
<span data-ttu-id="bc0ee-139">Определяет код ресурса набора шифрования диска, который нужно использовать для включения шифрования во время работы.</span><span class="sxs-lookup"><span data-stu-id="bc0ee-139">Specifies the resource Id of the disk encryption set to use for enabling encryption at rest.</span></span>

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

### <span data-ttu-id="bc0ee-140">-DiskIOPSReadOnly</span><span class="sxs-lookup"><span data-stu-id="bc0ee-140">-DiskIOPSReadOnly</span></span>
<span data-ttu-id="bc0ee-141">Общее количество IOPS, которое будет разрешено для всех ВМ-сообщений, которые имеют общий диск с иконой ReadOnly.</span><span class="sxs-lookup"><span data-stu-id="bc0ee-141">The total number of IOPS that will be allowed across all VMs mounting the shared disk as ReadOnly.</span></span> <span data-ttu-id="bc0ee-142">Одна операция может передаваться между 4k и 256k bytes.</span><span class="sxs-lookup"><span data-stu-id="bc0ee-142">One operation can transfer between 4k and 256k bytes.</span></span>

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

### <span data-ttu-id="bc0ee-143">-DiskIOPSReadWrite</span><span class="sxs-lookup"><span data-stu-id="bc0ee-143">-DiskIOPSReadWrite</span></span>
<span data-ttu-id="bc0ee-144">Количество IOPS, разрешенных для этого диска; только для дисков UltraSSD.</span><span class="sxs-lookup"><span data-stu-id="bc0ee-144">The number of IOPS allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="bc0ee-145">Одна операция может передаваться между 4k и 256k bytes.</span><span class="sxs-lookup"><span data-stu-id="bc0ee-145">One operation can transfer between 4k and 256k bytes.</span></span>

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

### <span data-ttu-id="bc0ee-146">-DiskMBpsReadOnly</span><span class="sxs-lookup"><span data-stu-id="bc0ee-146">-DiskMBpsReadOnly</span></span>
<span data-ttu-id="bc0ee-147">"описание": "Общая пропускная способность (MBPS), которая будет разрешена для всех ВМ-сообщений, которые крепят общий диск как ReadOnly.</span><span class="sxs-lookup"><span data-stu-id="bc0ee-147">"description": "The total throughput (MBps) that will be allowed across all VMs mounting the shared disk as ReadOnly.</span></span> <span data-ttu-id="bc0ee-148">MBps означает миллионыбайт в секунду. В этом случае используется нотация ISO с полномочиями 10.</span><span class="sxs-lookup"><span data-stu-id="bc0ee-148">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

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

### <span data-ttu-id="bc0ee-149">-DiskMBpsReadWrite</span><span class="sxs-lookup"><span data-stu-id="bc0ee-149">-DiskMBpsReadWrite</span></span>
<span data-ttu-id="bc0ee-150">пропускная способность, допустимая для этого диска; только для дисков UltraSSD.</span><span class="sxs-lookup"><span data-stu-id="bc0ee-150">The bandwidth allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="bc0ee-151">MBps означает миллионыбайт в секунду. В этом случае используется нотация ISO с полномочиями 10.</span><span class="sxs-lookup"><span data-stu-id="bc0ee-151">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

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

### <span data-ttu-id="bc0ee-152">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="bc0ee-152">-DiskSizeGB</span></span>
<span data-ttu-id="bc0ee-153">Определяет размер диска в ГБ.</span><span class="sxs-lookup"><span data-stu-id="bc0ee-153">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="bc0ee-154">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="bc0ee-154">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="bc0ee-155">Включить параметры шифрования.</span><span class="sxs-lookup"><span data-stu-id="bc0ee-155">Enable encryption settings.</span></span>

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

### <span data-ttu-id="bc0ee-156">-EncryptionType</span><span class="sxs-lookup"><span data-stu-id="bc0ee-156">-EncryptionType</span></span>
<span data-ttu-id="bc0ee-157">Тип ключа, используемого для шифрования данных на диске.</span><span class="sxs-lookup"><span data-stu-id="bc0ee-157">The type of key used to encrypt the data of the disk.</span></span>  <span data-ttu-id="bc0ee-158">Доступны такие значения: EncryptionAtRestWithPlatformKey, 'EncryptionAtRestWithCustomerKey'</span><span class="sxs-lookup"><span data-stu-id="bc0ee-158">Available values are: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'</span></span>

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

### <span data-ttu-id="bc0ee-159">-GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="bc0ee-159">-GalleryImageReference</span></span>
<span data-ttu-id="bc0ee-160">Объект GalleryImageReference.</span><span class="sxs-lookup"><span data-stu-id="bc0ee-160">The GalleryImageReference object.</span></span>  <span data-ttu-id="bc0ee-161">Требуется при создании из коллекции изображений.</span><span class="sxs-lookup"><span data-stu-id="bc0ee-161">Required if creating from a Gallery Image.</span></span> <span data-ttu-id="bc0ee-162">Он будет ARM общего изображения галли, из которого создается диск.</span><span class="sxs-lookup"><span data-stu-id="bc0ee-162">The id will be the ARM id of the shared galley image version from which to create a disk.</span></span>
<span data-ttu-id="bc0ee-163">Lun требуется, если источником копии является один из дисков данных в изображении коллекции; Если NULL, будет скопирован диск ОС изображения.</span><span class="sxs-lookup"><span data-stu-id="bc0ee-163">A lun is needed if the source of the copy is one of the data disks in the gallery image; if null, the OS disk of the image will be copied.</span></span>

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

### <span data-ttu-id="bc0ee-164">-HyperVGeneration</span><span class="sxs-lookup"><span data-stu-id="bc0ee-164">-HyperVGeneration</span></span>
<span data-ttu-id="bc0ee-165">Генерация гипервизора виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="bc0ee-165">The hypervisor generation of the Virtual Machine.</span></span> <span data-ttu-id="bc0ee-166">Применимо только к дискам ОС.</span><span class="sxs-lookup"><span data-stu-id="bc0ee-166">Applicable to OS disks only.</span></span>  <span data-ttu-id="bc0ee-167">Допустимые значения: V1 и V2.</span><span class="sxs-lookup"><span data-stu-id="bc0ee-167">Allowed values are V1 and V2.</span></span>

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

### <span data-ttu-id="bc0ee-168">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="bc0ee-168">-ImageReference</span></span>
<span data-ttu-id="bc0ee-169">Указывает ссылку на изображение на диске.</span><span class="sxs-lookup"><span data-stu-id="bc0ee-169">Specifies the image reference on a disk.</span></span>

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

### <span data-ttu-id="bc0ee-170">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="bc0ee-170">-KeyEncryptionKey</span></span>
<span data-ttu-id="bc0ee-171">Указывает ключ шифрования ключа на диске.</span><span class="sxs-lookup"><span data-stu-id="bc0ee-171">Specifies the Key encryption key on a disk.</span></span>

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

### <span data-ttu-id="bc0ee-172">-Location</span><span class="sxs-lookup"><span data-stu-id="bc0ee-172">-Location</span></span>
<span data-ttu-id="bc0ee-173">Определяет расположение.</span><span class="sxs-lookup"><span data-stu-id="bc0ee-173">Specifies a location.</span></span>

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

### <span data-ttu-id="bc0ee-174">-LogicalSectorSize</span><span class="sxs-lookup"><span data-stu-id="bc0ee-174">-LogicalSectorSize</span></span>
<span data-ttu-id="bc0ee-175">Логический размер сектора вбайтов для дисков Ultra.</span><span class="sxs-lookup"><span data-stu-id="bc0ee-175">Logical sector size in bytes for Ultra disks.</span></span> 

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

### <span data-ttu-id="bc0ee-176">-MaxSharesCount</span><span class="sxs-lookup"><span data-stu-id="bc0ee-176">-MaxSharesCount</span></span>
<span data-ttu-id="bc0ee-177">Максимальное количество ВТБ, которые можно одновременно прикрепить к диску.</span><span class="sxs-lookup"><span data-stu-id="bc0ee-177">The maximum number of VMs that can attach to the disk at the same time.</span></span>
<span data-ttu-id="bc0ee-178">Значение больше одного указывает на диск, который может быть одновременно установлен на нескольких ВМ-дисках.</span><span class="sxs-lookup"><span data-stu-id="bc0ee-178">Value greater than one indicates a disk that can be mounted on multiple VMs at the same time.</span></span>

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

### <span data-ttu-id="bc0ee-179">-NetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="bc0ee-179">-NetworkAccessPolicy</span></span>
<span data-ttu-id="bc0ee-180">Политика доступа к сети определяет политику доступа к сети.</span><span class="sxs-lookup"><span data-stu-id="bc0ee-180">Network access policy defines the network access policy.</span></span>
<span data-ttu-id="bc0ee-181">Возможные значения: 'AllowAll', 'AllowPrivate', 'DenyAll'</span><span class="sxs-lookup"><span data-stu-id="bc0ee-181">Possible values include: 'AllowAll', 'AllowPrivate', 'DenyAll'</span></span>

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

### <span data-ttu-id="bc0ee-182">-OsType</span><span class="sxs-lookup"><span data-stu-id="bc0ee-182">-OsType</span></span>
<span data-ttu-id="bc0ee-183">Тип ОС.</span><span class="sxs-lookup"><span data-stu-id="bc0ee-183">Specifies the OS type.</span></span>

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

### <span data-ttu-id="bc0ee-184">-SkuName</span><span class="sxs-lookup"><span data-stu-id="bc0ee-184">-SkuName</span></span>
<span data-ttu-id="bc0ee-185">Указывает имя SKU учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="bc0ee-185">Specifies the Sku name of the storage account.</span></span>  <span data-ttu-id="bc0ee-186">Доступны значения Standard_LRS, Premium_LRS, StandardSSD_LRS и UltraSSD_LRS.</span><span class="sxs-lookup"><span data-stu-id="bc0ee-186">Available values are Standard_LRS, Premium_LRS, StandardSSD_LRS, and UltraSSD_LRS.</span></span>  <span data-ttu-id="bc0ee-187">UltraSSD_LRS можно использовать только с пустым значением для параметра CreateOption.</span><span class="sxs-lookup"><span data-stu-id="bc0ee-187">UltraSSD_LRS can only be used with Empty value for CreateOption parameter.</span></span>

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

### <span data-ttu-id="bc0ee-188">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="bc0ee-188">-SourceResourceId</span></span>
<span data-ttu-id="bc0ee-189">Определяет код источника ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bc0ee-189">Specifies the  source resource ID.</span></span>

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

### <span data-ttu-id="bc0ee-190">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="bc0ee-190">-SourceUri</span></span>
<span data-ttu-id="bc0ee-191">Определяет исходный URI.</span><span class="sxs-lookup"><span data-stu-id="bc0ee-191">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="bc0ee-192">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="bc0ee-192">-StorageAccountId</span></span>
<span data-ttu-id="bc0ee-193">Определяет ИД учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="bc0ee-193">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="bc0ee-194">-Tag</span><span class="sxs-lookup"><span data-stu-id="bc0ee-194">-Tag</span></span>
<span data-ttu-id="bc0ee-195">Пары "ключевое значение" в виде hash table.</span><span class="sxs-lookup"><span data-stu-id="bc0ee-195">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="bc0ee-196">Например: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="bc0ee-196">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="bc0ee-197">-Tier</span><span class="sxs-lookup"><span data-stu-id="bc0ee-197">-Tier</span></span>
<span data-ttu-id="bc0ee-198">Уровень производительности диска.</span><span class="sxs-lookup"><span data-stu-id="bc0ee-198">Performance tier of the disk.</span></span>

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

### <span data-ttu-id="bc0ee-199">-UploadSizeInBytes</span><span class="sxs-lookup"><span data-stu-id="bc0ee-199">-UploadSizeInBytes</span></span>
<span data-ttu-id="bc0ee-200">Определяет размер содержимого загружаемого содержимого, включая принудитель VHD при отправке CreateOption.</span><span class="sxs-lookup"><span data-stu-id="bc0ee-200">Specifies the size of the contents of the upload including the VHD footer when CreateOption is Upload.</span></span>  <span data-ttu-id="bc0ee-201">Это значение должно быть в период между 20972032 (20 MiB + 512 bytes для footer vHD) и 35183298347520 bytes (32 TiB + 512 bytes for the VHD footer).</span><span class="sxs-lookup"><span data-stu-id="bc0ee-201">This value should be between 20972032 (20 MiB + 512 bytes for the VHD footer) and 35183298347520 bytes (32 TiB + 512 bytes for the VHD footer).</span></span>

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

### <span data-ttu-id="bc0ee-202">-Zone</span><span class="sxs-lookup"><span data-stu-id="bc0ee-202">-Zone</span></span>
<span data-ttu-id="bc0ee-203">Определяет логический список зон для диска.</span><span class="sxs-lookup"><span data-stu-id="bc0ee-203">Specifies the logical zone list for Disk.</span></span>

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

### <span data-ttu-id="bc0ee-204">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bc0ee-204">-Confirm</span></span>
<span data-ttu-id="bc0ee-205">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bc0ee-205">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc0ee-206">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc0ee-206">-WhatIf</span></span>
<span data-ttu-id="bc0ee-207">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bc0ee-207">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bc0ee-208">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="bc0ee-208">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc0ee-209">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc0ee-209">CommonParameters</span></span>
<span data-ttu-id="bc0ee-210">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc0ee-210">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc0ee-211">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bc0ee-211">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc0ee-212">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bc0ee-212">INPUTS</span></span>

### <span data-ttu-id="bc0ee-213">System.String</span><span class="sxs-lookup"><span data-stu-id="bc0ee-213">System.String</span></span>

### <span data-ttu-id="bc0ee-214">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="bc0ee-214">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="bc0ee-215">System.Int32</span><span class="sxs-lookup"><span data-stu-id="bc0ee-215">System.Int32</span></span>

### <span data-ttu-id="bc0ee-216">System.String[]</span><span class="sxs-lookup"><span data-stu-id="bc0ee-216">System.String[]</span></span>

### <span data-ttu-id="bc0ee-217">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="bc0ee-217">System.Collections.Hashtable</span></span>

### <span data-ttu-id="bc0ee-218">Microsoft.Azure.Management.Compute.Models.ImageDiskReference</span><span class="sxs-lookup"><span data-stu-id="bc0ee-218">Microsoft.Azure.Management.Compute.Models.ImageDiskReference</span></span>

### <span data-ttu-id="bc0ee-219">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="bc0ee-219">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="bc0ee-220">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="bc0ee-220">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="bc0ee-221">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="bc0ee-221">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="bc0ee-222">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="bc0ee-222">OUTPUTS</span></span>

### <span data-ttu-id="bc0ee-223">Microsoft.Azure.Commands.Compute.Automation.Models.PSDокне</span><span class="sxs-lookup"><span data-stu-id="bc0ee-223">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="bc0ee-224">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="bc0ee-224">NOTES</span></span>

## <span data-ttu-id="bc0ee-225">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bc0ee-225">RELATED LINKS</span></span>

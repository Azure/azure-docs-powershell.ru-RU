---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azdiskconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskConfig.md
ms.openlocfilehash: ec4d0444ad88fa7536fbf1ee050dc8dcb6a76af3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98509109"
---
# <span data-ttu-id="daa29-101">New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="daa29-101">New-AzDiskConfig</span></span>

## <span data-ttu-id="daa29-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="daa29-102">SYNOPSIS</span></span>
<span data-ttu-id="daa29-103">Создание настраиваемого диска.</span><span class="sxs-lookup"><span data-stu-id="daa29-103">Creates a configurable disk object.</span></span>

## <span data-ttu-id="daa29-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="daa29-104">SYNTAX</span></span>

```
New-AzDiskConfig [[-SkuName] <String>] [-Tier <String>] [-LogicalSectorSize <Int32>]
 [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>] [[-Location] <String>] [-Zone <String[]>]
 [-HyperVGeneration <String>] [-DiskIOPSReadWrite <Int64>] [-DiskMBpsReadWrite <Int64>]
 [-DiskIOPSReadOnly <Int64>] [-DiskMBpsReadOnly <Int64>] [-MaxSharesCount <Int32>] [-Tag <Hashtable>]
 [-CreateOption <String>] [-StorageAccountId <String>] [-ImageReference <ImageDiskReference>]
 [-GalleryImageReference <ImageDiskReference>] [-SourceUri <String>] [-SourceResourceId <String>]
 [-UploadSizeInBytes <Int64>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DiskEncryptionSetId <String>] [-EncryptionType <String>] [-DiskAccessId <String>]
 [-NetworkAccessPolicy <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="daa29-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="daa29-105">DESCRIPTION</span></span>
<span data-ttu-id="daa29-106">Для создания настраиваемого диска создается объект диска **New-AzDiskConfig.**</span><span class="sxs-lookup"><span data-stu-id="daa29-106">The **New-AzDiskConfig** cmdlet creates a configurable disk object.</span></span>

## <span data-ttu-id="daa29-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="daa29-107">EXAMPLES</span></span>

### <span data-ttu-id="daa29-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="daa29-108">Example 1</span></span>
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

<span data-ttu-id="daa29-109">Первая команда создает локальный пустой диск с размером 5 ГБ Standard_LRS типа учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="daa29-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span> <span data-ttu-id="daa29-110">Она также задает тип ос Windows и включает параметры шифрования.</span><span class="sxs-lookup"><span data-stu-id="daa29-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="daa29-111">Вторая и третья команды устанавливают параметры ключа шифрования диска и ключа шифрования для объекта диска.</span><span class="sxs-lookup"><span data-stu-id="daa29-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span> <span data-ttu-id="daa29-112">Последняя команда принимает объект диска и создает диск с именем "Диск01" в группе ресурсов "Группа ресурсов01".</span><span class="sxs-lookup"><span data-stu-id="daa29-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="daa29-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="daa29-113">Example 2</span></span>
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

<span data-ttu-id="daa29-114">Первая команда создает объект локального диска для отправки.</span><span class="sxs-lookup"><span data-stu-id="daa29-114">The first command creates a local disk object for Upload.</span></span>
<span data-ttu-id="daa29-115">Вторая команда принимает объект диска и создает диск с именем "Диск01" в группе ресурсов "Группа ресурсов01".</span><span class="sxs-lookup"><span data-stu-id="daa29-115">The second command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>
<span data-ttu-id="daa29-116">Третья команда получает URL-адрес SAS для диска.</span><span class="sxs-lookup"><span data-stu-id="daa29-116">The third command gets SAS Url for the disk.</span></span>
<span data-ttu-id="daa29-117">Четвертая команда получает состояние диска.</span><span class="sxs-lookup"><span data-stu-id="daa29-117">The fourth command gets the state of the disk.</span></span>
<span data-ttu-id="daa29-118">Если состояние диска — ReadyToUpload, пользователь может отправить диск из хранилища BLOB-дисков в URL-адрес SAS диска с помощью AzCopy.</span><span class="sxs-lookup"><span data-stu-id="daa29-118">If the disk state is 'ReadyToUpload', a user can upload a disk from blob storage to the disk SAS Url using AzCopy.</span></span>
<span data-ttu-id="daa29-119">Во время отправки состояние диска меняется на "ActiveUpload".</span><span class="sxs-lookup"><span data-stu-id="daa29-119">During uploading, the disk state is changed to 'ActiveUpload'.</span></span>
<span data-ttu-id="daa29-120">Последняя команда отменяет доступ к диску URL-адреса SAS.</span><span class="sxs-lookup"><span data-stu-id="daa29-120">The last command revokes the disk access for the SAS Url.</span></span>

### <span data-ttu-id="daa29-121">Пример 3</span><span class="sxs-lookup"><span data-stu-id="daa29-121">Example 3</span></span>
```
PS C:\> $galleryImageReference = @{Id = '/subscriptions/0296790d-427c-48ca-b204-8b729bbd8670/resourceGroups/swaggertests/providers/Microsoft.Compute/galleries/swaggergallery/images/swaggerimagedef/versions/1.0.0'; Lun=1}
PS C:\> $diskConfig = New-AzDiskConfig -Location 'West US' -CreateOption 'FromImage' -GalleryImageReference $galleryImageReference;
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskConfig
```

<span data-ttu-id="daa29-122">Создайте диск из общей коллекции изображений.</span><span class="sxs-lookup"><span data-stu-id="daa29-122">Create a disk from a Shared Gallery Image Version.</span></span>  <span data-ttu-id="daa29-123">ИД — это id версии изображения коллекции.</span><span class="sxs-lookup"><span data-stu-id="daa29-123">Id is the id of the shared gallery image version.</span></span> <span data-ttu-id="daa29-124">Lun требуется только в том случае, если источником является диск данных.</span><span class="sxs-lookup"><span data-stu-id="daa29-124">Lun is needed only if the source is a data disk.</span></span>

## <span data-ttu-id="daa29-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="daa29-125">PARAMETERS</span></span>

### <span data-ttu-id="daa29-126">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="daa29-126">-CreateOption</span></span>
<span data-ttu-id="daa29-127">Указывает, создает ли этот cmdlet диск в виртуальной машине из платформы или изображения пользователя, создает пустой диск или влог существующий диск.</span><span class="sxs-lookup"><span data-stu-id="daa29-127">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

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

### <span data-ttu-id="daa29-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="daa29-128">-DefaultProfile</span></span>
<span data-ttu-id="daa29-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="daa29-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="daa29-130">-DiskAccessId</span><span class="sxs-lookup"><span data-stu-id="daa29-130">-DiskAccessId</span></span>
<span data-ttu-id="daa29-131">Возвращает или ARM ИД ресурса DiskAccess для использования частных конечных точек.</span><span class="sxs-lookup"><span data-stu-id="daa29-131">Gets or sets ARM ID of the DiskAccess resource for using private endpoints on.</span></span>


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

### <span data-ttu-id="daa29-132">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="daa29-132">-DiskEncryptionKey</span></span>
<span data-ttu-id="daa29-133">Определяет объект ключа шифрования диска на диске.</span><span class="sxs-lookup"><span data-stu-id="daa29-133">Specifies the disk encryption key object on a disk.</span></span>

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

### <span data-ttu-id="daa29-134">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="daa29-134">-DiskEncryptionSetId</span></span>
<span data-ttu-id="daa29-135">Определяет код ресурса набора шифрования диска, который нужно использовать для включения шифрования во время работы.</span><span class="sxs-lookup"><span data-stu-id="daa29-135">Specifies the resource Id of the disk encryption set to use for enabling encryption at rest.</span></span>

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

### <span data-ttu-id="daa29-136">-DiskIOPSReadOnly</span><span class="sxs-lookup"><span data-stu-id="daa29-136">-DiskIOPSReadOnly</span></span>
<span data-ttu-id="daa29-137">Общее количество IOPS, которое будет разрешено для всех ВМ-сообщений, которые имеют общий диск с иконой ReadOnly.</span><span class="sxs-lookup"><span data-stu-id="daa29-137">The total number of IOPS that will be allowed across all VMs mounting the shared disk as ReadOnly.</span></span> <span data-ttu-id="daa29-138">Одна операция может передаваться между 4k и 256k bytes.</span><span class="sxs-lookup"><span data-stu-id="daa29-138">One operation can transfer between 4k and 256k bytes.</span></span>

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

### <span data-ttu-id="daa29-139">-DiskIOPSReadWrite</span><span class="sxs-lookup"><span data-stu-id="daa29-139">-DiskIOPSReadWrite</span></span>
<span data-ttu-id="daa29-140">Количество IOPS, разрешенных для этого диска; только для дисков UltraSSD.</span><span class="sxs-lookup"><span data-stu-id="daa29-140">The number of IOPS allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="daa29-141">Одна операция может передаваться между 4k и 256k bytes.</span><span class="sxs-lookup"><span data-stu-id="daa29-141">One operation can transfer between 4k and 256k bytes.</span></span>

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

### <span data-ttu-id="daa29-142">-DiskMBpsReadOnly</span><span class="sxs-lookup"><span data-stu-id="daa29-142">-DiskMBpsReadOnly</span></span>
<span data-ttu-id="daa29-143">"описание": "Общая пропускная способность (MBPS), которая будет разрешена для всех ВМ-сообщений, которые крепят общий диск как ReadOnly.</span><span class="sxs-lookup"><span data-stu-id="daa29-143">"description": "The total throughput (MBps) that will be allowed across all VMs mounting the shared disk as ReadOnly.</span></span> <span data-ttu-id="daa29-144">MBps означает миллионыбайтов в секунду. В этом случае используется нотация ISO с полномочиями 10.</span><span class="sxs-lookup"><span data-stu-id="daa29-144">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

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

### <span data-ttu-id="daa29-145">-DiskMBpsReadWrite</span><span class="sxs-lookup"><span data-stu-id="daa29-145">-DiskMBpsReadWrite</span></span>
<span data-ttu-id="daa29-146">пропускная способность, допустимая для этого диска; только для дисков UltraSSD.</span><span class="sxs-lookup"><span data-stu-id="daa29-146">The bandwidth allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="daa29-147">MBps означает миллионыбайтов в секунду. В этом случае используется нотация ISO с полномочиями 10.</span><span class="sxs-lookup"><span data-stu-id="daa29-147">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

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

### <span data-ttu-id="daa29-148">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="daa29-148">-DiskSizeGB</span></span>
<span data-ttu-id="daa29-149">Определяет размер диска в ГБ.</span><span class="sxs-lookup"><span data-stu-id="daa29-149">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="daa29-150">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="daa29-150">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="daa29-151">Включить параметры шифрования.</span><span class="sxs-lookup"><span data-stu-id="daa29-151">Enable encryption settings.</span></span>

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

### <span data-ttu-id="daa29-152">-EncryptionType</span><span class="sxs-lookup"><span data-stu-id="daa29-152">-EncryptionType</span></span>
<span data-ttu-id="daa29-153">Тип ключа, используемого для шифрования данных на диске.</span><span class="sxs-lookup"><span data-stu-id="daa29-153">The type of key used to encrypt the data of the disk.</span></span>  <span data-ttu-id="daa29-154">Доступны такие значения: EncryptionAtRestWithPlatformKey, 'EncryptionAtRestWithCustomerKey'</span><span class="sxs-lookup"><span data-stu-id="daa29-154">Available values are: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'</span></span>

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

### <span data-ttu-id="daa29-155">-GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="daa29-155">-GalleryImageReference</span></span>
<span data-ttu-id="daa29-156">Объект GalleryImageReference.</span><span class="sxs-lookup"><span data-stu-id="daa29-156">The GalleryImageReference object.</span></span>  <span data-ttu-id="daa29-157">Требуется при создании из коллекции изображений.</span><span class="sxs-lookup"><span data-stu-id="daa29-157">Required if creating from a Gallery Image.</span></span> <span data-ttu-id="daa29-158">Он будет ARM общего изображения галли, из которого создается диск.</span><span class="sxs-lookup"><span data-stu-id="daa29-158">The id will be the ARM id of the shared galley image version from which to create a disk.</span></span>
<span data-ttu-id="daa29-159">Lun требуется, если источником копии является один из дисков данных в изображении коллекции; Если NULL, будет скопирован диск ОС изображения.</span><span class="sxs-lookup"><span data-stu-id="daa29-159">A lun is needed if the source of the copy is one of the data disks in the gallery image; if null, the OS disk of the image will be copied.</span></span>

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

### <span data-ttu-id="daa29-160">-HyperVGeneration</span><span class="sxs-lookup"><span data-stu-id="daa29-160">-HyperVGeneration</span></span>
<span data-ttu-id="daa29-161">Генерация гипервизора виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="daa29-161">The hypervisor generation of the Virtual Machine.</span></span> <span data-ttu-id="daa29-162">Применимо только к дискам ОС.</span><span class="sxs-lookup"><span data-stu-id="daa29-162">Applicable to OS disks only.</span></span>  <span data-ttu-id="daa29-163">Допустимые значения: V1 и V2.</span><span class="sxs-lookup"><span data-stu-id="daa29-163">Allowed values are V1 and V2.</span></span>

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

### <span data-ttu-id="daa29-164">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="daa29-164">-ImageReference</span></span>
<span data-ttu-id="daa29-165">Указывает ссылку на изображение на диске.</span><span class="sxs-lookup"><span data-stu-id="daa29-165">Specifies the image reference on a disk.</span></span>

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

### <span data-ttu-id="daa29-166">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="daa29-166">-KeyEncryptionKey</span></span>
<span data-ttu-id="daa29-167">Указывает ключ шифрования ключа на диске.</span><span class="sxs-lookup"><span data-stu-id="daa29-167">Specifies the Key encryption key on a disk.</span></span>

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

### <span data-ttu-id="daa29-168">-Location</span><span class="sxs-lookup"><span data-stu-id="daa29-168">-Location</span></span>
<span data-ttu-id="daa29-169">Определяет расположение.</span><span class="sxs-lookup"><span data-stu-id="daa29-169">Specifies a location.</span></span>

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

### <span data-ttu-id="daa29-170">-LogicalSectorSize</span><span class="sxs-lookup"><span data-stu-id="daa29-170">-LogicalSectorSize</span></span>
<span data-ttu-id="daa29-171">Логический размер сектора вбайтов для дисков Ultra.</span><span class="sxs-lookup"><span data-stu-id="daa29-171">Logical sector size in bytes for Ultra disks.</span></span> 

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

### <span data-ttu-id="daa29-172">-MaxSharesCount</span><span class="sxs-lookup"><span data-stu-id="daa29-172">-MaxSharesCount</span></span>
<span data-ttu-id="daa29-173">Максимальное количество ВТБ, которые можно одновременно прикрепить к диску.</span><span class="sxs-lookup"><span data-stu-id="daa29-173">The maximum number of VMs that can attach to the disk at the same time.</span></span>
<span data-ttu-id="daa29-174">Значение больше одного указывает на диск, который может быть одновременно установлен на нескольких ВМ-дисках.</span><span class="sxs-lookup"><span data-stu-id="daa29-174">Value greater than one indicates a disk that can be mounted on multiple VMs at the same time.</span></span>

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

### <span data-ttu-id="daa29-175">-NetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="daa29-175">-NetworkAccessPolicy</span></span>
<span data-ttu-id="daa29-176">Политика доступа к сети определяет политику доступа к сети.</span><span class="sxs-lookup"><span data-stu-id="daa29-176">Network access policy defines the network access policy.</span></span>
<span data-ttu-id="daa29-177">Возможные значения: 'AllowAll', 'AllowPrivate', 'DenyAll'</span><span class="sxs-lookup"><span data-stu-id="daa29-177">Possible values include: 'AllowAll', 'AllowPrivate', 'DenyAll'</span></span>

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

### <span data-ttu-id="daa29-178">-OsType</span><span class="sxs-lookup"><span data-stu-id="daa29-178">-OsType</span></span>
<span data-ttu-id="daa29-179">Тип ОС.</span><span class="sxs-lookup"><span data-stu-id="daa29-179">Specifies the OS type.</span></span>

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

### <span data-ttu-id="daa29-180">-SkuName</span><span class="sxs-lookup"><span data-stu-id="daa29-180">-SkuName</span></span>
<span data-ttu-id="daa29-181">Указывает имя SKU учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="daa29-181">Specifies the Sku name of the storage account.</span></span>  <span data-ttu-id="daa29-182">Доступны значения Standard_LRS, Premium_LRS, StandardSSD_LRS и UltraSSD_LRS.</span><span class="sxs-lookup"><span data-stu-id="daa29-182">Available values are Standard_LRS, Premium_LRS, StandardSSD_LRS, and UltraSSD_LRS.</span></span>  <span data-ttu-id="daa29-183">UltraSSD_LRS можно использовать только с пустым значением для параметра CreateOption.</span><span class="sxs-lookup"><span data-stu-id="daa29-183">UltraSSD_LRS can only be used with Empty value for CreateOption parameter.</span></span>

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

### <span data-ttu-id="daa29-184">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="daa29-184">-SourceResourceId</span></span>
<span data-ttu-id="daa29-185">Определяет код источника ресурсов.</span><span class="sxs-lookup"><span data-stu-id="daa29-185">Specifies the  source resource ID.</span></span>

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

### <span data-ttu-id="daa29-186">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="daa29-186">-SourceUri</span></span>
<span data-ttu-id="daa29-187">Определяет исходный URI.</span><span class="sxs-lookup"><span data-stu-id="daa29-187">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="daa29-188">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="daa29-188">-StorageAccountId</span></span>
<span data-ttu-id="daa29-189">Определяет ИД учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="daa29-189">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="daa29-190">-Tag</span><span class="sxs-lookup"><span data-stu-id="daa29-190">-Tag</span></span>
<span data-ttu-id="daa29-191">Пары значений ключа в виде hash table.</span><span class="sxs-lookup"><span data-stu-id="daa29-191">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="daa29-192">Например: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="daa29-192">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="daa29-193">-Tier</span><span class="sxs-lookup"><span data-stu-id="daa29-193">-Tier</span></span>
<span data-ttu-id="daa29-194">Уровень производительности диска.</span><span class="sxs-lookup"><span data-stu-id="daa29-194">Performance tier of the disk.</span></span>

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

### <span data-ttu-id="daa29-195">-UploadSizeInBytes</span><span class="sxs-lookup"><span data-stu-id="daa29-195">-UploadSizeInBytes</span></span>
<span data-ttu-id="daa29-196">Определяет размер содержимого загружаемого содержимого, включая принудитель VHD при отправке CreateOption.</span><span class="sxs-lookup"><span data-stu-id="daa29-196">Specifies the size of the contents of the upload including the VHD footer when CreateOption is Upload.</span></span>  <span data-ttu-id="daa29-197">Это значение должно быть в период между 20972032 (20 MiB + 512 bytes для footer vHD) и 35183298347520 bytes (32 TiB + 512 bytes for the VHD footer).</span><span class="sxs-lookup"><span data-stu-id="daa29-197">This value should be between 20972032 (20 MiB + 512 bytes for the VHD footer) and 35183298347520 bytes (32 TiB + 512 bytes for the VHD footer).</span></span>

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

### <span data-ttu-id="daa29-198">-Zone</span><span class="sxs-lookup"><span data-stu-id="daa29-198">-Zone</span></span>
<span data-ttu-id="daa29-199">Определяет логический список зон для диска.</span><span class="sxs-lookup"><span data-stu-id="daa29-199">Specifies the logical zone list for Disk.</span></span>

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

### <span data-ttu-id="daa29-200">-Confirm</span><span class="sxs-lookup"><span data-stu-id="daa29-200">-Confirm</span></span>
<span data-ttu-id="daa29-201">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="daa29-201">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="daa29-202">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="daa29-202">-WhatIf</span></span>
<span data-ttu-id="daa29-203">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="daa29-203">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="daa29-204">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="daa29-204">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="daa29-205">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="daa29-205">CommonParameters</span></span>
<span data-ttu-id="daa29-206">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="daa29-206">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="daa29-207">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="daa29-207">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="daa29-208">INPUTS</span><span class="sxs-lookup"><span data-stu-id="daa29-208">INPUTS</span></span>

### <span data-ttu-id="daa29-209">System.String</span><span class="sxs-lookup"><span data-stu-id="daa29-209">System.String</span></span>

### <span data-ttu-id="daa29-210">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="daa29-210">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="daa29-211">System.Int32</span><span class="sxs-lookup"><span data-stu-id="daa29-211">System.Int32</span></span>

### <span data-ttu-id="daa29-212">System.String[]</span><span class="sxs-lookup"><span data-stu-id="daa29-212">System.String[]</span></span>

### <span data-ttu-id="daa29-213">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="daa29-213">System.Collections.Hashtable</span></span>

### <span data-ttu-id="daa29-214">Microsoft.Azure.Management.Compute.Models.ImageDiskReference</span><span class="sxs-lookup"><span data-stu-id="daa29-214">Microsoft.Azure.Management.Compute.Models.ImageDiskReference</span></span>

### <span data-ttu-id="daa29-215">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="daa29-215">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="daa29-216">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="daa29-216">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="daa29-217">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="daa29-217">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="daa29-218">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="daa29-218">OUTPUTS</span></span>

### <span data-ttu-id="daa29-219">Microsoft.Azure.Commands.Compute.Automation.Models.PSDокне</span><span class="sxs-lookup"><span data-stu-id="daa29-219">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="daa29-220">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="daa29-220">NOTES</span></span>

## <span data-ttu-id="daa29-221">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="daa29-221">RELATED LINKS</span></span>

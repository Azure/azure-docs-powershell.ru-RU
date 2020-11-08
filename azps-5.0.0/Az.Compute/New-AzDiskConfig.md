---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azdiskconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskConfig.md
ms.openlocfilehash: ec4d0444ad88fa7536fbf1ee050dc8dcb6a76af3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246248"
---
# <span data-ttu-id="5f0c7-101">New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="5f0c7-101">New-AzDiskConfig</span></span>

## <span data-ttu-id="5f0c7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5f0c7-102">SYNOPSIS</span></span>
<span data-ttu-id="5f0c7-103">Создание настраиваемого объекта диска.</span><span class="sxs-lookup"><span data-stu-id="5f0c7-103">Creates a configurable disk object.</span></span>

## <span data-ttu-id="5f0c7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5f0c7-104">SYNTAX</span></span>

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

## <span data-ttu-id="5f0c7-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5f0c7-105">DESCRIPTION</span></span>
<span data-ttu-id="5f0c7-106">Командлет **New-AzDiskConfig** создает настраиваемый объект диска.</span><span class="sxs-lookup"><span data-stu-id="5f0c7-106">The **New-AzDiskConfig** cmdlet creates a configurable disk object.</span></span>

## <span data-ttu-id="5f0c7-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5f0c7-107">EXAMPLES</span></span>

### <span data-ttu-id="5f0c7-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5f0c7-108">Example 1</span></span>
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

<span data-ttu-id="5f0c7-109">Первая команда создает локальный пустой объект диска с размером 5GB в Standard_LRS типе учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="5f0c7-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span> <span data-ttu-id="5f0c7-110">Она также задает тип операционной системы Windows и включает параметры шифрования.</span><span class="sxs-lookup"><span data-stu-id="5f0c7-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="5f0c7-111">Вторая и третья команды устанавливают параметры ключа шифрования диска и ключа шифрования для объекта диска.</span><span class="sxs-lookup"><span data-stu-id="5f0c7-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span> <span data-ttu-id="5f0c7-112">Последняя команда принимает объект диска и создает диск с именем "Disk01" в группе ресурсов "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="5f0c7-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="5f0c7-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="5f0c7-113">Example 2</span></span>
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

<span data-ttu-id="5f0c7-114">В первой команде создается объект локального диска для отправки.</span><span class="sxs-lookup"><span data-stu-id="5f0c7-114">The first command creates a local disk object for Upload.</span></span>
<span data-ttu-id="5f0c7-115">Вторая команда принимает объект диска и создает диск с именем "Disk01" в группе ресурсов "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="5f0c7-115">The second command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>
<span data-ttu-id="5f0c7-116">Третья команда получает URL-адрес SAS для диска.</span><span class="sxs-lookup"><span data-stu-id="5f0c7-116">The third command gets SAS Url for the disk.</span></span>
<span data-ttu-id="5f0c7-117">Четвертая команда получает состояние диска.</span><span class="sxs-lookup"><span data-stu-id="5f0c7-117">The fourth command gets the state of the disk.</span></span>
<span data-ttu-id="5f0c7-118">Если состояние диска — "ReadyToUpload", пользователь может отправить диск из хранилища BLOB-данных на диск с помощью AzCopy.</span><span class="sxs-lookup"><span data-stu-id="5f0c7-118">If the disk state is 'ReadyToUpload', a user can upload a disk from blob storage to the disk SAS Url using AzCopy.</span></span>
<span data-ttu-id="5f0c7-119">Во время передачи состояние диска изменится на "ActiveUpload".</span><span class="sxs-lookup"><span data-stu-id="5f0c7-119">During uploading, the disk state is changed to 'ActiveUpload'.</span></span>
<span data-ttu-id="5f0c7-120">Последняя команда отзывает доступ к диску по URL-адресу SAS.</span><span class="sxs-lookup"><span data-stu-id="5f0c7-120">The last command revokes the disk access for the SAS Url.</span></span>

### <span data-ttu-id="5f0c7-121">Пример 3</span><span class="sxs-lookup"><span data-stu-id="5f0c7-121">Example 3</span></span>
```
PS C:\> $galleryImageReference = @{Id = '/subscriptions/0296790d-427c-48ca-b204-8b729bbd8670/resourceGroups/swaggertests/providers/Microsoft.Compute/galleries/swaggergallery/images/swaggerimagedef/versions/1.0.0'; Lun=1}
PS C:\> $diskConfig = New-AzDiskConfig -Location 'West US' -CreateOption 'FromImage' -GalleryImageReference $galleryImageReference;
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskConfig
```

<span data-ttu-id="5f0c7-122">Создание диска из общей версии образа коллекции.</span><span class="sxs-lookup"><span data-stu-id="5f0c7-122">Create a disk from a Shared Gallery Image Version.</span></span>  <span data-ttu-id="5f0c7-123">ID — идентификатор общей версии образа коллекции.</span><span class="sxs-lookup"><span data-stu-id="5f0c7-123">Id is the id of the shared gallery image version.</span></span> <span data-ttu-id="5f0c7-124">LUN нужен только в том случае, если источником является диск с данными.</span><span class="sxs-lookup"><span data-stu-id="5f0c7-124">Lun is needed only if the source is a data disk.</span></span>

## <span data-ttu-id="5f0c7-125">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5f0c7-125">PARAMETERS</span></span>

### <span data-ttu-id="5f0c7-126">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="5f0c7-126">-CreateOption</span></span>
<span data-ttu-id="5f0c7-127">Указывает, создает ли этот командлет диск на виртуальной машине из платформы или пользовательского образа, создает пустой диск или прикрепляет существующий диск.</span><span class="sxs-lookup"><span data-stu-id="5f0c7-127">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

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

### <span data-ttu-id="5f0c7-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f0c7-128">-DefaultProfile</span></span>
<span data-ttu-id="5f0c7-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5f0c7-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5f0c7-130">-DiskAccessId</span><span class="sxs-lookup"><span data-stu-id="5f0c7-130">-DiskAccessId</span></span>
<span data-ttu-id="5f0c7-131">Возвращает или задает идентификатор ARM ресурса DiskAccess для использования закрытых конечных точек.</span><span class="sxs-lookup"><span data-stu-id="5f0c7-131">Gets or sets ARM ID of the DiskAccess resource for using private endpoints on.</span></span>


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

### <span data-ttu-id="5f0c7-132">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="5f0c7-132">-DiskEncryptionKey</span></span>
<span data-ttu-id="5f0c7-133">Указывает объект ключа шифрования диска на диске.</span><span class="sxs-lookup"><span data-stu-id="5f0c7-133">Specifies the disk encryption key object on a disk.</span></span>

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

### <span data-ttu-id="5f0c7-134">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="5f0c7-134">-DiskEncryptionSetId</span></span>
<span data-ttu-id="5f0c7-135">Указывает идентификатор ресурса, установленный для шифрования диска, используемого для включения шифрования на остальных.</span><span class="sxs-lookup"><span data-stu-id="5f0c7-135">Specifies the resource Id of the disk encryption set to use for enabling encryption at rest.</span></span>

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

### <span data-ttu-id="5f0c7-136">-DiskIOPSReadOnly</span><span class="sxs-lookup"><span data-stu-id="5f0c7-136">-DiskIOPSReadOnly</span></span>
<span data-ttu-id="5f0c7-137">Общее количество операций ввода/вывода, которые будут разрешены на всех виртуальных машинах, применяющих общий диск для чтения.</span><span class="sxs-lookup"><span data-stu-id="5f0c7-137">The total number of IOPS that will be allowed across all VMs mounting the shared disk as ReadOnly.</span></span> <span data-ttu-id="5f0c7-138">Одна операция может переключаться между 4 КБ и 256 Кбайт.</span><span class="sxs-lookup"><span data-stu-id="5f0c7-138">One operation can transfer between 4k and 256k bytes.</span></span>

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

### <span data-ttu-id="5f0c7-139">-DiskIOPSReadWrite</span><span class="sxs-lookup"><span data-stu-id="5f0c7-139">-DiskIOPSReadWrite</span></span>
<span data-ttu-id="5f0c7-140">Количество операций ввода/вывода, разрешенных для этого диска; только устанавливаемые для UltraSSD дисков.</span><span class="sxs-lookup"><span data-stu-id="5f0c7-140">The number of IOPS allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="5f0c7-141">Одна операция может переключаться между 4 КБ и 256 Кбайт.</span><span class="sxs-lookup"><span data-stu-id="5f0c7-141">One operation can transfer between 4k and 256k bytes.</span></span>

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

### <span data-ttu-id="5f0c7-142">-DiskMBpsReadOnly</span><span class="sxs-lookup"><span data-stu-id="5f0c7-142">-DiskMBpsReadOnly</span></span>
<span data-ttu-id="5f0c7-143">"Описание": "Общая пропускная способность (Мбит/с), которая будет разрешена на всех виртуальных машинах, применяющих общий диск для чтения.</span><span class="sxs-lookup"><span data-stu-id="5f0c7-143">"description": "The total throughput (MBps) that will be allowed across all VMs mounting the shared disk as ReadOnly.</span></span> <span data-ttu-id="5f0c7-144">Мбит/с — миллионные байты в секунду – используется нотация ISO с числом степеней 10.</span><span class="sxs-lookup"><span data-stu-id="5f0c7-144">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

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

### <span data-ttu-id="5f0c7-145">-DiskMBpsReadWrite</span><span class="sxs-lookup"><span data-stu-id="5f0c7-145">-DiskMBpsReadWrite</span></span>
<span data-ttu-id="5f0c7-146">Пропускная способность, разрешенная для этого диска; только устанавливаемые для UltraSSD дисков.</span><span class="sxs-lookup"><span data-stu-id="5f0c7-146">The bandwidth allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="5f0c7-147">Мбит/с — миллионные байты в секунду – используется нотация ISO с числом степеней 10.</span><span class="sxs-lookup"><span data-stu-id="5f0c7-147">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

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

### <span data-ttu-id="5f0c7-148">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="5f0c7-148">-DiskSizeGB</span></span>
<span data-ttu-id="5f0c7-149">Задает размер диска в ГБ.</span><span class="sxs-lookup"><span data-stu-id="5f0c7-149">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="5f0c7-150">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="5f0c7-150">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="5f0c7-151">Включите параметры шифрования.</span><span class="sxs-lookup"><span data-stu-id="5f0c7-151">Enable encryption settings.</span></span>

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

### <span data-ttu-id="5f0c7-152">-EncryptionType</span><span class="sxs-lookup"><span data-stu-id="5f0c7-152">-EncryptionType</span></span>
<span data-ttu-id="5f0c7-153">Тип ключа, используемого для шифрования данных диска.</span><span class="sxs-lookup"><span data-stu-id="5f0c7-153">The type of key used to encrypt the data of the disk.</span></span>  <span data-ttu-id="5f0c7-154">Доступны следующие значения: "EncryptionAtRestWithPlatformKey", "EncryptionAtRestWithCustomerKey"</span><span class="sxs-lookup"><span data-stu-id="5f0c7-154">Available values are: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'</span></span>

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

### <span data-ttu-id="5f0c7-155">-GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="5f0c7-155">-GalleryImageReference</span></span>
<span data-ttu-id="5f0c7-156">Объект GalleryImageReference.</span><span class="sxs-lookup"><span data-stu-id="5f0c7-156">The GalleryImageReference object.</span></span>  <span data-ttu-id="5f0c7-157">Требуется при создании из изображения коллекции.</span><span class="sxs-lookup"><span data-stu-id="5f0c7-157">Required if creating from a Gallery Image.</span></span> <span data-ttu-id="5f0c7-158">Идентификатором будет идентификатор ARM для общей версии изображения програнка, из которой нужно создать диск.</span><span class="sxs-lookup"><span data-stu-id="5f0c7-158">The id will be the ARM id of the shared galley image version from which to create a disk.</span></span>
<span data-ttu-id="5f0c7-159">LUN нужен, если источником копии является один из дисков данных в образе коллекции; Если значение равно null, будет скопирован диск операционной системы образа.</span><span class="sxs-lookup"><span data-stu-id="5f0c7-159">A lun is needed if the source of the copy is one of the data disks in the gallery image; if null, the OS disk of the image will be copied.</span></span>

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

### <span data-ttu-id="5f0c7-160">-HyperVGeneration</span><span class="sxs-lookup"><span data-stu-id="5f0c7-160">-HyperVGeneration</span></span>
<span data-ttu-id="5f0c7-161">Создание гипервизора виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="5f0c7-161">The hypervisor generation of the Virtual Machine.</span></span> <span data-ttu-id="5f0c7-162">Применимо только к дискам ОС.</span><span class="sxs-lookup"><span data-stu-id="5f0c7-162">Applicable to OS disks only.</span></span>  <span data-ttu-id="5f0c7-163">Допустимые значения: v1 и v2.</span><span class="sxs-lookup"><span data-stu-id="5f0c7-163">Allowed values are V1 and V2.</span></span>

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

### <span data-ttu-id="5f0c7-164">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="5f0c7-164">-ImageReference</span></span>
<span data-ttu-id="5f0c7-165">Указывает ссылку на изображение на диске.</span><span class="sxs-lookup"><span data-stu-id="5f0c7-165">Specifies the image reference on a disk.</span></span>

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

### <span data-ttu-id="5f0c7-166">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="5f0c7-166">-KeyEncryptionKey</span></span>
<span data-ttu-id="5f0c7-167">Задает ключ шифрования ключа на диске.</span><span class="sxs-lookup"><span data-stu-id="5f0c7-167">Specifies the Key encryption key on a disk.</span></span>

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

### <span data-ttu-id="5f0c7-168">-Location</span><span class="sxs-lookup"><span data-stu-id="5f0c7-168">-Location</span></span>
<span data-ttu-id="5f0c7-169">Задает расположение.</span><span class="sxs-lookup"><span data-stu-id="5f0c7-169">Specifies a location.</span></span>

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

### <span data-ttu-id="5f0c7-170">-LogicalSectorSize</span><span class="sxs-lookup"><span data-stu-id="5f0c7-170">-LogicalSectorSize</span></span>
<span data-ttu-id="5f0c7-171">Размер логического сектора в байтах для Ultra Disks.</span><span class="sxs-lookup"><span data-stu-id="5f0c7-171">Logical sector size in bytes for Ultra disks.</span></span> 

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

### <span data-ttu-id="5f0c7-172">-MaxSharesCount</span><span class="sxs-lookup"><span data-stu-id="5f0c7-172">-MaxSharesCount</span></span>
<span data-ttu-id="5f0c7-173">Максимальное количество виртуальных машин, которые могут одновременно присоединиться к диску.</span><span class="sxs-lookup"><span data-stu-id="5f0c7-173">The maximum number of VMs that can attach to the disk at the same time.</span></span>
<span data-ttu-id="5f0c7-174">Значение больше единицы указывает диск, который можно подключить к нескольким виртуальным машинам одновременно.</span><span class="sxs-lookup"><span data-stu-id="5f0c7-174">Value greater than one indicates a disk that can be mounted on multiple VMs at the same time.</span></span>

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

### <span data-ttu-id="5f0c7-175">-NetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="5f0c7-175">-NetworkAccessPolicy</span></span>
<span data-ttu-id="5f0c7-176">Политика доступа к сети определяет политику доступа к сети.</span><span class="sxs-lookup"><span data-stu-id="5f0c7-176">Network access policy defines the network access policy.</span></span>
<span data-ttu-id="5f0c7-177">Возможные значения: "AllowAll", "AllowPrivate", "DenyAll"</span><span class="sxs-lookup"><span data-stu-id="5f0c7-177">Possible values include: 'AllowAll', 'AllowPrivate', 'DenyAll'</span></span>

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

### <span data-ttu-id="5f0c7-178">-OsType</span><span class="sxs-lookup"><span data-stu-id="5f0c7-178">-OsType</span></span>
<span data-ttu-id="5f0c7-179">Указывает тип операционной системы.</span><span class="sxs-lookup"><span data-stu-id="5f0c7-179">Specifies the OS type.</span></span>

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

### <span data-ttu-id="5f0c7-180">-SkuName</span><span class="sxs-lookup"><span data-stu-id="5f0c7-180">-SkuName</span></span>
<span data-ttu-id="5f0c7-181">Указывает имя SKU учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="5f0c7-181">Specifies the Sku name of the storage account.</span></span>  <span data-ttu-id="5f0c7-182">Доступные значения: Standard_LRS, Premium_LRS, StandardSSD_LRS и UltraSSD_LRS.</span><span class="sxs-lookup"><span data-stu-id="5f0c7-182">Available values are Standard_LRS, Premium_LRS, StandardSSD_LRS, and UltraSSD_LRS.</span></span>  <span data-ttu-id="5f0c7-183">UltraSSD_LRS можно использовать только с пустым значением для параметра CreateOption.</span><span class="sxs-lookup"><span data-stu-id="5f0c7-183">UltraSSD_LRS can only be used with Empty value for CreateOption parameter.</span></span>

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

### <span data-ttu-id="5f0c7-184">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="5f0c7-184">-SourceResourceId</span></span>
<span data-ttu-id="5f0c7-185">Указывает исходный идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="5f0c7-185">Specifies the  source resource ID.</span></span>

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

### <span data-ttu-id="5f0c7-186">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="5f0c7-186">-SourceUri</span></span>
<span data-ttu-id="5f0c7-187">Указывает универсальный код ресурса (URI) источника.</span><span class="sxs-lookup"><span data-stu-id="5f0c7-187">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="5f0c7-188">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="5f0c7-188">-StorageAccountId</span></span>
<span data-ttu-id="5f0c7-189">Указывает идентификатор учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="5f0c7-189">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="5f0c7-190">-Тег</span><span class="sxs-lookup"><span data-stu-id="5f0c7-190">-Tag</span></span>
<span data-ttu-id="5f0c7-191">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="5f0c7-191">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="5f0c7-192">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="5f0c7-192">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="5f0c7-193">Уровень</span><span class="sxs-lookup"><span data-stu-id="5f0c7-193">-Tier</span></span>
<span data-ttu-id="5f0c7-194">Уровень производительности диска.</span><span class="sxs-lookup"><span data-stu-id="5f0c7-194">Performance tier of the disk.</span></span>

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

### <span data-ttu-id="5f0c7-195">-UploadSizeInBytes</span><span class="sxs-lookup"><span data-stu-id="5f0c7-195">-UploadSizeInBytes</span></span>
<span data-ttu-id="5f0c7-196">Указывает размер содержимого отправки, включая нижний колонтитул виртуального жесткого диска при отправке CreateOption.</span><span class="sxs-lookup"><span data-stu-id="5f0c7-196">Specifies the size of the contents of the upload including the VHD footer when CreateOption is Upload.</span></span>  <span data-ttu-id="5f0c7-197">Это значение должно быть между 20972032 (20 MiB + 512 байт для нижнего колонтитула VHD) и 35183298347520 байт (32 TiB + 512 байт для нижнего колонтитула VHD).</span><span class="sxs-lookup"><span data-stu-id="5f0c7-197">This value should be between 20972032 (20 MiB + 512 bytes for the VHD footer) and 35183298347520 bytes (32 TiB + 512 bytes for the VHD footer).</span></span>

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

### <span data-ttu-id="5f0c7-198">-Zone</span><span class="sxs-lookup"><span data-stu-id="5f0c7-198">-Zone</span></span>
<span data-ttu-id="5f0c7-199">Указывает список логических зон для диска.</span><span class="sxs-lookup"><span data-stu-id="5f0c7-199">Specifies the logical zone list for Disk.</span></span>

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

### <span data-ttu-id="5f0c7-200">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5f0c7-200">-Confirm</span></span>
<span data-ttu-id="5f0c7-201">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5f0c7-201">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f0c7-202">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f0c7-202">-WhatIf</span></span>
<span data-ttu-id="5f0c7-203">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5f0c7-203">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5f0c7-204">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5f0c7-204">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5f0c7-205">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f0c7-205">CommonParameters</span></span>
<span data-ttu-id="5f0c7-206">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5f0c7-206">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f0c7-207">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5f0c7-207">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f0c7-208">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5f0c7-208">INPUTS</span></span>

### <span data-ttu-id="5f0c7-209">System. String</span><span class="sxs-lookup"><span data-stu-id="5f0c7-209">System.String</span></span>

### <span data-ttu-id="5f0c7-210">System. Nullable "1 [[Microsoft. Azure. Management. COMPUTE. Model. OperatingSystemTypes, Microsoft. Azure. Management. COMPUTE, Version = 23.0.0.0, культура =" нейтрально ", PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="5f0c7-210">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="5f0c7-211">System. Int32</span><span class="sxs-lookup"><span data-stu-id="5f0c7-211">System.Int32</span></span>

### <span data-ttu-id="5f0c7-212">System. String []</span><span class="sxs-lookup"><span data-stu-id="5f0c7-212">System.String[]</span></span>

### <span data-ttu-id="5f0c7-213">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="5f0c7-213">System.Collections.Hashtable</span></span>

### <span data-ttu-id="5f0c7-214">Microsoft. Azure. Management. COMPUTE. Models. ImageDiskReference</span><span class="sxs-lookup"><span data-stu-id="5f0c7-214">Microsoft.Azure.Management.Compute.Models.ImageDiskReference</span></span>

### <span data-ttu-id="5f0c7-215">System. Nullable "1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="5f0c7-215">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="5f0c7-216">Microsoft. Azure. Management. COMPUTE. Models. KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="5f0c7-216">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="5f0c7-217">Microsoft. Azure. Management. COMPUTE. Models. KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="5f0c7-217">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="5f0c7-218">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5f0c7-218">OUTPUTS</span></span>

### <span data-ttu-id="5f0c7-219">Microsoft.Azure.Commands.Compute.Automation.Models.PSDISK</span><span class="sxs-lookup"><span data-stu-id="5f0c7-219">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="5f0c7-220">Пуск</span><span class="sxs-lookup"><span data-stu-id="5f0c7-220">NOTES</span></span>

## <span data-ttu-id="5f0c7-221">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5f0c7-221">RELATED LINKS</span></span>

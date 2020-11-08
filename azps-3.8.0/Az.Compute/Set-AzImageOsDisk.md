---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azimageosdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzImageOsDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzImageOsDisk.md
ms.openlocfilehash: 45f3e8f76e6f8ff3a5684fbd8f9ebf42e7a8e252
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94072872"
---
# <span data-ttu-id="94814-101">Set-AzImageOsDisk</span><span class="sxs-lookup"><span data-stu-id="94814-101">Set-AzImageOsDisk</span></span>

## <span data-ttu-id="94814-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="94814-102">SYNOPSIS</span></span>
<span data-ttu-id="94814-103">Задает свойства диска операционной системы для объекта Image.</span><span class="sxs-lookup"><span data-stu-id="94814-103">Sets the operating system disk properties on an image object.</span></span>

## <span data-ttu-id="94814-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="94814-104">SYNTAX</span></span>

```
Set-AzImageOsDisk [-Image] <PSImage> [[-OsType] <OperatingSystemTypes>]
 [[-OsState] <OperatingSystemStateTypes>] [[-BlobUri] <String>] [-Caching <CachingTypes>] [-DiskSizeGB <Int32>]
 [-StorageAccountType <String>] [-SnapshotId <String>] [-ManagedDiskId <String>]
 [-DiskEncryptionSetId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="94814-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="94814-105">DESCRIPTION</span></span>
<span data-ttu-id="94814-106">Командлет **Set-AzImageOsDisk** задает свойства диска операционной системы для объекта Image.</span><span class="sxs-lookup"><span data-stu-id="94814-106">The **Set-AzImageOsDisk** cmdlet sets the operating system disk properties on an image object.</span></span>

## <span data-ttu-id="94814-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="94814-107">EXAMPLES</span></span>

### <span data-ttu-id="94814-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="94814-108">Example 1</span></span>
```
PS C:\> $imageConfig = New-AzImageConfig -Location 'West US';
PS C:\> $osDiskVhdUri = "https://contoso.blob.core.windows.net/test/os.vhd"
PS C:\> $dataDiskVhdUri1 = "https://contoso.blob.core.windows.net/test/data1.vhd"
PS C:\> $dataDiskVhdUri2 = "https://contoso.blob.core.windows.net/test/data2.vhd"
PS C:\> Set-AzImageOsDisk -Image $imageConfig -OsType 'Windows' -OsState 'Generalized' -BlobUri $osDiskVhdUri;
PS C:\> Add-AzImageDataDisk -Image $imageConfig -Lun 1 -BlobUri $dataDiskVhdUri1;
PS C:\> Add-AzImageDataDisk -Image $imageConfig -Lun 2 -BlobUri $dataDiskVhdUri2;
PS C:\> New-AzImage -Image $imageConfig -ImageName 'ImageName01' -ResourceGroupName 'ResourceGroup01';
```

<span data-ttu-id="94814-109">В первой команде создается объект Image, который затем сохраняется в переменной $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="94814-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>
<span data-ttu-id="94814-110">Следующие три команды назначают пути к диску операционной системы и двум дискам данных в $osDiskVhdUri, $dataDiskVhdUri 1 и $dataDiskVhdUri 2 переменные.</span><span class="sxs-lookup"><span data-stu-id="94814-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="94814-111">Этот подход предназначен для чтения следующих команд.</span><span class="sxs-lookup"><span data-stu-id="94814-111">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="94814-112">Следующие три команды добавляют диск операционной системы и два диска данных в образ, хранящийся в $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="94814-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="94814-113">Универсальный код ресурса (URI) каждого диска хранится в $osDiskVhdUri, $dataDiskVhdUri 1 и $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="94814-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>
<span data-ttu-id="94814-114">Последняя команда создает изображение с именем "ImageName01" в группе ресурсов "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="94814-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="94814-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="94814-115">PARAMETERS</span></span>

### <span data-ttu-id="94814-116">-BlobUri</span><span class="sxs-lookup"><span data-stu-id="94814-116">-BlobUri</span></span>
<span data-ttu-id="94814-117">Задает универсальный код ресурса (URI) большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="94814-117">Specifies the Uri of the blob.</span></span>

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

### <span data-ttu-id="94814-118">-Caching</span><span class="sxs-lookup"><span data-stu-id="94814-118">-Caching</span></span>
<span data-ttu-id="94814-119">Задает режим кэширования диска.</span><span class="sxs-lookup"><span data-stu-id="94814-119">Specifies the caching mode of the disk.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.CachingTypes]
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94814-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94814-120">-DefaultProfile</span></span>
<span data-ttu-id="94814-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="94814-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="94814-122">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="94814-122">-DiskEncryptionSetId</span></span>
<span data-ttu-id="94814-123">Указывает идентификатор ресурса набора шифрования диска, управляемого клиентом.</span><span class="sxs-lookup"><span data-stu-id="94814-123">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="94814-124">Это может быть указано только для управляемого диска.</span><span class="sxs-lookup"><span data-stu-id="94814-124">This can only be specified for managed disk.</span></span>

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

### <span data-ttu-id="94814-125">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="94814-125">-DiskSizeGB</span></span>
<span data-ttu-id="94814-126">Задает размер диска в ГБ.</span><span class="sxs-lookup"><span data-stu-id="94814-126">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="94814-127">-Image</span><span class="sxs-lookup"><span data-stu-id="94814-127">-Image</span></span>
<span data-ttu-id="94814-128">Указывает локальный объект изображения.</span><span class="sxs-lookup"><span data-stu-id="94814-128">Specifies a local image object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSImage
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="94814-129">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="94814-129">-ManagedDiskId</span></span>
<span data-ttu-id="94814-130">Указывает идентификатор управляемого диска.</span><span class="sxs-lookup"><span data-stu-id="94814-130">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="94814-131">-OsState</span><span class="sxs-lookup"><span data-stu-id="94814-131">-OsState</span></span>
<span data-ttu-id="94814-132">Указывает состояние операционной системы.</span><span class="sxs-lookup"><span data-stu-id="94814-132">Specifies the OS state.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes]
Parameter Sets: (All)
Aliases:
Accepted values: Generalized, Specialized

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94814-133">-OsType</span><span class="sxs-lookup"><span data-stu-id="94814-133">-OsType</span></span>
<span data-ttu-id="94814-134">Указывает тип операционной системы.</span><span class="sxs-lookup"><span data-stu-id="94814-134">Specifies the OS type.</span></span>

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

### <span data-ttu-id="94814-135">-SnapshotId</span><span class="sxs-lookup"><span data-stu-id="94814-135">-SnapshotId</span></span>
<span data-ttu-id="94814-136">Указывает идентификатор снимка.</span><span class="sxs-lookup"><span data-stu-id="94814-136">Specifies the ID of a snapshot.</span></span>

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

### <span data-ttu-id="94814-137">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="94814-137">-StorageAccountType</span></span>
<span data-ttu-id="94814-138">Тип учетной записи хранения на диске образа операционной системы</span><span class="sxs-lookup"><span data-stu-id="94814-138">The Storage Account type of Os Image Disk</span></span>

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

### <span data-ttu-id="94814-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="94814-139">-Confirm</span></span>
<span data-ttu-id="94814-140">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="94814-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94814-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94814-141">-WhatIf</span></span>
<span data-ttu-id="94814-142">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="94814-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="94814-143">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="94814-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94814-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94814-144">CommonParameters</span></span>
<span data-ttu-id="94814-145">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="94814-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94814-146">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="94814-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94814-147">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="94814-147">INPUTS</span></span>

### <span data-ttu-id="94814-148">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="94814-148">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

### <span data-ttu-id="94814-149">System. Nullable "1 [[Microsoft. Azure. Management. COMPUTE. Model. OperatingSystemTypes, Microsoft. Azure. Management. COMPUTE, Version = 23.0.0.0, культура =" нейтрально ", PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="94814-149">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="94814-150">System. Nullable "1 [[Microsoft. Azure. Management. COMPUTE. Model. OperatingSystemStateTypes, Microsoft. Azure. Management. COMPUTE, Version = 23.0.0.0, культура =" нейтрально ", PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="94814-150">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="94814-151">System. String</span><span class="sxs-lookup"><span data-stu-id="94814-151">System.String</span></span>

### <span data-ttu-id="94814-152">System. Nullable "1 [[Microsoft. Azure. Management. COMPUTE. Model. CachingTypes, Microsoft. Azure. Management. COMPUTE, Version = 23.0.0.0, культура =" нейтрально ", PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="94814-152">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="94814-153">System. Int32</span><span class="sxs-lookup"><span data-stu-id="94814-153">System.Int32</span></span>

## <span data-ttu-id="94814-154">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="94814-154">OUTPUTS</span></span>

### <span data-ttu-id="94814-155">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="94814-155">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="94814-156">Пуск</span><span class="sxs-lookup"><span data-stu-id="94814-156">NOTES</span></span>

## <span data-ttu-id="94814-157">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="94814-157">RELATED LINKS</span></span>

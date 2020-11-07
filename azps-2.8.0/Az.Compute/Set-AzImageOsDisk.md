---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azimageosdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzImageOsDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzImageOsDisk.md
ms.openlocfilehash: 8cca0499d89656a2c95c971c66812b4663c3076b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721716"
---
# <span data-ttu-id="3f75e-101">Set-AzImageOsDisk</span><span class="sxs-lookup"><span data-stu-id="3f75e-101">Set-AzImageOsDisk</span></span>

## <span data-ttu-id="3f75e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3f75e-102">SYNOPSIS</span></span>
<span data-ttu-id="3f75e-103">Задает свойства диска операционной системы для объекта Image.</span><span class="sxs-lookup"><span data-stu-id="3f75e-103">Sets the operating system disk properties on an image object.</span></span>

## <span data-ttu-id="3f75e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3f75e-104">SYNTAX</span></span>

```
Set-AzImageOsDisk [-Image] <PSImage> [[-OsType] <OperatingSystemTypes>]
 [[-OsState] <OperatingSystemStateTypes>] [[-BlobUri] <String>] [-Caching <CachingTypes>] [-DiskSizeGB <Int32>]
 [-StorageAccountType <String>] [-SnapshotId <String>] [-ManagedDiskId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3f75e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3f75e-105">DESCRIPTION</span></span>
<span data-ttu-id="3f75e-106">Командлет **Set-AzImageOsDisk** задает свойства диска операционной системы для объекта Image.</span><span class="sxs-lookup"><span data-stu-id="3f75e-106">The **Set-AzImageOsDisk** cmdlet sets the operating system disk properties on an image object.</span></span>

## <span data-ttu-id="3f75e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3f75e-107">EXAMPLES</span></span>

### <span data-ttu-id="3f75e-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3f75e-108">Example 1</span></span>
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

<span data-ttu-id="3f75e-109">В первой команде создается объект Image, который затем сохраняется в переменной $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="3f75e-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>
<span data-ttu-id="3f75e-110">Следующие три команды назначают пути к диску операционной системы и двум дискам данных в $osDiskVhdUri, $dataDiskVhdUri 1 и $dataDiskVhdUri 2 переменные.</span><span class="sxs-lookup"><span data-stu-id="3f75e-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="3f75e-111">Этот подход предназначен для чтения следующих команд.</span><span class="sxs-lookup"><span data-stu-id="3f75e-111">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="3f75e-112">Следующие три команды добавляют диск операционной системы и два диска данных в образ, хранящийся в $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="3f75e-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="3f75e-113">Универсальный код ресурса (URI) каждого диска хранится в $osDiskVhdUri, $dataDiskVhdUri 1 и $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="3f75e-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>
<span data-ttu-id="3f75e-114">Последняя команда создает изображение с именем "ImageName01" в группе ресурсов "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="3f75e-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="3f75e-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3f75e-115">PARAMETERS</span></span>

### <span data-ttu-id="3f75e-116">-BlobUri</span><span class="sxs-lookup"><span data-stu-id="3f75e-116">-BlobUri</span></span>
<span data-ttu-id="3f75e-117">Задает универсальный код ресурса (URI) большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="3f75e-117">Specifies the Uri of the blob.</span></span>

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

### <span data-ttu-id="3f75e-118">-Caching</span><span class="sxs-lookup"><span data-stu-id="3f75e-118">-Caching</span></span>
<span data-ttu-id="3f75e-119">Задает режим кэширования диска.</span><span class="sxs-lookup"><span data-stu-id="3f75e-119">Specifies the caching mode of the disk.</span></span>

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

### <span data-ttu-id="3f75e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f75e-120">-DefaultProfile</span></span>
<span data-ttu-id="3f75e-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3f75e-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3f75e-122">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="3f75e-122">-DiskSizeGB</span></span>
<span data-ttu-id="3f75e-123">Задает размер диска в ГБ.</span><span class="sxs-lookup"><span data-stu-id="3f75e-123">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="3f75e-124">-Image</span><span class="sxs-lookup"><span data-stu-id="3f75e-124">-Image</span></span>
<span data-ttu-id="3f75e-125">Указывает локальный объект изображения.</span><span class="sxs-lookup"><span data-stu-id="3f75e-125">Specifies a local image object.</span></span>

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

### <span data-ttu-id="3f75e-126">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="3f75e-126">-ManagedDiskId</span></span>
<span data-ttu-id="3f75e-127">Указывает идентификатор управляемого диска.</span><span class="sxs-lookup"><span data-stu-id="3f75e-127">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="3f75e-128">-OsState</span><span class="sxs-lookup"><span data-stu-id="3f75e-128">-OsState</span></span>
<span data-ttu-id="3f75e-129">Указывает состояние операционной системы.</span><span class="sxs-lookup"><span data-stu-id="3f75e-129">Specifies the OS state.</span></span>

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

### <span data-ttu-id="3f75e-130">-OsType</span><span class="sxs-lookup"><span data-stu-id="3f75e-130">-OsType</span></span>
<span data-ttu-id="3f75e-131">Указывает тип операционной системы.</span><span class="sxs-lookup"><span data-stu-id="3f75e-131">Specifies the OS type.</span></span>

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

### <span data-ttu-id="3f75e-132">-SnapshotId</span><span class="sxs-lookup"><span data-stu-id="3f75e-132">-SnapshotId</span></span>
<span data-ttu-id="3f75e-133">Указывает идентификатор снимка.</span><span class="sxs-lookup"><span data-stu-id="3f75e-133">Specifies the ID of a snapshot.</span></span>

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

### <span data-ttu-id="3f75e-134">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="3f75e-134">-StorageAccountType</span></span>
<span data-ttu-id="3f75e-135">Тип учетной записи хранения на диске образа операционной системы</span><span class="sxs-lookup"><span data-stu-id="3f75e-135">The Storage Account type of Os Image Disk</span></span>

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

### <span data-ttu-id="3f75e-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3f75e-136">-Confirm</span></span>
<span data-ttu-id="3f75e-137">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3f75e-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f75e-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f75e-138">-WhatIf</span></span>
<span data-ttu-id="3f75e-139">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3f75e-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3f75e-140">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3f75e-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f75e-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f75e-141">CommonParameters</span></span>
<span data-ttu-id="3f75e-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3f75e-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f75e-143">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3f75e-143">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f75e-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3f75e-144">INPUTS</span></span>

### <span data-ttu-id="3f75e-145">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="3f75e-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

### <span data-ttu-id="3f75e-146">System. Nullable "1 [[Microsoft. Azure. Management. COMPUTE. Model. OperatingSystemTypes, Microsoft. Azure. Management. COMPUTE, Version = 23.0.0.0, культура =" нейтрально ", PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="3f75e-146">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="3f75e-147">System. Nullable "1 [[Microsoft. Azure. Management. COMPUTE. Model. OperatingSystemStateTypes, Microsoft. Azure. Management. COMPUTE, Version = 23.0.0.0, культура =" нейтрально ", PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="3f75e-147">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="3f75e-148">System. String</span><span class="sxs-lookup"><span data-stu-id="3f75e-148">System.String</span></span>

### <span data-ttu-id="3f75e-149">System. Nullable "1 [[Microsoft. Azure. Management. COMPUTE. Model. CachingTypes, Microsoft. Azure. Management. COMPUTE, Version = 23.0.0.0, культура =" нейтрально ", PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="3f75e-149">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="3f75e-150">System. Int32</span><span class="sxs-lookup"><span data-stu-id="3f75e-150">System.Int32</span></span>

## <span data-ttu-id="3f75e-151">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3f75e-151">OUTPUTS</span></span>

### <span data-ttu-id="3f75e-152">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="3f75e-152">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="3f75e-153">Пуск</span><span class="sxs-lookup"><span data-stu-id="3f75e-153">NOTES</span></span>

## <span data-ttu-id="3f75e-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3f75e-154">RELATED LINKS</span></span>

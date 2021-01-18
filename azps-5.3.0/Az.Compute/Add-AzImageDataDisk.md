---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azimagedatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzImageDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzImageDataDisk.md
ms.openlocfilehash: 0a50aa781177adb6ff457c3cc7d0a59ad8b350d0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98519666"
---
# <span data-ttu-id="7b9c8-101">Add-AzImageDataDisk</span><span class="sxs-lookup"><span data-stu-id="7b9c8-101">Add-AzImageDataDisk</span></span>

## <span data-ttu-id="7b9c8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7b9c8-102">SYNOPSIS</span></span>
<span data-ttu-id="7b9c8-103">Добавляет диск данных к объекту изображения.</span><span class="sxs-lookup"><span data-stu-id="7b9c8-103">Adds a data disk to an image object.</span></span>

## <span data-ttu-id="7b9c8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7b9c8-104">SYNTAX</span></span>

```
Add-AzImageDataDisk [-Image] <PSImage> [[-Lun] <Int32>] [[-BlobUri] <String>] [[-Caching] <CachingTypes>]
 [-DiskSizeGB <Int32>] [-StorageAccountType <String>] [-SnapshotId <String>] [-ManagedDiskId <String>]
 [-DiskEncryptionSetId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7b9c8-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7b9c8-105">DESCRIPTION</span></span>
<span data-ttu-id="7b9c8-106">Для добавления диска данных к объекту изображения добавляется диск данных **Add-AzImageDataDisk.**</span><span class="sxs-lookup"><span data-stu-id="7b9c8-106">The **Add-AzImageDataDisk** cmdlet adds a data disk to an image object.</span></span>

## <span data-ttu-id="7b9c8-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7b9c8-107">EXAMPLES</span></span>

### <span data-ttu-id="7b9c8-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7b9c8-108">Example 1</span></span>
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

<span data-ttu-id="7b9c8-109">Первая команда создает объект изображения, а затем сохраняет его в переменной $imageConfig изображения.</span><span class="sxs-lookup"><span data-stu-id="7b9c8-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>
<span data-ttu-id="7b9c8-110">Следующие три команды назначают пути диска операционной системы и двух дисков данных переменным $osDiskVhdUri, $dataDiskVhdUri 1 и $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="7b9c8-110">The next three commands assign paths of operating system disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="7b9c8-111">Этот подход подходит только для учитаемости следующих команд:</span><span class="sxs-lookup"><span data-stu-id="7b9c8-111">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="7b9c8-112">Следующие три команды добавляют диск операционной системы и два диска данных к изображению, хранямуся в $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="7b9c8-112">The next three commands each adds an operating system disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="7b9c8-113">URI каждого диска хранится в $osDiskVhdUri, $dataDiskVhdUri 1 и $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="7b9c8-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>
<span data-ttu-id="7b9c8-114">Конечная команда создает изображение с именем ImageName01 в группе ресурсов ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="7b9c8-114">The final command creates an image named ImageName01 in resource group ResourceGroup01.</span></span>

## <span data-ttu-id="7b9c8-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7b9c8-115">PARAMETERS</span></span>

### <span data-ttu-id="7b9c8-116">-BlobUri</span><span class="sxs-lookup"><span data-stu-id="7b9c8-116">-BlobUri</span></span>
<span data-ttu-id="7b9c8-117">Указывает ссылку в качестве URI BLOB-части.</span><span class="sxs-lookup"><span data-stu-id="7b9c8-117">Specifies the link, as a URI, of the blob.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b9c8-118">-Кэшинг</span><span class="sxs-lookup"><span data-stu-id="7b9c8-118">-Caching</span></span>
<span data-ttu-id="7b9c8-119">Определяет режим кэшации диска.</span><span class="sxs-lookup"><span data-stu-id="7b9c8-119">Specifies the caching mode of the disk.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.CachingTypes]
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b9c8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b9c8-120">-DefaultProfile</span></span>
<span data-ttu-id="7b9c8-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7b9c8-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7b9c8-122">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="7b9c8-122">-DiskEncryptionSetId</span></span>
<span data-ttu-id="7b9c8-123">Определяет код ресурса для набора шифрования диска, управляемого клиентом.</span><span class="sxs-lookup"><span data-stu-id="7b9c8-123">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="7b9c8-124">Эта проверка может быть задана только для управляемого диска.</span><span class="sxs-lookup"><span data-stu-id="7b9c8-124">This can only be specified for managed disk.</span></span>

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

### <span data-ttu-id="7b9c8-125">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="7b9c8-125">-DiskSizeGB</span></span>
<span data-ttu-id="7b9c8-126">Определяет размер диска в гигабайтах (ГБ).</span><span class="sxs-lookup"><span data-stu-id="7b9c8-126">Specifies the size of the disk in Gigabytes (GB).</span></span>

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

### <span data-ttu-id="7b9c8-127">-Image</span><span class="sxs-lookup"><span data-stu-id="7b9c8-127">-Image</span></span>
<span data-ttu-id="7b9c8-128">Определяет объект локального изображения.</span><span class="sxs-lookup"><span data-stu-id="7b9c8-128">Specifies a local image object.</span></span>

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

### <span data-ttu-id="7b9c8-129">-Lun</span><span class="sxs-lookup"><span data-stu-id="7b9c8-129">-Lun</span></span>
<span data-ttu-id="7b9c8-130">Определяет логический номер единицы (LUN).</span><span class="sxs-lookup"><span data-stu-id="7b9c8-130">Specifies the logical unit number (LUN).</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b9c8-131">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="7b9c8-131">-ManagedDiskId</span></span>
<span data-ttu-id="7b9c8-132">Определяет ИД управляемого диска.</span><span class="sxs-lookup"><span data-stu-id="7b9c8-132">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="7b9c8-133">-SnapshotId</span><span class="sxs-lookup"><span data-stu-id="7b9c8-133">-SnapshotId</span></span>
<span data-ttu-id="7b9c8-134">Определяет ИД моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="7b9c8-134">Specifies the ID of a snapshot.</span></span>

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

### <span data-ttu-id="7b9c8-135">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="7b9c8-135">-StorageAccountType</span></span>
<span data-ttu-id="7b9c8-136">Тип учетной записи хранения диска изображения данных</span><span class="sxs-lookup"><span data-stu-id="7b9c8-136">The Storage Account type of the data image disk</span></span>

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

### <span data-ttu-id="7b9c8-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7b9c8-137">-Confirm</span></span>
<span data-ttu-id="7b9c8-138">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7b9c8-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b9c8-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b9c8-139">-WhatIf</span></span>
<span data-ttu-id="7b9c8-140">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7b9c8-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7b9c8-141">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="7b9c8-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b9c8-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b9c8-142">CommonParameters</span></span>
<span data-ttu-id="7b9c8-143">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b9c8-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b9c8-144">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7b9c8-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b9c8-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7b9c8-145">INPUTS</span></span>

### <span data-ttu-id="7b9c8-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span><span class="sxs-lookup"><span data-stu-id="7b9c8-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

### <span data-ttu-id="7b9c8-147">System.Int32</span><span class="sxs-lookup"><span data-stu-id="7b9c8-147">System.Int32</span></span>

### <span data-ttu-id="7b9c8-148">System.String</span><span class="sxs-lookup"><span data-stu-id="7b9c8-148">System.String</span></span>

### <span data-ttu-id="7b9c8-149">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="7b9c8-149">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="7b9c8-150">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7b9c8-150">OUTPUTS</span></span>

### <span data-ttu-id="7b9c8-151">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span><span class="sxs-lookup"><span data-stu-id="7b9c8-151">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="7b9c8-152">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7b9c8-152">NOTES</span></span>

## <span data-ttu-id="7b9c8-153">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7b9c8-153">RELATED LINKS</span></span>

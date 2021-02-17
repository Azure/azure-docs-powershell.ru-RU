---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azimageosdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzImageOsDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzImageOsDisk.md
ms.openlocfilehash: 45f3e8f76e6f8ff3a5684fbd8f9ebf42e7a8e252
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100238703"
---
# <span data-ttu-id="9bf0a-101">Set-AzImageOsDisk</span><span class="sxs-lookup"><span data-stu-id="9bf0a-101">Set-AzImageOsDisk</span></span>

## <span data-ttu-id="9bf0a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9bf0a-102">SYNOPSIS</span></span>
<span data-ttu-id="9bf0a-103">Задает свойства диска операционной системы для объекта изображения.</span><span class="sxs-lookup"><span data-stu-id="9bf0a-103">Sets the operating system disk properties on an image object.</span></span>

## <span data-ttu-id="9bf0a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9bf0a-104">SYNTAX</span></span>

```
Set-AzImageOsDisk [-Image] <PSImage> [[-OsType] <OperatingSystemTypes>]
 [[-OsState] <OperatingSystemStateTypes>] [[-BlobUri] <String>] [-Caching <CachingTypes>] [-DiskSizeGB <Int32>]
 [-StorageAccountType <String>] [-SnapshotId <String>] [-ManagedDiskId <String>]
 [-DiskEncryptionSetId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9bf0a-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9bf0a-105">DESCRIPTION</span></span>
<span data-ttu-id="9bf0a-106">**Cmdlet Set-AzImageOsDisk** задает свойства диска операционной системы для изображения объекта.</span><span class="sxs-lookup"><span data-stu-id="9bf0a-106">The **Set-AzImageOsDisk** cmdlet sets the operating system disk properties on an image object.</span></span>

## <span data-ttu-id="9bf0a-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9bf0a-107">EXAMPLES</span></span>

### <span data-ttu-id="9bf0a-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9bf0a-108">Example 1</span></span>
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

<span data-ttu-id="9bf0a-109">Первая команда создает объект изображения, а затем сохраняет его в переменной $imageConfig изображения.</span><span class="sxs-lookup"><span data-stu-id="9bf0a-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>
<span data-ttu-id="9bf0a-110">Следующие три команды назначают пути диска оси и два диска данных переменным $osDiskVhdUri, $dataDiskVhdUri 1 и $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="9bf0a-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="9bf0a-111">Этот подход подходит только для учитаемости следующих команд:</span><span class="sxs-lookup"><span data-stu-id="9bf0a-111">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="9bf0a-112">Следующие три команды добавляют диск оси и два диска данных к изображению, хранямуся в $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="9bf0a-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="9bf0a-113">URI каждого диска хранится в $osDiskVhdUri, $dataDiskVhdUri 1 и $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="9bf0a-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>
<span data-ttu-id="9bf0a-114">В конечная команда создается изображение с именем "ИмяСхема01" в группе ресурсов "Группа ресурсов01".</span><span class="sxs-lookup"><span data-stu-id="9bf0a-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="9bf0a-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9bf0a-115">PARAMETERS</span></span>

### <span data-ttu-id="9bf0a-116">-BlobUri</span><span class="sxs-lookup"><span data-stu-id="9bf0a-116">-BlobUri</span></span>
<span data-ttu-id="9bf0a-117">Определяет URI BLOB-адреса.</span><span class="sxs-lookup"><span data-stu-id="9bf0a-117">Specifies the Uri of the blob.</span></span>

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

### <span data-ttu-id="9bf0a-118">-Кэшинг</span><span class="sxs-lookup"><span data-stu-id="9bf0a-118">-Caching</span></span>
<span data-ttu-id="9bf0a-119">Определяет режим кэшации диска.</span><span class="sxs-lookup"><span data-stu-id="9bf0a-119">Specifies the caching mode of the disk.</span></span>

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

### <span data-ttu-id="9bf0a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bf0a-120">-DefaultProfile</span></span>
<span data-ttu-id="9bf0a-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9bf0a-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9bf0a-122">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="9bf0a-122">-DiskEncryptionSetId</span></span>
<span data-ttu-id="9bf0a-123">Определяет код ресурса для набора шифрования диска, управляемого клиентом.</span><span class="sxs-lookup"><span data-stu-id="9bf0a-123">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="9bf0a-124">Эта проверка может быть задана только для управляемого диска.</span><span class="sxs-lookup"><span data-stu-id="9bf0a-124">This can only be specified for managed disk.</span></span>

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

### <span data-ttu-id="9bf0a-125">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="9bf0a-125">-DiskSizeGB</span></span>
<span data-ttu-id="9bf0a-126">Определяет размер диска в ГБ.</span><span class="sxs-lookup"><span data-stu-id="9bf0a-126">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="9bf0a-127">-Image</span><span class="sxs-lookup"><span data-stu-id="9bf0a-127">-Image</span></span>
<span data-ttu-id="9bf0a-128">Определяет объект локального изображения.</span><span class="sxs-lookup"><span data-stu-id="9bf0a-128">Specifies a local image object.</span></span>

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

### <span data-ttu-id="9bf0a-129">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="9bf0a-129">-ManagedDiskId</span></span>
<span data-ttu-id="9bf0a-130">Определяет ИД управляемого диска.</span><span class="sxs-lookup"><span data-stu-id="9bf0a-130">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="9bf0a-131">-OsState</span><span class="sxs-lookup"><span data-stu-id="9bf0a-131">-OsState</span></span>
<span data-ttu-id="9bf0a-132">Определяет состояние ОС.</span><span class="sxs-lookup"><span data-stu-id="9bf0a-132">Specifies the OS state.</span></span>

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

### <span data-ttu-id="9bf0a-133">-OsType</span><span class="sxs-lookup"><span data-stu-id="9bf0a-133">-OsType</span></span>
<span data-ttu-id="9bf0a-134">Тип ОС.</span><span class="sxs-lookup"><span data-stu-id="9bf0a-134">Specifies the OS type.</span></span>

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

### <span data-ttu-id="9bf0a-135">-SnapshotId</span><span class="sxs-lookup"><span data-stu-id="9bf0a-135">-SnapshotId</span></span>
<span data-ttu-id="9bf0a-136">Определяет ИД моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="9bf0a-136">Specifies the ID of a snapshot.</span></span>

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

### <span data-ttu-id="9bf0a-137">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="9bf0a-137">-StorageAccountType</span></span>
<span data-ttu-id="9bf0a-138">Тип учетной записи хранения диска образа Ос</span><span class="sxs-lookup"><span data-stu-id="9bf0a-138">The Storage Account type of Os Image Disk</span></span>

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

### <span data-ttu-id="9bf0a-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9bf0a-139">-Confirm</span></span>
<span data-ttu-id="9bf0a-140">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9bf0a-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9bf0a-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9bf0a-141">-WhatIf</span></span>
<span data-ttu-id="9bf0a-142">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9bf0a-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9bf0a-143">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="9bf0a-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9bf0a-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bf0a-144">CommonParameters</span></span>
<span data-ttu-id="9bf0a-145">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9bf0a-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bf0a-146">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9bf0a-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bf0a-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9bf0a-147">INPUTS</span></span>

### <span data-ttu-id="9bf0a-148">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span><span class="sxs-lookup"><span data-stu-id="9bf0a-148">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

### <span data-ttu-id="9bf0a-149">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="9bf0a-149">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="9bf0a-150">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="9bf0a-150">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="9bf0a-151">System.String</span><span class="sxs-lookup"><span data-stu-id="9bf0a-151">System.String</span></span>

### <span data-ttu-id="9bf0a-152">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="9bf0a-152">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="9bf0a-153">System.Int32</span><span class="sxs-lookup"><span data-stu-id="9bf0a-153">System.Int32</span></span>

## <span data-ttu-id="9bf0a-154">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9bf0a-154">OUTPUTS</span></span>

### <span data-ttu-id="9bf0a-155">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span><span class="sxs-lookup"><span data-stu-id="9bf0a-155">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="9bf0a-156">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9bf0a-156">NOTES</span></span>

## <span data-ttu-id="9bf0a-157">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9bf0a-157">RELATED LINKS</span></span>

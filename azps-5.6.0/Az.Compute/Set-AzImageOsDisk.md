---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azimageosdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzImageOsDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzImageOsDisk.md
ms.openlocfilehash: 79415e5a39703e61843fc58a55ebc4cc5168ef0f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008051"
---
# <span data-ttu-id="757db-101">Set-AzImageOsDisk</span><span class="sxs-lookup"><span data-stu-id="757db-101">Set-AzImageOsDisk</span></span>

## <span data-ttu-id="757db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="757db-102">SYNOPSIS</span></span>
<span data-ttu-id="757db-103">Задает свойства диска операционной системы для объекта изображения.</span><span class="sxs-lookup"><span data-stu-id="757db-103">Sets the operating system disk properties on an image object.</span></span>

## <span data-ttu-id="757db-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="757db-104">SYNTAX</span></span>

```
Set-AzImageOsDisk [-Image] <PSImage> [[-OsType] <OperatingSystemTypes>]
 [[-OsState] <OperatingSystemStateTypes>] [[-BlobUri] <String>] [-Caching <CachingTypes>] [-DiskSizeGB <Int32>]
 [-StorageAccountType <String>] [-SnapshotId <String>] [-ManagedDiskId <String>]
 [-DiskEncryptionSetId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="757db-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="757db-105">DESCRIPTION</span></span>
<span data-ttu-id="757db-106">**Cmdlet Set-AzImageOsDisk** задает свойства диска операционной системы для изображения объекта.</span><span class="sxs-lookup"><span data-stu-id="757db-106">The **Set-AzImageOsDisk** cmdlet sets the operating system disk properties on an image object.</span></span>

## <span data-ttu-id="757db-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="757db-107">EXAMPLES</span></span>

### <span data-ttu-id="757db-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="757db-108">Example 1</span></span>
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

<span data-ttu-id="757db-109">Первая команда создает объект изображения, а затем сохраняет его в переменной $imageConfig изображения.</span><span class="sxs-lookup"><span data-stu-id="757db-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>
<span data-ttu-id="757db-110">Следующие три команды назначают пути диска оси и два диска данных переменным $osDiskVhdUri, $dataDiskVhdUri 1 и $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="757db-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="757db-111">Этот подход подходит только для учитаемости следующих команд:</span><span class="sxs-lookup"><span data-stu-id="757db-111">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="757db-112">Следующие три команды добавляют диск оси и два диска данных к изображению, хранямуся в $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="757db-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="757db-113">URI каждого диска хранится в $osDiskVhdUri, $dataDiskVhdUri 1 и $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="757db-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>
<span data-ttu-id="757db-114">Конечная команда создает изображение с именем "ИмяСхема01" в группе ресурсов "Группа ресурсов01".</span><span class="sxs-lookup"><span data-stu-id="757db-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="757db-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="757db-115">PARAMETERS</span></span>

### <span data-ttu-id="757db-116">-BlobUri</span><span class="sxs-lookup"><span data-stu-id="757db-116">-BlobUri</span></span>
<span data-ttu-id="757db-117">Определяет URI BLOB-адреса.</span><span class="sxs-lookup"><span data-stu-id="757db-117">Specifies the Uri of the blob.</span></span>

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

### <span data-ttu-id="757db-118">-Кэшинг</span><span class="sxs-lookup"><span data-stu-id="757db-118">-Caching</span></span>
<span data-ttu-id="757db-119">Определяет режим кэшации диска.</span><span class="sxs-lookup"><span data-stu-id="757db-119">Specifies the caching mode of the disk.</span></span>

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

### <span data-ttu-id="757db-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="757db-120">-DefaultProfile</span></span>
<span data-ttu-id="757db-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="757db-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="757db-122">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="757db-122">-DiskEncryptionSetId</span></span>
<span data-ttu-id="757db-123">Определяет код ресурса для набора шифрования диска, управляемого клиентом.</span><span class="sxs-lookup"><span data-stu-id="757db-123">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="757db-124">Эта проверка может быть задана только для управляемого диска.</span><span class="sxs-lookup"><span data-stu-id="757db-124">This can only be specified for managed disk.</span></span>

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

### <span data-ttu-id="757db-125">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="757db-125">-DiskSizeGB</span></span>
<span data-ttu-id="757db-126">Определяет размер диска в ГБ.</span><span class="sxs-lookup"><span data-stu-id="757db-126">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="757db-127">-Image</span><span class="sxs-lookup"><span data-stu-id="757db-127">-Image</span></span>
<span data-ttu-id="757db-128">Определяет объект локального изображения.</span><span class="sxs-lookup"><span data-stu-id="757db-128">Specifies a local image object.</span></span>

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

### <span data-ttu-id="757db-129">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="757db-129">-ManagedDiskId</span></span>
<span data-ttu-id="757db-130">Определяет ИД управляемого диска.</span><span class="sxs-lookup"><span data-stu-id="757db-130">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="757db-131">-OsState</span><span class="sxs-lookup"><span data-stu-id="757db-131">-OsState</span></span>
<span data-ttu-id="757db-132">Определяет состояние ОС.</span><span class="sxs-lookup"><span data-stu-id="757db-132">Specifies the OS state.</span></span>

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

### <span data-ttu-id="757db-133">-OsType</span><span class="sxs-lookup"><span data-stu-id="757db-133">-OsType</span></span>
<span data-ttu-id="757db-134">Тип ОС.</span><span class="sxs-lookup"><span data-stu-id="757db-134">Specifies the OS type.</span></span>

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

### <span data-ttu-id="757db-135">-SnapshotId</span><span class="sxs-lookup"><span data-stu-id="757db-135">-SnapshotId</span></span>
<span data-ttu-id="757db-136">Определяет ИД моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="757db-136">Specifies the ID of a snapshot.</span></span>

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

### <span data-ttu-id="757db-137">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="757db-137">-StorageAccountType</span></span>
<span data-ttu-id="757db-138">Тип учетной записи хранения образного диска Ос</span><span class="sxs-lookup"><span data-stu-id="757db-138">The Storage Account type of Os Image Disk</span></span>

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

### <span data-ttu-id="757db-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="757db-139">-Confirm</span></span>
<span data-ttu-id="757db-140">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="757db-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="757db-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="757db-141">-WhatIf</span></span>
<span data-ttu-id="757db-142">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="757db-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="757db-143">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="757db-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="757db-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="757db-144">CommonParameters</span></span>
<span data-ttu-id="757db-145">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="757db-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="757db-146">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="757db-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="757db-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="757db-147">INPUTS</span></span>

### <span data-ttu-id="757db-148">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span><span class="sxs-lookup"><span data-stu-id="757db-148">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

### <span data-ttu-id="757db-149">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="757db-149">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="757db-150">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="757db-150">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="757db-151">System.String</span><span class="sxs-lookup"><span data-stu-id="757db-151">System.String</span></span>

### <span data-ttu-id="757db-152">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="757db-152">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="757db-153">System.Int32</span><span class="sxs-lookup"><span data-stu-id="757db-153">System.Int32</span></span>

## <span data-ttu-id="757db-154">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="757db-154">OUTPUTS</span></span>

### <span data-ttu-id="757db-155">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span><span class="sxs-lookup"><span data-stu-id="757db-155">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="757db-156">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="757db-156">NOTES</span></span>

## <span data-ttu-id="757db-157">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="757db-157">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 230DAE05-C197-451F-A24C-F4A2DAE4AD04
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssstorageprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssStorageProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssStorageProfile.md
ms.openlocfilehash: 7bf5e6b765fee14ca9ba12a289d6445e063ff9df
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98509013"
---
# <span data-ttu-id="78d26-101">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="78d26-101">Set-AzVmssStorageProfile</span></span>

## <span data-ttu-id="78d26-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78d26-102">SYNOPSIS</span></span>
<span data-ttu-id="78d26-103">Задает свойства профиля хранилища для VMSS.</span><span class="sxs-lookup"><span data-stu-id="78d26-103">Sets the storage profile properties for the VMSS.</span></span>

## <span data-ttu-id="78d26-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="78d26-104">SYNTAX</span></span>

```
Set-AzVmssStorageProfile [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-ImageReferencePublisher] <String>] [[-ImageReferenceOffer] <String>] [[-ImageReferenceSku] <String>]
 [[-ImageReferenceVersion] <String>] [[-OsDiskName] <String>] [[-OsDiskCaching] <CachingTypes>]
 [[-OsDiskCreateOption] <String>] [[-OsDiskOsType] <OperatingSystemTypes>] [[-Image] <String>]
 [[-VhdContainer] <String[]>] [-ImageReferenceId <String>] [-OsDiskWriteAccelerator]
 [-DiffDiskSetting <String>] [-ManagedDisk <String>] [-DiskEncryptionSetId <String>]
 [-DataDisk <VirtualMachineScaleSetDataDisk[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="78d26-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="78d26-105">DESCRIPTION</span></span>
<span data-ttu-id="78d26-106">Для набора виртуальных машин (VMSS) свойства профиля хранилища задает **cmdlet Set-AzVmssStorageProfile.**</span><span class="sxs-lookup"><span data-stu-id="78d26-106">The **Set-AzVmssStorageProfile** cmdlet sets the storage profile properties for the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="78d26-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="78d26-107">EXAMPLES</span></span>

### <span data-ttu-id="78d26-108">Пример 1. Настройка свойств профиля хранилища для VMSS</span><span class="sxs-lookup"><span data-stu-id="78d26-108">Example 1: Set the storage profile properties for the VMSS</span></span>
```
PS C:\> Set-AzVmssStorageProfile -VirtualMachineScaleSet "ContosoVMSS" -Name "Test" -OsDiskCreateOption "FromImage" -OsDiskCaching "None" `
            -ImageReferenceOffer $ImgRef.Offer -ImageReferenceSku $ImgRef.Skus -ImageReferenceVersion $ImgRef.Version `
            -ImageReferencePublisher $ImgRef.PublisherName -VhdContainer $VhdContainer
```

<span data-ttu-id="78d26-109">Эта команда задает свойства профиля хранилища для VMSS с именем ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="78d26-109">This command sets the storage profile properties for the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="78d26-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="78d26-110">PARAMETERS</span></span>

### <span data-ttu-id="78d26-111">-DataDisk</span><span class="sxs-lookup"><span data-stu-id="78d26-111">-DataDisk</span></span>
<span data-ttu-id="78d26-112">Определяет объект диска данных.</span><span class="sxs-lookup"><span data-stu-id="78d26-112">Specifies the data disk object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetDataDisk[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78d26-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78d26-113">-DefaultProfile</span></span>
<span data-ttu-id="78d26-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="78d26-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="78d26-115">-DiffDiskSetting</span><span class="sxs-lookup"><span data-stu-id="78d26-115">-DiffDiskSetting</span></span>
<span data-ttu-id="78d26-116">Определяет различные параметры диска операционной системы.</span><span class="sxs-lookup"><span data-stu-id="78d26-116">Specifies the differencing disk settings for operating system disk.</span></span>

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

### <span data-ttu-id="78d26-117">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="78d26-117">-DiskEncryptionSetId</span></span>
<span data-ttu-id="78d26-118">Определяет код ресурса для набора шифрования диска, управляемого клиентом.</span><span class="sxs-lookup"><span data-stu-id="78d26-118">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="78d26-119">Эта проверка может быть задана только для управляемого диска.</span><span class="sxs-lookup"><span data-stu-id="78d26-119">This can only be specified for managed disk.</span></span>

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

### <span data-ttu-id="78d26-120">-Image</span><span class="sxs-lookup"><span data-stu-id="78d26-120">-Image</span></span>
<span data-ttu-id="78d26-121">Определяет URI BLOB-данных для изображения пользователя.</span><span class="sxs-lookup"><span data-stu-id="78d26-121">Specifies the blob URI for the user image.</span></span>
<span data-ttu-id="78d26-122">VMSS создает диск операционной системы в том же контейнере изображения пользователя.</span><span class="sxs-lookup"><span data-stu-id="78d26-122">VMSS creates an operating system disk in the same container of the user image.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78d26-123">-ImageReferenceId</span><span class="sxs-lookup"><span data-stu-id="78d26-123">-ImageReferenceId</span></span>
<span data-ttu-id="78d26-124">Определяет ИД ссылки на изображение.</span><span class="sxs-lookup"><span data-stu-id="78d26-124">Specifies the image reference ID.</span></span>

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

### <span data-ttu-id="78d26-125">-ImageReferenceOffer</span><span class="sxs-lookup"><span data-stu-id="78d26-125">-ImageReferenceOffer</span></span>
<span data-ttu-id="78d26-126">Тип изображения виртуальной машины (VMImage).</span><span class="sxs-lookup"><span data-stu-id="78d26-126">Specifies the type of virtual machine image (VMImage) offer.</span></span>
<span data-ttu-id="78d26-127">Чтобы получить предложение для изображения, воспользуйтесь Get-AzVMImageOffer- и рисунками.</span><span class="sxs-lookup"><span data-stu-id="78d26-127">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="78d26-128">-ImageReferencePublisher</span><span class="sxs-lookup"><span data-stu-id="78d26-128">-ImageReferencePublisher</span></span>
<span data-ttu-id="78d26-129">Указывает имя издателя VMImage.</span><span class="sxs-lookup"><span data-stu-id="78d26-129">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="78d26-130">Чтобы получить издателя, воспользуйтесь Get-AzVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="78d26-130">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78d26-131">-ImageReferenceSku</span><span class="sxs-lookup"><span data-stu-id="78d26-131">-ImageReferenceSku</span></span>
<span data-ttu-id="78d26-132">Указывает SKU VMImage.</span><span class="sxs-lookup"><span data-stu-id="78d26-132">Specifies the VMImage SKU.</span></span>
<span data-ttu-id="78d26-133">Чтобы получить skus, используйте Get-AzVMImageSku-код.</span><span class="sxs-lookup"><span data-stu-id="78d26-133">To obtain SKUs, use the Get-AzVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="78d26-134">-ImageReferenceVersion</span><span class="sxs-lookup"><span data-stu-id="78d26-134">-ImageReferenceVersion</span></span>
<span data-ttu-id="78d26-135">Определяет версию VMImage.</span><span class="sxs-lookup"><span data-stu-id="78d26-135">Specifies the version of the VMImage.</span></span>
<span data-ttu-id="78d26-136">Чтобы использовать последнюю версию, укажите последнюю версию, а не конкретную.</span><span class="sxs-lookup"><span data-stu-id="78d26-136">To use the latest version, specify a value of latest instead of a particular version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78d26-137">-ManagedDisk</span><span class="sxs-lookup"><span data-stu-id="78d26-137">-ManagedDisk</span></span>
<span data-ttu-id="78d26-138">Определяет управляемый диск.</span><span class="sxs-lookup"><span data-stu-id="78d26-138">Specifies the managed disk.</span></span>

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

### <span data-ttu-id="78d26-139">-OsDiskCaching</span><span class="sxs-lookup"><span data-stu-id="78d26-139">-OsDiskCaching</span></span>
<span data-ttu-id="78d26-140">Определяет режим кэшации диска операционной системы.</span><span class="sxs-lookup"><span data-stu-id="78d26-140">Specifies the caching mode of the operating system disk.</span></span> <span data-ttu-id="78d26-141">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="78d26-141">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="78d26-142">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="78d26-142">ReadOnly</span></span>
- <span data-ttu-id="78d26-143">Значением по умолчанию readWrite является ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="78d26-143">ReadWrite The default value is ReadWrite.</span></span>
<span data-ttu-id="78d26-144">Если изменить значение кэшинга, будет перезапущена виртуальная машину.</span><span class="sxs-lookup"><span data-stu-id="78d26-144">If you change the caching value, the cmdlet will restart the virtual machine.</span></span>
<span data-ttu-id="78d26-145">Этот параметр влияет на согласованность и производительность диска.</span><span class="sxs-lookup"><span data-stu-id="78d26-145">This setting affects the consistency and performance of the disk.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.CachingTypes]
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78d26-146">-OsDiskCreateOption</span><span class="sxs-lookup"><span data-stu-id="78d26-146">-OsDiskCreateOption</span></span>
<span data-ttu-id="78d26-147">Определяет, как этот cmdlet создает виртуальные машины VMSS.</span><span class="sxs-lookup"><span data-stu-id="78d26-147">Specifies how this cmdlet creates the VMSS virtual machines.</span></span>
<span data-ttu-id="78d26-148">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="78d26-148">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="78d26-149">Attach : Это значение используется при создании виртуальной машины VMSS на специализированном диске.</span><span class="sxs-lookup"><span data-stu-id="78d26-149">Attach : This value is used when you are using a specialized disk to create the VMSS virtual machine.</span></span> 
- <span data-ttu-id="78d26-150">FromImage: это значение используется при использовании изображения для создания виртуальной машины VMSS.</span><span class="sxs-lookup"><span data-stu-id="78d26-150">FromImage : This value is used when you are using an image to create the VMSS virtual machine.</span></span>
<span data-ttu-id="78d26-151">Если вы используете изображение платформы, вы также будете использовать *параметр imageReference.*</span><span class="sxs-lookup"><span data-stu-id="78d26-151">If you are using a platform image, you will also use the *imageReference* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78d26-152">-OsDiskName</span><span class="sxs-lookup"><span data-stu-id="78d26-152">-OsDiskName</span></span>
<span data-ttu-id="78d26-153">Указывает имя диска операционной системы.</span><span class="sxs-lookup"><span data-stu-id="78d26-153">Specifies the name of the operating system disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78d26-154">-OsDiskOsType</span><span class="sxs-lookup"><span data-stu-id="78d26-154">-OsDiskOsType</span></span>
<span data-ttu-id="78d26-155">Определяет тип операционной системы на диске.</span><span class="sxs-lookup"><span data-stu-id="78d26-155">Specifies the type of operating system on the disk.</span></span>
<span data-ttu-id="78d26-156">Это необходимо только для сценариев использования изображений пользователей, а не для изображений платформы.</span><span class="sxs-lookup"><span data-stu-id="78d26-156">This is only needed for user image scenarios and not for a platform image.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes]
Parameter Sets: (All)
Aliases:
Accepted values: Windows, Linux

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78d26-157">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="78d26-157">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="78d26-158">Указывает, следует ли включить или отключить WriteAccelerator на диске ОС.</span><span class="sxs-lookup"><span data-stu-id="78d26-158">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78d26-159">-VhdContainer</span><span class="sxs-lookup"><span data-stu-id="78d26-159">-VhdContainer</span></span>
<span data-ttu-id="78d26-160">Определяет URL-адреса контейнеров, которые используются для хранения дисков операционной системы для VMSS.</span><span class="sxs-lookup"><span data-stu-id="78d26-160">Specifies the container URLs that are used to store operating system disks for the VMSS.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78d26-161">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="78d26-161">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="78d26-162">Указывает объект VMSS.</span><span class="sxs-lookup"><span data-stu-id="78d26-162">Specifies the VMSS object.</span></span>
<span data-ttu-id="78d26-163">Чтобы получить объект, используйте New-AzVmssConfig объекта.</span><span class="sxs-lookup"><span data-stu-id="78d26-163">To obtain the object, use the New-AzVmssConfig object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="78d26-164">-Confirm</span><span class="sxs-lookup"><span data-stu-id="78d26-164">-Confirm</span></span>
<span data-ttu-id="78d26-165">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="78d26-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78d26-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78d26-166">-WhatIf</span></span>
<span data-ttu-id="78d26-167">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="78d26-167">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="78d26-168">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="78d26-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78d26-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78d26-169">CommonParameters</span></span>
<span data-ttu-id="78d26-170">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78d26-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78d26-171">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="78d26-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78d26-172">INPUTS</span><span class="sxs-lookup"><span data-stu-id="78d26-172">INPUTS</span></span>

### <span data-ttu-id="78d26-173">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMa modelseScaleSet</span><span class="sxs-lookup"><span data-stu-id="78d26-173">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="78d26-174">System.String</span><span class="sxs-lookup"><span data-stu-id="78d26-174">System.String</span></span>

### <span data-ttu-id="78d26-175">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="78d26-175">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="78d26-176">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="78d26-176">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="78d26-177">System.String[]</span><span class="sxs-lookup"><span data-stu-id="78d26-177">System.String[]</span></span>

### <span data-ttu-id="78d26-178">Microsoft.Azure.Management.Compute.Models.VirtualMa modelseScaleSetDataDisk[]</span><span class="sxs-lookup"><span data-stu-id="78d26-178">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetDataDisk[]</span></span>

## <span data-ttu-id="78d26-179">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="78d26-179">OUTPUTS</span></span>

### <span data-ttu-id="78d26-180">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMa modelseScaleSet</span><span class="sxs-lookup"><span data-stu-id="78d26-180">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="78d26-181">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="78d26-181">NOTES</span></span>

## <span data-ttu-id="78d26-182">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="78d26-182">RELATED LINKS</span></span>

[<span data-ttu-id="78d26-183">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="78d26-183">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="78d26-184">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="78d26-184">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="78d26-185">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="78d26-185">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="78d26-186">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="78d26-186">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)



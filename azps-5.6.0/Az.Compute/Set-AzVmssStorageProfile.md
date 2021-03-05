---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 230DAE05-C197-451F-A24C-F4A2DAE4AD04
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmssstorageprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssStorageProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssStorageProfile.md
ms.openlocfilehash: ec233765f401348895275291ddad0571d1ddfc85
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101977480"
---
# <span data-ttu-id="91e75-101">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="91e75-101">Set-AzVmssStorageProfile</span></span>

## <span data-ttu-id="91e75-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91e75-102">SYNOPSIS</span></span>
<span data-ttu-id="91e75-103">Задает свойства профиля хранилища для VMSS.</span><span class="sxs-lookup"><span data-stu-id="91e75-103">Sets the storage profile properties for the VMSS.</span></span>

## <span data-ttu-id="91e75-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="91e75-104">SYNTAX</span></span>

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

## <span data-ttu-id="91e75-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="91e75-105">DESCRIPTION</span></span>
<span data-ttu-id="91e75-106">Для набора виртуальных машин (VMSS) свойства профиля хранилища задает **cmdlet Set-AzVmssStorageProfile.**</span><span class="sxs-lookup"><span data-stu-id="91e75-106">The **Set-AzVmssStorageProfile** cmdlet sets the storage profile properties for the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="91e75-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="91e75-107">EXAMPLES</span></span>

### <span data-ttu-id="91e75-108">Пример 1. Настройка свойств профиля хранилища для VMSS</span><span class="sxs-lookup"><span data-stu-id="91e75-108">Example 1: Set the storage profile properties for the VMSS</span></span>
```
PS C:\> Set-AzVmssStorageProfile -VirtualMachineScaleSet "ContosoVMSS" -Name "Test" -OsDiskCreateOption "FromImage" -OsDiskCaching "None" `
            -ImageReferenceOffer $ImgRef.Offer -ImageReferenceSku $ImgRef.Skus -ImageReferenceVersion $ImgRef.Version `
            -ImageReferencePublisher $ImgRef.PublisherName -VhdContainer $VhdContainer
```

<span data-ttu-id="91e75-109">Эта команда задает свойства профиля хранилища для VMSS с именем ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="91e75-109">This command sets the storage profile properties for the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="91e75-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="91e75-110">PARAMETERS</span></span>

### <span data-ttu-id="91e75-111">-DataDisk</span><span class="sxs-lookup"><span data-stu-id="91e75-111">-DataDisk</span></span>
<span data-ttu-id="91e75-112">Определяет объект диска данных.</span><span class="sxs-lookup"><span data-stu-id="91e75-112">Specifies the data disk object.</span></span>

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

### <span data-ttu-id="91e75-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91e75-113">-DefaultProfile</span></span>
<span data-ttu-id="91e75-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="91e75-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="91e75-115">-DiffDiskSetting</span><span class="sxs-lookup"><span data-stu-id="91e75-115">-DiffDiskSetting</span></span>
<span data-ttu-id="91e75-116">Определяет другие параметры диска операционной системы.</span><span class="sxs-lookup"><span data-stu-id="91e75-116">Specifies the differencing disk settings for operating system disk.</span></span>

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

### <span data-ttu-id="91e75-117">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="91e75-117">-DiskEncryptionSetId</span></span>
<span data-ttu-id="91e75-118">Определяет код ресурса для набора шифрования диска, управляемого клиентом.</span><span class="sxs-lookup"><span data-stu-id="91e75-118">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="91e75-119">Эта проверка может быть задана только для управляемого диска.</span><span class="sxs-lookup"><span data-stu-id="91e75-119">This can only be specified for managed disk.</span></span>

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

### <span data-ttu-id="91e75-120">-Image</span><span class="sxs-lookup"><span data-stu-id="91e75-120">-Image</span></span>
<span data-ttu-id="91e75-121">Определяет URI BLOB-данных для изображения пользователя.</span><span class="sxs-lookup"><span data-stu-id="91e75-121">Specifies the blob URI for the user image.</span></span>
<span data-ttu-id="91e75-122">VMSS создает диск операционной системы в том же контейнере изображения пользователя.</span><span class="sxs-lookup"><span data-stu-id="91e75-122">VMSS creates an operating system disk in the same container of the user image.</span></span>

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

### <span data-ttu-id="91e75-123">-ImageReferenceId</span><span class="sxs-lookup"><span data-stu-id="91e75-123">-ImageReferenceId</span></span>
<span data-ttu-id="91e75-124">Определяет ИД ссылки на изображение.</span><span class="sxs-lookup"><span data-stu-id="91e75-124">Specifies the image reference ID.</span></span>

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

### <span data-ttu-id="91e75-125">-ImageReferenceOffer</span><span class="sxs-lookup"><span data-stu-id="91e75-125">-ImageReferenceOffer</span></span>
<span data-ttu-id="91e75-126">Тип изображения виртуальной машины (VMImage).</span><span class="sxs-lookup"><span data-stu-id="91e75-126">Specifies the type of virtual machine image (VMImage) offer.</span></span>
<span data-ttu-id="91e75-127">Чтобы получить предложение для изображения, воспользуйтесь Get-AzVMImageOffer- и рисунками.</span><span class="sxs-lookup"><span data-stu-id="91e75-127">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="91e75-128">-ImageReferencePublisher</span><span class="sxs-lookup"><span data-stu-id="91e75-128">-ImageReferencePublisher</span></span>
<span data-ttu-id="91e75-129">Указывает имя издателя VMImage.</span><span class="sxs-lookup"><span data-stu-id="91e75-129">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="91e75-130">Чтобы получить издателя, воспользуйтесь Get-AzVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="91e75-130">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="91e75-131">-ImageReferenceSku</span><span class="sxs-lookup"><span data-stu-id="91e75-131">-ImageReferenceSku</span></span>
<span data-ttu-id="91e75-132">Указывает SKU VMImage.</span><span class="sxs-lookup"><span data-stu-id="91e75-132">Specifies the VMImage SKU.</span></span>
<span data-ttu-id="91e75-133">Чтобы получить skus, используйте Get-AzVMImageSku-код.</span><span class="sxs-lookup"><span data-stu-id="91e75-133">To obtain SKUs, use the Get-AzVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="91e75-134">-ImageReferenceVersion</span><span class="sxs-lookup"><span data-stu-id="91e75-134">-ImageReferenceVersion</span></span>
<span data-ttu-id="91e75-135">Определяет версию VMImage.</span><span class="sxs-lookup"><span data-stu-id="91e75-135">Specifies the version of the VMImage.</span></span>
<span data-ttu-id="91e75-136">Чтобы использовать последнюю версию, укажите последнюю версию, а не конкретную.</span><span class="sxs-lookup"><span data-stu-id="91e75-136">To use the latest version, specify a value of latest instead of a particular version.</span></span>

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

### <span data-ttu-id="91e75-137">-ManagedDisk</span><span class="sxs-lookup"><span data-stu-id="91e75-137">-ManagedDisk</span></span>
<span data-ttu-id="91e75-138">Определяет управляемый диск.</span><span class="sxs-lookup"><span data-stu-id="91e75-138">Specifies the managed disk.</span></span>

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

### <span data-ttu-id="91e75-139">-OsDiskCaching</span><span class="sxs-lookup"><span data-stu-id="91e75-139">-OsDiskCaching</span></span>
<span data-ttu-id="91e75-140">Определяет режим кэшации диска операционной системы.</span><span class="sxs-lookup"><span data-stu-id="91e75-140">Specifies the caching mode of the operating system disk.</span></span> <span data-ttu-id="91e75-141">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="91e75-141">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="91e75-142">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="91e75-142">ReadOnly</span></span>
- <span data-ttu-id="91e75-143">Значением по умолчанию readWrite является ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="91e75-143">ReadWrite The default value is ReadWrite.</span></span>
<span data-ttu-id="91e75-144">Если изменить значение кэшинга, будет перезапущена виртуальная машина.</span><span class="sxs-lookup"><span data-stu-id="91e75-144">If you change the caching value, the cmdlet will restart the virtual machine.</span></span>
<span data-ttu-id="91e75-145">Этот параметр влияет на согласованность и производительность диска.</span><span class="sxs-lookup"><span data-stu-id="91e75-145">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="91e75-146">-OsDiskCreateOption</span><span class="sxs-lookup"><span data-stu-id="91e75-146">-OsDiskCreateOption</span></span>
<span data-ttu-id="91e75-147">Определяет, как этот cmdlet создает виртуальные машины VMSS.</span><span class="sxs-lookup"><span data-stu-id="91e75-147">Specifies how this cmdlet creates the VMSS virtual machines.</span></span>
<span data-ttu-id="91e75-148">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="91e75-148">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="91e75-149">Attach : Это значение используется при создании виртуальной машины VMSS на специализированном диске.</span><span class="sxs-lookup"><span data-stu-id="91e75-149">Attach : This value is used when you are using a specialized disk to create the VMSS virtual machine.</span></span> 
- <span data-ttu-id="91e75-150">FromImage: это значение используется при использовании изображения для создания виртуальной машины VMSS.</span><span class="sxs-lookup"><span data-stu-id="91e75-150">FromImage : This value is used when you are using an image to create the VMSS virtual machine.</span></span>
<span data-ttu-id="91e75-151">Если вы используете изображение платформы, вы также будете использовать *параметр imageReference.*</span><span class="sxs-lookup"><span data-stu-id="91e75-151">If you are using a platform image, you will also use the *imageReference* parameter.</span></span>

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

### <span data-ttu-id="91e75-152">-OsDiskName</span><span class="sxs-lookup"><span data-stu-id="91e75-152">-OsDiskName</span></span>
<span data-ttu-id="91e75-153">Указывает имя диска операционной системы.</span><span class="sxs-lookup"><span data-stu-id="91e75-153">Specifies the name of the operating system disk.</span></span>

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

### <span data-ttu-id="91e75-154">-OsDiskOsType</span><span class="sxs-lookup"><span data-stu-id="91e75-154">-OsDiskOsType</span></span>
<span data-ttu-id="91e75-155">Определяет тип операционной системы на диске.</span><span class="sxs-lookup"><span data-stu-id="91e75-155">Specifies the type of operating system on the disk.</span></span>
<span data-ttu-id="91e75-156">Это необходимо только для сценариев использования изображений пользователей, а не для изображений платформы.</span><span class="sxs-lookup"><span data-stu-id="91e75-156">This is only needed for user image scenarios and not for a platform image.</span></span>

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

### <span data-ttu-id="91e75-157">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="91e75-157">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="91e75-158">Указывает, следует ли включить или отключить WriteAccelerator на диске ОС.</span><span class="sxs-lookup"><span data-stu-id="91e75-158">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="91e75-159">-VhdContainer</span><span class="sxs-lookup"><span data-stu-id="91e75-159">-VhdContainer</span></span>
<span data-ttu-id="91e75-160">Определяет URL-адреса контейнеров, которые используются для хранения дисков операционной системы для VMSS.</span><span class="sxs-lookup"><span data-stu-id="91e75-160">Specifies the container URLs that are used to store operating system disks for the VMSS.</span></span>

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

### <span data-ttu-id="91e75-161">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="91e75-161">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="91e75-162">Указывает объект VMSS.</span><span class="sxs-lookup"><span data-stu-id="91e75-162">Specifies the VMSS object.</span></span>
<span data-ttu-id="91e75-163">Чтобы получить объект, используйте New-AzVmssConfig объекта.</span><span class="sxs-lookup"><span data-stu-id="91e75-163">To obtain the object, use the New-AzVmssConfig object.</span></span>

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

### <span data-ttu-id="91e75-164">-Confirm</span><span class="sxs-lookup"><span data-stu-id="91e75-164">-Confirm</span></span>
<span data-ttu-id="91e75-165">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="91e75-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91e75-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91e75-166">-WhatIf</span></span>
<span data-ttu-id="91e75-167">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="91e75-167">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="91e75-168">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="91e75-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91e75-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91e75-169">CommonParameters</span></span>
<span data-ttu-id="91e75-170">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91e75-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91e75-171">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="91e75-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91e75-172">INPUTS</span><span class="sxs-lookup"><span data-stu-id="91e75-172">INPUTS</span></span>

### <span data-ttu-id="91e75-173">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMa modelseScaleSet</span><span class="sxs-lookup"><span data-stu-id="91e75-173">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="91e75-174">System.String</span><span class="sxs-lookup"><span data-stu-id="91e75-174">System.String</span></span>

### <span data-ttu-id="91e75-175">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="91e75-175">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="91e75-176">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="91e75-176">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="91e75-177">System.String[]</span><span class="sxs-lookup"><span data-stu-id="91e75-177">System.String[]</span></span>

### <span data-ttu-id="91e75-178">Microsoft.Azure.Management.Compute.Models.VirtualMa modelseScaleSetDataDisk[]</span><span class="sxs-lookup"><span data-stu-id="91e75-178">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetDataDisk[]</span></span>

## <span data-ttu-id="91e75-179">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="91e75-179">OUTPUTS</span></span>

### <span data-ttu-id="91e75-180">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMa modelseScaleSet</span><span class="sxs-lookup"><span data-stu-id="91e75-180">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="91e75-181">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="91e75-181">NOTES</span></span>

## <span data-ttu-id="91e75-182">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="91e75-182">RELATED LINKS</span></span>

[<span data-ttu-id="91e75-183">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="91e75-183">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="91e75-184">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="91e75-184">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="91e75-185">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="91e75-185">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="91e75-186">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="91e75-186">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)



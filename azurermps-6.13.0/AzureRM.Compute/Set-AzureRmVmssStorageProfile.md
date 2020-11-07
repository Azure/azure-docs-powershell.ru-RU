---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 230DAE05-C197-451F-A24C-F4A2DAE4AD04
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmssstorageprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVmssStorageProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVmssStorageProfile.md
ms.openlocfilehash: dc2f8633b303d15f3fe53bfc0be7eda3420e611f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733888"
---
# <span data-ttu-id="01e72-101">Set-AzureRmVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="01e72-101">Set-AzureRmVmssStorageProfile</span></span>

## <span data-ttu-id="01e72-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="01e72-102">SYNOPSIS</span></span>
<span data-ttu-id="01e72-103">Задает свойства профиля хранилища для VMSS.</span><span class="sxs-lookup"><span data-stu-id="01e72-103">Sets the storage profile properties for the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="01e72-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="01e72-104">SYNTAX</span></span>

```
Set-AzureRmVmssStorageProfile [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-ImageReferencePublisher] <String>] [[-ImageReferenceOffer] <String>] [[-ImageReferenceSku] <String>]
 [[-ImageReferenceVersion] <String>] [[-OsDiskName] <String>] [[-OsDiskCaching] <CachingTypes>]
 [[-OsDiskCreateOption] <String>] [[-OsDiskOsType] <OperatingSystemTypes>] [[-Image] <String>]
 [[-VhdContainer] <String[]>] [-ImageReferenceId <String>] [-OsDiskWriteAccelerator]
 [-DiffDiskSetting <String>] [-ManagedDisk <String>] [-DataDisk <VirtualMachineScaleSetDataDisk[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01e72-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="01e72-105">DESCRIPTION</span></span>
<span data-ttu-id="01e72-106">Командлет **Set-AzureRmVmssStorageProfile** задает свойства профиля хранения для набора масштабов виртуальных машин (VMSS).</span><span class="sxs-lookup"><span data-stu-id="01e72-106">The **Set-AzureRmVmssStorageProfile** cmdlet sets the storage profile properties for the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="01e72-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="01e72-107">EXAMPLES</span></span>

### <span data-ttu-id="01e72-108">Пример 1: Настройка свойств профиля хранения для VMSS</span><span class="sxs-lookup"><span data-stu-id="01e72-108">Example 1: Set the storage profile properties for the VMSS</span></span>
```
PS C:\> Set-AzureRmVmssStorageProfile -VirtualMachineScaleSet "ContosoVMSS" -Name "Test" -OsDiskCreateOption "FromImage" -OsDiskCaching "None" `
            -ImageReferenceOffer $ImgRef.Offer -ImageReferenceSku $ImgRef.Skus -ImageReferenceVersion $ImgRef.Version `
            -ImageReferencePublisher $ImgRef.PublisherName -VhdContainer $VhdContainer
```

<span data-ttu-id="01e72-109">Эта команда задает свойства профиля хранения для VMSS с именем ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="01e72-109">This command sets the storage profile properties for the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="01e72-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="01e72-110">PARAMETERS</span></span>

### <span data-ttu-id="01e72-111">-Диск</span><span class="sxs-lookup"><span data-stu-id="01e72-111">-DataDisk</span></span>
<span data-ttu-id="01e72-112">Указывает объект диска данных.</span><span class="sxs-lookup"><span data-stu-id="01e72-112">Specifies the data disk object.</span></span>

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

### <span data-ttu-id="01e72-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01e72-113">-DefaultProfile</span></span>
<span data-ttu-id="01e72-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="01e72-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01e72-115">-DiffDiskSetting</span><span class="sxs-lookup"><span data-stu-id="01e72-115">-DiffDiskSetting</span></span>
<span data-ttu-id="01e72-116">Задает параметры разностного диска для диска операционной системы.</span><span class="sxs-lookup"><span data-stu-id="01e72-116">Specifies the differencing disk settings for operating system disk.</span></span>

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

### <span data-ttu-id="01e72-117">-Image</span><span class="sxs-lookup"><span data-stu-id="01e72-117">-Image</span></span>
<span data-ttu-id="01e72-118">Указывает URI большого двоичного объекта для пользовательского изображения.</span><span class="sxs-lookup"><span data-stu-id="01e72-118">Specifies the blob URI for the user image.</span></span>
<span data-ttu-id="01e72-119">VMSS создает диск операционной системы в том же контейнере пользовательского образа.</span><span class="sxs-lookup"><span data-stu-id="01e72-119">VMSS creates an operating system disk in the same container of the user image.</span></span>

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

### <span data-ttu-id="01e72-120">-ImageReferenceId</span><span class="sxs-lookup"><span data-stu-id="01e72-120">-ImageReferenceId</span></span>
<span data-ttu-id="01e72-121">Указывает идентификатор ссылки на изображение.</span><span class="sxs-lookup"><span data-stu-id="01e72-121">Specifies the image reference ID.</span></span>

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

### <span data-ttu-id="01e72-122">-ImageReferenceOffer</span><span class="sxs-lookup"><span data-stu-id="01e72-122">-ImageReferenceOffer</span></span>
<span data-ttu-id="01e72-123">Указывает тип предложения для образа виртуальной машины (VMImage).</span><span class="sxs-lookup"><span data-stu-id="01e72-123">Specifies the type of virtual machine image (VMImage) offer.</span></span>
<span data-ttu-id="01e72-124">Чтобы получить предложение с изображением, используйте командлет Get-AzureRmVMImageOffer.</span><span class="sxs-lookup"><span data-stu-id="01e72-124">To obtain an image offer, use the Get-AzureRmVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="01e72-125">-ImageReferencePublisher</span><span class="sxs-lookup"><span data-stu-id="01e72-125">-ImageReferencePublisher</span></span>
<span data-ttu-id="01e72-126">Указывает имя издателя VMImage.</span><span class="sxs-lookup"><span data-stu-id="01e72-126">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="01e72-127">Чтобы получить издатель, используйте командлет Get-AzureRmVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="01e72-127">To obtain a publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="01e72-128">-ImageReferenceSku</span><span class="sxs-lookup"><span data-stu-id="01e72-128">-ImageReferenceSku</span></span>
<span data-ttu-id="01e72-129">Указывает SKU VMImage.</span><span class="sxs-lookup"><span data-stu-id="01e72-129">Specifies the VMImage SKU.</span></span>
<span data-ttu-id="01e72-130">Чтобы получить SKU, используйте командлет Get-AzureRmVMImageSku.</span><span class="sxs-lookup"><span data-stu-id="01e72-130">To obtain SKUs, use the Get-AzureRmVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="01e72-131">-ImageReferenceVersion</span><span class="sxs-lookup"><span data-stu-id="01e72-131">-ImageReferenceVersion</span></span>
<span data-ttu-id="01e72-132">Указывает версию VMImage.</span><span class="sxs-lookup"><span data-stu-id="01e72-132">Specifies the version of the VMImage.</span></span>
<span data-ttu-id="01e72-133">Чтобы использовать последнюю версию, укажите значение, которое не определено в последней версии.</span><span class="sxs-lookup"><span data-stu-id="01e72-133">To use the latest version, specify a value of latest instead of a particular version.</span></span>

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

### <span data-ttu-id="01e72-134">-ManagedDisk</span><span class="sxs-lookup"><span data-stu-id="01e72-134">-ManagedDisk</span></span>
<span data-ttu-id="01e72-135">Задает управляемый диск.</span><span class="sxs-lookup"><span data-stu-id="01e72-135">Specifies the managed disk.</span></span>

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

### <span data-ttu-id="01e72-136">-OsDiskCaching</span><span class="sxs-lookup"><span data-stu-id="01e72-136">-OsDiskCaching</span></span>
<span data-ttu-id="01e72-137">Задает режим кэширования диска операционной системы.</span><span class="sxs-lookup"><span data-stu-id="01e72-137">Specifies the caching mode of the operating system disk.</span></span> <span data-ttu-id="01e72-138">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="01e72-138">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="01e72-139">Чтения</span><span class="sxs-lookup"><span data-stu-id="01e72-139">ReadOnly</span></span>
- <span data-ttu-id="01e72-140">ReadWrite по умолчанию используется значение ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="01e72-140">ReadWrite The default value is ReadWrite.</span></span>
<span data-ttu-id="01e72-141">Если вы измените значение кэширования, командлет перезагрузит виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="01e72-141">If you change the caching value, the cmdlet will restart the virtual machine.</span></span>
<span data-ttu-id="01e72-142">Этот параметр влияет на согласованность и производительность диска.</span><span class="sxs-lookup"><span data-stu-id="01e72-142">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="01e72-143">-OsDiskCreateOption</span><span class="sxs-lookup"><span data-stu-id="01e72-143">-OsDiskCreateOption</span></span>
<span data-ttu-id="01e72-144">Указывает, как этот командлет создает виртуальные машины VMSS.</span><span class="sxs-lookup"><span data-stu-id="01e72-144">Specifies how this cmdlet creates the VMSS virtual machines.</span></span>
<span data-ttu-id="01e72-145">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="01e72-145">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="01e72-146">Прикрепить: это значение используется при использовании специализированного диска для создания виртуальной машины VMSS.</span><span class="sxs-lookup"><span data-stu-id="01e72-146">Attach : This value is used when you are using a specialized disk to create the VMSS virtual machine.</span></span> 
- <span data-ttu-id="01e72-147">FromImage: это значение используется при использовании изображения для создания виртуальной машины VMSS.</span><span class="sxs-lookup"><span data-stu-id="01e72-147">FromImage : This value is used when you are using an image to create the VMSS virtual machine.</span></span>
<span data-ttu-id="01e72-148">Если вы используете образ платформы, вы также будете использовать параметр *imageReference* .</span><span class="sxs-lookup"><span data-stu-id="01e72-148">If you are using a platform image, you will also use the *imageReference* parameter.</span></span>

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

### <span data-ttu-id="01e72-149">-OsDiskName</span><span class="sxs-lookup"><span data-stu-id="01e72-149">-OsDiskName</span></span>
<span data-ttu-id="01e72-150">Указывает имя диска операционной системы.</span><span class="sxs-lookup"><span data-stu-id="01e72-150">Specifies the name of the operating system disk.</span></span>

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

### <span data-ttu-id="01e72-151">-OsDiskOsType</span><span class="sxs-lookup"><span data-stu-id="01e72-151">-OsDiskOsType</span></span>
<span data-ttu-id="01e72-152">Указывает тип операционной системы на диске.</span><span class="sxs-lookup"><span data-stu-id="01e72-152">Specifies the type of operating system on the disk.</span></span>
<span data-ttu-id="01e72-153">Это необходимо только для сценариев пользовательского изображения, а не для образа платформы.</span><span class="sxs-lookup"><span data-stu-id="01e72-153">This is only needed for user image scenarios and not for a platform image.</span></span>

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

### <span data-ttu-id="01e72-154">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="01e72-154">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="01e72-155">Указывает, следует ли включить или отключить WriteAccelerator на диске операционной системы.</span><span class="sxs-lookup"><span data-stu-id="01e72-155">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="01e72-156">-VhdContainer</span><span class="sxs-lookup"><span data-stu-id="01e72-156">-VhdContainer</span></span>
<span data-ttu-id="01e72-157">Указывает URL-адреса контейнеров, которые используются для хранения дисков операционной системы для VMSS.</span><span class="sxs-lookup"><span data-stu-id="01e72-157">Specifies the container URLs that are used to store operating system disks for the VMSS.</span></span>

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

### <span data-ttu-id="01e72-158">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="01e72-158">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="01e72-159">Указывает объект VMSS.</span><span class="sxs-lookup"><span data-stu-id="01e72-159">Specifies the VMSS object.</span></span>
<span data-ttu-id="01e72-160">Чтобы получить объект, используйте объект New-AzureRmVmssConfig.</span><span class="sxs-lookup"><span data-stu-id="01e72-160">To obtain the object, use the New-AzureRmVmssConfig object.</span></span>

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

### <span data-ttu-id="01e72-161">-Confirm</span><span class="sxs-lookup"><span data-stu-id="01e72-161">-Confirm</span></span>
<span data-ttu-id="01e72-162">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="01e72-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01e72-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01e72-163">-WhatIf</span></span>
<span data-ttu-id="01e72-164">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="01e72-164">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="01e72-165">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="01e72-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01e72-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01e72-166">CommonParameters</span></span>
<span data-ttu-id="01e72-167">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="01e72-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01e72-168">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01e72-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01e72-169">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="01e72-169">INPUTS</span></span>

### <span data-ttu-id="01e72-170">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="01e72-170">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="01e72-171">System. String</span><span class="sxs-lookup"><span data-stu-id="01e72-171">System.String</span></span>

### <span data-ttu-id="01e72-172">System. Nullable "1 [[Microsoft. Azure. Management. COMPUTE. Model. CachingTypes, Microsoft. Azure. Management. COMPUTE, Version = 21.0.0.0, культура =" нейтрально ", PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="01e72-172">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=21.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="01e72-173">System. Nullable "1 [[Microsoft. Azure. Management. COMPUTE. Model. OperatingSystemTypes, Microsoft. Azure. Management. COMPUTE, Version = 21.0.0.0, культура =" нейтрально ", PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="01e72-173">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=21.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="01e72-174">System. String []</span><span class="sxs-lookup"><span data-stu-id="01e72-174">System.String[]</span></span>

### <span data-ttu-id="01e72-175">Microsoft. Azure. Management. COMPUTE. Models. VirtualMachineScaleSetDataDisk []</span><span class="sxs-lookup"><span data-stu-id="01e72-175">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetDataDisk[]</span></span>

## <span data-ttu-id="01e72-176">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="01e72-176">OUTPUTS</span></span>

### <span data-ttu-id="01e72-177">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="01e72-177">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="01e72-178">Пуск</span><span class="sxs-lookup"><span data-stu-id="01e72-178">NOTES</span></span>

## <span data-ttu-id="01e72-179">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="01e72-179">RELATED LINKS</span></span>

[<span data-ttu-id="01e72-180">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="01e72-180">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="01e72-181">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="01e72-181">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="01e72-182">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="01e72-182">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="01e72-183">New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="01e72-183">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)



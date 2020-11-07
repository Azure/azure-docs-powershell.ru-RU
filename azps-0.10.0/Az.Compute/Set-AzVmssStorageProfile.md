---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 230DAE05-C197-451F-A24C-F4A2DAE4AD04
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssstorageprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVmssStorageProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVmssStorageProfile.md
ms.openlocfilehash: d19c039a5038c9327ea35a4f0b385e5472b748a0
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911312"
---
# <span data-ttu-id="217e1-101">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="217e1-101">Set-AzVmssStorageProfile</span></span>

## <span data-ttu-id="217e1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="217e1-102">SYNOPSIS</span></span>
<span data-ttu-id="217e1-103">Задает свойства профиля хранилища для VMSS.</span><span class="sxs-lookup"><span data-stu-id="217e1-103">Sets the storage profile properties for the VMSS.</span></span>

## <span data-ttu-id="217e1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="217e1-104">SYNTAX</span></span>

```
Set-AzVmssStorageProfile [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-ImageReferencePublisher] <String>] [[-ImageReferenceOffer] <String>] [[-ImageReferenceSku] <String>]
 [[-ImageReferenceVersion] <String>] [[-OsDiskName] <String>] [[-OsDiskCaching] <CachingTypes>]
 [[-OsDiskCreateOption] <DiskCreateOptionTypes>] [[-OsDiskOsType] <OperatingSystemTypes>] [[-Image] <String>]
 [[-VhdContainer] <String[]>] [-ImageReferenceId <String>] [-OsDiskWriteAccelerator]
 [-ManagedDisk <StorageAccountTypes>] [-DataDisk <VirtualMachineScaleSetDataDisk[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="217e1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="217e1-105">DESCRIPTION</span></span>
<span data-ttu-id="217e1-106">Командлет **Set-AzVmssStorageProfile** задает свойства профиля хранения для набора масштабов виртуальных машин (VMSS).</span><span class="sxs-lookup"><span data-stu-id="217e1-106">The **Set-AzVmssStorageProfile** cmdlet sets the storage profile properties for the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="217e1-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="217e1-107">EXAMPLES</span></span>

### <span data-ttu-id="217e1-108">Пример 1: Настройка свойств профиля хранения для VMSS</span><span class="sxs-lookup"><span data-stu-id="217e1-108">Example 1: Set the storage profile properties for the VMSS</span></span>
```
PS C:\> Set-AzVmssStorageProfile -VirtualMachineScaleSet "ContosoVMSS" -Name "Test" -OsDiskCreateOption "FromImage" -OsDiskCaching "None" `
            -ImageReferenceOffer $ImgRef.Offer -ImageReferenceSku $ImgRef.Skus -ImageReferenceVersion $ImgRef.Version `
            -ImageReferencePublisher $ImgRef.PublisherName -VhdContainer $VhdContainer
```

<span data-ttu-id="217e1-109">Эта команда задает свойства профиля хранения для VMSS с именем ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="217e1-109">This command sets the storage profile properties for the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="217e1-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="217e1-110">PARAMETERS</span></span>

### <span data-ttu-id="217e1-111">-Диск</span><span class="sxs-lookup"><span data-stu-id="217e1-111">-DataDisk</span></span>
<span data-ttu-id="217e1-112">Указывает объект диска данных.</span><span class="sxs-lookup"><span data-stu-id="217e1-112">Specifies the data disk object.</span></span>

```yaml
Type: VirtualMachineScaleSetDataDisk[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="217e1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="217e1-113">-DefaultProfile</span></span>
<span data-ttu-id="217e1-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="217e1-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="217e1-115">-Image</span><span class="sxs-lookup"><span data-stu-id="217e1-115">-Image</span></span>
<span data-ttu-id="217e1-116">Указывает URI большого двоичного объекта для пользовательского изображения.</span><span class="sxs-lookup"><span data-stu-id="217e1-116">Specifies the blob URI for the user image.</span></span>
<span data-ttu-id="217e1-117">VMSS создает диск операционной системы в том же контейнере пользовательского образа.</span><span class="sxs-lookup"><span data-stu-id="217e1-117">VMSS creates an operating system disk in the same container of the user image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="217e1-118">-ImageReferenceId</span><span class="sxs-lookup"><span data-stu-id="217e1-118">-ImageReferenceId</span></span>
<span data-ttu-id="217e1-119">Указывает идентификатор ссылки на изображение.</span><span class="sxs-lookup"><span data-stu-id="217e1-119">Specifies the image reference ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="217e1-120">-ImageReferenceOffer</span><span class="sxs-lookup"><span data-stu-id="217e1-120">-ImageReferenceOffer</span></span>
<span data-ttu-id="217e1-121">Указывает тип предложения для образа виртуальной машины (VMImage).</span><span class="sxs-lookup"><span data-stu-id="217e1-121">Specifies the type of virtual machine image (VMImage) offer.</span></span>
<span data-ttu-id="217e1-122">Чтобы получить предложение с изображением, используйте командлет Get-AzVMImageOffer.</span><span class="sxs-lookup"><span data-stu-id="217e1-122">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="217e1-123">-ImageReferencePublisher</span><span class="sxs-lookup"><span data-stu-id="217e1-123">-ImageReferencePublisher</span></span>
<span data-ttu-id="217e1-124">Указывает имя издателя VMImage.</span><span class="sxs-lookup"><span data-stu-id="217e1-124">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="217e1-125">Чтобы получить издатель, используйте командлет Get-AzVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="217e1-125">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="217e1-126">-ImageReferenceSku</span><span class="sxs-lookup"><span data-stu-id="217e1-126">-ImageReferenceSku</span></span>
<span data-ttu-id="217e1-127">Указывает SKU VMImage.</span><span class="sxs-lookup"><span data-stu-id="217e1-127">Specifies the VMImage SKU.</span></span>
<span data-ttu-id="217e1-128">Чтобы получить SKU, используйте командлет Get-AzVMImageSku.</span><span class="sxs-lookup"><span data-stu-id="217e1-128">To obtain SKUs, use the Get-AzVMImageSku cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="217e1-129">-ImageReferenceVersion</span><span class="sxs-lookup"><span data-stu-id="217e1-129">-ImageReferenceVersion</span></span>
<span data-ttu-id="217e1-130">Указывает версию VMImage.</span><span class="sxs-lookup"><span data-stu-id="217e1-130">Specifies the version of the VMImage.</span></span>
<span data-ttu-id="217e1-131">Чтобы использовать последнюю версию, укажите значение, которое не определено в последней версии.</span><span class="sxs-lookup"><span data-stu-id="217e1-131">To use the latest version, specify a value of latest instead of a particular version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="217e1-132">-ManagedDisk</span><span class="sxs-lookup"><span data-stu-id="217e1-132">-ManagedDisk</span></span>
<span data-ttu-id="217e1-133">Задает управляемый диск.</span><span class="sxs-lookup"><span data-stu-id="217e1-133">Specifies the managed disk.</span></span>

```yaml
Type: StorageAccountTypes
Parameter Sets: (All)
Aliases: 
Accepted values: StandardLRS, PremiumLRS

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="217e1-134">-OsDiskCaching</span><span class="sxs-lookup"><span data-stu-id="217e1-134">-OsDiskCaching</span></span>
<span data-ttu-id="217e1-135">Задает режим кэширования диска операционной системы.</span><span class="sxs-lookup"><span data-stu-id="217e1-135">Specifies the caching mode of the operating system disk.</span></span> <span data-ttu-id="217e1-136">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="217e1-136">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="217e1-137">Чтения</span><span class="sxs-lookup"><span data-stu-id="217e1-137">ReadOnly</span></span>
- <span data-ttu-id="217e1-138">Операцию</span><span class="sxs-lookup"><span data-stu-id="217e1-138">ReadWrite</span></span>

<span data-ttu-id="217e1-139">Значением по умолчанию является ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="217e1-139">The default value is ReadWrite.</span></span>
<span data-ttu-id="217e1-140">Если вы измените значение кэширования, командлет перезагрузит виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="217e1-140">If you change the caching value, the cmdlet will restart the virtual machine.</span></span>

<span data-ttu-id="217e1-141">Этот параметр влияет на согласованность и производительность диска.</span><span class="sxs-lookup"><span data-stu-id="217e1-141">This setting affects the consistency and performance of the disk.</span></span>

```yaml
Type: CachingTypes
Parameter Sets: (All)
Aliases: 
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="217e1-142">-OsDiskCreateOption</span><span class="sxs-lookup"><span data-stu-id="217e1-142">-OsDiskCreateOption</span></span>
<span data-ttu-id="217e1-143">Указывает, как этот командлет создает виртуальные машины VMSS.</span><span class="sxs-lookup"><span data-stu-id="217e1-143">Specifies how this cmdlet creates the VMSS virtual machines.</span></span>

<span data-ttu-id="217e1-144">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="217e1-144">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="217e1-145">Прикрепить: это значение используется при использовании специализированного диска для создания виртуальной машины VMSS.</span><span class="sxs-lookup"><span data-stu-id="217e1-145">Attach : This value is used when you are using a specialized disk to create the VMSS virtual machine.</span></span> 
- <span data-ttu-id="217e1-146">FromImage: это значение используется при использовании изображения для создания виртуальной машины VMSS.</span><span class="sxs-lookup"><span data-stu-id="217e1-146">FromImage : This value is used when you are using an image to create the VMSS virtual machine.</span></span>
<span data-ttu-id="217e1-147">Если вы используете образ платформы, вы также будете использовать параметр *imageReference* .</span><span class="sxs-lookup"><span data-stu-id="217e1-147">If you are using a platform image, you will also use the *imageReference* parameter.</span></span>

```yaml
Type: DiskCreateOptionTypes
Parameter Sets: (All)
Aliases: 
Accepted values: FromImage, Empty, Attach

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="217e1-148">-OsDiskName</span><span class="sxs-lookup"><span data-stu-id="217e1-148">-OsDiskName</span></span>
<span data-ttu-id="217e1-149">Указывает имя диска операционной системы.</span><span class="sxs-lookup"><span data-stu-id="217e1-149">Specifies the name of the operating system disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="217e1-150">-OsDiskOsType</span><span class="sxs-lookup"><span data-stu-id="217e1-150">-OsDiskOsType</span></span>
<span data-ttu-id="217e1-151">Указывает тип операционной системы на диске.</span><span class="sxs-lookup"><span data-stu-id="217e1-151">Specifies the type of operating system on the disk.</span></span>
<span data-ttu-id="217e1-152">Это необходимо только для сценариев пользовательского изображения, а не для образа платформы.</span><span class="sxs-lookup"><span data-stu-id="217e1-152">This is only needed for user image scenarios and not for a platform image.</span></span>

```yaml
Type: OperatingSystemTypes
Parameter Sets: (All)
Aliases: 
Accepted values: Windows, Linux

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="217e1-153">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="217e1-153">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="217e1-154">Указывает, следует ли включить или отключить WriteAccelerator на диске операционной системы.</span><span class="sxs-lookup"><span data-stu-id="217e1-154">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="217e1-155">-VhdContainer</span><span class="sxs-lookup"><span data-stu-id="217e1-155">-VhdContainer</span></span>
<span data-ttu-id="217e1-156">Указывает URL-адреса контейнеров, которые используются для хранения дисков операционной системы для VMSS.</span><span class="sxs-lookup"><span data-stu-id="217e1-156">Specifies the container URLs that are used to store operating system disks for the VMSS.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="217e1-157">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="217e1-157">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="217e1-158">Указывает объект VMSS.</span><span class="sxs-lookup"><span data-stu-id="217e1-158">Specifies the VMSS object.</span></span>
<span data-ttu-id="217e1-159">Чтобы получить объект, используйте объект New-AzVmssConfig.</span><span class="sxs-lookup"><span data-stu-id="217e1-159">To obtain the object, use the New-AzVmssConfig object.</span></span>

```yaml
Type: PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="217e1-160">-Confirm</span><span class="sxs-lookup"><span data-stu-id="217e1-160">-Confirm</span></span>
<span data-ttu-id="217e1-161">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="217e1-161">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="217e1-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="217e1-162">-WhatIf</span></span>
<span data-ttu-id="217e1-163">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="217e1-163">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="217e1-164">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="217e1-164">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="217e1-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="217e1-165">CommonParameters</span></span>
<span data-ttu-id="217e1-166">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="217e1-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="217e1-167">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="217e1-167">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="217e1-168">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="217e1-168">INPUTS</span></span>

###  
<span data-ttu-id="217e1-169">Этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="217e1-169">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="217e1-170">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="217e1-170">OUTPUTS</span></span>

### <span data-ttu-id="217e1-171">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="217e1-171">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="217e1-172">Пуск</span><span class="sxs-lookup"><span data-stu-id="217e1-172">NOTES</span></span>

## <span data-ttu-id="217e1-173">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="217e1-173">RELATED LINKS</span></span>

[<span data-ttu-id="217e1-174">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="217e1-174">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="217e1-175">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="217e1-175">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="217e1-176">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="217e1-176">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="217e1-177">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="217e1-177">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)



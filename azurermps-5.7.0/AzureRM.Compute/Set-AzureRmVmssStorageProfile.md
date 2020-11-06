---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 230DAE05-C197-451F-A24C-F4A2DAE4AD04
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmssStorageProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmssStorageProfile.md
ms.openlocfilehash: 26f61261bd8fd1c2d5fc2bbdacec71f73db91fb9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566202"
---
# <span data-ttu-id="6abc1-101">Set-AzureRmVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="6abc1-101">Set-AzureRmVmssStorageProfile</span></span>

## <span data-ttu-id="6abc1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6abc1-102">SYNOPSIS</span></span>
<span data-ttu-id="6abc1-103">Задает свойства профиля хранилища для VMSS.</span><span class="sxs-lookup"><span data-stu-id="6abc1-103">Sets the storage profile properties for the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6abc1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6abc1-104">SYNTAX</span></span>

```
Set-AzureRmVmssStorageProfile [-VirtualMachineScaleSet] <VirtualMachineScaleSet>
 [[-ImageReferencePublisher] <String>] [[-ImageReferenceOffer] <String>] [[-ImageReferenceSku] <String>]
 [[-ImageReferenceVersion] <String>] [-OsDiskName <String>] [[-OsDiskCaching] <CachingTypes>]
 [[-OsDiskCreateOption] <DiskCreateOptionTypes>] [[-OsDiskOsType] <OperatingSystemTypes>] [[-Image] <String>]
 [[-VhdContainer] <String[]>] [-ImageReferenceId <String>] [-ManagedDisk <StorageAccountTypes>]
 [-DataDisk <VirtualMachineScaleSetDataDisk[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6abc1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6abc1-105">DESCRIPTION</span></span>
<span data-ttu-id="6abc1-106">Командлет **Set-AzureRmVmssStorageProfile** задает свойства профиля хранения для набора масштабов виртуальных машин (VMSS).</span><span class="sxs-lookup"><span data-stu-id="6abc1-106">The **Set-AzureRmVmssStorageProfile** cmdlet sets the storage profile properties for the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="6abc1-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6abc1-107">EXAMPLES</span></span>

### <span data-ttu-id="6abc1-108">Пример 1: Настройка свойств профиля хранения для VMSS</span><span class="sxs-lookup"><span data-stu-id="6abc1-108">Example 1: Set the storage profile properties for the VMSS</span></span>
```
PS C:\> Set-AzureRmVmssStorageProfile -VirtualMachineScaleSet "ContosoVMSS" -Name "Test" -OsDiskCreateOption "FromImage" -OsDiskCaching "None" `
            -ImageReferenceOffer $ImgRef.Offer -ImageReferenceSku $ImgRef.Skus -ImageReferenceVersion $ImgRef.Version `
            -ImageReferencePublisher $ImgRef.PublisherName -VhdContainer $VhdContainer
```

<span data-ttu-id="6abc1-109">Эта команда задает свойства профиля хранения для VMSS с именем ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="6abc1-109">This command sets the storage profile properties for the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="6abc1-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6abc1-110">PARAMETERS</span></span>

### <span data-ttu-id="6abc1-111">-Диск</span><span class="sxs-lookup"><span data-stu-id="6abc1-111">-DataDisk</span></span>
<span data-ttu-id="6abc1-112">Указывает объект диска данных.</span><span class="sxs-lookup"><span data-stu-id="6abc1-112">Specifies the data disk object.</span></span>

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

### <span data-ttu-id="6abc1-113">-Image</span><span class="sxs-lookup"><span data-stu-id="6abc1-113">-Image</span></span>
<span data-ttu-id="6abc1-114">Указывает URI большого двоичного объекта для пользовательского изображения.</span><span class="sxs-lookup"><span data-stu-id="6abc1-114">Specifies the blob URI for the user image.</span></span>
<span data-ttu-id="6abc1-115">VMSS создает диск операционной системы в том же контейнере пользовательского образа.</span><span class="sxs-lookup"><span data-stu-id="6abc1-115">VMSS creates an operating system disk in the same container of the user image.</span></span>

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

### <span data-ttu-id="6abc1-116">-ImageReferenceId</span><span class="sxs-lookup"><span data-stu-id="6abc1-116">-ImageReferenceId</span></span>
<span data-ttu-id="6abc1-117">Указывает идентификатор ссылки на изображение.</span><span class="sxs-lookup"><span data-stu-id="6abc1-117">Specifies the image reference ID.</span></span>

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

### <span data-ttu-id="6abc1-118">-ImageReferenceOffer</span><span class="sxs-lookup"><span data-stu-id="6abc1-118">-ImageReferenceOffer</span></span>
<span data-ttu-id="6abc1-119">Указывает тип предложения для образа виртуальной машины (VMImage).</span><span class="sxs-lookup"><span data-stu-id="6abc1-119">Specifies the type of virtual machine image (VMImage) offer.</span></span>
<span data-ttu-id="6abc1-120">Чтобы получить предложение с изображением, используйте командлет Get-AzureRmVMImageOffer.</span><span class="sxs-lookup"><span data-stu-id="6abc1-120">To obtain an image offer, use the Get-AzureRmVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="6abc1-121">-ImageReferencePublisher</span><span class="sxs-lookup"><span data-stu-id="6abc1-121">-ImageReferencePublisher</span></span>
<span data-ttu-id="6abc1-122">Указывает имя издателя VMImage.</span><span class="sxs-lookup"><span data-stu-id="6abc1-122">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="6abc1-123">Чтобы получить издатель, используйте командлет Get-AzureRmVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="6abc1-123">To obtain a publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="6abc1-124">-ImageReferenceSku</span><span class="sxs-lookup"><span data-stu-id="6abc1-124">-ImageReferenceSku</span></span>
<span data-ttu-id="6abc1-125">Указывает SKU VMImage.</span><span class="sxs-lookup"><span data-stu-id="6abc1-125">Specifies the VMImage SKU.</span></span>
<span data-ttu-id="6abc1-126">Чтобы получить SKU, используйте командлет Get-AzureRmVMImageSku.</span><span class="sxs-lookup"><span data-stu-id="6abc1-126">To obtain SKUs, use the Get-AzureRmVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="6abc1-127">-ImageReferenceVersion</span><span class="sxs-lookup"><span data-stu-id="6abc1-127">-ImageReferenceVersion</span></span>
<span data-ttu-id="6abc1-128">Указывает версию VMImage.</span><span class="sxs-lookup"><span data-stu-id="6abc1-128">Specifies the version of the VMImage.</span></span>
<span data-ttu-id="6abc1-129">Чтобы использовать последнюю версию, укажите значение, которое не определено в последней версии.</span><span class="sxs-lookup"><span data-stu-id="6abc1-129">To use the latest version, specify a value of latest instead of a particular version.</span></span>

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

### <span data-ttu-id="6abc1-130">-ManagedDisk</span><span class="sxs-lookup"><span data-stu-id="6abc1-130">-ManagedDisk</span></span>
<span data-ttu-id="6abc1-131">Задает управляемый диск.</span><span class="sxs-lookup"><span data-stu-id="6abc1-131">Specifies the managed disk.</span></span>

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

### <span data-ttu-id="6abc1-132">-OsDiskCaching</span><span class="sxs-lookup"><span data-stu-id="6abc1-132">-OsDiskCaching</span></span>
<span data-ttu-id="6abc1-133">Задает режим кэширования диска операционной системы.</span><span class="sxs-lookup"><span data-stu-id="6abc1-133">Specifies the caching mode of the operating system disk.</span></span> <span data-ttu-id="6abc1-134">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="6abc1-134">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6abc1-135">Чтения</span><span class="sxs-lookup"><span data-stu-id="6abc1-135">ReadOnly</span></span>
- <span data-ttu-id="6abc1-136">Операцию</span><span class="sxs-lookup"><span data-stu-id="6abc1-136">ReadWrite</span></span>

<span data-ttu-id="6abc1-137">Значением по умолчанию является ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="6abc1-137">The default value is ReadWrite.</span></span>
<span data-ttu-id="6abc1-138">Если вы измените значение кэширования, командлет перезагрузит виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="6abc1-138">If you change the caching value, the cmdlet will restart the virtual machine.</span></span>

<span data-ttu-id="6abc1-139">Этот параметр влияет на согласованность и производительность диска.</span><span class="sxs-lookup"><span data-stu-id="6abc1-139">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="6abc1-140">-OsDiskCreateOption</span><span class="sxs-lookup"><span data-stu-id="6abc1-140">-OsDiskCreateOption</span></span>
<span data-ttu-id="6abc1-141">Указывает, как этот командлет создает виртуальные машины VMSS.</span><span class="sxs-lookup"><span data-stu-id="6abc1-141">Specifies how this cmdlet creates the VMSS virtual machines.</span></span>

<span data-ttu-id="6abc1-142">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="6abc1-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6abc1-143">Прикрепить: это значение используется при использовании специализированного диска для создания виртуальной машины VMSS.</span><span class="sxs-lookup"><span data-stu-id="6abc1-143">Attach : This value is used when you are using a specialized disk to create the VMSS virtual machine.</span></span> 
- <span data-ttu-id="6abc1-144">FromImage: это значение используется при использовании изображения для создания виртуальной машины VMSS.</span><span class="sxs-lookup"><span data-stu-id="6abc1-144">FromImage : This value is used when you are using an image to create the VMSS virtual machine.</span></span>
<span data-ttu-id="6abc1-145">Если вы используете образ платформы, вы также будете использовать параметр *imageReference* .</span><span class="sxs-lookup"><span data-stu-id="6abc1-145">If you are using a platform image, you will also use the *imageReference* parameter.</span></span>

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

### <span data-ttu-id="6abc1-146">-OsDiskName</span><span class="sxs-lookup"><span data-stu-id="6abc1-146">-OsDiskName</span></span>
<span data-ttu-id="6abc1-147">Указывает имя диска операционной системы.</span><span class="sxs-lookup"><span data-stu-id="6abc1-147">Specifies the name of the operating system disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6abc1-148">-OsDiskOsType</span><span class="sxs-lookup"><span data-stu-id="6abc1-148">-OsDiskOsType</span></span>
<span data-ttu-id="6abc1-149">Указывает тип операционной системы на диске.</span><span class="sxs-lookup"><span data-stu-id="6abc1-149">Specifies the type of operating system on the disk.</span></span>
<span data-ttu-id="6abc1-150">Это необходимо только для сценариев пользовательского изображения, а не для образа платформы.</span><span class="sxs-lookup"><span data-stu-id="6abc1-150">This is only needed for user image scenarios and not for a platform image.</span></span>

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

### <span data-ttu-id="6abc1-151">-VhdContainer</span><span class="sxs-lookup"><span data-stu-id="6abc1-151">-VhdContainer</span></span>
<span data-ttu-id="6abc1-152">Указывает URL-адреса контейнеров, которые используются для хранения дисков операционной системы для VMSS.</span><span class="sxs-lookup"><span data-stu-id="6abc1-152">Specifies the container URLs that are used to store operating system disks for the VMSS.</span></span>

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

### <span data-ttu-id="6abc1-153">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="6abc1-153">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="6abc1-154">Указывает объект VMSS.</span><span class="sxs-lookup"><span data-stu-id="6abc1-154">Specifies the VMSS object.</span></span>
<span data-ttu-id="6abc1-155">Чтобы получить объект, используйте объект New-AzureRmVmssConfig.</span><span class="sxs-lookup"><span data-stu-id="6abc1-155">To obtain the object, use the New-AzureRmVmssConfig object.</span></span>

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6abc1-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6abc1-156">-Confirm</span></span>
<span data-ttu-id="6abc1-157">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6abc1-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6abc1-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6abc1-158">-WhatIf</span></span>
<span data-ttu-id="6abc1-159">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6abc1-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6abc1-160">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6abc1-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6abc1-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6abc1-161">CommonParameters</span></span>
<span data-ttu-id="6abc1-162">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6abc1-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6abc1-163">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6abc1-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6abc1-164">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6abc1-164">INPUTS</span></span>

###  
<span data-ttu-id="6abc1-165">Этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="6abc1-165">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="6abc1-166">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6abc1-166">OUTPUTS</span></span>

## <span data-ttu-id="6abc1-167">Пуск</span><span class="sxs-lookup"><span data-stu-id="6abc1-167">NOTES</span></span>

## <span data-ttu-id="6abc1-168">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6abc1-168">RELATED LINKS</span></span>

[<span data-ttu-id="6abc1-169">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="6abc1-169">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="6abc1-170">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="6abc1-170">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="6abc1-171">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="6abc1-171">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="6abc1-172">New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="6abc1-172">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)



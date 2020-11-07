---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 230DAE05-C197-451F-A24C-F4A2DAE4AD04
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmssstorageprofile
schema: 2.0.0
ms.openlocfilehash: c96ff571ef1b82e52a313c2044a41b97d46ffa0b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913907"
---
# <span data-ttu-id="78323-101">Set-AzureRmVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="78323-101">Set-AzureRmVmssStorageProfile</span></span>

## <span data-ttu-id="78323-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="78323-102">SYNOPSIS</span></span>
<span data-ttu-id="78323-103">Задает свойства профиля хранилища для VMSS.</span><span class="sxs-lookup"><span data-stu-id="78323-103">Sets the storage profile properties for the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="78323-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="78323-104">SYNTAX</span></span>

```
Set-AzureRmVmssStorageProfile [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-ImageReferencePublisher] <String>] [[-ImageReferenceOffer] <String>] [[-ImageReferenceSku] <String>]
 [[-ImageReferenceVersion] <String>] [[-OsDiskName] <String>] [[-OsDiskCaching] <CachingTypes>]
 [[-OsDiskCreateOption] <DiskCreateOptionTypes>] [[-OsDiskOsType] <OperatingSystemTypes>] [[-Image] <String>]
 [[-VhdContainer] <String[]>] [-ImageReferenceId <String>] [-OsDiskWriteAccelerator]
 [-ManagedDisk <StorageAccountTypes>] [-DataDisk <VirtualMachineScaleSetDataDisk[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78323-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="78323-105">DESCRIPTION</span></span>
<span data-ttu-id="78323-106">Командлет **Set-AzureRmVmssStorageProfile** задает свойства профиля хранения для набора масштабов виртуальных машин (VMSS).</span><span class="sxs-lookup"><span data-stu-id="78323-106">The **Set-AzureRmVmssStorageProfile** cmdlet sets the storage profile properties for the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="78323-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="78323-107">EXAMPLES</span></span>

### <span data-ttu-id="78323-108">Пример 1: Настройка свойств профиля хранения для VMSS</span><span class="sxs-lookup"><span data-stu-id="78323-108">Example 1: Set the storage profile properties for the VMSS</span></span>
```
PS C:\> Set-AzureRmVmssStorageProfile -VirtualMachineScaleSet "ContosoVMSS" -Name "Test" -OsDiskCreateOption "FromImage" -OsDiskCaching "None" `
            -ImageReferenceOffer $ImgRef.Offer -ImageReferenceSku $ImgRef.Skus -ImageReferenceVersion $ImgRef.Version `
            -ImageReferencePublisher $ImgRef.PublisherName -VhdContainer $VhdContainer
```

<span data-ttu-id="78323-109">Эта команда задает свойства профиля хранения для VMSS с именем ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="78323-109">This command sets the storage profile properties for the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="78323-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="78323-110">PARAMETERS</span></span>

### <span data-ttu-id="78323-111">-Диск</span><span class="sxs-lookup"><span data-stu-id="78323-111">-DataDisk</span></span>
<span data-ttu-id="78323-112">Указывает объект диска данных.</span><span class="sxs-lookup"><span data-stu-id="78323-112">Specifies the data disk object.</span></span>

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

### <span data-ttu-id="78323-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78323-113">-DefaultProfile</span></span>
<span data-ttu-id="78323-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="78323-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="78323-115">-Image</span><span class="sxs-lookup"><span data-stu-id="78323-115">-Image</span></span>
<span data-ttu-id="78323-116">Указывает URI большого двоичного объекта для пользовательского изображения.</span><span class="sxs-lookup"><span data-stu-id="78323-116">Specifies the blob URI for the user image.</span></span>
<span data-ttu-id="78323-117">VMSS создает диск операционной системы в том же контейнере пользовательского образа.</span><span class="sxs-lookup"><span data-stu-id="78323-117">VMSS creates an operating system disk in the same container of the user image.</span></span>

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

### <span data-ttu-id="78323-118">-ImageReferenceId</span><span class="sxs-lookup"><span data-stu-id="78323-118">-ImageReferenceId</span></span>
<span data-ttu-id="78323-119">Указывает идентификатор ссылки на изображение.</span><span class="sxs-lookup"><span data-stu-id="78323-119">Specifies the image reference ID.</span></span>

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

### <span data-ttu-id="78323-120">-ImageReferenceOffer</span><span class="sxs-lookup"><span data-stu-id="78323-120">-ImageReferenceOffer</span></span>
<span data-ttu-id="78323-121">Указывает тип предложения для образа виртуальной машины (VMImage).</span><span class="sxs-lookup"><span data-stu-id="78323-121">Specifies the type of virtual machine image (VMImage) offer.</span></span>
<span data-ttu-id="78323-122">Чтобы получить предложение с изображением, используйте командлет Get-AzureRmVMImageOffer.</span><span class="sxs-lookup"><span data-stu-id="78323-122">To obtain an image offer, use the Get-AzureRmVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="78323-123">-ImageReferencePublisher</span><span class="sxs-lookup"><span data-stu-id="78323-123">-ImageReferencePublisher</span></span>
<span data-ttu-id="78323-124">Указывает имя издателя VMImage.</span><span class="sxs-lookup"><span data-stu-id="78323-124">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="78323-125">Чтобы получить издатель, используйте командлет Get-AzureRmVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="78323-125">To obtain a publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="78323-126">-ImageReferenceSku</span><span class="sxs-lookup"><span data-stu-id="78323-126">-ImageReferenceSku</span></span>
<span data-ttu-id="78323-127">Указывает SKU VMImage.</span><span class="sxs-lookup"><span data-stu-id="78323-127">Specifies the VMImage SKU.</span></span>
<span data-ttu-id="78323-128">Чтобы получить SKU, используйте командлет Get-AzureRmVMImageSku.</span><span class="sxs-lookup"><span data-stu-id="78323-128">To obtain SKUs, use the Get-AzureRmVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="78323-129">-ImageReferenceVersion</span><span class="sxs-lookup"><span data-stu-id="78323-129">-ImageReferenceVersion</span></span>
<span data-ttu-id="78323-130">Указывает версию VMImage.</span><span class="sxs-lookup"><span data-stu-id="78323-130">Specifies the version of the VMImage.</span></span>
<span data-ttu-id="78323-131">Чтобы использовать последнюю версию, укажите значение, которое не определено в последней версии.</span><span class="sxs-lookup"><span data-stu-id="78323-131">To use the latest version, specify a value of latest instead of a particular version.</span></span>

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

### <span data-ttu-id="78323-132">-ManagedDisk</span><span class="sxs-lookup"><span data-stu-id="78323-132">-ManagedDisk</span></span>
<span data-ttu-id="78323-133">Задает управляемый диск.</span><span class="sxs-lookup"><span data-stu-id="78323-133">Specifies the managed disk.</span></span>

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

### <span data-ttu-id="78323-134">-OsDiskCaching</span><span class="sxs-lookup"><span data-stu-id="78323-134">-OsDiskCaching</span></span>
<span data-ttu-id="78323-135">Задает режим кэширования диска операционной системы.</span><span class="sxs-lookup"><span data-stu-id="78323-135">Specifies the caching mode of the operating system disk.</span></span> <span data-ttu-id="78323-136">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="78323-136">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="78323-137">Чтения</span><span class="sxs-lookup"><span data-stu-id="78323-137">ReadOnly</span></span>
- <span data-ttu-id="78323-138">Операцию</span><span class="sxs-lookup"><span data-stu-id="78323-138">ReadWrite</span></span>

<span data-ttu-id="78323-139">Значением по умолчанию является ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="78323-139">The default value is ReadWrite.</span></span>
<span data-ttu-id="78323-140">Если вы измените значение кэширования, командлет перезагрузит виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="78323-140">If you change the caching value, the cmdlet will restart the virtual machine.</span></span>

<span data-ttu-id="78323-141">Этот параметр влияет на согласованность и производительность диска.</span><span class="sxs-lookup"><span data-stu-id="78323-141">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="78323-142">-OsDiskCreateOption</span><span class="sxs-lookup"><span data-stu-id="78323-142">-OsDiskCreateOption</span></span>
<span data-ttu-id="78323-143">Указывает, как этот командлет создает виртуальные машины VMSS.</span><span class="sxs-lookup"><span data-stu-id="78323-143">Specifies how this cmdlet creates the VMSS virtual machines.</span></span>

<span data-ttu-id="78323-144">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="78323-144">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="78323-145">Прикрепить: это значение используется при использовании специализированного диска для создания виртуальной машины VMSS.</span><span class="sxs-lookup"><span data-stu-id="78323-145">Attach : This value is used when you are using a specialized disk to create the VMSS virtual machine.</span></span> 
- <span data-ttu-id="78323-146">FromImage: это значение используется при использовании изображения для создания виртуальной машины VMSS.</span><span class="sxs-lookup"><span data-stu-id="78323-146">FromImage : This value is used when you are using an image to create the VMSS virtual machine.</span></span>
<span data-ttu-id="78323-147">Если вы используете образ платформы, вы также будете использовать параметр *imageReference* .</span><span class="sxs-lookup"><span data-stu-id="78323-147">If you are using a platform image, you will also use the *imageReference* parameter.</span></span>

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

### <span data-ttu-id="78323-148">-OsDiskName</span><span class="sxs-lookup"><span data-stu-id="78323-148">-OsDiskName</span></span>
<span data-ttu-id="78323-149">Указывает имя диска операционной системы.</span><span class="sxs-lookup"><span data-stu-id="78323-149">Specifies the name of the operating system disk.</span></span>

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

### <span data-ttu-id="78323-150">-OsDiskOsType</span><span class="sxs-lookup"><span data-stu-id="78323-150">-OsDiskOsType</span></span>
<span data-ttu-id="78323-151">Указывает тип операционной системы на диске.</span><span class="sxs-lookup"><span data-stu-id="78323-151">Specifies the type of operating system on the disk.</span></span>
<span data-ttu-id="78323-152">Это необходимо только для сценариев пользовательского изображения, а не для образа платформы.</span><span class="sxs-lookup"><span data-stu-id="78323-152">This is only needed for user image scenarios and not for a platform image.</span></span>

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

### <span data-ttu-id="78323-153">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="78323-153">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="78323-154">Указывает, следует ли включить или отключить WriteAccelerator на диске операционной системы.</span><span class="sxs-lookup"><span data-stu-id="78323-154">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="78323-155">-VhdContainer</span><span class="sxs-lookup"><span data-stu-id="78323-155">-VhdContainer</span></span>
<span data-ttu-id="78323-156">Указывает URL-адреса контейнеров, которые используются для хранения дисков операционной системы для VMSS.</span><span class="sxs-lookup"><span data-stu-id="78323-156">Specifies the container URLs that are used to store operating system disks for the VMSS.</span></span>

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

### <span data-ttu-id="78323-157">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="78323-157">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="78323-158">Указывает объект VMSS.</span><span class="sxs-lookup"><span data-stu-id="78323-158">Specifies the VMSS object.</span></span>
<span data-ttu-id="78323-159">Чтобы получить объект, используйте объект New-AzureRmVmssConfig.</span><span class="sxs-lookup"><span data-stu-id="78323-159">To obtain the object, use the New-AzureRmVmssConfig object.</span></span>

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

### <span data-ttu-id="78323-160">-Confirm</span><span class="sxs-lookup"><span data-stu-id="78323-160">-Confirm</span></span>
<span data-ttu-id="78323-161">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="78323-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78323-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78323-162">-WhatIf</span></span>
<span data-ttu-id="78323-163">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="78323-163">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="78323-164">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="78323-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78323-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78323-165">CommonParameters</span></span>
<span data-ttu-id="78323-166">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="78323-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78323-167">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78323-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78323-168">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="78323-168">INPUTS</span></span>

###  
<span data-ttu-id="78323-169">Этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="78323-169">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="78323-170">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="78323-170">OUTPUTS</span></span>

### <span data-ttu-id="78323-171">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="78323-171">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="78323-172">Пуск</span><span class="sxs-lookup"><span data-stu-id="78323-172">NOTES</span></span>

## <span data-ttu-id="78323-173">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="78323-173">RELATED LINKS</span></span>

[<span data-ttu-id="78323-174">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="78323-174">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="78323-175">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="78323-175">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="78323-176">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="78323-176">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="78323-177">New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="78323-177">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)



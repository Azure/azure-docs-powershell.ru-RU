---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 230DAE05-C197-451F-A24C-F4A2DAE4AD04
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmssStorageProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmssStorageProfile.md
ms.openlocfilehash: 60d525cc50b62350853755ae46698cbecb358654
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557779"
---
# <span data-ttu-id="4638b-101">Set-AzureRmVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="4638b-101">Set-AzureRmVmssStorageProfile</span></span>

## <span data-ttu-id="4638b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4638b-102">SYNOPSIS</span></span>
<span data-ttu-id="4638b-103">Задает свойства профиля хранилища для VMSS.</span><span class="sxs-lookup"><span data-stu-id="4638b-103">Sets the storage profile properties for the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4638b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4638b-104">SYNTAX</span></span>

```
Set-AzureRmVmssStorageProfile [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-ImageReferencePublisher] <String>] [[-ImageReferenceOffer] <String>] [[-ImageReferenceSku] <String>]
 [[-ImageReferenceVersion] <String>] [[-OsDiskName] <String>] [[-OsDiskCaching] <CachingTypes>]
 [[-OsDiskCreateOption] <DiskCreateOptionTypes>] [[-OsDiskOsType] <OperatingSystemTypes>] [[-Image] <String>]
 [[-VhdContainer] <String[]>] [-ImageReferenceId <String>] [-ManagedDisk <StorageAccountTypes>]
 [-DataDisk <VirtualMachineScaleSetDataDisk[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4638b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4638b-105">DESCRIPTION</span></span>
<span data-ttu-id="4638b-106">Командлет **Set-AzureRmVmssStorageProfile** задает свойства профиля хранения для набора масштабов виртуальных машин (VMSS).</span><span class="sxs-lookup"><span data-stu-id="4638b-106">The **Set-AzureRmVmssStorageProfile** cmdlet sets the storage profile properties for the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="4638b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4638b-107">EXAMPLES</span></span>

### <span data-ttu-id="4638b-108">Пример 1: Настройка свойств профиля хранения для VMSS</span><span class="sxs-lookup"><span data-stu-id="4638b-108">Example 1: Set the storage profile properties for the VMSS</span></span>
```
PS C:\> Set-AzureRmVmssStorageProfile -VirtualMachineScaleSet "ContosoVMSS" -Name "Test" -OsDiskCreateOption "FromImage" -OsDiskCaching "None" `
            -ImageReferenceOffer $ImgRef.Offer -ImageReferenceSku $ImgRef.Skus -ImageReferenceVersion $ImgRef.Version `
            -ImageReferencePublisher $ImgRef.PublisherName -VhdContainer $VhdContainer
```

<span data-ttu-id="4638b-109">Эта команда задает свойства профиля хранения для VMSS с именем ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="4638b-109">This command sets the storage profile properties for the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="4638b-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4638b-110">PARAMETERS</span></span>

### <span data-ttu-id="4638b-111">-Диск</span><span class="sxs-lookup"><span data-stu-id="4638b-111">-DataDisk</span></span>
<span data-ttu-id="4638b-112">Указывает объект диска данных.</span><span class="sxs-lookup"><span data-stu-id="4638b-112">Specifies the data disk object.</span></span>

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

### <span data-ttu-id="4638b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4638b-113">-DefaultProfile</span></span>
<span data-ttu-id="4638b-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4638b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4638b-115">-Image</span><span class="sxs-lookup"><span data-stu-id="4638b-115">-Image</span></span>
<span data-ttu-id="4638b-116">Указывает URI большого двоичного объекта для пользовательского изображения.</span><span class="sxs-lookup"><span data-stu-id="4638b-116">Specifies the blob URI for the user image.</span></span>
<span data-ttu-id="4638b-117">VMSS создает диск операционной системы в том же контейнере пользовательского образа.</span><span class="sxs-lookup"><span data-stu-id="4638b-117">VMSS creates an operating system disk in the same container of the user image.</span></span>

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

### <span data-ttu-id="4638b-118">-ImageReferenceId</span><span class="sxs-lookup"><span data-stu-id="4638b-118">-ImageReferenceId</span></span>
<span data-ttu-id="4638b-119">Указывает идентификатор ссылки на изображение.</span><span class="sxs-lookup"><span data-stu-id="4638b-119">Specifies the image reference ID.</span></span>

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

### <span data-ttu-id="4638b-120">-ImageReferenceOffer</span><span class="sxs-lookup"><span data-stu-id="4638b-120">-ImageReferenceOffer</span></span>
<span data-ttu-id="4638b-121">Указывает тип предложения для образа виртуальной машины (VMImage).</span><span class="sxs-lookup"><span data-stu-id="4638b-121">Specifies the type of virtual machine image (VMImage) offer.</span></span>
<span data-ttu-id="4638b-122">Чтобы получить предложение с изображением, используйте командлет Get-AzureRmVMImageOffer.</span><span class="sxs-lookup"><span data-stu-id="4638b-122">To obtain an image offer, use the Get-AzureRmVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="4638b-123">-ImageReferencePublisher</span><span class="sxs-lookup"><span data-stu-id="4638b-123">-ImageReferencePublisher</span></span>
<span data-ttu-id="4638b-124">Указывает имя издателя VMImage.</span><span class="sxs-lookup"><span data-stu-id="4638b-124">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="4638b-125">Чтобы получить издатель, используйте командлет Get-AzureRmVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="4638b-125">To obtain a publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="4638b-126">-ImageReferenceSku</span><span class="sxs-lookup"><span data-stu-id="4638b-126">-ImageReferenceSku</span></span>
<span data-ttu-id="4638b-127">Указывает SKU VMImage.</span><span class="sxs-lookup"><span data-stu-id="4638b-127">Specifies the VMImage SKU.</span></span>
<span data-ttu-id="4638b-128">Чтобы получить SKU, используйте командлет Get-AzureRmVMImageSku.</span><span class="sxs-lookup"><span data-stu-id="4638b-128">To obtain SKUs, use the Get-AzureRmVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="4638b-129">-ImageReferenceVersion</span><span class="sxs-lookup"><span data-stu-id="4638b-129">-ImageReferenceVersion</span></span>
<span data-ttu-id="4638b-130">Указывает версию VMImage.</span><span class="sxs-lookup"><span data-stu-id="4638b-130">Specifies the version of the VMImage.</span></span>
<span data-ttu-id="4638b-131">Чтобы использовать последнюю версию, укажите значение, которое не определено в последней версии.</span><span class="sxs-lookup"><span data-stu-id="4638b-131">To use the latest version, specify a value of latest instead of a particular version.</span></span>

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

### <span data-ttu-id="4638b-132">-ManagedDisk</span><span class="sxs-lookup"><span data-stu-id="4638b-132">-ManagedDisk</span></span>
<span data-ttu-id="4638b-133">Задает управляемый диск.</span><span class="sxs-lookup"><span data-stu-id="4638b-133">Specifies the managed disk.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.StorageAccountTypes]
Parameter Sets: (All)
Aliases: 
Accepted values: StandardLRS, PremiumLRS

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4638b-134">-OsDiskCaching</span><span class="sxs-lookup"><span data-stu-id="4638b-134">-OsDiskCaching</span></span>
<span data-ttu-id="4638b-135">Задает режим кэширования диска операционной системы.</span><span class="sxs-lookup"><span data-stu-id="4638b-135">Specifies the caching mode of the operating system disk.</span></span> <span data-ttu-id="4638b-136">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="4638b-136">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4638b-137">Чтения</span><span class="sxs-lookup"><span data-stu-id="4638b-137">ReadOnly</span></span>
- <span data-ttu-id="4638b-138">Операцию</span><span class="sxs-lookup"><span data-stu-id="4638b-138">ReadWrite</span></span>

<span data-ttu-id="4638b-139">Значением по умолчанию является ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="4638b-139">The default value is ReadWrite.</span></span>
<span data-ttu-id="4638b-140">Если вы измените значение кэширования, командлет перезагрузит виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="4638b-140">If you change the caching value, the cmdlet will restart the virtual machine.</span></span>

<span data-ttu-id="4638b-141">Этот параметр влияет на согласованность и производительность диска.</span><span class="sxs-lookup"><span data-stu-id="4638b-141">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="4638b-142">-OsDiskCreateOption</span><span class="sxs-lookup"><span data-stu-id="4638b-142">-OsDiskCreateOption</span></span>
<span data-ttu-id="4638b-143">Указывает, как этот командлет создает виртуальные машины VMSS.</span><span class="sxs-lookup"><span data-stu-id="4638b-143">Specifies how this cmdlet creates the VMSS virtual machines.</span></span>

<span data-ttu-id="4638b-144">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="4638b-144">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4638b-145">Прикрепить: это значение используется при использовании специализированного диска для создания виртуальной машины VMSS.</span><span class="sxs-lookup"><span data-stu-id="4638b-145">Attach : This value is used when you are using a specialized disk to create the VMSS virtual machine.</span></span> 
- <span data-ttu-id="4638b-146">FromImage: это значение используется при использовании изображения для создания виртуальной машины VMSS.</span><span class="sxs-lookup"><span data-stu-id="4638b-146">FromImage : This value is used when you are using an image to create the VMSS virtual machine.</span></span>
<span data-ttu-id="4638b-147">Если вы используете образ платформы, вы также будете использовать параметр *imageReference* .</span><span class="sxs-lookup"><span data-stu-id="4638b-147">If you are using a platform image, you will also use the *imageReference* parameter.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.DiskCreateOptionTypes]
Parameter Sets: (All)
Aliases: 
Accepted values: FromImage, Empty, Attach

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4638b-148">-OsDiskName</span><span class="sxs-lookup"><span data-stu-id="4638b-148">-OsDiskName</span></span>
<span data-ttu-id="4638b-149">Указывает имя диска операционной системы.</span><span class="sxs-lookup"><span data-stu-id="4638b-149">Specifies the name of the operating system disk.</span></span>

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

### <span data-ttu-id="4638b-150">-OsDiskOsType</span><span class="sxs-lookup"><span data-stu-id="4638b-150">-OsDiskOsType</span></span>
<span data-ttu-id="4638b-151">Указывает тип операционной системы на диске.</span><span class="sxs-lookup"><span data-stu-id="4638b-151">Specifies the type of operating system on the disk.</span></span>
<span data-ttu-id="4638b-152">Это необходимо только для сценариев пользовательского изображения, а не для образа платформы.</span><span class="sxs-lookup"><span data-stu-id="4638b-152">This is only needed for user image scenarios and not for a platform image.</span></span>

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

### <span data-ttu-id="4638b-153">-VhdContainer</span><span class="sxs-lookup"><span data-stu-id="4638b-153">-VhdContainer</span></span>
<span data-ttu-id="4638b-154">Указывает URL-адреса контейнеров, которые используются для хранения дисков операционной системы для VMSS.</span><span class="sxs-lookup"><span data-stu-id="4638b-154">Specifies the container URLs that are used to store operating system disks for the VMSS.</span></span>

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

### <span data-ttu-id="4638b-155">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="4638b-155">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="4638b-156">Указывает объект VMSS.</span><span class="sxs-lookup"><span data-stu-id="4638b-156">Specifies the VMSS object.</span></span>
<span data-ttu-id="4638b-157">Чтобы получить объект, используйте объект New-AzureRmVmssConfig.</span><span class="sxs-lookup"><span data-stu-id="4638b-157">To obtain the object, use the New-AzureRmVmssConfig object.</span></span>

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

### <span data-ttu-id="4638b-158">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4638b-158">-Confirm</span></span>
<span data-ttu-id="4638b-159">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4638b-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4638b-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4638b-160">-WhatIf</span></span>
<span data-ttu-id="4638b-161">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4638b-161">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4638b-162">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4638b-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4638b-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4638b-163">CommonParameters</span></span>
<span data-ttu-id="4638b-164">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4638b-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4638b-165">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4638b-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4638b-166">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4638b-166">INPUTS</span></span>

###  
<span data-ttu-id="4638b-167">Этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="4638b-167">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="4638b-168">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4638b-168">OUTPUTS</span></span>

## <span data-ttu-id="4638b-169">Пуск</span><span class="sxs-lookup"><span data-stu-id="4638b-169">NOTES</span></span>

## <span data-ttu-id="4638b-170">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4638b-170">RELATED LINKS</span></span>

[<span data-ttu-id="4638b-171">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="4638b-171">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="4638b-172">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="4638b-172">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="4638b-173">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="4638b-173">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="4638b-174">New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="4638b-174">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 7EC166C7-151D-4DA0-9B10-165E735D4F12
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVmssExtension.md
ms.openlocfilehash: 97c8824bca395ddd8fb23ebb4750ab35931c5d51
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911582"
---
# <span data-ttu-id="9a34a-101">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="9a34a-101">Add-AzVmssExtension</span></span>

## <span data-ttu-id="9a34a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9a34a-102">SYNOPSIS</span></span>
<span data-ttu-id="9a34a-103">Добавляет расширение в VMSS.</span><span class="sxs-lookup"><span data-stu-id="9a34a-103">Adds an extension to the VMSS.</span></span>

## <span data-ttu-id="9a34a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9a34a-104">SYNTAX</span></span>

```
Add-AzVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [[-Publisher] <String>] [[-Type] <String>] [[-TypeHandlerVersion] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [[-Setting] <Object>] [[-ProtectedSetting] <Object>]
 [-ForceUpdateTag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9a34a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9a34a-105">DESCRIPTION</span></span>
<span data-ttu-id="9a34a-106">Командлет **Add-AzVmssExtension** добавляет расширение в установленный вами масштаб виртуальных машин (VMSS).</span><span class="sxs-lookup"><span data-stu-id="9a34a-106">The **Add-AzVmssExtension** cmdlet adds an extension to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="9a34a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9a34a-107">EXAMPLES</span></span>

### <span data-ttu-id="9a34a-108">Пример 1: Добавление расширения для VMSS</span><span class="sxs-lookup"><span data-stu-id="9a34a-108">Example 1: Add an extension to the VMSS</span></span>
```
PS C:\> Add-AzVmssExtension -VirtualMachineScaleSet $VMSS -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True
```

<span data-ttu-id="9a34a-109">Эта команда добавляет расширение в VMMS.</span><span class="sxs-lookup"><span data-stu-id="9a34a-109">This command adds an extension to the VMMS.</span></span>

## <span data-ttu-id="9a34a-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9a34a-110">PARAMETERS</span></span>

### <span data-ttu-id="9a34a-111">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="9a34a-111">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="9a34a-112">Указывает, следует ли автоматически обновлять версию расширения до более поздней дополнительной версии.</span><span class="sxs-lookup"><span data-stu-id="9a34a-112">Indicates whether the extension version should be automatically updated to a newer minor version.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a34a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a34a-113">-DefaultProfile</span></span>
<span data-ttu-id="9a34a-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9a34a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9a34a-115">-ForceUpdateTag</span><span class="sxs-lookup"><span data-stu-id="9a34a-115">-ForceUpdateTag</span></span>
<span data-ttu-id="9a34a-116">Если задано значение, которое отличается от предыдущего значения, обработчик расширений будет принудительно обновляться даже в том случае, если конфигурация расширения не изменилась.</span><span class="sxs-lookup"><span data-stu-id="9a34a-116">If a value is provided and is different from the previous value, the extension handler will be forced to update even if the extension configuration has not changed.</span></span>

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

### <span data-ttu-id="9a34a-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9a34a-117">-Name</span></span>
<span data-ttu-id="9a34a-118">Указывает имя расширения, которое добавляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="9a34a-118">Specifies the name of the extension that this cmdlet adds.</span></span>

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

### <span data-ttu-id="9a34a-119">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="9a34a-119">-ProtectedSetting</span></span>
<span data-ttu-id="9a34a-120">Задает частную конфигурацию для расширения в виде строки.</span><span class="sxs-lookup"><span data-stu-id="9a34a-120">Specifies private configuration for the extension, as a string.</span></span>
<span data-ttu-id="9a34a-121">Этот командлет шифрует закрытую конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="9a34a-121">This cmdlet encrypts the private configuration.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a34a-122">-Publisher</span><span class="sxs-lookup"><span data-stu-id="9a34a-122">-Publisher</span></span>
<span data-ttu-id="9a34a-123">Указывает имя издателя расширений.</span><span class="sxs-lookup"><span data-stu-id="9a34a-123">Specifies the name of the extension publisher.</span></span>
<span data-ttu-id="9a34a-124">Издатель предоставляет имя, когда Publisher регистрирует расширение.</span><span class="sxs-lookup"><span data-stu-id="9a34a-124">The publisher provides a name when the publisher registers an extension.</span></span>
<span data-ttu-id="9a34a-125">Это может использовать командлет [Get-AzVMImagePublisher](./Get-AzVMImagePublisher.md) для получения издателя.</span><span class="sxs-lookup"><span data-stu-id="9a34a-125">This can use the [Get-AzVMImagePublisher](./Get-AzVMImagePublisher.md) cmdlet to get the publisher.</span></span>

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

### <span data-ttu-id="9a34a-126">-Параметр</span><span class="sxs-lookup"><span data-stu-id="9a34a-126">-Setting</span></span>
<span data-ttu-id="9a34a-127">Указывает открытую конфигурацию в виде строки для расширения.</span><span class="sxs-lookup"><span data-stu-id="9a34a-127">Specifies the public configuration, as a string, for the extension.</span></span>
<span data-ttu-id="9a34a-128">Этот командлет не шифрует общедоступную конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="9a34a-128">This cmdlet does not encrypt public configuration.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a34a-129">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="9a34a-129">-Type</span></span>
<span data-ttu-id="9a34a-130">Указывает тип расширения.</span><span class="sxs-lookup"><span data-stu-id="9a34a-130">Specifies the extension type.</span></span>
<span data-ttu-id="9a34a-131">Вы можете использовать командлет [Get-AzVMExtensionImageType](./Get-AzVMExtensionImageType.md) , чтобы получить тип расширения.</span><span class="sxs-lookup"><span data-stu-id="9a34a-131">You can use the [Get-AzVMExtensionImageType](./Get-AzVMExtensionImageType.md) cmdlet to get the extension type.</span></span>

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

### <span data-ttu-id="9a34a-132">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="9a34a-132">-TypeHandlerVersion</span></span>
<span data-ttu-id="9a34a-133">Указывает версию расширения, используемую для этой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="9a34a-133">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="9a34a-134">Вы можете использовать командлет [Get-AzVMExtensionImage](./Get-AzVMExtensionImage.md) , чтобы получить версию расширения.</span><span class="sxs-lookup"><span data-stu-id="9a34a-134">You can use the [Get-AzVMExtensionImage](./Get-AzVMExtensionImage.md) cmdlet to get the version of the extension.</span></span>

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

### <span data-ttu-id="9a34a-135">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="9a34a-135">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="9a34a-136">Укажите объект VMSS.</span><span class="sxs-lookup"><span data-stu-id="9a34a-136">Specify the VMSS object.</span></span>
<span data-ttu-id="9a34a-137">Вы можете создать объект с помощью [New-AzVmssConfig](./New-AzVmssConfig.md) .</span><span class="sxs-lookup"><span data-stu-id="9a34a-137">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) to create the object.</span></span>

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

### <span data-ttu-id="9a34a-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9a34a-138">-Confirm</span></span>
<span data-ttu-id="9a34a-139">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9a34a-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a34a-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a34a-140">-WhatIf</span></span>
<span data-ttu-id="9a34a-141">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9a34a-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9a34a-142">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9a34a-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a34a-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a34a-143">CommonParameters</span></span>
<span data-ttu-id="9a34a-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9a34a-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a34a-145">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a34a-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a34a-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9a34a-146">INPUTS</span></span>

### <span data-ttu-id="9a34a-147">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="9a34a-147">VirtualMachineScaleSet</span></span>
<span data-ttu-id="9a34a-148">Параметр "VirtualMachineScaleSet" принимает значение типа "VirtualMachineScaleSet" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="9a34a-148">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="9a34a-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9a34a-149">OUTPUTS</span></span>

###  
<span data-ttu-id="9a34a-150">Этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="9a34a-150">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="9a34a-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="9a34a-151">NOTES</span></span>

## <span data-ttu-id="9a34a-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9a34a-152">RELATED LINKS</span></span>

[<span data-ttu-id="9a34a-153">Remove-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="9a34a-153">Remove-AzVmssExtension</span></span>](./Remove-AzVmssExtension.md)

[<span data-ttu-id="9a34a-154">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="9a34a-154">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="9a34a-155">Get-AzVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="9a34a-155">Get-AzVMExtensionImageType</span></span>](./Get-AzVMExtensionImageType.md)

[<span data-ttu-id="9a34a-156">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="9a34a-156">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)

[<span data-ttu-id="9a34a-157">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="9a34a-157">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)

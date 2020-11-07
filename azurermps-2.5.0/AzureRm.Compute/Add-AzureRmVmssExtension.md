---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7EC166C7-151D-4DA0-9B10-165E735D4F12
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmssextension
schema: 2.0.0
ms.openlocfilehash: f69b8901b2bc2c07bdf158da4c92deba0330109d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913397"
---
# <span data-ttu-id="bcf1e-101">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="bcf1e-101">Add-AzureRmVmssExtension</span></span>

## <span data-ttu-id="bcf1e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bcf1e-102">SYNOPSIS</span></span>
<span data-ttu-id="bcf1e-103">Добавляет расширение в VMSS.</span><span class="sxs-lookup"><span data-stu-id="bcf1e-103">Adds an extension to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bcf1e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bcf1e-104">SYNTAX</span></span>

```
Add-AzureRmVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [[-Publisher] <String>] [[-Type] <String>] [[-TypeHandlerVersion] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [[-Setting] <Object>] [[-ProtectedSetting] <Object>]
 [-ForceUpdateTag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bcf1e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bcf1e-105">DESCRIPTION</span></span>
<span data-ttu-id="bcf1e-106">Командлет **Add-AzureRmVmssExtension** добавляет расширение в установленный вами масштаб виртуальных машин (VMSS).</span><span class="sxs-lookup"><span data-stu-id="bcf1e-106">The **Add-AzureRmVmssExtension** cmdlet adds an extension to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="bcf1e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bcf1e-107">EXAMPLES</span></span>

### <span data-ttu-id="bcf1e-108">Пример 1: Добавление расширения для VMSS</span><span class="sxs-lookup"><span data-stu-id="bcf1e-108">Example 1: Add an extension to the VMSS</span></span>
```
PS C:\> Add-AzureRmVmssExtension -VirtualMachineScaleSet $VMSS -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True
```

<span data-ttu-id="bcf1e-109">Эта команда добавляет расширение в VMMS.</span><span class="sxs-lookup"><span data-stu-id="bcf1e-109">This command adds an extension to the VMMS.</span></span>

## <span data-ttu-id="bcf1e-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bcf1e-110">PARAMETERS</span></span>

### <span data-ttu-id="bcf1e-111">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="bcf1e-111">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="bcf1e-112">Указывает, следует ли автоматически обновлять версию расширения до более поздней дополнительной версии.</span><span class="sxs-lookup"><span data-stu-id="bcf1e-112">Indicates whether the extension version should be automatically updated to a newer minor version.</span></span>

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

### <span data-ttu-id="bcf1e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcf1e-113">-DefaultProfile</span></span>
<span data-ttu-id="bcf1e-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bcf1e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bcf1e-115">-ForceUpdateTag</span><span class="sxs-lookup"><span data-stu-id="bcf1e-115">-ForceUpdateTag</span></span>
<span data-ttu-id="bcf1e-116">Если задано значение, которое отличается от предыдущего значения, обработчик расширений будет принудительно обновляться даже в том случае, если конфигурация расширения не изменилась.</span><span class="sxs-lookup"><span data-stu-id="bcf1e-116">If a value is provided and is different from the previous value, the extension handler will be forced to update even if the extension configuration has not changed.</span></span>

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

### <span data-ttu-id="bcf1e-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="bcf1e-117">-Name</span></span>
<span data-ttu-id="bcf1e-118">Указывает имя расширения, которое добавляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="bcf1e-118">Specifies the name of the extension that this cmdlet adds.</span></span>

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

### <span data-ttu-id="bcf1e-119">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="bcf1e-119">-ProtectedSetting</span></span>
<span data-ttu-id="bcf1e-120">Задает частную конфигурацию для расширения в виде строки.</span><span class="sxs-lookup"><span data-stu-id="bcf1e-120">Specifies private configuration for the extension, as a string.</span></span>
<span data-ttu-id="bcf1e-121">Этот командлет шифрует закрытую конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="bcf1e-121">This cmdlet encrypts the private configuration.</span></span>

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

### <span data-ttu-id="bcf1e-122">-Publisher</span><span class="sxs-lookup"><span data-stu-id="bcf1e-122">-Publisher</span></span>
<span data-ttu-id="bcf1e-123">Указывает имя издателя расширений.</span><span class="sxs-lookup"><span data-stu-id="bcf1e-123">Specifies the name of the extension publisher.</span></span>
<span data-ttu-id="bcf1e-124">Издатель предоставляет имя, когда Publisher регистрирует расширение.</span><span class="sxs-lookup"><span data-stu-id="bcf1e-124">The publisher provides a name when the publisher registers an extension.</span></span>
<span data-ttu-id="bcf1e-125">Это может использовать командлет [Get-AzureRmVMImagePublisher](./Get-AzureRmVMImagePublisher.md) для получения издателя.</span><span class="sxs-lookup"><span data-stu-id="bcf1e-125">This can use the [Get-AzureRmVMImagePublisher](./Get-AzureRmVMImagePublisher.md) cmdlet to get the publisher.</span></span>

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

### <span data-ttu-id="bcf1e-126">-Параметр</span><span class="sxs-lookup"><span data-stu-id="bcf1e-126">-Setting</span></span>
<span data-ttu-id="bcf1e-127">Указывает открытую конфигурацию в виде строки для расширения.</span><span class="sxs-lookup"><span data-stu-id="bcf1e-127">Specifies the public configuration, as a string, for the extension.</span></span>
<span data-ttu-id="bcf1e-128">Этот командлет не шифрует общедоступную конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="bcf1e-128">This cmdlet does not encrypt public configuration.</span></span>

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

### <span data-ttu-id="bcf1e-129">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="bcf1e-129">-Type</span></span>
<span data-ttu-id="bcf1e-130">Указывает тип расширения.</span><span class="sxs-lookup"><span data-stu-id="bcf1e-130">Specifies the extension type.</span></span>
<span data-ttu-id="bcf1e-131">Вы можете использовать командлет [Get-AzureRmVMExtensionImageType](./Get-AzureRmVMExtensionImageType.md) , чтобы получить тип расширения.</span><span class="sxs-lookup"><span data-stu-id="bcf1e-131">You can use the [Get-AzureRmVMExtensionImageType](./Get-AzureRmVMExtensionImageType.md) cmdlet to get the extension type.</span></span>

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

### <span data-ttu-id="bcf1e-132">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="bcf1e-132">-TypeHandlerVersion</span></span>
<span data-ttu-id="bcf1e-133">Указывает версию расширения, используемую для этой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="bcf1e-133">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="bcf1e-134">Вы можете использовать командлет [Get-AzureRmVMExtensionImage](./Get-AzureRmVMExtensionImage.md) , чтобы получить версию расширения.</span><span class="sxs-lookup"><span data-stu-id="bcf1e-134">You can use the [Get-AzureRmVMExtensionImage](./Get-AzureRmVMExtensionImage.md) cmdlet to get the version of the extension.</span></span>

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

### <span data-ttu-id="bcf1e-135">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="bcf1e-135">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="bcf1e-136">Укажите объект VMSS.</span><span class="sxs-lookup"><span data-stu-id="bcf1e-136">Specify the VMSS object.</span></span>
<span data-ttu-id="bcf1e-137">Вы можете создать объект с помощью [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) .</span><span class="sxs-lookup"><span data-stu-id="bcf1e-137">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) to create the object.</span></span>

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

### <span data-ttu-id="bcf1e-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bcf1e-138">-Confirm</span></span>
<span data-ttu-id="bcf1e-139">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="bcf1e-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bcf1e-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bcf1e-140">-WhatIf</span></span>
<span data-ttu-id="bcf1e-141">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="bcf1e-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bcf1e-142">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="bcf1e-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bcf1e-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcf1e-143">CommonParameters</span></span>
<span data-ttu-id="bcf1e-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bcf1e-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcf1e-145">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bcf1e-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcf1e-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bcf1e-146">INPUTS</span></span>

### <span data-ttu-id="bcf1e-147">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="bcf1e-147">VirtualMachineScaleSet</span></span>
<span data-ttu-id="bcf1e-148">Параметр "VirtualMachineScaleSet" принимает значение типа "VirtualMachineScaleSet" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="bcf1e-148">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="bcf1e-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bcf1e-149">OUTPUTS</span></span>

###  
<span data-ttu-id="bcf1e-150">Этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="bcf1e-150">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="bcf1e-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="bcf1e-151">NOTES</span></span>

## <span data-ttu-id="bcf1e-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bcf1e-152">RELATED LINKS</span></span>

[<span data-ttu-id="bcf1e-153">Remove-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="bcf1e-153">Remove-AzureRmVmssExtension</span></span>](./Remove-AzureRmVmssExtension.md)

[<span data-ttu-id="bcf1e-154">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="bcf1e-154">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="bcf1e-155">Get-AzureRmVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="bcf1e-155">Get-AzureRmVMExtensionImageType</span></span>](./Get-AzureRmVMExtensionImageType.md)

[<span data-ttu-id="bcf1e-156">Get-AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="bcf1e-156">Get-AzureRmVMExtensionImage</span></span>](./Get-AzureRmVMExtensionImage.md)

[<span data-ttu-id="bcf1e-157">New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="bcf1e-157">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)

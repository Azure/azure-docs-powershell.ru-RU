---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 7EC166C7-151D-4DA0-9B10-165E735D4F12
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssExtension.md
ms.openlocfilehash: 20446fc7c93000b29680689001d9e3c40c4862e5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557576"
---
# <span data-ttu-id="e8134-101">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="e8134-101">Add-AzureRmVmssExtension</span></span>

## <span data-ttu-id="e8134-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e8134-102">SYNOPSIS</span></span>
<span data-ttu-id="e8134-103">Добавляет расширение в VMSS.</span><span class="sxs-lookup"><span data-stu-id="e8134-103">Adds an extension to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e8134-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e8134-104">SYNTAX</span></span>

```
Add-AzureRmVmssExtension [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [[-Name] <String>]
 [[-Publisher] <String>] [[-Type] <String>] [[-TypeHandlerVersion] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [[-Setting] <Object>] [[-ProtectedSetting] <Object>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8134-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e8134-105">DESCRIPTION</span></span>
<span data-ttu-id="e8134-106">Командлет **Add-AzureRmVmssExtension** добавляет расширение в установленный вами масштаб виртуальных машин (VMSS).</span><span class="sxs-lookup"><span data-stu-id="e8134-106">The **Add-AzureRmVmssExtension** cmdlet adds an extension to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="e8134-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e8134-107">EXAMPLES</span></span>

### <span data-ttu-id="e8134-108">Пример 1: Добавление расширения для VMSS</span><span class="sxs-lookup"><span data-stu-id="e8134-108">Example 1: Add an extension to the VMSS</span></span>
```
PS C:\> Add-AzureRmVmssExtension -VirtualMachineScaleSet $VMSS -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True
```

<span data-ttu-id="e8134-109">Эта команда добавляет расширение в VMMS.</span><span class="sxs-lookup"><span data-stu-id="e8134-109">This command adds an extension to the VMMS.</span></span>

## <span data-ttu-id="e8134-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e8134-110">PARAMETERS</span></span>

### <span data-ttu-id="e8134-111">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="e8134-111">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="e8134-112">Указывает, следует ли автоматически обновлять версию расширения до более поздней дополнительной версии.</span><span class="sxs-lookup"><span data-stu-id="e8134-112">Indicates whether the extension version should be automatically updated to a newer minor version.</span></span>

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

### <span data-ttu-id="e8134-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e8134-113">-Name</span></span>
<span data-ttu-id="e8134-114">Указывает имя расширения, которое добавляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="e8134-114">Specifies the name of the extension that this cmdlet adds.</span></span>

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

### <span data-ttu-id="e8134-115">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="e8134-115">-ProtectedSetting</span></span>
<span data-ttu-id="e8134-116">Задает частную конфигурацию для расширения в виде строки.</span><span class="sxs-lookup"><span data-stu-id="e8134-116">Specifies private configuration for the extension, as a string.</span></span>
<span data-ttu-id="e8134-117">Этот командлет шифрует закрытую конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="e8134-117">This cmdlet encrypts the private configuration.</span></span>

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

### <span data-ttu-id="e8134-118">-Publisher</span><span class="sxs-lookup"><span data-stu-id="e8134-118">-Publisher</span></span>
<span data-ttu-id="e8134-119">Указывает имя издателя расширений.</span><span class="sxs-lookup"><span data-stu-id="e8134-119">Specifies the name of the extension publisher.</span></span>
<span data-ttu-id="e8134-120">Издатель предоставляет имя, когда Publisher регистрирует расширение.</span><span class="sxs-lookup"><span data-stu-id="e8134-120">The publisher provides a name when the publisher registers an extension.</span></span>
<span data-ttu-id="e8134-121">Это может использовать командлет [Get-AzureRmVMImagePublisher](./Get-AzureRmVMImagePublisher.md) для получения издателя.</span><span class="sxs-lookup"><span data-stu-id="e8134-121">This can use the [Get-AzureRmVMImagePublisher](./Get-AzureRmVMImagePublisher.md) cmdlet to get the publisher.</span></span>

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

### <span data-ttu-id="e8134-122">-Параметр</span><span class="sxs-lookup"><span data-stu-id="e8134-122">-Setting</span></span>
<span data-ttu-id="e8134-123">Указывает открытую конфигурацию в виде строки для расширения.</span><span class="sxs-lookup"><span data-stu-id="e8134-123">Specifies the public configuration, as a string, for the extension.</span></span>
<span data-ttu-id="e8134-124">Этот командлет не шифрует общедоступную конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="e8134-124">This cmdlet does not encrypt public configuration.</span></span>

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

### <span data-ttu-id="e8134-125">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="e8134-125">-Type</span></span>
<span data-ttu-id="e8134-126">Указывает тип расширения.</span><span class="sxs-lookup"><span data-stu-id="e8134-126">Specifies the extension type.</span></span>
<span data-ttu-id="e8134-127">Вы можете использовать командлет [Get-AzureRmVMExtensionImageType](./Get-AzureRmVMExtensionImageType.md) , чтобы получить тип расширения.</span><span class="sxs-lookup"><span data-stu-id="e8134-127">You can use the [Get-AzureRmVMExtensionImageType](./Get-AzureRmVMExtensionImageType.md) cmdlet to get the extension type.</span></span>

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

### <span data-ttu-id="e8134-128">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="e8134-128">-TypeHandlerVersion</span></span>
<span data-ttu-id="e8134-129">Указывает версию расширения, используемую для этой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="e8134-129">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="e8134-130">Вы можете использовать командлет [Get-AzureRmVMExtensionImage](./Get-AzureRmVMExtensionImage.md) , чтобы получить версию расширения.</span><span class="sxs-lookup"><span data-stu-id="e8134-130">You can use the [Get-AzureRmVMExtensionImage](./Get-AzureRmVMExtensionImage.md) cmdlet to get the version of the extension.</span></span>

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

### <span data-ttu-id="e8134-131">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="e8134-131">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="e8134-132">Укажите объект VMSS.</span><span class="sxs-lookup"><span data-stu-id="e8134-132">Specify the VMSS object.</span></span>
<span data-ttu-id="e8134-133">Вы можете создать объект с помощью [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) .</span><span class="sxs-lookup"><span data-stu-id="e8134-133">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) to create the object.</span></span>

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

### <span data-ttu-id="e8134-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e8134-134">-Confirm</span></span>
<span data-ttu-id="e8134-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e8134-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8134-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8134-136">-WhatIf</span></span>
<span data-ttu-id="e8134-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e8134-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e8134-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e8134-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8134-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8134-139">CommonParameters</span></span>
<span data-ttu-id="e8134-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e8134-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8134-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8134-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8134-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e8134-142">INPUTS</span></span>

### <span data-ttu-id="e8134-143">Ничего</span><span class="sxs-lookup"><span data-stu-id="e8134-143">None</span></span>
<span data-ttu-id="e8134-144">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="e8134-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e8134-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e8134-145">OUTPUTS</span></span>

###  
<span data-ttu-id="e8134-146">Этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="e8134-146">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="e8134-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="e8134-147">NOTES</span></span>

## <span data-ttu-id="e8134-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e8134-148">RELATED LINKS</span></span>

[<span data-ttu-id="e8134-149">Remove-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="e8134-149">Remove-AzureRmVmssExtension</span></span>](./Remove-AzureRmVmssExtension.md)

[<span data-ttu-id="e8134-150">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="e8134-150">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="e8134-151">Get-AzureRmVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="e8134-151">Get-AzureRmVMExtensionImageType</span></span>](./Get-AzureRmVMExtensionImageType.md)

[<span data-ttu-id="e8134-152">Get-AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="e8134-152">Get-AzureRmVMExtensionImage</span></span>](./Get-AzureRmVMExtensionImage.md)

[<span data-ttu-id="e8134-153">New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="e8134-153">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)

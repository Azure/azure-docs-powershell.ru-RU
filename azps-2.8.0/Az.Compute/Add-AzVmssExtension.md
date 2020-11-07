---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7EC166C7-151D-4DA0-9B10-165E735D4F12
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssExtension.md
ms.openlocfilehash: 7ddfffc33c38960d19fd207e65833aabf8e827aa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93727512"
---
# <span data-ttu-id="b3394-101">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="b3394-101">Add-AzVmssExtension</span></span>

## <span data-ttu-id="b3394-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b3394-102">SYNOPSIS</span></span>
<span data-ttu-id="b3394-103">Добавляет расширение в VMSS.</span><span class="sxs-lookup"><span data-stu-id="b3394-103">Adds an extension to the VMSS.</span></span>

## <span data-ttu-id="b3394-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b3394-104">SYNTAX</span></span>

```
Add-AzVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [[-Publisher] <String>] [[-Type] <String>] [[-TypeHandlerVersion] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [[-Setting] <Object>] [[-ProtectedSetting] <Object>]
 [-ForceUpdateTag <String>] [-ProvisionAfterExtension <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3394-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b3394-105">DESCRIPTION</span></span>
<span data-ttu-id="b3394-106">Командлет **Add-AzVmssExtension** добавляет расширение в установленный вами масштаб виртуальных машин (VMSS).</span><span class="sxs-lookup"><span data-stu-id="b3394-106">The **Add-AzVmssExtension** cmdlet adds an extension to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="b3394-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b3394-107">EXAMPLES</span></span>

### <span data-ttu-id="b3394-108">Пример 1: Добавление расширения для VMSS</span><span class="sxs-lookup"><span data-stu-id="b3394-108">Example 1: Add an extension to the VMSS</span></span>
```
PS C:\> Add-AzVmssExtension -VirtualMachineScaleSet $VMSS -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True
```

<span data-ttu-id="b3394-109">Эта команда добавляет расширение в VMSS.</span><span class="sxs-lookup"><span data-stu-id="b3394-109">This command adds an extension to the VMSS.</span></span>

### <span data-ttu-id="b3394-110">Пример 2: Добавление расширения для VMSS с параметрами и защищенными параметрами</span><span class="sxs-lookup"><span data-stu-id="b3394-110">Example 2: Add an extension to the VMSS with settings and protected settings</span></span>
```
PS C:\> $Settings = @{"fileUris" = "[]"; "commandToExecute" = ""};
PS C:\> $ProtectedSettings = @{"storageAccountName" = $stoname; "storageAccountKey" = $stokey};

PS C:\> Add-AzVmssExtension -VirtualMachineScaleSet $vmss -Name $vmssExtensionName -Publisher $vmssPublisher  `
  -Type $vmssExtensionType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True  `
  -Setting $Settings -ProtectedSetting $ProtectedSettings
```

<span data-ttu-id="b3394-111">Эта команда добавляет расширение для VMSS с образцом скрипта Bash в хранилище BLOB-объектов в параметрах и доступе к данным в защищенных параметрах.</span><span class="sxs-lookup"><span data-stu-id="b3394-111">This command adds an extension to the VMSS with a sample bash script on a blob storage, specify the url of blob storage and executable command in settings and security access in protected settings.</span></span> 

## <span data-ttu-id="b3394-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b3394-112">PARAMETERS</span></span>

### <span data-ttu-id="b3394-113">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="b3394-113">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="b3394-114">Указывает, следует ли автоматически обновлять версию расширения до более поздней дополнительной версии.</span><span class="sxs-lookup"><span data-stu-id="b3394-114">Indicates whether the extension version should be automatically updated to a newer minor version.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3394-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3394-115">-DefaultProfile</span></span>
<span data-ttu-id="b3394-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b3394-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b3394-117">-ForceUpdateTag</span><span class="sxs-lookup"><span data-stu-id="b3394-117">-ForceUpdateTag</span></span>
<span data-ttu-id="b3394-118">Если задано значение, которое отличается от предыдущего значения, обработчик расширений будет принудительно обновляться даже в том случае, если конфигурация расширения не изменилась.</span><span class="sxs-lookup"><span data-stu-id="b3394-118">If a value is provided and is different from the previous value, the extension handler will be forced to update even if the extension configuration has not changed.</span></span>

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

### <span data-ttu-id="b3394-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b3394-119">-Name</span></span>
<span data-ttu-id="b3394-120">Указывает имя расширения, которое добавляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="b3394-120">Specifies the name of the extension that this cmdlet adds.</span></span>

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

### <span data-ttu-id="b3394-121">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="b3394-121">-ProtectedSetting</span></span>
<span data-ttu-id="b3394-122">Задает частную конфигурацию для расширения в виде строки.</span><span class="sxs-lookup"><span data-stu-id="b3394-122">Specifies private configuration for the extension, as a string.</span></span>
<span data-ttu-id="b3394-123">Этот командлет шифрует закрытую конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="b3394-123">This cmdlet encrypts the private configuration.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3394-124">-ProvisionAfterExtension</span><span class="sxs-lookup"><span data-stu-id="b3394-124">-ProvisionAfterExtension</span></span>
<span data-ttu-id="b3394-125">Коллекция имен расширений, после которых необходимо подготовить это расширение.</span><span class="sxs-lookup"><span data-stu-id="b3394-125">Collection of extension names after which this extension needs to be provisioned.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3394-126">-Publisher</span><span class="sxs-lookup"><span data-stu-id="b3394-126">-Publisher</span></span>
<span data-ttu-id="b3394-127">Указывает имя издателя расширений.</span><span class="sxs-lookup"><span data-stu-id="b3394-127">Specifies the name of the extension publisher.</span></span>
<span data-ttu-id="b3394-128">Издатель предоставляет имя, когда Publisher регистрирует расширение.</span><span class="sxs-lookup"><span data-stu-id="b3394-128">The publisher provides a name when the publisher registers an extension.</span></span>
<span data-ttu-id="b3394-129">Это может использовать командлет [Get-AzVMImagePublisher](./Get-AzVMImagePublisher.md) для получения издателя.</span><span class="sxs-lookup"><span data-stu-id="b3394-129">This can use the [Get-AzVMImagePublisher](./Get-AzVMImagePublisher.md) cmdlet to get the publisher.</span></span>

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

### <span data-ttu-id="b3394-130">-Параметр</span><span class="sxs-lookup"><span data-stu-id="b3394-130">-Setting</span></span>
<span data-ttu-id="b3394-131">Указывает открытую конфигурацию в виде строки для расширения.</span><span class="sxs-lookup"><span data-stu-id="b3394-131">Specifies the public configuration, as a string, for the extension.</span></span>
<span data-ttu-id="b3394-132">Этот командлет не шифрует общедоступную конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="b3394-132">This cmdlet does not encrypt public configuration.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3394-133">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="b3394-133">-Type</span></span>
<span data-ttu-id="b3394-134">Указывает тип расширения.</span><span class="sxs-lookup"><span data-stu-id="b3394-134">Specifies the extension type.</span></span>
<span data-ttu-id="b3394-135">Вы можете использовать командлет [Get-AzVMExtensionImageType](./Get-AzVMExtensionImageType.md) , чтобы получить тип расширения.</span><span class="sxs-lookup"><span data-stu-id="b3394-135">You can use the [Get-AzVMExtensionImageType](./Get-AzVMExtensionImageType.md) cmdlet to get the extension type.</span></span>

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

### <span data-ttu-id="b3394-136">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="b3394-136">-TypeHandlerVersion</span></span>
<span data-ttu-id="b3394-137">Указывает версию расширения, используемую для этой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="b3394-137">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="b3394-138">Вы можете использовать командлет [Get-AzVMExtensionImage](./Get-AzVMExtensionImage.md) , чтобы получить версию расширения.</span><span class="sxs-lookup"><span data-stu-id="b3394-138">You can use the [Get-AzVMExtensionImage](./Get-AzVMExtensionImage.md) cmdlet to get the version of the extension.</span></span>

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

### <span data-ttu-id="b3394-139">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="b3394-139">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="b3394-140">Укажите объект VMSS.</span><span class="sxs-lookup"><span data-stu-id="b3394-140">Specify the VMSS object.</span></span>
<span data-ttu-id="b3394-141">Вы можете создать объект с помощью [New-AzVmssConfig](./New-AzVmssConfig.md) .</span><span class="sxs-lookup"><span data-stu-id="b3394-141">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) to create the object.</span></span>

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

### <span data-ttu-id="b3394-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b3394-142">-Confirm</span></span>
<span data-ttu-id="b3394-143">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b3394-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3394-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3394-144">-WhatIf</span></span>
<span data-ttu-id="b3394-145">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b3394-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b3394-146">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b3394-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3394-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3394-147">CommonParameters</span></span>
<span data-ttu-id="b3394-148">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b3394-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3394-149">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b3394-149">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3394-150">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b3394-150">INPUTS</span></span>

### <span data-ttu-id="b3394-151">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="b3394-151">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="b3394-152">System. String</span><span class="sxs-lookup"><span data-stu-id="b3394-152">System.String</span></span>

### <span data-ttu-id="b3394-153">System. Nullable "1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="b3394-153">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="b3394-154">System. Object</span><span class="sxs-lookup"><span data-stu-id="b3394-154">System.Object</span></span>

## <span data-ttu-id="b3394-155">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b3394-155">OUTPUTS</span></span>

### <span data-ttu-id="b3394-156">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="b3394-156">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="b3394-157">Пуск</span><span class="sxs-lookup"><span data-stu-id="b3394-157">NOTES</span></span>

## <span data-ttu-id="b3394-158">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b3394-158">RELATED LINKS</span></span>

[<span data-ttu-id="b3394-159">Remove-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="b3394-159">Remove-AzVmssExtension</span></span>](./Remove-AzVmssExtension.md)

[<span data-ttu-id="b3394-160">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="b3394-160">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="b3394-161">Get-AzVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="b3394-161">Get-AzVMExtensionImageType</span></span>](./Get-AzVMExtensionImageType.md)

[<span data-ttu-id="b3394-162">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="b3394-162">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)

[<span data-ttu-id="b3394-163">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="b3394-163">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)

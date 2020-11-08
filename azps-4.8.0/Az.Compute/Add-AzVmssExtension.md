---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7EC166C7-151D-4DA0-9B10-165E735D4F12
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssExtension.md
ms.openlocfilehash: 87ea9af1980948f28477a9f483b3c6429df98d12
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94242892"
---
# <span data-ttu-id="a69d4-101">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="a69d4-101">Add-AzVmssExtension</span></span>

## <span data-ttu-id="a69d4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a69d4-102">SYNOPSIS</span></span>
<span data-ttu-id="a69d4-103">Добавляет расширение в VMSS.</span><span class="sxs-lookup"><span data-stu-id="a69d4-103">Adds an extension to the VMSS.</span></span>

## <span data-ttu-id="a69d4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a69d4-104">SYNTAX</span></span>

```
Add-AzVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [[-Publisher] <String>] [[-Type] <String>] [[-TypeHandlerVersion] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [[-Setting] <Object>] [[-ProtectedSetting] <Object>]
 [-ForceUpdateTag <String>] [-ProvisionAfterExtension <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a69d4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a69d4-105">DESCRIPTION</span></span>
<span data-ttu-id="a69d4-106">Командлет **Add-AzVmssExtension** добавляет расширение в установленный вами масштаб виртуальных машин (VMSS).</span><span class="sxs-lookup"><span data-stu-id="a69d4-106">The **Add-AzVmssExtension** cmdlet adds an extension to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="a69d4-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a69d4-107">EXAMPLES</span></span>

### <span data-ttu-id="a69d4-108">Пример 1: Добавление расширения для VMSS</span><span class="sxs-lookup"><span data-stu-id="a69d4-108">Example 1: Add an extension to the VMSS</span></span>
```
PS C:\> Add-AzVmssExtension -VirtualMachineScaleSet $VMSS -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True
```

<span data-ttu-id="a69d4-109">Эта команда добавляет расширение в VMSS.</span><span class="sxs-lookup"><span data-stu-id="a69d4-109">This command adds an extension to the VMSS.</span></span>

### <span data-ttu-id="a69d4-110">Пример 2: Добавление расширения для VMSS с параметрами и защищенными параметрами</span><span class="sxs-lookup"><span data-stu-id="a69d4-110">Example 2: Add an extension to the VMSS with settings and protected settings</span></span>
```
PS C:\> $Settings = @{"fileUris" = "[]"; "commandToExecute" = ""};
PS C:\> $ProtectedSettings = @{"storageAccountName" = $stoname; "storageAccountKey" = $stokey};

PS C:\> Add-AzVmssExtension -VirtualMachineScaleSet $vmss -Name $vmssExtensionName -Publisher $vmssPublisher  `
  -Type $vmssExtensionType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True  `
  -Setting $Settings -ProtectedSetting $ProtectedSettings
```

<span data-ttu-id="a69d4-111">Эта команда добавляет расширение для VMSS с образцом скрипта Bash в хранилище BLOB-объектов в параметрах и доступе к данным в защищенных параметрах.</span><span class="sxs-lookup"><span data-stu-id="a69d4-111">This command adds an extension to the VMSS with a sample bash script on a blob storage, specify the url of blob storage and executable command in settings and security access in protected settings.</span></span> 

## <span data-ttu-id="a69d4-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a69d4-112">PARAMETERS</span></span>

### <span data-ttu-id="a69d4-113">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="a69d4-113">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="a69d4-114">Указывает, следует ли автоматически обновлять версию расширения до более поздней дополнительной версии.</span><span class="sxs-lookup"><span data-stu-id="a69d4-114">Indicates whether the extension version should be automatically updated to a newer minor version.</span></span>

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

### <span data-ttu-id="a69d4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a69d4-115">-DefaultProfile</span></span>
<span data-ttu-id="a69d4-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a69d4-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a69d4-117">-ForceUpdateTag</span><span class="sxs-lookup"><span data-stu-id="a69d4-117">-ForceUpdateTag</span></span>
<span data-ttu-id="a69d4-118">Если задано значение, которое отличается от предыдущего значения, обработчик расширений будет принудительно обновляться даже в том случае, если конфигурация расширения не изменилась.</span><span class="sxs-lookup"><span data-stu-id="a69d4-118">If a value is provided and is different from the previous value, the extension handler will be forced to update even if the extension configuration has not changed.</span></span>

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

### <span data-ttu-id="a69d4-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a69d4-119">-Name</span></span>
<span data-ttu-id="a69d4-120">Указывает имя расширения, которое добавляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="a69d4-120">Specifies the name of the extension that this cmdlet adds.</span></span>

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

### <span data-ttu-id="a69d4-121">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="a69d4-121">-ProtectedSetting</span></span>
<span data-ttu-id="a69d4-122">Задает частную конфигурацию для расширения в виде строки.</span><span class="sxs-lookup"><span data-stu-id="a69d4-122">Specifies private configuration for the extension, as a string.</span></span>
<span data-ttu-id="a69d4-123">Этот командлет шифрует закрытую конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="a69d4-123">This cmdlet encrypts the private configuration.</span></span>

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

### <span data-ttu-id="a69d4-124">-ProvisionAfterExtension</span><span class="sxs-lookup"><span data-stu-id="a69d4-124">-ProvisionAfterExtension</span></span>
<span data-ttu-id="a69d4-125">Коллекция имен расширений, после которых необходимо подготовить это расширение.</span><span class="sxs-lookup"><span data-stu-id="a69d4-125">Collection of extension names after which this extension needs to be provisioned.</span></span>

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

### <span data-ttu-id="a69d4-126">-Publisher</span><span class="sxs-lookup"><span data-stu-id="a69d4-126">-Publisher</span></span>
<span data-ttu-id="a69d4-127">Указывает имя издателя расширений.</span><span class="sxs-lookup"><span data-stu-id="a69d4-127">Specifies the name of the extension publisher.</span></span>
<span data-ttu-id="a69d4-128">Издатель предоставляет имя, когда Publisher регистрирует расширение.</span><span class="sxs-lookup"><span data-stu-id="a69d4-128">The publisher provides a name when the publisher registers an extension.</span></span>
<span data-ttu-id="a69d4-129">Это может использовать командлет [Get-AzVMImagePublisher](./Get-AzVMImagePublisher.md) для получения издателя.</span><span class="sxs-lookup"><span data-stu-id="a69d4-129">This can use the [Get-AzVMImagePublisher](./Get-AzVMImagePublisher.md) cmdlet to get the publisher.</span></span>

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

### <span data-ttu-id="a69d4-130">-Параметр</span><span class="sxs-lookup"><span data-stu-id="a69d4-130">-Setting</span></span>
<span data-ttu-id="a69d4-131">Указывает открытую конфигурацию в виде строки для расширения.</span><span class="sxs-lookup"><span data-stu-id="a69d4-131">Specifies the public configuration, as a string, for the extension.</span></span>
<span data-ttu-id="a69d4-132">Этот командлет не шифрует общедоступную конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="a69d4-132">This cmdlet does not encrypt public configuration.</span></span>

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

### <span data-ttu-id="a69d4-133">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="a69d4-133">-Type</span></span>
<span data-ttu-id="a69d4-134">Указывает тип расширения.</span><span class="sxs-lookup"><span data-stu-id="a69d4-134">Specifies the extension type.</span></span>
<span data-ttu-id="a69d4-135">Вы можете использовать командлет [Get-AzVMExtensionImageType](./Get-AzVMExtensionImageType.md) , чтобы получить тип расширения.</span><span class="sxs-lookup"><span data-stu-id="a69d4-135">You can use the [Get-AzVMExtensionImageType](./Get-AzVMExtensionImageType.md) cmdlet to get the extension type.</span></span>

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

### <span data-ttu-id="a69d4-136">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="a69d4-136">-TypeHandlerVersion</span></span>
<span data-ttu-id="a69d4-137">Указывает версию расширения, используемую для этой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="a69d4-137">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="a69d4-138">Вы можете использовать командлет [Get-AzVMExtensionImage](./Get-AzVMExtensionImage.md) , чтобы получить версию расширения.</span><span class="sxs-lookup"><span data-stu-id="a69d4-138">You can use the [Get-AzVMExtensionImage](./Get-AzVMExtensionImage.md) cmdlet to get the version of the extension.</span></span>

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

### <span data-ttu-id="a69d4-139">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="a69d4-139">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="a69d4-140">Укажите объект VMSS.</span><span class="sxs-lookup"><span data-stu-id="a69d4-140">Specify the VMSS object.</span></span>
<span data-ttu-id="a69d4-141">Вы можете создать объект с помощью [New-AzVmssConfig](./New-AzVmssConfig.md) .</span><span class="sxs-lookup"><span data-stu-id="a69d4-141">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) to create the object.</span></span>

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

### <span data-ttu-id="a69d4-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a69d4-142">-Confirm</span></span>
<span data-ttu-id="a69d4-143">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a69d4-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a69d4-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a69d4-144">-WhatIf</span></span>
<span data-ttu-id="a69d4-145">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a69d4-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a69d4-146">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a69d4-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a69d4-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a69d4-147">CommonParameters</span></span>
<span data-ttu-id="a69d4-148">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a69d4-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a69d4-149">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a69d4-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a69d4-150">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a69d4-150">INPUTS</span></span>

### <span data-ttu-id="a69d4-151">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="a69d4-151">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="a69d4-152">System. String</span><span class="sxs-lookup"><span data-stu-id="a69d4-152">System.String</span></span>

### <span data-ttu-id="a69d4-153">System. Nullable "1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="a69d4-153">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="a69d4-154">System. Object</span><span class="sxs-lookup"><span data-stu-id="a69d4-154">System.Object</span></span>

## <span data-ttu-id="a69d4-155">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a69d4-155">OUTPUTS</span></span>

### <span data-ttu-id="a69d4-156">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="a69d4-156">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="a69d4-157">Пуск</span><span class="sxs-lookup"><span data-stu-id="a69d4-157">NOTES</span></span>

## <span data-ttu-id="a69d4-158">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a69d4-158">RELATED LINKS</span></span>

[<span data-ttu-id="a69d4-159">Remove-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="a69d4-159">Remove-AzVmssExtension</span></span>](./Remove-AzVmssExtension.md)

[<span data-ttu-id="a69d4-160">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="a69d4-160">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="a69d4-161">Get-AzVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="a69d4-161">Get-AzVMExtensionImageType</span></span>](./Get-AzVMExtensionImageType.md)

[<span data-ttu-id="a69d4-162">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="a69d4-162">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)

[<span data-ttu-id="a69d4-163">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="a69d4-163">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7EC166C7-151D-4DA0-9B10-165E735D4F12
online version: https://docs.microsoft.com/powershell/module/az.compute/add-azvmssextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssExtension.md
ms.openlocfilehash: 774fb61f2394c5634c8415a7a18ce63f4e696a3f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991553"
---
# <span data-ttu-id="d64a4-101">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="d64a4-101">Add-AzVmssExtension</span></span>

## <span data-ttu-id="d64a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d64a4-102">SYNOPSIS</span></span>
<span data-ttu-id="d64a4-103">Добавляет расширение к VMSS.</span><span class="sxs-lookup"><span data-stu-id="d64a4-103">Adds an extension to the VMSS.</span></span>

## <span data-ttu-id="d64a4-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d64a4-104">SYNTAX</span></span>

```
Add-AzVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [[-Publisher] <String>] [[-Type] <String>] [[-TypeHandlerVersion] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [[-Setting] <Object>] [[-ProtectedSetting] <Object>]
 [-EnableAutomaticUpgrade <Boolean>] [-ForceUpdateTag <String>] [-ProvisionAfterExtension <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d64a4-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d64a4-105">DESCRIPTION</span></span>
<span data-ttu-id="d64a4-106">**Cmdlet Add-AzVmssExtension** добавляет расширение к набору масштаба виртуальной машины (VMSS).</span><span class="sxs-lookup"><span data-stu-id="d64a4-106">The **Add-AzVmssExtension** cmdlet adds an extension to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="d64a4-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d64a4-107">EXAMPLES</span></span>

### <span data-ttu-id="d64a4-108">Пример 1. Добавление расширения к VMSS</span><span class="sxs-lookup"><span data-stu-id="d64a4-108">Example 1: Add an extension to the VMSS</span></span>
```
PS C:\> Add-AzVmssExtension -VirtualMachineScaleSet $VMSS -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True
```

<span data-ttu-id="d64a4-109">Эта команда добавляет расширение к VMSS.</span><span class="sxs-lookup"><span data-stu-id="d64a4-109">This command adds an extension to the VMSS.</span></span>

### <span data-ttu-id="d64a4-110">Пример 2. Добавление расширения к VMSS с настройками и защищенными настройками</span><span class="sxs-lookup"><span data-stu-id="d64a4-110">Example 2: Add an extension to the VMSS with settings and protected settings</span></span>
```
PS C:\> $Settings = @{"fileUris" = "[]"; "commandToExecute" = ""};
PS C:\> $ProtectedSettings = @{"storageAccountName" = $stoname; "storageAccountKey" = $stokey};

PS C:\> Add-AzVmssExtension -VirtualMachineScaleSet $vmss -Name $vmssExtensionName -Publisher $vmssPublisher  `
  -Type $vmssExtensionType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True  `
  -Setting $Settings -ProtectedSetting $ProtectedSettings
```

<span data-ttu-id="d64a4-111">Эта команда добавляет расширение к VMSS с образцом сценария bash для хранилища BLOB-параметров, укажите URL-адрес хранилища BLOB-параметров и исполняемой команды в параметрах и доступе к безопасности в защищенных параметрах.</span><span class="sxs-lookup"><span data-stu-id="d64a4-111">This command adds an extension to the VMSS with a sample bash script on a blob storage, specify the url of blob storage and executable command in settings and security access in protected settings.</span></span> 

## <span data-ttu-id="d64a4-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d64a4-112">PARAMETERS</span></span>

### <span data-ttu-id="d64a4-113">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="d64a4-113">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="d64a4-114">Указывает на то, должна ли версия расширения автоматически обновляться до более новой версии.</span><span class="sxs-lookup"><span data-stu-id="d64a4-114">Indicates whether the extension version should be automatically updated to a newer minor version.</span></span>

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

### <span data-ttu-id="d64a4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d64a4-115">-DefaultProfile</span></span>
<span data-ttu-id="d64a4-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d64a4-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d64a4-117">-EnableAutomaticUpgrade</span><span class="sxs-lookup"><span data-stu-id="d64a4-117">-EnableAutomaticUpgrade</span></span>
<span data-ttu-id="d64a4-118">Указывает на то, должно ли расширение автоматически обновляться платформой при наличии новой версии расширения.</span><span class="sxs-lookup"><span data-stu-id="d64a4-118">Indicates whether the extension should be automatically upgraded by the platform if there is a newer version of the extension available.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d64a4-119">-ForceUpdateTag</span><span class="sxs-lookup"><span data-stu-id="d64a4-119">-ForceUpdateTag</span></span>
<span data-ttu-id="d64a4-120">Если значение предоставляются и отличается от предыдущего, обработник расширения будет принудительно обновляться даже в том случае, если конфигурация расширения не изменилась.</span><span class="sxs-lookup"><span data-stu-id="d64a4-120">If a value is provided and is different from the previous value, the extension handler will be forced to update even if the extension configuration has not changed.</span></span>

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

### <span data-ttu-id="d64a4-121">-Name</span><span class="sxs-lookup"><span data-stu-id="d64a4-121">-Name</span></span>
<span data-ttu-id="d64a4-122">Указывает имя расширения, которое добавляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d64a4-122">Specifies the name of the extension that this cmdlet adds.</span></span>

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

### <span data-ttu-id="d64a4-123">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="d64a4-123">-ProtectedSetting</span></span>
<span data-ttu-id="d64a4-124">Указывает частную конфигурацию расширения в качестве строки.</span><span class="sxs-lookup"><span data-stu-id="d64a4-124">Specifies private configuration for the extension, as a string.</span></span>
<span data-ttu-id="d64a4-125">Этот cmdlet зашифрует частную конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="d64a4-125">This cmdlet encrypts the private configuration.</span></span>

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

### <span data-ttu-id="d64a4-126">-ProvisionAfterExtension</span><span class="sxs-lookup"><span data-stu-id="d64a4-126">-ProvisionAfterExtension</span></span>
<span data-ttu-id="d64a4-127">Набор имен расширений, после чего их нужно подготовка.</span><span class="sxs-lookup"><span data-stu-id="d64a4-127">Collection of extension names after which this extension needs to be provisioned.</span></span>

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

### <span data-ttu-id="d64a4-128">-Publisher</span><span class="sxs-lookup"><span data-stu-id="d64a4-128">-Publisher</span></span>
<span data-ttu-id="d64a4-129">Указывает имя издателя расширения.</span><span class="sxs-lookup"><span data-stu-id="d64a4-129">Specifies the name of the extension publisher.</span></span>
<span data-ttu-id="d64a4-130">Издатель предоставляет имя при регистрации расширения.</span><span class="sxs-lookup"><span data-stu-id="d64a4-130">The publisher provides a name when the publisher registers an extension.</span></span>
<span data-ttu-id="d64a4-131">Для получения издателя можно использовать [cmdlet Get-AzVMImagePublisher.](./Get-AzVMImagePublisher.md)</span><span class="sxs-lookup"><span data-stu-id="d64a4-131">This can use the [Get-AzVMImagePublisher](./Get-AzVMImagePublisher.md) cmdlet to get the publisher.</span></span>

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

### <span data-ttu-id="d64a4-132">-Setting</span><span class="sxs-lookup"><span data-stu-id="d64a4-132">-Setting</span></span>
<span data-ttu-id="d64a4-133">Указывает об общедоступных конфигурациях в качестве строки для расширения.</span><span class="sxs-lookup"><span data-stu-id="d64a4-133">Specifies the public configuration, as a string, for the extension.</span></span>
<span data-ttu-id="d64a4-134">Этот cmdlet не шифрует общедоступные конфигурации.</span><span class="sxs-lookup"><span data-stu-id="d64a4-134">This cmdlet does not encrypt public configuration.</span></span>

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

### <span data-ttu-id="d64a4-135">-Type</span><span class="sxs-lookup"><span data-stu-id="d64a4-135">-Type</span></span>
<span data-ttu-id="d64a4-136">Тип расширения.</span><span class="sxs-lookup"><span data-stu-id="d64a4-136">Specifies the extension type.</span></span>
<span data-ttu-id="d64a4-137">Для получения типа расширения можно использовать cmdlet [Get-AzVMExtensionImageType.](./Get-AzVMExtensionImageType.md)</span><span class="sxs-lookup"><span data-stu-id="d64a4-137">You can use the [Get-AzVMExtensionImageType](./Get-AzVMExtensionImageType.md) cmdlet to get the extension type.</span></span>

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

### <span data-ttu-id="d64a4-138">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="d64a4-138">-TypeHandlerVersion</span></span>
<span data-ttu-id="d64a4-139">Определяет версию расширения, используемого для этой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d64a4-139">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="d64a4-140">Чтобы получить версию расширения, можно использовать cmdlet [Get-AzVMExtensionImage.](./Get-AzVMExtensionImage.md)</span><span class="sxs-lookup"><span data-stu-id="d64a4-140">You can use the [Get-AzVMExtensionImage](./Get-AzVMExtensionImage.md) cmdlet to get the version of the extension.</span></span>

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

### <span data-ttu-id="d64a4-141">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="d64a4-141">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="d64a4-142">Укажите объект VMSS.</span><span class="sxs-lookup"><span data-stu-id="d64a4-142">Specify the VMSS object.</span></span>
<span data-ttu-id="d64a4-143">Создать объект можно с помощью [new-AzVmssConfig.](./New-AzVmssConfig.md)</span><span class="sxs-lookup"><span data-stu-id="d64a4-143">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) to create the object.</span></span>

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

### <span data-ttu-id="d64a4-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d64a4-144">-Confirm</span></span>
<span data-ttu-id="d64a4-145">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="d64a4-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d64a4-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d64a4-146">-WhatIf</span></span>
<span data-ttu-id="d64a4-147">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d64a4-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d64a4-148">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d64a4-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d64a4-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d64a4-149">CommonParameters</span></span>
<span data-ttu-id="d64a4-150">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d64a4-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d64a4-151">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d64a4-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d64a4-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d64a4-152">INPUTS</span></span>

### <span data-ttu-id="d64a4-153">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMa modelseScaleSet</span><span class="sxs-lookup"><span data-stu-id="d64a4-153">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="d64a4-154">System.String</span><span class="sxs-lookup"><span data-stu-id="d64a4-154">System.String</span></span>

### <span data-ttu-id="d64a4-155">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="d64a4-155">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="d64a4-156">System.Object</span><span class="sxs-lookup"><span data-stu-id="d64a4-156">System.Object</span></span>

## <span data-ttu-id="d64a4-157">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d64a4-157">OUTPUTS</span></span>

### <span data-ttu-id="d64a4-158">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMa modelseScaleSet</span><span class="sxs-lookup"><span data-stu-id="d64a4-158">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="d64a4-159">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d64a4-159">NOTES</span></span>

## <span data-ttu-id="d64a4-160">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d64a4-160">RELATED LINKS</span></span>

[<span data-ttu-id="d64a4-161">Remove-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="d64a4-161">Remove-AzVmssExtension</span></span>](./Remove-AzVmssExtension.md)

[<span data-ttu-id="d64a4-162">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="d64a4-162">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="d64a4-163">Get-AzVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="d64a4-163">Get-AzVMExtensionImageType</span></span>](./Get-AzVMExtensionImageType.md)

[<span data-ttu-id="d64a4-164">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="d64a4-164">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)

[<span data-ttu-id="d64a4-165">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="d64a4-165">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)

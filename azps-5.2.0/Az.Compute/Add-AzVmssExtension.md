---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7EC166C7-151D-4DA0-9B10-165E735D4F12
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssExtension.md
ms.openlocfilehash: 87ea9af1980948f28477a9f483b3c6429df98d12
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98416935"
---
# <span data-ttu-id="08c38-101">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="08c38-101">Add-AzVmssExtension</span></span>

## <span data-ttu-id="08c38-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="08c38-102">SYNOPSIS</span></span>
<span data-ttu-id="08c38-103">Добавляет расширение к VMSS.</span><span class="sxs-lookup"><span data-stu-id="08c38-103">Adds an extension to the VMSS.</span></span>

## <span data-ttu-id="08c38-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="08c38-104">SYNTAX</span></span>

```
Add-AzVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [[-Publisher] <String>] [[-Type] <String>] [[-TypeHandlerVersion] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [[-Setting] <Object>] [[-ProtectedSetting] <Object>]
 [-ForceUpdateTag <String>] [-ProvisionAfterExtension <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="08c38-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="08c38-105">DESCRIPTION</span></span>
<span data-ttu-id="08c38-106">**Cmdlet Add-AzVmssExtension** добавляет расширение к набору масштаба виртуальной машины (VMSS).</span><span class="sxs-lookup"><span data-stu-id="08c38-106">The **Add-AzVmssExtension** cmdlet adds an extension to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="08c38-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="08c38-107">EXAMPLES</span></span>

### <span data-ttu-id="08c38-108">Пример 1. Добавление расширения к VMSS</span><span class="sxs-lookup"><span data-stu-id="08c38-108">Example 1: Add an extension to the VMSS</span></span>
```
PS C:\> Add-AzVmssExtension -VirtualMachineScaleSet $VMSS -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True
```

<span data-ttu-id="08c38-109">Эта команда добавляет расширение к VMSS.</span><span class="sxs-lookup"><span data-stu-id="08c38-109">This command adds an extension to the VMSS.</span></span>

### <span data-ttu-id="08c38-110">Пример 2. Добавление расширения к VMSS с настройками и защищенными настройками</span><span class="sxs-lookup"><span data-stu-id="08c38-110">Example 2: Add an extension to the VMSS with settings and protected settings</span></span>
```
PS C:\> $Settings = @{"fileUris" = "[]"; "commandToExecute" = ""};
PS C:\> $ProtectedSettings = @{"storageAccountName" = $stoname; "storageAccountKey" = $stokey};

PS C:\> Add-AzVmssExtension -VirtualMachineScaleSet $vmss -Name $vmssExtensionName -Publisher $vmssPublisher  `
  -Type $vmssExtensionType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True  `
  -Setting $Settings -ProtectedSetting $ProtectedSettings
```

<span data-ttu-id="08c38-111">Эта команда добавляет расширение к VMSS с образцом сценария bash для хранилища BLOB-параметров, укажите URL-адрес хранилища BLOB-параметров и исполняемой команды в параметрах и доступе к безопасности в защищенных параметрах.</span><span class="sxs-lookup"><span data-stu-id="08c38-111">This command adds an extension to the VMSS with a sample bash script on a blob storage, specify the url of blob storage and executable command in settings and security access in protected settings.</span></span> 

## <span data-ttu-id="08c38-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="08c38-112">PARAMETERS</span></span>

### <span data-ttu-id="08c38-113">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="08c38-113">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="08c38-114">Указывает на то, должна ли версия расширения автоматически обновляться до более новой версии.</span><span class="sxs-lookup"><span data-stu-id="08c38-114">Indicates whether the extension version should be automatically updated to a newer minor version.</span></span>

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

### <span data-ttu-id="08c38-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08c38-115">-DefaultProfile</span></span>
<span data-ttu-id="08c38-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="08c38-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="08c38-117">-ForceUpdateTag</span><span class="sxs-lookup"><span data-stu-id="08c38-117">-ForceUpdateTag</span></span>
<span data-ttu-id="08c38-118">Если значение предоставляются и отличается от предыдущего, обработник расширения будет принудительно обновляться даже в том случае, если конфигурация расширения не изменилась.</span><span class="sxs-lookup"><span data-stu-id="08c38-118">If a value is provided and is different from the previous value, the extension handler will be forced to update even if the extension configuration has not changed.</span></span>

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

### <span data-ttu-id="08c38-119">-Name</span><span class="sxs-lookup"><span data-stu-id="08c38-119">-Name</span></span>
<span data-ttu-id="08c38-120">Указывает имя расширения, которое добавляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="08c38-120">Specifies the name of the extension that this cmdlet adds.</span></span>

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

### <span data-ttu-id="08c38-121">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="08c38-121">-ProtectedSetting</span></span>
<span data-ttu-id="08c38-122">Указывает частную конфигурацию расширения в качестве строки.</span><span class="sxs-lookup"><span data-stu-id="08c38-122">Specifies private configuration for the extension, as a string.</span></span>
<span data-ttu-id="08c38-123">Этот cmdlet зашифрует частную конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="08c38-123">This cmdlet encrypts the private configuration.</span></span>

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

### <span data-ttu-id="08c38-124">-ProvisionAfterExtension</span><span class="sxs-lookup"><span data-stu-id="08c38-124">-ProvisionAfterExtension</span></span>
<span data-ttu-id="08c38-125">Набор имен расширений, после чего их нужно будет использовать.</span><span class="sxs-lookup"><span data-stu-id="08c38-125">Collection of extension names after which this extension needs to be provisioned.</span></span>

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

### <span data-ttu-id="08c38-126">-Publisher</span><span class="sxs-lookup"><span data-stu-id="08c38-126">-Publisher</span></span>
<span data-ttu-id="08c38-127">Указывает имя издателя расширения.</span><span class="sxs-lookup"><span data-stu-id="08c38-127">Specifies the name of the extension publisher.</span></span>
<span data-ttu-id="08c38-128">Издатель предоставляет имя при регистрации расширения.</span><span class="sxs-lookup"><span data-stu-id="08c38-128">The publisher provides a name when the publisher registers an extension.</span></span>
<span data-ttu-id="08c38-129">Для этого можно использовать [cmdlet Get-AzVMImagePublisher.](./Get-AzVMImagePublisher.md)</span><span class="sxs-lookup"><span data-stu-id="08c38-129">This can use the [Get-AzVMImagePublisher](./Get-AzVMImagePublisher.md) cmdlet to get the publisher.</span></span>

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

### <span data-ttu-id="08c38-130">-Setting</span><span class="sxs-lookup"><span data-stu-id="08c38-130">-Setting</span></span>
<span data-ttu-id="08c38-131">Указывает об общедоступных конфигурациях в качестве строки для расширения.</span><span class="sxs-lookup"><span data-stu-id="08c38-131">Specifies the public configuration, as a string, for the extension.</span></span>
<span data-ttu-id="08c38-132">Этот cmdlet не шифрует общедоступные конфигурации.</span><span class="sxs-lookup"><span data-stu-id="08c38-132">This cmdlet does not encrypt public configuration.</span></span>

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

### <span data-ttu-id="08c38-133">-Type</span><span class="sxs-lookup"><span data-stu-id="08c38-133">-Type</span></span>
<span data-ttu-id="08c38-134">Тип расширения.</span><span class="sxs-lookup"><span data-stu-id="08c38-134">Specifies the extension type.</span></span>
<span data-ttu-id="08c38-135">Для получения типа расширения можно использовать cmdlet [Get-AzVMExtensionImageType.](./Get-AzVMExtensionImageType.md)</span><span class="sxs-lookup"><span data-stu-id="08c38-135">You can use the [Get-AzVMExtensionImageType](./Get-AzVMExtensionImageType.md) cmdlet to get the extension type.</span></span>

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

### <span data-ttu-id="08c38-136">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="08c38-136">-TypeHandlerVersion</span></span>
<span data-ttu-id="08c38-137">Определяет версию расширения, используемого для этой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="08c38-137">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="08c38-138">Чтобы получить версию расширения, можно использовать cmdlet [Get-AzVMExtensionImage.](./Get-AzVMExtensionImage.md)</span><span class="sxs-lookup"><span data-stu-id="08c38-138">You can use the [Get-AzVMExtensionImage](./Get-AzVMExtensionImage.md) cmdlet to get the version of the extension.</span></span>

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

### <span data-ttu-id="08c38-139">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="08c38-139">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="08c38-140">Укажите объект VMSS.</span><span class="sxs-lookup"><span data-stu-id="08c38-140">Specify the VMSS object.</span></span>
<span data-ttu-id="08c38-141">Создать объект можно с помощью [new-AzVmssConfig.](./New-AzVmssConfig.md)</span><span class="sxs-lookup"><span data-stu-id="08c38-141">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) to create the object.</span></span>

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

### <span data-ttu-id="08c38-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="08c38-142">-Confirm</span></span>
<span data-ttu-id="08c38-143">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="08c38-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08c38-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08c38-144">-WhatIf</span></span>
<span data-ttu-id="08c38-145">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="08c38-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="08c38-146">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="08c38-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08c38-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08c38-147">CommonParameters</span></span>
<span data-ttu-id="08c38-148">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08c38-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08c38-149">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="08c38-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08c38-150">INPUTS</span><span class="sxs-lookup"><span data-stu-id="08c38-150">INPUTS</span></span>

### <span data-ttu-id="08c38-151">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMa modelseScaleSet</span><span class="sxs-lookup"><span data-stu-id="08c38-151">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="08c38-152">System.String</span><span class="sxs-lookup"><span data-stu-id="08c38-152">System.String</span></span>

### <span data-ttu-id="08c38-153">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="08c38-153">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="08c38-154">System.Object</span><span class="sxs-lookup"><span data-stu-id="08c38-154">System.Object</span></span>

## <span data-ttu-id="08c38-155">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="08c38-155">OUTPUTS</span></span>

### <span data-ttu-id="08c38-156">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMa modelseScaleSet</span><span class="sxs-lookup"><span data-stu-id="08c38-156">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="08c38-157">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="08c38-157">NOTES</span></span>

## <span data-ttu-id="08c38-158">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="08c38-158">RELATED LINKS</span></span>

[<span data-ttu-id="08c38-159">Remove-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="08c38-159">Remove-AzVmssExtension</span></span>](./Remove-AzVmssExtension.md)

[<span data-ttu-id="08c38-160">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="08c38-160">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="08c38-161">Get-AzVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="08c38-161">Get-AzVMExtensionImageType</span></span>](./Get-AzVMExtensionImageType.md)

[<span data-ttu-id="08c38-162">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="08c38-162">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)

[<span data-ttu-id="08c38-163">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="08c38-163">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)

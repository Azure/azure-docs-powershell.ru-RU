---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7EC166C7-151D-4DA0-9B10-165E735D4F12
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmssextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVmssExtension.md
ms.openlocfilehash: ad87e4e556263889de23640abad391ee28d7b397
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566824"
---
# <span data-ttu-id="37489-101">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="37489-101">Add-AzureRmVmssExtension</span></span>

## <span data-ttu-id="37489-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="37489-102">SYNOPSIS</span></span>
<span data-ttu-id="37489-103">Добавляет расширение в VMSS.</span><span class="sxs-lookup"><span data-stu-id="37489-103">Adds an extension to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="37489-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="37489-104">SYNTAX</span></span>

```
Add-AzureRmVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [[-Publisher] <String>] [[-Type] <String>] [[-TypeHandlerVersion] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [[-Setting] <Object>] [[-ProtectedSetting] <Object>]
 [-ForceUpdateTag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="37489-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="37489-105">DESCRIPTION</span></span>
<span data-ttu-id="37489-106">Командлет **Add-AzureRmVmssExtension** добавляет расширение в установленный вами масштаб виртуальных машин (VMSS).</span><span class="sxs-lookup"><span data-stu-id="37489-106">The **Add-AzureRmVmssExtension** cmdlet adds an extension to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="37489-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="37489-107">EXAMPLES</span></span>

### <span data-ttu-id="37489-108">Пример 1: Добавление расширения для VMSS</span><span class="sxs-lookup"><span data-stu-id="37489-108">Example 1: Add an extension to the VMSS</span></span>
```
PS C:\> Add-AzureRmVmssExtension -VirtualMachineScaleSet $VMSS -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True
```

<span data-ttu-id="37489-109">Эта команда добавляет расширение в VMSS.</span><span class="sxs-lookup"><span data-stu-id="37489-109">This command adds an extension to the VMSS.</span></span>

### <span data-ttu-id="37489-110">Пример 2: Добавление расширения для VMSS с параметрами и защищенными параметрами</span><span class="sxs-lookup"><span data-stu-id="37489-110">Example 2: Add an extension to the VMSS with settings and protected settings</span></span>
```
PS C:\> $Settings = @{"fileUris" = "[]"; "commandToExecute" = ""};
PS C:\> $ProtectedSettings = @{"storageAccountName" = $stoname; "storageAccountKey" = $stokey};

PS C:\> Add-AzureRmVmssExtension -VirtualMachineScaleSet $vmss -Name $vmssExtensionName -Publisher $vmssPublisher  `
  -Type $vmssExtensionType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True  `
  -Setting $Settings -ProtectedSetting $ProtectedSettings
```

<span data-ttu-id="37489-111">Эта команда добавляет расширение для VMSS с образцом скрипта Bash в хранилище BLOB-объектов в параметрах и доступе к данным в защищенных параметрах.</span><span class="sxs-lookup"><span data-stu-id="37489-111">This command adds an extension to the VMSS with a sample bash script on a blob storage, specify the url of blob storage and executable command in settings and security access in protected settings.</span></span> 

## <span data-ttu-id="37489-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="37489-112">PARAMETERS</span></span>

### <span data-ttu-id="37489-113">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="37489-113">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="37489-114">Указывает, следует ли автоматически обновлять версию расширения до более поздней дополнительной версии.</span><span class="sxs-lookup"><span data-stu-id="37489-114">Indicates whether the extension version should be automatically updated to a newer minor version.</span></span>

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

### <span data-ttu-id="37489-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37489-115">-DefaultProfile</span></span>
<span data-ttu-id="37489-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="37489-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="37489-117">-ForceUpdateTag</span><span class="sxs-lookup"><span data-stu-id="37489-117">-ForceUpdateTag</span></span>
<span data-ttu-id="37489-118">Если задано значение, которое отличается от предыдущего значения, обработчик расширений будет принудительно обновляться даже в том случае, если конфигурация расширения не изменилась.</span><span class="sxs-lookup"><span data-stu-id="37489-118">If a value is provided and is different from the previous value, the extension handler will be forced to update even if the extension configuration has not changed.</span></span>

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

### <span data-ttu-id="37489-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="37489-119">-Name</span></span>
<span data-ttu-id="37489-120">Указывает имя расширения, которое добавляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="37489-120">Specifies the name of the extension that this cmdlet adds.</span></span>

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

### <span data-ttu-id="37489-121">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="37489-121">-ProtectedSetting</span></span>
<span data-ttu-id="37489-122">Задает частную конфигурацию для расширения в виде строки.</span><span class="sxs-lookup"><span data-stu-id="37489-122">Specifies private configuration for the extension, as a string.</span></span>
<span data-ttu-id="37489-123">Этот командлет шифрует закрытую конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="37489-123">This cmdlet encrypts the private configuration.</span></span>

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

### <span data-ttu-id="37489-124">-Publisher</span><span class="sxs-lookup"><span data-stu-id="37489-124">-Publisher</span></span>
<span data-ttu-id="37489-125">Указывает имя издателя расширений.</span><span class="sxs-lookup"><span data-stu-id="37489-125">Specifies the name of the extension publisher.</span></span>
<span data-ttu-id="37489-126">Издатель предоставляет имя, когда Publisher регистрирует расширение.</span><span class="sxs-lookup"><span data-stu-id="37489-126">The publisher provides a name when the publisher registers an extension.</span></span>
<span data-ttu-id="37489-127">Это может использовать командлет [Get-AzureRmVMImagePublisher](./Get-AzureRmVMImagePublisher.md) для получения издателя.</span><span class="sxs-lookup"><span data-stu-id="37489-127">This can use the [Get-AzureRmVMImagePublisher](./Get-AzureRmVMImagePublisher.md) cmdlet to get the publisher.</span></span>

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

### <span data-ttu-id="37489-128">-Параметр</span><span class="sxs-lookup"><span data-stu-id="37489-128">-Setting</span></span>
<span data-ttu-id="37489-129">Указывает открытую конфигурацию в виде строки для расширения.</span><span class="sxs-lookup"><span data-stu-id="37489-129">Specifies the public configuration, as a string, for the extension.</span></span>
<span data-ttu-id="37489-130">Этот командлет не шифрует общедоступную конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="37489-130">This cmdlet does not encrypt public configuration.</span></span>

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

### <span data-ttu-id="37489-131">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="37489-131">-Type</span></span>
<span data-ttu-id="37489-132">Указывает тип расширения.</span><span class="sxs-lookup"><span data-stu-id="37489-132">Specifies the extension type.</span></span>
<span data-ttu-id="37489-133">Вы можете использовать командлет [Get-AzureRmVMExtensionImageType](./Get-AzureRmVMExtensionImageType.md) , чтобы получить тип расширения.</span><span class="sxs-lookup"><span data-stu-id="37489-133">You can use the [Get-AzureRmVMExtensionImageType](./Get-AzureRmVMExtensionImageType.md) cmdlet to get the extension type.</span></span>

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

### <span data-ttu-id="37489-134">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="37489-134">-TypeHandlerVersion</span></span>
<span data-ttu-id="37489-135">Указывает версию расширения, используемую для этой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="37489-135">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="37489-136">Вы можете использовать командлет [Get-AzureRmVMExtensionImage](./Get-AzureRmVMExtensionImage.md) , чтобы получить версию расширения.</span><span class="sxs-lookup"><span data-stu-id="37489-136">You can use the [Get-AzureRmVMExtensionImage](./Get-AzureRmVMExtensionImage.md) cmdlet to get the version of the extension.</span></span>

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

### <span data-ttu-id="37489-137">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="37489-137">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="37489-138">Укажите объект VMSS.</span><span class="sxs-lookup"><span data-stu-id="37489-138">Specify the VMSS object.</span></span>
<span data-ttu-id="37489-139">Вы можете создать объект с помощью [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) .</span><span class="sxs-lookup"><span data-stu-id="37489-139">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) to create the object.</span></span>

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

### <span data-ttu-id="37489-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="37489-140">-Confirm</span></span>
<span data-ttu-id="37489-141">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="37489-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37489-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37489-142">-WhatIf</span></span>
<span data-ttu-id="37489-143">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="37489-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="37489-144">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="37489-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37489-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37489-145">CommonParameters</span></span>
<span data-ttu-id="37489-146">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="37489-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37489-147">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37489-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37489-148">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="37489-148">INPUTS</span></span>

### <span data-ttu-id="37489-149">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="37489-149">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="37489-150">System. String</span><span class="sxs-lookup"><span data-stu-id="37489-150">System.String</span></span>

### <span data-ttu-id="37489-151">System. Nullable "1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="37489-151">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="37489-152">System. Object</span><span class="sxs-lookup"><span data-stu-id="37489-152">System.Object</span></span>

## <span data-ttu-id="37489-153">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="37489-153">OUTPUTS</span></span>

### <span data-ttu-id="37489-154">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="37489-154">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="37489-155">Пуск</span><span class="sxs-lookup"><span data-stu-id="37489-155">NOTES</span></span>

## <span data-ttu-id="37489-156">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="37489-156">RELATED LINKS</span></span>

[<span data-ttu-id="37489-157">Remove-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="37489-157">Remove-AzureRmVmssExtension</span></span>](./Remove-AzureRmVmssExtension.md)

[<span data-ttu-id="37489-158">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="37489-158">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="37489-159">Get-AzureRmVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="37489-159">Get-AzureRmVMExtensionImageType</span></span>](./Get-AzureRmVMExtensionImageType.md)

[<span data-ttu-id="37489-160">Get-AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="37489-160">Get-AzureRmVMExtensionImage</span></span>](./Get-AzureRmVMExtensionImage.md)

[<span data-ttu-id="37489-161">New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="37489-161">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 064196C3-ABF3-4F3A-A4AB-EB0D27098C70
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMExtension.md
ms.openlocfilehash: dc19566a9baaee7aa70dc03e5d9effa22df8d758
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100238653"
---
# <span data-ttu-id="0538b-101">Set-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="0538b-101">Set-AzVMExtension</span></span>

## <span data-ttu-id="0538b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0538b-102">SYNOPSIS</span></span>
<span data-ttu-id="0538b-103">Обновляет свойства расширения или добавляет расширение на виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="0538b-103">Updates extension properties or adds an extension to a virtual machine.</span></span>

## <span data-ttu-id="0538b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0538b-104">SYNTAX</span></span>

### <span data-ttu-id="0538b-105">Параметры (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0538b-105">Settings (Default)</span></span>
```
Set-AzVMExtension -Publisher <String> -ExtensionType <String> [-Settings <Hashtable>]
 [-ProtectedSettings <Hashtable>] [-AsJob] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion]
 [-EnableAutomaticUpgrade <Boolean>] [-ForceRerun <String>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0538b-106">SettingString</span><span class="sxs-lookup"><span data-stu-id="0538b-106">SettingString</span></span>
```
Set-AzVMExtension -Publisher <String> -ExtensionType <String> [-SettingString <String>]
 [-ProtectedSettingString <String>] [-AsJob] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion]
 [-EnableAutomaticUpgrade <Boolean>] [-ForceRerun <String>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0538b-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0538b-107">DESCRIPTION</span></span>
<span data-ttu-id="0538b-108">**Cmdlet Set-AzVMExtension** обновляет свойства существующих расширений виртуальной машины или добавляет расширение на виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="0538b-108">The **Set-AzVMExtension** cmdlet updates properties for existing Virtual Machine Extensions or adds an extension to a virtual machine.</span></span>

## <span data-ttu-id="0538b-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0538b-109">EXAMPLES</span></span>

### <span data-ttu-id="0538b-110">Пример 1. Изменение параметров с помощью hash tables</span><span class="sxs-lookup"><span data-stu-id="0538b-110">Example 1: Modify settings by using hash tables</span></span>
```
PS C:\> $Settings = @{"fileUris" = "[]"; "commandToExecute" = ""};
PS C:\> $ProtectedSettings = @{"storageAccountName" = $stoname; "storageAccountKey" = $stokey};
PS C:\> Set-AzVMExtension -ResourceGroupName "ResourceGroup11" -Location "West US" -VMName "VirtualMachine22" -Name "ContosoTest" -Publisher "Contoso.Compute" -Type "CustomScriptExtension" -TypeHandlerVersion "1.1" -Settings $Settings -ProtectedSettings $ProtectedSettings;
```

<span data-ttu-id="0538b-111">Первые две команды используют стандартный Windows PowerShell для создания hash tables, а затем сохраняет их в $Settings и $ProtectedSettings переменных.</span><span class="sxs-lookup"><span data-stu-id="0538b-111">The first two commands use standard Windows PowerShell syntax to create hash tables, and then stores those hash tables in the $Settings and $ProtectedSettings variables.</span></span>
<span data-ttu-id="0538b-112">Для получения дополнительных сведений введите `Get-Help about_Hash_Tables` .</span><span class="sxs-lookup"><span data-stu-id="0538b-112">For more information, type `Get-Help about_Hash_Tables`.</span></span>
<span data-ttu-id="0538b-113">Вторая команда содержит два значения, которые ранее были созданы и сохранены в переменных.</span><span class="sxs-lookup"><span data-stu-id="0538b-113">The second command includes two values previously created and stored in variables.</span></span>
<span data-ttu-id="0538b-114">Окончательная команда изменяет расширение виртуальной машины с именем VirtualMa в ResourceGroup11 в соответствии с содержимым $Settings и $ProtectedSettings.</span><span class="sxs-lookup"><span data-stu-id="0538b-114">The final command modifies an extension of the virtual machine named VirtualMachine22 in ResourceGroup11 according to the contents of $Settings and $ProtectedSettings.</span></span>
<span data-ttu-id="0538b-115">Эта команда определяет другие необходимые сведения, включая издателя и тип расширения.</span><span class="sxs-lookup"><span data-stu-id="0538b-115">The command specifies other required information that includes the publisher and the extension type.</span></span>

### <span data-ttu-id="0538b-116">Пример 2. Изменение параметров с помощью строк</span><span class="sxs-lookup"><span data-stu-id="0538b-116">Example 2: Modify settings by using strings</span></span>
```
PS C:\> $SettingsString = '{"fileUris":[],"commandToExecute":""}';
PS C:\> $ProtectedSettingsString = '{"storageAccountName":"' + $stoname + '","storageAccountKey":"' + $stokey + '"}';
PS C:\> Set-AzVMExtension -ResourceGroupName "ResourceGroup11" -Location "West US" -VMName "VirtualMachine22" -Name "CustomScriptExtension" -Publisher "Contoso.Compute" -Type "CustomScriptExtension" -TypeHandlerVersion "1.1" -SettingString $SettingsString -ProtectedSettingString $ProtectedSettingsString ;
```

<span data-ttu-id="0538b-117">Первые две команды создают строки, содержащие параметры, а затем $SettingsString и $ProtectedSettingsString переменных.</span><span class="sxs-lookup"><span data-stu-id="0538b-117">The first two commands create strings that contain settings, and then stores them in the $SettingsString and $ProtectedSettingsString variables.</span></span>
<span data-ttu-id="0538b-118">Окончательная команда изменяет расширение виртуальной машины с именем VirtualMachine22 в ResourceGroup11 в соответствии с содержимым $SettingsString и $ProtectedSettingsString.</span><span class="sxs-lookup"><span data-stu-id="0538b-118">The final command modifies an extension of the virtual machine named VirtualMachine22 in ResourceGroup11 according to the contents of $SettingsString and $ProtectedSettingsString.</span></span>
<span data-ttu-id="0538b-119">Эта команда определяет другие необходимые сведения, включая издателя и тип расширения.</span><span class="sxs-lookup"><span data-stu-id="0538b-119">The command specifies other required information that includes the publisher and the extension type.</span></span>

## <span data-ttu-id="0538b-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0538b-120">PARAMETERS</span></span>

### <span data-ttu-id="0538b-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0538b-121">-AsJob</span></span>
<span data-ttu-id="0538b-122">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="0538b-122">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0538b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0538b-123">-DefaultProfile</span></span>
<span data-ttu-id="0538b-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0538b-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0538b-125">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="0538b-125">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="0538b-126">Указывает на то, что этот cmdlet предотвращает автоматическое обновление расширений до более новой конечной версии агентом гостей Azure.</span><span class="sxs-lookup"><span data-stu-id="0538b-126">Indicates that this cmdlet prevents the Azure guest agent from automatically updating the extensions to a newer minor version.</span></span>
<span data-ttu-id="0538b-127">По умолчанию этот cmdlet позволяет агенту гостя обновить расширения.</span><span class="sxs-lookup"><span data-stu-id="0538b-127">By default, this cmdlet enables the guest agent to update the extensions.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0538b-128">-EnableAutomaticUpgrade</span><span class="sxs-lookup"><span data-stu-id="0538b-128">-EnableAutomaticUpgrade</span></span>
<span data-ttu-id="0538b-129">Указывает на то, должно ли расширение автоматически обновляться платформой при наличии новой версии расширения.</span><span class="sxs-lookup"><span data-stu-id="0538b-129">Indicates whether the extension should be automatically upgraded by the platform if there is a newer version of the extension available.</span></span>

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

### <span data-ttu-id="0538b-130">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="0538b-130">-ExtensionType</span></span>
<span data-ttu-id="0538b-131">Тип расширения.</span><span class="sxs-lookup"><span data-stu-id="0538b-131">Specifies the extension type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Type

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0538b-132">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="0538b-132">-ForceRerun</span></span>
<span data-ttu-id="0538b-133">Указывает на то, что этот cmdlet привязет к повторному повтору одной и той же конфигурации расширения на виртуальной машине, не устраив и повторно установив расширение.</span><span class="sxs-lookup"><span data-stu-id="0538b-133">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="0538b-134">Значение может быть любой строкой, которая отличается от текущей.</span><span class="sxs-lookup"><span data-stu-id="0538b-134">The value can be any string different from the current value.</span></span>
<span data-ttu-id="0538b-135">Если параметр forceUpdateTag не изменился, обработник по-прежнему применяет обновления общедоступных или защищенных параметров.</span><span class="sxs-lookup"><span data-stu-id="0538b-135">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="0538b-136">-Location</span><span class="sxs-lookup"><span data-stu-id="0538b-136">-Location</span></span>
<span data-ttu-id="0538b-137">Определяет расположение виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="0538b-137">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="0538b-138">-Name</span><span class="sxs-lookup"><span data-stu-id="0538b-138">-Name</span></span>
<span data-ttu-id="0538b-139">Указывает имя расширения.</span><span class="sxs-lookup"><span data-stu-id="0538b-139">Specifies the name of an extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0538b-140">-NoWait</span><span class="sxs-lookup"><span data-stu-id="0538b-140">-NoWait</span></span>
<span data-ttu-id="0538b-141">Начинает операцию и возвращает ее немедленно до ее завершения.</span><span class="sxs-lookup"><span data-stu-id="0538b-141">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="0538b-142">Чтобы определить успешное завершение операции, используйте другой механизм.</span><span class="sxs-lookup"><span data-stu-id="0538b-142">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0538b-143">-ProtectedSettings</span><span class="sxs-lookup"><span data-stu-id="0538b-143">-ProtectedSettings</span></span>
<span data-ttu-id="0538b-144">Указывает частную конфигурацию расширения в качестве hash table.</span><span class="sxs-lookup"><span data-stu-id="0538b-144">Specifies private configuration for the extension, as a hash table.</span></span>
<span data-ttu-id="0538b-145">Этот cmdlet зашифрует частную конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="0538b-145">This cmdlet encrypts the private configuration.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Settings
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0538b-146">-ProtectedSettingString</span><span class="sxs-lookup"><span data-stu-id="0538b-146">-ProtectedSettingString</span></span>
<span data-ttu-id="0538b-147">Указывает частную конфигурацию расширения в качестве строки.</span><span class="sxs-lookup"><span data-stu-id="0538b-147">Specifies private configuration for the extension, as a string.</span></span>
<span data-ttu-id="0538b-148">Этот cmdlet зашифрует частную конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="0538b-148">This cmdlet encrypts the private configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SettingString
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0538b-149">-Publisher</span><span class="sxs-lookup"><span data-stu-id="0538b-149">-Publisher</span></span>
<span data-ttu-id="0538b-150">Указывает имя издателя расширения.</span><span class="sxs-lookup"><span data-stu-id="0538b-150">Specifies the name of the extension publisher.</span></span>
<span data-ttu-id="0538b-151">Издатель предоставляет имя при регистрации расширения.</span><span class="sxs-lookup"><span data-stu-id="0538b-151">The publisher provides a name when the publisher registers an extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0538b-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0538b-152">-ResourceGroupName</span></span>
<span data-ttu-id="0538b-153">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="0538b-153">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0538b-154">-Settings</span><span class="sxs-lookup"><span data-stu-id="0538b-154">-Settings</span></span>
<span data-ttu-id="0538b-155">Указывает общедоступные конфигурации расширения в качестве hash table.</span><span class="sxs-lookup"><span data-stu-id="0538b-155">Specifies public configuration for the extension, as a hash table.</span></span>
<span data-ttu-id="0538b-156">Этот cmdlet не шифрует общедоступные конфигурации.</span><span class="sxs-lookup"><span data-stu-id="0538b-156">This cmdlet does not encrypt public configuration.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Settings
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0538b-157">-SettingString</span><span class="sxs-lookup"><span data-stu-id="0538b-157">-SettingString</span></span>
<span data-ttu-id="0538b-158">Указывает общедоступный конфигурацию расширения в качестве строки.</span><span class="sxs-lookup"><span data-stu-id="0538b-158">Specifies public configuration for the extension, as a string.</span></span>
<span data-ttu-id="0538b-159">Этот cmdlet не шифрует общедоступные конфигурации.</span><span class="sxs-lookup"><span data-stu-id="0538b-159">This cmdlet does not encrypt public configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SettingString
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0538b-160">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="0538b-160">-TypeHandlerVersion</span></span>
<span data-ttu-id="0538b-161">Определяет версию расширения, используемого для этой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="0538b-161">Specifies the version of the extension to use for this virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0538b-162">-VMName</span><span class="sxs-lookup"><span data-stu-id="0538b-162">-VMName</span></span>
<span data-ttu-id="0538b-163">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="0538b-163">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="0538b-164">Этот cmdlet изменяет расширения для виртуальной машины, указанные этим параметром.</span><span class="sxs-lookup"><span data-stu-id="0538b-164">This cmdlet modifies extensions for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0538b-165">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0538b-165">-Confirm</span></span>
<span data-ttu-id="0538b-166">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="0538b-166">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0538b-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0538b-167">-WhatIf</span></span>
<span data-ttu-id="0538b-168">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0538b-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0538b-169">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="0538b-169">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0538b-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0538b-170">CommonParameters</span></span>
<span data-ttu-id="0538b-171">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0538b-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0538b-172">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0538b-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0538b-173">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0538b-173">INPUTS</span></span>

### <span data-ttu-id="0538b-174">System.String</span><span class="sxs-lookup"><span data-stu-id="0538b-174">System.String</span></span>

### <span data-ttu-id="0538b-175">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="0538b-175">System.Collections.Hashtable</span></span>

### <span data-ttu-id="0538b-176">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="0538b-176">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="0538b-177">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0538b-177">OUTPUTS</span></span>

### <span data-ttu-id="0538b-178">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="0538b-178">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="0538b-179">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0538b-179">NOTES</span></span>

## <span data-ttu-id="0538b-180">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0538b-180">RELATED LINKS</span></span>

[<span data-ttu-id="0538b-181">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="0538b-181">Get-AzVMExtension</span></span>](./Get-AzVMExtension.md)

[<span data-ttu-id="0538b-182">Remove-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="0538b-182">Remove-AzVMExtension</span></span>](./Remove-AzVMExtension.md)



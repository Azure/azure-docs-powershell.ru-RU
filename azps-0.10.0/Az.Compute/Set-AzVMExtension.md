---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 064196C3-ABF3-4F3A-A4AB-EB0D27098C70
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMExtension.md
ms.openlocfilehash: c8aa9660be48f5b5eb2b95343c8a11420978448d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911332"
---
# <span data-ttu-id="a4f0e-101">Set-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="a4f0e-101">Set-AzVMExtension</span></span>

## <span data-ttu-id="a4f0e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a4f0e-102">SYNOPSIS</span></span>
<span data-ttu-id="a4f0e-103">Обновляет свойства расширения или добавляет расширение к виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="a4f0e-103">Updates extension properties or adds an extension to a virtual machine.</span></span>

## <span data-ttu-id="a4f0e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a4f0e-104">SYNTAX</span></span>

### <span data-ttu-id="a4f0e-105">Параметры (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a4f0e-105">Settings (Default)</span></span>
```
Set-AzVMExtension -Publisher <String> -ExtensionType <String> [-Settings <Hashtable>]
 [-ProtectedSettings <Hashtable>] [-AsJob] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4f0e-106">SettingString</span><span class="sxs-lookup"><span data-stu-id="a4f0e-106">SettingString</span></span>
```
Set-AzVMExtension -Publisher <String> -ExtensionType <String> [-SettingString <String>]
 [-ProtectedSettingString <String>] [-AsJob] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4f0e-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a4f0e-107">DESCRIPTION</span></span>
<span data-ttu-id="a4f0e-108">Командлет **Set-AzVMExtension** обновляет свойства для существующих расширений виртуальных машин или добавляет расширение к виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="a4f0e-108">The **Set-AzVMExtension** cmdlet updates properties for existing Virtual Machine Extensions or adds an extension to a virtual machine.</span></span>

## <span data-ttu-id="a4f0e-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a4f0e-109">EXAMPLES</span></span>

### <span data-ttu-id="a4f0e-110">Пример 1: изменение параметров с помощью хэш-таблиц</span><span class="sxs-lookup"><span data-stu-id="a4f0e-110">Example 1: Modify settings by using hash tables</span></span>
```
PS C:\> $Settings = @{"fileUris" = "[]"; "commandToExecute" = ""};
PS C:\> $ProtectedSettings = @{"storageAccountName" = $stoname; "storageAccountKey" = $stokey};
PS C:\> Set-AzVMExtension -ResourceGroupName "ResourceGroup11" -Location "West US" -VMName "VirtualMachine22" -Name "ContosoTest" -Publisher "Contoso.Compute" -Type "CustomScriptExtension" -TypeHandlerVersion "1.1" -Settings $Settings -ProtectedSettings $ProtectedSettings;
```

<span data-ttu-id="a4f0e-111">Первые две команды используют стандартный синтаксис Windows PowerShell для создания хэш-таблиц, а затем хранят эти хэш-таблицы в переменных $Settings и $ProtectedSettings.</span><span class="sxs-lookup"><span data-stu-id="a4f0e-111">The first two commands use standard Windows PowerShell syntax to create hash tables, and then stores those hash tables in the $Settings and $ProtectedSettings variables.</span></span>
<span data-ttu-id="a4f0e-112">Для получения дополнительных сведений введите `Get-Help about_Hash_Tables` .</span><span class="sxs-lookup"><span data-stu-id="a4f0e-112">For more information, type `Get-Help about_Hash_Tables`.</span></span>
<span data-ttu-id="a4f0e-113">Вторая команда содержит два значения, ранее созданные и хранимые в переменных.</span><span class="sxs-lookup"><span data-stu-id="a4f0e-113">The second command includes two values previously created and stored in variables.</span></span>

<span data-ttu-id="a4f0e-114">Последняя команда изменяет расширение виртуальной машины с именем VirtualMachine22 в ResourceGroup11 в соответствии с содержимым $Settings и $ProtectedSettings.</span><span class="sxs-lookup"><span data-stu-id="a4f0e-114">The final command modifies an extension of the virtual machine named VirtualMachine22 in ResourceGroup11 according to the contents of $Settings and $ProtectedSettings.</span></span>
<span data-ttu-id="a4f0e-115">Команда задает другие необходимые сведения, включающие издателя и тип расширения.</span><span class="sxs-lookup"><span data-stu-id="a4f0e-115">The command specifies other required information that includes the publisher and the extension type.</span></span>

### <span data-ttu-id="a4f0e-116">Пример 2: изменение параметров с помощью строк</span><span class="sxs-lookup"><span data-stu-id="a4f0e-116">Example 2: Modify settings by using strings</span></span>
```
PS C:\> $SettingsString = '{"fileUris":[],"commandToExecute":""}';
PS C:\> $ProtectedSettingsString = '{"storageAccountName":"' + $stoname + '","storageAccountKey":"' + $stokey + '"}';
PS C:\> Set-AzVMExtension -ResourceGroupName "ResourceGroup11" -Location "West US" -VMName "VirtualMachine22" -Name "CustomScriptExtension" -Publisher "Contoso.Compute" -Type "CustomScriptExtension" -TypeHandlerVersion "1.1" -SettingString $SettingsString -ProtectedSettingString $ProtectedSettingsString ;
```

<span data-ttu-id="a4f0e-117">Первые две команды создают строки, содержащие параметры, а затем сохраняют их в переменных $SettingsString и $ProtectedSettingsString.</span><span class="sxs-lookup"><span data-stu-id="a4f0e-117">The first two commands create strings that contain settings, and then stores them in the $SettingsString and $ProtectedSettingsString variables.</span></span>

<span data-ttu-id="a4f0e-118">Последняя команда изменяет расширение виртуальной машины с именем VirtualMachine22 в ResourceGroup11 в соответствии с содержимым $SettingsString и $ProtectedSettingsString.</span><span class="sxs-lookup"><span data-stu-id="a4f0e-118">The final command modifies an extension of the virtual machine named VirtualMachine22 in ResourceGroup11 according to the contents of $SettingsString and $ProtectedSettingsString.</span></span>
<span data-ttu-id="a4f0e-119">Команда задает другие необходимые сведения, включающие издателя и тип расширения.</span><span class="sxs-lookup"><span data-stu-id="a4f0e-119">The command specifies other required information that includes the publisher and the extension type.</span></span>

## <span data-ttu-id="a4f0e-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a4f0e-120">PARAMETERS</span></span>

### <span data-ttu-id="a4f0e-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a4f0e-121">-AsJob</span></span>
<span data-ttu-id="a4f0e-122">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="a4f0e-122">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4f0e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4f0e-123">-DefaultProfile</span></span>
<span data-ttu-id="a4f0e-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a4f0e-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a4f0e-125">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="a4f0e-125">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="a4f0e-126">Указывает, что этот командлет запрещает гостевой агенту Azure автоматически обновлять расширения до более поздней дополнительной версии.</span><span class="sxs-lookup"><span data-stu-id="a4f0e-126">Indicates that this cmdlet prevents the Azure guest agent from automatically updating the extensions to a newer minor version.</span></span>
<span data-ttu-id="a4f0e-127">По умолчанию этот командлет позволяет гостевому агенту обновлять расширения.</span><span class="sxs-lookup"><span data-stu-id="a4f0e-127">By default, this cmdlet enables the guest agent to update the extensions.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4f0e-128">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="a4f0e-128">-ExtensionType</span></span>
<span data-ttu-id="a4f0e-129">Указывает тип расширения.</span><span class="sxs-lookup"><span data-stu-id="a4f0e-129">Specifies the extension type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Type

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4f0e-130">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="a4f0e-130">-ForceRerun</span></span>
<span data-ttu-id="a4f0e-131">Указывает на то, что этот командлет принудительно выполняет повторное выполнение той же конфигурации на виртуальной машине без удаления и повторной установки расширения.</span><span class="sxs-lookup"><span data-stu-id="a4f0e-131">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="a4f0e-132">Значением может быть любая строка, отличающаяся от текущего значения.</span><span class="sxs-lookup"><span data-stu-id="a4f0e-132">The value can be any string different from the current value.</span></span>

<span data-ttu-id="a4f0e-133">Если forceUpdateTag не меняется, обновления открытых и защищенных параметров по-прежнему применяются обработчиком.</span><span class="sxs-lookup"><span data-stu-id="a4f0e-133">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="a4f0e-134">-Location</span><span class="sxs-lookup"><span data-stu-id="a4f0e-134">-Location</span></span>
<span data-ttu-id="a4f0e-135">Указывает расположение виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="a4f0e-135">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="a4f0e-136">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a4f0e-136">-Name</span></span>
<span data-ttu-id="a4f0e-137">Указывает имя расширения.</span><span class="sxs-lookup"><span data-stu-id="a4f0e-137">Specifies the name of an extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4f0e-138">-ProtectedSettings</span><span class="sxs-lookup"><span data-stu-id="a4f0e-138">-ProtectedSettings</span></span>
<span data-ttu-id="a4f0e-139">Задает частную конфигурацию для расширения в качестве хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="a4f0e-139">Specifies private configuration for the extension, as a hash table.</span></span>
<span data-ttu-id="a4f0e-140">Этот командлет шифрует закрытую конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="a4f0e-140">This cmdlet encrypts the private configuration.</span></span>

```yaml
Type: Hashtable
Parameter Sets: Settings
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4f0e-141">-ProtectedSettingString</span><span class="sxs-lookup"><span data-stu-id="a4f0e-141">-ProtectedSettingString</span></span>
<span data-ttu-id="a4f0e-142">Задает частную конфигурацию для расширения в виде строки.</span><span class="sxs-lookup"><span data-stu-id="a4f0e-142">Specifies private configuration for the extension, as a string.</span></span>
<span data-ttu-id="a4f0e-143">Этот командлет шифрует закрытую конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="a4f0e-143">This cmdlet encrypts the private configuration.</span></span>

```yaml
Type: String
Parameter Sets: SettingString
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4f0e-144">-Publisher</span><span class="sxs-lookup"><span data-stu-id="a4f0e-144">-Publisher</span></span>
<span data-ttu-id="a4f0e-145">Указывает имя издателя расширений.</span><span class="sxs-lookup"><span data-stu-id="a4f0e-145">Specifies the name of the extension publisher.</span></span>
<span data-ttu-id="a4f0e-146">Издатель предоставляет имя, когда Publisher регистрирует расширение.</span><span class="sxs-lookup"><span data-stu-id="a4f0e-146">The publisher provides a name when the publisher registers an extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4f0e-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4f0e-147">-ResourceGroupName</span></span>
<span data-ttu-id="a4f0e-148">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="a4f0e-148">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4f0e-149">-Параметры</span><span class="sxs-lookup"><span data-stu-id="a4f0e-149">-Settings</span></span>
<span data-ttu-id="a4f0e-150">Задает общедоступную конфигурацию для расширения в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="a4f0e-150">Specifies public configuration for the extension, as a hash table.</span></span>
<span data-ttu-id="a4f0e-151">Этот командлет не шифрует общедоступную конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="a4f0e-151">This cmdlet does not encrypt public configuration.</span></span>

```yaml
Type: Hashtable
Parameter Sets: Settings
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4f0e-152">-SettingString</span><span class="sxs-lookup"><span data-stu-id="a4f0e-152">-SettingString</span></span>
<span data-ttu-id="a4f0e-153">Указывает открытую конфигурацию для расширения в виде строки.</span><span class="sxs-lookup"><span data-stu-id="a4f0e-153">Specifies public configuration for the extension, as a string.</span></span>
<span data-ttu-id="a4f0e-154">Этот командлет не шифрует общедоступную конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="a4f0e-154">This cmdlet does not encrypt public configuration.</span></span>

```yaml
Type: String
Parameter Sets: SettingString
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4f0e-155">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="a4f0e-155">-TypeHandlerVersion</span></span>
<span data-ttu-id="a4f0e-156">Указывает версию расширения, используемую для этой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="a4f0e-156">Specifies the version of the extension to use for this virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4f0e-157">-VMName</span><span class="sxs-lookup"><span data-stu-id="a4f0e-157">-VMName</span></span>
<span data-ttu-id="a4f0e-158">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="a4f0e-158">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="a4f0e-159">Этот командлет изменяет расширения для виртуальной машины, указанную в этом параметре.</span><span class="sxs-lookup"><span data-stu-id="a4f0e-159">This cmdlet modifies extensions for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4f0e-160">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a4f0e-160">-Confirm</span></span>
<span data-ttu-id="a4f0e-161">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a4f0e-161">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4f0e-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4f0e-162">-WhatIf</span></span>
<span data-ttu-id="a4f0e-163">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a4f0e-163">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="a4f0e-164">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a4f0e-164">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4f0e-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4f0e-165">CommonParameters</span></span>
<span data-ttu-id="a4f0e-166">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a4f0e-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4f0e-167">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4f0e-167">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4f0e-168">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a4f0e-168">INPUTS</span></span>

### <span data-ttu-id="a4f0e-169">Ничего</span><span class="sxs-lookup"><span data-stu-id="a4f0e-169">None</span></span>
<span data-ttu-id="a4f0e-170">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="a4f0e-170">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a4f0e-171">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a4f0e-171">OUTPUTS</span></span>

### <span data-ttu-id="a4f0e-172">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="a4f0e-172">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="a4f0e-173">Пуск</span><span class="sxs-lookup"><span data-stu-id="a4f0e-173">NOTES</span></span>

## <span data-ttu-id="a4f0e-174">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a4f0e-174">RELATED LINKS</span></span>

[<span data-ttu-id="a4f0e-175">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="a4f0e-175">Get-AzVMExtension</span></span>](./Get-AzVMExtension.md)

[<span data-ttu-id="a4f0e-176">Remove-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="a4f0e-176">Remove-AzVMExtension</span></span>](./Remove-AzVMExtension.md)



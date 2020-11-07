---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 064196C3-ABF3-4F3A-A4AB-EB0D27098C70
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMExtension.md
ms.openlocfilehash: 1f758f77fc7162f8110f0e2d5887eadb55d7f7c1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732030"
---
# <span data-ttu-id="ace65-101">Set-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="ace65-101">Set-AzureRmVMExtension</span></span>

## <span data-ttu-id="ace65-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ace65-102">SYNOPSIS</span></span>
<span data-ttu-id="ace65-103">Обновляет свойства расширения или добавляет расширение к виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="ace65-103">Updates extension properties or adds an extension to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ace65-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ace65-104">SYNTAX</span></span>

### <span data-ttu-id="ace65-105">Параметры (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ace65-105">Settings (Default)</span></span>
```
Set-AzureRmVMExtension -Publisher <String> -ExtensionType <String> [-Settings <Hashtable>]
 [-ProtectedSettings <Hashtable>] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ace65-106">SettingString</span><span class="sxs-lookup"><span data-stu-id="ace65-106">SettingString</span></span>
```
Set-AzureRmVMExtension -Publisher <String> -ExtensionType <String> [-SettingString <String>]
 [-ProtectedSettingString <String>] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ace65-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ace65-107">DESCRIPTION</span></span>
<span data-ttu-id="ace65-108">Командлет **Set-AzureRmVMExtension** обновляет свойства для существующих расширений виртуальных машин или добавляет расширение к виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="ace65-108">The **Set-AzureRmVMExtension** cmdlet updates properties for existing Virtual Machine Extensions or adds an extension to a virtual machine.</span></span>

## <span data-ttu-id="ace65-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ace65-109">EXAMPLES</span></span>

### <span data-ttu-id="ace65-110">Пример 1: изменение параметров с помощью хэш-таблиц</span><span class="sxs-lookup"><span data-stu-id="ace65-110">Example 1: Modify settings by using hash tables</span></span>
```
PS C:\> $Settings = @{"fileUris" = "[]"; "commandToExecute" = ""};
PS C:\> $ProtectedSettings = @{"storageAccountName" = $stoname; "storageAccountKey" = $stokey};
PS C:\> Set-AzureRmVMExtension -ResourceGroupName "ResourceGroup11" -Location "West US" -VMName "VirtualMachine22" -Name "ContosoTest" -Publisher "Contoso.Compute" -Type "CustomScriptExtension" -TypeHandlerVersion "1.1" -Settings $Settings -ProtectedSettings $ProtectedSettings;
```

<span data-ttu-id="ace65-111">Первые две команды используют стандартный синтаксис Windows PowerShell для создания хэш-таблиц, а затем хранят эти хэш-таблицы в переменных $Settings и $ProtectedSettings.</span><span class="sxs-lookup"><span data-stu-id="ace65-111">The first two commands use standard Windows PowerShell syntax to create hash tables, and then stores those hash tables in the $Settings and $ProtectedSettings variables.</span></span>
<span data-ttu-id="ace65-112">Для получения дополнительных сведений введите `Get-Help about_Hash_Tables` .</span><span class="sxs-lookup"><span data-stu-id="ace65-112">For more information, type `Get-Help about_Hash_Tables`.</span></span>
<span data-ttu-id="ace65-113">Вторая команда содержит два значения, ранее созданные и хранимые в переменных.</span><span class="sxs-lookup"><span data-stu-id="ace65-113">The second command includes two values previously created and stored in variables.</span></span>

<span data-ttu-id="ace65-114">Последняя команда изменяет расширение виртуальной машины с именем VirtualMachine22 в ResourceGroup11 в соответствии с содержимым $Settings и $ProtectedSettings.</span><span class="sxs-lookup"><span data-stu-id="ace65-114">The final command modifies an extension of the virtual machine named VirtualMachine22 in ResourceGroup11 according to the contents of $Settings and $ProtectedSettings.</span></span>
<span data-ttu-id="ace65-115">Команда задает другие необходимые сведения, включающие издателя и тип расширения.</span><span class="sxs-lookup"><span data-stu-id="ace65-115">The command specifies other required information that includes the publisher and the extension type.</span></span>

### <span data-ttu-id="ace65-116">Пример 2: изменение параметров с помощью строк</span><span class="sxs-lookup"><span data-stu-id="ace65-116">Example 2: Modify settings by using strings</span></span>
```
PS C:\> $SettingsString = '{"fileUris":[],"commandToExecute":""}';
PS C:\> $ProtectedSettingsString = '{"storageAccountName":"' + $stoname + '","storageAccountKey":"' + $stokey + '"}';
PS C:\> Set-AzureRmVMExtension -ResourceGroupName "ResourceGroup11" -Location "West US" -VMName "VirtualMachine22" -Name "CustomScriptExtension" -Publisher "Contoso.Compute" -Type "CustomScriptExtension" -TypeHandlerVersion "1.1" -SettingString $SettingsString -ProtectedSettingString $ProtectedSettingsString ;
```

<span data-ttu-id="ace65-117">Первые две команды создают строки, содержащие параметры, а затем сохраняют их в переменных $SettingsString и $ProtectedSettingsString.</span><span class="sxs-lookup"><span data-stu-id="ace65-117">The first two commands create strings that contain settings, and then stores them in the $SettingsString and $ProtectedSettingsString variables.</span></span>

<span data-ttu-id="ace65-118">Последняя команда изменяет расширение виртуальной машины с именем VirtualMachine22 в ResourceGroup11 в соответствии с содержимым $SettingsString и $ProtectedSettingsString.</span><span class="sxs-lookup"><span data-stu-id="ace65-118">The final command modifies an extension of the virtual machine named VirtualMachine22 in ResourceGroup11 according to the contents of $SettingsString and $ProtectedSettingsString.</span></span>
<span data-ttu-id="ace65-119">Команда задает другие необходимые сведения, включающие издателя и тип расширения.</span><span class="sxs-lookup"><span data-stu-id="ace65-119">The command specifies other required information that includes the publisher and the extension type.</span></span>

## <span data-ttu-id="ace65-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ace65-120">PARAMETERS</span></span>

### <span data-ttu-id="ace65-121">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="ace65-121">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="ace65-122">Указывает, что этот командлет запрещает гостевой агенту Azure автоматически обновлять расширения до более поздней дополнительной версии.</span><span class="sxs-lookup"><span data-stu-id="ace65-122">Indicates that this cmdlet prevents the Azure guest agent from automatically updating the extensions to a newer minor version.</span></span>
<span data-ttu-id="ace65-123">По умолчанию этот командлет позволяет гостевому агенту обновлять расширения.</span><span class="sxs-lookup"><span data-stu-id="ace65-123">By default, this cmdlet enables the guest agent to update the extensions.</span></span>

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

### <span data-ttu-id="ace65-124">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="ace65-124">-ExtensionType</span></span>
<span data-ttu-id="ace65-125">Указывает тип расширения.</span><span class="sxs-lookup"><span data-stu-id="ace65-125">Specifies the extension type.</span></span>

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

### <span data-ttu-id="ace65-126">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="ace65-126">-ForceRerun</span></span>
<span data-ttu-id="ace65-127">Указывает на то, что этот командлет принудительно выполняет повторное выполнение той же конфигурации на виртуальной машине без удаления и повторной установки расширения.</span><span class="sxs-lookup"><span data-stu-id="ace65-127">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="ace65-128">Значением может быть любая строка, отличающаяся от текущего значения.</span><span class="sxs-lookup"><span data-stu-id="ace65-128">The value can be any string different from the current value.</span></span>

<span data-ttu-id="ace65-129">Если forceUpdateTag не меняется, обновления открытых и защищенных параметров по-прежнему применяются обработчиком.</span><span class="sxs-lookup"><span data-stu-id="ace65-129">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="ace65-130">-Location</span><span class="sxs-lookup"><span data-stu-id="ace65-130">-Location</span></span>
<span data-ttu-id="ace65-131">Указывает расположение виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="ace65-131">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="ace65-132">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ace65-132">-Name</span></span>
<span data-ttu-id="ace65-133">Указывает имя расширения.</span><span class="sxs-lookup"><span data-stu-id="ace65-133">Specifies the name of an extension.</span></span>

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

### <span data-ttu-id="ace65-134">-ProtectedSettings</span><span class="sxs-lookup"><span data-stu-id="ace65-134">-ProtectedSettings</span></span>
<span data-ttu-id="ace65-135">Задает частную конфигурацию для расширения в качестве хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="ace65-135">Specifies private configuration for the extension, as a hash table.</span></span>
<span data-ttu-id="ace65-136">Этот командлет шифрует закрытую конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="ace65-136">This cmdlet encrypts the private configuration.</span></span>

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

### <span data-ttu-id="ace65-137">-ProtectedSettingString</span><span class="sxs-lookup"><span data-stu-id="ace65-137">-ProtectedSettingString</span></span>
<span data-ttu-id="ace65-138">Задает частную конфигурацию для расширения в виде строки.</span><span class="sxs-lookup"><span data-stu-id="ace65-138">Specifies private configuration for the extension, as a string.</span></span>
<span data-ttu-id="ace65-139">Этот командлет шифрует закрытую конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="ace65-139">This cmdlet encrypts the private configuration.</span></span>

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

### <span data-ttu-id="ace65-140">-Publisher</span><span class="sxs-lookup"><span data-stu-id="ace65-140">-Publisher</span></span>
<span data-ttu-id="ace65-141">Указывает имя издателя расширений.</span><span class="sxs-lookup"><span data-stu-id="ace65-141">Specifies the name of the extension publisher.</span></span>
<span data-ttu-id="ace65-142">Издатель предоставляет имя, когда Publisher регистрирует расширение.</span><span class="sxs-lookup"><span data-stu-id="ace65-142">The publisher provides a name when the publisher registers an extension.</span></span>

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

### <span data-ttu-id="ace65-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ace65-143">-ResourceGroupName</span></span>
<span data-ttu-id="ace65-144">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="ace65-144">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="ace65-145">-Параметры</span><span class="sxs-lookup"><span data-stu-id="ace65-145">-Settings</span></span>
<span data-ttu-id="ace65-146">Задает общедоступную конфигурацию для расширения в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="ace65-146">Specifies public configuration for the extension, as a hash table.</span></span>
<span data-ttu-id="ace65-147">Этот командлет не шифрует общедоступную конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="ace65-147">This cmdlet does not encrypt public configuration.</span></span>

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

### <span data-ttu-id="ace65-148">-SettingString</span><span class="sxs-lookup"><span data-stu-id="ace65-148">-SettingString</span></span>
<span data-ttu-id="ace65-149">Указывает открытую конфигурацию для расширения в виде строки.</span><span class="sxs-lookup"><span data-stu-id="ace65-149">Specifies public configuration for the extension, as a string.</span></span>
<span data-ttu-id="ace65-150">Этот командлет не шифрует общедоступную конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="ace65-150">This cmdlet does not encrypt public configuration.</span></span>

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

### <span data-ttu-id="ace65-151">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="ace65-151">-TypeHandlerVersion</span></span>
<span data-ttu-id="ace65-152">Указывает версию расширения, используемую для этой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="ace65-152">Specifies the version of the extension to use for this virtual machine.</span></span>

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

### <span data-ttu-id="ace65-153">-VMName</span><span class="sxs-lookup"><span data-stu-id="ace65-153">-VMName</span></span>
<span data-ttu-id="ace65-154">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="ace65-154">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="ace65-155">Этот командлет изменяет расширения для виртуальной машины, указанную в этом параметре.</span><span class="sxs-lookup"><span data-stu-id="ace65-155">This cmdlet modifies extensions for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="ace65-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ace65-156">-Confirm</span></span>
<span data-ttu-id="ace65-157">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ace65-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ace65-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ace65-158">-WhatIf</span></span>
<span data-ttu-id="ace65-159">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ace65-159">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="ace65-160">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ace65-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ace65-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ace65-161">CommonParameters</span></span>
<span data-ttu-id="ace65-162">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ace65-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ace65-163">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ace65-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ace65-164">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ace65-164">INPUTS</span></span>

### <span data-ttu-id="ace65-165">Ничего</span><span class="sxs-lookup"><span data-stu-id="ace65-165">None</span></span>
<span data-ttu-id="ace65-166">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="ace65-166">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ace65-167">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ace65-167">OUTPUTS</span></span>

## <span data-ttu-id="ace65-168">Пуск</span><span class="sxs-lookup"><span data-stu-id="ace65-168">NOTES</span></span>

## <span data-ttu-id="ace65-169">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ace65-169">RELATED LINKS</span></span>

[<span data-ttu-id="ace65-170">Get-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="ace65-170">Get-AzureRmVMExtension</span></span>](./Get-AzureRmVMExtension.md)

[<span data-ttu-id="ace65-171">Remove-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="ace65-171">Remove-AzureRmVMExtension</span></span>](./Remove-AzureRmVMExtension.md)



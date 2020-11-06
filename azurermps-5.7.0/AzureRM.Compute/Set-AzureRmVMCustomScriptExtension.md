---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 64AB1BAE-A756-43A8-A40F-10B746EA0946
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMCustomScriptExtension.md
ms.openlocfilehash: 693809e46823cbcb8331eade7b8cd38c83238be2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561888"
---
# <span data-ttu-id="0b5c2-101">Set-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="0b5c2-101">Set-AzureRmVMCustomScriptExtension</span></span>

## <span data-ttu-id="0b5c2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0b5c2-102">SYNOPSIS</span></span>
<span data-ttu-id="0b5c2-103">Добавляет на виртуальную машину расширение настраиваемого сценария.</span><span class="sxs-lookup"><span data-stu-id="0b5c2-103">Adds a custom script extension to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0b5c2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0b5c2-104">SYNTAX</span></span>

### <span data-ttu-id="0b5c2-105">SetCustomScriptExtensionByContainerAndFileNames (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0b5c2-105">SetCustomScriptExtensionByContainerAndFileNames (Default)</span></span>
```
Set-AzureRmVMCustomScriptExtension -ContainerName <String> -FileName <String[]> [-StorageAccountName <String>]
 [-StorageEndpointSuffix <String>] [-StorageAccountKey <String>] [-Run <String>] [-Argument <String>]
 [-SecureExecution] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b5c2-106">SetCustomScriptExtensionByUriLinks</span><span class="sxs-lookup"><span data-stu-id="0b5c2-106">SetCustomScriptExtensionByUriLinks</span></span>
```
Set-AzureRmVMCustomScriptExtension [-FileUri <String[]>] [-Run <String>] [-Argument <String>]
 [-SecureExecution] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b5c2-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0b5c2-107">DESCRIPTION</span></span>
<span data-ttu-id="0b5c2-108">Командлет **Set-AzureRmVMCustomScriptExtension** добавляет расширение виртуальной машины специального сценария к виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="0b5c2-108">The **Set-AzureRmVMCustomScriptExtension** cmdlet adds a custom script Virtual Machine Extension to a virtual machine.</span></span>
<span data-ttu-id="0b5c2-109">Это расширение позволяет запускать собственные сценарии на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="0b5c2-109">This extension lets you run your own scripts on the virtual machine.</span></span>

## <span data-ttu-id="0b5c2-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0b5c2-110">EXAMPLES</span></span>

### <span data-ttu-id="0b5c2-111">Пример 1: Добавление настраиваемого сценария</span><span class="sxs-lookup"><span data-stu-id="0b5c2-111">Example 1: Add a custom script</span></span>
```
PS C:\> Set-AzureRmVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -Location "Central US" -VMName "VirtualMachine07" -Name "ContosoTest" -TypeHandlerVersion "1.1" -StorageAccountName "Contoso" -StorageAccountKey <StorageKey> -FileName "ContosoScript.exe" -ContainerName "Scripts"
```

<span data-ttu-id="0b5c2-112">Эта команда добавляет настраиваемый сценарий на виртуальную машину с именем VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="0b5c2-112">This command adds a custom script to the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="0b5c2-113">Файл сценария contososcript.exe.</span><span class="sxs-lookup"><span data-stu-id="0b5c2-113">The script file is contososcript.exe.</span></span>

## <span data-ttu-id="0b5c2-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0b5c2-114">PARAMETERS</span></span>

### <span data-ttu-id="0b5c2-115">-Аргумент</span><span class="sxs-lookup"><span data-stu-id="0b5c2-115">-Argument</span></span>
<span data-ttu-id="0b5c2-116">Задает аргументы, которые расширение сценария передает сценарию.</span><span class="sxs-lookup"><span data-stu-id="0b5c2-116">Specifies arguments that the script extension passes to the script.</span></span>

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

### <span data-ttu-id="0b5c2-117">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="0b5c2-117">-ContainerName</span></span>
<span data-ttu-id="0b5c2-118">Указывает имя контейнера хранилища Azure, в котором этот командлет хранит сценарий.</span><span class="sxs-lookup"><span data-stu-id="0b5c2-118">Specifies the name of the Azure storage container where this cmdlet stores the script.</span></span>

```yaml
Type: String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b5c2-119">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="0b5c2-119">-DisableAutoUpgradeMinorVersion</span></span>
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

### <span data-ttu-id="0b5c2-120">-FileName</span><span class="sxs-lookup"><span data-stu-id="0b5c2-120">-FileName</span></span>
<span data-ttu-id="0b5c2-121">Указывает имя файла сценария.</span><span class="sxs-lookup"><span data-stu-id="0b5c2-121">Specifies the name of the script file.</span></span>

```yaml
Type: String[]
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b5c2-122">-FileUri</span><span class="sxs-lookup"><span data-stu-id="0b5c2-122">-FileUri</span></span>
<span data-ttu-id="0b5c2-123">Задает универсальный код ресурса (URI) файла сценария.</span><span class="sxs-lookup"><span data-stu-id="0b5c2-123">Specifies the URI of the script file.</span></span>

```yaml
Type: String[]
Parameter Sets: SetCustomScriptExtensionByUriLinks
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b5c2-124">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="0b5c2-124">-ForceRerun</span></span>
<span data-ttu-id="0b5c2-125">Указывает на то, что этот командлет принудительно выполняет повторное выполнение той же конфигурации на виртуальной машине без удаления и повторной установки расширения.</span><span class="sxs-lookup"><span data-stu-id="0b5c2-125">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="0b5c2-126">Значением может быть любая строка, отличающаяся от текущего значения.</span><span class="sxs-lookup"><span data-stu-id="0b5c2-126">The value can be any string different from the current value.</span></span>

<span data-ttu-id="0b5c2-127">Если forceUpdateTag не меняется, обновления открытых и защищенных параметров по-прежнему применяются обработчиком.</span><span class="sxs-lookup"><span data-stu-id="0b5c2-127">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="0b5c2-128">-Location</span><span class="sxs-lookup"><span data-stu-id="0b5c2-128">-Location</span></span>
<span data-ttu-id="0b5c2-129">Указывает расположение виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="0b5c2-129">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="0b5c2-130">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0b5c2-130">-Name</span></span>
<span data-ttu-id="0b5c2-131">Указывает имя настраиваемого расширения сценария.</span><span class="sxs-lookup"><span data-stu-id="0b5c2-131">Specifies the name of the custom script extension.</span></span>

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

### <span data-ttu-id="0b5c2-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b5c2-132">-ResourceGroupName</span></span>
<span data-ttu-id="0b5c2-133">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="0b5c2-133">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="0b5c2-134">-Run</span><span class="sxs-lookup"><span data-stu-id="0b5c2-134">-Run</span></span>
<span data-ttu-id="0b5c2-135">Задает команду для использования при выполнении сценария.</span><span class="sxs-lookup"><span data-stu-id="0b5c2-135">Specifies the command to use that runs your script.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: RunFile, Command

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b5c2-136">-SecureExecution</span><span class="sxs-lookup"><span data-stu-id="0b5c2-136">-SecureExecution</span></span>
<span data-ttu-id="0b5c2-137">Указывает на то, что этот командлет гарантирует, что значение параметра *Run* не записывается на сервер или возвращается пользователю с помощью API получения расширения.</span><span class="sxs-lookup"><span data-stu-id="0b5c2-137">Indicates that this cmdlet makes sure that the value of the *Run* parameter is not logged on the server or returned to the user by using the GET extension API.</span></span>
<span data-ttu-id="0b5c2-138">Значение *Run* может содержать секреты или пароли, которые можно безопасно передавать в файл сценария.</span><span class="sxs-lookup"><span data-stu-id="0b5c2-138">The value of *Run* might contain secrets or passwords to be passed to the script file securely.</span></span>

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

### <span data-ttu-id="0b5c2-139">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="0b5c2-139">-StorageAccountKey</span></span>
<span data-ttu-id="0b5c2-140">Задает ключ для контейнера хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="0b5c2-140">Specifies the key for the Azure storage container.</span></span>

```yaml
Type: String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b5c2-141">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="0b5c2-141">-StorageAccountName</span></span>
<span data-ttu-id="0b5c2-142">Указывает имя учетной записи службы хранилища Azure, в которой этот командлет хранит сценарий.</span><span class="sxs-lookup"><span data-stu-id="0b5c2-142">Specifies the name of the Azure storage account where this cmdlet stores the script.</span></span>

```yaml
Type: String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b5c2-143">-StorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="0b5c2-143">-StorageEndpointSuffix</span></span>
<span data-ttu-id="0b5c2-144">Указывает суффикс конечной точки хранилища.</span><span class="sxs-lookup"><span data-stu-id="0b5c2-144">Specifies the storage endpoint suffix.</span></span>

```yaml
Type: String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b5c2-145">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="0b5c2-145">-TypeHandlerVersion</span></span>
<span data-ttu-id="0b5c2-146">Указывает версию расширения, используемую для этой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="0b5c2-146">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="0b5c2-147">Чтобы получить версию, выполните командлет Get-AzureRmVMExtensionImage со значением Microsoft. COMPUTE для параметра *PublisherName* и VMAccessAgent для параметра *Type* .</span><span class="sxs-lookup"><span data-stu-id="0b5c2-147">To obtain the version, run the Get-AzureRmVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and VMAccessAgent for the *Type* parameter.</span></span>

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

### <span data-ttu-id="0b5c2-148">-VMName</span><span class="sxs-lookup"><span data-stu-id="0b5c2-148">-VMName</span></span>
<span data-ttu-id="0b5c2-149">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="0b5c2-149">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="0b5c2-150">Этот командлет добавляет расширение настраиваемого сценария для виртуальной машины, указывающей этот параметр.</span><span class="sxs-lookup"><span data-stu-id="0b5c2-150">This cmdlet adds the custom script extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="0b5c2-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0b5c2-151">-Confirm</span></span>
<span data-ttu-id="0b5c2-152">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0b5c2-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b5c2-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b5c2-153">-WhatIf</span></span>
<span data-ttu-id="0b5c2-154">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0b5c2-154">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="0b5c2-155">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0b5c2-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b5c2-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b5c2-156">CommonParameters</span></span>
<span data-ttu-id="0b5c2-157">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0b5c2-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b5c2-158">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b5c2-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b5c2-159">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0b5c2-159">INPUTS</span></span>

### <span data-ttu-id="0b5c2-160">Ничего</span><span class="sxs-lookup"><span data-stu-id="0b5c2-160">None</span></span>
<span data-ttu-id="0b5c2-161">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="0b5c2-161">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0b5c2-162">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0b5c2-162">OUTPUTS</span></span>

## <span data-ttu-id="0b5c2-163">Пуск</span><span class="sxs-lookup"><span data-stu-id="0b5c2-163">NOTES</span></span>

## <span data-ttu-id="0b5c2-164">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0b5c2-164">RELATED LINKS</span></span>

[<span data-ttu-id="0b5c2-165">Get-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="0b5c2-165">Get-AzureRmVMCustomScriptExtension</span></span>](./Get-AzureRmVMCustomScriptExtension.md)

[<span data-ttu-id="0b5c2-166">Remove-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="0b5c2-166">Remove-AzureRmVMCustomScriptExtension</span></span>](./Remove-AzureRmVMCustomScriptExtension.md)



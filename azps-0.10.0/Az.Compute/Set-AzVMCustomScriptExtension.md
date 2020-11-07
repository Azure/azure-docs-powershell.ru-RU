---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 64AB1BAE-A756-43A8-A40F-10B746EA0946
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmcustomscriptextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMCustomScriptExtension.md
ms.openlocfilehash: 6fe34ae33ed70cebe4c8f76beb235e6fa7445fee
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911344"
---
# <span data-ttu-id="c910f-101">Set-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="c910f-101">Set-AzVMCustomScriptExtension</span></span>

## <span data-ttu-id="c910f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c910f-102">SYNOPSIS</span></span>
<span data-ttu-id="c910f-103">Добавляет на виртуальную машину расширение настраиваемого сценария.</span><span class="sxs-lookup"><span data-stu-id="c910f-103">Adds a custom script extension to a virtual machine.</span></span>

## <span data-ttu-id="c910f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c910f-104">SYNTAX</span></span>

### <span data-ttu-id="c910f-105">SetCustomScriptExtensionByContainerAndFileNames (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c910f-105">SetCustomScriptExtensionByContainerAndFileNames (Default)</span></span>
```
Set-AzVMCustomScriptExtension -ContainerName <String> -FileName <String[]> [-StorageAccountName <String>]
 [-StorageEndpointSuffix <String>] [-StorageAccountKey <String>] [-Run <String>] [-Argument <String>]
 [-SecureExecution] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c910f-106">SetCustomScriptExtensionByUriLinks</span><span class="sxs-lookup"><span data-stu-id="c910f-106">SetCustomScriptExtensionByUriLinks</span></span>
```
Set-AzVMCustomScriptExtension [-FileUri <String[]>] [-Run <String>] [-Argument <String>]
 [-SecureExecution] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c910f-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c910f-107">DESCRIPTION</span></span>
<span data-ttu-id="c910f-108">Командлет **Set-AzVMCustomScriptExtension** добавляет расширение виртуальной машины специального сценария к виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="c910f-108">The **Set-AzVMCustomScriptExtension** cmdlet adds a custom script Virtual Machine Extension to a virtual machine.</span></span>
<span data-ttu-id="c910f-109">Это расширение позволяет запускать собственные сценарии на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="c910f-109">This extension lets you run your own scripts on the virtual machine.</span></span>

## <span data-ttu-id="c910f-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c910f-110">EXAMPLES</span></span>

### <span data-ttu-id="c910f-111">Пример 1: Добавление настраиваемого сценария</span><span class="sxs-lookup"><span data-stu-id="c910f-111">Example 1: Add a custom script</span></span>
```
PS C:\> Set-AzVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -Location "Central US" -VMName "VirtualMachine07" -Name "ContosoTest" -TypeHandlerVersion "1.1" -StorageAccountName "Contoso" -StorageAccountKey <StorageKey> -FileName "ContosoScript.exe" -ContainerName "Scripts"
```

<span data-ttu-id="c910f-112">Эта команда добавляет настраиваемый сценарий на виртуальную машину с именем VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="c910f-112">This command adds a custom script to the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="c910f-113">Файл сценария contososcript.exe.</span><span class="sxs-lookup"><span data-stu-id="c910f-113">The script file is contososcript.exe.</span></span>

## <span data-ttu-id="c910f-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c910f-114">PARAMETERS</span></span>

### <span data-ttu-id="c910f-115">-Аргумент</span><span class="sxs-lookup"><span data-stu-id="c910f-115">-Argument</span></span>
<span data-ttu-id="c910f-116">Задает аргументы, которые расширение сценария передает сценарию.</span><span class="sxs-lookup"><span data-stu-id="c910f-116">Specifies arguments that the script extension passes to the script.</span></span>

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

### <span data-ttu-id="c910f-117">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="c910f-117">-ContainerName</span></span>
<span data-ttu-id="c910f-118">Указывает имя контейнера хранилища Azure, в котором этот командлет хранит сценарий.</span><span class="sxs-lookup"><span data-stu-id="c910f-118">Specifies the name of the Azure storage container where this cmdlet stores the script.</span></span>

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

### <span data-ttu-id="c910f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c910f-119">-DefaultProfile</span></span>
<span data-ttu-id="c910f-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c910f-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c910f-121">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="c910f-121">-DisableAutoUpgradeMinorVersion</span></span>
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

### <span data-ttu-id="c910f-122">-FileName</span><span class="sxs-lookup"><span data-stu-id="c910f-122">-FileName</span></span>
<span data-ttu-id="c910f-123">Указывает имя файла сценария.</span><span class="sxs-lookup"><span data-stu-id="c910f-123">Specifies the name of the script file.</span></span> <span data-ttu-id="c910f-124">Если файл хранится в хранилище больших двоичных объектов Azure, значение имени файла — Case-senstive.</span><span class="sxs-lookup"><span data-stu-id="c910f-124">If the file is stored in Azure Blob storage, the file name value is case-senstive.</span></span> <span data-ttu-id="c910f-125">Имена файлов, хранящихся в хранилище файлов Azure, не являются строчными senstive.</span><span class="sxs-lookup"><span data-stu-id="c910f-125">File names of files stored in Azure File storage are not case-senstive.</span></span>

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

### <span data-ttu-id="c910f-126">-FileUri</span><span class="sxs-lookup"><span data-stu-id="c910f-126">-FileUri</span></span>
<span data-ttu-id="c910f-127">Задает универсальный код ресурса (URI) файла сценария.</span><span class="sxs-lookup"><span data-stu-id="c910f-127">Specifies the URI of the script file.</span></span>

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

### <span data-ttu-id="c910f-128">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="c910f-128">-ForceRerun</span></span>
<span data-ttu-id="c910f-129">Указывает на то, что этот командлет принудительно выполняет повторное выполнение той же конфигурации на виртуальной машине без удаления и повторной установки расширения.</span><span class="sxs-lookup"><span data-stu-id="c910f-129">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="c910f-130">Значением может быть любая строка, отличающаяся от текущего значения.</span><span class="sxs-lookup"><span data-stu-id="c910f-130">The value can be any string different from the current value.</span></span>

<span data-ttu-id="c910f-131">Если forceUpdateTag не меняется, обновления открытых и защищенных параметров по-прежнему применяются обработчиком.</span><span class="sxs-lookup"><span data-stu-id="c910f-131">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="c910f-132">-Location</span><span class="sxs-lookup"><span data-stu-id="c910f-132">-Location</span></span>
<span data-ttu-id="c910f-133">Указывает расположение виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c910f-133">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="c910f-134">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c910f-134">-Name</span></span>
<span data-ttu-id="c910f-135">Указывает имя настраиваемого расширения сценария.</span><span class="sxs-lookup"><span data-stu-id="c910f-135">Specifies the name of the custom script extension.</span></span>

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

### <span data-ttu-id="c910f-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c910f-136">-ResourceGroupName</span></span>
<span data-ttu-id="c910f-137">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c910f-137">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="c910f-138">-Run</span><span class="sxs-lookup"><span data-stu-id="c910f-138">-Run</span></span>
<span data-ttu-id="c910f-139">Задает команду для использования при выполнении сценария.</span><span class="sxs-lookup"><span data-stu-id="c910f-139">Specifies the command to use that runs your script.</span></span>

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

### <span data-ttu-id="c910f-140">-SecureExecution</span><span class="sxs-lookup"><span data-stu-id="c910f-140">-SecureExecution</span></span>
<span data-ttu-id="c910f-141">Указывает на то, что этот командлет гарантирует, что значение параметра *Run* не записывается на сервер или возвращается пользователю с помощью API получения расширения.</span><span class="sxs-lookup"><span data-stu-id="c910f-141">Indicates that this cmdlet makes sure that the value of the *Run* parameter is not logged on the server or returned to the user by using the GET extension API.</span></span>
<span data-ttu-id="c910f-142">Значение *Run* может содержать секреты или пароли, которые можно безопасно передавать в файл сценария.</span><span class="sxs-lookup"><span data-stu-id="c910f-142">The value of *Run* might contain secrets or passwords to be passed to the script file securely.</span></span>

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

### <span data-ttu-id="c910f-143">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="c910f-143">-StorageAccountKey</span></span>
<span data-ttu-id="c910f-144">Задает ключ для контейнера хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="c910f-144">Specifies the key for the Azure storage container.</span></span>

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

### <span data-ttu-id="c910f-145">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="c910f-145">-StorageAccountName</span></span>
<span data-ttu-id="c910f-146">Указывает имя учетной записи службы хранилища Azure, в которой этот командлет хранит сценарий.</span><span class="sxs-lookup"><span data-stu-id="c910f-146">Specifies the name of the Azure storage account where this cmdlet stores the script.</span></span>

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

### <span data-ttu-id="c910f-147">-StorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="c910f-147">-StorageEndpointSuffix</span></span>
<span data-ttu-id="c910f-148">Указывает суффикс конечной точки хранилища.</span><span class="sxs-lookup"><span data-stu-id="c910f-148">Specifies the storage endpoint suffix.</span></span>

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

### <span data-ttu-id="c910f-149">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="c910f-149">-TypeHandlerVersion</span></span>
<span data-ttu-id="c910f-150">Указывает версию расширения, используемую для этой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c910f-150">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="c910f-151">Чтобы получить версию, выполните командлет Get-AzVMExtensionImage со значением Microsoft. COMPUTE для параметра *PublisherName* и VMAccessAgent для параметра *Type* .</span><span class="sxs-lookup"><span data-stu-id="c910f-151">To obtain the version, run the Get-AzVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and VMAccessAgent for the *Type* parameter.</span></span>

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

### <span data-ttu-id="c910f-152">-VMName</span><span class="sxs-lookup"><span data-stu-id="c910f-152">-VMName</span></span>
<span data-ttu-id="c910f-153">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c910f-153">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="c910f-154">Этот командлет добавляет расширение настраиваемого сценария для виртуальной машины, указывающей этот параметр.</span><span class="sxs-lookup"><span data-stu-id="c910f-154">This cmdlet adds the custom script extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="c910f-155">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c910f-155">-Confirm</span></span>
<span data-ttu-id="c910f-156">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c910f-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c910f-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c910f-157">-WhatIf</span></span>
<span data-ttu-id="c910f-158">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c910f-158">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="c910f-159">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c910f-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c910f-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c910f-160">CommonParameters</span></span>
<span data-ttu-id="c910f-161">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c910f-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c910f-162">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c910f-162">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c910f-163">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c910f-163">INPUTS</span></span>

### <span data-ttu-id="c910f-164">Ничего</span><span class="sxs-lookup"><span data-stu-id="c910f-164">None</span></span>
<span data-ttu-id="c910f-165">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="c910f-165">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c910f-166">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c910f-166">OUTPUTS</span></span>

### <span data-ttu-id="c910f-167">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="c910f-167">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="c910f-168">Пуск</span><span class="sxs-lookup"><span data-stu-id="c910f-168">NOTES</span></span>

## <span data-ttu-id="c910f-169">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c910f-169">RELATED LINKS</span></span>

[<span data-ttu-id="c910f-170">Get-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="c910f-170">Get-AzVMCustomScriptExtension</span></span>](./Get-AzVMCustomScriptExtension.md)

[<span data-ttu-id="c910f-171">Remove-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="c910f-171">Remove-AzVMCustomScriptExtension</span></span>](./Remove-AzVMCustomScriptExtension.md)



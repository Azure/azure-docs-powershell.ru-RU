---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 64AB1BAE-A756-43A8-A40F-10B746EA0946
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmcustomscriptextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVMCustomScriptExtension.md
ms.openlocfilehash: 926a33040421acbcb6424c89ec10da89ad87e5ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564660"
---
# <span data-ttu-id="9a895-101">Set-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="9a895-101">Set-AzureRmVMCustomScriptExtension</span></span>

## <span data-ttu-id="9a895-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9a895-102">SYNOPSIS</span></span>
<span data-ttu-id="9a895-103">Добавляет на виртуальную машину расширение настраиваемого сценария.</span><span class="sxs-lookup"><span data-stu-id="9a895-103">Adds a custom script extension to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9a895-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9a895-104">SYNTAX</span></span>

### <span data-ttu-id="9a895-105">SetCustomScriptExtensionByContainerAndFileNames (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9a895-105">SetCustomScriptExtensionByContainerAndFileNames (Default)</span></span>
```
Set-AzureRmVMCustomScriptExtension -ContainerName <String> -FileName <String[]> [-StorageAccountName <String>]
 [-StorageEndpointSuffix <String>] [-StorageAccountKey <String>] [-Run <String>] [-Argument <String>]
 [-SecureExecution] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a895-106">SetCustomScriptExtensionByUriLinks</span><span class="sxs-lookup"><span data-stu-id="9a895-106">SetCustomScriptExtensionByUriLinks</span></span>
```
Set-AzureRmVMCustomScriptExtension [-FileUri <String[]>] [-Run <String>] [-Argument <String>]
 [-SecureExecution] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a895-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9a895-107">DESCRIPTION</span></span>
<span data-ttu-id="9a895-108">Командлет **Set-AzureRmVMCustomScriptExtension** добавляет расширение виртуальной машины специального сценария к виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="9a895-108">The **Set-AzureRmVMCustomScriptExtension** cmdlet adds a custom script Virtual Machine Extension to a virtual machine.</span></span>
<span data-ttu-id="9a895-109">Это расширение позволяет запускать собственные сценарии на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="9a895-109">This extension lets you run your own scripts on the virtual machine.</span></span>

## <span data-ttu-id="9a895-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9a895-110">EXAMPLES</span></span>

### <span data-ttu-id="9a895-111">Пример 1: Добавление настраиваемого сценария</span><span class="sxs-lookup"><span data-stu-id="9a895-111">Example 1: Add a custom script</span></span>
```
PS C:\> Set-AzureRmVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -Location "Central US" -VMName "VirtualMachine07" -Name "ContosoTest" -TypeHandlerVersion "1.1" -StorageAccountName "Contoso" -StorageAccountKey <StorageKey> -FileName "ContosoScript.exe" -ContainerName "Scripts"
```

<span data-ttu-id="9a895-112">Эта команда добавляет настраиваемый сценарий на виртуальную машину с именем VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="9a895-112">This command adds a custom script to the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="9a895-113">Файл сценария contososcript.exe.</span><span class="sxs-lookup"><span data-stu-id="9a895-113">The script file is contososcript.exe.</span></span>

## <span data-ttu-id="9a895-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9a895-114">PARAMETERS</span></span>

### <span data-ttu-id="9a895-115">-Аргумент</span><span class="sxs-lookup"><span data-stu-id="9a895-115">-Argument</span></span>
<span data-ttu-id="9a895-116">Задает аргументы, которые расширение сценария передает сценарию.</span><span class="sxs-lookup"><span data-stu-id="9a895-116">Specifies arguments that the script extension passes to the script.</span></span>

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

### <span data-ttu-id="9a895-117">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="9a895-117">-ContainerName</span></span>
<span data-ttu-id="9a895-118">Указывает имя контейнера хранилища Azure, в котором этот командлет хранит сценарий.</span><span class="sxs-lookup"><span data-stu-id="9a895-118">Specifies the name of the Azure storage container where this cmdlet stores the script.</span></span>

```yaml
Type: System.String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a895-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a895-119">-DefaultProfile</span></span>
<span data-ttu-id="9a895-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9a895-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9a895-121">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="9a895-121">-DisableAutoUpgradeMinorVersion</span></span>
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

### <span data-ttu-id="9a895-122">-FileName</span><span class="sxs-lookup"><span data-stu-id="9a895-122">-FileName</span></span>
<span data-ttu-id="9a895-123">Указывает имя файла сценария.</span><span class="sxs-lookup"><span data-stu-id="9a895-123">Specifies the name of the script file.</span></span> <span data-ttu-id="9a895-124">Если файл хранится в хранилище больших двоичных объектов Azure, значение имени файла — Case-senstive.</span><span class="sxs-lookup"><span data-stu-id="9a895-124">If the file is stored in Azure Blob storage, the file name value is case-senstive.</span></span> <span data-ttu-id="9a895-125">Имена файлов, хранящихся в хранилище файлов Azure, не являются строчными senstive.</span><span class="sxs-lookup"><span data-stu-id="9a895-125">File names of files stored in Azure File storage are not case-senstive.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a895-126">-FileUri</span><span class="sxs-lookup"><span data-stu-id="9a895-126">-FileUri</span></span>
<span data-ttu-id="9a895-127">Задает универсальный код ресурса (URI) файла сценария.</span><span class="sxs-lookup"><span data-stu-id="9a895-127">Specifies the URI of the script file.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SetCustomScriptExtensionByUriLinks
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a895-128">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="9a895-128">-ForceRerun</span></span>
<span data-ttu-id="9a895-129">Указывает на то, что этот командлет принудительно выполняет повторное выполнение той же конфигурации на виртуальной машине без удаления и повторной установки расширения.</span><span class="sxs-lookup"><span data-stu-id="9a895-129">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="9a895-130">Значением может быть любая строка, отличающаяся от текущего значения.</span><span class="sxs-lookup"><span data-stu-id="9a895-130">The value can be any string different from the current value.</span></span>
<span data-ttu-id="9a895-131">Если forceUpdateTag не меняется, обновления открытых и защищенных параметров по-прежнему применяются обработчиком.</span><span class="sxs-lookup"><span data-stu-id="9a895-131">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="9a895-132">-Location</span><span class="sxs-lookup"><span data-stu-id="9a895-132">-Location</span></span>
<span data-ttu-id="9a895-133">Указывает расположение виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="9a895-133">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="9a895-134">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9a895-134">-Name</span></span>
<span data-ttu-id="9a895-135">Указывает имя настраиваемого расширения сценария.</span><span class="sxs-lookup"><span data-stu-id="9a895-135">Specifies the name of the custom script extension.</span></span>

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

### <span data-ttu-id="9a895-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a895-136">-ResourceGroupName</span></span>
<span data-ttu-id="9a895-137">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="9a895-137">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="9a895-138">-Run</span><span class="sxs-lookup"><span data-stu-id="9a895-138">-Run</span></span>
<span data-ttu-id="9a895-139">Задает команду для использования при выполнении сценария.</span><span class="sxs-lookup"><span data-stu-id="9a895-139">Specifies the command to use that runs your script.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RunFile, Command

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a895-140">-SecureExecution</span><span class="sxs-lookup"><span data-stu-id="9a895-140">-SecureExecution</span></span>
<span data-ttu-id="9a895-141">Указывает на то, что этот командлет гарантирует, что значение параметра *Run* не записывается на сервер или возвращается пользователю с помощью API получения расширения.</span><span class="sxs-lookup"><span data-stu-id="9a895-141">Indicates that this cmdlet makes sure that the value of the *Run* parameter is not logged on the server or returned to the user by using the GET extension API.</span></span>
<span data-ttu-id="9a895-142">Значение *Run* может содержать секреты или пароли, которые можно безопасно передавать в файл сценария.</span><span class="sxs-lookup"><span data-stu-id="9a895-142">The value of *Run* might contain secrets or passwords to be passed to the script file securely.</span></span>

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

### <span data-ttu-id="9a895-143">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="9a895-143">-StorageAccountKey</span></span>
<span data-ttu-id="9a895-144">Задает ключ для контейнера хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="9a895-144">Specifies the key for the Azure storage container.</span></span>

```yaml
Type: System.String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a895-145">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="9a895-145">-StorageAccountName</span></span>
<span data-ttu-id="9a895-146">Указывает имя учетной записи службы хранилища Azure, в которой этот командлет хранит сценарий.</span><span class="sxs-lookup"><span data-stu-id="9a895-146">Specifies the name of the Azure storage account where this cmdlet stores the script.</span></span>

```yaml
Type: System.String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a895-147">-StorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="9a895-147">-StorageEndpointSuffix</span></span>
<span data-ttu-id="9a895-148">Указывает суффикс конечной точки хранилища.</span><span class="sxs-lookup"><span data-stu-id="9a895-148">Specifies the storage endpoint suffix.</span></span>

```yaml
Type: System.String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a895-149">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="9a895-149">-TypeHandlerVersion</span></span>
<span data-ttu-id="9a895-150">Указывает версию расширения, используемую для этой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="9a895-150">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="9a895-151">Чтобы получить версию, выполните командлет Get-AzureRmVMExtensionImage со значением Microsoft. COMPUTE для параметра *PublisherName* и VMAccessAgent для параметра *Type* .</span><span class="sxs-lookup"><span data-stu-id="9a895-151">To obtain the version, run the Get-AzureRmVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and VMAccessAgent for the *Type* parameter.</span></span>

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

### <span data-ttu-id="9a895-152">-VMName</span><span class="sxs-lookup"><span data-stu-id="9a895-152">-VMName</span></span>
<span data-ttu-id="9a895-153">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="9a895-153">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="9a895-154">Этот командлет добавляет расширение настраиваемого сценария для виртуальной машины, указывающей этот параметр.</span><span class="sxs-lookup"><span data-stu-id="9a895-154">This cmdlet adds the custom script extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="9a895-155">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9a895-155">-Confirm</span></span>
<span data-ttu-id="9a895-156">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9a895-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a895-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a895-157">-WhatIf</span></span>
<span data-ttu-id="9a895-158">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9a895-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a895-159">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9a895-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a895-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a895-160">CommonParameters</span></span>
<span data-ttu-id="9a895-161">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9a895-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a895-162">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a895-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a895-163">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9a895-163">INPUTS</span></span>

### <span data-ttu-id="9a895-164">System. String</span><span class="sxs-lookup"><span data-stu-id="9a895-164">System.String</span></span>

### <span data-ttu-id="9a895-165">System. String []</span><span class="sxs-lookup"><span data-stu-id="9a895-165">System.String[]</span></span>

### <span data-ttu-id="9a895-166">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="9a895-166">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="9a895-167">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9a895-167">OUTPUTS</span></span>

### <span data-ttu-id="9a895-168">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="9a895-168">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="9a895-169">Пуск</span><span class="sxs-lookup"><span data-stu-id="9a895-169">NOTES</span></span>

## <span data-ttu-id="9a895-170">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9a895-170">RELATED LINKS</span></span>

[<span data-ttu-id="9a895-171">Get-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="9a895-171">Get-AzureRmVMCustomScriptExtension</span></span>](./Get-AzureRmVMCustomScriptExtension.md)

[<span data-ttu-id="9a895-172">Remove-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="9a895-172">Remove-AzureRmVMCustomScriptExtension</span></span>](./Remove-AzureRmVMCustomScriptExtension.md)



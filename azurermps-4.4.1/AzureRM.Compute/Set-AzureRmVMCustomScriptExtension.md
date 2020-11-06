---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 64AB1BAE-A756-43A8-A40F-10B746EA0946
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMCustomScriptExtension.md
ms.openlocfilehash: a9d03bd7f506c7210eeee90c379f90dd0833818e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557808"
---
# <span data-ttu-id="dcec7-101">Set-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="dcec7-101">Set-AzureRmVMCustomScriptExtension</span></span>

## <span data-ttu-id="dcec7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dcec7-102">SYNOPSIS</span></span>
<span data-ttu-id="dcec7-103">Добавляет на виртуальную машину расширение настраиваемого сценария.</span><span class="sxs-lookup"><span data-stu-id="dcec7-103">Adds a custom script extension to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dcec7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dcec7-104">SYNTAX</span></span>

### <span data-ttu-id="dcec7-105">SetCustomScriptExtensionByContainerAndFileNames (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="dcec7-105">SetCustomScriptExtensionByContainerAndFileNames (Default)</span></span>
```
Set-AzureRmVMCustomScriptExtension -ContainerName <String> -FileName <String[]> [-StorageAccountName <String>]
 [-StorageEndpointSuffix <String>] [-StorageAccountKey <String>] [-Run <String>] [-Argument <String>]
 [-SecureExecution] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dcec7-106">SetCustomScriptExtensionByUriLinks</span><span class="sxs-lookup"><span data-stu-id="dcec7-106">SetCustomScriptExtensionByUriLinks</span></span>
```
Set-AzureRmVMCustomScriptExtension [-FileUri <String[]>] [-Run <String>] [-Argument <String>]
 [-SecureExecution] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dcec7-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dcec7-107">DESCRIPTION</span></span>
<span data-ttu-id="dcec7-108">Командлет **Set-AzureRmVMCustomScriptExtension** добавляет расширение виртуальной машины специального сценария к виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="dcec7-108">The **Set-AzureRmVMCustomScriptExtension** cmdlet adds a custom script Virtual Machine Extension to a virtual machine.</span></span>
<span data-ttu-id="dcec7-109">Это расширение позволяет запускать собственные сценарии на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="dcec7-109">This extension lets you run your own scripts on the virtual machine.</span></span>

## <span data-ttu-id="dcec7-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dcec7-110">EXAMPLES</span></span>

### <span data-ttu-id="dcec7-111">Пример 1: Добавление настраиваемого сценария</span><span class="sxs-lookup"><span data-stu-id="dcec7-111">Example 1: Add a custom script</span></span>
```
PS C:\> Set-AzureRmVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -Location "Central US" -VMName "VirtualMachine07" -Name "ContosoTest" -TypeHandlerVersion "1.1" -StorageAccountName "Contoso" -StorageAccountKey <StorageKey> -FileName "ContosoScript.exe" -ContainerName "Scripts"
```

<span data-ttu-id="dcec7-112">Эта команда добавляет настраиваемый сценарий на виртуальную машину с именем VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="dcec7-112">This command adds a custom script to the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="dcec7-113">Файл сценария contososcript.exe.</span><span class="sxs-lookup"><span data-stu-id="dcec7-113">The script file is contososcript.exe.</span></span>

## <span data-ttu-id="dcec7-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dcec7-114">PARAMETERS</span></span>

### <span data-ttu-id="dcec7-115">-Аргумент</span><span class="sxs-lookup"><span data-stu-id="dcec7-115">-Argument</span></span>
<span data-ttu-id="dcec7-116">Задает аргументы, которые расширение сценария передает сценарию.</span><span class="sxs-lookup"><span data-stu-id="dcec7-116">Specifies arguments that the script extension passes to the script.</span></span>

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

### <span data-ttu-id="dcec7-117">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="dcec7-117">-ContainerName</span></span>
<span data-ttu-id="dcec7-118">Указывает имя контейнера хранилища Azure, в котором этот командлет хранит сценарий.</span><span class="sxs-lookup"><span data-stu-id="dcec7-118">Specifies the name of the Azure storage container where this cmdlet stores the script.</span></span>

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

### <span data-ttu-id="dcec7-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcec7-119">-DefaultProfile</span></span>
<span data-ttu-id="dcec7-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dcec7-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dcec7-121">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="dcec7-121">-DisableAutoUpgradeMinorVersion</span></span>
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

### <span data-ttu-id="dcec7-122">-FileName</span><span class="sxs-lookup"><span data-stu-id="dcec7-122">-FileName</span></span>
<span data-ttu-id="dcec7-123">Указывает имя файла сценария.</span><span class="sxs-lookup"><span data-stu-id="dcec7-123">Specifies the name of the script file.</span></span>

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

### <span data-ttu-id="dcec7-124">-FileUri</span><span class="sxs-lookup"><span data-stu-id="dcec7-124">-FileUri</span></span>
<span data-ttu-id="dcec7-125">Задает универсальный код ресурса (URI) файла сценария.</span><span class="sxs-lookup"><span data-stu-id="dcec7-125">Specifies the URI of the script file.</span></span>

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

### <span data-ttu-id="dcec7-126">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="dcec7-126">-ForceRerun</span></span>
<span data-ttu-id="dcec7-127">Указывает на то, что этот командлет принудительно выполняет повторное выполнение той же конфигурации на виртуальной машине без удаления и повторной установки расширения.</span><span class="sxs-lookup"><span data-stu-id="dcec7-127">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="dcec7-128">Значением может быть любая строка, отличающаяся от текущего значения.</span><span class="sxs-lookup"><span data-stu-id="dcec7-128">The value can be any string different from the current value.</span></span>

<span data-ttu-id="dcec7-129">Если forceUpdateTag не меняется, обновления открытых и защищенных параметров по-прежнему применяются обработчиком.</span><span class="sxs-lookup"><span data-stu-id="dcec7-129">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="dcec7-130">-Location</span><span class="sxs-lookup"><span data-stu-id="dcec7-130">-Location</span></span>
<span data-ttu-id="dcec7-131">Указывает расположение виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="dcec7-131">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="dcec7-132">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="dcec7-132">-Name</span></span>
<span data-ttu-id="dcec7-133">Указывает имя настраиваемого расширения сценария.</span><span class="sxs-lookup"><span data-stu-id="dcec7-133">Specifies the name of the custom script extension.</span></span>

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

### <span data-ttu-id="dcec7-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dcec7-134">-ResourceGroupName</span></span>
<span data-ttu-id="dcec7-135">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="dcec7-135">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="dcec7-136">-Run</span><span class="sxs-lookup"><span data-stu-id="dcec7-136">-Run</span></span>
<span data-ttu-id="dcec7-137">Задает команду для использования при выполнении сценария.</span><span class="sxs-lookup"><span data-stu-id="dcec7-137">Specifies the command to use that runs your script.</span></span>

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

### <span data-ttu-id="dcec7-138">-SecureExecution</span><span class="sxs-lookup"><span data-stu-id="dcec7-138">-SecureExecution</span></span>
<span data-ttu-id="dcec7-139">Указывает на то, что этот командлет гарантирует, что значение параметра *Run* не записывается на сервер или возвращается пользователю с помощью API получения расширения.</span><span class="sxs-lookup"><span data-stu-id="dcec7-139">Indicates that this cmdlet makes sure that the value of the *Run* parameter is not logged on the server or returned to the user by using the GET extension API.</span></span>
<span data-ttu-id="dcec7-140">Значение *Run* может содержать секреты или пароли, которые можно безопасно передавать в файл сценария.</span><span class="sxs-lookup"><span data-stu-id="dcec7-140">The value of *Run* might contain secrets or passwords to be passed to the script file securely.</span></span>

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

### <span data-ttu-id="dcec7-141">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="dcec7-141">-StorageAccountKey</span></span>
<span data-ttu-id="dcec7-142">Задает ключ для контейнера хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="dcec7-142">Specifies the key for the Azure storage container.</span></span>

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

### <span data-ttu-id="dcec7-143">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="dcec7-143">-StorageAccountName</span></span>
<span data-ttu-id="dcec7-144">Указывает имя учетной записи службы хранилища Azure, в которой этот командлет хранит сценарий.</span><span class="sxs-lookup"><span data-stu-id="dcec7-144">Specifies the name of the Azure storage account where this cmdlet stores the script.</span></span>

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

### <span data-ttu-id="dcec7-145">-StorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="dcec7-145">-StorageEndpointSuffix</span></span>
<span data-ttu-id="dcec7-146">Указывает суффикс конечной точки хранилища.</span><span class="sxs-lookup"><span data-stu-id="dcec7-146">Specifies the storage endpoint suffix.</span></span>

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

### <span data-ttu-id="dcec7-147">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="dcec7-147">-TypeHandlerVersion</span></span>
<span data-ttu-id="dcec7-148">Указывает версию расширения, используемую для этой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="dcec7-148">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="dcec7-149">Чтобы получить версию, выполните командлет Get-AzureRmVMExtensionImage со значением Microsoft. COMPUTE для параметра *PublisherName* и VMAccessAgent для параметра *Type* .</span><span class="sxs-lookup"><span data-stu-id="dcec7-149">To obtain the version, run the Get-AzureRmVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and VMAccessAgent for the *Type* parameter.</span></span>

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

### <span data-ttu-id="dcec7-150">-VMName</span><span class="sxs-lookup"><span data-stu-id="dcec7-150">-VMName</span></span>
<span data-ttu-id="dcec7-151">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="dcec7-151">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="dcec7-152">Этот командлет добавляет расширение настраиваемого сценария для виртуальной машины, указывающей этот параметр.</span><span class="sxs-lookup"><span data-stu-id="dcec7-152">This cmdlet adds the custom script extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="dcec7-153">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dcec7-153">-Confirm</span></span>
<span data-ttu-id="dcec7-154">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="dcec7-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dcec7-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dcec7-155">-WhatIf</span></span>
<span data-ttu-id="dcec7-156">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="dcec7-156">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="dcec7-157">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="dcec7-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dcec7-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcec7-158">CommonParameters</span></span>
<span data-ttu-id="dcec7-159">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dcec7-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcec7-160">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dcec7-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcec7-161">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dcec7-161">INPUTS</span></span>

## <span data-ttu-id="dcec7-162">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dcec7-162">OUTPUTS</span></span>

## <span data-ttu-id="dcec7-163">Пуск</span><span class="sxs-lookup"><span data-stu-id="dcec7-163">NOTES</span></span>

## <span data-ttu-id="dcec7-164">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dcec7-164">RELATED LINKS</span></span>

[<span data-ttu-id="dcec7-165">Get-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="dcec7-165">Get-AzureRmVMCustomScriptExtension</span></span>](./Get-AzureRmVMCustomScriptExtension.md)

[<span data-ttu-id="dcec7-166">Remove-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="dcec7-166">Remove-AzureRmVMCustomScriptExtension</span></span>](./Remove-AzureRmVMCustomScriptExtension.md)



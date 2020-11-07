---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 64AB1BAE-A756-43A8-A40F-10B746EA0946
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmcustomscriptextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMCustomScriptExtension.md
ms.openlocfilehash: f858ee5992c633674e52118a7d92554190107f75
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721686"
---
# <span data-ttu-id="9e23a-101">Set-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="9e23a-101">Set-AzVMCustomScriptExtension</span></span>

## <span data-ttu-id="9e23a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9e23a-102">SYNOPSIS</span></span>
<span data-ttu-id="9e23a-103">Добавляет на виртуальную машину расширение настраиваемого сценария.</span><span class="sxs-lookup"><span data-stu-id="9e23a-103">Adds a custom script extension to a virtual machine.</span></span>

## <span data-ttu-id="9e23a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9e23a-104">SYNTAX</span></span>

### <span data-ttu-id="9e23a-105">ByNameWithContainerAndFileNamesParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9e23a-105">ByNameWithContainerAndFileNamesParameterSet (Default)</span></span>
```
Set-AzVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 -ContainerName <String> -FileName <String[]> [-StorageAccountName <String>] [-StorageEndpointSuffix <String>]
 [-StorageAccountKey <String>] [-Run <String>] [-Argument <String>] [-SecureExecution]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e23a-106">ByNameWithFileUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e23a-106">ByNameWithFileUriParameterSet</span></span>
```
Set-AzVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-FileUri <String[]>] [-Run <String>] [-Argument <String>] [-SecureExecution] [-TypeHandlerVersion <String>]
 [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e23a-107">ByParentObjectWithContainerAndFileNamesParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e23a-107">ByParentObjectWithContainerAndFileNamesParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -Name <String> -VMObject <PSVirtualMachine> -ContainerName <String>
 -FileName <String[]> [-StorageAccountName <String>] [-StorageEndpointSuffix <String>]
 [-StorageAccountKey <String>] [-Run <String>] [-Argument <String>] [-SecureExecution]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e23a-108">ByParentObjectWithFileUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e23a-108">ByParentObjectWithFileUriParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -Name <String> -VMObject <PSVirtualMachine> [-FileUri <String[]>] [-Run <String>]
 [-Argument <String>] [-SecureExecution] [-TypeHandlerVersion <String>] [-Location <String>]
 [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e23a-109">ByResourceIdWithContainerAndFileNamesParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e23a-109">ByResourceIdWithContainerAndFileNamesParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -ResourceId <String> -ContainerName <String> -FileName <String[]>
 [-StorageAccountName <String>] [-StorageEndpointSuffix <String>] [-StorageAccountKey <String>] [-Run <String>]
 [-Argument <String>] [-SecureExecution] [-TypeHandlerVersion <String>] [-Location <String>]
 [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e23a-110">ByResourceIdWithFileUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e23a-110">ByResourceIdWithFileUriParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -ResourceId <String> [-FileUri <String[]>] [-Run <String>] [-Argument <String>]
 [-SecureExecution] [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion]
 [-ForceRerun <String>] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9e23a-111">ByInputObjectWithContainerAndFileNamesParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e23a-111">ByInputObjectWithContainerAndFileNamesParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -InputObject <VirtualMachineCustomScriptExtensionContext> -ContainerName <String>
 -FileName <String[]> [-StorageAccountName <String>] [-StorageEndpointSuffix <String>]
 [-StorageAccountKey <String>] [-Run <String>] [-Argument <String>] [-SecureExecution]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e23a-112">ByInputObjectWithFileUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e23a-112">ByInputObjectWithFileUriParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -InputObject <VirtualMachineCustomScriptExtensionContext> [-FileUri <String[]>]
 [-Run <String>] [-Argument <String>] [-SecureExecution] [-TypeHandlerVersion <String>] [-Location <String>]
 [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9e23a-113">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9e23a-113">DESCRIPTION</span></span>
<span data-ttu-id="9e23a-114">Командлет **Set-AzVMCustomScriptExtension** добавляет расширение виртуальной машины специального сценария к виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="9e23a-114">The **Set-AzVMCustomScriptExtension** cmdlet adds a custom script Virtual Machine Extension to a virtual machine.</span></span>
<span data-ttu-id="9e23a-115">Это расширение позволяет запускать собственные сценарии на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="9e23a-115">This extension lets you run your own scripts on the virtual machine.</span></span>

## <span data-ttu-id="9e23a-116">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9e23a-116">EXAMPLES</span></span>

### <span data-ttu-id="9e23a-117">Пример 1: Добавление настраиваемого сценария</span><span class="sxs-lookup"><span data-stu-id="9e23a-117">Example 1: Add a custom script</span></span>
```
PS C:\> Set-AzVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -Location "Central US" -VMName "VirtualMachine07" -Name "ContosoTest" -TypeHandlerVersion "1.1" -StorageAccountName "Contoso" -StorageAccountKey <StorageKey> -FileName "ContosoScript.exe" -ContainerName "Scripts"
```

<span data-ttu-id="9e23a-118">Эта команда добавляет настраиваемый сценарий на виртуальную машину с именем VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="9e23a-118">This command adds a custom script to the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="9e23a-119">Файл сценария contososcript.exe.</span><span class="sxs-lookup"><span data-stu-id="9e23a-119">The script file is contososcript.exe.</span></span>

## <span data-ttu-id="9e23a-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9e23a-120">PARAMETERS</span></span>

### <span data-ttu-id="9e23a-121">-Аргумент</span><span class="sxs-lookup"><span data-stu-id="9e23a-121">-Argument</span></span>
<span data-ttu-id="9e23a-122">Задает аргументы, которые расширение сценария передает сценарию.</span><span class="sxs-lookup"><span data-stu-id="9e23a-122">Specifies arguments that the script extension passes to the script.</span></span>

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

### <span data-ttu-id="9e23a-123">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="9e23a-123">-ContainerName</span></span>
<span data-ttu-id="9e23a-124">Указывает имя контейнера хранилища Azure, в котором этот командлет хранит сценарий.</span><span class="sxs-lookup"><span data-stu-id="9e23a-124">Specifies the name of the Azure storage container where this cmdlet stores the script.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameWithContainerAndFileNamesParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByParentObjectWithContainerAndFileNamesParameterSet, ByResourceIdWithContainerAndFileNamesParameterSet, ByInputObjectWithContainerAndFileNamesParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e23a-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e23a-125">-DefaultProfile</span></span>
<span data-ttu-id="9e23a-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9e23a-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9e23a-127">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="9e23a-127">-DisableAutoUpgradeMinorVersion</span></span>
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

### <span data-ttu-id="9e23a-128">-FileName</span><span class="sxs-lookup"><span data-stu-id="9e23a-128">-FileName</span></span>
<span data-ttu-id="9e23a-129">Указывает имя файла сценария.</span><span class="sxs-lookup"><span data-stu-id="9e23a-129">Specifies the name of the script file.</span></span> <span data-ttu-id="9e23a-130">Если файл хранится в хранилище BLOB-объектов Azure, значение имени файла задается с учетом регистра.</span><span class="sxs-lookup"><span data-stu-id="9e23a-130">If the file is stored in Azure Blob storage, the file name value is case-sensitive.</span></span> <span data-ttu-id="9e23a-131">Имена файлов, хранящихся в хранилище файлов Azure, не чувствительны к регистру.</span><span class="sxs-lookup"><span data-stu-id="9e23a-131">File names of files stored in Azure File storage are not case-sensitive.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByNameWithContainerAndFileNamesParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: ByParentObjectWithContainerAndFileNamesParameterSet, ByResourceIdWithContainerAndFileNamesParameterSet, ByInputObjectWithContainerAndFileNamesParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e23a-132">-FileUri</span><span class="sxs-lookup"><span data-stu-id="9e23a-132">-FileUri</span></span>
<span data-ttu-id="9e23a-133">Задает универсальный код ресурса (URI) файла сценария.</span><span class="sxs-lookup"><span data-stu-id="9e23a-133">Specifies the URI of the script file.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByNameWithFileUriParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: ByParentObjectWithFileUriParameterSet, ByResourceIdWithFileUriParameterSet, ByInputObjectWithFileUriParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e23a-134">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="9e23a-134">-ForceRerun</span></span>
<span data-ttu-id="9e23a-135">Указывает на то, что этот командлет принудительно выполняет повторное выполнение той же конфигурации на виртуальной машине без удаления и повторной установки расширения.</span><span class="sxs-lookup"><span data-stu-id="9e23a-135">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="9e23a-136">Значением может быть любая строка, отличающаяся от текущего значения.</span><span class="sxs-lookup"><span data-stu-id="9e23a-136">The value can be any string different from the current value.</span></span>
<span data-ttu-id="9e23a-137">Если forceUpdateTag не меняется, обновления открытых и защищенных параметров по-прежнему применяются обработчиком.</span><span class="sxs-lookup"><span data-stu-id="9e23a-137">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="9e23a-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9e23a-138">-InputObject</span></span>
<span data-ttu-id="9e23a-139">Объект расширения ВМ.</span><span class="sxs-lookup"><span data-stu-id="9e23a-139">VM extension object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.VirtualMachineCustomScriptExtensionContext
Parameter Sets: ByInputObjectWithContainerAndFileNamesParameterSet, ByInputObjectWithFileUriParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9e23a-140">-Location</span><span class="sxs-lookup"><span data-stu-id="9e23a-140">-Location</span></span>
<span data-ttu-id="9e23a-141">Указывает расположение виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="9e23a-141">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="9e23a-142">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9e23a-142">-Name</span></span>
<span data-ttu-id="9e23a-143">Указывает имя настраиваемого расширения сценария.</span><span class="sxs-lookup"><span data-stu-id="9e23a-143">Specifies the name of the custom script extension.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameWithContainerAndFileNamesParameterSet, ByNameWithFileUriParameterSet
Aliases: ExtensionName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByParentObjectWithContainerAndFileNamesParameterSet, ByParentObjectWithFileUriParameterSet
Aliases: ExtensionName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e23a-144">-Wait</span><span class="sxs-lookup"><span data-stu-id="9e23a-144">-NoWait</span></span>
<span data-ttu-id="9e23a-145">Запускает операцию и возвращает значение немедленно, прежде чем операция завершится.</span><span class="sxs-lookup"><span data-stu-id="9e23a-145">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="9e23a-146">Для определения того, успешно ли завершилась операция, используйте какой – то другой механизм.</span><span class="sxs-lookup"><span data-stu-id="9e23a-146">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="9e23a-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e23a-147">-ResourceGroupName</span></span>
<span data-ttu-id="9e23a-148">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="9e23a-148">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameWithContainerAndFileNamesParameterSet, ByNameWithFileUriParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e23a-149">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9e23a-149">-ResourceId</span></span>
<span data-ttu-id="9e23a-150">Расширение ИД виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="9e23a-150">VM extension ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdWithContainerAndFileNamesParameterSet, ByResourceIdWithFileUriParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e23a-151">-Run</span><span class="sxs-lookup"><span data-stu-id="9e23a-151">-Run</span></span>
<span data-ttu-id="9e23a-152">Задает команду для использования при выполнении сценария.</span><span class="sxs-lookup"><span data-stu-id="9e23a-152">Specifies the command to use that runs your script.</span></span>

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

### <span data-ttu-id="9e23a-153">-SecureExecution</span><span class="sxs-lookup"><span data-stu-id="9e23a-153">-SecureExecution</span></span>
<span data-ttu-id="9e23a-154">Указывает на то, что этот командлет гарантирует, что значение параметра *Run* не записывается на сервер или возвращается пользователю с помощью API получения расширения.</span><span class="sxs-lookup"><span data-stu-id="9e23a-154">Indicates that this cmdlet makes sure that the value of the *Run* parameter is not logged on the server or returned to the user by using the GET extension API.</span></span>
<span data-ttu-id="9e23a-155">Значение *Run* может содержать секреты или пароли, которые можно безопасно передавать в файл сценария.</span><span class="sxs-lookup"><span data-stu-id="9e23a-155">The value of *Run* might contain secrets or passwords to be passed to the script file securely.</span></span>

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

### <span data-ttu-id="9e23a-156">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="9e23a-156">-StorageAccountKey</span></span>
<span data-ttu-id="9e23a-157">Задает ключ для контейнера хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="9e23a-157">Specifies the key for the Azure storage container.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameWithContainerAndFileNamesParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByParentObjectWithContainerAndFileNamesParameterSet, ByResourceIdWithContainerAndFileNamesParameterSet, ByInputObjectWithContainerAndFileNamesParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e23a-158">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="9e23a-158">-StorageAccountName</span></span>
<span data-ttu-id="9e23a-159">Указывает имя учетной записи службы хранилища Azure, в которой этот командлет хранит сценарий.</span><span class="sxs-lookup"><span data-stu-id="9e23a-159">Specifies the name of the Azure storage account where this cmdlet stores the script.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameWithContainerAndFileNamesParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByParentObjectWithContainerAndFileNamesParameterSet, ByResourceIdWithContainerAndFileNamesParameterSet, ByInputObjectWithContainerAndFileNamesParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e23a-160">-StorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="9e23a-160">-StorageEndpointSuffix</span></span>
<span data-ttu-id="9e23a-161">Указывает суффикс конечной точки хранилища.</span><span class="sxs-lookup"><span data-stu-id="9e23a-161">Specifies the storage endpoint suffix.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameWithContainerAndFileNamesParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByParentObjectWithContainerAndFileNamesParameterSet, ByResourceIdWithContainerAndFileNamesParameterSet, ByInputObjectWithContainerAndFileNamesParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e23a-162">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="9e23a-162">-TypeHandlerVersion</span></span>
<span data-ttu-id="9e23a-163">Указывает версию расширения, используемую для этой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="9e23a-163">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="9e23a-164">Чтобы получить версию, выполните командлет Get-AzVMExtensionImage со значением Microsoft. COMPUTE для параметра *PublisherName* и CustomScriptExtension для параметра *Type* .</span><span class="sxs-lookup"><span data-stu-id="9e23a-164">To obtain the version, run the Get-AzVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and CustomScriptExtension for the *Type* parameter.</span></span>

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

### <span data-ttu-id="9e23a-165">-VMName</span><span class="sxs-lookup"><span data-stu-id="9e23a-165">-VMName</span></span>
<span data-ttu-id="9e23a-166">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="9e23a-166">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="9e23a-167">Этот командлет добавляет расширение настраиваемого сценария для виртуальной машины, указывающей этот параметр.</span><span class="sxs-lookup"><span data-stu-id="9e23a-167">This cmdlet adds the custom script extension for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameWithContainerAndFileNamesParameterSet, ByNameWithFileUriParameterSet
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e23a-168">-VMObject</span><span class="sxs-lookup"><span data-stu-id="9e23a-168">-VMObject</span></span>
<span data-ttu-id="9e23a-169">Объект ВМ.</span><span class="sxs-lookup"><span data-stu-id="9e23a-169">VM object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: ByParentObjectWithContainerAndFileNamesParameterSet, ByParentObjectWithFileUriParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9e23a-170">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9e23a-170">-Confirm</span></span>
<span data-ttu-id="9e23a-171">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9e23a-171">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e23a-172">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e23a-172">-WhatIf</span></span>
<span data-ttu-id="9e23a-173">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9e23a-173">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e23a-174">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9e23a-174">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e23a-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e23a-175">CommonParameters</span></span>
<span data-ttu-id="9e23a-176">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9e23a-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e23a-177">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9e23a-177">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e23a-178">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9e23a-178">INPUTS</span></span>

### <span data-ttu-id="9e23a-179">System. String</span><span class="sxs-lookup"><span data-stu-id="9e23a-179">System.String</span></span>

### <span data-ttu-id="9e23a-180">System. String []</span><span class="sxs-lookup"><span data-stu-id="9e23a-180">System.String[]</span></span>

### <span data-ttu-id="9e23a-181">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="9e23a-181">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="9e23a-182">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9e23a-182">OUTPUTS</span></span>

### <span data-ttu-id="9e23a-183">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="9e23a-183">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="9e23a-184">Пуск</span><span class="sxs-lookup"><span data-stu-id="9e23a-184">NOTES</span></span>

## <span data-ttu-id="9e23a-185">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9e23a-185">RELATED LINKS</span></span>

[<span data-ttu-id="9e23a-186">Get-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="9e23a-186">Get-AzVMCustomScriptExtension</span></span>](./Get-AzVMCustomScriptExtension.md)

[<span data-ttu-id="9e23a-187">Remove-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="9e23a-187">Remove-AzVMCustomScriptExtension</span></span>](./Remove-AzVMCustomScriptExtension.md)



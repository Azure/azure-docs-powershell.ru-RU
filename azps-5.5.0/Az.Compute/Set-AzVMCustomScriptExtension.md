---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 64AB1BAE-A756-43A8-A40F-10B746EA0946
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmcustomscriptextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMCustomScriptExtension.md
ms.openlocfilehash: 69b6dec11f0135803320bb7b58bdb8362aaee26e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100211540"
---
# <span data-ttu-id="5a18a-101">Set-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="5a18a-101">Set-AzVMCustomScriptExtension</span></span>

## <span data-ttu-id="5a18a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a18a-102">SYNOPSIS</span></span>
<span data-ttu-id="5a18a-103">Добавляет настраиваемые расширения сценариев на виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="5a18a-103">Adds a custom script extension to a virtual machine.</span></span>

## <span data-ttu-id="5a18a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5a18a-104">SYNTAX</span></span>

### <span data-ttu-id="5a18a-105">ByNameWithContainerAndFileNamesParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5a18a-105">ByNameWithContainerAndFileNamesParameterSet (Default)</span></span>
```
Set-AzVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 -ContainerName <String> -FileName <String[]> [-StorageAccountName <String>] [-StorageEndpointSuffix <String>]
 [-StorageAccountKey <String>] [-Run <String>] [-Argument <String>] [-SecureExecution]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a18a-106">ByNameWithFileUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="5a18a-106">ByNameWithFileUriParameterSet</span></span>
```
Set-AzVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-FileUri <String[]>] [-Run <String>] [-Argument <String>] [-SecureExecution] [-TypeHandlerVersion <String>]
 [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a18a-107">ByParentObjectWithContainerAndFileNamesParameterSet</span><span class="sxs-lookup"><span data-stu-id="5a18a-107">ByParentObjectWithContainerAndFileNamesParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -Name <String> -VMObject <PSVirtualMachine> -ContainerName <String>
 -FileName <String[]> [-StorageAccountName <String>] [-StorageEndpointSuffix <String>]
 [-StorageAccountKey <String>] [-Run <String>] [-Argument <String>] [-SecureExecution]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a18a-108">ByParentObjectWithFileUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="5a18a-108">ByParentObjectWithFileUriParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -Name <String> -VMObject <PSVirtualMachine> [-FileUri <String[]>] [-Run <String>]
 [-Argument <String>] [-SecureExecution] [-TypeHandlerVersion <String>] [-Location <String>]
 [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a18a-109">ByResourceIdWithContainerAndFileNamesParameterSet</span><span class="sxs-lookup"><span data-stu-id="5a18a-109">ByResourceIdWithContainerAndFileNamesParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -ResourceId <String> -ContainerName <String> -FileName <String[]>
 [-StorageAccountName <String>] [-StorageEndpointSuffix <String>] [-StorageAccountKey <String>] [-Run <String>]
 [-Argument <String>] [-SecureExecution] [-TypeHandlerVersion <String>] [-Location <String>]
 [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a18a-110">ByResourceIdWithFileUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="5a18a-110">ByResourceIdWithFileUriParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -ResourceId <String> [-FileUri <String[]>] [-Run <String>] [-Argument <String>]
 [-SecureExecution] [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion]
 [-ForceRerun <String>] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5a18a-111">ByInputObjectWithContainerAndFileNamesParameterSet</span><span class="sxs-lookup"><span data-stu-id="5a18a-111">ByInputObjectWithContainerAndFileNamesParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -InputObject <VirtualMachineCustomScriptExtensionContext> -ContainerName <String>
 -FileName <String[]> [-StorageAccountName <String>] [-StorageEndpointSuffix <String>]
 [-StorageAccountKey <String>] [-Run <String>] [-Argument <String>] [-SecureExecution]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a18a-112">ByInputObjectWithFileUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="5a18a-112">ByInputObjectWithFileUriParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -InputObject <VirtualMachineCustomScriptExtensionContext> [-FileUri <String[]>]
 [-Run <String>] [-Argument <String>] [-SecureExecution] [-TypeHandlerVersion <String>] [-Location <String>]
 [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a18a-113">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5a18a-113">DESCRIPTION</span></span>
<span data-ttu-id="5a18a-114">Cmdlet **Set-AzVMCustomScriptExtension** добавляет настраиваемый сценарий расширения виртуальной машины на виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="5a18a-114">The **Set-AzVMCustomScriptExtension** cmdlet adds a custom script Virtual Machine Extension to a virtual machine.</span></span>
<span data-ttu-id="5a18a-115">Это расширение позволяет запускать собственные сценарии на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="5a18a-115">This extension lets you run your own scripts on the virtual machine.</span></span>

## <span data-ttu-id="5a18a-116">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5a18a-116">EXAMPLES</span></span>

### <span data-ttu-id="5a18a-117">Пример 1. Добавление пользовательского сценария</span><span class="sxs-lookup"><span data-stu-id="5a18a-117">Example 1: Add a custom script</span></span>
```powershell
PS C:\> Set-AzVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -Location "Central US" -VMName "VirtualMachine07" -Name "ContosoTest" -TypeHandlerVersion "1.1" -StorageAccountName "Contoso" -StorageAccountKey <StorageKey> -FileName "ContosoScript.exe" -ContainerName "Scripts"
```

<span data-ttu-id="5a18a-118">Эта команда добавляет настраиваемый сценарий на виртуальную машину с именем VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="5a18a-118">This command adds a custom script to the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="5a18a-119">Файл сценария contososcript.exe.</span><span class="sxs-lookup"><span data-stu-id="5a18a-119">The script file is contososcript.exe.</span></span>

### <span data-ttu-id="5a18a-120">Пример 2</span><span class="sxs-lookup"><span data-stu-id="5a18a-120">Example 2</span></span>

<span data-ttu-id="5a18a-121">Добавляет настраиваемые расширения сценариев на виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="5a18a-121">Adds a custom script extension to a virtual machine.</span></span> <span data-ttu-id="5a18a-122">(autogenerated)</span><span class="sxs-lookup"><span data-stu-id="5a18a-122">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzVMCustomScriptExtension -Argument <String> -ContainerName 'Scripts' -DefaultProfile <IAzureContextContainer> -FileName 'ContosoScript.exe' -Location 'Central US' -Name 'ContosoTest' -ResourceGroupName 'ResourceGroup11' -Run 'myScript.ps1' -SecureExecution -StorageAccountKey <String> -StorageAccountName 'Contoso' -TypeHandlerVersion '1.1' -VMName 'VirtualMachine07'
```

## <span data-ttu-id="5a18a-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5a18a-123">PARAMETERS</span></span>

### <span data-ttu-id="5a18a-124">-Аргумент</span><span class="sxs-lookup"><span data-stu-id="5a18a-124">-Argument</span></span>
<span data-ttu-id="5a18a-125">Указывает аргументы, которые расширение сценария передает сценарию.</span><span class="sxs-lookup"><span data-stu-id="5a18a-125">Specifies arguments that the script extension passes to the script.</span></span>

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

### <span data-ttu-id="5a18a-126">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="5a18a-126">-ContainerName</span></span>
<span data-ttu-id="5a18a-127">Имя контейнера хранилища Azure, в котором хранится сценарий.</span><span class="sxs-lookup"><span data-stu-id="5a18a-127">Specifies the name of the Azure storage container where this cmdlet stores the script.</span></span>

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

### <span data-ttu-id="5a18a-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a18a-128">-DefaultProfile</span></span>
<span data-ttu-id="5a18a-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5a18a-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5a18a-130">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="5a18a-130">-DisableAutoUpgradeMinorVersion</span></span>
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

### <span data-ttu-id="5a18a-131">-FileName</span><span class="sxs-lookup"><span data-stu-id="5a18a-131">-FileName</span></span>
<span data-ttu-id="5a18a-132">Указывает имя файла сценария.</span><span class="sxs-lookup"><span data-stu-id="5a18a-132">Specifies the name of the script file.</span></span> <span data-ttu-id="5a18a-133">Если файл хранится в хранилище BLOB-файлов Azure, в имени файла в этом случае внося важные данные.</span><span class="sxs-lookup"><span data-stu-id="5a18a-133">If the file is stored in Azure Blob storage, the file name value is case-sensitive.</span></span> <span data-ttu-id="5a18a-134">Имена файлов, хранимых в хранилище файлов Azure, нечувствительны к делу.</span><span class="sxs-lookup"><span data-stu-id="5a18a-134">File names of files stored in Azure File storage are not case-sensitive.</span></span>

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

### <span data-ttu-id="5a18a-135">-FileUri</span><span class="sxs-lookup"><span data-stu-id="5a18a-135">-FileUri</span></span>
<span data-ttu-id="5a18a-136">Определяет URI файла сценария.</span><span class="sxs-lookup"><span data-stu-id="5a18a-136">Specifies the URI of the script file.</span></span>

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

### <span data-ttu-id="5a18a-137">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="5a18a-137">-ForceRerun</span></span>
<span data-ttu-id="5a18a-138">Указывает на то, что этот cmdlet приостановит повторение одной и той же конфигурации расширения на виртуальной машине, не устраив и повторно установив расширение.</span><span class="sxs-lookup"><span data-stu-id="5a18a-138">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="5a18a-139">Значение может быть любой строкой, которая отличается от текущей.</span><span class="sxs-lookup"><span data-stu-id="5a18a-139">The value can be any string different from the current value.</span></span>
<span data-ttu-id="5a18a-140">Если параметр forceUpdateTag не изменился, обработник по-прежнему применяет обновления общедоступных или защищенных параметров.</span><span class="sxs-lookup"><span data-stu-id="5a18a-140">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="5a18a-141">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5a18a-141">-InputObject</span></span>
<span data-ttu-id="5a18a-142">Объект расширения VM.</span><span class="sxs-lookup"><span data-stu-id="5a18a-142">VM extension object.</span></span>

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

### <span data-ttu-id="5a18a-143">-Location</span><span class="sxs-lookup"><span data-stu-id="5a18a-143">-Location</span></span>
<span data-ttu-id="5a18a-144">Определяет расположение виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="5a18a-144">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="5a18a-145">-Name</span><span class="sxs-lookup"><span data-stu-id="5a18a-145">-Name</span></span>
<span data-ttu-id="5a18a-146">Указывает имя настраиваемого расширения сценария.</span><span class="sxs-lookup"><span data-stu-id="5a18a-146">Specifies the name of the custom script extension.</span></span>

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

### <span data-ttu-id="5a18a-147">-NoWait</span><span class="sxs-lookup"><span data-stu-id="5a18a-147">-NoWait</span></span>
<span data-ttu-id="5a18a-148">Начинает операцию и возвращает ее немедленно до ее завершения.</span><span class="sxs-lookup"><span data-stu-id="5a18a-148">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="5a18a-149">Чтобы определить успешное завершение операции, используйте другой механизм.</span><span class="sxs-lookup"><span data-stu-id="5a18a-149">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="5a18a-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a18a-150">-ResourceGroupName</span></span>
<span data-ttu-id="5a18a-151">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="5a18a-151">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="5a18a-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5a18a-152">-ResourceId</span></span>
<span data-ttu-id="5a18a-153">Расширение VM ResourceID.</span><span class="sxs-lookup"><span data-stu-id="5a18a-153">VM extension ResourceID.</span></span>

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

### <span data-ttu-id="5a18a-154">-Run</span><span class="sxs-lookup"><span data-stu-id="5a18a-154">-Run</span></span>
<span data-ttu-id="5a18a-155">Указывает команду, которая будет использовать сценарий.</span><span class="sxs-lookup"><span data-stu-id="5a18a-155">Specifies the command to use that runs your script.</span></span>

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

### <span data-ttu-id="5a18a-156">-SecureExecution</span><span class="sxs-lookup"><span data-stu-id="5a18a-156">-SecureExecution</span></span>
<span data-ttu-id="5a18a-157">Этот cmdlet позволяет убедиться, что значение параметра *Run* не было возвращено с сервера или возвращено пользователю с помощью API расширения GET.</span><span class="sxs-lookup"><span data-stu-id="5a18a-157">Indicates that this cmdlet makes sure that the value of the *Run* parameter is not logged on the server or returned to the user by using the GET extension API.</span></span>
<span data-ttu-id="5a18a-158">Значение *"Выполнить"* может содержать секрет или пароли, которые необходимо безопасно передать файлу сценария.</span><span class="sxs-lookup"><span data-stu-id="5a18a-158">The value of *Run* might contain secrets or passwords to be passed to the script file securely.</span></span>

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

### <span data-ttu-id="5a18a-159">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="5a18a-159">-StorageAccountKey</span></span>
<span data-ttu-id="5a18a-160">Ключ для контейнера хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="5a18a-160">Specifies the key for the Azure storage container.</span></span>

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

### <span data-ttu-id="5a18a-161">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="5a18a-161">-StorageAccountName</span></span>
<span data-ttu-id="5a18a-162">Указывает имя учетной записи хранилища Azure, в которой этот cmdlet хранит сценарий.</span><span class="sxs-lookup"><span data-stu-id="5a18a-162">Specifies the name of the Azure storage account where this cmdlet stores the script.</span></span>

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

### <span data-ttu-id="5a18a-163">-StorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="5a18a-163">-StorageEndpointSuffix</span></span>
<span data-ttu-id="5a18a-164">Определяет суффикс конечной точки хранения.</span><span class="sxs-lookup"><span data-stu-id="5a18a-164">Specifies the storage endpoint suffix.</span></span>

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

### <span data-ttu-id="5a18a-165">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="5a18a-165">-TypeHandlerVersion</span></span>
<span data-ttu-id="5a18a-166">Определяет версию расширения, используемого для этой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="5a18a-166">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="5a18a-167">Чтобы получить версию, запустите Get-AzVMExtensionImage Microsoft.Compute для параметра *PublisherName* и CustomScriptExtension для параметра *Type.*</span><span class="sxs-lookup"><span data-stu-id="5a18a-167">To obtain the version, run the Get-AzVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and CustomScriptExtension for the *Type* parameter.</span></span>

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

### <span data-ttu-id="5a18a-168">-VMName</span><span class="sxs-lookup"><span data-stu-id="5a18a-168">-VMName</span></span>
<span data-ttu-id="5a18a-169">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="5a18a-169">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="5a18a-170">Этот cmdlet добавляет расширение настраиваемого сценария для виртуальной машины, указанное этим параметром.</span><span class="sxs-lookup"><span data-stu-id="5a18a-170">This cmdlet adds the custom script extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="5a18a-171">-VMObject</span><span class="sxs-lookup"><span data-stu-id="5a18a-171">-VMObject</span></span>
<span data-ttu-id="5a18a-172">Объект VM.</span><span class="sxs-lookup"><span data-stu-id="5a18a-172">VM object.</span></span>

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

### <span data-ttu-id="5a18a-173">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5a18a-173">-Confirm</span></span>
<span data-ttu-id="5a18a-174">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="5a18a-174">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a18a-175">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a18a-175">-WhatIf</span></span>
<span data-ttu-id="5a18a-176">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a18a-176">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a18a-177">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="5a18a-177">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a18a-178">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a18a-178">CommonParameters</span></span>
<span data-ttu-id="5a18a-179">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a18a-179">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a18a-180">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5a18a-180">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a18a-181">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5a18a-181">INPUTS</span></span>

### <span data-ttu-id="5a18a-182">System.String</span><span class="sxs-lookup"><span data-stu-id="5a18a-182">System.String</span></span>

### <span data-ttu-id="5a18a-183">System.String[]</span><span class="sxs-lookup"><span data-stu-id="5a18a-183">System.String[]</span></span>

### <span data-ttu-id="5a18a-184">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="5a18a-184">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="5a18a-185">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5a18a-185">OUTPUTS</span></span>

### <span data-ttu-id="5a18a-186">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="5a18a-186">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="5a18a-187">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5a18a-187">NOTES</span></span>

## <span data-ttu-id="5a18a-188">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5a18a-188">RELATED LINKS</span></span>

[<span data-ttu-id="5a18a-189">Get-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="5a18a-189">Get-AzVMCustomScriptExtension</span></span>](./Get-AzVMCustomScriptExtension.md)

[<span data-ttu-id="5a18a-190">Remove-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="5a18a-190">Remove-AzVMCustomScriptExtension</span></span>](./Remove-AzVMCustomScriptExtension.md)



---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/update-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Update-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Update-AzConnectedMachineExtension.md
ms.openlocfilehash: 95334b4f67685183e499518b068f1003f5bb6547
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248728"
---
# <span data-ttu-id="75527-101">Update-AzConnectedMachineExtension</span><span class="sxs-lookup"><span data-stu-id="75527-101">Update-AzConnectedMachineExtension</span></span>

## <span data-ttu-id="75527-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="75527-102">SYNOPSIS</span></span>
<span data-ttu-id="75527-103">Операция, позволяющая создать или обновить расширение.</span><span class="sxs-lookup"><span data-stu-id="75527-103">The operation to create or update the extension.</span></span>

## <span data-ttu-id="75527-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="75527-104">SYNTAX</span></span>

### <span data-ttu-id="75527-105">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="75527-105">UpdateExpanded (Default)</span></span>
```
Update-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-AutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-ProtectedSetting <IMachineExtensionUpdatePropertiesProtectedSettings>] [-Publisher <String>]
 [-Setting <IMachineExtensionUpdatePropertiesSettings>] [-Tag <Hashtable>] [-Type <String>]
 [-TypeHandlerVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="75527-106">Обновление</span><span class="sxs-lookup"><span data-stu-id="75527-106">Update</span></span>
```
Update-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -ExtensionParameter <IMachineExtensionUpdate> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="75527-107">UpdateViaIdentity</span><span class="sxs-lookup"><span data-stu-id="75527-107">UpdateViaIdentity</span></span>
```
Update-AzConnectedMachineExtension -InputObject <IConnectedMachineIdentity>
 -ExtensionParameter <IMachineExtensionUpdate> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="75527-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="75527-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzConnectedMachineExtension -InputObject <IConnectedMachineIdentity> [-AutoUpgradeMinorVersion]
 [-ForceRerun <String>] [-ProtectedSetting <IMachineExtensionUpdatePropertiesProtectedSettings>]
 [-Publisher <String>] [-Setting <IMachineExtensionUpdatePropertiesSettings>] [-Tag <Hashtable>]
 [-Type <String>] [-TypeHandlerVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="75527-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="75527-109">DESCRIPTION</span></span>
<span data-ttu-id="75527-110">Операция, позволяющая создать или обновить расширение.</span><span class="sxs-lookup"><span data-stu-id="75527-110">The operation to create or update the extension.</span></span>

## <span data-ttu-id="75527-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="75527-111">EXAMPLES</span></span>

### <span data-ttu-id="75527-112">Пример 1: обновление расширения</span><span class="sxs-lookup"><span data-stu-id="75527-112">Example 1: Update an extension</span></span>
```powershell
PS C:\> $splat = @{
            ResourceGroupName = "connectedMachines"
            MachineName = "linux-eastus1_1"
            Name = "customScript"
            Settings = @{
                commandToExecute = "ls -l"
            }
        }
PS C:\> Update-AzConnectedMachineExtension @splat

Name         Location ProvisioningState
----         -------- -----------------
customScript eastus   Succeeded
```

<span data-ttu-id="75527-113">Обновляет расширение на определенном компьютере.</span><span class="sxs-lookup"><span data-stu-id="75527-113">Updates an extension on a specific machine.</span></span>

### <span data-ttu-id="75527-114">Пример 2: обновление расширения с расположением, указанным через конвейер</span><span class="sxs-lookup"><span data-stu-id="75527-114">Example 2: Update an extension with location specified via the pipeline</span></span>
```powershell
PS C:\> $extToUpdate = Get-AzConnectedMachineExtension -ResourceGroupName connectedMachines -MachineName linux-eastus1_1 -Name customScript
PS C:\> $extToUpdate | Update-AzConnectedMachineExtension -Settings @{
                commandToExecute = "ls -l"
            }

Name         Location ProvisioningState
----         -------- -----------------
customScript eastus   Succeeded
```

<span data-ttu-id="75527-115">Обновляет определенное расширение, передаваемое через конвейер.</span><span class="sxs-lookup"><span data-stu-id="75527-115">Updates a specific extension passed in via the pipeline.</span></span>
<span data-ttu-id="75527-116">Здесь мы используем расширение, передаваемое с помощью конвейера, чтобы определить, на какой добавочный номер следует работать, и указать, что мы будем менять с помощью обычных параметров (например, `-Settings` ).</span><span class="sxs-lookup"><span data-stu-id="75527-116">Here we are using the extension passed in via the pipeline to help us identify which extension we want to operate on and are specifying what we want to change via the normal parameters (like `-Settings`)</span></span>

### <span data-ttu-id="75527-117">Пример 3: обновление расширения с помощью параметров расширения, указанных через конвейер</span><span class="sxs-lookup"><span data-stu-id="75527-117">Example 3: Update an extension with extension parameters specified via the pipeline</span></span>
```powershell
PS C:\> $extToUpdate = Get-AzConnectedMachineExtension -ResourceGroupName connectedMachines -MachineName linux-eastus1_1 -Name customScript
PS C:\> # Update the settings on the object that will be used via the pipeline
PS C:\> $extToUpdate.Setting.commandToExecute = "ls -l"
PS C:\> $splat = @{
            ResourceGroupName = "connectedMachines"
            MachineName = "linux-eastus1_1"
            Name = "customScript"
        }
PS C:\> $extToUpdate | Update-AzConnectedMachineExtension @splat

Name         Location ProvisioningState
----         -------- -----------------
customScript eastus   Succeeded
```

<span data-ttu-id="75527-118">Обновляет определенное расширение, передаваемое через конвейер.</span><span class="sxs-lookup"><span data-stu-id="75527-118">Updates a specific extension passed in via the pipeline.</span></span>
<span data-ttu-id="75527-119">Здесь мы используем расширение, передаваемое с помощью конвейера, чтобы предоставить изменения, которые мы хотели бы вносить на расширение.</span><span class="sxs-lookup"><span data-stu-id="75527-119">Here we are using the extension passed in via the pipeline to provide the changes we want to make on the extension.</span></span>
<span data-ttu-id="75527-120">Расположение расширения не извлекается с помощью конвейера, а через параметры, заданные в обычном режиме (с помощью параметра Splat).</span><span class="sxs-lookup"><span data-stu-id="75527-120">The location of the extension is not retrieved via the pipeline but rather via the parameters specified normally (by the splat parameter).</span></span>

### <span data-ttu-id="75527-121">Пример 4: использование объекта расширения в качестве местоположения и параметров для обновления</span><span class="sxs-lookup"><span data-stu-id="75527-121">Example 4: Using an extension object as both the location and parameters for updating</span></span>
```powershell
PS C:\> $extToUpdate = Get-AzConnectedMachineExtension -ResourceGroupName connectedMachines -MachineName linux-eastus1_1 -Name customScript
PS C:\> # Update the settings on the object that will be used via the pipeline
PS C:\> $extToUpdate.Setting.commandToExecute = "ls -l"
PS C:\> $extToUpdate | Update-AzConnectedMachineExtension -ExtensionParameter $extToUpdate

Name         Location ProvisioningState
----         -------- -----------------
customScript eastus   Succeeded
```

<span data-ttu-id="75527-122">Обновляет определенное расширение, передаваемое через конвейер.</span><span class="sxs-lookup"><span data-stu-id="75527-122">Updates a specific extension passed in via the pipeline.</span></span>
<span data-ttu-id="75527-123">Здесь мы используем расширение, передаваемое через конвейер, чтобы помочь нам определить, на какое расширение мы будем работать.</span><span class="sxs-lookup"><span data-stu-id="75527-123">Here we are using the extension passed in via the pipeline to help us identify which extension we want to operate on.</span></span>
<span data-ttu-id="75527-124">Кроме того, мы используем параметры объекта расширения, чтобы указать, что нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="75527-124">In addition to that, we are using the parameters of the extension object to specify what to update.</span></span>

## <span data-ttu-id="75527-125">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="75527-125">PARAMETERS</span></span>

### <span data-ttu-id="75527-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="75527-126">-AsJob</span></span>
<span data-ttu-id="75527-127">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="75527-127">Run the command as a job</span></span>

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

### <span data-ttu-id="75527-128">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="75527-128">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="75527-129">Указывает, должно ли расширение использовать более новую вспомогательную версию, если она доступна во время развертывания.</span><span class="sxs-lookup"><span data-stu-id="75527-129">Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span>
<span data-ttu-id="75527-130">Однако после развертывания расширение не будет обновлять дополнительные версии, если только повторно не развернуто, даже если для этого свойства задано значение true.</span><span class="sxs-lookup"><span data-stu-id="75527-130">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75527-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75527-131">-DefaultProfile</span></span>
<span data-ttu-id="75527-132">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="75527-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75527-133">-ExtensionParameter</span><span class="sxs-lookup"><span data-stu-id="75527-133">-ExtensionParameter</span></span>
<span data-ttu-id="75527-134">В этой статье описано обновление для компьютера с расширением.</span><span class="sxs-lookup"><span data-stu-id="75527-134">Describes a Machine Extension Update.</span></span>
<span data-ttu-id="75527-135">Для конструирования ознакомьтесь с разделом "Заметки" для свойств EXTENSIONPARAMETER и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="75527-135">To construct, see NOTES section for EXTENSIONPARAMETER properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionUpdate
Parameter Sets: Update, UpdateViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="75527-136">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="75527-136">-ForceRerun</span></span>
<span data-ttu-id="75527-137">Как следует принудительно обновлять обработчик расширений, даже если конфигурация расширения не изменилась.</span><span class="sxs-lookup"><span data-stu-id="75527-137">How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75527-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="75527-138">-InputObject</span></span>
<span data-ttu-id="75527-139">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="75527-139">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity
Parameter Sets: UpdateViaIdentity, UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="75527-140">-MachineName</span><span class="sxs-lookup"><span data-stu-id="75527-140">-MachineName</span></span>
<span data-ttu-id="75527-141">Имя компьютера, на котором нужно создать или обновить расширение.</span><span class="sxs-lookup"><span data-stu-id="75527-141">The name of the machine where the extension should be created or updated.</span></span>

```yaml
Type: System.String
Parameter Sets: Update, UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75527-142">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="75527-142">-Name</span></span>
<span data-ttu-id="75527-143">Имя расширения компьютера.</span><span class="sxs-lookup"><span data-stu-id="75527-143">The name of the machine extension.</span></span>

```yaml
Type: System.String
Parameter Sets: Update, UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75527-144">-Wait</span><span class="sxs-lookup"><span data-stu-id="75527-144">-NoWait</span></span>
<span data-ttu-id="75527-145">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="75527-145">Run the command asynchronously</span></span>

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

### <span data-ttu-id="75527-146">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="75527-146">-ProtectedSetting</span></span>
<span data-ttu-id="75527-147">Расширение может содержать либо protectedSettings, либо protectedSettingsFromKeyVault, или вообще не защищенные параметры.</span><span class="sxs-lookup"><span data-stu-id="75527-147">The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionUpdatePropertiesProtectedSettings
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases: ProtectedSettings

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75527-148">-Publisher</span><span class="sxs-lookup"><span data-stu-id="75527-148">-Publisher</span></span>
<span data-ttu-id="75527-149">Имя издателя обработчика расширений.</span><span class="sxs-lookup"><span data-stu-id="75527-149">The name of the extension handler publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75527-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75527-150">-ResourceGroupName</span></span>
<span data-ttu-id="75527-151">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="75527-151">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Update, UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75527-152">-Параметр</span><span class="sxs-lookup"><span data-stu-id="75527-152">-Setting</span></span>
<span data-ttu-id="75527-153">Отформатированные общедоступные параметры JSON для расширения.</span><span class="sxs-lookup"><span data-stu-id="75527-153">Json formatted public settings for the extension.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionUpdatePropertiesSettings
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases: Settings

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75527-154">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="75527-154">-SubscriptionId</span></span>
<span data-ttu-id="75527-155">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="75527-155">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="75527-156">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="75527-156">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Update, UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75527-157">-Тег</span><span class="sxs-lookup"><span data-stu-id="75527-157">-Tag</span></span>
<span data-ttu-id="75527-158">Теги ресурсов</span><span class="sxs-lookup"><span data-stu-id="75527-158">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75527-159">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="75527-159">-Type</span></span>
<span data-ttu-id="75527-160">Указывает тип расширения; Пример: "CustomScriptExtension".</span><span class="sxs-lookup"><span data-stu-id="75527-160">Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75527-161">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="75527-161">-TypeHandlerVersion</span></span>
<span data-ttu-id="75527-162">Указывает версию обработчика сценария.</span><span class="sxs-lookup"><span data-stu-id="75527-162">Specifies the version of the script handler.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75527-163">-Confirm</span><span class="sxs-lookup"><span data-stu-id="75527-163">-Confirm</span></span>
<span data-ttu-id="75527-164">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="75527-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75527-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75527-165">-WhatIf</span></span>
<span data-ttu-id="75527-166">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="75527-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75527-167">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="75527-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75527-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75527-168">CommonParameters</span></span>
<span data-ttu-id="75527-169">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="75527-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75527-170">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="75527-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75527-171">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="75527-171">INPUTS</span></span>

### <span data-ttu-id="75527-172">Microsoft. Azure. PowerShell. командлеты. ConnectedMachine. Models. Api20200802. IMachineExtensionUpdate</span><span class="sxs-lookup"><span data-stu-id="75527-172">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionUpdate</span></span>

### <span data-ttu-id="75527-173">Microsoft. Azure. PowerShell. командлеты. ConnectedMachine. Models. IConnectedMachineIdentity</span><span class="sxs-lookup"><span data-stu-id="75527-173">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span></span>

## <span data-ttu-id="75527-174">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="75527-174">OUTPUTS</span></span>

### <span data-ttu-id="75527-175">Microsoft. Azure. PowerShell. командлеты. ConnectedMachine. Models. Api20200802. IMachineExtension</span><span class="sxs-lookup"><span data-stu-id="75527-175">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

## <span data-ttu-id="75527-176">Пуск</span><span class="sxs-lookup"><span data-stu-id="75527-176">NOTES</span></span>

<span data-ttu-id="75527-177">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="75527-177">ALIASES</span></span>

<span data-ttu-id="75527-178">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="75527-178">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="75527-179">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="75527-179">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="75527-180">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="75527-180">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="75527-181">EXTENSIONPARAMETER <IMachineExtensionUpdate> : описывает обновление для компьютера с расширением.</span><span class="sxs-lookup"><span data-stu-id="75527-181">EXTENSIONPARAMETER <IMachineExtensionUpdate>: Describes a Machine Extension Update.</span></span>
  - <span data-ttu-id="75527-182">`[Tag <IUpdateResourceTags>]`: Теги ресурсов</span><span class="sxs-lookup"><span data-stu-id="75527-182">`[Tag <IUpdateResourceTags>]`: Resource tags</span></span>
    - <span data-ttu-id="75527-183">`[(Any) <String>]`: Это указывает на то, что в этот объект можно добавить любое свойство.</span><span class="sxs-lookup"><span data-stu-id="75527-183">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="75527-184">`[AutoUpgradeMinorVersion <Boolean?>]`: Указывает, должно ли расширение использовать более новую вспомогательную версию, если она доступна во время развертывания.</span><span class="sxs-lookup"><span data-stu-id="75527-184">`[AutoUpgradeMinorVersion <Boolean?>]`: Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span> <span data-ttu-id="75527-185">Однако после развертывания расширение не будет обновлять дополнительные версии, если только повторно не развернуто, даже если для этого свойства задано значение true.</span><span class="sxs-lookup"><span data-stu-id="75527-185">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>
  - <span data-ttu-id="75527-186">`[ForceUpdateTag <String>]`: Как следует принудительно обновлять обработчик расширений, даже если конфигурация расширения не изменилась.</span><span class="sxs-lookup"><span data-stu-id="75527-186">`[ForceUpdateTag <String>]`: How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>
  - <span data-ttu-id="75527-187">`[ProtectedSetting <IMachineExtensionUpdatePropertiesProtectedSettings>]`: Расширение может содержать либо protectedSettings, либо protectedSettingsFromKeyVault, или вообще не защищенные параметры.</span><span class="sxs-lookup"><span data-stu-id="75527-187">`[ProtectedSetting <IMachineExtensionUpdatePropertiesProtectedSettings>]`: The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>
  - <span data-ttu-id="75527-188">`[Publisher <String>]`: Имя издателя обработчика расширений.</span><span class="sxs-lookup"><span data-stu-id="75527-188">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
  - <span data-ttu-id="75527-189">`[Setting <IMachineExtensionUpdatePropertiesSettings>]`: Отформатированные общедоступные параметры JSON для расширения.</span><span class="sxs-lookup"><span data-stu-id="75527-189">`[Setting <IMachineExtensionUpdatePropertiesSettings>]`: Json formatted public settings for the extension.</span></span>
  - <span data-ttu-id="75527-190">`[Type <String>]`: Указывает тип расширения; Пример: "CustomScriptExtension".</span><span class="sxs-lookup"><span data-stu-id="75527-190">`[Type <String>]`: Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>
  - <span data-ttu-id="75527-191">`[TypeHandlerVersion <String>]`: Определяет версию обработчика сценария.</span><span class="sxs-lookup"><span data-stu-id="75527-191">`[TypeHandlerVersion <String>]`: Specifies the version of the script handler.</span></span>

<span data-ttu-id="75527-192">INPUTOBJECT <IConnectedMachineIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="75527-192">INPUTOBJECT <IConnectedMachineIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="75527-193">`[ExtensionName <String>]`: Имя расширения компьютера.</span><span class="sxs-lookup"><span data-stu-id="75527-193">`[ExtensionName <String>]`: The name of the machine extension.</span></span>
  - <span data-ttu-id="75527-194">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="75527-194">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="75527-195">`[Name <String>]`: Имя гибридного компьютера.</span><span class="sxs-lookup"><span data-stu-id="75527-195">`[Name <String>]`: The name of the hybrid machine.</span></span>
  - <span data-ttu-id="75527-196">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="75527-196">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="75527-197">`[SubscriptionId <String>]`: Учетные данные подписки, однозначно определяющие подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="75527-197">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="75527-198">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="75527-198">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="75527-199">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="75527-199">RELATED LINKS</span></span>


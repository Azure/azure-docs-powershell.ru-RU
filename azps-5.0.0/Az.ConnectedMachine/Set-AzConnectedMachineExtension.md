---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/set-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Set-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Set-AzConnectedMachineExtension.md
ms.openlocfilehash: b136f5194bdc7e0f4b4dfc969564d7ef8476d9bf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248732"
---
# <span data-ttu-id="c411e-101">Set-AzConnectedMachineExtension</span><span class="sxs-lookup"><span data-stu-id="c411e-101">Set-AzConnectedMachineExtension</span></span>

## <span data-ttu-id="c411e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c411e-102">SYNOPSIS</span></span>
<span data-ttu-id="c411e-103">Операция, позволяющая создать или обновить расширение.</span><span class="sxs-lookup"><span data-stu-id="c411e-103">The operation to create or update the extension.</span></span>

## <span data-ttu-id="c411e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c411e-104">SYNTAX</span></span>

### <span data-ttu-id="c411e-105">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c411e-105">UpdateExpanded (Default)</span></span>
```
Set-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -Location <String> [-SubscriptionId <String>] [-AutoUpgradeMinorVersion] [-ExtensionType <String>]
 [-ForceRerun <String>] [-ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]
 [-Publisher <String>] [-Setting <IMachineExtensionPropertiesSettings>] [-Tag <Hashtable>]
 [-TypeHandlerVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="c411e-106">Обновление</span><span class="sxs-lookup"><span data-stu-id="c411e-106">Update</span></span>
```
Set-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -ExtensionParameter <IMachineExtension> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c411e-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c411e-107">DESCRIPTION</span></span>
<span data-ttu-id="c411e-108">Операция, позволяющая создать или обновить расширение.</span><span class="sxs-lookup"><span data-stu-id="c411e-108">The operation to create or update the extension.</span></span>

## <span data-ttu-id="c411e-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c411e-109">EXAMPLES</span></span>

### <span data-ttu-id="c411e-110">Пример 1: Настройка расширения на компьютере</span><span class="sxs-lookup"><span data-stu-id="c411e-110">Example 1: Set an extension on a machine</span></span>
```powershell
PS C:\> $Settings = @{ "commandToExecute" = "powershell.exe -c Get-Process" }
PS C:\> Set-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName win-eastus1 -Location eastus -Publisher "Microsoft.Compute" -TypeHandlerVersion 1.10 -Settings $Settings -ExtensionType CustomScriptExtension

Name   Location ProvisioningState
----   -------- -----------------
custom eastus   Succeeded
```

<span data-ttu-id="c411e-111">Задает расширение на компьютере.</span><span class="sxs-lookup"><span data-stu-id="c411e-111">Sets an extension on a machine.</span></span>

### <span data-ttu-id="c411e-112">Пример 2: Настройка расширения с помощью параметров расширения, указанных через конвейер</span><span class="sxs-lookup"><span data-stu-id="c411e-112">Example 2: Set an extension with extension parameters specified via the pipeline</span></span>
```powershell
PS C:\> $otherExtension = Get-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName other
PS C:\> $otherExtension | Set-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName important

Name   Location ProvisioningState
----   -------- -----------------
custom eastus   Succeeded
```

<span data-ttu-id="c411e-113">Это задает расширение с параметрами расширения, предоставленными объектом, который передается через конвейер.</span><span class="sxs-lookup"><span data-stu-id="c411e-113">This sets an extension with the extension parameters provided by the object passed in via the pipeline.</span></span>
<span data-ttu-id="c411e-114">Это очень удобно, если вы хотите захватить параметры одного компьютера и применить его к другому компьютеру.</span><span class="sxs-lookup"><span data-stu-id="c411e-114">This is great if you want to grab the parameters of one machine and apply it to another machine.</span></span>

## <span data-ttu-id="c411e-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c411e-115">PARAMETERS</span></span>

### <span data-ttu-id="c411e-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c411e-116">-AsJob</span></span>
<span data-ttu-id="c411e-117">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="c411e-117">Run the command as a job</span></span>

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

### <span data-ttu-id="c411e-118">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="c411e-118">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="c411e-119">Указывает, должно ли расширение использовать более новую вспомогательную версию, если она доступна во время развертывания.</span><span class="sxs-lookup"><span data-stu-id="c411e-119">Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span>
<span data-ttu-id="c411e-120">Однако после развертывания расширение не будет обновлять дополнительные версии, если только повторно не развернуто, даже если для этого свойства задано значение true.</span><span class="sxs-lookup"><span data-stu-id="c411e-120">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c411e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c411e-121">-DefaultProfile</span></span>
<span data-ttu-id="c411e-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c411e-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c411e-123">-ExtensionParameter</span><span class="sxs-lookup"><span data-stu-id="c411e-123">-ExtensionParameter</span></span>
<span data-ttu-id="c411e-124">Описывает расширение компьютера.</span><span class="sxs-lookup"><span data-stu-id="c411e-124">Describes a Machine Extension.</span></span>
<span data-ttu-id="c411e-125">Для конструирования ознакомьтесь с разделом "Заметки" для свойств EXTENSIONPARAMETER и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="c411e-125">To construct, see NOTES section for EXTENSIONPARAMETER properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension
Parameter Sets: Update
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c411e-126">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="c411e-126">-ExtensionType</span></span>
<span data-ttu-id="c411e-127">Указывает тип расширения; Пример: "CustomScriptExtension".</span><span class="sxs-lookup"><span data-stu-id="c411e-127">Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c411e-128">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="c411e-128">-ForceRerun</span></span>
<span data-ttu-id="c411e-129">Как следует принудительно обновлять обработчик расширений, даже если конфигурация расширения не изменилась.</span><span class="sxs-lookup"><span data-stu-id="c411e-129">How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c411e-130">-Location</span><span class="sxs-lookup"><span data-stu-id="c411e-130">-Location</span></span>
<span data-ttu-id="c411e-131">Географическое расположение, в котором находится ресурс</span><span class="sxs-lookup"><span data-stu-id="c411e-131">The geo-location where the resource lives</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c411e-132">-MachineName</span><span class="sxs-lookup"><span data-stu-id="c411e-132">-MachineName</span></span>
<span data-ttu-id="c411e-133">Имя компьютера, на котором нужно создать или обновить расширение.</span><span class="sxs-lookup"><span data-stu-id="c411e-133">The name of the machine where the extension should be created or updated.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c411e-134">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c411e-134">-Name</span></span>
<span data-ttu-id="c411e-135">Имя расширения компьютера.</span><span class="sxs-lookup"><span data-stu-id="c411e-135">The name of the machine extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c411e-136">-Wait</span><span class="sxs-lookup"><span data-stu-id="c411e-136">-NoWait</span></span>
<span data-ttu-id="c411e-137">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="c411e-137">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c411e-138">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="c411e-138">-ProtectedSetting</span></span>
<span data-ttu-id="c411e-139">Расширение может содержать либо protectedSettings, либо protectedSettingsFromKeyVault, или вообще не защищенные параметры.</span><span class="sxs-lookup"><span data-stu-id="c411e-139">The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionPropertiesProtectedSettings
Parameter Sets: UpdateExpanded
Aliases: ProtectedSettings

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c411e-140">-Publisher</span><span class="sxs-lookup"><span data-stu-id="c411e-140">-Publisher</span></span>
<span data-ttu-id="c411e-141">Имя издателя обработчика расширений.</span><span class="sxs-lookup"><span data-stu-id="c411e-141">The name of the extension handler publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c411e-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c411e-142">-ResourceGroupName</span></span>
<span data-ttu-id="c411e-143">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c411e-143">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c411e-144">-Параметр</span><span class="sxs-lookup"><span data-stu-id="c411e-144">-Setting</span></span>
<span data-ttu-id="c411e-145">Отформатированные общедоступные параметры JSON для расширения.</span><span class="sxs-lookup"><span data-stu-id="c411e-145">Json formatted public settings for the extension.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionPropertiesSettings
Parameter Sets: UpdateExpanded
Aliases: Settings

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c411e-146">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c411e-146">-SubscriptionId</span></span>
<span data-ttu-id="c411e-147">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="c411e-147">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="c411e-148">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="c411e-148">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c411e-149">-Тег</span><span class="sxs-lookup"><span data-stu-id="c411e-149">-Tag</span></span>
<span data-ttu-id="c411e-150">Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c411e-150">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c411e-151">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="c411e-151">-TypeHandlerVersion</span></span>
<span data-ttu-id="c411e-152">Указывает версию обработчика сценария.</span><span class="sxs-lookup"><span data-stu-id="c411e-152">Specifies the version of the script handler.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c411e-153">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c411e-153">-Confirm</span></span>
<span data-ttu-id="c411e-154">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c411e-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c411e-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c411e-155">-WhatIf</span></span>
<span data-ttu-id="c411e-156">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c411e-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c411e-157">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c411e-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c411e-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c411e-158">CommonParameters</span></span>
<span data-ttu-id="c411e-159">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c411e-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c411e-160">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c411e-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c411e-161">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c411e-161">INPUTS</span></span>

### <span data-ttu-id="c411e-162">Microsoft. Azure. PowerShell. командлеты. ConnectedMachine. Models. Api20200802. IMachineExtension</span><span class="sxs-lookup"><span data-stu-id="c411e-162">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

## <span data-ttu-id="c411e-163">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c411e-163">OUTPUTS</span></span>

### <span data-ttu-id="c411e-164">Microsoft. Azure. PowerShell. командлеты. ConnectedMachine. Models. Api20200802. IMachineExtension</span><span class="sxs-lookup"><span data-stu-id="c411e-164">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

## <span data-ttu-id="c411e-165">Пуск</span><span class="sxs-lookup"><span data-stu-id="c411e-165">NOTES</span></span>

<span data-ttu-id="c411e-166">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="c411e-166">ALIASES</span></span>

<span data-ttu-id="c411e-167">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="c411e-167">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c411e-168">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="c411e-168">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c411e-169">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c411e-169">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c411e-170">EXTENSIONPARAMETER <IMachineExtension> : описывает расширение компьютера.</span><span class="sxs-lookup"><span data-stu-id="c411e-170">EXTENSIONPARAMETER <IMachineExtension>: Describes a Machine Extension.</span></span>
  - <span data-ttu-id="c411e-171">`Location <String>`: Географическое расположение, в котором находится ресурс</span><span class="sxs-lookup"><span data-stu-id="c411e-171">`Location <String>`: The geo-location where the resource lives</span></span>
  - <span data-ttu-id="c411e-172">`[Tag <ITrackedResourceTags>]`: Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c411e-172">`[Tag <ITrackedResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="c411e-173">`[(Any) <String>]`: Это указывает на то, что в этот объект можно добавить любое свойство.</span><span class="sxs-lookup"><span data-stu-id="c411e-173">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="c411e-174">`[AutoUpgradeMinorVersion <Boolean?>]`: Указывает, должно ли расширение использовать более новую вспомогательную версию, если она доступна во время развертывания.</span><span class="sxs-lookup"><span data-stu-id="c411e-174">`[AutoUpgradeMinorVersion <Boolean?>]`: Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span> <span data-ttu-id="c411e-175">Однако после развертывания расширение не будет обновлять дополнительные версии, если только повторно не развернуто, даже если для этого свойства задано значение true.</span><span class="sxs-lookup"><span data-stu-id="c411e-175">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>
  - <span data-ttu-id="c411e-176">`[ForceUpdateTag <String>]`: Как следует принудительно обновлять обработчик расширений, даже если конфигурация расширения не изменилась.</span><span class="sxs-lookup"><span data-stu-id="c411e-176">`[ForceUpdateTag <String>]`: How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>
  - <span data-ttu-id="c411e-177">`[MachineExtensionType <String>]`: Указывает тип расширения; Пример: "CustomScriptExtension".</span><span class="sxs-lookup"><span data-stu-id="c411e-177">`[MachineExtensionType <String>]`: Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>
  - <span data-ttu-id="c411e-178">`[ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]`: Расширение может содержать либо protectedSettings, либо protectedSettingsFromKeyVault, или вообще не защищенные параметры.</span><span class="sxs-lookup"><span data-stu-id="c411e-178">`[ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]`: The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>
  - <span data-ttu-id="c411e-179">`[Publisher <String>]`: Имя издателя обработчика расширений.</span><span class="sxs-lookup"><span data-stu-id="c411e-179">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
  - <span data-ttu-id="c411e-180">`[Setting <IMachineExtensionPropertiesSettings>]`: Отформатированные общедоступные параметры JSON для расширения.</span><span class="sxs-lookup"><span data-stu-id="c411e-180">`[Setting <IMachineExtensionPropertiesSettings>]`: Json formatted public settings for the extension.</span></span>
  - <span data-ttu-id="c411e-181">`[TypeHandlerVersion <String>]`: Определяет версию обработчика сценария.</span><span class="sxs-lookup"><span data-stu-id="c411e-181">`[TypeHandlerVersion <String>]`: Specifies the version of the script handler.</span></span>

## <span data-ttu-id="c411e-182">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c411e-182">RELATED LINKS</span></span>


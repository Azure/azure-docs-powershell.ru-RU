---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/powershell/module/az.connectedmachine/set-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Set-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Set-AzConnectedMachineExtension.md
ms.openlocfilehash: accea82dd6594d71f627d6c3e32943d004fa35e3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012344"
---
# <span data-ttu-id="fb86a-101">Set-AzConnectedMachineExtension</span><span class="sxs-lookup"><span data-stu-id="fb86a-101">Set-AzConnectedMachineExtension</span></span>

## <span data-ttu-id="fb86a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb86a-102">SYNOPSIS</span></span>
<span data-ttu-id="fb86a-103">Операция создания или обновления расширения.</span><span class="sxs-lookup"><span data-stu-id="fb86a-103">The operation to create or update the extension.</span></span>

## <span data-ttu-id="fb86a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="fb86a-104">SYNTAX</span></span>

### <span data-ttu-id="fb86a-105">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fb86a-105">UpdateExpanded (Default)</span></span>
```
Set-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -Location <String> [-SubscriptionId <String>] [-AutoUpgradeMinorVersion] [-ExtensionType <String>]
 [-ForceRerun <String>] [-ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]
 [-Publisher <String>] [-Setting <IMachineExtensionPropertiesSettings>] [-Tag <Hashtable>]
 [-TypeHandlerVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="fb86a-106">Обновление</span><span class="sxs-lookup"><span data-stu-id="fb86a-106">Update</span></span>
```
Set-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -ExtensionParameter <IMachineExtension> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="fb86a-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fb86a-107">DESCRIPTION</span></span>
<span data-ttu-id="fb86a-108">Операция создания или обновления расширения.</span><span class="sxs-lookup"><span data-stu-id="fb86a-108">The operation to create or update the extension.</span></span>

## <span data-ttu-id="fb86a-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="fb86a-109">EXAMPLES</span></span>

### <span data-ttu-id="fb86a-110">Пример 1. Настройка расширения на компьютере</span><span class="sxs-lookup"><span data-stu-id="fb86a-110">Example 1: Set an extension on a machine</span></span>
```powershell
PS C:\> $Settings = @{ "commandToExecute" = "powershell.exe -c Get-Process" }
PS C:\> Set-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName win-eastus1 -Location eastus -Publisher "Microsoft.Compute" -TypeHandlerVersion 1.10 -Settings $Settings -ExtensionType CustomScriptExtension

Name   Location ProvisioningState
----   -------- -----------------
custom eastus   Succeeded
```

<span data-ttu-id="fb86a-111">Задает расширение на компьютере.</span><span class="sxs-lookup"><span data-stu-id="fb86a-111">Sets an extension on a machine.</span></span>

### <span data-ttu-id="fb86a-112">Пример 2. Настройка расширения с параметрами расширения, указанными в конвейере</span><span class="sxs-lookup"><span data-stu-id="fb86a-112">Example 2: Set an extension with extension parameters specified via the pipeline</span></span>
```powershell
PS C:\> $otherExtension = Get-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName other
PS C:\> $otherExtension | Set-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName important

Name   Location ProvisioningState
----   -------- -----------------
custom eastus   Succeeded
```

<span data-ttu-id="fb86a-113">При этом устанавливается расширение с параметрами расширения, предоставленными объектом, переданным через канал.</span><span class="sxs-lookup"><span data-stu-id="fb86a-113">This sets an extension with the extension parameters provided by the object passed in via the pipeline.</span></span>
<span data-ttu-id="fb86a-114">Это очень здорово, если вы хотите захватить параметры одного компьютера и применить его к другому компьютеру.</span><span class="sxs-lookup"><span data-stu-id="fb86a-114">This is great if you want to grab the parameters of one machine and apply it to another machine.</span></span>

## <span data-ttu-id="fb86a-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fb86a-115">PARAMETERS</span></span>

### <span data-ttu-id="fb86a-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fb86a-116">-AsJob</span></span>
<span data-ttu-id="fb86a-117">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="fb86a-117">Run the command as a job</span></span>

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

### <span data-ttu-id="fb86a-118">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="fb86a-118">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="fb86a-119">Указывает, следует ли использовать в расширении более новую версию, если она доступна во время развертывания.</span><span class="sxs-lookup"><span data-stu-id="fb86a-119">Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span>
<span data-ttu-id="fb86a-120">Однако после развертывания расширение не будет обновлять дополнительные версии, если не развернуть их снова, даже если для этого свойства установлено true.</span><span class="sxs-lookup"><span data-stu-id="fb86a-120">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>

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

### <span data-ttu-id="fb86a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb86a-121">-DefaultProfile</span></span>
<span data-ttu-id="fb86a-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fb86a-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb86a-123">-ExtensionParameter</span><span class="sxs-lookup"><span data-stu-id="fb86a-123">-ExtensionParameter</span></span>
<span data-ttu-id="fb86a-124">Описание расширения компьютера.</span><span class="sxs-lookup"><span data-stu-id="fb86a-124">Describes a Machine Extension.</span></span>
<span data-ttu-id="fb86a-125">Чтобы создать таблицу, см. раздел "ЗАМЕТКИ" для свойств EXTENSIONPARAMETER и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="fb86a-125">To construct, see NOTES section for EXTENSIONPARAMETER properties and create a hash table.</span></span>

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

### <span data-ttu-id="fb86a-126">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="fb86a-126">-ExtensionType</span></span>
<span data-ttu-id="fb86a-127">Тип расширения. например: CustomScriptExtension.</span><span class="sxs-lookup"><span data-stu-id="fb86a-127">Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>

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

### <span data-ttu-id="fb86a-128">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="fb86a-128">-ForceRerun</span></span>
<span data-ttu-id="fb86a-129">Как обработник расширений должен быть принудительно обновляться, даже если конфигурация расширения не изменилась.</span><span class="sxs-lookup"><span data-stu-id="fb86a-129">How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>

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

### <span data-ttu-id="fb86a-130">-Location</span><span class="sxs-lookup"><span data-stu-id="fb86a-130">-Location</span></span>
<span data-ttu-id="fb86a-131">Географическое расположение ресурса</span><span class="sxs-lookup"><span data-stu-id="fb86a-131">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="fb86a-132">-MachineName</span><span class="sxs-lookup"><span data-stu-id="fb86a-132">-MachineName</span></span>
<span data-ttu-id="fb86a-133">Имя компьютера, на котором нужно создать или обновить расширение.</span><span class="sxs-lookup"><span data-stu-id="fb86a-133">The name of the machine where the extension should be created or updated.</span></span>

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

### <span data-ttu-id="fb86a-134">-Name</span><span class="sxs-lookup"><span data-stu-id="fb86a-134">-Name</span></span>
<span data-ttu-id="fb86a-135">Имя расширения компьютера.</span><span class="sxs-lookup"><span data-stu-id="fb86a-135">The name of the machine extension.</span></span>

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

### <span data-ttu-id="fb86a-136">-NoWait</span><span class="sxs-lookup"><span data-stu-id="fb86a-136">-NoWait</span></span>
<span data-ttu-id="fb86a-137">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="fb86a-137">Run the command asynchronously</span></span>

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

### <span data-ttu-id="fb86a-138">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="fb86a-138">-ProtectedSetting</span></span>
<span data-ttu-id="fb86a-139">Расширение может содержать защищенные параметрыSettings или protectedSettingsFromKeyVault или не защищенные параметры.</span><span class="sxs-lookup"><span data-stu-id="fb86a-139">The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>

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

### <span data-ttu-id="fb86a-140">-Publisher</span><span class="sxs-lookup"><span data-stu-id="fb86a-140">-Publisher</span></span>
<span data-ttu-id="fb86a-141">Имя издателя обработера расширений.</span><span class="sxs-lookup"><span data-stu-id="fb86a-141">The name of the extension handler publisher.</span></span>

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

### <span data-ttu-id="fb86a-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb86a-142">-ResourceGroupName</span></span>
<span data-ttu-id="fb86a-143">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fb86a-143">The name of the resource group.</span></span>

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

### <span data-ttu-id="fb86a-144">-Setting</span><span class="sxs-lookup"><span data-stu-id="fb86a-144">-Setting</span></span>
<span data-ttu-id="fb86a-145">Общедоступные параметры расширения, отформатированные Json.</span><span class="sxs-lookup"><span data-stu-id="fb86a-145">Json formatted public settings for the extension.</span></span>

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

### <span data-ttu-id="fb86a-146">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fb86a-146">-SubscriptionId</span></span>
<span data-ttu-id="fb86a-147">Учетные данные подписки, однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="fb86a-147">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="fb86a-148">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="fb86a-148">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="fb86a-149">-Tag</span><span class="sxs-lookup"><span data-stu-id="fb86a-149">-Tag</span></span>
<span data-ttu-id="fb86a-150">Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fb86a-150">Resource tags.</span></span>

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

### <span data-ttu-id="fb86a-151">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="fb86a-151">-TypeHandlerVersion</span></span>
<span data-ttu-id="fb86a-152">Определяет версию обработера сценариев.</span><span class="sxs-lookup"><span data-stu-id="fb86a-152">Specifies the version of the script handler.</span></span>

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

### <span data-ttu-id="fb86a-153">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fb86a-153">-Confirm</span></span>
<span data-ttu-id="fb86a-154">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fb86a-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb86a-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb86a-155">-WhatIf</span></span>
<span data-ttu-id="fb86a-156">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fb86a-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb86a-157">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="fb86a-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb86a-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb86a-158">CommonParameters</span></span>
<span data-ttu-id="fb86a-159">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb86a-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb86a-160">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fb86a-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb86a-161">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fb86a-161">INPUTS</span></span>

### <span data-ttu-id="fb86a-162">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMa modelse.Models.Api20200802.IMa modelseExtension</span><span class="sxs-lookup"><span data-stu-id="fb86a-162">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

## <span data-ttu-id="fb86a-163">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="fb86a-163">OUTPUTS</span></span>

### <span data-ttu-id="fb86a-164">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMa modelse.Models.Api20200802.IMa modelseExtension</span><span class="sxs-lookup"><span data-stu-id="fb86a-164">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

## <span data-ttu-id="fb86a-165">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="fb86a-165">NOTES</span></span>

<span data-ttu-id="fb86a-166">ALIASES</span><span class="sxs-lookup"><span data-stu-id="fb86a-166">ALIASES</span></span>

<span data-ttu-id="fb86a-167">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="fb86a-167">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="fb86a-168">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="fb86a-168">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="fb86a-169">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="fb86a-169">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="fb86a-170">EXTENSIONPARAMETER: <IMachineExtension> описание расширения компьютера.</span><span class="sxs-lookup"><span data-stu-id="fb86a-170">EXTENSIONPARAMETER <IMachineExtension>: Describes a Machine Extension.</span></span>
  - <span data-ttu-id="fb86a-171">`Location <String>`: географическое расположение ресурса</span><span class="sxs-lookup"><span data-stu-id="fb86a-171">`Location <String>`: The geo-location where the resource lives</span></span>
  - <span data-ttu-id="fb86a-172">`[Tag <ITrackedResourceTags>]`: теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fb86a-172">`[Tag <ITrackedResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="fb86a-173">`[(Any) <String>]`— это означает, что к этому объекту можно добавить любое свойство.</span><span class="sxs-lookup"><span data-stu-id="fb86a-173">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="fb86a-174">`[AutoUpgradeMinorVersion <Boolean?>]`: указывает, следует ли использовать в расширении более новую версию, если она доступна во время развертывания.</span><span class="sxs-lookup"><span data-stu-id="fb86a-174">`[AutoUpgradeMinorVersion <Boolean?>]`: Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span> <span data-ttu-id="fb86a-175">Однако после развертывания расширение не будет обновлять дополнительные версии, если не развернуть их снова, даже если для этого свойства установлено true.</span><span class="sxs-lookup"><span data-stu-id="fb86a-175">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>
  - <span data-ttu-id="fb86a-176">`[ForceUpdateTag <String>]`. Как обработник расширений должен быть принудительно обновляться, даже если конфигурация расширения не изменилась.</span><span class="sxs-lookup"><span data-stu-id="fb86a-176">`[ForceUpdateTag <String>]`: How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>
  - <span data-ttu-id="fb86a-177">`[MachineExtensionType <String>]`: тип расширения; например: CustomScriptExtension.</span><span class="sxs-lookup"><span data-stu-id="fb86a-177">`[MachineExtensionType <String>]`: Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>
  - <span data-ttu-id="fb86a-178">`[ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]`: Расширение может содержать защищенные параметрыSettings или protectedSettingsFromKeyVault или не защищенные параметры.</span><span class="sxs-lookup"><span data-stu-id="fb86a-178">`[ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]`: The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>
  - <span data-ttu-id="fb86a-179">`[Publisher <String>]`: имя издателя обработера расширений.</span><span class="sxs-lookup"><span data-stu-id="fb86a-179">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
  - <span data-ttu-id="fb86a-180">`[Setting <IMachineExtensionPropertiesSettings>]`: Общедоступные параметры расширения отформатированы Json.</span><span class="sxs-lookup"><span data-stu-id="fb86a-180">`[Setting <IMachineExtensionPropertiesSettings>]`: Json formatted public settings for the extension.</span></span>
  - <span data-ttu-id="fb86a-181">`[TypeHandlerVersion <String>]`: определяет версию обработера сценариев.</span><span class="sxs-lookup"><span data-stu-id="fb86a-181">`[TypeHandlerVersion <String>]`: Specifies the version of the script handler.</span></span>

## <span data-ttu-id="fb86a-182">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fb86a-182">RELATED LINKS</span></span>


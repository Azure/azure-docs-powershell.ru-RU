---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/set-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Set-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Set-AzConnectedMachineExtension.md
ms.openlocfilehash: b136f5194bdc7e0f4b4dfc969564d7ef8476d9bf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100243968"
---
# <span data-ttu-id="139a5-101">Set-AzConnectedMachineExtension</span><span class="sxs-lookup"><span data-stu-id="139a5-101">Set-AzConnectedMachineExtension</span></span>

## <span data-ttu-id="139a5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="139a5-102">SYNOPSIS</span></span>
<span data-ttu-id="139a5-103">Операция создания или обновления расширения.</span><span class="sxs-lookup"><span data-stu-id="139a5-103">The operation to create or update the extension.</span></span>

## <span data-ttu-id="139a5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="139a5-104">SYNTAX</span></span>

### <span data-ttu-id="139a5-105">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="139a5-105">UpdateExpanded (Default)</span></span>
```
Set-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -Location <String> [-SubscriptionId <String>] [-AutoUpgradeMinorVersion] [-ExtensionType <String>]
 [-ForceRerun <String>] [-ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]
 [-Publisher <String>] [-Setting <IMachineExtensionPropertiesSettings>] [-Tag <Hashtable>]
 [-TypeHandlerVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="139a5-106">Обновление</span><span class="sxs-lookup"><span data-stu-id="139a5-106">Update</span></span>
```
Set-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -ExtensionParameter <IMachineExtension> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="139a5-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="139a5-107">DESCRIPTION</span></span>
<span data-ttu-id="139a5-108">Операция создания или обновления расширения.</span><span class="sxs-lookup"><span data-stu-id="139a5-108">The operation to create or update the extension.</span></span>

## <span data-ttu-id="139a5-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="139a5-109">EXAMPLES</span></span>

### <span data-ttu-id="139a5-110">Пример 1. Настройка расширения на компьютере</span><span class="sxs-lookup"><span data-stu-id="139a5-110">Example 1: Set an extension on a machine</span></span>
```powershell
PS C:\> $Settings = @{ "commandToExecute" = "powershell.exe -c Get-Process" }
PS C:\> Set-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName win-eastus1 -Location eastus -Publisher "Microsoft.Compute" -TypeHandlerVersion 1.10 -Settings $Settings -ExtensionType CustomScriptExtension

Name   Location ProvisioningState
----   -------- -----------------
custom eastus   Succeeded
```

<span data-ttu-id="139a5-111">Задает расширение на компьютере.</span><span class="sxs-lookup"><span data-stu-id="139a5-111">Sets an extension on a machine.</span></span>

### <span data-ttu-id="139a5-112">Пример 2. Настройка расширения с параметрами расширения, указанными через конвейер</span><span class="sxs-lookup"><span data-stu-id="139a5-112">Example 2: Set an extension with extension parameters specified via the pipeline</span></span>
```powershell
PS C:\> $otherExtension = Get-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName other
PS C:\> $otherExtension | Set-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName important

Name   Location ProvisioningState
----   -------- -----------------
custom eastus   Succeeded
```

<span data-ttu-id="139a5-113">При этом устанавливается расширение с параметрами расширения, предоставленными объектом, переданным через канал.</span><span class="sxs-lookup"><span data-stu-id="139a5-113">This sets an extension with the extension parameters provided by the object passed in via the pipeline.</span></span>
<span data-ttu-id="139a5-114">Это очень здорово, если вы хотите захватить параметры одного компьютера и применить его к другому компьютеру.</span><span class="sxs-lookup"><span data-stu-id="139a5-114">This is great if you want to grab the parameters of one machine and apply it to another machine.</span></span>

## <span data-ttu-id="139a5-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="139a5-115">PARAMETERS</span></span>

### <span data-ttu-id="139a5-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="139a5-116">-AsJob</span></span>
<span data-ttu-id="139a5-117">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="139a5-117">Run the command as a job</span></span>

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

### <span data-ttu-id="139a5-118">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="139a5-118">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="139a5-119">Указывает, следует ли использовать в расширении более новую версию, если она доступна во время развертывания.</span><span class="sxs-lookup"><span data-stu-id="139a5-119">Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span>
<span data-ttu-id="139a5-120">Однако после развертывания расширение не будет обновлять дополнительные версии, если не развернуть их снова, даже если для этого свойства установлено true.</span><span class="sxs-lookup"><span data-stu-id="139a5-120">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>

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

### <span data-ttu-id="139a5-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="139a5-121">-DefaultProfile</span></span>
<span data-ttu-id="139a5-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="139a5-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="139a5-123">-ExtensionParameter</span><span class="sxs-lookup"><span data-stu-id="139a5-123">-ExtensionParameter</span></span>
<span data-ttu-id="139a5-124">Описание расширения компьютера.</span><span class="sxs-lookup"><span data-stu-id="139a5-124">Describes a Machine Extension.</span></span>
<span data-ttu-id="139a5-125">Чтобы создать таблицу, см. раздел "ЗАМЕТКИ" для свойств EXTENSIONPARAMETER и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="139a5-125">To construct, see NOTES section for EXTENSIONPARAMETER properties and create a hash table.</span></span>

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

### <span data-ttu-id="139a5-126">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="139a5-126">-ExtensionType</span></span>
<span data-ttu-id="139a5-127">Тип расширения. например: CustomScriptExtension.</span><span class="sxs-lookup"><span data-stu-id="139a5-127">Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>

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

### <span data-ttu-id="139a5-128">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="139a5-128">-ForceRerun</span></span>
<span data-ttu-id="139a5-129">Как обработник расширений должен быть принудительно обновляться, даже если конфигурация расширения не изменилась.</span><span class="sxs-lookup"><span data-stu-id="139a5-129">How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>

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

### <span data-ttu-id="139a5-130">-Location</span><span class="sxs-lookup"><span data-stu-id="139a5-130">-Location</span></span>
<span data-ttu-id="139a5-131">Географическое расположение ресурса</span><span class="sxs-lookup"><span data-stu-id="139a5-131">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="139a5-132">-MachineName</span><span class="sxs-lookup"><span data-stu-id="139a5-132">-MachineName</span></span>
<span data-ttu-id="139a5-133">Имя компьютера, на котором нужно создать или обновить расширение.</span><span class="sxs-lookup"><span data-stu-id="139a5-133">The name of the machine where the extension should be created or updated.</span></span>

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

### <span data-ttu-id="139a5-134">-Name</span><span class="sxs-lookup"><span data-stu-id="139a5-134">-Name</span></span>
<span data-ttu-id="139a5-135">Имя расширения компьютера.</span><span class="sxs-lookup"><span data-stu-id="139a5-135">The name of the machine extension.</span></span>

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

### <span data-ttu-id="139a5-136">-NoWait</span><span class="sxs-lookup"><span data-stu-id="139a5-136">-NoWait</span></span>
<span data-ttu-id="139a5-137">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="139a5-137">Run the command asynchronously</span></span>

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

### <span data-ttu-id="139a5-138">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="139a5-138">-ProtectedSetting</span></span>
<span data-ttu-id="139a5-139">Расширение может содержать защищенные параметрыSettings или protectedSettingsFromKeyVault или не защищенные параметры.</span><span class="sxs-lookup"><span data-stu-id="139a5-139">The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>

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

### <span data-ttu-id="139a5-140">-Publisher</span><span class="sxs-lookup"><span data-stu-id="139a5-140">-Publisher</span></span>
<span data-ttu-id="139a5-141">Имя издателя обработера расширений.</span><span class="sxs-lookup"><span data-stu-id="139a5-141">The name of the extension handler publisher.</span></span>

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

### <span data-ttu-id="139a5-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="139a5-142">-ResourceGroupName</span></span>
<span data-ttu-id="139a5-143">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="139a5-143">The name of the resource group.</span></span>

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

### <span data-ttu-id="139a5-144">-Setting</span><span class="sxs-lookup"><span data-stu-id="139a5-144">-Setting</span></span>
<span data-ttu-id="139a5-145">Общедоступные параметры расширения, отформатированные Json.</span><span class="sxs-lookup"><span data-stu-id="139a5-145">Json formatted public settings for the extension.</span></span>

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

### <span data-ttu-id="139a5-146">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="139a5-146">-SubscriptionId</span></span>
<span data-ttu-id="139a5-147">Учетные данные подписки, однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="139a5-147">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="139a5-148">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="139a5-148">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="139a5-149">-Tag</span><span class="sxs-lookup"><span data-stu-id="139a5-149">-Tag</span></span>
<span data-ttu-id="139a5-150">Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="139a5-150">Resource tags.</span></span>

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

### <span data-ttu-id="139a5-151">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="139a5-151">-TypeHandlerVersion</span></span>
<span data-ttu-id="139a5-152">Определяет версию обработера сценариев.</span><span class="sxs-lookup"><span data-stu-id="139a5-152">Specifies the version of the script handler.</span></span>

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

### <span data-ttu-id="139a5-153">-Confirm</span><span class="sxs-lookup"><span data-stu-id="139a5-153">-Confirm</span></span>
<span data-ttu-id="139a5-154">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="139a5-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="139a5-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="139a5-155">-WhatIf</span></span>
<span data-ttu-id="139a5-156">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="139a5-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="139a5-157">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="139a5-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="139a5-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="139a5-158">CommonParameters</span></span>
<span data-ttu-id="139a5-159">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="139a5-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="139a5-160">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="139a5-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="139a5-161">INPUTS</span><span class="sxs-lookup"><span data-stu-id="139a5-161">INPUTS</span></span>

### <span data-ttu-id="139a5-162">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMa modelse.Models.Api20200802.IMa modelseExtension</span><span class="sxs-lookup"><span data-stu-id="139a5-162">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

## <span data-ttu-id="139a5-163">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="139a5-163">OUTPUTS</span></span>

### <span data-ttu-id="139a5-164">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMa modelse.Models.Api20200802.IMa modelseExtension</span><span class="sxs-lookup"><span data-stu-id="139a5-164">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

## <span data-ttu-id="139a5-165">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="139a5-165">NOTES</span></span>

<span data-ttu-id="139a5-166">ALIASES</span><span class="sxs-lookup"><span data-stu-id="139a5-166">ALIASES</span></span>

<span data-ttu-id="139a5-167">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="139a5-167">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="139a5-168">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="139a5-168">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="139a5-169">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="139a5-169">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="139a5-170">EXTENSIONPARAMETER: <IMachineExtension> описание расширения компьютера.</span><span class="sxs-lookup"><span data-stu-id="139a5-170">EXTENSIONPARAMETER <IMachineExtension>: Describes a Machine Extension.</span></span>
  - <span data-ttu-id="139a5-171">`Location <String>`: географическое расположение ресурса</span><span class="sxs-lookup"><span data-stu-id="139a5-171">`Location <String>`: The geo-location where the resource lives</span></span>
  - <span data-ttu-id="139a5-172">`[Tag <ITrackedResourceTags>]`: теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="139a5-172">`[Tag <ITrackedResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="139a5-173">`[(Any) <String>]`— это означает, что к этому объекту можно добавить любое свойство.</span><span class="sxs-lookup"><span data-stu-id="139a5-173">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="139a5-174">`[AutoUpgradeMinorVersion <Boolean?>]`: указывает, следует ли использовать в расширении более новую дополнительное версию, если она доступна во время развертывания.</span><span class="sxs-lookup"><span data-stu-id="139a5-174">`[AutoUpgradeMinorVersion <Boolean?>]`: Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span> <span data-ttu-id="139a5-175">Однако после развертывания расширение не будет обновлять дополнительные версии, если не развернуть их снова, даже если для этого свойства установлено true.</span><span class="sxs-lookup"><span data-stu-id="139a5-175">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>
  - <span data-ttu-id="139a5-176">`[ForceUpdateTag <String>]`. Как обработник расширений должен быть принудительно обновляться, даже если конфигурация расширения не изменилась.</span><span class="sxs-lookup"><span data-stu-id="139a5-176">`[ForceUpdateTag <String>]`: How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>
  - <span data-ttu-id="139a5-177">`[MachineExtensionType <String>]`: тип расширения; например: CustomScriptExtension.</span><span class="sxs-lookup"><span data-stu-id="139a5-177">`[MachineExtensionType <String>]`: Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>
  - <span data-ttu-id="139a5-178">`[ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]`: Расширение может содержать защищенные параметрыSettings или protectedSettingsFromKeyVault или не защищенные параметры.</span><span class="sxs-lookup"><span data-stu-id="139a5-178">`[ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]`: The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>
  - <span data-ttu-id="139a5-179">`[Publisher <String>]`: имя издателя обработера расширений.</span><span class="sxs-lookup"><span data-stu-id="139a5-179">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
  - <span data-ttu-id="139a5-180">`[Setting <IMachineExtensionPropertiesSettings>]`: общедоступные параметры расширения, отформатированные Json.</span><span class="sxs-lookup"><span data-stu-id="139a5-180">`[Setting <IMachineExtensionPropertiesSettings>]`: Json formatted public settings for the extension.</span></span>
  - <span data-ttu-id="139a5-181">`[TypeHandlerVersion <String>]`: определяет версию обработера сценариев.</span><span class="sxs-lookup"><span data-stu-id="139a5-181">`[TypeHandlerVersion <String>]`: Specifies the version of the script handler.</span></span>

## <span data-ttu-id="139a5-182">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="139a5-182">RELATED LINKS</span></span>


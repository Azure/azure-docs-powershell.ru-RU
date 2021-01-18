---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/new-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/New-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/New-AzConnectedMachineExtension.md
ms.openlocfilehash: 13095d24bd095e27bac788d0d578bdcdf3e1a0f7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98519414"
---
# <span data-ttu-id="920a3-101">New-AzConnectedMachineExtension</span><span class="sxs-lookup"><span data-stu-id="920a3-101">New-AzConnectedMachineExtension</span></span>

## <span data-ttu-id="920a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="920a3-102">SYNOPSIS</span></span>
<span data-ttu-id="920a3-103">Операция создания или обновления расширения.</span><span class="sxs-lookup"><span data-stu-id="920a3-103">The operation to create or update the extension.</span></span>

## <span data-ttu-id="920a3-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="920a3-104">SYNTAX</span></span>

### <span data-ttu-id="920a3-105">CreateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="920a3-105">CreateExpanded (Default)</span></span>
```
New-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -Location <String> [-SubscriptionId <String>] [-AutoUpgradeMinorVersion] [-ExtensionType <String>]
 [-ForceRerun <String>] [-ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]
 [-Publisher <String>] [-Setting <IMachineExtensionPropertiesSettings>] [-Tag <Hashtable>]
 [-TypeHandlerVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="920a3-106">"Создать"</span><span class="sxs-lookup"><span data-stu-id="920a3-106">Create</span></span>
```
New-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -ExtensionParameter <IMachineExtension> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="920a3-107">CreateViaIdentity</span><span class="sxs-lookup"><span data-stu-id="920a3-107">CreateViaIdentity</span></span>
```
New-AzConnectedMachineExtension -InputObject <IConnectedMachineIdentity>
 -ExtensionParameter <IMachineExtension> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="920a3-108">CreateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="920a3-108">CreateViaIdentityExpanded</span></span>
```
New-AzConnectedMachineExtension -InputObject <IConnectedMachineIdentity> -Location <String>
 [-AutoUpgradeMinorVersion] [-ExtensionType <String>] [-ForceRerun <String>]
 [-ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>] [-Publisher <String>]
 [-Setting <IMachineExtensionPropertiesSettings>] [-Tag <Hashtable>] [-TypeHandlerVersion <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="920a3-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="920a3-109">DESCRIPTION</span></span>
<span data-ttu-id="920a3-110">Операция создания или обновления расширения.</span><span class="sxs-lookup"><span data-stu-id="920a3-110">The operation to create or update the extension.</span></span>

## <span data-ttu-id="920a3-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="920a3-111">EXAMPLES</span></span>

### <span data-ttu-id="920a3-112">Пример 1. Добавление нового расширения на компьютер</span><span class="sxs-lookup"><span data-stu-id="920a3-112">Example 1: Add a new extension to a machine</span></span>
```powershell
PS C:\> $Settings = @{ "commandToExecute" = "powershell.exe -c Get-Process" }
PS C:\> New-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName win-eastus1 -Location eastus -Publisher "Microsoft.Compute" -TypeHandlerVersion 1.10 -Settings $Settings -ExtensionType CustomScriptExtension

Name   Location ProvisioningState
----   -------- -----------------
custom eastus   Succeeded
```

<span data-ttu-id="920a3-113">Задает расширение на компьютере.</span><span class="sxs-lookup"><span data-stu-id="920a3-113">Sets an extension on a machine.</span></span>

### <span data-ttu-id="920a3-114">Пример 2. Добавление нового расширения с параметрами расширения, указанными через конвейер</span><span class="sxs-lookup"><span data-stu-id="920a3-114">Example 2: Add a new extension with extension parameters specified via the pipeline</span></span>
```powershell
PS C:\> $otherExtension = Get-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName other
PS C:\> $otherExtension | New-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName important

Name   Location ProvisioningState
----   -------- -----------------
custom eastus   Succeeded
```

<span data-ttu-id="920a3-115">При этом будет создаваться новое расширение с параметрами расширения, предоставленными объектом, переданным через канал.</span><span class="sxs-lookup"><span data-stu-id="920a3-115">This creates a new extension with the extension parameters provided by the object passed in via the pipeline.</span></span>
<span data-ttu-id="920a3-116">Это очень здорово, если вы хотите захватить параметры одного компьютера и применить его к другому компьютеру.</span><span class="sxs-lookup"><span data-stu-id="920a3-116">This is great if you want to grab the parameters of one machine and apply it to another machine.</span></span>

### <span data-ttu-id="920a3-117">Пример 3. Добавление нового расширения с указанным расположением в конвейере</span><span class="sxs-lookup"><span data-stu-id="920a3-117">Example 3: Add a new extension with location specified via the pipeline</span></span>
```powershell
PS C:\> $identity = [Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.ConnectedMachineIdentity]@{
    Id = "/subscriptions/$($SubscriptionId)/resourceGroups/$($ResourceGroupName)/providers/Microsoft.HybridCompute/machines/$MachineName/extensions/$ExtensionName"
}
PS C:\> $Settings = @{ "commandToExecute" = "powershell.exe -c Get-Process" }
PS C:\> $identity | New-AzConnectedMachineExtension -Location eastus -Publisher "Microsoft.Compute" -TypeHandlerVersion 1.10 -Settings $Settings -ExtensionType CustomScriptExtension

Name   Location ProvisioningState
----   -------- -----------------
custom eastus   Succeeded
```

<span data-ttu-id="920a3-118">При этом будет создаваться расширение компьютера с использованием удостоверения, предоставленного через канал.</span><span class="sxs-lookup"><span data-stu-id="920a3-118">This creates a new machine extension using the identity provided via the pipeline.</span></span>
<span data-ttu-id="920a3-119">Скорее всего, вы не сделаете этого, но это возможно.</span><span class="sxs-lookup"><span data-stu-id="920a3-119">You likely won't do this, but it's possible.</span></span>

### <span data-ttu-id="920a3-120">Пример 4. Добавление нового расширения с использованием объекта расширения в качестве расположения и параметров обновления</span><span class="sxs-lookup"><span data-stu-id="920a3-120">Example 4: Add a new extension using an extension object as both the location and parameters for updating</span></span>
```powershell
PS C:\> $ext = Get-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName other
PS C:\> $ext | New-AzConnectedMachineExtension -ExtensionParameter $ext
```

<span data-ttu-id="920a3-121">При этом будет создаваться расширение компьютера с использованием удостоверения, предоставленного через канал, и сведений о расширении, предоставленного в объекте расширения.</span><span class="sxs-lookup"><span data-stu-id="920a3-121">This creates a new machine extension using the identity provided via the pipeline and the extension details provided by the passed in extension object.</span></span>
<span data-ttu-id="920a3-122">Скорее всего, вы не сделаете этого, но это возможно.</span><span class="sxs-lookup"><span data-stu-id="920a3-122">You likely won't do this, but it's possible.</span></span>

## <span data-ttu-id="920a3-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="920a3-123">PARAMETERS</span></span>

### <span data-ttu-id="920a3-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="920a3-124">-AsJob</span></span>
<span data-ttu-id="920a3-125">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="920a3-125">Run the command as a job</span></span>

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

### <span data-ttu-id="920a3-126">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="920a3-126">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="920a3-127">Указывает, следует ли использовать в расширении более новую версию, если она доступна во время развертывания.</span><span class="sxs-lookup"><span data-stu-id="920a3-127">Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span>
<span data-ttu-id="920a3-128">Однако после развертывания расширение не будет обновлять дополнительные версии, если не развернуть их снова, даже если для этого свойства установлено true.</span><span class="sxs-lookup"><span data-stu-id="920a3-128">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="920a3-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="920a3-129">-DefaultProfile</span></span>
<span data-ttu-id="920a3-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="920a3-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="920a3-131">-ExtensionParameter</span><span class="sxs-lookup"><span data-stu-id="920a3-131">-ExtensionParameter</span></span>
<span data-ttu-id="920a3-132">Описание расширения компьютера.</span><span class="sxs-lookup"><span data-stu-id="920a3-132">Describes a Machine Extension.</span></span>
<span data-ttu-id="920a3-133">Чтобы создать таблицу, см. раздел "ЗАМЕТКИ" для свойств EXTENSIONPARAMETER и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="920a3-133">To construct, see NOTES section for EXTENSIONPARAMETER properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension
Parameter Sets: Create, CreateViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="920a3-134">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="920a3-134">-ExtensionType</span></span>
<span data-ttu-id="920a3-135">Тип расширения. Например: CustomScriptExtension.</span><span class="sxs-lookup"><span data-stu-id="920a3-135">Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="920a3-136">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="920a3-136">-ForceRerun</span></span>
<span data-ttu-id="920a3-137">Как обработник расширений должен быть принудительно обновляться, даже если конфигурация расширения не изменилась.</span><span class="sxs-lookup"><span data-stu-id="920a3-137">How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="920a3-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="920a3-138">-InputObject</span></span>
<span data-ttu-id="920a3-139">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="920a3-139">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity
Parameter Sets: CreateViaIdentity, CreateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="920a3-140">-Location</span><span class="sxs-lookup"><span data-stu-id="920a3-140">-Location</span></span>
<span data-ttu-id="920a3-141">Географическое расположение ресурса</span><span class="sxs-lookup"><span data-stu-id="920a3-141">The geo-location where the resource lives</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="920a3-142">-MachineName</span><span class="sxs-lookup"><span data-stu-id="920a3-142">-MachineName</span></span>
<span data-ttu-id="920a3-143">Имя компьютера, на котором нужно создать или обновить расширение.</span><span class="sxs-lookup"><span data-stu-id="920a3-143">The name of the machine where the extension should be created or updated.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="920a3-144">-Name</span><span class="sxs-lookup"><span data-stu-id="920a3-144">-Name</span></span>
<span data-ttu-id="920a3-145">Имя расширения компьютера.</span><span class="sxs-lookup"><span data-stu-id="920a3-145">The name of the machine extension.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="920a3-146">-NoWait</span><span class="sxs-lookup"><span data-stu-id="920a3-146">-NoWait</span></span>
<span data-ttu-id="920a3-147">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="920a3-147">Run the command asynchronously</span></span>

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

### <span data-ttu-id="920a3-148">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="920a3-148">-ProtectedSetting</span></span>
<span data-ttu-id="920a3-149">Расширение может содержать защищенные параметрыSettings или protectedSettingsFromKeyVault или не защищенные параметры.</span><span class="sxs-lookup"><span data-stu-id="920a3-149">The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionPropertiesProtectedSettings
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases: ProtectedSettings

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="920a3-150">-Publisher</span><span class="sxs-lookup"><span data-stu-id="920a3-150">-Publisher</span></span>
<span data-ttu-id="920a3-151">Имя издателя обработера расширений.</span><span class="sxs-lookup"><span data-stu-id="920a3-151">The name of the extension handler publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="920a3-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="920a3-152">-ResourceGroupName</span></span>
<span data-ttu-id="920a3-153">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="920a3-153">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="920a3-154">-Setting</span><span class="sxs-lookup"><span data-stu-id="920a3-154">-Setting</span></span>
<span data-ttu-id="920a3-155">Общедоступные параметры расширения, отформатированные Json.</span><span class="sxs-lookup"><span data-stu-id="920a3-155">Json formatted public settings for the extension.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionPropertiesSettings
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases: Settings

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="920a3-156">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="920a3-156">-SubscriptionId</span></span>
<span data-ttu-id="920a3-157">Учетные данные подписки, однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="920a3-157">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="920a3-158">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="920a3-158">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="920a3-159">-Tag</span><span class="sxs-lookup"><span data-stu-id="920a3-159">-Tag</span></span>
<span data-ttu-id="920a3-160">Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="920a3-160">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="920a3-161">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="920a3-161">-TypeHandlerVersion</span></span>
<span data-ttu-id="920a3-162">Определяет версию обработера сценариев.</span><span class="sxs-lookup"><span data-stu-id="920a3-162">Specifies the version of the script handler.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="920a3-163">-Confirm</span><span class="sxs-lookup"><span data-stu-id="920a3-163">-Confirm</span></span>
<span data-ttu-id="920a3-164">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="920a3-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="920a3-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="920a3-165">-WhatIf</span></span>
<span data-ttu-id="920a3-166">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="920a3-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="920a3-167">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="920a3-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="920a3-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="920a3-168">CommonParameters</span></span>
<span data-ttu-id="920a3-169">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="920a3-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="920a3-170">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="920a3-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="920a3-171">INPUTS</span><span class="sxs-lookup"><span data-stu-id="920a3-171">INPUTS</span></span>

### <span data-ttu-id="920a3-172">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMa modelse.Models.Api20200802.IMa modelseExtension</span><span class="sxs-lookup"><span data-stu-id="920a3-172">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

### <span data-ttu-id="920a3-173">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMa modelse.Models.IConnectedMa modelseIdentity</span><span class="sxs-lookup"><span data-stu-id="920a3-173">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span></span>

## <span data-ttu-id="920a3-174">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="920a3-174">OUTPUTS</span></span>

### <span data-ttu-id="920a3-175">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMa modelse.Models.Api20200802.IMa modelseExtension</span><span class="sxs-lookup"><span data-stu-id="920a3-175">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

## <span data-ttu-id="920a3-176">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="920a3-176">NOTES</span></span>

<span data-ttu-id="920a3-177">ALIASES</span><span class="sxs-lookup"><span data-stu-id="920a3-177">ALIASES</span></span>

<span data-ttu-id="920a3-178">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="920a3-178">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="920a3-179">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="920a3-179">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="920a3-180">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="920a3-180">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="920a3-181">EXTENSIONPARAMETER: <IMachineExtension> описание расширения компьютера.</span><span class="sxs-lookup"><span data-stu-id="920a3-181">EXTENSIONPARAMETER <IMachineExtension>: Describes a Machine Extension.</span></span>
  - <span data-ttu-id="920a3-182">`Location <String>`: географическое расположение ресурса</span><span class="sxs-lookup"><span data-stu-id="920a3-182">`Location <String>`: The geo-location where the resource lives</span></span>
  - <span data-ttu-id="920a3-183">`[Tag <ITrackedResourceTags>]`: теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="920a3-183">`[Tag <ITrackedResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="920a3-184">`[(Any) <String>]`— это означает, что к этому объекту можно добавить любое свойство.</span><span class="sxs-lookup"><span data-stu-id="920a3-184">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="920a3-185">`[AutoUpgradeMinorVersion <Boolean?>]`: указывает, следует ли использовать в расширении более новую версию, если она доступна во время развертывания.</span><span class="sxs-lookup"><span data-stu-id="920a3-185">`[AutoUpgradeMinorVersion <Boolean?>]`: Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span> <span data-ttu-id="920a3-186">Однако после развертывания расширение не будет обновлять дополнительные версии, если не развернуть их снова, даже если для этого свойства установлено true.</span><span class="sxs-lookup"><span data-stu-id="920a3-186">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>
  - <span data-ttu-id="920a3-187">`[ForceUpdateTag <String>]`. Как обработник расширений должен быть принудительно обновляться, даже если конфигурация расширения не изменилась.</span><span class="sxs-lookup"><span data-stu-id="920a3-187">`[ForceUpdateTag <String>]`: How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>
  - <span data-ttu-id="920a3-188">`[MachineExtensionType <String>]`: тип расширения; Например: CustomScriptExtension.</span><span class="sxs-lookup"><span data-stu-id="920a3-188">`[MachineExtensionType <String>]`: Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>
  - <span data-ttu-id="920a3-189">`[ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]`: Расширение может содержать защищенные параметрыSettings или protectedSettingsFromKeyVault или не защищенные параметры.</span><span class="sxs-lookup"><span data-stu-id="920a3-189">`[ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]`: The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>
  - <span data-ttu-id="920a3-190">`[Publisher <String>]`: имя издателя обработера расширений.</span><span class="sxs-lookup"><span data-stu-id="920a3-190">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
  - <span data-ttu-id="920a3-191">`[Setting <IMachineExtensionPropertiesSettings>]`: Общедоступные параметры расширения отформатированы Json.</span><span class="sxs-lookup"><span data-stu-id="920a3-191">`[Setting <IMachineExtensionPropertiesSettings>]`: Json formatted public settings for the extension.</span></span>
  - <span data-ttu-id="920a3-192">`[TypeHandlerVersion <String>]`: определяет версию обработера сценариев.</span><span class="sxs-lookup"><span data-stu-id="920a3-192">`[TypeHandlerVersion <String>]`: Specifies the version of the script handler.</span></span>

<span data-ttu-id="920a3-193">INPUTOBJECT <IConnectedMachineIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="920a3-193">INPUTOBJECT <IConnectedMachineIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="920a3-194">`[ExtensionName <String>]`: имя расширения компьютера.</span><span class="sxs-lookup"><span data-stu-id="920a3-194">`[ExtensionName <String>]`: The name of the machine extension.</span></span>
  - <span data-ttu-id="920a3-195">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="920a3-195">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="920a3-196">`[Name <String>]`: имя гибридной машины.</span><span class="sxs-lookup"><span data-stu-id="920a3-196">`[Name <String>]`: The name of the hybrid machine.</span></span>
  - <span data-ttu-id="920a3-197">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="920a3-197">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="920a3-198">`[SubscriptionId <String>]`: учетные данные подписки, однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="920a3-198">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="920a3-199">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="920a3-199">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="920a3-200">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="920a3-200">RELATED LINKS</span></span>


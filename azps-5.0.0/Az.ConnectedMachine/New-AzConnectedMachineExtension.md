---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/new-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/New-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/New-AzConnectedMachineExtension.md
ms.openlocfilehash: 13095d24bd095e27bac788d0d578bdcdf3e1a0f7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248739"
---
# <span data-ttu-id="07b09-101">New-AzConnectedMachineExtension</span><span class="sxs-lookup"><span data-stu-id="07b09-101">New-AzConnectedMachineExtension</span></span>

## <span data-ttu-id="07b09-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="07b09-102">SYNOPSIS</span></span>
<span data-ttu-id="07b09-103">Операция, позволяющая создать или обновить расширение.</span><span class="sxs-lookup"><span data-stu-id="07b09-103">The operation to create or update the extension.</span></span>

## <span data-ttu-id="07b09-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="07b09-104">SYNTAX</span></span>

### <span data-ttu-id="07b09-105">CreateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="07b09-105">CreateExpanded (Default)</span></span>
```
New-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -Location <String> [-SubscriptionId <String>] [-AutoUpgradeMinorVersion] [-ExtensionType <String>]
 [-ForceRerun <String>] [-ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]
 [-Publisher <String>] [-Setting <IMachineExtensionPropertiesSettings>] [-Tag <Hashtable>]
 [-TypeHandlerVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="07b09-106">Заново</span><span class="sxs-lookup"><span data-stu-id="07b09-106">Create</span></span>
```
New-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -ExtensionParameter <IMachineExtension> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="07b09-107">CreateViaIdentity</span><span class="sxs-lookup"><span data-stu-id="07b09-107">CreateViaIdentity</span></span>
```
New-AzConnectedMachineExtension -InputObject <IConnectedMachineIdentity>
 -ExtensionParameter <IMachineExtension> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="07b09-108">CreateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="07b09-108">CreateViaIdentityExpanded</span></span>
```
New-AzConnectedMachineExtension -InputObject <IConnectedMachineIdentity> -Location <String>
 [-AutoUpgradeMinorVersion] [-ExtensionType <String>] [-ForceRerun <String>]
 [-ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>] [-Publisher <String>]
 [-Setting <IMachineExtensionPropertiesSettings>] [-Tag <Hashtable>] [-TypeHandlerVersion <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="07b09-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="07b09-109">DESCRIPTION</span></span>
<span data-ttu-id="07b09-110">Операция, позволяющая создать или обновить расширение.</span><span class="sxs-lookup"><span data-stu-id="07b09-110">The operation to create or update the extension.</span></span>

## <span data-ttu-id="07b09-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="07b09-111">EXAMPLES</span></span>

### <span data-ttu-id="07b09-112">Пример 1: Добавление нового расширения для компьютера</span><span class="sxs-lookup"><span data-stu-id="07b09-112">Example 1: Add a new extension to a machine</span></span>
```powershell
PS C:\> $Settings = @{ "commandToExecute" = "powershell.exe -c Get-Process" }
PS C:\> New-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName win-eastus1 -Location eastus -Publisher "Microsoft.Compute" -TypeHandlerVersion 1.10 -Settings $Settings -ExtensionType CustomScriptExtension

Name   Location ProvisioningState
----   -------- -----------------
custom eastus   Succeeded
```

<span data-ttu-id="07b09-113">Задает расширение на компьютере.</span><span class="sxs-lookup"><span data-stu-id="07b09-113">Sets an extension on a machine.</span></span>

### <span data-ttu-id="07b09-114">Пример 2: Добавление нового расширения с параметрами расширения, указанными через конвейер</span><span class="sxs-lookup"><span data-stu-id="07b09-114">Example 2: Add a new extension with extension parameters specified via the pipeline</span></span>
```powershell
PS C:\> $otherExtension = Get-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName other
PS C:\> $otherExtension | New-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName important

Name   Location ProvisioningState
----   -------- -----------------
custom eastus   Succeeded
```

<span data-ttu-id="07b09-115">В результате будет создано новое расширение с параметрами расширения, предоставленными объектом, передаваемым через конвейер.</span><span class="sxs-lookup"><span data-stu-id="07b09-115">This creates a new extension with the extension parameters provided by the object passed in via the pipeline.</span></span>
<span data-ttu-id="07b09-116">Это очень удобно, если вы хотите захватить параметры одного компьютера и применить его к другому компьютеру.</span><span class="sxs-lookup"><span data-stu-id="07b09-116">This is great if you want to grab the parameters of one machine and apply it to another machine.</span></span>

### <span data-ttu-id="07b09-117">Пример 3: Добавление нового расширения с расположением, указанным через конвейер</span><span class="sxs-lookup"><span data-stu-id="07b09-117">Example 3: Add a new extension with location specified via the pipeline</span></span>
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

<span data-ttu-id="07b09-118">Это приведет к созданию нового расширения компьютера с помощью удостоверения, указанного через конвейер.</span><span class="sxs-lookup"><span data-stu-id="07b09-118">This creates a new machine extension using the identity provided via the pipeline.</span></span>
<span data-ttu-id="07b09-119">Возможно, вам не удастся это сделать.</span><span class="sxs-lookup"><span data-stu-id="07b09-119">You likely won't do this, but it's possible.</span></span>

### <span data-ttu-id="07b09-120">Пример 4: Добавление нового расширения с помощью объекта расширения в качестве местоположения и параметров для обновления</span><span class="sxs-lookup"><span data-stu-id="07b09-120">Example 4: Add a new extension using an extension object as both the location and parameters for updating</span></span>
```powershell
PS C:\> $ext = Get-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName other
PS C:\> $ext | New-AzConnectedMachineExtension -ExtensionParameter $ext
```

<span data-ttu-id="07b09-121">Это приведет к созданию нового расширения компьютера с использованием удостоверения, предоставленного через конвейер, и подробных сведений о расширении, предоставленных объектом, передаваемым в объекте Extension.</span><span class="sxs-lookup"><span data-stu-id="07b09-121">This creates a new machine extension using the identity provided via the pipeline and the extension details provided by the passed in extension object.</span></span>
<span data-ttu-id="07b09-122">Возможно, вам не удастся это сделать.</span><span class="sxs-lookup"><span data-stu-id="07b09-122">You likely won't do this, but it's possible.</span></span>

## <span data-ttu-id="07b09-123">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="07b09-123">PARAMETERS</span></span>

### <span data-ttu-id="07b09-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="07b09-124">-AsJob</span></span>
<span data-ttu-id="07b09-125">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="07b09-125">Run the command as a job</span></span>

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

### <span data-ttu-id="07b09-126">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="07b09-126">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="07b09-127">Указывает, должно ли расширение использовать более новую вспомогательную версию, если она доступна во время развертывания.</span><span class="sxs-lookup"><span data-stu-id="07b09-127">Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span>
<span data-ttu-id="07b09-128">Однако после развертывания расширение не будет обновлять дополнительные версии, если только повторно не развернуто, даже если для этого свойства задано значение true.</span><span class="sxs-lookup"><span data-stu-id="07b09-128">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>

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

### <span data-ttu-id="07b09-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07b09-129">-DefaultProfile</span></span>
<span data-ttu-id="07b09-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="07b09-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07b09-131">-ExtensionParameter</span><span class="sxs-lookup"><span data-stu-id="07b09-131">-ExtensionParameter</span></span>
<span data-ttu-id="07b09-132">Описывает расширение компьютера.</span><span class="sxs-lookup"><span data-stu-id="07b09-132">Describes a Machine Extension.</span></span>
<span data-ttu-id="07b09-133">Для конструирования ознакомьтесь с разделом "Заметки" для свойств EXTENSIONPARAMETER и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="07b09-133">To construct, see NOTES section for EXTENSIONPARAMETER properties and create a hash table.</span></span>

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

### <span data-ttu-id="07b09-134">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="07b09-134">-ExtensionType</span></span>
<span data-ttu-id="07b09-135">Указывает тип расширения; Пример: "CustomScriptExtension".</span><span class="sxs-lookup"><span data-stu-id="07b09-135">Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>

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

### <span data-ttu-id="07b09-136">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="07b09-136">-ForceRerun</span></span>
<span data-ttu-id="07b09-137">Как следует принудительно обновлять обработчик расширений, даже если конфигурация расширения не изменилась.</span><span class="sxs-lookup"><span data-stu-id="07b09-137">How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>

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

### <span data-ttu-id="07b09-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="07b09-138">-InputObject</span></span>
<span data-ttu-id="07b09-139">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="07b09-139">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="07b09-140">-Location</span><span class="sxs-lookup"><span data-stu-id="07b09-140">-Location</span></span>
<span data-ttu-id="07b09-141">Географическое расположение, в котором находится ресурс</span><span class="sxs-lookup"><span data-stu-id="07b09-141">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="07b09-142">-MachineName</span><span class="sxs-lookup"><span data-stu-id="07b09-142">-MachineName</span></span>
<span data-ttu-id="07b09-143">Имя компьютера, на котором нужно создать или обновить расширение.</span><span class="sxs-lookup"><span data-stu-id="07b09-143">The name of the machine where the extension should be created or updated.</span></span>

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

### <span data-ttu-id="07b09-144">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="07b09-144">-Name</span></span>
<span data-ttu-id="07b09-145">Имя расширения компьютера.</span><span class="sxs-lookup"><span data-stu-id="07b09-145">The name of the machine extension.</span></span>

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

### <span data-ttu-id="07b09-146">-Wait</span><span class="sxs-lookup"><span data-stu-id="07b09-146">-NoWait</span></span>
<span data-ttu-id="07b09-147">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="07b09-147">Run the command asynchronously</span></span>

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

### <span data-ttu-id="07b09-148">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="07b09-148">-ProtectedSetting</span></span>
<span data-ttu-id="07b09-149">Расширение может содержать либо protectedSettings, либо protectedSettingsFromKeyVault, или вообще не защищенные параметры.</span><span class="sxs-lookup"><span data-stu-id="07b09-149">The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>

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

### <span data-ttu-id="07b09-150">-Publisher</span><span class="sxs-lookup"><span data-stu-id="07b09-150">-Publisher</span></span>
<span data-ttu-id="07b09-151">Имя издателя обработчика расширений.</span><span class="sxs-lookup"><span data-stu-id="07b09-151">The name of the extension handler publisher.</span></span>

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

### <span data-ttu-id="07b09-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07b09-152">-ResourceGroupName</span></span>
<span data-ttu-id="07b09-153">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="07b09-153">The name of the resource group.</span></span>

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

### <span data-ttu-id="07b09-154">-Параметр</span><span class="sxs-lookup"><span data-stu-id="07b09-154">-Setting</span></span>
<span data-ttu-id="07b09-155">Отформатированные общедоступные параметры JSON для расширения.</span><span class="sxs-lookup"><span data-stu-id="07b09-155">Json formatted public settings for the extension.</span></span>

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

### <span data-ttu-id="07b09-156">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="07b09-156">-SubscriptionId</span></span>
<span data-ttu-id="07b09-157">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="07b09-157">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="07b09-158">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="07b09-158">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="07b09-159">-Тег</span><span class="sxs-lookup"><span data-stu-id="07b09-159">-Tag</span></span>
<span data-ttu-id="07b09-160">Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="07b09-160">Resource tags.</span></span>

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

### <span data-ttu-id="07b09-161">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="07b09-161">-TypeHandlerVersion</span></span>
<span data-ttu-id="07b09-162">Указывает версию обработчика сценария.</span><span class="sxs-lookup"><span data-stu-id="07b09-162">Specifies the version of the script handler.</span></span>

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

### <span data-ttu-id="07b09-163">-Confirm</span><span class="sxs-lookup"><span data-stu-id="07b09-163">-Confirm</span></span>
<span data-ttu-id="07b09-164">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="07b09-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07b09-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07b09-165">-WhatIf</span></span>
<span data-ttu-id="07b09-166">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="07b09-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07b09-167">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="07b09-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07b09-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07b09-168">CommonParameters</span></span>
<span data-ttu-id="07b09-169">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="07b09-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07b09-170">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="07b09-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07b09-171">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="07b09-171">INPUTS</span></span>

### <span data-ttu-id="07b09-172">Microsoft. Azure. PowerShell. командлеты. ConnectedMachine. Models. Api20200802. IMachineExtension</span><span class="sxs-lookup"><span data-stu-id="07b09-172">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

### <span data-ttu-id="07b09-173">Microsoft. Azure. PowerShell. командлеты. ConnectedMachine. Models. IConnectedMachineIdentity</span><span class="sxs-lookup"><span data-stu-id="07b09-173">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span></span>

## <span data-ttu-id="07b09-174">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="07b09-174">OUTPUTS</span></span>

### <span data-ttu-id="07b09-175">Microsoft. Azure. PowerShell. командлеты. ConnectedMachine. Models. Api20200802. IMachineExtension</span><span class="sxs-lookup"><span data-stu-id="07b09-175">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

## <span data-ttu-id="07b09-176">Пуск</span><span class="sxs-lookup"><span data-stu-id="07b09-176">NOTES</span></span>

<span data-ttu-id="07b09-177">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="07b09-177">ALIASES</span></span>

<span data-ttu-id="07b09-178">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="07b09-178">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="07b09-179">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="07b09-179">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="07b09-180">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="07b09-180">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="07b09-181">EXTENSIONPARAMETER <IMachineExtension> : описывает расширение компьютера.</span><span class="sxs-lookup"><span data-stu-id="07b09-181">EXTENSIONPARAMETER <IMachineExtension>: Describes a Machine Extension.</span></span>
  - <span data-ttu-id="07b09-182">`Location <String>`: Географическое расположение, в котором находится ресурс</span><span class="sxs-lookup"><span data-stu-id="07b09-182">`Location <String>`: The geo-location where the resource lives</span></span>
  - <span data-ttu-id="07b09-183">`[Tag <ITrackedResourceTags>]`: Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="07b09-183">`[Tag <ITrackedResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="07b09-184">`[(Any) <String>]`: Это указывает на то, что в этот объект можно добавить любое свойство.</span><span class="sxs-lookup"><span data-stu-id="07b09-184">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="07b09-185">`[AutoUpgradeMinorVersion <Boolean?>]`: Указывает, должно ли расширение использовать более новую вспомогательную версию, если она доступна во время развертывания.</span><span class="sxs-lookup"><span data-stu-id="07b09-185">`[AutoUpgradeMinorVersion <Boolean?>]`: Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span> <span data-ttu-id="07b09-186">Однако после развертывания расширение не будет обновлять дополнительные версии, если только повторно не развернуто, даже если для этого свойства задано значение true.</span><span class="sxs-lookup"><span data-stu-id="07b09-186">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>
  - <span data-ttu-id="07b09-187">`[ForceUpdateTag <String>]`: Как следует принудительно обновлять обработчик расширений, даже если конфигурация расширения не изменилась.</span><span class="sxs-lookup"><span data-stu-id="07b09-187">`[ForceUpdateTag <String>]`: How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>
  - <span data-ttu-id="07b09-188">`[MachineExtensionType <String>]`: Указывает тип расширения; Пример: "CustomScriptExtension".</span><span class="sxs-lookup"><span data-stu-id="07b09-188">`[MachineExtensionType <String>]`: Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>
  - <span data-ttu-id="07b09-189">`[ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]`: Расширение может содержать либо protectedSettings, либо protectedSettingsFromKeyVault, или вообще не защищенные параметры.</span><span class="sxs-lookup"><span data-stu-id="07b09-189">`[ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]`: The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>
  - <span data-ttu-id="07b09-190">`[Publisher <String>]`: Имя издателя обработчика расширений.</span><span class="sxs-lookup"><span data-stu-id="07b09-190">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
  - <span data-ttu-id="07b09-191">`[Setting <IMachineExtensionPropertiesSettings>]`: Отформатированные общедоступные параметры JSON для расширения.</span><span class="sxs-lookup"><span data-stu-id="07b09-191">`[Setting <IMachineExtensionPropertiesSettings>]`: Json formatted public settings for the extension.</span></span>
  - <span data-ttu-id="07b09-192">`[TypeHandlerVersion <String>]`: Определяет версию обработчика сценария.</span><span class="sxs-lookup"><span data-stu-id="07b09-192">`[TypeHandlerVersion <String>]`: Specifies the version of the script handler.</span></span>

<span data-ttu-id="07b09-193">INPUTOBJECT <IConnectedMachineIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="07b09-193">INPUTOBJECT <IConnectedMachineIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="07b09-194">`[ExtensionName <String>]`: Имя расширения компьютера.</span><span class="sxs-lookup"><span data-stu-id="07b09-194">`[ExtensionName <String>]`: The name of the machine extension.</span></span>
  - <span data-ttu-id="07b09-195">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="07b09-195">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="07b09-196">`[Name <String>]`: Имя гибридного компьютера.</span><span class="sxs-lookup"><span data-stu-id="07b09-196">`[Name <String>]`: The name of the hybrid machine.</span></span>
  - <span data-ttu-id="07b09-197">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="07b09-197">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="07b09-198">`[SubscriptionId <String>]`: Учетные данные подписки, однозначно определяющие подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="07b09-198">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="07b09-199">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="07b09-199">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="07b09-200">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="07b09-200">RELATED LINKS</span></span>


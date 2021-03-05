---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 73E6DF02-7171-481B-966F-DECEC122A602
online version: https://docs.microsoft.com/powershell/module/az.automation/register-azautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Register-AzAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Register-AzAutomationDscNode.md
ms.openlocfilehash: ceae5a9e7dec9913d90aae836784c6bfe66b680f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010003"
---
# <span data-ttu-id="ef176-101">Register-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="ef176-101">Register-AzAutomationDscNode</span></span>

## <span data-ttu-id="ef176-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef176-102">SYNOPSIS</span></span>
<span data-ttu-id="ef176-103">Регистрирует виртуальную машину Azure под управлением Ос Windows в качестве узла DSC для учетной записи автоматизации.</span><span class="sxs-lookup"><span data-stu-id="ef176-103">Registers an Azure virtual machine running Windows OS as a DSC node for an Automation account.</span></span>

## <span data-ttu-id="ef176-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ef176-104">SYNTAX</span></span>

```
Register-AzAutomationDscNode -AzureVMName <String> [-NodeConfigurationName <String>]
 [-ConfigurationMode <String>] [-ConfigurationModeFrequencyMins <Int32>] [-RefreshFrequencyMins <Int32>]
 [-RebootNodeIfNeeded <Boolean>] [-ActionAfterReboot <String>] [-AllowModuleOverwrite <Boolean>]
 [-AzureVMResourceGroup <String>] [-AzureVMLocation <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ef176-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ef176-105">DESCRIPTION</span></span>
<span data-ttu-id="ef176-106">**Cmdlet Register-AzAutomationDscNode** регистрирует виртуальную машину Azure как узел APS Desired State Configuration (DSC) в учетной записи автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="ef176-106">The **Register-AzAutomationDscNode** cmdlet registers an Azure virtual machine as an APS Desired State Configuration (DSC) node in an Azure Automation account.</span></span> <span data-ttu-id="ef176-107">Этот cmdlet будет зарегистрировать VMs в операционной системы Windows OS только в качестве узла DSC автоматизации для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="ef176-107">This cmdlet will only register VMs running Windows OS as an Automation DSC Node for an account.</span></span>

<span data-ttu-id="ef176-108">Если вам нужно зарегистрировать узел в учетной записи автоматизации в другой подписке, необходимо использовать ARM, а не cmdlets.</span><span class="sxs-lookup"><span data-stu-id="ef176-108">If you need to register a node to an automation account in a different subscription, you will need to use an ARM template rather than cmdlets.</span></span> <span data-ttu-id="ef176-109">Дополнительные сведения см. [в документации](https://docs.microsoft.com/azure/automation/automation-dsc-onboarding#registering-virtual-machines-across-azure-subscriptions) автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="ef176-109">See the Azure Automation [documentation](https://docs.microsoft.com/azure/automation/automation-dsc-onboarding#registering-virtual-machines-across-azure-subscriptions) for more details.</span></span>

## <span data-ttu-id="ef176-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ef176-110">EXAMPLES</span></span>

### <span data-ttu-id="ef176-111">Пример 1. Регистрация виртуальной машины Azure в качестве узла DSC Azure</span><span class="sxs-lookup"><span data-stu-id="ef176-111">Example 1: Register an Azure virtual machine as an Azure DSC node</span></span>
```
PS C:\>Register-AzAutomationDscNode -AutomationAccountName "Contoso17" -AzureVMName "VirtualMachine01" -ResourceGroupName "ResourceGroup01"-NodeConfigurationName "ContosoConfiguration.webserver"
```

<span data-ttu-id="ef176-112">Эта команда регистрирует виртуальную машину Azure с именем VirtualMachine01 в качестве узла DSC в учетной записи автоматизации Contoso17.</span><span class="sxs-lookup"><span data-stu-id="ef176-112">This command registers the Azure virtual machine named VirtualMachine01 as a DSC node in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="ef176-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ef176-113">PARAMETERS</span></span>

### <span data-ttu-id="ef176-114">-ActionAfterReboot</span><span class="sxs-lookup"><span data-stu-id="ef176-114">-ActionAfterReboot</span></span>
<span data-ttu-id="ef176-115">Определяет действие, которое будет происходить у виртуальной машины после перезапуска.</span><span class="sxs-lookup"><span data-stu-id="ef176-115">Specifies the action that the virtual machine takes after it restarts.</span></span>
<span data-ttu-id="ef176-116">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="ef176-116">Valid values are:</span></span> 
- <span data-ttu-id="ef176-117">ContinueConfiguration</span><span class="sxs-lookup"><span data-stu-id="ef176-117">ContinueConfiguration</span></span> 
- <span data-ttu-id="ef176-118">StopConfiguration</span><span class="sxs-lookup"><span data-stu-id="ef176-118">StopConfiguration</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: ContinueConfiguration, StopConfiguration

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef176-119">-AllowModuleOverwrite</span><span class="sxs-lookup"><span data-stu-id="ef176-119">-AllowModuleOverwrite</span></span>
<span data-ttu-id="ef176-120">Указывает, заменяют ли новые конфигурации, которые этот узел DSC скачивает с загружаемого сервера DSC автоматизации Azure, существующие модули, уже имеющиеся на целевом узле.</span><span class="sxs-lookup"><span data-stu-id="ef176-120">Specifies whether new configurations that this DSC node downloads from the Azure Automation DSC pull server replace the existing modules already on the target node.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef176-121">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ef176-121">-AutomationAccountName</span></span>
<span data-ttu-id="ef176-122">Указывает имя учетной записи автоматизации, в которой этот cmdlet регистрирует виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="ef176-122">Specifies the name of an Automation account in which this cmdlet registers a virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef176-123">-AzureVMLocation</span><span class="sxs-lookup"><span data-stu-id="ef176-123">-AzureVMLocation</span></span>
<span data-ttu-id="ef176-124">Расположение azure VM.</span><span class="sxs-lookup"><span data-stu-id="ef176-124">The Azure VM location.</span></span>

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

### <span data-ttu-id="ef176-125">-AzureVMName</span><span class="sxs-lookup"><span data-stu-id="ef176-125">-AzureVMName</span></span>
<span data-ttu-id="ef176-126">Имя виртуальной машины Azure, которая будет зарегистрирована для управления в службе DSC автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="ef176-126">The name of the Azure virtual machine to register for management with Azure Automation DSC.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef176-127">-AzureVMResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ef176-127">-AzureVMResourceGroup</span></span>
<span data-ttu-id="ef176-128">Имя группы ресурсов Azure VM.</span><span class="sxs-lookup"><span data-stu-id="ef176-128">The Azure VM resource group name.</span></span>

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

### <span data-ttu-id="ef176-129">-ConfigurationMode</span><span class="sxs-lookup"><span data-stu-id="ef176-129">-ConfigurationMode</span></span>
<span data-ttu-id="ef176-130">Определяет режим конфигурации DSC.</span><span class="sxs-lookup"><span data-stu-id="ef176-130">Specifies the DSC configuration mode.</span></span>
<span data-ttu-id="ef176-131">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="ef176-131">Valid values are:</span></span> 
- <span data-ttu-id="ef176-132">ApplyAndMonitor</span><span class="sxs-lookup"><span data-stu-id="ef176-132">ApplyAndMonitor</span></span> 
- <span data-ttu-id="ef176-133">ApplyAndAutocorrect</span><span class="sxs-lookup"><span data-stu-id="ef176-133">ApplyAndAutocorrect</span></span> 
- <span data-ttu-id="ef176-134">ApplyOnly</span><span class="sxs-lookup"><span data-stu-id="ef176-134">ApplyOnly</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: ApplyAndMonitor, ApplyAndAutocorrect, ApplyOnly

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef176-135">-ConfigurationModeFrequencyMins</span><span class="sxs-lookup"><span data-stu-id="ef176-135">-ConfigurationModeFrequencyMins</span></span>
<span data-ttu-id="ef176-136">Определяет частоту в минутах, когда фоновое приложение DSC пытается реализовать текущую конфигурацию на целевом узле.</span><span class="sxs-lookup"><span data-stu-id="ef176-136">Specifies the frequency, in minutes, at which the background application of DSC attempts to implement the current configuration on the target node.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef176-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef176-137">-DefaultProfile</span></span>
<span data-ttu-id="ef176-138">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="ef176-138">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ef176-139">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="ef176-139">-NodeConfigurationName</span></span>
<span data-ttu-id="ef176-140">Указывает имя конфигурации узла, которую этот cmdlet настраивает для виртуальной машины, извлекаемую из DSC автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="ef176-140">Specifies the name of the node configuration that this cmdlet configures the virtual machine to pull from Azure Automation DSC.</span></span>

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

### <span data-ttu-id="ef176-141">-RebootNodeIfNeeded</span><span class="sxs-lookup"><span data-stu-id="ef176-141">-RebootNodeIfNeeded</span></span>
<span data-ttu-id="ef176-142">При необходимости указывает, следует ли перезапускать виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="ef176-142">Specifies whether to restart the virtual machine, if needed.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef176-143">-RefreshFrequencyMins</span><span class="sxs-lookup"><span data-stu-id="ef176-143">-RefreshFrequencyMins</span></span>
<span data-ttu-id="ef176-144">Определяет частоту в минутах, когда локальный диспетчер конфигураций свяжется с сервером загрузки последней конфигурации узла автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="ef176-144">Specifies the frequency, in minutes, at which the local Configuration Manager contacts the Azure Automation DSC pull server to download the latest node configuration.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef176-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef176-145">-ResourceGroupName</span></span>
<span data-ttu-id="ef176-146">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ef176-146">Specifies the name of a resource group.</span></span>
<span data-ttu-id="ef176-147">Учетная запись автоматизации, с помощью которой этот cmdlet регистрирует виртуальную машину, относится к группе ресурсов, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="ef176-147">The Automation account with which this cmdlet registers a virtual machine belongs to the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="ef176-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef176-148">CommonParameters</span></span>
<span data-ttu-id="ef176-149">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef176-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef176-150">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef176-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef176-151">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ef176-151">INPUTS</span></span>

### <span data-ttu-id="ef176-152">System.String</span><span class="sxs-lookup"><span data-stu-id="ef176-152">System.String</span></span>

### <span data-ttu-id="ef176-153">System.Int32</span><span class="sxs-lookup"><span data-stu-id="ef176-153">System.Int32</span></span>

### <span data-ttu-id="ef176-154">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ef176-154">System.Boolean</span></span>

## <span data-ttu-id="ef176-155">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ef176-155">OUTPUTS</span></span>

### <span data-ttu-id="ef176-156">System.Void</span><span class="sxs-lookup"><span data-stu-id="ef176-156">System.Void</span></span>

## <span data-ttu-id="ef176-157">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ef176-157">NOTES</span></span>

## <span data-ttu-id="ef176-158">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ef176-158">RELATED LINKS</span></span>

[<span data-ttu-id="ef176-159">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="ef176-159">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="ef176-160">Set-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="ef176-160">Set-AzAutomationDscNode</span></span>](./Set-AzAutomationDscNode.md)

[<span data-ttu-id="ef176-161">Unregister-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="ef176-161">Unregister-AzAutomationDscNode</span></span>](./Unregister-AzAutomationDscNode.md)



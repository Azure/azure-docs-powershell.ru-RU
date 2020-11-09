---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 73E6DF02-7171-481B-966F-DECEC122A602
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/register-azautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Register-AzAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Register-AzAutomationDscNode.md
ms.openlocfilehash: e8367d4e291f3cd08cdb1020375cce1741a679c8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94315260"
---
# <span data-ttu-id="593a9-101">Register-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="593a9-101">Register-AzAutomationDscNode</span></span>

## <span data-ttu-id="593a9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="593a9-102">SYNOPSIS</span></span>
<span data-ttu-id="593a9-103">Регистрация виртуальной машины Azure под управлением операционной системы Windows в качестве узла DSC для учетной записи автоматизации.</span><span class="sxs-lookup"><span data-stu-id="593a9-103">Registers an Azure virtual machine running Windows OS as a DSC node for an Automation account.</span></span>

## <span data-ttu-id="593a9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="593a9-104">SYNTAX</span></span>

```
Register-AzAutomationDscNode -AzureVMName <String> [-NodeConfigurationName <String>]
 [-ConfigurationMode <String>] [-ConfigurationModeFrequencyMins <Int32>] [-RefreshFrequencyMins <Int32>]
 [-RebootNodeIfNeeded <Boolean>] [-ActionAfterReboot <String>] [-AllowModuleOverwrite <Boolean>]
 [-AzureVMResourceGroup <String>] [-AzureVMLocation <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="593a9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="593a9-105">DESCRIPTION</span></span>
<span data-ttu-id="593a9-106">Командлет **Register-AzAutomationDscNode** регистрирует виртуальную машину Azure как узел конфигурации нужного состояния ТД в учетной записи службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="593a9-106">The **Register-AzAutomationDscNode** cmdlet registers an Azure virtual machine as an APS Desired State Configuration (DSC) node in an Azure Automation account.</span></span> <span data-ttu-id="593a9-107">Этот командлет будет регистрировать виртуальные машины под управлением операционной системы Windows в качестве узла Automation DSC для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="593a9-107">This cmdlet will only register VMs running Windows OS as an Automation DSC Node for an account.</span></span>

<span data-ttu-id="593a9-108">Если вам нужно зарегистрировать узел в учетной записи автоматизации в другой подписке, вам потребуется использовать шаблон ARM, а не командлеты.</span><span class="sxs-lookup"><span data-stu-id="593a9-108">If you need to register a node to an automation account in a different subscription, you will need to use an ARM template rather than cmdlets.</span></span> <span data-ttu-id="593a9-109">Дополнительные сведения см. в [документации по](https://docs.microsoft.com/en-us/azure/automation/automation-dsc-onboarding#registering-virtual-machines-across-azure-subscriptions) службе автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="593a9-109">See the Azure Automation [documentation](https://docs.microsoft.com/en-us/azure/automation/automation-dsc-onboarding#registering-virtual-machines-across-azure-subscriptions) for more details.</span></span>

## <span data-ttu-id="593a9-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="593a9-110">EXAMPLES</span></span>

### <span data-ttu-id="593a9-111">Пример 1: регистрация виртуальной машины Azure в качестве узла Azure DSC</span><span class="sxs-lookup"><span data-stu-id="593a9-111">Example 1: Register an Azure virtual machine as an Azure DSC node</span></span>
```
PS C:\>Register-AzAutomationDscNode -AutomationAccountName "Contoso17" -AzureVMName "VirtualMachine01" -ResourceGroupName "ResourceGroup01"-NodeConfigurationName "ContosoConfiguration.webserver"
```

<span data-ttu-id="593a9-112">Эта команда регистрирует виртуальную машину Azure с именем VirtualMachine01 в качестве узла DSC в учетной записи автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="593a9-112">This command registers the Azure virtual machine named VirtualMachine01 as a DSC node in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="593a9-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="593a9-113">PARAMETERS</span></span>

### <span data-ttu-id="593a9-114">-ActionAfterReboot</span><span class="sxs-lookup"><span data-stu-id="593a9-114">-ActionAfterReboot</span></span>
<span data-ttu-id="593a9-115">Указывает действие, выполняемое виртуальной машиной после перезапуска.</span><span class="sxs-lookup"><span data-stu-id="593a9-115">Specifies the action that the virtual machine takes after it restarts.</span></span>
<span data-ttu-id="593a9-116">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="593a9-116">Valid values are:</span></span> 
- <span data-ttu-id="593a9-117">ContinueConfiguration</span><span class="sxs-lookup"><span data-stu-id="593a9-117">ContinueConfiguration</span></span> 
- <span data-ttu-id="593a9-118">StopConfiguration</span><span class="sxs-lookup"><span data-stu-id="593a9-118">StopConfiguration</span></span>

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

### <span data-ttu-id="593a9-119">-AllowModuleOverwrite</span><span class="sxs-lookup"><span data-stu-id="593a9-119">-AllowModuleOverwrite</span></span>
<span data-ttu-id="593a9-120">Указывает, будут ли новые конфигурации, загружаемые этим узлом DSC, с опрашивающего сервера Azure Automation DSC заменять существующие модули, уже имеющиеся на целевом узле.</span><span class="sxs-lookup"><span data-stu-id="593a9-120">Specifies whether new configurations that this DSC node downloads from the Azure Automation DSC pull server replace the existing modules already on the target node.</span></span>

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

### <span data-ttu-id="593a9-121">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="593a9-121">-AutomationAccountName</span></span>
<span data-ttu-id="593a9-122">Указывает имя учетной записи автоматизации, в которой этот командлет регистрирует виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="593a9-122">Specifies the name of an Automation account in which this cmdlet registers a virtual machine.</span></span>

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

### <span data-ttu-id="593a9-123">-AzureVMLocation</span><span class="sxs-lookup"><span data-stu-id="593a9-123">-AzureVMLocation</span></span>
<span data-ttu-id="593a9-124">Расположение виртуальной машины Azure.</span><span class="sxs-lookup"><span data-stu-id="593a9-124">The Azure VM location.</span></span>

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

### <span data-ttu-id="593a9-125">-AzureVMName</span><span class="sxs-lookup"><span data-stu-id="593a9-125">-AzureVMName</span></span>
<span data-ttu-id="593a9-126">Имя виртуальной машины Azure, которую нужно зарегистрировать для управления с помощью Azure Automation DSC.</span><span class="sxs-lookup"><span data-stu-id="593a9-126">The name of the Azure virtual machine to register for management with Azure Automation DSC.</span></span>

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

### <span data-ttu-id="593a9-127">-AzureVMResourceGroup</span><span class="sxs-lookup"><span data-stu-id="593a9-127">-AzureVMResourceGroup</span></span>
<span data-ttu-id="593a9-128">Имя группы ресурсов Azure VM.</span><span class="sxs-lookup"><span data-stu-id="593a9-128">The Azure VM resource group name.</span></span>

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

### <span data-ttu-id="593a9-129">-ConfigurationMode</span><span class="sxs-lookup"><span data-stu-id="593a9-129">-ConfigurationMode</span></span>
<span data-ttu-id="593a9-130">Задает режим конфигурации DSC.</span><span class="sxs-lookup"><span data-stu-id="593a9-130">Specifies the DSC configuration mode.</span></span>
<span data-ttu-id="593a9-131">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="593a9-131">Valid values are:</span></span> 
- <span data-ttu-id="593a9-132">ApplyAndMonitor</span><span class="sxs-lookup"><span data-stu-id="593a9-132">ApplyAndMonitor</span></span> 
- <span data-ttu-id="593a9-133">ApplyAndAutocorrect</span><span class="sxs-lookup"><span data-stu-id="593a9-133">ApplyAndAutocorrect</span></span> 
- <span data-ttu-id="593a9-134">ApplyOnly</span><span class="sxs-lookup"><span data-stu-id="593a9-134">ApplyOnly</span></span>

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

### <span data-ttu-id="593a9-135">-ConfigurationModeFrequencyMins</span><span class="sxs-lookup"><span data-stu-id="593a9-135">-ConfigurationModeFrequencyMins</span></span>
<span data-ttu-id="593a9-136">Указывает частоту (в минутах), с которой фоновое приложение DSC пытается реализовать текущую конфигурацию на целевом узле.</span><span class="sxs-lookup"><span data-stu-id="593a9-136">Specifies the frequency, in minutes, at which the background application of DSC attempts to implement the current configuration on the target node.</span></span>

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

### <span data-ttu-id="593a9-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="593a9-137">-DefaultProfile</span></span>
<span data-ttu-id="593a9-138">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="593a9-138">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="593a9-139">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="593a9-139">-NodeConfigurationName</span></span>
<span data-ttu-id="593a9-140">Указывает имя конфигурации узла, которую этот командлет настраивает для виртуальной машины, чтобы извлечь ее из Azure Automation DSC.</span><span class="sxs-lookup"><span data-stu-id="593a9-140">Specifies the name of the node configuration that this cmdlet configures the virtual machine to pull from Azure Automation DSC.</span></span>

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

### <span data-ttu-id="593a9-141">-RebootNodeIfNeeded</span><span class="sxs-lookup"><span data-stu-id="593a9-141">-RebootNodeIfNeeded</span></span>
<span data-ttu-id="593a9-142">Указывает, следует ли перезапускать виртуальную машину при необходимости.</span><span class="sxs-lookup"><span data-stu-id="593a9-142">Specifies whether to restart the virtual machine, if needed.</span></span>

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

### <span data-ttu-id="593a9-143">-RefreshFrequencyMins</span><span class="sxs-lookup"><span data-stu-id="593a9-143">-RefreshFrequencyMins</span></span>
<span data-ttu-id="593a9-144">Указывает частоту (в минутах), с которой локальный диспетчер конфигураций связывается с сервером Azure Automation DSC, чтобы скачать последнюю конфигурацию узла.</span><span class="sxs-lookup"><span data-stu-id="593a9-144">Specifies the frequency, in minutes, at which the local Configuration Manager contacts the Azure Automation DSC pull server to download the latest node configuration.</span></span>

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

### <span data-ttu-id="593a9-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="593a9-145">-ResourceGroupName</span></span>
<span data-ttu-id="593a9-146">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="593a9-146">Specifies the name of a resource group.</span></span>
<span data-ttu-id="593a9-147">Учетная запись автоматизации, с помощью которой этот командлет регистрирует виртуальную машину, принадлежит к группе ресурсов, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="593a9-147">The Automation account with which this cmdlet registers a virtual machine belongs to the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="593a9-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="593a9-148">CommonParameters</span></span>
<span data-ttu-id="593a9-149">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="593a9-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="593a9-150">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="593a9-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="593a9-151">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="593a9-151">INPUTS</span></span>

### <span data-ttu-id="593a9-152">System. String</span><span class="sxs-lookup"><span data-stu-id="593a9-152">System.String</span></span>

### <span data-ttu-id="593a9-153">System. Int32</span><span class="sxs-lookup"><span data-stu-id="593a9-153">System.Int32</span></span>

### <span data-ttu-id="593a9-154">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="593a9-154">System.Boolean</span></span>

## <span data-ttu-id="593a9-155">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="593a9-155">OUTPUTS</span></span>

### <span data-ttu-id="593a9-156">System. void</span><span class="sxs-lookup"><span data-stu-id="593a9-156">System.Void</span></span>

## <span data-ttu-id="593a9-157">Пуск</span><span class="sxs-lookup"><span data-stu-id="593a9-157">NOTES</span></span>

## <span data-ttu-id="593a9-158">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="593a9-158">RELATED LINKS</span></span>

[<span data-ttu-id="593a9-159">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="593a9-159">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="593a9-160">Set-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="593a9-160">Set-AzAutomationDscNode</span></span>](./Set-AzAutomationDscNode.md)

[<span data-ttu-id="593a9-161">Отмена регистрации — AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="593a9-161">Unregister-AzAutomationDscNode</span></span>](./Unregister-AzAutomationDscNode.md)


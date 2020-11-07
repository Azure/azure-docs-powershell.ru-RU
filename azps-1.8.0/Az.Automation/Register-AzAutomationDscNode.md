---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 73E6DF02-7171-481B-966F-DECEC122A602
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/register-azautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Register-AzAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Register-AzAutomationDscNode.md
ms.openlocfilehash: 5dc2682597be6f05a65bafc38424139e9707578f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93731548"
---
# <span data-ttu-id="ecf70-101">Register-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="ecf70-101">Register-AzAutomationDscNode</span></span>

## <span data-ttu-id="ecf70-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ecf70-102">SYNOPSIS</span></span>
<span data-ttu-id="ecf70-103">Регистрирует виртуальную машину Azure как узел DSC для учетной записи автоматизации.</span><span class="sxs-lookup"><span data-stu-id="ecf70-103">Registers an Azure virtual machine as a DSC node for an Automation account.</span></span>

## <span data-ttu-id="ecf70-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ecf70-104">SYNTAX</span></span>

```
Register-AzAutomationDscNode -AzureVMName <String> [-NodeConfigurationName <String>]
 [-ConfigurationMode <String>] [-ConfigurationModeFrequencyMins <Int32>] [-RefreshFrequencyMins <Int32>]
 [-RebootNodeIfNeeded <Boolean>] [-ActionAfterReboot <String>] [-AllowModuleOverwrite <Boolean>]
 [-AzureVMResourceGroup <String>] [-AzureVMLocation <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ecf70-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ecf70-105">DESCRIPTION</span></span>
<span data-ttu-id="ecf70-106">Командлет **Register-AzAutomationDscNode** регистрирует виртуальную машину Azure как узел конфигурации нужного состояния ТД в учетной записи службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="ecf70-106">The **Register-AzAutomationDscNode** cmdlet registers an Azure virtual machine as an APS Desired State Configuration (DSC) node in an Azure Automation account.</span></span>

## <span data-ttu-id="ecf70-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ecf70-107">EXAMPLES</span></span>

### <span data-ttu-id="ecf70-108">Пример 1: регистрация виртуальной машины Azure в качестве узла Azure DSC</span><span class="sxs-lookup"><span data-stu-id="ecf70-108">Example 1: Register an Azure virtual machine as an Azure DSC node</span></span>
```
PS C:\>Register-AzAutomationDscNode -AutomationAccountName "Contoso17" -AzVMName "VirtualMachine01" -ResourceGroupName "ResourceGroup01"-NodeConfigurationName "ContosoConfiguration.webserver"
```

<span data-ttu-id="ecf70-109">Эта команда регистрирует виртуальную машину Azure с именем VirtualMachine01 в качестве узла DSC в учетной записи автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="ecf70-109">This command registers the Azure virtual machine named VirtualMachine01 as a DSC node in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="ecf70-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ecf70-110">PARAMETERS</span></span>

### <span data-ttu-id="ecf70-111">-ActionAfterReboot</span><span class="sxs-lookup"><span data-stu-id="ecf70-111">-ActionAfterReboot</span></span>
<span data-ttu-id="ecf70-112">Указывает действие, выполняемое виртуальной машиной после перезапуска.</span><span class="sxs-lookup"><span data-stu-id="ecf70-112">Specifies the action that the virtual machine takes after it restarts.</span></span>
<span data-ttu-id="ecf70-113">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="ecf70-113">Valid values are:</span></span> 
- <span data-ttu-id="ecf70-114">ContinueConfiguration</span><span class="sxs-lookup"><span data-stu-id="ecf70-114">ContinueConfiguration</span></span> 
- <span data-ttu-id="ecf70-115">StopConfiguration</span><span class="sxs-lookup"><span data-stu-id="ecf70-115">StopConfiguration</span></span>

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

### <span data-ttu-id="ecf70-116">-AllowModuleOverwrite</span><span class="sxs-lookup"><span data-stu-id="ecf70-116">-AllowModuleOverwrite</span></span>
<span data-ttu-id="ecf70-117">Указывает, будут ли новые конфигурации, загружаемые этим узлом DSC, с опрашивающего сервера Azure Automation DSC заменять существующие модули, уже имеющиеся на целевом узле.</span><span class="sxs-lookup"><span data-stu-id="ecf70-117">Specifies whether new configurations that this DSC node downloads from the Azure Automation DSC pull server replace the existing modules already on the target node.</span></span>

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

### <span data-ttu-id="ecf70-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ecf70-118">-AutomationAccountName</span></span>
<span data-ttu-id="ecf70-119">Указывает имя учетной записи автоматизации, в которой этот командлет регистрирует виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="ecf70-119">Specifies the name of an Automation account in which this cmdlet registers a virtual machine.</span></span>

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

### <span data-ttu-id="ecf70-120">-AzureVMLocation</span><span class="sxs-lookup"><span data-stu-id="ecf70-120">-AzureVMLocation</span></span>
<span data-ttu-id="ecf70-121">Расположение виртуальной машины Azure.</span><span class="sxs-lookup"><span data-stu-id="ecf70-121">The Azure VM location.</span></span>

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

### <span data-ttu-id="ecf70-122">-AzureVMName</span><span class="sxs-lookup"><span data-stu-id="ecf70-122">-AzureVMName</span></span>
<span data-ttu-id="ecf70-123">Имя виртуальной машины Azure, которую нужно зарегистрировать для управления с помощью Azure Automation DSC.</span><span class="sxs-lookup"><span data-stu-id="ecf70-123">The name of the Azure virtual machine to register for management with Azure Automation DSC.</span></span>

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

### <span data-ttu-id="ecf70-124">-AzureVMResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ecf70-124">-AzureVMResourceGroup</span></span>
<span data-ttu-id="ecf70-125">Имя группы ресурсов Azure VM.</span><span class="sxs-lookup"><span data-stu-id="ecf70-125">The Azure VM resource group name.</span></span>

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

### <span data-ttu-id="ecf70-126">-ConfigurationMode</span><span class="sxs-lookup"><span data-stu-id="ecf70-126">-ConfigurationMode</span></span>
<span data-ttu-id="ecf70-127">Задает режим конфигурации DSC.</span><span class="sxs-lookup"><span data-stu-id="ecf70-127">Specifies the DSC configuration mode.</span></span>
<span data-ttu-id="ecf70-128">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="ecf70-128">Valid values are:</span></span> 
- <span data-ttu-id="ecf70-129">ApplyAndMonitor</span><span class="sxs-lookup"><span data-stu-id="ecf70-129">ApplyAndMonitor</span></span> 
- <span data-ttu-id="ecf70-130">ApplyAndAutocorrect</span><span class="sxs-lookup"><span data-stu-id="ecf70-130">ApplyAndAutocorrect</span></span> 
- <span data-ttu-id="ecf70-131">ApplyOnly</span><span class="sxs-lookup"><span data-stu-id="ecf70-131">ApplyOnly</span></span>

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

### <span data-ttu-id="ecf70-132">-ConfigurationModeFrequencyMins</span><span class="sxs-lookup"><span data-stu-id="ecf70-132">-ConfigurationModeFrequencyMins</span></span>
<span data-ttu-id="ecf70-133">Указывает частоту (в минутах), с которой фоновое приложение DSC пытается реализовать текущую конфигурацию на целевом узле.</span><span class="sxs-lookup"><span data-stu-id="ecf70-133">Specifies the frequency, in minutes, at which the background application of DSC attempts to implement the current configuration on the target node.</span></span>

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

### <span data-ttu-id="ecf70-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecf70-134">-DefaultProfile</span></span>
<span data-ttu-id="ecf70-135">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="ecf70-135">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ecf70-136">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="ecf70-136">-NodeConfigurationName</span></span>
<span data-ttu-id="ecf70-137">Указывает имя конфигурации узла, которую этот командлет настраивает для виртуальной машины, чтобы извлечь ее из Azure Automation DSC.</span><span class="sxs-lookup"><span data-stu-id="ecf70-137">Specifies the name of the node configuration that this cmdlet configures the virtual machine to pull from Azure Automation DSC.</span></span>

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

### <span data-ttu-id="ecf70-138">-RebootNodeIfNeeded</span><span class="sxs-lookup"><span data-stu-id="ecf70-138">-RebootNodeIfNeeded</span></span>
<span data-ttu-id="ecf70-139">Указывает, следует ли перезапускать виртуальную машину при необходимости.</span><span class="sxs-lookup"><span data-stu-id="ecf70-139">Specifies whether to restart the virtual machine, if needed.</span></span>

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

### <span data-ttu-id="ecf70-140">-RefreshFrequencyMins</span><span class="sxs-lookup"><span data-stu-id="ecf70-140">-RefreshFrequencyMins</span></span>
<span data-ttu-id="ecf70-141">Указывает частоту (в минутах), с которой локальный диспетчер конфигураций связывается с сервером Azure Automation DSC, чтобы скачать последнюю конфигурацию узла.</span><span class="sxs-lookup"><span data-stu-id="ecf70-141">Specifies the frequency, in minutes, at which the local Configuration Manager contacts the Azure Automation DSC pull server to download the latest node configuration.</span></span>

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

### <span data-ttu-id="ecf70-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ecf70-142">-ResourceGroupName</span></span>
<span data-ttu-id="ecf70-143">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ecf70-143">Specifies the name of a resource group.</span></span>
<span data-ttu-id="ecf70-144">Учетная запись автоматизации, с помощью которой этот командлет регистрирует виртуальную машину, принадлежит к группе ресурсов, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="ecf70-144">The Automation account with which this cmdlet registers a virtual machine belongs to the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="ecf70-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecf70-145">CommonParameters</span></span>
<span data-ttu-id="ecf70-146">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ecf70-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecf70-147">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ecf70-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecf70-148">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ecf70-148">INPUTS</span></span>

### <span data-ttu-id="ecf70-149">System. String</span><span class="sxs-lookup"><span data-stu-id="ecf70-149">System.String</span></span>

### <span data-ttu-id="ecf70-150">System. Int32</span><span class="sxs-lookup"><span data-stu-id="ecf70-150">System.Int32</span></span>

### <span data-ttu-id="ecf70-151">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ecf70-151">System.Boolean</span></span>

## <span data-ttu-id="ecf70-152">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ecf70-152">OUTPUTS</span></span>

### <span data-ttu-id="ecf70-153">System. void</span><span class="sxs-lookup"><span data-stu-id="ecf70-153">System.Void</span></span>

## <span data-ttu-id="ecf70-154">Пуск</span><span class="sxs-lookup"><span data-stu-id="ecf70-154">NOTES</span></span>

## <span data-ttu-id="ecf70-155">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ecf70-155">RELATED LINKS</span></span>

[<span data-ttu-id="ecf70-156">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="ecf70-156">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="ecf70-157">Set-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="ecf70-157">Set-AzAutomationDscNode</span></span>](./Set-AzAutomationDscNode.md)

[<span data-ttu-id="ecf70-158">Отмена регистрации — AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="ecf70-158">Unregister-AzAutomationDscNode</span></span>](./Unregister-AzAutomationDscNode.md)



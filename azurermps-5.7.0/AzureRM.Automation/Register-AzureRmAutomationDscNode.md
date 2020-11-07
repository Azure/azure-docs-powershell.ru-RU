---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 73E6DF02-7171-481B-966F-DECEC122A602
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/register-azurermautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Register-AzureRmAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Register-AzureRmAutomationDscNode.md
ms.openlocfilehash: 614e954f4e8ec37d24495e766a139eb8a961c743
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734730"
---
# <span data-ttu-id="71403-101">Register-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="71403-101">Register-AzureRmAutomationDscNode</span></span>

## <span data-ttu-id="71403-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="71403-102">SYNOPSIS</span></span>
<span data-ttu-id="71403-103">Регистрирует виртуальную машину Azure как узел DSC для учетной записи автоматизации.</span><span class="sxs-lookup"><span data-stu-id="71403-103">Registers an Azure virtual machine as a DSC node for an Automation account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="71403-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="71403-104">SYNTAX</span></span>

```
Register-AzureRmAutomationDscNode -AzureVMName <String> [-NodeConfigurationName <String>]
 [-ConfigurationMode <String>] [-ConfigurationModeFrequencyMins <Int32>] [-RefreshFrequencyMins <Int32>]
 [-RebootNodeIfNeeded <Boolean>] [-ActionAfterReboot <String>] [-AllowModuleOverwrite <Boolean>]
 [-AzureVMResourceGroup <String>] [-AzureVMLocation <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="71403-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="71403-105">DESCRIPTION</span></span>
<span data-ttu-id="71403-106">Командлет **Register-AzureRmAutomationDscNode** регистрирует виртуальную машину Azure как узел конфигурации нужного состояния ТД в учетной записи службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="71403-106">The **Register-AzureRmAutomationDscNode** cmdlet registers an Azure virtual machine as an APS Desired State Configuration (DSC) node in an Azure Automation account.</span></span>

## <span data-ttu-id="71403-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="71403-107">EXAMPLES</span></span>

### <span data-ttu-id="71403-108">Пример 1: регистрация виртуальной машины Azure в качестве узла Azure DSC</span><span class="sxs-lookup"><span data-stu-id="71403-108">Example 1: Register an Azure virtual machine as an Azure DSC node</span></span>
```
PS C:\>Register-AzureRmAutomationDscNode -AutomationAccountName "Contoso17" -AzureVMName "VirtualMachine01" -ResourceGroupName "ResourceGroup01"-NodeConfigurationName "ContosoConfiguration.webserver"
```

<span data-ttu-id="71403-109">Эта команда регистрирует виртуальную машину Azure с именем VirtualMachine01 в качестве узла DSC в учетной записи автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="71403-109">This command registers the Azure virtual machine named VirtualMachine01 as a DSC node in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="71403-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="71403-110">PARAMETERS</span></span>

### <span data-ttu-id="71403-111">-ActionAfterReboot</span><span class="sxs-lookup"><span data-stu-id="71403-111">-ActionAfterReboot</span></span>
<span data-ttu-id="71403-112">Указывает действие, выполняемое виртуальной машиной после перезапуска.</span><span class="sxs-lookup"><span data-stu-id="71403-112">Specifies the action that the virtual machine takes after it restarts.</span></span>
<span data-ttu-id="71403-113">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="71403-113">Valid values are:</span></span> 

- <span data-ttu-id="71403-114">ContinueConfiguration</span><span class="sxs-lookup"><span data-stu-id="71403-114">ContinueConfiguration</span></span> 
- <span data-ttu-id="71403-115">StopConfiguration</span><span class="sxs-lookup"><span data-stu-id="71403-115">StopConfiguration</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: ContinueConfiguration, StopConfiguration

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71403-116">-AllowModuleOverwrite</span><span class="sxs-lookup"><span data-stu-id="71403-116">-AllowModuleOverwrite</span></span>
<span data-ttu-id="71403-117">Указывает, будут ли новые конфигурации, загружаемые этим узлом DSC, с опрашивающего сервера Azure Automation DSC заменять существующие модули, уже имеющиеся на целевом узле.</span><span class="sxs-lookup"><span data-stu-id="71403-117">Specifies whether new configurations that this DSC node downloads from the Azure Automation DSC pull server replace the existing modules already on the target node.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71403-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="71403-118">-AutomationAccountName</span></span>
<span data-ttu-id="71403-119">Указывает имя учетной записи автоматизации, в которой этот командлет регистрирует виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="71403-119">Specifies the name of an Automation account in which this cmdlet registers a virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71403-120">-AzureVMLocation</span><span class="sxs-lookup"><span data-stu-id="71403-120">-AzureVMLocation</span></span>
<span data-ttu-id="71403-121">Указывает расположение, в котором этот командлет регистрирует виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="71403-121">Specifies the location in which this cmdlet registers a virtual machine.</span></span>
<span data-ttu-id="71403-122">Для получения допустимых местоположений используйте командлет Get-AzureRMLocation.</span><span class="sxs-lookup"><span data-stu-id="71403-122">To obtain valid locations, use the Get-AzureRMLocation cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71403-123">-AzureVMName</span><span class="sxs-lookup"><span data-stu-id="71403-123">-AzureVMName</span></span>
<span data-ttu-id="71403-124">Указывает имя виртуальной машины Azure, которая регистрируется этим командлетом для управления.</span><span class="sxs-lookup"><span data-stu-id="71403-124">Specifies the name of the Azure virtual machine that this cmdlet registers for management.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71403-125">-AzureVMResourceGroup</span><span class="sxs-lookup"><span data-stu-id="71403-125">-AzureVMResourceGroup</span></span>
<span data-ttu-id="71403-126">Указывает имя группы ресурсов виртуальной машины Azure, которая регистрируется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="71403-126">Specifies the name of the resource group of the Azure virtual machine that this cmdlet registers.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71403-127">-ConfigurationMode</span><span class="sxs-lookup"><span data-stu-id="71403-127">-ConfigurationMode</span></span>
<span data-ttu-id="71403-128">Задает режим конфигурации DSC.</span><span class="sxs-lookup"><span data-stu-id="71403-128">Specifies the DSC configuration mode.</span></span>
<span data-ttu-id="71403-129">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="71403-129">Valid values are:</span></span> 

- <span data-ttu-id="71403-130">ApplyAndMonitor</span><span class="sxs-lookup"><span data-stu-id="71403-130">ApplyAndMonitor</span></span> 
- <span data-ttu-id="71403-131">ApplyAndAutocorrect</span><span class="sxs-lookup"><span data-stu-id="71403-131">ApplyAndAutocorrect</span></span> 
- <span data-ttu-id="71403-132">ApplyOnly</span><span class="sxs-lookup"><span data-stu-id="71403-132">ApplyOnly</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: ApplyAndMonitor, ApplyAndAutocorrect, ApplyOnly

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71403-133">-ConfigurationModeFrequencyMins</span><span class="sxs-lookup"><span data-stu-id="71403-133">-ConfigurationModeFrequencyMins</span></span>
<span data-ttu-id="71403-134">Указывает частоту (в минутах), с которой фоновое приложение DSC пытается реализовать текущую конфигурацию на целевом узле.</span><span class="sxs-lookup"><span data-stu-id="71403-134">Specifies the frequency, in minutes, at which the background application of DSC attempts to implement the current configuration on the target node.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71403-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71403-135">-DefaultProfile</span></span>
<span data-ttu-id="71403-136">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="71403-136">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71403-137">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="71403-137">-NodeConfigurationName</span></span>
<span data-ttu-id="71403-138">Указывает имя конфигурации узла, которую этот командлет настраивает для виртуальной машины, чтобы извлечь ее из Azure Automation DSC.</span><span class="sxs-lookup"><span data-stu-id="71403-138">Specifies the name of the node configuration that this cmdlet configures the virtual machine to pull from Azure Automation DSC.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71403-139">-RebootNodeIfNeeded</span><span class="sxs-lookup"><span data-stu-id="71403-139">-RebootNodeIfNeeded</span></span>
<span data-ttu-id="71403-140">Указывает, следует ли перезапускать виртуальную машину при необходимости.</span><span class="sxs-lookup"><span data-stu-id="71403-140">Specifies whether to restart the virtual machine, if needed.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71403-141">-RefreshFrequencyMins</span><span class="sxs-lookup"><span data-stu-id="71403-141">-RefreshFrequencyMins</span></span>
<span data-ttu-id="71403-142">Указывает частоту (в минутах), с которой локальный диспетчер конфигураций связывается с сервером Azure Automation DSC, чтобы скачать последнюю конфигурацию узла.</span><span class="sxs-lookup"><span data-stu-id="71403-142">Specifies the frequency, in minutes, at which the local Configuration Manager contacts the Azure Automation DSC pull server to download the latest node configuration.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71403-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71403-143">-ResourceGroupName</span></span>
<span data-ttu-id="71403-144">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="71403-144">Specifies the name of a resource group.</span></span>
<span data-ttu-id="71403-145">Учетная запись автоматизации, с помощью которой этот командлет регистрирует виртуальную машину, принадлежит к группе ресурсов, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="71403-145">The Automation account with which this cmdlet registers a virtual machine belongs to the resource group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71403-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71403-146">CommonParameters</span></span>
<span data-ttu-id="71403-147">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="71403-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71403-148">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71403-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71403-149">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="71403-149">INPUTS</span></span>

### <span data-ttu-id="71403-150">Ничего</span><span class="sxs-lookup"><span data-stu-id="71403-150">None</span></span>
<span data-ttu-id="71403-151">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="71403-151">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="71403-152">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="71403-152">OUTPUTS</span></span>

## <span data-ttu-id="71403-153">Пуск</span><span class="sxs-lookup"><span data-stu-id="71403-153">NOTES</span></span>

## <span data-ttu-id="71403-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="71403-154">RELATED LINKS</span></span>

[<span data-ttu-id="71403-155">Get-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="71403-155">Get-AzureRmAutomationDscNode</span></span>](./Get-AzureRmAutomationDscNode.md)

[<span data-ttu-id="71403-156">Set-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="71403-156">Set-AzureRmAutomationDscNode</span></span>](./Set-AzureRmAutomationDscNode.md)

[<span data-ttu-id="71403-157">Отмена регистрации — AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="71403-157">Unregister-AzureRmAutomationDscNode</span></span>](./Unregister-AzureRmAutomationDscNode.md)



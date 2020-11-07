---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 6250EC11-79CF-428B-A72F-9BD72C1751F0
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVM.md
ms.openlocfilehash: 5fd3e89a20dba274c1bdcad69bed150e9d20fc22
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721928"
---
# <span data-ttu-id="02ba9-101">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="02ba9-101">Get-AzVM</span></span>

## <span data-ttu-id="02ba9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="02ba9-102">SYNOPSIS</span></span>
<span data-ttu-id="02ba9-103">Получает свойства виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="02ba9-103">Gets the properties of a virtual machine.</span></span>

## <span data-ttu-id="02ba9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="02ba9-104">SYNTAX</span></span>

### <span data-ttu-id="02ba9-105">DefaultParamSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="02ba9-105">DefaultParamSet (Default)</span></span>
```
Get-AzVM [[-ResourceGroupName] <String>] [[-Name] <String>] [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="02ba9-106">GetVirtualMachineInResourceGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="02ba9-106">GetVirtualMachineInResourceGroupParamSet</span></span>
```
Get-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Status] [-DisplayHint <DisplayHintType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="02ba9-107">ListLocationVirtualMachinesParamSet</span><span class="sxs-lookup"><span data-stu-id="02ba9-107">ListLocationVirtualMachinesParamSet</span></span>
```
Get-AzVM -Location <String> [-Status] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="02ba9-108">ListNextLinkVirtualMachinesParamSet</span><span class="sxs-lookup"><span data-stu-id="02ba9-108">ListNextLinkVirtualMachinesParamSet</span></span>
```
Get-AzVM [-Status] [-NextLink] <Uri> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="02ba9-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="02ba9-109">DESCRIPTION</span></span>
<span data-ttu-id="02ba9-110">Командлет **Get-AzVM** получает представление модели и экземпляр для виртуальной машины Azure.</span><span class="sxs-lookup"><span data-stu-id="02ba9-110">The **Get-AzVM** cmdlet gets the model view and instance view of an Azure virtual machine.</span></span>
<span data-ttu-id="02ba9-111">Представление модели — это указанные пользователем свойства виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="02ba9-111">The model view is the user specified properties of the virtual machine.</span></span>
<span data-ttu-id="02ba9-112">Представление экземпляра — это состояние уровня экземпляра виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="02ba9-112">The instance view is the instance level status of the virtual machine.</span></span>
<span data-ttu-id="02ba9-113">Укажите параметр *Status* , чтобы получить только представление экземпляра виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="02ba9-113">Specify the *Status* parameter to get only the instance view of a virtual machine.</span></span>

## <span data-ttu-id="02ba9-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="02ba9-114">EXAMPLES</span></span>

### <span data-ttu-id="02ba9-115">Пример 1: получение свойств модели и представления экземпляров</span><span class="sxs-lookup"><span data-stu-id="02ba9-115">Example 1: Get model and instance view properties</span></span>
```
PS C:\> Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"

ResourceGroupName        : ResourceGroup11
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup11/providers/M
icrosoft.Compute/virtualMachines/VirtualMachine07
VmId                     : 00000000-0000-0000-0000-000000000000
Name                     : VirtualMachine07
Type                     : Microsoft.Compute/virtualMachines
Location                 : eastus
Tags                     : {"creationSource":"acs-VirtualMachine07"}
AvailabilitySetReference : {Id}
DiagnosticsProfile       : {BootDiagnostics}
Extensions               : {linuxdiagnostic, waitforleader}
HardwareProfile          : {VmSize}
NetworkProfile           : {NetworkInterfaces}
OSProfile                : {ComputerName, AdminUsername, LinuxConfiguration, Secrets}
ProvisioningState        : Succeeded
StorageProfile           : {ImageReference, OsDisk, DataDisks}
```

<span data-ttu-id="02ba9-116">Эта команда получает свойства представления модели и экземпляра виртуальной машины с именем VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="02ba9-116">This command gets the model view and instance view properties of the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="02ba9-117">Пример 2: получение свойств представления экземпляра</span><span class="sxs-lookup"><span data-stu-id="02ba9-117">Example 2: Get instance view properties</span></span>
```
PS C:\> Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Status

ResourceGroupName       : ResourceGroup11
Name                    : VirtualMachine07
Disks[0]                :
  Name                  : VirtualMachine07-osdisk
  Statuses[0]           :
    Code                : ProvisioningState/succeeded
    Level               : Info
    DisplayStatus       : Provisioning succeeded
    Time                : 3/1/2019 12:59:30 AM
Extensions[0]           :
  Name                  : linuxdiagnostic
  Type                  : Microsoft.OSTCExtensions.LinuxDiagnostic
  TypeHandlerVersion    : 2.3.9029
  Statuses[0]           :
    Code                : ProvisioningState/succeeded
    Level               : Info
    DisplayStatus       : Provisioning succeeded
    Message             : Invalid config settings given: Empty storageAccountName. Install will proceed, but enable
can't proceed, in which case it's still considered a success as it's an external error.
Extensions[1]           :
  Name                  : waitforleader
  Type                  : Microsoft.OSTCExtensions.CustomScriptForLinux
  TypeHandlerVersion    : 1.5.4
  Statuses[0]           :
    Code                : ProvisioningState/succeeded
    Level               : Info
    DisplayStatus       : Provisioning succeeded
    Message             : Command is finished.
---stdout---
waiting for leader.mesos
waiting for leader.mesos
waiting for leader.mesos
waiting for leader.mesos
waiting for leader.mesos
waiting for leader.mesos
PING leader.mesos (xxx.xx.x.x) 56(84) bytes of data.
64 bytes from xxx.xx.x.x: icmp_seq=1 ttl=64 time=0.022 ms

--- leader.mesos ping statistics ---
1 packets transmitted, 1 received, 0% packet loss, time 0ms
rtt min/avg/max/mdev = 0.022/0.022/0.022/0.000 ms
leader.mesos up

---errout---
ping: unknown host leader.mesos
ping: unknown host leader.mesos
ping: unknown host leader.mesos
ping: unknown host leader.mesos
ping: unknown host leader.mesos
ping: unknown host leader.mesos


PlatformFaultDomain     : 0
PlatformUpdateDomain    : 0
VMAgent                 :
  VmAgentVersion        : 2.2.37
  ExtensionHandlers[0]  :
    Type                : Microsoft.OSTCExtensions.LinuxDiagnostic
    TypeHandlerVersion  : 2.3.9029
    Status              :
      Code              : ProvisioningState/succeeded
      Level             : Info
      DisplayStatus     : Ready
      Message           : Plugin enabled
  ExtensionHandlers[1]  :
    Type                : Microsoft.OSTCExtensions.CustomScriptForLinux
    TypeHandlerVersion  : 1.5.4
    Status              :
      Code              : ProvisioningState/succeeded
      Level             : Info
      DisplayStatus     : Ready
      Message           : Plugin enabled
  Statuses[0]           :
    Code                : ProvisioningState/succeeded
    Level               : Info
    DisplayStatus       : Ready
    Message             : Guest Agent is running
    Time                : 3/1/2019 2:04:12 AM
Statuses[0]             :
  Code                  : ProvisioningState/succeeded
  Level                 : Info
  DisplayStatus         : Provisioning succeeded
  Time                  : 3/1/2019 1:01:57 AM
Statuses[1]             :
  Code                  : PowerState/running
  Level                 : Info
  DisplayStatus         : VM running
```

<span data-ttu-id="02ba9-118">Эта команда получает свойства виртуальной машины с именем VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="02ba9-118">This command gets properties of the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="02ba9-119">Эта команда задает параметр *Status* .</span><span class="sxs-lookup"><span data-stu-id="02ba9-119">This command specifies the *Status* parameter.</span></span>
<span data-ttu-id="02ba9-120">Таким образом, команда возвращает только свойства представления экземпляра.</span><span class="sxs-lookup"><span data-stu-id="02ba9-120">Therefore, the command gets only the instance view properties.</span></span>

### <span data-ttu-id="02ba9-121">Пример 3: получение свойств для всех виртуальных машин в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="02ba9-121">Example 3: Get properties for all virtual machines in a resource group</span></span>
```
PS C:\> Get-AzVM -ResourceGroupName "ResourceGroup11"

ResourceGroupName    Name       Location          VmSize  OsType            NIC
-----------------    ----       --------          ------  ------            ---
ResourceGroup11     test1         eastus Standard_DS1_v2 Windows          test1
ResourceGroup11     test2         westus Standard_DS1_v2 Windows          test2
ResourceGroup11     test3         eastus Standard_DS1_v2 Windows          test3
```

<span data-ttu-id="02ba9-122">Эта команда получает свойства всех виртуальных машин в группе ресурсов с именем ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="02ba9-122">This command gets properties for all the virtual machines in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="02ba9-123">Пример 4: получение всех виртуальных машин в подписке</span><span class="sxs-lookup"><span data-stu-id="02ba9-123">Example 4: Get all virtual machines in your subscription</span></span>
```
PS C:\> Get-AzVM

ResourceGroupName    Name       Location          VmSize  OsType            NIC
-----------------    ----       --------          ------  ------            ---
TEST1               test1         eastus Standard_DS1_v2 Windows          test1
TEST1               test2         westus Standard_DS1_v2 Windows          test2
TEST1               test3         eastus Standard_DS1_v2 Windows          test3
TEST2               test4         westus Standard_DS1_v2 Windows          test4
TEST2               test5         eastus Standard_DS1_v2 Windows          test5
```

<span data-ttu-id="02ba9-124">Эта команда возвращает все виртуальные машины в вашей подписке.</span><span class="sxs-lookup"><span data-stu-id="02ba9-124">This command gets all the virtual machines in your subscription.</span></span>

### <span data-ttu-id="02ba9-125">Пример 5: получение всех виртуальных машин в расположении.</span><span class="sxs-lookup"><span data-stu-id="02ba9-125">Example 5: Get all virtual machines in the location.</span></span>
```
PS C:\> Get-AzVM -Location "westus"

ResourceGroupName    Name       Location          VmSize  OsType            NIC
-----------------    ----       --------          ------  ------            ---
TEST1               test2         westus Standard_DS1_v2 Windows          test2
TEST2               test4         westus Standard_DS1_v2 Windows          test4
```

<span data-ttu-id="02ba9-126">Эта команда возвращает все виртуальные машины в регионе "Западная часть США".</span><span class="sxs-lookup"><span data-stu-id="02ba9-126">This command gets all the virtual machines in West US region.</span></span>

### <span data-ttu-id="02ba9-127">Пример 6: получение всех виртуальных машин с помощью фильтрации</span><span class="sxs-lookup"><span data-stu-id="02ba9-127">Example 6: Get all virtual machines using filtering</span></span>
```
PS C:\> Get-AzVM -Name test*

ResourceGroupName    Name       Location          VmSize  OsType            NIC
-----------------    ----       --------          ------  ------            ---
TEST1               test1         eastus Standard_DS1_v2 Windows          test1
TEST1               test2         westus Standard_DS1_v2 Windows          test2
TEST1               test3         eastus Standard_DS1_v2 Windows          test3
TEST2               test4         westus Standard_DS1_v2 Windows          test4
TEST2               test5         eastus Standard_DS1_v2 Windows          test5
```

<span data-ttu-id="02ba9-128">Эта команда возвращает все виртуальные машины в подписке, которые начинаются с "Test".</span><span class="sxs-lookup"><span data-stu-id="02ba9-128">This command gets all the virtual machines in your subscription that start with "test".</span></span>

## <span data-ttu-id="02ba9-129">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="02ba9-129">PARAMETERS</span></span>

### <span data-ttu-id="02ba9-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02ba9-130">-DefaultProfile</span></span>
<span data-ttu-id="02ba9-131">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="02ba9-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="02ba9-132">-DisplayHint</span><span class="sxs-lookup"><span data-stu-id="02ba9-132">-DisplayHint</span></span>
<span data-ttu-id="02ba9-133">Определяет способ отображения объекта виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="02ba9-133">Determines how the virtual machine object is displayed.</span></span>
<span data-ttu-id="02ba9-134">Допустимые значения:--Compact: отображает только свойства верхнего уровня--Expand: отображает все свойства на всех уровнях.</span><span class="sxs-lookup"><span data-stu-id="02ba9-134">Valid values are: -- Compact: displays only top level properties -- Expand: displays all properties in all levels</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.DisplayHintType
Parameter Sets: GetVirtualMachineInResourceGroupParamSet
Aliases:
Accepted values: Compact, Expand

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02ba9-135">-Location</span><span class="sxs-lookup"><span data-stu-id="02ba9-135">-Location</span></span>
<span data-ttu-id="02ba9-136">Задает расположение для списка виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="02ba9-136">Specifies a location for the virtual machines to list.</span></span>

```yaml
Type: System.String
Parameter Sets: ListLocationVirtualMachinesParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02ba9-137">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="02ba9-137">-Name</span></span>
<span data-ttu-id="02ba9-138">Указывает имя виртуальной машины, которую требуется получить.</span><span class="sxs-lookup"><span data-stu-id="02ba9-138">Specifies the name of the virtual machine to get.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParamSet
Aliases: ResourceName, VMName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: GetVirtualMachineInResourceGroupParamSet
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="02ba9-139">-NextLink</span><span class="sxs-lookup"><span data-stu-id="02ba9-139">-NextLink</span></span>
<span data-ttu-id="02ba9-140">Указывает следующую ссылку.</span><span class="sxs-lookup"><span data-stu-id="02ba9-140">Specifies the next link.</span></span>

```yaml
Type: System.Uri
Parameter Sets: ListNextLinkVirtualMachinesParamSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02ba9-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02ba9-141">-ResourceGroupName</span></span>
<span data-ttu-id="02ba9-142">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="02ba9-142">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParamSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: GetVirtualMachineInResourceGroupParamSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="02ba9-143">-Status (состояние)</span><span class="sxs-lookup"><span data-stu-id="02ba9-143">-Status</span></span>
<span data-ttu-id="02ba9-144">Указывает на то, что этот командлет получает только представление экземпляра виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="02ba9-144">Indicates that this cmdlet gets only the instance view of the virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02ba9-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02ba9-145">CommonParameters</span></span>
<span data-ttu-id="02ba9-146">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="02ba9-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02ba9-147">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="02ba9-147">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02ba9-148">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="02ba9-148">INPUTS</span></span>

### <span data-ttu-id="02ba9-149">System. String</span><span class="sxs-lookup"><span data-stu-id="02ba9-149">System.String</span></span>

### <span data-ttu-id="02ba9-150">System. URI</span><span class="sxs-lookup"><span data-stu-id="02ba9-150">System.Uri</span></span>

### <span data-ttu-id="02ba9-151">Microsoft. Azure. Commands. COMPUTE. Models. DisplayHintType</span><span class="sxs-lookup"><span data-stu-id="02ba9-151">Microsoft.Azure.Commands.Compute.Models.DisplayHintType</span></span>

## <span data-ttu-id="02ba9-152">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="02ba9-152">OUTPUTS</span></span>

### <span data-ttu-id="02ba9-153">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="02ba9-153">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="02ba9-154">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineInstanceView</span><span class="sxs-lookup"><span data-stu-id="02ba9-154">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView</span></span>

## <span data-ttu-id="02ba9-155">Пуск</span><span class="sxs-lookup"><span data-stu-id="02ba9-155">NOTES</span></span>

## <span data-ttu-id="02ba9-156">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="02ba9-156">RELATED LINKS</span></span>

[<span data-ttu-id="02ba9-157">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="02ba9-157">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="02ba9-158">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="02ba9-158">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="02ba9-159">Restarting-AzVM</span><span class="sxs-lookup"><span data-stu-id="02ba9-159">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="02ba9-160">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="02ba9-160">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="02ba9-161">Остановить-AzVM</span><span class="sxs-lookup"><span data-stu-id="02ba9-161">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="02ba9-162">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="02ba9-162">Update-AzVM</span></span>](./Update-AzVM.md)



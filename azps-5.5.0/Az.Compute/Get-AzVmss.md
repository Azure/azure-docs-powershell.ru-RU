---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: FC6BC096-DBC4-48DA-A366-B87EB18A0496
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmss.md
ms.openlocfilehash: 7985a979f9bbb89d6594416575e3fa00640784b5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100215756"
---
# <span data-ttu-id="6452c-101">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="6452c-101">Get-AzVmss</span></span>

## <span data-ttu-id="6452c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6452c-102">SYNOPSIS</span></span>
<span data-ttu-id="6452c-103">Свойства VMSS.</span><span class="sxs-lookup"><span data-stu-id="6452c-103">Gets the properties of a VMSS.</span></span>

## <span data-ttu-id="6452c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6452c-104">SYNTAX</span></span>

### <span data-ttu-id="6452c-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6452c-105">DefaultParameter (Default)</span></span>
```
Get-AzVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6452c-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="6452c-106">FriendMethod</span></span>
```
Get-AzVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [-InstanceView]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6452c-107">OSUpgradeHistoryMethodParameter</span><span class="sxs-lookup"><span data-stu-id="6452c-107">OSUpgradeHistoryMethodParameter</span></span>
```
Get-AzVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [-OSUpgradeHistory]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6452c-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6452c-108">DESCRIPTION</span></span>
<span data-ttu-id="6452c-109">Для **этого можно получить** представление модели и экземпляра набора масштаба виртуальной машины (VMSS).</span><span class="sxs-lookup"><span data-stu-id="6452c-109">The **Get-AzVmss** cmdlet gets the model and instance view of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="6452c-110">Представление модели — это свойства набора масштаба виртуальной машины, заданные пользователем.</span><span class="sxs-lookup"><span data-stu-id="6452c-110">The model view is the user specified properties of the virtual machine scale set.</span></span>
<span data-ttu-id="6452c-111">Представление экземпляра — это состояние уровня экземпляра набора масштаба виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="6452c-111">The instance view is the instance level status of the virtual machine scale set.</span></span>
<span data-ttu-id="6452c-112">Укажите параметр *InstanceView,* чтобы получить только представление экземпляра набора масштаба виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="6452c-112">Specify the *InstanceView* parameter to get only the instance view of a virtual machine scale set.</span></span>

## <span data-ttu-id="6452c-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6452c-113">EXAMPLES</span></span>

### <span data-ttu-id="6452c-114">Пример 1. Просмотр свойств VMSS</span><span class="sxs-lookup"><span data-stu-id="6452c-114">Example 1: Get the properties of a VMSS</span></span>
```
PS C:\> Get-AzVmss -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"

ResourceGroupName                           : Group001
Sku                                         :
  Name                                      : Standard_DS1_v2
  Tier                                      : Standard
  Capacity                                  : 2
UpgradePolicy                               :
  Mode                                      : Manual
VirtualMachineProfile                       :
  OsProfile                                 :
    ComputerNamePrefix                      : test
    AdminUsername                           : contoso
    WindowsConfiguration                    :
      ProvisionVMAgent                      : True
      EnableAutomaticUpdates                : True
  StorageProfile                            :
    ImageReference                          :
      Publisher                             : MicrosoftWindowsServer
      Offer                                 : WindowsServer
      Sku                                   : 2016-Datacenter
      Version                               : latest
    OsDisk                                  :
      Caching                               : None
      CreateOption                          : FromImage
      ManagedDisk                           :
        StorageAccountType                  : Premium_LRS
  NetworkProfile                            :
    NetworkInterfaceConfigurations[0]       :
      Name                                  : Group001
      Primary                               : True
      EnableAcceleratedNetworking           : False
      NetworkSecurityGroup                  :
        Id                                  : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/Group001
/providers/Microsoft.Network/networkSecurityGroups/Group001
      DnsSettings                           :
      IpConfigurations[0]                   :
        Name                                : Group001
        Subnet                              :
          Id                                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/group001
/providers/Microsoft.Network/virtualNetworks/Group001/subnets/Group001
        PrivateIPAddressVersion             : IPv4
        LoadBalancerBackendAddressPools[0]  :
          Id                                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/group001
/providers/Microsoft.Network/loadBalancers/Group001/backendAddressPools/Group001
        LoadBalancerInboundNatPools[0]      :
          Id                                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/group001
/providers/Microsoft.Network/loadBalancers/Group001/inboundNatPools/Group001
        LoadBalancerInboundNatPools[1]      :
          Id                                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/group001
/providers/Microsoft.Network/loadBalancers/Group001/inboundNatPools/Group001
      EnableIPForwarding                    : False
ProvisioningState                           : Succeeded
Overprovision                               : True
UniqueId                                    : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SinglePlacementGroup                        : False
Id                                          : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/Group001/
providers/Microsoft.Compute/virtualMachineScaleSets/VMSS001
Name                                        : VMSS001
Type                                        : Microsoft.Compute/virtualMachineScaleSets
Location                                    : eastus
Tags                                        : {}
```

<span data-ttu-id="6452c-115">Эта команда получает свойства VMSS под названием VMSS001, которые принадлежат группе ресурсов Group001.</span><span class="sxs-lookup"><span data-stu-id="6452c-115">This command gets the properties of the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="6452c-116">Так как команда не указывает параметр переключения *InstanceView,* командлет получает представление модели набора масштаба виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="6452c-116">Since the command does not specify the *InstanceView* switch parameter, the cmdlet gets the model view of the virtual machine scale set.</span></span>

### <span data-ttu-id="6452c-117">Пример 2. Получить все вимы в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="6452c-117">Example 2: Get all Vmss in a resource group</span></span>
```
PS C:\> Get-AzVmss -ResourceGroupName "Group001"

ResourceGroupName                               Name       Location             Sku Capacity ProvisioningState
-----------------                               ----       --------             --- -------- -----------------
Group001                                       VMSS001      eastus Standard_DS1_v2        2         Succeeded
Group001                                       VMSS002      eastus     Standard_A1        2         Succeeded
```

<span data-ttu-id="6452c-118">Получить все ВМЫ в группе ресурсов "Группа001"</span><span class="sxs-lookup"><span data-stu-id="6452c-118">Get all Vmss in resource group "Group001"</span></span>

### <span data-ttu-id="6452c-119">Пример 3. Все ВММ в подписке</span><span class="sxs-lookup"><span data-stu-id="6452c-119">Example 3: Get all Vmss in a subscription</span></span>
```
PS C:\> Get-AzVmss

ResourceGroupName                               Name       Location             Sku Capacity ProvisioningState
-----------------                               ----       --------             --- -------- -----------------
Group001                                       VMSS001      eastus Standard_DS1_v2        2         Succeeded
Group001                                       VMSS002      eastus     Standard_A1        2         Succeeded
Group002                                       VMSS003      eastus     Standard_A1        1         Succeeded
Group002                                       VMSS004      eastus Standard_DS1_v2        2         Succeeded
```

<span data-ttu-id="6452c-120">Получите все ВМЫ в подписке.</span><span class="sxs-lookup"><span data-stu-id="6452c-120">Get all Vmss in subscription.</span></span>

### <span data-ttu-id="6452c-121">Пример 4. Получите все вимы с помощью фильтрации</span><span class="sxs-lookup"><span data-stu-id="6452c-121">Example 4: Get all Vmss using filtering</span></span>
```
PS C:\> Get-AzVmss -Name VMSS00*

ResourceGroupName                               Name       Location             Sku Capacity ProvisioningState
-----------------                               ----       --------             --- -------- -----------------
Group001                                       VMSS001      eastus Standard_DS1_v2        2         Succeeded
Group001                                       VMSS002      eastus     Standard_A1        2         Succeeded
Group002                                       VMSS003      eastus     Standard_A1        1         Succeeded
Group002                                       VMSS004      eastus Standard_DS1_v2        2         Succeeded
```

<span data-ttu-id="6452c-122">Получите все Вмы в подписке, которые начинаются с "VMSS00".</span><span class="sxs-lookup"><span data-stu-id="6452c-122">Get all Vmss in subscription that start with "VMSS00".</span></span>

## <span data-ttu-id="6452c-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6452c-123">PARAMETERS</span></span>

### <span data-ttu-id="6452c-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6452c-124">-DefaultProfile</span></span>
<span data-ttu-id="6452c-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6452c-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6452c-126">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="6452c-126">-InstanceView</span></span>
<span data-ttu-id="6452c-127">Указывает на то, что этот cmdlet получает только представление экземпляра набора масштаба виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="6452c-127">Indicates that this cmdlet gets only the instance view of the virtual machine scale set.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FriendMethod
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6452c-128">-OSUpgradeHistory</span><span class="sxs-lookup"><span data-stu-id="6452c-128">-OSUpgradeHistory</span></span>
<span data-ttu-id="6452c-129">Указывает на то, что этот cmdlet содержит список истории обновления ос в наборе масштаба виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="6452c-129">Indicates that this cmdlet lists the os upgrade history of the virtual machine scale set.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: OSUpgradeHistoryMethodParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6452c-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6452c-130">-ResourceGroupName</span></span>
<span data-ttu-id="6452c-131">Имя группы ресурсов VMSS.</span><span class="sxs-lookup"><span data-stu-id="6452c-131">Specifies the name of the Resource Group of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="6452c-132">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="6452c-132">-VMScaleSetName</span></span>
<span data-ttu-id="6452c-133">Вид имени VMSS.</span><span class="sxs-lookup"><span data-stu-id="6452c-133">Species the name of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="6452c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6452c-134">CommonParameters</span></span>
<span data-ttu-id="6452c-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6452c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6452c-136">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6452c-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6452c-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6452c-137">INPUTS</span></span>

### <span data-ttu-id="6452c-138">System.String</span><span class="sxs-lookup"><span data-stu-id="6452c-138">System.String</span></span>

## <span data-ttu-id="6452c-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6452c-139">OUTPUTS</span></span>

### <span data-ttu-id="6452c-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMa modelseScaleSet</span><span class="sxs-lookup"><span data-stu-id="6452c-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="6452c-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6452c-141">NOTES</span></span>

## <span data-ttu-id="6452c-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6452c-142">RELATED LINKS</span></span>

[<span data-ttu-id="6452c-143">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="6452c-143">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="6452c-144">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="6452c-144">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="6452c-145">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="6452c-145">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="6452c-146">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="6452c-146">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="6452c-147">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="6452c-147">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="6452c-148">Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="6452c-148">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="6452c-149">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="6452c-149">Update-AzVmss</span></span>](./Update-AzVmss.md)



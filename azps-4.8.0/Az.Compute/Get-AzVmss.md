---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: FC6BC096-DBC4-48DA-A366-B87EB18A0496
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmss.md
ms.openlocfilehash: 7985a979f9bbb89d6594416575e3fa00640784b5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078128"
---
# <span data-ttu-id="ffa8b-101">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="ffa8b-101">Get-AzVmss</span></span>

## <span data-ttu-id="ffa8b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ffa8b-102">SYNOPSIS</span></span>
<span data-ttu-id="ffa8b-103">Возвращает свойства VMSS.</span><span class="sxs-lookup"><span data-stu-id="ffa8b-103">Gets the properties of a VMSS.</span></span>

## <span data-ttu-id="ffa8b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ffa8b-104">SYNTAX</span></span>

### <span data-ttu-id="ffa8b-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ffa8b-105">DefaultParameter (Default)</span></span>
```
Get-AzVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ffa8b-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="ffa8b-106">FriendMethod</span></span>
```
Get-AzVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [-InstanceView]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ffa8b-107">OSUpgradeHistoryMethodParameter</span><span class="sxs-lookup"><span data-stu-id="ffa8b-107">OSUpgradeHistoryMethodParameter</span></span>
```
Get-AzVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [-OSUpgradeHistory]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ffa8b-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ffa8b-108">DESCRIPTION</span></span>
<span data-ttu-id="ffa8b-109">Командлет **Get-AzVmss** Возвращает модель и представление экземпляра набора масштабирования виртуальных машин (VMSS).</span><span class="sxs-lookup"><span data-stu-id="ffa8b-109">The **Get-AzVmss** cmdlet gets the model and instance view of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="ffa8b-110">Представление "модель" — свойства, заданные пользователем в наборе масштабов виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="ffa8b-110">The model view is the user specified properties of the virtual machine scale set.</span></span>
<span data-ttu-id="ffa8b-111">Представление экземпляра — это состояние уровня экземпляра для набора масштабов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="ffa8b-111">The instance view is the instance level status of the virtual machine scale set.</span></span>
<span data-ttu-id="ffa8b-112">Укажите параметр *InstanceView* , чтобы получить только представление экземпляра для набора шкал виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="ffa8b-112">Specify the *InstanceView* parameter to get only the instance view of a virtual machine scale set.</span></span>

## <span data-ttu-id="ffa8b-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ffa8b-113">EXAMPLES</span></span>

### <span data-ttu-id="ffa8b-114">Пример 1: получение свойств VMSS</span><span class="sxs-lookup"><span data-stu-id="ffa8b-114">Example 1: Get the properties of a VMSS</span></span>
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

<span data-ttu-id="ffa8b-115">Эта команда получает свойства VMSS с именем VMSS001, которые относятся к группе ресурсов с именем Group001.</span><span class="sxs-lookup"><span data-stu-id="ffa8b-115">This command gets the properties of the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="ffa8b-116">Так как в команде не указан параметр переключателя *InstanceView* , командлет возвращает представление модели для набора масштабов виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="ffa8b-116">Since the command does not specify the *InstanceView* switch parameter, the cmdlet gets the model view of the virtual machine scale set.</span></span>

### <span data-ttu-id="ffa8b-117">Пример 2: получение всех Vmss в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="ffa8b-117">Example 2: Get all Vmss in a resource group</span></span>
```
PS C:\> Get-AzVmss -ResourceGroupName "Group001"

ResourceGroupName                               Name       Location             Sku Capacity ProvisioningState
-----------------                               ----       --------             --- -------- -----------------
Group001                                       VMSS001      eastus Standard_DS1_v2        2         Succeeded
Group001                                       VMSS002      eastus     Standard_A1        2         Succeeded
```

<span data-ttu-id="ffa8b-118">Получить все Vmss в группе ресурсов "Group001"</span><span class="sxs-lookup"><span data-stu-id="ffa8b-118">Get all Vmss in resource group "Group001"</span></span>

### <span data-ttu-id="ffa8b-119">Пример 3: получение всех Vmss в подписке</span><span class="sxs-lookup"><span data-stu-id="ffa8b-119">Example 3: Get all Vmss in a subscription</span></span>
```
PS C:\> Get-AzVmss

ResourceGroupName                               Name       Location             Sku Capacity ProvisioningState
-----------------                               ----       --------             --- -------- -----------------
Group001                                       VMSS001      eastus Standard_DS1_v2        2         Succeeded
Group001                                       VMSS002      eastus     Standard_A1        2         Succeeded
Group002                                       VMSS003      eastus     Standard_A1        1         Succeeded
Group002                                       VMSS004      eastus Standard_DS1_v2        2         Succeeded
```

<span data-ttu-id="ffa8b-120">Получить все Vmss в подписке.</span><span class="sxs-lookup"><span data-stu-id="ffa8b-120">Get all Vmss in subscription.</span></span>

### <span data-ttu-id="ffa8b-121">Пример 4: получение всех Vmss с помощью фильтрации</span><span class="sxs-lookup"><span data-stu-id="ffa8b-121">Example 4: Get all Vmss using filtering</span></span>
```
PS C:\> Get-AzVmss -Name VMSS00*

ResourceGroupName                               Name       Location             Sku Capacity ProvisioningState
-----------------                               ----       --------             --- -------- -----------------
Group001                                       VMSS001      eastus Standard_DS1_v2        2         Succeeded
Group001                                       VMSS002      eastus     Standard_A1        2         Succeeded
Group002                                       VMSS003      eastus     Standard_A1        1         Succeeded
Group002                                       VMSS004      eastus Standard_DS1_v2        2         Succeeded
```

<span data-ttu-id="ffa8b-122">Получить все Vmss в подписке, которые начинаются с "VMSS00".</span><span class="sxs-lookup"><span data-stu-id="ffa8b-122">Get all Vmss in subscription that start with "VMSS00".</span></span>

## <span data-ttu-id="ffa8b-123">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ffa8b-123">PARAMETERS</span></span>

### <span data-ttu-id="ffa8b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffa8b-124">-DefaultProfile</span></span>
<span data-ttu-id="ffa8b-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ffa8b-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ffa8b-126">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="ffa8b-126">-InstanceView</span></span>
<span data-ttu-id="ffa8b-127">Указывает на то, что этот командлет получает только представление экземпляра для набора масштабов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="ffa8b-127">Indicates that this cmdlet gets only the instance view of the virtual machine scale set.</span></span>

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

### <span data-ttu-id="ffa8b-128">-OSUpgradeHistory</span><span class="sxs-lookup"><span data-stu-id="ffa8b-128">-OSUpgradeHistory</span></span>
<span data-ttu-id="ffa8b-129">Указывает на то, что этот командлет перечисляет историю обновления операционной системы для набора масштабов виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="ffa8b-129">Indicates that this cmdlet lists the os upgrade history of the virtual machine scale set.</span></span>

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

### <span data-ttu-id="ffa8b-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ffa8b-130">-ResourceGroupName</span></span>
<span data-ttu-id="ffa8b-131">Указывает имя группы ресурсов для VMSS.</span><span class="sxs-lookup"><span data-stu-id="ffa8b-131">Specifies the name of the Resource Group of the VMSS.</span></span>

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

### <span data-ttu-id="ffa8b-132">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="ffa8b-132">-VMScaleSetName</span></span>
<span data-ttu-id="ffa8b-133">Форель имя VMSS.</span><span class="sxs-lookup"><span data-stu-id="ffa8b-133">Species the name of the VMSS.</span></span>

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

### <span data-ttu-id="ffa8b-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffa8b-134">CommonParameters</span></span>
<span data-ttu-id="ffa8b-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ffa8b-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffa8b-136">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ffa8b-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffa8b-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ffa8b-137">INPUTS</span></span>

### <span data-ttu-id="ffa8b-138">System. String</span><span class="sxs-lookup"><span data-stu-id="ffa8b-138">System.String</span></span>

## <span data-ttu-id="ffa8b-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ffa8b-139">OUTPUTS</span></span>

### <span data-ttu-id="ffa8b-140">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="ffa8b-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="ffa8b-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="ffa8b-141">NOTES</span></span>

## <span data-ttu-id="ffa8b-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ffa8b-142">RELATED LINKS</span></span>

[<span data-ttu-id="ffa8b-143">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="ffa8b-143">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="ffa8b-144">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="ffa8b-144">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="ffa8b-145">Restarting-AzVmss</span><span class="sxs-lookup"><span data-stu-id="ffa8b-145">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="ffa8b-146">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="ffa8b-146">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="ffa8b-147">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="ffa8b-147">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="ffa8b-148">Остановить-AzVmss</span><span class="sxs-lookup"><span data-stu-id="ffa8b-148">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="ffa8b-149">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="ffa8b-149">Update-AzVmss</span></span>](./Update-AzVmss.md)



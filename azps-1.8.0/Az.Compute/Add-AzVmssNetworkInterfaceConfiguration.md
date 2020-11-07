---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: BAC2FA68-1D82-411D-A853-FD4EE525B533
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssnetworkinterfaceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssNetworkInterfaceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssNetworkInterfaceConfiguration.md
ms.openlocfilehash: 629f7d0b04c0b5b511e26a25657deb611497f497
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93901385"
---
# <span data-ttu-id="b60b7-101">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="b60b7-101">Add-AzVmssNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="b60b7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b60b7-102">SYNOPSIS</span></span>
<span data-ttu-id="b60b7-103">Добавляет конфигурацию сетевого интерфейса в VMSS.</span><span class="sxs-lookup"><span data-stu-id="b60b7-103">Adds a network interface configuration to the VMSS.</span></span>

## <span data-ttu-id="b60b7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b60b7-104">SYNTAX</span></span>

```
Add-AzVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [[-Primary] <Boolean>] [[-Id] <String>] [[-IpConfiguration] <VirtualMachineScaleSetIPConfiguration[]>]
 [-EnableAcceleratedNetworking] [-EnableIPForwarding] [-NetworkSecurityGroupId <String>]
 [-DnsSettingsDnsServer <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b60b7-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b60b7-105">DESCRIPTION</span></span>
<span data-ttu-id="b60b7-106">Командлет **Add-AzVmssNetworkInterfaceConfiguration** добавляет конфигурацию сетевого интерфейса в набор масштабов виртуальных машин (VMSS).</span><span class="sxs-lookup"><span data-stu-id="b60b7-106">The **Add-AzVmssNetworkInterfaceConfiguration** cmdlet adds a network interface configuration to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="b60b7-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b60b7-107">EXAMPLES</span></span>

### <span data-ttu-id="b60b7-108">Пример 1: Добавление конфигурации сетевого интерфейса в VMSS</span><span class="sxs-lookup"><span data-stu-id="b60b7-108">Example 1: Add a network interface configuration to the VMSS</span></span>
```
PS C:\> Add-AzVmssNetworkInterfaceConfiguration -VirtualMachineScaleSet $VMSS -Name "Test" -Primary $True -IPConfiguration $IPCfg
```

<span data-ttu-id="b60b7-109">Эта команда добавляет конфигурацию сетевого интерфейса в VMSS.</span><span class="sxs-lookup"><span data-stu-id="b60b7-109">This command adds a network interface configuration to the VMSS.</span></span>

## <span data-ttu-id="b60b7-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b60b7-110">PARAMETERS</span></span>

### <span data-ttu-id="b60b7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b60b7-111">-DefaultProfile</span></span>
<span data-ttu-id="b60b7-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b60b7-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b60b7-113">-DnsSettingsDnsServer</span><span class="sxs-lookup"><span data-stu-id="b60b7-113">-DnsSettingsDnsServer</span></span>
<span data-ttu-id="b60b7-114">Список IP-адресов DNS-серверов для параметров DNS.</span><span class="sxs-lookup"><span data-stu-id="b60b7-114">List of dns server IP addresses for dns settings.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: DnsServer

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b60b7-115">-EnableAcceleratedNetworking</span><span class="sxs-lookup"><span data-stu-id="b60b7-115">-EnableAcceleratedNetworking</span></span>
<span data-ttu-id="b60b7-116">Указывает, разрешено ли сетевому интерфейсу использование сети.</span><span class="sxs-lookup"><span data-stu-id="b60b7-116">Specifies whether the network interface is accelerated networking-enabled.</span></span>

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

### <span data-ttu-id="b60b7-117">-EnableIPForwarding</span><span class="sxs-lookup"><span data-stu-id="b60b7-117">-EnableIPForwarding</span></span>
<span data-ttu-id="b60b7-118">Указывает, включена ли переадресация IP для этого сетевого адаптера.</span><span class="sxs-lookup"><span data-stu-id="b60b7-118">Specifies whether IP forwarding enabled on this NIC.</span></span>

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

### <span data-ttu-id="b60b7-119">-ID</span><span class="sxs-lookup"><span data-stu-id="b60b7-119">-Id</span></span>
<span data-ttu-id="b60b7-120">Указывает идентификатор ресурса виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="b60b7-120">Specifies the Resource ID of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b60b7-121">-Конфигурацию</span><span class="sxs-lookup"><span data-stu-id="b60b7-121">-IpConfiguration</span></span>
<span data-ttu-id="b60b7-122">Задает IP-конфигурации сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="b60b7-122">Specifies the IP configurations of the network interface.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIPConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b60b7-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b60b7-123">-Name</span></span>
<span data-ttu-id="b60b7-124">Указывает имя конфигурации сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="b60b7-124">Specifies the name of the network interface configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b60b7-125">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="b60b7-125">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="b60b7-126">Идентификатор группы безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="b60b7-126">Id of the network security group.</span></span>

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

### <span data-ttu-id="b60b7-127">-Primary</span><span class="sxs-lookup"><span data-stu-id="b60b7-127">-Primary</span></span>
<span data-ttu-id="b60b7-128">Показывает, является ли сетевыми интерфейсами, созданными из конфигурации сетевого интерфейса, основной центр сведений о сети (NIC) виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="b60b7-128">Indicates whether network interfaces created from the network interface configuration will be the primary network information center (NIC) of the virtual machine.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b60b7-129">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="b60b7-129">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="b60b7-130">Указывает объект VMSS.</span><span class="sxs-lookup"><span data-stu-id="b60b7-130">Specifies the VMSS object.</span></span>
<span data-ttu-id="b60b7-131">Для создания объекта можно использовать командлет [New-AzVmssConfig](./New-AzVmssConfig.md) .</span><span class="sxs-lookup"><span data-stu-id="b60b7-131">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create the object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b60b7-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b60b7-132">-Confirm</span></span>
<span data-ttu-id="b60b7-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b60b7-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b60b7-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b60b7-134">-WhatIf</span></span>
<span data-ttu-id="b60b7-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b60b7-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b60b7-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b60b7-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b60b7-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b60b7-137">CommonParameters</span></span>
<span data-ttu-id="b60b7-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b60b7-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b60b7-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b60b7-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b60b7-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b60b7-140">INPUTS</span></span>

### <span data-ttu-id="b60b7-141">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="b60b7-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="b60b7-142">System. String</span><span class="sxs-lookup"><span data-stu-id="b60b7-142">System.String</span></span>

### <span data-ttu-id="b60b7-143">System. Nullable "1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="b60b7-143">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="b60b7-144">Microsoft. Azure. Management. COMPUTE. Models. VirtualMachineScaleSetIPConfiguration []</span><span class="sxs-lookup"><span data-stu-id="b60b7-144">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIPConfiguration[]</span></span>

### <span data-ttu-id="b60b7-145">System. String []</span><span class="sxs-lookup"><span data-stu-id="b60b7-145">System.String[]</span></span>

## <span data-ttu-id="b60b7-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b60b7-146">OUTPUTS</span></span>

### <span data-ttu-id="b60b7-147">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="b60b7-147">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="b60b7-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="b60b7-148">NOTES</span></span>

## <span data-ttu-id="b60b7-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b60b7-149">RELATED LINKS</span></span>

[<span data-ttu-id="b60b7-150">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="b60b7-150">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: BAC2FA68-1D82-411D-A853-FD4EE525B533
online version: https://docs.microsoft.com/powershell/module/az.compute/add-azvmssnetworkinterfaceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssNetworkInterfaceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssNetworkInterfaceConfiguration.md
ms.openlocfilehash: c85c4292fcae081e50ba98ff873f967f8e32fbac
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101969555"
---
# <span data-ttu-id="60557-101">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="60557-101">Add-AzVmssNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="60557-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60557-102">SYNOPSIS</span></span>
<span data-ttu-id="60557-103">Добавляет конфигурацию сетевого интерфейса в VMSS.</span><span class="sxs-lookup"><span data-stu-id="60557-103">Adds a network interface configuration to the VMSS.</span></span>

## <span data-ttu-id="60557-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="60557-104">SYNTAX</span></span>

```
Add-AzVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [[-Primary] <Boolean>] [[-Id] <String>] [[-IpConfiguration] <VirtualMachineScaleSetIPConfiguration[]>]
 [-EnableAcceleratedNetworking] [-EnableIPForwarding] [-NetworkSecurityGroupId <String>]
 [-DnsSettingsDnsServer <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="60557-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="60557-105">DESCRIPTION</span></span>
<span data-ttu-id="60557-106">Командлет **Add-AzVmssNetworkInterfaceConfiguration** добавляет конфигурацию сетевого интерфейса в набор масштаба виртуальной машины (VMSS).</span><span class="sxs-lookup"><span data-stu-id="60557-106">The **Add-AzVmssNetworkInterfaceConfiguration** cmdlet adds a network interface configuration to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="60557-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="60557-107">EXAMPLES</span></span>

### <span data-ttu-id="60557-108">Пример 1. Добавление конфигурации сетевого интерфейса в VMSS</span><span class="sxs-lookup"><span data-stu-id="60557-108">Example 1: Add a network interface configuration to the VMSS</span></span>
```
PS C:\> Add-AzVmssNetworkInterfaceConfiguration -VirtualMachineScaleSet $VMSS -Name "Test" -Primary $True -IPConfiguration $IPCfg
```

<span data-ttu-id="60557-109">Эта команда добавляет конфигурацию сетевого интерфейса к VMSS.</span><span class="sxs-lookup"><span data-stu-id="60557-109">This command adds a network interface configuration to the VMSS.</span></span>

## <span data-ttu-id="60557-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="60557-110">PARAMETERS</span></span>

### <span data-ttu-id="60557-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60557-111">-DefaultProfile</span></span>
<span data-ttu-id="60557-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="60557-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="60557-113">-DnsSettingsDnsServer</span><span class="sxs-lookup"><span data-stu-id="60557-113">-DnsSettingsDnsServer</span></span>
<span data-ttu-id="60557-114">Список IP-адресов DNS-сервера для параметров DNS.</span><span class="sxs-lookup"><span data-stu-id="60557-114">List of dns server IP addresses for dns settings.</span></span>

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

### <span data-ttu-id="60557-115">-EnableAcceleratedNetworking</span><span class="sxs-lookup"><span data-stu-id="60557-115">-EnableAcceleratedNetworking</span></span>
<span data-ttu-id="60557-116">Указывает, будет ли ускоренный сетевой интерфейс включен.</span><span class="sxs-lookup"><span data-stu-id="60557-116">Specifies whether the network interface is accelerated networking-enabled.</span></span>

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

### <span data-ttu-id="60557-117">-EnableIPForwarding</span><span class="sxs-lookup"><span data-stu-id="60557-117">-EnableIPForwarding</span></span>
<span data-ttu-id="60557-118">Указывает, включена ли для этой NIC переадваровка IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="60557-118">Specifies whether IP forwarding enabled on this NIC.</span></span>

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

### <span data-ttu-id="60557-119">-Id</span><span class="sxs-lookup"><span data-stu-id="60557-119">-Id</span></span>
<span data-ttu-id="60557-120">Определяет ИД ресурса виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="60557-120">Specifies the Resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="60557-121">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="60557-121">-IpConfiguration</span></span>
<span data-ttu-id="60557-122">Определяет конфигурации IP-адреса интерфейса сети.</span><span class="sxs-lookup"><span data-stu-id="60557-122">Specifies the IP configurations of the network interface.</span></span>

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

### <span data-ttu-id="60557-123">-Name</span><span class="sxs-lookup"><span data-stu-id="60557-123">-Name</span></span>
<span data-ttu-id="60557-124">Указывает имя конфигурации сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="60557-124">Specifies the name of the network interface configuration.</span></span>

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

### <span data-ttu-id="60557-125">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="60557-125">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="60557-126">ИД группы безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="60557-126">Id of the network security group.</span></span>

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

### <span data-ttu-id="60557-127">-Primary</span><span class="sxs-lookup"><span data-stu-id="60557-127">-Primary</span></span>
<span data-ttu-id="60557-128">Указывает, будут ли сетевые интерфейсы, созданные с помощью конфигурации сетевого интерфейса, основным информационным центром сети (NIC) виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="60557-128">Indicates whether network interfaces created from the network interface configuration will be the primary network information center (NIC) of the virtual machine.</span></span>

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

### <span data-ttu-id="60557-129">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="60557-129">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="60557-130">Указывает объект VMSS.</span><span class="sxs-lookup"><span data-stu-id="60557-130">Specifies the VMSS object.</span></span>
<span data-ttu-id="60557-131">Для создания объекта можно использовать [cmdlet New-AzVmssConfig.](./New-AzVmssConfig.md)</span><span class="sxs-lookup"><span data-stu-id="60557-131">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="60557-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="60557-132">-Confirm</span></span>
<span data-ttu-id="60557-133">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="60557-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60557-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60557-134">-WhatIf</span></span>
<span data-ttu-id="60557-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="60557-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="60557-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="60557-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60557-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60557-137">CommonParameters</span></span>
<span data-ttu-id="60557-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60557-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60557-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="60557-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60557-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="60557-140">INPUTS</span></span>

### <span data-ttu-id="60557-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMa modelseScaleSet</span><span class="sxs-lookup"><span data-stu-id="60557-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="60557-142">System.String</span><span class="sxs-lookup"><span data-stu-id="60557-142">System.String</span></span>

### <span data-ttu-id="60557-143">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="60557-143">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="60557-144">Microsoft.Azure.Management.Compute.Models.VirtualMa modelseScaleSetIPConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="60557-144">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIPConfiguration[]</span></span>

### <span data-ttu-id="60557-145">System.String[]</span><span class="sxs-lookup"><span data-stu-id="60557-145">System.String[]</span></span>

## <span data-ttu-id="60557-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="60557-146">OUTPUTS</span></span>

### <span data-ttu-id="60557-147">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMa modelseScaleSet</span><span class="sxs-lookup"><span data-stu-id="60557-147">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="60557-148">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="60557-148">NOTES</span></span>

## <span data-ttu-id="60557-149">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="60557-149">RELATED LINKS</span></span>

[<span data-ttu-id="60557-150">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="60557-150">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)

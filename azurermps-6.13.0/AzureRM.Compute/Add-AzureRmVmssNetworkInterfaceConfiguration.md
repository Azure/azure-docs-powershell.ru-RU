---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: BAC2FA68-1D82-411D-A853-FD4EE525B533
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmssnetworkinterfaceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVmssNetworkInterfaceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVmssNetworkInterfaceConfiguration.md
ms.openlocfilehash: 6789b2a0f3309e8011cc6e87a27dbf9f28579d05
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564691"
---
# <span data-ttu-id="c602f-101">Add-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="c602f-101">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="c602f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c602f-102">SYNOPSIS</span></span>
<span data-ttu-id="c602f-103">Добавляет конфигурацию сетевого интерфейса в VMSS.</span><span class="sxs-lookup"><span data-stu-id="c602f-103">Adds a network interface configuration to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c602f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c602f-104">SYNTAX</span></span>

```
Add-AzureRmVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-Name] <String>] [[-Primary] <Boolean>] [[-Id] <String>]
 [[-IpConfiguration] <VirtualMachineScaleSetIPConfiguration[]>] [-EnableAcceleratedNetworking]
 [-EnableIPForwarding] [-NetworkSecurityGroupId <String>] [-DnsSettingsDnsServer <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c602f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c602f-105">DESCRIPTION</span></span>
<span data-ttu-id="c602f-106">Командлет **Add-AzureRmVmssNetworkInterfaceConfiguration** добавляет конфигурацию сетевого интерфейса в набор масштабов виртуальных машин (VMSS).</span><span class="sxs-lookup"><span data-stu-id="c602f-106">The **Add-AzureRmVmssNetworkInterfaceConfiguration** cmdlet adds a network interface configuration to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="c602f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c602f-107">EXAMPLES</span></span>

### <span data-ttu-id="c602f-108">Пример 1: Добавление конфигурации сетевого интерфейса в VMSS</span><span class="sxs-lookup"><span data-stu-id="c602f-108">Example 1: Add a network interface configuration to the VMSS</span></span>
```
PS C:\> Add-AzureRmVmssNetworkInterfaceConfiguration -VirtualMachineScaleSet $VMSS -Name "Test" -Primary $True -IPConfiguration $IPCfg
```

<span data-ttu-id="c602f-109">Эта команда добавляет конфигурацию сетевого интерфейса в VMSS.</span><span class="sxs-lookup"><span data-stu-id="c602f-109">This command adds a network interface configuration to the VMSS.</span></span>

## <span data-ttu-id="c602f-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c602f-110">PARAMETERS</span></span>

### <span data-ttu-id="c602f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c602f-111">-DefaultProfile</span></span>
<span data-ttu-id="c602f-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c602f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c602f-113">-DnsSettingsDnsServer</span><span class="sxs-lookup"><span data-stu-id="c602f-113">-DnsSettingsDnsServer</span></span>
<span data-ttu-id="c602f-114">Список IP-адресов DNS-серверов для параметров DNS.</span><span class="sxs-lookup"><span data-stu-id="c602f-114">List of dns server IP addresses for dns settings.</span></span>

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

### <span data-ttu-id="c602f-115">-EnableAcceleratedNetworking</span><span class="sxs-lookup"><span data-stu-id="c602f-115">-EnableAcceleratedNetworking</span></span>
<span data-ttu-id="c602f-116">Указывает, разрешено ли сетевому интерфейсу использование сети.</span><span class="sxs-lookup"><span data-stu-id="c602f-116">Specifies whether the network interface is accelerated networking-enabled.</span></span>

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

### <span data-ttu-id="c602f-117">-EnableIPForwarding</span><span class="sxs-lookup"><span data-stu-id="c602f-117">-EnableIPForwarding</span></span>
<span data-ttu-id="c602f-118">Указывает, включена ли переадресация IP для этого сетевого адаптера.</span><span class="sxs-lookup"><span data-stu-id="c602f-118">Specifies whether IP forwarding enabled on this NIC.</span></span>

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

### <span data-ttu-id="c602f-119">-ID</span><span class="sxs-lookup"><span data-stu-id="c602f-119">-Id</span></span>
<span data-ttu-id="c602f-120">Указывает идентификатор ресурса виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c602f-120">Specifies the Resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="c602f-121">-Конфигурацию</span><span class="sxs-lookup"><span data-stu-id="c602f-121">-IpConfiguration</span></span>
<span data-ttu-id="c602f-122">Задает IP-конфигурации сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="c602f-122">Specifies the IP configurations of the network interface.</span></span>

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

### <span data-ttu-id="c602f-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c602f-123">-Name</span></span>
<span data-ttu-id="c602f-124">Указывает имя конфигурации сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="c602f-124">Specifies the name of the network interface configuration.</span></span>

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

### <span data-ttu-id="c602f-125">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="c602f-125">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="c602f-126">Идентификатор группы безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="c602f-126">Id of the network security group.</span></span>

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

### <span data-ttu-id="c602f-127">-Primary</span><span class="sxs-lookup"><span data-stu-id="c602f-127">-Primary</span></span>
<span data-ttu-id="c602f-128">Показывает, является ли сетевыми интерфейсами, созданными из конфигурации сетевого интерфейса, основной центр сведений о сети (NIC) виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c602f-128">Indicates whether network interfaces created from the network interface configuration will be the primary network information center (NIC) of the virtual machine.</span></span>

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

### <span data-ttu-id="c602f-129">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="c602f-129">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="c602f-130">Указывает объект VMSS.</span><span class="sxs-lookup"><span data-stu-id="c602f-130">Specifies the VMSS object.</span></span>
<span data-ttu-id="c602f-131">Для создания объекта можно использовать командлет [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) .</span><span class="sxs-lookup"><span data-stu-id="c602f-131">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="c602f-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c602f-132">-Confirm</span></span>
<span data-ttu-id="c602f-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c602f-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c602f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c602f-134">-WhatIf</span></span>
<span data-ttu-id="c602f-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c602f-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c602f-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c602f-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c602f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c602f-137">CommonParameters</span></span>
<span data-ttu-id="c602f-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c602f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c602f-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c602f-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c602f-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c602f-140">INPUTS</span></span>

### <span data-ttu-id="c602f-141">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="c602f-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="c602f-142">System. String</span><span class="sxs-lookup"><span data-stu-id="c602f-142">System.String</span></span>

### <span data-ttu-id="c602f-143">System. Nullable "1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="c602f-143">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="c602f-144">Microsoft. Azure. Management. COMPUTE. Models. VirtualMachineScaleSetIPConfiguration []</span><span class="sxs-lookup"><span data-stu-id="c602f-144">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIPConfiguration[]</span></span>

### <span data-ttu-id="c602f-145">System. String []</span><span class="sxs-lookup"><span data-stu-id="c602f-145">System.String[]</span></span>

## <span data-ttu-id="c602f-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c602f-146">OUTPUTS</span></span>

### <span data-ttu-id="c602f-147">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="c602f-147">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="c602f-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="c602f-148">NOTES</span></span>

## <span data-ttu-id="c602f-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c602f-149">RELATED LINKS</span></span>

[<span data-ttu-id="c602f-150">New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="c602f-150">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)

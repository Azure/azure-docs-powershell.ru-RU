---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: BAC2FA68-1D82-411D-A853-FD4EE525B533
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssNetworkInterfaceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssNetworkInterfaceConfiguration.md
ms.openlocfilehash: 0b21b5fa3b5b605ee3092a61eaf67a2c63c4346b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732037"
---
# <span data-ttu-id="afd33-101">Add-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="afd33-101">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="afd33-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="afd33-102">SYNOPSIS</span></span>
<span data-ttu-id="afd33-103">Добавляет конфигурацию сетевого интерфейса в VMSS.</span><span class="sxs-lookup"><span data-stu-id="afd33-103">Adds a network interface configuration to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="afd33-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="afd33-104">SYNTAX</span></span>

```
Add-AzureRmVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <VirtualMachineScaleSet>
 [[-Name] <String>] [[-Primary] <Boolean>] [[-Id] <String>]
 [[-IpConfiguration] <VirtualMachineScaleSetIPConfiguration[]>] [-NetworkSecurityGroupId <String>]
 [-DnsSettingsDnsServer <String[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="afd33-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="afd33-105">DESCRIPTION</span></span>
<span data-ttu-id="afd33-106">Командлет **Add-AzureRmVmssNetworkInterfaceConfiguration** добавляет конфигурацию сетевого интерфейса в набор масштабов виртуальных машин (VMSS).</span><span class="sxs-lookup"><span data-stu-id="afd33-106">The **Add-AzureRmVmssNetworkInterfaceConfiguration** cmdlet adds a network interface configuration to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="afd33-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="afd33-107">EXAMPLES</span></span>

### <span data-ttu-id="afd33-108">Пример 1: Добавление конфигурации сетевого интерфейса в VMSS</span><span class="sxs-lookup"><span data-stu-id="afd33-108">Example 1: Add a network interface configuration to the VMSS</span></span>
```
PS C:\> Add-AzureRmVmssNetworkInterfaceConfiguration -VirtualMachineScaleSet $VMSS -Name "Test" -Primary $True -IPConfiguration $IPCfg
```

<span data-ttu-id="afd33-109">Эта команда добавляет конфигурацию сетевого интерфейса в VMSS.</span><span class="sxs-lookup"><span data-stu-id="afd33-109">This command adds a network interface configuration to the VMSS.</span></span>

## <span data-ttu-id="afd33-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="afd33-110">PARAMETERS</span></span>

### <span data-ttu-id="afd33-111">-DnsSettingsDnsServer</span><span class="sxs-lookup"><span data-stu-id="afd33-111">-DnsSettingsDnsServer</span></span>
<span data-ttu-id="afd33-112">Список IP-адресов DNS-серверов для параметров DNS.</span><span class="sxs-lookup"><span data-stu-id="afd33-112">List of dns server IP addresses for dns settings.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="afd33-113">-ID</span><span class="sxs-lookup"><span data-stu-id="afd33-113">-Id</span></span>
<span data-ttu-id="afd33-114">Указывает идентификатор ресурса виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="afd33-114">Specifies the Resource ID of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="afd33-115">-Конфигурацию</span><span class="sxs-lookup"><span data-stu-id="afd33-115">-IpConfiguration</span></span>
<span data-ttu-id="afd33-116">Задает IP-конфигурации сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="afd33-116">Specifies the IP configurations of the network interface.</span></span>

```yaml
Type: VirtualMachineScaleSetIPConfiguration[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="afd33-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="afd33-117">-Name</span></span>
<span data-ttu-id="afd33-118">Указывает имя конфигурации сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="afd33-118">Specifies the name of the network interface configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="afd33-119">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="afd33-119">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="afd33-120">Идентификатор группы безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="afd33-120">Id of the network security group.</span></span>

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

### <span data-ttu-id="afd33-121">-Primary</span><span class="sxs-lookup"><span data-stu-id="afd33-121">-Primary</span></span>
<span data-ttu-id="afd33-122">Показывает, является ли сетевыми интерфейсами, созданными из конфигурации сетевого интерфейса, основной центр сведений о сети (NIC) виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="afd33-122">Indicates whether network interfaces created from the network interface configuration will be the primary network information center (NIC) of the virtual machine.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="afd33-123">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="afd33-123">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="afd33-124">Указывает объект VMSS.</span><span class="sxs-lookup"><span data-stu-id="afd33-124">Specifies the VMSS object.</span></span>
<span data-ttu-id="afd33-125">Для создания объекта можно использовать командлет [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) .</span><span class="sxs-lookup"><span data-stu-id="afd33-125">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create the object.</span></span>

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="afd33-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="afd33-126">-Confirm</span></span>
<span data-ttu-id="afd33-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="afd33-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afd33-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="afd33-128">-WhatIf</span></span>
<span data-ttu-id="afd33-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="afd33-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="afd33-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="afd33-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afd33-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afd33-131">CommonParameters</span></span>
<span data-ttu-id="afd33-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="afd33-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afd33-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="afd33-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afd33-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="afd33-134">INPUTS</span></span>

### <span data-ttu-id="afd33-135">Ничего</span><span class="sxs-lookup"><span data-stu-id="afd33-135">None</span></span>
<span data-ttu-id="afd33-136">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="afd33-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="afd33-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="afd33-137">OUTPUTS</span></span>

###  
<span data-ttu-id="afd33-138">Этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="afd33-138">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="afd33-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="afd33-139">NOTES</span></span>

## <span data-ttu-id="afd33-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="afd33-140">RELATED LINKS</span></span>

[<span data-ttu-id="afd33-141">New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="afd33-141">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)

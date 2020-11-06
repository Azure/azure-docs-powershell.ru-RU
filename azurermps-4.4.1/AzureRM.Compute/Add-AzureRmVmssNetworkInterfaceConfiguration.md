---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: BAC2FA68-1D82-411D-A853-FD4EE525B533
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssNetworkInterfaceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssNetworkInterfaceConfiguration.md
ms.openlocfilehash: 651e339de5782d288350535ba1b0527d7a3eb0de
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566302"
---
# <span data-ttu-id="32f60-101">Add-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="32f60-101">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="32f60-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="32f60-102">SYNOPSIS</span></span>
<span data-ttu-id="32f60-103">Добавляет конфигурацию сетевого интерфейса в VMSS.</span><span class="sxs-lookup"><span data-stu-id="32f60-103">Adds a network interface configuration to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="32f60-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="32f60-104">SYNTAX</span></span>

```
Add-AzureRmVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-Name] <String>] [[-Primary] <Boolean>] [[-Id] <String>]
 [[-IpConfiguration] <VirtualMachineScaleSetIPConfiguration[]>] [-EnableAcceleratedNetworking]
 [-NetworkSecurityGroupId <String>] [-DnsSettingsDnsServer <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32f60-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="32f60-105">DESCRIPTION</span></span>
<span data-ttu-id="32f60-106">Командлет **Add-AzureRmVmssNetworkInterfaceConfiguration** добавляет конфигурацию сетевого интерфейса в набор масштабов виртуальных машин (VMSS).</span><span class="sxs-lookup"><span data-stu-id="32f60-106">The **Add-AzureRmVmssNetworkInterfaceConfiguration** cmdlet adds a network interface configuration to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="32f60-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="32f60-107">EXAMPLES</span></span>

### <span data-ttu-id="32f60-108">Пример 1: Добавление конфигурации сетевого интерфейса в VMSS</span><span class="sxs-lookup"><span data-stu-id="32f60-108">Example 1: Add a network interface configuration to the VMSS</span></span>
```
PS C:\> Add-AzureRmVmssNetworkInterfaceConfiguration -VirtualMachineScaleSet $VMSS -Name "Test" -Primary $True -IPConfiguration $IPCfg
```

<span data-ttu-id="32f60-109">Эта команда добавляет конфигурацию сетевого интерфейса в VMSS.</span><span class="sxs-lookup"><span data-stu-id="32f60-109">This command adds a network interface configuration to the VMSS.</span></span>

## <span data-ttu-id="32f60-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="32f60-110">PARAMETERS</span></span>

### <span data-ttu-id="32f60-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32f60-111">-DefaultProfile</span></span>
<span data-ttu-id="32f60-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="32f60-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="32f60-113">-DnsSettingsDnsServer</span><span class="sxs-lookup"><span data-stu-id="32f60-113">-DnsSettingsDnsServer</span></span>
<span data-ttu-id="32f60-114">Список IP-адресов DNS-серверов для параметров DNS.</span><span class="sxs-lookup"><span data-stu-id="32f60-114">List of dns server IP addresses for dns settings.</span></span>

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

### <span data-ttu-id="32f60-115">-EnableAcceleratedNetworking</span><span class="sxs-lookup"><span data-stu-id="32f60-115">-EnableAcceleratedNetworking</span></span>
<span data-ttu-id="32f60-116">Указывает, разрешено ли сетевому интерфейсу использование сети.</span><span class="sxs-lookup"><span data-stu-id="32f60-116">Specifies whether the network interface is accelerated networking-enabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32f60-117">-ID</span><span class="sxs-lookup"><span data-stu-id="32f60-117">-Id</span></span>
<span data-ttu-id="32f60-118">Указывает идентификатор ресурса виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="32f60-118">Specifies the Resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="32f60-119">-Конфигурацию</span><span class="sxs-lookup"><span data-stu-id="32f60-119">-IpConfiguration</span></span>
<span data-ttu-id="32f60-120">Задает IP-конфигурации сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="32f60-120">Specifies the IP configurations of the network interface.</span></span>

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

### <span data-ttu-id="32f60-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="32f60-121">-Name</span></span>
<span data-ttu-id="32f60-122">Указывает имя конфигурации сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="32f60-122">Specifies the name of the network interface configuration.</span></span>

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

### <span data-ttu-id="32f60-123">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="32f60-123">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="32f60-124">Идентификатор группы безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="32f60-124">Id of the network security group.</span></span>

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

### <span data-ttu-id="32f60-125">-Primary</span><span class="sxs-lookup"><span data-stu-id="32f60-125">-Primary</span></span>
<span data-ttu-id="32f60-126">Показывает, является ли сетевыми интерфейсами, созданными из конфигурации сетевого интерфейса, основной центр сведений о сети (NIC) виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="32f60-126">Indicates whether network interfaces created from the network interface configuration will be the primary network information center (NIC) of the virtual machine.</span></span>

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

### <span data-ttu-id="32f60-127">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="32f60-127">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="32f60-128">Указывает объект VMSS.</span><span class="sxs-lookup"><span data-stu-id="32f60-128">Specifies the VMSS object.</span></span>
<span data-ttu-id="32f60-129">Для создания объекта можно использовать командлет [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) .</span><span class="sxs-lookup"><span data-stu-id="32f60-129">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="32f60-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="32f60-130">-Confirm</span></span>
<span data-ttu-id="32f60-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="32f60-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32f60-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32f60-132">-WhatIf</span></span>
<span data-ttu-id="32f60-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="32f60-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="32f60-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="32f60-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32f60-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32f60-135">CommonParameters</span></span>
<span data-ttu-id="32f60-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="32f60-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32f60-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32f60-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32f60-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="32f60-138">INPUTS</span></span>

## <span data-ttu-id="32f60-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="32f60-139">OUTPUTS</span></span>

###  
<span data-ttu-id="32f60-140">Этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="32f60-140">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="32f60-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="32f60-141">NOTES</span></span>

## <span data-ttu-id="32f60-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="32f60-142">RELATED LINKS</span></span>

[<span data-ttu-id="32f60-143">New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="32f60-143">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)

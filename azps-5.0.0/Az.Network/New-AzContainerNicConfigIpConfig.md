---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-AzContainerNicconfigipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzContainerNicConfigIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzContainerNicConfigIpConfig.md
ms.openlocfilehash: 2e15819fe8b6b21b0f0c0751dc39736408606a7c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248550"
---
# <span data-ttu-id="cfedb-101">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="cfedb-101">New-AzContainerNicConfigIpConfig</span></span>

## <span data-ttu-id="cfedb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cfedb-102">SYNOPSIS</span></span>
<span data-ttu-id="cfedb-103">Создает объект конфигурации конфигурации для контейнера IP-карты.</span><span class="sxs-lookup"><span data-stu-id="cfedb-103">Creates a container nic configuration ip configuration object.</span></span>

## <span data-ttu-id="cfedb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cfedb-104">SYNTAX</span></span>

```
New-AzContainerNicConfigIpConfig -Name <String> -Subnet <PSSubnet> [-SubnetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cfedb-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cfedb-105">DESCRIPTION</span></span>
<span data-ttu-id="cfedb-106">Командлет **New-AzContainerNicConfigIpConfig** создает новую конфигурацию IP-интерфейса сети контейнера.</span><span class="sxs-lookup"><span data-stu-id="cfedb-106">The **New-AzContainerNicConfigIpConfig** cmdlet creates a new container network interface configuration ip configuration.</span></span> 

## <span data-ttu-id="cfedb-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cfedb-107">EXAMPLES</span></span>

### <span data-ttu-id="cfedb-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="cfedb-108">Example 1</span></span>
```powershell
$subnet = New-AzVirtualNetworkSubnetConfig -Name subnet -AddressPrefix 10.0.1.0/24

$vnet = New-AzVirtualNetwork -Name vnet -ResourceGroupName rg1 -Location "West US" -AddressPrefix 10.0.0.0/16 -Subnet $subnet

$containerNicConfigIpConfig = New-AzContainerNicConfigIpConfig -Name ipconfigprofile1 -Subnet $vnet.Subnets[0]

$containerNicConfig = New-AzContainerNicConfig -Name cnic -IpConfiguration containerNicConfigIpConfig

$networkProfile = New-AzNetworkProfile -Name np1 -Location "West US" -ResourceGroupName rg1 -ContainerNetworkInterfaceConfiguration $containerNicConfig
```

<span data-ttu-id="cfedb-109">Первые две команды создают и инициализируют виртуальную сеть и подсеть.</span><span class="sxs-lookup"><span data-stu-id="cfedb-109">The first two commands create and initialize a vnet and a subnet.</span></span> <span data-ttu-id="cfedb-110">Третья команда создает контейнерный профиль IP NIC конфигурации, указывающий на созданную подсеть.</span><span class="sxs-lookup"><span data-stu-id="cfedb-110">The third command creates a container nic ip configuration profile referencing the created subnet.</span></span> <span data-ttu-id="cfedb-111">Четвертая команда создает контейнер конфигурации сетевого интерфейса, на котором указан профиль конфигурации IP, созданный в предыдущей команде.</span><span class="sxs-lookup"><span data-stu-id="cfedb-111">The fourth command creates a container network interface configuration supplying the ip configuration profile created in the previous command.</span></span> <span data-ttu-id="cfedb-112">Наконец, пятая команда создает сетевой профиль, инициализируемый с помощью конфигурации контейнера сетевого интерфейса, хранящейся в $containerNicConfig.</span><span class="sxs-lookup"><span data-stu-id="cfedb-112">Finally, the fifth command creates a network profile initialized with the container network interface configuration stored in $containerNicConfig.</span></span>

## <span data-ttu-id="cfedb-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cfedb-113">PARAMETERS</span></span>

### <span data-ttu-id="cfedb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfedb-114">-DefaultProfile</span></span>
<span data-ttu-id="cfedb-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cfedb-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cfedb-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="cfedb-116">-Name</span></span>
<span data-ttu-id="cfedb-117">Имя профиля IP-конфигурации сетевого интерфейса контейнера.</span><span class="sxs-lookup"><span data-stu-id="cfedb-117">Name of the container network interface configuration ip configuration profile.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfedb-118">-Подсеть</span><span class="sxs-lookup"><span data-stu-id="cfedb-118">-Subnet</span></span>
<span data-ttu-id="cfedb-119">Связью</span><span class="sxs-lookup"><span data-stu-id="cfedb-119">Subnet</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfedb-120">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="cfedb-120">-SubnetId</span></span>
<span data-ttu-id="cfedb-121">SubnetId</span><span class="sxs-lookup"><span data-stu-id="cfedb-121">SubnetId</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfedb-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cfedb-122">-Confirm</span></span>
<span data-ttu-id="cfedb-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="cfedb-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cfedb-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cfedb-124">-WhatIf</span></span>
<span data-ttu-id="cfedb-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="cfedb-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cfedb-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="cfedb-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cfedb-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfedb-127">CommonParameters</span></span>
<span data-ttu-id="cfedb-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cfedb-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfedb-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cfedb-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfedb-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cfedb-130">INPUTS</span></span>

### <span data-ttu-id="cfedb-131">Ничего</span><span class="sxs-lookup"><span data-stu-id="cfedb-131">None</span></span>

## <span data-ttu-id="cfedb-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cfedb-132">OUTPUTS</span></span>

### <span data-ttu-id="cfedb-133">Microsoft. Azure. Commands. Network. Models. PSContainerNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="cfedb-133">Microsoft.Azure.Commands.Network.Models.PSContainerNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="cfedb-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="cfedb-134">NOTES</span></span>

## <span data-ttu-id="cfedb-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cfedb-135">RELATED LINKS</span></span>

[<span data-ttu-id="cfedb-136">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="cfedb-136">New-AzContainerNicConfig</span></span>](./New-AzContainerNicConfig.md)

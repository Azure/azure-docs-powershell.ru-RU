---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-AzureRmNetworkProfileContainerNicconfigipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmContainerNicConfigIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmContainerNicConfigIpConfig.md
ms.openlocfilehash: 0a2157d006277aa491281c51f1c3b7a910b8a5c9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565864"
---
# <span data-ttu-id="a6189-101">New-AzureRmNetworkProfileContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="a6189-101">New-AzureRmNetworkProfileContainerNicConfigIpConfig</span></span>

## <span data-ttu-id="a6189-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a6189-102">SYNOPSIS</span></span>
<span data-ttu-id="a6189-103">Создает объект конфигурации конфигурации для контейнера IP-карты.</span><span class="sxs-lookup"><span data-stu-id="a6189-103">Creates a container nic configuration ip configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a6189-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a6189-104">SYNTAX</span></span>

```
New-AzureRmNetworkProfileContainerNicConfigIpConfig -Name <String> -Subnet <PSSubnet> [-SubnetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6189-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a6189-105">DESCRIPTION</span></span>
<span data-ttu-id="a6189-106">Командлет **New-AzureRmNetworkProfileContainerNicConfigIpConfig** создает новую конфигурацию IP-интерфейса сети контейнера.</span><span class="sxs-lookup"><span data-stu-id="a6189-106">The **New-AzureRmNetworkProfileContainerNicConfigIpConfig** cmdlet creates a new container network interface configuration ip configuration.</span></span> 

## <span data-ttu-id="a6189-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a6189-107">EXAMPLES</span></span>

### <span data-ttu-id="a6189-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a6189-108">Example 1</span></span>
```powershell
$subnet = New-AzureRmVirtualNetworkSubnetConfig -Name subnet -AddressPrefix 10.0.1.0/24

$vnet = New-AzureRmVirtualNetwork -Name vnet -ResourceGroupName rg1 -Location "West US" -AddressPrefix 10.0.0.0/16 -Subnet $subnet

$containerNicConfigIpConfig = New-AzureRmNetworkProfileContainerNicConfigIpConfig -Name ipconfigprofile1 -Subnet $vnet.Subnets[0]

$containerNicConfig = New-AzureRmNetworkProfileContainerNicConfig -Name cnic -IpConfiguration containerNicConfigIpConfig

$networkProfile = New-AzureRmNetworkProfile -Name np1 -Location "West US" -ResourceGroupName rg1 -ContainerNetworkInterfaceConfiguration $containerNicConfig
```

<span data-ttu-id="a6189-109">Первые две команды создают и инициализируют виртуальную сеть и подсеть.</span><span class="sxs-lookup"><span data-stu-id="a6189-109">The first two commands create and initialize a vnet and a subnet.</span></span> <span data-ttu-id="a6189-110">Третья команда создает контейнерный профиль IP NIC конфигурации, указывающий на созданную подсеть.</span><span class="sxs-lookup"><span data-stu-id="a6189-110">The third command creates a container nic ip configuration profile referencing the created subnet.</span></span>  <span data-ttu-id="a6189-111">Четвертая команда создает контейнер конфигурации сетевого интерфейса, на котором указан профиль конфигурации IP, созданный в предыдущей команде.</span><span class="sxs-lookup"><span data-stu-id="a6189-111">The fourth command creates a container network interface configuration supplying the ip configuration profile created in the previous command.</span></span> <span data-ttu-id="a6189-112">Наконец, пятая команда создает сетевой профиль, инициализируемый с помощью конфигурации контейнера сетевого интерфейса, хранящейся в $containerNicConfig.</span><span class="sxs-lookup"><span data-stu-id="a6189-112">Finally, the fifth command creates a network profile initialized with the container network interface configuration stored in $containerNicConfig.</span></span>

## <span data-ttu-id="a6189-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a6189-113">PARAMETERS</span></span>

### <span data-ttu-id="a6189-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6189-114">-DefaultProfile</span></span>
<span data-ttu-id="a6189-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a6189-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6189-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a6189-116">-Name</span></span>
<span data-ttu-id="a6189-117">Имя профиля IP-конфигурации сетевого интерфейса контейнера.</span><span class="sxs-lookup"><span data-stu-id="a6189-117">Name of the container network interface configuration ip configuration profile.</span></span>

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

### <span data-ttu-id="a6189-118">-Подсеть</span><span class="sxs-lookup"><span data-stu-id="a6189-118">-Subnet</span></span>
<span data-ttu-id="a6189-119">Связью</span><span class="sxs-lookup"><span data-stu-id="a6189-119">Subnet</span></span>

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

### <span data-ttu-id="a6189-120">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="a6189-120">-SubnetId</span></span>
<span data-ttu-id="a6189-121">SubnetId</span><span class="sxs-lookup"><span data-stu-id="a6189-121">SubnetId</span></span>

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

### <span data-ttu-id="a6189-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a6189-122">-Confirm</span></span>
<span data-ttu-id="a6189-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a6189-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6189-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6189-124">-WhatIf</span></span>
<span data-ttu-id="a6189-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a6189-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6189-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a6189-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6189-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6189-127">CommonParameters</span></span>
<span data-ttu-id="a6189-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a6189-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6189-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6189-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6189-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a6189-130">INPUTS</span></span>

### <span data-ttu-id="a6189-131">Ничего</span><span class="sxs-lookup"><span data-stu-id="a6189-131">None</span></span>

## <span data-ttu-id="a6189-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a6189-132">OUTPUTS</span></span>

### <span data-ttu-id="a6189-133">Microsoft. Azure. Commands. Network. Models. PSContainerNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="a6189-133">Microsoft.Azure.Commands.Network.Models.PSContainerNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="a6189-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="a6189-134">NOTES</span></span>

## <span data-ttu-id="a6189-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a6189-135">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-AzContainerNicconfigipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzContainerNicConfigIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzContainerNicConfigIpConfig.md
ms.openlocfilehash: 6ed82377de2a87b3bc40d3d4e8dff6af751ed1f4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101958595"
---
# <span data-ttu-id="5c6ed-101">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="5c6ed-101">New-AzContainerNicConfigIpConfig</span></span>

## <span data-ttu-id="5c6ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c6ed-102">SYNOPSIS</span></span>
<span data-ttu-id="5c6ed-103">Создание объекта конфигурации ip-конфигурации контейнера.</span><span class="sxs-lookup"><span data-stu-id="5c6ed-103">Creates a container nic configuration ip configuration object.</span></span>

## <span data-ttu-id="5c6ed-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5c6ed-104">SYNTAX</span></span>

```
New-AzContainerNicConfigIpConfig -Name <String> -Subnet <PSSubnet> [-SubnetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c6ed-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5c6ed-105">DESCRIPTION</span></span>
<span data-ttu-id="5c6ed-106">С **помощью cmdlet New-AzContainerNicConfigIpConfig создается** конфигурация IP-интерфейса контейнера.</span><span class="sxs-lookup"><span data-stu-id="5c6ed-106">The **New-AzContainerNicConfigIpConfig** cmdlet creates a new container network interface configuration ip configuration.</span></span> 

## <span data-ttu-id="5c6ed-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5c6ed-107">EXAMPLES</span></span>

### <span data-ttu-id="5c6ed-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5c6ed-108">Example 1</span></span>
```powershell
$subnet = New-AzVirtualNetworkSubnetConfig -Name subnet -AddressPrefix 10.0.1.0/24

$vnet = New-AzVirtualNetwork -Name vnet -ResourceGroupName rg1 -Location "West US" -AddressPrefix 10.0.0.0/16 -Subnet $subnet

$containerNicConfigIpConfig = New-AzContainerNicConfigIpConfig -Name ipconfigprofile1 -Subnet $vnet.Subnets[0]

$containerNicConfig = New-AzContainerNicConfig -Name cnic -IpConfiguration containerNicConfigIpConfig

$networkProfile = New-AzNetworkProfile -Name np1 -Location "West US" -ResourceGroupName rg1 -ContainerNetworkInterfaceConfiguration $containerNicConfig
```

<span data-ttu-id="5c6ed-109">Первые две команды создают и инициализируют vnet и подсеть.</span><span class="sxs-lookup"><span data-stu-id="5c6ed-109">The first two commands create and initialize a vnet and a subnet.</span></span> <span data-ttu-id="5c6ed-110">Третья команда создает профиль конфигурации контейнера nic, ссылающийся на созданную подсеть.</span><span class="sxs-lookup"><span data-stu-id="5c6ed-110">The third command creates a container nic ip configuration profile referencing the created subnet.</span></span> <span data-ttu-id="5c6ed-111">Четвертая команда создает конфигурацию сетевого интерфейса контейнера с профилем конфигурации IP, созданным в предыдущей команде.</span><span class="sxs-lookup"><span data-stu-id="5c6ed-111">The fourth command creates a container network interface configuration supplying the ip configuration profile created in the previous command.</span></span> <span data-ttu-id="5c6ed-112">Наконец, пятая команда создает профиль сети, инициализированный с конфигурацией сетевого интерфейса контейнера, храняной в $containerNicConfig.</span><span class="sxs-lookup"><span data-stu-id="5c6ed-112">Finally, the fifth command creates a network profile initialized with the container network interface configuration stored in $containerNicConfig.</span></span>

## <span data-ttu-id="5c6ed-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5c6ed-113">PARAMETERS</span></span>

### <span data-ttu-id="5c6ed-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c6ed-114">-DefaultProfile</span></span>
<span data-ttu-id="5c6ed-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5c6ed-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5c6ed-116">-Name</span><span class="sxs-lookup"><span data-stu-id="5c6ed-116">-Name</span></span>
<span data-ttu-id="5c6ed-117">Имя профиля конфигурации конфигурации сетевого интерфейса контейнера.</span><span class="sxs-lookup"><span data-stu-id="5c6ed-117">Name of the container network interface configuration ip configuration profile.</span></span>

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

### <span data-ttu-id="5c6ed-118">-Subnet</span><span class="sxs-lookup"><span data-stu-id="5c6ed-118">-Subnet</span></span>
<span data-ttu-id="5c6ed-119">Подсеть</span><span class="sxs-lookup"><span data-stu-id="5c6ed-119">Subnet</span></span>

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

### <span data-ttu-id="5c6ed-120">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="5c6ed-120">-SubnetId</span></span>
<span data-ttu-id="5c6ed-121">SubnetId</span><span class="sxs-lookup"><span data-stu-id="5c6ed-121">SubnetId</span></span>

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

### <span data-ttu-id="5c6ed-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5c6ed-122">-Confirm</span></span>
<span data-ttu-id="5c6ed-123">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5c6ed-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c6ed-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c6ed-124">-WhatIf</span></span>
<span data-ttu-id="5c6ed-125">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5c6ed-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c6ed-126">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="5c6ed-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c6ed-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c6ed-127">CommonParameters</span></span>
<span data-ttu-id="5c6ed-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c6ed-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c6ed-129">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c6ed-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c6ed-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5c6ed-130">INPUTS</span></span>

### <span data-ttu-id="5c6ed-131">Нет</span><span class="sxs-lookup"><span data-stu-id="5c6ed-131">None</span></span>

## <span data-ttu-id="5c6ed-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5c6ed-132">OUTPUTS</span></span>

### <span data-ttu-id="5c6ed-133">Microsoft.Azure.Commands.Network.Models.PSContainerNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="5c6ed-133">Microsoft.Azure.Commands.Network.Models.PSContainerNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="5c6ed-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5c6ed-134">NOTES</span></span>

## <span data-ttu-id="5c6ed-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5c6ed-135">RELATED LINKS</span></span>

[<span data-ttu-id="5c6ed-136">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="5c6ed-136">New-AzContainerNicConfig</span></span>](./New-AzContainerNicConfig.md)

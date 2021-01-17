---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-AzContainerNicconfigipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzContainerNicConfigIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzContainerNicConfigIpConfig.md
ms.openlocfilehash: 2e15819fe8b6b21b0f0c0751dc39736408606a7c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98416095"
---
# <span data-ttu-id="12b7d-101">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="12b7d-101">New-AzContainerNicConfigIpConfig</span></span>

## <span data-ttu-id="12b7d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12b7d-102">SYNOPSIS</span></span>
<span data-ttu-id="12b7d-103">Создание объекта конфигурации ip-конфигурации контейнера.</span><span class="sxs-lookup"><span data-stu-id="12b7d-103">Creates a container nic configuration ip configuration object.</span></span>

## <span data-ttu-id="12b7d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="12b7d-104">SYNTAX</span></span>

```
New-AzContainerNicConfigIpConfig -Name <String> -Subnet <PSSubnet> [-SubnetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12b7d-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="12b7d-105">DESCRIPTION</span></span>
<span data-ttu-id="12b7d-106">С **помощью cmdlet New-AzContainerNicConfigIpConfig создается** конфигурация IP-интерфейса контейнера.</span><span class="sxs-lookup"><span data-stu-id="12b7d-106">The **New-AzContainerNicConfigIpConfig** cmdlet creates a new container network interface configuration ip configuration.</span></span> 

## <span data-ttu-id="12b7d-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="12b7d-107">EXAMPLES</span></span>

### <span data-ttu-id="12b7d-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="12b7d-108">Example 1</span></span>
```powershell
$subnet = New-AzVirtualNetworkSubnetConfig -Name subnet -AddressPrefix 10.0.1.0/24

$vnet = New-AzVirtualNetwork -Name vnet -ResourceGroupName rg1 -Location "West US" -AddressPrefix 10.0.0.0/16 -Subnet $subnet

$containerNicConfigIpConfig = New-AzContainerNicConfigIpConfig -Name ipconfigprofile1 -Subnet $vnet.Subnets[0]

$containerNicConfig = New-AzContainerNicConfig -Name cnic -IpConfiguration containerNicConfigIpConfig

$networkProfile = New-AzNetworkProfile -Name np1 -Location "West US" -ResourceGroupName rg1 -ContainerNetworkInterfaceConfiguration $containerNicConfig
```

<span data-ttu-id="12b7d-109">Первые две команды создают и инициализируют vnet и подсеть.</span><span class="sxs-lookup"><span data-stu-id="12b7d-109">The first two commands create and initialize a vnet and a subnet.</span></span> <span data-ttu-id="12b7d-110">Третья команда создает профиль конфигурации контейнера nic, ссылающийся на созданную подсеть.</span><span class="sxs-lookup"><span data-stu-id="12b7d-110">The third command creates a container nic ip configuration profile referencing the created subnet.</span></span> <span data-ttu-id="12b7d-111">Четвертая команда создает конфигурацию сетевого интерфейса контейнера с профилем конфигурации IP, созданным в предыдущей команде.</span><span class="sxs-lookup"><span data-stu-id="12b7d-111">The fourth command creates a container network interface configuration supplying the ip configuration profile created in the previous command.</span></span> <span data-ttu-id="12b7d-112">Наконец, пятая команда создает профиль сети, инициализированный с конфигурацией сетевого интерфейса контейнера, храняной в $containerNicConfig.</span><span class="sxs-lookup"><span data-stu-id="12b7d-112">Finally, the fifth command creates a network profile initialized with the container network interface configuration stored in $containerNicConfig.</span></span>

## <span data-ttu-id="12b7d-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="12b7d-113">PARAMETERS</span></span>

### <span data-ttu-id="12b7d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12b7d-114">-DefaultProfile</span></span>
<span data-ttu-id="12b7d-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="12b7d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12b7d-116">-Name</span><span class="sxs-lookup"><span data-stu-id="12b7d-116">-Name</span></span>
<span data-ttu-id="12b7d-117">Имя профиля конфигурации сетевого интерфейса контейнера.</span><span class="sxs-lookup"><span data-stu-id="12b7d-117">Name of the container network interface configuration ip configuration profile.</span></span>

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

### <span data-ttu-id="12b7d-118">-Subnet</span><span class="sxs-lookup"><span data-stu-id="12b7d-118">-Subnet</span></span>
<span data-ttu-id="12b7d-119">Подсеть</span><span class="sxs-lookup"><span data-stu-id="12b7d-119">Subnet</span></span>

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

### <span data-ttu-id="12b7d-120">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="12b7d-120">-SubnetId</span></span>
<span data-ttu-id="12b7d-121">SubnetId</span><span class="sxs-lookup"><span data-stu-id="12b7d-121">SubnetId</span></span>

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

### <span data-ttu-id="12b7d-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="12b7d-122">-Confirm</span></span>
<span data-ttu-id="12b7d-123">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="12b7d-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12b7d-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12b7d-124">-WhatIf</span></span>
<span data-ttu-id="12b7d-125">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="12b7d-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12b7d-126">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="12b7d-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12b7d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12b7d-127">CommonParameters</span></span>
<span data-ttu-id="12b7d-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12b7d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12b7d-129">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12b7d-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12b7d-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="12b7d-130">INPUTS</span></span>

### <span data-ttu-id="12b7d-131">Нет</span><span class="sxs-lookup"><span data-stu-id="12b7d-131">None</span></span>

## <span data-ttu-id="12b7d-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="12b7d-132">OUTPUTS</span></span>

### <span data-ttu-id="12b7d-133">Microsoft.Azure.Commands.Network.Models.PSContainerNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="12b7d-133">Microsoft.Azure.Commands.Network.Models.PSContainerNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="12b7d-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="12b7d-134">NOTES</span></span>

## <span data-ttu-id="12b7d-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="12b7d-135">RELATED LINKS</span></span>

[<span data-ttu-id="12b7d-136">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="12b7d-136">New-AzContainerNicConfig</span></span>](./New-AzContainerNicConfig.md)

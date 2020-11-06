---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D7065B04-1A01-4BB4-A519-1DA9002CDE02
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayConnection.md
ms.openlocfilehash: 218ef3115a4bc8325bc4dda37ae0a5e5820afae2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561691"
---
# <span data-ttu-id="7fdea-101">Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="7fdea-101">Set-AzureRmVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="7fdea-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7fdea-102">SYNOPSIS</span></span>
<span data-ttu-id="7fdea-103">Настройка подключения к шлюзу виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="7fdea-103">Configures a virtual network gateway connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7fdea-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7fdea-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetworkGatewayConnection -VirtualNetworkGatewayConnection <PSVirtualNetworkGatewayConnection>
 [-EnableBgp <Boolean>] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-IpsecPolicies <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7fdea-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7fdea-105">DESCRIPTION</span></span>
<span data-ttu-id="7fdea-106">Командлет **Set-AzureRmVirtualNetworkGatewayConnection** настраивает подключение к шлюзу виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="7fdea-106">The **Set-AzureRmVirtualNetworkGatewayConnection** cmdlet configures a virtual network gateway connection.</span></span>

## <span data-ttu-id="7fdea-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7fdea-107">EXAMPLES</span></span>

## <span data-ttu-id="7fdea-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7fdea-108">PARAMETERS</span></span>

### <span data-ttu-id="7fdea-109">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7fdea-109">-AsJob</span></span>
<span data-ttu-id="7fdea-110">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="7fdea-110">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fdea-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fdea-111">-DefaultProfile</span></span>
<span data-ttu-id="7fdea-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7fdea-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fdea-113">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="7fdea-113">-EnableBgp</span></span>
<span data-ttu-id="7fdea-114">Необходимость использования сеанса BGP через туннель VPN S2S</span><span class="sxs-lookup"><span data-stu-id="7fdea-114">Whether to use a BGP session over a S2S VPN tunnel</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7fdea-115">-Force</span><span class="sxs-lookup"><span data-stu-id="7fdea-115">-Force</span></span>
<span data-ttu-id="7fdea-116">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="7fdea-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fdea-117">-IpsecPolicies</span><span class="sxs-lookup"><span data-stu-id="7fdea-117">-IpsecPolicies</span></span>
<span data-ttu-id="7fdea-118">Список политик IPSec.</span><span class="sxs-lookup"><span data-stu-id="7fdea-118">A list of IPSec policies.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7fdea-119">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="7fdea-119">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="7fdea-120">Следует ли использовать селекторы трафика на основе политики для S2S-соединения</span><span class="sxs-lookup"><span data-stu-id="7fdea-120">Whether to use policy-based traffic selectors for a S2S connection</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fdea-121">-VirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="7fdea-121">-VirtualNetworkGatewayConnection</span></span>
<span data-ttu-id="7fdea-122">Указывает объект PSVirtualNetworkGatewayConnection, используемый этим командлетом для изменения подключения к шлюзу виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="7fdea-122">Specifies the PSVirtualNetworkGatewayConnection object that this cmdlet uses to modify the virtual network gateway connection.</span></span>

```yaml
Type: PSVirtualNetworkGatewayConnection
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7fdea-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7fdea-123">-Confirm</span></span>
<span data-ttu-id="7fdea-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7fdea-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fdea-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7fdea-125">-WhatIf</span></span>
<span data-ttu-id="7fdea-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7fdea-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7fdea-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7fdea-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fdea-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fdea-128">CommonParameters</span></span>
<span data-ttu-id="7fdea-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7fdea-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fdea-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7fdea-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fdea-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7fdea-131">INPUTS</span></span>

### <span data-ttu-id="7fdea-132">PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="7fdea-132">PSVirtualNetworkGatewayConnection</span></span>
<span data-ttu-id="7fdea-133">Параметр "VirtualNetworkGatewayConnection" принимает значение типа "PSVirtualNetworkGatewayConnection" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="7fdea-133">Parameter 'VirtualNetworkGatewayConnection' accepts value of type 'PSVirtualNetworkGatewayConnection' from the pipeline</span></span>

## <span data-ttu-id="7fdea-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7fdea-134">OUTPUTS</span></span>

### <span data-ttu-id="7fdea-135">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="7fdea-135">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="7fdea-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="7fdea-136">NOTES</span></span>

## <span data-ttu-id="7fdea-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7fdea-137">RELATED LINKS</span></span>

[<span data-ttu-id="7fdea-138">Get-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="7fdea-138">Get-AzureRmVirtualNetworkGatewayConnection</span></span>](./Get-AzureRmVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="7fdea-139">New-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="7fdea-139">New-AzureRmVirtualNetworkGatewayConnection</span></span>](./New-AzureRmVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="7fdea-140">Remove-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="7fdea-140">Remove-AzureRmVirtualNetworkGatewayConnection</span></span>](./Remove-AzureRmVirtualNetworkGatewayConnection.md)



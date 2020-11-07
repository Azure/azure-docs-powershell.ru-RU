---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D7065B04-1A01-4BB4-A519-1DA9002CDE02
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetworkgatewayconnection
schema: 2.0.0
ms.openlocfilehash: bb098e23f6e55cc28fcae02b7094a953c5179308
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914394"
---
# <span data-ttu-id="cd9f8-101">Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="cd9f8-101">Set-AzureRmVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="cd9f8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cd9f8-102">SYNOPSIS</span></span>
<span data-ttu-id="cd9f8-103">Настройка подключения к шлюзу виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="cd9f8-103">Configures a virtual network gateway connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cd9f8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cd9f8-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetworkGatewayConnection -VirtualNetworkGatewayConnection <PSVirtualNetworkGatewayConnection>
 [-EnableBgp <Boolean>] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-IpsecPolicies <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd9f8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cd9f8-105">DESCRIPTION</span></span>
<span data-ttu-id="cd9f8-106">Командлет **Set-AzureRmVirtualNetworkGatewayConnection** настраивает подключение к шлюзу виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="cd9f8-106">The **Set-AzureRmVirtualNetworkGatewayConnection** cmdlet configures a virtual network gateway connection.</span></span>

## <span data-ttu-id="cd9f8-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cd9f8-107">EXAMPLES</span></span>

### <span data-ttu-id="cd9f8-108">1:</span><span class="sxs-lookup"><span data-stu-id="cd9f8-108">1:</span></span>
```

```

## <span data-ttu-id="cd9f8-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cd9f8-109">PARAMETERS</span></span>

### <span data-ttu-id="cd9f8-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cd9f8-110">-AsJob</span></span>
<span data-ttu-id="cd9f8-111">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="cd9f8-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cd9f8-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd9f8-112">-DefaultProfile</span></span>
<span data-ttu-id="cd9f8-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cd9f8-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cd9f8-114">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="cd9f8-114">-EnableBgp</span></span>
<span data-ttu-id="cd9f8-115">Необходимость использования сеанса BGP через туннель VPN S2S</span><span class="sxs-lookup"><span data-stu-id="cd9f8-115">Whether to use a BGP session over a S2S VPN tunnel</span></span>

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

### <span data-ttu-id="cd9f8-116">-Force</span><span class="sxs-lookup"><span data-stu-id="cd9f8-116">-Force</span></span>
<span data-ttu-id="cd9f8-117">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="cd9f8-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="cd9f8-118">-IpsecPolicies</span><span class="sxs-lookup"><span data-stu-id="cd9f8-118">-IpsecPolicies</span></span>
<span data-ttu-id="cd9f8-119">Список политик IPSec.</span><span class="sxs-lookup"><span data-stu-id="cd9f8-119">A list of IPSec policies.</span></span>

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

### <span data-ttu-id="cd9f8-120">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="cd9f8-120">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="cd9f8-121">Следует ли использовать селекторы трафика на основе политики для S2S-соединения</span><span class="sxs-lookup"><span data-stu-id="cd9f8-121">Whether to use policy-based traffic selectors for a S2S connection</span></span>

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

### <span data-ttu-id="cd9f8-122">-VirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="cd9f8-122">-VirtualNetworkGatewayConnection</span></span>
<span data-ttu-id="cd9f8-123">Указывает объект PSVirtualNetworkGatewayConnection, используемый этим командлетом для изменения подключения к шлюзу виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="cd9f8-123">Specifies the PSVirtualNetworkGatewayConnection object that this cmdlet uses to modify the virtual network gateway connection.</span></span>

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

### <span data-ttu-id="cd9f8-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cd9f8-124">-Confirm</span></span>
<span data-ttu-id="cd9f8-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="cd9f8-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd9f8-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd9f8-126">-WhatIf</span></span>
<span data-ttu-id="cd9f8-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="cd9f8-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd9f8-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="cd9f8-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd9f8-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd9f8-129">CommonParameters</span></span>
<span data-ttu-id="cd9f8-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cd9f8-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd9f8-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd9f8-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd9f8-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cd9f8-132">INPUTS</span></span>

### <span data-ttu-id="cd9f8-133">PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="cd9f8-133">PSVirtualNetworkGatewayConnection</span></span>
<span data-ttu-id="cd9f8-134">Параметр "VirtualNetworkGatewayConnection" принимает значение типа "PSVirtualNetworkGatewayConnection" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="cd9f8-134">Parameter 'VirtualNetworkGatewayConnection' accepts value of type 'PSVirtualNetworkGatewayConnection' from the pipeline</span></span>

## <span data-ttu-id="cd9f8-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cd9f8-135">OUTPUTS</span></span>

### <span data-ttu-id="cd9f8-136">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="cd9f8-136">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="cd9f8-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="cd9f8-137">NOTES</span></span>

## <span data-ttu-id="cd9f8-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cd9f8-138">RELATED LINKS</span></span>

[<span data-ttu-id="cd9f8-139">Get-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="cd9f8-139">Get-AzureRmVirtualNetworkGatewayConnection</span></span>](./Get-AzureRmVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="cd9f8-140">New-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="cd9f8-140">New-AzureRmVirtualNetworkGatewayConnection</span></span>](./New-AzureRmVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="cd9f8-141">Remove-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="cd9f8-141">Remove-AzureRmVirtualNetworkGatewayConnection</span></span>](./Remove-AzureRmVirtualNetworkGatewayConnection.md)



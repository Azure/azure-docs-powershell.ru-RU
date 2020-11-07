---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D7065B04-1A01-4BB4-A519-1DA9002CDE02
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: b38ef9d212ceeb519e29d99391b17099177236a5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911012"
---
# <span data-ttu-id="ea08d-101">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="ea08d-101">Set-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="ea08d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ea08d-102">SYNOPSIS</span></span>
<span data-ttu-id="ea08d-103">Настройка подключения к шлюзу виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="ea08d-103">Configures a virtual network gateway connection.</span></span>

## <span data-ttu-id="ea08d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ea08d-104">SYNTAX</span></span>

```
Set-AzVirtualNetworkGatewayConnection -VirtualNetworkGatewayConnection <PSVirtualNetworkGatewayConnection>
 [-EnableBgp <Boolean>] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-IpsecPolicies <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea08d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ea08d-105">DESCRIPTION</span></span>
<span data-ttu-id="ea08d-106">Командлет **Set-AzVirtualNetworkGatewayConnection** настраивает подключение к шлюзу виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="ea08d-106">The **Set-AzVirtualNetworkGatewayConnection** cmdlet configures a virtual network gateway connection.</span></span>

## <span data-ttu-id="ea08d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ea08d-107">EXAMPLES</span></span>

### <span data-ttu-id="ea08d-108">1:</span><span class="sxs-lookup"><span data-stu-id="ea08d-108">1:</span></span>
```

```

## <span data-ttu-id="ea08d-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ea08d-109">PARAMETERS</span></span>

### <span data-ttu-id="ea08d-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ea08d-110">-AsJob</span></span>
<span data-ttu-id="ea08d-111">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="ea08d-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ea08d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea08d-112">-DefaultProfile</span></span>
<span data-ttu-id="ea08d-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ea08d-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ea08d-114">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="ea08d-114">-EnableBgp</span></span>
<span data-ttu-id="ea08d-115">Необходимость использования сеанса BGP через туннель VPN S2S</span><span class="sxs-lookup"><span data-stu-id="ea08d-115">Whether to use a BGP session over a S2S VPN tunnel</span></span>

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

### <span data-ttu-id="ea08d-116">-Force</span><span class="sxs-lookup"><span data-stu-id="ea08d-116">-Force</span></span>
<span data-ttu-id="ea08d-117">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="ea08d-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ea08d-118">-IpsecPolicies</span><span class="sxs-lookup"><span data-stu-id="ea08d-118">-IpsecPolicies</span></span>
<span data-ttu-id="ea08d-119">Список политик IPSec.</span><span class="sxs-lookup"><span data-stu-id="ea08d-119">A list of IPSec policies.</span></span>

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

### <span data-ttu-id="ea08d-120">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="ea08d-120">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="ea08d-121">Следует ли использовать селекторы трафика на основе политики для S2S-соединения</span><span class="sxs-lookup"><span data-stu-id="ea08d-121">Whether to use policy-based traffic selectors for a S2S connection</span></span>

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

### <span data-ttu-id="ea08d-122">-VirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="ea08d-122">-VirtualNetworkGatewayConnection</span></span>
<span data-ttu-id="ea08d-123">Указывает объект PSVirtualNetworkGatewayConnection, используемый этим командлетом для изменения подключения к шлюзу виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="ea08d-123">Specifies the PSVirtualNetworkGatewayConnection object that this cmdlet uses to modify the virtual network gateway connection.</span></span>

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

### <span data-ttu-id="ea08d-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ea08d-124">-Confirm</span></span>
<span data-ttu-id="ea08d-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ea08d-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea08d-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea08d-126">-WhatIf</span></span>
<span data-ttu-id="ea08d-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ea08d-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea08d-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ea08d-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea08d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea08d-129">CommonParameters</span></span>
<span data-ttu-id="ea08d-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ea08d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea08d-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea08d-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea08d-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ea08d-132">INPUTS</span></span>

### <span data-ttu-id="ea08d-133">PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="ea08d-133">PSVirtualNetworkGatewayConnection</span></span>
<span data-ttu-id="ea08d-134">Параметр "VirtualNetworkGatewayConnection" принимает значение типа "PSVirtualNetworkGatewayConnection" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="ea08d-134">Parameter 'VirtualNetworkGatewayConnection' accepts value of type 'PSVirtualNetworkGatewayConnection' from the pipeline</span></span>

## <span data-ttu-id="ea08d-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ea08d-135">OUTPUTS</span></span>

### <span data-ttu-id="ea08d-136">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="ea08d-136">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="ea08d-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="ea08d-137">NOTES</span></span>

## <span data-ttu-id="ea08d-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ea08d-138">RELATED LINKS</span></span>

[<span data-ttu-id="ea08d-139">Get-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="ea08d-139">Get-AzVirtualNetworkGatewayConnection</span></span>](./Get-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="ea08d-140">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="ea08d-140">New-AzVirtualNetworkGatewayConnection</span></span>](./New-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="ea08d-141">Remove-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="ea08d-141">Remove-AzVirtualNetworkGatewayConnection</span></span>](./Remove-AzVirtualNetworkGatewayConnection.md)



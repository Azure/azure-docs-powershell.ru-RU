---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D7065B04-1A01-4BB4-A519-1DA9002CDE02
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayConnection.md
ms.openlocfilehash: 5885f98d66e6226273215dcde856f5fc50d0bd56
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562380"
---
# <span data-ttu-id="7cd44-101">Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="7cd44-101">Set-AzureRmVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="7cd44-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7cd44-102">SYNOPSIS</span></span>
<span data-ttu-id="7cd44-103">Настройка подключения к шлюзу виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="7cd44-103">Configures a virtual network gateway connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7cd44-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7cd44-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetworkGatewayConnection -VirtualNetworkGatewayConnection <PSVirtualNetworkGatewayConnection>
 [-EnableBgp <Boolean>] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-IpsecPolicies <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7cd44-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7cd44-105">DESCRIPTION</span></span>
<span data-ttu-id="7cd44-106">Командлет **Set-AzureRmVirtualNetworkGatewayConnection** настраивает подключение к шлюзу виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="7cd44-106">The **Set-AzureRmVirtualNetworkGatewayConnection** cmdlet configures a virtual network gateway connection.</span></span>

## <span data-ttu-id="7cd44-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7cd44-107">EXAMPLES</span></span>

## <span data-ttu-id="7cd44-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7cd44-108">PARAMETERS</span></span>

### <span data-ttu-id="7cd44-109">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="7cd44-109">-EnableBgp</span></span>
<span data-ttu-id="7cd44-110">Необходимость использования сеанса BGP через туннель VPN S2S</span><span class="sxs-lookup"><span data-stu-id="7cd44-110">Whether to use a BGP session over a S2S VPN tunnel</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7cd44-111">-Force</span><span class="sxs-lookup"><span data-stu-id="7cd44-111">-Force</span></span>
<span data-ttu-id="7cd44-112">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="7cd44-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7cd44-113">-IpsecPolicies</span><span class="sxs-lookup"><span data-stu-id="7cd44-113">-IpsecPolicies</span></span>
<span data-ttu-id="7cd44-114">Список политик IPSec.</span><span class="sxs-lookup"><span data-stu-id="7cd44-114">A list of IPSec policies.</span></span>

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

### <span data-ttu-id="7cd44-115">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="7cd44-115">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="7cd44-116">Следует ли использовать селекторы трафика на основе политики для S2S-соединения</span><span class="sxs-lookup"><span data-stu-id="7cd44-116">Whether to use policy-based traffic selectors for a S2S connection</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cd44-117">-VirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="7cd44-117">-VirtualNetworkGatewayConnection</span></span>
<span data-ttu-id="7cd44-118">Указывает объект PSVirtualNetworkGatewayConnection, используемый этим командлетом для изменения подключения к шлюзу виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="7cd44-118">Specifies the PSVirtualNetworkGatewayConnection object that this cmdlet uses to modify the virtual network gateway connection.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7cd44-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7cd44-119">-Confirm</span></span>
<span data-ttu-id="7cd44-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7cd44-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cd44-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7cd44-121">-WhatIf</span></span>
<span data-ttu-id="7cd44-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7cd44-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7cd44-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7cd44-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cd44-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cd44-124">-DefaultProfile</span></span>
<span data-ttu-id="7cd44-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7cd44-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7cd44-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cd44-126">CommonParameters</span></span>
<span data-ttu-id="7cd44-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7cd44-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cd44-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7cd44-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cd44-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7cd44-129">INPUTS</span></span>

### <span data-ttu-id="7cd44-130">PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="7cd44-130">PSVirtualNetworkGatewayConnection</span></span>
<span data-ttu-id="7cd44-131">Параметр "VirtualNetworkGatewayConnection" принимает значение типа "PSVirtualNetworkGatewayConnection" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="7cd44-131">Parameter 'VirtualNetworkGatewayConnection' accepts value of type 'PSVirtualNetworkGatewayConnection' from the pipeline</span></span>

## <span data-ttu-id="7cd44-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7cd44-132">OUTPUTS</span></span>

### <span data-ttu-id="7cd44-133">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="7cd44-133">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="7cd44-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="7cd44-134">NOTES</span></span>

## <span data-ttu-id="7cd44-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7cd44-135">RELATED LINKS</span></span>

[<span data-ttu-id="7cd44-136">Get-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="7cd44-136">Get-AzureRmVirtualNetworkGatewayConnection</span></span>](./Get-AzureRmVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="7cd44-137">New-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="7cd44-137">New-AzureRmVirtualNetworkGatewayConnection</span></span>](./New-AzureRmVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="7cd44-138">Remove-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="7cd44-138">Remove-AzureRmVirtualNetworkGatewayConnection</span></span>](./Remove-AzureRmVirtualNetworkGatewayConnection.md)



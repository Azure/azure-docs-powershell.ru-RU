---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 443F6492-EFA7-4417-943A-3A8D47F8C83C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/reset-azurermvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Reset-AzureRmVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Reset-AzureRmVirtualNetworkGateway.md
ms.openlocfilehash: c5d77619fa5f89c60ce20a097e096709e9a48bae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568447"
---
# <span data-ttu-id="1c1a3-101">Reset-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1c1a3-101">Reset-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="1c1a3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1c1a3-102">SYNOPSIS</span></span>
<span data-ttu-id="1c1a3-103">Сброс шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="1c1a3-103">Resets the Virtual Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1c1a3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1c1a3-104">SYNTAX</span></span>

```
Reset-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewayVip <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1c1a3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1c1a3-105">DESCRIPTION</span></span>
<span data-ttu-id="1c1a3-106">Сброс шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="1c1a3-106">Resets the Virtual Network Gateway</span></span>

## <span data-ttu-id="1c1a3-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1c1a3-107">EXAMPLES</span></span>

### <span data-ttu-id="1c1a3-108">Пример 1:</span><span class="sxs-lookup"><span data-stu-id="1c1a3-108">Example 1:</span></span>
```
$Gateway = Get-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway"
Reset-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $Gateway
```

## <span data-ttu-id="1c1a3-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1c1a3-109">PARAMETERS</span></span>

### <span data-ttu-id="1c1a3-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1c1a3-110">-AsJob</span></span>
<span data-ttu-id="1c1a3-111">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="1c1a3-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1c1a3-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c1a3-112">-DefaultProfile</span></span>
<span data-ttu-id="1c1a3-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1c1a3-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1c1a3-114">-GatewayVip</span><span class="sxs-lookup"><span data-stu-id="1c1a3-114">-GatewayVip</span></span>
<span data-ttu-id="1c1a3-115">IP-адрес шлюза для сброса определенного экземпляра шлюза (например, в случае включения Active-Activeных шлюзов). По умолчанию основной экземпляр шлюза будет сброшен, если значение не передается.</span><span class="sxs-lookup"><span data-stu-id="1c1a3-115">The gateway vip in order to reset particular gateway instance (e.g. in case of Active-Active feature enabled gateways.) By default, gateway primary instance will be reset if no value is passed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1c1a3-116">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1c1a3-116">-VirtualNetworkGateway</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1c1a3-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c1a3-117">CommonParameters</span></span>
<span data-ttu-id="1c1a3-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1c1a3-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c1a3-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c1a3-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c1a3-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1c1a3-120">INPUTS</span></span>

### <span data-ttu-id="1c1a3-121">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1c1a3-121">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>
<span data-ttu-id="1c1a3-122">Параметры: VirtualNetworkGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="1c1a3-122">Parameters: VirtualNetworkGateway (ByValue)</span></span>

### <span data-ttu-id="1c1a3-123">System. String</span><span class="sxs-lookup"><span data-stu-id="1c1a3-123">System.String</span></span>
<span data-ttu-id="1c1a3-124">Параметры: GatewayVip (ByValue)</span><span class="sxs-lookup"><span data-stu-id="1c1a3-124">Parameters: GatewayVip (ByValue)</span></span>

## <span data-ttu-id="1c1a3-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1c1a3-125">OUTPUTS</span></span>

### <span data-ttu-id="1c1a3-126">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1c1a3-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="1c1a3-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="1c1a3-127">NOTES</span></span>

## <span data-ttu-id="1c1a3-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1c1a3-128">RELATED LINKS</span></span>

[<span data-ttu-id="1c1a3-129">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1c1a3-129">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="1c1a3-130">New-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1c1a3-130">New-AzureRmVirtualNetworkGateway</span></span>](./New-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="1c1a3-131">Remove-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1c1a3-131">Remove-AzureRmVirtualNetworkGateway</span></span>](./Remove-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="1c1a3-132">Изменить размер — AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1c1a3-132">Resize-AzureRmVirtualNetworkGateway</span></span>](./Resize-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="1c1a3-133">Set-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1c1a3-133">Set-AzureRmVirtualNetworkGateway</span></span>](./Set-AzureRmVirtualNetworkGateway.md)



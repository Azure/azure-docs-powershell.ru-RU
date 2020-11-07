---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 443F6492-EFA7-4417-943A-3A8D47F8C83C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/reset-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVirtualNetworkGateway.md
ms.openlocfilehash: 59f4a96c324a9743c876cf987e1347bbe0c8d946
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730080"
---
# <span data-ttu-id="b34c0-101">Reset-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b34c0-101">Reset-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="b34c0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b34c0-102">SYNOPSIS</span></span>
<span data-ttu-id="b34c0-103">Сброс шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="b34c0-103">Resets the Virtual Network Gateway</span></span>

## <span data-ttu-id="b34c0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b34c0-104">SYNTAX</span></span>

```
Reset-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewayVip <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b34c0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b34c0-105">DESCRIPTION</span></span>
<span data-ttu-id="b34c0-106">Сброс шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="b34c0-106">Resets the Virtual Network Gateway</span></span>

## <span data-ttu-id="b34c0-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b34c0-107">EXAMPLES</span></span>

### <span data-ttu-id="b34c0-108">Пример 1:</span><span class="sxs-lookup"><span data-stu-id="b34c0-108">Example 1:</span></span>
```
$Gateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
Reset-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway
```

## <span data-ttu-id="b34c0-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b34c0-109">PARAMETERS</span></span>

### <span data-ttu-id="b34c0-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b34c0-110">-AsJob</span></span>
<span data-ttu-id="b34c0-111">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="b34c0-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b34c0-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b34c0-112">-DefaultProfile</span></span>
<span data-ttu-id="b34c0-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b34c0-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b34c0-114">-GatewayVip</span><span class="sxs-lookup"><span data-stu-id="b34c0-114">-GatewayVip</span></span>
<span data-ttu-id="b34c0-115">IP-адрес шлюза для сброса определенного экземпляра шлюза (например, в случае включения Active-Activeных шлюзов). По умолчанию основной экземпляр шлюза будет сброшен, если значение не передается.</span><span class="sxs-lookup"><span data-stu-id="b34c0-115">The gateway vip in order to reset particular gateway instance (e.g. in case of Active-Active feature enabled gateways.) By default, gateway primary instance will be reset if no value is passed.</span></span>

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

### <span data-ttu-id="b34c0-116">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b34c0-116">-VirtualNetworkGateway</span></span>
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

### <span data-ttu-id="b34c0-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b34c0-117">CommonParameters</span></span>
<span data-ttu-id="b34c0-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b34c0-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b34c0-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b34c0-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b34c0-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b34c0-120">INPUTS</span></span>

### <span data-ttu-id="b34c0-121">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b34c0-121">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="b34c0-122">System. String</span><span class="sxs-lookup"><span data-stu-id="b34c0-122">System.String</span></span>

## <span data-ttu-id="b34c0-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b34c0-123">OUTPUTS</span></span>

### <span data-ttu-id="b34c0-124">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b34c0-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="b34c0-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="b34c0-125">NOTES</span></span>

## <span data-ttu-id="b34c0-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b34c0-126">RELATED LINKS</span></span>

[<span data-ttu-id="b34c0-127">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b34c0-127">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="b34c0-128">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b34c0-128">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="b34c0-129">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b34c0-129">Remove-AzVirtualNetworkGateway</span></span>](./Remove-AzVirtualNetworkGateway.md)

[<span data-ttu-id="b34c0-130">Изменить размер — AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b34c0-130">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)

[<span data-ttu-id="b34c0-131">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b34c0-131">Set-AzVirtualNetworkGateway</span></span>](./Set-AzVirtualNetworkGateway.md)

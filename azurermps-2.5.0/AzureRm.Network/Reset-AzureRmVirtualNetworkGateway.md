---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 443F6492-EFA7-4417-943A-3A8D47F8C83C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/reset-azurermvirtualnetworkgateway
schema: 2.0.0
ms.openlocfilehash: f4039fb8a616a474a858728b6e222537c2d75c66
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93915070"
---
# <span data-ttu-id="80fbe-101">Reset-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="80fbe-101">Reset-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="80fbe-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="80fbe-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="80fbe-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="80fbe-103">SYNTAX</span></span>

```
Reset-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewayVip <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="80fbe-104">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="80fbe-104">DESCRIPTION</span></span>

## <span data-ttu-id="80fbe-105">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="80fbe-105">EXAMPLES</span></span>

### <span data-ttu-id="80fbe-106">1:</span><span class="sxs-lookup"><span data-stu-id="80fbe-106">1:</span></span>
```

```

## <span data-ttu-id="80fbe-107">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="80fbe-107">PARAMETERS</span></span>

### <span data-ttu-id="80fbe-108">-AsJob</span><span class="sxs-lookup"><span data-stu-id="80fbe-108">-AsJob</span></span>
<span data-ttu-id="80fbe-109">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="80fbe-109">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="80fbe-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80fbe-110">-DefaultProfile</span></span>
<span data-ttu-id="80fbe-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="80fbe-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="80fbe-112">-GatewayVip</span><span class="sxs-lookup"><span data-stu-id="80fbe-112">-GatewayVip</span></span>
<span data-ttu-id="80fbe-113">IP-адрес шлюза для сброса определенного экземпляра шлюза (например, в случае включения Active-Activeных шлюзов). По умолчанию основной экземпляр шлюза будет сброшен, если значение не передается.</span><span class="sxs-lookup"><span data-stu-id="80fbe-113">The gateway vip in order to reset particular gateway instance (e.g. in case of Active-Active feature enabled gateways.) By default, gateway primary instance will be reset if no value is passed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="80fbe-114">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="80fbe-114">-VirtualNetworkGateway</span></span>
```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="80fbe-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80fbe-115">CommonParameters</span></span>
<span data-ttu-id="80fbe-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="80fbe-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80fbe-117">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80fbe-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80fbe-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="80fbe-118">INPUTS</span></span>

### <span data-ttu-id="80fbe-119">Подстрок</span><span class="sxs-lookup"><span data-stu-id="80fbe-119">String</span></span>
<span data-ttu-id="80fbe-120">Параметр "GatewayVip" принимает значение типа String из конвейера.</span><span class="sxs-lookup"><span data-stu-id="80fbe-120">Parameter 'GatewayVip' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="80fbe-121">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="80fbe-121">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="80fbe-122">Параметр "VirtualNetworkGateway" принимает значение типа "PSVirtualNetworkGateway" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="80fbe-122">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="80fbe-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="80fbe-123">OUTPUTS</span></span>

### <span data-ttu-id="80fbe-124">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="80fbe-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="80fbe-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="80fbe-125">NOTES</span></span>

## <span data-ttu-id="80fbe-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="80fbe-126">RELATED LINKS</span></span>

[<span data-ttu-id="80fbe-127">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="80fbe-127">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="80fbe-128">New-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="80fbe-128">New-AzureRmVirtualNetworkGateway</span></span>](./New-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="80fbe-129">Remove-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="80fbe-129">Remove-AzureRmVirtualNetworkGateway</span></span>](./Remove-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="80fbe-130">Изменить размер — AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="80fbe-130">Resize-AzureRmVirtualNetworkGateway</span></span>](./Resize-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="80fbe-131">Set-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="80fbe-131">Set-AzureRmVirtualNetworkGateway</span></span>](./Set-AzureRmVirtualNetworkGateway.md)



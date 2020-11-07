---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 443F6492-EFA7-4417-943A-3A8D47F8C83C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Reset-AzureRmVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Reset-AzureRmVirtualNetworkGateway.md
ms.openlocfilehash: 2b2947ec86e928506624aea49b380db3c4f24bc0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734267"
---
# <span data-ttu-id="9e399-101">Reset-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9e399-101">Reset-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="9e399-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9e399-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9e399-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9e399-103">SYNTAX</span></span>

```
Reset-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewayVip <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9e399-104">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9e399-104">DESCRIPTION</span></span>

## <span data-ttu-id="9e399-105">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9e399-105">EXAMPLES</span></span>

## <span data-ttu-id="9e399-106">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9e399-106">PARAMETERS</span></span>

### <span data-ttu-id="9e399-107">-GatewayVip</span><span class="sxs-lookup"><span data-stu-id="9e399-107">-GatewayVip</span></span>
<span data-ttu-id="9e399-108">IP-адрес шлюза для сброса определенного экземпляра шлюза (например, в случае включения Active-Activeных шлюзов). По умолчанию основной экземпляр шлюза будет сброшен, если значение не передается.</span><span class="sxs-lookup"><span data-stu-id="9e399-108">The gateway vip in order to reset particular gateway instance (e.g. in case of Active-Active feature enabled gateways.) By default, gateway primary instance will be reset if no value is passed.</span></span>

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

### <span data-ttu-id="9e399-109">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9e399-109">-VirtualNetworkGateway</span></span>
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

### <span data-ttu-id="9e399-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e399-110">-DefaultProfile</span></span>
<span data-ttu-id="9e399-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9e399-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9e399-112">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e399-112">CommonParameters</span></span>
<span data-ttu-id="9e399-113">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9e399-113">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e399-114">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e399-114">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e399-115">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9e399-115">INPUTS</span></span>

### <span data-ttu-id="9e399-116">Подстрок</span><span class="sxs-lookup"><span data-stu-id="9e399-116">String</span></span>
<span data-ttu-id="9e399-117">Параметр "GatewayVip" принимает значение типа String из конвейера.</span><span class="sxs-lookup"><span data-stu-id="9e399-117">Parameter 'GatewayVip' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="9e399-118">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9e399-118">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="9e399-119">Параметр "VirtualNetworkGateway" принимает значение типа "PSVirtualNetworkGateway" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="9e399-119">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="9e399-120">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9e399-120">OUTPUTS</span></span>

### <span data-ttu-id="9e399-121">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9e399-121">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="9e399-122">Пуск</span><span class="sxs-lookup"><span data-stu-id="9e399-122">NOTES</span></span>

## <span data-ttu-id="9e399-123">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9e399-123">RELATED LINKS</span></span>

[<span data-ttu-id="9e399-124">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9e399-124">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="9e399-125">New-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9e399-125">New-AzureRmVirtualNetworkGateway</span></span>](./New-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="9e399-126">Remove-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9e399-126">Remove-AzureRmVirtualNetworkGateway</span></span>](./Remove-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="9e399-127">Изменить размер — AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9e399-127">Resize-AzureRmVirtualNetworkGateway</span></span>](./Resize-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="9e399-128">Set-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9e399-128">Set-AzureRmVirtualNetworkGateway</span></span>](./Set-AzureRmVirtualNetworkGateway.md)



---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 443F6492-EFA7-4417-943A-3A8D47F8C83C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/reset-azurermvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Reset-AzureRmVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Reset-AzureRmVirtualNetworkGateway.md
ms.openlocfilehash: 815f7d3fdc0f058f2abfce5687b129054814adab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734424"
---
# <span data-ttu-id="b243f-101">Reset-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b243f-101">Reset-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="b243f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b243f-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b243f-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b243f-103">SYNTAX</span></span>

```
Reset-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewayVip <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b243f-104">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b243f-104">DESCRIPTION</span></span>

## <span data-ttu-id="b243f-105">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b243f-105">EXAMPLES</span></span>

## <span data-ttu-id="b243f-106">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b243f-106">PARAMETERS</span></span>

### <span data-ttu-id="b243f-107">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b243f-107">-AsJob</span></span>
<span data-ttu-id="b243f-108">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="b243f-108">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b243f-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b243f-109">-DefaultProfile</span></span>
<span data-ttu-id="b243f-110">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b243f-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b243f-111">-GatewayVip</span><span class="sxs-lookup"><span data-stu-id="b243f-111">-GatewayVip</span></span>
<span data-ttu-id="b243f-112">IP-адрес шлюза для сброса определенного экземпляра шлюза (например, в случае включения Active-Activeных шлюзов). По умолчанию основной экземпляр шлюза будет сброшен, если значение не передается.</span><span class="sxs-lookup"><span data-stu-id="b243f-112">The gateway vip in order to reset particular gateway instance (e.g. in case of Active-Active feature enabled gateways.) By default, gateway primary instance will be reset if no value is passed.</span></span>

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

### <span data-ttu-id="b243f-113">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b243f-113">-VirtualNetworkGateway</span></span>
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

### <span data-ttu-id="b243f-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b243f-114">CommonParameters</span></span>
<span data-ttu-id="b243f-115">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b243f-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b243f-116">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b243f-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b243f-117">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b243f-117">INPUTS</span></span>

### <span data-ttu-id="b243f-118">Подстрок</span><span class="sxs-lookup"><span data-stu-id="b243f-118">String</span></span>
<span data-ttu-id="b243f-119">Параметр "GatewayVip" принимает значение типа String из конвейера.</span><span class="sxs-lookup"><span data-stu-id="b243f-119">Parameter 'GatewayVip' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="b243f-120">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b243f-120">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="b243f-121">Параметр "VirtualNetworkGateway" принимает значение типа "PSVirtualNetworkGateway" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="b243f-121">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="b243f-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b243f-122">OUTPUTS</span></span>

### <span data-ttu-id="b243f-123">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b243f-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="b243f-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="b243f-124">NOTES</span></span>

## <span data-ttu-id="b243f-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b243f-125">RELATED LINKS</span></span>

[<span data-ttu-id="b243f-126">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b243f-126">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="b243f-127">New-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b243f-127">New-AzureRmVirtualNetworkGateway</span></span>](./New-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="b243f-128">Remove-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b243f-128">Remove-AzureRmVirtualNetworkGateway</span></span>](./Remove-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="b243f-129">Изменить размер — AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b243f-129">Resize-AzureRmVirtualNetworkGateway</span></span>](./Resize-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="b243f-130">Set-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b243f-130">Set-AzureRmVirtualNetworkGateway</span></span>](./Set-AzureRmVirtualNetworkGateway.md)



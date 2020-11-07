---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 443F6492-EFA7-4417-943A-3A8D47F8C83C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/reset-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Reset-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Reset-AzVirtualNetworkGateway.md
ms.openlocfilehash: 53a4eb40d82a721c93102067c8c7e9fe0cbd86be
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911091"
---
# <span data-ttu-id="63ad3-101">Reset-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="63ad3-101">Reset-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="63ad3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="63ad3-102">SYNOPSIS</span></span>

## <span data-ttu-id="63ad3-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="63ad3-103">SYNTAX</span></span>

```
Reset-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewayVip <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="63ad3-104">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="63ad3-104">DESCRIPTION</span></span>

## <span data-ttu-id="63ad3-105">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="63ad3-105">EXAMPLES</span></span>

### <span data-ttu-id="63ad3-106">1:</span><span class="sxs-lookup"><span data-stu-id="63ad3-106">1:</span></span>
```

```

## <span data-ttu-id="63ad3-107">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="63ad3-107">PARAMETERS</span></span>

### <span data-ttu-id="63ad3-108">-AsJob</span><span class="sxs-lookup"><span data-stu-id="63ad3-108">-AsJob</span></span>
<span data-ttu-id="63ad3-109">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="63ad3-109">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="63ad3-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63ad3-110">-DefaultProfile</span></span>
<span data-ttu-id="63ad3-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="63ad3-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="63ad3-112">-GatewayVip</span><span class="sxs-lookup"><span data-stu-id="63ad3-112">-GatewayVip</span></span>
<span data-ttu-id="63ad3-113">IP-адрес шлюза для сброса определенного экземпляра шлюза (например, в случае включения Active-Activeных шлюзов). По умолчанию основной экземпляр шлюза будет сброшен, если значение не передается.</span><span class="sxs-lookup"><span data-stu-id="63ad3-113">The gateway vip in order to reset particular gateway instance (e.g. in case of Active-Active feature enabled gateways.) By default, gateway primary instance will be reset if no value is passed.</span></span>

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

### <span data-ttu-id="63ad3-114">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="63ad3-114">-VirtualNetworkGateway</span></span>
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

### <span data-ttu-id="63ad3-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63ad3-115">CommonParameters</span></span>
<span data-ttu-id="63ad3-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="63ad3-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63ad3-117">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63ad3-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63ad3-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="63ad3-118">INPUTS</span></span>

### <span data-ttu-id="63ad3-119">Подстрок</span><span class="sxs-lookup"><span data-stu-id="63ad3-119">String</span></span>
<span data-ttu-id="63ad3-120">Параметр "GatewayVip" принимает значение типа String из конвейера.</span><span class="sxs-lookup"><span data-stu-id="63ad3-120">Parameter 'GatewayVip' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="63ad3-121">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="63ad3-121">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="63ad3-122">Параметр "VirtualNetworkGateway" принимает значение типа "PSVirtualNetworkGateway" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="63ad3-122">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="63ad3-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="63ad3-123">OUTPUTS</span></span>

### <span data-ttu-id="63ad3-124">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="63ad3-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="63ad3-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="63ad3-125">NOTES</span></span>

## <span data-ttu-id="63ad3-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="63ad3-126">RELATED LINKS</span></span>

[<span data-ttu-id="63ad3-127">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="63ad3-127">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="63ad3-128">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="63ad3-128">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="63ad3-129">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="63ad3-129">Remove-AzVirtualNetworkGateway</span></span>](./Remove-AzVirtualNetworkGateway.md)

[<span data-ttu-id="63ad3-130">Изменить размер — AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="63ad3-130">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)

[<span data-ttu-id="63ad3-131">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="63ad3-131">Set-AzVirtualNetworkGateway</span></span>](./Set-AzVirtualNetworkGateway.md)



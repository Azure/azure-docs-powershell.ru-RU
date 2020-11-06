---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F8C1DF39-1DAF-4BDB-8B0E-1BC3B5E82185
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLocalNetworkGateway.md
ms.openlocfilehash: 8d2b3c6c15a48407b138fa26778bdf906b5a7a2d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562412"
---
# <span data-ttu-id="0a09a-101">Set-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="0a09a-101">Set-AzureRmLocalNetworkGateway</span></span>

## <span data-ttu-id="0a09a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0a09a-102">SYNOPSIS</span></span>
<span data-ttu-id="0a09a-103">Изменение шлюза локальной сети.</span><span class="sxs-lookup"><span data-stu-id="0a09a-103">Modifies a local network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0a09a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0a09a-104">SYNTAX</span></span>

```
Set-AzureRmLocalNetworkGateway -LocalNetworkGateway <PSLocalNetworkGateway>
 [-AddressPrefix <System.Collections.Generic.List`1[System.String]>] [-Asn <UInt32>]
 [-BgpPeeringAddress <String>] [-PeerWeight <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0a09a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0a09a-105">DESCRIPTION</span></span>
<span data-ttu-id="0a09a-106">Командлет **Set-AzureRmLocalNetworkGateway** изменяет шлюз локальной сети.</span><span class="sxs-lookup"><span data-stu-id="0a09a-106">The **Set-AzureRmLocalNetworkGateway** cmdlet modifies a local network gateway.</span></span>

## <span data-ttu-id="0a09a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0a09a-107">EXAMPLES</span></span>

## <span data-ttu-id="0a09a-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0a09a-108">PARAMETERS</span></span>

### <span data-ttu-id="0a09a-109">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="0a09a-109">-AddressPrefix</span></span>
```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a09a-110">-ASN</span><span class="sxs-lookup"><span data-stu-id="0a09a-110">-Asn</span></span>
```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a09a-111">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="0a09a-111">-BgpPeeringAddress</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a09a-112">-LocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="0a09a-112">-LocalNetworkGateway</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0a09a-113">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="0a09a-113">-PeerWeight</span></span>
```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a09a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a09a-114">-DefaultProfile</span></span>
<span data-ttu-id="0a09a-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0a09a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0a09a-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a09a-116">CommonParameters</span></span>
<span data-ttu-id="0a09a-117">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0a09a-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a09a-118">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a09a-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a09a-119">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0a09a-119">INPUTS</span></span>

### <span data-ttu-id="0a09a-120">PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="0a09a-120">PSLocalNetworkGateway</span></span>
<span data-ttu-id="0a09a-121">Параметр "LocalNetworkGateway" принимает значение типа "PSLocalNetworkGateway" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="0a09a-121">Parameter 'LocalNetworkGateway' accepts value of type 'PSLocalNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="0a09a-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0a09a-122">OUTPUTS</span></span>

### <span data-ttu-id="0a09a-123">Microsoft. Azure. Commands. Network. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="0a09a-123">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="0a09a-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="0a09a-124">NOTES</span></span>

## <span data-ttu-id="0a09a-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0a09a-125">RELATED LINKS</span></span>

[<span data-ttu-id="0a09a-126">Get-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="0a09a-126">Get-AzureRmLocalNetworkGateway</span></span>](./Get-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="0a09a-127">New-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="0a09a-127">New-AzureRmLocalNetworkGateway</span></span>](./New-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="0a09a-128">Remove-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="0a09a-128">Remove-AzureRmLocalNetworkGateway</span></span>](./Remove-AzureRmLocalNetworkGateway.md)



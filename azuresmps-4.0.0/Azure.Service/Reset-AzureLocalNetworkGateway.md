---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 0E4D44EE-BF28-46FE-B2FA-D35C1651016F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3940a5e6fc69ebee02f3e0de963bc87f790f8860
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075472"
---
# <span data-ttu-id="710ec-101">Reset-AzureLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="710ec-101">Reset-AzureLocalNetworkGateway</span></span>

## <span data-ttu-id="710ec-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="710ec-102">SYNOPSIS</span></span>
<span data-ttu-id="710ec-103">Сброс шлюза локальной сети.</span><span class="sxs-lookup"><span data-stu-id="710ec-103">Resets a local network gateway.</span></span>

## <span data-ttu-id="710ec-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="710ec-104">SYNTAX</span></span>

```
Reset-AzureLocalNetworkGateway -GatewayId <String>
 -AddressSpace <System.Collections.Generic.List`1[System.String]> [-Asn <UInt32>] [-BgpPeeringAddress <String>]
 [-PeerWeight <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="710ec-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="710ec-105">DESCRIPTION</span></span>
<span data-ttu-id="710ec-106">Командлет **Reset-AzureLocalNetworkGateway** сбрасывает шлюз локальной сети.</span><span class="sxs-lookup"><span data-stu-id="710ec-106">The **Reset-AzureLocalNetworkGateway** cmdlet resets a local network gateway.</span></span>

## <span data-ttu-id="710ec-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="710ec-107">EXAMPLES</span></span>

## <span data-ttu-id="710ec-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="710ec-108">PARAMETERS</span></span>

### <span data-ttu-id="710ec-109">-AddressSpace</span><span class="sxs-lookup"><span data-stu-id="710ec-109">-AddressSpace</span></span>
<span data-ttu-id="710ec-110">Указывает адресное пространство.</span><span class="sxs-lookup"><span data-stu-id="710ec-110">Specifies the address space.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="710ec-111">-ASN</span><span class="sxs-lookup"><span data-stu-id="710ec-111">-Asn</span></span>
<span data-ttu-id="710ec-112">Задает номер автономной системы (ASN).</span><span class="sxs-lookup"><span data-stu-id="710ec-112">Specifies the autonomous system number (ASN).</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="710ec-113">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="710ec-113">-BgpPeeringAddress</span></span>
<span data-ttu-id="710ec-114">Указывает адрес пиринга протокола пограничного шлюза (BGP).</span><span class="sxs-lookup"><span data-stu-id="710ec-114">Specifies the Border Gateway Protocol (BGP) peering address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="710ec-115">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="710ec-115">-GatewayId</span></span>
<span data-ttu-id="710ec-116">Указывает идентификатор шлюза.</span><span class="sxs-lookup"><span data-stu-id="710ec-116">Specifies the ID of the gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="710ec-117">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="710ec-117">-PeerWeight</span></span>
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="710ec-118">-Profile</span><span class="sxs-lookup"><span data-stu-id="710ec-118">-Profile</span></span>
<span data-ttu-id="710ec-119">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="710ec-119">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="710ec-120">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="710ec-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="710ec-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="710ec-121">CommonParameters</span></span>
<span data-ttu-id="710ec-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="710ec-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="710ec-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="710ec-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="710ec-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="710ec-124">INPUTS</span></span>

## <span data-ttu-id="710ec-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="710ec-125">OUTPUTS</span></span>

## <span data-ttu-id="710ec-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="710ec-126">NOTES</span></span>

## <span data-ttu-id="710ec-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="710ec-127">RELATED LINKS</span></span>

[<span data-ttu-id="710ec-128">Get-AzureLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="710ec-128">Get-AzureLocalNetworkGateway</span></span>](./Get-AzureLocalNetworkGateway.md)

[<span data-ttu-id="710ec-129">New-AzureLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="710ec-129">New-AzureLocalNetworkGateway</span></span>](./New-AzureLocalNetworkGateway.md)

[<span data-ttu-id="710ec-130">Remove-AzureLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="710ec-130">Remove-AzureLocalNetworkGateway</span></span>](./Remove-AzureLocalNetworkGateway.md)



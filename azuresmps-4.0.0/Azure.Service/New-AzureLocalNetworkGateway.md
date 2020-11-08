---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 9F9E4639-A557-4BD8-88C2-894F6C848C4A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4aa54a7bd236bb561b3de4b9c2a3c0a2710deb61
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076007"
---
# <span data-ttu-id="9456a-101">New-AzureLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9456a-101">New-AzureLocalNetworkGateway</span></span>

## <span data-ttu-id="9456a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9456a-102">SYNOPSIS</span></span>
<span data-ttu-id="9456a-103">Создание шлюза локальной сети Azure.</span><span class="sxs-lookup"><span data-stu-id="9456a-103">creates an Azure local network gateway.</span></span>

## <span data-ttu-id="9456a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9456a-104">SYNTAX</span></span>

```
New-AzureLocalNetworkGateway -GatewayName <String> -IpAddress <String>
 -AddressSpace <System.Collections.Generic.List`1[System.String]> [-Asn <UInt32>] [-BgpPeeringAddress <String>]
 [-PeerWeight <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="9456a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9456a-105">DESCRIPTION</span></span>
<span data-ttu-id="9456a-106">Командлет **New-AzureLocalNetworkGateway** создает шлюз локальной сети Azure.</span><span class="sxs-lookup"><span data-stu-id="9456a-106">The **New-AzureLocalNetworkGateway** cmdlet creates an Azure local network gateway.</span></span>

## <span data-ttu-id="9456a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9456a-107">EXAMPLES</span></span>

## <span data-ttu-id="9456a-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9456a-108">PARAMETERS</span></span>

### <span data-ttu-id="9456a-109">-AddressSpace</span><span class="sxs-lookup"><span data-stu-id="9456a-109">-AddressSpace</span></span>
<span data-ttu-id="9456a-110">Указывает адресное пространство.</span><span class="sxs-lookup"><span data-stu-id="9456a-110">Specifies the address space.</span></span>

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

### <span data-ttu-id="9456a-111">-ASN</span><span class="sxs-lookup"><span data-stu-id="9456a-111">-Asn</span></span>
<span data-ttu-id="9456a-112">Задает номер автономной системы (ASN).</span><span class="sxs-lookup"><span data-stu-id="9456a-112">Specifies the autonomous system number (ASN).</span></span>

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

### <span data-ttu-id="9456a-113">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="9456a-113">-BgpPeeringAddress</span></span>
<span data-ttu-id="9456a-114">Указывает адрес пиринга протокола пограничного шлюза (BGP).</span><span class="sxs-lookup"><span data-stu-id="9456a-114">Specifies the Border Gateway Protocol (BGP) peering address.</span></span>

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

### <span data-ttu-id="9456a-115">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="9456a-115">-GatewayName</span></span>
<span data-ttu-id="9456a-116">Указывает имя шлюза.</span><span class="sxs-lookup"><span data-stu-id="9456a-116">Specifies the name of the gateway.</span></span>

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

### <span data-ttu-id="9456a-117">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="9456a-117">-IpAddress</span></span>
<span data-ttu-id="9456a-118">Указывает IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="9456a-118">Specifies the IP address.</span></span>

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

### <span data-ttu-id="9456a-119">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="9456a-119">-PeerWeight</span></span>
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

### <span data-ttu-id="9456a-120">-Profile</span><span class="sxs-lookup"><span data-stu-id="9456a-120">-Profile</span></span>
<span data-ttu-id="9456a-121">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="9456a-121">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="9456a-122">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9456a-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9456a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9456a-123">CommonParameters</span></span>
<span data-ttu-id="9456a-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9456a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9456a-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9456a-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9456a-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9456a-126">INPUTS</span></span>

## <span data-ttu-id="9456a-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9456a-127">OUTPUTS</span></span>

## <span data-ttu-id="9456a-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="9456a-128">NOTES</span></span>

## <span data-ttu-id="9456a-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9456a-129">RELATED LINKS</span></span>

[<span data-ttu-id="9456a-130">Get-AzureLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9456a-130">Get-AzureLocalNetworkGateway</span></span>](./Get-AzureLocalNetworkGateway.md)

[<span data-ttu-id="9456a-131">Remove-AzureLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9456a-131">Remove-AzureLocalNetworkGateway</span></span>](./Remove-AzureLocalNetworkGateway.md)

[<span data-ttu-id="9456a-132">Сброс — AzureLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9456a-132">Reset-AzureLocalNetworkGateway</span></span>](./Reset-AzureLocalNetworkGateway.md)



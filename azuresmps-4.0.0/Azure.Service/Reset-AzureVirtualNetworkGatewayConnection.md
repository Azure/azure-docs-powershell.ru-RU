---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 09642B94-E888-4A22-9E8E-62109DB9394E
online version: ''
schema: 2.0.0
ms.openlocfilehash: f42a788f29f8546e6f402f1685f4c91aa3d7e5cb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076089"
---
# <span data-ttu-id="6dc79-101">Reset-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="6dc79-101">Reset-AzureVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="6dc79-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6dc79-102">SYNOPSIS</span></span>
<span data-ttu-id="6dc79-103">Сбрасывает подключение к шлюзу виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="6dc79-103">Resets a virtual network gateway connection.</span></span>

## <span data-ttu-id="6dc79-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6dc79-104">SYNTAX</span></span>

```
Reset-AzureVirtualNetworkGatewayConnection -GatewayId <String> -ConnectedEntityId <String>
 -RoutingWeight <Int32> [-SharedKey <String>] [-EnableBgp <Boolean>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="6dc79-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6dc79-105">DESCRIPTION</span></span>
<span data-ttu-id="6dc79-106">Командлет **Reset-AzureVirtualNetworkGatewayConnection** сбрасывает соединение с шлюзом виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="6dc79-106">The **Reset-AzureVirtualNetworkGatewayConnection** cmdlet resets a virtual network gateway connection.</span></span>

## <span data-ttu-id="6dc79-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6dc79-107">EXAMPLES</span></span>

## <span data-ttu-id="6dc79-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6dc79-108">PARAMETERS</span></span>

### <span data-ttu-id="6dc79-109">-ConnectedEntityId</span><span class="sxs-lookup"><span data-stu-id="6dc79-109">-ConnectedEntityId</span></span>
<span data-ttu-id="6dc79-110">Указывает идентификатор подключенной сущности.</span><span class="sxs-lookup"><span data-stu-id="6dc79-110">Specifies the ID of a connected entity.</span></span>

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

### <span data-ttu-id="6dc79-111">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="6dc79-111">-EnableBgp</span></span>
<span data-ttu-id="6dc79-112">Включает протокол пограничного шлюза (BGP).</span><span class="sxs-lookup"><span data-stu-id="6dc79-112">Enables Border Gateway Protocol (BGP).</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dc79-113">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="6dc79-113">-GatewayId</span></span>
<span data-ttu-id="6dc79-114">Указывает идентификатор шлюза.</span><span class="sxs-lookup"><span data-stu-id="6dc79-114">Specifies the ID of a gateway.</span></span>

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

### <span data-ttu-id="6dc79-115">-Profile</span><span class="sxs-lookup"><span data-stu-id="6dc79-115">-Profile</span></span>
<span data-ttu-id="6dc79-116">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="6dc79-116">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="6dc79-117">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6dc79-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6dc79-118">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="6dc79-118">-RoutingWeight</span></span>
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dc79-119">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="6dc79-119">-SharedKey</span></span>
<span data-ttu-id="6dc79-120">Указывает общий ключ.</span><span class="sxs-lookup"><span data-stu-id="6dc79-120">Specifies a shared key.</span></span>

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

### <span data-ttu-id="6dc79-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6dc79-121">CommonParameters</span></span>
<span data-ttu-id="6dc79-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6dc79-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6dc79-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6dc79-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6dc79-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6dc79-124">INPUTS</span></span>

## <span data-ttu-id="6dc79-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6dc79-125">OUTPUTS</span></span>

## <span data-ttu-id="6dc79-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="6dc79-126">NOTES</span></span>

## <span data-ttu-id="6dc79-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6dc79-127">RELATED LINKS</span></span>

[<span data-ttu-id="6dc79-128">Get-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="6dc79-128">Get-AzureVirtualNetworkGatewayConnection</span></span>](./Get-AzureVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="6dc79-129">New-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="6dc79-129">New-AzureVirtualNetworkGatewayConnection</span></span>](./New-AzureVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="6dc79-130">Remove-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="6dc79-130">Remove-AzureVirtualNetworkGatewayConnection</span></span>](./Remove-AzureVirtualNetworkGatewayConnection.md)



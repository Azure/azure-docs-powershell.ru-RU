---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: E3C0C3AA-3941-469E-A6CC-A92ADD7377B4
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2bf6824219879af52549d7815d65dcb502a2a752
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076185"
---
# <span data-ttu-id="2b0b2-101">New-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="2b0b2-101">New-AzureVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="2b0b2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2b0b2-102">SYNOPSIS</span></span>
<span data-ttu-id="2b0b2-103">Создает сетевое подключение к виртуальному шлюзу Azure.</span><span class="sxs-lookup"><span data-stu-id="2b0b2-103">Creates an Azure virtual gateway network connection.</span></span>

## <span data-ttu-id="2b0b2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2b0b2-104">SYNTAX</span></span>

```
New-AzureVirtualNetworkGatewayConnection -ConnectedEntityId <String> -GatewayConnectionName <String>
 -GatewayConnectionType <String> [-RoutingWeight <Int32>] [-SharedKey <String>]
 -VirtualNetworkGatewayId <String> [-EnableBgp <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="2b0b2-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2b0b2-105">DESCRIPTION</span></span>
<span data-ttu-id="2b0b2-106">Командлет **New-AzureVirtualNetworkGatewayConnection** создает сетевое подключение к виртуальному шлюзу Azure.</span><span class="sxs-lookup"><span data-stu-id="2b0b2-106">The **New-AzureVirtualNetworkGatewayConnection** cmdlet creates an Azure virtual gateway network connection.</span></span>

## <span data-ttu-id="2b0b2-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2b0b2-107">EXAMPLES</span></span>

## <span data-ttu-id="2b0b2-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2b0b2-108">PARAMETERS</span></span>

### <span data-ttu-id="2b0b2-109">-ConnectedEntityId</span><span class="sxs-lookup"><span data-stu-id="2b0b2-109">-ConnectedEntityId</span></span>
<span data-ttu-id="2b0b2-110">Указывает идентификатор подключенной сущности.</span><span class="sxs-lookup"><span data-stu-id="2b0b2-110">Specifies the ID of a connected entity.</span></span>

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

### <span data-ttu-id="2b0b2-111">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="2b0b2-111">-EnableBgp</span></span>
<span data-ttu-id="2b0b2-112">Включает протокол пограничного шлюза (BGP).</span><span class="sxs-lookup"><span data-stu-id="2b0b2-112">Enables Border Gateway Protocol (BGP).</span></span>

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

### <span data-ttu-id="2b0b2-113">-GatewayConnectionName</span><span class="sxs-lookup"><span data-stu-id="2b0b2-113">-GatewayConnectionName</span></span>
<span data-ttu-id="2b0b2-114">Задает имя для подключения к шлюзу.</span><span class="sxs-lookup"><span data-stu-id="2b0b2-114">Specifies a name for the gateway connection.</span></span>

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

### <span data-ttu-id="2b0b2-115">-GatewayConnectionType</span><span class="sxs-lookup"><span data-stu-id="2b0b2-115">-GatewayConnectionType</span></span>
<span data-ttu-id="2b0b2-116">Указывает тип подключения к шлюзу.</span><span class="sxs-lookup"><span data-stu-id="2b0b2-116">Specifies the type of gateway connection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b0b2-117">-Profile</span><span class="sxs-lookup"><span data-stu-id="2b0b2-117">-Profile</span></span>
<span data-ttu-id="2b0b2-118">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="2b0b2-118">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="2b0b2-119">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2b0b2-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2b0b2-120">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="2b0b2-120">-RoutingWeight</span></span>
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

### <span data-ttu-id="2b0b2-121">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="2b0b2-121">-SharedKey</span></span>
<span data-ttu-id="2b0b2-122">Указывает общий ключ.</span><span class="sxs-lookup"><span data-stu-id="2b0b2-122">Specifies a shared key.</span></span>

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

### <span data-ttu-id="2b0b2-123">-VirtualNetworkGatewayId</span><span class="sxs-lookup"><span data-stu-id="2b0b2-123">-VirtualNetworkGatewayId</span></span>
<span data-ttu-id="2b0b2-124">Указывает идентификатор шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="2b0b2-124">Specifies the ID of a virtual network gateway.</span></span>

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

### <span data-ttu-id="2b0b2-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b0b2-125">CommonParameters</span></span>
<span data-ttu-id="2b0b2-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2b0b2-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b0b2-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b0b2-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b0b2-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2b0b2-128">INPUTS</span></span>

## <span data-ttu-id="2b0b2-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2b0b2-129">OUTPUTS</span></span>

## <span data-ttu-id="2b0b2-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="2b0b2-130">NOTES</span></span>

## <span data-ttu-id="2b0b2-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2b0b2-131">RELATED LINKS</span></span>

[<span data-ttu-id="2b0b2-132">Get-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="2b0b2-132">Get-AzureVirtualNetworkGatewayConnection</span></span>](./Get-AzureVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="2b0b2-133">Remove-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="2b0b2-133">Remove-AzureVirtualNetworkGatewayConnection</span></span>](./Remove-AzureVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="2b0b2-134">Сброс — AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="2b0b2-134">Reset-AzureVirtualNetworkGatewayConnection</span></span>](./Reset-AzureVirtualNetworkGatewayConnection.md)



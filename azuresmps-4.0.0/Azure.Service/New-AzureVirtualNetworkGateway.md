---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: A40F3BBB-4DC6-452E-A939-ED610F541EB1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7797c916813c985802a0a2f63a5a43e033009a06
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076186"
---
# <span data-ttu-id="9ee8f-101">New-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9ee8f-101">New-AzureVirtualNetworkGateway</span></span>

## <span data-ttu-id="9ee8f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9ee8f-102">SYNOPSIS</span></span>
<span data-ttu-id="9ee8f-103">Создание шлюза виртуальной сети Azure.</span><span class="sxs-lookup"><span data-stu-id="9ee8f-103">Creates an Azure virtual network gateway.</span></span>

## <span data-ttu-id="9ee8f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9ee8f-104">SYNTAX</span></span>

```
New-AzureVirtualNetworkGateway -VNetName <String> -GatewayName <String> [-GatewayType <String>]
 [-GatewaySKU <String>] [-Location <String>] [-VnetId <String>] [-Asn <UInt32>] [-PeerWeight <Int32>] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="9ee8f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9ee8f-105">DESCRIPTION</span></span>
<span data-ttu-id="9ee8f-106">Командлет **New-AzureVirtualNetworkGateway** создает шлюз виртуальной сети Azure.</span><span class="sxs-lookup"><span data-stu-id="9ee8f-106">The **New-AzureVirtualNetworkGateway** cmdlet creates an Azure virtual network gateway.</span></span>

## <span data-ttu-id="9ee8f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9ee8f-107">EXAMPLES</span></span>

## <span data-ttu-id="9ee8f-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9ee8f-108">PARAMETERS</span></span>

### <span data-ttu-id="9ee8f-109">-ASN</span><span class="sxs-lookup"><span data-stu-id="9ee8f-109">-Asn</span></span>
<span data-ttu-id="9ee8f-110">Задает номер автономной системы (ASN).</span><span class="sxs-lookup"><span data-stu-id="9ee8f-110">Specifies the autonomous system number (ASN).</span></span>

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

### <span data-ttu-id="9ee8f-111">-Force</span><span class="sxs-lookup"><span data-stu-id="9ee8f-111">-Force</span></span>
<span data-ttu-id="9ee8f-112">Не подтверждать Создание шлюза виртуальной сети Azure</span><span class="sxs-lookup"><span data-stu-id="9ee8f-112">Do not confirm Azure Virtual Network Gateway Creation</span></span>

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

### <span data-ttu-id="9ee8f-113">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="9ee8f-113">-GatewayName</span></span>
<span data-ttu-id="9ee8f-114">Указывает имя шлюза.</span><span class="sxs-lookup"><span data-stu-id="9ee8f-114">Specifies the name of the gateway.</span></span>

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

### <span data-ttu-id="9ee8f-115">-GatewaySKU</span><span class="sxs-lookup"><span data-stu-id="9ee8f-115">-GatewaySKU</span></span>
<span data-ttu-id="9ee8f-116">Указывает SKU шлюза виртуальной сети, который создает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="9ee8f-116">Specifies the SKU of the virtual network gateway that this cmdlet creates.</span></span>
<span data-ttu-id="9ee8f-117">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="9ee8f-117">Valid values are:</span></span>

- <span data-ttu-id="9ee8f-118">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="9ee8f-118">Default</span></span>
- <span data-ttu-id="9ee8f-119">Стандартная</span><span class="sxs-lookup"><span data-stu-id="9ee8f-119">Standard</span></span>
- <span data-ttu-id="9ee8f-120">HighPerformance</span><span class="sxs-lookup"><span data-stu-id="9ee8f-120">HighPerformance</span></span>

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

### <span data-ttu-id="9ee8f-121">-GatewayType</span><span class="sxs-lookup"><span data-stu-id="9ee8f-121">-GatewayType</span></span>
<span data-ttu-id="9ee8f-122">Указывает тип шлюза.</span><span class="sxs-lookup"><span data-stu-id="9ee8f-122">Specifies the type of gateway.</span></span>

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

### <span data-ttu-id="9ee8f-123">-Location</span><span class="sxs-lookup"><span data-stu-id="9ee8f-123">-Location</span></span>
<span data-ttu-id="9ee8f-124">Задает расположение.</span><span class="sxs-lookup"><span data-stu-id="9ee8f-124">Specifies the location.</span></span>

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

### <span data-ttu-id="9ee8f-125">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="9ee8f-125">-PeerWeight</span></span>
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

### <span data-ttu-id="9ee8f-126">-Profile</span><span class="sxs-lookup"><span data-stu-id="9ee8f-126">-Profile</span></span>
<span data-ttu-id="9ee8f-127">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="9ee8f-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9ee8f-128">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9ee8f-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9ee8f-129">-VnetId</span><span class="sxs-lookup"><span data-stu-id="9ee8f-129">-VnetId</span></span>
<span data-ttu-id="9ee8f-130">Указывает идентификатор виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="9ee8f-130">Specifies the ID of a virtual network.</span></span>

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

### <span data-ttu-id="9ee8f-131">-VNetName</span><span class="sxs-lookup"><span data-stu-id="9ee8f-131">-VNetName</span></span>
<span data-ttu-id="9ee8f-132">Указывает виртуальную сеть.</span><span class="sxs-lookup"><span data-stu-id="9ee8f-132">Specifies a virtual network.</span></span>

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

### <span data-ttu-id="9ee8f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ee8f-133">CommonParameters</span></span>
<span data-ttu-id="9ee8f-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9ee8f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ee8f-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ee8f-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ee8f-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9ee8f-136">INPUTS</span></span>

## <span data-ttu-id="9ee8f-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9ee8f-137">OUTPUTS</span></span>

## <span data-ttu-id="9ee8f-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="9ee8f-138">NOTES</span></span>

## <span data-ttu-id="9ee8f-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9ee8f-139">RELATED LINKS</span></span>

[<span data-ttu-id="9ee8f-140">Get-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9ee8f-140">Get-AzureVirtualNetworkGateway</span></span>](./Get-AzureVirtualNetworkGateway.md)

[<span data-ttu-id="9ee8f-141">Remove-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9ee8f-141">Remove-AzureVirtualNetworkGateway</span></span>](./Remove-AzureVirtualNetworkGateway.md)

[<span data-ttu-id="9ee8f-142">Изменить размер — AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9ee8f-142">Resize-AzureVirtualNetworkGateway</span></span>](./Resize-AzureVirtualNetworkGateway.md)

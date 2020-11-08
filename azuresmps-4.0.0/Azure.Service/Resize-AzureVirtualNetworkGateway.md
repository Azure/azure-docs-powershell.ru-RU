---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: AD5F4D69-45AF-46FB-ADF0-59CEF9908EF7
online version: ''
schema: 2.0.0
ms.openlocfilehash: d63ac418d2dcee97afef9ae5f351fb2c1eebece0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076086"
---
# <span data-ttu-id="d08fd-101">Resize-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d08fd-101">Resize-AzureVirtualNetworkGateway</span></span>

## <span data-ttu-id="d08fd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d08fd-102">SYNOPSIS</span></span>
<span data-ttu-id="d08fd-103">Изменение размера шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="d08fd-103">Resizes a virtual network gateway.</span></span>

## <span data-ttu-id="d08fd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d08fd-104">SYNTAX</span></span>

```
Resize-AzureVirtualNetworkGateway -GatewayId <String> -GatewaySKU <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="d08fd-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d08fd-105">DESCRIPTION</span></span>
<span data-ttu-id="d08fd-106">Командлет Resize-AzureVirtualNetworkGateway изменяет размер шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="d08fd-106">The Resize-AzureVirtualNetworkGateway cmdlet resizes a virtual network gateway.</span></span>

## <span data-ttu-id="d08fd-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d08fd-107">EXAMPLES</span></span>

## <span data-ttu-id="d08fd-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d08fd-108">PARAMETERS</span></span>

### <span data-ttu-id="d08fd-109">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="d08fd-109">-GatewayId</span></span>
<span data-ttu-id="d08fd-110">Указывает идентификатор шлюза.</span><span class="sxs-lookup"><span data-stu-id="d08fd-110">Specifies the ID of a gateway.</span></span>

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

### <span data-ttu-id="d08fd-111">-GatewaySKU</span><span class="sxs-lookup"><span data-stu-id="d08fd-111">-GatewaySKU</span></span>
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

### <span data-ttu-id="d08fd-112">-Profile</span><span class="sxs-lookup"><span data-stu-id="d08fd-112">-Profile</span></span>
<span data-ttu-id="d08fd-113">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="d08fd-113">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="d08fd-114">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d08fd-114">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d08fd-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d08fd-115">CommonParameters</span></span>
<span data-ttu-id="d08fd-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d08fd-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d08fd-117">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d08fd-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d08fd-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d08fd-118">INPUTS</span></span>

## <span data-ttu-id="d08fd-119">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d08fd-119">OUTPUTS</span></span>

## <span data-ttu-id="d08fd-120">Пуск</span><span class="sxs-lookup"><span data-stu-id="d08fd-120">NOTES</span></span>

## <span data-ttu-id="d08fd-121">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d08fd-121">RELATED LINKS</span></span>

[<span data-ttu-id="d08fd-122">Get-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d08fd-122">Get-AzureVirtualNetworkGateway</span></span>](./Get-AzureVirtualNetworkGateway.md)

[<span data-ttu-id="d08fd-123">New-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d08fd-123">New-AzureVirtualNetworkGateway</span></span>](./New-AzureVirtualNetworkGateway.md)

[<span data-ttu-id="d08fd-124">Remove-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d08fd-124">Remove-AzureVirtualNetworkGateway</span></span>](./Remove-AzureVirtualNetworkGateway.md)

[<span data-ttu-id="d08fd-125">Сброс — AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d08fd-125">Reset-AzureVirtualNetworkGateway</span></span>](./Reset-AzureVirtualNetworkGateway.md)



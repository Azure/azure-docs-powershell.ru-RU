---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: CD735391-62A8-40EC-B2F1-9044DC0676CA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1cc46fb250a7bc76d05193ea231c81d61668e853
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076090"
---
# <span data-ttu-id="1d397-101">Reset-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1d397-101">Reset-AzureVirtualNetworkGateway</span></span>

## <span data-ttu-id="1d397-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1d397-102">SYNOPSIS</span></span>
<span data-ttu-id="1d397-103">Сброс шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="1d397-103">Resets a virtual network gateway.</span></span>

## <span data-ttu-id="1d397-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1d397-104">SYNTAX</span></span>

```
Reset-AzureVirtualNetworkGateway -GatewayId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="1d397-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1d397-105">DESCRIPTION</span></span>
<span data-ttu-id="1d397-106">Командлет **Reset-AzureVirtualNetworkGateway** сбрасывает шлюз виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="1d397-106">The **Reset-AzureVirtualNetworkGateway** cmdlet resets a virtual network gateway.</span></span>

## <span data-ttu-id="1d397-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1d397-107">EXAMPLES</span></span>

## <span data-ttu-id="1d397-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1d397-108">PARAMETERS</span></span>

### <span data-ttu-id="1d397-109">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="1d397-109">-GatewayId</span></span>
<span data-ttu-id="1d397-110">Указывает идентификатор шлюза.</span><span class="sxs-lookup"><span data-stu-id="1d397-110">Specifies the ID of a gateway.</span></span>

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

### <span data-ttu-id="1d397-111">-Profile</span><span class="sxs-lookup"><span data-stu-id="1d397-111">-Profile</span></span>
<span data-ttu-id="1d397-112">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="1d397-112">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="1d397-113">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1d397-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1d397-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d397-114">CommonParameters</span></span>
<span data-ttu-id="1d397-115">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1d397-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d397-116">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d397-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d397-117">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1d397-117">INPUTS</span></span>

## <span data-ttu-id="1d397-118">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1d397-118">OUTPUTS</span></span>

## <span data-ttu-id="1d397-119">Пуск</span><span class="sxs-lookup"><span data-stu-id="1d397-119">NOTES</span></span>

## <span data-ttu-id="1d397-120">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1d397-120">RELATED LINKS</span></span>

[<span data-ttu-id="1d397-121">Get-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1d397-121">Get-AzureVirtualNetworkGateway</span></span>](./Get-AzureVirtualNetworkGateway.md)

[<span data-ttu-id="1d397-122">New-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1d397-122">New-AzureVirtualNetworkGateway</span></span>](./New-AzureVirtualNetworkGateway.md)

[<span data-ttu-id="1d397-123">Remove-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1d397-123">Remove-AzureVirtualNetworkGateway</span></span>](./Remove-AzureVirtualNetworkGateway.md)

[<span data-ttu-id="1d397-124">Изменить размер — AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1d397-124">Resize-AzureVirtualNetworkGateway</span></span>](./Resize-AzureVirtualNetworkGateway.md)



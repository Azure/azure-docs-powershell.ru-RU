---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 8099942A-B6EB-4C01-9F57-378B0EB7B3C9
online version: ''
schema: 2.0.0
ms.openlocfilehash: 67c933b716095392a215543cfc61d334cd347835
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075437"
---
# <span data-ttu-id="9dda1-101">Set-AzureVirtualNetworkGatewayKey</span><span class="sxs-lookup"><span data-stu-id="9dda1-101">Set-AzureVirtualNetworkGatewayKey</span></span>

## <span data-ttu-id="9dda1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9dda1-102">SYNOPSIS</span></span>
<span data-ttu-id="9dda1-103">Задает ключ для шлюза виртуальной сети Azure.</span><span class="sxs-lookup"><span data-stu-id="9dda1-103">Sets the key for an Azure virtual network gateway.</span></span>

## <span data-ttu-id="9dda1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9dda1-104">SYNTAX</span></span>

```
Set-AzureVirtualNetworkGatewayKey -GatewayId <String> -ConnectedEntityId <String> -SharedKey <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="9dda1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9dda1-105">DESCRIPTION</span></span>
<span data-ttu-id="9dda1-106">Командлет **Set-AzureVirtualNetworkGatewayKey** задает ключ для шлюза виртуальной сети Azure.</span><span class="sxs-lookup"><span data-stu-id="9dda1-106">The **Set-AzureVirtualNetworkGatewayKey** cmdlet sets the key for an Azure virtual network gateway.</span></span>

## <span data-ttu-id="9dda1-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9dda1-107">EXAMPLES</span></span>

## <span data-ttu-id="9dda1-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9dda1-108">PARAMETERS</span></span>

### <span data-ttu-id="9dda1-109">-ConnectedEntityId</span><span class="sxs-lookup"><span data-stu-id="9dda1-109">-ConnectedEntityId</span></span>
<span data-ttu-id="9dda1-110">Указывает идентификатор подключенной сущности.</span><span class="sxs-lookup"><span data-stu-id="9dda1-110">Specifies the ID of a connected entity.</span></span>

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

### <span data-ttu-id="9dda1-111">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="9dda1-111">-GatewayId</span></span>
<span data-ttu-id="9dda1-112">Указывает идентификатор шлюза.</span><span class="sxs-lookup"><span data-stu-id="9dda1-112">Specifies the ID of a gateway.</span></span>

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

### <span data-ttu-id="9dda1-113">-Profile</span><span class="sxs-lookup"><span data-stu-id="9dda1-113">-Profile</span></span>
<span data-ttu-id="9dda1-114">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="9dda1-114">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="9dda1-115">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9dda1-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9dda1-116">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="9dda1-116">-SharedKey</span></span>
<span data-ttu-id="9dda1-117">Указывает общий ключ.</span><span class="sxs-lookup"><span data-stu-id="9dda1-117">Specifies a shared key.</span></span>

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

### <span data-ttu-id="9dda1-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9dda1-118">CommonParameters</span></span>
<span data-ttu-id="9dda1-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9dda1-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9dda1-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9dda1-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9dda1-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9dda1-121">INPUTS</span></span>

## <span data-ttu-id="9dda1-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9dda1-122">OUTPUTS</span></span>

## <span data-ttu-id="9dda1-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="9dda1-123">NOTES</span></span>

## <span data-ttu-id="9dda1-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9dda1-124">RELATED LINKS</span></span>

[<span data-ttu-id="9dda1-125">Get-AzureVirtualNetworkGatewayKey</span><span class="sxs-lookup"><span data-stu-id="9dda1-125">Get-AzureVirtualNetworkGatewayKey</span></span>](./Get-AzureVirtualNetworkGatewayKey.md)

[<span data-ttu-id="9dda1-126">Сброс — AzureVirtualNetworkGatewayKey</span><span class="sxs-lookup"><span data-stu-id="9dda1-126">Reset-AzureVirtualNetworkGatewayKey</span></span>](./Reset-AzureVirtualNetworkGatewayKey.md)



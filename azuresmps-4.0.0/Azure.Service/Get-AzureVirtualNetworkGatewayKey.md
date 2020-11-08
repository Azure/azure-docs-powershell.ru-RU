---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 5F016D72-80EB-462D-9646-25EC4E33293E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 485b29130fd4b54c378f3ec19389b6c24ba86c63
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076513"
---
# <span data-ttu-id="09e6d-101">Get-AzureVirtualNetworkGatewayKey</span><span class="sxs-lookup"><span data-stu-id="09e6d-101">Get-AzureVirtualNetworkGatewayKey</span></span>

## <span data-ttu-id="09e6d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="09e6d-102">SYNOPSIS</span></span>
<span data-ttu-id="09e6d-103">Получает ключ для шлюза виртуальной сети Azure.</span><span class="sxs-lookup"><span data-stu-id="09e6d-103">Gets the key for an Azure virtual network gateway.</span></span>

## <span data-ttu-id="09e6d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="09e6d-104">SYNTAX</span></span>

```
Get-AzureVirtualNetworkGatewayKey -GatewayId <String> -ConnectedEntityId <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="09e6d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="09e6d-105">DESCRIPTION</span></span>
<span data-ttu-id="09e6d-106">Командлет **Get-AzureVirtualNetworkGatewayKey** получает ключ для шлюза виртуальной сети Azure.</span><span class="sxs-lookup"><span data-stu-id="09e6d-106">The **Get-AzureVirtualNetworkGatewayKey** cmdlet gets the key for an Azure virtual network gateway.</span></span>

## <span data-ttu-id="09e6d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="09e6d-107">EXAMPLES</span></span>

## <span data-ttu-id="09e6d-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="09e6d-108">PARAMETERS</span></span>

### <span data-ttu-id="09e6d-109">-ConnectedEntityId</span><span class="sxs-lookup"><span data-stu-id="09e6d-109">-ConnectedEntityId</span></span>
<span data-ttu-id="09e6d-110">Указывает идентификатор подключенной сущности.</span><span class="sxs-lookup"><span data-stu-id="09e6d-110">Specifies the ID of a connected entity.</span></span>

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

### <span data-ttu-id="09e6d-111">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="09e6d-111">-GatewayId</span></span>
<span data-ttu-id="09e6d-112">Указывает идентификатор шлюза.</span><span class="sxs-lookup"><span data-stu-id="09e6d-112">Specifies the ID of a gateway.</span></span>

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

### <span data-ttu-id="09e6d-113">-Profile</span><span class="sxs-lookup"><span data-stu-id="09e6d-113">-Profile</span></span>
<span data-ttu-id="09e6d-114">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="09e6d-114">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="09e6d-115">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="09e6d-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="09e6d-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09e6d-116">CommonParameters</span></span>
<span data-ttu-id="09e6d-117">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="09e6d-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09e6d-118">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09e6d-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09e6d-119">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="09e6d-119">INPUTS</span></span>

## <span data-ttu-id="09e6d-120">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="09e6d-120">OUTPUTS</span></span>

## <span data-ttu-id="09e6d-121">Пуск</span><span class="sxs-lookup"><span data-stu-id="09e6d-121">NOTES</span></span>

## <span data-ttu-id="09e6d-122">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="09e6d-122">RELATED LINKS</span></span>

[<span data-ttu-id="09e6d-123">Сброс — AzureVirtualNetworkGatewayKey</span><span class="sxs-lookup"><span data-stu-id="09e6d-123">Reset-AzureVirtualNetworkGatewayKey</span></span>](./Reset-AzureVirtualNetworkGatewayKey.md)

[<span data-ttu-id="09e6d-124">Set-AzureVirtualNetworkGatewayKey</span><span class="sxs-lookup"><span data-stu-id="09e6d-124">Set-AzureVirtualNetworkGatewayKey</span></span>](./Set-AzureVirtualNetworkGatewayKey.md)



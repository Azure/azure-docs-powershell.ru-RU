---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 425008DB-9761-42F1-8D6D-F35757A3CA6C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 37aa0718c4faa637b16ccde61f5e5b241bb9aa92
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076515"
---
# <span data-ttu-id="3ae48-101">Get-AzureVirtualNetworkGatewayIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="3ae48-101">Get-AzureVirtualNetworkGatewayIPsecParameters</span></span>

## <span data-ttu-id="3ae48-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3ae48-102">SYNOPSIS</span></span>
<span data-ttu-id="3ae48-103">Получает параметры IPsec для шлюза виртуальной сети Azure.</span><span class="sxs-lookup"><span data-stu-id="3ae48-103">Gets the IPsec parameters for an Azure virtual network gateway.</span></span>

## <span data-ttu-id="3ae48-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3ae48-104">SYNTAX</span></span>

```
Get-AzureVirtualNetworkGatewayIPsecParameters -GatewayId <String> -ConnectedEntityId <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="3ae48-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3ae48-105">DESCRIPTION</span></span>
<span data-ttu-id="3ae48-106">Командлет **Get-AzureVirtualNetworkGatewayIPsecParameters** получает параметры IPsec для шлюза виртуальной сети Azure.</span><span class="sxs-lookup"><span data-stu-id="3ae48-106">The **Get-AzureVirtualNetworkGatewayIPsecParameters** cmdlet gets the IPsec parameters for an Azure virtual network gateway.</span></span>

## <span data-ttu-id="3ae48-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3ae48-107">EXAMPLES</span></span>

## <span data-ttu-id="3ae48-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3ae48-108">PARAMETERS</span></span>

### <span data-ttu-id="3ae48-109">-ConnectedEntityId</span><span class="sxs-lookup"><span data-stu-id="3ae48-109">-ConnectedEntityId</span></span>
<span data-ttu-id="3ae48-110">Указывает идентификатор подключенного entitiy.</span><span class="sxs-lookup"><span data-stu-id="3ae48-110">Specifies the ID of a connected entitiy.</span></span>

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

### <span data-ttu-id="3ae48-111">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="3ae48-111">-GatewayId</span></span>
<span data-ttu-id="3ae48-112">Указывает идентификатор шлюза.</span><span class="sxs-lookup"><span data-stu-id="3ae48-112">Specifies the ID of a gateway.</span></span>

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

### <span data-ttu-id="3ae48-113">-Profile</span><span class="sxs-lookup"><span data-stu-id="3ae48-113">-Profile</span></span>
<span data-ttu-id="3ae48-114">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="3ae48-114">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="3ae48-115">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3ae48-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3ae48-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ae48-116">CommonParameters</span></span>
<span data-ttu-id="3ae48-117">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3ae48-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ae48-118">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ae48-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ae48-119">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3ae48-119">INPUTS</span></span>

## <span data-ttu-id="3ae48-120">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3ae48-120">OUTPUTS</span></span>

## <span data-ttu-id="3ae48-121">Пуск</span><span class="sxs-lookup"><span data-stu-id="3ae48-121">NOTES</span></span>

## <span data-ttu-id="3ae48-122">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3ae48-122">RELATED LINKS</span></span>

[<span data-ttu-id="3ae48-123">Set-AzureVirtualNetworkGatewayIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="3ae48-123">Set-AzureVirtualNetworkGatewayIPsecParameters</span></span>](./Set-AzureVirtualNetworkGatewayIPsecParameters.md)



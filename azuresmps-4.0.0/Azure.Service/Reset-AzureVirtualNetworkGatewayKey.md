---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 4F1E69B8-15FB-495F-B910-04E450D3215F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8a5b53f909b840a761d40f79a311fb61b7e2337b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076088"
---
# <span data-ttu-id="3e67b-101">Reset-AzureVirtualNetworkGatewayKey</span><span class="sxs-lookup"><span data-stu-id="3e67b-101">Reset-AzureVirtualNetworkGatewayKey</span></span>

## <span data-ttu-id="3e67b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3e67b-102">SYNOPSIS</span></span>
<span data-ttu-id="3e67b-103">Сброс ключа шлюза виртуальных сетей.</span><span class="sxs-lookup"><span data-stu-id="3e67b-103">Resets a virtual network gateway key.</span></span>

## <span data-ttu-id="3e67b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3e67b-104">SYNTAX</span></span>

```
Reset-AzureVirtualNetworkGatewayKey -GatewayId <String> -ConnectedEntityId <String> -keyLength <Int32>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="3e67b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3e67b-105">DESCRIPTION</span></span>
<span data-ttu-id="3e67b-106">Командлет **Reset-AzureVirtualNetworkGatewayKey** сбрасывает ключ шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="3e67b-106">The **Reset-AzureVirtualNetworkGatewayKey** cmdlet resets a virtual network gateway key.</span></span>

## <span data-ttu-id="3e67b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3e67b-107">EXAMPLES</span></span>

## <span data-ttu-id="3e67b-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3e67b-108">PARAMETERS</span></span>

### <span data-ttu-id="3e67b-109">-ConnectedEntityId</span><span class="sxs-lookup"><span data-stu-id="3e67b-109">-ConnectedEntityId</span></span>
<span data-ttu-id="3e67b-110">Указывает идентификатор подключенной сущности.</span><span class="sxs-lookup"><span data-stu-id="3e67b-110">Specifies the ID of a connected entity.</span></span>

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

### <span data-ttu-id="3e67b-111">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="3e67b-111">-GatewayId</span></span>
<span data-ttu-id="3e67b-112">Указывает идентификатор шлюза.</span><span class="sxs-lookup"><span data-stu-id="3e67b-112">Specifies the ID of a gateway.</span></span>

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

### <span data-ttu-id="3e67b-113">-keyLength</span><span class="sxs-lookup"><span data-stu-id="3e67b-113">-keyLength</span></span>
<span data-ttu-id="3e67b-114">Задает длину ключа.</span><span class="sxs-lookup"><span data-stu-id="3e67b-114">Specifies the key length.</span></span>

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

### <span data-ttu-id="3e67b-115">-Profile</span><span class="sxs-lookup"><span data-stu-id="3e67b-115">-Profile</span></span>
<span data-ttu-id="3e67b-116">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="3e67b-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3e67b-117">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3e67b-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3e67b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e67b-118">CommonParameters</span></span>
<span data-ttu-id="3e67b-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3e67b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e67b-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e67b-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e67b-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3e67b-121">INPUTS</span></span>

## <span data-ttu-id="3e67b-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3e67b-122">OUTPUTS</span></span>

## <span data-ttu-id="3e67b-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="3e67b-123">NOTES</span></span>

## <span data-ttu-id="3e67b-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3e67b-124">RELATED LINKS</span></span>

[<span data-ttu-id="3e67b-125">Get-AzureVirtualNetworkGatewayKey</span><span class="sxs-lookup"><span data-stu-id="3e67b-125">Get-AzureVirtualNetworkGatewayKey</span></span>](./Get-AzureVirtualNetworkGatewayKey.md)

[<span data-ttu-id="3e67b-126">Set-AzureVirtualNetworkGatewayKey</span><span class="sxs-lookup"><span data-stu-id="3e67b-126">Set-AzureVirtualNetworkGatewayKey</span></span>](./Set-AzureVirtualNetworkGatewayKey.md)

---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 88AB3621-7C80-41BA-BE49-4F8F9C46BCF5
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1fb0fa13cb5ea155b945505fd3f99c28494c5dc0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076523"
---
# <span data-ttu-id="b29ab-101">Get-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="b29ab-101">Get-AzureVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="b29ab-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b29ab-102">SYNOPSIS</span></span>
<span data-ttu-id="b29ab-103">Возвращает подключение к шлюзу виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="b29ab-103">Gets a virtual network gateway connection.</span></span>

## <span data-ttu-id="b29ab-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b29ab-104">SYNTAX</span></span>

```
Get-AzureVirtualNetworkGatewayConnection [-GatewayId <String>] [-ConnectedEntityId <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b29ab-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b29ab-105">DESCRIPTION</span></span>
<span data-ttu-id="b29ab-106">Командлет **Get-AzureVirtualNetworkGatewayConnection** получает подключение к шлюзу виртуальной сети Azure.</span><span class="sxs-lookup"><span data-stu-id="b29ab-106">The **Get-AzureVirtualNetworkGatewayConnection** cmdlet gets an Azure virtual network gateway connection.</span></span>

## <span data-ttu-id="b29ab-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b29ab-107">EXAMPLES</span></span>

## <span data-ttu-id="b29ab-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b29ab-108">PARAMETERS</span></span>

### <span data-ttu-id="b29ab-109">-ConnectedEntityId</span><span class="sxs-lookup"><span data-stu-id="b29ab-109">-ConnectedEntityId</span></span>
<span data-ttu-id="b29ab-110">Указывает идентификатор подключенной сущности.</span><span class="sxs-lookup"><span data-stu-id="b29ab-110">Specifies the ID of a connected entity.</span></span>

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

### <span data-ttu-id="b29ab-111">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="b29ab-111">-GatewayId</span></span>
<span data-ttu-id="b29ab-112">Указывает идентификатор шлюза.</span><span class="sxs-lookup"><span data-stu-id="b29ab-112">Specifies the ID of the gateway.</span></span>

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

### <span data-ttu-id="b29ab-113">-Profile</span><span class="sxs-lookup"><span data-stu-id="b29ab-113">-Profile</span></span>
<span data-ttu-id="b29ab-114">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="b29ab-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b29ab-115">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b29ab-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b29ab-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b29ab-116">CommonParameters</span></span>
<span data-ttu-id="b29ab-117">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b29ab-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b29ab-118">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b29ab-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b29ab-119">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b29ab-119">INPUTS</span></span>

## <span data-ttu-id="b29ab-120">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b29ab-120">OUTPUTS</span></span>

## <span data-ttu-id="b29ab-121">Пуск</span><span class="sxs-lookup"><span data-stu-id="b29ab-121">NOTES</span></span>

## <span data-ttu-id="b29ab-122">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b29ab-122">RELATED LINKS</span></span>

[<span data-ttu-id="b29ab-123">New-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="b29ab-123">New-AzureVirtualNetworkGatewayConnection</span></span>](./New-AzureVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="b29ab-124">Remove-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="b29ab-124">Remove-AzureVirtualNetworkGatewayConnection</span></span>](./Remove-AzureVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="b29ab-125">Сброс — AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="b29ab-125">Reset-AzureVirtualNetworkGatewayConnection</span></span>](./Reset-AzureVirtualNetworkGatewayConnection.md)

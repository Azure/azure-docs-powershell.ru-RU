---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: F3D44471-50F0-4737-9AF5-3DE7222EAF9D
online version: ''
schema: 2.0.0
ms.openlocfilehash: b9aa386b47c02ed945cad63c00425534d68e66f0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075485"
---
# <span data-ttu-id="d5888-101">Remove-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="d5888-101">Remove-AzureVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="d5888-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d5888-102">SYNOPSIS</span></span>
<span data-ttu-id="d5888-103">Удаляет подключение к шлюзу виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="d5888-103">Removes a virtual network gateway connection.</span></span>

## <span data-ttu-id="d5888-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d5888-104">SYNTAX</span></span>

```
Remove-AzureVirtualNetworkGatewayConnection -GatewayId <String> -ConnectedEntityId <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d5888-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d5888-105">DESCRIPTION</span></span>
<span data-ttu-id="d5888-106">Командлет **Remove-AzureVirtualNetworkGatewayConnection** удаляет подключение к шлюзу виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="d5888-106">The **Remove-AzureVirtualNetworkGatewayConnection** cmdlet removes a virtual network gateway connection.</span></span>

## <span data-ttu-id="d5888-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d5888-107">EXAMPLES</span></span>

## <span data-ttu-id="d5888-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d5888-108">PARAMETERS</span></span>

### <span data-ttu-id="d5888-109">-ConnectedEntityId</span><span class="sxs-lookup"><span data-stu-id="d5888-109">-ConnectedEntityId</span></span>
<span data-ttu-id="d5888-110">Указывает идентификатор подключенной сущности.</span><span class="sxs-lookup"><span data-stu-id="d5888-110">Specifies the ID of a connected entity.</span></span>

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

### <span data-ttu-id="d5888-111">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="d5888-111">-GatewayId</span></span>
<span data-ttu-id="d5888-112">Указывает идентификатор шлюза.</span><span class="sxs-lookup"><span data-stu-id="d5888-112">Specifies the ID of a gateway.</span></span>

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

### <span data-ttu-id="d5888-113">-Profile</span><span class="sxs-lookup"><span data-stu-id="d5888-113">-Profile</span></span>
<span data-ttu-id="d5888-114">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="d5888-114">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="d5888-115">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d5888-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d5888-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5888-116">CommonParameters</span></span>
<span data-ttu-id="d5888-117">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d5888-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5888-118">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5888-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5888-119">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d5888-119">INPUTS</span></span>

## <span data-ttu-id="d5888-120">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d5888-120">OUTPUTS</span></span>

## <span data-ttu-id="d5888-121">Пуск</span><span class="sxs-lookup"><span data-stu-id="d5888-121">NOTES</span></span>

## <span data-ttu-id="d5888-122">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d5888-122">RELATED LINKS</span></span>

[<span data-ttu-id="d5888-123">Get-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="d5888-123">Get-AzureVirtualNetworkGatewayConnection</span></span>](./Get-AzureVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="d5888-124">New-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="d5888-124">New-AzureVirtualNetworkGatewayConnection</span></span>](./New-AzureVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="d5888-125">Сброс — AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="d5888-125">Reset-AzureVirtualNetworkGatewayConnection</span></span>](./Reset-AzureVirtualNetworkGatewayConnection.md)



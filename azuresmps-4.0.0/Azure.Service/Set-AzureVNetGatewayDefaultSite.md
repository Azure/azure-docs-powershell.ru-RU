---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: A34A2B01-A658-410E-8B68-98A6427DFC33
online version: ''
schema: 2.0.0
ms.openlocfilehash: 345d9048ea729b6fe954d2da5e01310be42c79ef
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076413"
---
# <span data-ttu-id="0915d-101">Set-AzureVNetGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="0915d-101">Set-AzureVNetGatewayDefaultSite</span></span>

## <span data-ttu-id="0915d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0915d-102">SYNOPSIS</span></span>
<span data-ttu-id="0915d-103">Задает сайт по умолчанию для трафика принудительного туннелирования.</span><span class="sxs-lookup"><span data-stu-id="0915d-103">Sets the default site for forced tunneling traffic.</span></span>

## <span data-ttu-id="0915d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0915d-104">SYNTAX</span></span>

```
Set-AzureVNetGatewayDefaultSite -VNetName <String> -DefaultSite <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="0915d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0915d-105">DESCRIPTION</span></span>
<span data-ttu-id="0915d-106">Командлет **Set-AzureVNetGatewayDefaultSite** задает маршрут по умолчанию для локального сайта для принудительного туннелирования трафика.</span><span class="sxs-lookup"><span data-stu-id="0915d-106">The **Set-AzureVNetGatewayDefaultSite** cmdlet sets the default route to the on-premises site for forced tunneling traffic.</span></span>
<span data-ttu-id="0915d-107">Эта команда задает маршрут для виртуальной сети с помощью VPN-шлюза виртуальной частной сети Azure.</span><span class="sxs-lookup"><span data-stu-id="0915d-107">This command sets the route on an Azure virtual private network (VPN) gateway for a virtual network.</span></span>

## <span data-ttu-id="0915d-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0915d-108">EXAMPLES</span></span>

## <span data-ttu-id="0915d-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0915d-109">PARAMETERS</span></span>

### <span data-ttu-id="0915d-110">-DefaultSite</span><span class="sxs-lookup"><span data-stu-id="0915d-110">-DefaultSite</span></span>
<span data-ttu-id="0915d-111">Задает имя локального сайта локальной сети для принудительного туннелирования трафика.</span><span class="sxs-lookup"><span data-stu-id="0915d-111">Specifies the name of the on-premises local network site for forced tunneling traffic.</span></span>

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

### <span data-ttu-id="0915d-112">-Profile</span><span class="sxs-lookup"><span data-stu-id="0915d-112">-Profile</span></span>
<span data-ttu-id="0915d-113">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="0915d-113">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0915d-114">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0915d-114">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0915d-115">-VNetName</span><span class="sxs-lookup"><span data-stu-id="0915d-115">-VNetName</span></span>
<span data-ttu-id="0915d-116">Указывает виртуальную сеть.</span><span class="sxs-lookup"><span data-stu-id="0915d-116">Specifies a virtual network.</span></span>
<span data-ttu-id="0915d-117">Этот командлет задает маршрут по умолчанию VPN-шлюза для принудительного туннелирования трафика для виртуальной сети, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="0915d-117">This cmdlet sets the default route of the VPN gateway for forced tunneling traffic for the virtual network that this parameter specifies.</span></span>

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

### <span data-ttu-id="0915d-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0915d-118">CommonParameters</span></span>
<span data-ttu-id="0915d-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0915d-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0915d-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0915d-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0915d-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0915d-121">INPUTS</span></span>

## <span data-ttu-id="0915d-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0915d-122">OUTPUTS</span></span>

## <span data-ttu-id="0915d-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="0915d-123">NOTES</span></span>

## <span data-ttu-id="0915d-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0915d-124">RELATED LINKS</span></span>

[<span data-ttu-id="0915d-125">Remove-AzureVNetGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="0915d-125">Remove-AzureVNetGatewayDefaultSite</span></span>](./Remove-AzureVNetGatewayDefaultSite.md)

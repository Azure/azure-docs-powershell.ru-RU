---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 67260128-D57B-4587-BB61-2475703ABA66
online version: ''
schema: 2.0.0
ms.openlocfilehash: 38aca36799c57dd5a135af99e4b99ab713d2b1ca
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075489"
---
# <span data-ttu-id="101e5-101">Remove-AzureVNetGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="101e5-101">Remove-AzureVNetGatewayDefaultSite</span></span>

## <span data-ttu-id="101e5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="101e5-102">SYNOPSIS</span></span>
<span data-ttu-id="101e5-103">Удаляет маршрут по умолчанию для трафика принудительного туннелирования.</span><span class="sxs-lookup"><span data-stu-id="101e5-103">Removes the default route for forced tunneling traffic.</span></span>

## <span data-ttu-id="101e5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="101e5-104">SYNTAX</span></span>

```
Remove-AzureVNetGatewayDefaultSite -VNetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="101e5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="101e5-105">DESCRIPTION</span></span>
<span data-ttu-id="101e5-106">Командлет **Remove-AzureVNetGatewayDefaultSite** удаляет маршрут по умолчанию для локального сайта для принудительного туннелирования трафика.</span><span class="sxs-lookup"><span data-stu-id="101e5-106">The **Remove-AzureVNetGatewayDefaultSite** cmdlet removes the default route to the on-premises site for forced tunneling traffic.</span></span>
<span data-ttu-id="101e5-107">Этот командлет удаляет маршрут из шлюза виртуальной частной сети Azure (VPN) для виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="101e5-107">This cmdlet removes the route from an Azure virtual private network (VPN) gateway for a virtual network.</span></span>

## <span data-ttu-id="101e5-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="101e5-108">EXAMPLES</span></span>

### <span data-ttu-id="101e5-109">Пример 1: Удаление маршрута к сайту по умолчанию</span><span class="sxs-lookup"><span data-stu-id="101e5-109">Example 1: Remove a route to the default site</span></span>
```
PS C:\> Remove-AzureVNetGatewayDefaultSite -VnetName "ContosoVNet01"
```

<span data-ttu-id="101e5-110">Эта команда удаляет маршрут к сайту по умолчанию из VPN виртуальной сети с именем ContosoVNet01.</span><span class="sxs-lookup"><span data-stu-id="101e5-110">This command removes the route to the default site from the VPN of the virtual network named ContosoVNet01.</span></span>

## <span data-ttu-id="101e5-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="101e5-111">PARAMETERS</span></span>

### <span data-ttu-id="101e5-112">-Profile</span><span class="sxs-lookup"><span data-stu-id="101e5-112">-Profile</span></span>
<span data-ttu-id="101e5-113">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="101e5-113">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="101e5-114">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="101e5-114">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="101e5-115">-VNetName</span><span class="sxs-lookup"><span data-stu-id="101e5-115">-VNetName</span></span>
<span data-ttu-id="101e5-116">Указывает виртуальную сеть.</span><span class="sxs-lookup"><span data-stu-id="101e5-116">Specifies a virtual network.</span></span>
<span data-ttu-id="101e5-117">Этот командлет удаляет маршрут по умолчанию из VPN-шлюза для виртуальной сети, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="101e5-117">This cmdlet removes the default route from the VPN gateway for the virtual network that this parameter specifies.</span></span>

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

### <span data-ttu-id="101e5-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="101e5-118">CommonParameters</span></span>
<span data-ttu-id="101e5-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="101e5-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="101e5-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="101e5-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="101e5-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="101e5-121">INPUTS</span></span>

## <span data-ttu-id="101e5-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="101e5-122">OUTPUTS</span></span>

## <span data-ttu-id="101e5-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="101e5-123">NOTES</span></span>

## <span data-ttu-id="101e5-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="101e5-124">RELATED LINKS</span></span>

[<span data-ttu-id="101e5-125">Set-AzureVNetGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="101e5-125">Set-AzureVNetGatewayDefaultSite</span></span>](./Set-AzureVNetGatewayDefaultSite.md)

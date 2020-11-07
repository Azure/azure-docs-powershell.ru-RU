---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A27EE9C0-C7F5-4BF6-AE52-58087BD1B1C3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetworkgatewaydefaultsite
schema: 2.0.0
ms.openlocfilehash: 463951ca6b6679671f330a3ddb0f9460a878a3d3
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914390"
---
# <span data-ttu-id="ba32a-101">Set-AzureRmVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="ba32a-101">Set-AzureRmVirtualNetworkGatewayDefaultSite</span></span>

## <span data-ttu-id="ba32a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ba32a-102">SYNOPSIS</span></span>
<span data-ttu-id="ba32a-103">Задает сайт по умолчанию для шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="ba32a-103">Sets the default site for a virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ba32a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ba32a-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway <PSVirtualNetworkGateway>
 -GatewayDefaultSite <PSLocalNetworkGateway> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ba32a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ba32a-105">DESCRIPTION</span></span>
<span data-ttu-id="ba32a-106">Командлет **Set-AzureRmVirtualNetworkGatewayDefaultSite** назначает сайт по умолчанию для виртуального сетевого шлюза с принудительным туннелированием.</span><span class="sxs-lookup"><span data-stu-id="ba32a-106">The **Set-AzureRmVirtualNetworkGatewayDefaultSite** cmdlet assigns a forced tunneling default site to a virtual network gateway.</span></span>
<span data-ttu-id="ba32a-107">Принудительное туннелирование обеспечивает способ переадресации трафика с привязкой к Интернету с виртуальных машин Azure в локальную сеть; Это позволяет проверять и проверять трафик перед его выпуском.</span><span class="sxs-lookup"><span data-stu-id="ba32a-107">Forced tunneling provides a way for you to redirect Internet-bound traffic from Azure virtual machines to your on-premises network; this enables you to inspect and audit traffic before releasing it.</span></span>
<span data-ttu-id="ba32a-108">Принудительное туннелирование выполняется с помощью туннеля виртуальной частной сети (VPN). для этого туннеля требуется сайт по умолчанию, локальный шлюз, на котором перенаправляются все данные, связанные с Интернетом Azure.</span><span class="sxs-lookup"><span data-stu-id="ba32a-108">Forced tunneling is carried out by using a virtual private network (VPN) tunnel; this tunnel requires a default site, a local gateway where all the Azure Internet-bound traffic is redirected.</span></span>
<span data-ttu-id="ba32a-109">**Set-AzureRmVirtualNetworkGatewayDefaultSite** предоставляет способ изменения сайта по умолчанию, назначенного шлюзом.</span><span class="sxs-lookup"><span data-stu-id="ba32a-109">**Set-AzureRmVirtualNetworkGatewayDefaultSite** provides a way to change the default site assigned to a gateway.</span></span>

## <span data-ttu-id="ba32a-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ba32a-110">EXAMPLES</span></span>

### <span data-ttu-id="ba32a-111">Пример 1: назначение сайта по умолчанию шлюзу виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="ba32a-111">Example 1: Assign a default site to a virtual network gateway</span></span>
```
PS C:\>$LocalGateway = Get-AzureRmLocalNetworkGateway -Name "ContosoLocalGateway " -ResourceGroup "ContosoResourceGroup"
PS C:\> $VirtualGateway = Get-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Set-AzureRmVirtualNetworkGatewayDefaultSite -GatewayDefaultSite $LocalGateway -VirtualNetworkGateway $VirtualGateway
```

<span data-ttu-id="ba32a-112">В этом примере сайт по умолчанию назначается шлюзу виртуальной сети с именем ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="ba32a-112">This example assigns a default site to a virtual network gateway named ContosoVirtualGateway.</span></span>

<span data-ttu-id="ba32a-113">Первая команда создает ссылку на объект на локальный шлюз с именем ContosoLocalGateway.</span><span class="sxs-lookup"><span data-stu-id="ba32a-113">The first command creates an object reference to a local gateway named ContosoLocalGateway.</span></span>
<span data-ttu-id="ba32a-114">Эта ссылка на объект, хранящаяся в переменной с именем $LocalGateway, представляет шлюз для настройки в качестве сайта по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ba32a-114">This object reference that is stored in the variable named $LocalGateway represents the gateway to be configured as the default site</span></span>

<span data-ttu-id="ba32a-115">.</span><span class="sxs-lookup"><span data-stu-id="ba32a-115">.</span></span>
<span data-ttu-id="ba32a-116">Вторая команда создает ссылку на объект для шлюза виртуальной сети и сохраняет результат в переменной с именем $VirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="ba32a-116">The second command then creates an object reference to the virtual network gateway and stores the result in the variable named $VirtualGateway.</span></span>

<span data-ttu-id="ba32a-117">Третья команда использует командлет **Set-AzureRmVirtualNetworkGatewayDefaultSite** , чтобы назначить сайт по умолчанию ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="ba32a-117">The third command uses the **Set-AzureRmVirtualNetworkGatewayDefaultSite** cmdlet to assign the default site to ContosoVirtualGateway.</span></span>

## <span data-ttu-id="ba32a-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ba32a-118">PARAMETERS</span></span>

### <span data-ttu-id="ba32a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba32a-119">-DefaultProfile</span></span>
<span data-ttu-id="ba32a-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ba32a-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba32a-121">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="ba32a-121">-GatewayDefaultSite</span></span>
<span data-ttu-id="ba32a-122">Указывает ссылку на объект для шлюза локальной сети, назначаемого в качестве сайта по умолчанию для указанной виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="ba32a-122">Specifies an object reference to the local network gateway to be assigned as the default site for the specified virtual network.</span></span>
<span data-ttu-id="ba32a-123">Вы можете использовать командлет Get-AzureRmLocalNetworkGateway для создания ссылки на объект на локальный шлюз.</span><span class="sxs-lookup"><span data-stu-id="ba32a-123">You can use the Get-AzureRmLocalNetworkGateway cmdlet to create an object reference to a local gateway.</span></span>

```yaml
Type: PSLocalNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba32a-124">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ba32a-124">-VirtualNetworkGateway</span></span>
<span data-ttu-id="ba32a-125">Указывает ссылку на объект шлюза виртуальной сети, на котором будет назначен сайт по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ba32a-125">Specifies an object reference to the virtual network gateway where the default site will be assigned.</span></span>
<span data-ttu-id="ba32a-126">Вы можете создать ссылку на объект для шлюза виртуальной сети с помощью **Get-AzureRmVirtualNetworkGateway** и указать имя шлюза.</span><span class="sxs-lookup"><span data-stu-id="ba32a-126">You can create an object reference to a virtual network gateway by using the **Get-AzureRmVirtualNetworkGateway** and specifying the name of the gateway.</span></span>

<span data-ttu-id="ba32a-127">Переменную $VirtualGateway можно использовать в качестве значения параметра для параметра *VirtualNetworkGateway* :</span><span class="sxs-lookup"><span data-stu-id="ba32a-127">The variable $VirtualGateway can then be used as the parameter value for the *VirtualNetworkGateway* parameter:</span></span>

```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ba32a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba32a-128">CommonParameters</span></span>
<span data-ttu-id="ba32a-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ba32a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba32a-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba32a-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba32a-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ba32a-131">INPUTS</span></span>

###  
<span data-ttu-id="ba32a-132">Этот командлет принимает конвейерные экземпляры объекта **Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway** .</span><span class="sxs-lookup"><span data-stu-id="ba32a-132">This cmdlet accepts pipelined instances of the **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** object.</span></span>

## <span data-ttu-id="ba32a-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ba32a-133">OUTPUTS</span></span>

###  
<span data-ttu-id="ba32a-134">Этот командлет изменяет существующие экземпляры объекта **Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway** .</span><span class="sxs-lookup"><span data-stu-id="ba32a-134">This cmdlet modifies existing instances of the **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** object.</span></span>

## <span data-ttu-id="ba32a-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="ba32a-135">NOTES</span></span>

## <span data-ttu-id="ba32a-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ba32a-136">RELATED LINKS</span></span>

[<span data-ttu-id="ba32a-137">Get-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ba32a-137">Get-AzureRmLocalNetworkGateway</span></span>](./Get-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="ba32a-138">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ba32a-138">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="ba32a-139">Remove-AzureRmVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="ba32a-139">Remove-AzureRmVirtualNetworkGatewayDefaultSite</span></span>](./Remove-AzureRmVirtualNetworkGatewayDefaultSite.md)



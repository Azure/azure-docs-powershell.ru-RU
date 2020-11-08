---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: A7DFF559-188D-4CF9-9315-CA327E0C5C0B
online version: ''
schema: 2.0.0
ms.openlocfilehash: d502ba2961e5238426228e4ac58a29b922be81f3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075823"
---
# <span data-ttu-id="8aaac-101">Set-AzureRoute</span><span class="sxs-lookup"><span data-stu-id="8aaac-101">Set-AzureRoute</span></span>

## <span data-ttu-id="8aaac-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8aaac-102">SYNOPSIS</span></span>
<span data-ttu-id="8aaac-103">Создает маршрут в таблице маршрутов.</span><span class="sxs-lookup"><span data-stu-id="8aaac-103">Creates a route in a route table.</span></span>

## <span data-ttu-id="8aaac-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8aaac-104">SYNTAX</span></span>

```
Set-AzureRoute -RouteName <String> -AddressPrefix <String> -NextHopType <String> [-NextHopIpAddress <String>]
 -RouteTable <IRouteTable> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="8aaac-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8aaac-105">DESCRIPTION</span></span>
<span data-ttu-id="8aaac-106">Командлет **Set-AzureRoute** создает маршрут в таблице маршрутов.</span><span class="sxs-lookup"><span data-stu-id="8aaac-106">The **Set-AzureRoute** cmdlet creates a route in a route table.</span></span>
<span data-ttu-id="8aaac-107">Новый маршрут вступает в силу практически сразу на виртуальных машинах, связанных с таблицей маршрутов.</span><span class="sxs-lookup"><span data-stu-id="8aaac-107">The new route takes effect almost immediately on the virtual machines that are associated with the route table.</span></span>

## <span data-ttu-id="8aaac-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8aaac-108">EXAMPLES</span></span>

### <span data-ttu-id="8aaac-109">Пример 1: Добавление виртуального устройства, маршрут следующего прыжка</span><span class="sxs-lookup"><span data-stu-id="8aaac-109">Example 1: Add a virtual appliance next hop route</span></span>
```
PS C:\> New-AzureRouteTable -Name "ApplianceRouteTable" -Location "Central US" -Label "Appliance Route Table" | Set-AzureRoute -RouteName "ApplianceRoute03" -AddressPrefix "10.0.0.0/24" -NextHopType VirtualAppliance -NextHopIpAddress "10.0.1.5"

Routes                        Name                          Location                      Label
------                        ----                          --------                      -----
{approute}                    AppRT                         Central US                    Appliance Route Table
```

<span data-ttu-id="8aaac-110">Эта команда создает таблицу маршрутов с именем ApplianceRouteTable в указанном расположении.</span><span class="sxs-lookup"><span data-stu-id="8aaac-110">This command creates a route table named ApplianceRouteTable in the specified location.</span></span>
<span data-ttu-id="8aaac-111">Команда передает эту таблицу маршрутов в текущий командлет.</span><span class="sxs-lookup"><span data-stu-id="8aaac-111">The command passes that route table to the current cmdlet.</span></span>
<span data-ttu-id="8aaac-112">Текущий командлет добавляет маршрут с именем ApplianceRoute03, который является типом VirtualAppliance следующего прыжка.</span><span class="sxs-lookup"><span data-stu-id="8aaac-112">The current cmdlet adds a route named ApplianceRoute03, which is a VirtualAppliance next hop type.</span></span>
<span data-ttu-id="8aaac-113">Команда задает IP-адрес следующего прыжка и префикс адреса для маршрута.</span><span class="sxs-lookup"><span data-stu-id="8aaac-113">The command specifies the next hop IP address and the address prefix for the route.</span></span>

### <span data-ttu-id="8aaac-114">Пример 2: Добавление маршрутизатора следующего прыжка к Интернету</span><span class="sxs-lookup"><span data-stu-id="8aaac-114">Example 2: Add an Internet next hop route</span></span>
```
PS C:\> Get-AzureRouteTable -Name "ApplianceRouteTable" | Set-AzureRoute -RouteName "InternetRoute" -AddressPrefix "0.0.0.0/0" -NextHopType Internet

Routes                        Name                          Location                      Label
------                        ----                          --------                      -----
{approute, internetroute}     AppRT                         Central US                    Appliance Route Table
```

<span data-ttu-id="8aaac-115">Эта команда получает таблицу маршрутов с именем ApplianceRouteTable.</span><span class="sxs-lookup"><span data-stu-id="8aaac-115">This command gets a route table named ApplianceRouteTable.</span></span>
<span data-ttu-id="8aaac-116">Команда передает эту таблицу маршрутов в текущий командлет.</span><span class="sxs-lookup"><span data-stu-id="8aaac-116">The command passes that route table to the current cmdlet.</span></span>
<span data-ttu-id="8aaac-117">Текущий командлет добавляет маршрут с именем InternetRoute, который является типом следующего прыжка в Интернете.</span><span class="sxs-lookup"><span data-stu-id="8aaac-117">The current cmdlet adds a route named InternetRoute, which is an Internet next hop type.</span></span>
<span data-ttu-id="8aaac-118">Команда задает префикс адреса для маршрута.</span><span class="sxs-lookup"><span data-stu-id="8aaac-118">The command specifies the address prefix for the route.</span></span>

## <span data-ttu-id="8aaac-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8aaac-119">PARAMETERS</span></span>

### <span data-ttu-id="8aaac-120">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="8aaac-120">-AddressPrefix</span></span>
<span data-ttu-id="8aaac-121">Указывает префикс адреса для нового маршрута.</span><span class="sxs-lookup"><span data-stu-id="8aaac-121">Specifies an address prefix for the new route.</span></span>

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

### <span data-ttu-id="8aaac-122">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="8aaac-122">-NextHopIpAddress</span></span>
<span data-ttu-id="8aaac-123">Указывает IP-адрес устройства, которое является следующим прыжком для трафика, использующего этот маршрут.</span><span class="sxs-lookup"><span data-stu-id="8aaac-123">Specifies the IP address of the appliance that is the next hop for traffic that uses this route.</span></span>
<span data-ttu-id="8aaac-124">Укажите это значение только в том случае, если для параметра *NextHopType* задано значение VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="8aaac-124">Specify this value only if you specify a value of VirtualAppliance for the *NextHopType* parameter.</span></span>

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

### <span data-ttu-id="8aaac-125">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="8aaac-125">-NextHopType</span></span>
<span data-ttu-id="8aaac-126">Указывает тип следующего прыжка для трафика, использующего этот маршрут.</span><span class="sxs-lookup"><span data-stu-id="8aaac-126">Specifies the next hop type for traffic that uses this route.</span></span>
<span data-ttu-id="8aaac-127">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="8aaac-127">Valid values are:</span></span> 

- <span data-ttu-id="8aaac-128">VPNGateway</span><span class="sxs-lookup"><span data-stu-id="8aaac-128">VPNGateway</span></span>
- <span data-ttu-id="8aaac-129">VNETLocal</span><span class="sxs-lookup"><span data-stu-id="8aaac-129">VNETLocal</span></span>
- <span data-ttu-id="8aaac-130">IIS</span><span class="sxs-lookup"><span data-stu-id="8aaac-130">Internet</span></span>
- <span data-ttu-id="8aaac-131">VirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="8aaac-131">VirtualAppliance</span></span>
- <span data-ttu-id="8aaac-132">Значения</span><span class="sxs-lookup"><span data-stu-id="8aaac-132">Null</span></span>

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

### <span data-ttu-id="8aaac-133">-Profile</span><span class="sxs-lookup"><span data-stu-id="8aaac-133">-Profile</span></span>
<span data-ttu-id="8aaac-134">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="8aaac-134">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="8aaac-135">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8aaac-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8aaac-136">-RouteName</span><span class="sxs-lookup"><span data-stu-id="8aaac-136">-RouteName</span></span>
<span data-ttu-id="8aaac-137">Задает имя для нового маршрута, который добавляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="8aaac-137">Specifies a name for the new route that this cmdlet adds.</span></span>

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

### <span data-ttu-id="8aaac-138">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="8aaac-138">-RouteTable</span></span>
<span data-ttu-id="8aaac-139">Указывает таблицу маршрутов, к которой этот командлет добавляет новый маршрут.</span><span class="sxs-lookup"><span data-stu-id="8aaac-139">Specifies the route table to which this cmdlet adds the new route.</span></span>

```yaml
Type: IRouteTable
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8aaac-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8aaac-140">CommonParameters</span></span>
<span data-ttu-id="8aaac-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8aaac-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8aaac-142">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8aaac-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8aaac-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8aaac-143">INPUTS</span></span>

## <span data-ttu-id="8aaac-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8aaac-144">OUTPUTS</span></span>

## <span data-ttu-id="8aaac-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="8aaac-145">NOTES</span></span>

## <span data-ttu-id="8aaac-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8aaac-146">RELATED LINKS</span></span>

[<span data-ttu-id="8aaac-147">Remove-AzureRoute</span><span class="sxs-lookup"><span data-stu-id="8aaac-147">Remove-AzureRoute</span></span>](./Remove-AzureRoute.md)



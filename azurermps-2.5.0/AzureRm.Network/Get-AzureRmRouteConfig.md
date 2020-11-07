---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: DBD40431-DD7A-42CB-83AA-568B1065A468
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermrouteconfig
schema: 2.0.0
ms.openlocfilehash: 907ca017518304a38340e9539aa4e8faf4216d59
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93915153"
---
# <span data-ttu-id="1ac07-101">Get-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="1ac07-101">Get-AzureRmRouteConfig</span></span>

## <span data-ttu-id="1ac07-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1ac07-102">SYNOPSIS</span></span>
<span data-ttu-id="1ac07-103">Возвращает маршруты из таблицы маршрутов.</span><span class="sxs-lookup"><span data-stu-id="1ac07-103">Gets routes from a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1ac07-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1ac07-104">SYNTAX</span></span>

```
Get-AzureRmRouteConfig -RouteTable <PSRouteTable> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1ac07-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1ac07-105">DESCRIPTION</span></span>
<span data-ttu-id="1ac07-106">Командлет **Get-AzureRmRouteConfig** получает маршруты из таблицы маршрута Azure.</span><span class="sxs-lookup"><span data-stu-id="1ac07-106">The **Get-AzureRmRouteConfig** cmdlet gets routes from an Azure route table.</span></span>
<span data-ttu-id="1ac07-107">Вы можете указать маршрут по имени.</span><span class="sxs-lookup"><span data-stu-id="1ac07-107">You can specify a route by name.</span></span>

## <span data-ttu-id="1ac07-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1ac07-108">EXAMPLES</span></span>

### <span data-ttu-id="1ac07-109">Пример 1: получение таблицы маршрутов</span><span class="sxs-lookup"><span data-stu-id="1ac07-109">Example 1: Get a route table</span></span>
```
PS C:\>Get-AzureRmRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Get-AzureRmRouteConfig -Name "Route07"
Name              : route07
Id                : 
Etag              : 
ProvisioningState : 
AddressPrefix     : 10.1.0.0/16
NextHopType       : VnetLocal
NextHopIpAddress  :
```

<span data-ttu-id="1ac07-110">Эта команда получает таблицу маршрутов с именем RouteTable01 с помощью командлета **Get-AzureRmRouteTable** .</span><span class="sxs-lookup"><span data-stu-id="1ac07-110">This command gets the route table named RouteTable01 by using the **Get-AzureRmRouteTable** cmdlet.</span></span>
<span data-ttu-id="1ac07-111">Команда передает эту таблицу в текущий командлет с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="1ac07-111">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="1ac07-112">Текущий командлет получает маршрут с именем Route07 в таблице маршрутов с именем RouteTable01.</span><span class="sxs-lookup"><span data-stu-id="1ac07-112">The current cmdlet gets the route named Route07 in the route table named RouteTable01.</span></span>

## <span data-ttu-id="1ac07-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1ac07-113">PARAMETERS</span></span>

### <span data-ttu-id="1ac07-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ac07-114">-DefaultProfile</span></span>
<span data-ttu-id="1ac07-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1ac07-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1ac07-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1ac07-116">-Name</span></span>
<span data-ttu-id="1ac07-117">Указывает имя маршрута, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="1ac07-117">Specifies the name of the route that this cmdlet gets.</span></span>

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

### <span data-ttu-id="1ac07-118">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="1ac07-118">-RouteTable</span></span>
<span data-ttu-id="1ac07-119">Указывает таблицу маршрутов, из которой этот командлет получает маршруты.</span><span class="sxs-lookup"><span data-stu-id="1ac07-119">Specifies the route table from which this cmdlet gets routes.</span></span>

```yaml
Type: PSRouteTable
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1ac07-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ac07-120">CommonParameters</span></span>
<span data-ttu-id="1ac07-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1ac07-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ac07-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ac07-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ac07-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1ac07-123">INPUTS</span></span>

### <span data-ttu-id="1ac07-124">PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="1ac07-124">PSRouteTable</span></span>
<span data-ttu-id="1ac07-125">Параметр "RouteTable" принимает значение типа "PSRouteTable" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="1ac07-125">Parameter 'RouteTable' accepts value of type 'PSRouteTable' from the pipeline</span></span>

## <span data-ttu-id="1ac07-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1ac07-126">OUTPUTS</span></span>

### <span data-ttu-id="1ac07-127">Microsoft. Azure. Commands. Network. Models. PSRoute</span><span class="sxs-lookup"><span data-stu-id="1ac07-127">Microsoft.Azure.Commands.Network.Models.PSRoute</span></span>

## <span data-ttu-id="1ac07-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="1ac07-128">NOTES</span></span>

## <span data-ttu-id="1ac07-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1ac07-129">RELATED LINKS</span></span>

[<span data-ttu-id="1ac07-130">Add-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="1ac07-130">Add-AzureRmRouteConfig</span></span>](./Add-AzureRmRouteConfig.md)

[<span data-ttu-id="1ac07-131">Get-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="1ac07-131">Get-AzureRmRouteTable</span></span>](./Get-AzureRmRouteTable.md)

[<span data-ttu-id="1ac07-132">New-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="1ac07-132">New-AzureRmRouteConfig</span></span>](./New-AzureRmRouteConfig.md)

[<span data-ttu-id="1ac07-133">Remove-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="1ac07-133">Remove-AzureRmRouteConfig</span></span>](./Remove-AzureRmRouteConfig.md)

[<span data-ttu-id="1ac07-134">Set-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="1ac07-134">Set-AzureRmRouteConfig</span></span>](./Set-AzureRmRouteConfig.md)



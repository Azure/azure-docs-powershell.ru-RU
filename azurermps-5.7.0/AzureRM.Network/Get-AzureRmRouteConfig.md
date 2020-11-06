---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: DBD40431-DD7A-42CB-83AA-568B1065A468
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmRouteConfig.md
ms.openlocfilehash: f00a1d0c67d7bb395a328e01915f5bb0334d3d83
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560308"
---
# <span data-ttu-id="f6ad4-101">Get-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="f6ad4-101">Get-AzureRmRouteConfig</span></span>

## <span data-ttu-id="f6ad4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f6ad4-102">SYNOPSIS</span></span>
<span data-ttu-id="f6ad4-103">Возвращает маршруты из таблицы маршрутов.</span><span class="sxs-lookup"><span data-stu-id="f6ad4-103">Gets routes from a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f6ad4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f6ad4-104">SYNTAX</span></span>

```
Get-AzureRmRouteConfig -RouteTable <PSRouteTable> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f6ad4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f6ad4-105">DESCRIPTION</span></span>
<span data-ttu-id="f6ad4-106">Командлет **Get-AzureRmRouteConfig** получает маршруты из таблицы маршрута Azure.</span><span class="sxs-lookup"><span data-stu-id="f6ad4-106">The **Get-AzureRmRouteConfig** cmdlet gets routes from an Azure route table.</span></span>
<span data-ttu-id="f6ad4-107">Вы можете указать маршрут по имени.</span><span class="sxs-lookup"><span data-stu-id="f6ad4-107">You can specify a route by name.</span></span>

## <span data-ttu-id="f6ad4-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f6ad4-108">EXAMPLES</span></span>

### <span data-ttu-id="f6ad4-109">Пример 1: получение таблицы маршрутов</span><span class="sxs-lookup"><span data-stu-id="f6ad4-109">Example 1: Get a route table</span></span>
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

<span data-ttu-id="f6ad4-110">Эта команда получает таблицу маршрутов с именем RouteTable01 с помощью командлета **Get-AzureRmRouteTable** .</span><span class="sxs-lookup"><span data-stu-id="f6ad4-110">This command gets the route table named RouteTable01 by using the **Get-AzureRmRouteTable** cmdlet.</span></span>
<span data-ttu-id="f6ad4-111">Команда передает эту таблицу в текущий командлет с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="f6ad4-111">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="f6ad4-112">Текущий командлет получает маршрут с именем Route07 в таблице маршрутов с именем RouteTable01.</span><span class="sxs-lookup"><span data-stu-id="f6ad4-112">The current cmdlet gets the route named Route07 in the route table named RouteTable01.</span></span>

## <span data-ttu-id="f6ad4-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f6ad4-113">PARAMETERS</span></span>

### <span data-ttu-id="f6ad4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6ad4-114">-DefaultProfile</span></span>
<span data-ttu-id="f6ad4-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f6ad4-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f6ad4-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f6ad4-116">-Name</span></span>
<span data-ttu-id="f6ad4-117">Указывает имя маршрута, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="f6ad4-117">Specifies the name of the route that this cmdlet gets.</span></span>

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

### <span data-ttu-id="f6ad4-118">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="f6ad4-118">-RouteTable</span></span>
<span data-ttu-id="f6ad4-119">Указывает таблицу маршрутов, из которой этот командлет получает маршруты.</span><span class="sxs-lookup"><span data-stu-id="f6ad4-119">Specifies the route table from which this cmdlet gets routes.</span></span>

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

### <span data-ttu-id="f6ad4-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6ad4-120">CommonParameters</span></span>
<span data-ttu-id="f6ad4-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f6ad4-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6ad4-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6ad4-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6ad4-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f6ad4-123">INPUTS</span></span>

### <span data-ttu-id="f6ad4-124">PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="f6ad4-124">PSRouteTable</span></span>
<span data-ttu-id="f6ad4-125">Параметр "RouteTable" принимает значение типа "PSRouteTable" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="f6ad4-125">Parameter 'RouteTable' accepts value of type 'PSRouteTable' from the pipeline</span></span>

## <span data-ttu-id="f6ad4-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f6ad4-126">OUTPUTS</span></span>

### <span data-ttu-id="f6ad4-127">Microsoft. Azure. Commands. Network. Models. PSRoute</span><span class="sxs-lookup"><span data-stu-id="f6ad4-127">Microsoft.Azure.Commands.Network.Models.PSRoute</span></span>

## <span data-ttu-id="f6ad4-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="f6ad4-128">NOTES</span></span>

## <span data-ttu-id="f6ad4-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f6ad4-129">RELATED LINKS</span></span>

[<span data-ttu-id="f6ad4-130">Add-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="f6ad4-130">Add-AzureRmRouteConfig</span></span>](./Add-AzureRmRouteConfig.md)

[<span data-ttu-id="f6ad4-131">Get-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="f6ad4-131">Get-AzureRmRouteTable</span></span>](./Get-AzureRmRouteTable.md)

[<span data-ttu-id="f6ad4-132">New-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="f6ad4-132">New-AzureRmRouteConfig</span></span>](./New-AzureRmRouteConfig.md)

[<span data-ttu-id="f6ad4-133">Remove-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="f6ad4-133">Remove-AzureRmRouteConfig</span></span>](./Remove-AzureRmRouteConfig.md)

[<span data-ttu-id="f6ad4-134">Set-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="f6ad4-134">Set-AzureRmRouteConfig</span></span>](./Set-AzureRmRouteConfig.md)



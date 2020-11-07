---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DBD40431-DD7A-42CB-83AA-568B1065A468
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzRouteConfig.md
ms.openlocfilehash: a5b80a15711314d5acc4f0288c1fd0304da772fc
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93909881"
---
# <span data-ttu-id="dc5b3-101">Get-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="dc5b3-101">Get-AzRouteConfig</span></span>

## <span data-ttu-id="dc5b3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dc5b3-102">SYNOPSIS</span></span>
<span data-ttu-id="dc5b3-103">Возвращает маршруты из таблицы маршрутов.</span><span class="sxs-lookup"><span data-stu-id="dc5b3-103">Gets routes from a route table.</span></span>

## <span data-ttu-id="dc5b3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dc5b3-104">SYNTAX</span></span>

```
Get-AzRouteConfig -RouteTable <PSRouteTable> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dc5b3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dc5b3-105">DESCRIPTION</span></span>
<span data-ttu-id="dc5b3-106">Командлет **Get-AzRouteConfig** получает маршруты из таблицы маршрута Azure.</span><span class="sxs-lookup"><span data-stu-id="dc5b3-106">The **Get-AzRouteConfig** cmdlet gets routes from an Azure route table.</span></span>
<span data-ttu-id="dc5b3-107">Вы можете указать маршрут по имени.</span><span class="sxs-lookup"><span data-stu-id="dc5b3-107">You can specify a route by name.</span></span>

## <span data-ttu-id="dc5b3-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dc5b3-108">EXAMPLES</span></span>

### <span data-ttu-id="dc5b3-109">Пример 1: получение таблицы маршрутов</span><span class="sxs-lookup"><span data-stu-id="dc5b3-109">Example 1: Get a route table</span></span>
```
PS C:\>Get-AzRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Get-AzRouteConfig -Name "Route07"
Name              : route07
Id                : 
Etag              : 
ProvisioningState : 
AddressPrefix     : 10.1.0.0/16
NextHopType       : VnetLocal
NextHopIpAddress  :
```

<span data-ttu-id="dc5b3-110">Эта команда получает таблицу маршрутов с именем RouteTable01 с помощью командлета **Get-AzRouteTable** .</span><span class="sxs-lookup"><span data-stu-id="dc5b3-110">This command gets the route table named RouteTable01 by using the **Get-AzRouteTable** cmdlet.</span></span>
<span data-ttu-id="dc5b3-111">Команда передает эту таблицу в текущий командлет с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="dc5b3-111">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="dc5b3-112">Текущий командлет получает маршрут с именем Route07 в таблице маршрутов с именем RouteTable01.</span><span class="sxs-lookup"><span data-stu-id="dc5b3-112">The current cmdlet gets the route named Route07 in the route table named RouteTable01.</span></span>

## <span data-ttu-id="dc5b3-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dc5b3-113">PARAMETERS</span></span>

### <span data-ttu-id="dc5b3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc5b3-114">-DefaultProfile</span></span>
<span data-ttu-id="dc5b3-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dc5b3-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dc5b3-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="dc5b3-116">-Name</span></span>
<span data-ttu-id="dc5b3-117">Указывает имя маршрута, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="dc5b3-117">Specifies the name of the route that this cmdlet gets.</span></span>

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

### <span data-ttu-id="dc5b3-118">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="dc5b3-118">-RouteTable</span></span>
<span data-ttu-id="dc5b3-119">Указывает таблицу маршрутов, из которой этот командлет получает маршруты.</span><span class="sxs-lookup"><span data-stu-id="dc5b3-119">Specifies the route table from which this cmdlet gets routes.</span></span>

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

### <span data-ttu-id="dc5b3-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc5b3-120">CommonParameters</span></span>
<span data-ttu-id="dc5b3-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dc5b3-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc5b3-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc5b3-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc5b3-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dc5b3-123">INPUTS</span></span>

### <span data-ttu-id="dc5b3-124">PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="dc5b3-124">PSRouteTable</span></span>
<span data-ttu-id="dc5b3-125">Параметр "RouteTable" принимает значение типа "PSRouteTable" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="dc5b3-125">Parameter 'RouteTable' accepts value of type 'PSRouteTable' from the pipeline</span></span>

## <span data-ttu-id="dc5b3-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dc5b3-126">OUTPUTS</span></span>

### <span data-ttu-id="dc5b3-127">Microsoft. Azure. Commands. Network. Models. PSRoute</span><span class="sxs-lookup"><span data-stu-id="dc5b3-127">Microsoft.Azure.Commands.Network.Models.PSRoute</span></span>

## <span data-ttu-id="dc5b3-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="dc5b3-128">NOTES</span></span>

## <span data-ttu-id="dc5b3-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dc5b3-129">RELATED LINKS</span></span>

[<span data-ttu-id="dc5b3-130">Add-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="dc5b3-130">Add-AzRouteConfig</span></span>](./Add-AzRouteConfig.md)

[<span data-ttu-id="dc5b3-131">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="dc5b3-131">Get-AzRouteTable</span></span>](./Get-AzRouteTable.md)

[<span data-ttu-id="dc5b3-132">New-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="dc5b3-132">New-AzRouteConfig</span></span>](./New-AzRouteConfig.md)

[<span data-ttu-id="dc5b3-133">Remove-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="dc5b3-133">Remove-AzRouteConfig</span></span>](./Remove-AzRouteConfig.md)

[<span data-ttu-id="dc5b3-134">Set-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="dc5b3-134">Set-AzRouteConfig</span></span>](./Set-AzRouteConfig.md)



---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: DBD40431-DD7A-42CB-83AA-568B1065A468
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmRouteConfig.md
ms.openlocfilehash: dd23891bc56ac2eb8fce30708d9a72055a567bf3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562947"
---
# <span data-ttu-id="0dc76-101">Get-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="0dc76-101">Get-AzureRmRouteConfig</span></span>

## <span data-ttu-id="0dc76-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0dc76-102">SYNOPSIS</span></span>
<span data-ttu-id="0dc76-103">Возвращает маршруты из таблицы маршрутов.</span><span class="sxs-lookup"><span data-stu-id="0dc76-103">Gets routes from a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0dc76-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0dc76-104">SYNTAX</span></span>

```
Get-AzureRmRouteConfig -RouteTable <PSRouteTable> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0dc76-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0dc76-105">DESCRIPTION</span></span>
<span data-ttu-id="0dc76-106">Командлет **Get-AzureRmRouteConfig** получает маршруты из таблицы маршрута Azure.</span><span class="sxs-lookup"><span data-stu-id="0dc76-106">The **Get-AzureRmRouteConfig** cmdlet gets routes from an Azure route table.</span></span>
<span data-ttu-id="0dc76-107">Вы можете указать маршрут по имени.</span><span class="sxs-lookup"><span data-stu-id="0dc76-107">You can specify a route by name.</span></span>

## <span data-ttu-id="0dc76-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0dc76-108">EXAMPLES</span></span>

### <span data-ttu-id="0dc76-109">Пример 1: получение таблицы маршрутов</span><span class="sxs-lookup"><span data-stu-id="0dc76-109">Example 1: Get a route table</span></span>
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

<span data-ttu-id="0dc76-110">Эта команда получает таблицу маршрутов с именем RouteTable01 с помощью командлета **Get-AzureRmRouteTable** .</span><span class="sxs-lookup"><span data-stu-id="0dc76-110">This command gets the route table named RouteTable01 by using the **Get-AzureRmRouteTable** cmdlet.</span></span>
<span data-ttu-id="0dc76-111">Команда передает эту таблицу в текущий командлет с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="0dc76-111">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="0dc76-112">Текущий командлет получает маршрут с именем Route07 в таблице маршрутов с именем RouteTable01.</span><span class="sxs-lookup"><span data-stu-id="0dc76-112">The current cmdlet gets the route named Route07 in the route table named RouteTable01.</span></span>

## <span data-ttu-id="0dc76-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0dc76-113">PARAMETERS</span></span>

### <span data-ttu-id="0dc76-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0dc76-114">-DefaultProfile</span></span>
<span data-ttu-id="0dc76-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0dc76-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dc76-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0dc76-116">-Name</span></span>
<span data-ttu-id="0dc76-117">Указывает имя маршрута, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="0dc76-117">Specifies the name of the route that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dc76-118">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="0dc76-118">-RouteTable</span></span>
<span data-ttu-id="0dc76-119">Указывает таблицу маршрутов, из которой этот командлет получает маршруты.</span><span class="sxs-lookup"><span data-stu-id="0dc76-119">Specifies the route table from which this cmdlet gets routes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteTable
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0dc76-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0dc76-120">CommonParameters</span></span>
<span data-ttu-id="0dc76-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0dc76-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0dc76-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0dc76-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0dc76-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0dc76-123">INPUTS</span></span>

### <span data-ttu-id="0dc76-124">Microsoft. Azure. Commands. Network. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="0dc76-124">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="0dc76-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0dc76-125">OUTPUTS</span></span>

### <span data-ttu-id="0dc76-126">Microsoft. Azure. Commands. Network. Models. PSRoute</span><span class="sxs-lookup"><span data-stu-id="0dc76-126">Microsoft.Azure.Commands.Network.Models.PSRoute</span></span>

## <span data-ttu-id="0dc76-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="0dc76-127">NOTES</span></span>

## <span data-ttu-id="0dc76-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0dc76-128">RELATED LINKS</span></span>

[<span data-ttu-id="0dc76-129">Add-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="0dc76-129">Add-AzureRmRouteConfig</span></span>](./Add-AzureRmRouteConfig.md)

[<span data-ttu-id="0dc76-130">Get-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="0dc76-130">Get-AzureRmRouteTable</span></span>](./Get-AzureRmRouteTable.md)

[<span data-ttu-id="0dc76-131">New-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="0dc76-131">New-AzureRmRouteConfig</span></span>](./New-AzureRmRouteConfig.md)

[<span data-ttu-id="0dc76-132">Remove-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="0dc76-132">Remove-AzureRmRouteConfig</span></span>](./Remove-AzureRmRouteConfig.md)

[<span data-ttu-id="0dc76-133">Set-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="0dc76-133">Set-AzureRmRouteConfig</span></span>](./Set-AzureRmRouteConfig.md)



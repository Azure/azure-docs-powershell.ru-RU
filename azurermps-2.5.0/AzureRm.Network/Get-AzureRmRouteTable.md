---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 4F487FCA-930D-4D56-8D28-7693312E1A01
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermroutetable
schema: 2.0.0
ms.openlocfilehash: 9498b93d2062bc84d6af423c89eb351c6680eddd
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913451"
---
# <span data-ttu-id="93622-101">Get-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="93622-101">Get-AzureRmRouteTable</span></span>

## <span data-ttu-id="93622-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="93622-102">SYNOPSIS</span></span>
<span data-ttu-id="93622-103">Возвращает таблицы маршрутов.</span><span class="sxs-lookup"><span data-stu-id="93622-103">Gets route tables.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="93622-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="93622-104">SYNTAX</span></span>

### <span data-ttu-id="93622-105">Кройте</span><span class="sxs-lookup"><span data-stu-id="93622-105">Expand</span></span>
```
Get-AzureRmRouteTable -ResourceGroupName <String> -Name <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="93622-106">NOEXPAND</span><span class="sxs-lookup"><span data-stu-id="93622-106">NoExpand</span></span>
```
Get-AzureRmRouteTable [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="93622-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="93622-107">DESCRIPTION</span></span>
<span data-ttu-id="93622-108">Командлет **Get-AzureRmRouteTable** получает таблицы маршрутов Azure.</span><span class="sxs-lookup"><span data-stu-id="93622-108">The **Get-AzureRmRouteTable** cmdlet gets Azure route tables.</span></span>
<span data-ttu-id="93622-109">Вы можете получить одну таблицу маршрутов или получить все таблицы маршрутов в группе ресурсов или в вашей подписке.</span><span class="sxs-lookup"><span data-stu-id="93622-109">You can get a single route table, or get all the route tables in a resource group or in your subscription.</span></span>

## <span data-ttu-id="93622-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="93622-110">EXAMPLES</span></span>

### <span data-ttu-id="93622-111">Пример 1: получение таблицы маршрутов</span><span class="sxs-lookup"><span data-stu-id="93622-111">Example 1: Get a route table</span></span>
```
PS C:\>Get-AzureRmRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01"
Name              : routetable01
ResourceGroupName : ResourceGroup11
Location          : eastus
Id                : /subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Microsoft.Networ
                    k/routeTables/routetable01
Etag              : W/"db5f4e12-3f34-465b-92dd-0ab3bf6fc274"
ProvisioningState : Succeeded
Tags              : 
Routes            : [
                      {
                        "Name": "route07",
                        "Etag": "W/\"db5f4e12-3f34-465b-92dd-0ab3bf6fc274\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/routeTables/routetable01/routes/route07",
                        "AddressPrefix": "10.1.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      }
                    ] 
Subnets           : []
```

<span data-ttu-id="93622-112">Эта команда получает таблицу маршрутов с именем RouteTable01 в группе ресурсов с именем ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="93622-112">This command gets the route table named RouteTable01 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="93622-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="93622-113">PARAMETERS</span></span>

### <span data-ttu-id="93622-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93622-114">-DefaultProfile</span></span>
<span data-ttu-id="93622-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="93622-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="93622-116">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="93622-116">-ExpandResource</span></span>
```yaml
Type: String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93622-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="93622-117">-Name</span></span>
<span data-ttu-id="93622-118">Указывает имя таблицы маршрутов, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="93622-118">Specifies the name of the route table that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93622-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93622-119">-ResourceGroupName</span></span>
<span data-ttu-id="93622-120">Указывает имя группы ресурсов, содержащей таблицы маршрутов, которые получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="93622-120">Specifies the name of the resource group that contains the route tables that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: NoExpand
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93622-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93622-121">CommonParameters</span></span>
<span data-ttu-id="93622-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="93622-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93622-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93622-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93622-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="93622-124">INPUTS</span></span>

## <span data-ttu-id="93622-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="93622-125">OUTPUTS</span></span>

### <span data-ttu-id="93622-126">Microsoft. Azure. Commands. Network. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="93622-126">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="93622-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="93622-127">NOTES</span></span>

## <span data-ttu-id="93622-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="93622-128">RELATED LINKS</span></span>

[<span data-ttu-id="93622-129">New-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="93622-129">New-AzureRmRouteTable</span></span>](./New-AzureRmRouteTable.md)

[<span data-ttu-id="93622-130">Remove-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="93622-130">Remove-AzureRmRouteTable</span></span>](./Remove-AzureRmRouteTable.md)

[<span data-ttu-id="93622-131">Set-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="93622-131">Set-AzureRmRouteTable</span></span>](./Set-AzureRmRouteTable.md)



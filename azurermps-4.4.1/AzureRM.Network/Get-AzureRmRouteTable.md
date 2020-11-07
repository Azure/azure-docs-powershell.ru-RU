---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 4F487FCA-930D-4D56-8D28-7693312E1A01
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmRouteTable.md
ms.openlocfilehash: fb675f1d834160bd1fcf5e2dde60dc00e697d629
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732763"
---
# <span data-ttu-id="035af-101">Get-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="035af-101">Get-AzureRmRouteTable</span></span>

## <span data-ttu-id="035af-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="035af-102">SYNOPSIS</span></span>
<span data-ttu-id="035af-103">Возвращает таблицы маршрутов.</span><span class="sxs-lookup"><span data-stu-id="035af-103">Gets route tables.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="035af-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="035af-104">SYNTAX</span></span>

### <span data-ttu-id="035af-105">NOEXPAND</span><span class="sxs-lookup"><span data-stu-id="035af-105">NoExpand</span></span>
```
Get-AzureRmRouteTable [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="035af-106">Кройте</span><span class="sxs-lookup"><span data-stu-id="035af-106">Expand</span></span>
```
Get-AzureRmRouteTable -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="035af-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="035af-107">DESCRIPTION</span></span>
<span data-ttu-id="035af-108">Командлет **Get-AzureRmRouteTable** получает таблицы маршрутов Azure.</span><span class="sxs-lookup"><span data-stu-id="035af-108">The **Get-AzureRmRouteTable** cmdlet gets Azure route tables.</span></span>
<span data-ttu-id="035af-109">Вы можете получить одну таблицу маршрутов или получить все таблицы маршрутов в группе ресурсов или в вашей подписке.</span><span class="sxs-lookup"><span data-stu-id="035af-109">You can get a single route table, or get all the route tables in a resource group or in your subscription.</span></span>

## <span data-ttu-id="035af-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="035af-110">EXAMPLES</span></span>

### <span data-ttu-id="035af-111">Пример 1: получение таблицы маршрутов</span><span class="sxs-lookup"><span data-stu-id="035af-111">Example 1: Get a route table</span></span>
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

<span data-ttu-id="035af-112">Эта команда получает таблицу маршрутов с именем RouteTable01 в группе ресурсов с именем ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="035af-112">This command gets the route table named RouteTable01 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="035af-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="035af-113">PARAMETERS</span></span>

### <span data-ttu-id="035af-114">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="035af-114">-ExpandResource</span></span>
```yaml
Type: System.String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="035af-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="035af-115">-Name</span></span>
<span data-ttu-id="035af-116">Указывает имя таблицы маршрутов, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="035af-116">Specifies the name of the route table that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="035af-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="035af-117">-ResourceGroupName</span></span>
<span data-ttu-id="035af-118">Указывает имя группы ресурсов, содержащей таблицы маршрутов, которые получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="035af-118">Specifies the name of the resource group that contains the route tables that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="035af-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="035af-119">-DefaultProfile</span></span>
<span data-ttu-id="035af-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="035af-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="035af-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="035af-121">CommonParameters</span></span>
<span data-ttu-id="035af-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="035af-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="035af-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="035af-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="035af-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="035af-124">INPUTS</span></span>

## <span data-ttu-id="035af-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="035af-125">OUTPUTS</span></span>

### <span data-ttu-id="035af-126">Microsoft. Azure. Commands. Network. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="035af-126">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="035af-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="035af-127">NOTES</span></span>

## <span data-ttu-id="035af-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="035af-128">RELATED LINKS</span></span>

[<span data-ttu-id="035af-129">New-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="035af-129">New-AzureRmRouteTable</span></span>](./New-AzureRmRouteTable.md)

[<span data-ttu-id="035af-130">Remove-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="035af-130">Remove-AzureRmRouteTable</span></span>](./Remove-AzureRmRouteTable.md)

[<span data-ttu-id="035af-131">Set-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="035af-131">Set-AzureRmRouteTable</span></span>](./Set-AzureRmRouteTable.md)



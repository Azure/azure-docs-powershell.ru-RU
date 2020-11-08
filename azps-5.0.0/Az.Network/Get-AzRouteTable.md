---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4F487FCA-930D-4D56-8D28-7693312E1A01
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteTable.md
ms.openlocfilehash: 613519f6d9d3d2d8ce1c83ff0ad5a2d9421859b8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249691"
---
# <span data-ttu-id="8c051-101">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="8c051-101">Get-AzRouteTable</span></span>

## <span data-ttu-id="8c051-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8c051-102">SYNOPSIS</span></span>
<span data-ttu-id="8c051-103">Возвращает таблицы маршрутов.</span><span class="sxs-lookup"><span data-stu-id="8c051-103">Gets route tables.</span></span>

## <span data-ttu-id="8c051-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8c051-104">SYNTAX</span></span>

### <span data-ttu-id="8c051-105">NOEXPAND (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8c051-105">NoExpand (Default)</span></span>
```
Get-AzRouteTable [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8c051-106">Кройте</span><span class="sxs-lookup"><span data-stu-id="8c051-106">Expand</span></span>
```
Get-AzRouteTable -ResourceGroupName <String> -Name <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8c051-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8c051-107">DESCRIPTION</span></span>
<span data-ttu-id="8c051-108">Командлет **Get-AzRouteTable** получает таблицы маршрутов Azure.</span><span class="sxs-lookup"><span data-stu-id="8c051-108">The **Get-AzRouteTable** cmdlet gets Azure route tables.</span></span>
<span data-ttu-id="8c051-109">Вы можете получить одну таблицу маршрутов или получить все таблицы маршрутов в группе ресурсов или в вашей подписке.</span><span class="sxs-lookup"><span data-stu-id="8c051-109">You can get a single route table, or get all the route tables in a resource group or in your subscription.</span></span>

## <span data-ttu-id="8c051-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8c051-110">EXAMPLES</span></span>

### <span data-ttu-id="8c051-111">Пример 1: получение таблицы маршрутов</span><span class="sxs-lookup"><span data-stu-id="8c051-111">Example 1: Get a route table</span></span>
```
PS C:\> Get-AzRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01"

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

<span data-ttu-id="8c051-112">Эта команда получает таблицу маршрутов с именем RouteTable01 в группе ресурсов с именем ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="8c051-112">This command gets the route table named RouteTable01 in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="8c051-113">Пример 2: перечисление таблиц маршрутов с помощью фильтрации</span><span class="sxs-lookup"><span data-stu-id="8c051-113">Example 2: List route tables using filtering</span></span>
```
PS C:\> Get-AzRouteTable -Name RouteTable*

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

Name              : routetable02
ResourceGroupName : ResourceGroup11
Location          : eastus
Id                : /subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Microsoft.Networ
                    k/routeTables/routetable02
Etag              : W/"db5f4e12-3f34-465b-92dd-0ab3bf6fc274"
ProvisioningState : Succeeded
Tags              : 
Routes            : [
                      {
                        "Name": "route07",
                        "Etag": "W/\"db5f4e12-3f34-465b-92dd-0ab3bf6fc274\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/routeTables/routetable02/routes/route07",
                        "AddressPrefix": "10.1.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      }
                    ] 
Subnets           : []
```

<span data-ttu-id="8c051-114">Эта команда получает все таблицы маршрутов, имя которых начинается с "RouteTable"</span><span class="sxs-lookup"><span data-stu-id="8c051-114">This command gets all route tables whose name starts with "RouteTable"</span></span>

## <span data-ttu-id="8c051-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8c051-115">PARAMETERS</span></span>

### <span data-ttu-id="8c051-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c051-116">-DefaultProfile</span></span>
<span data-ttu-id="8c051-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8c051-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c051-118">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="8c051-118">-ExpandResource</span></span>
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

### <span data-ttu-id="8c051-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8c051-119">-Name</span></span>
<span data-ttu-id="8c051-120">Указывает имя таблицы маршрутов, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="8c051-120">Specifies the name of the route table that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="8c051-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c051-121">-ResourceGroupName</span></span>
<span data-ttu-id="8c051-122">Указывает имя группы ресурсов, содержащей таблицы маршрутов, которые получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="8c051-122">Specifies the name of the resource group that contains the route tables that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="8c051-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c051-123">CommonParameters</span></span>
<span data-ttu-id="8c051-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8c051-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c051-125">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8c051-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c051-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8c051-126">INPUTS</span></span>

### <span data-ttu-id="8c051-127">System. String</span><span class="sxs-lookup"><span data-stu-id="8c051-127">System.String</span></span>

## <span data-ttu-id="8c051-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8c051-128">OUTPUTS</span></span>

### <span data-ttu-id="8c051-129">Microsoft. Azure. Commands. Network. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="8c051-129">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="8c051-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="8c051-130">NOTES</span></span>

## <span data-ttu-id="8c051-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8c051-131">RELATED LINKS</span></span>

[<span data-ttu-id="8c051-132">New-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="8c051-132">New-AzRouteTable</span></span>](./New-AzRouteTable.md)

[<span data-ttu-id="8c051-133">Remove-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="8c051-133">Remove-AzRouteTable</span></span>](./Remove-AzRouteTable.md)

[<span data-ttu-id="8c051-134">Set-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="8c051-134">Set-AzRouteTable</span></span>](./Set-AzRouteTable.md)



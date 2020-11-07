---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4F487FCA-930D-4D56-8D28-7693312E1A01
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzRouteTable.md
ms.openlocfilehash: a881e438166729aea8956dc633b7a635499d3752
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93909866"
---
# <span data-ttu-id="313b0-101">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="313b0-101">Get-AzRouteTable</span></span>

## <span data-ttu-id="313b0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="313b0-102">SYNOPSIS</span></span>
<span data-ttu-id="313b0-103">Возвращает таблицы маршрутов.</span><span class="sxs-lookup"><span data-stu-id="313b0-103">Gets route tables.</span></span>

## <span data-ttu-id="313b0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="313b0-104">SYNTAX</span></span>

### <span data-ttu-id="313b0-105">Кройте</span><span class="sxs-lookup"><span data-stu-id="313b0-105">Expand</span></span>
```
Get-AzRouteTable -ResourceGroupName <String> -Name <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="313b0-106">NOEXPAND</span><span class="sxs-lookup"><span data-stu-id="313b0-106">NoExpand</span></span>
```
Get-AzRouteTable [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="313b0-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="313b0-107">DESCRIPTION</span></span>
<span data-ttu-id="313b0-108">Командлет **Get-AzRouteTable** получает таблицы маршрутов Azure.</span><span class="sxs-lookup"><span data-stu-id="313b0-108">The **Get-AzRouteTable** cmdlet gets Azure route tables.</span></span>
<span data-ttu-id="313b0-109">Вы можете получить одну таблицу маршрутов или получить все таблицы маршрутов в группе ресурсов или в вашей подписке.</span><span class="sxs-lookup"><span data-stu-id="313b0-109">You can get a single route table, or get all the route tables in a resource group or in your subscription.</span></span>

## <span data-ttu-id="313b0-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="313b0-110">EXAMPLES</span></span>

### <span data-ttu-id="313b0-111">Пример 1: получение таблицы маршрутов</span><span class="sxs-lookup"><span data-stu-id="313b0-111">Example 1: Get a route table</span></span>
```
PS C:\>Get-AzRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01"
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

<span data-ttu-id="313b0-112">Эта команда получает таблицу маршрутов с именем RouteTable01 в группе ресурсов с именем ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="313b0-112">This command gets the route table named RouteTable01 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="313b0-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="313b0-113">PARAMETERS</span></span>

### <span data-ttu-id="313b0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="313b0-114">-DefaultProfile</span></span>
<span data-ttu-id="313b0-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="313b0-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="313b0-116">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="313b0-116">-ExpandResource</span></span>
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

### <span data-ttu-id="313b0-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="313b0-117">-Name</span></span>
<span data-ttu-id="313b0-118">Указывает имя таблицы маршрутов, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="313b0-118">Specifies the name of the route table that this cmdlet gets.</span></span>

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

### <span data-ttu-id="313b0-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="313b0-119">-ResourceGroupName</span></span>
<span data-ttu-id="313b0-120">Указывает имя группы ресурсов, содержащей таблицы маршрутов, которые получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="313b0-120">Specifies the name of the resource group that contains the route tables that this cmdlet gets.</span></span>

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

### <span data-ttu-id="313b0-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="313b0-121">CommonParameters</span></span>
<span data-ttu-id="313b0-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="313b0-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="313b0-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="313b0-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="313b0-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="313b0-124">INPUTS</span></span>

## <span data-ttu-id="313b0-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="313b0-125">OUTPUTS</span></span>

### <span data-ttu-id="313b0-126">Microsoft. Azure. Commands. Network. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="313b0-126">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="313b0-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="313b0-127">NOTES</span></span>

## <span data-ttu-id="313b0-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="313b0-128">RELATED LINKS</span></span>

[<span data-ttu-id="313b0-129">New-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="313b0-129">New-AzRouteTable</span></span>](./New-AzRouteTable.md)

[<span data-ttu-id="313b0-130">Remove-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="313b0-130">Remove-AzRouteTable</span></span>](./Remove-AzRouteTable.md)

[<span data-ttu-id="313b0-131">Set-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="313b0-131">Set-AzRouteTable</span></span>](./Set-AzRouteTable.md)



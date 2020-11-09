---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualHubRouteTable.md
ms.openlocfilehash: bc93ba739a622a97f418dd7e01d4bbdc7d6824dc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248577"
---
# <span data-ttu-id="2689e-101">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="2689e-101">Get-AzVirtualHubRouteTable</span></span>

## <span data-ttu-id="2689e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2689e-102">SYNOPSIS</span></span>
<span data-ttu-id="2689e-103">Возвращает таблицу виртуальных маршрутизаторов виртуального концентратора в виртуальном концентраторе или список всех таблиц маршрутов в виртуальном концентраторе.</span><span class="sxs-lookup"><span data-stu-id="2689e-103">Gets a Virtual Hub Route Table in a virtual hub or lists all route tables in a virtual hub.</span></span>

## <span data-ttu-id="2689e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2689e-104">SYNTAX</span></span>

### <span data-ttu-id="2689e-105">ByVirtualHubName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2689e-105">ByVirtualHubName (Default)</span></span>
```
Get-AzVirtualHubRouteTable -ResourceGroupName <String> -HubName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2689e-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="2689e-106">ByVirtualHubObject</span></span>
```
Get-AzVirtualHubRouteTable -VirtualHub <PSVirtualHub> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2689e-107">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="2689e-107">ByVirtualHubResourceId</span></span>
```
Get-AzVirtualHubRouteTable -ParentResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2689e-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2689e-108">DESCRIPTION</span></span>
<span data-ttu-id="2689e-109">Возвращает таблицу виртуальных маршрутизаторов виртуального концентратора в виртуальном концентраторе или список всех таблиц маршрутов в виртуальном концентраторе.</span><span class="sxs-lookup"><span data-stu-id="2689e-109">Gets a Virtual Hub Route Table in a virtual hub or lists all route tables in a virtual hub.</span></span>

## <span data-ttu-id="2689e-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2689e-110">EXAMPLES</span></span>

### <span data-ttu-id="2689e-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2689e-111">Example 1</span></span>
```powershell
PS C:\> Get-AzVirtualHubRouteTable�-ResourceGroupName�"testRg"�-HubName�"westushub"�-Name�"routeTable1"

Name                : routeTable1
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/westushub/routeTables/routeTable1
Routes              : {Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute}
Connections : {All_Vnets}
ProvisioningState   : Succeeded
```

<span data-ttu-id="2689e-112">Этот командлет извлекает ресурс таблицы маршрутов с помощью имени группы ресурсов, имени концентратора и имени таблицы маршрута.</span><span class="sxs-lookup"><span data-stu-id="2689e-112">This cmdlet retrieves a route table resource using resource group name, hub name and the route table name.</span></span>

### <span data-ttu-id="2689e-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="2689e-113">Example 2</span></span>
```powershell
PS C:\> Get-AzVirtualHubRouteTable�-ResourceGroupName�"testRg"�-HubName�"westushub"

Name                : routeTable1
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/westushub/routeTables/routeTable1
Routes              : {Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute}
Connections : {All_Vnets}
ProvisioningState   : Succeeded

Name                : routeTable2
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/westushub/routeTables/routeTable2
Routes              : {Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute}
Connections : {All_Branches}
ProvisioningState   : Succeeded
```

<span data-ttu-id="2689e-114">Этот командлет перечисляет все таблицы маршрутов, представленные на виртуальном концентраторе, используя имя группы ресурсов и имя концентратора.</span><span class="sxs-lookup"><span data-stu-id="2689e-114">This cmdlet lists all route tables present in a virtual hub using resource group name and the hub name.</span></span>

## <span data-ttu-id="2689e-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2689e-115">PARAMETERS</span></span>

### <span data-ttu-id="2689e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2689e-116">-DefaultProfile</span></span>
<span data-ttu-id="2689e-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2689e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2689e-118">-HubName</span><span class="sxs-lookup"><span data-stu-id="2689e-118">-HubName</span></span>
<span data-ttu-id="2689e-119">Имя родительского ресурса.</span><span class="sxs-lookup"><span data-stu-id="2689e-119">The parent resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubName
Aliases: VirtualHubName, ParentVirtualHubName, ParentResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2689e-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2689e-120">-Name</span></span>
<span data-ttu-id="2689e-121">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="2689e-121">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, VirtualHubRouteTableName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2689e-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="2689e-122">-ParentResourceId</span></span>
<span data-ttu-id="2689e-123">Родительский идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="2689e-123">The parent resource id.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubResourceId
Aliases: VirtualHubId, ParentVirtualHubId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2689e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2689e-124">-ResourceGroupName</span></span>
<span data-ttu-id="2689e-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2689e-125">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2689e-126">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="2689e-126">-VirtualHub</span></span>
<span data-ttu-id="2689e-127">Родительский ресурс.</span><span class="sxs-lookup"><span data-stu-id="2689e-127">The parent resource.</span></span>

```yaml
Type: PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases: ParentObject, ParentVirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2689e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2689e-128">CommonParameters</span></span>
<span data-ttu-id="2689e-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2689e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2689e-130">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2689e-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2689e-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2689e-131">INPUTS</span></span>

### <span data-ttu-id="2689e-132">Microsoft. Azure. Commands. Network. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="2689e-132">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="2689e-133">System. String</span><span class="sxs-lookup"><span data-stu-id="2689e-133">System.String</span></span>

## <span data-ttu-id="2689e-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2689e-134">OUTPUTS</span></span>

### <span data-ttu-id="2689e-135">Microsoft. Azure. Commands. Network. Models. PSVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="2689e-135">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable</span></span>

## <span data-ttu-id="2689e-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="2689e-136">NOTES</span></span>

## <span data-ttu-id="2689e-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2689e-137">RELATED LINKS</span></span>
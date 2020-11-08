---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azprivateendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpoint.md
ms.openlocfilehash: 9535e5858f1c7621745035a28c45f932cd943bc1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073304"
---
# <span data-ttu-id="ec80d-101">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="ec80d-101">Get-AzPrivateEndpoint</span></span>

## <span data-ttu-id="ec80d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ec80d-102">SYNOPSIS</span></span>
<span data-ttu-id="ec80d-103">Получение закрытой конечной точки</span><span class="sxs-lookup"><span data-stu-id="ec80d-103">Get a private endpoint</span></span>

## <span data-ttu-id="ec80d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ec80d-104">SYNTAX</span></span>

### <span data-ttu-id="ec80d-105">NOEXPAND (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ec80d-105">NoExpand (Default)</span></span>
```
Get-AzPrivateEndpoint [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ec80d-106">Кройте</span><span class="sxs-lookup"><span data-stu-id="ec80d-106">Expand</span></span>
```
Get-AzPrivateEndpoint -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ec80d-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ec80d-107">DESCRIPTION</span></span>
<span data-ttu-id="ec80d-108">Командлет **Get-AzPrivateEndpoint** получает одну или несколько закрытых конечных точек.</span><span class="sxs-lookup"><span data-stu-id="ec80d-108">The **Get-AzPrivateEndpoint** cmdlet gets one or more private endpoints.</span></span>

## <span data-ttu-id="ec80d-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ec80d-109">EXAMPLES</span></span>

### <span data-ttu-id="ec80d-110">1: получение частной конечной точки</span><span class="sxs-lookup"><span data-stu-id="ec80d-110">1: Retrieve a private endpoint</span></span>
```
Get-AzPrivateEndpoint -Name MyPrivateEndpoint1 -ResourceGroupName TestResourceGroup

Name                                : MyPrivateEndpoint1
ResourceGroupName                   : TestResourceGroup
Location                            : eastus2euap
Id                                  : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/provi
                                      ders/Microsoft.Network/privateEndpoints/MyPrivateEndpoint1
Etag                                : W/"00000000-0000-0000-0000-000000000000"
ProvisioningState                   : Succeeded
Subnet                              : {
                                        "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork1/subnets/backendSubnet",
                                      }
NetworkInterfaces                   : [
                                        {

                                          "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/networkInterfaces/MyNic1",
                                        }
                                      ]
PrivateLinkServiceConnections       : []
ManualPrivateLinkServiceConnections : [
                                        {
                                          "Name": "MyPrivateLinkServiceConnection",
                                          "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/privateEndpoints/MyPrivateEndpoint1/manualPrivateLinkServi
                                      ceConnections/MyPrivateLinkServiceConnection",
                                          "PrivateLinkServiceId": "/subscriptions/00000000-0000-0000-0000-000000000000/
                                      resourceGroups/TestResourceGroup/providers/Microsoft.Network/priv
                                      ateLinkServices/MyPrivateLinkService",
                                          "PrivateLinkServiceConnectionState": {
                                            "Status": "Pending",
                                            "Description": "Awaiting approval"
                                          }
                                        }
                                      ]
```

<span data-ttu-id="ec80d-111">Эта команда получает частную конечную точку с именем MyPrivateEndpoint1 в группе ресурсов TestResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ec80d-111">This command gets the private endpoint named MyPrivateEndpoint1 in the resource group TestResourceGroup</span></span>

### <span data-ttu-id="ec80d-112">2: Перечислите все закрытые конечные точки в ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="ec80d-112">2: List all private endpoints in ResourceGroup</span></span>
```
Get-AzPrivateEndpoint -ResourceGroupName TestResourceGroup

Name                                : MyPrivateEndpoint1
ResourceGroupName                   : TestResourceGroup
Location                            : eastus2euap
Id                                  : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/provi
                                      ders/Microsoft.Network/privateEndpoints/MyPrivateEndpoint1
Etag                                : W/"00000000-0000-0000-0000-000000000000"
ProvisioningState                   : Succeeded
Subnet                              : {
                                        "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork1/subnets/backendSubnet",
                                      }
NetworkInterfaces                   : [
                                        {

                                          "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/networkInterfaces/MyNic1",
                                        }
                                      ]
PrivateLinkServiceConnections       : []
ManualPrivateLinkServiceConnections : [
                                        {
                                          "Name": "MyPrivateLinkServiceConnection",
                                          "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/privateEndpoints/MyPrivateEndpoint1/manualPrivateLinkServi
                                      ceConnections/MyPrivateLinkServiceConnection",
                                          "PrivateLinkServiceId": "/subscriptions/00000000-0000-0000-0000-000000000000/
                                      resourceGroups/TestResourceGroup/providers/Microsoft.Network/priv
                                      ateLinkServices/MyPrivateLinkService",
                                          "PrivateLinkServiceConnectionState": {
                                            "Status": "Pending",
                                            "Description": "Awaiting approval"
                                          }
                                        }
                                      ]
```

<span data-ttu-id="ec80d-113">Эта команда получает все закрытые конечные точки в группе ресурсов TestResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ec80d-113">This command gets all of private end points in the resource group TestResourceGroup</span></span>

## <span data-ttu-id="ec80d-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ec80d-114">PARAMETERS</span></span>

### <span data-ttu-id="ec80d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec80d-115">-DefaultProfile</span></span>
<span data-ttu-id="ec80d-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ec80d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec80d-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="ec80d-117">-ExpandResource</span></span>
<span data-ttu-id="ec80d-118">Развернутая ссылка на ресурс.</span><span class="sxs-lookup"><span data-stu-id="ec80d-118">The resource reference to be expanded.</span></span>

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

### <span data-ttu-id="ec80d-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ec80d-119">-Name</span></span>
<span data-ttu-id="ec80d-120">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="ec80d-120">The resource name.</span></span>

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

### <span data-ttu-id="ec80d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec80d-121">-ResourceGroupName</span></span>
<span data-ttu-id="ec80d-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ec80d-122">The resource group name.</span></span>

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

### <span data-ttu-id="ec80d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec80d-123">CommonParameters</span></span>
<span data-ttu-id="ec80d-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ec80d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec80d-125">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ec80d-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec80d-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ec80d-126">INPUTS</span></span>

### <span data-ttu-id="ec80d-127">System. String</span><span class="sxs-lookup"><span data-stu-id="ec80d-127">System.String</span></span>

## <span data-ttu-id="ec80d-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ec80d-128">OUTPUTS</span></span>

### <span data-ttu-id="ec80d-129">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ec80d-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="ec80d-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="ec80d-130">NOTES</span></span>

## <span data-ttu-id="ec80d-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ec80d-131">RELATED LINKS</span></span>

[<span data-ttu-id="ec80d-132">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="ec80d-132">New-AzPrivateEndpoint</span></span>](./New-AzPrivateEndpoint.md)

[<span data-ttu-id="ec80d-133">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="ec80d-133">Remove-AzPrivateEndpoint</span></span>](./Remove-AzPrivateEndpoint.md)
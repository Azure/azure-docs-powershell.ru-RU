---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azprivateendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpoint.md
ms.openlocfilehash: 11a0b65118fc9b580a885510f1e5ffa337b1d2e0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100223788"
---
# <span data-ttu-id="b0053-101">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="b0053-101">Get-AzPrivateEndpoint</span></span>

## <span data-ttu-id="b0053-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0053-102">SYNOPSIS</span></span>
<span data-ttu-id="b0053-103">Получить частную конечную точку</span><span class="sxs-lookup"><span data-stu-id="b0053-103">Get a private endpoint</span></span>

## <span data-ttu-id="b0053-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b0053-104">SYNTAX</span></span>

### <span data-ttu-id="b0053-105">NoExpand (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b0053-105">NoExpand (Default)</span></span>
```
Get-AzPrivateEndpoint [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b0053-106">Развернуть</span><span class="sxs-lookup"><span data-stu-id="b0053-106">Expand</span></span>
```
Get-AzPrivateEndpoint -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b0053-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b0053-107">DESCRIPTION</span></span>
<span data-ttu-id="b0053-108">Для получения одной или более частных конечных точек **возвращается cmdlet Get-AzPrivateEndpoint.**</span><span class="sxs-lookup"><span data-stu-id="b0053-108">The **Get-AzPrivateEndpoint** cmdlet gets one or more private endpoints.</span></span>

## <span data-ttu-id="b0053-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b0053-109">EXAMPLES</span></span>

### <span data-ttu-id="b0053-110">Пример 1. Извлечение закрытой конечной точки</span><span class="sxs-lookup"><span data-stu-id="b0053-110">Example 1: Retrieve a private endpoint</span></span>
```powershell
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

<span data-ttu-id="b0053-111">Эта команда получает частную конечную точку MyPrivateEndpoint1 в группе ресурсов TestResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="b0053-111">This command gets the private endpoint named MyPrivateEndpoint1 in the resource group TestResourceGroup</span></span>

### <span data-ttu-id="b0053-112">Пример 2. Список всех частных конечных точек в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="b0053-112">Example 2: List all private endpoints in ResourceGroup</span></span>
```powershell
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

<span data-ttu-id="b0053-113">Эта команда получает все личные конечные точки в группе ресурсов TestResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b0053-113">This command gets all of private end points in the resource group TestResourceGroup</span></span>

## <span data-ttu-id="b0053-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b0053-114">PARAMETERS</span></span>

### <span data-ttu-id="b0053-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0053-115">-DefaultProfile</span></span>
<span data-ttu-id="b0053-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b0053-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0053-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="b0053-117">-ExpandResource</span></span>
<span data-ttu-id="b0053-118">Ссылка на ресурсы, которая будет расширена.</span><span class="sxs-lookup"><span data-stu-id="b0053-118">The resource reference to be expanded.</span></span>

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

### <span data-ttu-id="b0053-119">-Name</span><span class="sxs-lookup"><span data-stu-id="b0053-119">-Name</span></span>
<span data-ttu-id="b0053-120">Имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="b0053-120">The resource name.</span></span>

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

### <span data-ttu-id="b0053-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0053-121">-ResourceGroupName</span></span>
<span data-ttu-id="b0053-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b0053-122">The resource group name.</span></span>

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

### <span data-ttu-id="b0053-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0053-123">CommonParameters</span></span>
<span data-ttu-id="b0053-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0053-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0053-125">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b0053-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0053-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b0053-126">INPUTS</span></span>

### <span data-ttu-id="b0053-127">System.String</span><span class="sxs-lookup"><span data-stu-id="b0053-127">System.String</span></span>

## <span data-ttu-id="b0053-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b0053-128">OUTPUTS</span></span>

### <span data-ttu-id="b0053-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b0053-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="b0053-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b0053-130">NOTES</span></span>

## <span data-ttu-id="b0053-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b0053-131">RELATED LINKS</span></span>

[<span data-ttu-id="b0053-132">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="b0053-132">New-AzPrivateEndpoint</span></span>](./New-AzPrivateEndpoint.md)

[<span data-ttu-id="b0053-133">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="b0053-133">Remove-AzPrivateEndpoint</span></span>](./Remove-AzPrivateEndpoint.md)
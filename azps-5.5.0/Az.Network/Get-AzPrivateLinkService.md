---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkService.md
ms.openlocfilehash: fdbb023c6796a780bfe9e6474191185a58489c91
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100218780"
---
# <span data-ttu-id="ca5da-101">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="ca5da-101">Get-AzPrivateLinkService</span></span>

## <span data-ttu-id="ca5da-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca5da-102">SYNOPSIS</span></span>
<span data-ttu-id="ca5da-103">Получает личную службу ссылок</span><span class="sxs-lookup"><span data-stu-id="ca5da-103">Gets private link service</span></span>

## <span data-ttu-id="ca5da-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ca5da-104">SYNTAX</span></span>

### <span data-ttu-id="ca5da-105">NoExpand (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ca5da-105">NoExpand (Default)</span></span>
```
Get-AzPrivateLinkService [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ca5da-106">Развернуть</span><span class="sxs-lookup"><span data-stu-id="ca5da-106">Expand</span></span>
```
Get-AzPrivateLinkService -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ca5da-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ca5da-107">DESCRIPTION</span></span>
<span data-ttu-id="ca5da-108">Для получения одной или более **частных** служб ссылок можно получить одну или несколько личных служб.</span><span class="sxs-lookup"><span data-stu-id="ca5da-108">The **Get-AzPrivateLinkService** cmdlet gets one or more private link services.</span></span>

## <span data-ttu-id="ca5da-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ca5da-109">EXAMPLES</span></span>

### <span data-ttu-id="ca5da-110">Пример</span><span class="sxs-lookup"><span data-stu-id="ca5da-110">Example</span></span>
```
Get-AzPrivateLinkService -Name MyPLS -ResourceGroupName TestResourceGroup

Name                                 : MyPLS
ResourceGroupName                    : TestResourceGroup
Id                                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/prov
                                       iders/Microsoft.Network/privateLinkServices/MyPLS
Location                             : eastus2euap
Type                                 : Microsoft.Network/privateLinkServices
Etag                                 : W/"00000000-0000-0000-0000-000000000000"
Tag                                  : {}
ProvisioningState                    : Succeeded
Visibility                           : 
AutoApproval                         : 
Alias                                :
LoadBalancerFrontendIpConfigurations : []
IpConfigurations                     : [
                                         {
                                           "PrivateIPAddress": "10.0.2.5",
                                           "PrivateIPAllocationMethod": "Static",
                                           "ProvisioningState": "Failed",
                                           "PrivateIPAddressVersion": "IPv4",
                                           "Name": "IP-Config",
                                           "Subnet": {
                                             "Delegations": [],
                                             "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/
                                       TestResourceGroup/providers/Microsoft.Network/virtualNetworks/myvnet/subnets/backendSubne
                                       t",
                                             "ServiceAssociationLinks": []
                                           }
                                         }
                                       ]
PrivateEndpointConnections           : []
NetworkInterfaces                    : [
                                         {
                                           "TapConfigurations": [],
                                           "HostedWorkloads": [],
                                           "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/networkInterfaces/mytestinterface"
                                         }
                                       ]
```

<span data-ttu-id="ca5da-111">Этот командлет получает частную службу ссылок в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ca5da-111">This commandlet gets a private link service in the resource group.</span></span>

## <span data-ttu-id="ca5da-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ca5da-112">PARAMETERS</span></span>

### <span data-ttu-id="ca5da-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca5da-113">-DefaultProfile</span></span>
<span data-ttu-id="ca5da-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ca5da-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca5da-115">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="ca5da-115">-ExpandResource</span></span>
<span data-ttu-id="ca5da-116">Ссылка на ресурсы, которая должна быть расширена.</span><span class="sxs-lookup"><span data-stu-id="ca5da-116">The resource reference to be expanded.</span></span>

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

### <span data-ttu-id="ca5da-117">-Name</span><span class="sxs-lookup"><span data-stu-id="ca5da-117">-Name</span></span>
<span data-ttu-id="ca5da-118">Имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="ca5da-118">The resource name.</span></span>

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

### <span data-ttu-id="ca5da-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca5da-119">-ResourceGroupName</span></span>
<span data-ttu-id="ca5da-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ca5da-120">The resource group name.</span></span>

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

### <span data-ttu-id="ca5da-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca5da-121">CommonParameters</span></span>
<span data-ttu-id="ca5da-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca5da-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca5da-123">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ca5da-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca5da-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ca5da-124">INPUTS</span></span>

### <span data-ttu-id="ca5da-125">System.String</span><span class="sxs-lookup"><span data-stu-id="ca5da-125">System.String</span></span>

## <span data-ttu-id="ca5da-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ca5da-126">OUTPUTS</span></span>

### <span data-ttu-id="ca5da-127">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="ca5da-127">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="ca5da-128">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ca5da-128">NOTES</span></span>

## <span data-ttu-id="ca5da-129">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ca5da-129">RELATED LINKS</span></span>

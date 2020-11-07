---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkService.md
ms.openlocfilehash: 9f40d9ce99db8640fcf98d48f8dc3920a8517b3b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93902877"
---
# <span data-ttu-id="1aaff-101">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="1aaff-101">Get-AzPrivateLinkService</span></span>

## <span data-ttu-id="1aaff-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1aaff-102">SYNOPSIS</span></span>
<span data-ttu-id="1aaff-103">Возвращает службу частной ссылки</span><span class="sxs-lookup"><span data-stu-id="1aaff-103">Gets private link service</span></span>

## <span data-ttu-id="1aaff-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1aaff-104">SYNTAX</span></span>

### <span data-ttu-id="1aaff-105">NOEXPAND (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1aaff-105">NoExpand (Default)</span></span>
```
Get-AzPrivateLinkService [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1aaff-106">Кройте</span><span class="sxs-lookup"><span data-stu-id="1aaff-106">Expand</span></span>
```
Get-AzPrivateLinkService -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1aaff-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1aaff-107">DESCRIPTION</span></span>
<span data-ttu-id="1aaff-108">Командлет **Get-AzPrivateLinkService** получает одну или несколько служб частной связи.</span><span class="sxs-lookup"><span data-stu-id="1aaff-108">The **Get-AzPrivateLinkService** cmdlet gets one or more private link services.</span></span>

## <span data-ttu-id="1aaff-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1aaff-109">EXAMPLES</span></span>

### <span data-ttu-id="1aaff-110">Образом</span><span class="sxs-lookup"><span data-stu-id="1aaff-110">Example</span></span>
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

<span data-ttu-id="1aaff-111">Этот unifiedgroup Возвращает службу частной ссылки в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1aaff-111">This commandlet gets a private link service in the resource group.</span></span>

## <span data-ttu-id="1aaff-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1aaff-112">PARAMETERS</span></span>

### <span data-ttu-id="1aaff-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1aaff-113">-DefaultProfile</span></span>
<span data-ttu-id="1aaff-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1aaff-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1aaff-115">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="1aaff-115">-ExpandResource</span></span>
<span data-ttu-id="1aaff-116">Развернутая ссылка на ресурс.</span><span class="sxs-lookup"><span data-stu-id="1aaff-116">The resource reference to be expanded.</span></span>

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

### <span data-ttu-id="1aaff-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1aaff-117">-Name</span></span>
<span data-ttu-id="1aaff-118">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="1aaff-118">The resource name.</span></span>

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

### <span data-ttu-id="1aaff-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1aaff-119">-ResourceGroupName</span></span>
<span data-ttu-id="1aaff-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1aaff-120">The resource group name.</span></span>

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

### <span data-ttu-id="1aaff-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1aaff-121">CommonParameters</span></span>
<span data-ttu-id="1aaff-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1aaff-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1aaff-123">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1aaff-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1aaff-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1aaff-124">INPUTS</span></span>

### <span data-ttu-id="1aaff-125">System. String</span><span class="sxs-lookup"><span data-stu-id="1aaff-125">System.String</span></span>

## <span data-ttu-id="1aaff-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1aaff-126">OUTPUTS</span></span>

### <span data-ttu-id="1aaff-127">Microsoft. Azure. Commands. Network. Models. PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="1aaff-127">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="1aaff-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="1aaff-128">NOTES</span></span>

## <span data-ttu-id="1aaff-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1aaff-129">RELATED LINKS</span></span>

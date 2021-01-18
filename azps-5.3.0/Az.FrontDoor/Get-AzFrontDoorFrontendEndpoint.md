---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/get-azfrontdoorfrontendendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorFrontendEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorFrontendEndpoint.md
ms.openlocfilehash: cc07dd366d5c82705a23e3b9276ee9d681c6ae2c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504892"
---
# <span data-ttu-id="65b08-101">Get-AzFrontDoorFrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="65b08-101">Get-AzFrontDoorFrontendEndpoint</span></span>

## <span data-ttu-id="65b08-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65b08-102">SYNOPSIS</span></span>
<span data-ttu-id="65b08-103">Получите конечную точку переднего входа.</span><span class="sxs-lookup"><span data-stu-id="65b08-103">Get a front door frontend endpoint.</span></span>

## <span data-ttu-id="65b08-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="65b08-104">SYNTAX</span></span>

### <span data-ttu-id="65b08-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="65b08-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzFrontDoorFrontendEndpoint -ResourceGroupName <String> -FrontDoorName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="65b08-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="65b08-106">ByObjectParameterSet</span></span>
```
Get-AzFrontDoorFrontendEndpoint [-Name <String>] -FrontDoorObject <PSFrontDoor>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="65b08-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="65b08-107">ByResourceIdParameterSet</span></span>
```
Get-AzFrontDoorFrontendEndpoint -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="65b08-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="65b08-108">DESCRIPTION</span></span>
<span data-ttu-id="65b08-109">В **ресурсе Get-AzFrontDoorFrontendEndpoint** все существующие конечные точки переднего входа в ресурсе Front Door, совпадают с предоставленными сведениями.</span><span class="sxs-lookup"><span data-stu-id="65b08-109">The **Get-AzFrontDoorFrontendEndpoint** cmdlet gets all existing frontend endpoints in the current Front Door resource that matches provided information.</span></span>

## <span data-ttu-id="65b08-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="65b08-110">EXAMPLES</span></span>

### <span data-ttu-id="65b08-111">Пример 1. Получить все конечные точки переднего входа в front door "frontdoor1", который входит в группу ресурсов "rg1".</span><span class="sxs-lookup"><span data-stu-id="65b08-111">Example 1: Get all frontend endpoints in Front Door "frontdoor1" which is part of resource group "rg1".</span></span>
```powershell
PS C:\> Get-AzFrontDoorFrontendEndpoint -ResourceGroupName "rg1" -FrontDoorName "frontdoor1"


HostName                         : frontdoor1.azurefd.net
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Disabled
CustomHttpsProvisioningSubstate  : None
CertificateSource                :
ProtocolType                     :
Vault                            :
SecretName                       :
SecretVersion                    :
CertificateType                  :
ResourceState                    : Enabled
Id                               : /subscriptions/{guid}/resourcegroups/resourcegroup1
                                   /providers/Microsoft.Network/frontdoors/frontdoor1/frontendendpoints/frontdoor1-azurefd-net
Name                             : frontdoor1-azurefd-net
Type                             : Microsoft.Network/frontdoors/frontendendpoints

HostName                         : frontendpointname1.custom.xyz
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Disabled
CustomHttpsProvisioningSubstate  : None
CertificateSource                :
ProtocolType                     :
Vault                            :
SecretName                       :
SecretVersion                    :
CertificateType                  :
ResourceState                    : Enabled
Id                               : /subscriptions/{guid}/resourcegroups/resourcegroup1
                                   /providers/Microsoft.Network/frontdoors/frontdoor1/frontendendpoints/frontendpointname1-custom-xyz
Name                             : frontendpointname1-custom-xyz
Type                             : Microsoft.Network/frontdoors/frontendendpoints
```

<span data-ttu-id="65b08-112">Получить все конечные точки переднего входа в front door "frontdoor1", который входит в группу ресурсов "rg1".</span><span class="sxs-lookup"><span data-stu-id="65b08-112">Get all frontend endpoints in Front Door "frontdoor1" which is part of resource group "rg1".</span></span>

### <span data-ttu-id="65b08-113">Пример 2. Получите конечную точку переднего использования с именем "frontdoor1-azurefd-net" в front door "frontdoor1", которая входит в группу ресурсов "rg1"</span><span class="sxs-lookup"><span data-stu-id="65b08-113">Example 2: Get frontend endpoint with name "frontdoor1-azurefd-net" in Front Door "frontdoor1" which is part of resource group "rg1"</span></span>
```powershell
PS C:\> Get-AzFrontDoorFrontendEndpoint -ResourceGroupName "rg1" -FrontDoorName "frontdoor1" -Name "frontdoor1-azurefd-net"


HostName                         : frontdoor1.azurefd.net
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Disabled
CustomHttpsProvisioningSubstate  : None
CertificateSource                :
ProtocolType                     :
Vault                            :
SecretName                       :
SecretVersion                    :
CertificateType                  :
ResourceState                    : Enabled
Id                               : /subscriptions/{guid}/resourcegroups/resourcegroup1
                                   /providers/Microsoft.Network/frontdoors/frontdoor1/frontendendpoints/frontdoor1-azurefd-net
Name                             : frontdoor1-azurefd-net
Type                             : Microsoft.Network/frontdoors/frontendendpoints
```

<span data-ttu-id="65b08-114">Получить переднюю конечную точку с именем frontdoor1-azurefd-net в front door "frontdoor1", который входит в группу ресурсов "rg1"</span><span class="sxs-lookup"><span data-stu-id="65b08-114">Get frontend endpoint with name "frontdoor1-azurefd-net" in Front Door "frontdoor1" which is part of resource group "rg1"</span></span>

## <span data-ttu-id="65b08-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="65b08-115">PARAMETERS</span></span>

### <span data-ttu-id="65b08-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65b08-116">-DefaultProfile</span></span>
<span data-ttu-id="65b08-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="65b08-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65b08-118">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="65b08-118">-FrontDoorName</span></span>
<span data-ttu-id="65b08-119">Имя передней двери.</span><span class="sxs-lookup"><span data-stu-id="65b08-119">Front Door name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65b08-120">-FrontDoorObject</span><span class="sxs-lookup"><span data-stu-id="65b08-120">-FrontDoorObject</span></span>
<span data-ttu-id="65b08-121">Объект FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="65b08-121">The FrontDoor object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="65b08-122">-Name</span><span class="sxs-lookup"><span data-stu-id="65b08-122">-Name</span></span>
<span data-ttu-id="65b08-123">Имя конечной точки frontend.</span><span class="sxs-lookup"><span data-stu-id="65b08-123">Frontend endpoint name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65b08-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65b08-124">-ResourceGroupName</span></span>
<span data-ttu-id="65b08-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="65b08-125">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65b08-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="65b08-126">-ResourceId</span></span>
<span data-ttu-id="65b08-127">ИД ресурса переднего входа</span><span class="sxs-lookup"><span data-stu-id="65b08-127">Resource Id of the Front Door</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65b08-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65b08-128">CommonParameters</span></span>
<span data-ttu-id="65b08-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65b08-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65b08-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="65b08-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65b08-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="65b08-131">INPUTS</span></span>

### <span data-ttu-id="65b08-132">Нет</span><span class="sxs-lookup"><span data-stu-id="65b08-132">None</span></span>

## <span data-ttu-id="65b08-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="65b08-133">OUTPUTS</span></span>

### <span data-ttu-id="65b08-134">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="65b08-134">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span></span>

## <span data-ttu-id="65b08-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="65b08-135">NOTES</span></span>

## <span data-ttu-id="65b08-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="65b08-136">RELATED LINKS</span></span>

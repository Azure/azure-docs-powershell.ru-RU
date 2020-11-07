---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/get-azfrontdoorfrontendendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorFrontendEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorFrontendEndpoint.md
ms.openlocfilehash: cc07dd366d5c82705a23e3b9276ee9d681c6ae2c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93911996"
---
# <span data-ttu-id="3f6ee-101">Get-AzFrontDoorFrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="3f6ee-101">Get-AzFrontDoorFrontendEndpoint</span></span>

## <span data-ttu-id="3f6ee-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3f6ee-102">SYNOPSIS</span></span>
<span data-ttu-id="3f6ee-103">Получение конечной точки переднего плана для передней дверцы.</span><span class="sxs-lookup"><span data-stu-id="3f6ee-103">Get a front door frontend endpoint.</span></span>

## <span data-ttu-id="3f6ee-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3f6ee-104">SYNTAX</span></span>

### <span data-ttu-id="3f6ee-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3f6ee-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzFrontDoorFrontendEndpoint -ResourceGroupName <String> -FrontDoorName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3f6ee-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3f6ee-106">ByObjectParameterSet</span></span>
```
Get-AzFrontDoorFrontendEndpoint [-Name <String>] -FrontDoorObject <PSFrontDoor>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3f6ee-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3f6ee-107">ByResourceIdParameterSet</span></span>
```
Get-AzFrontDoorFrontendEndpoint -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3f6ee-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3f6ee-108">DESCRIPTION</span></span>
<span data-ttu-id="3f6ee-109">Командлет **Get-AzFrontDoorFrontendEndpoint** получает все существующие конечные точки в текущем ресурсе передней дверцы, соответствующие указанным сведениям.</span><span class="sxs-lookup"><span data-stu-id="3f6ee-109">The **Get-AzFrontDoorFrontendEndpoint** cmdlet gets all existing frontend endpoints in the current Front Door resource that matches provided information.</span></span>

## <span data-ttu-id="3f6ee-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3f6ee-110">EXAMPLES</span></span>

### <span data-ttu-id="3f6ee-111">Пример 1: получение всех конечных точек на передней дверце "frontdoor1", которая входит в группу ресурсов "Rg1".</span><span class="sxs-lookup"><span data-stu-id="3f6ee-111">Example 1: Get all frontend endpoints in Front Door "frontdoor1" which is part of resource group "rg1".</span></span>
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

<span data-ttu-id="3f6ee-112">Получение всех конечных точек на передней дверце "frontdoor1", которая входит в группу ресурсов "Rg1".</span><span class="sxs-lookup"><span data-stu-id="3f6ee-112">Get all frontend endpoints in Front Door "frontdoor1" which is part of resource group "rg1".</span></span>

### <span data-ttu-id="3f6ee-113">Пример 2: получение конечной точки переднего плана с именем "frontdoor1-azurefd-NET" на передней дверце "frontdoor1", которая входит в группу ресурсов "Rg1"</span><span class="sxs-lookup"><span data-stu-id="3f6ee-113">Example 2: Get frontend endpoint with name "frontdoor1-azurefd-net" in Front Door "frontdoor1" which is part of resource group "rg1"</span></span>
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

<span data-ttu-id="3f6ee-114">Получение конечной точки переднего плана с именем "frontdoor1-azurefd-NET" на передней дверце "frontdoor1", которая входит в группу ресурсов "Rg1"</span><span class="sxs-lookup"><span data-stu-id="3f6ee-114">Get frontend endpoint with name "frontdoor1-azurefd-net" in Front Door "frontdoor1" which is part of resource group "rg1"</span></span>

## <span data-ttu-id="3f6ee-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3f6ee-115">PARAMETERS</span></span>

### <span data-ttu-id="3f6ee-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f6ee-116">-DefaultProfile</span></span>
<span data-ttu-id="3f6ee-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3f6ee-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f6ee-118">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="3f6ee-118">-FrontDoorName</span></span>
<span data-ttu-id="3f6ee-119">Имя передней дверцы.</span><span class="sxs-lookup"><span data-stu-id="3f6ee-119">Front Door name.</span></span>

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

### <span data-ttu-id="3f6ee-120">-FrontDoorObject</span><span class="sxs-lookup"><span data-stu-id="3f6ee-120">-FrontDoorObject</span></span>
<span data-ttu-id="3f6ee-121">Объект FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="3f6ee-121">The FrontDoor object.</span></span>

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

### <span data-ttu-id="3f6ee-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3f6ee-122">-Name</span></span>
<span data-ttu-id="3f6ee-123">Имя конечной точки переднего плана.</span><span class="sxs-lookup"><span data-stu-id="3f6ee-123">Frontend endpoint name.</span></span>

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

### <span data-ttu-id="3f6ee-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f6ee-124">-ResourceGroupName</span></span>
<span data-ttu-id="3f6ee-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3f6ee-125">The resource group name.</span></span>

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

### <span data-ttu-id="3f6ee-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3f6ee-126">-ResourceId</span></span>
<span data-ttu-id="3f6ee-127">Идентификатор ресурса передней дверцы</span><span class="sxs-lookup"><span data-stu-id="3f6ee-127">Resource Id of the Front Door</span></span>

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

### <span data-ttu-id="3f6ee-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f6ee-128">CommonParameters</span></span>
<span data-ttu-id="3f6ee-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3f6ee-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f6ee-130">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3f6ee-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f6ee-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3f6ee-131">INPUTS</span></span>

### <span data-ttu-id="3f6ee-132">Ничего</span><span class="sxs-lookup"><span data-stu-id="3f6ee-132">None</span></span>

## <span data-ttu-id="3f6ee-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3f6ee-133">OUTPUTS</span></span>

### <span data-ttu-id="3f6ee-134">Microsoft. Azure. Commands. FrontDoor. Models. PSFrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="3f6ee-134">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span></span>

## <span data-ttu-id="3f6ee-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="3f6ee-135">NOTES</span></span>

## <span data-ttu-id="3f6ee-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3f6ee-136">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/disable-azfrontdoorcustomdomainhttps
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Disable-AzFrontDoorCustomDomainHttps.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Disable-AzFrontDoorCustomDomainHttps.md
ms.openlocfilehash: 65c9bca6eb678ff3f3cb0a61d815f8415c715e43
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98507465"
---
# <span data-ttu-id="b0c0e-101">Disable-AzFrontDoorCustomDomainHttps</span><span class="sxs-lookup"><span data-stu-id="b0c0e-101">Disable-AzFrontDoorCustomDomainHttps</span></span>

## <span data-ttu-id="b0c0e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0c0e-102">SYNOPSIS</span></span>
<span data-ttu-id="b0c0e-103">Отключение HTTPS для пользовательского домена</span><span class="sxs-lookup"><span data-stu-id="b0c0e-103">Disable HTTPS for a custom domain</span></span>

## <span data-ttu-id="b0c0e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b0c0e-104">SYNTAX</span></span>

### <span data-ttu-id="b0c0e-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b0c0e-105">ByFieldsParameterSet (Default)</span></span>
```
Disable-AzFrontDoorCustomDomainHttps -ResourceGroupName <String> -FrontDoorName <String>
 -FrontendEndpointName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b0c0e-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b0c0e-106">ByResourceIdParameterSet</span></span>
```
Disable-AzFrontDoorCustomDomainHttps -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0c0e-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b0c0e-107">ByObjectParameterSet</span></span>
```
Disable-AzFrontDoorCustomDomainHttps -InputObject <PSFrontendEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0c0e-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b0c0e-108">DESCRIPTION</span></span>
<span data-ttu-id="b0c0e-109">**Disable-AzFrontDoorCustomDomainHttps** отключает HTTPS для пользовательского домена.</span><span class="sxs-lookup"><span data-stu-id="b0c0e-109">The **Disable-AzFrontDoorCustomDomainHttps** disables HTTPS for a custom domain.</span></span>

## <span data-ttu-id="b0c0e-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b0c0e-110">EXAMPLES</span></span>

### <span data-ttu-id="b0c0e-111">Пример 1. Отключать HTTPS для пользовательского домена с помощью FrontDoorName и ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="b0c0e-111">Example 1: Disable HTTPS for a custom domain with FrontDoorName and ResourceGroupName.</span></span>
```powershell
PS C:\> Disable-AzFrontDoorCustomDomainHttps -ResourceGroupName "resourcegroup1" -FrontDoorName "frontdoor1" -FrontendEndpointName "frontendpointname1-custom-xyz"

HostName                         : frontendpointname1.custom.xyz
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Disabling
CustomHttpsProvisioningSubstate  : DeletingCertificate
CertificateSource                : FrontDoor
ProtocolType                     : ServerNameIndication
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

<span data-ttu-id="b0c0e-112">Отключать HTTPS для пользовательского домена frontendpointname1-custom-xyz, при этом FrontDoorName будет называться frontdoor1, а ResourceGroupName — как "resourcegroup1".</span><span class="sxs-lookup"><span data-stu-id="b0c0e-112">Disable HTTPS for a custom domain "frontendpointname1-custom-xyz" with FrontDoorName as "frontdoor1" and ResourceGroupName as "resourcegroup1".</span></span>

### <span data-ttu-id="b0c0e-113">Пример 2. Отключение HTTPS для пользовательского домена с объектом PSFrontendEndPoint.</span><span class="sxs-lookup"><span data-stu-id="b0c0e-113">Example 2: Disable HTTPS for a custom domain with PSFrontendEndpoint object.</span></span>
```powershell
PS C:\> Get-AzFrontDoorFrontendEndpoint -ResourceGroupName "resourcegroup1" -FrontDoorName "frontdoor1" -FrontendEndpointName "frontendpointname1-custom-xyz" | Disable-AzFrontDoorCustomDomainHttps -InputObject $frontendEndpointObj 

HostName                         : frontendpointname1.custom.xyz
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Disabling
CustomHttpsProvisioningSubstate  : DeletingCertificate
CertificateSource                : FrontDoor
ProtocolType                     : ServerNameIndication
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

<span data-ttu-id="b0c0e-114">Отключать HTTPS для пользовательского домена с объектом PSFrontendEndpoint.</span><span class="sxs-lookup"><span data-stu-id="b0c0e-114">Disable HTTPS for a custom domain with PSFrontendEndpoint object.</span></span>

### <span data-ttu-id="b0c0e-115">Пример 3. Отключение HTTPS для пользовательского домена с помощью ResourceId.</span><span class="sxs-lookup"><span data-stu-id="b0c0e-115">Example 3: Disable HTTPS for a custom domain with ResourceId.</span></span>
```powershell
PS C:\> Disable-AzFrontDoorCustomDomainHttps -ResourceId $resourceId 

HostName                         : frontendpointname1.custom.xyz
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Disabling
CustomHttpsProvisioningSubstate  : DeletingCertificate
CertificateSource                : FrontDoor
ProtocolType                     : ServerNameIndication
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

<span data-ttu-id="b0c0e-116">Отключать HTTPS для пользовательского домена frontendpointname1-custom-xyz с ResourceId как $resourceId.</span><span class="sxs-lookup"><span data-stu-id="b0c0e-116">Disable HTTPS for a custom domain "frontendpointname1-custom-xyz" with ResourceId as $resourceId.</span></span>

## <span data-ttu-id="b0c0e-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b0c0e-117">PARAMETERS</span></span>

### <span data-ttu-id="b0c0e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0c0e-118">-DefaultProfile</span></span>
<span data-ttu-id="b0c0e-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b0c0e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0c0e-120">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="b0c0e-120">-FrontDoorName</span></span>
<span data-ttu-id="b0c0e-121">Название передней двери.</span><span class="sxs-lookup"><span data-stu-id="b0c0e-121">The name of the Front Door.</span></span>

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

### <span data-ttu-id="b0c0e-122">-FrontendEndpointName</span><span class="sxs-lookup"><span data-stu-id="b0c0e-122">-FrontendEndpointName</span></span>
<span data-ttu-id="b0c0e-123">Имя конечной точки frontend.</span><span class="sxs-lookup"><span data-stu-id="b0c0e-123">Frontend endpoint name.</span></span>

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

### <span data-ttu-id="b0c0e-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b0c0e-124">-InputObject</span></span>
<span data-ttu-id="b0c0e-125">Объект конечной точки Frontend, который нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="b0c0e-125">The Frontend endpoint object to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b0c0e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0c0e-126">-ResourceGroupName</span></span>
<span data-ttu-id="b0c0e-127">Группа ресурсов, к которой относится front Door.</span><span class="sxs-lookup"><span data-stu-id="b0c0e-127">The resource group to which the Front Door belongs.</span></span>

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

### <span data-ttu-id="b0c0e-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b0c0e-128">-ResourceId</span></span>
<span data-ttu-id="b0c0e-129">ИД ресурса конечной точки переднего входа, чтобы отключить https</span><span class="sxs-lookup"><span data-stu-id="b0c0e-129">Resource Id of the Front Door endpoint to disable https</span></span>

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

### <span data-ttu-id="b0c0e-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b0c0e-130">-Confirm</span></span>
<span data-ttu-id="b0c0e-131">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="b0c0e-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0c0e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0c0e-132">-WhatIf</span></span>
<span data-ttu-id="b0c0e-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b0c0e-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b0c0e-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="b0c0e-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0c0e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0c0e-135">CommonParameters</span></span>
<span data-ttu-id="b0c0e-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0c0e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0c0e-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b0c0e-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0c0e-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b0c0e-138">INPUTS</span></span>

### <span data-ttu-id="b0c0e-139">System.String</span><span class="sxs-lookup"><span data-stu-id="b0c0e-139">System.String</span></span>

## <span data-ttu-id="b0c0e-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b0c0e-140">OUTPUTS</span></span>

### <span data-ttu-id="b0c0e-141">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="b0c0e-141">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span></span>

## <span data-ttu-id="b0c0e-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b0c0e-142">NOTES</span></span>

## <span data-ttu-id="b0c0e-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b0c0e-143">RELATED LINKS</span></span>

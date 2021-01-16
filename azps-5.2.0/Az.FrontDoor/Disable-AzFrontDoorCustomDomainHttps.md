---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/disable-azfrontdoorcustomdomainhttps
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Disable-AzFrontDoorCustomDomainHttps.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Disable-AzFrontDoorCustomDomainHttps.md
ms.openlocfilehash: 65c9bca6eb678ff3f3cb0a61d815f8415c715e43
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98400631"
---
# <span data-ttu-id="631b5-101">Disable-AzFrontDoorCustomDomainHttps</span><span class="sxs-lookup"><span data-stu-id="631b5-101">Disable-AzFrontDoorCustomDomainHttps</span></span>

## <span data-ttu-id="631b5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="631b5-102">SYNOPSIS</span></span>
<span data-ttu-id="631b5-103">Отключение HTTPS для пользовательского домена</span><span class="sxs-lookup"><span data-stu-id="631b5-103">Disable HTTPS for a custom domain</span></span>

## <span data-ttu-id="631b5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="631b5-104">SYNTAX</span></span>

### <span data-ttu-id="631b5-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="631b5-105">ByFieldsParameterSet (Default)</span></span>
```
Disable-AzFrontDoorCustomDomainHttps -ResourceGroupName <String> -FrontDoorName <String>
 -FrontendEndpointName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="631b5-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="631b5-106">ByResourceIdParameterSet</span></span>
```
Disable-AzFrontDoorCustomDomainHttps -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="631b5-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="631b5-107">ByObjectParameterSet</span></span>
```
Disable-AzFrontDoorCustomDomainHttps -InputObject <PSFrontendEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="631b5-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="631b5-108">DESCRIPTION</span></span>
<span data-ttu-id="631b5-109">**Disable-AzFrontDoorCustomDomainHttps** отключает HTTPS для пользовательского домена.</span><span class="sxs-lookup"><span data-stu-id="631b5-109">The **Disable-AzFrontDoorCustomDomainHttps** disables HTTPS for a custom domain.</span></span>

## <span data-ttu-id="631b5-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="631b5-110">EXAMPLES</span></span>

### <span data-ttu-id="631b5-111">Пример 1. Отключать HTTPS для пользовательского домена с помощью FrontDoorName и ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="631b5-111">Example 1: Disable HTTPS for a custom domain with FrontDoorName and ResourceGroupName.</span></span>
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

<span data-ttu-id="631b5-112">Отключать HTTPS для пользовательского домена frontendpointname1-custom-xyz, при этом FrontDoorName будет называться frontdoor1, а ResourceGroupName — как "resourcegroup1".</span><span class="sxs-lookup"><span data-stu-id="631b5-112">Disable HTTPS for a custom domain "frontendpointname1-custom-xyz" with FrontDoorName as "frontdoor1" and ResourceGroupName as "resourcegroup1".</span></span>

### <span data-ttu-id="631b5-113">Пример 2. Отключение HTTPS для пользовательского домена с объектом PSFrontendEndPoint.</span><span class="sxs-lookup"><span data-stu-id="631b5-113">Example 2: Disable HTTPS for a custom domain with PSFrontendEndpoint object.</span></span>
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

<span data-ttu-id="631b5-114">Отключать HTTPS для пользовательского домена с объектом PSFrontendEndpoint.</span><span class="sxs-lookup"><span data-stu-id="631b5-114">Disable HTTPS for a custom domain with PSFrontendEndpoint object.</span></span>

### <span data-ttu-id="631b5-115">Пример 3. Отключение HTTPS для пользовательского домена с помощью ResourceId.</span><span class="sxs-lookup"><span data-stu-id="631b5-115">Example 3: Disable HTTPS for a custom domain with ResourceId.</span></span>
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

<span data-ttu-id="631b5-116">Отключать HTTPS для пользовательского домена frontendpointname1-custom-xyz с ResourceId как $resourceId.</span><span class="sxs-lookup"><span data-stu-id="631b5-116">Disable HTTPS for a custom domain "frontendpointname1-custom-xyz" with ResourceId as $resourceId.</span></span>

## <span data-ttu-id="631b5-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="631b5-117">PARAMETERS</span></span>

### <span data-ttu-id="631b5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="631b5-118">-DefaultProfile</span></span>
<span data-ttu-id="631b5-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="631b5-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="631b5-120">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="631b5-120">-FrontDoorName</span></span>
<span data-ttu-id="631b5-121">Название передней двери.</span><span class="sxs-lookup"><span data-stu-id="631b5-121">The name of the Front Door.</span></span>

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

### <span data-ttu-id="631b5-122">-FrontendEndpointName</span><span class="sxs-lookup"><span data-stu-id="631b5-122">-FrontendEndpointName</span></span>
<span data-ttu-id="631b5-123">Имя конечной точки frontend.</span><span class="sxs-lookup"><span data-stu-id="631b5-123">Frontend endpoint name.</span></span>

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

### <span data-ttu-id="631b5-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="631b5-124">-InputObject</span></span>
<span data-ttu-id="631b5-125">Объект конечной точки Frontend, который нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="631b5-125">The Frontend endpoint object to update.</span></span>

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

### <span data-ttu-id="631b5-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="631b5-126">-ResourceGroupName</span></span>
<span data-ttu-id="631b5-127">Группа ресурсов, к которой относится front Door.</span><span class="sxs-lookup"><span data-stu-id="631b5-127">The resource group to which the Front Door belongs.</span></span>

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

### <span data-ttu-id="631b5-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="631b5-128">-ResourceId</span></span>
<span data-ttu-id="631b5-129">ИД ресурса конечной точки front Door для отключения https</span><span class="sxs-lookup"><span data-stu-id="631b5-129">Resource Id of the Front Door endpoint to disable https</span></span>

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

### <span data-ttu-id="631b5-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="631b5-130">-Confirm</span></span>
<span data-ttu-id="631b5-131">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="631b5-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="631b5-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="631b5-132">-WhatIf</span></span>
<span data-ttu-id="631b5-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="631b5-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="631b5-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="631b5-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="631b5-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="631b5-135">CommonParameters</span></span>
<span data-ttu-id="631b5-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="631b5-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="631b5-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="631b5-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="631b5-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="631b5-138">INPUTS</span></span>

### <span data-ttu-id="631b5-139">System.String</span><span class="sxs-lookup"><span data-stu-id="631b5-139">System.String</span></span>

## <span data-ttu-id="631b5-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="631b5-140">OUTPUTS</span></span>

### <span data-ttu-id="631b5-141">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="631b5-141">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span></span>

## <span data-ttu-id="631b5-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="631b5-142">NOTES</span></span>

## <span data-ttu-id="631b5-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="631b5-143">RELATED LINKS</span></span>

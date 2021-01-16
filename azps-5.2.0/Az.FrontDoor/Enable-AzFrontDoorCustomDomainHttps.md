---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/enable-azfrontdoorcustomdomainhttps
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Enable-AzFrontDoorCustomDomainHttps.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Enable-AzFrontDoorCustomDomainHttps.md
ms.openlocfilehash: 6d3eb8d4cbeb2a8c40e3fc6fbf0f54e8973e8f79
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98407372"
---
# <span data-ttu-id="b3743-101">Enable-AzFrontDoorCustomDomainHttps</span><span class="sxs-lookup"><span data-stu-id="b3743-101">Enable-AzFrontDoorCustomDomainHttps</span></span>

## <span data-ttu-id="b3743-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3743-102">SYNOPSIS</span></span>
<span data-ttu-id="b3743-103">Включить HTTPS для пользовательского домена с помощью сертификата, управляемого front Door, или с помощью собственного сертификата из хранилища ключей Azure.</span><span class="sxs-lookup"><span data-stu-id="b3743-103">Enable HTTPS for a custom domain using Front Door managed certificate or using own certificate from Azure Key Vault.</span></span>

## <span data-ttu-id="b3743-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b3743-104">SYNTAX</span></span>

### <span data-ttu-id="b3743-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b3743-105">ByFieldsParameterSet (Default)</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -ResourceGroupName <String> -FrontDoorName <String>
 -FrontendEndpointName <String> [-MinimumTlsVersion <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3743-106">ByFieldsWithVaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="b3743-106">ByFieldsWithVaultParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -ResourceGroupName <String> -FrontDoorName <String>
 -FrontendEndpointName <String> -VaultId <String> -SecretName <String> -SecretVersion <String>
 [-MinimumTlsVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b3743-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b3743-107">ByResourceIdParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -ResourceId <String> [-MinimumTlsVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3743-108">ByResourceIdWithVaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="b3743-108">ByResourceIdWithVaultParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -ResourceId <String> -VaultId <String> -SecretName <String>
 -SecretVersion <String> [-MinimumTlsVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3743-109">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b3743-109">ByObjectParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -InputObject <PSFrontendEndpoint> [-MinimumTlsVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3743-110">ByObjectWithVaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="b3743-110">ByObjectWithVaultParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -InputObject <PSFrontendEndpoint> -VaultId <String> -SecretName <String>
 -SecretVersion <String> [-MinimumTlsVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3743-111">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b3743-111">DESCRIPTION</span></span>
<span data-ttu-id="b3743-112">**Enable-AzFrontDoorCustomDomainHttps** включает HTTPS для пользовательского домена.</span><span class="sxs-lookup"><span data-stu-id="b3743-112">The **Enable-AzFrontDoorCustomDomainHttps** enables HTTPS for a custom domain.</span></span>

## <span data-ttu-id="b3743-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b3743-113">EXAMPLES</span></span>

### <span data-ttu-id="b3743-114">Пример 1. Включить HTTPS для пользовательского домена с помощью FrontDoorName и ResourceGroupName с помощью сертификата Front Door Managed.</span><span class="sxs-lookup"><span data-stu-id="b3743-114">Example 1: Enable HTTPS for a custom domain with FrontDoorName and ResourceGroupName using Front Door managed certificate.</span></span>
```powershell
PS C:\> Enable-AzFrontDoorCustomDomainHttps -ResourceGroupName "resourcegroup1" -FrontDoorName "frontdoor1" -FrontendEndpointName "frontendpointname1-custom-xyz" -MinimumTlsVersion "1.2"


HostName                         : frontendpointname1.custom.xyz
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Enabling
CustomHttpsProvisioningSubstate  : SubmittingDomainControlValidationRequest
CertificateSource                : FrontDoor
ProtocolType                     : ServerNameIndication
MinimumTlsVersion                : 1.2
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

<span data-ttu-id="b3743-115">Включить HTTPS для пользовательского домена frontendpointname1-custom-xyz, который является частью front door "frontdoor1" в группе ресурсов "resourcegroup1", используя сертификат Front Door Managed.</span><span class="sxs-lookup"><span data-stu-id="b3743-115">Enable HTTPS for a custom domain "frontendpointname1-custom-xyz" that is part of Front Door "frontdoor1" in resource group "resourcegroup1" using Front Door managed certificate.</span></span>

### <span data-ttu-id="b3743-116">Пример 2. Включить HTTPS для пользовательского домена с помощью FrontDoorName и ResourceGroupName с помощью собственного сертификата в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="b3743-116">Example 2: Enable HTTPS for a custom domain with FrontDoorName and ResourceGroupName using own certificate in Key Vault.</span></span>
```powershell
PS C:\> $vaultId = (Get-AzKeyVault -VaultName $vaultName).ResourceId
PS C:\> Enable-AzFrontDoorCustomDomainHttps -ResourceGroupName "resourcegroup1" -FrontDoorName "frontdoor1" -FrontendEndpointName "frontendpointname1-custom-xyz" -Vault $vaultId -secretName $secretName -SecretVersion $secretVersion -MinimumTlsVersion "1.0"


HostName                         : frontendpointname1.custom.xyz
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Enabling
CustomHttpsProvisioningSubstate  : SubmittingDomainControlValidationRequest
CertificateSource                : AzureKeyVault
ProtocolType                     : ServerNameIndication
MinimumTlsVersion                : 1.0
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

<span data-ttu-id="b3743-117">Включить HTTPS для пользовательского домена frontendpointname1-custom-xyz, который является частью передней двери "frontdoor1" в группе ресурсов "resourcegroup1", используя сертификат, управляемый front Door.</span><span class="sxs-lookup"><span data-stu-id="b3743-117">Enable HTTPS for a custom domain "frontendpointname1-custom-xyz" that is part of Front Door "frontdoor1" in resource group "resourcegroup1" using Front Door managed certificate.</span></span>

### <span data-ttu-id="b3743-118">Пример 3. Включить HTTPS для пользовательского домена с объектом PSFrontendEndPoint с помощью сертификата Front Door Managed.</span><span class="sxs-lookup"><span data-stu-id="b3743-118">Example 3: Enable HTTPS for a custom domain with PSFrontendEndpoint object using Front Door managed certificate.</span></span>
```powershell
PS C:\> Get-AzFrontDoorFrontendEndpoint -ResourceGroupName "resourcegroup1" -FrontDoorName "frontdoor1" -Name "frontendpointname1-custom-xyz" | Enable-AzFrontDoorCustomDomainHttps 


HostName                         : frontendpointname1.custom.xyz
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Enabling
CustomHttpsProvisioningSubstate  : SubmittingDomainControlValidationRequest
CertificateSource                : FrontDoor
ProtocolType                     : ServerNameIndication
MinimumTlsVersion                : 1.2
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

<span data-ttu-id="b3743-119">Включить HTTPS для пользовательского домена с объектом PSFrontendEndpoint с помощью сертификата Front Door Managed.</span><span class="sxs-lookup"><span data-stu-id="b3743-119">Enable HTTPS for a custom domain with PSFrontendEndpoint object using Front Door managed certificate.</span></span>

### <span data-ttu-id="b3743-120">Пример 4. Включить HTTPS для пользовательского домена с помощью ИД ресурса с помощью сертификата Front Door Managed.</span><span class="sxs-lookup"><span data-stu-id="b3743-120">Example 4: Enable HTTPS for a custom domain with resource id using Front Door managed certificate.</span></span>
```powershell
PS C:\> Enable-AzFrontDoorCustomDomainHttps -ResourceId $resourceId


HostName                         : frontendpointname1.custom.xyz
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Enabling
CustomHttpsProvisioningSubstate  : SubmittingDomainControlValidationRequest
CertificateSource                : FrontDoor
ProtocolType                     : ServerNameIndication
MinimumTlsVersion                : 1.2
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

<span data-ttu-id="b3743-121">Включить HTTPS для пользовательского домена frontendpointname1-custom-xyz с помощью $resourceId ресурса с помощью сертификата Front Door Managed.</span><span class="sxs-lookup"><span data-stu-id="b3743-121">Enable HTTPS for a custom domain "frontendpointname1-custom-xyz" with resource id $resourceId using Front Door managed certificate.</span></span>

## <span data-ttu-id="b3743-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b3743-122">PARAMETERS</span></span>

### <span data-ttu-id="b3743-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3743-123">-DefaultProfile</span></span>
<span data-ttu-id="b3743-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b3743-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3743-125">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="b3743-125">-FrontDoorName</span></span>
<span data-ttu-id="b3743-126">Название передней двери.</span><span class="sxs-lookup"><span data-stu-id="b3743-126">The name of the Front Door.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsWithVaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3743-127">-FrontendEndpointName</span><span class="sxs-lookup"><span data-stu-id="b3743-127">-FrontendEndpointName</span></span>
<span data-ttu-id="b3743-128">Имя конечной точки frontend.</span><span class="sxs-lookup"><span data-stu-id="b3743-128">Frontend endpoint name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsWithVaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3743-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b3743-129">-InputObject</span></span>
<span data-ttu-id="b3743-130">Объект конечной точки Frontend, который нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="b3743-130">The Frontend endpoint object to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint
Parameter Sets: ByObjectParameterSet, ByObjectWithVaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b3743-131">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="b3743-131">-MinimumTlsVersion</span></span>
<span data-ttu-id="b3743-132">Минимальная версия TLS, необходимая клиентам для того, чтобы получить SSL-handshake with Front Door.</span><span class="sxs-lookup"><span data-stu-id="b3743-132">The minimum TLS version required from the clients to establish an SSL handshake with Front Door.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3743-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3743-133">-ResourceGroupName</span></span>
<span data-ttu-id="b3743-134">Группа ресурсов, к которой относится front Door.</span><span class="sxs-lookup"><span data-stu-id="b3743-134">The resource group to which the Front Door belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsWithVaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3743-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b3743-135">-ResourceId</span></span>
<span data-ttu-id="b3743-136">ИД ресурса конечной точки front Door, чтобы включить https</span><span class="sxs-lookup"><span data-stu-id="b3743-136">Resource Id of the Front Door endpoint to enable https</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet, ByResourceIdWithVaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3743-137">-SecretName</span><span class="sxs-lookup"><span data-stu-id="b3743-137">-SecretName</span></span>
<span data-ttu-id="b3743-138">Имя секретного сейфа ключа, представляющее полный сертификат PFX</span><span class="sxs-lookup"><span data-stu-id="b3743-138">The name of the Key Vault secret representing the full certificate PFX</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithVaultParameterSet, ByResourceIdWithVaultParameterSet, ByObjectWithVaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3743-139">-SecretVersion</span><span class="sxs-lookup"><span data-stu-id="b3743-139">-SecretVersion</span></span>
<span data-ttu-id="b3743-140">Версия секретного сейфа ключа, представляющая полный сертификат PFX</span><span class="sxs-lookup"><span data-stu-id="b3743-140">The version of the Key Vault secret representing the full certificate PFX</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithVaultParameterSet, ByResourceIdWithVaultParameterSet, ByObjectWithVaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3743-141">-VaultId</span><span class="sxs-lookup"><span data-stu-id="b3743-141">-VaultId</span></span>
<span data-ttu-id="b3743-142">Удостоверение ключа, содержащее SSL-сертификат</span><span class="sxs-lookup"><span data-stu-id="b3743-142">The Key Vault id containing the SSL certificate</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithVaultParameterSet, ByResourceIdWithVaultParameterSet, ByObjectWithVaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3743-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b3743-143">-Confirm</span></span>
<span data-ttu-id="b3743-144">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="b3743-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3743-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3743-145">-WhatIf</span></span>
<span data-ttu-id="b3743-146">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b3743-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b3743-147">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="b3743-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3743-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3743-148">CommonParameters</span></span>
<span data-ttu-id="b3743-149">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3743-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3743-150">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b3743-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3743-151">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b3743-151">INPUTS</span></span>

### <span data-ttu-id="b3743-152">System.String</span><span class="sxs-lookup"><span data-stu-id="b3743-152">System.String</span></span>
## <span data-ttu-id="b3743-153">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b3743-153">OUTPUTS</span></span>

### <span data-ttu-id="b3743-154">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="b3743-154">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span></span>
## <span data-ttu-id="b3743-155">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b3743-155">NOTES</span></span>

## <span data-ttu-id="b3743-156">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b3743-156">RELATED LINKS</span></span>
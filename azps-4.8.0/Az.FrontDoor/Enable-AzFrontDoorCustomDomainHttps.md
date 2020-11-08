---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/enable-azfrontdoorcustomdomainhttps
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Enable-AzFrontDoorCustomDomainHttps.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Enable-AzFrontDoorCustomDomainHttps.md
ms.openlocfilehash: 6d3eb8d4cbeb2a8c40e3fc6fbf0f54e8973e8f79
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244959"
---
# <span data-ttu-id="4ba2b-101">Enable-AzFrontDoorCustomDomainHttps</span><span class="sxs-lookup"><span data-stu-id="4ba2b-101">Enable-AzFrontDoorCustomDomainHttps</span></span>

## <span data-ttu-id="4ba2b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4ba2b-102">SYNOPSIS</span></span>
<span data-ttu-id="4ba2b-103">Включите HTTPS для пользовательского домена с помощью управляемого сертификата с передней дверцой или с помощью собственного сертификата из хранилища ключей Azure.</span><span class="sxs-lookup"><span data-stu-id="4ba2b-103">Enable HTTPS for a custom domain using Front Door managed certificate or using own certificate from Azure Key Vault.</span></span>

## <span data-ttu-id="4ba2b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4ba2b-104">SYNTAX</span></span>

### <span data-ttu-id="4ba2b-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4ba2b-105">ByFieldsParameterSet (Default)</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -ResourceGroupName <String> -FrontDoorName <String>
 -FrontendEndpointName <String> [-MinimumTlsVersion <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ba2b-106">ByFieldsWithVaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="4ba2b-106">ByFieldsWithVaultParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -ResourceGroupName <String> -FrontDoorName <String>
 -FrontendEndpointName <String> -VaultId <String> -SecretName <String> -SecretVersion <String>
 [-MinimumTlsVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4ba2b-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4ba2b-107">ByResourceIdParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -ResourceId <String> [-MinimumTlsVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ba2b-108">ByResourceIdWithVaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="4ba2b-108">ByResourceIdWithVaultParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -ResourceId <String> -VaultId <String> -SecretName <String>
 -SecretVersion <String> [-MinimumTlsVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ba2b-109">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4ba2b-109">ByObjectParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -InputObject <PSFrontendEndpoint> [-MinimumTlsVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ba2b-110">ByObjectWithVaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="4ba2b-110">ByObjectWithVaultParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -InputObject <PSFrontendEndpoint> -VaultId <String> -SecretName <String>
 -SecretVersion <String> [-MinimumTlsVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ba2b-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4ba2b-111">DESCRIPTION</span></span>
<span data-ttu-id="4ba2b-112">Параметр **Enable-AzFrontDoorCustomDomainHttps** включает HTTPS для настраиваемого домена.</span><span class="sxs-lookup"><span data-stu-id="4ba2b-112">The **Enable-AzFrontDoorCustomDomainHttps** enables HTTPS for a custom domain.</span></span>

## <span data-ttu-id="4ba2b-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4ba2b-113">EXAMPLES</span></span>

### <span data-ttu-id="4ba2b-114">Пример 1: включение HTTPS для пользовательского домена с FrontDoorName и ResourceGroupName с помощью управляемого сертификата передней дверцы.</span><span class="sxs-lookup"><span data-stu-id="4ba2b-114">Example 1: Enable HTTPS for a custom domain with FrontDoorName and ResourceGroupName using Front Door managed certificate.</span></span>
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

<span data-ttu-id="4ba2b-115">Включите HTTPS для пользовательского домена "frontendpointname1-Custom-XYZ", который является частью передней дверцы "frontdoor1" в группе ресурсов "resourcegroup1" с помощью управляемого сертификата передней дверцы.</span><span class="sxs-lookup"><span data-stu-id="4ba2b-115">Enable HTTPS for a custom domain "frontendpointname1-custom-xyz" that is part of Front Door "frontdoor1" in resource group "resourcegroup1" using Front Door managed certificate.</span></span>

### <span data-ttu-id="4ba2b-116">Пример 2: включение HTTPS для пользовательского домена с FrontDoorName и ResourceGroupName с помощью собственного сертификата в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="4ba2b-116">Example 2: Enable HTTPS for a custom domain with FrontDoorName and ResourceGroupName using own certificate in Key Vault.</span></span>
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

<span data-ttu-id="4ba2b-117">Включите HTTPS для пользовательского домена "frontendpointname1-Custom-XYZ", который является частью передней дверцы "frontdoor1" в группе ресурсов "resourcegroup1" с помощью управляемого сертификата передней дверцы.</span><span class="sxs-lookup"><span data-stu-id="4ba2b-117">Enable HTTPS for a custom domain "frontendpointname1-custom-xyz" that is part of Front Door "frontdoor1" in resource group "resourcegroup1" using Front Door managed certificate.</span></span>

### <span data-ttu-id="4ba2b-118">Пример 3: включите HTTPS для пользовательского домена с объектом PSFrontendEndpoint, используя управляемый сертификат передней дверцы.</span><span class="sxs-lookup"><span data-stu-id="4ba2b-118">Example 3: Enable HTTPS for a custom domain with PSFrontendEndpoint object using Front Door managed certificate.</span></span>
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

<span data-ttu-id="4ba2b-119">Включите HTTPS для пользовательского домена с объектом PSFrontendEndpoint, используя управляемый сертификат передней дверцы.</span><span class="sxs-lookup"><span data-stu-id="4ba2b-119">Enable HTTPS for a custom domain with PSFrontendEndpoint object using Front Door managed certificate.</span></span>

### <span data-ttu-id="4ba2b-120">Пример 4: включение HTTPS для пользовательского домена с идентификатором ресурса с помощью управляемого сертификата с использованием передней дверцы.</span><span class="sxs-lookup"><span data-stu-id="4ba2b-120">Example 4: Enable HTTPS for a custom domain with resource id using Front Door managed certificate.</span></span>
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

<span data-ttu-id="4ba2b-121">Включите HTTPS для пользовательского домена "frontendpointname1-Custom-XYZ" с идентификатором ресурса $resourceId помощью управляемого сертификата передней дверцы.</span><span class="sxs-lookup"><span data-stu-id="4ba2b-121">Enable HTTPS for a custom domain "frontendpointname1-custom-xyz" with resource id $resourceId using Front Door managed certificate.</span></span>

## <span data-ttu-id="4ba2b-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4ba2b-122">PARAMETERS</span></span>

### <span data-ttu-id="4ba2b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ba2b-123">-DefaultProfile</span></span>
<span data-ttu-id="4ba2b-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4ba2b-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ba2b-125">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="4ba2b-125">-FrontDoorName</span></span>
<span data-ttu-id="4ba2b-126">Название передней дверцы.</span><span class="sxs-lookup"><span data-stu-id="4ba2b-126">The name of the Front Door.</span></span>

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

### <span data-ttu-id="4ba2b-127">-FrontendEndpointName</span><span class="sxs-lookup"><span data-stu-id="4ba2b-127">-FrontendEndpointName</span></span>
<span data-ttu-id="4ba2b-128">Имя конечной точки переднего плана.</span><span class="sxs-lookup"><span data-stu-id="4ba2b-128">Frontend endpoint name.</span></span>

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

### <span data-ttu-id="4ba2b-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4ba2b-129">-InputObject</span></span>
<span data-ttu-id="4ba2b-130">Обновляемый объект одноинтерфейсной точки.</span><span class="sxs-lookup"><span data-stu-id="4ba2b-130">The Frontend endpoint object to update.</span></span>

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

### <span data-ttu-id="4ba2b-131">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="4ba2b-131">-MinimumTlsVersion</span></span>
<span data-ttu-id="4ba2b-132">Минимальная версия TLS, необходимая на клиентах для установления подтверждения SSL с помощью передней дверцы.</span><span class="sxs-lookup"><span data-stu-id="4ba2b-132">The minimum TLS version required from the clients to establish an SSL handshake with Front Door.</span></span>

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

### <span data-ttu-id="4ba2b-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ba2b-133">-ResourceGroupName</span></span>
<span data-ttu-id="4ba2b-134">Группа ресурсов, к которой принадлежит передняя дверь.</span><span class="sxs-lookup"><span data-stu-id="4ba2b-134">The resource group to which the Front Door belongs.</span></span>

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

### <span data-ttu-id="4ba2b-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4ba2b-135">-ResourceId</span></span>
<span data-ttu-id="4ba2b-136">Идентификатор ресурса конечной точки передней дверцы для включения HTTPS</span><span class="sxs-lookup"><span data-stu-id="4ba2b-136">Resource Id of the Front Door endpoint to enable https</span></span>

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

### <span data-ttu-id="4ba2b-137">-SecretName</span><span class="sxs-lookup"><span data-stu-id="4ba2b-137">-SecretName</span></span>
<span data-ttu-id="4ba2b-138">Имя секрета в хранилище ключей, представляющее полный PFX-сертификат.</span><span class="sxs-lookup"><span data-stu-id="4ba2b-138">The name of the Key Vault secret representing the full certificate PFX</span></span>

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

### <span data-ttu-id="4ba2b-139">-SecretVersion</span><span class="sxs-lookup"><span data-stu-id="4ba2b-139">-SecretVersion</span></span>
<span data-ttu-id="4ba2b-140">Версия секрета хранилища ключей, представляющая полный PFX-сертификат.</span><span class="sxs-lookup"><span data-stu-id="4ba2b-140">The version of the Key Vault secret representing the full certificate PFX</span></span>

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

### <span data-ttu-id="4ba2b-141">-VaultId</span><span class="sxs-lookup"><span data-stu-id="4ba2b-141">-VaultId</span></span>
<span data-ttu-id="4ba2b-142">Идентификатор хранилища ключей, содержащий сертификат SSL.</span><span class="sxs-lookup"><span data-stu-id="4ba2b-142">The Key Vault id containing the SSL certificate</span></span>

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

### <span data-ttu-id="4ba2b-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4ba2b-143">-Confirm</span></span>
<span data-ttu-id="4ba2b-144">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4ba2b-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ba2b-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ba2b-145">-WhatIf</span></span>
<span data-ttu-id="4ba2b-146">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4ba2b-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4ba2b-147">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4ba2b-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ba2b-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ba2b-148">CommonParameters</span></span>
<span data-ttu-id="4ba2b-149">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4ba2b-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ba2b-150">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4ba2b-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ba2b-151">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4ba2b-151">INPUTS</span></span>

### <span data-ttu-id="4ba2b-152">System. String</span><span class="sxs-lookup"><span data-stu-id="4ba2b-152">System.String</span></span>
## <span data-ttu-id="4ba2b-153">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4ba2b-153">OUTPUTS</span></span>

### <span data-ttu-id="4ba2b-154">Microsoft. Azure. Commands. FrontDoor. Models. PSFrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="4ba2b-154">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span></span>
## <span data-ttu-id="4ba2b-155">Пуск</span><span class="sxs-lookup"><span data-stu-id="4ba2b-155">NOTES</span></span>

## <span data-ttu-id="4ba2b-156">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4ba2b-156">RELATED LINKS</span></span>

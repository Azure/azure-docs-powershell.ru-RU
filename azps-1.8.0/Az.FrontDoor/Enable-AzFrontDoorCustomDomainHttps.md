---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/enable-azfrontdoorcustomdomainhttps
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Enable-AzFrontDoorCustomDomainHttps.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Enable-AzFrontDoorCustomDomainHttps.md
ms.openlocfilehash: b07893dcf8394d4378a75f48a6321e393a21cfc5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93900645"
---
# <span data-ttu-id="ed246-101">Enable-AzFrontDoorCustomDomainHttps</span><span class="sxs-lookup"><span data-stu-id="ed246-101">Enable-AzFrontDoorCustomDomainHttps</span></span>

## <span data-ttu-id="ed246-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ed246-102">SYNOPSIS</span></span>
<span data-ttu-id="ed246-103">Включите HTTPS для пользовательского домена с помощью управляемого сертификата с передней дверцой или с помощью собственного сертификата из хранилища ключей Azure.</span><span class="sxs-lookup"><span data-stu-id="ed246-103">Enable HTTPS for a custom domain using Front Door managed certificate or using own certificate from Azure Key Vault.</span></span>

## <span data-ttu-id="ed246-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ed246-104">SYNTAX</span></span>

### <span data-ttu-id="ed246-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ed246-105">ByFieldsParameterSet (Default)</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -ResourceGroupName <String> -FrontDoorName <String>
 -FrontendEndpointName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ed246-106">ByFieldsWithVaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="ed246-106">ByFieldsWithVaultParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -ResourceGroupName <String> -FrontDoorName <String>
 -FrontendEndpointName <String> -VaultId <String> -SecretName <String> -SecretVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed246-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ed246-107">ByResourceIdParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed246-108">ByResourceIdWithVaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="ed246-108">ByResourceIdWithVaultParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -ResourceId <String> -VaultId <String> -SecretName <String>
 -SecretVersion <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed246-109">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ed246-109">ByObjectParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -InputObject <PSFrontendEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed246-110">ByObjectWithVaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="ed246-110">ByObjectWithVaultParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -InputObject <PSFrontendEndpoint> -VaultId <String> -SecretName <String>
 -SecretVersion <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed246-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ed246-111">DESCRIPTION</span></span>
<span data-ttu-id="ed246-112">Параметр **Enable-AzFrontDoorCustomDomainHttps** включает HTTPS для настраиваемого домена.</span><span class="sxs-lookup"><span data-stu-id="ed246-112">The **Enable-AzFrontDoorCustomDomainHttps** enables HTTPS for a custom domain.</span></span>

## <span data-ttu-id="ed246-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ed246-113">EXAMPLES</span></span>

### <span data-ttu-id="ed246-114">Пример 1: включение HTTPS для пользовательского домена с FrontDoorName и ResourceGroupName с помощью управляемого сертификата передней дверцы.</span><span class="sxs-lookup"><span data-stu-id="ed246-114">Example 1: Enable HTTPS for a custom domain with FrontDoorName and ResourceGroupName using Front Door managed certificate.</span></span>
```powershell
PS C:\> Enable-AzFrontDoorCustomDomainHttps -ResourceGroupName "resourcegroup1" -FrontDoorName "frontdoor1" -FrontendEndpointName "frontendpointname1-custom-xyz"


HostName                         : frontendpointname1.custom.xyz
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Enabling
CustomHttpsProvisioningSubstate  : SubmittingDomainControlValidationRequest
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

<span data-ttu-id="ed246-115">Включите HTTPS для пользовательского домена "frontendpointname1-Custom-XYZ", который является частью передней дверцы "frontdoor1" в группе ресурсов "resourcegroup1" с помощью управляемого сертификата передней дверцы.</span><span class="sxs-lookup"><span data-stu-id="ed246-115">Enable HTTPS for a custom domain "frontendpointname1-custom-xyz" that is part of Front Door "frontdoor1" in resource group "resourcegroup1" using Front Door managed certificate.</span></span>

### <span data-ttu-id="ed246-116">Пример 2: включение HTTPS для пользовательского домена с FrontDoorName и ResourceGroupName с помощью собственного сертификата в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="ed246-116">Example 2: Enable HTTPS for a custom domain with FrontDoorName and ResourceGroupName using own certificate in Key Vault.</span></span>
```powershell
PS C:\> Enable-AzFrontDoorCustomDomainHttps -ResourceGroupName "resourcegroup1" -FrontDoorName "frontdoor1" -FrontendEndpointName "frontendpointname1-custom-xyz" -Vault $vaultId -secretName $secretName -SecretVersion $secretVersion


HostName                         : frontendpointname1.custom.xyz
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Enabling
CustomHttpsProvisioningSubstate  : SubmittingDomainControlValidationRequest
CertificateSource                : AzureKeyVault
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

<span data-ttu-id="ed246-117">Включите HTTPS для пользовательского домена "frontendpointname1-Custom-XYZ", который является частью передней дверцы "frontdoor1" в группе ресурсов "resourcegroup1" с помощью управляемого сертификата передней дверцы.</span><span class="sxs-lookup"><span data-stu-id="ed246-117">Enable HTTPS for a custom domain "frontendpointname1-custom-xyz" that is part of Front Door "frontdoor1" in resource group "resourcegroup1" using Front Door managed certificate.</span></span>

### <span data-ttu-id="ed246-118">Пример 3: включите HTTPS для пользовательского домена с объектом PSFrontendEndpoint, используя управляемый сертификат передней дверцы.</span><span class="sxs-lookup"><span data-stu-id="ed246-118">Example 3: Enable HTTPS for a custom domain with PSFrontendEndpoint object using Front Door managed certificate.</span></span>
```powershell
PS C:\> Get-AzFrontDoorFrontendEndpoint -ResourceGroupName "resourcegroup1" -FrontDoorName "frontdoor1" -FrontendEndpointName "frontendpointname1-custom-xyz" | Enable-AzFrontDoorCustomDomainHttps 


HostName                         : frontendpointname1.custom.xyz
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Enabling
CustomHttpsProvisioningSubstate  : SubmittingDomainControlValidationRequest
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

<span data-ttu-id="ed246-119">Включите HTTPS для пользовательского домена с объектом PSFrontendEndpoint, используя управляемый сертификат передней дверцы.</span><span class="sxs-lookup"><span data-stu-id="ed246-119">Enable HTTPS for a custom domain with PSFrontendEndpoint object using Front Door managed certificate.</span></span>

### <span data-ttu-id="ed246-120">Пример 4: включение HTTPS для пользовательского домена с идентификатором ресурса с помощью управляемого сертификата с использованием передней дверцы.</span><span class="sxs-lookup"><span data-stu-id="ed246-120">Example 4: Enable HTTPS for a custom domain with resource id using Front Door managed certificate.</span></span>
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

<span data-ttu-id="ed246-121">Включите HTTPS для пользовательского домена "frontendpointname1-Custom-XYZ" с идентификатором ресурса $resourceId помощью управляемого сертификата передней дверцы.</span><span class="sxs-lookup"><span data-stu-id="ed246-121">Enable HTTPS for a custom domain "frontendpointname1-custom-xyz" with resource id $resourceId using Front Door managed certificate.</span></span>

## <span data-ttu-id="ed246-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ed246-122">PARAMETERS</span></span>

### <span data-ttu-id="ed246-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed246-123">-DefaultProfile</span></span>
<span data-ttu-id="ed246-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ed246-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed246-125">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="ed246-125">-FrontDoorName</span></span>
<span data-ttu-id="ed246-126">Название передней дверцы.</span><span class="sxs-lookup"><span data-stu-id="ed246-126">The name of the Front Door.</span></span>

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

### <span data-ttu-id="ed246-127">-FrontendEndpointName</span><span class="sxs-lookup"><span data-stu-id="ed246-127">-FrontendEndpointName</span></span>
<span data-ttu-id="ed246-128">Имя конечной точки переднего плана.</span><span class="sxs-lookup"><span data-stu-id="ed246-128">Frontend endpoint name.</span></span>

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

### <span data-ttu-id="ed246-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ed246-129">-InputObject</span></span>
<span data-ttu-id="ed246-130">Обновляемый объект одноинтерфейсной точки.</span><span class="sxs-lookup"><span data-stu-id="ed246-130">The Frontend endpoint object to update.</span></span>

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

### <span data-ttu-id="ed246-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed246-131">-ResourceGroupName</span></span>
<span data-ttu-id="ed246-132">Группа ресурсов, к которой принадлежит передняя дверь.</span><span class="sxs-lookup"><span data-stu-id="ed246-132">The resource group to which the Front Door belongs.</span></span>

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

### <span data-ttu-id="ed246-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ed246-133">-ResourceId</span></span>
<span data-ttu-id="ed246-134">Идентификатор ресурса конечной точки передней дверцы для включения HTTPS</span><span class="sxs-lookup"><span data-stu-id="ed246-134">Resource Id of the Front Door endpoint to enable https</span></span>

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

### <span data-ttu-id="ed246-135">-SecretName</span><span class="sxs-lookup"><span data-stu-id="ed246-135">-SecretName</span></span>
<span data-ttu-id="ed246-136">Имя секрета в хранилище ключей, представляющее полный PFX-сертификат.</span><span class="sxs-lookup"><span data-stu-id="ed246-136">The name of the Key Vault secret representing the full certificate PFX</span></span>

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

### <span data-ttu-id="ed246-137">-SecretVersion</span><span class="sxs-lookup"><span data-stu-id="ed246-137">-SecretVersion</span></span>
<span data-ttu-id="ed246-138">Версия секрета хранилища ключей, представляющая полный PFX-сертификат.</span><span class="sxs-lookup"><span data-stu-id="ed246-138">The version of the Key Vault secret representing the full certificate PFX</span></span>

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

### <span data-ttu-id="ed246-139">-VaultId</span><span class="sxs-lookup"><span data-stu-id="ed246-139">-VaultId</span></span>
<span data-ttu-id="ed246-140">Идентификатор хранилища ключей, содержащий сертификат SSL.</span><span class="sxs-lookup"><span data-stu-id="ed246-140">The Key Vault id containing the SSL certificate</span></span>

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

### <span data-ttu-id="ed246-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ed246-141">-Confirm</span></span>
<span data-ttu-id="ed246-142">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ed246-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed246-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed246-143">-WhatIf</span></span>
<span data-ttu-id="ed246-144">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ed246-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ed246-145">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ed246-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed246-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed246-146">CommonParameters</span></span>
<span data-ttu-id="ed246-147">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ed246-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed246-148">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ed246-148">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed246-149">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ed246-149">INPUTS</span></span>

### <span data-ttu-id="ed246-150">System. String</span><span class="sxs-lookup"><span data-stu-id="ed246-150">System.String</span></span>

## <span data-ttu-id="ed246-151">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ed246-151">OUTPUTS</span></span>

### <span data-ttu-id="ed246-152">Microsoft. Azure. Commands. FrontDoor. Models. PSFrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="ed246-152">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span></span>

## <span data-ttu-id="ed246-153">Пуск</span><span class="sxs-lookup"><span data-stu-id="ed246-153">NOTES</span></span>

## <span data-ttu-id="ed246-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ed246-154">RELATED LINKS</span></span>

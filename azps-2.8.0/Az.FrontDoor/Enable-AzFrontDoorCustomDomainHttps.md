---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/enable-azfrontdoorcustomdomainhttps
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Enable-AzFrontDoorCustomDomainHttps.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Enable-AzFrontDoorCustomDomainHttps.md
ms.openlocfilehash: 6edf891d693e0c1cb2143236d12e623fdd2b4a3f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720909"
---
# <span data-ttu-id="8c6c5-101">Enable-AzFrontDoorCustomDomainHttps</span><span class="sxs-lookup"><span data-stu-id="8c6c5-101">Enable-AzFrontDoorCustomDomainHttps</span></span>

## <span data-ttu-id="8c6c5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8c6c5-102">SYNOPSIS</span></span>
<span data-ttu-id="8c6c5-103">Включите HTTPS для пользовательского домена с помощью управляемого сертификата с передней дверцой или с помощью собственного сертификата из хранилища ключей Azure.</span><span class="sxs-lookup"><span data-stu-id="8c6c5-103">Enable HTTPS for a custom domain using Front Door managed certificate or using own certificate from Azure Key Vault.</span></span>

## <span data-ttu-id="8c6c5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8c6c5-104">SYNTAX</span></span>

### <span data-ttu-id="8c6c5-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8c6c5-105">ByFieldsParameterSet (Default)</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -ResourceGroupName <String> -FrontDoorName <String>
 -FrontendEndpointName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8c6c5-106">ByFieldsWithVaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="8c6c5-106">ByFieldsWithVaultParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -ResourceGroupName <String> -FrontDoorName <String>
 -FrontendEndpointName <String> -VaultId <String> -SecretName <String> -SecretVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c6c5-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8c6c5-107">ByResourceIdParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c6c5-108">ByResourceIdWithVaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="8c6c5-108">ByResourceIdWithVaultParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -ResourceId <String> -VaultId <String> -SecretName <String>
 -SecretVersion <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c6c5-109">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8c6c5-109">ByObjectParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -InputObject <PSFrontendEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c6c5-110">ByObjectWithVaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="8c6c5-110">ByObjectWithVaultParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -InputObject <PSFrontendEndpoint> -VaultId <String> -SecretName <String>
 -SecretVersion <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c6c5-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8c6c5-111">DESCRIPTION</span></span>
<span data-ttu-id="8c6c5-112">Параметр **Enable-AzFrontDoorCustomDomainHttps** включает HTTPS для настраиваемого домена.</span><span class="sxs-lookup"><span data-stu-id="8c6c5-112">The **Enable-AzFrontDoorCustomDomainHttps** enables HTTPS for a custom domain.</span></span>

## <span data-ttu-id="8c6c5-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8c6c5-113">EXAMPLES</span></span>

### <span data-ttu-id="8c6c5-114">Пример 1: включение HTTPS для пользовательского домена с FrontDoorName и ResourceGroupName с помощью управляемого сертификата передней дверцы.</span><span class="sxs-lookup"><span data-stu-id="8c6c5-114">Example 1: Enable HTTPS for a custom domain with FrontDoorName and ResourceGroupName using Front Door managed certificate.</span></span>
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

<span data-ttu-id="8c6c5-115">Включите HTTPS для пользовательского домена "frontendpointname1-Custom-XYZ", который является частью передней дверцы "frontdoor1" в группе ресурсов "resourcegroup1" с помощью управляемого сертификата передней дверцы.</span><span class="sxs-lookup"><span data-stu-id="8c6c5-115">Enable HTTPS for a custom domain "frontendpointname1-custom-xyz" that is part of Front Door "frontdoor1" in resource group "resourcegroup1" using Front Door managed certificate.</span></span>

### <span data-ttu-id="8c6c5-116">Пример 2: включение HTTPS для пользовательского домена с FrontDoorName и ResourceGroupName с помощью собственного сертификата в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="8c6c5-116">Example 2: Enable HTTPS for a custom domain with FrontDoorName and ResourceGroupName using own certificate in Key Vault.</span></span>
```powershell
PS C:\> $vaultId = (Get-AzKeyVault -VaultName $vaultName).ResourceId
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

<span data-ttu-id="8c6c5-117">Включите HTTPS для пользовательского домена "frontendpointname1-Custom-XYZ", который является частью передней дверцы "frontdoor1" в группе ресурсов "resourcegroup1" с помощью управляемого сертификата передней дверцы.</span><span class="sxs-lookup"><span data-stu-id="8c6c5-117">Enable HTTPS for a custom domain "frontendpointname1-custom-xyz" that is part of Front Door "frontdoor1" in resource group "resourcegroup1" using Front Door managed certificate.</span></span>

### <span data-ttu-id="8c6c5-118">Пример 3: включите HTTPS для пользовательского домена с объектом PSFrontendEndpoint, используя управляемый сертификат передней дверцы.</span><span class="sxs-lookup"><span data-stu-id="8c6c5-118">Example 3: Enable HTTPS for a custom domain with PSFrontendEndpoint object using Front Door managed certificate.</span></span>
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

<span data-ttu-id="8c6c5-119">Включите HTTPS для пользовательского домена с объектом PSFrontendEndpoint, используя управляемый сертификат передней дверцы.</span><span class="sxs-lookup"><span data-stu-id="8c6c5-119">Enable HTTPS for a custom domain with PSFrontendEndpoint object using Front Door managed certificate.</span></span>

### <span data-ttu-id="8c6c5-120">Пример 4: включение HTTPS для пользовательского домена с идентификатором ресурса с помощью управляемого сертификата с использованием передней дверцы.</span><span class="sxs-lookup"><span data-stu-id="8c6c5-120">Example 4: Enable HTTPS for a custom domain with resource id using Front Door managed certificate.</span></span>
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

<span data-ttu-id="8c6c5-121">Включите HTTPS для пользовательского домена "frontendpointname1-Custom-XYZ" с идентификатором ресурса $resourceId помощью управляемого сертификата передней дверцы.</span><span class="sxs-lookup"><span data-stu-id="8c6c5-121">Enable HTTPS for a custom domain "frontendpointname1-custom-xyz" with resource id $resourceId using Front Door managed certificate.</span></span>

## <span data-ttu-id="8c6c5-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8c6c5-122">PARAMETERS</span></span>

### <span data-ttu-id="8c6c5-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c6c5-123">-DefaultProfile</span></span>
<span data-ttu-id="8c6c5-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8c6c5-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8c6c5-125">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="8c6c5-125">-FrontDoorName</span></span>
<span data-ttu-id="8c6c5-126">Название передней дверцы.</span><span class="sxs-lookup"><span data-stu-id="8c6c5-126">The name of the Front Door.</span></span>

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

### <span data-ttu-id="8c6c5-127">-FrontendEndpointName</span><span class="sxs-lookup"><span data-stu-id="8c6c5-127">-FrontendEndpointName</span></span>
<span data-ttu-id="8c6c5-128">Имя конечной точки переднего плана.</span><span class="sxs-lookup"><span data-stu-id="8c6c5-128">Frontend endpoint name.</span></span>

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

### <span data-ttu-id="8c6c5-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8c6c5-129">-InputObject</span></span>
<span data-ttu-id="8c6c5-130">Обновляемый объект одноинтерфейсной точки.</span><span class="sxs-lookup"><span data-stu-id="8c6c5-130">The Frontend endpoint object to update.</span></span>

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

### <span data-ttu-id="8c6c5-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c6c5-131">-ResourceGroupName</span></span>
<span data-ttu-id="8c6c5-132">Группа ресурсов, к которой принадлежит передняя дверь.</span><span class="sxs-lookup"><span data-stu-id="8c6c5-132">The resource group to which the Front Door belongs.</span></span>

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

### <span data-ttu-id="8c6c5-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8c6c5-133">-ResourceId</span></span>
<span data-ttu-id="8c6c5-134">Идентификатор ресурса конечной точки передней дверцы для включения HTTPS</span><span class="sxs-lookup"><span data-stu-id="8c6c5-134">Resource Id of the Front Door endpoint to enable https</span></span>

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

### <span data-ttu-id="8c6c5-135">-SecretName</span><span class="sxs-lookup"><span data-stu-id="8c6c5-135">-SecretName</span></span>
<span data-ttu-id="8c6c5-136">Имя секрета в хранилище ключей, представляющее полный PFX-сертификат.</span><span class="sxs-lookup"><span data-stu-id="8c6c5-136">The name of the Key Vault secret representing the full certificate PFX</span></span>

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

### <span data-ttu-id="8c6c5-137">-SecretVersion</span><span class="sxs-lookup"><span data-stu-id="8c6c5-137">-SecretVersion</span></span>
<span data-ttu-id="8c6c5-138">Версия секрета хранилища ключей, представляющая полный PFX-сертификат.</span><span class="sxs-lookup"><span data-stu-id="8c6c5-138">The version of the Key Vault secret representing the full certificate PFX</span></span>

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

### <span data-ttu-id="8c6c5-139">-VaultId</span><span class="sxs-lookup"><span data-stu-id="8c6c5-139">-VaultId</span></span>
<span data-ttu-id="8c6c5-140">Идентификатор хранилища ключей, содержащий сертификат SSL.</span><span class="sxs-lookup"><span data-stu-id="8c6c5-140">The Key Vault id containing the SSL certificate</span></span>

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

### <span data-ttu-id="8c6c5-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8c6c5-141">-Confirm</span></span>
<span data-ttu-id="8c6c5-142">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8c6c5-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c6c5-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c6c5-143">-WhatIf</span></span>
<span data-ttu-id="8c6c5-144">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8c6c5-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8c6c5-145">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8c6c5-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c6c5-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c6c5-146">CommonParameters</span></span>
<span data-ttu-id="8c6c5-147">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8c6c5-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c6c5-148">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8c6c5-148">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c6c5-149">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8c6c5-149">INPUTS</span></span>

### <span data-ttu-id="8c6c5-150">System. String</span><span class="sxs-lookup"><span data-stu-id="8c6c5-150">System.String</span></span>

## <span data-ttu-id="8c6c5-151">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8c6c5-151">OUTPUTS</span></span>

### <span data-ttu-id="8c6c5-152">Microsoft. Azure. Commands. FrontDoor. Models. PSFrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="8c6c5-152">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span></span>

## <span data-ttu-id="8c6c5-153">Пуск</span><span class="sxs-lookup"><span data-stu-id="8c6c5-153">NOTES</span></span>

## <span data-ttu-id="8c6c5-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8c6c5-154">RELATED LINKS</span></span>

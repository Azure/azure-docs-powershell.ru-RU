---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/disable-azfrontdoorcustomdomainhttps
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Disable-AzFrontDoorCustomDomainHttps.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Disable-AzFrontDoorCustomDomainHttps.md
ms.openlocfilehash: 2f6b5635b029548f8d92917e0abfca18d5c0c415
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93900670"
---
# <span data-ttu-id="00da2-101">Disable-AzFrontDoorCustomDomainHttps</span><span class="sxs-lookup"><span data-stu-id="00da2-101">Disable-AzFrontDoorCustomDomainHttps</span></span>

## <span data-ttu-id="00da2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="00da2-102">SYNOPSIS</span></span>
<span data-ttu-id="00da2-103">Отключение HTTPS для настраиваемого домена</span><span class="sxs-lookup"><span data-stu-id="00da2-103">Disable HTTPS for a custom domain</span></span>

## <span data-ttu-id="00da2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="00da2-104">SYNTAX</span></span>

### <span data-ttu-id="00da2-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="00da2-105">ByFieldsParameterSet (Default)</span></span>
```
Disable-AzFrontDoorCustomDomainHttps -ResourceGroupName <String> -FrontDoorName <String>
 -FrontendEndpointName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="00da2-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="00da2-106">ByResourceIdParameterSet</span></span>
```
Disable-AzFrontDoorCustomDomainHttps -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00da2-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="00da2-107">ByObjectParameterSet</span></span>
```
Disable-AzFrontDoorCustomDomainHttps -InputObject <PSFrontendEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="00da2-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="00da2-108">DESCRIPTION</span></span>
<span data-ttu-id="00da2-109">**Disable-AzFrontDoorCustomDomainHttps** отключает HTTPS для настраиваемого домена.</span><span class="sxs-lookup"><span data-stu-id="00da2-109">The **Disable-AzFrontDoorCustomDomainHttps** disables HTTPS for a custom domain.</span></span>

## <span data-ttu-id="00da2-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="00da2-110">EXAMPLES</span></span>

### <span data-ttu-id="00da2-111">Пример 1: отключение HTTPS для настраиваемого домена с помощью FrontDoorName и ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="00da2-111">Example 1: Disable HTTPS for a custom domain with FrontDoorName and ResourceGroupName.</span></span>
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

<span data-ttu-id="00da2-112">Отключите HTTPS для собственного домена "frontendpointname1-Custom-XYZ" с FrontDoorName как "frontdoor1" и ResourceGroupName как "resourcegroup1".</span><span class="sxs-lookup"><span data-stu-id="00da2-112">Disable HTTPS for a custom domain "frontendpointname1-custom-xyz" with FrontDoorName as "frontdoor1" and ResourceGroupName as "resourcegroup1".</span></span>

### <span data-ttu-id="00da2-113">Пример 2: отключение HTTPS для настраиваемого домена с объектом PSFrontendEndpoint.</span><span class="sxs-lookup"><span data-stu-id="00da2-113">Example 2: Disable HTTPS for a custom domain with PSFrontendEndpoint object.</span></span>
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

<span data-ttu-id="00da2-114">Отключите HTTPS для настраиваемого домена с объектом PSFrontendEndpoint.</span><span class="sxs-lookup"><span data-stu-id="00da2-114">Disable HTTPS for a custom domain with PSFrontendEndpoint object.</span></span>

### <span data-ttu-id="00da2-115">Пример 3: отключение HTTPS для настраиваемого домена с ResourceId.</span><span class="sxs-lookup"><span data-stu-id="00da2-115">Example 3: Disable HTTPS for a custom domain with ResourceId.</span></span>
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

<span data-ttu-id="00da2-116">Отключите HTTPS для собственного домена "frontendpointname1-Custom-XYZ" с ResourceId как $resourceId.</span><span class="sxs-lookup"><span data-stu-id="00da2-116">Disable HTTPS for a custom domain "frontendpointname1-custom-xyz" with ResourceId as $resourceId.</span></span>

## <span data-ttu-id="00da2-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="00da2-117">PARAMETERS</span></span>

### <span data-ttu-id="00da2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00da2-118">-DefaultProfile</span></span>
<span data-ttu-id="00da2-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="00da2-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="00da2-120">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="00da2-120">-FrontDoorName</span></span>
<span data-ttu-id="00da2-121">Название передней дверцы.</span><span class="sxs-lookup"><span data-stu-id="00da2-121">The name of the Front Door.</span></span>

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

### <span data-ttu-id="00da2-122">-FrontendEndpointName</span><span class="sxs-lookup"><span data-stu-id="00da2-122">-FrontendEndpointName</span></span>
<span data-ttu-id="00da2-123">Имя конечной точки переднего плана.</span><span class="sxs-lookup"><span data-stu-id="00da2-123">Frontend endpoint name.</span></span>

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

### <span data-ttu-id="00da2-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="00da2-124">-InputObject</span></span>
<span data-ttu-id="00da2-125">Обновляемый объект одноинтерфейсной точки.</span><span class="sxs-lookup"><span data-stu-id="00da2-125">The Frontend endpoint object to update.</span></span>

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

### <span data-ttu-id="00da2-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00da2-126">-ResourceGroupName</span></span>
<span data-ttu-id="00da2-127">Группа ресурсов, к которой принадлежит передняя дверь.</span><span class="sxs-lookup"><span data-stu-id="00da2-127">The resource group to which the Front Door belongs.</span></span>

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

### <span data-ttu-id="00da2-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="00da2-128">-ResourceId</span></span>
<span data-ttu-id="00da2-129">Идентификатор ресурса конечной точки передней дверцы для отключения HTTPS</span><span class="sxs-lookup"><span data-stu-id="00da2-129">Resource Id of the Front Door endpoint to disable https</span></span>

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

### <span data-ttu-id="00da2-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="00da2-130">-Confirm</span></span>
<span data-ttu-id="00da2-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="00da2-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00da2-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00da2-132">-WhatIf</span></span>
<span data-ttu-id="00da2-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="00da2-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="00da2-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="00da2-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00da2-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00da2-135">CommonParameters</span></span>
<span data-ttu-id="00da2-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="00da2-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00da2-137">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="00da2-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00da2-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="00da2-138">INPUTS</span></span>

### <span data-ttu-id="00da2-139">System. String</span><span class="sxs-lookup"><span data-stu-id="00da2-139">System.String</span></span>

## <span data-ttu-id="00da2-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="00da2-140">OUTPUTS</span></span>

### <span data-ttu-id="00da2-141">Microsoft. Azure. Commands. FrontDoor. Models. PSFrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="00da2-141">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span></span>

## <span data-ttu-id="00da2-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="00da2-142">NOTES</span></span>

## <span data-ttu-id="00da2-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="00da2-143">RELATED LINKS</span></span>

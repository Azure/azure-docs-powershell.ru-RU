---
Module Name: Az.FrontDoor
Module Guid: 91832aaa-dc11-4583-8239-adb7df531604
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor
Help Version: 0.1.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Az.FrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Az.FrontDoor.md
ms.openlocfilehash: 6f42c3e8588a40b2e912b2c93ec2bfb9534efeef
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "93719800"
---
# <span data-ttu-id="3e228-101">AZ. FrontDoor Module</span><span class="sxs-lookup"><span data-stu-id="3e228-101">Az.FrontDoor Module</span></span>
## <span data-ttu-id="3e228-102">Nописание</span><span class="sxs-lookup"><span data-stu-id="3e228-102">Description</span></span>
<span data-ttu-id="3e228-103">В этом разделе описаны командлеты PowerShell для Azure в среде диспетчера ресурсов Azure (ARM) для службы "Передняя дверь" Azure.</span><span class="sxs-lookup"><span data-stu-id="3e228-103">The topics in this section document the Azure PowerShell cmdlets for Azure Front Door Service in the Azure Resource Manager (ARM) framework.</span></span> <span data-ttu-id="3e228-104">Командлеты существуют в пространстве имен Microsoft. Azure. Commands. FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="3e228-104">The cmdlets exist in the Microsoft.Azure.Commands.FrontDoor namespace.</span></span>

## <span data-ttu-id="3e228-105">Командлеты AZ. FrontDoor</span><span class="sxs-lookup"><span data-stu-id="3e228-105">Az.FrontDoor Cmdlets</span></span>
### [<span data-ttu-id="3e228-106">Disable-AzFrontDoorCustomDomainHttps</span><span class="sxs-lookup"><span data-stu-id="3e228-106">Disable-AzFrontDoorCustomDomainHttps</span></span>](Disable-AzFrontDoorCustomDomainHttps.md)
<span data-ttu-id="3e228-107">Отключение HTTPS для настраиваемого домена</span><span class="sxs-lookup"><span data-stu-id="3e228-107">Disable HTTPS for a custom domain</span></span>

### [<span data-ttu-id="3e228-108">Enable-AzFrontDoorCustomDomainHttps</span><span class="sxs-lookup"><span data-stu-id="3e228-108">Enable-AzFrontDoorCustomDomainHttps</span></span>](Enable-AzFrontDoorCustomDomainHttps.md)
<span data-ttu-id="3e228-109">Включите HTTPS для пользовательского домена с помощью управляемого сертификата с передней дверцой или с помощью собственного сертификата из хранилища ключей Azure.</span><span class="sxs-lookup"><span data-stu-id="3e228-109">Enable HTTPS for a custom domain using Front Door managed certificate or using own certificate from Azure Key Vault.</span></span>

### [<span data-ttu-id="3e228-110">Get-AzFrontDoor</span><span class="sxs-lookup"><span data-stu-id="3e228-110">Get-AzFrontDoor</span></span>](Get-AzFrontDoor.md)
<span data-ttu-id="3e228-111">Получение подсистемы балансировки нагрузки для передней дверцы</span><span class="sxs-lookup"><span data-stu-id="3e228-111">Get Front Door load balancer</span></span>

### [<span data-ttu-id="3e228-112">Get-AzFrontDoorFireWallPolicy</span><span class="sxs-lookup"><span data-stu-id="3e228-112">Get-AzFrontDoorFireWallPolicy</span></span>](Get-AzFrontDoorFireWallPolicy.md)
<span data-ttu-id="3e228-113">Получение политики WAF</span><span class="sxs-lookup"><span data-stu-id="3e228-113">Get WAF policy</span></span>

### [<span data-ttu-id="3e228-114">Get-AzFrontDoorFrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="3e228-114">Get-AzFrontDoorFrontendEndpoint</span></span>](Get-AzFrontDoorFrontendEndpoint.md)
<span data-ttu-id="3e228-115">Получение конечной точки переднего плана для передней дверцы.</span><span class="sxs-lookup"><span data-stu-id="3e228-115">Get a front door frontend endpoint.</span></span>

### [<span data-ttu-id="3e228-116">New-AzFrontDoor</span><span class="sxs-lookup"><span data-stu-id="3e228-116">New-AzFrontDoor</span></span>](New-AzFrontDoor.md)
<span data-ttu-id="3e228-117">Создание нового подсистемы балансировки нагрузки на передней дверцу Azure</span><span class="sxs-lookup"><span data-stu-id="3e228-117">Create a new Azure Front Door load balancer</span></span>

### [<span data-ttu-id="3e228-118">New-AzFrontDoorBackendObject</span><span class="sxs-lookup"><span data-stu-id="3e228-118">New-AzFrontDoorBackendObject</span></span>](New-AzFrontDoorBackendObject.md)
<span data-ttu-id="3e228-119">Создание объекта PSBackend</span><span class="sxs-lookup"><span data-stu-id="3e228-119">Create a PSBackend object</span></span>

### [<span data-ttu-id="3e228-120">New-AzFrontDoorBackendPoolObject</span><span class="sxs-lookup"><span data-stu-id="3e228-120">New-AzFrontDoorBackendPoolObject</span></span>](New-AzFrontDoorBackendPoolObject.md)
<span data-ttu-id="3e228-121">Создание объекта PSBackendPool для создания передней дверцы</span><span class="sxs-lookup"><span data-stu-id="3e228-121">Create a PSBackendPool object for Front Door creation</span></span>

### [<span data-ttu-id="3e228-122">New-AzFrontDoorCustomRuleObject</span><span class="sxs-lookup"><span data-stu-id="3e228-122">New-AzFrontDoorCustomRuleObject</span></span>](New-AzFrontDoorCustomRuleObject.md)
<span data-ttu-id="3e228-123">Создание объекта CustomRule для создания политики WAF</span><span class="sxs-lookup"><span data-stu-id="3e228-123">Create CustomRule Object for WAF policy creation</span></span>

### [<span data-ttu-id="3e228-124">New-AzFrontDoorFireWallPolicy</span><span class="sxs-lookup"><span data-stu-id="3e228-124">New-AzFrontDoorFireWallPolicy</span></span>](New-AzFrontDoorFireWallPolicy.md)
<span data-ttu-id="3e228-125">Создание политики WAF</span><span class="sxs-lookup"><span data-stu-id="3e228-125">Create WAF policy</span></span>

### [<span data-ttu-id="3e228-126">New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="3e228-126">New-AzFrontDoorFrontendEndpointObject</span></span>](New-AzFrontDoorFrontendEndpointObject.md)
<span data-ttu-id="3e228-127">Создание объекта PSFrontendEndpoint для создания передней дверцы</span><span class="sxs-lookup"><span data-stu-id="3e228-127">Create a PSFrontendEndpoint Object for Front Door creation</span></span>

### [<span data-ttu-id="3e228-128">New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="3e228-128">New-AzFrontDoorHealthProbeSettingObject</span></span>](New-AzFrontDoorHealthProbeSettingObject.md)
<span data-ttu-id="3e228-129">Создание объекта PSHealthProbeSetting для создания передней дверцы</span><span class="sxs-lookup"><span data-stu-id="3e228-129">Create a PSHealthProbeSetting object for Front Door creation</span></span>

### [<span data-ttu-id="3e228-130">New-AzFrontDoorLoadBalancingSettingObject</span><span class="sxs-lookup"><span data-stu-id="3e228-130">New-AzFrontDoorLoadBalancingSettingObject</span></span>](New-AzFrontDoorLoadBalancingSettingObject.md)
<span data-ttu-id="3e228-131">Создание объекта PSLoadBalancingSetting для создания передней дверцы</span><span class="sxs-lookup"><span data-stu-id="3e228-131">Create a PSLoadBalancingSetting object for Front Door creation</span></span>

### [<span data-ttu-id="3e228-132">New-AzFrontDoorManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="3e228-132">New-AzFrontDoorManagedRuleObject</span></span>](New-AzFrontDoorManagedRuleObject.md)
<span data-ttu-id="3e228-133">Создание объекта ManagedRule для создания политики WAF</span><span class="sxs-lookup"><span data-stu-id="3e228-133">Create ManagedRule Object for WAF policy creation</span></span>

### [<span data-ttu-id="3e228-134">New-AzFrontDoorManagedRuleOverrideObject</span><span class="sxs-lookup"><span data-stu-id="3e228-134">New-AzFrontDoorManagedRuleOverrideObject</span></span>](New-AzFrontDoorManagedRuleOverrideObject.md)
<span data-ttu-id="3e228-135">Создание объекта переопределения управляемого правила</span><span class="sxs-lookup"><span data-stu-id="3e228-135">Create managed rule override object</span></span>

### [<span data-ttu-id="3e228-136">New-AzFrontDoorMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="3e228-136">New-AzFrontDoorMatchConditionObject</span></span>](New-AzFrontDoorMatchConditionObject.md)
<span data-ttu-id="3e228-137">Создание объекта MatchCondition для создания политики WAF</span><span class="sxs-lookup"><span data-stu-id="3e228-137">Create MatchCondition Object for WAF policy creation</span></span>

### [<span data-ttu-id="3e228-138">New-AzFrontDoorRoutingRuleObject</span><span class="sxs-lookup"><span data-stu-id="3e228-138">New-AzFrontDoorRoutingRuleObject</span></span>](New-AzFrontDoorRoutingRuleObject.md)
<span data-ttu-id="3e228-139">Создание PSRoutingRuleObject для создания передней дверцы</span><span class="sxs-lookup"><span data-stu-id="3e228-139">Create a PSRoutingRuleObject for Front Door creation</span></span>

### [<span data-ttu-id="3e228-140">New-AzFrontDoorRuleGroupOverrideObject</span><span class="sxs-lookup"><span data-stu-id="3e228-140">New-AzFrontDoorRuleGroupOverrideObject</span></span>](New-AzFrontDoorRuleGroupOverrideObject.md)
<span data-ttu-id="3e228-141">Создание объекта RuleGroupOverride для создания политики WAF</span><span class="sxs-lookup"><span data-stu-id="3e228-141">Create RuleGroupOverride Object for WAF policy creation</span></span>

### [<span data-ttu-id="3e228-142">Remove-AzFrontDoor</span><span class="sxs-lookup"><span data-stu-id="3e228-142">Remove-AzFrontDoor</span></span>](Remove-AzFrontDoor.md)
<span data-ttu-id="3e228-143">Удаление подсистемы балансировки нагрузки передней дверцы</span><span class="sxs-lookup"><span data-stu-id="3e228-143">Remove Front Door load balancer</span></span>

### [<span data-ttu-id="3e228-144">Remove-AzFrontDoorContent</span><span class="sxs-lookup"><span data-stu-id="3e228-144">Remove-AzFrontDoorContent</span></span>](Remove-AzFrontDoorContent.md)
<span data-ttu-id="3e228-145">Удаление содержимого с передней дверцы</span><span class="sxs-lookup"><span data-stu-id="3e228-145">Remove contents in Front Door</span></span>

### [<span data-ttu-id="3e228-146">Remove-AzFrontDoorFireWallPolicy</span><span class="sxs-lookup"><span data-stu-id="3e228-146">Remove-AzFrontDoorFireWallPolicy</span></span>](Remove-AzFrontDoorFireWallPolicy.md)
<span data-ttu-id="3e228-147">Удаление политики WAF</span><span class="sxs-lookup"><span data-stu-id="3e228-147">Remove WAF policy</span></span>

### [<span data-ttu-id="3e228-148">Set-AzFrontDoor</span><span class="sxs-lookup"><span data-stu-id="3e228-148">Set-AzFrontDoor</span></span>](Set-AzFrontDoor.md)
<span data-ttu-id="3e228-149">Обновление подсистемы балансировки нагрузки на передней дверце</span><span class="sxs-lookup"><span data-stu-id="3e228-149">Update a Front Door load balancer</span></span>

### [<span data-ttu-id="3e228-150">Update-AzFrontDoorFireWallPolicy</span><span class="sxs-lookup"><span data-stu-id="3e228-150">Update-AzFrontDoorFireWallPolicy</span></span>](Update-AzFrontDoorFireWallPolicy.md)
<span data-ttu-id="3e228-151">Обновление политики WAF</span><span class="sxs-lookup"><span data-stu-id="3e228-151">Update WAF policy</span></span>


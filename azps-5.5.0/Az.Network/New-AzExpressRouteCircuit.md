---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: E40CAF2F-ED57-4AC1-8B9A-E48042DD8F91
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuit.md
ms.openlocfilehash: 479b89296ae52221f714992791ed73cd14bf2fe0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100218585"
---
# <span data-ttu-id="4522d-101">New-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4522d-101">New-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="4522d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4522d-102">SYNOPSIS</span></span>
<span data-ttu-id="4522d-103">Создает канал экспресс-маршрутов Azure.</span><span class="sxs-lookup"><span data-stu-id="4522d-103">Creates an Azure express route circuit.</span></span>

## <span data-ttu-id="4522d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4522d-104">SYNTAX</span></span>

### <span data-ttu-id="4522d-105">ServiceProvider (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4522d-105">ServiceProvider (Default)</span></span>
```
New-AzExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String> [-SkuTier <String>]
 [-SkuFamily <String>] -ServiceProviderName <String> -PeeringLocation <String> -BandwidthInMbps <Int32>
 [-Peering <PSPeering[]>] [-Authorization <PSExpressRouteCircuitAuthorization[]>]
 [-AllowClassicOperations <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4522d-106">ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="4522d-106">ExpressRoutePort</span></span>
```
New-AzExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String> [-SkuTier <String>]
 [-SkuFamily <String>] -ExpressRoutePort <PSExpressRoutePort> -BandwidthInGbps <Double>
 [-Peering <PSPeering[]>] [-Authorization <PSExpressRouteCircuitAuthorization[]>]
 [-AllowClassicOperations <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4522d-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4522d-107">DESCRIPTION</span></span>
<span data-ttu-id="4522d-108">Для создания схемы экспресс-маршрутов Azure создается новый **cmdlet AzExpressRouteCircuit.**</span><span class="sxs-lookup"><span data-stu-id="4522d-108">The **New-AzExpressRouteCircuit** cmdlet creates an Azure express route circuit.</span></span>

## <span data-ttu-id="4522d-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4522d-109">EXAMPLES</span></span>

### <span data-ttu-id="4522d-110">Пример 1. Создание схемы ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="4522d-110">Example 1: Create a new ExpressRoute circuit</span></span>
```powershell
$parameters = @{
    Name='ExpressRouteCircuit'
    ResourceGroupName='ExpressRouteResourceGroup'
    Location='West US'
    SkuTier='Standard'
    SkuFamily='MeteredData'
    ServiceProviderName='Equinix'
    PeeringLocation='Silicon Valley'
    BandwidthInMbps=200
}
New-AzExpressRouteCircuit @parameters
```

### <span data-ttu-id="4522d-111">Пример 2. Создание схемы ExpressRoute в ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="4522d-111">Example 2: Create a new ExpressRoute circuit on ExpressRoutePort</span></span>
```powershell
$parameters = @{
    Name='ExpressRouteCircuit'
    ResourceGroupName='ExpressRouteResourceGroup'
    Location='West US'
    SkuTier='Standard'
    SkuFamily='MeteredData'
    ExpressRoutePort=$PSExpressRoutePort
    BandwidthInGbps=10.0
}
New-AzExpressRouteCircuit @parameters
```

## <span data-ttu-id="4522d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4522d-112">PARAMETERS</span></span>

### <span data-ttu-id="4522d-113">-AllowClassicOperations</span><span class="sxs-lookup"><span data-stu-id="4522d-113">-AllowClassicOperations</span></span>
<span data-ttu-id="4522d-114">Использование этого параметра позволяет управлять каналом с помощью классических cmdlets Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="4522d-114">The use of this parameter allows you to use the classic Azure PowerShell cmdlets to manage the circuit.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4522d-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4522d-115">-AsJob</span></span>
<span data-ttu-id="4522d-116">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="4522d-116">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4522d-117">-Authorization</span><span class="sxs-lookup"><span data-stu-id="4522d-117">-Authorization</span></span>
<span data-ttu-id="4522d-118">Список авторизации каналов.</span><span class="sxs-lookup"><span data-stu-id="4522d-118">A list of circuit authorizations.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4522d-119">-BandwidthInGbps</span><span class="sxs-lookup"><span data-stu-id="4522d-119">-BandwidthInGbps</span></span>
<span data-ttu-id="4522d-120">Пропускная способность канала при предоставлении канала для ресурса ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="4522d-120">The bandwidth of the circuit when the circuit is provisioned on an ExpressRoutePort resource.</span></span>

```yaml
Type: System.Double
Parameter Sets: ExpressRoutePort
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4522d-121">-BandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="4522d-121">-BandwidthInMbps</span></span>
<span data-ttu-id="4522d-122">Пропускная способность канала.</span><span class="sxs-lookup"><span data-stu-id="4522d-122">The bandwidth of the circuit.</span></span> <span data-ttu-id="4522d-123">Это значение должно поддерживаться поставщиком услуг.</span><span class="sxs-lookup"><span data-stu-id="4522d-123">This must be a value that is supported by the service provider.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ServiceProvider
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4522d-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4522d-124">-DefaultProfile</span></span>
<span data-ttu-id="4522d-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4522d-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4522d-126">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="4522d-126">-ExpressRoutePort</span></span>
<span data-ttu-id="4522d-127">Ссылка на ресурс ExpressRoutePort при предоставлении каналов для ресурса ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="4522d-127">The reference to the ExpressRoutePort resource when the circuit is provisioned on an ExpressRoutePort resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort
Parameter Sets: ExpressRoutePort
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4522d-128">-Force</span><span class="sxs-lookup"><span data-stu-id="4522d-128">-Force</span></span>
<span data-ttu-id="4522d-129">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="4522d-129">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4522d-130">-Location</span><span class="sxs-lookup"><span data-stu-id="4522d-130">-Location</span></span>
<span data-ttu-id="4522d-131">Расположение схемы.</span><span class="sxs-lookup"><span data-stu-id="4522d-131">The location of the circuit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4522d-132">-Name</span><span class="sxs-lookup"><span data-stu-id="4522d-132">-Name</span></span>
<span data-ttu-id="4522d-133">Имя созда создаемого контура ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="4522d-133">The name of the ExpressRoute circuit being created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4522d-134">-Пиринг</span><span class="sxs-lookup"><span data-stu-id="4522d-134">-Peering</span></span>
<span data-ttu-id="4522d-135">Одноранговая конфигурация списка.</span><span class="sxs-lookup"><span data-stu-id="4522d-135">A list peer configurations.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPeering[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4522d-136">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="4522d-136">-PeeringLocation</span></span>
<span data-ttu-id="4522d-137">Имя расположения пиринга, поддерживаемого поставщиком услуг.</span><span class="sxs-lookup"><span data-stu-id="4522d-137">The name of the peering location supported by the service provider.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceProvider
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4522d-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4522d-138">-ResourceGroupName</span></span>
<span data-ttu-id="4522d-139">Группа ресурсов, которая будет содержать канал.</span><span class="sxs-lookup"><span data-stu-id="4522d-139">The resource group that will contain the circuit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4522d-140">-ServiceProviderName</span><span class="sxs-lookup"><span data-stu-id="4522d-140">-ServiceProviderName</span></span>
<span data-ttu-id="4522d-141">Имя поставщика услуг каналов.</span><span class="sxs-lookup"><span data-stu-id="4522d-141">The name of the circuit service provider.</span></span> <span data-ttu-id="4522d-142">Он должен совпадать с именем, указанным Get-AzExpressRouteServiceProvider командлетом.</span><span class="sxs-lookup"><span data-stu-id="4522d-142">This must match a name listed by the Get-AzExpressRouteServiceProvider cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceProvider
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4522d-143">-SkuFamily</span><span class="sxs-lookup"><span data-stu-id="4522d-143">-SkuFamily</span></span>
<span data-ttu-id="4522d-144">Тип вы счета определяет семейство SKU.</span><span class="sxs-lookup"><span data-stu-id="4522d-144">SKU family determines the billing type.</span></span> <span data-ttu-id="4522d-145">Возможные значения для этого параметра: `MeteredData` или `UnlimitedData` .</span><span class="sxs-lookup"><span data-stu-id="4522d-145">Possible values for this parameter are: `MeteredData` or `UnlimitedData`.</span></span> <span data-ttu-id="4522d-146">Обратите внимание, что вы можете изменить тип вычета с MeteredData на UnlimitedData, но не можете изменить его с UnlimitedData на MeteredData.</span><span class="sxs-lookup"><span data-stu-id="4522d-146">Note that you can change the billing type from MeteredData to UnlimitedData, but you can't change the type from UnlimitedData to MeteredData.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: MeteredData, UnlimitedData

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4522d-147">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="4522d-147">-SkuTier</span></span>
<span data-ttu-id="4522d-148">Уровень обслуживания для схемы.</span><span class="sxs-lookup"><span data-stu-id="4522d-148">The tier of service for the circuit.</span></span> <span data-ttu-id="4522d-149">Возможные значения для этого параметра: `Standard` `Premium` или `Local` .</span><span class="sxs-lookup"><span data-stu-id="4522d-149">Possible values for this parameter are: `Standard`, `Premium` or `Local`.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Standard, Premium, Local

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4522d-150">-Tag</span><span class="sxs-lookup"><span data-stu-id="4522d-150">-Tag</span></span>
<span data-ttu-id="4522d-151">Пары значений ключа в виде hash table.</span><span class="sxs-lookup"><span data-stu-id="4522d-151">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="4522d-152">Например: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="4522d-152">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4522d-153">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4522d-153">-Confirm</span></span>
<span data-ttu-id="4522d-154">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="4522d-154">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4522d-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4522d-155">-WhatIf</span></span>
<span data-ttu-id="4522d-156">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4522d-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4522d-157">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="4522d-157">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4522d-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4522d-158">CommonParameters</span></span>
<span data-ttu-id="4522d-159">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4522d-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4522d-160">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4522d-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4522d-161">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4522d-161">INPUTS</span></span>

### <span data-ttu-id="4522d-162">System.String</span><span class="sxs-lookup"><span data-stu-id="4522d-162">System.String</span></span>

### <span data-ttu-id="4522d-163">System.Int32</span><span class="sxs-lookup"><span data-stu-id="4522d-163">System.Int32</span></span>

### <span data-ttu-id="4522d-164">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="4522d-164">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

### <span data-ttu-id="4522d-165">System.Double</span><span class="sxs-lookup"><span data-stu-id="4522d-165">System.Double</span></span>

### <span data-ttu-id="4522d-166">Microsoft.Azure.Commands.Network.Models.PSPeering[]</span><span class="sxs-lookup"><span data-stu-id="4522d-166">Microsoft.Azure.Commands.Network.Models.PSPeering[]</span></span>

### <span data-ttu-id="4522d-167">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization[]</span><span class="sxs-lookup"><span data-stu-id="4522d-167">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization[]</span></span>

### <span data-ttu-id="4522d-168">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="4522d-168">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="4522d-169">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="4522d-169">System.Collections.Hashtable</span></span>

## <span data-ttu-id="4522d-170">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4522d-170">OUTPUTS</span></span>

### <span data-ttu-id="4522d-171">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4522d-171">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="4522d-172">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4522d-172">NOTES</span></span>

## <span data-ttu-id="4522d-173">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4522d-173">RELATED LINKS</span></span>

[<span data-ttu-id="4522d-174">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4522d-174">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="4522d-175">Move-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4522d-175">Move-AzExpressRouteCircuit</span></span>](Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="4522d-176">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4522d-176">Remove-AzExpressRouteCircuit</span></span>](Remove-AzExpressRouteCircuit.md)

[<span data-ttu-id="4522d-177">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4522d-177">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)

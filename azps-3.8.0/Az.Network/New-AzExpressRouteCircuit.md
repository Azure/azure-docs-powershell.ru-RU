---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: E40CAF2F-ED57-4AC1-8B9A-E48042DD8F91
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuit.md
ms.openlocfilehash: 76888e38487d54c3c7f2796cb49d660872fc5c96
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074750"
---
# <span data-ttu-id="8dc6c-101">New-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="8dc6c-101">New-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="8dc6c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8dc6c-102">SYNOPSIS</span></span>
<span data-ttu-id="8dc6c-103">Создает цепь маршрутов Azure Express.</span><span class="sxs-lookup"><span data-stu-id="8dc6c-103">Creates an Azure express route circuit.</span></span>

## <span data-ttu-id="8dc6c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8dc6c-104">SYNTAX</span></span>

### <span data-ttu-id="8dc6c-105">ServiceProvider (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8dc6c-105">ServiceProvider (Default)</span></span>
```
New-AzExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String> [-SkuTier <String>]
 [-SkuFamily <String>] -ServiceProviderName <String> -PeeringLocation <String> -BandwidthInMbps <Int32>
 [-Peering <PSPeering[]>] [-Authorization <PSExpressRouteCircuitAuthorization[]>]
 [-AllowClassicOperations <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8dc6c-106">ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="8dc6c-106">ExpressRoutePort</span></span>
```
New-AzExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String> [-SkuTier <String>]
 [-SkuFamily <String>] -ExpressRoutePort <PSExpressRoutePort> -BandwidthInGbps <Double>
 [-Peering <PSPeering[]>] [-Authorization <PSExpressRouteCircuitAuthorization[]>]
 [-AllowClassicOperations <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8dc6c-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8dc6c-107">DESCRIPTION</span></span>
<span data-ttu-id="8dc6c-108">Командлет **New-AzExpressRouteCircuit** создает цепь маршрутов Azure Express.</span><span class="sxs-lookup"><span data-stu-id="8dc6c-108">The **New-AzExpressRouteCircuit** cmdlet creates an Azure express route circuit.</span></span>

## <span data-ttu-id="8dc6c-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8dc6c-109">EXAMPLES</span></span>

### <span data-ttu-id="8dc6c-110">Пример 1: создание новой цепи ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="8dc6c-110">Example 1: Create a new ExpressRoute circuit</span></span>
```
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

### <span data-ttu-id="8dc6c-111">Пример 2: создание новой цепи ExpressRoute на ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="8dc6c-111">Example 2: Create a new ExpressRoute circuit on ExpressRoutePort</span></span>
```
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

## <span data-ttu-id="8dc6c-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8dc6c-112">PARAMETERS</span></span>

### <span data-ttu-id="8dc6c-113">-AllowClassicOperations</span><span class="sxs-lookup"><span data-stu-id="8dc6c-113">-AllowClassicOperations</span></span>
<span data-ttu-id="8dc6c-114">Использование этого параметра позволяет использовать классические командлеты PowerShell Azure для управления цепью.</span><span class="sxs-lookup"><span data-stu-id="8dc6c-114">The use of this parameter allows you to use the classic Azure PowerShell cmdlets to manage the circuit.</span></span>

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

### <span data-ttu-id="8dc6c-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8dc6c-115">-AsJob</span></span>
<span data-ttu-id="8dc6c-116">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="8dc6c-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8dc6c-117">-Authorization</span><span class="sxs-lookup"><span data-stu-id="8dc6c-117">-Authorization</span></span>
<span data-ttu-id="8dc6c-118">Список поправок на каналы.</span><span class="sxs-lookup"><span data-stu-id="8dc6c-118">A list of circuit authorizations.</span></span>

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

### <span data-ttu-id="8dc6c-119">-BandwidthInGbps</span><span class="sxs-lookup"><span data-stu-id="8dc6c-119">-BandwidthInGbps</span></span>
<span data-ttu-id="8dc6c-120">Пропускная способность канала при подготовке канала на ресурсе ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="8dc6c-120">The bandwidth of the circuit when the circuit is provisioned on an ExpressRoutePort resource.</span></span>

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

### <span data-ttu-id="8dc6c-121">-BandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="8dc6c-121">-BandwidthInMbps</span></span>
<span data-ttu-id="8dc6c-122">Пропускная способность канала.</span><span class="sxs-lookup"><span data-stu-id="8dc6c-122">The bandwidth of the circuit.</span></span> <span data-ttu-id="8dc6c-123">Оно должно быть значением, которое поддерживается поставщиком услуг.</span><span class="sxs-lookup"><span data-stu-id="8dc6c-123">This must be a value that is supported by the service provider.</span></span>

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

### <span data-ttu-id="8dc6c-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8dc6c-124">-DefaultProfile</span></span>
<span data-ttu-id="8dc6c-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8dc6c-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8dc6c-126">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="8dc6c-126">-ExpressRoutePort</span></span>
<span data-ttu-id="8dc6c-127">Ссылка на ресурс ExpressRoutePort, когда канал подготовлен на ресурсе ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="8dc6c-127">The reference to the ExpressRoutePort resource when the circuit is provisioned on an ExpressRoutePort resource.</span></span>

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

### <span data-ttu-id="8dc6c-128">-Force</span><span class="sxs-lookup"><span data-stu-id="8dc6c-128">-Force</span></span>
<span data-ttu-id="8dc6c-129">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="8dc6c-129">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8dc6c-130">-Location</span><span class="sxs-lookup"><span data-stu-id="8dc6c-130">-Location</span></span>
<span data-ttu-id="8dc6c-131">Расположение цепи.</span><span class="sxs-lookup"><span data-stu-id="8dc6c-131">The location of the circuit.</span></span>

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

### <span data-ttu-id="8dc6c-132">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8dc6c-132">-Name</span></span>
<span data-ttu-id="8dc6c-133">Имя создаваемого канала ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="8dc6c-133">The name of the ExpressRoute circuit being created.</span></span>

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

### <span data-ttu-id="8dc6c-134">-Пиринг</span><span class="sxs-lookup"><span data-stu-id="8dc6c-134">-Peering</span></span>
<span data-ttu-id="8dc6c-135">Конфигурации одноранговых элементов списка.</span><span class="sxs-lookup"><span data-stu-id="8dc6c-135">A list peer configurations.</span></span>

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

### <span data-ttu-id="8dc6c-136">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="8dc6c-136">-PeeringLocation</span></span>
<span data-ttu-id="8dc6c-137">Имя расположения пиринга, поддерживаемое поставщиком услуг.</span><span class="sxs-lookup"><span data-stu-id="8dc6c-137">The name of the peering location supported by the service provider.</span></span>

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

### <span data-ttu-id="8dc6c-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8dc6c-138">-ResourceGroupName</span></span>
<span data-ttu-id="8dc6c-139">Группа ресурсов, в которой будет содержаться цепь.</span><span class="sxs-lookup"><span data-stu-id="8dc6c-139">The resource group that will contain the circuit.</span></span>

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

### <span data-ttu-id="8dc6c-140">-ServiceProviderName</span><span class="sxs-lookup"><span data-stu-id="8dc6c-140">-ServiceProviderName</span></span>
<span data-ttu-id="8dc6c-141">Имя поставщика услуг цепи.</span><span class="sxs-lookup"><span data-stu-id="8dc6c-141">The name of the circuit service provider.</span></span> <span data-ttu-id="8dc6c-142">Оно должно совпадать с именем, указанным в командлете Get-AzExpressRouteServiceProvider.</span><span class="sxs-lookup"><span data-stu-id="8dc6c-142">This must match a name listed by the Get-AzExpressRouteServiceProvider cmdlet.</span></span>

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

### <span data-ttu-id="8dc6c-143">-SkuFamily</span><span class="sxs-lookup"><span data-stu-id="8dc6c-143">-SkuFamily</span></span>
<span data-ttu-id="8dc6c-144">Семейство КОНФИГУРАЦИй определяет тип выставления счетов.</span><span class="sxs-lookup"><span data-stu-id="8dc6c-144">SKU family determines the billing type.</span></span> <span data-ttu-id="8dc6c-145">Возможные значения для этого параметра: `MeteredData` или `UnlimitedData` .</span><span class="sxs-lookup"><span data-stu-id="8dc6c-145">Possible values for this parameter are: `MeteredData` or `UnlimitedData`.</span></span> <span data-ttu-id="8dc6c-146">Обратите внимание, что вы можете изменить тип выставления счетов с MeteredData на UnlimitedData, но вы не можете изменить тип с UnlimitedData на MeteredData.</span><span class="sxs-lookup"><span data-stu-id="8dc6c-146">Note that you can change the billing type from MeteredData to UnlimitedData, but you can't change the type from UnlimitedData to MeteredData.</span></span>

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

### <span data-ttu-id="8dc6c-147">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="8dc6c-147">-SkuTier</span></span>
<span data-ttu-id="8dc6c-148">Уровень обслуживания для канала.</span><span class="sxs-lookup"><span data-stu-id="8dc6c-148">The tier of service for the circuit.</span></span> <span data-ttu-id="8dc6c-149">Возможные значения для этого параметра: `Standard` `Premium` или `Local` .</span><span class="sxs-lookup"><span data-stu-id="8dc6c-149">Possible values for this parameter are: `Standard`, `Premium` or `Local`.</span></span>

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

### <span data-ttu-id="8dc6c-150">-Тег</span><span class="sxs-lookup"><span data-stu-id="8dc6c-150">-Tag</span></span>
<span data-ttu-id="8dc6c-151">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="8dc6c-151">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="8dc6c-152">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="8dc6c-152">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="8dc6c-153">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8dc6c-153">-Confirm</span></span>
<span data-ttu-id="8dc6c-154">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8dc6c-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8dc6c-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8dc6c-155">-WhatIf</span></span>
<span data-ttu-id="8dc6c-156">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8dc6c-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8dc6c-157">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8dc6c-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8dc6c-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8dc6c-158">CommonParameters</span></span>
<span data-ttu-id="8dc6c-159">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8dc6c-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8dc6c-160">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8dc6c-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8dc6c-161">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8dc6c-161">INPUTS</span></span>

### <span data-ttu-id="8dc6c-162">System. String</span><span class="sxs-lookup"><span data-stu-id="8dc6c-162">System.String</span></span>

### <span data-ttu-id="8dc6c-163">System. Int32</span><span class="sxs-lookup"><span data-stu-id="8dc6c-163">System.Int32</span></span>

### <span data-ttu-id="8dc6c-164">Microsoft. Azure. Commands. Network. Models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="8dc6c-164">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

### <span data-ttu-id="8dc6c-165">System. Double</span><span class="sxs-lookup"><span data-stu-id="8dc6c-165">System.Double</span></span>

### <span data-ttu-id="8dc6c-166">Microsoft. Azure. Commands. Network. Models. PSPeering []</span><span class="sxs-lookup"><span data-stu-id="8dc6c-166">Microsoft.Azure.Commands.Network.Models.PSPeering[]</span></span>

### <span data-ttu-id="8dc6c-167">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuitAuthorization []</span><span class="sxs-lookup"><span data-stu-id="8dc6c-167">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization[]</span></span>

### <span data-ttu-id="8dc6c-168">System. Nullable "1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="8dc6c-168">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="8dc6c-169">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="8dc6c-169">System.Collections.Hashtable</span></span>

## <span data-ttu-id="8dc6c-170">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8dc6c-170">OUTPUTS</span></span>

### <span data-ttu-id="8dc6c-171">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="8dc6c-171">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="8dc6c-172">Пуск</span><span class="sxs-lookup"><span data-stu-id="8dc6c-172">NOTES</span></span>

## <span data-ttu-id="8dc6c-173">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8dc6c-173">RELATED LINKS</span></span>

[<span data-ttu-id="8dc6c-174">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="8dc6c-174">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="8dc6c-175">Move-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="8dc6c-175">Move-AzExpressRouteCircuit</span></span>](Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="8dc6c-176">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="8dc6c-176">Remove-AzExpressRouteCircuit</span></span>](Remove-AzExpressRouteCircuit.md)

[<span data-ttu-id="8dc6c-177">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="8dc6c-177">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)

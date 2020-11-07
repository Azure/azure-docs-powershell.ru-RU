---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: E40CAF2F-ED57-4AC1-8B9A-E48042DD8F91
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuit.md
ms.openlocfilehash: e28ebb5209736ad676404e11961d9095cc30da04
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730358"
---
# <span data-ttu-id="45ce6-101">New-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="45ce6-101">New-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="45ce6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="45ce6-102">SYNOPSIS</span></span>
<span data-ttu-id="45ce6-103">Создает цепь маршрутов Azure Express.</span><span class="sxs-lookup"><span data-stu-id="45ce6-103">Creates an Azure express route circuit.</span></span>

## <span data-ttu-id="45ce6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="45ce6-104">SYNTAX</span></span>

### <span data-ttu-id="45ce6-105">ServiceProvider (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="45ce6-105">ServiceProvider (Default)</span></span>
```
New-AzExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String> [-SkuTier <String>]
 [-SkuFamily <String>] -ServiceProviderName <String> -PeeringLocation <String> -BandwidthInMbps <Int32>
 [-Peering <PSPeering[]>] [-Authorization <PSExpressRouteCircuitAuthorization[]>]
 [-AllowClassicOperations <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45ce6-106">ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="45ce6-106">ExpressRoutePort</span></span>
```
New-AzExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String> [-SkuTier <String>]
 [-SkuFamily <String>] -ExpressRoutePort <PSExpressRoutePort> -BandwidthInGbps <Double>
 [-Peering <PSPeering[]>] [-Authorization <PSExpressRouteCircuitAuthorization[]>]
 [-AllowClassicOperations <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45ce6-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="45ce6-107">DESCRIPTION</span></span>
<span data-ttu-id="45ce6-108">Командлет **New-AzExpressRouteCircuit** создает цепь маршрутов Azure Express.</span><span class="sxs-lookup"><span data-stu-id="45ce6-108">The **New-AzExpressRouteCircuit** cmdlet creates an Azure express route circuit.</span></span>

## <span data-ttu-id="45ce6-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="45ce6-109">EXAMPLES</span></span>

### <span data-ttu-id="45ce6-110">Пример 1: создание новой цепи ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="45ce6-110">Example 1: Create a new ExpressRoute circuit</span></span>
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

### <span data-ttu-id="45ce6-111">Пример 2: создание новой цепи ExpressRoute на ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="45ce6-111">Example 2: Create a new ExpressRoute circuit on ExpressRoutePort</span></span>
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

## <span data-ttu-id="45ce6-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="45ce6-112">PARAMETERS</span></span>

### <span data-ttu-id="45ce6-113">-AllowClassicOperations</span><span class="sxs-lookup"><span data-stu-id="45ce6-113">-AllowClassicOperations</span></span>
<span data-ttu-id="45ce6-114">Использование этого параметра позволяет использовать классические командлеты PowerShell Azure для управления цепью.</span><span class="sxs-lookup"><span data-stu-id="45ce6-114">The use of this parameter allows you to use the classic Azure PowerShell cmdlets to manage the circuit.</span></span>

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

### <span data-ttu-id="45ce6-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="45ce6-115">-AsJob</span></span>
<span data-ttu-id="45ce6-116">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="45ce6-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="45ce6-117">-Authorization</span><span class="sxs-lookup"><span data-stu-id="45ce6-117">-Authorization</span></span>
<span data-ttu-id="45ce6-118">Список поправок на каналы.</span><span class="sxs-lookup"><span data-stu-id="45ce6-118">A list of circuit authorizations.</span></span>

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

### <span data-ttu-id="45ce6-119">-BandwidthInGbps</span><span class="sxs-lookup"><span data-stu-id="45ce6-119">-BandwidthInGbps</span></span>
<span data-ttu-id="45ce6-120">Пропускная способность канала при подготовке канала на ресурсе ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="45ce6-120">The bandwidth of the circuit when the circuit is provisioned on an ExpressRoutePort resource.</span></span>

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

### <span data-ttu-id="45ce6-121">-BandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="45ce6-121">-BandwidthInMbps</span></span>
<span data-ttu-id="45ce6-122">Пропускная способность канала.</span><span class="sxs-lookup"><span data-stu-id="45ce6-122">The bandwidth of the circuit.</span></span> <span data-ttu-id="45ce6-123">Оно должно быть значением, которое поддерживается поставщиком услуг.</span><span class="sxs-lookup"><span data-stu-id="45ce6-123">This must be a value that is supported by the service provider.</span></span>

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

### <span data-ttu-id="45ce6-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45ce6-124">-DefaultProfile</span></span>
<span data-ttu-id="45ce6-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="45ce6-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="45ce6-126">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="45ce6-126">-ExpressRoutePort</span></span>
<span data-ttu-id="45ce6-127">Ссылка на ресурс ExpressRoutePort, когда канал подготовлен на ресурсе ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="45ce6-127">The reference to the ExpressRoutePort resource when the circuit is provisioned on an ExpressRoutePort resource.</span></span>

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

### <span data-ttu-id="45ce6-128">-Force</span><span class="sxs-lookup"><span data-stu-id="45ce6-128">-Force</span></span>
<span data-ttu-id="45ce6-129">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="45ce6-129">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="45ce6-130">-Location</span><span class="sxs-lookup"><span data-stu-id="45ce6-130">-Location</span></span>
<span data-ttu-id="45ce6-131">Расположение цепи.</span><span class="sxs-lookup"><span data-stu-id="45ce6-131">The location of the circuit.</span></span>

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

### <span data-ttu-id="45ce6-132">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="45ce6-132">-Name</span></span>
<span data-ttu-id="45ce6-133">Имя создаваемого канала ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="45ce6-133">The name of the ExpressRoute circuit being created.</span></span>

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

### <span data-ttu-id="45ce6-134">-Пиринг</span><span class="sxs-lookup"><span data-stu-id="45ce6-134">-Peering</span></span>
<span data-ttu-id="45ce6-135">Конфигурации одноранговых элементов списка.</span><span class="sxs-lookup"><span data-stu-id="45ce6-135">A list peer configurations.</span></span>

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

### <span data-ttu-id="45ce6-136">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="45ce6-136">-PeeringLocation</span></span>
<span data-ttu-id="45ce6-137">Имя расположения пиринга, поддерживаемое поставщиком услуг.</span><span class="sxs-lookup"><span data-stu-id="45ce6-137">The name of the peering location supported by the service provider.</span></span>

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

### <span data-ttu-id="45ce6-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45ce6-138">-ResourceGroupName</span></span>
<span data-ttu-id="45ce6-139">Группа ресурсов, в которой будет содержаться цепь.</span><span class="sxs-lookup"><span data-stu-id="45ce6-139">The resource group that will contain the circuit.</span></span>

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

### <span data-ttu-id="45ce6-140">-ServiceProviderName</span><span class="sxs-lookup"><span data-stu-id="45ce6-140">-ServiceProviderName</span></span>
<span data-ttu-id="45ce6-141">Имя поставщика услуг цепи.</span><span class="sxs-lookup"><span data-stu-id="45ce6-141">The name of the circuit service provider.</span></span> <span data-ttu-id="45ce6-142">Оно должно совпадать с именем, указанным в командлете Get-AzExpressRouteServiceProvider.</span><span class="sxs-lookup"><span data-stu-id="45ce6-142">This must match a name listed by the Get-AzExpressRouteServiceProvider cmdlet.</span></span>

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

### <span data-ttu-id="45ce6-143">-SkuFamily</span><span class="sxs-lookup"><span data-stu-id="45ce6-143">-SkuFamily</span></span>
<span data-ttu-id="45ce6-144">Семейство КОНФИГУРАЦИй определяет тип выставления счетов.</span><span class="sxs-lookup"><span data-stu-id="45ce6-144">SKU family determines the billing type.</span></span> <span data-ttu-id="45ce6-145">Возможные значения для этого параметра: `MeteredData` или `UnlimitedData` .</span><span class="sxs-lookup"><span data-stu-id="45ce6-145">Possible values for this parameter are: `MeteredData` or `UnlimitedData`.</span></span> <span data-ttu-id="45ce6-146">Обратите внимание, что вы можете изменить тип выставления счетов с MeteredData на UnlimitedData, но вы не можете изменить тип с UnlimitedData на MeteredData.</span><span class="sxs-lookup"><span data-stu-id="45ce6-146">Note that you can change the billing type from MeteredData to UnlimitedData, but you can't change the type from UnlimitedData to MeteredData.</span></span>

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

### <span data-ttu-id="45ce6-147">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="45ce6-147">-SkuTier</span></span>
<span data-ttu-id="45ce6-148">Уровень обслуживания для канала.</span><span class="sxs-lookup"><span data-stu-id="45ce6-148">The tier of service for the circuit.</span></span> <span data-ttu-id="45ce6-149">Возможные значения для этого параметра: `Standard` `Premium` или `Basic` .</span><span class="sxs-lookup"><span data-stu-id="45ce6-149">Possible values for this parameter are: `Standard`, `Premium` or `Basic`.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Standard, Premium, Basic

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45ce6-150">-Тег</span><span class="sxs-lookup"><span data-stu-id="45ce6-150">-Tag</span></span>
<span data-ttu-id="45ce6-151">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="45ce6-151">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="45ce6-152">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="45ce6-152">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="45ce6-153">-Confirm</span><span class="sxs-lookup"><span data-stu-id="45ce6-153">-Confirm</span></span>
<span data-ttu-id="45ce6-154">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="45ce6-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45ce6-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45ce6-155">-WhatIf</span></span>
<span data-ttu-id="45ce6-156">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="45ce6-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45ce6-157">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="45ce6-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45ce6-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45ce6-158">CommonParameters</span></span>
<span data-ttu-id="45ce6-159">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="45ce6-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45ce6-160">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45ce6-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45ce6-161">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="45ce6-161">INPUTS</span></span>

### <span data-ttu-id="45ce6-162">System. String</span><span class="sxs-lookup"><span data-stu-id="45ce6-162">System.String</span></span>

### <span data-ttu-id="45ce6-163">System. Int32</span><span class="sxs-lookup"><span data-stu-id="45ce6-163">System.Int32</span></span>

### <span data-ttu-id="45ce6-164">Microsoft. Azure. Commands. Network. Models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="45ce6-164">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

### <span data-ttu-id="45ce6-165">System. Double</span><span class="sxs-lookup"><span data-stu-id="45ce6-165">System.Double</span></span>

### <span data-ttu-id="45ce6-166">Microsoft. Azure. Commands. Network. Models. PSPeering []</span><span class="sxs-lookup"><span data-stu-id="45ce6-166">Microsoft.Azure.Commands.Network.Models.PSPeering[]</span></span>

### <span data-ttu-id="45ce6-167">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuitAuthorization []</span><span class="sxs-lookup"><span data-stu-id="45ce6-167">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization[]</span></span>

### <span data-ttu-id="45ce6-168">System. Nullable "1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="45ce6-168">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="45ce6-169">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="45ce6-169">System.Collections.Hashtable</span></span>

## <span data-ttu-id="45ce6-170">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="45ce6-170">OUTPUTS</span></span>

### <span data-ttu-id="45ce6-171">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="45ce6-171">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="45ce6-172">Пуск</span><span class="sxs-lookup"><span data-stu-id="45ce6-172">NOTES</span></span>

## <span data-ttu-id="45ce6-173">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="45ce6-173">RELATED LINKS</span></span>

[<span data-ttu-id="45ce6-174">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="45ce6-174">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="45ce6-175">Move-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="45ce6-175">Move-AzExpressRouteCircuit</span></span>](Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="45ce6-176">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="45ce6-176">Remove-AzExpressRouteCircuit</span></span>](Remove-AzExpressRouteCircuit.md)

[<span data-ttu-id="45ce6-177">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="45ce6-177">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)

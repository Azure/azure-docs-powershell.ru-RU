---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: E40CAF2F-ED57-4AC1-8B9A-E48042DD8F91
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermexpressroutecircuit
schema: 2.0.0
ms.openlocfilehash: 43084ab54ed20a094cc292eca2bf133598171f09
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913433"
---
# <span data-ttu-id="82ea7-101">New-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="82ea7-101">New-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="82ea7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="82ea7-102">SYNOPSIS</span></span>
<span data-ttu-id="82ea7-103">Создает цепь маршрутов Azure Express.</span><span class="sxs-lookup"><span data-stu-id="82ea7-103">Creates an Azure express route circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="82ea7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="82ea7-104">SYNTAX</span></span>

```
New-AzureRmExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String>
 [-SkuTier <String>] [-SkuFamily <String>] -ServiceProviderName <String> -PeeringLocation <String>
 -BandwidthInMbps <Int32>
 [-Peering <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPeering]>]
 [-Authorization <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization]>]
 [-AllowClassicOperations <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="82ea7-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="82ea7-105">DESCRIPTION</span></span>
<span data-ttu-id="82ea7-106">Командлет **New-AzureRmExpressRouteCircuit** создает цепь маршрутов Azure Express.</span><span class="sxs-lookup"><span data-stu-id="82ea7-106">The **New-AzureRmExpressRouteCircuit** cmdlet creates an Azure express route circuit.</span></span>

## <span data-ttu-id="82ea7-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="82ea7-107">EXAMPLES</span></span>

### <span data-ttu-id="82ea7-108">Пример 1: создание новой цепи ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="82ea7-108">Example 1: Create a new ExpressRoute circuit</span></span>
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
New-AzureRmExpressRouteCircuit @parameters
```

## <span data-ttu-id="82ea7-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="82ea7-109">PARAMETERS</span></span>

### <span data-ttu-id="82ea7-110">-AllowClassicOperations</span><span class="sxs-lookup"><span data-stu-id="82ea7-110">-AllowClassicOperations</span></span>
<span data-ttu-id="82ea7-111">Использование этого параметра позволяет использовать классические командлеты PowerShell Azure для управления цепью.</span><span class="sxs-lookup"><span data-stu-id="82ea7-111">The use of this parameter allows you to use the classic Azure PowerShell cmdlets to manage the circuit.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82ea7-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="82ea7-112">-AsJob</span></span>
<span data-ttu-id="82ea7-113">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="82ea7-113">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82ea7-114">-Authorization</span><span class="sxs-lookup"><span data-stu-id="82ea7-114">-Authorization</span></span>
<span data-ttu-id="82ea7-115">Список поправок на каналы.</span><span class="sxs-lookup"><span data-stu-id="82ea7-115">A list of circuit authorizations.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82ea7-116">-BandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="82ea7-116">-BandwidthInMbps</span></span>
<span data-ttu-id="82ea7-117">Пропускная способность канала.</span><span class="sxs-lookup"><span data-stu-id="82ea7-117">The bandwidth of the circuit.</span></span> <span data-ttu-id="82ea7-118">Оно должно быть значением, которое поддерживается поставщиком услуг.</span><span class="sxs-lookup"><span data-stu-id="82ea7-118">This must be a value that is supported by the service provider.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82ea7-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82ea7-119">-DefaultProfile</span></span>
<span data-ttu-id="82ea7-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="82ea7-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82ea7-121">-Force</span><span class="sxs-lookup"><span data-stu-id="82ea7-121">-Force</span></span>
<span data-ttu-id="82ea7-122">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="82ea7-122">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82ea7-123">-Location</span><span class="sxs-lookup"><span data-stu-id="82ea7-123">-Location</span></span>
<span data-ttu-id="82ea7-124">Расположение цепи.</span><span class="sxs-lookup"><span data-stu-id="82ea7-124">The location of the circuit.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82ea7-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="82ea7-125">-Name</span></span>
<span data-ttu-id="82ea7-126">Имя создаваемого канала ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="82ea7-126">The name of the ExpressRoute circuit being created.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82ea7-127">-Пиринг</span><span class="sxs-lookup"><span data-stu-id="82ea7-127">-Peering</span></span>
<span data-ttu-id="82ea7-128">Конфигурации одноранговых элементов списка.</span><span class="sxs-lookup"><span data-stu-id="82ea7-128">A list peer configurations.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPeering]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82ea7-129">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="82ea7-129">-PeeringLocation</span></span>
<span data-ttu-id="82ea7-130">Имя расположения пиринга, поддерживаемое поставщиком услуг.</span><span class="sxs-lookup"><span data-stu-id="82ea7-130">The name of the peering location supported by the service provider.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82ea7-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82ea7-131">-ResourceGroupName</span></span>
<span data-ttu-id="82ea7-132">Группа ресурсов, в которой будет содержаться цепь.</span><span class="sxs-lookup"><span data-stu-id="82ea7-132">The resource group that will contain the circuit.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82ea7-133">-ServiceProviderName</span><span class="sxs-lookup"><span data-stu-id="82ea7-133">-ServiceProviderName</span></span>
<span data-ttu-id="82ea7-134">Имя поставщика услуг цепи.</span><span class="sxs-lookup"><span data-stu-id="82ea7-134">The name of the circuit service provider.</span></span> <span data-ttu-id="82ea7-135">Оно должно совпадать с именем, указанным в командлете Get-AzureRmExpressRouteServiceProvider.</span><span class="sxs-lookup"><span data-stu-id="82ea7-135">This must match a name listed by the Get-AzureRmExpressRouteServiceProvider cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82ea7-136">-SkuFamily</span><span class="sxs-lookup"><span data-stu-id="82ea7-136">-SkuFamily</span></span>
<span data-ttu-id="82ea7-137">Семейство КОНФИГУРАЦИй определяет тип выставления счетов.</span><span class="sxs-lookup"><span data-stu-id="82ea7-137">SKU family determines the billing type.</span></span> <span data-ttu-id="82ea7-138">Возможные значения для этого параметра: `MeteredData` или `UnlimitedData` .</span><span class="sxs-lookup"><span data-stu-id="82ea7-138">Possible values for this parameter are: `MeteredData` or `UnlimitedData`.</span></span> <span data-ttu-id="82ea7-139">Обратите внимание, что вы можете изменить тип выставления счетов с MeteredData на UnlimitedData, но вы не можете изменить тип с UnlimitedData на MeteredData.</span><span class="sxs-lookup"><span data-stu-id="82ea7-139">Note that you can change the billing type from MeteredData to UnlimitedData, but you can't change the type from UnlimitedData to MeteredData.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: MeteredData, UnlimitedData

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82ea7-140">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="82ea7-140">-SkuTier</span></span>
<span data-ttu-id="82ea7-141">Уровень обслуживания для канала.</span><span class="sxs-lookup"><span data-stu-id="82ea7-141">The tier of service for the circuit.</span></span> <span data-ttu-id="82ea7-142">Возможные значения для этого параметра: `Standard` или `Premium` .</span><span class="sxs-lookup"><span data-stu-id="82ea7-142">Possible values for this parameter are: `Standard` or `Premium`.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82ea7-143">-Тег</span><span class="sxs-lookup"><span data-stu-id="82ea7-143">-Tag</span></span>
<span data-ttu-id="82ea7-144">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="82ea7-144">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="82ea7-145">Например:</span><span class="sxs-lookup"><span data-stu-id="82ea7-145">For example:</span></span>

<span data-ttu-id="82ea7-146">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="82ea7-146">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82ea7-147">-Confirm</span><span class="sxs-lookup"><span data-stu-id="82ea7-147">-Confirm</span></span>
<span data-ttu-id="82ea7-148">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="82ea7-148">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82ea7-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82ea7-149">-WhatIf</span></span>
<span data-ttu-id="82ea7-150">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="82ea7-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82ea7-151">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="82ea7-151">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82ea7-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82ea7-152">CommonParameters</span></span>
<span data-ttu-id="82ea7-153">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="82ea7-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82ea7-154">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82ea7-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82ea7-155">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="82ea7-155">INPUTS</span></span>

## <span data-ttu-id="82ea7-156">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="82ea7-156">OUTPUTS</span></span>

### <span data-ttu-id="82ea7-157">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="82ea7-157">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="82ea7-158">Пуск</span><span class="sxs-lookup"><span data-stu-id="82ea7-158">NOTES</span></span>

## <span data-ttu-id="82ea7-159">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="82ea7-159">RELATED LINKS</span></span>

[<span data-ttu-id="82ea7-160">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="82ea7-160">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="82ea7-161">Move-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="82ea7-161">Move-AzureRmExpressRouteCircuit</span></span>](Move-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="82ea7-162">Remove-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="82ea7-162">Remove-AzureRmExpressRouteCircuit</span></span>](Remove-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="82ea7-163">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="82ea7-163">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)

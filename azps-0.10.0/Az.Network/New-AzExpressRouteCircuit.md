---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: E40CAF2F-ED57-4AC1-8B9A-E48042DD8F91
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzExpressRouteCircuit.md
ms.openlocfilehash: d03b52c477686f3aa724057771285eaf9d522a56
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93909710"
---
# <span data-ttu-id="bc8e5-101">New-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="bc8e5-101">New-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="bc8e5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bc8e5-102">SYNOPSIS</span></span>
<span data-ttu-id="bc8e5-103">Создает цепь маршрутов Azure Express.</span><span class="sxs-lookup"><span data-stu-id="bc8e5-103">Creates an Azure express route circuit.</span></span>

## <span data-ttu-id="bc8e5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bc8e5-104">SYNTAX</span></span>

```
New-AzExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String>
 [-SkuTier <String>] [-SkuFamily <String>] -ServiceProviderName <String> -PeeringLocation <String>
 -BandwidthInMbps <Int32>
 [-Peering <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPeering]>]
 [-Authorization <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization]>]
 [-AllowClassicOperations <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc8e5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bc8e5-105">DESCRIPTION</span></span>
<span data-ttu-id="bc8e5-106">Командлет **New-AzExpressRouteCircuit** создает цепь маршрутов Azure Express.</span><span class="sxs-lookup"><span data-stu-id="bc8e5-106">The **New-AzExpressRouteCircuit** cmdlet creates an Azure express route circuit.</span></span>

## <span data-ttu-id="bc8e5-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bc8e5-107">EXAMPLES</span></span>

### <span data-ttu-id="bc8e5-108">Пример 1: создание новой цепи ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="bc8e5-108">Example 1: Create a new ExpressRoute circuit</span></span>
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

## <span data-ttu-id="bc8e5-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bc8e5-109">PARAMETERS</span></span>

### <span data-ttu-id="bc8e5-110">-AllowClassicOperations</span><span class="sxs-lookup"><span data-stu-id="bc8e5-110">-AllowClassicOperations</span></span>
<span data-ttu-id="bc8e5-111">Использование этого параметра позволяет использовать классические командлеты PowerShell Azure для управления цепью.</span><span class="sxs-lookup"><span data-stu-id="bc8e5-111">The use of this parameter allows you to use the classic Azure PowerShell cmdlets to manage the circuit.</span></span>

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

### <span data-ttu-id="bc8e5-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bc8e5-112">-AsJob</span></span>
<span data-ttu-id="bc8e5-113">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="bc8e5-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bc8e5-114">-Authorization</span><span class="sxs-lookup"><span data-stu-id="bc8e5-114">-Authorization</span></span>
<span data-ttu-id="bc8e5-115">Список поправок на каналы.</span><span class="sxs-lookup"><span data-stu-id="bc8e5-115">A list of circuit authorizations.</span></span>

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

### <span data-ttu-id="bc8e5-116">-BandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="bc8e5-116">-BandwidthInMbps</span></span>
<span data-ttu-id="bc8e5-117">Пропускная способность канала.</span><span class="sxs-lookup"><span data-stu-id="bc8e5-117">The bandwidth of the circuit.</span></span> <span data-ttu-id="bc8e5-118">Оно должно быть значением, которое поддерживается поставщиком услуг.</span><span class="sxs-lookup"><span data-stu-id="bc8e5-118">This must be a value that is supported by the service provider.</span></span>

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

### <span data-ttu-id="bc8e5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc8e5-119">-DefaultProfile</span></span>
<span data-ttu-id="bc8e5-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bc8e5-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bc8e5-121">-Force</span><span class="sxs-lookup"><span data-stu-id="bc8e5-121">-Force</span></span>
<span data-ttu-id="bc8e5-122">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="bc8e5-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="bc8e5-123">-Location</span><span class="sxs-lookup"><span data-stu-id="bc8e5-123">-Location</span></span>
<span data-ttu-id="bc8e5-124">Расположение цепи.</span><span class="sxs-lookup"><span data-stu-id="bc8e5-124">The location of the circuit.</span></span>

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

### <span data-ttu-id="bc8e5-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="bc8e5-125">-Name</span></span>
<span data-ttu-id="bc8e5-126">Имя создаваемого канала ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="bc8e5-126">The name of the ExpressRoute circuit being created.</span></span>

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

### <span data-ttu-id="bc8e5-127">-Пиринг</span><span class="sxs-lookup"><span data-stu-id="bc8e5-127">-Peering</span></span>
<span data-ttu-id="bc8e5-128">Конфигурации одноранговых элементов списка.</span><span class="sxs-lookup"><span data-stu-id="bc8e5-128">A list peer configurations.</span></span>

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

### <span data-ttu-id="bc8e5-129">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="bc8e5-129">-PeeringLocation</span></span>
<span data-ttu-id="bc8e5-130">Имя расположения пиринга, поддерживаемое поставщиком услуг.</span><span class="sxs-lookup"><span data-stu-id="bc8e5-130">The name of the peering location supported by the service provider.</span></span>

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

### <span data-ttu-id="bc8e5-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc8e5-131">-ResourceGroupName</span></span>
<span data-ttu-id="bc8e5-132">Группа ресурсов, в которой будет содержаться цепь.</span><span class="sxs-lookup"><span data-stu-id="bc8e5-132">The resource group that will contain the circuit.</span></span>

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

### <span data-ttu-id="bc8e5-133">-ServiceProviderName</span><span class="sxs-lookup"><span data-stu-id="bc8e5-133">-ServiceProviderName</span></span>
<span data-ttu-id="bc8e5-134">Имя поставщика услуг цепи.</span><span class="sxs-lookup"><span data-stu-id="bc8e5-134">The name of the circuit service provider.</span></span> <span data-ttu-id="bc8e5-135">Оно должно совпадать с именем, указанным в командлете Get-AzExpressRouteServiceProvider.</span><span class="sxs-lookup"><span data-stu-id="bc8e5-135">This must match a name listed by the Get-AzExpressRouteServiceProvider cmdlet.</span></span>

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

### <span data-ttu-id="bc8e5-136">-SkuFamily</span><span class="sxs-lookup"><span data-stu-id="bc8e5-136">-SkuFamily</span></span>
<span data-ttu-id="bc8e5-137">Семейство КОНФИГУРАЦИй определяет тип выставления счетов.</span><span class="sxs-lookup"><span data-stu-id="bc8e5-137">SKU family determines the billing type.</span></span> <span data-ttu-id="bc8e5-138">Возможные значения для этого параметра: `MeteredData` или `UnlimitedData` .</span><span class="sxs-lookup"><span data-stu-id="bc8e5-138">Possible values for this parameter are: `MeteredData` or `UnlimitedData`.</span></span> <span data-ttu-id="bc8e5-139">Обратите внимание, что вы можете изменить тип выставления счетов с MeteredData на UnlimitedData, но вы не можете изменить тип с UnlimitedData на MeteredData.</span><span class="sxs-lookup"><span data-stu-id="bc8e5-139">Note that you can change the billing type from MeteredData to UnlimitedData, but you can't change the type from UnlimitedData to MeteredData.</span></span>

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

### <span data-ttu-id="bc8e5-140">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="bc8e5-140">-SkuTier</span></span>
<span data-ttu-id="bc8e5-141">Уровень обслуживания для канала.</span><span class="sxs-lookup"><span data-stu-id="bc8e5-141">The tier of service for the circuit.</span></span> <span data-ttu-id="bc8e5-142">Возможные значения для этого параметра: `Standard` или `Premium` .</span><span class="sxs-lookup"><span data-stu-id="bc8e5-142">Possible values for this parameter are: `Standard` or `Premium`.</span></span>

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

### <span data-ttu-id="bc8e5-143">-Тег</span><span class="sxs-lookup"><span data-stu-id="bc8e5-143">-Tag</span></span>
<span data-ttu-id="bc8e5-144">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="bc8e5-144">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="bc8e5-145">Например:</span><span class="sxs-lookup"><span data-stu-id="bc8e5-145">For example:</span></span>

<span data-ttu-id="bc8e5-146">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="bc8e5-146">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="bc8e5-147">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bc8e5-147">-Confirm</span></span>
<span data-ttu-id="bc8e5-148">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="bc8e5-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc8e5-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc8e5-149">-WhatIf</span></span>
<span data-ttu-id="bc8e5-150">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="bc8e5-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc8e5-151">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="bc8e5-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc8e5-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc8e5-152">CommonParameters</span></span>
<span data-ttu-id="bc8e5-153">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bc8e5-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc8e5-154">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc8e5-154">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc8e5-155">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bc8e5-155">INPUTS</span></span>

## <span data-ttu-id="bc8e5-156">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bc8e5-156">OUTPUTS</span></span>

### <span data-ttu-id="bc8e5-157">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="bc8e5-157">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="bc8e5-158">Пуск</span><span class="sxs-lookup"><span data-stu-id="bc8e5-158">NOTES</span></span>

## <span data-ttu-id="bc8e5-159">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bc8e5-159">RELATED LINKS</span></span>

[<span data-ttu-id="bc8e5-160">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="bc8e5-160">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="bc8e5-161">Move-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="bc8e5-161">Move-AzExpressRouteCircuit</span></span>](Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="bc8e5-162">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="bc8e5-162">Remove-AzExpressRouteCircuit</span></span>](Remove-AzExpressRouteCircuit.md)

[<span data-ttu-id="bc8e5-163">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="bc8e5-163">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)

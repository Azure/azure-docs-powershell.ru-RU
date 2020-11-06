---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: E40CAF2F-ED57-4AC1-8B9A-E48042DD8F91
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmExpressRouteCircuit.md
ms.openlocfilehash: 4a5c59f6cc561bdd5f12462aab1e4cd634e70fc4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563879"
---
# <span data-ttu-id="b4be2-101">New-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b4be2-101">New-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="b4be2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b4be2-102">SYNOPSIS</span></span>
<span data-ttu-id="b4be2-103">Создает цепь маршрутов Azure Express.</span><span class="sxs-lookup"><span data-stu-id="b4be2-103">Creates an Azure express route circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b4be2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b4be2-104">SYNTAX</span></span>

```
New-AzureRmExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String>
 [-SkuTier <String>] [-SkuFamily <String>] -ServiceProviderName <String> -PeeringLocation <String>
 -BandwidthInMbps <Int32>
 [-Peering <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPeering]>]
 [-Authorization <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization]>]
 [-AllowClassicOperations <Boolean>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4be2-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b4be2-105">DESCRIPTION</span></span>
<span data-ttu-id="b4be2-106">Командлет **New-AzureRmExpressRouteCircuit** создает цепь маршрутов Azure Express.</span><span class="sxs-lookup"><span data-stu-id="b4be2-106">The **New-AzureRmExpressRouteCircuit** cmdlet creates an Azure express route circuit.</span></span>

## <span data-ttu-id="b4be2-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b4be2-107">EXAMPLES</span></span>

### <span data-ttu-id="b4be2-108">Пример 1: создание новой цепи ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="b4be2-108">Example 1: Create a new ExpressRoute circuit</span></span>
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

## <span data-ttu-id="b4be2-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b4be2-109">PARAMETERS</span></span>

### <span data-ttu-id="b4be2-110">-AllowClassicOperations</span><span class="sxs-lookup"><span data-stu-id="b4be2-110">-AllowClassicOperations</span></span>
<span data-ttu-id="b4be2-111">Использование этого параметра позволяет использовать классические командлеты PowerShell Azure для управления цепью.</span><span class="sxs-lookup"><span data-stu-id="b4be2-111">The use of this parameter allows you to use the classic Azure PowerShell cmdlets to manage the circuit.</span></span>

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

### <span data-ttu-id="b4be2-112">-Authorization</span><span class="sxs-lookup"><span data-stu-id="b4be2-112">-Authorization</span></span>
<span data-ttu-id="b4be2-113">Список поправок на каналы.</span><span class="sxs-lookup"><span data-stu-id="b4be2-113">A list of circuit authorizations.</span></span>

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

### <span data-ttu-id="b4be2-114">-BandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="b4be2-114">-BandwidthInMbps</span></span>
<span data-ttu-id="b4be2-115">Пропускная способность канала.</span><span class="sxs-lookup"><span data-stu-id="b4be2-115">The bandwidth of the circuit.</span></span> <span data-ttu-id="b4be2-116">Оно должно быть значением, которое поддерживается поставщиком услуг.</span><span class="sxs-lookup"><span data-stu-id="b4be2-116">This must be a value that is supported by the service provider.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4be2-117">-Force</span><span class="sxs-lookup"><span data-stu-id="b4be2-117">-Force</span></span>
<span data-ttu-id="b4be2-118">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="b4be2-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b4be2-119">-Location</span><span class="sxs-lookup"><span data-stu-id="b4be2-119">-Location</span></span>
<span data-ttu-id="b4be2-120">Расположение цепи.</span><span class="sxs-lookup"><span data-stu-id="b4be2-120">The location of the circuit.</span></span>

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

### <span data-ttu-id="b4be2-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b4be2-121">-Name</span></span>
<span data-ttu-id="b4be2-122">Имя создаваемого канала ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="b4be2-122">The name of the ExpressRoute circuit being created.</span></span>

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

### <span data-ttu-id="b4be2-123">-Пиринг</span><span class="sxs-lookup"><span data-stu-id="b4be2-123">-Peering</span></span>
<span data-ttu-id="b4be2-124">Конфигурации одноранговых элементов списка.</span><span class="sxs-lookup"><span data-stu-id="b4be2-124">A list peer configurations.</span></span>

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

### <span data-ttu-id="b4be2-125">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="b4be2-125">-PeeringLocation</span></span>
<span data-ttu-id="b4be2-126">Имя расположения пиринга, поддерживаемое поставщиком услуг.</span><span class="sxs-lookup"><span data-stu-id="b4be2-126">The name of the peering location supported by the service provider.</span></span>

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

### <span data-ttu-id="b4be2-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4be2-127">-ResourceGroupName</span></span>
<span data-ttu-id="b4be2-128">Группа ресурсов, в которой будет содержаться цепь.</span><span class="sxs-lookup"><span data-stu-id="b4be2-128">The resource group that will contain the circuit.</span></span>

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

### <span data-ttu-id="b4be2-129">-ServiceProviderName</span><span class="sxs-lookup"><span data-stu-id="b4be2-129">-ServiceProviderName</span></span>
<span data-ttu-id="b4be2-130">Имя поставщика услуг цепи.</span><span class="sxs-lookup"><span data-stu-id="b4be2-130">The name of the circuit service provider.</span></span> <span data-ttu-id="b4be2-131">Оно должно совпадать с именем, указанным в командлете Get-AzureRmExpressRouteServiceProvider.</span><span class="sxs-lookup"><span data-stu-id="b4be2-131">This must match a name listed by the Get-AzureRmExpressRouteServiceProvider cmdlet.</span></span>

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

### <span data-ttu-id="b4be2-132">-SkuFamily</span><span class="sxs-lookup"><span data-stu-id="b4be2-132">-SkuFamily</span></span>
<span data-ttu-id="b4be2-133">Семейство КОНФИГУРАЦИй определяет тип выставления счетов.</span><span class="sxs-lookup"><span data-stu-id="b4be2-133">SKU family determines the billing type.</span></span> <span data-ttu-id="b4be2-134">Возможные значения для этого параметра: `MeteredData` или `UnlimitedData` .</span><span class="sxs-lookup"><span data-stu-id="b4be2-134">Possible values for this parameter are: `MeteredData` or `UnlimitedData`.</span></span> <span data-ttu-id="b4be2-135">Обратите внимание, что вы можете изменить тип выставления счетов с MeteredData на UnlimitedData, но вы не можете изменить тип с UnlimitedData на MeteredData.</span><span class="sxs-lookup"><span data-stu-id="b4be2-135">Note that you can change the billing type from MeteredData to UnlimitedData, but you can't change the type from UnlimitedData to MeteredData.</span></span>

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

### <span data-ttu-id="b4be2-136">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="b4be2-136">-SkuTier</span></span>
<span data-ttu-id="b4be2-137">Уровень обслуживания для канала.</span><span class="sxs-lookup"><span data-stu-id="b4be2-137">The tier of service for the circuit.</span></span> <span data-ttu-id="b4be2-138">Возможные значения для этого параметра: `Standard` или `Premium` .</span><span class="sxs-lookup"><span data-stu-id="b4be2-138">Possible values for this parameter are: `Standard` or `Premium`.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4be2-139">-Тег</span><span class="sxs-lookup"><span data-stu-id="b4be2-139">-Tag</span></span>
<span data-ttu-id="b4be2-140">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="b4be2-140">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="b4be2-141">Например:</span><span class="sxs-lookup"><span data-stu-id="b4be2-141">For example:</span></span>

<span data-ttu-id="b4be2-142">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="b4be2-142">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="b4be2-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b4be2-143">-Confirm</span></span>
<span data-ttu-id="b4be2-144">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b4be2-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4be2-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4be2-145">-WhatIf</span></span>
<span data-ttu-id="b4be2-146">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b4be2-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4be2-147">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b4be2-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4be2-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4be2-148">-DefaultProfile</span></span>
<span data-ttu-id="b4be2-149">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b4be2-149">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4be2-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4be2-150">CommonParameters</span></span>
<span data-ttu-id="b4be2-151">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b4be2-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4be2-152">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4be2-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4be2-153">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b4be2-153">INPUTS</span></span>

## <span data-ttu-id="b4be2-154">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b4be2-154">OUTPUTS</span></span>

### <span data-ttu-id="b4be2-155">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b4be2-155">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="b4be2-156">Пуск</span><span class="sxs-lookup"><span data-stu-id="b4be2-156">NOTES</span></span>

## <span data-ttu-id="b4be2-157">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b4be2-157">RELATED LINKS</span></span>

[<span data-ttu-id="b4be2-158">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b4be2-158">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="b4be2-159">Move-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b4be2-159">Move-AzureRmExpressRouteCircuit</span></span>](Move-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="b4be2-160">Remove-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b4be2-160">Remove-AzureRmExpressRouteCircuit</span></span>](Remove-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="b4be2-161">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b4be2-161">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)

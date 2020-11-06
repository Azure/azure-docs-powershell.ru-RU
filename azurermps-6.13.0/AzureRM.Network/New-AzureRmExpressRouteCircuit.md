---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: E40CAF2F-ED57-4AC1-8B9A-E48042DD8F91
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmExpressRouteCircuit.md
ms.openlocfilehash: cee0318367ad764a9cc9e37995f092462cd157a5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564268"
---
# <span data-ttu-id="0b7f6-101">New-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="0b7f6-101">New-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="0b7f6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0b7f6-102">SYNOPSIS</span></span>
<span data-ttu-id="0b7f6-103">Создает цепь маршрутов Azure Express.</span><span class="sxs-lookup"><span data-stu-id="0b7f6-103">Creates an Azure express route circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0b7f6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0b7f6-104">SYNTAX</span></span>

### <span data-ttu-id="0b7f6-105">Поставщик</span><span class="sxs-lookup"><span data-stu-id="0b7f6-105">ServiceProvider</span></span>
```
New-AzureRmExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String>
 [-SkuTier <String>] [-SkuFamily <String>] [-ServiceProviderName <String>] [-PeeringLocation <String>]
 [-BandwidthInMbps <Int32>]
 [-Peering <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPeering]>]
 [-Authorization <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization]>]
 [-AllowClassicOperations <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b7f6-106">ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="0b7f6-106">ExpressRoutePort</span></span>
```
New-AzureRmExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String>
 [-SkuTier <String>] [-SkuFamily <String>] [-ExpressRoutePort <PSExpressRoutePort>] [-BandwidthInGbps <Double>]
 [-Peering <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPeering]>]
 [-Authorization <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization]>]
 [-AllowClassicOperations <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b7f6-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0b7f6-107">DESCRIPTION</span></span>
<span data-ttu-id="0b7f6-108">Командлет **New-AzureRmExpressRouteCircuit** создает цепь маршрутов Azure Express.</span><span class="sxs-lookup"><span data-stu-id="0b7f6-108">The **New-AzureRmExpressRouteCircuit** cmdlet creates an Azure express route circuit.</span></span>

## <span data-ttu-id="0b7f6-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0b7f6-109">EXAMPLES</span></span>

### <span data-ttu-id="0b7f6-110">Пример 1: создание новой цепи ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="0b7f6-110">Example 1: Create a new ExpressRoute circuit</span></span>
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

### <span data-ttu-id="0b7f6-111">Пример 2: создание новой цепи ExpressRoute на ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="0b7f6-111">Example 2: Create a new ExpressRoute circuit on ExpressRoutePort</span></span>
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
New-AzureRmExpressRouteCircuit @parameters
```

## <span data-ttu-id="0b7f6-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0b7f6-112">PARAMETERS</span></span>

### <span data-ttu-id="0b7f6-113">-AllowClassicOperations</span><span class="sxs-lookup"><span data-stu-id="0b7f6-113">-AllowClassicOperations</span></span>
<span data-ttu-id="0b7f6-114">Использование этого параметра позволяет использовать классические командлеты PowerShell Azure для управления цепью.</span><span class="sxs-lookup"><span data-stu-id="0b7f6-114">The use of this parameter allows you to use the classic Azure PowerShell cmdlets to manage the circuit.</span></span>

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

### <span data-ttu-id="0b7f6-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0b7f6-115">-AsJob</span></span>
<span data-ttu-id="0b7f6-116">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="0b7f6-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0b7f6-117">-Authorization</span><span class="sxs-lookup"><span data-stu-id="0b7f6-117">-Authorization</span></span>
<span data-ttu-id="0b7f6-118">Список поправок на каналы.</span><span class="sxs-lookup"><span data-stu-id="0b7f6-118">A list of circuit authorizations.</span></span>

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

### <span data-ttu-id="0b7f6-119">-BandwidthInGbps</span><span class="sxs-lookup"><span data-stu-id="0b7f6-119">-BandwidthInGbps</span></span>
<span data-ttu-id="0b7f6-120">Пропускная способность канала при подготовке канала на ресурсе ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="0b7f6-120">The bandwidth of the circuit when the circuit is provisioned on an ExpressRoutePort resource.</span></span>

```yaml
Type: Double
Parameter Sets: ExpressRoutePort
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b7f6-121">-BandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="0b7f6-121">-BandwidthInMbps</span></span>
<span data-ttu-id="0b7f6-122">Пропускная способность канала.</span><span class="sxs-lookup"><span data-stu-id="0b7f6-122">The bandwidth of the circuit.</span></span> <span data-ttu-id="0b7f6-123">Оно должно быть значением, которое поддерживается поставщиком услуг.</span><span class="sxs-lookup"><span data-stu-id="0b7f6-123">This must be a value that is supported by the service provider.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ServiceProvider
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b7f6-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b7f6-124">-DefaultProfile</span></span>
<span data-ttu-id="0b7f6-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0b7f6-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0b7f6-126">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="0b7f6-126">-ExpressRoutePort</span></span>
<span data-ttu-id="0b7f6-127">Ссылка на ресурс ExpressRoutePort, когда канал подготовлен на ресурсе ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="0b7f6-127">The reference to the ExpressRoutePort resource when the circuit is provisioned on an ExpressRoutePort resource.</span></span>

```yaml
Type: PSExpressRoutePort
Parameter Sets: ExpressRoutePort
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0b7f6-128">-Force</span><span class="sxs-lookup"><span data-stu-id="0b7f6-128">-Force</span></span>
<span data-ttu-id="0b7f6-129">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="0b7f6-129">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0b7f6-130">-Location</span><span class="sxs-lookup"><span data-stu-id="0b7f6-130">-Location</span></span>
<span data-ttu-id="0b7f6-131">Расположение цепи.</span><span class="sxs-lookup"><span data-stu-id="0b7f6-131">The location of the circuit.</span></span>

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

### <span data-ttu-id="0b7f6-132">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0b7f6-132">-Name</span></span>
<span data-ttu-id="0b7f6-133">Имя создаваемого канала ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="0b7f6-133">The name of the ExpressRoute circuit being created.</span></span>

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

### <span data-ttu-id="0b7f6-134">-Пиринг</span><span class="sxs-lookup"><span data-stu-id="0b7f6-134">-Peering</span></span>
<span data-ttu-id="0b7f6-135">Конфигурации одноранговых элементов списка.</span><span class="sxs-lookup"><span data-stu-id="0b7f6-135">A list peer configurations.</span></span>

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

### <span data-ttu-id="0b7f6-136">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="0b7f6-136">-PeeringLocation</span></span>
<span data-ttu-id="0b7f6-137">Имя расположения пиринга, поддерживаемое поставщиком услуг.</span><span class="sxs-lookup"><span data-stu-id="0b7f6-137">The name of the peering location supported by the service provider.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceProvider
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b7f6-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b7f6-138">-ResourceGroupName</span></span>
<span data-ttu-id="0b7f6-139">Группа ресурсов, в которой будет содержаться цепь.</span><span class="sxs-lookup"><span data-stu-id="0b7f6-139">The resource group that will contain the circuit.</span></span>

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

### <span data-ttu-id="0b7f6-140">-ServiceProviderName</span><span class="sxs-lookup"><span data-stu-id="0b7f6-140">-ServiceProviderName</span></span>
<span data-ttu-id="0b7f6-141">Имя поставщика услуг цепи.</span><span class="sxs-lookup"><span data-stu-id="0b7f6-141">The name of the circuit service provider.</span></span> <span data-ttu-id="0b7f6-142">Оно должно совпадать с именем, указанным в командлете Get-AzureRmExpressRouteServiceProvider.</span><span class="sxs-lookup"><span data-stu-id="0b7f6-142">This must match a name listed by the Get-AzureRmExpressRouteServiceProvider cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceProvider
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b7f6-143">-SkuFamily</span><span class="sxs-lookup"><span data-stu-id="0b7f6-143">-SkuFamily</span></span>
<span data-ttu-id="0b7f6-144">Семейство КОНФИГУРАЦИй определяет тип выставления счетов.</span><span class="sxs-lookup"><span data-stu-id="0b7f6-144">SKU family determines the billing type.</span></span> <span data-ttu-id="0b7f6-145">Возможные значения для этого параметра: `MeteredData` или `UnlimitedData` .</span><span class="sxs-lookup"><span data-stu-id="0b7f6-145">Possible values for this parameter are: `MeteredData` or `UnlimitedData`.</span></span> <span data-ttu-id="0b7f6-146">Обратите внимание, что вы можете изменить тип выставления счетов с MeteredData на UnlimitedData, но вы не можете изменить тип с UnlimitedData на MeteredData.</span><span class="sxs-lookup"><span data-stu-id="0b7f6-146">Note that you can change the billing type from MeteredData to UnlimitedData, but you can't change the type from UnlimitedData to MeteredData.</span></span>

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

### <span data-ttu-id="0b7f6-147">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="0b7f6-147">-SkuTier</span></span>
<span data-ttu-id="0b7f6-148">Уровень обслуживания для канала.</span><span class="sxs-lookup"><span data-stu-id="0b7f6-148">The tier of service for the circuit.</span></span> <span data-ttu-id="0b7f6-149">Возможные значения для этого параметра: `Standard` или `Premium` .</span><span class="sxs-lookup"><span data-stu-id="0b7f6-149">Possible values for this parameter are: `Standard` or `Premium`.</span></span>

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

### <span data-ttu-id="0b7f6-150">-Тег</span><span class="sxs-lookup"><span data-stu-id="0b7f6-150">-Tag</span></span>
<span data-ttu-id="0b7f6-151">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="0b7f6-151">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="0b7f6-152">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="0b7f6-152">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="0b7f6-153">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0b7f6-153">-Confirm</span></span>
<span data-ttu-id="0b7f6-154">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0b7f6-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b7f6-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b7f6-155">-WhatIf</span></span>
<span data-ttu-id="0b7f6-156">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0b7f6-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b7f6-157">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0b7f6-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b7f6-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b7f6-158">CommonParameters</span></span>
<span data-ttu-id="0b7f6-159">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0b7f6-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b7f6-160">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b7f6-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b7f6-161">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0b7f6-161">INPUTS</span></span>

### <span data-ttu-id="0b7f6-162">System. String</span><span class="sxs-lookup"><span data-stu-id="0b7f6-162">System.String</span></span>

### <span data-ttu-id="0b7f6-163">System. Int32</span><span class="sxs-lookup"><span data-stu-id="0b7f6-163">System.Int32</span></span>

### <span data-ttu-id="0b7f6-164">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. Network. Models. PSPeering, Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="0b7f6-164">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSPeering, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="0b7f6-165">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuitAuthorization, Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="0b7f6-165">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="0b7f6-166">System. Nullable "1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="0b7f6-166">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="0b7f6-167">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="0b7f6-167">System.Collections.Hashtable</span></span>

## <span data-ttu-id="0b7f6-168">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0b7f6-168">OUTPUTS</span></span>

### <span data-ttu-id="0b7f6-169">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="0b7f6-169">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="0b7f6-170">Пуск</span><span class="sxs-lookup"><span data-stu-id="0b7f6-170">NOTES</span></span>

## <span data-ttu-id="0b7f6-171">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0b7f6-171">RELATED LINKS</span></span>

[<span data-ttu-id="0b7f6-172">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="0b7f6-172">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="0b7f6-173">Move-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="0b7f6-173">Move-AzureRmExpressRouteCircuit</span></span>](Move-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="0b7f6-174">Remove-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="0b7f6-174">Remove-AzureRmExpressRouteCircuit</span></span>](Remove-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="0b7f6-175">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="0b7f6-175">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)

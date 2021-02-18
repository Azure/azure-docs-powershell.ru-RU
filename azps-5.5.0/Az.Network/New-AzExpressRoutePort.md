---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePort.md
ms.openlocfilehash: 54cdcbbd1d9564dde4fbe4a9aa0b0bea8a0325a3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100240832"
---
# <span data-ttu-id="78264-101">New-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="78264-101">New-AzExpressRoutePort</span></span>

## <span data-ttu-id="78264-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78264-102">SYNOPSIS</span></span>
<span data-ttu-id="78264-103">Создает Azure ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="78264-103">Creates an Azure ExpressRoutePort.</span></span>

## <span data-ttu-id="78264-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="78264-104">SYNTAX</span></span>

### <span data-ttu-id="78264-105">ResourceNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="78264-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzExpressRoutePort -ResourceGroupName <String> -Name <String> -PeeringLocation <String>
 -BandwidthInGbps <Int32> -Encapsulation <String> -Location <String> [-Tag <Hashtable>]
 [-Link <PSExpressRouteLink[]>] [-Force] [-AsJob] [-Identity <PSManagedServiceIdentity>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78264-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="78264-106">ResourceIdParameterSet</span></span>
```
New-AzExpressRoutePort -ResourceId <String> -PeeringLocation <String> -BandwidthInGbps <Int32>
 -Encapsulation <String> -Location <String> [-Tag <Hashtable>] [-Link <PSExpressRouteLink[]>] [-Force] [-AsJob]
 [-Identity <PSManagedServiceIdentity>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="78264-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="78264-107">DESCRIPTION</span></span>
<span data-ttu-id="78264-108">С **его использованием** создается azure ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="78264-108">The **New-AzExpressRoutePort** cmdlet creates an Azure ExpressRoutePort</span></span>

## <span data-ttu-id="78264-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="78264-109">EXAMPLES</span></span>

### <span data-ttu-id="78264-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="78264-110">Example 1</span></span>
```powershell
PS C:\> $parameters = @{
    Name='ExpressRoutePort'
    ResourceGroupName='ExpressRouteResourceGroup'
    Location='West US'
    PeeringLocation='Silicon Valley'
    BandwidthInGbps=100
    Encapsulation='QinQ'
}
PS C:\> New-AzExpressRoutePort @parameters
```

### <span data-ttu-id="78264-111">Пример 2</span><span class="sxs-lookup"><span data-stu-id="78264-111">Example 2</span></span>
```powershell
PS C:\> $parameters = @{
    ResourceId='/subscriptions/<SubId>/resourceGroups/<ResourceGroupName>/providers/Microsoft.Network/expressRoutePorts/<PortName>'
    Location='West US'
    PeeringLocation='Silicon Valley'
    BandwidthInGbps=100
    Encapsulation='QinQ'
}
PS C:\> New-AzExpressRoutePort @parameters
```

## <span data-ttu-id="78264-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="78264-112">PARAMETERS</span></span>

### <span data-ttu-id="78264-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="78264-113">-AsJob</span></span>
<span data-ttu-id="78264-114">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="78264-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="78264-115">-BandwidthInGbps</span><span class="sxs-lookup"><span data-stu-id="78264-115">-BandwidthInGbps</span></span>
<span data-ttu-id="78264-116">Пропускная способность закупаемого порта в Гбит/с</span><span class="sxs-lookup"><span data-stu-id="78264-116">Bandwidth of procured ports in Gbps</span></span>

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

### <span data-ttu-id="78264-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78264-117">-DefaultProfile</span></span>
<span data-ttu-id="78264-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="78264-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78264-119">-Инкапсуляция</span><span class="sxs-lookup"><span data-stu-id="78264-119">-Encapsulation</span></span>
<span data-ttu-id="78264-120">Метод инкапсуляции для физических портов.</span><span class="sxs-lookup"><span data-stu-id="78264-120">Encapsulation method on physical ports.</span></span>

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

### <span data-ttu-id="78264-121">-Force</span><span class="sxs-lookup"><span data-stu-id="78264-121">-Force</span></span>
<span data-ttu-id="78264-122">Не спрашивайте подтверждения при переописи ресурса</span><span class="sxs-lookup"><span data-stu-id="78264-122">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="78264-123">-Identity</span><span class="sxs-lookup"><span data-stu-id="78264-123">-Identity</span></span>
<span data-ttu-id="78264-124">Назначенное пользователем удостоверение для чтения конфигурации MacSec</span><span class="sxs-lookup"><span data-stu-id="78264-124">User Assigned Identity for reading MacSec configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78264-125">-Link</span><span class="sxs-lookup"><span data-stu-id="78264-125">-Link</span></span>
<span data-ttu-id="78264-126">Набор физических связей ресурса ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="78264-126">The set of physical links of the ExpressRoutePort resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78264-127">-Location</span><span class="sxs-lookup"><span data-stu-id="78264-127">-Location</span></span>
<span data-ttu-id="78264-128">Расположение.</span><span class="sxs-lookup"><span data-stu-id="78264-128">The location.</span></span>

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

### <span data-ttu-id="78264-129">-Name</span><span class="sxs-lookup"><span data-stu-id="78264-129">-Name</span></span>
<span data-ttu-id="78264-130">Имя ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="78264-130">The name of the ExpressRoutePort.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78264-131">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="78264-131">-PeeringLocation</span></span>
<span data-ttu-id="78264-132">Имя расположения пиринга, с которое физически сопожается ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="78264-132">The name of the peering location that the ExpressRoutePort is mapped to physically.</span></span>

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

### <span data-ttu-id="78264-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78264-133">-ResourceGroupName</span></span>
<span data-ttu-id="78264-134">Имя группы ресурсов ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="78264-134">The resource group name of the ExpressRoutePort.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78264-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="78264-135">-ResourceId</span></span>
<span data-ttu-id="78264-136">ResourceId порта express route.</span><span class="sxs-lookup"><span data-stu-id="78264-136">ResourceId of the express route port.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78264-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="78264-137">-Tag</span></span>
<span data-ttu-id="78264-138">A hashtable which represents resource tags.</span><span class="sxs-lookup"><span data-stu-id="78264-138">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="78264-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="78264-139">-Confirm</span></span>
<span data-ttu-id="78264-140">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="78264-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78264-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78264-141">-WhatIf</span></span>
<span data-ttu-id="78264-142">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="78264-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78264-143">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="78264-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78264-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78264-144">CommonParameters</span></span>
<span data-ttu-id="78264-145">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78264-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78264-146">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78264-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78264-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="78264-147">INPUTS</span></span>

### <span data-ttu-id="78264-148">System.String</span><span class="sxs-lookup"><span data-stu-id="78264-148">System.String</span></span>

### <span data-ttu-id="78264-149">System.Int32</span><span class="sxs-lookup"><span data-stu-id="78264-149">System.Int32</span></span>

### <span data-ttu-id="78264-150">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="78264-150">System.Collections.Hashtable</span></span>

### <span data-ttu-id="78264-151">Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink[]</span><span class="sxs-lookup"><span data-stu-id="78264-151">Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink[]</span></span>

## <span data-ttu-id="78264-152">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="78264-152">OUTPUTS</span></span>

### <span data-ttu-id="78264-153">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="78264-153">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="78264-154">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="78264-154">NOTES</span></span>

## <span data-ttu-id="78264-155">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="78264-155">RELATED LINKS</span></span>

[<span data-ttu-id="78264-156">Get-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="78264-156">Get-AzExpressRoutePort</span></span>](./Get-AzExpressRoutePort.md)

[<span data-ttu-id="78264-157">Remove-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="78264-157">Remove-AzExpressRoutePort</span></span>](./Remove-AzExpressRoutePort.md)

[<span data-ttu-id="78264-158">Set-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="78264-158">Set-AzExpressRoutePort</span></span>](./Set-AzExpressRoutePort.md)

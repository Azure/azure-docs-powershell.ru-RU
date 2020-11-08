---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/Remove-aznetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterfaceTapConfig.md
ms.openlocfilehash: 52fc2a3c84c70d52c173bc256ca2b0d952307e91
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247255"
---
# <span data-ttu-id="4801d-101">Remove-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="4801d-101">Remove-AzNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="4801d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4801d-102">SYNOPSIS</span></span>
<span data-ttu-id="4801d-103">Удаление конфигурации TAP из данного сетевого интерфейса</span><span class="sxs-lookup"><span data-stu-id="4801d-103">Removes a tap configuration from given network interface</span></span>

## <span data-ttu-id="4801d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4801d-104">SYNTAX</span></span>

### <span data-ttu-id="4801d-105">RemoveByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4801d-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzNetworkInterfaceTapConfig -ResourceGroupName <String> -NetworkInterfaceName <String> -Name <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4801d-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4801d-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzNetworkInterfaceTapConfig -ResourceId <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4801d-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4801d-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzNetworkInterfaceTapConfig -InputObject <PSNetworkInterfaceTapConfiguration> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4801d-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4801d-108">DESCRIPTION</span></span>
<span data-ttu-id="4801d-109">Командлет **Remove-AzNetworkInterfaceTapConfig** удаляет конфигурацию TAP для Azure из списка сетевых интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="4801d-109">The **Remove-AzNetworkInterfaceTapConfig** cmdlet removes an Azure tap configuration from a network interface list.</span></span>

## <span data-ttu-id="4801d-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4801d-110">EXAMPLES</span></span>

### <span data-ttu-id="4801d-111">Пример 1: Удаление конфигурации TAP</span><span class="sxs-lookup"><span data-stu-id="4801d-111">Example 1: Remove a tap configuration</span></span>
```
PS C:\>Remove-AzNetworkInterfaceTapConfig -Name "TapConfiguration" -NetworkInterfaceName "NetworkInterface1" -ResourceGroup "ResourceGroup1"
```

<span data-ttu-id="4801d-112">Эта команда удаляет TapConfiguration из NetworkInterface1 в группе ресурсов ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="4801d-112">This command removes the TapConfiguration from NetworkInterface1 in a resource group ResourceGroup1.</span></span>
<span data-ttu-id="4801d-113">Так как параметр *Force* не используется, пользователю будет предложено подтвердить это действие.</span><span class="sxs-lookup"><span data-stu-id="4801d-113">Because the *Force* parameter is not used, the user will be prompted to confirm this action.</span></span>

### <span data-ttu-id="4801d-114">Пример 2: Удаление сетевого интерфейса</span><span class="sxs-lookup"><span data-stu-id="4801d-114">Example 2: Remove a network interface</span></span>
```
PS C:\>Get-AzNetworkInterfaceTapConfig -Name "TapConfiguration" -NetworkInterfaceName "NetworkInterface1" -ResourceGroup "ResourceGroup1" | Remove-AzNetworkInterfaceTapConfig -Force
```

<span data-ttu-id="4801d-115">Эта команда удаляет TapConfiguration из NetworkInterface1 в группе ресурсов ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="4801d-115">This command removes the TapConfiguration from NetworkInterface1 in a resource group ResourceGroup1.</span></span>
<span data-ttu-id="4801d-116">Поскольку используется параметр *Force* , пользователь не получает запрос на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="4801d-116">Because the *Force* parameter is used, the user is not prompted for confirmation.</span></span>

## <span data-ttu-id="4801d-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4801d-117">PARAMETERS</span></span>

### <span data-ttu-id="4801d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4801d-118">-DefaultProfile</span></span>
<span data-ttu-id="4801d-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4801d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4801d-120">-Force</span><span class="sxs-lookup"><span data-stu-id="4801d-120">-Force</span></span>
<span data-ttu-id="4801d-121">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="4801d-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="4801d-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4801d-122">-InputObject</span></span>
<span data-ttu-id="4801d-123">Ссылка на NetworkInterfaceTapConfig.</span><span class="sxs-lookup"><span data-stu-id="4801d-123">Reference to NetworkInterfaceTapConfig.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4801d-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4801d-124">-Name</span></span>
<span data-ttu-id="4801d-125">Имя пиринга виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="4801d-125">The virtual network peering name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4801d-126">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="4801d-126">-NetworkInterfaceName</span></span>
<span data-ttu-id="4801d-127">Имя виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="4801d-127">The virtual network name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4801d-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4801d-128">-PassThru</span></span>
<span data-ttu-id="4801d-129">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="4801d-129">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="4801d-130">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="4801d-130">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="4801d-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4801d-131">-ResourceGroupName</span></span>
<span data-ttu-id="4801d-132">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4801d-132">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4801d-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4801d-133">-ResourceId</span></span>
<span data-ttu-id="4801d-134">Идентификатор ресурса NetworkInterfaceTapConfig.</span><span class="sxs-lookup"><span data-stu-id="4801d-134">NetworkInterfaceTapConfig resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4801d-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4801d-135">-Confirm</span></span>
<span data-ttu-id="4801d-136">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4801d-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4801d-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4801d-137">-WhatIf</span></span>
<span data-ttu-id="4801d-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4801d-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4801d-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4801d-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4801d-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4801d-140">CommonParameters</span></span>
<span data-ttu-id="4801d-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4801d-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4801d-142">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4801d-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4801d-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4801d-143">INPUTS</span></span>

### <span data-ttu-id="4801d-144">System. String</span><span class="sxs-lookup"><span data-stu-id="4801d-144">System.String</span></span>

### <span data-ttu-id="4801d-145">Microsoft. Azure. Commands. Network. Models. PSNetworkInterfaceTapConfiguration</span><span class="sxs-lookup"><span data-stu-id="4801d-145">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span></span>

## <span data-ttu-id="4801d-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4801d-146">OUTPUTS</span></span>

### <span data-ttu-id="4801d-147">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="4801d-147">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="4801d-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="4801d-148">NOTES</span></span>

## <span data-ttu-id="4801d-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4801d-149">RELATED LINKS</span></span>

[<span data-ttu-id="4801d-150">Add-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="4801d-150">Add-AzNetworkInterfaceTapConfig</span></span>](./Add-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="4801d-151">Get-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="4801d-151">Get-AzNetworkInterfaceTapConfig</span></span>](./Get-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="4801d-152">Set-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="4801d-152">Set-AzNetworkInterfaceTapConfig</span></span>](./Set-AzNetworkInterfaceTapConfig.md)

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/Remove-aznetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterfaceTapConfig.md
ms.openlocfilehash: 8ad89a0f5fad61fea2ba898ea17f63b6f935ae84
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93903445"
---
# <span data-ttu-id="2ca7b-101">Remove-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="2ca7b-101">Remove-AzNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="2ca7b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2ca7b-102">SYNOPSIS</span></span>
<span data-ttu-id="2ca7b-103">Удаление конфигурации TAP из данного сетевого интерфейса</span><span class="sxs-lookup"><span data-stu-id="2ca7b-103">Removes a tap configuration from given network interface</span></span>

## <span data-ttu-id="2ca7b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2ca7b-104">SYNTAX</span></span>

### <span data-ttu-id="2ca7b-105">RemoveByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2ca7b-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzNetworkInterfaceTapConfig -ResourceGroupName <String> -NetworkInterfaceName <String> -Name <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ca7b-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2ca7b-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzNetworkInterfaceTapConfig -ResourceId <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ca7b-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2ca7b-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzNetworkInterfaceTapConfig -InputObject <PSNetworkInterfaceTapConfiguration> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ca7b-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2ca7b-108">DESCRIPTION</span></span>
<span data-ttu-id="2ca7b-109">Командлет **Remove-AzNetworkInterfaceTapConfig** удаляет конфигурацию TAP для Azure из списка сетевых интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="2ca7b-109">The **Remove-AzNetworkInterfaceTapConfig** cmdlet removes an Azure tap configuration from a network interface list.</span></span>

## <span data-ttu-id="2ca7b-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2ca7b-110">EXAMPLES</span></span>

### <span data-ttu-id="2ca7b-111">Пример 1: Удаление конфигурации TAP</span><span class="sxs-lookup"><span data-stu-id="2ca7b-111">Example 1: Remove a tap configuration</span></span>
```
PS C:\>Remove-AzNetworkInterfaceTapConfig -Name "TapConfiguration" -NetworkInterfaceName "NetworkInterface1" -ResourceGroup "ResourceGroup1"
```

<span data-ttu-id="2ca7b-112">Эта команда удаляет TapConfiguration из NetworkInterface1 в группе ресурсов ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="2ca7b-112">This command removes the TapConfiguration from NetworkInterface1 in a resource group ResourceGroup1.</span></span>
<span data-ttu-id="2ca7b-113">Так как параметр *Force* не используется, пользователю будет предложено подтвердить это действие.</span><span class="sxs-lookup"><span data-stu-id="2ca7b-113">Because the *Force* parameter is not used, the user will be prompted to confirm this action.</span></span>

### <span data-ttu-id="2ca7b-114">Пример 2: Удаление сетевого интерфейса</span><span class="sxs-lookup"><span data-stu-id="2ca7b-114">Example 2: Remove a network interface</span></span>
```
PS C:\>Get-AzNetworkInterfaceTapConfig -Name "TapConfiguration" -NetworkInterfaceName "NetworkInterface1" -ResourceGroup "ResourceGroup1" | Remove-AzNetworkInterfaceTapConfig -Force
```

<span data-ttu-id="2ca7b-115">Эта команда удаляет TapConfiguration из NetworkInterface1 в группе ресурсов ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="2ca7b-115">This command removes the TapConfiguration from NetworkInterface1 in a resource group ResourceGroup1.</span></span>
<span data-ttu-id="2ca7b-116">Поскольку используется параметр *Force* , пользователь не получает запрос на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="2ca7b-116">Because the *Force* parameter is used, the user is not prompted for confirmation.</span></span>

## <span data-ttu-id="2ca7b-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2ca7b-117">PARAMETERS</span></span>

### <span data-ttu-id="2ca7b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ca7b-118">-DefaultProfile</span></span>
<span data-ttu-id="2ca7b-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2ca7b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ca7b-120">-Force</span><span class="sxs-lookup"><span data-stu-id="2ca7b-120">-Force</span></span>
<span data-ttu-id="2ca7b-121">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="2ca7b-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="2ca7b-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2ca7b-122">-InputObject</span></span>
<span data-ttu-id="2ca7b-123">Ссылка на NetworkInterfaceTapConfig.</span><span class="sxs-lookup"><span data-stu-id="2ca7b-123">Reference to NetworkInterfaceTapConfig.</span></span>

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

### <span data-ttu-id="2ca7b-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2ca7b-124">-Name</span></span>
<span data-ttu-id="2ca7b-125">Имя пиринга виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="2ca7b-125">The virtual network peering name.</span></span>

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

### <span data-ttu-id="2ca7b-126">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="2ca7b-126">-NetworkInterfaceName</span></span>
<span data-ttu-id="2ca7b-127">Имя виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="2ca7b-127">The virtual network name.</span></span>

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

### <span data-ttu-id="2ca7b-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2ca7b-128">-PassThru</span></span>
<span data-ttu-id="2ca7b-129">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="2ca7b-129">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="2ca7b-130">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="2ca7b-130">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2ca7b-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ca7b-131">-ResourceGroupName</span></span>
<span data-ttu-id="2ca7b-132">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2ca7b-132">The resource group name.</span></span>

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

### <span data-ttu-id="2ca7b-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2ca7b-133">-ResourceId</span></span>
<span data-ttu-id="2ca7b-134">Идентификатор ресурса NetworkInterfaceTapConfig.</span><span class="sxs-lookup"><span data-stu-id="2ca7b-134">NetworkInterfaceTapConfig resource id.</span></span>

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

### <span data-ttu-id="2ca7b-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2ca7b-135">-Confirm</span></span>
<span data-ttu-id="2ca7b-136">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2ca7b-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ca7b-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ca7b-137">-WhatIf</span></span>
<span data-ttu-id="2ca7b-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2ca7b-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ca7b-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2ca7b-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ca7b-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ca7b-140">CommonParameters</span></span>
<span data-ttu-id="2ca7b-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2ca7b-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ca7b-142">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ca7b-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ca7b-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2ca7b-143">INPUTS</span></span>

### <span data-ttu-id="2ca7b-144">System. String</span><span class="sxs-lookup"><span data-stu-id="2ca7b-144">System.String</span></span>

### <span data-ttu-id="2ca7b-145">Microsoft. Azure. Commands. Network. Models. PSNetworkInterfaceTapConfiguration</span><span class="sxs-lookup"><span data-stu-id="2ca7b-145">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span></span>

## <span data-ttu-id="2ca7b-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2ca7b-146">OUTPUTS</span></span>

### <span data-ttu-id="2ca7b-147">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="2ca7b-147">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="2ca7b-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="2ca7b-148">NOTES</span></span>

## <span data-ttu-id="2ca7b-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2ca7b-149">RELATED LINKS</span></span>

[<span data-ttu-id="2ca7b-150">Add-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="2ca7b-150">Add-AzNetworkInterfaceTapConfig</span></span>](./Add-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="2ca7b-151">Get-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="2ca7b-151">Get-AzNetworkInterfaceTapConfig</span></span>](./Get-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="2ca7b-152">Set-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="2ca7b-152">Set-AzNetworkInterfaceTapConfig</span></span>](./Set-AzNetworkInterfaceTapConfig.md)

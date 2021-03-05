---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/Remove-aznetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterfaceTapConfig.md
ms.openlocfilehash: 54468717f979188d31d6ba318556be87c37e50b9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993639"
---
# <span data-ttu-id="45407-101">Remove-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="45407-101">Remove-AzNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="45407-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="45407-102">SYNOPSIS</span></span>
<span data-ttu-id="45407-103">Удаление конфигурации темы из заданного сетевого интерфейса</span><span class="sxs-lookup"><span data-stu-id="45407-103">Removes a tap configuration from given network interface</span></span>

## <span data-ttu-id="45407-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="45407-104">SYNTAX</span></span>

### <span data-ttu-id="45407-105">RemoveByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="45407-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzNetworkInterfaceTapConfig -ResourceGroupName <String> -NetworkInterfaceName <String> -Name <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45407-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="45407-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzNetworkInterfaceTapConfig -ResourceId <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45407-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="45407-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzNetworkInterfaceTapConfig -InputObject <PSNetworkInterfaceTapConfiguration> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45407-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="45407-108">DESCRIPTION</span></span>
<span data-ttu-id="45407-109">Командлет **Remove-AzNetworkInterfaceTapConfig** удаляет конфигурацию касания Azure из списка сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="45407-109">The **Remove-AzNetworkInterfaceTapConfig** cmdlet removes an Azure tap configuration from a network interface list.</span></span>

## <span data-ttu-id="45407-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="45407-110">EXAMPLES</span></span>

### <span data-ttu-id="45407-111">Пример 1. Удаление конфигурации касания</span><span class="sxs-lookup"><span data-stu-id="45407-111">Example 1: Remove a tap configuration</span></span>
```
PS C:\>Remove-AzNetworkInterfaceTapConfig -Name "TapConfiguration" -NetworkInterfaceName "NetworkInterface1" -ResourceGroup "ResourceGroup1"
```

<span data-ttu-id="45407-112">Эта команда удаляет команду TapConfiguration из NetworkInterface1 в группе ресурсов ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="45407-112">This command removes the TapConfiguration from NetworkInterface1 in a resource group ResourceGroup1.</span></span>
<span data-ttu-id="45407-113">Так как *параметр Force* не используется, пользователю будет предложено подтвердить это действие.</span><span class="sxs-lookup"><span data-stu-id="45407-113">Because the *Force* parameter is not used, the user will be prompted to confirm this action.</span></span>

### <span data-ttu-id="45407-114">Пример 2. Удаление сетевого интерфейса</span><span class="sxs-lookup"><span data-stu-id="45407-114">Example 2: Remove a network interface</span></span>
```
PS C:\>Get-AzNetworkInterfaceTapConfig -Name "TapConfiguration" -NetworkInterfaceName "NetworkInterface1" -ResourceGroup "ResourceGroup1" | Remove-AzNetworkInterfaceTapConfig -Force
```

<span data-ttu-id="45407-115">Эта команда удаляет команду TapConfiguration из NetworkInterface1 в группе ресурсов ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="45407-115">This command removes the TapConfiguration from NetworkInterface1 in a resource group ResourceGroup1.</span></span>
<span data-ttu-id="45407-116">Так как используется параметр *Force,* пользователю не будет предложено подтверждение.</span><span class="sxs-lookup"><span data-stu-id="45407-116">Because the *Force* parameter is used, the user is not prompted for confirmation.</span></span>

## <span data-ttu-id="45407-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="45407-117">PARAMETERS</span></span>

### <span data-ttu-id="45407-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45407-118">-DefaultProfile</span></span>
<span data-ttu-id="45407-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="45407-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="45407-120">-Force</span><span class="sxs-lookup"><span data-stu-id="45407-120">-Force</span></span>
<span data-ttu-id="45407-121">Не спрашивайте подтверждения.</span><span class="sxs-lookup"><span data-stu-id="45407-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="45407-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="45407-122">-InputObject</span></span>
<span data-ttu-id="45407-123">Ссылка на NetworkInterfaceTapConfig.</span><span class="sxs-lookup"><span data-stu-id="45407-123">Reference to NetworkInterfaceTapConfig.</span></span>

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

### <span data-ttu-id="45407-124">-Name</span><span class="sxs-lookup"><span data-stu-id="45407-124">-Name</span></span>
<span data-ttu-id="45407-125">Имя виртуального сетевого пиринга.</span><span class="sxs-lookup"><span data-stu-id="45407-125">The virtual network peering name.</span></span>

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

### <span data-ttu-id="45407-126">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="45407-126">-NetworkInterfaceName</span></span>
<span data-ttu-id="45407-127">Имя виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="45407-127">The virtual network name.</span></span>

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

### <span data-ttu-id="45407-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="45407-128">-PassThru</span></span>
<span data-ttu-id="45407-129">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="45407-129">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="45407-130">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="45407-130">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="45407-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45407-131">-ResourceGroupName</span></span>
<span data-ttu-id="45407-132">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="45407-132">The resource group name.</span></span>

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

### <span data-ttu-id="45407-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="45407-133">-ResourceId</span></span>
<span data-ttu-id="45407-134">NetworkInterfaceTapConfig resource id.</span><span class="sxs-lookup"><span data-stu-id="45407-134">NetworkInterfaceTapConfig resource id.</span></span>

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

### <span data-ttu-id="45407-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="45407-135">-Confirm</span></span>
<span data-ttu-id="45407-136">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="45407-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45407-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45407-137">-WhatIf</span></span>
<span data-ttu-id="45407-138">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45407-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45407-139">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="45407-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45407-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45407-140">CommonParameters</span></span>
<span data-ttu-id="45407-141">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45407-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45407-142">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45407-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45407-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="45407-143">INPUTS</span></span>

### <span data-ttu-id="45407-144">System.String</span><span class="sxs-lookup"><span data-stu-id="45407-144">System.String</span></span>

### <span data-ttu-id="45407-145">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span><span class="sxs-lookup"><span data-stu-id="45407-145">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span></span>

## <span data-ttu-id="45407-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="45407-146">OUTPUTS</span></span>

### <span data-ttu-id="45407-147">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="45407-147">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="45407-148">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="45407-148">NOTES</span></span>

## <span data-ttu-id="45407-149">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="45407-149">RELATED LINKS</span></span>

[<span data-ttu-id="45407-150">Add-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="45407-150">Add-AzNetworkInterfaceTapConfig</span></span>](./Add-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="45407-151">Get-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="45407-151">Get-AzNetworkInterfaceTapConfig</span></span>](./Get-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="45407-152">Set-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="45407-152">Set-AzNetworkInterfaceTapConfig</span></span>](./Set-AzNetworkInterfaceTapConfig.md)

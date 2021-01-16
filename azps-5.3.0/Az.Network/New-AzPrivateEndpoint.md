---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivateendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateEndpoint.md
ms.openlocfilehash: df298b41ea1efa4915cb7556b9fd07b1d8f3e2de
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98507829"
---
# <span data-ttu-id="6ccc3-101">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="6ccc3-101">New-AzPrivateEndpoint</span></span>

## <span data-ttu-id="6ccc3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ccc3-102">SYNOPSIS</span></span>
<span data-ttu-id="6ccc3-103">Создает частную конечную точку.</span><span class="sxs-lookup"><span data-stu-id="6ccc3-103">Creates a private endpoint.</span></span>

## <span data-ttu-id="6ccc3-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6ccc3-104">SYNTAX</span></span>

### <span data-ttu-id="6ccc3-105">Все</span><span class="sxs-lookup"><span data-stu-id="6ccc3-105">All</span></span>

```
New-AzPrivateEndpoint -Name <String> -ResourceGroupName <String> -Location <String> -Subnet <PSSubnet>
 -PrivateLinkServiceConnection <PSPrivateLinkServiceConnection[]> [-ByManualRequest] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ccc3-106">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6ccc3-106">DESCRIPTION</span></span>

<span data-ttu-id="6ccc3-107">Для создания закрытой конечной точки будет назначена конечная точка **New-AzPrivateEndpoint.**</span><span class="sxs-lookup"><span data-stu-id="6ccc3-107">The **New-AzPrivateEndpoint** cmdlet creates a private endpoint.</span></span>

## <span data-ttu-id="6ccc3-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6ccc3-108">EXAMPLES</span></span>

### <span data-ttu-id="6ccc3-109">Пример 1. Создание закрытой конечной точки</span><span class="sxs-lookup"><span data-stu-id="6ccc3-109">Example 1: Create a private endpoint</span></span>

<span data-ttu-id="6ccc3-110">В следующем примере создается частная конечная точка с определенным ИД службы частных ссылок в указанной подсети виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="6ccc3-110">The following example creates a private endpoint with a specific private link service ID in the specified subnet in a virtual network.</span></span>

```powershell
$virtualNetwork = Get-AzVirtualNetwork -ResourceName 'myVirtualNetwork' -ResourceGroupName 'myResourceGroup'
$subnet = $virtualNetwork | Select-Object -ExpandProperty subnets | Where-Object Name -eq 'mySubnet'
$plsConnection= New-AzPrivateLinkServiceConnection -Name 'MyPLSConnections' -PrivateLinkServiceId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myResourceGroup/providers/Microsoft.Network/privateLinkServices/privateLinkService' -RequestMessage 'Please Approve my request'
New-AzPrivateEndpoint -Name 'MyPrivateEndpoint' -ResourceGroup 'myResourceGroup' -Location 'centralus' -PrivateLinkServiceConnection $plsConnection -Subnet $subnet
```

## <span data-ttu-id="6ccc3-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6ccc3-111">PARAMETERS</span></span>

### <span data-ttu-id="6ccc3-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6ccc3-112">-AsJob</span></span>

<span data-ttu-id="6ccc3-113">Запуск cmdlet в качестве задания в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="6ccc3-113">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="6ccc3-114">-ByManualRequest</span><span class="sxs-lookup"><span data-stu-id="6ccc3-114">-ByManualRequest</span></span>

<span data-ttu-id="6ccc3-115">Используйте ручной запрос для установления соединения.</span><span class="sxs-lookup"><span data-stu-id="6ccc3-115">Use manual request to establish the connection.</span></span>

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

### <span data-ttu-id="6ccc3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ccc3-116">-DefaultProfile</span></span>

<span data-ttu-id="6ccc3-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6ccc3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ccc3-118">-Force</span><span class="sxs-lookup"><span data-stu-id="6ccc3-118">-Force</span></span>

<span data-ttu-id="6ccc3-119">Не спрашивайте подтверждения для переописи ресурса.</span><span class="sxs-lookup"><span data-stu-id="6ccc3-119">Do not ask for confirmation to overwrite a resource.</span></span>

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

### <span data-ttu-id="6ccc3-120">-Location</span><span class="sxs-lookup"><span data-stu-id="6ccc3-120">-Location</span></span>

<span data-ttu-id="6ccc3-121">Указывает расположение закрытой конечной точки.</span><span class="sxs-lookup"><span data-stu-id="6ccc3-121">Specifies a location for the private endpoint.</span></span> <span data-ttu-id="6ccc3-122">С [помощью Get-AzLocation](/powershell/module/az.resources/get-azlocation) можно определить допустимые значения для этого параметра.</span><span class="sxs-lookup"><span data-stu-id="6ccc3-122">Use [Get-AzLocation](/powershell/module/az.resources/get-azlocation) to determine valid values for this parameter.</span></span>

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

### <span data-ttu-id="6ccc3-123">-Name</span><span class="sxs-lookup"><span data-stu-id="6ccc3-123">-Name</span></span>

<span data-ttu-id="6ccc3-124">Имя закрытой конечной точки.</span><span class="sxs-lookup"><span data-stu-id="6ccc3-124">Name of the private endpoint.</span></span>

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

### <span data-ttu-id="6ccc3-125">-PrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="6ccc3-125">-PrivateLinkServiceConnection</span></span>

<span data-ttu-id="6ccc3-126">ИД ресурса для подключения частной конечной точки.</span><span class="sxs-lookup"><span data-stu-id="6ccc3-126">The resource ID to connect the private endpoint.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceConnection[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ccc3-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ccc3-127">-ResourceGroupName</span></span>

<span data-ttu-id="6ccc3-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6ccc3-128">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="6ccc3-129">-Subnet</span><span class="sxs-lookup"><span data-stu-id="6ccc3-129">-Subnet</span></span>

<span data-ttu-id="6ccc3-130">Подсеть закрытой конечной точки.</span><span class="sxs-lookup"><span data-stu-id="6ccc3-130">The subnet of the private endpoint.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ccc3-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="6ccc3-131">-Tag</span></span>

<span data-ttu-id="6ccc3-132">Пары значений ключа в виде hash table.</span><span class="sxs-lookup"><span data-stu-id="6ccc3-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="6ccc3-133">Например: @{key0='value0';key1=$null;key2='value2'}</span><span class="sxs-lookup"><span data-stu-id="6ccc3-133">For example: @{key0='value0';key1=$null;key2='value2'}</span></span>

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

### <span data-ttu-id="6ccc3-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6ccc3-134">-Confirm</span></span>

<span data-ttu-id="6ccc3-135">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ccc3-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ccc3-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ccc3-136">-WhatIf</span></span>

<span data-ttu-id="6ccc3-137">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ccc3-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ccc3-138">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="6ccc3-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ccc3-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ccc3-139">CommonParameters</span></span>

<span data-ttu-id="6ccc3-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ccc3-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ccc3-141">Дополнительные сведения см. [в about_CommonParameters.](/powershell/module/microsoft.powershell.core/about/about_commonparameters)</span><span class="sxs-lookup"><span data-stu-id="6ccc3-141">For more information, see [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).</span></span>

## <span data-ttu-id="6ccc3-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6ccc3-142">INPUTS</span></span>

### <span data-ttu-id="6ccc3-143">System.String</span><span class="sxs-lookup"><span data-stu-id="6ccc3-143">System.String</span></span>

### <span data-ttu-id="6ccc3-144">Microsoft.Azure.Commands.Network.Models.PSSubnet</span><span class="sxs-lookup"><span data-stu-id="6ccc3-144">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="6ccc3-145">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceConnection[]</span><span class="sxs-lookup"><span data-stu-id="6ccc3-145">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceConnection[]</span></span>

## <span data-ttu-id="6ccc3-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6ccc3-146">OUTPUTS</span></span>

### <span data-ttu-id="6ccc3-147">Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="6ccc3-147">Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint</span></span>

## <span data-ttu-id="6ccc3-148">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6ccc3-148">NOTES</span></span>

## <span data-ttu-id="6ccc3-149">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6ccc3-149">RELATED LINKS</span></span>

[<span data-ttu-id="6ccc3-150">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="6ccc3-150">Get-AzPrivateEndpoint</span></span>](./Get-AzPrivateEndpoint.md)

[<span data-ttu-id="6ccc3-151">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="6ccc3-151">Remove-AzPrivateEndpoint</span></span>](./Remove-AzPrivateEndpoint.md)

[<span data-ttu-id="6ccc3-152">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="6ccc3-152">New-AzPrivateLinkServiceConnection</span></span>](./New-AzPrivateLinkServiceConnection.md)
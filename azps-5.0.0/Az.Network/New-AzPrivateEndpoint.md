---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivateendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateEndpoint.md
ms.openlocfilehash: df298b41ea1efa4915cb7556b9fd07b1d8f3e2de
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248830"
---
# <span data-ttu-id="7c130-101">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="7c130-101">New-AzPrivateEndpoint</span></span>

## <span data-ttu-id="7c130-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7c130-102">SYNOPSIS</span></span>
<span data-ttu-id="7c130-103">Создает частную конечную точку.</span><span class="sxs-lookup"><span data-stu-id="7c130-103">Creates a private endpoint.</span></span>

## <span data-ttu-id="7c130-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7c130-104">SYNTAX</span></span>

### <span data-ttu-id="7c130-105">Весь</span><span class="sxs-lookup"><span data-stu-id="7c130-105">All</span></span>

```
New-AzPrivateEndpoint -Name <String> -ResourceGroupName <String> -Location <String> -Subnet <PSSubnet>
 -PrivateLinkServiceConnection <PSPrivateLinkServiceConnection[]> [-ByManualRequest] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c130-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7c130-106">DESCRIPTION</span></span>

<span data-ttu-id="7c130-107">Командлет **New-AzPrivateEndpoint** создает частную конечную точку.</span><span class="sxs-lookup"><span data-stu-id="7c130-107">The **New-AzPrivateEndpoint** cmdlet creates a private endpoint.</span></span>

## <span data-ttu-id="7c130-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7c130-108">EXAMPLES</span></span>

### <span data-ttu-id="7c130-109">Пример 1: создание частной конечной точки</span><span class="sxs-lookup"><span data-stu-id="7c130-109">Example 1: Create a private endpoint</span></span>

<span data-ttu-id="7c130-110">В следующем примере создается частная конечная точка с определенным ИДЕНТИФИКАТОРом службы частной ссылки в указанной подсети виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="7c130-110">The following example creates a private endpoint with a specific private link service ID in the specified subnet in a virtual network.</span></span>

```powershell
$virtualNetwork = Get-AzVirtualNetwork -ResourceName 'myVirtualNetwork' -ResourceGroupName 'myResourceGroup'
$subnet = $virtualNetwork | Select-Object -ExpandProperty subnets | Where-Object Name -eq 'mySubnet'
$plsConnection= New-AzPrivateLinkServiceConnection -Name 'MyPLSConnections' -PrivateLinkServiceId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myResourceGroup/providers/Microsoft.Network/privateLinkServices/privateLinkService' -RequestMessage 'Please Approve my request'
New-AzPrivateEndpoint -Name 'MyPrivateEndpoint' -ResourceGroup 'myResourceGroup' -Location 'centralus' -PrivateLinkServiceConnection $plsConnection -Subnet $subnet
```

## <span data-ttu-id="7c130-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7c130-111">PARAMETERS</span></span>

### <span data-ttu-id="7c130-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7c130-112">-AsJob</span></span>

<span data-ttu-id="7c130-113">Запустите командлет как задание в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="7c130-113">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="7c130-114">-ByManualRequest</span><span class="sxs-lookup"><span data-stu-id="7c130-114">-ByManualRequest</span></span>

<span data-ttu-id="7c130-115">Использование запроса вручную для установления соединения.</span><span class="sxs-lookup"><span data-stu-id="7c130-115">Use manual request to establish the connection.</span></span>

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

### <span data-ttu-id="7c130-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c130-116">-DefaultProfile</span></span>

<span data-ttu-id="7c130-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7c130-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c130-118">-Force</span><span class="sxs-lookup"><span data-stu-id="7c130-118">-Force</span></span>

<span data-ttu-id="7c130-119">Не запрашивать подтверждение на перезапись ресурса.</span><span class="sxs-lookup"><span data-stu-id="7c130-119">Do not ask for confirmation to overwrite a resource.</span></span>

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

### <span data-ttu-id="7c130-120">-Location</span><span class="sxs-lookup"><span data-stu-id="7c130-120">-Location</span></span>

<span data-ttu-id="7c130-121">Задает расположение для закрытой конечной точки.</span><span class="sxs-lookup"><span data-stu-id="7c130-121">Specifies a location for the private endpoint.</span></span> <span data-ttu-id="7c130-122">Для определения допустимых значений для этого параметра используйте [Get-AzLocation](/powershell/module/az.resources/get-azlocation) .</span><span class="sxs-lookup"><span data-stu-id="7c130-122">Use [Get-AzLocation](/powershell/module/az.resources/get-azlocation) to determine valid values for this parameter.</span></span>

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

### <span data-ttu-id="7c130-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7c130-123">-Name</span></span>

<span data-ttu-id="7c130-124">Имя частной конечной точки.</span><span class="sxs-lookup"><span data-stu-id="7c130-124">Name of the private endpoint.</span></span>

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

### <span data-ttu-id="7c130-125">-PrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="7c130-125">-PrivateLinkServiceConnection</span></span>

<span data-ttu-id="7c130-126">Идентификатор ресурса для подключения закрытой конечной точки.</span><span class="sxs-lookup"><span data-stu-id="7c130-126">The resource ID to connect the private endpoint.</span></span>

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

### <span data-ttu-id="7c130-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c130-127">-ResourceGroupName</span></span>

<span data-ttu-id="7c130-128">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7c130-128">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="7c130-129">-Подсеть</span><span class="sxs-lookup"><span data-stu-id="7c130-129">-Subnet</span></span>

<span data-ttu-id="7c130-130">Подсеть частной конечной точки.</span><span class="sxs-lookup"><span data-stu-id="7c130-130">The subnet of the private endpoint.</span></span>

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

### <span data-ttu-id="7c130-131">-Тег</span><span class="sxs-lookup"><span data-stu-id="7c130-131">-Tag</span></span>

<span data-ttu-id="7c130-132">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="7c130-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="7c130-133">Например: @ {Key0 = ' value0 '; key1 = $null; key2 = ' значение2 '}</span><span class="sxs-lookup"><span data-stu-id="7c130-133">For example: @{key0='value0';key1=$null;key2='value2'}</span></span>

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

### <span data-ttu-id="7c130-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7c130-134">-Confirm</span></span>

<span data-ttu-id="7c130-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7c130-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c130-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c130-136">-WhatIf</span></span>

<span data-ttu-id="7c130-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7c130-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c130-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7c130-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c130-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c130-139">CommonParameters</span></span>

<span data-ttu-id="7c130-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7c130-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c130-141">Дополнительные сведения можно найти в разделе [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).</span><span class="sxs-lookup"><span data-stu-id="7c130-141">For more information, see [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).</span></span>

## <span data-ttu-id="7c130-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7c130-142">INPUTS</span></span>

### <span data-ttu-id="7c130-143">System. String</span><span class="sxs-lookup"><span data-stu-id="7c130-143">System.String</span></span>

### <span data-ttu-id="7c130-144">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="7c130-144">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="7c130-145">Microsoft. Azure. Commands. Network. Models. PSPrivateLinkServiceConnection []</span><span class="sxs-lookup"><span data-stu-id="7c130-145">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceConnection[]</span></span>

## <span data-ttu-id="7c130-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7c130-146">OUTPUTS</span></span>

### <span data-ttu-id="7c130-147">Microsoft. Azure. Commands. Network. Models. PSPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="7c130-147">Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint</span></span>

## <span data-ttu-id="7c130-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="7c130-148">NOTES</span></span>

## <span data-ttu-id="7c130-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7c130-149">RELATED LINKS</span></span>

[<span data-ttu-id="7c130-150">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="7c130-150">Get-AzPrivateEndpoint</span></span>](./Get-AzPrivateEndpoint.md)

[<span data-ttu-id="7c130-151">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="7c130-151">Remove-AzPrivateEndpoint</span></span>](./Remove-AzPrivateEndpoint.md)

[<span data-ttu-id="7c130-152">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="7c130-152">New-AzPrivateLinkServiceConnection</span></span>](./New-AzPrivateLinkServiceConnection.md)
---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivateendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateEndpoint.md
ms.openlocfilehash: df298b41ea1efa4915cb7556b9fd07b1d8f3e2de
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94242988"
---
# <span data-ttu-id="b7aef-101">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="b7aef-101">New-AzPrivateEndpoint</span></span>

## <span data-ttu-id="b7aef-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b7aef-102">SYNOPSIS</span></span>
<span data-ttu-id="b7aef-103">Создает частную конечную точку.</span><span class="sxs-lookup"><span data-stu-id="b7aef-103">Creates a private endpoint.</span></span>

## <span data-ttu-id="b7aef-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b7aef-104">SYNTAX</span></span>

### <span data-ttu-id="b7aef-105">Весь</span><span class="sxs-lookup"><span data-stu-id="b7aef-105">All</span></span>

```
New-AzPrivateEndpoint -Name <String> -ResourceGroupName <String> -Location <String> -Subnet <PSSubnet>
 -PrivateLinkServiceConnection <PSPrivateLinkServiceConnection[]> [-ByManualRequest] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7aef-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b7aef-106">DESCRIPTION</span></span>

<span data-ttu-id="b7aef-107">Командлет **New-AzPrivateEndpoint** создает частную конечную точку.</span><span class="sxs-lookup"><span data-stu-id="b7aef-107">The **New-AzPrivateEndpoint** cmdlet creates a private endpoint.</span></span>

## <span data-ttu-id="b7aef-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b7aef-108">EXAMPLES</span></span>

### <span data-ttu-id="b7aef-109">Пример 1: создание частной конечной точки</span><span class="sxs-lookup"><span data-stu-id="b7aef-109">Example 1: Create a private endpoint</span></span>

<span data-ttu-id="b7aef-110">В следующем примере создается частная конечная точка с определенным ИДЕНТИФИКАТОРом службы частной ссылки в указанной подсети виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="b7aef-110">The following example creates a private endpoint with a specific private link service ID in the specified subnet in a virtual network.</span></span>

```powershell
$virtualNetwork = Get-AzVirtualNetwork -ResourceName 'myVirtualNetwork' -ResourceGroupName 'myResourceGroup'
$subnet = $virtualNetwork | Select-Object -ExpandProperty subnets | Where-Object Name -eq 'mySubnet'
$plsConnection= New-AzPrivateLinkServiceConnection -Name 'MyPLSConnections' -PrivateLinkServiceId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myResourceGroup/providers/Microsoft.Network/privateLinkServices/privateLinkService' -RequestMessage 'Please Approve my request'
New-AzPrivateEndpoint -Name 'MyPrivateEndpoint' -ResourceGroup 'myResourceGroup' -Location 'centralus' -PrivateLinkServiceConnection $plsConnection -Subnet $subnet
```

## <span data-ttu-id="b7aef-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b7aef-111">PARAMETERS</span></span>

### <span data-ttu-id="b7aef-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b7aef-112">-AsJob</span></span>

<span data-ttu-id="b7aef-113">Запустите командлет как задание в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="b7aef-113">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="b7aef-114">-ByManualRequest</span><span class="sxs-lookup"><span data-stu-id="b7aef-114">-ByManualRequest</span></span>

<span data-ttu-id="b7aef-115">Использование запроса вручную для установления соединения.</span><span class="sxs-lookup"><span data-stu-id="b7aef-115">Use manual request to establish the connection.</span></span>

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

### <span data-ttu-id="b7aef-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7aef-116">-DefaultProfile</span></span>

<span data-ttu-id="b7aef-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b7aef-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7aef-118">-Force</span><span class="sxs-lookup"><span data-stu-id="b7aef-118">-Force</span></span>

<span data-ttu-id="b7aef-119">Не запрашивать подтверждение на перезапись ресурса.</span><span class="sxs-lookup"><span data-stu-id="b7aef-119">Do not ask for confirmation to overwrite a resource.</span></span>

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

### <span data-ttu-id="b7aef-120">-Location</span><span class="sxs-lookup"><span data-stu-id="b7aef-120">-Location</span></span>

<span data-ttu-id="b7aef-121">Задает расположение для закрытой конечной точки.</span><span class="sxs-lookup"><span data-stu-id="b7aef-121">Specifies a location for the private endpoint.</span></span> <span data-ttu-id="b7aef-122">Для определения допустимых значений для этого параметра используйте [Get-AzLocation](/powershell/module/az.resources/get-azlocation) .</span><span class="sxs-lookup"><span data-stu-id="b7aef-122">Use [Get-AzLocation](/powershell/module/az.resources/get-azlocation) to determine valid values for this parameter.</span></span>

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

### <span data-ttu-id="b7aef-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b7aef-123">-Name</span></span>

<span data-ttu-id="b7aef-124">Имя частной конечной точки.</span><span class="sxs-lookup"><span data-stu-id="b7aef-124">Name of the private endpoint.</span></span>

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

### <span data-ttu-id="b7aef-125">-PrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="b7aef-125">-PrivateLinkServiceConnection</span></span>

<span data-ttu-id="b7aef-126">Идентификатор ресурса для подключения закрытой конечной точки.</span><span class="sxs-lookup"><span data-stu-id="b7aef-126">The resource ID to connect the private endpoint.</span></span>

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

### <span data-ttu-id="b7aef-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7aef-127">-ResourceGroupName</span></span>

<span data-ttu-id="b7aef-128">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b7aef-128">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="b7aef-129">-Подсеть</span><span class="sxs-lookup"><span data-stu-id="b7aef-129">-Subnet</span></span>

<span data-ttu-id="b7aef-130">Подсеть частной конечной точки.</span><span class="sxs-lookup"><span data-stu-id="b7aef-130">The subnet of the private endpoint.</span></span>

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

### <span data-ttu-id="b7aef-131">-Тег</span><span class="sxs-lookup"><span data-stu-id="b7aef-131">-Tag</span></span>

<span data-ttu-id="b7aef-132">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="b7aef-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="b7aef-133">Например: @ {Key0 = ' value0 '; key1 = $null; key2 = ' значение2 '}</span><span class="sxs-lookup"><span data-stu-id="b7aef-133">For example: @{key0='value0';key1=$null;key2='value2'}</span></span>

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

### <span data-ttu-id="b7aef-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b7aef-134">-Confirm</span></span>

<span data-ttu-id="b7aef-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b7aef-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7aef-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7aef-136">-WhatIf</span></span>

<span data-ttu-id="b7aef-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b7aef-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7aef-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b7aef-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7aef-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7aef-139">CommonParameters</span></span>

<span data-ttu-id="b7aef-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b7aef-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7aef-141">Дополнительные сведения можно найти в разделе [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).</span><span class="sxs-lookup"><span data-stu-id="b7aef-141">For more information, see [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).</span></span>

## <span data-ttu-id="b7aef-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b7aef-142">INPUTS</span></span>

### <span data-ttu-id="b7aef-143">System. String</span><span class="sxs-lookup"><span data-stu-id="b7aef-143">System.String</span></span>

### <span data-ttu-id="b7aef-144">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="b7aef-144">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="b7aef-145">Microsoft. Azure. Commands. Network. Models. PSPrivateLinkServiceConnection []</span><span class="sxs-lookup"><span data-stu-id="b7aef-145">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceConnection[]</span></span>

## <span data-ttu-id="b7aef-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b7aef-146">OUTPUTS</span></span>

### <span data-ttu-id="b7aef-147">Microsoft. Azure. Commands. Network. Models. PSPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="b7aef-147">Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint</span></span>

## <span data-ttu-id="b7aef-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="b7aef-148">NOTES</span></span>

## <span data-ttu-id="b7aef-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b7aef-149">RELATED LINKS</span></span>

[<span data-ttu-id="b7aef-150">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="b7aef-150">Get-AzPrivateEndpoint</span></span>](./Get-AzPrivateEndpoint.md)

[<span data-ttu-id="b7aef-151">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="b7aef-151">Remove-AzPrivateEndpoint</span></span>](./Remove-AzPrivateEndpoint.md)

[<span data-ttu-id="b7aef-152">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="b7aef-152">New-AzPrivateLinkServiceConnection</span></span>](./New-AzPrivateLinkServiceConnection.md)
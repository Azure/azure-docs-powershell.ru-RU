---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivateendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateEndpoint.md
ms.openlocfilehash: c72af57f860dcc1c889ecf81111341fa7dbe21eb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93903605"
---
# <span data-ttu-id="d64e8-101">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="d64e8-101">New-AzPrivateEndpoint</span></span>

## <span data-ttu-id="d64e8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d64e8-102">SYNOPSIS</span></span>
<span data-ttu-id="d64e8-103">Создает частную конечную точку.</span><span class="sxs-lookup"><span data-stu-id="d64e8-103">Creates a private endpoint.</span></span>

## <span data-ttu-id="d64e8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d64e8-104">SYNTAX</span></span>

```
New-AzPrivateEndpoint -Name <String> -ResourceGroupName <String> -Location <String> -Subnet <PSSubnet>
 -PrivateLinkServiceConnection <PSPrivateLinkServiceConnection[]> [-ByManualRequest] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d64e8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d64e8-105">DESCRIPTION</span></span>
<span data-ttu-id="d64e8-106">Командлет **New-AzPrivateEndpoint** создает частную конечную точку.</span><span class="sxs-lookup"><span data-stu-id="d64e8-106">The **New-AzPrivateEndpoint** cmdlet creates a private endpoint.</span></span>

## <span data-ttu-id="d64e8-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d64e8-107">EXAMPLES</span></span>

### <span data-ttu-id="d64e8-108">1: создание частной конечной точки</span><span class="sxs-lookup"><span data-stu-id="d64e8-108">1: Create a private endpoint</span></span>
```
$virtualNetwork = Get-AzVirtualNetwork -ResourceName MyVirtualNetwork -ResourceGroupName TestResourceGroup
$plsConnection= New-AzPrivateLinkServiceConnection -Name MyPLSConnections -PrivateLinkServiceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/privateLinkServices/privateLinkService" -RequestMessage "Please Approve my request"
New-AzPrivateEndpoint -Name MyPrivateEndpoint -ResourceGroup TestResourceGroup -Location centralus -PrivateLinkServiceConnection $plsConnection -Subnet $virtualNetwork.Subnets[0]
```

<span data-ttu-id="d64e8-109">В этом примере создается частная конечная точка с определенным ИД службы частной ссылки в конкретной подсети виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="d64e8-109">This example creates a private endpoint with specific private link service id in a specific subnet in a virtual network.</span></span>

## <span data-ttu-id="d64e8-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d64e8-110">PARAMETERS</span></span>

### <span data-ttu-id="d64e8-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d64e8-111">-AsJob</span></span>
<span data-ttu-id="d64e8-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="d64e8-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d64e8-113">-ByManualRequest</span><span class="sxs-lookup"><span data-stu-id="d64e8-113">-ByManualRequest</span></span>
<span data-ttu-id="d64e8-114">Использование ручного запроса.</span><span class="sxs-lookup"><span data-stu-id="d64e8-114">Using manual request.</span></span>

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

### <span data-ttu-id="d64e8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d64e8-115">-DefaultProfile</span></span>
<span data-ttu-id="d64e8-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d64e8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d64e8-117">-Force</span><span class="sxs-lookup"><span data-stu-id="d64e8-117">-Force</span></span>
<span data-ttu-id="d64e8-118">Не запрашивать подтверждение, если вы хотите перезаписать ресурс</span><span class="sxs-lookup"><span data-stu-id="d64e8-118">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="d64e8-119">-Location</span><span class="sxs-lookup"><span data-stu-id="d64e8-119">-Location</span></span>
<span data-ttu-id="d64e8-120">поиска.</span><span class="sxs-lookup"><span data-stu-id="d64e8-120">location.</span></span>

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

### <span data-ttu-id="d64e8-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d64e8-121">-Name</span></span>
<span data-ttu-id="d64e8-122">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="d64e8-122">The resource name.</span></span>

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

### <span data-ttu-id="d64e8-123">-PrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="d64e8-123">-PrivateLinkServiceConnection</span></span>
<span data-ttu-id="d64e8-124">Подключение к службе частной ссылки.</span><span class="sxs-lookup"><span data-stu-id="d64e8-124">The private link service connection.</span></span>

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

### <span data-ttu-id="d64e8-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d64e8-125">-ResourceGroupName</span></span>
<span data-ttu-id="d64e8-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d64e8-126">The resource group name.</span></span>

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

### <span data-ttu-id="d64e8-127">-Подсеть</span><span class="sxs-lookup"><span data-stu-id="d64e8-127">-Subnet</span></span>
<span data-ttu-id="d64e8-128">Подсеть частной конечной точки</span><span class="sxs-lookup"><span data-stu-id="d64e8-128">The subnet of the private endpoint</span></span>

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

### <span data-ttu-id="d64e8-129">-Тег</span><span class="sxs-lookup"><span data-stu-id="d64e8-129">-Tag</span></span>
<span data-ttu-id="d64e8-130">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="d64e8-130">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="d64e8-131">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="d64e8-131">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="d64e8-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d64e8-132">-Confirm</span></span>
<span data-ttu-id="d64e8-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d64e8-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d64e8-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d64e8-134">-WhatIf</span></span>
<span data-ttu-id="d64e8-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d64e8-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d64e8-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d64e8-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d64e8-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d64e8-137">CommonParameters</span></span>
<span data-ttu-id="d64e8-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d64e8-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d64e8-139">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d64e8-139">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d64e8-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d64e8-140">INPUTS</span></span>

### <span data-ttu-id="d64e8-141">System. String</span><span class="sxs-lookup"><span data-stu-id="d64e8-141">System.String</span></span>

### <span data-ttu-id="d64e8-142">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="d64e8-142">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="d64e8-143">Microsoft. Azure. Commands. Network. Models. PSPrivateLinkServiceConnection []</span><span class="sxs-lookup"><span data-stu-id="d64e8-143">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceConnection[]</span></span>

## <span data-ttu-id="d64e8-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d64e8-144">OUTPUTS</span></span>

### <span data-ttu-id="d64e8-145">Microsoft. Azure. Commands. Network. Models. PSPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="d64e8-145">Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint</span></span>

## <span data-ttu-id="d64e8-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="d64e8-146">NOTES</span></span>

## <span data-ttu-id="d64e8-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d64e8-147">RELATED LINKS</span></span>

[<span data-ttu-id="d64e8-148">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="d64e8-148">Get-AzPrivateEndpoint</span></span>](./Get-AzPrivateEndpoint.md)

[<span data-ttu-id="d64e8-149">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="d64e8-149">Remove-AzPrivateEndpoint</span></span>](./Remove-AzPrivateEndpoint.md)

[<span data-ttu-id="d64e8-150">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="d64e8-150">New-AzPrivateLinkServiceConnection</span></span>](./New-AzPrivateLinkServiceConnection.md)
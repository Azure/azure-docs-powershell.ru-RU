---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/new-azdatabricksvnetpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/New-AzDatabricksVNetPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/New-AzDatabricksVNetPeering.md
ms.openlocfilehash: f1af71bd2c05f2b1219a3ad7f1f09eb2f9560ad4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94077812"
---
# <span data-ttu-id="c44f1-101">New-AzDatabricksVNetPeering</span><span class="sxs-lookup"><span data-stu-id="c44f1-101">New-AzDatabricksVNetPeering</span></span>

## <span data-ttu-id="c44f1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c44f1-102">SYNOPSIS</span></span>
<span data-ttu-id="c44f1-103">Создает одноранговую сеть vNet для рабочей области.</span><span class="sxs-lookup"><span data-stu-id="c44f1-103">Creates vNet Peering for workspace.</span></span>

## <span data-ttu-id="c44f1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c44f1-104">SYNTAX</span></span>

```
New-AzDatabricksVNetPeering -Name <String> -ResourceGroupName <String> -WorkspaceName <String>
 [-SubscriptionId <String>] [-AllowForwardedTraffic] [-AllowGatewayTransit] [-AllowVirtualNetworkAccess]
 [-DatabricksAddressSpacePrefix <String[]>] [-DatabricksVirtualNetworkId <String>]
 [-RemoteAddressSpacePrefix <String[]>] [-RemoteVirtualNetworkId <String>] [-UseRemoteGateway]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c44f1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c44f1-105">DESCRIPTION</span></span>
<span data-ttu-id="c44f1-106">Создает одноранговую сеть vNet для рабочей области.</span><span class="sxs-lookup"><span data-stu-id="c44f1-106">Creates vNet Peering for workspace.</span></span>

## <span data-ttu-id="c44f1-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c44f1-107">EXAMPLES</span></span>

### <span data-ttu-id="c44f1-108">Пример 1: создание однорангового соединения vnet для кирпичей</span><span class="sxs-lookup"><span data-stu-id="c44f1-108">Example 1: Create a vnet peering for databricks</span></span>
```powershell
PS C:\> New-AzDatabricksVNetPeering -Name vnetpeering-t01 -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test -RemoteVirtualNetworkId '/subscriptions/xxxxxx-xxxx-xxx-xxx/resourceGroups/azure-manual-test/providers/Microsoft.Network/virtualNetworks/vnet-test01'

Name            Type
----            ----
vnetpeering-t01
```

<span data-ttu-id="c44f1-109">Эта команда создает одноранговый элемент vnet для кирпичей.</span><span class="sxs-lookup"><span data-stu-id="c44f1-109">This command creates a vnet peering for databricks.</span></span>

## <span data-ttu-id="c44f1-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c44f1-110">PARAMETERS</span></span>

### <span data-ttu-id="c44f1-111">-AllowForwardedTraffic</span><span class="sxs-lookup"><span data-stu-id="c44f1-111">-AllowForwardedTraffic</span></span>
<span data-ttu-id="c44f1-112">Будет ли переадресованный трафик из виртуальных машин в локальной виртуальной сети разрешен и запрещен в удаленной виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="c44f1-112">Whether the forwarded traffic from the VMs in the local virtual network will be allowed/disallowed in remote virtual network.</span></span>

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

### <span data-ttu-id="c44f1-113">-AllowGatewayTransit</span><span class="sxs-lookup"><span data-stu-id="c44f1-113">-AllowGatewayTransit</span></span>
<span data-ttu-id="c44f1-114">Если вы можете использовать ссылки на шлюзы в удаленных виртуальных сетях, чтобы добавить ссылку на эту виртуальную сеть.</span><span class="sxs-lookup"><span data-stu-id="c44f1-114">If gateway links can be used in remote virtual networking to link to this virtual network.</span></span>

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

### <span data-ttu-id="c44f1-115">-AllowVirtualNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="c44f1-115">-AllowVirtualNetworkAccess</span></span>
<span data-ttu-id="c44f1-116">Смогут ли виртуальные машины в локальной виртуальной сети иметь доступ к виртуальным машинам в удаленной виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="c44f1-116">Whether the VMs in the local virtual network space would be able to access the VMs in remote virtual network space.</span></span>

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

### <span data-ttu-id="c44f1-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c44f1-117">-AsJob</span></span>
<span data-ttu-id="c44f1-118">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="c44f1-118">Run the command as a job</span></span>

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

### <span data-ttu-id="c44f1-119">-DatabricksAddressSpacePrefix</span><span class="sxs-lookup"><span data-stu-id="c44f1-119">-DatabricksAddressSpacePrefix</span></span>
<span data-ttu-id="c44f1-120">Список блоков адресов, зарезервированных для этой виртуальной сети в нотации CIDR.</span><span class="sxs-lookup"><span data-stu-id="c44f1-120">A list of address blocks reserved for this virtual network in CIDR notation.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c44f1-121">-DatabricksVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="c44f1-121">-DatabricksVirtualNetworkId</span></span>
<span data-ttu-id="c44f1-122">Идентификатор виртуальной сети данных о модулях данных.</span><span class="sxs-lookup"><span data-stu-id="c44f1-122">The Id of the databricks virtual network.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c44f1-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c44f1-123">-DefaultProfile</span></span>
<span data-ttu-id="c44f1-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c44f1-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c44f1-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c44f1-125">-Name</span></span>
<span data-ttu-id="c44f1-126">Имя одноранговой сети виртуальной среды.</span><span class="sxs-lookup"><span data-stu-id="c44f1-126">The name of the workspace vNet peering.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c44f1-127">-Wait</span><span class="sxs-lookup"><span data-stu-id="c44f1-127">-NoWait</span></span>
<span data-ttu-id="c44f1-128">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="c44f1-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c44f1-129">-RemoteAddressSpacePrefix</span><span class="sxs-lookup"><span data-stu-id="c44f1-129">-RemoteAddressSpacePrefix</span></span>
<span data-ttu-id="c44f1-130">Список блоков адресов, зарезервированных для этой виртуальной сети в нотации CIDR.</span><span class="sxs-lookup"><span data-stu-id="c44f1-130">A list of address blocks reserved for this virtual network in CIDR notation.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c44f1-131">-RemoteVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="c44f1-131">-RemoteVirtualNetworkId</span></span>
<span data-ttu-id="c44f1-132">Идентификатор удаленной виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="c44f1-132">The Id of the remote virtual network.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c44f1-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c44f1-133">-ResourceGroupName</span></span>
<span data-ttu-id="c44f1-134">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c44f1-134">The name of the resource group.</span></span>
<span data-ttu-id="c44f1-135">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="c44f1-135">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c44f1-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c44f1-136">-SubscriptionId</span></span>
<span data-ttu-id="c44f1-137">Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="c44f1-137">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c44f1-138">-UseRemoteGateway</span><span class="sxs-lookup"><span data-stu-id="c44f1-138">-UseRemoteGateway</span></span>
<span data-ttu-id="c44f1-139">Если удаленные шлюзы можно использовать в этой виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="c44f1-139">If remote gateways can be used on this virtual network.</span></span>
<span data-ttu-id="c44f1-140">Если флаг имеет значение true, а allowGatewayTransit на удаленном одноранговом соединении также имеет значение true, виртуальная сеть будет использовать шлюзы удаленной виртуальной сети для транзита.</span><span class="sxs-lookup"><span data-stu-id="c44f1-140">If the flag is set to true, and allowGatewayTransit on remote peering is also true, virtual network will use gateways of remote virtual network for transit.</span></span>
<span data-ttu-id="c44f1-141">Этот флаг может иметь значение true только для одного однорангового элемента.</span><span class="sxs-lookup"><span data-stu-id="c44f1-141">Only one peering can have this flag set to true.</span></span>
<span data-ttu-id="c44f1-142">Этот флаг не может быть установлен, если у виртуальной сети уже есть шлюз.</span><span class="sxs-lookup"><span data-stu-id="c44f1-142">This flag cannot be set if virtual network already has a gateway.</span></span>

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

### <span data-ttu-id="c44f1-143">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c44f1-143">-WorkspaceName</span></span>
<span data-ttu-id="c44f1-144">Имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="c44f1-144">The name of the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c44f1-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c44f1-145">-Confirm</span></span>
<span data-ttu-id="c44f1-146">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c44f1-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c44f1-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c44f1-147">-WhatIf</span></span>
<span data-ttu-id="c44f1-148">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c44f1-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c44f1-149">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c44f1-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c44f1-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c44f1-150">CommonParameters</span></span>
<span data-ttu-id="c44f1-151">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c44f1-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c44f1-152">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c44f1-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c44f1-153">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c44f1-153">INPUTS</span></span>

## <span data-ttu-id="c44f1-154">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c44f1-154">OUTPUTS</span></span>

### <span data-ttu-id="c44f1-155">Microsoft. Azure. PowerShell. командлеты. кирпичи. Api20180401. IVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="c44f1-155">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IVirtualNetworkPeering</span></span>

## <span data-ttu-id="c44f1-156">Пуск</span><span class="sxs-lookup"><span data-stu-id="c44f1-156">NOTES</span></span>

<span data-ttu-id="c44f1-157">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="c44f1-157">ALIASES</span></span>

## <span data-ttu-id="c44f1-158">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c44f1-158">RELATED LINKS</span></span>


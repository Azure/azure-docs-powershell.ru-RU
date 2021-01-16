---
external help file: Az.StackHCI-help.xml
Module Name: Az.StackHCI
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackhci/unregister-azstackhci
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Unregister-AzStackHCI.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Unregister-AzStackHCI.md
ms.openlocfilehash: e063af1a489c9e68845f087e339f42de65281501
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98418887"
---
# <span data-ttu-id="56917-101">Unregister-AzStackHCI</span><span class="sxs-lookup"><span data-stu-id="56917-101">Unregister-AzStackHCI</span></span>

## <span data-ttu-id="56917-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56917-102">SYNOPSIS</span></span>
<span data-ttu-id="56917-103">Unregister-AzStackHCI удаляет облачный ресурс Microsoft.AzureStackHCI, представляющий собой локальное кластерное решение, и отозвает регистрацию локального кластера с помощью Azure.</span><span class="sxs-lookup"><span data-stu-id="56917-103">Unregister-AzStackHCI deletes the Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and unregisters the on-premise cluster with Azure.</span></span>
<span data-ttu-id="56917-104">Зарегистрированные данные, доступные на кластере, используются для регистрации кластера, если параметры не были переданы.</span><span class="sxs-lookup"><span data-stu-id="56917-104">The registered information available on the cluster is used to unregister the cluster if no parameters are passed.</span></span>

## <span data-ttu-id="56917-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="56917-105">SYNTAX</span></span>

```
Unregister-AzStackHCI [[-SubscriptionId] <String>] [[-ResourceName] <String>] [[-TenantId] <String>]
 [[-ResourceGroupName] <String>] [[-ArmAccessToken] <String>] [[-GraphAccessToken] <String>]
 [[-AccountId] <String>] [[-EnvironmentName] <String>] [[-ComputerName] <String>] [-UseDeviceAuthentication]
 [[-Credential] <PSCredential>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56917-106">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="56917-106">DESCRIPTION</span></span>
<span data-ttu-id="56917-107">Unregister-AzStackHCI удаляет облачный ресурс Microsoft.AzureStackHCI, представляющий собой локальное кластерное решение, и отозвает регистрацию локального кластера с помощью Azure.</span><span class="sxs-lookup"><span data-stu-id="56917-107">Unregister-AzStackHCI deletes the Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and unregisters the on-premise cluster with Azure.</span></span>
<span data-ttu-id="56917-108">Зарегистрированные данные, доступные на кластере, используются для регистрации кластера, если параметры не были переданы.</span><span class="sxs-lookup"><span data-stu-id="56917-108">The registered information available on the cluster is used to unregister the cluster if no parameters are passed.</span></span>

## <span data-ttu-id="56917-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="56917-109">EXAMPLES</span></span>

### <span data-ttu-id="56917-110">ПРИМЕР 1</span><span class="sxs-lookup"><span data-stu-id="56917-110">EXAMPLE 1</span></span>
```
Invoking on one of the cluster node
```

<span data-ttu-id="56917-111">C:\PS \> Unregister-AzStackHCI Result: Success</span><span class="sxs-lookup"><span data-stu-id="56917-111">C:\PS\>Unregister-AzStackHCI Result: Success</span></span>

### <span data-ttu-id="56917-112">ПРИМЕР 2</span><span class="sxs-lookup"><span data-stu-id="56917-112">EXAMPLE 2</span></span>
```
Invoking from the management node
```

<span data-ttu-id="56917-113">C:\PS \> Unregister-AzStackHCI -ComputerName ClusterNode1 Result: Success</span><span class="sxs-lookup"><span data-stu-id="56917-113">C:\PS\>Unregister-AzStackHCI -ComputerName ClusterNode1 Result: Success</span></span>

### <span data-ttu-id="56917-114">ПРИМЕР 3</span><span class="sxs-lookup"><span data-stu-id="56917-114">EXAMPLE 3</span></span>
```
Invoking from WAC
```

<span data-ttu-id="56917-115">C:\PS \> Unregister-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ArmAccessToken etyer.. ere= -GraphAccessToken acyee.. rerrer -AccountId user1@corp1.com -ResourceName DemoHCICluster3 -ResourceGroupName DemoHCIRG -Confirm:$False Result: Success</span><span class="sxs-lookup"><span data-stu-id="56917-115">C:\PS\>Unregister-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ArmAccessToken etyer..ere= -GraphAccessToken acyee..rerrer -AccountId user1@corp1.com -ResourceName DemoHCICluster3 -ResourceGroupName DemoHCIRG -Confirm:$False Result: Success</span></span>

### <span data-ttu-id="56917-116">ПРИМЕР 4</span><span class="sxs-lookup"><span data-stu-id="56917-116">EXAMPLE 4</span></span>
```
Invoking with all the parameters
```

<span data-ttu-id="56917-117">C:\PS \> Unregister-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ResourceName HciCluster1 -TenantId "c31c0dbb-ce27-4c78-ad26-a5f717c14557" -ResourceGroupName HciClusterRG -ArmAccessToken eerrer.. ere= -GraphAccessToken acee.. rerrer -AccountId user1@corp1.com -EnvironmentName AzureCloud -ComputerName node1hci -Credential Get-Credential Result: Success</span><span class="sxs-lookup"><span data-stu-id="56917-117">C:\PS\>Unregister-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ResourceName HciCluster1 -TenantId "c31c0dbb-ce27-4c78-ad26-a5f717c14557" -ResourceGroupName HciClusterRG -ArmAccessToken eerrer..ere= -GraphAccessToken acee..rerrer -AccountId user1@corp1.com -EnvironmentName AzureCloud -ComputerName node1hci -Credential Get-Credential Result: Success</span></span>

## <span data-ttu-id="56917-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="56917-118">PARAMETERS</span></span>

### <span data-ttu-id="56917-119">-AccountId</span><span class="sxs-lookup"><span data-stu-id="56917-119">-AccountId</span></span>
<span data-ttu-id="56917-120">Определяет маркер ARM доступа.</span><span class="sxs-lookup"><span data-stu-id="56917-120">Specifies the ARM access token.</span></span>
<span data-ttu-id="56917-121">Это указание вместе с ArmAccessToken и GraphAccessToken позволит избежать интерактивного логотипа Azure.</span><span class="sxs-lookup"><span data-stu-id="56917-121">Specifying this along with ArmAccessToken and GraphAccessToken will avoid Azure interactive logon.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56917-122">-ArmAccessToken</span><span class="sxs-lookup"><span data-stu-id="56917-122">-ArmAccessToken</span></span>
<span data-ttu-id="56917-123">Определяет маркер ARM доступа.</span><span class="sxs-lookup"><span data-stu-id="56917-123">Specifies the ARM access token.</span></span>
<span data-ttu-id="56917-124">Если указать это вместе с GraphAccessToken и AccountId, это позволит избежать интерактивного логотипа Azure.</span><span class="sxs-lookup"><span data-stu-id="56917-124">Specifying this along with GraphAccessToken and AccountId will avoid Azure interactive logon.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56917-125">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="56917-125">-ComputerName</span></span>
<span data-ttu-id="56917-126">Указывает один из узлов кластера в локальном кластере, регистрируется в Azure.</span><span class="sxs-lookup"><span data-stu-id="56917-126">Specifies one of the cluster node in on-premise cluster that is being registered to Azure.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56917-127">-Credential</span><span class="sxs-lookup"><span data-stu-id="56917-127">-Credential</span></span>
<span data-ttu-id="56917-128">Определяет учетные данные для computerName.</span><span class="sxs-lookup"><span data-stu-id="56917-128">Specifies the credential for the ComputerName.</span></span>
<span data-ttu-id="56917-129">По умолчанию выполняется текущий пользователь, который выполняет cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56917-129">Default is the current user executing the Cmdlet.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56917-130">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="56917-130">-EnvironmentName</span></span>
<span data-ttu-id="56917-131">Указывает среду Azure.</span><span class="sxs-lookup"><span data-stu-id="56917-131">Specifies the Azure Environment.</span></span>
<span data-ttu-id="56917-132">По умолчанию это AzureCloud.</span><span class="sxs-lookup"><span data-stu-id="56917-132">Default is AzureCloud.</span></span>
<span data-ttu-id="56917-133">Допустимые значения: AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span><span class="sxs-lookup"><span data-stu-id="56917-133">Valid values are AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: $AzureCloud
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56917-134">-GraphAccessToken</span><span class="sxs-lookup"><span data-stu-id="56917-134">-GraphAccessToken</span></span>
<span data-ttu-id="56917-135">Определяет маркер доступа Graph.</span><span class="sxs-lookup"><span data-stu-id="56917-135">Specifies the Graph access token.</span></span>
<span data-ttu-id="56917-136">Это указание вместе с ArmAccessToken и AccountId позволит избежать интерактивного логотипа Azure.</span><span class="sxs-lookup"><span data-stu-id="56917-136">Specifying this along with ArmAccessToken and AccountId will avoid Azure interactive logon.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56917-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56917-137">-ResourceGroupName</span></span>
<span data-ttu-id="56917-138">Имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="56917-138">Specifies the Azure Resource Group name.</span></span>
<span data-ttu-id="56917-139">Если не указано , -rg будет использоваться в качестве имени \<LocalClusterName\> группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="56917-139">If not specified \<LocalClusterName\>-rg will be used as resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56917-140">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="56917-140">-ResourceName</span></span>
<span data-ttu-id="56917-141">Указывает имя ресурса, созданного в Azure.</span><span class="sxs-lookup"><span data-stu-id="56917-141">Specifies the resource name of the resource created in Azure.</span></span>
<span data-ttu-id="56917-142">Если не указано, используется название локального кластера.</span><span class="sxs-lookup"><span data-stu-id="56917-142">If not specified, on-premise cluster name is used.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56917-143">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="56917-143">-SubscriptionId</span></span>
<span data-ttu-id="56917-144">Указывает подписку Azure для создания ресурса.</span><span class="sxs-lookup"><span data-stu-id="56917-144">Specifies the Azure Subscription to create the resource</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56917-145">-TenantId</span><span class="sxs-lookup"><span data-stu-id="56917-145">-TenantId</span></span>
<span data-ttu-id="56917-146">Указывает Azure TenantId.</span><span class="sxs-lookup"><span data-stu-id="56917-146">Specifies the Azure TenantId.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56917-147">-UseDeviceAuthentication</span><span class="sxs-lookup"><span data-stu-id="56917-147">-UseDeviceAuthentication</span></span>
<span data-ttu-id="56917-148">Используйте проверку подлинности кода устройства вместо интерактивного запроса браузера.</span><span class="sxs-lookup"><span data-stu-id="56917-148">Use device code authentication instead of an interactive browser prompt.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56917-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="56917-149">-Confirm</span></span>
<span data-ttu-id="56917-150">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56917-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56917-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56917-151">-WhatIf</span></span>
<span data-ttu-id="56917-152">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56917-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56917-153">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="56917-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56917-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56917-154">CommonParameters</span></span>
<span data-ttu-id="56917-155">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56917-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56917-156">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="56917-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56917-157">INPUTS</span><span class="sxs-lookup"><span data-stu-id="56917-157">INPUTS</span></span>

## <span data-ttu-id="56917-158">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="56917-158">OUTPUTS</span></span>

### <span data-ttu-id="56917-159">PSCustomObject.</span><span class="sxs-lookup"><span data-stu-id="56917-159">PSCustomObject.</span></span> <span data-ttu-id="56917-160">Возвращает следующие свойства в PSCustomObject:</span><span class="sxs-lookup"><span data-stu-id="56917-160">Returns following Properties in PSCustomObject</span></span>
### <span data-ttu-id="56917-161">Результат: успешно, сбой или отмена.</span><span class="sxs-lookup"><span data-stu-id="56917-161">Result: Success or Failed or Cancelled.</span></span>
## <span data-ttu-id="56917-162">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="56917-162">NOTES</span></span>

## <span data-ttu-id="56917-163">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="56917-163">RELATED LINKS</span></span>

---
external help file: Az.StackHCI-help.xml
Module Name: Az.StackHCI
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackhci/unregister-azstackhci
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Unregister-AzStackHCI.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Unregister-AzStackHCI.md
ms.openlocfilehash: cc887fb8e41fd9464914144e7cbed5a332948228
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247192"
---
# <span data-ttu-id="ab608-101">Unregister-AzStackHCI</span><span class="sxs-lookup"><span data-stu-id="ab608-101">Unregister-AzStackHCI</span></span>

## <span data-ttu-id="ab608-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ab608-102">SYNOPSIS</span></span>
<span data-ttu-id="ab608-103">Unregister-AzStackHCI удаляет облачный ресурс Microsoft. AzureStackHCI, представляющий локальный кластер, и отменяет регистрацию локального кластера с помощью Azure.</span><span class="sxs-lookup"><span data-stu-id="ab608-103">Unregister-AzStackHCI deletes the Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and unregisters the on-premise cluster with Azure.</span></span>
<span data-ttu-id="ab608-104">Зарегистрированные данные, доступные в кластере, используются для отмены регистрации кластера, если не переданы никакие параметры.</span><span class="sxs-lookup"><span data-stu-id="ab608-104">The registered information available on the cluster is used to unregister the cluster if no parameters are passed.</span></span>

## <span data-ttu-id="ab608-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ab608-105">SYNTAX</span></span>

```
Unregister-AzStackHCI [[-SubscriptionId] <String>] [[-ResourceName] <String>] [[-TenantId] <String>]
 [[-ResourceGroupName] <String>] [[-ArmAccessToken] <String>] [[-GraphAccessToken] <String>]
 [[-AccountId] <String>] [[-EnvironmentName] <String>] [[-ComputerName] <String>]
 [[-Credential] <PSCredential>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ab608-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ab608-106">DESCRIPTION</span></span>
<span data-ttu-id="ab608-107">Unregister-AzStackHCI удаляет облачный ресурс Microsoft. AzureStackHCI, представляющий локальный кластер, и отменяет регистрацию локального кластера с помощью Azure.</span><span class="sxs-lookup"><span data-stu-id="ab608-107">Unregister-AzStackHCI deletes the Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and unregisters the on-premise cluster with Azure.</span></span>
<span data-ttu-id="ab608-108">Зарегистрированные данные, доступные в кластере, используются для отмены регистрации кластера, если не переданы никакие параметры.</span><span class="sxs-lookup"><span data-stu-id="ab608-108">The registered information available on the cluster is used to unregister the cluster if no parameters are passed.</span></span>

## <span data-ttu-id="ab608-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ab608-109">EXAMPLES</span></span>

### <span data-ttu-id="ab608-110">ПРИМЕР 1</span><span class="sxs-lookup"><span data-stu-id="ab608-110">EXAMPLE 1</span></span>
```
Invoking on one of the cluster node
```

<span data-ttu-id="ab608-111">\>Отмена регистрации C:\PS — результат AzStackHCI: успешное удаление</span><span class="sxs-lookup"><span data-stu-id="ab608-111">C:\PS\>Unregister-AzStackHCI Result: Success</span></span>

### <span data-ttu-id="ab608-112">ПРИМЕР 2</span><span class="sxs-lookup"><span data-stu-id="ab608-112">EXAMPLE 2</span></span>
```
Invoking from the management node
```

<span data-ttu-id="ab608-113">C:\PS \> Unregister-AzStackHCI-ComputerName ClusterNode1 результат: успешно</span><span class="sxs-lookup"><span data-stu-id="ab608-113">C:\PS\>Unregister-AzStackHCI -ComputerName ClusterNode1 Result: Success</span></span>

### <span data-ttu-id="ab608-114">ПРИМЕР 3</span><span class="sxs-lookup"><span data-stu-id="ab608-114">EXAMPLE 3</span></span>
```
Invoking from WAC
```

<span data-ttu-id="ab608-115">C:\PS \> Unregister-AzStackHCI-SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd"-ArmAccessToken etyer.. Ere =-GraphAccessToken acyee.. rerrer-AccountId user1@corp1.com -resourceName DemoHCICluster3-ResourceGroupName DemoHCIRG-Confirm: $false результат: успех</span><span class="sxs-lookup"><span data-stu-id="ab608-115">C:\PS\>Unregister-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ArmAccessToken etyer..ere= -GraphAccessToken acyee..rerrer -AccountId user1@corp1.com -ResourceName DemoHCICluster3 -ResourceGroupName DemoHCIRG -Confirm:$False Result: Success</span></span>

### <span data-ttu-id="ab608-116">ПРИМЕР 4</span><span class="sxs-lookup"><span data-stu-id="ab608-116">EXAMPLE 4</span></span>
```
Invoking with all the parameters
```

<span data-ttu-id="ab608-117">C:\PS \> Unregister-AzStackHCI-SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd"-resourceName HciCluster1-TenantId "c31c0dbb-ce27-4c78-ad26-a5f717c14557"-ResourceGroupName HciClusterRG.. Ere =-GraphAccessToken ACee.. rerrer-AccountId user1@corp1.com -EnvironmentName AzureCloud-ComputerName node1hci-credentials Get-Credential result: Success (успешно)</span><span class="sxs-lookup"><span data-stu-id="ab608-117">C:\PS\>Unregister-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ResourceName HciCluster1 -TenantId "c31c0dbb-ce27-4c78-ad26-a5f717c14557" -ResourceGroupName HciClusterRG -ArmAccessToken eerrer..ere= -GraphAccessToken acee..rerrer -AccountId user1@corp1.com -EnvironmentName AzureCloud -ComputerName node1hci -Credential Get-Credential Result: Success</span></span>

## <span data-ttu-id="ab608-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ab608-118">PARAMETERS</span></span>

### <span data-ttu-id="ab608-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ab608-119">-SubscriptionId</span></span>
<span data-ttu-id="ab608-120">Указывает подписку Azure для создания ресурса.</span><span class="sxs-lookup"><span data-stu-id="ab608-120">Specifies the Azure Subscription to create the resource</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab608-121">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="ab608-121">-ResourceName</span></span>
<span data-ttu-id="ab608-122">Указывает имя ресурса, созданного в Azure.</span><span class="sxs-lookup"><span data-stu-id="ab608-122">Specifies the resource name of the resource created in Azure.</span></span>
<span data-ttu-id="ab608-123">Если не указано, используется локальное имя кластера.</span><span class="sxs-lookup"><span data-stu-id="ab608-123">If not specified, on-premise cluster name is used.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab608-124">-TenantId</span><span class="sxs-lookup"><span data-stu-id="ab608-124">-TenantId</span></span>
<span data-ttu-id="ab608-125">Указывает Azure TenantId.</span><span class="sxs-lookup"><span data-stu-id="ab608-125">Specifies the Azure TenantId.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab608-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab608-126">-ResourceGroupName</span></span>
<span data-ttu-id="ab608-127">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="ab608-127">Specifies the Azure Resource Group name.</span></span>
<span data-ttu-id="ab608-128">Если не указано, \<LocalClusterName\> RG будет использоваться в качестве имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ab608-128">If not specified \<LocalClusterName\>-rg will be used as resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab608-129">-ArmAccessToken</span><span class="sxs-lookup"><span data-stu-id="ab608-129">-ArmAccessToken</span></span>
<span data-ttu-id="ab608-130">Указывает маркер доступа ARM.</span><span class="sxs-lookup"><span data-stu-id="ab608-130">Specifies the ARM access token.</span></span>
<span data-ttu-id="ab608-131">Указав этот параметр вместе с GraphAccessToken и AccountId, вы не сможете интерактивно войти в Azure.</span><span class="sxs-lookup"><span data-stu-id="ab608-131">Specifying this along with GraphAccessToken and AccountId will avoid Azure interactive logon.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab608-132">-GraphAccessToken</span><span class="sxs-lookup"><span data-stu-id="ab608-132">-GraphAccessToken</span></span>
<span data-ttu-id="ab608-133">Указывает маркер доступа Graph.</span><span class="sxs-lookup"><span data-stu-id="ab608-133">Specifies the Graph access token.</span></span>
<span data-ttu-id="ab608-134">Указав этот параметр вместе с ArmAccessToken и AccountId, вы не сможете интерактивно войти в Azure.</span><span class="sxs-lookup"><span data-stu-id="ab608-134">Specifying this along with ArmAccessToken and AccountId will avoid Azure interactive logon.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab608-135">-AccountId</span><span class="sxs-lookup"><span data-stu-id="ab608-135">-AccountId</span></span>
<span data-ttu-id="ab608-136">Указывает маркер доступа ARM.</span><span class="sxs-lookup"><span data-stu-id="ab608-136">Specifies the ARM access token.</span></span>
<span data-ttu-id="ab608-137">Если указать этот параметр вместе с ArmAccessToken и GraphAccessToken, вы не сможете интерактивно войти в Azure.</span><span class="sxs-lookup"><span data-stu-id="ab608-137">Specifying this along with ArmAccessToken and GraphAccessToken will avoid Azure interactive logon.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab608-138">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="ab608-138">-EnvironmentName</span></span>
<span data-ttu-id="ab608-139">Указывает среду Azure.</span><span class="sxs-lookup"><span data-stu-id="ab608-139">Specifies the Azure Environment.</span></span>
<span data-ttu-id="ab608-140">По умолчанию используется AzureCloud.</span><span class="sxs-lookup"><span data-stu-id="ab608-140">Default is AzureCloud.</span></span>
<span data-ttu-id="ab608-141">Допустимые значения — AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span><span class="sxs-lookup"><span data-stu-id="ab608-141">Valid values are AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: $AzureCloud
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab608-142">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="ab608-142">-ComputerName</span></span>
<span data-ttu-id="ab608-143">Указывает один из узлов кластера в локальном кластере, который регистрируется в Azure.</span><span class="sxs-lookup"><span data-stu-id="ab608-143">Specifies one of the cluster node in on-premise cluster that is being registered to Azure.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab608-144">-Credential</span><span class="sxs-lookup"><span data-stu-id="ab608-144">-Credential</span></span>
<span data-ttu-id="ab608-145">Указывает учетные данные для ComputerName.</span><span class="sxs-lookup"><span data-stu-id="ab608-145">Specifies the credential for the ComputerName.</span></span>
<span data-ttu-id="ab608-146">По умолчанию — текущий пользователь, выполняющий командлет.</span><span class="sxs-lookup"><span data-stu-id="ab608-146">Default is the current user executing the Cmdlet.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab608-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab608-147">-WhatIf</span></span>
<span data-ttu-id="ab608-148">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ab608-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab608-149">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ab608-149">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab608-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ab608-150">-Confirm</span></span>
<span data-ttu-id="ab608-151">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ab608-151">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab608-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab608-152">CommonParameters</span></span>
<span data-ttu-id="ab608-153">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ab608-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab608-154">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ab608-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab608-155">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ab608-155">INPUTS</span></span>

## <span data-ttu-id="ab608-156">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ab608-156">OUTPUTS</span></span>

### <span data-ttu-id="ab608-157">PSCustomObject.</span><span class="sxs-lookup"><span data-stu-id="ab608-157">PSCustomObject.</span></span> <span data-ttu-id="ab608-158">Возвращает следующие свойства в PSCustomObject</span><span class="sxs-lookup"><span data-stu-id="ab608-158">Returns following Properties in PSCustomObject</span></span>
### <span data-ttu-id="ab608-159">Результат: "успешно" или "не пройден" или "отменено".</span><span class="sxs-lookup"><span data-stu-id="ab608-159">Result: Success or Failed or Cancelled.</span></span>
## <span data-ttu-id="ab608-160">Пуск</span><span class="sxs-lookup"><span data-stu-id="ab608-160">NOTES</span></span>

## <span data-ttu-id="ab608-161">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ab608-161">RELATED LINKS</span></span>

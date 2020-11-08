---
external help file: Az.StackHCI-help.xml
Module Name: Az.StackHCI
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackhci/register-azstackhci
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Register-AzStackHCI.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Register-AzStackHCI.md
ms.openlocfilehash: c09c4b4c8d71d90bbbac0771c75ea3ea51ee05dc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243191"
---
# <span data-ttu-id="46f3c-101">Register-AzStackHCI</span><span class="sxs-lookup"><span data-stu-id="46f3c-101">Register-AzStackHCI</span></span>

## <span data-ttu-id="46f3c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="46f3c-102">SYNOPSIS</span></span>
<span data-ttu-id="46f3c-103">Register-AzStackHCI создает облачный ресурс Microsoft. AzureStackHCI, представляющий локальный кластер, и регистрирует локальный кластер с помощью Azure.</span><span class="sxs-lookup"><span data-stu-id="46f3c-103">Register-AzStackHCI creates a Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and registers the on-premise cluster with Azure.</span></span>

## <span data-ttu-id="46f3c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="46f3c-104">SYNTAX</span></span>

```
Register-AzStackHCI [-SubscriptionId] <String> [[-Region] <String>] [[-ResourceName] <String>]
 [[-TenantId] <String>] [[-ResourceGroupName] <String>] [[-ArmAccessToken] <String>]
 [[-GraphAccessToken] <String>] [[-AccountId] <String>] [[-EnvironmentName] <String>]
 [[-ComputerName] <String>] [[-Credential] <PSCredential>] [<CommonParameters>]
```

## <span data-ttu-id="46f3c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="46f3c-105">DESCRIPTION</span></span>
<span data-ttu-id="46f3c-106">Register-AzStackHCI создает облачный ресурс Microsoft. AzureStackHCI, представляющий локальный кластер, и регистрирует локальный кластер с помощью Azure.</span><span class="sxs-lookup"><span data-stu-id="46f3c-106">Register-AzStackHCI creates a Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and registers the on-premise cluster with Azure.</span></span>

## <span data-ttu-id="46f3c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="46f3c-107">EXAMPLES</span></span>

### <span data-ttu-id="46f3c-108">ПРИМЕР 1</span><span class="sxs-lookup"><span data-stu-id="46f3c-108">EXAMPLE 1</span></span>
```
Invoking on one of the cluster node.
```

<span data-ttu-id="46f3c-109">C:\PS \> Register-AzStackHCI-SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" результат: ИД ресурса успешно:/Subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster1-RG/providers/Microsoft.AzureStackHCI/Clusters/DemoHCICluster1 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster1-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster1/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/980be58d-578c-4cff-b4cd-43e9c3a77826/isMSAApp/</span><span class="sxs-lookup"><span data-stu-id="46f3c-109">C:\PS\>Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" Result: Success ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster1-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster1 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster1-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster1/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/980be58d-578c-4cff-b4cd-43e9c3a77826/isMSAApp/</span></span>

### <span data-ttu-id="46f3c-110">ПРИМЕР 2</span><span class="sxs-lookup"><span data-stu-id="46f3c-110">EXAMPLE 2</span></span>
```
Invoking from the management node
```

<span data-ttu-id="46f3c-111">C:\PS \> Register-AzStackHCI-SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd"-имя_компьютера ClusterNode1 результат: ИД ResourceId:/Subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster2-RG/providers/Microsoft.AzureStackHCI/Clusters/DemoHCICluster2 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster2-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster2/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/950be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span><span class="sxs-lookup"><span data-stu-id="46f3c-111">C:\PS\>Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ComputerName ClusterNode1 Result: Success ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster2-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster2 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster2-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster2/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/950be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span></span>

### <span data-ttu-id="46f3c-112">ПРИМЕР 3</span><span class="sxs-lookup"><span data-stu-id="46f3c-112">EXAMPLE 3</span></span>
```
Invoking from WAC
```

<span data-ttu-id="46f3c-113">C:\PS \> Register-AzStackHCI-SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd"-ArmAccessToken etyer.. Ere =-GraphAccessToken acyee.. rerrer-AccountId user1@corp1.com -Region westus-resourceName DemoHCICluster3-ResourceGroupName DemoHCIRG result: PendingForAdminConsent ResourceId:/Subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCIRG/providers/Microsoft.AzureStackHCI/Clusters/DemoHCICluster3 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCIRG/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster3/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/980be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span><span class="sxs-lookup"><span data-stu-id="46f3c-113">C:\PS\>Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ArmAccessToken etyer..ere= -GraphAccessToken acyee..rerrer -AccountId user1@corp1.com -Region westus -ResourceName DemoHCICluster3 -ResourceGroupName DemoHCIRG Result: PendingForAdminConsent ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCIRG/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster3 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCIRG/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster3/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/980be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span></span>

### <span data-ttu-id="46f3c-114">ПРИМЕР 4</span><span class="sxs-lookup"><span data-stu-id="46f3c-114">EXAMPLE 4</span></span>
```
Invoking with all the parameters
```

<span data-ttu-id="46f3c-115">C:\PS \> Register-AzStackHCI-SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd"-Region westus-resourceName HciCluster1-TenantId "c31c0dbb-ce27-4c78-ad26-a5f717c14557"-ResourceGroupName HciClusterRG-ArmAccessToken eerrer.. Ere =-GraphAccessToken ACee.. rerrer-AccountId user1@corp1.com -EnvironmentName AzureCloud-ComputerName node1hci-Credential Get-Credential результат: ИД ResourceId:/Subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/HciClusterRG/providers/Microsoft.AzureStackHCI/Clusters/HciCluster1 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/HciClusterRG/providers/Microsoft.AzureStackHCI/clusters/HciCluster1/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/990be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span><span class="sxs-lookup"><span data-stu-id="46f3c-115">C:\PS\>Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -Region westus -ResourceName HciCluster1 -TenantId "c31c0dbb-ce27-4c78-ad26-a5f717c14557" -ResourceGroupName HciClusterRG -ArmAccessToken eerrer..ere= -GraphAccessToken acee..rerrer -AccountId user1@corp1.com -EnvironmentName AzureCloud -ComputerName node1hci -Credential Get-Credential Result: Success ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/HciClusterRG/providers/Microsoft.AzureStackHCI/clusters/HciCluster1 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/HciClusterRG/providers/Microsoft.AzureStackHCI/clusters/HciCluster1/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/990be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span></span>

## <span data-ttu-id="46f3c-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="46f3c-116">PARAMETERS</span></span>

### <span data-ttu-id="46f3c-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="46f3c-117">-SubscriptionId</span></span>
<span data-ttu-id="46f3c-118">Указывает подписку Azure для создания ресурса.</span><span class="sxs-lookup"><span data-stu-id="46f3c-118">Specifies the Azure Subscription to create the resource.</span></span>
<span data-ttu-id="46f3c-119">Это единственный обязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="46f3c-119">This is the only Mandatory parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46f3c-120">-Region (регион)</span><span class="sxs-lookup"><span data-stu-id="46f3c-120">-Region</span></span>
<span data-ttu-id="46f3c-121">Указывает регион для создания ресурса.</span><span class="sxs-lookup"><span data-stu-id="46f3c-121">Specifies the Region to create the resource.</span></span>
<span data-ttu-id="46f3c-122">По умолчанию используется EastUS.</span><span class="sxs-lookup"><span data-stu-id="46f3c-122">Default is EastUS.</span></span>

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

### <span data-ttu-id="46f3c-123">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="46f3c-123">-ResourceName</span></span>
<span data-ttu-id="46f3c-124">Указывает имя ресурса, созданного в Azure.</span><span class="sxs-lookup"><span data-stu-id="46f3c-124">Specifies the resource name of the resource created in Azure.</span></span>
<span data-ttu-id="46f3c-125">Если не указано, используется локальное имя кластера.</span><span class="sxs-lookup"><span data-stu-id="46f3c-125">If not specified, on-premise cluster name is used.</span></span>

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

### <span data-ttu-id="46f3c-126">-TenantId</span><span class="sxs-lookup"><span data-stu-id="46f3c-126">-TenantId</span></span>
<span data-ttu-id="46f3c-127">Указывает Azure TenantId.</span><span class="sxs-lookup"><span data-stu-id="46f3c-127">Specifies the Azure TenantId.</span></span>

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

### <span data-ttu-id="46f3c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46f3c-128">-ResourceGroupName</span></span>
<span data-ttu-id="46f3c-129">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="46f3c-129">Specifies the Azure Resource Group name.</span></span>
<span data-ttu-id="46f3c-130">Если не указано, \<LocalClusterName\> RG будет использоваться в качестве имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="46f3c-130">If not specified \<LocalClusterName\>-rg will be used as resource group name.</span></span>

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

### <span data-ttu-id="46f3c-131">-ArmAccessToken</span><span class="sxs-lookup"><span data-stu-id="46f3c-131">-ArmAccessToken</span></span>
<span data-ttu-id="46f3c-132">Указывает маркер доступа ARM.</span><span class="sxs-lookup"><span data-stu-id="46f3c-132">Specifies the ARM access token.</span></span>
<span data-ttu-id="46f3c-133">Указав этот параметр вместе с GraphAccessToken и AccountId, вы не сможете интерактивно войти в Azure.</span><span class="sxs-lookup"><span data-stu-id="46f3c-133">Specifying this along with GraphAccessToken and AccountId will avoid Azure interactive logon.</span></span>

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

### <span data-ttu-id="46f3c-134">-GraphAccessToken</span><span class="sxs-lookup"><span data-stu-id="46f3c-134">-GraphAccessToken</span></span>
<span data-ttu-id="46f3c-135">Указывает маркер доступа Graph.</span><span class="sxs-lookup"><span data-stu-id="46f3c-135">Specifies the Graph access token.</span></span>
<span data-ttu-id="46f3c-136">Указав этот параметр вместе с ArmAccessToken и AccountId, вы не сможете интерактивно войти в Azure.</span><span class="sxs-lookup"><span data-stu-id="46f3c-136">Specifying this along with ArmAccessToken and AccountId will avoid Azure interactive logon.</span></span>

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

### <span data-ttu-id="46f3c-137">-AccountId</span><span class="sxs-lookup"><span data-stu-id="46f3c-137">-AccountId</span></span>
<span data-ttu-id="46f3c-138">Указывает маркер доступа ARM.</span><span class="sxs-lookup"><span data-stu-id="46f3c-138">Specifies the ARM access token.</span></span>
<span data-ttu-id="46f3c-139">Если указать этот параметр вместе с ArmAccessToken и GraphAccessToken, вы не сможете интерактивно войти в Azure.</span><span class="sxs-lookup"><span data-stu-id="46f3c-139">Specifying this along with ArmAccessToken and GraphAccessToken will avoid Azure interactive logon.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46f3c-140">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="46f3c-140">-EnvironmentName</span></span>
<span data-ttu-id="46f3c-141">Указывает среду Azure.</span><span class="sxs-lookup"><span data-stu-id="46f3c-141">Specifies the Azure Environment.</span></span>
<span data-ttu-id="46f3c-142">По умолчанию используется AzureCloud.</span><span class="sxs-lookup"><span data-stu-id="46f3c-142">Default is AzureCloud.</span></span>
<span data-ttu-id="46f3c-143">Допустимые значения — AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span><span class="sxs-lookup"><span data-stu-id="46f3c-143">Valid values are AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: $AzureCloud
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46f3c-144">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="46f3c-144">-ComputerName</span></span>
<span data-ttu-id="46f3c-145">Указывает имя кластера или один из узлов кластера в локальном кластере, который регистрируется в Azure.</span><span class="sxs-lookup"><span data-stu-id="46f3c-145">Specifies the cluster name or one of the cluster node in on-premise cluster that is being registered to Azure.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46f3c-146">-Credential</span><span class="sxs-lookup"><span data-stu-id="46f3c-146">-Credential</span></span>
<span data-ttu-id="46f3c-147">Указывает учетные данные для ComputerName.</span><span class="sxs-lookup"><span data-stu-id="46f3c-147">Specifies the credential for the ComputerName.</span></span>
<span data-ttu-id="46f3c-148">По умолчанию — текущий пользователь, выполняющий командлет.</span><span class="sxs-lookup"><span data-stu-id="46f3c-148">Default is the current user executing the Cmdlet.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46f3c-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46f3c-149">CommonParameters</span></span>
<span data-ttu-id="46f3c-150">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="46f3c-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46f3c-151">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="46f3c-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46f3c-152">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="46f3c-152">INPUTS</span></span>

## <span data-ttu-id="46f3c-153">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="46f3c-153">OUTPUTS</span></span>

### <span data-ttu-id="46f3c-154">PSCustomObject.</span><span class="sxs-lookup"><span data-stu-id="46f3c-154">PSCustomObject.</span></span> <span data-ttu-id="46f3c-155">Возвращает следующие свойства в PSCustomObject</span><span class="sxs-lookup"><span data-stu-id="46f3c-155">Returns following Properties in PSCustomObject</span></span>
### <span data-ttu-id="46f3c-156">Результат: успех или сбой или PendingForAdminConsent или отменен.</span><span class="sxs-lookup"><span data-stu-id="46f3c-156">Result: Success or Failed or PendingForAdminConsent or Cancelled.</span></span>
### <span data-ttu-id="46f3c-157">ResourceId: идентификатор ресурса ресурса, созданного в Azure.</span><span class="sxs-lookup"><span data-stu-id="46f3c-157">ResourceId: Resource ID of the resource created in Azure.</span></span>
### <span data-ttu-id="46f3c-158">PortalResourceURL: URL-адрес ресурса портала Azure.</span><span class="sxs-lookup"><span data-stu-id="46f3c-158">PortalResourceURL: Azure Portal Resource URL.</span></span>
### <span data-ttu-id="46f3c-159">PortalAADAppPermissionsURL: URL-адрес портала Azure на странице разрешений приложения AAD.</span><span class="sxs-lookup"><span data-stu-id="46f3c-159">PortalAADAppPermissionsURL: Azure Portal URL for AAD App permissions page.</span></span>
## <span data-ttu-id="46f3c-160">Пуск</span><span class="sxs-lookup"><span data-stu-id="46f3c-160">NOTES</span></span>

## <span data-ttu-id="46f3c-161">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="46f3c-161">RELATED LINKS</span></span>

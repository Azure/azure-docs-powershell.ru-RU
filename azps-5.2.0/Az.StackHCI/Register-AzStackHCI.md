---
external help file: Az.StackHCI-help.xml
Module Name: Az.StackHCI
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackhci/register-azstackhci
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Register-AzStackHCI.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Register-AzStackHCI.md
ms.openlocfilehash: ad9c09118252499f99708ae99d36ee9ba2418ff2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98404415"
---
# <span data-ttu-id="004cf-101">Register-AzStackHCI</span><span class="sxs-lookup"><span data-stu-id="004cf-101">Register-AzStackHCI</span></span>

## <span data-ttu-id="004cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="004cf-102">SYNOPSIS</span></span>
<span data-ttu-id="004cf-103">Register-AzStackHCI создает облачный ресурс Microsoft.AzureStackHCI, представляющий собой локальное кластерное решение, и регистрирует его в Azure.</span><span class="sxs-lookup"><span data-stu-id="004cf-103">Register-AzStackHCI creates a Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and registers the on-premise cluster with Azure.</span></span>

## <span data-ttu-id="004cf-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="004cf-104">SYNTAX</span></span>

```
Register-AzStackHCI [-SubscriptionId] <String> [[-Region] <String>] [[-ResourceName] <String>]
 [[-TenantId] <String>] [[-ResourceGroupName] <String>] [[-ArmAccessToken] <String>]
 [[-GraphAccessToken] <String>] [[-AccountId] <String>] [[-EnvironmentName] <String>]
 [[-ComputerName] <String>] [[-CertificateThumbprint] <String>] [-RepairRegistration]
 [-UseDeviceAuthentication] [[-Credential] <PSCredential>] [<CommonParameters>]
```

## <span data-ttu-id="004cf-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="004cf-105">DESCRIPTION</span></span>
<span data-ttu-id="004cf-106">Register-AzStackHCI создает облачный ресурс Microsoft.AzureStackHCI, представляющий собой локальное кластерное решение, и регистрирует его в Azure.</span><span class="sxs-lookup"><span data-stu-id="004cf-106">Register-AzStackHCI creates a Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and registers the on-premise cluster with Azure.</span></span>

## <span data-ttu-id="004cf-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="004cf-107">EXAMPLES</span></span>

### <span data-ttu-id="004cf-108">ПРИМЕР 1</span><span class="sxs-lookup"><span data-stu-id="004cf-108">EXAMPLE 1</span></span>
```
Invoking on one of the cluster node.
```

<span data-ttu-id="004cf-109">C:\PS \> Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" Result: Success ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster1-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster1 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster1-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster1/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/980be58d-578c-4cff-b4cd-43e9c3a77826/isMSAApp/</span><span class="sxs-lookup"><span data-stu-id="004cf-109">C:\PS\>Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" Result: Success ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster1-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster1 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster1-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster1/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/980be58d-578c-4cff-b4cd-43e9c3a77826/isMSAApp/</span></span>

### <span data-ttu-id="004cf-110">ПРИМЕР 2</span><span class="sxs-lookup"><span data-stu-id="004cf-110">EXAMPLE 2</span></span>
```
Invoking from the management node
```

<span data-ttu-id="004cf-111">C:\PS \> Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ComputerName ClusterNode1 Result: Success ResourceId: /subscriptions/12a0f531- 56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster2-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster2 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster2-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster2/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/950be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span><span class="sxs-lookup"><span data-stu-id="004cf-111">C:\PS\>Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ComputerName ClusterNode1 Result: Success ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster2-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster2 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster2-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster2/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/950be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span></span>

### <span data-ttu-id="004cf-112">ПРИМЕР 3</span><span class="sxs-lookup"><span data-stu-id="004cf-112">EXAMPLE 3</span></span>
```
Invoking from WAC
```

<span data-ttu-id="004cf-113">C:\PS \> Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ArmAccessToken etyer.. ere= -GraphAccessToken acyee.. rerrer -AccountId user1@corp1.com -Region westus -ResourceName DemoHCICluster3 -ResourceGroupName DemoHCIRG Result: PendingForAdminConsent ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCIRG/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster3 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCIRG/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster3/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/980be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span><span class="sxs-lookup"><span data-stu-id="004cf-113">C:\PS\>Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ArmAccessToken etyer..ere= -GraphAccessToken acyee..rerrer -AccountId user1@corp1.com -Region westus -ResourceName DemoHCICluster3 -ResourceGroupName DemoHCIRG Result: PendingForAdminConsent ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCIRG/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster3 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCIRG/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster3/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/980be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span></span>

### <span data-ttu-id="004cf-114">ПРИМЕР 4</span><span class="sxs-lookup"><span data-stu-id="004cf-114">EXAMPLE 4</span></span>
```
Invoking with all the parameters
```

<span data-ttu-id="004cf-115">C:\PS \> Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -Region westus -ResourceName HciCluster1 -TenantId "c31c0dbb-ce27-4c78-ad26-a5f717c14557" -ResourceGroupName HciClusterRG -ArmAccessToken eerrer.. ere= -GraphAccessToken acee.. rerrer -AccountId user1@corp1.com -EnvironmentName AzureCloud -ComputerName node1hci -Credential Get-Credential Result: Success ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/HciClusterRG/providers/Microsoft.AzureStackHCI/clusters/HciCluster1 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/HciClusterRG/providers/Microsoft.AzureStackHCI/clusters/HciCluster1/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/990be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span><span class="sxs-lookup"><span data-stu-id="004cf-115">C:\PS\>Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -Region westus -ResourceName HciCluster1 -TenantId "c31c0dbb-ce27-4c78-ad26-a5f717c14557" -ResourceGroupName HciClusterRG -ArmAccessToken eerrer..ere= -GraphAccessToken acee..rerrer -AccountId user1@corp1.com -EnvironmentName AzureCloud -ComputerName node1hci -Credential Get-Credential Result: Success ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/HciClusterRG/providers/Microsoft.AzureStackHCI/clusters/HciCluster1 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/HciClusterRG/providers/Microsoft.AzureStackHCI/clusters/HciCluster1/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/990be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span></span>

## <span data-ttu-id="004cf-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="004cf-116">PARAMETERS</span></span>

### <span data-ttu-id="004cf-117">-AccountId</span><span class="sxs-lookup"><span data-stu-id="004cf-117">-AccountId</span></span>
<span data-ttu-id="004cf-118">Определяет маркер ARM доступа.</span><span class="sxs-lookup"><span data-stu-id="004cf-118">Specifies the ARM access token.</span></span>
<span data-ttu-id="004cf-119">Это указание вместе с ArmAccessToken и GraphAccessToken позволит избежать интерактивного логотипа Azure.</span><span class="sxs-lookup"><span data-stu-id="004cf-119">Specifying this along with ArmAccessToken and GraphAccessToken will avoid Azure interactive logon.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="004cf-120">-ArmAccessToken</span><span class="sxs-lookup"><span data-stu-id="004cf-120">-ArmAccessToken</span></span>
<span data-ttu-id="004cf-121">Определяет маркер ARM доступа.</span><span class="sxs-lookup"><span data-stu-id="004cf-121">Specifies the ARM access token.</span></span>
<span data-ttu-id="004cf-122">Если указать это вместе с GraphAccessToken и AccountId, это позволит избежать интерактивного логотипа Azure.</span><span class="sxs-lookup"><span data-stu-id="004cf-122">Specifying this along with GraphAccessToken and AccountId will avoid Azure interactive logon.</span></span>

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

### <span data-ttu-id="004cf-123">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="004cf-123">-CertificateThumbprint</span></span>
<span data-ttu-id="004cf-124">Определяет эскиз сертификата, доступный на всех узлах.</span><span class="sxs-lookup"><span data-stu-id="004cf-124">Specifies the thumbprint of the certificate available on all the nodes.</span></span> <span data-ttu-id="004cf-125">Пользователь отвечает за управление сертификатом.</span><span class="sxs-lookup"><span data-stu-id="004cf-125">User is responsible for managing the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="004cf-126">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="004cf-126">-ComputerName</span></span>
<span data-ttu-id="004cf-127">Указывает имя кластера или одного из узлов кластера в локальном кластере, зарегистрированном в Azure.</span><span class="sxs-lookup"><span data-stu-id="004cf-127">Specifies the cluster name or one of the cluster node in on-premise cluster that is being registered to Azure.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="004cf-128">-Credential</span><span class="sxs-lookup"><span data-stu-id="004cf-128">-Credential</span></span>
<span data-ttu-id="004cf-129">Определяет учетные данные для computerName.</span><span class="sxs-lookup"><span data-stu-id="004cf-129">Specifies the credential for the ComputerName.</span></span>
<span data-ttu-id="004cf-130">По умолчанию выполняется текущий пользователь, который выполняет cmdlet.</span><span class="sxs-lookup"><span data-stu-id="004cf-130">Default is the current user executing the Cmdlet.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 12
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="004cf-131">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="004cf-131">-EnvironmentName</span></span>
<span data-ttu-id="004cf-132">Указывает среду Azure.</span><span class="sxs-lookup"><span data-stu-id="004cf-132">Specifies the Azure Environment.</span></span>
<span data-ttu-id="004cf-133">По умолчанию это AzureCloud.</span><span class="sxs-lookup"><span data-stu-id="004cf-133">Default is AzureCloud.</span></span>
<span data-ttu-id="004cf-134">Допустимые значения: AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span><span class="sxs-lookup"><span data-stu-id="004cf-134">Valid values are AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: $AzureCloud
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="004cf-135">-GraphAccessToken</span><span class="sxs-lookup"><span data-stu-id="004cf-135">-GraphAccessToken</span></span>
<span data-ttu-id="004cf-136">Определяет маркер доступа Graph.</span><span class="sxs-lookup"><span data-stu-id="004cf-136">Specifies the Graph access token.</span></span>
<span data-ttu-id="004cf-137">Это указание вместе с ArmAccessToken и AccountId позволит избежать интерактивного логотипа Azure.</span><span class="sxs-lookup"><span data-stu-id="004cf-137">Specifying this along with ArmAccessToken and AccountId will avoid Azure interactive logon.</span></span>

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

### <span data-ttu-id="004cf-138">-Регион</span><span class="sxs-lookup"><span data-stu-id="004cf-138">-Region</span></span>
<span data-ttu-id="004cf-139">Определяет регион, в который нужно создать ресурс.</span><span class="sxs-lookup"><span data-stu-id="004cf-139">Specifies the Region to create the resource.</span></span>
<span data-ttu-id="004cf-140">Значение по умолчанию — EastUS.</span><span class="sxs-lookup"><span data-stu-id="004cf-140">Default is EastUS.</span></span>

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

### <span data-ttu-id="004cf-141">-RepairRegistration</span><span class="sxs-lookup"><span data-stu-id="004cf-141">-RepairRegistration</span></span>
<span data-ttu-id="004cf-142">Восстановление текущей регистрации Azure Stack HCI с помощью облака.</span><span class="sxs-lookup"><span data-stu-id="004cf-142">Repair the current Azure Stack HCI registration with the cloud.</span></span> <span data-ttu-id="004cf-143">Этот cmdlet удаляет локальные сертификаты на узлах с кластером и удаленные сертификаты в приложении Azure AD в облаке и создает новые сертификаты на замену для обоих.</span><span class="sxs-lookup"><span data-stu-id="004cf-143">This cmdlet deletes the local certificates on the clustered nodes and the remote certificates in the Azure AD application in the cloud and generates new replacement certificates for both.</span></span> <span data-ttu-id="004cf-144">Сохраняется группа ресурсов, название ресурса и другие варианты регистрации.</span><span class="sxs-lookup"><span data-stu-id="004cf-144">The resource group, resource name, and other registration choices are preserved.</span></span>

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

### <span data-ttu-id="004cf-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="004cf-145">-ResourceGroupName</span></span>
<span data-ttu-id="004cf-146">Имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="004cf-146">Specifies the Azure Resource Group name.</span></span>
<span data-ttu-id="004cf-147">Если не указано , -rg будет использоваться в качестве имени \<LocalClusterName\> группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="004cf-147">If not specified \<LocalClusterName\>-rg will be used as resource group name.</span></span>

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

### <span data-ttu-id="004cf-148">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="004cf-148">-ResourceName</span></span>
<span data-ttu-id="004cf-149">Указывает имя ресурса, созданного в Azure.</span><span class="sxs-lookup"><span data-stu-id="004cf-149">Specifies the resource name of the resource created in Azure.</span></span>
<span data-ttu-id="004cf-150">Если не указано, используется название локального кластера.</span><span class="sxs-lookup"><span data-stu-id="004cf-150">If not specified, on-premise cluster name is used.</span></span>

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

### <span data-ttu-id="004cf-151">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="004cf-151">-SubscriptionId</span></span>
<span data-ttu-id="004cf-152">Указывает подписку Azure для создания ресурса.</span><span class="sxs-lookup"><span data-stu-id="004cf-152">Specifies the Azure Subscription to create the resource.</span></span>
<span data-ttu-id="004cf-153">Это единственный обязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="004cf-153">This is the only Mandatory parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="004cf-154">-TenantId</span><span class="sxs-lookup"><span data-stu-id="004cf-154">-TenantId</span></span>
<span data-ttu-id="004cf-155">Указывает Azure TenantId.</span><span class="sxs-lookup"><span data-stu-id="004cf-155">Specifies the Azure TenantId.</span></span>

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

### <span data-ttu-id="004cf-156">-UseDeviceAuthentication</span><span class="sxs-lookup"><span data-stu-id="004cf-156">-UseDeviceAuthentication</span></span>
<span data-ttu-id="004cf-157">Используйте проверку подлинности кода устройства вместо интерактивного запроса браузера.</span><span class="sxs-lookup"><span data-stu-id="004cf-157">Use device code authentication instead of an interactive browser prompt.</span></span>

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

### <span data-ttu-id="004cf-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="004cf-158">CommonParameters</span></span>
<span data-ttu-id="004cf-159">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="004cf-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="004cf-160">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="004cf-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="004cf-161">INPUTS</span><span class="sxs-lookup"><span data-stu-id="004cf-161">INPUTS</span></span>

## <span data-ttu-id="004cf-162">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="004cf-162">OUTPUTS</span></span>

### <span data-ttu-id="004cf-163">PSCustomObject.</span><span class="sxs-lookup"><span data-stu-id="004cf-163">PSCustomObject.</span></span> <span data-ttu-id="004cf-164">Возвращает следующие свойства в PSCustomObject:</span><span class="sxs-lookup"><span data-stu-id="004cf-164">Returns following Properties in PSCustomObject</span></span>
### <span data-ttu-id="004cf-165">Результат: успех, сбой, ожиданиеForAdminConsent или Отменено.</span><span class="sxs-lookup"><span data-stu-id="004cf-165">Result: Success or Failed or PendingForAdminConsent or Cancelled.</span></span>
### <span data-ttu-id="004cf-166">ResourceId: ИД ресурса, созданного в Azure.</span><span class="sxs-lookup"><span data-stu-id="004cf-166">ResourceId: Resource ID of the resource created in Azure.</span></span>
### <span data-ttu-id="004cf-167">PortalResourceURL: URL-адрес ресурса портала Azure.</span><span class="sxs-lookup"><span data-stu-id="004cf-167">PortalResourceURL: Azure Portal Resource URL.</span></span>
### <span data-ttu-id="004cf-168">PortalAADAppPermissionsURL: URL-адрес портала Azure для страницы разрешений приложения AAD.</span><span class="sxs-lookup"><span data-stu-id="004cf-168">PortalAADAppPermissionsURL: Azure Portal URL for AAD App permissions page.</span></span>
## <span data-ttu-id="004cf-169">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="004cf-169">NOTES</span></span>

## <span data-ttu-id="004cf-170">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="004cf-170">RELATED LINKS</span></span>

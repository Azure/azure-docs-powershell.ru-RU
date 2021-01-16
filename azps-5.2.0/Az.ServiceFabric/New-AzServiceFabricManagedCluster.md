---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/new-azservicefabricmanagedcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricManagedCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricManagedCluster.md
ms.openlocfilehash: 9dd54f0f1ca56a8bedf3550e238a4308b519925d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98417508"
---
# <span data-ttu-id="1797f-101">New-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="1797f-101">New-AzServiceFabricManagedCluster</span></span>

## <span data-ttu-id="1797f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1797f-102">SYNOPSIS</span></span>
<span data-ttu-id="1797f-103">Создание нового управляемого кластера.</span><span class="sxs-lookup"><span data-stu-id="1797f-103">Create new managed cluster.</span></span>

## <span data-ttu-id="1797f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1797f-104">SYNTAX</span></span>

### <span data-ttu-id="1797f-105">ClientCertByTp (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1797f-105">ClientCertByTp (Default)</span></span>
```
New-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-Name] <String> -Location <String>
 [-UpgradeMode <ClusterUpgradeMode>] [-CodeVersion <String>] [-ClientCertIsAdmin]
 -ClientCertThumbprint <String> -AdminPassword <SecureString> [-AdminUserName <String>]
 [-HttpGatewayConnectionPort <Int32>] [-ClientConnectionPort <Int32>] [-DnsName <String>]
 [-ReverseProxyEndpointPort <Int32>] [-Sku <ManagedClusterSku>] [-UseTestExtension] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1797f-106">ClientCertByCn</span><span class="sxs-lookup"><span data-stu-id="1797f-106">ClientCertByCn</span></span>
```
New-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-Name] <String> -Location <String>
 [-UpgradeMode <ClusterUpgradeMode>] [-CodeVersion <String>] [-ClientCertIsAdmin]
 -ClientCertCommonName <String> [-ClientCertIssuerThumbprint <String[]>] -AdminPassword <SecureString>
 [-AdminUserName <String>] [-HttpGatewayConnectionPort <Int32>] [-ClientConnectionPort <Int32>]
 [-DnsName <String>] [-ReverseProxyEndpointPort <Int32>] [-Sku <ManagedClusterSku>] [-UseTestExtension]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1797f-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1797f-107">DESCRIPTION</span></span>
<span data-ttu-id="1797f-108">Этот cmdlet создаст управляемый ресурс кластера без типов узлов.</span><span class="sxs-lookup"><span data-stu-id="1797f-108">This cmdlet will create a managed cluster resource without node types.</span></span> <span data-ttu-id="1797f-109">Чтобы bootstrap the cluster A primary node type needs to be added use [New-AzServiceFabricManagedNodeType.](./New-AzServiceFabricManagedNodeType.md)</span><span class="sxs-lookup"><span data-stu-id="1797f-109">To bootstrap the cluster A primary node type needs to be added use [New-AzServiceFabricManagedNodeType](./New-AzServiceFabricManagedNodeType.md).</span></span>

## <span data-ttu-id="1797f-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1797f-110">EXAMPLES</span></span>

### <span data-ttu-id="1797f-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1797f-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$password = ConvertTo-SecureString -AsPlainText -Force "testpass1234!@#$"
New-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Location centraluseuap -ClusterName $clusterName -AdminPassword $password -Verbose
```

<span data-ttu-id="1797f-112">Эта команда создает ресурс кластера со стандартными базовыми SKU.</span><span class="sxs-lookup"><span data-stu-id="1797f-112">This command creates a cluster resource with default basic sku.</span></span>

### <span data-ttu-id="1797f-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="1797f-113">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$password = ConvertTo-SecureString -AsPlainText -Force "testpass1234!@#$"
New-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Location centraluseuap -ClusterName $clusterName -ClientCertThumbprint XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX -ClientCertIsAdmin -AdminPassword $password -Sku Standard -Verbose
```

<span data-ttu-id="1797f-114">Эта команда создает ресурс кластера в центральнойuseuap с первоначальным сертификатом клиента администрирования и стандартным SKU.</span><span class="sxs-lookup"><span data-stu-id="1797f-114">This command creates a cluster resource in centraluseuap with an initial admin client certificate and standard sku.</span></span>

## <span data-ttu-id="1797f-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1797f-115">PARAMETERS</span></span>

### <span data-ttu-id="1797f-116">-AdminPassword</span><span class="sxs-lookup"><span data-stu-id="1797f-116">-AdminPassword</span></span>
<span data-ttu-id="1797f-117">Пароль администратора, используемый на виртуальных машинах.</span><span class="sxs-lookup"><span data-stu-id="1797f-117">Admin password used for the virtual machines.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1797f-118">-AdminUserName</span><span class="sxs-lookup"><span data-stu-id="1797f-118">-AdminUserName</span></span>
<span data-ttu-id="1797f-119">Пароль администратора, используемый на виртуальных машинах.</span><span class="sxs-lookup"><span data-stu-id="1797f-119">Admin password used for the virtual machines.</span></span>
<span data-ttu-id="1797f-120">По умолчанию: vmadmin.</span><span class="sxs-lookup"><span data-stu-id="1797f-120">Default: vmadmin.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: "vmadmin"
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1797f-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1797f-121">-AsJob</span></span>
<span data-ttu-id="1797f-122">Запустите его в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="1797f-122">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="1797f-123">-ClientCertCommonName</span><span class="sxs-lookup"><span data-stu-id="1797f-123">-ClientCertCommonName</span></span>
<span data-ttu-id="1797f-124">Общее имя сертификата клиента.</span><span class="sxs-lookup"><span data-stu-id="1797f-124">Client certificate common name.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientCertByCn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1797f-125">-ClientCertIsAdmin</span><span class="sxs-lookup"><span data-stu-id="1797f-125">-ClientCertIsAdmin</span></span>
<span data-ttu-id="1797f-126">Используется для указания уровня администратора сертификата клиента.</span><span class="sxs-lookup"><span data-stu-id="1797f-126">Use to specify if the client certificate has administrator level.</span></span>

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

### <span data-ttu-id="1797f-127">-ClientCertIssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="1797f-127">-ClientCertIssuerThumbprint</span></span>
<span data-ttu-id="1797f-128">Список эскизов issuer для сертификата клиента.</span><span class="sxs-lookup"><span data-stu-id="1797f-128">List of Issuer thumbprints for the client certificate.</span></span>
<span data-ttu-id="1797f-129">Используется только в сочетании с ClientCertCommonName.</span><span class="sxs-lookup"><span data-stu-id="1797f-129">Only use in combination with ClientCertCommonName.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ClientCertByCn
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1797f-130">-ClientCertThumbprint</span><span class="sxs-lookup"><span data-stu-id="1797f-130">-ClientCertThumbprint</span></span>
<span data-ttu-id="1797f-131">Эскиз сертификата клиента.</span><span class="sxs-lookup"><span data-stu-id="1797f-131">Client certificate thumbprint.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientCertByTp
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1797f-132">-ClientConnectionPort</span><span class="sxs-lookup"><span data-stu-id="1797f-132">-ClientConnectionPort</span></span>
<span data-ttu-id="1797f-133">Порт, используемый для клиентских подключений к кластеру.</span><span class="sxs-lookup"><span data-stu-id="1797f-133">Port used for client connections to the cluster.</span></span>
<span data-ttu-id="1797f-134">Значение по умолчанию: 19 000.</span><span class="sxs-lookup"><span data-stu-id="1797f-134">Default: 19000.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 19000
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1797f-135">-CodeVersion</span><span class="sxs-lookup"><span data-stu-id="1797f-135">-CodeVersion</span></span>
<span data-ttu-id="1797f-136">Версия кода тканью кластера.</span><span class="sxs-lookup"><span data-stu-id="1797f-136">Cluster service fabric code version.</span></span>
<span data-ttu-id="1797f-137">Используйте этот режим только в режиме обновления вручную.</span><span class="sxs-lookup"><span data-stu-id="1797f-137">Only use if upgrade mode is Manual.</span></span>

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

### <span data-ttu-id="1797f-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1797f-138">-DefaultProfile</span></span>
<span data-ttu-id="1797f-139">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1797f-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1797f-140">-DnsName</span><span class="sxs-lookup"><span data-stu-id="1797f-140">-DnsName</span></span>
<span data-ttu-id="1797f-141">Имя DNS кластера.</span><span class="sxs-lookup"><span data-stu-id="1797f-141">Cluster's dns name.</span></span>

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

### <span data-ttu-id="1797f-142">-HttpGatewayConnectionPort</span><span class="sxs-lookup"><span data-stu-id="1797f-142">-HttpGatewayConnectionPort</span></span>
<span data-ttu-id="1797f-143">Порт, используемый для http-подключений к кластеру.</span><span class="sxs-lookup"><span data-stu-id="1797f-143">Port used for http connections to the cluster.</span></span>
<span data-ttu-id="1797f-144">Значение по умолчанию: 19080.</span><span class="sxs-lookup"><span data-stu-id="1797f-144">Default: 19080.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 19080
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1797f-145">-Location</span><span class="sxs-lookup"><span data-stu-id="1797f-145">-Location</span></span>
<span data-ttu-id="1797f-146">Расположение ресурса</span><span class="sxs-lookup"><span data-stu-id="1797f-146">The resource location</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1797f-147">-Name</span><span class="sxs-lookup"><span data-stu-id="1797f-147">-Name</span></span>
<span data-ttu-id="1797f-148">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="1797f-148">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1797f-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1797f-149">-ResourceGroupName</span></span>
<span data-ttu-id="1797f-150">Укажите имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1797f-150">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1797f-151">-ReverseProxyEndpointPort</span><span class="sxs-lookup"><span data-stu-id="1797f-151">-ReverseProxyEndpointPort</span></span>
<span data-ttu-id="1797f-152">Конечная точка, используемая обратным прокси-сервером.</span><span class="sxs-lookup"><span data-stu-id="1797f-152">Endpoint used by reverse proxy.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1797f-153">-SKU</span><span class="sxs-lookup"><span data-stu-id="1797f-153">-Sku</span></span>
<span data-ttu-id="1797f-154">SKU кластера: вариант "Базовый": он будет иметь не менее трех основных узлов и только 1 тип узла и стандартный: он будет иметь не менее 5 основных узлов и допускает несколько типов узлов.</span><span class="sxs-lookup"><span data-stu-id="1797f-154">Cluster's Sku, the options are Basic: it will have a minimum of 3 seed nodes and only allows 1 node type and Standard: it will have a minimum of 5 seed nodes and allows multiple node types.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.ManagedClusterSku
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard

Required: False
Position: Named
Default value: Basic
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1797f-155">-UpgradeMode</span><span class="sxs-lookup"><span data-stu-id="1797f-155">-UpgradeMode</span></span>
<span data-ttu-id="1797f-156">Режим обновления версии кода тканью службы кластера.</span><span class="sxs-lookup"><span data-stu-id="1797f-156">Cluster service fabric code version upgrade mode.</span></span>
<span data-ttu-id="1797f-157">Автоматически или вручную.</span><span class="sxs-lookup"><span data-stu-id="1797f-157">Automatic or Manual.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.ClusterUpgradeMode
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, Manual

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1797f-158">-UseTestExtension</span><span class="sxs-lookup"><span data-stu-id="1797f-158">-UseTestExtension</span></span>
<span data-ttu-id="1797f-159">При указании кластера будет перенагрещено расширением тестовых vmss службы.</span><span class="sxs-lookup"><span data-stu-id="1797f-159">If Specify The cluster will be crated with service test vmss extension.</span></span>

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

### <span data-ttu-id="1797f-160">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1797f-160">-Confirm</span></span>
<span data-ttu-id="1797f-161">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1797f-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1797f-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1797f-162">-WhatIf</span></span>
<span data-ttu-id="1797f-163">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1797f-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1797f-164">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="1797f-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1797f-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1797f-165">CommonParameters</span></span>
<span data-ttu-id="1797f-166">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1797f-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1797f-167">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1797f-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1797f-168">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1797f-168">INPUTS</span></span>

### <span data-ttu-id="1797f-169">System.String</span><span class="sxs-lookup"><span data-stu-id="1797f-169">System.String</span></span>

## <span data-ttu-id="1797f-170">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1797f-170">OUTPUTS</span></span>

### <span data-ttu-id="1797f-171">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span><span class="sxs-lookup"><span data-stu-id="1797f-171">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span></span>

## <span data-ttu-id="1797f-172">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1797f-172">NOTES</span></span>

## <span data-ttu-id="1797f-173">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1797f-173">RELATED LINKS</span></span>

[<span data-ttu-id="1797f-174">New-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="1797f-174">New-AzServiceFabricManagedNodeType</span></span>](./New-AzServiceFabricManagedNodeType.md)
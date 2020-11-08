---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/new-azservicefabricmanagedcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricManagedCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricManagedCluster.md
ms.openlocfilehash: 9dd54f0f1ca56a8bedf3550e238a4308b519925d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236622"
---
# <span data-ttu-id="b14d2-101">New-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="b14d2-101">New-AzServiceFabricManagedCluster</span></span>

## <span data-ttu-id="b14d2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b14d2-102">SYNOPSIS</span></span>
<span data-ttu-id="b14d2-103">Создайте новый управляемый кластер.</span><span class="sxs-lookup"><span data-stu-id="b14d2-103">Create new managed cluster.</span></span>

## <span data-ttu-id="b14d2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b14d2-104">SYNTAX</span></span>

### <span data-ttu-id="b14d2-105">ClientCertByTp (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b14d2-105">ClientCertByTp (Default)</span></span>
```
New-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-Name] <String> -Location <String>
 [-UpgradeMode <ClusterUpgradeMode>] [-CodeVersion <String>] [-ClientCertIsAdmin]
 -ClientCertThumbprint <String> -AdminPassword <SecureString> [-AdminUserName <String>]
 [-HttpGatewayConnectionPort <Int32>] [-ClientConnectionPort <Int32>] [-DnsName <String>]
 [-ReverseProxyEndpointPort <Int32>] [-Sku <ManagedClusterSku>] [-UseTestExtension] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b14d2-106">ClientCertByCn</span><span class="sxs-lookup"><span data-stu-id="b14d2-106">ClientCertByCn</span></span>
```
New-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-Name] <String> -Location <String>
 [-UpgradeMode <ClusterUpgradeMode>] [-CodeVersion <String>] [-ClientCertIsAdmin]
 -ClientCertCommonName <String> [-ClientCertIssuerThumbprint <String[]>] -AdminPassword <SecureString>
 [-AdminUserName <String>] [-HttpGatewayConnectionPort <Int32>] [-ClientConnectionPort <Int32>]
 [-DnsName <String>] [-ReverseProxyEndpointPort <Int32>] [-Sku <ManagedClusterSku>] [-UseTestExtension]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b14d2-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b14d2-107">DESCRIPTION</span></span>
<span data-ttu-id="b14d2-108">Этот командлет создаст ресурс управляемого кластера без типов узлов.</span><span class="sxs-lookup"><span data-stu-id="b14d2-108">This cmdlet will create a managed cluster resource without node types.</span></span> <span data-ttu-id="b14d2-109">Для загрузки кластера необходимо добавить основной тип узла с помощью [New-AzServiceFabricManagedNodeType](./New-AzServiceFabricManagedNodeType.md).</span><span class="sxs-lookup"><span data-stu-id="b14d2-109">To bootstrap the cluster A primary node type needs to be added use [New-AzServiceFabricManagedNodeType](./New-AzServiceFabricManagedNodeType.md).</span></span>

## <span data-ttu-id="b14d2-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b14d2-110">EXAMPLES</span></span>

### <span data-ttu-id="b14d2-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b14d2-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$password = ConvertTo-SecureString -AsPlainText -Force "testpass1234!@#$"
New-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Location centraluseuap -ClusterName $clusterName -AdminPassword $password -Verbose
```

<span data-ttu-id="b14d2-112">Эта команда создает ресурс кластера с базовой конфигурацией по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b14d2-112">This command creates a cluster resource with default basic sku.</span></span>

### <span data-ttu-id="b14d2-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="b14d2-113">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$password = ConvertTo-SecureString -AsPlainText -Force "testpass1234!@#$"
New-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Location centraluseuap -ClusterName $clusterName -ClientCertThumbprint XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX -ClientCertIsAdmin -AdminPassword $password -Sku Standard -Verbose
```

<span data-ttu-id="b14d2-114">Эта команда создает ресурс кластера в centraluseuap с первоначальным клиентским сертификатом администратора и стандартным SKU.</span><span class="sxs-lookup"><span data-stu-id="b14d2-114">This command creates a cluster resource in centraluseuap with an initial admin client certificate and standard sku.</span></span>

## <span data-ttu-id="b14d2-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b14d2-115">PARAMETERS</span></span>

### <span data-ttu-id="b14d2-116">-AdminPassword</span><span class="sxs-lookup"><span data-stu-id="b14d2-116">-AdminPassword</span></span>
<span data-ttu-id="b14d2-117">Пароль администратора, используемый для виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="b14d2-117">Admin password used for the virtual machines.</span></span>

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

### <span data-ttu-id="b14d2-118">-AdminUserName</span><span class="sxs-lookup"><span data-stu-id="b14d2-118">-AdminUserName</span></span>
<span data-ttu-id="b14d2-119">Пароль администратора, используемый для виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="b14d2-119">Admin password used for the virtual machines.</span></span>
<span data-ttu-id="b14d2-120">По умолчанию: vmadmin.</span><span class="sxs-lookup"><span data-stu-id="b14d2-120">Default: vmadmin.</span></span>

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

### <span data-ttu-id="b14d2-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b14d2-121">-AsJob</span></span>
<span data-ttu-id="b14d2-122">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="b14d2-122">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="b14d2-123">-ClientCertCommonName</span><span class="sxs-lookup"><span data-stu-id="b14d2-123">-ClientCertCommonName</span></span>
<span data-ttu-id="b14d2-124">Общее имя сертификата клиента.</span><span class="sxs-lookup"><span data-stu-id="b14d2-124">Client certificate common name.</span></span>

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

### <span data-ttu-id="b14d2-125">-ClientCertIsAdmin</span><span class="sxs-lookup"><span data-stu-id="b14d2-125">-ClientCertIsAdmin</span></span>
<span data-ttu-id="b14d2-126">Используется, чтобы указать, имеет ли клиентский сертификат уровень администратора.</span><span class="sxs-lookup"><span data-stu-id="b14d2-126">Use to specify if the client certificate has administrator level.</span></span>

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

### <span data-ttu-id="b14d2-127">-ClientCertIssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="b14d2-127">-ClientCertIssuerThumbprint</span></span>
<span data-ttu-id="b14d2-128">Список отпечаток поставщика для клиентского сертификата.</span><span class="sxs-lookup"><span data-stu-id="b14d2-128">List of Issuer thumbprints for the client certificate.</span></span>
<span data-ttu-id="b14d2-129">Используется только в сочетании с ClientCertCommonName.</span><span class="sxs-lookup"><span data-stu-id="b14d2-129">Only use in combination with ClientCertCommonName.</span></span>

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

### <span data-ttu-id="b14d2-130">-ClientCertThumbprint</span><span class="sxs-lookup"><span data-stu-id="b14d2-130">-ClientCertThumbprint</span></span>
<span data-ttu-id="b14d2-131">Отпечаток сертификата клиента.</span><span class="sxs-lookup"><span data-stu-id="b14d2-131">Client certificate thumbprint.</span></span>

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

### <span data-ttu-id="b14d2-132">-ClientConnectionPort</span><span class="sxs-lookup"><span data-stu-id="b14d2-132">-ClientConnectionPort</span></span>
<span data-ttu-id="b14d2-133">Порт, используемый для клиентских подключений к кластеру.</span><span class="sxs-lookup"><span data-stu-id="b14d2-133">Port used for client connections to the cluster.</span></span>
<span data-ttu-id="b14d2-134">По умолчанию: 19000.</span><span class="sxs-lookup"><span data-stu-id="b14d2-134">Default: 19000.</span></span>

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

### <span data-ttu-id="b14d2-135">-CodeVersion</span><span class="sxs-lookup"><span data-stu-id="b14d2-135">-CodeVersion</span></span>
<span data-ttu-id="b14d2-136">Версия кода фабрики службы кластеров.</span><span class="sxs-lookup"><span data-stu-id="b14d2-136">Cluster service fabric code version.</span></span>
<span data-ttu-id="b14d2-137">Используйте только в том случае, если вы используете режим обновления вручную.</span><span class="sxs-lookup"><span data-stu-id="b14d2-137">Only use if upgrade mode is Manual.</span></span>

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

### <span data-ttu-id="b14d2-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b14d2-138">-DefaultProfile</span></span>
<span data-ttu-id="b14d2-139">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b14d2-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b14d2-140">-DnsName</span><span class="sxs-lookup"><span data-stu-id="b14d2-140">-DnsName</span></span>
<span data-ttu-id="b14d2-141">DNS-имя кластера.</span><span class="sxs-lookup"><span data-stu-id="b14d2-141">Cluster's dns name.</span></span>

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

### <span data-ttu-id="b14d2-142">-HttpGatewayConnectionPort</span><span class="sxs-lookup"><span data-stu-id="b14d2-142">-HttpGatewayConnectionPort</span></span>
<span data-ttu-id="b14d2-143">Порт, используемый для подключений HTTP к кластеру.</span><span class="sxs-lookup"><span data-stu-id="b14d2-143">Port used for http connections to the cluster.</span></span>
<span data-ttu-id="b14d2-144">По умолчанию: 19080.</span><span class="sxs-lookup"><span data-stu-id="b14d2-144">Default: 19080.</span></span>

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

### <span data-ttu-id="b14d2-145">-Location</span><span class="sxs-lookup"><span data-stu-id="b14d2-145">-Location</span></span>
<span data-ttu-id="b14d2-146">Расположение ресурса</span><span class="sxs-lookup"><span data-stu-id="b14d2-146">The resource location</span></span>

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

### <span data-ttu-id="b14d2-147">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b14d2-147">-Name</span></span>
<span data-ttu-id="b14d2-148">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="b14d2-148">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="b14d2-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b14d2-149">-ResourceGroupName</span></span>
<span data-ttu-id="b14d2-150">Укажите имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b14d2-150">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="b14d2-151">-ReverseProxyEndpointPort</span><span class="sxs-lookup"><span data-stu-id="b14d2-151">-ReverseProxyEndpointPort</span></span>
<span data-ttu-id="b14d2-152">Конечная точка, используемая в обратном прокси.</span><span class="sxs-lookup"><span data-stu-id="b14d2-152">Endpoint used by reverse proxy.</span></span>

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

### <span data-ttu-id="b14d2-153">-SKU</span><span class="sxs-lookup"><span data-stu-id="b14d2-153">-Sku</span></span>
<span data-ttu-id="b14d2-154">SKU кластера, доступны следующие варианты: у него есть не менее 3 начальных узла и разрешено только 1 тип узла и стандарт: у него будет не менее 5 начальных узлов и разрешено использовать несколько типов узлов.</span><span class="sxs-lookup"><span data-stu-id="b14d2-154">Cluster's Sku, the options are Basic: it will have a minimum of 3 seed nodes and only allows 1 node type and Standard: it will have a minimum of 5 seed nodes and allows multiple node types.</span></span>

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

### <span data-ttu-id="b14d2-155">-UpgradeMode</span><span class="sxs-lookup"><span data-stu-id="b14d2-155">-UpgradeMode</span></span>
<span data-ttu-id="b14d2-156">Режим обновления версии кода фабрики службы кластеров.</span><span class="sxs-lookup"><span data-stu-id="b14d2-156">Cluster service fabric code version upgrade mode.</span></span>
<span data-ttu-id="b14d2-157">Автоматически или вручную.</span><span class="sxs-lookup"><span data-stu-id="b14d2-157">Automatic or Manual.</span></span>

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

### <span data-ttu-id="b14d2-158">-UseTestExtension</span><span class="sxs-lookup"><span data-stu-id="b14d2-158">-UseTestExtension</span></span>
<span data-ttu-id="b14d2-159">Если указать кластер, будет использоваться расширение Service Test vmss.</span><span class="sxs-lookup"><span data-stu-id="b14d2-159">If Specify The cluster will be crated with service test vmss extension.</span></span>

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

### <span data-ttu-id="b14d2-160">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b14d2-160">-Confirm</span></span>
<span data-ttu-id="b14d2-161">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b14d2-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b14d2-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b14d2-162">-WhatIf</span></span>
<span data-ttu-id="b14d2-163">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b14d2-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b14d2-164">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b14d2-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b14d2-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b14d2-165">CommonParameters</span></span>
<span data-ttu-id="b14d2-166">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b14d2-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b14d2-167">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b14d2-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b14d2-168">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b14d2-168">INPUTS</span></span>

### <span data-ttu-id="b14d2-169">System. String</span><span class="sxs-lookup"><span data-stu-id="b14d2-169">System.String</span></span>

## <span data-ttu-id="b14d2-170">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b14d2-170">OUTPUTS</span></span>

### <span data-ttu-id="b14d2-171">Microsoft. Azure. Commands. ServiceFabric. Models. PSManagedCluster</span><span class="sxs-lookup"><span data-stu-id="b14d2-171">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span></span>

## <span data-ttu-id="b14d2-172">Пуск</span><span class="sxs-lookup"><span data-stu-id="b14d2-172">NOTES</span></span>

## <span data-ttu-id="b14d2-173">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b14d2-173">RELATED LINKS</span></span>

[<span data-ttu-id="b14d2-174">New-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="b14d2-174">New-AzServiceFabricManagedNodeType</span></span>](./New-AzServiceFabricManagedNodeType.md)
---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricmanagedclusterclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedClusterClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedClusterClientCertificate.md
ms.openlocfilehash: d9a3e5488fe55a1d5090fb21ffb211e6fcec53c2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98517205"
---
# <span data-ttu-id="b7ec7-101">Remove-AzServiceFabricManagedClusterClientCertificate</span><span class="sxs-lookup"><span data-stu-id="b7ec7-101">Remove-AzServiceFabricManagedClusterClientCertificate</span></span>

## <span data-ttu-id="b7ec7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7ec7-102">SYNOPSIS</span></span>
<span data-ttu-id="b7ec7-103">Remvoe client certificate by thumbprint or common name.</span><span class="sxs-lookup"><span data-stu-id="b7ec7-103">Remvoe client certificate by thumbprint or common name.</span></span>

## <span data-ttu-id="b7ec7-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b7ec7-104">SYNTAX</span></span>

### <span data-ttu-id="b7ec7-105">ClientCertByTpByObj (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b7ec7-105">ClientCertByTpByObj (Default)</span></span>
```
Remove-AzServiceFabricManagedClusterClientCertificate [-InputObject] <PSManagedCluster> -Thumbprint <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7ec7-106">ClientCertByCnTpName</span><span class="sxs-lookup"><span data-stu-id="b7ec7-106">ClientCertByCnTpName</span></span>
```
Remove-AzServiceFabricManagedClusterClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -Thumbprint <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b7ec7-107">ClientCertByCnByName</span><span class="sxs-lookup"><span data-stu-id="b7ec7-107">ClientCertByCnByName</span></span>
```
Remove-AzServiceFabricManagedClusterClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -CommonName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b7ec7-108">ClientCertByCnByObj</span><span class="sxs-lookup"><span data-stu-id="b7ec7-108">ClientCertByCnByObj</span></span>
```
Remove-AzServiceFabricManagedClusterClientCertificate [-InputObject] <PSManagedCluster> -CommonName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7ec7-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b7ec7-109">DESCRIPTION</span></span>
<span data-ttu-id="b7ec7-110">Remvoe client certificate by thumbprint or common name.</span><span class="sxs-lookup"><span data-stu-id="b7ec7-110">Remvoe client certificate by thumbprint or common name.</span></span>

## <span data-ttu-id="b7ec7-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b7ec7-111">EXAMPLES</span></span>

### <span data-ttu-id="b7ec7-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b7ec7-112">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Remove-AzServiceFabricManagedClusterClientCertificate -ResourceGroupName $rgName -Name $clusterName -CommonName 'Contoso.com'
```

<span data-ttu-id="b7ec7-113">Удаление сертификата клиента по общему имени.</span><span class="sxs-lookup"><span data-stu-id="b7ec7-113">Remove client certificate by common name.</span></span>

### <span data-ttu-id="b7ec7-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="b7ec7-114">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Remove-AzServiceFabricManagedClusterClientCertificate -ResourceGroupName $rgName -Name $clusterName -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="b7ec7-115">Удаление сертификата клиента по прейспировке.</span><span class="sxs-lookup"><span data-stu-id="b7ec7-115">Remove client certificate by thumbprint.</span></span>

### <span data-ttu-id="b7ec7-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="b7ec7-116">Example 3</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$cluster = Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName

$cluster | Remove-AzServiceFabricManagedClusterClientCertificate -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="b7ec7-117">Удаление сертификата клиента по прейспировке с помощью piping.</span><span class="sxs-lookup"><span data-stu-id="b7ec7-117">Remove client certificate by thumbprint, with piping.</span></span>

## <span data-ttu-id="b7ec7-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b7ec7-118">PARAMETERS</span></span>

### <span data-ttu-id="b7ec7-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b7ec7-119">-AsJob</span></span>
<span data-ttu-id="b7ec7-120">Запустите его в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="b7ec7-120">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="b7ec7-121">-CommonName</span><span class="sxs-lookup"><span data-stu-id="b7ec7-121">-CommonName</span></span>
<span data-ttu-id="b7ec7-122">Общее имя сертификата клиента.</span><span class="sxs-lookup"><span data-stu-id="b7ec7-122">Client certificate common name.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientCertByCnByName, ClientCertByCnByObj
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7ec7-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7ec7-123">-DefaultProfile</span></span>
<span data-ttu-id="b7ec7-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b7ec7-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7ec7-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b7ec7-125">-InputObject</span></span>
<span data-ttu-id="b7ec7-126">Управляемый кластерный ресурс</span><span class="sxs-lookup"><span data-stu-id="b7ec7-126">Managed cluster resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster
Parameter Sets: ClientCertByTpByObj, ClientCertByCnByObj
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b7ec7-127">-Name</span><span class="sxs-lookup"><span data-stu-id="b7ec7-127">-Name</span></span>
<span data-ttu-id="b7ec7-128">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="b7ec7-128">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientCertByCnTpName, ClientCertByCnByName
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7ec7-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b7ec7-129">-PassThru</span></span>
<span data-ttu-id="b7ec7-130">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="b7ec7-130">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="b7ec7-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7ec7-131">-ResourceGroupName</span></span>
<span data-ttu-id="b7ec7-132">Укажите имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b7ec7-132">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientCertByCnTpName, ClientCertByCnByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7ec7-133">-Thumbprint</span><span class="sxs-lookup"><span data-stu-id="b7ec7-133">-Thumbprint</span></span>
<span data-ttu-id="b7ec7-134">Эскиз сертификата клиента.</span><span class="sxs-lookup"><span data-stu-id="b7ec7-134">Client certificate thumbprint.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientCertByTpByObj, ClientCertByCnTpName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7ec7-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b7ec7-135">-Confirm</span></span>
<span data-ttu-id="b7ec7-136">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="b7ec7-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7ec7-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7ec7-137">-WhatIf</span></span>
<span data-ttu-id="b7ec7-138">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b7ec7-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7ec7-139">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="b7ec7-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7ec7-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7ec7-140">CommonParameters</span></span>
<span data-ttu-id="b7ec7-141">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7ec7-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7ec7-142">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b7ec7-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7ec7-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b7ec7-143">INPUTS</span></span>

### <span data-ttu-id="b7ec7-144">System.String</span><span class="sxs-lookup"><span data-stu-id="b7ec7-144">System.String</span></span>

## <span data-ttu-id="b7ec7-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b7ec7-145">OUTPUTS</span></span>

### <span data-ttu-id="b7ec7-146">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span><span class="sxs-lookup"><span data-stu-id="b7ec7-146">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span></span>

## <span data-ttu-id="b7ec7-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b7ec7-147">NOTES</span></span>

## <span data-ttu-id="b7ec7-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b7ec7-148">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricmanagedclusterclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedClusterClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedClusterClientCertificate.md
ms.openlocfilehash: d9a3e5488fe55a1d5090fb21ffb211e6fcec53c2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100225212"
---
# <span data-ttu-id="4f72b-101">Remove-AzServiceFabricManagedClusterClientCertificate</span><span class="sxs-lookup"><span data-stu-id="4f72b-101">Remove-AzServiceFabricManagedClusterClientCertificate</span></span>

## <span data-ttu-id="4f72b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f72b-102">SYNOPSIS</span></span>
<span data-ttu-id="4f72b-103">Remvoe client certificate by thumbprint or common name.</span><span class="sxs-lookup"><span data-stu-id="4f72b-103">Remvoe client certificate by thumbprint or common name.</span></span>

## <span data-ttu-id="4f72b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4f72b-104">SYNTAX</span></span>

### <span data-ttu-id="4f72b-105">ClientCertByTpByObj (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4f72b-105">ClientCertByTpByObj (Default)</span></span>
```
Remove-AzServiceFabricManagedClusterClientCertificate [-InputObject] <PSManagedCluster> -Thumbprint <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f72b-106">ClientCertByCnTpName</span><span class="sxs-lookup"><span data-stu-id="4f72b-106">ClientCertByCnTpName</span></span>
```
Remove-AzServiceFabricManagedClusterClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -Thumbprint <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4f72b-107">ClientCertByCnByName</span><span class="sxs-lookup"><span data-stu-id="4f72b-107">ClientCertByCnByName</span></span>
```
Remove-AzServiceFabricManagedClusterClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -CommonName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4f72b-108">ClientCertByCnByObj</span><span class="sxs-lookup"><span data-stu-id="4f72b-108">ClientCertByCnByObj</span></span>
```
Remove-AzServiceFabricManagedClusterClientCertificate [-InputObject] <PSManagedCluster> -CommonName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f72b-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4f72b-109">DESCRIPTION</span></span>
<span data-ttu-id="4f72b-110">Remvoe client certificate by thumbprint or common name.</span><span class="sxs-lookup"><span data-stu-id="4f72b-110">Remvoe client certificate by thumbprint or common name.</span></span>

## <span data-ttu-id="4f72b-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4f72b-111">EXAMPLES</span></span>

### <span data-ttu-id="4f72b-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4f72b-112">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Remove-AzServiceFabricManagedClusterClientCertificate -ResourceGroupName $rgName -Name $clusterName -CommonName 'Contoso.com'
```

<span data-ttu-id="4f72b-113">Удаление сертификата клиента по общему имени.</span><span class="sxs-lookup"><span data-stu-id="4f72b-113">Remove client certificate by common name.</span></span>

### <span data-ttu-id="4f72b-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="4f72b-114">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Remove-AzServiceFabricManagedClusterClientCertificate -ResourceGroupName $rgName -Name $clusterName -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="4f72b-115">Удаление сертификата клиента по прейспировке.</span><span class="sxs-lookup"><span data-stu-id="4f72b-115">Remove client certificate by thumbprint.</span></span>

### <span data-ttu-id="4f72b-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="4f72b-116">Example 3</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$cluster = Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName

$cluster | Remove-AzServiceFabricManagedClusterClientCertificate -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="4f72b-117">Удаление сертификата клиента по прейспировке с помощью piping.</span><span class="sxs-lookup"><span data-stu-id="4f72b-117">Remove client certificate by thumbprint, with piping.</span></span>

## <span data-ttu-id="4f72b-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4f72b-118">PARAMETERS</span></span>

### <span data-ttu-id="4f72b-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4f72b-119">-AsJob</span></span>
<span data-ttu-id="4f72b-120">Запустите его в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="4f72b-120">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="4f72b-121">-CommonName</span><span class="sxs-lookup"><span data-stu-id="4f72b-121">-CommonName</span></span>
<span data-ttu-id="4f72b-122">Общее имя сертификата клиента.</span><span class="sxs-lookup"><span data-stu-id="4f72b-122">Client certificate common name.</span></span>

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

### <span data-ttu-id="4f72b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f72b-123">-DefaultProfile</span></span>
<span data-ttu-id="4f72b-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4f72b-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4f72b-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4f72b-125">-InputObject</span></span>
<span data-ttu-id="4f72b-126">Управляемый кластерный ресурс</span><span class="sxs-lookup"><span data-stu-id="4f72b-126">Managed cluster resource</span></span>

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

### <span data-ttu-id="4f72b-127">-Name</span><span class="sxs-lookup"><span data-stu-id="4f72b-127">-Name</span></span>
<span data-ttu-id="4f72b-128">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="4f72b-128">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="4f72b-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4f72b-129">-PassThru</span></span>
<span data-ttu-id="4f72b-130">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="4f72b-130">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="4f72b-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f72b-131">-ResourceGroupName</span></span>
<span data-ttu-id="4f72b-132">Укажите имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4f72b-132">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="4f72b-133">-Thumbprint</span><span class="sxs-lookup"><span data-stu-id="4f72b-133">-Thumbprint</span></span>
<span data-ttu-id="4f72b-134">Эскиз сертификата клиента.</span><span class="sxs-lookup"><span data-stu-id="4f72b-134">Client certificate thumbprint.</span></span>

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

### <span data-ttu-id="4f72b-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4f72b-135">-Confirm</span></span>
<span data-ttu-id="4f72b-136">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4f72b-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f72b-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f72b-137">-WhatIf</span></span>
<span data-ttu-id="4f72b-138">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4f72b-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f72b-139">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="4f72b-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f72b-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f72b-140">CommonParameters</span></span>
<span data-ttu-id="4f72b-141">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f72b-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f72b-142">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4f72b-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f72b-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4f72b-143">INPUTS</span></span>

### <span data-ttu-id="4f72b-144">System.String</span><span class="sxs-lookup"><span data-stu-id="4f72b-144">System.String</span></span>

## <span data-ttu-id="4f72b-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4f72b-145">OUTPUTS</span></span>

### <span data-ttu-id="4f72b-146">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span><span class="sxs-lookup"><span data-stu-id="4f72b-146">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span></span>

## <span data-ttu-id="4f72b-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4f72b-147">NOTES</span></span>

## <span data-ttu-id="4f72b-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4f72b-148">RELATED LINKS</span></span>

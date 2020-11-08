---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricmanagedclusterclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedClusterClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedClusterClientCertificate.md
ms.openlocfilehash: d9a3e5488fe55a1d5090fb21ffb211e6fcec53c2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243954"
---
# <span data-ttu-id="e77eb-101">Remove-AzServiceFabricManagedClusterClientCertificate</span><span class="sxs-lookup"><span data-stu-id="e77eb-101">Remove-AzServiceFabricManagedClusterClientCertificate</span></span>

## <span data-ttu-id="e77eb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e77eb-102">SYNOPSIS</span></span>
<span data-ttu-id="e77eb-103">Remvoe сертификат клиента по отпечатному или общему имени.</span><span class="sxs-lookup"><span data-stu-id="e77eb-103">Remvoe client certificate by thumbprint or common name.</span></span>

## <span data-ttu-id="e77eb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e77eb-104">SYNTAX</span></span>

### <span data-ttu-id="e77eb-105">ClientCertByTpByObj (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e77eb-105">ClientCertByTpByObj (Default)</span></span>
```
Remove-AzServiceFabricManagedClusterClientCertificate [-InputObject] <PSManagedCluster> -Thumbprint <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e77eb-106">ClientCertByCnTpName</span><span class="sxs-lookup"><span data-stu-id="e77eb-106">ClientCertByCnTpName</span></span>
```
Remove-AzServiceFabricManagedClusterClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -Thumbprint <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e77eb-107">ClientCertByCnByName</span><span class="sxs-lookup"><span data-stu-id="e77eb-107">ClientCertByCnByName</span></span>
```
Remove-AzServiceFabricManagedClusterClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -CommonName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e77eb-108">ClientCertByCnByObj</span><span class="sxs-lookup"><span data-stu-id="e77eb-108">ClientCertByCnByObj</span></span>
```
Remove-AzServiceFabricManagedClusterClientCertificate [-InputObject] <PSManagedCluster> -CommonName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e77eb-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e77eb-109">DESCRIPTION</span></span>
<span data-ttu-id="e77eb-110">Remvoe сертификат клиента по отпечатному или общему имени.</span><span class="sxs-lookup"><span data-stu-id="e77eb-110">Remvoe client certificate by thumbprint or common name.</span></span>

## <span data-ttu-id="e77eb-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e77eb-111">EXAMPLES</span></span>

### <span data-ttu-id="e77eb-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e77eb-112">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Remove-AzServiceFabricManagedClusterClientCertificate -ResourceGroupName $rgName -Name $clusterName -CommonName 'Contoso.com'
```

<span data-ttu-id="e77eb-113">Удаление сертификата клиента по обычному имени.</span><span class="sxs-lookup"><span data-stu-id="e77eb-113">Remove client certificate by common name.</span></span>

### <span data-ttu-id="e77eb-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="e77eb-114">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Remove-AzServiceFabricManagedClusterClientCertificate -ResourceGroupName $rgName -Name $clusterName -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="e77eb-115">Удаление сертификата клиента по отпечатку.</span><span class="sxs-lookup"><span data-stu-id="e77eb-115">Remove client certificate by thumbprint.</span></span>

### <span data-ttu-id="e77eb-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="e77eb-116">Example 3</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$cluster = Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName

$cluster | Remove-AzServiceFabricManagedClusterClientCertificate -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="e77eb-117">Удаление сертификата клиента по отпечатку с помощью трубопроводов.</span><span class="sxs-lookup"><span data-stu-id="e77eb-117">Remove client certificate by thumbprint, with piping.</span></span>

## <span data-ttu-id="e77eb-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e77eb-118">PARAMETERS</span></span>

### <span data-ttu-id="e77eb-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e77eb-119">-AsJob</span></span>
<span data-ttu-id="e77eb-120">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="e77eb-120">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="e77eb-121">-CommonName</span><span class="sxs-lookup"><span data-stu-id="e77eb-121">-CommonName</span></span>
<span data-ttu-id="e77eb-122">Общее имя сертификата клиента.</span><span class="sxs-lookup"><span data-stu-id="e77eb-122">Client certificate common name.</span></span>

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

### <span data-ttu-id="e77eb-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e77eb-123">-DefaultProfile</span></span>
<span data-ttu-id="e77eb-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e77eb-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e77eb-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e77eb-125">-InputObject</span></span>
<span data-ttu-id="e77eb-126">Управляемый ресурс кластера</span><span class="sxs-lookup"><span data-stu-id="e77eb-126">Managed cluster resource</span></span>

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

### <span data-ttu-id="e77eb-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e77eb-127">-Name</span></span>
<span data-ttu-id="e77eb-128">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="e77eb-128">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="e77eb-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e77eb-129">-PassThru</span></span>
<span data-ttu-id="e77eb-130">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="e77eb-130">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="e77eb-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e77eb-131">-ResourceGroupName</span></span>
<span data-ttu-id="e77eb-132">Укажите имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e77eb-132">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="e77eb-133">-Отпечаток</span><span class="sxs-lookup"><span data-stu-id="e77eb-133">-Thumbprint</span></span>
<span data-ttu-id="e77eb-134">Отпечаток сертификата клиента.</span><span class="sxs-lookup"><span data-stu-id="e77eb-134">Client certificate thumbprint.</span></span>

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

### <span data-ttu-id="e77eb-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e77eb-135">-Confirm</span></span>
<span data-ttu-id="e77eb-136">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e77eb-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e77eb-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e77eb-137">-WhatIf</span></span>
<span data-ttu-id="e77eb-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e77eb-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e77eb-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e77eb-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e77eb-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e77eb-140">CommonParameters</span></span>
<span data-ttu-id="e77eb-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e77eb-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e77eb-142">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e77eb-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e77eb-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e77eb-143">INPUTS</span></span>

### <span data-ttu-id="e77eb-144">System. String</span><span class="sxs-lookup"><span data-stu-id="e77eb-144">System.String</span></span>

## <span data-ttu-id="e77eb-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e77eb-145">OUTPUTS</span></span>

### <span data-ttu-id="e77eb-146">Microsoft. Azure. Commands. ServiceFabric. Models. PSManagedCluster</span><span class="sxs-lookup"><span data-stu-id="e77eb-146">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span></span>

## <span data-ttu-id="e77eb-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="e77eb-147">NOTES</span></span>

## <span data-ttu-id="e77eb-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e77eb-148">RELATED LINKS</span></span>

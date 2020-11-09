---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricmanagedclusterclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedClusterClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedClusterClientCertificate.md
ms.openlocfilehash: e948acb179a0ae6a338fa02f01d1cb7d6efbd4fe
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249459"
---
# <span data-ttu-id="cb3b1-101">Add-AzServiceFabricManagedClusterClientCertificate</span><span class="sxs-lookup"><span data-stu-id="cb3b1-101">Add-AzServiceFabricManagedClusterClientCertificate</span></span>

## <span data-ttu-id="cb3b1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cb3b1-102">SYNOPSIS</span></span>
<span data-ttu-id="cb3b1-103">Добавьте в кластер общее имя или отпечаток сертификата.</span><span class="sxs-lookup"><span data-stu-id="cb3b1-103">Add certificate common name or thumbprint to the cluster.</span></span> <span data-ttu-id="cb3b1-104">Это приведет к повторному регистрации сертификата в целях проверки подлинности клиента.</span><span class="sxs-lookup"><span data-stu-id="cb3b1-104">This will register the certificate agains the cluster for client authentication purposes.</span></span>

## <span data-ttu-id="cb3b1-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cb3b1-105">SYNTAX</span></span>

### <span data-ttu-id="cb3b1-106">ClientCertByTpByObj (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cb3b1-106">ClientCertByTpByObj (Default)</span></span>
```
Add-AzServiceFabricManagedClusterClientCertificate [-InputObject] <PSManagedCluster> [-Admin]
 -Thumbprint <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cb3b1-107">ClientCertByTpByName</span><span class="sxs-lookup"><span data-stu-id="cb3b1-107">ClientCertByTpByName</span></span>
```
Add-AzServiceFabricManagedClusterClientCertificate [-ResourceGroupName] <String> [-Name] <String> [-Admin]
 -Thumbprint <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cb3b1-108">ClientCertByCnByName</span><span class="sxs-lookup"><span data-stu-id="cb3b1-108">ClientCertByCnByName</span></span>
```
Add-AzServiceFabricManagedClusterClientCertificate [-ResourceGroupName] <String> [-Name] <String> [-Admin]
 -CommonName <String> [-IssuerThumbprint <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb3b1-109">ClientCertByCnByObj</span><span class="sxs-lookup"><span data-stu-id="cb3b1-109">ClientCertByCnByObj</span></span>
```
Add-AzServiceFabricManagedClusterClientCertificate [-InputObject] <PSManagedCluster> [-Admin]
 -CommonName <String> [-IssuerThumbprint <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb3b1-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cb3b1-110">DESCRIPTION</span></span>
<span data-ttu-id="cb3b1-111">Добавьте в кластер общее имя или отпечаток сертификата.</span><span class="sxs-lookup"><span data-stu-id="cb3b1-111">Add certificate common name or thumbprint to the cluster.</span></span> <span data-ttu-id="cb3b1-112">Это приведет к повторному регистрации сертификата в целях проверки подлинности клиента.</span><span class="sxs-lookup"><span data-stu-id="cb3b1-112">This will register the certificate agains the cluster for client authentication purposes.</span></span>

## <span data-ttu-id="cb3b1-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cb3b1-113">EXAMPLES</span></span>

### <span data-ttu-id="cb3b1-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="cb3b1-114">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Add-AzServiceFabricManagedClusterClientCertificate -ResourceGroupName $rgName -ClusterName $clusterName -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A -Admin
```

<span data-ttu-id="cb3b1-115">Эта команда добавит сертификат с отпечатком "5F3660C715EBBDA31DB1FFDCF508302348DE8E7A" в кластер, чтобы клиент мог использовать этот сертификат в качестве администратора для связи с кластером.</span><span class="sxs-lookup"><span data-stu-id="cb3b1-115">This command will add the certificate with thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' to the cluster, so the client can use the certificate as admin to communicate with the cluster.</span></span>

### <span data-ttu-id="cb3b1-116">Пример 2</span><span class="sxs-lookup"><span data-stu-id="cb3b1-116">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Add-AzServiceFabricManagedClusterClientCertificate -ResourceGroupName $rgName -ClusterName $clusterName -CommonName 'Contoso.com' -IssuerThumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A, 5F3660C715EBBDA31DB1FFDCF508302348DE8E7B
```

<span data-ttu-id="cb3b1-117">Эта команда добавит сертификат клиента только для чтения с общим именем "Contoso.com" и 2 поставщиками.</span><span class="sxs-lookup"><span data-stu-id="cb3b1-117">This command will add a read only client certificate with common name 'Contoso.com' and 2 issuers.</span></span>

### <span data-ttu-id="cb3b1-118">Пример 3</span><span class="sxs-lookup"><span data-stu-id="cb3b1-118">Example 3</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$cluster = Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName
$cluster | Add-AzServiceFabricManagedClusterClientCertificate -CommonName 'Contoso.com' -IssuerThumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A, 5F3660C715EBBDA31DB1FFDCF508302348DE8E7B
```

<span data-ttu-id="cb3b1-119">Эта команда добавит сертификат клиента только для чтения с обычным именем "Contoso.com" и 2 поставщиками с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="cb3b1-119">This command will add a read only client certificate with common name 'Contoso.com' and 2 issuers, with piping.</span></span>

## <span data-ttu-id="cb3b1-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cb3b1-120">PARAMETERS</span></span>

### <span data-ttu-id="cb3b1-121">-Администратор</span><span class="sxs-lookup"><span data-stu-id="cb3b1-121">-Admin</span></span>
<span data-ttu-id="cb3b1-122">Используется, чтобы указать, имеет ли клиентский сертификат уровень администратора.</span><span class="sxs-lookup"><span data-stu-id="cb3b1-122">Use to specify if the client certificate has administrator level.</span></span>

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

### <span data-ttu-id="cb3b1-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cb3b1-123">-AsJob</span></span>
<span data-ttu-id="cb3b1-124">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="cb3b1-124">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="cb3b1-125">-CommonName</span><span class="sxs-lookup"><span data-stu-id="cb3b1-125">-CommonName</span></span>
<span data-ttu-id="cb3b1-126">Общее имя сертификата клиента.</span><span class="sxs-lookup"><span data-stu-id="cb3b1-126">Client certificate common name.</span></span>

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

### <span data-ttu-id="cb3b1-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb3b1-127">-DefaultProfile</span></span>
<span data-ttu-id="cb3b1-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cb3b1-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb3b1-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cb3b1-129">-InputObject</span></span>
<span data-ttu-id="cb3b1-130">Управляемый ресурс кластера</span><span class="sxs-lookup"><span data-stu-id="cb3b1-130">Managed cluster resource</span></span>

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

### <span data-ttu-id="cb3b1-131">-IssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="cb3b1-131">-IssuerThumbprint</span></span>
<span data-ttu-id="cb3b1-132">Список отпечаток поставщика для клиентского сертификата.</span><span class="sxs-lookup"><span data-stu-id="cb3b1-132">List of Issuer thumbprints for the client certificate.</span></span>
<span data-ttu-id="cb3b1-133">Используется только в сочетании с CommonName.</span><span class="sxs-lookup"><span data-stu-id="cb3b1-133">Only use in combination with CommonName.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ClientCertByCnByName, ClientCertByCnByObj
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb3b1-134">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="cb3b1-134">-Name</span></span>
<span data-ttu-id="cb3b1-135">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="cb3b1-135">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientCertByTpByName, ClientCertByCnByName
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb3b1-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb3b1-136">-ResourceGroupName</span></span>
<span data-ttu-id="cb3b1-137">Укажите имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cb3b1-137">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientCertByTpByName, ClientCertByCnByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb3b1-138">-Отпечаток</span><span class="sxs-lookup"><span data-stu-id="cb3b1-138">-Thumbprint</span></span>
<span data-ttu-id="cb3b1-139">Отпечаток сертификата клиента.</span><span class="sxs-lookup"><span data-stu-id="cb3b1-139">Client certificate thumbprint.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientCertByTpByObj, ClientCertByTpByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb3b1-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cb3b1-140">-Confirm</span></span>
<span data-ttu-id="cb3b1-141">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="cb3b1-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb3b1-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb3b1-142">-WhatIf</span></span>
<span data-ttu-id="cb3b1-143">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="cb3b1-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb3b1-144">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="cb3b1-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb3b1-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb3b1-145">CommonParameters</span></span>
<span data-ttu-id="cb3b1-146">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cb3b1-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb3b1-147">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cb3b1-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb3b1-148">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cb3b1-148">INPUTS</span></span>

### <span data-ttu-id="cb3b1-149">System. String</span><span class="sxs-lookup"><span data-stu-id="cb3b1-149">System.String</span></span>

## <span data-ttu-id="cb3b1-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cb3b1-150">OUTPUTS</span></span>

### <span data-ttu-id="cb3b1-151">Microsoft. Azure. Commands. ServiceFabric. Models. PSManagedCluster</span><span class="sxs-lookup"><span data-stu-id="cb3b1-151">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span></span>

## <span data-ttu-id="cb3b1-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="cb3b1-152">NOTES</span></span>

## <span data-ttu-id="cb3b1-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cb3b1-153">RELATED LINKS</span></span>
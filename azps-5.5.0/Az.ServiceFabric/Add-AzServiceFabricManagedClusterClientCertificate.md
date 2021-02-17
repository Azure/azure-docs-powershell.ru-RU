---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricmanagedclusterclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedClusterClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedClusterClientCertificate.md
ms.openlocfilehash: e948acb179a0ae6a338fa02f01d1cb7d6efbd4fe
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100223172"
---
# <span data-ttu-id="7f6cd-101">Add-AzServiceFabricManagedClusterClientCertificate</span><span class="sxs-lookup"><span data-stu-id="7f6cd-101">Add-AzServiceFabricManagedClusterClientCertificate</span></span>

## <span data-ttu-id="7f6cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f6cd-102">SYNOPSIS</span></span>
<span data-ttu-id="7f6cd-103">Добавьте общее имя сертификата или эскиз на кластер.</span><span class="sxs-lookup"><span data-stu-id="7f6cd-103">Add certificate common name or thumbprint to the cluster.</span></span> <span data-ttu-id="7f6cd-104">При этом сертификат будет зарегистрировать кластер повторно в целях проверки подлинности клиента.</span><span class="sxs-lookup"><span data-stu-id="7f6cd-104">This will register the certificate agains the cluster for client authentication purposes.</span></span>

## <span data-ttu-id="7f6cd-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7f6cd-105">SYNTAX</span></span>

### <span data-ttu-id="7f6cd-106">ClientCertByTpByObj (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7f6cd-106">ClientCertByTpByObj (Default)</span></span>
```
Add-AzServiceFabricManagedClusterClientCertificate [-InputObject] <PSManagedCluster> [-Admin]
 -Thumbprint <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7f6cd-107">ClientCertByTpByName</span><span class="sxs-lookup"><span data-stu-id="7f6cd-107">ClientCertByTpByName</span></span>
```
Add-AzServiceFabricManagedClusterClientCertificate [-ResourceGroupName] <String> [-Name] <String> [-Admin]
 -Thumbprint <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7f6cd-108">ClientCertByCnByName</span><span class="sxs-lookup"><span data-stu-id="7f6cd-108">ClientCertByCnByName</span></span>
```
Add-AzServiceFabricManagedClusterClientCertificate [-ResourceGroupName] <String> [-Name] <String> [-Admin]
 -CommonName <String> [-IssuerThumbprint <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f6cd-109">ClientCertByCnByObj</span><span class="sxs-lookup"><span data-stu-id="7f6cd-109">ClientCertByCnByObj</span></span>
```
Add-AzServiceFabricManagedClusterClientCertificate [-InputObject] <PSManagedCluster> [-Admin]
 -CommonName <String> [-IssuerThumbprint <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f6cd-110">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7f6cd-110">DESCRIPTION</span></span>
<span data-ttu-id="7f6cd-111">Добавьте общее имя сертификата или эскиз на кластер.</span><span class="sxs-lookup"><span data-stu-id="7f6cd-111">Add certificate common name or thumbprint to the cluster.</span></span> <span data-ttu-id="7f6cd-112">При этом сертификат будет снова зарегистрирован для проверки подлинности клиента.</span><span class="sxs-lookup"><span data-stu-id="7f6cd-112">This will register the certificate agains the cluster for client authentication purposes.</span></span>

## <span data-ttu-id="7f6cd-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7f6cd-113">EXAMPLES</span></span>

### <span data-ttu-id="7f6cd-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7f6cd-114">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Add-AzServiceFabricManagedClusterClientCertificate -ResourceGroupName $rgName -ClusterName $clusterName -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A -Admin
```

<span data-ttu-id="7f6cd-115">Эта команда добавит в кластер сертификат с препечаткой 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A, чтобы клиент может использовать сертификат как администратор для взаимодействия с кластером.</span><span class="sxs-lookup"><span data-stu-id="7f6cd-115">This command will add the certificate with thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' to the cluster, so the client can use the certificate as admin to communicate with the cluster.</span></span>

### <span data-ttu-id="7f6cd-116">Пример 2</span><span class="sxs-lookup"><span data-stu-id="7f6cd-116">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Add-AzServiceFabricManagedClusterClientCertificate -ResourceGroupName $rgName -ClusterName $clusterName -CommonName 'Contoso.com' -IssuerThumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A, 5F3660C715EBBDA31DB1FFDCF508302348DE8E7B
```

<span data-ttu-id="7f6cd-117">Эта команда добавит сертификат клиента только для чтения с общим именем "Contoso.com" и 2ми выпусками.</span><span class="sxs-lookup"><span data-stu-id="7f6cd-117">This command will add a read only client certificate with common name 'Contoso.com' and 2 issuers.</span></span>

### <span data-ttu-id="7f6cd-118">Пример 3</span><span class="sxs-lookup"><span data-stu-id="7f6cd-118">Example 3</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$cluster = Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName
$cluster | Add-AzServiceFabricManagedClusterClientCertificate -CommonName 'Contoso.com' -IssuerThumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A, 5F3660C715EBBDA31DB1FFDCF508302348DE8E7B
```

<span data-ttu-id="7f6cd-119">Эта команда добавит с помощью piping сертификат клиента только для чтения с общим именем "Contoso.com" и 2-ми выпусками.</span><span class="sxs-lookup"><span data-stu-id="7f6cd-119">This command will add a read only client certificate with common name 'Contoso.com' and 2 issuers, with piping.</span></span>

## <span data-ttu-id="7f6cd-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7f6cd-120">PARAMETERS</span></span>

### <span data-ttu-id="7f6cd-121">-Администратор</span><span class="sxs-lookup"><span data-stu-id="7f6cd-121">-Admin</span></span>
<span data-ttu-id="7f6cd-122">Используется для указания уровня администратора сертификата клиента.</span><span class="sxs-lookup"><span data-stu-id="7f6cd-122">Use to specify if the client certificate has administrator level.</span></span>

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

### <span data-ttu-id="7f6cd-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7f6cd-123">-AsJob</span></span>
<span data-ttu-id="7f6cd-124">Запустите его в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="7f6cd-124">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="7f6cd-125">-CommonName</span><span class="sxs-lookup"><span data-stu-id="7f6cd-125">-CommonName</span></span>
<span data-ttu-id="7f6cd-126">Общее имя сертификата клиента.</span><span class="sxs-lookup"><span data-stu-id="7f6cd-126">Client certificate common name.</span></span>

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

### <span data-ttu-id="7f6cd-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f6cd-127">-DefaultProfile</span></span>
<span data-ttu-id="7f6cd-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7f6cd-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f6cd-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7f6cd-129">-InputObject</span></span>
<span data-ttu-id="7f6cd-130">Управляемый ресурс кластера</span><span class="sxs-lookup"><span data-stu-id="7f6cd-130">Managed cluster resource</span></span>

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

### <span data-ttu-id="7f6cd-131">-IssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="7f6cd-131">-IssuerThumbprint</span></span>
<span data-ttu-id="7f6cd-132">Список эскизов issuer для сертификата клиента.</span><span class="sxs-lookup"><span data-stu-id="7f6cd-132">List of Issuer thumbprints for the client certificate.</span></span>
<span data-ttu-id="7f6cd-133">Используется только в сочетании с CommonName.</span><span class="sxs-lookup"><span data-stu-id="7f6cd-133">Only use in combination with CommonName.</span></span>

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

### <span data-ttu-id="7f6cd-134">-Name</span><span class="sxs-lookup"><span data-stu-id="7f6cd-134">-Name</span></span>
<span data-ttu-id="7f6cd-135">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="7f6cd-135">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="7f6cd-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f6cd-136">-ResourceGroupName</span></span>
<span data-ttu-id="7f6cd-137">Укажите имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7f6cd-137">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="7f6cd-138">-Thumbprint</span><span class="sxs-lookup"><span data-stu-id="7f6cd-138">-Thumbprint</span></span>
<span data-ttu-id="7f6cd-139">Эскиз сертификата клиента.</span><span class="sxs-lookup"><span data-stu-id="7f6cd-139">Client certificate thumbprint.</span></span>

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

### <span data-ttu-id="7f6cd-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7f6cd-140">-Confirm</span></span>
<span data-ttu-id="7f6cd-141">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="7f6cd-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f6cd-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f6cd-142">-WhatIf</span></span>
<span data-ttu-id="7f6cd-143">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f6cd-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f6cd-144">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="7f6cd-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f6cd-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f6cd-145">CommonParameters</span></span>
<span data-ttu-id="7f6cd-146">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f6cd-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f6cd-147">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7f6cd-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f6cd-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7f6cd-148">INPUTS</span></span>

### <span data-ttu-id="7f6cd-149">System.String</span><span class="sxs-lookup"><span data-stu-id="7f6cd-149">System.String</span></span>

## <span data-ttu-id="7f6cd-150">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7f6cd-150">OUTPUTS</span></span>

### <span data-ttu-id="7f6cd-151">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span><span class="sxs-lookup"><span data-stu-id="7f6cd-151">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span></span>

## <span data-ttu-id="7f6cd-152">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7f6cd-152">NOTES</span></span>

## <span data-ttu-id="7f6cd-153">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7f6cd-153">RELATED LINKS</span></span>

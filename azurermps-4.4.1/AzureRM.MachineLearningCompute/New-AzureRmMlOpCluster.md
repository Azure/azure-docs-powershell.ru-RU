---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/New-AzureRmMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/New-AzureRmMlOpCluster.md
ms.openlocfilehash: 222813dc78b4dd7c0118b8146a75ca4d225ce83c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567118"
---
# <span data-ttu-id="75d6a-101">New-AzureRmMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="75d6a-101">New-AzureRmMlOpCluster</span></span>

## <span data-ttu-id="75d6a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="75d6a-102">SYNOPSIS</span></span>
<span data-ttu-id="75d6a-103">Создание нового кластера для выоперационных операций.</span><span class="sxs-lookup"><span data-stu-id="75d6a-103">Creates a new operationalization cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="75d6a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="75d6a-104">SYNTAX</span></span>

### <span data-ttu-id="75d6a-105">Создайте новый кластер выопераций из определения экземпляра OperationalizationCluster.</span><span class="sxs-lookup"><span data-stu-id="75d6a-105">Create a new operationalization cluster from an OperationalizationCluster instance definition.</span></span>
```
New-AzureRmMlOpCluster -ResourceGroupName <String> -Name <String> -InputObject <PSOperationalizationCluster>
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="75d6a-106">Создание нового кластера для выоперационных операций из входных параметров командлета.</span><span class="sxs-lookup"><span data-stu-id="75d6a-106">Create a new operationalization cluster from cmdlet input parameters.</span></span>
```
New-AzureRmMlOpCluster -ResourceGroupName <String> -Name <String> -Location <String> -ClusterType <String>
 [-OrchestratorType <String>] [-ServicePrincipalName <String>] [-ServicePrincipalSecret <String>]
 [-Description <String>] [-MasterCount <Int32>] [-AgentCount <Int32>] [-AgentVmSize <String>]
 [-GlobalServiceConfigurationETag <String>] [-SslStatus <String>] [-SslCertificate <String>] [-SslKey <String>]
 [-SslCName <String>] [-StorageAccount <String>] [-AzureContainerRegistry <String>]
 [-GlobalServiceConfigurationAdditionalProperties <Hashtable>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="75d6a-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="75d6a-107">DESCRIPTION</span></span>
<span data-ttu-id="75d6a-108">Создание нового кластера для выоперационных операций.</span><span class="sxs-lookup"><span data-stu-id="75d6a-108">Creates a new operationalization cluster.</span></span> <span data-ttu-id="75d6a-109">При этом будет создан объект кластера, служба контейнеров (при необходимости), Application Insights и реестр контейнера Azure.</span><span class="sxs-lookup"><span data-stu-id="75d6a-109">This will create a cluster object, a container service if needed, application insights, and an azure container registry.</span></span>

## <span data-ttu-id="75d6a-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="75d6a-110">EXAMPLES</span></span>

### <span data-ttu-id="75d6a-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="75d6a-111">Example 1</span></span>
```
PS C:\> New-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster -Location "East US 2" -ClusterType "ACS" -OrchestratorType "Kubernetes" -ClientId "abc" -Secret "xyz"
```

<span data-ttu-id="75d6a-112">Создание нового кластера операций с помощью службы контейнеров Azure и Kubernetes в качестве Orchestrator.</span><span class="sxs-lookup"><span data-stu-id="75d6a-112">Creates a new operationalization cluster with azure container service and Kubernetes as the orchestrator.</span></span>

### <span data-ttu-id="75d6a-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="75d6a-113">Example 2</span></span>
```
PS C:\> New-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster -Location "East US 2" -ClusterType "Local"
```

<span data-ttu-id="75d6a-114">Создание нового кластера для функционирования на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="75d6a-114">Creates a new operationalization cluster locally.</span></span> <span data-ttu-id="75d6a-115">Это приведет к созданию реестра контейнера Azure, Application Insights и учетной записи хранилища, но не создает службу контейнеров.</span><span class="sxs-lookup"><span data-stu-id="75d6a-115">This creates an azure container registry, application insights, and storage account, but does not create a container service.</span></span>

## <span data-ttu-id="75d6a-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="75d6a-116">PARAMETERS</span></span>

### <span data-ttu-id="75d6a-117">-AgentCount</span><span class="sxs-lookup"><span data-stu-id="75d6a-117">-AgentCount</span></span>
<span data-ttu-id="75d6a-118">Количество узлов агента в кластере ACS.</span><span class="sxs-lookup"><span data-stu-id="75d6a-118">The number of agent nodes in the ACS cluster.</span></span>

```yaml
Type: Int32
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75d6a-119">-AgentVmSize</span><span class="sxs-lookup"><span data-stu-id="75d6a-119">-AgentVmSize</span></span>
<span data-ttu-id="75d6a-120">Количество узлов агента в кластере ACS.</span><span class="sxs-lookup"><span data-stu-id="75d6a-120">The number of agent nodes in the ACS cluster.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75d6a-121">-AzureContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="75d6a-121">-AzureContainerRegistry</span></span>
<span data-ttu-id="75d6a-122">Универсальный код ресурса (URI) контейнера Azure, который необходимо использовать вместо его создания.</span><span class="sxs-lookup"><span data-stu-id="75d6a-122">The URI to the azure container registry to use instead of creating one.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75d6a-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="75d6a-123">-InputObject</span></span>
<span data-ttu-id="75d6a-124">Свойства кластера для операционной работы.</span><span class="sxs-lookup"><span data-stu-id="75d6a-124">The operationalization cluster properties.</span></span>

```yaml
Type: PSOperationalizationCluster
Parameter Sets: Create a new operationalization cluster from an OperationalizationCluster instance definition.
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75d6a-125">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="75d6a-125">-ClusterType</span></span>
<span data-ttu-id="75d6a-126">Тип кластера для операционной работы.</span><span class="sxs-lookup"><span data-stu-id="75d6a-126">The operationalization cluster type.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75d6a-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="75d6a-127">-Confirm</span></span>
<span data-ttu-id="75d6a-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="75d6a-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75d6a-129">-Описание</span><span class="sxs-lookup"><span data-stu-id="75d6a-129">-Description</span></span>
<span data-ttu-id="75d6a-130">Количество главных узлов в кластере ACS.</span><span class="sxs-lookup"><span data-stu-id="75d6a-130">The number of master nodes in the ACS cluster.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75d6a-131">-GlobalServiceConfigurationAdditionalProperties</span><span class="sxs-lookup"><span data-stu-id="75d6a-131">-GlobalServiceConfigurationAdditionalProperties</span></span>
<span data-ttu-id="75d6a-132">Дополнительные свойства для глобальной конфигурации службы.</span><span class="sxs-lookup"><span data-stu-id="75d6a-132">Additional properties for the global service configuration.</span></span>

```yaml
Type: Hashtable
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75d6a-133">-GlobalServiceConfigurationETag</span><span class="sxs-lookup"><span data-stu-id="75d6a-133">-GlobalServiceConfigurationETag</span></span>
<span data-ttu-id="75d6a-134">Тег ETag конфигурации для обновлений.</span><span class="sxs-lookup"><span data-stu-id="75d6a-134">The configuration ETag for updates.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75d6a-135">-Location</span><span class="sxs-lookup"><span data-stu-id="75d6a-135">-Location</span></span>
<span data-ttu-id="75d6a-136">Расположение кластера для операций.</span><span class="sxs-lookup"><span data-stu-id="75d6a-136">The operationalization cluster's location.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75d6a-137">-MasterCount</span><span class="sxs-lookup"><span data-stu-id="75d6a-137">-MasterCount</span></span>
<span data-ttu-id="75d6a-138">Количество главных узлов в кластере ACS.</span><span class="sxs-lookup"><span data-stu-id="75d6a-138">The number of master nodes in the ACS cluster.</span></span>

```yaml
Type: Int32
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75d6a-139">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="75d6a-139">-Name</span></span>
<span data-ttu-id="75d6a-140">Название кластера операций.</span><span class="sxs-lookup"><span data-stu-id="75d6a-140">The name of the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75d6a-141">-OrchestratorType</span><span class="sxs-lookup"><span data-stu-id="75d6a-141">-OrchestratorType</span></span>
<span data-ttu-id="75d6a-142">Тип Orchestrator кластера ACS.</span><span class="sxs-lookup"><span data-stu-id="75d6a-142">The ACS cluster's orchestrator type.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75d6a-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75d6a-143">-ResourceGroupName</span></span>
<span data-ttu-id="75d6a-144">Имя группы ресурсов для кластера операций.</span><span class="sxs-lookup"><span data-stu-id="75d6a-144">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75d6a-145">-ClientId</span><span class="sxs-lookup"><span data-stu-id="75d6a-145">-ClientId</span></span>
<span data-ttu-id="75d6a-146">Идентификатор субъекта-службы Orchestrator в кластере ACS.</span><span class="sxs-lookup"><span data-stu-id="75d6a-146">The ACS cluster's orchestrator service principal id.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75d6a-147">-Secret (секретный)</span><span class="sxs-lookup"><span data-stu-id="75d6a-147">-Secret</span></span>
<span data-ttu-id="75d6a-148">Секретный ключ службы Orchestrator в кластере ACS.</span><span class="sxs-lookup"><span data-stu-id="75d6a-148">The ACS cluster's orchestrator service principal secret.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75d6a-149">-SslCName</span><span class="sxs-lookup"><span data-stu-id="75d6a-149">-SslCName</span></span>
<span data-ttu-id="75d6a-150">CName-запись сертификата SSL.</span><span class="sxs-lookup"><span data-stu-id="75d6a-150">The CName for the SSL certificate.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75d6a-151">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="75d6a-151">-SslCertificate</span></span>
<span data-ttu-id="75d6a-152">Данные SSL-сертификата в формате PEM кодируются как строка Base64.</span><span class="sxs-lookup"><span data-stu-id="75d6a-152">The SSL certificate data in PEM format encoded as base64 string.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75d6a-153">-SslKey</span><span class="sxs-lookup"><span data-stu-id="75d6a-153">-SslKey</span></span>
<span data-ttu-id="75d6a-154">Данные ключа SSL в формате PEM кодируются как строка Base64.</span><span class="sxs-lookup"><span data-stu-id="75d6a-154">The SSL key data in PEM format encoded as base64 string.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75d6a-155">-SslStatus</span><span class="sxs-lookup"><span data-stu-id="75d6a-155">-SslStatus</span></span>
<span data-ttu-id="75d6a-156">Состояние SSL.</span><span class="sxs-lookup"><span data-stu-id="75d6a-156">SSL status.</span></span>
<span data-ttu-id="75d6a-157">Возможны значения "включено" и "отключено".</span><span class="sxs-lookup"><span data-stu-id="75d6a-157">Possible values are 'Enabled' and 'Disabled'.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75d6a-158">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="75d6a-158">-StorageAccount</span></span>
<span data-ttu-id="75d6a-159">Универсальный код ресурса (URI) для учетной записи хранения, который будет использоваться вместо создания.</span><span class="sxs-lookup"><span data-stu-id="75d6a-159">The URI to the storage account to use instead of creating one.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75d6a-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75d6a-160">-WhatIf</span></span>
<span data-ttu-id="75d6a-161">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="75d6a-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75d6a-162">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="75d6a-162">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="75d6a-163">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="75d6a-163">INPUTS</span></span>

### <span data-ttu-id="75d6a-164">Ничего</span><span class="sxs-lookup"><span data-stu-id="75d6a-164">None</span></span>


## <span data-ttu-id="75d6a-165">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="75d6a-165">OUTPUTS</span></span>

### <span data-ttu-id="75d6a-166">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="75d6a-166">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>


## <span data-ttu-id="75d6a-167">Пуск</span><span class="sxs-lookup"><span data-stu-id="75d6a-167">NOTES</span></span>

## <span data-ttu-id="75d6a-168">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="75d6a-168">RELATED LINKS</span></span>


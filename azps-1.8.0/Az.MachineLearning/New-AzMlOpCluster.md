---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearningCompute.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/new-azmlopcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlOpCluster.md
ms.openlocfilehash: 51c8beb396bb0795fa77431a256ddc38e4e8df38
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93899758"
---
# <span data-ttu-id="c7509-101">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="c7509-101">New-AzMlOpCluster</span></span>

## <span data-ttu-id="c7509-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c7509-102">SYNOPSIS</span></span>
<span data-ttu-id="c7509-103">Создание нового кластера для выоперационных операций.</span><span class="sxs-lookup"><span data-stu-id="c7509-103">Creates a new operationalization cluster.</span></span>

## <span data-ttu-id="c7509-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c7509-104">SYNTAX</span></span>

### <span data-ttu-id="c7509-105">CreateWithInputObject</span><span class="sxs-lookup"><span data-stu-id="c7509-105">CreateWithInputObject</span></span>
```
New-AzMlOpCluster -ResourceGroupName <String> -Name <String> -InputObject <PSOperationalizationCluster>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7509-106">CreateWithParameters</span><span class="sxs-lookup"><span data-stu-id="c7509-106">CreateWithParameters</span></span>
```
New-AzMlOpCluster -ResourceGroupName <String> -Name <String> -Location <String> -ClusterType <String>
 [-OrchestratorType <String>] [-ClientId <String>] [-Secret <String>] [-Description <String>]
 [-MasterCount <Int32>] [-AgentCount <Int32>] [-AgentVmSize <String>]
 [-GlobalServiceConfigurationETag <String>] [-SslStatus <String>] [-SslCertificate <String>] [-SslKey <String>]
 [-SslCName <String>] [-StorageAccount <String>] [-AzureContainerRegistry <String>]
 [-DefaultProfile <IAzureContextContainer>] [-GlobalServiceConfigurationAdditionalProperties <Hashtable>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c7509-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c7509-107">DESCRIPTION</span></span>
<span data-ttu-id="c7509-108">Создание нового кластера для выоперационных операций.</span><span class="sxs-lookup"><span data-stu-id="c7509-108">Creates a new operationalization cluster.</span></span> <span data-ttu-id="c7509-109">При этом будет создан объект кластера, служба контейнеров (при необходимости), Application Insights и реестр контейнера Azure.</span><span class="sxs-lookup"><span data-stu-id="c7509-109">This will create a cluster object, a container service if needed, application insights, and an azure container registry.</span></span>

## <span data-ttu-id="c7509-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c7509-110">EXAMPLES</span></span>

### <span data-ttu-id="c7509-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c7509-111">Example 1</span></span>
```
PS C:\> New-AzMlOpCluster -ResourceGroupName my-group -Name my-cluster -Location "East US 2" -ClusterType "ACS" -OrchestratorType "Kubernetes" -ClientId "abc" -Secret "xyz"
```

<span data-ttu-id="c7509-112">Создание нового кластера операций с помощью службы контейнеров Azure и Kubernetes в качестве Orchestrator.</span><span class="sxs-lookup"><span data-stu-id="c7509-112">Creates a new operationalization cluster with azure container service and Kubernetes as the orchestrator.</span></span>

### <span data-ttu-id="c7509-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="c7509-113">Example 2</span></span>
```
PS C:\> New-AzMlOpCluster -ResourceGroupName my-group -Name my-cluster -Location "East US 2" -ClusterType "Local"
```

<span data-ttu-id="c7509-114">Создание нового кластера для функционирования на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="c7509-114">Creates a new operationalization cluster locally.</span></span> <span data-ttu-id="c7509-115">Это приведет к созданию реестра контейнера Azure, Application Insights и учетной записи хранилища, но не создает службу контейнеров.</span><span class="sxs-lookup"><span data-stu-id="c7509-115">This creates an azure container registry, application insights, and storage account, but does not create a container service.</span></span>

## <span data-ttu-id="c7509-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c7509-116">PARAMETERS</span></span>

### <span data-ttu-id="c7509-117">-AgentCount</span><span class="sxs-lookup"><span data-stu-id="c7509-117">-AgentCount</span></span>
<span data-ttu-id="c7509-118">Количество узлов агента в кластере ACS.</span><span class="sxs-lookup"><span data-stu-id="c7509-118">The number of agent nodes in the ACS cluster.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7509-119">-AgentVmSize</span><span class="sxs-lookup"><span data-stu-id="c7509-119">-AgentVmSize</span></span>
<span data-ttu-id="c7509-120">Количество узлов агента в кластере ACS.</span><span class="sxs-lookup"><span data-stu-id="c7509-120">The number of agent nodes in the ACS cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7509-121">-AzureContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="c7509-121">-AzureContainerRegistry</span></span>
<span data-ttu-id="c7509-122">Универсальный код ресурса (URI) контейнера Azure, который необходимо использовать вместо его создания.</span><span class="sxs-lookup"><span data-stu-id="c7509-122">The URI to the azure container registry to use instead of creating one.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7509-123">-ClientId</span><span class="sxs-lookup"><span data-stu-id="c7509-123">-ClientId</span></span>
<span data-ttu-id="c7509-124">Идентификатор субъекта-службы Orchestrator в кластере ACS.</span><span class="sxs-lookup"><span data-stu-id="c7509-124">The ACS cluster's orchestrator service principal id.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7509-125">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="c7509-125">-ClusterType</span></span>
<span data-ttu-id="c7509-126">Тип кластера для операционной работы.</span><span class="sxs-lookup"><span data-stu-id="c7509-126">The operationalization cluster type.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7509-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7509-127">-DefaultProfile</span></span>
<span data-ttu-id="c7509-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c7509-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c7509-129">-Описание</span><span class="sxs-lookup"><span data-stu-id="c7509-129">-Description</span></span>
<span data-ttu-id="c7509-130">Количество главных узлов в кластере ACS.</span><span class="sxs-lookup"><span data-stu-id="c7509-130">The number of master nodes in the ACS cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7509-131">-GlobalServiceConfigurationAdditionalProperties</span><span class="sxs-lookup"><span data-stu-id="c7509-131">-GlobalServiceConfigurationAdditionalProperties</span></span>
<span data-ttu-id="c7509-132">Дополнительные свойства для глобальной конфигурации службы.</span><span class="sxs-lookup"><span data-stu-id="c7509-132">Additional properties for the global service configuration.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7509-133">-GlobalServiceConfigurationETag</span><span class="sxs-lookup"><span data-stu-id="c7509-133">-GlobalServiceConfigurationETag</span></span>
<span data-ttu-id="c7509-134">Тег ETag конфигурации для обновлений.</span><span class="sxs-lookup"><span data-stu-id="c7509-134">The configuration ETag for updates.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7509-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c7509-135">-InputObject</span></span>
<span data-ttu-id="c7509-136">Свойства кластера для операционной работы.</span><span class="sxs-lookup"><span data-stu-id="c7509-136">The operationalization cluster properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster
Parameter Sets: CreateWithInputObject
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7509-137">-Location</span><span class="sxs-lookup"><span data-stu-id="c7509-137">-Location</span></span>
<span data-ttu-id="c7509-138">Расположение кластера для операций.</span><span class="sxs-lookup"><span data-stu-id="c7509-138">The operationalization cluster's location.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7509-139">-MasterCount</span><span class="sxs-lookup"><span data-stu-id="c7509-139">-MasterCount</span></span>
<span data-ttu-id="c7509-140">Количество главных узлов в кластере ACS.</span><span class="sxs-lookup"><span data-stu-id="c7509-140">The number of master nodes in the ACS cluster.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7509-141">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c7509-141">-Name</span></span>
<span data-ttu-id="c7509-142">Название кластера операций.</span><span class="sxs-lookup"><span data-stu-id="c7509-142">The name of the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7509-143">-OrchestratorType</span><span class="sxs-lookup"><span data-stu-id="c7509-143">-OrchestratorType</span></span>
<span data-ttu-id="c7509-144">Тип Orchestrator кластера ACS.</span><span class="sxs-lookup"><span data-stu-id="c7509-144">The ACS cluster's orchestrator type.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7509-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7509-145">-ResourceGroupName</span></span>
<span data-ttu-id="c7509-146">Имя группы ресурсов для кластера операций.</span><span class="sxs-lookup"><span data-stu-id="c7509-146">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7509-147">-Secret (секретный)</span><span class="sxs-lookup"><span data-stu-id="c7509-147">-Secret</span></span>
<span data-ttu-id="c7509-148">Секретный ключ службы Orchestrator в кластере ACS.</span><span class="sxs-lookup"><span data-stu-id="c7509-148">The ACS cluster's orchestrator service principal secret.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7509-149">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="c7509-149">-SslCertificate</span></span>
<span data-ttu-id="c7509-150">Данные SSL-сертификата в формате PEM кодируются как строка Base64.</span><span class="sxs-lookup"><span data-stu-id="c7509-150">The SSL certificate data in PEM format encoded as base64 string.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7509-151">-SslCName</span><span class="sxs-lookup"><span data-stu-id="c7509-151">-SslCName</span></span>
<span data-ttu-id="c7509-152">CName-запись сертификата SSL.</span><span class="sxs-lookup"><span data-stu-id="c7509-152">The CName for the SSL certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7509-153">-SslKey</span><span class="sxs-lookup"><span data-stu-id="c7509-153">-SslKey</span></span>
<span data-ttu-id="c7509-154">Данные ключа SSL в формате PEM кодируются как строка Base64.</span><span class="sxs-lookup"><span data-stu-id="c7509-154">The SSL key data in PEM format encoded as base64 string.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7509-155">-SslStatus</span><span class="sxs-lookup"><span data-stu-id="c7509-155">-SslStatus</span></span>
<span data-ttu-id="c7509-156">Состояние SSL.</span><span class="sxs-lookup"><span data-stu-id="c7509-156">SSL status.</span></span>
<span data-ttu-id="c7509-157">Возможны значения "включено" и "отключено".</span><span class="sxs-lookup"><span data-stu-id="c7509-157">Possible values are 'Enabled' and 'Disabled'.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7509-158">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="c7509-158">-StorageAccount</span></span>
<span data-ttu-id="c7509-159">Универсальный код ресурса (URI) для учетной записи хранения, который будет использоваться вместо создания.</span><span class="sxs-lookup"><span data-stu-id="c7509-159">The URI to the storage account to use instead of creating one.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7509-160">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c7509-160">-Confirm</span></span>
<span data-ttu-id="c7509-161">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c7509-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7509-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7509-162">-WhatIf</span></span>
<span data-ttu-id="c7509-163">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c7509-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7509-164">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c7509-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7509-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7509-165">CommonParameters</span></span>
<span data-ttu-id="c7509-166">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c7509-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7509-167">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7509-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7509-168">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c7509-168">INPUTS</span></span>

### <span data-ttu-id="c7509-169">Ничего</span><span class="sxs-lookup"><span data-stu-id="c7509-169">None</span></span>

## <span data-ttu-id="c7509-170">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c7509-170">OUTPUTS</span></span>

### <span data-ttu-id="c7509-171">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="c7509-171">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

## <span data-ttu-id="c7509-172">Пуск</span><span class="sxs-lookup"><span data-stu-id="c7509-172">NOTES</span></span>

## <span data-ttu-id="c7509-173">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c7509-173">RELATED LINKS</span></span>

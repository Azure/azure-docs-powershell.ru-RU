---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearningcompute/new-azurermmlopcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/New-AzureRmMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/New-AzureRmMlOpCluster.md
ms.openlocfilehash: 8e93847c3a6d993c689d0ac8c40327ddfcbe76af
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567980"
---
# <span data-ttu-id="75c26-101">New-AzureRmMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="75c26-101">New-AzureRmMlOpCluster</span></span>

## <span data-ttu-id="75c26-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="75c26-102">SYNOPSIS</span></span>
<span data-ttu-id="75c26-103">Создание нового кластера для выоперационных операций.</span><span class="sxs-lookup"><span data-stu-id="75c26-103">Creates a new operationalization cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="75c26-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="75c26-104">SYNTAX</span></span>

### <span data-ttu-id="75c26-105">CreateWithInputObject</span><span class="sxs-lookup"><span data-stu-id="75c26-105">CreateWithInputObject</span></span>
```
New-AzureRmMlOpCluster -ResourceGroupName <String> -Name <String> -InputObject <PSOperationalizationCluster>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75c26-106">CreateWithParameters</span><span class="sxs-lookup"><span data-stu-id="75c26-106">CreateWithParameters</span></span>
```
New-AzureRmMlOpCluster -ResourceGroupName <String> -Name <String> -Location <String> -ClusterType <String>
 [-OrchestratorType <String>] [-ClientId <String>] [-Secret <String>] [-Description <String>]
 [-MasterCount <Int32>] [-AgentCount <Int32>] [-AgentVmSize <String>]
 [-GlobalServiceConfigurationETag <String>] [-SslStatus <String>] [-SslCertificate <String>] [-SslKey <String>]
 [-SslCName <String>] [-StorageAccount <String>] [-AzureContainerRegistry <String>]
 [-DefaultProfile <IAzureContextContainer>] [-GlobalServiceConfigurationAdditionalProperties <Hashtable>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75c26-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="75c26-107">DESCRIPTION</span></span>
<span data-ttu-id="75c26-108">Создание нового кластера для выоперационных операций.</span><span class="sxs-lookup"><span data-stu-id="75c26-108">Creates a new operationalization cluster.</span></span> <span data-ttu-id="75c26-109">При этом будет создан объект кластера, служба контейнеров (при необходимости), Application Insights и реестр контейнера Azure.</span><span class="sxs-lookup"><span data-stu-id="75c26-109">This will create a cluster object, a container service if needed, application insights, and an azure container registry.</span></span>

## <span data-ttu-id="75c26-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="75c26-110">EXAMPLES</span></span>

### <span data-ttu-id="75c26-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="75c26-111">Example 1</span></span>
```
PS C:\> New-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster -Location "East US 2" -ClusterType "ACS" -OrchestratorType "Kubernetes" -ClientId "abc" -Secret "xyz"
```

<span data-ttu-id="75c26-112">Создание нового кластера операций с помощью службы контейнеров Azure и Kubernetes в качестве Orchestrator.</span><span class="sxs-lookup"><span data-stu-id="75c26-112">Creates a new operationalization cluster with azure container service and Kubernetes as the orchestrator.</span></span>

### <span data-ttu-id="75c26-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="75c26-113">Example 2</span></span>
```
PS C:\> New-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster -Location "East US 2" -ClusterType "Local"
```

<span data-ttu-id="75c26-114">Создание нового кластера для функционирования на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="75c26-114">Creates a new operationalization cluster locally.</span></span> <span data-ttu-id="75c26-115">Это приведет к созданию реестра контейнера Azure, Application Insights и учетной записи хранилища, но не создает службу контейнеров.</span><span class="sxs-lookup"><span data-stu-id="75c26-115">This creates an azure container registry, application insights, and storage account, but does not create a container service.</span></span>

## <span data-ttu-id="75c26-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="75c26-116">PARAMETERS</span></span>

### <span data-ttu-id="75c26-117">-AgentCount</span><span class="sxs-lookup"><span data-stu-id="75c26-117">-AgentCount</span></span>
<span data-ttu-id="75c26-118">Количество узлов агента в кластере ACS.</span><span class="sxs-lookup"><span data-stu-id="75c26-118">The number of agent nodes in the ACS cluster.</span></span>

```yaml
Type: Int32
Parameter Sets: CreateWithParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75c26-119">-AgentVmSize</span><span class="sxs-lookup"><span data-stu-id="75c26-119">-AgentVmSize</span></span>
<span data-ttu-id="75c26-120">Количество узлов агента в кластере ACS.</span><span class="sxs-lookup"><span data-stu-id="75c26-120">The number of agent nodes in the ACS cluster.</span></span>

```yaml
Type: String
Parameter Sets: CreateWithParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75c26-121">-AzureContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="75c26-121">-AzureContainerRegistry</span></span>
<span data-ttu-id="75c26-122">Универсальный код ресурса (URI) контейнера Azure, который необходимо использовать вместо его создания.</span><span class="sxs-lookup"><span data-stu-id="75c26-122">The URI to the azure container registry to use instead of creating one.</span></span>

```yaml
Type: String
Parameter Sets: CreateWithParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75c26-123">-ClientId</span><span class="sxs-lookup"><span data-stu-id="75c26-123">-ClientId</span></span>
<span data-ttu-id="75c26-124">Идентификатор субъекта-службы Orchestrator в кластере ACS.</span><span class="sxs-lookup"><span data-stu-id="75c26-124">The ACS cluster's orchestrator service principal id.</span></span>

```yaml
Type: String
Parameter Sets: CreateWithParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75c26-125">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="75c26-125">-ClusterType</span></span>
<span data-ttu-id="75c26-126">Тип кластера для операционной работы.</span><span class="sxs-lookup"><span data-stu-id="75c26-126">The operationalization cluster type.</span></span>

```yaml
Type: String
Parameter Sets: CreateWithParameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75c26-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75c26-127">-DefaultProfile</span></span>
<span data-ttu-id="75c26-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="75c26-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75c26-129">-Описание</span><span class="sxs-lookup"><span data-stu-id="75c26-129">-Description</span></span>
<span data-ttu-id="75c26-130">Количество главных узлов в кластере ACS.</span><span class="sxs-lookup"><span data-stu-id="75c26-130">The number of master nodes in the ACS cluster.</span></span>

```yaml
Type: String
Parameter Sets: CreateWithParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75c26-131">-GlobalServiceConfigurationAdditionalProperties</span><span class="sxs-lookup"><span data-stu-id="75c26-131">-GlobalServiceConfigurationAdditionalProperties</span></span>
<span data-ttu-id="75c26-132">Дополнительные свойства для глобальной конфигурации службы.</span><span class="sxs-lookup"><span data-stu-id="75c26-132">Additional properties for the global service configuration.</span></span>

```yaml
Type: Hashtable
Parameter Sets: CreateWithParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75c26-133">-GlobalServiceConfigurationETag</span><span class="sxs-lookup"><span data-stu-id="75c26-133">-GlobalServiceConfigurationETag</span></span>
<span data-ttu-id="75c26-134">Тег ETag конфигурации для обновлений.</span><span class="sxs-lookup"><span data-stu-id="75c26-134">The configuration ETag for updates.</span></span>

```yaml
Type: String
Parameter Sets: CreateWithParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75c26-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="75c26-135">-InputObject</span></span>
<span data-ttu-id="75c26-136">Свойства кластера для операционной работы.</span><span class="sxs-lookup"><span data-stu-id="75c26-136">The operationalization cluster properties.</span></span>

```yaml
Type: PSOperationalizationCluster
Parameter Sets: CreateWithInputObject
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75c26-137">-Location</span><span class="sxs-lookup"><span data-stu-id="75c26-137">-Location</span></span>
<span data-ttu-id="75c26-138">Расположение кластера для операций.</span><span class="sxs-lookup"><span data-stu-id="75c26-138">The operationalization cluster's location.</span></span>

```yaml
Type: String
Parameter Sets: CreateWithParameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75c26-139">-MasterCount</span><span class="sxs-lookup"><span data-stu-id="75c26-139">-MasterCount</span></span>
<span data-ttu-id="75c26-140">Количество главных узлов в кластере ACS.</span><span class="sxs-lookup"><span data-stu-id="75c26-140">The number of master nodes in the ACS cluster.</span></span>

```yaml
Type: Int32
Parameter Sets: CreateWithParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75c26-141">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="75c26-141">-Name</span></span>
<span data-ttu-id="75c26-142">Название кластера операций.</span><span class="sxs-lookup"><span data-stu-id="75c26-142">The name of the operationalization cluster.</span></span>

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

### <span data-ttu-id="75c26-143">-OrchestratorType</span><span class="sxs-lookup"><span data-stu-id="75c26-143">-OrchestratorType</span></span>
<span data-ttu-id="75c26-144">Тип Orchestrator кластера ACS.</span><span class="sxs-lookup"><span data-stu-id="75c26-144">The ACS cluster's orchestrator type.</span></span>

```yaml
Type: String
Parameter Sets: CreateWithParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75c26-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75c26-145">-ResourceGroupName</span></span>
<span data-ttu-id="75c26-146">Имя группы ресурсов для кластера операций.</span><span class="sxs-lookup"><span data-stu-id="75c26-146">The name of the resource group for the operationalization cluster.</span></span>

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

### <span data-ttu-id="75c26-147">-Secret (секретный)</span><span class="sxs-lookup"><span data-stu-id="75c26-147">-Secret</span></span>
<span data-ttu-id="75c26-148">Секретный ключ службы Orchestrator в кластере ACS.</span><span class="sxs-lookup"><span data-stu-id="75c26-148">The ACS cluster's orchestrator service principal secret.</span></span>

```yaml
Type: String
Parameter Sets: CreateWithParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75c26-149">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="75c26-149">-SslCertificate</span></span>
<span data-ttu-id="75c26-150">Данные SSL-сертификата в формате PEM кодируются как строка Base64.</span><span class="sxs-lookup"><span data-stu-id="75c26-150">The SSL certificate data in PEM format encoded as base64 string.</span></span>

```yaml
Type: String
Parameter Sets: CreateWithParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75c26-151">-SslCName</span><span class="sxs-lookup"><span data-stu-id="75c26-151">-SslCName</span></span>
<span data-ttu-id="75c26-152">CName-запись сертификата SSL.</span><span class="sxs-lookup"><span data-stu-id="75c26-152">The CName for the SSL certificate.</span></span>

```yaml
Type: String
Parameter Sets: CreateWithParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75c26-153">-SslKey</span><span class="sxs-lookup"><span data-stu-id="75c26-153">-SslKey</span></span>
<span data-ttu-id="75c26-154">Данные ключа SSL в формате PEM кодируются как строка Base64.</span><span class="sxs-lookup"><span data-stu-id="75c26-154">The SSL key data in PEM format encoded as base64 string.</span></span>

```yaml
Type: String
Parameter Sets: CreateWithParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75c26-155">-SslStatus</span><span class="sxs-lookup"><span data-stu-id="75c26-155">-SslStatus</span></span>
<span data-ttu-id="75c26-156">Состояние SSL.</span><span class="sxs-lookup"><span data-stu-id="75c26-156">SSL status.</span></span>
<span data-ttu-id="75c26-157">Возможны значения "включено" и "отключено".</span><span class="sxs-lookup"><span data-stu-id="75c26-157">Possible values are 'Enabled' and 'Disabled'.</span></span>

```yaml
Type: String
Parameter Sets: CreateWithParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75c26-158">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="75c26-158">-StorageAccount</span></span>
<span data-ttu-id="75c26-159">Универсальный код ресурса (URI) для учетной записи хранения, который будет использоваться вместо создания.</span><span class="sxs-lookup"><span data-stu-id="75c26-159">The URI to the storage account to use instead of creating one.</span></span>

```yaml
Type: String
Parameter Sets: CreateWithParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75c26-160">-Confirm</span><span class="sxs-lookup"><span data-stu-id="75c26-160">-Confirm</span></span>
<span data-ttu-id="75c26-161">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="75c26-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75c26-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75c26-162">-WhatIf</span></span>
<span data-ttu-id="75c26-163">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="75c26-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75c26-164">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="75c26-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75c26-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75c26-165">CommonParameters</span></span>
<span data-ttu-id="75c26-166">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="75c26-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75c26-167">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75c26-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75c26-168">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="75c26-168">INPUTS</span></span>

### <span data-ttu-id="75c26-169">Ничего</span><span class="sxs-lookup"><span data-stu-id="75c26-169">None</span></span>

## <span data-ttu-id="75c26-170">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="75c26-170">OUTPUTS</span></span>

### <span data-ttu-id="75c26-171">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="75c26-171">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

## <span data-ttu-id="75c26-172">Пуск</span><span class="sxs-lookup"><span data-stu-id="75c26-172">NOTES</span></span>

## <span data-ttu-id="75c26-173">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="75c26-173">RELATED LINKS</span></span>


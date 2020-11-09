---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapseintegrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseIntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseIntegrationRuntime.md
ms.openlocfilehash: 715b6a52bc2f2a19dbfec3641d54752fe4321011
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245748"
---
# <span data-ttu-id="3076a-101">Set-AzSynapseIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="3076a-101">Set-AzSynapseIntegrationRuntime</span></span>

## <span data-ttu-id="3076a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3076a-102">SYNOPSIS</span></span>
<span data-ttu-id="3076a-103">Обновляет среду выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="3076a-103">Updates an integration runtime.</span></span>

## <span data-ttu-id="3076a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3076a-104">SYNTAX</span></span>

### <span data-ttu-id="3076a-105">SetByIntegrationRuntimeName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3076a-105">SetByIntegrationRuntimeName (Default)</span></span>
```
Set-AzSynapseIntegrationRuntime [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Type <String>] [-Description <String>] [-Location <String>] [-NodeSize <String>] [-NodeCount <Int32>]
 [-CatalogServerEndpoint <String>] [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>]
 [-VNetId <String>] [-Subnet <String>] [-PublicIP <String[]>] [-DataFlowComputeType <String>]
 [-DataFlowCoreCount <Int32>] [-DataFlowTimeToLive <Int32>] [-SetupScriptContainerSasUri <String>]
 [-Edition <String>] [-ExpressCustomSetup <ArrayList>] [-DataProxyIntegrationRuntimeName <String>]
 [-DataProxyStagingLinkedServiceName <String>] [-DataProxyStagingPath <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>] [-AuthKey <SecureString>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3076a-106">SetByLinkedIntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="3076a-106">SetByLinkedIntegrationRuntimeName</span></span>
```
Set-AzSynapseIntegrationRuntime [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Type <String>] [-Description <String>] -SharedIntegrationRuntimeResourceId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3076a-107">SetByParentObject</span><span class="sxs-lookup"><span data-stu-id="3076a-107">SetByParentObject</span></span>
```
Set-AzSynapseIntegrationRuntime -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-Type <String>]
 [-Description <String>] [-Location <String>] [-NodeSize <String>] [-NodeCount <Int32>]
 [-CatalogServerEndpoint <String>] [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>]
 [-VNetId <String>] [-Subnet <String>] [-PublicIP <String[]>] [-DataFlowComputeType <String>]
 [-DataFlowCoreCount <Int32>] [-DataFlowTimeToLive <Int32>] [-SetupScriptContainerSasUri <String>]
 [-Edition <String>] [-ExpressCustomSetup <ArrayList>] [-DataProxyIntegrationRuntimeName <String>]
 [-DataProxyStagingLinkedServiceName <String>] [-DataProxyStagingPath <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>] [-AuthKey <SecureString>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3076a-108">SetByLinkedIntegrationRuntimeParentObject</span><span class="sxs-lookup"><span data-stu-id="3076a-108">SetByLinkedIntegrationRuntimeParentObject</span></span>
```
Set-AzSynapseIntegrationRuntime -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-Type <String>]
 [-Description <String>] -SharedIntegrationRuntimeResourceId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3076a-109">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="3076a-109">SetByResourceId</span></span>
```
Set-AzSynapseIntegrationRuntime -ResourceId <String> [-Type <String>] [-Description <String>]
 [-Location <String>] [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-PublicIP <String[]>] [-DataFlowComputeType <String>] [-DataFlowCoreCount <Int32>]
 [-DataFlowTimeToLive <Int32>] [-SetupScriptContainerSasUri <String>] [-Edition <String>]
 [-ExpressCustomSetup <ArrayList>] [-DataProxyIntegrationRuntimeName <String>]
 [-DataProxyStagingLinkedServiceName <String>] [-DataProxyStagingPath <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>] [-AuthKey <SecureString>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3076a-110">SetByLinkedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="3076a-110">SetByLinkedIntegrationRuntimeResourceId</span></span>
```
Set-AzSynapseIntegrationRuntime -ResourceId <String> [-Type <String>] [-Description <String>]
 -SharedIntegrationRuntimeResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3076a-111">SetByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="3076a-111">SetByIntegrationRuntimeObject</span></span>
```
Set-AzSynapseIntegrationRuntime -InputObject <PSIntegrationRuntime> [-Type <String>] [-Description <String>]
 [-Location <String>] [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-PublicIP <String[]>] [-DataFlowComputeType <String>] [-DataFlowCoreCount <Int32>]
 [-DataFlowTimeToLive <Int32>] [-SetupScriptContainerSasUri <String>] [-Edition <String>]
 [-ExpressCustomSetup <ArrayList>] [-DataProxyIntegrationRuntimeName <String>]
 [-DataProxyStagingLinkedServiceName <String>] [-DataProxyStagingPath <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>] [-AuthKey <SecureString>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3076a-112">SetByLinkedIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="3076a-112">SetByLinkedIntegrationRuntimeObject</span></span>
```
Set-AzSynapseIntegrationRuntime -InputObject <PSIntegrationRuntime> [-Type <String>] [-Description <String>]
 -SharedIntegrationRuntimeResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3076a-113">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3076a-113">DESCRIPTION</span></span>
<span data-ttu-id="3076a-114">Командлет **Set-AzSynapseIntegrationRuntime** обновляет среду выполнения интеграции с определенными параметрами.</span><span class="sxs-lookup"><span data-stu-id="3076a-114">The **Set-AzSynapseIntegrationRuntime** cmdlet updates an integration runtime with specific parameters.</span></span>

## <span data-ttu-id="3076a-115">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3076a-115">EXAMPLES</span></span>

### <span data-ttu-id="3076a-116">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3076a-116">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir' -Description 'New description'
```

<span data-ttu-id="3076a-117">Командлет обновляет описание среды выполнения интеграции с именем Test-SelfHost-IR.</span><span class="sxs-lookup"><span data-stu-id="3076a-117">The cmdlet updates the description of integration runtime named 'test-selfhost-ir'.</span></span>

### <span data-ttu-id="3076a-118">Пример 2</span><span class="sxs-lookup"><span data-stu-id="3076a-118">Example 2</span></span>
```powershell
PS C:\> Set-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir' `
                                        -SharedIntegrationRuntimeResourceId '/subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir' -Type "SelfHosted"
```

<span data-ttu-id="3076a-119">Командлет добавит рабочую область, чтобы использовать общую среду выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="3076a-119">The cmdlet adds the workspace to use the shared integration runtime.</span></span> <span data-ttu-id="3076a-120">При использовании `-SharedIntegrationRuntimeResourceId` параметра `-Type` также необходимо включить.</span><span class="sxs-lookup"><span data-stu-id="3076a-120">When using `-SharedIntegrationRuntimeResourceId` parameter the `-Type` must also be included.</span></span> <span data-ttu-id="3076a-121">Обратите внимание, что рабочей области необходимо предоставить разрешение на использование среды выполнения интеграции перед выполнением командлета.</span><span class="sxs-lookup"><span data-stu-id="3076a-121">Note that the workspace need to be granted permission to use the integration runtime before running cmdlet.</span></span>

## <span data-ttu-id="3076a-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3076a-122">PARAMETERS</span></span>

### <span data-ttu-id="3076a-123">-AuthKey</span><span class="sxs-lookup"><span data-stu-id="3076a-123">-AuthKey</span></span>
<span data-ttu-id="3076a-124">Ключ проверки подлинности на саморазмещенной среде выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="3076a-124">The authentication key of the self-hosted integration runtime.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3076a-125">-CatalogAdminCredential</span><span class="sxs-lookup"><span data-stu-id="3076a-125">-CatalogAdminCredential</span></span>
<span data-ttu-id="3076a-126">Учетные данные администратора базы данных каталога среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="3076a-126">The catalog database administrator credential of the integration runtime.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3076a-127">-CatalogPricingTier</span><span class="sxs-lookup"><span data-stu-id="3076a-127">-CatalogPricingTier</span></span>
<span data-ttu-id="3076a-128">Ценовая категория базы данных каталога в среде выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="3076a-128">The catalog database pricing tier of the integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3076a-129">-CatalogServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="3076a-129">-CatalogServerEndpoint</span></span>
<span data-ttu-id="3076a-130">Конечная точка сервера базы данных каталога среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="3076a-130">The catalog database server endpoint of the integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3076a-131">-DataFlowComputeType</span><span class="sxs-lookup"><span data-stu-id="3076a-131">-DataFlowComputeType</span></span>
<span data-ttu-id="3076a-132">Тип вычисления кластера потоков данных, который будет выполнять задание потока данных.</span><span class="sxs-lookup"><span data-stu-id="3076a-132">Compute type of the data flow cluster which will execute data flow job.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3076a-133">-DataFlowCoreCount</span><span class="sxs-lookup"><span data-stu-id="3076a-133">-DataFlowCoreCount</span></span>
<span data-ttu-id="3076a-134">Число ядер кластера потоков данных, который будет выполнять задание потока данных.</span><span class="sxs-lookup"><span data-stu-id="3076a-134">Core count of the data flow cluster which will execute data flow job.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3076a-135">-DataFlowTimeToLive</span><span class="sxs-lookup"><span data-stu-id="3076a-135">-DataFlowTimeToLive</span></span>
<span data-ttu-id="3076a-136">Параметр время жизни (в минутах) для кластера потоков данных, который будет выполнять задание потока данных.</span><span class="sxs-lookup"><span data-stu-id="3076a-136">Time to live (in minutes) setting of the data flow cluster which will execute data flow job.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3076a-137">-DataProxyIntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="3076a-137">-DataProxyIntegrationRuntimeName</span></span>
<span data-ttu-id="3076a-138">Имя среды выполнения интеграции Self-Hosted, используемое в качестве прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="3076a-138">The Self-Hosted Integration Runtime name which is used as a proxy.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3076a-139">-DataProxyStagingLinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="3076a-139">-DataProxyStagingLinkedServiceName</span></span>
<span data-ttu-id="3076a-140">Имя связанной службы хранилища BLOB-объектов Azure, которое ссылается на промежуточное хранилище данных, которое будет использоваться при переносе данных между Self-Hosted и средой выполнения интеграции Azure-SSIS.</span><span class="sxs-lookup"><span data-stu-id="3076a-140">The Azure Blob Storage Linked Service name that references the staging data store to be used when moving data between Self-Hosted and Azure-SSIS Integration Runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3076a-141">-DataProxyStagingPath</span><span class="sxs-lookup"><span data-stu-id="3076a-141">-DataProxyStagingPath</span></span>
<span data-ttu-id="3076a-142">Путь в хранилище промежуточных данных, который будет использоваться при перемещении данных между Self-Hostedми и средами выполнения интеграции Azure-SSIS, если не указан, будет использоваться контейнер по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3076a-142">The path in staging data store to be used when moving data between Self-Hosted and Azure-SSIS Integration Runtimes, a default container will be used if unspecified.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3076a-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3076a-143">-DefaultProfile</span></span>
<span data-ttu-id="3076a-144">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3076a-144">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3076a-145">-Описание</span><span class="sxs-lookup"><span data-stu-id="3076a-145">-Description</span></span>
<span data-ttu-id="3076a-146">Описание среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="3076a-146">The integration runtime description.</span></span>

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

### <span data-ttu-id="3076a-147">-Edition</span><span class="sxs-lookup"><span data-stu-id="3076a-147">-Edition</span></span>
<span data-ttu-id="3076a-148">Выпуски среды выполнения интеграции служб SSIS, которые могут быть стандартными или корпоративными, по умолчанию используется стандартный, если он не указан.</span><span class="sxs-lookup"><span data-stu-id="3076a-148">The edition for SSIS integration runtime which could be Standard or Enterprise, default is Standard if it is not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:
Accepted values: Standard, Enterprise

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3076a-149">-ExpressCustomSetup</span><span class="sxs-lookup"><span data-stu-id="3076a-149">-ExpressCustomSetup</span></span>
<span data-ttu-id="3076a-150">Быстрая настраиваемая Настройка среды выполнения интеграции служб SSIS, которую можно использовать для настройки конфигураций и сторонних компонентов без специального сценария настройки.</span><span class="sxs-lookup"><span data-stu-id="3076a-150">The express custom setup for SSIS integration runtime which could be used to setup configurations and 3rd party components without custom setup script.</span></span>

```yaml
Type: System.Collections.ArrayList
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3076a-151">-Force</span><span class="sxs-lookup"><span data-stu-id="3076a-151">-Force</span></span>
<span data-ttu-id="3076a-152">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="3076a-152">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="3076a-153">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3076a-153">-InputObject</span></span>
<span data-ttu-id="3076a-154">Объект среды выполнения Integration.</span><span class="sxs-lookup"><span data-stu-id="3076a-154">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime
Parameter Sets: SetByIntegrationRuntimeObject, SetByLinkedIntegrationRuntimeObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3076a-155">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="3076a-155">-LicenseType</span></span>
<span data-ttu-id="3076a-156">Тип лицензии, которую вы хотите выбрать для ИК-связи служб SSIS.</span><span class="sxs-lookup"><span data-stu-id="3076a-156">The license type that you want to select for the SSIS IR.</span></span>
<span data-ttu-id="3076a-157">Существует два типа: LicenseIncluded или BasePrice.</span><span class="sxs-lookup"><span data-stu-id="3076a-157">There are two types: LicenseIncluded or BasePrice.</span></span>
<span data-ttu-id="3076a-158">Если вы ищете цены на использование гибридной льготы для использования Azure (AHUB), пожалуйста, выберите BasePrice.</span><span class="sxs-lookup"><span data-stu-id="3076a-158">If you are qualified for the Azure Hybrid Use Benefit (AHUB) pricing, please select BasePrice.</span></span>
<span data-ttu-id="3076a-159">Если это не так, пожалуйста, выберите LicenseIncluded.</span><span class="sxs-lookup"><span data-stu-id="3076a-159">If not, please select LicenseIncluded.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:
Accepted values: LicenseIncluded, BasePrice

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3076a-160">-Location</span><span class="sxs-lookup"><span data-stu-id="3076a-160">-Location</span></span>
<span data-ttu-id="3076a-161">Описание среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="3076a-161">The integration runtime description.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3076a-162">-MaxParallelExecutionsPerNode</span><span class="sxs-lookup"><span data-stu-id="3076a-162">-MaxParallelExecutionsPerNode</span></span>
<span data-ttu-id="3076a-163">Максимальное количество параллельных выполнений на каждом узле для управляемой среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="3076a-163">Maximum parallel execution count per node for a managed dedicated integration runtime.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3076a-164">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3076a-164">-Name</span></span>
<span data-ttu-id="3076a-165">Имя среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="3076a-165">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByLinkedIntegrationRuntimeName, SetByParentObject, SetByLinkedIntegrationRuntimeParentObject
Aliases: IntegrationRuntimeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3076a-166">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="3076a-166">-NodeCount</span></span>
<span data-ttu-id="3076a-167">Количество целевых узлов в среде выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="3076a-167">Target nodes count of the integration runtime.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3076a-168">-NodeSize</span><span class="sxs-lookup"><span data-stu-id="3076a-168">-NodeSize</span></span>
<span data-ttu-id="3076a-169">Размер узла среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="3076a-169">The integration runtime node size.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3076a-170">-PublicIP</span><span class="sxs-lookup"><span data-stu-id="3076a-170">-PublicIP</span></span>
<span data-ttu-id="3076a-171">Статические общедоступные IP-адреса, которые будут использоваться средой выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="3076a-171">The static public IP addresses which the integration runtime will use.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases: PublicIPs

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3076a-172">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3076a-172">-ResourceGroupName</span></span>
<span data-ttu-id="3076a-173">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3076a-173">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByLinkedIntegrationRuntimeName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3076a-174">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3076a-174">-ResourceId</span></span>
<span data-ttu-id="3076a-175">Идентификатор ресурса среды выполнения интеграции Synapse.</span><span class="sxs-lookup"><span data-stu-id="3076a-175">Resource identifier of Synapse integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId, SetByLinkedIntegrationRuntimeResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3076a-176">-SetupScriptContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="3076a-176">-SetupScriptContainerSasUri</span></span>
<span data-ttu-id="3076a-177">Универсальный код ресурса (URI) SAS контейнера BLOB-объектов Azure, содержащего настраиваемый сценарий настройки.</span><span class="sxs-lookup"><span data-stu-id="3076a-177">The SAS URI of the Azure blob container that contains the custom setup script.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3076a-178">-SharedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="3076a-178">-SharedIntegrationRuntimeResourceId</span></span>
<span data-ttu-id="3076a-179">Идентификатор ресурса общей среды выполнения интеграции с самостоятельным размещением.</span><span class="sxs-lookup"><span data-stu-id="3076a-179">The resource id of the shared self-hosted integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByLinkedIntegrationRuntimeName, SetByLinkedIntegrationRuntimeParentObject, SetByLinkedIntegrationRuntimeResourceId, SetByLinkedIntegrationRuntimeObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3076a-180">-Подсеть</span><span class="sxs-lookup"><span data-stu-id="3076a-180">-Subnet</span></span>
<span data-ttu-id="3076a-181">Имя подсети в виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="3076a-181">The name of the subnet in the VNet.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases: SubnetName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3076a-182">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="3076a-182">-Type</span></span>
<span data-ttu-id="3076a-183">Тип среды выполнения Integration.</span><span class="sxs-lookup"><span data-stu-id="3076a-183">The integration runtime type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Managed, SelfHosted

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3076a-184">-VNetId</span><span class="sxs-lookup"><span data-stu-id="3076a-184">-VNetId</span></span>
<span data-ttu-id="3076a-185">ИДЕНТИФИКАТОР виртуальной сети, к которой будет присоединиться среда выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="3076a-185">The ID of the VNet which the integration runtime will join.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3076a-186">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="3076a-186">-WorkspaceName</span></span>
<span data-ttu-id="3076a-187">Имя Synapse рабочей области.</span><span class="sxs-lookup"><span data-stu-id="3076a-187">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByLinkedIntegrationRuntimeName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3076a-188">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="3076a-188">-WorkspaceObject</span></span>
<span data-ttu-id="3076a-189">объект ввода в рабочую область, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="3076a-189">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByParentObject, SetByLinkedIntegrationRuntimeParentObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3076a-190">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3076a-190">-Confirm</span></span>
<span data-ttu-id="3076a-191">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3076a-191">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3076a-192">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3076a-192">-WhatIf</span></span>
<span data-ttu-id="3076a-193">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3076a-193">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3076a-194">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3076a-194">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3076a-195">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3076a-195">CommonParameters</span></span>
<span data-ttu-id="3076a-196">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3076a-196">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3076a-197">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3076a-197">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3076a-198">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3076a-198">INPUTS</span></span>

### <span data-ttu-id="3076a-199">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="3076a-199">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="3076a-200">Microsoft. Azure. Commands. Synapse. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="3076a-200">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="3076a-201">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3076a-201">OUTPUTS</span></span>

### <span data-ttu-id="3076a-202">Microsoft. Azure. Commands. Synapse. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="3076a-202">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="3076a-203">Пуск</span><span class="sxs-lookup"><span data-stu-id="3076a-203">NOTES</span></span>

## <span data-ttu-id="3076a-204">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3076a-204">RELATED LINKS</span></span>
---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 0a687c1a2c21301ca61d92d7c4701d7b59d227f3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94313751"
---
# <span data-ttu-id="2415e-101">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="2415e-101">Set-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="2415e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2415e-102">SYNOPSIS</span></span>
<span data-ttu-id="2415e-103">Обновляет среду выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="2415e-103">Updates an integration runtime.</span></span>

## <span data-ttu-id="2415e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2415e-104">SYNTAX</span></span>

### <span data-ttu-id="2415e-105">ByIntegrationRuntimeName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2415e-105">ByIntegrationRuntimeName (Default)</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Name] <String> [-Type <String>] [-Description <String>] [-Location <String>] [-NodeSize <String>]
 [-NodeCount <Int32>] [-CatalogServerEndpoint <String>] [-CatalogAdminCredential <PSCredential>]
 [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>] [-PublicIPs <String[]>]
 [-DataFlowComputeType <String>] [-DataFlowCoreCount <Int32>] [-DataFlowTimeToLive <Int32>]
 [-SetupScriptContainerSasUri <String>] [-Edition <String>] [-ExpressCustomSetup <ArrayList>]
 [-DataProxyIntegrationRuntimeName <String>] [-DataProxyStagingLinkedServiceName <String>]
 [-DataProxyStagingPath <String>] [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>]
 [-AuthKey <SecureString>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2415e-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="2415e-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceId] <String> [-Type <String>] [-Description <String>]
 [-Location <String>] [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-PublicIPs <String[]>] [-DataFlowComputeType <String>] [-DataFlowCoreCount <Int32>]
 [-DataFlowTimeToLive <Int32>] [-SetupScriptContainerSasUri <String>] [-Edition <String>]
 [-ExpressCustomSetup <ArrayList>] [-DataProxyIntegrationRuntimeName <String>]
 [-DataProxyStagingLinkedServiceName <String>] [-DataProxyStagingPath <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>] [-AuthKey <SecureString>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2415e-107">ByLinkedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="2415e-107">ByLinkedIntegrationRuntimeResourceId</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceId] <String> [-Type <String>] [-Description <String>]
 -SharedIntegrationRuntimeResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2415e-108">ByLinkedIntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="2415e-108">ByLinkedIntegrationRuntimeName</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Name] <String> [-Type <String>] [-Description <String>] -SharedIntegrationRuntimeResourceId <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2415e-109">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="2415e-109">ByIntegrationRuntimeObject</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-InputObject] <PSIntegrationRuntime> [-Type <String>]
 [-Description <String>] [-Location <String>] [-NodeSize <String>] [-NodeCount <Int32>]
 [-CatalogServerEndpoint <String>] [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>]
 [-VNetId <String>] [-Subnet <String>] [-PublicIPs <String[]>] [-DataFlowComputeType <String>]
 [-DataFlowCoreCount <Int32>] [-DataFlowTimeToLive <Int32>] [-SetupScriptContainerSasUri <String>]
 [-Edition <String>] [-ExpressCustomSetup <ArrayList>] [-DataProxyIntegrationRuntimeName <String>]
 [-DataProxyStagingLinkedServiceName <String>] [-DataProxyStagingPath <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>] [-AuthKey <SecureString>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2415e-110">ByLinkedIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="2415e-110">ByLinkedIntegrationRuntimeObject</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-InputObject] <PSIntegrationRuntime> [-Type <String>]
 [-Description <String>] -SharedIntegrationRuntimeResourceId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2415e-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2415e-111">DESCRIPTION</span></span>
<span data-ttu-id="2415e-112">Командлет Set-AzDataFactoryV2IntegrationRuntime обновляет среду выполнения интеграции с определенными параметрами.</span><span class="sxs-lookup"><span data-stu-id="2415e-112">The Set-AzDataFactoryV2IntegrationRuntime cmdlet updates an integration runtime with specific parameters.</span></span>

## <span data-ttu-id="2415e-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2415e-113">EXAMPLES</span></span>

### <span data-ttu-id="2415e-114">Пример 1: Описание обновления среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="2415e-114">Example 1: Update integration runtime description.</span></span>
```
PS C:\> Set-AzDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' `
                                            -Description 'New description'

    Id                : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
    ResourceGroupName : rg-test-dfv2
    DataFactoryName   : test-df-eu2
    Name              : test-selfhost-ir
    Description       : New description
```

<span data-ttu-id="2415e-115">Командлет обновляет описание среды выполнения интеграции с именем Test-SelfHost-IR.</span><span class="sxs-lookup"><span data-stu-id="2415e-115">The cmdlet updates the description of integration runtime named 'test-selfhost-ir'.</span></span>

### <span data-ttu-id="2415e-116">Пример 2: общий доступ к среде выполнения интеграции с самостоятельным размещением.</span><span class="sxs-lookup"><span data-stu-id="2415e-116">Example 2: Share Self-hosted integration runtime.</span></span>
```
PS C:\> Set-AzDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' `
                                            -SharedIntegrationRuntimeResourceId '/subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir' -Type "SelfHosted"

    Id                : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
    ResourceGroupName : rg-test-dfv2
    DataFactoryName   : test-df-eu2
    Name              : test-selfhost-ir
    Description       : New description
```

<span data-ttu-id="2415e-117">Командлет добавляет файл ADF для использования общей среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="2415e-117">The cmdlet adds the ADF to use the shared integration runtime.</span></span> <span data-ttu-id="2415e-118">При использовании `-SharedIntegrationRuntimeResourceId` параметра `-Type` также необходимо включить.</span><span class="sxs-lookup"><span data-stu-id="2415e-118">When using `-SharedIntegrationRuntimeResourceId` parameter the `-Type` must also be included.</span></span> <span data-ttu-id="2415e-119">Обратите внимание, что необходимо предоставить фабрике данных разрешение на использование среды выполнения интеграции перед выполнением командлета.</span><span class="sxs-lookup"><span data-stu-id="2415e-119">Note that the data factory need to be granted permission to use the integration runtime before running cmdlet.</span></span>

### <span data-ttu-id="2415e-120">Пример 3: Настройка Self-Hosted инфракрасной связи в качестве прокси-сервера для службы Azure-SSIS IR в ADF.</span><span class="sxs-lookup"><span data-stu-id="2415e-120">Example 3: Configure Self-Hosted IR as a proxy for Azure-SSIS IR in ADF.</span></span>
```
PS C:\> Set-AzDataFactoryV2IntegrationRuntime -ResourceGroupName testgroup `
                                           -DataFactoryName testdf `
                                           -Name SSISIRWithDataProxy `
                                           -DataProxyIntegrationRuntimeName proxySelfhostedIR `
                                           -DataProxyStagingLinkedServiceName AzureBlobStorage `
                                           -DataProxyStagingPath teststaging

    Location                          : EastUS
    NodeSize                          : Standard_D8_v3
    NodeCount                         : 1
    MaxParallelExecutionsPerNode      : 8
    CatalogServerEndpoint             : 
    CatalogAdminUserName              : 
    CatalogAdminPassword              : 
    CatalogPricingTier                : 
    VNetId                            : 
    Subnet                            : 
    PublicIPs                         : 
    State                             : Initial
    LicenseType                       : LicenseIncluded
    SetupScriptContainerSasUri        : 
    DataProxyIntegrationRuntimeName   : proxySelfhostedIR
    DataProxyStagingLinkedServiceName : AzureBlobStorage
    DataProxyStagingPath              : 
    Edition                           : Standard
    Name                              : SSISIRWithDataProxy
    Type                              : Managed
    ResourceGroupName                 : testgroup
    DataFactoryName                   : testdf
    Description                       : 
    Id                                : /subscriptions/cb715d05-3337-4640-8c43-4f943c50d06e/resourceGroups/testgroup/providers/Microsoft.DataFactory/factories/testdf/integrationruntimes/SSISIRWithDataProxy
```

<span data-ttu-id="2415e-121">Командлет обновите среду выполнения интеграции Azure-SSIS для использования саморазмещенной среды выполнения интеграции в качестве прокси-сервера данных.</span><span class="sxs-lookup"><span data-stu-id="2415e-121">The cmdlet update Azure-SSIS integration runtime to use Self-hosted integration runtime as a data proxy.</span></span>

## <span data-ttu-id="2415e-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2415e-122">PARAMETERS</span></span>

### <span data-ttu-id="2415e-123">-AuthKey</span><span class="sxs-lookup"><span data-stu-id="2415e-123">-AuthKey</span></span>
<span data-ttu-id="2415e-124">Ключ проверки подлинности на саморазмещенной среде выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="2415e-124">The authentication key of the self-hosted integration runtime.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2415e-125">-CatalogAdminCredential</span><span class="sxs-lookup"><span data-stu-id="2415e-125">-CatalogAdminCredential</span></span>
<span data-ttu-id="2415e-126">Учетные данные администратора базы данных каталога среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="2415e-126">The catalog database administrator credential of the integration runtime.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2415e-127">-CatalogPricingTier</span><span class="sxs-lookup"><span data-stu-id="2415e-127">-CatalogPricingTier</span></span>
<span data-ttu-id="2415e-128">Ценовая категория базы данных каталога в среде выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="2415e-128">The catalog database pricing tier of the integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2415e-129">-CatalogServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="2415e-129">-CatalogServerEndpoint</span></span>
<span data-ttu-id="2415e-130">Конечная точка сервера базы данных каталога среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="2415e-130">The catalog database server endpoint of the integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2415e-131">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="2415e-131">-DataFactoryName</span></span>
<span data-ttu-id="2415e-132">Имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="2415e-132">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByLinkedIntegrationRuntimeName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2415e-133">-DataFlowComputeType</span><span class="sxs-lookup"><span data-stu-id="2415e-133">-DataFlowComputeType</span></span>
<span data-ttu-id="2415e-134">Тип вычисления кластера потоков данных, который будет выполнять задание потока данных.</span><span class="sxs-lookup"><span data-stu-id="2415e-134">Compute type of the data flow cluster which will execute data flow job.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2415e-135">-DataFlowCoreCount</span><span class="sxs-lookup"><span data-stu-id="2415e-135">-DataFlowCoreCount</span></span>
<span data-ttu-id="2415e-136">Число ядер кластера потоков данных, который будет выполнять задание потока данных.</span><span class="sxs-lookup"><span data-stu-id="2415e-136">Core count of the data flow cluster which will execute data flow job.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2415e-137">-DataFlowTimeToLive</span><span class="sxs-lookup"><span data-stu-id="2415e-137">-DataFlowTimeToLive</span></span>
<span data-ttu-id="2415e-138">Параметр время жизни (в минутах) для кластера потоков данных, который будет выполнять задание потока данных.</span><span class="sxs-lookup"><span data-stu-id="2415e-138">Time to live (in minutes) setting of the data flow cluster which will execute data flow job.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2415e-139">-DataProxyIntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="2415e-139">-DataProxyIntegrationRuntimeName</span></span>
<span data-ttu-id="2415e-140">Имя среды выполнения интеграции Self-Hosted, используемое в качестве прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="2415e-140">The Self-Hosted Integration Runtime name which is used as a proxy</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2415e-141">-DataProxyStagingLinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="2415e-141">-DataProxyStagingLinkedServiceName</span></span>
<span data-ttu-id="2415e-142">Имя связанной службы хранилища BLOB-объектов Azure, которое ссылается на промежуточное хранилище данных, которое будет использоваться при переносе данных между Self-Hosted и средой выполнения интеграции Azure-SSIS</span><span class="sxs-lookup"><span data-stu-id="2415e-142">The Azure Blob Storage Linked Service name that references the staging data store to be used when moving data between Self-Hosted and Azure-SSIS Integration Runtime</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2415e-143">-DataProxyStagingPath</span><span class="sxs-lookup"><span data-stu-id="2415e-143">-DataProxyStagingPath</span></span>
<span data-ttu-id="2415e-144">Путь в хранилище промежуточных данных, который будет использоваться при перемещении данных между Self-Hostedми и средами выполнения интеграции Azure-SSIS, используется контейнер по умолчанию, если он не указан</span><span class="sxs-lookup"><span data-stu-id="2415e-144">The path in staging data store to be used when moving data between Self-Hosted and Azure-SSIS Integration Runtimes, a default container will be used if unspecified</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2415e-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2415e-145">-DefaultProfile</span></span>
<span data-ttu-id="2415e-146">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2415e-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2415e-147">-Описание</span><span class="sxs-lookup"><span data-stu-id="2415e-147">-Description</span></span>
<span data-ttu-id="2415e-148">Описание среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="2415e-148">The integration runtime description.</span></span>

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

### <span data-ttu-id="2415e-149">-Edition</span><span class="sxs-lookup"><span data-stu-id="2415e-149">-Edition</span></span>
<span data-ttu-id="2415e-150">Выпуски среды выполнения интеграции служб SSIS, которые могут быть стандартными или корпоративными, по умолчанию используется стандартный, если он не указан.</span><span class="sxs-lookup"><span data-stu-id="2415e-150">The edition for SSIS integration runtime which could be Standard or Enterprise, default is Standard if it is not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:
Accepted values: Standard, Enterprise

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2415e-151">-Force</span><span class="sxs-lookup"><span data-stu-id="2415e-151">-Force</span></span>
<span data-ttu-id="2415e-152">Запускает командлет без запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="2415e-152">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="2415e-153">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2415e-153">-InputObject</span></span>
<span data-ttu-id="2415e-154">Объект среды выполнения Integration.</span><span class="sxs-lookup"><span data-stu-id="2415e-154">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject, ByLinkedIntegrationRuntimeObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2415e-155">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="2415e-155">-LicenseType</span></span>
<span data-ttu-id="2415e-156">Тип лицензии, которую вы хотите выбрать для ИК-связи служб SSIS.</span><span class="sxs-lookup"><span data-stu-id="2415e-156">The license type that you want to select for the SSIS IR.</span></span> <span data-ttu-id="2415e-157">Существует два типа: LicenseIncluded или BasePrice.</span><span class="sxs-lookup"><span data-stu-id="2415e-157">There are two types: LicenseIncluded or BasePrice.</span></span> <span data-ttu-id="2415e-158">Если вы ищете цены на использование гибридной льготы для использования Azure (AHUB), пожалуйста, выберите BasePrice.</span><span class="sxs-lookup"><span data-stu-id="2415e-158">If you are qualified for the Azure Hybrid Use Benefit (AHUB) pricing, please select BasePrice.</span></span> <span data-ttu-id="2415e-159">Если это не так, пожалуйста, выберите LicenseIncluded.</span><span class="sxs-lookup"><span data-stu-id="2415e-159">If not, please select LicenseIncluded.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:
Accepted values: LicenseIncluded, BasePrice

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2415e-160">-Location</span><span class="sxs-lookup"><span data-stu-id="2415e-160">-Location</span></span>
<span data-ttu-id="2415e-161">Расположение среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="2415e-161">The integration runtime location.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2415e-162">-MaxParallelExecutionsPerNode</span><span class="sxs-lookup"><span data-stu-id="2415e-162">-MaxParallelExecutionsPerNode</span></span>
<span data-ttu-id="2415e-163">Максимальное количество параллельных выполнений на каждом узле для управляемой среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="2415e-163">Maximum parallel execution count per node for a managed dedicated integration runtime.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2415e-164">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2415e-164">-Name</span></span>
<span data-ttu-id="2415e-165">Имя среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="2415e-165">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByLinkedIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2415e-166">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="2415e-166">-NodeCount</span></span>
<span data-ttu-id="2415e-167">Количество целевых узлов в среде выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="2415e-167">Target nodes count of the integration runtime.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2415e-168">-NodeSize</span><span class="sxs-lookup"><span data-stu-id="2415e-168">-NodeSize</span></span>
<span data-ttu-id="2415e-169">Размер узла среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="2415e-169">The integration runtime node size.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2415e-170">-PublicIPs</span><span class="sxs-lookup"><span data-stu-id="2415e-170">-PublicIPs</span></span>
<span data-ttu-id="2415e-171">Статические общедоступные IP-адреса, которые будут использоваться средой выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="2415e-171">The static public IP addresses which the integration runtime will use.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2415e-172">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2415e-172">-ResourceGroupName</span></span>
<span data-ttu-id="2415e-173">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2415e-173">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByLinkedIntegrationRuntimeName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2415e-174">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2415e-174">-ResourceId</span></span>
<span data-ttu-id="2415e-175">Идентификатор ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="2415e-175">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId, ByLinkedIntegrationRuntimeResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2415e-176">-SetupScriptContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="2415e-176">-SetupScriptContainerSasUri</span></span>
<span data-ttu-id="2415e-177">Универсальный код ресурса (URI) SAS контейнера BLOB-объектов Azure, содержащего настраиваемый сценарий настройки.</span><span class="sxs-lookup"><span data-stu-id="2415e-177">The SAS URI of the Azure blob container that contains the custom setup script.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2415e-178">-SharedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="2415e-178">-SharedIntegrationRuntimeResourceId</span></span>
<span data-ttu-id="2415e-179">Идентификатор ресурса общей среды выполнения интеграции с самостоятельным размещением.</span><span class="sxs-lookup"><span data-stu-id="2415e-179">The resource id of the shared self-hosted integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: ByLinkedIntegrationRuntimeResourceId, ByLinkedIntegrationRuntimeName, ByLinkedIntegrationRuntimeObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2415e-180">-Подсеть</span><span class="sxs-lookup"><span data-stu-id="2415e-180">-Subnet</span></span>
<span data-ttu-id="2415e-181">Имя подсети в виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="2415e-181">The name of the subnet in the VNet.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases: SubnetName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2415e-182">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="2415e-182">-Type</span></span>
<span data-ttu-id="2415e-183">Тип среды выполнения Integration.</span><span class="sxs-lookup"><span data-stu-id="2415e-183">The integration runtime type.</span></span>

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

### <span data-ttu-id="2415e-184">-VNetId</span><span class="sxs-lookup"><span data-stu-id="2415e-184">-VNetId</span></span>
<span data-ttu-id="2415e-185">ИДЕНТИФИКАТОР виртуальной сети, к которой присоединяется среда выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="2415e-185">The ID of the VNet that the integration runtime joins.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2415e-186">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2415e-186">-Confirm</span></span>
<span data-ttu-id="2415e-187">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2415e-187">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2415e-188">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2415e-188">-WhatIf</span></span>
<span data-ttu-id="2415e-189">Показано, что происходит при запуске командлета, но не запускает командлет.</span><span class="sxs-lookup"><span data-stu-id="2415e-189">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="2415e-190">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2415e-190">CommonParameters</span></span>
<span data-ttu-id="2415e-191">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2415e-191">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2415e-192">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2415e-192">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2415e-193">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2415e-193">INPUTS</span></span>

### <span data-ttu-id="2415e-194">System. String</span><span class="sxs-lookup"><span data-stu-id="2415e-194">System.String</span></span>

### <span data-ttu-id="2415e-195">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="2415e-195">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="2415e-196">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2415e-196">OUTPUTS</span></span>

### <span data-ttu-id="2415e-197">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="2415e-197">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="2415e-198">Пуск</span><span class="sxs-lookup"><span data-stu-id="2415e-198">NOTES</span></span>

## <span data-ttu-id="2415e-199">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2415e-199">RELATED LINKS</span></span>

[<span data-ttu-id="2415e-200">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="2415e-200">Set-AzDataFactoryV2IntegrationRuntime</span></span>]()

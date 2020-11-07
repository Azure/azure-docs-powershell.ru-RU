---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 274c6cda9154348bfeffe600fd19512d1a85502d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721436"
---
# <span data-ttu-id="13d13-101">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="13d13-101">Set-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="13d13-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="13d13-102">SYNOPSIS</span></span>
<span data-ttu-id="13d13-103">Обновляет среду выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="13d13-103">Updates an integration runtime.</span></span>

## <span data-ttu-id="13d13-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="13d13-104">SYNTAX</span></span>

### <span data-ttu-id="13d13-105">ByIntegrationRuntimeName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="13d13-105">ByIntegrationRuntimeName (Default)</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Name] <String> [-Type <String>] [-Description <String>] [-Location <String>] [-NodeSize <String>]
 [-NodeCount <Int32>] [-CatalogServerEndpoint <String>] [-CatalogAdminCredential <PSCredential>]
 [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>] [-SetupScriptContainerSasUri <String>]
 [-Edition <String>] [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>] [-AuthKey <SecureString>]
 [-DataProxyIntegrationRuntimeName <String>] [-DataProxyStagingLinkedServiceName <String>] [-DataProxyStagingPath <String>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13d13-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="13d13-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceId] <String> [-Type <String>] [-Description <String>]
 [-Location <String>] [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-SetupScriptContainerSasUri <String>] [-Edition <String>] [-MaxParallelExecutionsPerNode <Int32>]
 [-DataProxyIntegrationRuntimeName <String>] [-DataProxyStagingLinkedServiceName <String>] [-DataProxyStagingPath <String>]
 [-LicenseType <String>] [-AuthKey <SecureString>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13d13-107">ByLinkedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="13d13-107">ByLinkedIntegrationRuntimeResourceId</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceId] <String> [-Type <String>] [-Description <String>]
 -SharedIntegrationRuntimeResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13d13-108">ByLinkedIntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="13d13-108">ByLinkedIntegrationRuntimeName</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Name] <String> [-Type <String>] [-Description <String>] -SharedIntegrationRuntimeResourceId <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13d13-109">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="13d13-109">ByIntegrationRuntimeObject</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-InputObject] <PSIntegrationRuntime> [-Type <String>]
 [-Description <String>] [-Location <String>] [-NodeSize <String>] [-NodeCount <Int32>]
 [-CatalogServerEndpoint <String>] [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>]
 [-VNetId <String>] [-Subnet <String>] [-SetupScriptContainerSasUri <String>] [-Edition <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>]  [-DataProxyIntegrationRuntimeName <String>]
 [-DataProxyStagingLinkedServiceName <String>] [-DataProxyStagingPath <String>] [-AuthKey <SecureString>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13d13-110">ByLinkedIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="13d13-110">ByLinkedIntegrationRuntimeObject</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-InputObject] <PSIntegrationRuntime> [-Type <String>]
 [-Description <String>] -SharedIntegrationRuntimeResourceId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13d13-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="13d13-111">DESCRIPTION</span></span>
<span data-ttu-id="13d13-112">Командлет Set-AzDataFactoryV2IntegrationRuntime обновляет среду выполнения интеграции с определенными параметрами.</span><span class="sxs-lookup"><span data-stu-id="13d13-112">The Set-AzDataFactoryV2IntegrationRuntime cmdlet updates an integration runtime with specific parameters.</span></span>

## <span data-ttu-id="13d13-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="13d13-113">EXAMPLES</span></span>

### <span data-ttu-id="13d13-114">Пример 1: Описание обновления среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="13d13-114">Example 1: Update integration runtime description.</span></span>
```
PS C:\> Set-AzDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' `
                                            -Description 'New description'

    Id                : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
    ResourceGroupName : rg-test-dfv2
    DataFactoryName   : test-df-eu2
    Name              : test-selfhost-ir
    Description       : New description
```

<span data-ttu-id="13d13-115">Командлет обновляет описание среды выполнения интеграции с именем Test-SelfHost-IR.</span><span class="sxs-lookup"><span data-stu-id="13d13-115">The cmdlet updates the description of integration runtime named 'test-selfhost-ir'.</span></span>

### <span data-ttu-id="13d13-116">Пример 2: общий доступ к среде выполнения интеграции с самостоятельным размещением.</span><span class="sxs-lookup"><span data-stu-id="13d13-116">Example 2: Share Self-hosted integration runtime.</span></span>
```
PS C:\> Set-AzDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' `
                                            -SharedIntegrationRuntimeResourceId '/subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir' -Type "SelfHosted"

    Id                : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
    ResourceGroupName : rg-test-dfv2
    DataFactoryName   : test-df-eu2
    Name              : test-selfhost-ir
    Description       : New description
```

<span data-ttu-id="13d13-117">Командлет добавляет файл ADF для использования общей среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="13d13-117">The cmdlet adds the ADF to use the shared integration runtime.</span></span> <span data-ttu-id="13d13-118">При использовании `-SharedIntegrationRuntimeResourceId` параметра `-Type` также необходимо включить.</span><span class="sxs-lookup"><span data-stu-id="13d13-118">When using `-SharedIntegrationRuntimeResourceId` parameter the `-Type` must also be included.</span></span> <span data-ttu-id="13d13-119">Обратите внимание, что необходимо предоставить фабрике данных разрешение на использование среды выполнения интеграции перед выполнением командлета.</span><span class="sxs-lookup"><span data-stu-id="13d13-119">Note that the data factory need to be granted permission to use the integration runtime before running cmdlet.</span></span>

### <span data-ttu-id="13d13-120">Пример 3: Настройка Self-Hosted инфракрасной связи в качестве прокси-сервера для службы Azure-SSIS IR в ADF.</span><span class="sxs-lookup"><span data-stu-id="13d13-120">Example 3: Configure Self-Hosted IR as a proxy for Azure-SSIS IR in ADF.</span></span>
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

<span data-ttu-id="13d13-121">Командлет обновите среду выполнения интеграции Azure-SSIS для использования саморазмещенной среды выполнения интеграции в качестве прокси-сервера данных.</span><span class="sxs-lookup"><span data-stu-id="13d13-121">The cmdlet update Azure-SSIS integration runtime to use Self-hosted integration runtime as a data proxy.</span></span>

## <span data-ttu-id="13d13-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="13d13-122">PARAMETERS</span></span>

### <span data-ttu-id="13d13-123">-AuthKey</span><span class="sxs-lookup"><span data-stu-id="13d13-123">-AuthKey</span></span>
<span data-ttu-id="13d13-124">Ключ проверки подлинности на саморазмещенной среде выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="13d13-124">The authentication key of the self-hosted integration runtime.</span></span>

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

### <span data-ttu-id="13d13-125">-CatalogAdminCredential</span><span class="sxs-lookup"><span data-stu-id="13d13-125">-CatalogAdminCredential</span></span>
<span data-ttu-id="13d13-126">Учетные данные администратора базы данных каталога среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="13d13-126">The catalog database administrator credential of the integration runtime.</span></span>

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

### <span data-ttu-id="13d13-127">-CatalogPricingTier</span><span class="sxs-lookup"><span data-stu-id="13d13-127">-CatalogPricingTier</span></span>
<span data-ttu-id="13d13-128">Ценовая категория базы данных каталога в среде выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="13d13-128">The catalog database pricing tier of the integration runtime.</span></span>

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

### <span data-ttu-id="13d13-129">-CatalogServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="13d13-129">-CatalogServerEndpoint</span></span>
<span data-ttu-id="13d13-130">Конечная точка сервера базы данных каталога среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="13d13-130">The catalog database server endpoint of the integration runtime.</span></span>

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

### <span data-ttu-id="13d13-131">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="13d13-131">-DataFactoryName</span></span>
<span data-ttu-id="13d13-132">Имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="13d13-132">The data factory name.</span></span>

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

### <span data-ttu-id="13d13-133">-DataProxyIntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="13d13-133">-DataProxyIntegrationRuntimeName</span></span>
<span data-ttu-id="13d13-134">Имя среды выполнения интеграции Self-Hosted, используемое в качестве прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="13d13-134">The Self-Hosted Integration Runtime name which is used as a proxy</span></span>

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

### <span data-ttu-id="13d13-135">-DataProxyStagingLinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="13d13-135">-DataProxyStagingLinkedServiceName</span></span>
<span data-ttu-id="13d13-136">Имя связанной службы хранилища BLOB-объектов Azure, которое ссылается на промежуточное хранилище данных, которое будет использоваться при переносе данных между Self-Hosted и средой выполнения интеграции Azure-SSIS</span><span class="sxs-lookup"><span data-stu-id="13d13-136">The Azure Blob Storage Linked Service name that references the staging data store to be used when moving data between Self-Hosted and Azure-SSIS Integration Runtime</span></span>

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

### <span data-ttu-id="13d13-137">-DataProxyStagingPath</span><span class="sxs-lookup"><span data-stu-id="13d13-137">-DataProxyStagingPath</span></span>
<span data-ttu-id="13d13-138">Путь в хранилище промежуточных данных, который будет использоваться при перемещении данных между Self-Hostedми и средами выполнения интеграции Azure-SSIS, используется контейнер по умолчанию, если он не указан</span><span class="sxs-lookup"><span data-stu-id="13d13-138">The path in staging data store to be used when moving data between Self-Hosted and Azure-SSIS Integration Runtimes, a default container will be used if unspecified</span></span>

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

### <span data-ttu-id="13d13-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13d13-139">-DefaultProfile</span></span>
<span data-ttu-id="13d13-140">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="13d13-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="13d13-141">-Описание</span><span class="sxs-lookup"><span data-stu-id="13d13-141">-Description</span></span>
<span data-ttu-id="13d13-142">Описание среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="13d13-142">The integration runtime description.</span></span>

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

### <span data-ttu-id="13d13-143">-Edition</span><span class="sxs-lookup"><span data-stu-id="13d13-143">-Edition</span></span>
<span data-ttu-id="13d13-144">Выпуски среды выполнения интеграции служб SSIS, которые могут быть стандартными или корпоративными, по умолчанию используется стандартный, если он не указан.</span><span class="sxs-lookup"><span data-stu-id="13d13-144">The edition for SSIS integration runtime which could be Standard or Enterprise, default is Standard if it is not specified.</span></span>

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

### <span data-ttu-id="13d13-145">-Force</span><span class="sxs-lookup"><span data-stu-id="13d13-145">-Force</span></span>
<span data-ttu-id="13d13-146">Запускает командлет без запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="13d13-146">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="13d13-147">-InputObject</span><span class="sxs-lookup"><span data-stu-id="13d13-147">-InputObject</span></span>
<span data-ttu-id="13d13-148">Объект среды выполнения Integration.</span><span class="sxs-lookup"><span data-stu-id="13d13-148">The integration runtime object.</span></span>

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

### <span data-ttu-id="13d13-149">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="13d13-149">-LicenseType</span></span>
<span data-ttu-id="13d13-150">Тип лицензии, которую вы хотите выбрать для ИК-связи служб SSIS.</span><span class="sxs-lookup"><span data-stu-id="13d13-150">The license type that you want to select for the SSIS IR.</span></span> <span data-ttu-id="13d13-151">Существует два типа: LicenseIncluded или BasePrice.</span><span class="sxs-lookup"><span data-stu-id="13d13-151">There are two types: LicenseIncluded or BasePrice.</span></span> <span data-ttu-id="13d13-152">Если вы ищете цены на использование гибридной льготы для использования Azure (AHUB), пожалуйста, выберите BasePrice.</span><span class="sxs-lookup"><span data-stu-id="13d13-152">If you are qualified for the Azure Hybrid Use Benefit (AHUB) pricing, please select BasePrice.</span></span> <span data-ttu-id="13d13-153">Если это не так, пожалуйста, выберите LicenseIncluded.</span><span class="sxs-lookup"><span data-stu-id="13d13-153">If not, please select LicenseIncluded.</span></span>

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

### <span data-ttu-id="13d13-154">-Location</span><span class="sxs-lookup"><span data-stu-id="13d13-154">-Location</span></span>
<span data-ttu-id="13d13-155">Расположение среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="13d13-155">The integration runtime location.</span></span>

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

### <span data-ttu-id="13d13-156">-MaxParallelExecutionsPerNode</span><span class="sxs-lookup"><span data-stu-id="13d13-156">-MaxParallelExecutionsPerNode</span></span>
<span data-ttu-id="13d13-157">Максимальное количество параллельных выполнений на каждом узле для управляемой среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="13d13-157">Maximum parallel execution count per node for a managed dedicated integration runtime.</span></span>

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

### <span data-ttu-id="13d13-158">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="13d13-158">-Name</span></span>
<span data-ttu-id="13d13-159">Имя среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="13d13-159">The integration runtime name.</span></span>

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

### <span data-ttu-id="13d13-160">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="13d13-160">-NodeCount</span></span>
<span data-ttu-id="13d13-161">Количество целевых узлов в среде выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="13d13-161">Target nodes count of the integration runtime.</span></span>

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

### <span data-ttu-id="13d13-162">-NodeSize</span><span class="sxs-lookup"><span data-stu-id="13d13-162">-NodeSize</span></span>
<span data-ttu-id="13d13-163">Размер узла среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="13d13-163">The integration runtime node size.</span></span>

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

### <span data-ttu-id="13d13-164">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13d13-164">-ResourceGroupName</span></span>
<span data-ttu-id="13d13-165">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="13d13-165">The resource group name.</span></span>

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

### <span data-ttu-id="13d13-166">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="13d13-166">-ResourceId</span></span>
<span data-ttu-id="13d13-167">Идентификатор ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="13d13-167">The Azure resource ID.</span></span>

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

### <span data-ttu-id="13d13-168">-SetupScriptContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="13d13-168">-SetupScriptContainerSasUri</span></span>
<span data-ttu-id="13d13-169">Универсальный код ресурса (URI) SAS контейнера BLOB-объектов Azure, содержащего настраиваемый сценарий настройки.</span><span class="sxs-lookup"><span data-stu-id="13d13-169">The SAS URI of the Azure blob container that contains the custom setup script.</span></span>

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

### <span data-ttu-id="13d13-170">-SharedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="13d13-170">-SharedIntegrationRuntimeResourceId</span></span>
<span data-ttu-id="13d13-171">Идентификатор ресурса общей среды выполнения интеграции с самостоятельным размещением.</span><span class="sxs-lookup"><span data-stu-id="13d13-171">The resource id of the shared self-hosted integration runtime.</span></span>

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

### <span data-ttu-id="13d13-172">-Подсеть</span><span class="sxs-lookup"><span data-stu-id="13d13-172">-Subnet</span></span>
<span data-ttu-id="13d13-173">Имя подсети в виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="13d13-173">The name of the subnet in the VNet.</span></span>

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

### <span data-ttu-id="13d13-174">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="13d13-174">-Type</span></span>
<span data-ttu-id="13d13-175">Тип среды выполнения Integration.</span><span class="sxs-lookup"><span data-stu-id="13d13-175">The integration runtime type.</span></span>

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

### <span data-ttu-id="13d13-176">-VNetId</span><span class="sxs-lookup"><span data-stu-id="13d13-176">-VNetId</span></span>
<span data-ttu-id="13d13-177">ИДЕНТИФИКАТОР виртуальной сети, к которой присоединяется среда выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="13d13-177">The ID of the VNet that the integration runtime joins.</span></span>

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

### <span data-ttu-id="13d13-178">-Confirm</span><span class="sxs-lookup"><span data-stu-id="13d13-178">-Confirm</span></span>
<span data-ttu-id="13d13-179">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="13d13-179">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13d13-180">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13d13-180">-WhatIf</span></span>
<span data-ttu-id="13d13-181">Показано, что происходит при запуске командлета, но не запускает командлет.</span><span class="sxs-lookup"><span data-stu-id="13d13-181">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="13d13-182">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13d13-182">CommonParameters</span></span>
<span data-ttu-id="13d13-183">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="13d13-183">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13d13-184">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13d13-184">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13d13-185">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="13d13-185">INPUTS</span></span>

### <span data-ttu-id="13d13-186">System. String</span><span class="sxs-lookup"><span data-stu-id="13d13-186">System.String</span></span>

### <span data-ttu-id="13d13-187">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="13d13-187">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="13d13-188">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="13d13-188">OUTPUTS</span></span>

### <span data-ttu-id="13d13-189">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="13d13-189">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="13d13-190">Пуск</span><span class="sxs-lookup"><span data-stu-id="13d13-190">NOTES</span></span>

## <span data-ttu-id="13d13-191">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="13d13-191">RELATED LINKS</span></span>

[<span data-ttu-id="13d13-192">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="13d13-192">Set-AzDataFactoryV2IntegrationRuntime</span></span>]()

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 0a687c1a2c21301ca61d92d7c4701d7b59d227f3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98508441"
---
# <span data-ttu-id="69d0c-101">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="69d0c-101">Set-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="69d0c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69d0c-102">SYNOPSIS</span></span>
<span data-ttu-id="69d0c-103">Обновляет время интеграции.</span><span class="sxs-lookup"><span data-stu-id="69d0c-103">Updates an integration runtime.</span></span>

## <span data-ttu-id="69d0c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="69d0c-104">SYNTAX</span></span>

### <span data-ttu-id="69d0c-105">ByIntegrationRuntimeName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="69d0c-105">ByIntegrationRuntimeName (Default)</span></span>
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

### <span data-ttu-id="69d0c-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="69d0c-106">ByResourceId</span></span>
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

### <span data-ttu-id="69d0c-107">ByLinkedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="69d0c-107">ByLinkedIntegrationRuntimeResourceId</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceId] <String> [-Type <String>] [-Description <String>]
 -SharedIntegrationRuntimeResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69d0c-108">ByLinkedIntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="69d0c-108">ByLinkedIntegrationRuntimeName</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Name] <String> [-Type <String>] [-Description <String>] -SharedIntegrationRuntimeResourceId <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69d0c-109">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="69d0c-109">ByIntegrationRuntimeObject</span></span>
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

### <span data-ttu-id="69d0c-110">ByLinkedIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="69d0c-110">ByLinkedIntegrationRuntimeObject</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-InputObject] <PSIntegrationRuntime> [-Type <String>]
 [-Description <String>] -SharedIntegrationRuntimeResourceId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69d0c-111">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="69d0c-111">DESCRIPTION</span></span>
<span data-ttu-id="69d0c-112">Этот Set-AzDataFactoryV2IntegrationRuntime обновляет время интеграции с определенными параметрами.</span><span class="sxs-lookup"><span data-stu-id="69d0c-112">The Set-AzDataFactoryV2IntegrationRuntime cmdlet updates an integration runtime with specific parameters.</span></span>

## <span data-ttu-id="69d0c-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="69d0c-113">EXAMPLES</span></span>

### <span data-ttu-id="69d0c-114">Пример 1. Описание времени обновления интеграции со временем запуска.</span><span class="sxs-lookup"><span data-stu-id="69d0c-114">Example 1: Update integration runtime description.</span></span>
```
PS C:\> Set-AzDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' `
                                            -Description 'New description'

    Id                : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
    ResourceGroupName : rg-test-dfv2
    DataFactoryName   : test-df-eu2
    Name              : test-selfhost-ir
    Description       : New description
```

<span data-ttu-id="69d0c-115">Этот cmdlet updates the description of integration runtime named 'test-selfhost-ir'.</span><span class="sxs-lookup"><span data-stu-id="69d0c-115">The cmdlet updates the description of integration runtime named 'test-selfhost-ir'.</span></span>

### <span data-ttu-id="69d0c-116">Пример 2. Время самостоятельной интеграции.</span><span class="sxs-lookup"><span data-stu-id="69d0c-116">Example 2: Share Self-hosted integration runtime.</span></span>
```
PS C:\> Set-AzDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' `
                                            -SharedIntegrationRuntimeResourceId '/subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir' -Type "SelfHosted"

    Id                : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
    ResourceGroupName : rg-test-dfv2
    DataFactoryName   : test-df-eu2
    Name              : test-selfhost-ir
    Description       : New description
```

<span data-ttu-id="69d0c-117">Он добавляет ADF, чтобы использовать общую емку времени интеграции.</span><span class="sxs-lookup"><span data-stu-id="69d0c-117">The cmdlet adds the ADF to use the shared integration runtime.</span></span> <span data-ttu-id="69d0c-118">При использовании `-SharedIntegrationRuntimeResourceId` параметра `-Type` также необходимо включить в него параметр.</span><span class="sxs-lookup"><span data-stu-id="69d0c-118">When using `-SharedIntegrationRuntimeResourceId` parameter the `-Type` must also be included.</span></span> <span data-ttu-id="69d0c-119">Обратите внимание, что фабрике данных необходимо предоставить разрешение на использование времени интеграции перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69d0c-119">Note that the data factory need to be granted permission to use the integration runtime before running cmdlet.</span></span>

### <span data-ttu-id="69d0c-120">Пример 3. Настройка Self-Hosted IR в качестве прокси-сервера для Azure-SSIS IR в ADF.</span><span class="sxs-lookup"><span data-stu-id="69d0c-120">Example 3: Configure Self-Hosted IR as a proxy for Azure-SSIS IR in ADF.</span></span>
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

<span data-ttu-id="69d0c-121">Время запуска интеграции Azure и SSIS с помощью cmdlet-обновления для использования времени самостоятельной интеграции в качестве прокси-сервера данных.</span><span class="sxs-lookup"><span data-stu-id="69d0c-121">The cmdlet update Azure-SSIS integration runtime to use Self-hosted integration runtime as a data proxy.</span></span>

## <span data-ttu-id="69d0c-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="69d0c-122">PARAMETERS</span></span>

### <span data-ttu-id="69d0c-123">-AuthKey</span><span class="sxs-lookup"><span data-stu-id="69d0c-123">-AuthKey</span></span>
<span data-ttu-id="69d0c-124">Ключ проверки подлинности для самостоятельной интеграции с runtime.</span><span class="sxs-lookup"><span data-stu-id="69d0c-124">The authentication key of the self-hosted integration runtime.</span></span>

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

### <span data-ttu-id="69d0c-125">-CatalogAdminCredential</span><span class="sxs-lookup"><span data-stu-id="69d0c-125">-CatalogAdminCredential</span></span>
<span data-ttu-id="69d0c-126">Учетные данные администратора базы данных каталога для времени запуска интеграции.</span><span class="sxs-lookup"><span data-stu-id="69d0c-126">The catalog database administrator credential of the integration runtime.</span></span>

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

### <span data-ttu-id="69d0c-127">-CatalogPricingTier</span><span class="sxs-lookup"><span data-stu-id="69d0c-127">-CatalogPricingTier</span></span>
<span data-ttu-id="69d0c-128">Уровень цены для базы данных каталога, уровень интеграции с runtime.</span><span class="sxs-lookup"><span data-stu-id="69d0c-128">The catalog database pricing tier of the integration runtime.</span></span>

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

### <span data-ttu-id="69d0c-129">-CatalogServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="69d0c-129">-CatalogServerEndpoint</span></span>
<span data-ttu-id="69d0c-130">Конечная точка сервера базы данных каталога, интегрированная со временем интеграции.</span><span class="sxs-lookup"><span data-stu-id="69d0c-130">The catalog database server endpoint of the integration runtime.</span></span>

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

### <span data-ttu-id="69d0c-131">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="69d0c-131">-DataFactoryName</span></span>
<span data-ttu-id="69d0c-132">Название фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="69d0c-132">The data factory name.</span></span>

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

### <span data-ttu-id="69d0c-133">-DataFlowComputeType</span><span class="sxs-lookup"><span data-stu-id="69d0c-133">-DataFlowComputeType</span></span>
<span data-ttu-id="69d0c-134">Вычислять тип кластера потоков данных, который будет выполнять задание потока данных.</span><span class="sxs-lookup"><span data-stu-id="69d0c-134">Compute type of the data flow cluster which will execute data flow job.</span></span>

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

### <span data-ttu-id="69d0c-135">-DataFlowCoreCount</span><span class="sxs-lookup"><span data-stu-id="69d0c-135">-DataFlowCoreCount</span></span>
<span data-ttu-id="69d0c-136">Основное количество кластеров потоков данных, которые выполняют задание потока данных.</span><span class="sxs-lookup"><span data-stu-id="69d0c-136">Core count of the data flow cluster which will execute data flow job.</span></span>

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

### <span data-ttu-id="69d0c-137">-DataFlowTimeToLive</span><span class="sxs-lookup"><span data-stu-id="69d0c-137">-DataFlowTimeToLive</span></span>
<span data-ttu-id="69d0c-138">Параметр времени жизни (в минутах) кластера потоков данных, который выполняет задание потока данных.</span><span class="sxs-lookup"><span data-stu-id="69d0c-138">Time to live (in minutes) setting of the data flow cluster which will execute data flow job.</span></span>

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

### <span data-ttu-id="69d0c-139">-DataProxyIntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="69d0c-139">-DataProxyIntegrationRuntimeName</span></span>
<span data-ttu-id="69d0c-140">Имя Self-Hosted Integration Runtime, которое используется в качестве прокси-сервера</span><span class="sxs-lookup"><span data-stu-id="69d0c-140">The Self-Hosted Integration Runtime name which is used as a proxy</span></span>

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

### <span data-ttu-id="69d0c-141">-DataProxyStagingLinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="69d0c-141">-DataProxyStagingLinkedServiceName</span></span>
<span data-ttu-id="69d0c-142">Имя связанной службы хранилища BLOB-приложений Azure, которая ссылается на промежуточное хранилище данных, которое будет использоваться при переносе данных между Self-Hosted и Azure-SSIS Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="69d0c-142">The Azure Blob Storage Linked Service name that references the staging data store to be used when moving data between Self-Hosted and Azure-SSIS Integration Runtime</span></span>

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

### <span data-ttu-id="69d0c-143">-DataProxyStagingPath</span><span class="sxs-lookup"><span data-stu-id="69d0c-143">-DataProxyStagingPath</span></span>
<span data-ttu-id="69d0c-144">Путь к промежуточному храну данных, который будет использоваться при переносе данных между Self-Hosted и runtimes интеграции Azure и SSIS, если неукален, будет использоваться контейнер по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="69d0c-144">The path in staging data store to be used when moving data between Self-Hosted and Azure-SSIS Integration Runtimes, a default container will be used if unspecified</span></span>

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

### <span data-ttu-id="69d0c-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69d0c-145">-DefaultProfile</span></span>
<span data-ttu-id="69d0c-146">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="69d0c-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="69d0c-147">-Description</span><span class="sxs-lookup"><span data-stu-id="69d0c-147">-Description</span></span>
<span data-ttu-id="69d0c-148">Описание времени запуска интеграции.</span><span class="sxs-lookup"><span data-stu-id="69d0c-148">The integration runtime description.</span></span>

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

### <span data-ttu-id="69d0c-149">-Edition</span><span class="sxs-lookup"><span data-stu-id="69d0c-149">-Edition</span></span>
<span data-ttu-id="69d0c-150">Выпуск для интеграции служб SSIS runtime, который может быть стандартным или корпоративным, по умолчанию является стандартным, если он не указан.</span><span class="sxs-lookup"><span data-stu-id="69d0c-150">The edition for SSIS integration runtime which could be Standard or Enterprise, default is Standard if it is not specified.</span></span>

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

### <span data-ttu-id="69d0c-151">-Force</span><span class="sxs-lookup"><span data-stu-id="69d0c-151">-Force</span></span>
<span data-ttu-id="69d0c-152">Выполняется cmdlet без запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="69d0c-152">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="69d0c-153">-InputObject</span><span class="sxs-lookup"><span data-stu-id="69d0c-153">-InputObject</span></span>
<span data-ttu-id="69d0c-154">Объект runtime интеграции.</span><span class="sxs-lookup"><span data-stu-id="69d0c-154">The integration runtime object.</span></span>

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

### <span data-ttu-id="69d0c-155">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="69d0c-155">-LicenseType</span></span>
<span data-ttu-id="69d0c-156">Тип лицензии, который вы хотите выбрать для ИД SSIS.</span><span class="sxs-lookup"><span data-stu-id="69d0c-156">The license type that you want to select for the SSIS IR.</span></span> <span data-ttu-id="69d0c-157">Существует два типа: LicenseIncluded или BasePrice.</span><span class="sxs-lookup"><span data-stu-id="69d0c-157">There are two types: LicenseIncluded or BasePrice.</span></span> <span data-ttu-id="69d0c-158">Если у вас есть право на использование преимущества гибридного использования Azure (AHUB), выберите BasePrice.</span><span class="sxs-lookup"><span data-stu-id="69d0c-158">If you are qualified for the Azure Hybrid Use Benefit (AHUB) pricing, please select BasePrice.</span></span> <span data-ttu-id="69d0c-159">Если нет, выберите LicenseIncluded.</span><span class="sxs-lookup"><span data-stu-id="69d0c-159">If not, please select LicenseIncluded.</span></span>

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

### <span data-ttu-id="69d0c-160">-Location</span><span class="sxs-lookup"><span data-stu-id="69d0c-160">-Location</span></span>
<span data-ttu-id="69d0c-161">Расположение времени запуска интеграции.</span><span class="sxs-lookup"><span data-stu-id="69d0c-161">The integration runtime location.</span></span>

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

### <span data-ttu-id="69d0c-162">-MaxParallelExecutionsPerNode</span><span class="sxs-lookup"><span data-stu-id="69d0c-162">-MaxParallelExecutionsPerNode</span></span>
<span data-ttu-id="69d0c-163">Максимальное количество параллельных выполнения на каждого узла для управляемой выделенной интеграции во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="69d0c-163">Maximum parallel execution count per node for a managed dedicated integration runtime.</span></span>

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

### <span data-ttu-id="69d0c-164">-Name</span><span class="sxs-lookup"><span data-stu-id="69d0c-164">-Name</span></span>
<span data-ttu-id="69d0c-165">Имя времени запуска интеграции.</span><span class="sxs-lookup"><span data-stu-id="69d0c-165">The integration runtime name.</span></span>

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

### <span data-ttu-id="69d0c-166">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="69d0c-166">-NodeCount</span></span>
<span data-ttu-id="69d0c-167">Количество целевых узлов в времени запуска интеграции.</span><span class="sxs-lookup"><span data-stu-id="69d0c-167">Target nodes count of the integration runtime.</span></span>

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

### <span data-ttu-id="69d0c-168">-NodeSize</span><span class="sxs-lookup"><span data-stu-id="69d0c-168">-NodeSize</span></span>
<span data-ttu-id="69d0c-169">Размер узла время запуска интеграции.</span><span class="sxs-lookup"><span data-stu-id="69d0c-169">The integration runtime node size.</span></span>

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

### <span data-ttu-id="69d0c-170">-PublicIPs</span><span class="sxs-lookup"><span data-stu-id="69d0c-170">-PublicIPs</span></span>
<span data-ttu-id="69d0c-171">Статические общедоступные IP-адреса, которые будут использовать время запуска интеграции.</span><span class="sxs-lookup"><span data-stu-id="69d0c-171">The static public IP addresses which the integration runtime will use.</span></span>

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

### <span data-ttu-id="69d0c-172">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69d0c-172">-ResourceGroupName</span></span>
<span data-ttu-id="69d0c-173">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="69d0c-173">The resource group name.</span></span>

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

### <span data-ttu-id="69d0c-174">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="69d0c-174">-ResourceId</span></span>
<span data-ttu-id="69d0c-175">ИД ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="69d0c-175">The Azure resource ID.</span></span>

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

### <span data-ttu-id="69d0c-176">-SetupScriptContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="69d0c-176">-SetupScriptContainerSasUri</span></span>
<span data-ttu-id="69d0c-177">URI SAS контейнера BLOB-lob Azure, который содержит сценарий настройки.</span><span class="sxs-lookup"><span data-stu-id="69d0c-177">The SAS URI of the Azure blob container that contains the custom setup script.</span></span>

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

### <span data-ttu-id="69d0c-178">-SharedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="69d0c-178">-SharedIntegrationRuntimeResourceId</span></span>
<span data-ttu-id="69d0c-179">ИД ресурса для общей самостоятельной интеграции во время работы.</span><span class="sxs-lookup"><span data-stu-id="69d0c-179">The resource id of the shared self-hosted integration runtime.</span></span>

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

### <span data-ttu-id="69d0c-180">-Subnet</span><span class="sxs-lookup"><span data-stu-id="69d0c-180">-Subnet</span></span>
<span data-ttu-id="69d0c-181">Имя подсети в VNet.</span><span class="sxs-lookup"><span data-stu-id="69d0c-181">The name of the subnet in the VNet.</span></span>

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

### <span data-ttu-id="69d0c-182">-Type</span><span class="sxs-lookup"><span data-stu-id="69d0c-182">-Type</span></span>
<span data-ttu-id="69d0c-183">Тип времени запуска интеграции.</span><span class="sxs-lookup"><span data-stu-id="69d0c-183">The integration runtime type.</span></span>

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

### <span data-ttu-id="69d0c-184">-VNetId</span><span class="sxs-lookup"><span data-stu-id="69d0c-184">-VNetId</span></span>
<span data-ttu-id="69d0c-185">ИД VNet, который присоединяется к окне времени запуска интеграции.</span><span class="sxs-lookup"><span data-stu-id="69d0c-185">The ID of the VNet that the integration runtime joins.</span></span>

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

### <span data-ttu-id="69d0c-186">-Confirm</span><span class="sxs-lookup"><span data-stu-id="69d0c-186">-Confirm</span></span>
<span data-ttu-id="69d0c-187">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69d0c-187">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69d0c-188">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69d0c-188">-WhatIf</span></span>
<span data-ttu-id="69d0c-189">Показывает, что происходит, если выполняется только запуск, но не выполняется.</span><span class="sxs-lookup"><span data-stu-id="69d0c-189">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="69d0c-190">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69d0c-190">CommonParameters</span></span>
<span data-ttu-id="69d0c-191">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69d0c-191">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69d0c-192">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69d0c-192">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69d0c-193">INPUTS</span><span class="sxs-lookup"><span data-stu-id="69d0c-193">INPUTS</span></span>

### <span data-ttu-id="69d0c-194">System.String</span><span class="sxs-lookup"><span data-stu-id="69d0c-194">System.String</span></span>

### <span data-ttu-id="69d0c-195">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="69d0c-195">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="69d0c-196">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="69d0c-196">OUTPUTS</span></span>

### <span data-ttu-id="69d0c-197">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="69d0c-197">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="69d0c-198">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="69d0c-198">NOTES</span></span>

## <span data-ttu-id="69d0c-199">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="69d0c-199">RELATED LINKS</span></span>

[<span data-ttu-id="69d0c-200">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="69d0c-200">Set-AzDataFactoryV2IntegrationRuntime</span></span>]()

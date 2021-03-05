---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/set-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 09b0ac3083a0440b6c229da6f45bf6412817b7ea
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964936"
---
# <span data-ttu-id="76298-101">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="76298-101">Set-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="76298-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76298-102">SYNOPSIS</span></span>
<span data-ttu-id="76298-103">Обновляет время интеграции.</span><span class="sxs-lookup"><span data-stu-id="76298-103">Updates an integration runtime.</span></span>

## <span data-ttu-id="76298-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="76298-104">SYNTAX</span></span>

### <span data-ttu-id="76298-105">ByIntegrationRuntimeName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="76298-105">ByIntegrationRuntimeName (Default)</span></span>
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

### <span data-ttu-id="76298-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="76298-106">ByResourceId</span></span>
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

### <span data-ttu-id="76298-107">ByLinkedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="76298-107">ByLinkedIntegrationRuntimeResourceId</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceId] <String> [-Type <String>] [-Description <String>]
 -SharedIntegrationRuntimeResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76298-108">ByLinkedIntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="76298-108">ByLinkedIntegrationRuntimeName</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Name] <String> [-Type <String>] [-Description <String>] -SharedIntegrationRuntimeResourceId <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76298-109">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="76298-109">ByIntegrationRuntimeObject</span></span>
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

### <span data-ttu-id="76298-110">ByLinkedIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="76298-110">ByLinkedIntegrationRuntimeObject</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-InputObject] <PSIntegrationRuntime> [-Type <String>]
 [-Description <String>] -SharedIntegrationRuntimeResourceId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76298-111">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="76298-111">DESCRIPTION</span></span>
<span data-ttu-id="76298-112">Этот Set-AzDataFactoryV2IntegrationRuntime обновляет время интеграции с определенными параметрами.</span><span class="sxs-lookup"><span data-stu-id="76298-112">The Set-AzDataFactoryV2IntegrationRuntime cmdlet updates an integration runtime with specific parameters.</span></span>

## <span data-ttu-id="76298-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="76298-113">EXAMPLES</span></span>

### <span data-ttu-id="76298-114">Пример 1. Описание времени обновления интеграции со временем запуска.</span><span class="sxs-lookup"><span data-stu-id="76298-114">Example 1: Update integration runtime description.</span></span>
```
PS C:\> Set-AzDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' `
                                            -Description 'New description'

    Id                : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
    ResourceGroupName : rg-test-dfv2
    DataFactoryName   : test-df-eu2
    Name              : test-selfhost-ir
    Description       : New description
```

<span data-ttu-id="76298-115">Этот cmdlet обновляет описание интегрированной системы runtime с именем test-selfhost-ir.</span><span class="sxs-lookup"><span data-stu-id="76298-115">The cmdlet updates the description of integration runtime named 'test-selfhost-ir'.</span></span>

### <span data-ttu-id="76298-116">Пример 2. Время самостоятельной интеграции.</span><span class="sxs-lookup"><span data-stu-id="76298-116">Example 2: Share Self-hosted integration runtime.</span></span>
```
PS C:\> Set-AzDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' `
                                            -SharedIntegrationRuntimeResourceId '/subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir' -Type "SelfHosted"

    Id                : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
    ResourceGroupName : rg-test-dfv2
    DataFactoryName   : test-df-eu2
    Name              : test-selfhost-ir
    Description       : New description
```

<span data-ttu-id="76298-117">Он добавляет ADF, чтобы использовать общую емку времени интеграции.</span><span class="sxs-lookup"><span data-stu-id="76298-117">The cmdlet adds the ADF to use the shared integration runtime.</span></span> <span data-ttu-id="76298-118">При использовании `-SharedIntegrationRuntimeResourceId` параметра `-Type` также необходимо включить в него параметр.</span><span class="sxs-lookup"><span data-stu-id="76298-118">When using `-SharedIntegrationRuntimeResourceId` parameter the `-Type` must also be included.</span></span> <span data-ttu-id="76298-119">Обратите внимание, что фабрике данных необходимо предоставить разрешение на использование времени интеграции перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="76298-119">Note that the data factory need to be granted permission to use the integration runtime before running cmdlet.</span></span>

### <span data-ttu-id="76298-120">Пример 3. Настройка Self-Hosted IR в качестве прокси-сервера для Azure-SSIS IR в ADF.</span><span class="sxs-lookup"><span data-stu-id="76298-120">Example 3: Configure Self-Hosted IR as a proxy for Azure-SSIS IR in ADF.</span></span>
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

<span data-ttu-id="76298-121">Процесс интеграции Azure и SSIS с помощью cmdlet-обновления используется для использования времени самостоятельной интеграции в качестве прокси-сервера данных.</span><span class="sxs-lookup"><span data-stu-id="76298-121">The cmdlet update Azure-SSIS integration runtime to use Self-hosted integration runtime as a data proxy.</span></span>

## <span data-ttu-id="76298-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="76298-122">PARAMETERS</span></span>

### <span data-ttu-id="76298-123">-AuthKey</span><span class="sxs-lookup"><span data-stu-id="76298-123">-AuthKey</span></span>
<span data-ttu-id="76298-124">Ключ проверки подлинности для самостоятельной интеграции с runtime.</span><span class="sxs-lookup"><span data-stu-id="76298-124">The authentication key of the self-hosted integration runtime.</span></span>

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

### <span data-ttu-id="76298-125">-CatalogAdminCredential</span><span class="sxs-lookup"><span data-stu-id="76298-125">-CatalogAdminCredential</span></span>
<span data-ttu-id="76298-126">Учетные данные администратора базы данных каталога для времени запуска интеграции.</span><span class="sxs-lookup"><span data-stu-id="76298-126">The catalog database administrator credential of the integration runtime.</span></span>

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

### <span data-ttu-id="76298-127">-CatalogPricingTier</span><span class="sxs-lookup"><span data-stu-id="76298-127">-CatalogPricingTier</span></span>
<span data-ttu-id="76298-128">Уровень цены для базы данных каталога, уровень интеграции с runtime.</span><span class="sxs-lookup"><span data-stu-id="76298-128">The catalog database pricing tier of the integration runtime.</span></span>

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

### <span data-ttu-id="76298-129">-CatalogServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="76298-129">-CatalogServerEndpoint</span></span>
<span data-ttu-id="76298-130">Конечная точка сервера базы данных каталога, интегрированная со временем интеграции.</span><span class="sxs-lookup"><span data-stu-id="76298-130">The catalog database server endpoint of the integration runtime.</span></span>

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

### <span data-ttu-id="76298-131">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="76298-131">-DataFactoryName</span></span>
<span data-ttu-id="76298-132">Название фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="76298-132">The data factory name.</span></span>

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

### <span data-ttu-id="76298-133">-DataFlowComputeType</span><span class="sxs-lookup"><span data-stu-id="76298-133">-DataFlowComputeType</span></span>
<span data-ttu-id="76298-134">Вычислять тип кластера потоков данных, который будет выполнять задание потока данных.</span><span class="sxs-lookup"><span data-stu-id="76298-134">Compute type of the data flow cluster which will execute data flow job.</span></span>

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

### <span data-ttu-id="76298-135">-DataFlowCoreCount</span><span class="sxs-lookup"><span data-stu-id="76298-135">-DataFlowCoreCount</span></span>
<span data-ttu-id="76298-136">Основное количество кластеров потоков данных, которые выполняют задание потока данных.</span><span class="sxs-lookup"><span data-stu-id="76298-136">Core count of the data flow cluster which will execute data flow job.</span></span>

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

### <span data-ttu-id="76298-137">-DataFlowTimeToLive</span><span class="sxs-lookup"><span data-stu-id="76298-137">-DataFlowTimeToLive</span></span>
<span data-ttu-id="76298-138">Параметр времени жизни (в минутах) кластера потоков данных, который выполняет задание потока данных.</span><span class="sxs-lookup"><span data-stu-id="76298-138">Time to live (in minutes) setting of the data flow cluster which will execute data flow job.</span></span>

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

### <span data-ttu-id="76298-139">-DataProxyIntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="76298-139">-DataProxyIntegrationRuntimeName</span></span>
<span data-ttu-id="76298-140">Имя Self-Hosted Integration Runtime, которое используется в качестве прокси-сервера</span><span class="sxs-lookup"><span data-stu-id="76298-140">The Self-Hosted Integration Runtime name which is used as a proxy</span></span>

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

### <span data-ttu-id="76298-141">-DataProxyStagingLinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="76298-141">-DataProxyStagingLinkedServiceName</span></span>
<span data-ttu-id="76298-142">Имя связанной службы хранилища BLOB-приложений Azure, которая ссылается на промежуточное хранилище данных, которое будет использоваться при переносе данных между Self-Hosted и Azure-SSIS Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="76298-142">The Azure Blob Storage Linked Service name that references the staging data store to be used when moving data between Self-Hosted and Azure-SSIS Integration Runtime</span></span>

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

### <span data-ttu-id="76298-143">-DataProxyStagingPath</span><span class="sxs-lookup"><span data-stu-id="76298-143">-DataProxyStagingPath</span></span>
<span data-ttu-id="76298-144">Путь к промежуточному храну данных, который будет использоваться при переносе данных между Self-Hosted и runtimes интеграции Azure и SSIS, если неукален, будет использоваться контейнер по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="76298-144">The path in staging data store to be used when moving data between Self-Hosted and Azure-SSIS Integration Runtimes, a default container will be used if unspecified</span></span>

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

### <span data-ttu-id="76298-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76298-145">-DefaultProfile</span></span>
<span data-ttu-id="76298-146">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="76298-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="76298-147">-Description</span><span class="sxs-lookup"><span data-stu-id="76298-147">-Description</span></span>
<span data-ttu-id="76298-148">Описание времени запуска интеграции.</span><span class="sxs-lookup"><span data-stu-id="76298-148">The integration runtime description.</span></span>

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

### <span data-ttu-id="76298-149">-Edition</span><span class="sxs-lookup"><span data-stu-id="76298-149">-Edition</span></span>
<span data-ttu-id="76298-150">Выпуск для интеграции служб SSIS runtime, который может быть стандартным или корпоративным, по умолчанию является стандартным, если он не указан.</span><span class="sxs-lookup"><span data-stu-id="76298-150">The edition for SSIS integration runtime which could be Standard or Enterprise, default is Standard if it is not specified.</span></span>

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

### <span data-ttu-id="76298-151">-Force</span><span class="sxs-lookup"><span data-stu-id="76298-151">-Force</span></span>
<span data-ttu-id="76298-152">Выполняется cmdlet без запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="76298-152">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="76298-153">-InputObject</span><span class="sxs-lookup"><span data-stu-id="76298-153">-InputObject</span></span>
<span data-ttu-id="76298-154">Объект runtime интеграции.</span><span class="sxs-lookup"><span data-stu-id="76298-154">The integration runtime object.</span></span>

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

### <span data-ttu-id="76298-155">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="76298-155">-LicenseType</span></span>
<span data-ttu-id="76298-156">Тип лицензии, который вы хотите выбрать для ИД SSIS.</span><span class="sxs-lookup"><span data-stu-id="76298-156">The license type that you want to select for the SSIS IR.</span></span> <span data-ttu-id="76298-157">Существует два типа: LicenseIncluded или BasePrice.</span><span class="sxs-lookup"><span data-stu-id="76298-157">There are two types: LicenseIncluded or BasePrice.</span></span> <span data-ttu-id="76298-158">Если у вас есть право на использование преимущества гибридного использования Azure (AHUB), выберите BasePrice.</span><span class="sxs-lookup"><span data-stu-id="76298-158">If you are qualified for the Azure Hybrid Use Benefit (AHUB) pricing, please select BasePrice.</span></span> <span data-ttu-id="76298-159">Если нет, выберите LicenseIncluded.</span><span class="sxs-lookup"><span data-stu-id="76298-159">If not, please select LicenseIncluded.</span></span>

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

### <span data-ttu-id="76298-160">-Location</span><span class="sxs-lookup"><span data-stu-id="76298-160">-Location</span></span>
<span data-ttu-id="76298-161">Расположение времени запуска интеграции.</span><span class="sxs-lookup"><span data-stu-id="76298-161">The integration runtime location.</span></span>

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

### <span data-ttu-id="76298-162">-MaxParallelExecutionsPerNode</span><span class="sxs-lookup"><span data-stu-id="76298-162">-MaxParallelExecutionsPerNode</span></span>
<span data-ttu-id="76298-163">Максимальное количество параллельных выполнения на каждого узла для управляемой выделенной интеграции во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="76298-163">Maximum parallel execution count per node for a managed dedicated integration runtime.</span></span>

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

### <span data-ttu-id="76298-164">-Name</span><span class="sxs-lookup"><span data-stu-id="76298-164">-Name</span></span>
<span data-ttu-id="76298-165">Имя времени запуска интеграции.</span><span class="sxs-lookup"><span data-stu-id="76298-165">The integration runtime name.</span></span>

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

### <span data-ttu-id="76298-166">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="76298-166">-NodeCount</span></span>
<span data-ttu-id="76298-167">Количество целевых узлов в времени запуска интеграции.</span><span class="sxs-lookup"><span data-stu-id="76298-167">Target nodes count of the integration runtime.</span></span>

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

### <span data-ttu-id="76298-168">-NodeSize</span><span class="sxs-lookup"><span data-stu-id="76298-168">-NodeSize</span></span>
<span data-ttu-id="76298-169">Размер узла время запуска интеграции.</span><span class="sxs-lookup"><span data-stu-id="76298-169">The integration runtime node size.</span></span>

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

### <span data-ttu-id="76298-170">-PublicIPs</span><span class="sxs-lookup"><span data-stu-id="76298-170">-PublicIPs</span></span>
<span data-ttu-id="76298-171">Статические общедоступные IP-адреса, которые будут использовать время запуска интеграции.</span><span class="sxs-lookup"><span data-stu-id="76298-171">The static public IP addresses which the integration runtime will use.</span></span>

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

### <span data-ttu-id="76298-172">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76298-172">-ResourceGroupName</span></span>
<span data-ttu-id="76298-173">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="76298-173">The resource group name.</span></span>

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

### <span data-ttu-id="76298-174">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="76298-174">-ResourceId</span></span>
<span data-ttu-id="76298-175">ИД ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="76298-175">The Azure resource ID.</span></span>

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

### <span data-ttu-id="76298-176">-SetupScriptContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="76298-176">-SetupScriptContainerSasUri</span></span>
<span data-ttu-id="76298-177">URI SAS контейнера BLOB-lob Azure, который содержит сценарий настройки.</span><span class="sxs-lookup"><span data-stu-id="76298-177">The SAS URI of the Azure blob container that contains the custom setup script.</span></span>

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

### <span data-ttu-id="76298-178">-SharedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="76298-178">-SharedIntegrationRuntimeResourceId</span></span>
<span data-ttu-id="76298-179">ИД ресурса для общей самостоятельной интеграции.</span><span class="sxs-lookup"><span data-stu-id="76298-179">The resource id of the shared self-hosted integration runtime.</span></span>

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

### <span data-ttu-id="76298-180">-Subnet</span><span class="sxs-lookup"><span data-stu-id="76298-180">-Subnet</span></span>
<span data-ttu-id="76298-181">Имя подсети в VNet.</span><span class="sxs-lookup"><span data-stu-id="76298-181">The name of the subnet in the VNet.</span></span>

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

### <span data-ttu-id="76298-182">-Type</span><span class="sxs-lookup"><span data-stu-id="76298-182">-Type</span></span>
<span data-ttu-id="76298-183">Тип времени запуска интеграции.</span><span class="sxs-lookup"><span data-stu-id="76298-183">The integration runtime type.</span></span>

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

### <span data-ttu-id="76298-184">-VNetId</span><span class="sxs-lookup"><span data-stu-id="76298-184">-VNetId</span></span>
<span data-ttu-id="76298-185">ИД VNet, который присоединяется к интеграции со временем запуска интеграции.</span><span class="sxs-lookup"><span data-stu-id="76298-185">The ID of the VNet that the integration runtime joins.</span></span>

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

### <span data-ttu-id="76298-186">-Confirm</span><span class="sxs-lookup"><span data-stu-id="76298-186">-Confirm</span></span>
<span data-ttu-id="76298-187">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="76298-187">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76298-188">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76298-188">-WhatIf</span></span>
<span data-ttu-id="76298-189">Показывает, что происходит, если выполняется только запуск, но не выполняется.</span><span class="sxs-lookup"><span data-stu-id="76298-189">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="76298-190">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76298-190">CommonParameters</span></span>
<span data-ttu-id="76298-191">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76298-191">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76298-192">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76298-192">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76298-193">INPUTS</span><span class="sxs-lookup"><span data-stu-id="76298-193">INPUTS</span></span>

### <span data-ttu-id="76298-194">System.String</span><span class="sxs-lookup"><span data-stu-id="76298-194">System.String</span></span>

### <span data-ttu-id="76298-195">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="76298-195">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="76298-196">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="76298-196">OUTPUTS</span></span>

### <span data-ttu-id="76298-197">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="76298-197">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="76298-198">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="76298-198">NOTES</span></span>

## <span data-ttu-id="76298-199">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="76298-199">RELATED LINKS</span></span>

[<span data-ttu-id="76298-200">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="76298-200">Set-AzDataFactoryV2IntegrationRuntime</span></span>]()

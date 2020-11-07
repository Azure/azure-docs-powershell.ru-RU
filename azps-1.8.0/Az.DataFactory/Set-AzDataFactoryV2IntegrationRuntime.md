---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: e92d04e60132463b22741242f411f6af5d09c2b0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93900914"
---
# <span data-ttu-id="9fbd4-101">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="9fbd4-101">Set-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="9fbd4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9fbd4-102">SYNOPSIS</span></span>
<span data-ttu-id="9fbd4-103">Обновляет среду выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="9fbd4-103">Updates an integration runtime.</span></span>

## <span data-ttu-id="9fbd4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9fbd4-104">SYNTAX</span></span>

### <span data-ttu-id="9fbd4-105">ByIntegrationRuntimeName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9fbd4-105">ByIntegrationRuntimeName (Default)</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Name] <String> [-Type <String>] [-Description <String>] [-Location <String>] [-NodeSize <String>]
 [-NodeCount <Int32>] [-CatalogServerEndpoint <String>] [-CatalogAdminCredential <PSCredential>]
 [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>] [-SetupScriptContainerSasUri <String>]
 [-Edition <String>] [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>] [-AuthKey <SecureString>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9fbd4-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="9fbd4-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceId] <String> [-Type <String>] [-Description <String>]
 [-Location <String>] [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-SetupScriptContainerSasUri <String>] [-Edition <String>] [-MaxParallelExecutionsPerNode <Int32>]
 [-LicenseType <String>] [-AuthKey <SecureString>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9fbd4-107">ByLinkedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="9fbd4-107">ByLinkedIntegrationRuntimeResourceId</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceId] <String> [-Type <String>] [-Description <String>]
 -SharedIntegrationRuntimeResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9fbd4-108">ByLinkedIntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="9fbd4-108">ByLinkedIntegrationRuntimeName</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Name] <String> [-Type <String>] [-Description <String>] -SharedIntegrationRuntimeResourceId <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9fbd4-109">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="9fbd4-109">ByIntegrationRuntimeObject</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-InputObject] <PSIntegrationRuntime> [-Type <String>]
 [-Description <String>] [-Location <String>] [-NodeSize <String>] [-NodeCount <Int32>]
 [-CatalogServerEndpoint <String>] [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>]
 [-VNetId <String>] [-Subnet <String>] [-SetupScriptContainerSasUri <String>] [-Edition <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>] [-AuthKey <SecureString>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9fbd4-110">ByLinkedIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="9fbd4-110">ByLinkedIntegrationRuntimeObject</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-InputObject] <PSIntegrationRuntime> [-Type <String>]
 [-Description <String>] -SharedIntegrationRuntimeResourceId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9fbd4-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9fbd4-111">DESCRIPTION</span></span>
<span data-ttu-id="9fbd4-112">Командлет Set-AzDataFactoryV2IntegrationRuntime обновляет среду выполнения интеграции с определенными параметрами.</span><span class="sxs-lookup"><span data-stu-id="9fbd4-112">The Set-AzDataFactoryV2IntegrationRuntime cmdlet updates an integration runtime with specific parameters.</span></span>

## <span data-ttu-id="9fbd4-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9fbd4-113">EXAMPLES</span></span>

### <span data-ttu-id="9fbd4-114">Пример 1: Описание обновления среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="9fbd4-114">Example 1: Update integration runtime description.</span></span>
```
PS C:\> Set-AzDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' `
                                            -Description 'New description'

    Id                : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
    ResourceGroupName : rg-test-dfv2
    DataFactoryName   : test-df-eu2
    Name              : test-selfhost-ir
    Description       : New description
```

<span data-ttu-id="9fbd4-115">Командлет обновляет описание среды выполнения интеграции с именем Test-SelfHost-IR.</span><span class="sxs-lookup"><span data-stu-id="9fbd4-115">The cmdlet updates the description of integration runtime named 'test-selfhost-ir'.</span></span>

### <span data-ttu-id="9fbd4-116">Пример 2: общий доступ к среде выполнения интеграции с самостоятельным размещением.</span><span class="sxs-lookup"><span data-stu-id="9fbd4-116">Example 2: Share Self-hosted integration runtime.</span></span>
```
PS C:\> Set-AzDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' `
                                            -SharedIntegrationRuntimeResourceId '/subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir' -Type "SelfHosted"

    Id                : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
    ResourceGroupName : rg-test-dfv2
    DataFactoryName   : test-df-eu2
    Name              : test-selfhost-ir
    Description       : New description
```

<span data-ttu-id="9fbd4-117">Командлет добавляет файл ADF для использования общей среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="9fbd4-117">The cmdlet adds the ADF to use the shared integration runtime.</span></span> <span data-ttu-id="9fbd4-118">При использовании `-SharedIntegrationRuntimeResourceId` параметра `-Type` также необходимо включить.</span><span class="sxs-lookup"><span data-stu-id="9fbd4-118">When using `-SharedIntegrationRuntimeResourceId` parameter the `-Type` must also be included.</span></span> <span data-ttu-id="9fbd4-119">Обратите внимание, что необходимо предоставить фабрике данных разрешение на использование среды выполнения интеграции перед выполнением командлета.</span><span class="sxs-lookup"><span data-stu-id="9fbd4-119">Note that the data factory need to be granted permission to use the integration runtime before running cmdlet.</span></span>

## <span data-ttu-id="9fbd4-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9fbd4-120">PARAMETERS</span></span>

### <span data-ttu-id="9fbd4-121">-AuthKey</span><span class="sxs-lookup"><span data-stu-id="9fbd4-121">-AuthKey</span></span>
<span data-ttu-id="9fbd4-122">Ключ проверки подлинности на саморазмещенной среде выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="9fbd4-122">The authentication key of the self-hosted integration runtime.</span></span>

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

### <span data-ttu-id="9fbd4-123">-CatalogAdminCredential</span><span class="sxs-lookup"><span data-stu-id="9fbd4-123">-CatalogAdminCredential</span></span>
<span data-ttu-id="9fbd4-124">Учетные данные администратора базы данных каталога среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="9fbd4-124">The catalog database administrator credential of the integration runtime.</span></span>

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

### <span data-ttu-id="9fbd4-125">-CatalogPricingTier</span><span class="sxs-lookup"><span data-stu-id="9fbd4-125">-CatalogPricingTier</span></span>
<span data-ttu-id="9fbd4-126">Ценовая категория базы данных каталога в среде выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="9fbd4-126">The catalog database pricing tier of the integration runtime.</span></span>

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

### <span data-ttu-id="9fbd4-127">-CatalogServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="9fbd4-127">-CatalogServerEndpoint</span></span>
<span data-ttu-id="9fbd4-128">Конечная точка сервера базы данных каталога среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="9fbd4-128">The catalog database server endpoint of the integration runtime.</span></span>

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

### <span data-ttu-id="9fbd4-129">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="9fbd4-129">-DataFactoryName</span></span>
<span data-ttu-id="9fbd4-130">Имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="9fbd4-130">The data factory name.</span></span>

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

### <span data-ttu-id="9fbd4-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fbd4-131">-DefaultProfile</span></span>
<span data-ttu-id="9fbd4-132">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9fbd4-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9fbd4-133">-Описание</span><span class="sxs-lookup"><span data-stu-id="9fbd4-133">-Description</span></span>
<span data-ttu-id="9fbd4-134">Описание среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="9fbd4-134">The integration runtime description.</span></span>

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

### <span data-ttu-id="9fbd4-135">-Edition</span><span class="sxs-lookup"><span data-stu-id="9fbd4-135">-Edition</span></span>
<span data-ttu-id="9fbd4-136">Выпуски среды выполнения интеграции служб SSIS, которые могут быть стандартными или корпоративными, по умолчанию используется стандартный, если он не указан.</span><span class="sxs-lookup"><span data-stu-id="9fbd4-136">The edition for SSIS integration runtime which could be Standard or Enterprise, default is Standard if it is not specified.</span></span>

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

### <span data-ttu-id="9fbd4-137">-Force</span><span class="sxs-lookup"><span data-stu-id="9fbd4-137">-Force</span></span>
<span data-ttu-id="9fbd4-138">Запускает командлет без запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="9fbd4-138">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="9fbd4-139">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9fbd4-139">-InputObject</span></span>
<span data-ttu-id="9fbd4-140">Объект среды выполнения Integration.</span><span class="sxs-lookup"><span data-stu-id="9fbd4-140">The integration runtime object.</span></span>

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

### <span data-ttu-id="9fbd4-141">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="9fbd4-141">-LicenseType</span></span>
<span data-ttu-id="9fbd4-142">Тип лицензии, которую вы хотите выбрать для ИК-связи служб SSIS.</span><span class="sxs-lookup"><span data-stu-id="9fbd4-142">The license type that you want to select for the SSIS IR.</span></span> <span data-ttu-id="9fbd4-143">Существует два типа: LicenseIncluded или BasePrice.</span><span class="sxs-lookup"><span data-stu-id="9fbd4-143">There are two types: LicenseIncluded or BasePrice.</span></span> <span data-ttu-id="9fbd4-144">Если вы ищете цены на использование гибридной льготы для использования Azure (AHUB), пожалуйста, выберите BasePrice.</span><span class="sxs-lookup"><span data-stu-id="9fbd4-144">If you are qualified for the Azure Hybrid Use Benefit (AHUB) pricing, please select BasePrice.</span></span> <span data-ttu-id="9fbd4-145">Если это не так, пожалуйста, выберите LicenseIncluded.</span><span class="sxs-lookup"><span data-stu-id="9fbd4-145">If not, please select LicenseIncluded.</span></span>

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

### <span data-ttu-id="9fbd4-146">-Location</span><span class="sxs-lookup"><span data-stu-id="9fbd4-146">-Location</span></span>
<span data-ttu-id="9fbd4-147">Расположение среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="9fbd4-147">The integration runtime location.</span></span>

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

### <span data-ttu-id="9fbd4-148">-MaxParallelExecutionsPerNode</span><span class="sxs-lookup"><span data-stu-id="9fbd4-148">-MaxParallelExecutionsPerNode</span></span>
<span data-ttu-id="9fbd4-149">Максимальное количество параллельных выполнений на каждом узле для управляемой среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="9fbd4-149">Maximum parallel execution count per node for a managed dedicated integration runtime.</span></span>

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

### <span data-ttu-id="9fbd4-150">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9fbd4-150">-Name</span></span>
<span data-ttu-id="9fbd4-151">Имя среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="9fbd4-151">The integration runtime name.</span></span>

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

### <span data-ttu-id="9fbd4-152">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="9fbd4-152">-NodeCount</span></span>
<span data-ttu-id="9fbd4-153">Количество целевых узлов в среде выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="9fbd4-153">Target nodes count of the integration runtime.</span></span>

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

### <span data-ttu-id="9fbd4-154">-NodeSize</span><span class="sxs-lookup"><span data-stu-id="9fbd4-154">-NodeSize</span></span>
<span data-ttu-id="9fbd4-155">Размер узла среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="9fbd4-155">The integration runtime node size.</span></span>

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

### <span data-ttu-id="9fbd4-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9fbd4-156">-ResourceGroupName</span></span>
<span data-ttu-id="9fbd4-157">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9fbd4-157">The resource group name.</span></span>

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

### <span data-ttu-id="9fbd4-158">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9fbd4-158">-ResourceId</span></span>
<span data-ttu-id="9fbd4-159">Идентификатор ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="9fbd4-159">The Azure resource ID.</span></span>

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

### <span data-ttu-id="9fbd4-160">-SetupScriptContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="9fbd4-160">-SetupScriptContainerSasUri</span></span>
<span data-ttu-id="9fbd4-161">Универсальный код ресурса (URI) SAS контейнера BLOB-объектов Azure, содержащего настраиваемый сценарий настройки.</span><span class="sxs-lookup"><span data-stu-id="9fbd4-161">The SAS URI of the Azure blob container that contains the custom setup script.</span></span>

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

### <span data-ttu-id="9fbd4-162">-SharedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="9fbd4-162">-SharedIntegrationRuntimeResourceId</span></span>
<span data-ttu-id="9fbd4-163">Идентификатор ресурса общей среды выполнения интеграции с самостоятельным размещением.</span><span class="sxs-lookup"><span data-stu-id="9fbd4-163">The resource id of the shared self-hosted integration runtime.</span></span>

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

### <span data-ttu-id="9fbd4-164">-Подсеть</span><span class="sxs-lookup"><span data-stu-id="9fbd4-164">-Subnet</span></span>
<span data-ttu-id="9fbd4-165">Имя подсети в виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="9fbd4-165">The name of the subnet in the VNet.</span></span>

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

### <span data-ttu-id="9fbd4-166">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="9fbd4-166">-Type</span></span>
<span data-ttu-id="9fbd4-167">Тип среды выполнения Integration.</span><span class="sxs-lookup"><span data-stu-id="9fbd4-167">The integration runtime type.</span></span>

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

### <span data-ttu-id="9fbd4-168">-VNetId</span><span class="sxs-lookup"><span data-stu-id="9fbd4-168">-VNetId</span></span>
<span data-ttu-id="9fbd4-169">ИДЕНТИФИКАТОР виртуальной сети, к которой присоединяется среда выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="9fbd4-169">The ID of the VNet that the integration runtime joins.</span></span>

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

### <span data-ttu-id="9fbd4-170">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9fbd4-170">-Confirm</span></span>
<span data-ttu-id="9fbd4-171">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9fbd4-171">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9fbd4-172">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9fbd4-172">-WhatIf</span></span>
<span data-ttu-id="9fbd4-173">Показано, что происходит при запуске командлета, но не запускает командлет.</span><span class="sxs-lookup"><span data-stu-id="9fbd4-173">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="9fbd4-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fbd4-174">CommonParameters</span></span>
<span data-ttu-id="9fbd4-175">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9fbd4-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fbd4-176">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9fbd4-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fbd4-177">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9fbd4-177">INPUTS</span></span>

### <span data-ttu-id="9fbd4-178">System. String</span><span class="sxs-lookup"><span data-stu-id="9fbd4-178">System.String</span></span>

### <span data-ttu-id="9fbd4-179">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="9fbd4-179">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="9fbd4-180">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9fbd4-180">OUTPUTS</span></span>

### <span data-ttu-id="9fbd4-181">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="9fbd4-181">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="9fbd4-182">Пуск</span><span class="sxs-lookup"><span data-stu-id="9fbd4-182">NOTES</span></span>

## <span data-ttu-id="9fbd4-183">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9fbd4-183">RELATED LINKS</span></span>

[<span data-ttu-id="9fbd4-184">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="9fbd4-184">Set-AzDataFactoryV2IntegrationRuntime</span></span>]()

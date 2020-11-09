---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2.md
ms.openlocfilehash: 5020ddeccc755ef52bf7410d61eb57b637d261bf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94313766"
---
# <span data-ttu-id="59d8e-101">Set-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="59d8e-101">Set-AzDataFactoryV2</span></span>

## <span data-ttu-id="59d8e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="59d8e-102">SYNOPSIS</span></span>
<span data-ttu-id="59d8e-103">Создание фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="59d8e-103">Creates a data factory.</span></span>

## <span data-ttu-id="59d8e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="59d8e-104">SYNTAX</span></span>

### <span data-ttu-id="59d8e-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="59d8e-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>]
 [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59d8e-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="59d8e-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2 [-ResourceId] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59d8e-107">ByResourceIdFactoryRepoVstsConfig</span><span class="sxs-lookup"><span data-stu-id="59d8e-107">ByResourceIdFactoryRepoVstsConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceId] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -ProjectName <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59d8e-108">ByResourceIdFactoryRepoGitConfig</span><span class="sxs-lookup"><span data-stu-id="59d8e-108">ByResourceIdFactoryRepoGitConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceId] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -HostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="59d8e-109">ByFactoryNameFactoryRepoGitConfig</span><span class="sxs-lookup"><span data-stu-id="59d8e-109">ByFactoryNameFactoryRepoGitConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>]
 [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -HostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="59d8e-110">ByFactoryNameFactoryRepoVstsConfig</span><span class="sxs-lookup"><span data-stu-id="59d8e-110">ByFactoryNameFactoryRepoVstsConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>]
 [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -ProjectName <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59d8e-111">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="59d8e-111">ByInputObject</span></span>
```
Set-AzDataFactoryV2 -InputObject <PSDataFactory> [[-Location] <String>] [[-Tag] <Hashtable>] [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59d8e-112">ByInputObjectFactoryRepoVstsConfig</span><span class="sxs-lookup"><span data-stu-id="59d8e-112">ByInputObjectFactoryRepoVstsConfig</span></span>
```
Set-AzDataFactoryV2 -InputObject <PSDataFactory> [[-Location] <String>] [[-Tag] <Hashtable>] [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 [-AccountName <String>] [-RepositoryName <String>] [-CollaborationBranch <String>] [-RootFolder <String>]
 [-LastCommitId <String>] -ProjectName <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59d8e-113">ByInputObjectFactoryRepoGitConfig</span><span class="sxs-lookup"><span data-stu-id="59d8e-113">ByInputObjectFactoryRepoGitConfig</span></span>
```
Set-AzDataFactoryV2 -InputObject <PSDataFactory> [[-Location] <String>] [[-Tag] <Hashtable>] [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 [-AccountName <String>] [-RepositoryName <String>] [-CollaborationBranch <String>] [-RootFolder <String>]
 [-LastCommitId <String>] -HostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="59d8e-114">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="59d8e-114">DESCRIPTION</span></span>
<span data-ttu-id="59d8e-115">Командлет **Set-AzDataFactoryV2** создает фабрику данных с указанным именем группы ресурсов и расположением.</span><span class="sxs-lookup"><span data-stu-id="59d8e-115">The **Set-AzDataFactoryV2** cmdlet creates a data factory with the specified resource group name and location.</span></span>
<span data-ttu-id="59d8e-116">Эти операции выполняются в указанном ниже порядке:--Создание фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="59d8e-116">Perform these operations in the following order: -- Create a data factory.</span></span>
<span data-ttu-id="59d8e-117">--Создание связанных служб.</span><span class="sxs-lookup"><span data-stu-id="59d8e-117">-- Create linked services.</span></span>
<span data-ttu-id="59d8e-118">--Создание наборов данных.</span><span class="sxs-lookup"><span data-stu-id="59d8e-118">-- Create datasets.</span></span>
<span data-ttu-id="59d8e-119">--Создание конвейера.</span><span class="sxs-lookup"><span data-stu-id="59d8e-119">-- Create a pipeline.</span></span>

## <span data-ttu-id="59d8e-120">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="59d8e-120">EXAMPLES</span></span>

### <span data-ttu-id="59d8e-121">Пример 1: Создание фабрики данных</span><span class="sxs-lookup"><span data-stu-id="59d8e-121">Example 1: Create a data factory</span></span>
```
PS C:\> Set-AzDataFactoryV2 -ResourceGroupName "ADF" -Name "WikiADF" -Location "WestUS"

    DataFactoryName   : WikiADF
    DataFactoryId     : /subscriptions/3e8e61b5-9a7d-4952-bfae-545ab997b9ea/resourceGroups/adf/providers/Microsoft.DataFactory/factories/wikiadf
    ResourceGroupName : ADF
    Location          : EastUS
    Tags              : {}
    Identity          : Microsoft.Azure.Management.DataFactory.Models.FactoryIdentity
    ProvisioningState : Succeeded
    RepoConfiguration :
```

### <span data-ttu-id="59d8e-122">Пример 2: Создание фабрики данных с подробными сведениями о конфигурации репозитория с помощью существующего объекта фабрики.</span><span class="sxs-lookup"><span data-stu-id="59d8e-122">Example 2: Create a data factory with repo configuration details using an existing factory object.</span></span>
```
PS C:\> Get-AzDataFactoryV2 -ResourceGroupName "ADF" -Name "WikiADF" | Set-AzDataFactoryV2 -AccountName msdata -RepositoryName ADFRepo -CollaborationBranch master -RootFolder / -ProjectName "Azure Data Factory"

    DataFactoryName   : WikiADF
    DataFactoryId     : /subscriptions/3e8e61b5-9a7d-4952-bfae-545ab997b9ea/resourceGroups/adf/providers/Microsoft.DataFactory/factories/wikiadf
    ResourceGroupName : ADF
    Location          : EastUS
    Tags              : {}
    Identity          : Microsoft.Azure.Management.DataFactory.Models.FactoryIdentity
    ProvisioningState : Succeeded
    RepoConfiguration : Microsoft.Azure.Management.DataFactory.Models.FactoryVSTSConfiguration
```

<span data-ttu-id="59d8e-123">Эта команда создает фабрику данных с именем WikiADF в группе ресурсов "ADF" в расположении EastUS с конфигурацией системы управления версиями для Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="59d8e-123">This command creates a data factory named WikiADF in the resource group named ADF in the EastUS location with Azure DevOps source control configuration.</span></span>

### <span data-ttu-id="59d8e-124">Пример 3: Создание фабрики данных с подробными сведениями о конфигурации репозитория GitHub с помощью нового объекта фабрики.</span><span class="sxs-lookup"><span data-stu-id="59d8e-124">Example 3: Create a data factory with GitHub repo configuration details using a new factory object.</span></span>
```
PS C:\> New-AzDataFactoryV2 -ResourceGroupName "ADF" -Name "WikiADF" -Location 'EastUS' -HostName 'https://github.com' -AccountName msdata -RepositoryName ADFRepo -CollaborationBranch master -RootFolder /

    DataFactoryName   : WikiADF
    DataFactoryId     : /subscriptions/3e8e61b5-9a7d-4952-bfae-545ab997b9ea/resourceGroups/adf/providers/Microsoft.DataFactory/factories/wikiadf
    ResourceGroupName : ADF
    Location          : EastUS
    Tags              : {}
    Identity          : Microsoft.Azure.Management.DataFactory.Models.FactoryIdentity
    ProvisioningState : Succeeded
    RepoConfiguration : Microsoft.Azure.Management.DataFactory.Models.FactoryGitHubConfiguration
```

<span data-ttu-id="59d8e-125">Эта команда создает фабрику данных с именем WikiADF в группе ресурсов с именем ADF в расположении EastUS с конфигурацией системы управления версиями для GitHub...</span><span class="sxs-lookup"><span data-stu-id="59d8e-125">This command creates a data factory named WikiADF in the resource group named ADF in the EastUS location with GitHub source control configuration..</span></span>

## <span data-ttu-id="59d8e-126">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="59d8e-126">PARAMETERS</span></span>

### <span data-ttu-id="59d8e-127">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="59d8e-127">-AccountName</span></span>
<span data-ttu-id="59d8e-128">Имя учетной записи для конфигурации репозитория.</span><span class="sxs-lookup"><span data-stu-id="59d8e-128">The account name for repo configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdFactoryRepoVstsConfig, ByResourceIdFactoryRepoGitConfig, ByFactoryNameFactoryRepoGitConfig, ByFactoryNameFactoryRepoVstsConfig
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByInputObjectFactoryRepoVstsConfig, ByInputObjectFactoryRepoGitConfig
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59d8e-129">-CollaborationBranch</span><span class="sxs-lookup"><span data-stu-id="59d8e-129">-CollaborationBranch</span></span>
<span data-ttu-id="59d8e-130">Ветвь совместной работы для конфигурации репозитория.</span><span class="sxs-lookup"><span data-stu-id="59d8e-130">The collaboration branch for repo configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdFactoryRepoVstsConfig, ByResourceIdFactoryRepoGitConfig, ByFactoryNameFactoryRepoGitConfig, ByFactoryNameFactoryRepoVstsConfig
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByInputObjectFactoryRepoVstsConfig, ByInputObjectFactoryRepoGitConfig
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59d8e-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59d8e-131">-DefaultProfile</span></span>
<span data-ttu-id="59d8e-132">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="59d8e-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="59d8e-133">-Force</span><span class="sxs-lookup"><span data-stu-id="59d8e-133">-Force</span></span>
<span data-ttu-id="59d8e-134">Запускает командлет без запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="59d8e-134">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="59d8e-135">-GlobalParameterDefinition</span><span class="sxs-lookup"><span data-stu-id="59d8e-135">-GlobalParameterDefinition</span></span>
<span data-ttu-id="59d8e-136">Словарь, содержащий глобальные параметры фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="59d8e-136">The dictionary containing the global parameters of the data factory.</span></span>

```yaml
Type: System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59d8e-137">-HostName</span><span class="sxs-lookup"><span data-stu-id="59d8e-137">-HostName</span></span>
<span data-ttu-id="59d8e-138">Имя узла для конфигурации репозитория GitHub.</span><span class="sxs-lookup"><span data-stu-id="59d8e-138">The host name for GitHub repo configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdFactoryRepoGitConfig, ByFactoryNameFactoryRepoGitConfig, ByInputObjectFactoryRepoGitConfig
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59d8e-139">-InputObject</span><span class="sxs-lookup"><span data-stu-id="59d8e-139">-InputObject</span></span>
<span data-ttu-id="59d8e-140">Объект фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="59d8e-140">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByInputObject, ByInputObjectFactoryRepoVstsConfig, ByInputObjectFactoryRepoGitConfig
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="59d8e-141">-LastCommitId</span><span class="sxs-lookup"><span data-stu-id="59d8e-141">-LastCommitId</span></span>
<span data-ttu-id="59d8e-142">Последний идентификатор фиксации для конфигурации репозитория.</span><span class="sxs-lookup"><span data-stu-id="59d8e-142">The last commit id for repo configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdFactoryRepoVstsConfig, ByResourceIdFactoryRepoGitConfig, ByFactoryNameFactoryRepoGitConfig, ByFactoryNameFactoryRepoVstsConfig, ByInputObjectFactoryRepoVstsConfig, ByInputObjectFactoryRepoGitConfig
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59d8e-143">-Location</span><span class="sxs-lookup"><span data-stu-id="59d8e-143">-Location</span></span>
<span data-ttu-id="59d8e-144">Фабрика данных создается в этом регионе.</span><span class="sxs-lookup"><span data-stu-id="59d8e-144">The data factory is created in this region.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByResourceId, ByResourceIdFactoryRepoVstsConfig, ByResourceIdFactoryRepoGitConfig, ByFactoryNameFactoryRepoGitConfig, ByFactoryNameFactoryRepoVstsConfig
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByInputObject, ByInputObjectFactoryRepoVstsConfig, ByInputObjectFactoryRepoGitConfig
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59d8e-145">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="59d8e-145">-Name</span></span>
<span data-ttu-id="59d8e-146">Имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="59d8e-146">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryNameFactoryRepoGitConfig, ByFactoryNameFactoryRepoVstsConfig
Aliases: DataFactoryName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59d8e-147">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="59d8e-147">-ProjectName</span></span>
<span data-ttu-id="59d8e-148">Имя проекта Azure DevOps для конфигурации репозитория.</span><span class="sxs-lookup"><span data-stu-id="59d8e-148">The project name Azure DevOps for repo configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdFactoryRepoVstsConfig, ByFactoryNameFactoryRepoVstsConfig, ByInputObjectFactoryRepoVstsConfig
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59d8e-149">-RepositoryName</span><span class="sxs-lookup"><span data-stu-id="59d8e-149">-RepositoryName</span></span>
<span data-ttu-id="59d8e-150">Имя репозитория для конфигурации репозитория.</span><span class="sxs-lookup"><span data-stu-id="59d8e-150">The repository name for repo configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdFactoryRepoVstsConfig, ByResourceIdFactoryRepoGitConfig, ByFactoryNameFactoryRepoGitConfig, ByFactoryNameFactoryRepoVstsConfig
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByInputObjectFactoryRepoVstsConfig, ByInputObjectFactoryRepoGitConfig
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59d8e-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59d8e-151">-ResourceGroupName</span></span>
<span data-ttu-id="59d8e-152">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="59d8e-152">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryNameFactoryRepoGitConfig, ByFactoryNameFactoryRepoVstsConfig
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59d8e-153">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="59d8e-153">-ResourceId</span></span>
<span data-ttu-id="59d8e-154">Идентификатор ресурса Azure фабрики данных v2.</span><span class="sxs-lookup"><span data-stu-id="59d8e-154">The Azure resource ID of V2 data factory.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId, ByResourceIdFactoryRepoVstsConfig, ByResourceIdFactoryRepoGitConfig
Aliases: Id, DataFactoryId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59d8e-155">-RootFolder</span><span class="sxs-lookup"><span data-stu-id="59d8e-155">-RootFolder</span></span>
<span data-ttu-id="59d8e-156">Корневая папка для конфигурации репозитория.</span><span class="sxs-lookup"><span data-stu-id="59d8e-156">The root folder for repo configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdFactoryRepoVstsConfig, ByResourceIdFactoryRepoGitConfig, ByFactoryNameFactoryRepoGitConfig, ByFactoryNameFactoryRepoVstsConfig
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByInputObjectFactoryRepoVstsConfig, ByInputObjectFactoryRepoGitConfig
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59d8e-157">-Тег</span><span class="sxs-lookup"><span data-stu-id="59d8e-157">-Tag</span></span>
<span data-ttu-id="59d8e-158">Теги фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="59d8e-158">The tags of the data factory.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByFactoryName, ByResourceId, ByResourceIdFactoryRepoVstsConfig, ByResourceIdFactoryRepoGitConfig, ByFactoryNameFactoryRepoGitConfig, ByFactoryNameFactoryRepoVstsConfig
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByInputObject, ByInputObjectFactoryRepoVstsConfig, ByInputObjectFactoryRepoGitConfig
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59d8e-159">-TenantId</span><span class="sxs-lookup"><span data-stu-id="59d8e-159">-TenantId</span></span>
<span data-ttu-id="59d8e-160">Идентификатор клиента для конфигурации репозитория Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="59d8e-160">The tenant id for Azure DevOps repo configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdFactoryRepoVstsConfig, ByFactoryNameFactoryRepoVstsConfig, ByInputObjectFactoryRepoVstsConfig
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59d8e-161">-Confirm</span><span class="sxs-lookup"><span data-stu-id="59d8e-161">-Confirm</span></span>
<span data-ttu-id="59d8e-162">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="59d8e-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59d8e-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59d8e-163">-WhatIf</span></span>
<span data-ttu-id="59d8e-164">Показано, что происходит при запуске командлета, но не запускает командлет.</span><span class="sxs-lookup"><span data-stu-id="59d8e-164">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="59d8e-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59d8e-165">CommonParameters</span></span>
<span data-ttu-id="59d8e-166">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="59d8e-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59d8e-167">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="59d8e-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59d8e-168">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="59d8e-168">INPUTS</span></span>

### <span data-ttu-id="59d8e-169">System. String</span><span class="sxs-lookup"><span data-stu-id="59d8e-169">System.String</span></span>

### <span data-ttu-id="59d8e-170">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="59d8e-170">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

### <span data-ttu-id="59d8e-171">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="59d8e-171">System.Collections.Hashtable</span></span>

## <span data-ttu-id="59d8e-172">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="59d8e-172">OUTPUTS</span></span>

### <span data-ttu-id="59d8e-173">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="59d8e-173">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="59d8e-174">Пуск</span><span class="sxs-lookup"><span data-stu-id="59d8e-174">NOTES</span></span>
<span data-ttu-id="59d8e-175">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики</span><span class="sxs-lookup"><span data-stu-id="59d8e-175">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="59d8e-176">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="59d8e-176">RELATED LINKS</span></span>

[<span data-ttu-id="59d8e-177">Get-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="59d8e-177">Get-AzDataFactoryV2</span></span>]()

[<span data-ttu-id="59d8e-178">Remove-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="59d8e-178">Remove-AzDataFactoryV2</span></span>]()

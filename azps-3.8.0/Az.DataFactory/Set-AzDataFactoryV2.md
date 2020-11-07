---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2.md
ms.openlocfilehash: 219e5b18a04332d2ee840fb41b92aa9d282a1792
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912807"
---
# <span data-ttu-id="e9d1b-101">Set-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="e9d1b-101">Set-AzDataFactoryV2</span></span>

## <span data-ttu-id="e9d1b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e9d1b-102">SYNOPSIS</span></span>
<span data-ttu-id="e9d1b-103">Создание фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="e9d1b-103">Creates a data factory.</span></span>

## <span data-ttu-id="e9d1b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e9d1b-104">SYNTAX</span></span>

### <span data-ttu-id="e9d1b-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e9d1b-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9d1b-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e9d1b-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2 [-ResourceId] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9d1b-107">ByResourceIdFactoryRepoVstsConfig</span><span class="sxs-lookup"><span data-stu-id="e9d1b-107">ByResourceIdFactoryRepoVstsConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceId] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -ProjectName <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9d1b-108">ByResourceIdFactoryRepoGitConfig</span><span class="sxs-lookup"><span data-stu-id="e9d1b-108">ByResourceIdFactoryRepoGitConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceId] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -HostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e9d1b-109">ByFactoryNameFactoryRepoGitConfig</span><span class="sxs-lookup"><span data-stu-id="e9d1b-109">ByFactoryNameFactoryRepoGitConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>]
 [-Force] -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -HostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e9d1b-110">ByFactoryNameFactoryRepoVstsConfig</span><span class="sxs-lookup"><span data-stu-id="e9d1b-110">ByFactoryNameFactoryRepoVstsConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>]
 [-Force] -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -ProjectName <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9d1b-111">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="e9d1b-111">ByInputObject</span></span>
```
Set-AzDataFactoryV2 -InputObject <PSDataFactory> [[-Location] <String>] [[-Tag] <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9d1b-112">ByInputObjectFactoryRepoVstsConfig</span><span class="sxs-lookup"><span data-stu-id="e9d1b-112">ByInputObjectFactoryRepoVstsConfig</span></span>
```
Set-AzDataFactoryV2 -InputObject <PSDataFactory> [[-Location] <String>] [[-Tag] <Hashtable>] [-Force]
 [-AccountName <String>] [-RepositoryName <String>] [-CollaborationBranch <String>] [-RootFolder <String>]
 [-LastCommitId <String>] -ProjectName <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9d1b-113">ByInputObjectFactoryRepoGitConfig</span><span class="sxs-lookup"><span data-stu-id="e9d1b-113">ByInputObjectFactoryRepoGitConfig</span></span>
```
Set-AzDataFactoryV2 -InputObject <PSDataFactory> [[-Location] <String>] [[-Tag] <Hashtable>] [-Force]
 [-AccountName <String>] [-RepositoryName <String>] [-CollaborationBranch <String>] [-RootFolder <String>]
 [-LastCommitId <String>] -HostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e9d1b-114">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e9d1b-114">DESCRIPTION</span></span>
<span data-ttu-id="e9d1b-115">Командлет **Set-AzDataFactoryV2** создает фабрику данных с указанным именем группы ресурсов и расположением.</span><span class="sxs-lookup"><span data-stu-id="e9d1b-115">The **Set-AzDataFactoryV2** cmdlet creates a data factory with the specified resource group name and location.</span></span>
<span data-ttu-id="e9d1b-116">Эти операции выполняются в указанном ниже порядке:--Создание фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="e9d1b-116">Perform these operations in the following order: -- Create a data factory.</span></span>
<span data-ttu-id="e9d1b-117">--Создание связанных служб.</span><span class="sxs-lookup"><span data-stu-id="e9d1b-117">-- Create linked services.</span></span>
<span data-ttu-id="e9d1b-118">--Создание наборов данных.</span><span class="sxs-lookup"><span data-stu-id="e9d1b-118">-- Create datasets.</span></span>
<span data-ttu-id="e9d1b-119">--Создание конвейера.</span><span class="sxs-lookup"><span data-stu-id="e9d1b-119">-- Create a pipeline.</span></span>

## <span data-ttu-id="e9d1b-120">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e9d1b-120">EXAMPLES</span></span>

### <span data-ttu-id="e9d1b-121">Пример 1: Создание фабрики данных</span><span class="sxs-lookup"><span data-stu-id="e9d1b-121">Example 1: Create a data factory</span></span>
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

### <span data-ttu-id="e9d1b-122">Пример 2: Создание фабрики данных с подробными сведениями о конфигурации репозитория с помощью существующего объекта фабрики.</span><span class="sxs-lookup"><span data-stu-id="e9d1b-122">Example 2: Create a data factory with repo configuration details using an existing factory object.</span></span>
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

<span data-ttu-id="e9d1b-123">Эта команда создает фабрику данных с именем WikiADF в группе ресурсов "ADF" в расположении EastUS с конфигурацией системы управления версиями для Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="e9d1b-123">This command creates a data factory named WikiADF in the resource group named ADF in the EastUS location with Azure DevOps source control configuration.</span></span>

### <span data-ttu-id="e9d1b-124">Пример 3: Создание фабрики данных с подробными сведениями о конфигурации репозитория GitHub с помощью нового объекта фабрики.</span><span class="sxs-lookup"><span data-stu-id="e9d1b-124">Example 3: Create a data factory with GitHub repo configuration details using a new factory object.</span></span>
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

<span data-ttu-id="e9d1b-125">Эта команда создает фабрику данных с именем WikiADF в группе ресурсов с именем ADF в расположении EastUS с конфигурацией системы управления версиями для GitHub...</span><span class="sxs-lookup"><span data-stu-id="e9d1b-125">This command creates a data factory named WikiADF in the resource group named ADF in the EastUS location with GitHub source control configuration..</span></span>

## <span data-ttu-id="e9d1b-126">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e9d1b-126">PARAMETERS</span></span>

### <span data-ttu-id="e9d1b-127">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="e9d1b-127">-AccountName</span></span>
<span data-ttu-id="e9d1b-128">Имя учетной записи для конфигурации репозитория.</span><span class="sxs-lookup"><span data-stu-id="e9d1b-128">The account name for repo configuration.</span></span>

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

### <span data-ttu-id="e9d1b-129">-CollaborationBranch</span><span class="sxs-lookup"><span data-stu-id="e9d1b-129">-CollaborationBranch</span></span>
<span data-ttu-id="e9d1b-130">Ветвь совместной работы для конфигурации репозитория.</span><span class="sxs-lookup"><span data-stu-id="e9d1b-130">The collaboration branch for repo configuration.</span></span>

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

### <span data-ttu-id="e9d1b-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9d1b-131">-DefaultProfile</span></span>
<span data-ttu-id="e9d1b-132">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e9d1b-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e9d1b-133">-Force</span><span class="sxs-lookup"><span data-stu-id="e9d1b-133">-Force</span></span>
<span data-ttu-id="e9d1b-134">Запускает командлет без запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="e9d1b-134">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="e9d1b-135">-HostName</span><span class="sxs-lookup"><span data-stu-id="e9d1b-135">-HostName</span></span>
<span data-ttu-id="e9d1b-136">Имя узла для конфигурации репозитория GitHub.</span><span class="sxs-lookup"><span data-stu-id="e9d1b-136">The host name for GitHub repo configuration.</span></span>

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

### <span data-ttu-id="e9d1b-137">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e9d1b-137">-InputObject</span></span>
<span data-ttu-id="e9d1b-138">Объект фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="e9d1b-138">The data factory object.</span></span>

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

### <span data-ttu-id="e9d1b-139">-LastCommitId</span><span class="sxs-lookup"><span data-stu-id="e9d1b-139">-LastCommitId</span></span>
<span data-ttu-id="e9d1b-140">Последний идентификатор фиксации для конфигурации репозитория.</span><span class="sxs-lookup"><span data-stu-id="e9d1b-140">The last commit id for repo configuration.</span></span>

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

### <span data-ttu-id="e9d1b-141">-Location</span><span class="sxs-lookup"><span data-stu-id="e9d1b-141">-Location</span></span>
<span data-ttu-id="e9d1b-142">Фабрика данных создается в этом регионе.</span><span class="sxs-lookup"><span data-stu-id="e9d1b-142">The data factory is created in this region.</span></span>

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

### <span data-ttu-id="e9d1b-143">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e9d1b-143">-Name</span></span>
<span data-ttu-id="e9d1b-144">Имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="e9d1b-144">The data factory name.</span></span>

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

### <span data-ttu-id="e9d1b-145">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="e9d1b-145">-ProjectName</span></span>
<span data-ttu-id="e9d1b-146">Имя проекта Azure DevOps для конфигурации репозитория.</span><span class="sxs-lookup"><span data-stu-id="e9d1b-146">The project name Azure DevOps for repo configuration.</span></span>

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

### <span data-ttu-id="e9d1b-147">-RepositoryName</span><span class="sxs-lookup"><span data-stu-id="e9d1b-147">-RepositoryName</span></span>
<span data-ttu-id="e9d1b-148">Имя репозитория для конфигурации репозитория.</span><span class="sxs-lookup"><span data-stu-id="e9d1b-148">The repository name for repo configuration.</span></span>

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

### <span data-ttu-id="e9d1b-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9d1b-149">-ResourceGroupName</span></span>
<span data-ttu-id="e9d1b-150">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e9d1b-150">The resource group name.</span></span>

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

### <span data-ttu-id="e9d1b-151">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e9d1b-151">-ResourceId</span></span>
<span data-ttu-id="e9d1b-152">Идентификатор ресурса Azure фабрики данных v2.</span><span class="sxs-lookup"><span data-stu-id="e9d1b-152">The Azure resource ID of V2 data factory.</span></span>

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

### <span data-ttu-id="e9d1b-153">-RootFolder</span><span class="sxs-lookup"><span data-stu-id="e9d1b-153">-RootFolder</span></span>
<span data-ttu-id="e9d1b-154">Корневая папка для конфигурации репозитория.</span><span class="sxs-lookup"><span data-stu-id="e9d1b-154">The root folder for repo configuration.</span></span>

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

### <span data-ttu-id="e9d1b-155">-Тег</span><span class="sxs-lookup"><span data-stu-id="e9d1b-155">-Tag</span></span>
<span data-ttu-id="e9d1b-156">Теги фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="e9d1b-156">The tags of the data factory.</span></span>

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

### <span data-ttu-id="e9d1b-157">-TenantId</span><span class="sxs-lookup"><span data-stu-id="e9d1b-157">-TenantId</span></span>
<span data-ttu-id="e9d1b-158">Идентификатор клиента для конфигурации репозитория Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="e9d1b-158">The tenant id for Azure DevOps repo configuration.</span></span>

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

### <span data-ttu-id="e9d1b-159">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e9d1b-159">-Confirm</span></span>
<span data-ttu-id="e9d1b-160">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e9d1b-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9d1b-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9d1b-161">-WhatIf</span></span>
<span data-ttu-id="e9d1b-162">Показано, что происходит при запуске командлета, но не запускает командлет.</span><span class="sxs-lookup"><span data-stu-id="e9d1b-162">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="e9d1b-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9d1b-163">CommonParameters</span></span>
<span data-ttu-id="e9d1b-164">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e9d1b-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9d1b-165">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9d1b-165">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9d1b-166">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e9d1b-166">INPUTS</span></span>

### <span data-ttu-id="e9d1b-167">System. String</span><span class="sxs-lookup"><span data-stu-id="e9d1b-167">System.String</span></span>

### <span data-ttu-id="e9d1b-168">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="e9d1b-168">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e9d1b-169">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e9d1b-169">OUTPUTS</span></span>

### <span data-ttu-id="e9d1b-170">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="e9d1b-170">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="e9d1b-171">Пуск</span><span class="sxs-lookup"><span data-stu-id="e9d1b-171">NOTES</span></span>
<span data-ttu-id="e9d1b-172">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики</span><span class="sxs-lookup"><span data-stu-id="e9d1b-172">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="e9d1b-173">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e9d1b-173">RELATED LINKS</span></span>

[<span data-ttu-id="e9d1b-174">Get-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="e9d1b-174">Get-AzDataFactoryV2</span></span>]()

[<span data-ttu-id="e9d1b-175">Remove-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="e9d1b-175">Remove-AzDataFactoryV2</span></span>]()

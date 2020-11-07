---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2.md
ms.openlocfilehash: 374263c26a3572e8d85e18d1795c27a761866a4a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721442"
---
# <span data-ttu-id="8cda0-101">Set-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="8cda0-101">Set-AzDataFactoryV2</span></span>

## <span data-ttu-id="8cda0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8cda0-102">SYNOPSIS</span></span>
<span data-ttu-id="8cda0-103">Создание фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="8cda0-103">Creates a data factory.</span></span>

## <span data-ttu-id="8cda0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8cda0-104">SYNTAX</span></span>

### <span data-ttu-id="8cda0-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8cda0-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8cda0-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="8cda0-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2 [-ResourceId] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8cda0-107">ByResourceIdFactoryRepoVstsConfig</span><span class="sxs-lookup"><span data-stu-id="8cda0-107">ByResourceIdFactoryRepoVstsConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceId] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -ProjectName <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8cda0-108">ByResourceIdFactoryRepoGitConfig</span><span class="sxs-lookup"><span data-stu-id="8cda0-108">ByResourceIdFactoryRepoGitConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceId] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -HostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8cda0-109">ByFactoryNameFactoryRepoGitConfig</span><span class="sxs-lookup"><span data-stu-id="8cda0-109">ByFactoryNameFactoryRepoGitConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>]
 [-Force] -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -HostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8cda0-110">ByFactoryNameFactoryRepoVstsConfig</span><span class="sxs-lookup"><span data-stu-id="8cda0-110">ByFactoryNameFactoryRepoVstsConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>]
 [-Force] -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -ProjectName <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8cda0-111">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="8cda0-111">ByInputObject</span></span>
```
Set-AzDataFactoryV2 -InputObject <PSDataFactory> [[-Location] <String>] [[-Tag] <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8cda0-112">ByInputObjectFactoryRepoVstsConfig</span><span class="sxs-lookup"><span data-stu-id="8cda0-112">ByInputObjectFactoryRepoVstsConfig</span></span>
```
Set-AzDataFactoryV2 -InputObject <PSDataFactory> [[-Location] <String>] [[-Tag] <Hashtable>] [-Force]
 [-AccountName <String>] [-RepositoryName <String>] [-CollaborationBranch <String>] [-RootFolder <String>]
 [-LastCommitId <String>] -ProjectName <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8cda0-113">ByInputObjectFactoryRepoGitConfig</span><span class="sxs-lookup"><span data-stu-id="8cda0-113">ByInputObjectFactoryRepoGitConfig</span></span>
```
Set-AzDataFactoryV2 -InputObject <PSDataFactory> [[-Location] <String>] [[-Tag] <Hashtable>] [-Force]
 [-AccountName <String>] [-RepositoryName <String>] [-CollaborationBranch <String>] [-RootFolder <String>]
 [-LastCommitId <String>] -HostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8cda0-114">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8cda0-114">DESCRIPTION</span></span>
<span data-ttu-id="8cda0-115">Командлет **Set-AzDataFactoryV2** создает фабрику данных с указанным именем группы ресурсов и расположением.</span><span class="sxs-lookup"><span data-stu-id="8cda0-115">The **Set-AzDataFactoryV2** cmdlet creates a data factory with the specified resource group name and location.</span></span>
<span data-ttu-id="8cda0-116">Эти операции выполняются в указанном ниже порядке:--Создание фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="8cda0-116">Perform these operations in the following order: -- Create a data factory.</span></span>
<span data-ttu-id="8cda0-117">--Создание связанных служб.</span><span class="sxs-lookup"><span data-stu-id="8cda0-117">-- Create linked services.</span></span>
<span data-ttu-id="8cda0-118">--Создание наборов данных.</span><span class="sxs-lookup"><span data-stu-id="8cda0-118">-- Create datasets.</span></span>
<span data-ttu-id="8cda0-119">--Создание конвейера.</span><span class="sxs-lookup"><span data-stu-id="8cda0-119">-- Create a pipeline.</span></span>

## <span data-ttu-id="8cda0-120">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8cda0-120">EXAMPLES</span></span>

### <span data-ttu-id="8cda0-121">Пример 1: Создание фабрики данных</span><span class="sxs-lookup"><span data-stu-id="8cda0-121">Example 1: Create a data factory</span></span>
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

### <span data-ttu-id="8cda0-122">Пример 2: Создание фабрики данных со сведениями о repoconfiguration с помощью существующего объекта фабрики.</span><span class="sxs-lookup"><span data-stu-id="8cda0-122">Example 2: Create a data factory with repoconfiguration details using an existing factory object.</span></span>
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

<span data-ttu-id="8cda0-123">Эта команда создает фабрику данных с именем WikiADF в группе ресурсов с именем ADF в расположении WestUS.</span><span class="sxs-lookup"><span data-stu-id="8cda0-123">This command creates a data factory named WikiADF in the resource group named ADF in the WestUS location.</span></span>

## <span data-ttu-id="8cda0-124">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8cda0-124">PARAMETERS</span></span>

### <span data-ttu-id="8cda0-125">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="8cda0-125">-AccountName</span></span>
<span data-ttu-id="8cda0-126">Имя учетной записи для конфигурации репозитория.</span><span class="sxs-lookup"><span data-stu-id="8cda0-126">The account name for repo configuration.</span></span>

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

### <span data-ttu-id="8cda0-127">-CollaborationBranch</span><span class="sxs-lookup"><span data-stu-id="8cda0-127">-CollaborationBranch</span></span>
<span data-ttu-id="8cda0-128">Ветвь совместной работы для конфигурации репозитория.</span><span class="sxs-lookup"><span data-stu-id="8cda0-128">The collaboration branch for repo configuration.</span></span>

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

### <span data-ttu-id="8cda0-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cda0-129">-DefaultProfile</span></span>
<span data-ttu-id="8cda0-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8cda0-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8cda0-131">-Force</span><span class="sxs-lookup"><span data-stu-id="8cda0-131">-Force</span></span>
<span data-ttu-id="8cda0-132">Запускает командлет без запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="8cda0-132">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="8cda0-133">-HostName</span><span class="sxs-lookup"><span data-stu-id="8cda0-133">-HostName</span></span>
<span data-ttu-id="8cda0-134">Имя узла для конфигурации репозитория.</span><span class="sxs-lookup"><span data-stu-id="8cda0-134">The host name for repo configuration.</span></span>

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

### <span data-ttu-id="8cda0-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8cda0-135">-InputObject</span></span>
<span data-ttu-id="8cda0-136">Объект фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="8cda0-136">The data factory object.</span></span>

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

### <span data-ttu-id="8cda0-137">-LastCommitId</span><span class="sxs-lookup"><span data-stu-id="8cda0-137">-LastCommitId</span></span>
<span data-ttu-id="8cda0-138">Последний идентификатор фиксации для конфигурации репозитория.</span><span class="sxs-lookup"><span data-stu-id="8cda0-138">The last commit id for repo configuration.</span></span>

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

### <span data-ttu-id="8cda0-139">-Location</span><span class="sxs-lookup"><span data-stu-id="8cda0-139">-Location</span></span>
<span data-ttu-id="8cda0-140">Фабрика данных создается в этом регионе.</span><span class="sxs-lookup"><span data-stu-id="8cda0-140">The data factory is created in this region.</span></span>

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

### <span data-ttu-id="8cda0-141">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8cda0-141">-Name</span></span>
<span data-ttu-id="8cda0-142">Имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="8cda0-142">The data factory name.</span></span>

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

### <span data-ttu-id="8cda0-143">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="8cda0-143">-ProjectName</span></span>
<span data-ttu-id="8cda0-144">Название проекта для конфигурации репозитория.</span><span class="sxs-lookup"><span data-stu-id="8cda0-144">The project name for repo configuration.</span></span>

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

### <span data-ttu-id="8cda0-145">-RepositoryName</span><span class="sxs-lookup"><span data-stu-id="8cda0-145">-RepositoryName</span></span>
<span data-ttu-id="8cda0-146">Имя репозитория для конфигурации репозитория.</span><span class="sxs-lookup"><span data-stu-id="8cda0-146">The repository name for repo configuration.</span></span>

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

### <span data-ttu-id="8cda0-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8cda0-147">-ResourceGroupName</span></span>
<span data-ttu-id="8cda0-148">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8cda0-148">The resource group name.</span></span>

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

### <span data-ttu-id="8cda0-149">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8cda0-149">-ResourceId</span></span>
<span data-ttu-id="8cda0-150">Идентификатор ресурса Azure фабрики данных v2.</span><span class="sxs-lookup"><span data-stu-id="8cda0-150">The Azure resource ID of V2 data factory.</span></span>

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

### <span data-ttu-id="8cda0-151">-RootFolder</span><span class="sxs-lookup"><span data-stu-id="8cda0-151">-RootFolder</span></span>
<span data-ttu-id="8cda0-152">Корневая папка для конфигурации репозитория.</span><span class="sxs-lookup"><span data-stu-id="8cda0-152">The root folder for repo configuration.</span></span>

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

### <span data-ttu-id="8cda0-153">-Тег</span><span class="sxs-lookup"><span data-stu-id="8cda0-153">-Tag</span></span>
<span data-ttu-id="8cda0-154">Теги фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="8cda0-154">The tags of the data factory.</span></span>

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

### <span data-ttu-id="8cda0-155">-TenantId</span><span class="sxs-lookup"><span data-stu-id="8cda0-155">-TenantId</span></span>
<span data-ttu-id="8cda0-156">Идентификатор клиента для конфигурации репозитория.</span><span class="sxs-lookup"><span data-stu-id="8cda0-156">The tenant id for repo configuration.</span></span>

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

### <span data-ttu-id="8cda0-157">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8cda0-157">-Confirm</span></span>
<span data-ttu-id="8cda0-158">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8cda0-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8cda0-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8cda0-159">-WhatIf</span></span>
<span data-ttu-id="8cda0-160">Показано, что происходит при запуске командлета, но не запускает командлет.</span><span class="sxs-lookup"><span data-stu-id="8cda0-160">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="8cda0-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cda0-161">CommonParameters</span></span>
<span data-ttu-id="8cda0-162">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8cda0-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cda0-163">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8cda0-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cda0-164">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8cda0-164">INPUTS</span></span>

### <span data-ttu-id="8cda0-165">System. String</span><span class="sxs-lookup"><span data-stu-id="8cda0-165">System.String</span></span>

### <span data-ttu-id="8cda0-166">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="8cda0-166">System.Collections.Hashtable</span></span>

## <span data-ttu-id="8cda0-167">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8cda0-167">OUTPUTS</span></span>

### <span data-ttu-id="8cda0-168">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="8cda0-168">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="8cda0-169">Пуск</span><span class="sxs-lookup"><span data-stu-id="8cda0-169">NOTES</span></span>
<span data-ttu-id="8cda0-170">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики</span><span class="sxs-lookup"><span data-stu-id="8cda0-170">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="8cda0-171">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8cda0-171">RELATED LINKS</span></span>

[<span data-ttu-id="8cda0-172">Get-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="8cda0-172">Get-AzDataFactoryV2</span></span>]()

[<span data-ttu-id="8cda0-173">Remove-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="8cda0-173">Remove-AzDataFactoryV2</span></span>]()

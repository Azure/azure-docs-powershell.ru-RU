---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/set-azurermdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 8b91e1a68fc731476240021889cc80c9c4848357
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563635"
---
# <span data-ttu-id="529f9-101">Set-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="529f9-101">Set-AzureRmDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="529f9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="529f9-102">SYNOPSIS</span></span>
<span data-ttu-id="529f9-103">Обновляет среду выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="529f9-103">Updates an integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="529f9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="529f9-104">SYNTAX</span></span>

### <span data-ttu-id="529f9-105">ByIntegrationRuntimeName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="529f9-105">ByIntegrationRuntimeName (Default)</span></span>
```
Set-AzureRmDataFactoryV2IntegrationRuntime [-Type <String>] [-Description <String>] [-Location <String>]
 [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-SetupScriptContainerSasUri <String>] [-Edition <String>] [-MaxParallelExecutionsPerNode <Int32>]
 [-LicenseType <String>] [-AuthKey <SecureString>] [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="529f9-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="529f9-106">ByResourceId</span></span>
```
Set-AzureRmDataFactoryV2IntegrationRuntime [-Type <String>] [-Description <String>] [-Location <String>]
 [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-SetupScriptContainerSasUri <String>] [-Edition <String>] [-MaxParallelExecutionsPerNode <Int32>]
 [-LicenseType <String>] [-AuthKey <SecureString>] [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="529f9-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="529f9-107">ByIntegrationRuntimeObject</span></span>
```
Set-AzureRmDataFactoryV2IntegrationRuntime [-Type <String>] [-Description <String>] [-Location <String>]
 [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-SetupScriptContainerSasUri <String>] [-Edition <String>] [-MaxParallelExecutionsPerNode <Int32>]
 [-LicenseType <String>] [-AuthKey <SecureString>] [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="529f9-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="529f9-108">DESCRIPTION</span></span>
<span data-ttu-id="529f9-109">Командлет Set-AzureRmDataFactoryV2IntegrationRuntime обновляет среду выполнения интеграции с определенными параметрами.</span><span class="sxs-lookup"><span data-stu-id="529f9-109">The Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet updates an integration runtime with specific parameters.</span></span>

## <span data-ttu-id="529f9-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="529f9-110">EXAMPLES</span></span>

### <span data-ttu-id="529f9-111">Пример 1: Описание обновления среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="529f9-111">Example 1: Update integration runtime description.</span></span>
```
PS C:\> Set-AzureRmDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' `
                                            -Description 'New description'

    Id                : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
    ResourceGroupName : rg-test-dfv2
    DataFactoryName   : test-df-eu2
    Name              : test-selfhost-ir
    Description       : New description
```

<span data-ttu-id="529f9-112">Командлет обновляет описание среды выполнения интеграции с именем Test-SelfHost-IR.</span><span class="sxs-lookup"><span data-stu-id="529f9-112">The cmdlet updates the description of integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="529f9-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="529f9-113">PARAMETERS</span></span>

### <span data-ttu-id="529f9-114">-AuthKey</span><span class="sxs-lookup"><span data-stu-id="529f9-114">-AuthKey</span></span>
<span data-ttu-id="529f9-115">Ключ проверки подлинности на саморазмещенной среде выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="529f9-115">The authentication key of the self-hosted integration runtime.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="529f9-116">-CatalogAdminCredential</span><span class="sxs-lookup"><span data-stu-id="529f9-116">-CatalogAdminCredential</span></span>
<span data-ttu-id="529f9-117">Учетные данные администратора базы данных каталога среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="529f9-117">The catalog database administrator credential of the integration runtime.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="529f9-118">-CatalogPricingTier</span><span class="sxs-lookup"><span data-stu-id="529f9-118">-CatalogPricingTier</span></span>
<span data-ttu-id="529f9-119">Ценовая категория базы данных каталога в среде выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="529f9-119">The catalog database pricing tier of the integration runtime.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="529f9-120">-CatalogServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="529f9-120">-CatalogServerEndpoint</span></span>
<span data-ttu-id="529f9-121">Конечная точка сервера базы данных каталога среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="529f9-121">The catalog database server endpoint of the integration runtime.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="529f9-122">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="529f9-122">-DataFactoryName</span></span>
<span data-ttu-id="529f9-123">Имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="529f9-123">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="529f9-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="529f9-124">-DefaultProfile</span></span>
<span data-ttu-id="529f9-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="529f9-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="529f9-126">-Описание</span><span class="sxs-lookup"><span data-stu-id="529f9-126">-Description</span></span>
<span data-ttu-id="529f9-127">Описание среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="529f9-127">The integration runtime description.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="529f9-128">-Edition</span><span class="sxs-lookup"><span data-stu-id="529f9-128">-Edition</span></span>
<span data-ttu-id="529f9-129">Выпуски среды выполнения интеграции служб SSIS, которые могут быть стандартными или корпоративными, по умолчанию используется стандартный, если он не указан.</span><span class="sxs-lookup"><span data-stu-id="529f9-129">The edition for SSIS integration runtime which could be Standard or Enterprise, default is Standard if it is not specified.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Standard, Enterprise

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="529f9-130">-Force</span><span class="sxs-lookup"><span data-stu-id="529f9-130">-Force</span></span>
<span data-ttu-id="529f9-131">Запускает командлет без запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="529f9-131">Runs the cmdlet without prompting for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="529f9-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="529f9-132">-InputObject</span></span>
<span data-ttu-id="529f9-133">Объект среды выполнения Integration.</span><span class="sxs-lookup"><span data-stu-id="529f9-133">The integration runtime object.</span></span>

```yaml
Type: PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="529f9-134">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="529f9-134">-LicenseType</span></span>
<span data-ttu-id="529f9-135">Тип лицензии, которую вы хотите выбрать для ИК-связи служб SSIS.</span><span class="sxs-lookup"><span data-stu-id="529f9-135">The license type that you want to select for the SSIS IR.</span></span> <span data-ttu-id="529f9-136">Существует два типа: LicenseIncluded или BasePrice.</span><span class="sxs-lookup"><span data-stu-id="529f9-136">There are two types: LicenseIncluded or BasePrice.</span></span> <span data-ttu-id="529f9-137">Если вы ищете цены на использование гибридной льготы для использования Azure (AHUB), пожалуйста, выберите BasePrice.</span><span class="sxs-lookup"><span data-stu-id="529f9-137">If you are qualified for the Azure Hybrid Use Benefit (AHUB) pricing, please select BasePrice.</span></span> <span data-ttu-id="529f9-138">Если это не так, пожалуйста, выберите LicenseIncluded.</span><span class="sxs-lookup"><span data-stu-id="529f9-138">If not, please select LicenseIncluded.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: LicenseIncluded, BasePrice

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="529f9-139">-Location</span><span class="sxs-lookup"><span data-stu-id="529f9-139">-Location</span></span>
<span data-ttu-id="529f9-140">Расположение среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="529f9-140">The integration runtime location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="529f9-141">-MaxParallelExecutionsPerNode</span><span class="sxs-lookup"><span data-stu-id="529f9-141">-MaxParallelExecutionsPerNode</span></span>
<span data-ttu-id="529f9-142">Максимальное количество параллельных выполнений на каждом узле для управляемой среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="529f9-142">Maximum parallel execution count per node for a managed dedicated integration runtime.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="529f9-143">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="529f9-143">-Name</span></span>
<span data-ttu-id="529f9-144">Имя среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="529f9-144">The integration runtime name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="529f9-145">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="529f9-145">-NodeCount</span></span>
<span data-ttu-id="529f9-146">Количество целевых узлов в среде выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="529f9-146">Target nodes count of the integration runtime.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="529f9-147">-NodeSize</span><span class="sxs-lookup"><span data-stu-id="529f9-147">-NodeSize</span></span>
<span data-ttu-id="529f9-148">Размер узла среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="529f9-148">The integration runtime node size.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="529f9-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="529f9-149">-ResourceGroupName</span></span>
<span data-ttu-id="529f9-150">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="529f9-150">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="529f9-151">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="529f9-151">-ResourceId</span></span>
<span data-ttu-id="529f9-152">Идентификатор ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="529f9-152">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="529f9-153">-SetupScriptContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="529f9-153">-SetupScriptContainerSasUri</span></span>
<span data-ttu-id="529f9-154">Универсальный код ресурса (URI) SAS контейнера BLOB-объектов Azure, содержащего настраиваемый сценарий настройки.</span><span class="sxs-lookup"><span data-stu-id="529f9-154">The SAS URI of the Azure blob container that contains the custom setup script.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="529f9-155">-Подсеть</span><span class="sxs-lookup"><span data-stu-id="529f9-155">-Subnet</span></span>
<span data-ttu-id="529f9-156">Имя подсети в виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="529f9-156">The name of the subnet in the VNet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SubnetName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="529f9-157">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="529f9-157">-Type</span></span>
<span data-ttu-id="529f9-158">Тип среды выполнения Integration.</span><span class="sxs-lookup"><span data-stu-id="529f9-158">The integration runtime type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Managed, SelfHosted

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="529f9-159">-VNetId</span><span class="sxs-lookup"><span data-stu-id="529f9-159">-VNetId</span></span>
<span data-ttu-id="529f9-160">ИДЕНТИФИКАТОР виртуальной сети, к которой присоединяется среда выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="529f9-160">The ID of the VNet that the integration runtime joins.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="529f9-161">-Confirm</span><span class="sxs-lookup"><span data-stu-id="529f9-161">-Confirm</span></span>
<span data-ttu-id="529f9-162">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="529f9-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="529f9-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="529f9-163">-WhatIf</span></span>
<span data-ttu-id="529f9-164">Показано, что происходит при запуске командлета, но не запускает командлет.</span><span class="sxs-lookup"><span data-stu-id="529f9-164">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="529f9-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="529f9-165">CommonParameters</span></span>
<span data-ttu-id="529f9-166">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="529f9-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="529f9-167">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="529f9-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="529f9-168">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="529f9-168">INPUTS</span></span>

### <span data-ttu-id="529f9-169">System. String</span><span class="sxs-lookup"><span data-stu-id="529f9-169">System.String</span></span>
<span data-ttu-id="529f9-170">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="529f9-170">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="529f9-171">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="529f9-171">OUTPUTS</span></span>

### <span data-ttu-id="529f9-172">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="529f9-172">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="529f9-173">Пуск</span><span class="sxs-lookup"><span data-stu-id="529f9-173">NOTES</span></span>

## <span data-ttu-id="529f9-174">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="529f9-174">RELATED LINKS</span></span>

[<span data-ttu-id="529f9-175">Set-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="529f9-175">Set-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()

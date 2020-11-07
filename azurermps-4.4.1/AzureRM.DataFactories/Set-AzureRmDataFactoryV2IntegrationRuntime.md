---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: ce842abf58dabb0bdd518f02e7030f3fb2feabc1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734875"
---
# <span data-ttu-id="27ea4-101">Set-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="27ea4-101">Set-AzureRmDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="27ea4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="27ea4-102">SYNOPSIS</span></span>
<span data-ttu-id="27ea4-103">Обновляет среду выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="27ea4-103">Updates an integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="27ea4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="27ea4-104">SYNTAX</span></span>

### <span data-ttu-id="27ea4-105">ByIntegrationRuntimeName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="27ea4-105">ByIntegrationRuntimeName (Default)</span></span>
```
Set-AzureRmDataFactoryV2IntegrationRuntime [-Type <String>] [-Description <String>] [-Location <String>]
 [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="27ea4-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="27ea4-106">ByResourceId</span></span>
```
Set-AzureRmDataFactoryV2IntegrationRuntime [-Type <String>] [-Description <String>] [-Location <String>]
 [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27ea4-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="27ea4-107">ByIntegrationRuntimeObject</span></span>
```
Set-AzureRmDataFactoryV2IntegrationRuntime [-Type <String>] [-Description <String>] [-Location <String>]
 [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27ea4-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="27ea4-108">DESCRIPTION</span></span>
<span data-ttu-id="27ea4-109">Командлет Set-AzureRmDataFactoryV2IntegrationRuntime обновляет среду выполнения интеграции с определенными параметрами.</span><span class="sxs-lookup"><span data-stu-id="27ea4-109">The Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet updates an integration runtime with specific parameters.</span></span>

## <span data-ttu-id="27ea4-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="27ea4-110">EXAMPLES</span></span>

### <span data-ttu-id="27ea4-111">Пример 1: Описание обновления среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="27ea4-111">Example 1: Update integration runtime description.</span></span>
```
PS C:\> Set-AzureRmDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' `
                                            -Description 'New description'

    Id                : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
    ResourceGroupName : rg-test-dfv2
    DataFactoryName   : test-df-eu2
    Name              : test-selfhost-ir
    Description       : New description
```

<span data-ttu-id="27ea4-112">Командлет обновляет описание среды выполнения интеграции с именем Test-SelfHost-IR.</span><span class="sxs-lookup"><span data-stu-id="27ea4-112">The cmdlet updates the description of integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="27ea4-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="27ea4-113">PARAMETERS</span></span>

### <span data-ttu-id="27ea4-114">-CatalogAdminCredential</span><span class="sxs-lookup"><span data-stu-id="27ea4-114">-CatalogAdminCredential</span></span>
<span data-ttu-id="27ea4-115">Учетные данные администратора базы данных каталога среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="27ea4-115">The catalog database administrator credential of the integration runtime.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27ea4-116">-CatalogPricingTier</span><span class="sxs-lookup"><span data-stu-id="27ea4-116">-CatalogPricingTier</span></span>
<span data-ttu-id="27ea4-117">Ценовая категория базы данных каталога в среде выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="27ea4-117">The catalog database pricing tier of the integration runtime.</span></span>

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

### <span data-ttu-id="27ea4-118">-CatalogServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="27ea4-118">-CatalogServerEndpoint</span></span>
<span data-ttu-id="27ea4-119">Конечная точка сервера базы данных каталога среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="27ea4-119">The catalog database server endpoint of the integration runtime.</span></span>

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

### <span data-ttu-id="27ea4-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="27ea4-120">-Confirm</span></span>
<span data-ttu-id="27ea4-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="27ea4-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27ea4-122">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="27ea4-122">-DataFactoryName</span></span>
<span data-ttu-id="27ea4-123">Имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="27ea4-123">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27ea4-124">-Описание</span><span class="sxs-lookup"><span data-stu-id="27ea4-124">-Description</span></span>
<span data-ttu-id="27ea4-125">Описание среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="27ea4-125">The integration runtime description.</span></span>

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

### <span data-ttu-id="27ea4-126">-Force</span><span class="sxs-lookup"><span data-stu-id="27ea4-126">-Force</span></span>
<span data-ttu-id="27ea4-127">Запускает командлет без запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="27ea4-127">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="27ea4-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="27ea4-128">-InputObject</span></span>
<span data-ttu-id="27ea4-129">Объект среды выполнения Integration.</span><span class="sxs-lookup"><span data-stu-id="27ea4-129">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="27ea4-130">-Location</span><span class="sxs-lookup"><span data-stu-id="27ea4-130">-Location</span></span>
<span data-ttu-id="27ea4-131">Расположение среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="27ea4-131">The integration runtime location.</span></span>

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

### <span data-ttu-id="27ea4-132">-MaxParallelExecutionsPerNode</span><span class="sxs-lookup"><span data-stu-id="27ea4-132">-MaxParallelExecutionsPerNode</span></span>
<span data-ttu-id="27ea4-133">Максимальное количество параллельных выполнений на каждом узле для управляемой среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="27ea4-133">Maximum parallel execution count per node for a managed dedicated integration runtime.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27ea4-134">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="27ea4-134">-Name</span></span>
<span data-ttu-id="27ea4-135">Имя среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="27ea4-135">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27ea4-136">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="27ea4-136">-NodeCount</span></span>
<span data-ttu-id="27ea4-137">Количество целевых узлов в среде выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="27ea4-137">Target nodes count of the integration runtime.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27ea4-138">-NodeSize</span><span class="sxs-lookup"><span data-stu-id="27ea4-138">-NodeSize</span></span>
<span data-ttu-id="27ea4-139">Размер узла среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="27ea4-139">The integration runtime node size.</span></span>

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

### <span data-ttu-id="27ea4-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27ea4-140">-ResourceGroupName</span></span>
<span data-ttu-id="27ea4-141">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="27ea4-141">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27ea4-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="27ea4-142">-ResourceId</span></span>
<span data-ttu-id="27ea4-143">Идентификатор ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="27ea4-143">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27ea4-144">-Подсеть</span><span class="sxs-lookup"><span data-stu-id="27ea4-144">-Subnet</span></span>
<span data-ttu-id="27ea4-145">Имя подсети в виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="27ea4-145">The name of the subnet in the VNet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubnetName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27ea4-146">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="27ea4-146">-Type</span></span>
<span data-ttu-id="27ea4-147">Тип среды выполнения Integration.</span><span class="sxs-lookup"><span data-stu-id="27ea4-147">The integration runtime type.</span></span>

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

### <span data-ttu-id="27ea4-148">-VNetId</span><span class="sxs-lookup"><span data-stu-id="27ea4-148">-VNetId</span></span>
<span data-ttu-id="27ea4-149">ИДЕНТИФИКАТОР виртуальной сети, к которой присоединяется среда выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="27ea4-149">The ID of the VNet that the integration runtime joins.</span></span>

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

### <span data-ttu-id="27ea4-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27ea4-150">-WhatIf</span></span>
<span data-ttu-id="27ea4-151">Показано, что происходит при запуске командлета, но не запускает командлет.</span><span class="sxs-lookup"><span data-stu-id="27ea4-151">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="27ea4-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27ea4-152">-DefaultProfile</span></span>
<span data-ttu-id="27ea4-153">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="27ea4-153">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27ea4-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27ea4-154">CommonParameters</span></span>
<span data-ttu-id="27ea4-155">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="27ea4-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27ea4-156">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27ea4-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27ea4-157">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="27ea4-157">INPUTS</span></span>

### <span data-ttu-id="27ea4-158">System. String</span><span class="sxs-lookup"><span data-stu-id="27ea4-158">System.String</span></span>
<span data-ttu-id="27ea4-159">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="27ea4-159">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="27ea4-160">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="27ea4-160">OUTPUTS</span></span>

### <span data-ttu-id="27ea4-161">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="27ea4-161">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="27ea4-162">Пуск</span><span class="sxs-lookup"><span data-stu-id="27ea4-162">NOTES</span></span>

## <span data-ttu-id="27ea4-163">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="27ea4-163">RELATED LINKS</span></span>

[<span data-ttu-id="27ea4-164">Set-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="27ea4-164">Set-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()

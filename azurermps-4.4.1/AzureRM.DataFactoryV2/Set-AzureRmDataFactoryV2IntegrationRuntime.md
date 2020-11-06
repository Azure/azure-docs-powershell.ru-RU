---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2IntegrationRuntime.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: f24d42f1c4648343b979586ee906913f5d6a07f7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93570440"
---
# <span data-ttu-id="71a90-101">Set-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="71a90-101">Set-AzureRmDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="71a90-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="71a90-102">SYNOPSIS</span></span>
<span data-ttu-id="71a90-103">Обновляет среду выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="71a90-103">Updates an integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="71a90-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="71a90-104">SYNTAX</span></span>

### <span data-ttu-id="71a90-105">ByIntegrationRuntimeName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="71a90-105">ByIntegrationRuntimeName (Default)</span></span>
```
Set-AzureRmDataFactoryV2IntegrationRuntime [-Type <String>] [-Description <String>] [-Location <String>]
 [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="71a90-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="71a90-106">ByResourceId</span></span>
```
Set-AzureRmDataFactoryV2IntegrationRuntime [-Type <String>] [-Description <String>] [-Location <String>]
 [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-Force] [-ResourceId] <String> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="71a90-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="71a90-107">ByIntegrationRuntimeObject</span></span>
```
Set-AzureRmDataFactoryV2IntegrationRuntime [-Type <String>] [-Description <String>] [-Location <String>]
 [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-Force] [-InputObject] <PSIntegrationRuntime> [-WhatIf]
 [-Confirm]
```

## <span data-ttu-id="71a90-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="71a90-108">DESCRIPTION</span></span>
<span data-ttu-id="71a90-109">Командлет Set-AzureRmDataFactoryV2IntegrationRuntime обновляет среду выполнения интеграции с определенными параметрами.</span><span class="sxs-lookup"><span data-stu-id="71a90-109">The Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet updates an integration runtime with specific parameters.</span></span>

## <span data-ttu-id="71a90-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="71a90-110">EXAMPLES</span></span>

### <span data-ttu-id="71a90-111">Пример 1: Описание обновления среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="71a90-111">Example 1: Update integration runtime description.</span></span>
```
PS C:\> Set-AzureRmDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' `
                                            -Description 'New description'

    Id                : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
    ResourceGroupName : rg-test-dfv2
    DataFactoryName   : test-df-eu2
    Name              : test-selfhost-ir
    Description       : New description

```

<span data-ttu-id="71a90-112">Командлет обновляет описание среды выполнения интеграции с именем Test-SelfHost-IR.</span><span class="sxs-lookup"><span data-stu-id="71a90-112">The cmdlet updates the description of integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="71a90-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="71a90-113">PARAMETERS</span></span>

### <span data-ttu-id="71a90-114">-CatalogAdminCredential</span><span class="sxs-lookup"><span data-stu-id="71a90-114">-CatalogAdminCredential</span></span>
<span data-ttu-id="71a90-115">Учетные данные администратора базы данных каталога среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="71a90-115">The catalog database administrator credential of the integration runtime.</span></span>

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

### <span data-ttu-id="71a90-116">-CatalogPricingTier</span><span class="sxs-lookup"><span data-stu-id="71a90-116">-CatalogPricingTier</span></span>
<span data-ttu-id="71a90-117">Ценовая категория базы данных каталога в среде выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="71a90-117">The catalog database pricing tier of the integration runtime.</span></span>

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

### <span data-ttu-id="71a90-118">-CatalogServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="71a90-118">-CatalogServerEndpoint</span></span>
<span data-ttu-id="71a90-119">Конечная точка сервера базы данных каталога среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="71a90-119">The catalog database server endpoint of the integration runtime.</span></span>

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

### <span data-ttu-id="71a90-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="71a90-120">-Confirm</span></span>
<span data-ttu-id="71a90-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="71a90-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71a90-122">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="71a90-122">-DataFactoryName</span></span>
<span data-ttu-id="71a90-123">Имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="71a90-123">The data factory name.</span></span>

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

### <span data-ttu-id="71a90-124">-Описание</span><span class="sxs-lookup"><span data-stu-id="71a90-124">-Description</span></span>
<span data-ttu-id="71a90-125">Описание среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="71a90-125">The integration runtime description.</span></span>

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

### <span data-ttu-id="71a90-126">-Force</span><span class="sxs-lookup"><span data-stu-id="71a90-126">-Force</span></span>
<span data-ttu-id="71a90-127">Запускает командлет без запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="71a90-127">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="71a90-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="71a90-128">-InputObject</span></span>
<span data-ttu-id="71a90-129">Объект среды выполнения Integration.</span><span class="sxs-lookup"><span data-stu-id="71a90-129">The integration runtime object.</span></span>

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

### <span data-ttu-id="71a90-130">-Location</span><span class="sxs-lookup"><span data-stu-id="71a90-130">-Location</span></span>
<span data-ttu-id="71a90-131">Расположение среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="71a90-131">The integration runtime location.</span></span>

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

### <span data-ttu-id="71a90-132">-MaxParallelExecutionsPerNode</span><span class="sxs-lookup"><span data-stu-id="71a90-132">-MaxParallelExecutionsPerNode</span></span>
<span data-ttu-id="71a90-133">Максимальное количество параллельных выполнений на каждом узле для управляемой среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="71a90-133">Maximum parallel execution count per node for a managed dedicated integration runtime.</span></span>

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

### <span data-ttu-id="71a90-134">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="71a90-134">-Name</span></span>
<span data-ttu-id="71a90-135">Имя среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="71a90-135">The integration runtime name.</span></span>

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

### <span data-ttu-id="71a90-136">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="71a90-136">-NodeCount</span></span>
<span data-ttu-id="71a90-137">Количество целевых узлов в среде выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="71a90-137">Target nodes count of the integration runtime.</span></span>

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

### <span data-ttu-id="71a90-138">-NodeSize</span><span class="sxs-lookup"><span data-stu-id="71a90-138">-NodeSize</span></span>
<span data-ttu-id="71a90-139">Размер узла среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="71a90-139">The integration runtime node size.</span></span>

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

### <span data-ttu-id="71a90-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71a90-140">-ResourceGroupName</span></span>
<span data-ttu-id="71a90-141">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="71a90-141">The resource group name.</span></span>

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

### <span data-ttu-id="71a90-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="71a90-142">-ResourceId</span></span>
<span data-ttu-id="71a90-143">Идентификатор ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="71a90-143">The Azure resource ID.</span></span>

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

### <span data-ttu-id="71a90-144">-Подсеть</span><span class="sxs-lookup"><span data-stu-id="71a90-144">-Subnet</span></span>
<span data-ttu-id="71a90-145">Имя подсети в виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="71a90-145">The name of the subnet in the VNet.</span></span>

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

### <span data-ttu-id="71a90-146">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="71a90-146">-Type</span></span>
<span data-ttu-id="71a90-147">Тип среды выполнения Integration.</span><span class="sxs-lookup"><span data-stu-id="71a90-147">The integration runtime type.</span></span>

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

### <span data-ttu-id="71a90-148">-VNetId</span><span class="sxs-lookup"><span data-stu-id="71a90-148">-VNetId</span></span>
<span data-ttu-id="71a90-149">ИДЕНТИФИКАТОР виртуальной сети, к которой присоединяется среда выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="71a90-149">The ID of the VNet that the integration runtime joins.</span></span>

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

### <span data-ttu-id="71a90-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71a90-150">-WhatIf</span></span>
<span data-ttu-id="71a90-151">Показано, что происходит при запуске командлета, но не запускает командлет.</span><span class="sxs-lookup"><span data-stu-id="71a90-151">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

## <span data-ttu-id="71a90-152">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="71a90-152">INPUTS</span></span>

### <span data-ttu-id="71a90-153">System. String</span><span class="sxs-lookup"><span data-stu-id="71a90-153">System.String</span></span>
<span data-ttu-id="71a90-154">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="71a90-154">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="71a90-155">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="71a90-155">OUTPUTS</span></span>

### <span data-ttu-id="71a90-156">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="71a90-156">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="71a90-157">Пуск</span><span class="sxs-lookup"><span data-stu-id="71a90-157">NOTES</span></span>

## <span data-ttu-id="71a90-158">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="71a90-158">RELATED LINKS</span></span>
[<span data-ttu-id="71a90-159">Set-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="71a90-159">Set-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()

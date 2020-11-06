---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2IntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2IntegrationRuntimeNode.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: e5bf7ca6951a78fc631b5bc2ffa96a2042423d9f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568077"
---
# <span data-ttu-id="3aa7b-101">Remove-AzureRmDataFactoryV2IntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="3aa7b-101">Remove-AzureRmDataFactoryV2IntegrationRuntimeNode</span></span>

## <span data-ttu-id="3aa7b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3aa7b-102">SYNOPSIS</span></span>
<span data-ttu-id="3aa7b-103">Удаление узла с заданным именем в среде выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="3aa7b-103">Remove a node with the given name on an integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3aa7b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3aa7b-104">SYNTAX</span></span>

### <span data-ttu-id="3aa7b-105">ByIntegrationRuntimeName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3aa7b-105">ByIntegrationRuntimeName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntimeNode -NodeName <String> [-Force]
 [-IntegrationRuntimeName] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String> [-WhatIf]
 [-Confirm]
```

### <span data-ttu-id="3aa7b-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="3aa7b-106">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntimeNode -NodeName <String> [-Force] [-ResourceId] <String> [-WhatIf]
 [-Confirm]
```

### <span data-ttu-id="3aa7b-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="3aa7b-107">ByIntegrationRuntimeObject</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntimeNode -NodeName <String> [-Force]
 [-InputObject] <PSIntegrationRuntime> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="3aa7b-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3aa7b-108">DESCRIPTION</span></span>
<span data-ttu-id="3aa7b-109">Командлет Remove-AzureRmDataFactoryV2IntegrationRuntimeNode удаляет узел в среде выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="3aa7b-109">The Remove-AzureRmDataFactoryV2IntegrationRuntimeNode cmdlet removes a node in an integration runtime.</span></span>

## <span data-ttu-id="3aa7b-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3aa7b-110">EXAMPLES</span></span>

### <span data-ttu-id="3aa7b-111">Пример 1: Удаление узла из среды выполнения интеграции</span><span class="sxs-lookup"><span data-stu-id="3aa7b-111">Example 1: Remove a node from an integration runtime</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2IntegrationRuntimeNode -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' -NodeName 'Node_1'
```

<span data-ttu-id="3aa7b-112">Эта команда удаляет узел с именем "Node_1" в среде выполнения интеграции с именем "Test-SelfHost-IR" в подписке для группы ресурсов с именем "Test-DF-Eu2".</span><span class="sxs-lookup"><span data-stu-id="3aa7b-112">This command removes an node named 'Node_1' in the integration runtime named 'test-selfhost-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

## <span data-ttu-id="3aa7b-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3aa7b-113">PARAMETERS</span></span>

### <span data-ttu-id="3aa7b-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3aa7b-114">-Confirm</span></span>
<span data-ttu-id="3aa7b-115">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3aa7b-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3aa7b-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="3aa7b-116">-DataFactoryName</span></span>
<span data-ttu-id="3aa7b-117">Имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="3aa7b-117">The data factory name.</span></span>

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

### <span data-ttu-id="3aa7b-118">-Force</span><span class="sxs-lookup"><span data-stu-id="3aa7b-118">-Force</span></span>
<span data-ttu-id="3aa7b-119">Запускает командлет без запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="3aa7b-119">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="3aa7b-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3aa7b-120">-InputObject</span></span>
<span data-ttu-id="3aa7b-121">Объект среды выполнения Integration.</span><span class="sxs-lookup"><span data-stu-id="3aa7b-121">The integration runtime object.</span></span>

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

### <span data-ttu-id="3aa7b-122">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="3aa7b-122">-IntegrationRuntimeName</span></span>
<span data-ttu-id="3aa7b-123">Имя среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="3aa7b-123">The integration runtime name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3aa7b-124">-NodeName</span><span class="sxs-lookup"><span data-stu-id="3aa7b-124">-NodeName</span></span>
<span data-ttu-id="3aa7b-125">Имя узла среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="3aa7b-125">The integration runtime node name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3aa7b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3aa7b-126">-ResourceGroupName</span></span>
<span data-ttu-id="3aa7b-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3aa7b-127">The resource group name.</span></span>

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

### <span data-ttu-id="3aa7b-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3aa7b-128">-ResourceId</span></span>
<span data-ttu-id="3aa7b-129">Идентификатор ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="3aa7b-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="3aa7b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3aa7b-130">-WhatIf</span></span>
<span data-ttu-id="3aa7b-131">Показано, что происходит при запуске командлета, но не запускает командлет.</span><span class="sxs-lookup"><span data-stu-id="3aa7b-131">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

## <span data-ttu-id="3aa7b-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3aa7b-132">INPUTS</span></span>

### <span data-ttu-id="3aa7b-133">System. String</span><span class="sxs-lookup"><span data-stu-id="3aa7b-133">System.String</span></span>
<span data-ttu-id="3aa7b-134">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="3aa7b-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>


## <span data-ttu-id="3aa7b-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3aa7b-135">OUTPUTS</span></span>

### <span data-ttu-id="3aa7b-136">System. Object</span><span class="sxs-lookup"><span data-stu-id="3aa7b-136">System.Object</span></span>

## <span data-ttu-id="3aa7b-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="3aa7b-137">NOTES</span></span>

## <span data-ttu-id="3aa7b-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3aa7b-138">RELATED LINKS</span></span>


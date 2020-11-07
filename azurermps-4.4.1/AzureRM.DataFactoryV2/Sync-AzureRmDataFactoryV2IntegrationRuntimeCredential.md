---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 63889ce74af1051211a579d1af7cc54be14822f5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732225"
---
# <span data-ttu-id="7556f-101">Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential</span><span class="sxs-lookup"><span data-stu-id="7556f-101">Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential</span></span>

## <span data-ttu-id="7556f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7556f-102">SYNOPSIS</span></span>
<span data-ttu-id="7556f-103">Синхронизирует учетные данные между узлами среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="7556f-103">Synchronizes credentials among integration runtime nodes.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7556f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7556f-104">SYNTAX</span></span>

### <span data-ttu-id="7556f-105">ByIntegrationRuntimeName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7556f-105">ByIntegrationRuntimeName (Default)</span></span>
```
Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential [-Force] [-IntegrationRuntimeName] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="7556f-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="7556f-106">ByResourceId</span></span>
```
Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential [-Force] [-ResourceId] <String> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="7556f-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="7556f-107">ByIntegrationRuntimeObject</span></span>
```
Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential [-Force] [-InputObject] <PSIntegrationRuntime>
 [-WhatIf] [-Confirm]
```

## <span data-ttu-id="7556f-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7556f-108">DESCRIPTION</span></span>
<span data-ttu-id="7556f-109">Командлет **Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential** синхронизирует локальные учетные данные между узлами среды выполнения интеграции, что приводит к идентичности учетных данных на всех узлах.</span><span class="sxs-lookup"><span data-stu-id="7556f-109">The **Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential** cmdlet synchronizes on-premises credentials among integration runtime nodes, which forces the credentials to be identical in all nodes.</span></span>

## <span data-ttu-id="7556f-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7556f-110">EXAMPLES</span></span>

### <span data-ttu-id="7556f-111">Пример 1: Синхронизация учетных данных среды выполнения интеграции</span><span class="sxs-lookup"><span data-stu-id="7556f-111">Example 1: Sync an integration runtime credential</span></span>
```
PS C:\> Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'
```

<span data-ttu-id="7556f-112">Командлет синхронизирует учетные данные между узлами среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="7556f-112">The cmdlet synchronizes credentials among integration runtime nodes.</span></span>

## <span data-ttu-id="7556f-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7556f-113">PARAMETERS</span></span>

### <span data-ttu-id="7556f-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7556f-114">-Confirm</span></span>
<span data-ttu-id="7556f-115">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7556f-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7556f-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="7556f-116">-DataFactoryName</span></span>
<span data-ttu-id="7556f-117">Имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="7556f-117">The data factory name.</span></span>

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

### <span data-ttu-id="7556f-118">-Force</span><span class="sxs-lookup"><span data-stu-id="7556f-118">-Force</span></span>
<span data-ttu-id="7556f-119">Запускает командлет без запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="7556f-119">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="7556f-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7556f-120">-InputObject</span></span>
<span data-ttu-id="7556f-121">Объект среды выполнения Integration.</span><span class="sxs-lookup"><span data-stu-id="7556f-121">The integration runtime object.</span></span>

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

### <span data-ttu-id="7556f-122">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="7556f-122">-IntegrationRuntimeName</span></span>
<span data-ttu-id="7556f-123">Имя среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="7556f-123">The integration runtime name.</span></span>

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

### <span data-ttu-id="7556f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7556f-124">-ResourceGroupName</span></span>
<span data-ttu-id="7556f-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7556f-125">The resource group name.</span></span>

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

### <span data-ttu-id="7556f-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7556f-126">-ResourceId</span></span>
<span data-ttu-id="7556f-127">Идентификатор ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="7556f-127">The Azure resource ID.</span></span>

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

### <span data-ttu-id="7556f-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7556f-128">-WhatIf</span></span>
<span data-ttu-id="7556f-129">Показано, что происходит при запуске командлета, но не запускает командлет.</span><span class="sxs-lookup"><span data-stu-id="7556f-129">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

## <span data-ttu-id="7556f-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7556f-130">INPUTS</span></span>

### <span data-ttu-id="7556f-131">System. String</span><span class="sxs-lookup"><span data-stu-id="7556f-131">System.String</span></span>
<span data-ttu-id="7556f-132">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="7556f-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>


## <span data-ttu-id="7556f-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7556f-133">OUTPUTS</span></span>

### <span data-ttu-id="7556f-134">System. Object</span><span class="sxs-lookup"><span data-stu-id="7556f-134">System.Object</span></span>

## <span data-ttu-id="7556f-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="7556f-135">NOTES</span></span>

## <span data-ttu-id="7556f-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7556f-136">RELATED LINKS</span></span>

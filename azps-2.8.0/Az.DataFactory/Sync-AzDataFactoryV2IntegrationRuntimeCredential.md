---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/sync-azdatafactoryv2integrationruntimecredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Sync-AzDataFactoryV2IntegrationRuntimeCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Sync-AzDataFactoryV2IntegrationRuntimeCredential.md
ms.openlocfilehash: 40f6a6c5f446b23a92a2ca5c5c8c872297b2a81a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721414"
---
# <span data-ttu-id="6fb49-101">Sync-AzDataFactoryV2IntegrationRuntimeCredential</span><span class="sxs-lookup"><span data-stu-id="6fb49-101">Sync-AzDataFactoryV2IntegrationRuntimeCredential</span></span>

## <span data-ttu-id="6fb49-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6fb49-102">SYNOPSIS</span></span>
<span data-ttu-id="6fb49-103">Синхронизирует учетные данные между узлами среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="6fb49-103">Synchronizes credentials among integration runtime nodes.</span></span>

## <span data-ttu-id="6fb49-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6fb49-104">SYNTAX</span></span>

### <span data-ttu-id="6fb49-105">ByIntegrationRuntimeName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6fb49-105">ByIntegrationRuntimeName (Default)</span></span>
```
Sync-AzDataFactoryV2IntegrationRuntimeCredential [-Force] [-IntegrationRuntimeName] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6fb49-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="6fb49-106">ByResourceId</span></span>
```
Sync-AzDataFactoryV2IntegrationRuntimeCredential [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6fb49-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="6fb49-107">ByIntegrationRuntimeObject</span></span>
```
Sync-AzDataFactoryV2IntegrationRuntimeCredential [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6fb49-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6fb49-108">DESCRIPTION</span></span>
<span data-ttu-id="6fb49-109">Командлет **Sync-AzDataFactoryV2IntegrationRuntimeCredential** синхронизирует локальные учетные данные между узлами среды выполнения интеграции, что приводит к идентичности учетных данных на всех узлах.</span><span class="sxs-lookup"><span data-stu-id="6fb49-109">The **Sync-AzDataFactoryV2IntegrationRuntimeCredential** cmdlet synchronizes on-premises credentials among integration runtime nodes, which forces the credentials to be identical in all nodes.</span></span>

## <span data-ttu-id="6fb49-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6fb49-110">EXAMPLES</span></span>

### <span data-ttu-id="6fb49-111">Пример 1: Синхронизация учетных данных среды выполнения интеграции</span><span class="sxs-lookup"><span data-stu-id="6fb49-111">Example 1: Sync an integration runtime credential</span></span>
```
PS C:\> Sync-AzDataFactoryV2IntegrationRuntimeCredential -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'
```

<span data-ttu-id="6fb49-112">Командлет синхронизирует учетные данные между узлами среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="6fb49-112">The cmdlet synchronizes credentials among integration runtime nodes.</span></span>

## <span data-ttu-id="6fb49-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6fb49-113">PARAMETERS</span></span>

### <span data-ttu-id="6fb49-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="6fb49-114">-DataFactoryName</span></span>
<span data-ttu-id="6fb49-115">Имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="6fb49-115">The data factory name.</span></span>

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

### <span data-ttu-id="6fb49-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fb49-116">-DefaultProfile</span></span>
<span data-ttu-id="6fb49-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6fb49-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6fb49-118">-Force</span><span class="sxs-lookup"><span data-stu-id="6fb49-118">-Force</span></span>
<span data-ttu-id="6fb49-119">Запускает командлет без запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="6fb49-119">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="6fb49-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6fb49-120">-InputObject</span></span>
<span data-ttu-id="6fb49-121">Объект среды выполнения Integration.</span><span class="sxs-lookup"><span data-stu-id="6fb49-121">The integration runtime object.</span></span>

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

### <span data-ttu-id="6fb49-122">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="6fb49-122">-IntegrationRuntimeName</span></span>
<span data-ttu-id="6fb49-123">Имя среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="6fb49-123">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fb49-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6fb49-124">-ResourceGroupName</span></span>
<span data-ttu-id="6fb49-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6fb49-125">The resource group name.</span></span>

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

### <span data-ttu-id="6fb49-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6fb49-126">-ResourceId</span></span>
<span data-ttu-id="6fb49-127">Идентификатор ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="6fb49-127">The Azure resource ID.</span></span>

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

### <span data-ttu-id="6fb49-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6fb49-128">-Confirm</span></span>
<span data-ttu-id="6fb49-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6fb49-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6fb49-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6fb49-130">-WhatIf</span></span>
<span data-ttu-id="6fb49-131">Показано, что происходит при запуске командлета, но не запускает командлет.</span><span class="sxs-lookup"><span data-stu-id="6fb49-131">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="6fb49-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fb49-132">CommonParameters</span></span>
<span data-ttu-id="6fb49-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6fb49-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fb49-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6fb49-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fb49-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6fb49-135">INPUTS</span></span>

### <span data-ttu-id="6fb49-136">System. String</span><span class="sxs-lookup"><span data-stu-id="6fb49-136">System.String</span></span>

### <span data-ttu-id="6fb49-137">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="6fb49-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="6fb49-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6fb49-138">OUTPUTS</span></span>

### <span data-ttu-id="6fb49-139">System. void</span><span class="sxs-lookup"><span data-stu-id="6fb49-139">System.Void</span></span>

## <span data-ttu-id="6fb49-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="6fb49-140">NOTES</span></span>

## <span data-ttu-id="6fb49-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6fb49-141">RELATED LINKS</span></span>

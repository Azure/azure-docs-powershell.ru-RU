---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/sync-azdatafactoryv2integrationruntimecredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Sync-AzDataFactoryV2IntegrationRuntimeCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Sync-AzDataFactoryV2IntegrationRuntimeCredential.md
ms.openlocfilehash: cb9362a64b58770beb7d3b70f989fc740a2fc00e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912767"
---
# <span data-ttu-id="7a186-101">Sync-AzDataFactoryV2IntegrationRuntimeCredential</span><span class="sxs-lookup"><span data-stu-id="7a186-101">Sync-AzDataFactoryV2IntegrationRuntimeCredential</span></span>

## <span data-ttu-id="7a186-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7a186-102">SYNOPSIS</span></span>
<span data-ttu-id="7a186-103">Синхронизирует учетные данные между узлами среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="7a186-103">Synchronizes credentials among integration runtime nodes.</span></span>

## <span data-ttu-id="7a186-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7a186-104">SYNTAX</span></span>

### <span data-ttu-id="7a186-105">ByIntegrationRuntimeName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7a186-105">ByIntegrationRuntimeName (Default)</span></span>
```
Sync-AzDataFactoryV2IntegrationRuntimeCredential [-Force] [-IntegrationRuntimeName] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a186-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="7a186-106">ByResourceId</span></span>
```
Sync-AzDataFactoryV2IntegrationRuntimeCredential [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a186-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="7a186-107">ByIntegrationRuntimeObject</span></span>
```
Sync-AzDataFactoryV2IntegrationRuntimeCredential [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a186-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7a186-108">DESCRIPTION</span></span>
<span data-ttu-id="7a186-109">Командлет **Sync-AzDataFactoryV2IntegrationRuntimeCredential** синхронизирует локальные учетные данные между узлами среды выполнения интеграции, что приводит к идентичности учетных данных на всех узлах.</span><span class="sxs-lookup"><span data-stu-id="7a186-109">The **Sync-AzDataFactoryV2IntegrationRuntimeCredential** cmdlet synchronizes on-premises credentials among integration runtime nodes, which forces the credentials to be identical in all nodes.</span></span>

## <span data-ttu-id="7a186-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7a186-110">EXAMPLES</span></span>

### <span data-ttu-id="7a186-111">Пример 1: Синхронизация учетных данных среды выполнения интеграции</span><span class="sxs-lookup"><span data-stu-id="7a186-111">Example 1: Sync an integration runtime credential</span></span>
```
PS C:\> Sync-AzDataFactoryV2IntegrationRuntimeCredential -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'
```

<span data-ttu-id="7a186-112">Командлет синхронизирует учетные данные между узлами среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="7a186-112">The cmdlet synchronizes credentials among integration runtime nodes.</span></span>

## <span data-ttu-id="7a186-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7a186-113">PARAMETERS</span></span>

### <span data-ttu-id="7a186-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="7a186-114">-DataFactoryName</span></span>
<span data-ttu-id="7a186-115">Имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="7a186-115">The data factory name.</span></span>

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

### <span data-ttu-id="7a186-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a186-116">-DefaultProfile</span></span>
<span data-ttu-id="7a186-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7a186-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7a186-118">-Force</span><span class="sxs-lookup"><span data-stu-id="7a186-118">-Force</span></span>
<span data-ttu-id="7a186-119">Запускает командлет без запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="7a186-119">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="7a186-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7a186-120">-InputObject</span></span>
<span data-ttu-id="7a186-121">Объект среды выполнения Integration.</span><span class="sxs-lookup"><span data-stu-id="7a186-121">The integration runtime object.</span></span>

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

### <span data-ttu-id="7a186-122">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="7a186-122">-IntegrationRuntimeName</span></span>
<span data-ttu-id="7a186-123">Имя среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="7a186-123">The integration runtime name.</span></span>

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

### <span data-ttu-id="7a186-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a186-124">-ResourceGroupName</span></span>
<span data-ttu-id="7a186-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7a186-125">The resource group name.</span></span>

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

### <span data-ttu-id="7a186-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7a186-126">-ResourceId</span></span>
<span data-ttu-id="7a186-127">Идентификатор ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="7a186-127">The Azure resource ID.</span></span>

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

### <span data-ttu-id="7a186-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7a186-128">-Confirm</span></span>
<span data-ttu-id="7a186-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7a186-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a186-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a186-130">-WhatIf</span></span>
<span data-ttu-id="7a186-131">Показано, что происходит при запуске командлета, но не запускает командлет.</span><span class="sxs-lookup"><span data-stu-id="7a186-131">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="7a186-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a186-132">CommonParameters</span></span>
<span data-ttu-id="7a186-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7a186-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a186-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a186-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a186-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7a186-135">INPUTS</span></span>

### <span data-ttu-id="7a186-136">System. String</span><span class="sxs-lookup"><span data-stu-id="7a186-136">System.String</span></span>

### <span data-ttu-id="7a186-137">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="7a186-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="7a186-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7a186-138">OUTPUTS</span></span>

### <span data-ttu-id="7a186-139">System. void</span><span class="sxs-lookup"><span data-stu-id="7a186-139">System.Void</span></span>

## <span data-ttu-id="7a186-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="7a186-140">NOTES</span></span>

## <span data-ttu-id="7a186-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7a186-141">RELATED LINKS</span></span>

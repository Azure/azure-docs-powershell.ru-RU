---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/sync-azurermdatafactoryv2integrationruntimecredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential.md
ms.openlocfilehash: 05b9c5bce3158413f562c38eb116523609696523
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564588"
---
# <span data-ttu-id="353eb-101">Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential</span><span class="sxs-lookup"><span data-stu-id="353eb-101">Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential</span></span>

## <span data-ttu-id="353eb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="353eb-102">SYNOPSIS</span></span>
<span data-ttu-id="353eb-103">Синхронизирует учетные данные между узлами среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="353eb-103">Synchronizes credentials among integration runtime nodes.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="353eb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="353eb-104">SYNTAX</span></span>

### <span data-ttu-id="353eb-105">ByIntegrationRuntimeName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="353eb-105">ByIntegrationRuntimeName (Default)</span></span>
```
Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential [-Force] [-IntegrationRuntimeName] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="353eb-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="353eb-106">ByResourceId</span></span>
```
Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="353eb-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="353eb-107">ByIntegrationRuntimeObject</span></span>
```
Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="353eb-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="353eb-108">DESCRIPTION</span></span>
<span data-ttu-id="353eb-109">Командлет **Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential** синхронизирует локальные учетные данные между узлами среды выполнения интеграции, что приводит к идентичности учетных данных на всех узлах.</span><span class="sxs-lookup"><span data-stu-id="353eb-109">The **Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential** cmdlet synchronizes on-premises credentials among integration runtime nodes, which forces the credentials to be identical in all nodes.</span></span>

## <span data-ttu-id="353eb-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="353eb-110">EXAMPLES</span></span>

### <span data-ttu-id="353eb-111">Пример 1: Синхронизация учетных данных среды выполнения интеграции</span><span class="sxs-lookup"><span data-stu-id="353eb-111">Example 1: Sync an integration runtime credential</span></span>
```
PS C:\> Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'
```

<span data-ttu-id="353eb-112">Командлет синхронизирует учетные данные между узлами среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="353eb-112">The cmdlet synchronizes credentials among integration runtime nodes.</span></span>

## <span data-ttu-id="353eb-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="353eb-113">PARAMETERS</span></span>

### <span data-ttu-id="353eb-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="353eb-114">-DataFactoryName</span></span>
<span data-ttu-id="353eb-115">Имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="353eb-115">The data factory name.</span></span>

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

### <span data-ttu-id="353eb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="353eb-116">-DefaultProfile</span></span>
<span data-ttu-id="353eb-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="353eb-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="353eb-118">-Force</span><span class="sxs-lookup"><span data-stu-id="353eb-118">-Force</span></span>
<span data-ttu-id="353eb-119">Запускает командлет без запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="353eb-119">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="353eb-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="353eb-120">-InputObject</span></span>
<span data-ttu-id="353eb-121">Объект среды выполнения Integration.</span><span class="sxs-lookup"><span data-stu-id="353eb-121">The integration runtime object.</span></span>

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

### <span data-ttu-id="353eb-122">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="353eb-122">-IntegrationRuntimeName</span></span>
<span data-ttu-id="353eb-123">Имя среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="353eb-123">The integration runtime name.</span></span>

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

### <span data-ttu-id="353eb-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="353eb-124">-ResourceGroupName</span></span>
<span data-ttu-id="353eb-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="353eb-125">The resource group name.</span></span>

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

### <span data-ttu-id="353eb-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="353eb-126">-ResourceId</span></span>
<span data-ttu-id="353eb-127">Идентификатор ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="353eb-127">The Azure resource ID.</span></span>

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

### <span data-ttu-id="353eb-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="353eb-128">-Confirm</span></span>
<span data-ttu-id="353eb-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="353eb-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="353eb-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="353eb-130">-WhatIf</span></span>
<span data-ttu-id="353eb-131">Показано, что происходит при запуске командлета, но не запускает командлет.</span><span class="sxs-lookup"><span data-stu-id="353eb-131">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="353eb-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="353eb-132">CommonParameters</span></span>
<span data-ttu-id="353eb-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="353eb-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="353eb-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="353eb-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="353eb-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="353eb-135">INPUTS</span></span>

### <span data-ttu-id="353eb-136">System. String</span><span class="sxs-lookup"><span data-stu-id="353eb-136">System.String</span></span>

### <span data-ttu-id="353eb-137">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="353eb-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>
<span data-ttu-id="353eb-138">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="353eb-138">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="353eb-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="353eb-139">OUTPUTS</span></span>

### <span data-ttu-id="353eb-140">System. void</span><span class="sxs-lookup"><span data-stu-id="353eb-140">System.Void</span></span>

## <span data-ttu-id="353eb-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="353eb-141">NOTES</span></span>

## <span data-ttu-id="353eb-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="353eb-142">RELATED LINKS</span></span>

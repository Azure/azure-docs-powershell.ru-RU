---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseintegrationruntimekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeKey.md
ms.openlocfilehash: 08ce91d6d9a942dd20078e0c3b5b537360aac9fc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245996"
---
# <span data-ttu-id="1c4b7-101">Get-AzSynapseIntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="1c4b7-101">Get-AzSynapseIntegrationRuntimeKey</span></span>

## <span data-ttu-id="1c4b7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1c4b7-102">SYNOPSIS</span></span>
<span data-ttu-id="1c4b7-103">Возвращает клавиши для среды выполнения интеграции с самостоятельным размещением.</span><span class="sxs-lookup"><span data-stu-id="1c4b7-103">Gets keys for a self-hosted integration runtime.</span></span>

## <span data-ttu-id="1c4b7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1c4b7-104">SYNTAX</span></span>

### <span data-ttu-id="1c4b7-105">GetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1c4b7-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseIntegrationRuntimeKey [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1c4b7-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1c4b7-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeKey -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1c4b7-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1c4b7-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeKey -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1c4b7-108">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1c4b7-108">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeKey -InputObject <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1c4b7-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1c4b7-109">DESCRIPTION</span></span>
<span data-ttu-id="1c4b7-110">Командлет **Get-AzSynapseIntegrationRuntimeKey** получает ключи для среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="1c4b7-110">The **Get-AzSynapseIntegrationRuntimeKey** cmdlet gets keys for an integration runtime.</span></span> <span data-ttu-id="1c4b7-111">Ключи используются для регистрации узла среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="1c4b7-111">The keys are used to register an integration runtime node.</span></span>

## <span data-ttu-id="1c4b7-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1c4b7-112">EXAMPLES</span></span>

### <span data-ttu-id="1c4b7-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1c4b7-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntimeKey -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir'
```

<span data-ttu-id="1c4b7-114">Командлет извлекает ключи для среды выполнения интеграции с именем Test-SelfHost-IR.</span><span class="sxs-lookup"><span data-stu-id="1c4b7-114">The cmdlet retrieves keys for an integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="1c4b7-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1c4b7-115">PARAMETERS</span></span>

### <span data-ttu-id="1c4b7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c4b7-116">-DefaultProfile</span></span>
<span data-ttu-id="1c4b7-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1c4b7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c4b7-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1c4b7-118">-InputObject</span></span>
<span data-ttu-id="1c4b7-119">Объект среды выполнения Integration.</span><span class="sxs-lookup"><span data-stu-id="1c4b7-119">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime
Parameter Sets: GetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1c4b7-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1c4b7-120">-Name</span></span>
<span data-ttu-id="1c4b7-121">Имя среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="1c4b7-121">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases: IntegrationRuntimeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c4b7-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c4b7-122">-ResourceGroupName</span></span>
<span data-ttu-id="1c4b7-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1c4b7-123">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c4b7-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1c4b7-124">-ResourceId</span></span>
<span data-ttu-id="1c4b7-125">Идентификатор ресурса среды выполнения интеграции Synapse.</span><span class="sxs-lookup"><span data-stu-id="1c4b7-125">Resource identifier of Synapse integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c4b7-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="1c4b7-126">-WorkspaceName</span></span>
<span data-ttu-id="1c4b7-127">Имя Synapse рабочей области.</span><span class="sxs-lookup"><span data-stu-id="1c4b7-127">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c4b7-128">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="1c4b7-128">-WorkspaceObject</span></span>
<span data-ttu-id="1c4b7-129">объект ввода в рабочую область, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="1c4b7-129">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1c4b7-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c4b7-130">CommonParameters</span></span>
<span data-ttu-id="1c4b7-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1c4b7-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c4b7-132">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1c4b7-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c4b7-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1c4b7-133">INPUTS</span></span>

### <span data-ttu-id="1c4b7-134">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="1c4b7-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="1c4b7-135">Microsoft. Azure. Commands. Synapse. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="1c4b7-135">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="1c4b7-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1c4b7-136">OUTPUTS</span></span>

### <span data-ttu-id="1c4b7-137">Microsoft. Azure. Commands. Synapse. Models. PSIntegrationRuntimeKeys</span><span class="sxs-lookup"><span data-stu-id="1c4b7-137">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntimeKeys</span></span>

## <span data-ttu-id="1c4b7-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="1c4b7-138">NOTES</span></span>

## <span data-ttu-id="1c4b7-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1c4b7-139">RELATED LINKS</span></span>

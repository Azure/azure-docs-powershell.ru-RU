---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsetriggerrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTriggerRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTriggerRun.md
ms.openlocfilehash: 0d6d3bb99062177e1d75c4ab496562782cf142c1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235192"
---
# <span data-ttu-id="b48b2-101">Get-AzSynapseTriggerRun</span><span class="sxs-lookup"><span data-stu-id="b48b2-101">Get-AzSynapseTriggerRun</span></span>

## <span data-ttu-id="b48b2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b48b2-102">SYNOPSIS</span></span>
<span data-ttu-id="b48b2-103">Возвращает сведения о запусках триггеров.</span><span class="sxs-lookup"><span data-stu-id="b48b2-103">Returns information about trigger runs.</span></span>

## <span data-ttu-id="b48b2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b48b2-104">SYNTAX</span></span>

### <span data-ttu-id="b48b2-105">GetByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b48b2-105">GetByName (Default)</span></span>
```
Get-AzSynapseTriggerRun -WorkspaceName <String> -Name <String> -RunStartedAfter <DateTimeOffset>
 -RunStartedBefore <DateTimeOffset> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b48b2-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="b48b2-106">GetByObject</span></span>
```
Get-AzSynapseTriggerRun -WorkspaceObject <PSSynapseWorkspace> -Name <String> -RunStartedAfter <DateTimeOffset>
 -RunStartedBefore <DateTimeOffset> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b48b2-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b48b2-107">DESCRIPTION</span></span>
<span data-ttu-id="b48b2-108">Команда **Get-AzSynapseTriggerRun** возвращает подробные сведения о выполнении триггеров для определенного триггера в течение заданного периода.</span><span class="sxs-lookup"><span data-stu-id="b48b2-108">The **Get-AzSynapseTriggerRun** command returns detailed information about trigger runs for the specified trigger in the given timeframe.</span></span>

## <span data-ttu-id="b48b2-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b48b2-109">EXAMPLES</span></span>

### <span data-ttu-id="b48b2-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b48b2-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseTriggerRun -WorkspaceName ContosoWorkspace -Name ContosoTrigger -RunStartedAfter [DateTimeOffset]"2018-09-01T21:00" -RunStartedBefore [DateTimeOffset]"2019-09-01T21:00"
```

<span data-ttu-id="b48b2-111">Эта команда отображает сведения о запусках для ContosoTrigger в рабочей области ContosoWorkspace, которая была запущена между "2018-09-01T21:00" и "2019-09-01T21:00".</span><span class="sxs-lookup"><span data-stu-id="b48b2-111">This command shows information about runs for ContosoTrigger in the workspace ContosoWorkspace that started between "2018-09-01T21:00" and "2019-09-01T21:00".</span></span>

### <span data-ttu-id="b48b2-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="b48b2-112">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseTriggerRun -Name ContosoTrigger -RunStartedAfter [DateTimeOffset]"2018-09-01T21:00" -RunStartedBefore [DateTimeOffset]"2019-09-01T21:00"
```

<span data-ttu-id="b48b2-113">Эта команда показывает сведения о запусках для ContosoTrigger в рабочей области ContosoWorkspace, которая начинается с "2018-09-01T21:00" и "2019-09-01T21:00" через конвейер.</span><span class="sxs-lookup"><span data-stu-id="b48b2-113">This command shows information about runs for ContosoTrigger in the workspace ContosoWorkspace that started between "2018-09-01T21:00" and "2019-09-01T21:00" through pipeline.</span></span>

## <span data-ttu-id="b48b2-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b48b2-114">PARAMETERS</span></span>

### <span data-ttu-id="b48b2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b48b2-115">-DefaultProfile</span></span>
<span data-ttu-id="b48b2-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b48b2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b48b2-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b48b2-117">-Name</span></span>
<span data-ttu-id="b48b2-118">Имя триггера.</span><span class="sxs-lookup"><span data-stu-id="b48b2-118">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TriggerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b48b2-119">-RunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="b48b2-119">-RunStartedAfter</span></span>
<span data-ttu-id="b48b2-120">Время, в течение или после которого событие "выполнение" было Обновлено в формате ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="b48b2-120">The time at or after which the run event was updated in 'ISO 8601' format.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b48b2-121">-RunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="b48b2-121">-RunStartedBefore</span></span>
<span data-ttu-id="b48b2-122">Время, в течение которого событие запуска было Обновлено в формате ISO 8601, или до него.</span><span class="sxs-lookup"><span data-stu-id="b48b2-122">The time at or before which the run event was updated in 'ISO 8601' format.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b48b2-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b48b2-123">-WorkspaceName</span></span>
<span data-ttu-id="b48b2-124">Имя Synapse рабочей области.</span><span class="sxs-lookup"><span data-stu-id="b48b2-124">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b48b2-125">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="b48b2-125">-WorkspaceObject</span></span>
<span data-ttu-id="b48b2-126">объект ввода в рабочую область, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="b48b2-126">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b48b2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b48b2-127">CommonParameters</span></span>
<span data-ttu-id="b48b2-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b48b2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b48b2-129">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b48b2-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b48b2-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b48b2-130">INPUTS</span></span>

### <span data-ttu-id="b48b2-131">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="b48b2-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="b48b2-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b48b2-132">OUTPUTS</span></span>

### <span data-ttu-id="b48b2-133">Microsoft. Azure. Commands. Synapse. Models. PSTriggerRun</span><span class="sxs-lookup"><span data-stu-id="b48b2-133">Microsoft.Azure.Commands.Synapse.Models.PSTriggerRun</span></span>

## <span data-ttu-id="b48b2-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="b48b2-134">NOTES</span></span>

## <span data-ttu-id="b48b2-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b48b2-135">RELATED LINKS</span></span>

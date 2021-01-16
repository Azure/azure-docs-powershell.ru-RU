---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsetriggerrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTriggerRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTriggerRun.md
ms.openlocfilehash: 0d6d3bb99062177e1d75c4ab496562782cf142c1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98393820"
---
# <span data-ttu-id="26034-101">Get-AzSynapseTriggerRun</span><span class="sxs-lookup"><span data-stu-id="26034-101">Get-AzSynapseTriggerRun</span></span>

## <span data-ttu-id="26034-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26034-102">SYNOPSIS</span></span>
<span data-ttu-id="26034-103">Возвращает сведения о запусках триггера.</span><span class="sxs-lookup"><span data-stu-id="26034-103">Returns information about trigger runs.</span></span>

## <span data-ttu-id="26034-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="26034-104">SYNTAX</span></span>

### <span data-ttu-id="26034-105">GetByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="26034-105">GetByName (Default)</span></span>
```
Get-AzSynapseTriggerRun -WorkspaceName <String> -Name <String> -RunStartedAfter <DateTimeOffset>
 -RunStartedBefore <DateTimeOffset> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="26034-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="26034-106">GetByObject</span></span>
```
Get-AzSynapseTriggerRun -WorkspaceObject <PSSynapseWorkspace> -Name <String> -RunStartedAfter <DateTimeOffset>
 -RunStartedBefore <DateTimeOffset> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="26034-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="26034-107">DESCRIPTION</span></span>
<span data-ttu-id="26034-108">Команда **Get-AzSynapseTriggerRun** возвращает подробные сведения о запусках триггера для указанного триггера на заданный период времени.</span><span class="sxs-lookup"><span data-stu-id="26034-108">The **Get-AzSynapseTriggerRun** command returns detailed information about trigger runs for the specified trigger in the given timeframe.</span></span>

## <span data-ttu-id="26034-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="26034-109">EXAMPLES</span></span>

### <span data-ttu-id="26034-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="26034-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseTriggerRun -WorkspaceName ContosoWorkspace -Name ContosoTrigger -RunStartedAfter [DateTimeOffset]"2018-09-01T21:00" -RunStartedBefore [DateTimeOffset]"2019-09-01T21:00"
```

<span data-ttu-id="26034-111">Эта команда отображает сведения о запуске ContosoTrigger в рабочей области ContosoWorkspace, который начался с "2018-09-01T21:00" и "2019-09-01T21:00".</span><span class="sxs-lookup"><span data-stu-id="26034-111">This command shows information about runs for ContosoTrigger in the workspace ContosoWorkspace that started between "2018-09-01T21:00" and "2019-09-01T21:00".</span></span>

### <span data-ttu-id="26034-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="26034-112">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseTriggerRun -Name ContosoTrigger -RunStartedAfter [DateTimeOffset]"2018-09-01T21:00" -RunStartedBefore [DateTimeOffset]"2019-09-01T21:00"
```

<span data-ttu-id="26034-113">Эта команда отображает сведения о запуске ContosoTrigger в рабочей области ContosoWorkspace, который запустился в канале "2018-09-01T21:00" и "2019-09-01T21:00".</span><span class="sxs-lookup"><span data-stu-id="26034-113">This command shows information about runs for ContosoTrigger in the workspace ContosoWorkspace that started between "2018-09-01T21:00" and "2019-09-01T21:00" through pipeline.</span></span>

## <span data-ttu-id="26034-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="26034-114">PARAMETERS</span></span>

### <span data-ttu-id="26034-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26034-115">-DefaultProfile</span></span>
<span data-ttu-id="26034-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="26034-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26034-117">-Name</span><span class="sxs-lookup"><span data-stu-id="26034-117">-Name</span></span>
<span data-ttu-id="26034-118">Имя триггера.</span><span class="sxs-lookup"><span data-stu-id="26034-118">The trigger name.</span></span>

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

### <span data-ttu-id="26034-119">-RunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="26034-119">-RunStartedAfter</span></span>
<span data-ttu-id="26034-120">Время, в течение или после которого событие запуска обновлялось в формате ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="26034-120">The time at or after which the run event was updated in 'ISO 8601' format.</span></span>

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

### <span data-ttu-id="26034-121">-RunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="26034-121">-RunStartedBefore</span></span>
<span data-ttu-id="26034-122">Время, в течение или до которого событие запуска обновлялось в формате ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="26034-122">The time at or before which the run event was updated in 'ISO 8601' format.</span></span>

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

### <span data-ttu-id="26034-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="26034-123">-WorkspaceName</span></span>
<span data-ttu-id="26034-124">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="26034-124">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="26034-125">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="26034-125">-WorkspaceObject</span></span>
<span data-ttu-id="26034-126">объект ввода рабочей области, обычно переданный по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="26034-126">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="26034-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26034-127">CommonParameters</span></span>
<span data-ttu-id="26034-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26034-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26034-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="26034-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26034-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="26034-130">INPUTS</span></span>

### <span data-ttu-id="26034-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="26034-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="26034-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="26034-132">OUTPUTS</span></span>

### <span data-ttu-id="26034-133">Microsoft.Azure.Commands.Synapse.Models.PSTriggerRun</span><span class="sxs-lookup"><span data-stu-id="26034-133">Microsoft.Azure.Commands.Synapse.Models.PSTriggerRun</span></span>

## <span data-ttu-id="26034-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="26034-134">NOTES</span></span>

## <span data-ttu-id="26034-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="26034-135">RELATED LINKS</span></span>
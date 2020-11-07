---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 92261663-CF50-4EBD-85D2-C2E254F39B41
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsStorageInsight.md
ms.openlocfilehash: b7fbfe720cd63389ced0c1703925e1551ebad40e
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/13/2020
ms.locfileid: "93731926"
---
# <span data-ttu-id="aa87c-101">Remove-AzOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="aa87c-101">Remove-AzOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="aa87c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="aa87c-102">SYNOPSIS</span></span>
<span data-ttu-id="aa87c-103">Удаление аналитического анализа данных.</span><span class="sxs-lookup"><span data-stu-id="aa87c-103">Removes a Storage Insight.</span></span>

## <span data-ttu-id="aa87c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="aa87c-104">SYNTAX</span></span>

### <span data-ttu-id="aa87c-105">ByWorkspaceName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="aa87c-105">ByWorkspaceName (Default)</span></span>
```
Remove-AzOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa87c-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="aa87c-106">ByWorkspaceObject</span></span>
```
Remove-AzOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa87c-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="aa87c-107">DESCRIPTION</span></span>
<span data-ttu-id="aa87c-108">Командлет **Remove-AzOperationalInsightsStorageInsight** удаляет представление хранилища из рабочей области.</span><span class="sxs-lookup"><span data-stu-id="aa87c-108">The **Remove-AzOperationalInsightsStorageInsight** cmdlet deletes a Storage Insight from a workspace.</span></span>

## <span data-ttu-id="aa87c-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="aa87c-109">EXAMPLES</span></span>

### <span data-ttu-id="aa87c-110">Пример 1: удаление аналитических данных по имени</span><span class="sxs-lookup"><span data-stu-id="aa87c-110">Example 1: Remove a Storage Insight by name</span></span>
```
PS C:\>Remove-AzOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -Name "MyStorageInsight"
```

<span data-ttu-id="aa87c-111">Эта команда удаляет сведения о хранилище с именем MyStorageInsight из рабочей области с именем MyWorkspace в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="aa87c-111">This command removes the Storage Insight named MyStorageInsight from the workspace named MyWorkspace in the specified resource group.</span></span>
<span data-ttu-id="aa87c-112">В команде не указан параметр *Force* , поэтому перед удалением анализа хранилища появится запрос на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="aa87c-112">The command does not specify the *Force* parameter, so it prompts you for confirmation before removing the Storage Insight.</span></span>

### <span data-ttu-id="aa87c-113">Пример 2: удаление аналитического хранилища без подтверждения</span><span class="sxs-lookup"><span data-stu-id="aa87c-113">Example 2: Remove a Storage Insight without confirmation</span></span>
```
PS C:\>$Workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"

PS C:\>Remove-AzOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight" -Force
```

<span data-ttu-id="aa87c-114">Первая команда использует командлет Get-AzOperationalInsightsWorkspace, чтобы получить рабочую область с именем MyWorkspace, а затем сохранит ее в переменной $Workspace. Вторая команда удаляет сведения о хранилище с именем MyStorageInsight из $Workspace без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="aa87c-114">The first command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then stores it in the $Workspace variable.The second command removes the storage insight named MyStorageInsight from $Workspace without prompting you for confirmation.</span></span>

## <span data-ttu-id="aa87c-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="aa87c-115">PARAMETERS</span></span>

### <span data-ttu-id="aa87c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa87c-116">-DefaultProfile</span></span>
<span data-ttu-id="aa87c-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="aa87c-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aa87c-118">-Force</span><span class="sxs-lookup"><span data-stu-id="aa87c-118">-Force</span></span>
<span data-ttu-id="aa87c-119">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="aa87c-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="aa87c-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="aa87c-120">-Name</span></span>
<span data-ttu-id="aa87c-121">Указывает имя аналитического хранилища.</span><span class="sxs-lookup"><span data-stu-id="aa87c-121">Specifies the name of the Storage Insight.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa87c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa87c-122">-ResourceGroupName</span></span>
<span data-ttu-id="aa87c-123">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="aa87c-123">Specifies the name of an Azure resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa87c-124">-Рабочая область</span><span class="sxs-lookup"><span data-stu-id="aa87c-124">-Workspace</span></span>
<span data-ttu-id="aa87c-125">Указывает рабочую область, в которой находится аналитика хранилища.</span><span class="sxs-lookup"><span data-stu-id="aa87c-125">Specifies the workspace that contains the Storage Insight.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aa87c-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="aa87c-126">-WorkspaceName</span></span>
<span data-ttu-id="aa87c-127">Указывает имя рабочей области, в которой находится аналитика хранилища.</span><span class="sxs-lookup"><span data-stu-id="aa87c-127">Specifies the name of the workspace that contains the Storage Insight.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa87c-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aa87c-128">-Confirm</span></span>
<span data-ttu-id="aa87c-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="aa87c-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa87c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa87c-130">-WhatIf</span></span>
<span data-ttu-id="aa87c-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="aa87c-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa87c-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="aa87c-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa87c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa87c-133">CommonParameters</span></span>
<span data-ttu-id="aa87c-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="aa87c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa87c-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa87c-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa87c-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="aa87c-136">INPUTS</span></span>

### <span data-ttu-id="aa87c-137">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="aa87c-137">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="aa87c-138">System. String</span><span class="sxs-lookup"><span data-stu-id="aa87c-138">System.String</span></span>

## <span data-ttu-id="aa87c-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="aa87c-139">OUTPUTS</span></span>

### <span data-ttu-id="aa87c-140">System. void</span><span class="sxs-lookup"><span data-stu-id="aa87c-140">System.Void</span></span>

## <span data-ttu-id="aa87c-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="aa87c-141">NOTES</span></span>

## <span data-ttu-id="aa87c-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="aa87c-142">RELATED LINKS</span></span>

[<span data-ttu-id="aa87c-143">Командлеты оперативной аналитики Azure</span><span class="sxs-lookup"><span data-stu-id="aa87c-143">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)

[<span data-ttu-id="aa87c-144">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="aa87c-144">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)



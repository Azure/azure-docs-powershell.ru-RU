---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 92261663-CF50-4EBD-85D2-C2E254F39B41
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/remove-azoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsStorageInsight.md
ms.openlocfilehash: 7eece12130095889c5da574a4d0a3ec8d0b0bed2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989764"
---
# <span data-ttu-id="f023a-101">Remove-AzOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="f023a-101">Remove-AzOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="f023a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f023a-102">SYNOPSIS</span></span>
<span data-ttu-id="f023a-103">Удаляет сведения о хранилище.</span><span class="sxs-lookup"><span data-stu-id="f023a-103">Removes a Storage Insight.</span></span>

## <span data-ttu-id="f023a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f023a-104">SYNTAX</span></span>

### <span data-ttu-id="f023a-105">ByWorkspaceName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f023a-105">ByWorkspaceName (Default)</span></span>
```
Remove-AzOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f023a-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="f023a-106">ByWorkspaceObject</span></span>
```
Remove-AzOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f023a-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f023a-107">DESCRIPTION</span></span>
<span data-ttu-id="f023a-108">При этом из рабочей области **удаляется** информация о хранилище.</span><span class="sxs-lookup"><span data-stu-id="f023a-108">The **Remove-AzOperationalInsightsStorageInsight** cmdlet deletes a Storage Insight from a workspace.</span></span>

## <span data-ttu-id="f023a-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f023a-109">EXAMPLES</span></span>

### <span data-ttu-id="f023a-110">Пример 1. Удаление статистики хранилища по имени</span><span class="sxs-lookup"><span data-stu-id="f023a-110">Example 1: Remove a Storage Insight by name</span></span>
```
PS C:\>Remove-AzOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -Name "MyStorageInsight"
```

<span data-ttu-id="f023a-111">Эта команда удаляет сведения о хранилище с именем MyStorageInsight из рабочей области MyWorkspace в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f023a-111">This command removes the Storage Insight named MyStorageInsight from the workspace named MyWorkspace in the specified resource group.</span></span>
<span data-ttu-id="f023a-112">Команда не указывает параметр *Force,* поэтому перед удалением параметра Storage Insight будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="f023a-112">The command does not specify the *Force* parameter, so it prompts you for confirmation before removing the Storage Insight.</span></span>

### <span data-ttu-id="f023a-113">Пример 2. Удаление статистики хранилища без подтверждения</span><span class="sxs-lookup"><span data-stu-id="f023a-113">Example 2: Remove a Storage Insight without confirmation</span></span>
```
PS C:\>$Workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"

PS C:\>Remove-AzOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight" -Force
```

<span data-ttu-id="f023a-114">Первая команда использует Get-AzOperationalInsightsWorkspace для получения рабочей области MyWorkspace, а затем сохраняет ее в $Workspace переменной. Вторая команда удаляет данные хранилища MyStorageInsight из $Workspace без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="f023a-114">The first command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then stores it in the $Workspace variable.The second command removes the storage insight named MyStorageInsight from $Workspace without prompting you for confirmation.</span></span>

## <span data-ttu-id="f023a-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f023a-115">PARAMETERS</span></span>

### <span data-ttu-id="f023a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f023a-116">-DefaultProfile</span></span>
<span data-ttu-id="f023a-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f023a-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f023a-118">-Force</span><span class="sxs-lookup"><span data-stu-id="f023a-118">-Force</span></span>
<span data-ttu-id="f023a-119">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="f023a-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f023a-120">-Name</span><span class="sxs-lookup"><span data-stu-id="f023a-120">-Name</span></span>
<span data-ttu-id="f023a-121">Указывает имя службы "Сведения о хранилище".</span><span class="sxs-lookup"><span data-stu-id="f023a-121">Specifies the name of the Storage Insight.</span></span>

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

### <span data-ttu-id="f023a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f023a-122">-ResourceGroupName</span></span>
<span data-ttu-id="f023a-123">Имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="f023a-123">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="f023a-124">-Workspace</span><span class="sxs-lookup"><span data-stu-id="f023a-124">-Workspace</span></span>
<span data-ttu-id="f023a-125">Определяет рабочее пространство, содержательное сведения о хранилище.</span><span class="sxs-lookup"><span data-stu-id="f023a-125">Specifies the workspace that contains the Storage Insight.</span></span>

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

### <span data-ttu-id="f023a-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f023a-126">-WorkspaceName</span></span>
<span data-ttu-id="f023a-127">Указывает имя рабочей области, которая содержит сведения о хранилище.</span><span class="sxs-lookup"><span data-stu-id="f023a-127">Specifies the name of the workspace that contains the Storage Insight.</span></span>

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

### <span data-ttu-id="f023a-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f023a-128">-Confirm</span></span>
<span data-ttu-id="f023a-129">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f023a-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f023a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f023a-130">-WhatIf</span></span>
<span data-ttu-id="f023a-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f023a-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f023a-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="f023a-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f023a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f023a-133">CommonParameters</span></span>
<span data-ttu-id="f023a-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f023a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f023a-135">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f023a-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f023a-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f023a-136">INPUTS</span></span>

### <span data-ttu-id="f023a-137">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="f023a-137">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="f023a-138">System.String</span><span class="sxs-lookup"><span data-stu-id="f023a-138">System.String</span></span>

## <span data-ttu-id="f023a-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f023a-139">OUTPUTS</span></span>

### <span data-ttu-id="f023a-140">System.Void</span><span class="sxs-lookup"><span data-stu-id="f023a-140">System.Void</span></span>

## <span data-ttu-id="f023a-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f023a-141">NOTES</span></span>

## <span data-ttu-id="f023a-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f023a-142">RELATED LINKS</span></span>

[<span data-ttu-id="f023a-143">Azure Operational Insights Cmdlets</span><span class="sxs-lookup"><span data-stu-id="f023a-143">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="f023a-144">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="f023a-144">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)



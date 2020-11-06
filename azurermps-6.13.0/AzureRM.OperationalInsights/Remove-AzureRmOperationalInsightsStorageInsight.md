---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 92261663-CF50-4EBD-85D2-C2E254F39B41
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/remove-azurermoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsStorageInsight.md
ms.openlocfilehash: 726386fb4a455b3daab314e5f61d33122592dcf8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564160"
---
# <span data-ttu-id="385a3-101">Remove-AzureRmOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="385a3-101">Remove-AzureRmOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="385a3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="385a3-102">SYNOPSIS</span></span>
<span data-ttu-id="385a3-103">Удаление аналитического анализа данных.</span><span class="sxs-lookup"><span data-stu-id="385a3-103">Removes a Storage Insight.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="385a3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="385a3-104">SYNTAX</span></span>

### <span data-ttu-id="385a3-105">ByWorkspaceName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="385a3-105">ByWorkspaceName (Default)</span></span>
```
Remove-AzureRmOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="385a3-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="385a3-106">ByWorkspaceObject</span></span>
```
Remove-AzureRmOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="385a3-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="385a3-107">DESCRIPTION</span></span>
<span data-ttu-id="385a3-108">Командлет **Remove-AzureRmOperationalInsightsStorageInsight** удаляет представление хранилища из рабочей области.</span><span class="sxs-lookup"><span data-stu-id="385a3-108">The **Remove-AzureRmOperationalInsightsStorageInsight** cmdlet deletes a Storage Insight from a workspace.</span></span>

## <span data-ttu-id="385a3-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="385a3-109">EXAMPLES</span></span>

### <span data-ttu-id="385a3-110">Пример 1: удаление аналитических данных по имени</span><span class="sxs-lookup"><span data-stu-id="385a3-110">Example 1: Remove a Storage Insight by name</span></span>
```
PS C:\>Remove-AzureRmOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -Name "MyStorageInsight"
```

<span data-ttu-id="385a3-111">Эта команда удаляет сведения о хранилище с именем MyStorageInsight из рабочей области с именем MyWorkspace в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="385a3-111">This command removes the Storage Insight named MyStorageInsight from the workspace named MyWorkspace in the specified resource group.</span></span>
<span data-ttu-id="385a3-112">В команде не указан параметр *Force* , поэтому перед удалением анализа хранилища появится запрос на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="385a3-112">The command does not specify the *Force* parameter, so it prompts you for confirmation before removing the Storage Insight.</span></span>

### <span data-ttu-id="385a3-113">Пример 2: удаление аналитического хранилища без подтверждения</span><span class="sxs-lookup"><span data-stu-id="385a3-113">Example 2: Remove a Storage Insight without confirmation</span></span>
```
PS C:\>$Workspace = Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"

PS C:\>Remove-AzureRmOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight" -Force
```

<span data-ttu-id="385a3-114">Первая команда использует командлет Get-AzureRmOperationalInsightsWorkspace, чтобы получить рабочую область с именем MyWorkspace, а затем сохранит ее в переменной $Workspace. Вторая команда удаляет сведения о хранилище с именем MyStorageInsight из $Workspace без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="385a3-114">The first command uses the Get-AzureRmOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then stores it in the $Workspace variable.The second command removes the storage insight named MyStorageInsight from $Workspace without prompting you for confirmation.</span></span>

## <span data-ttu-id="385a3-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="385a3-115">PARAMETERS</span></span>

### <span data-ttu-id="385a3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="385a3-116">-DefaultProfile</span></span>
<span data-ttu-id="385a3-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="385a3-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="385a3-118">-Force</span><span class="sxs-lookup"><span data-stu-id="385a3-118">-Force</span></span>
<span data-ttu-id="385a3-119">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="385a3-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="385a3-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="385a3-120">-Name</span></span>
<span data-ttu-id="385a3-121">Указывает имя аналитического хранилища.</span><span class="sxs-lookup"><span data-stu-id="385a3-121">Specifies the name of the Storage Insight.</span></span>

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

### <span data-ttu-id="385a3-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="385a3-122">-ResourceGroupName</span></span>
<span data-ttu-id="385a3-123">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="385a3-123">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="385a3-124">-Рабочая область</span><span class="sxs-lookup"><span data-stu-id="385a3-124">-Workspace</span></span>
<span data-ttu-id="385a3-125">Указывает рабочую область, в которой находится аналитика хранилища.</span><span class="sxs-lookup"><span data-stu-id="385a3-125">Specifies the workspace that contains the Storage Insight.</span></span>

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

### <span data-ttu-id="385a3-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="385a3-126">-WorkspaceName</span></span>
<span data-ttu-id="385a3-127">Указывает имя рабочей области, в которой находится аналитика хранилища.</span><span class="sxs-lookup"><span data-stu-id="385a3-127">Specifies the name of the workspace that contains the Storage Insight.</span></span>

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

### <span data-ttu-id="385a3-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="385a3-128">-Confirm</span></span>
<span data-ttu-id="385a3-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="385a3-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="385a3-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="385a3-130">-WhatIf</span></span>
<span data-ttu-id="385a3-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="385a3-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="385a3-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="385a3-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="385a3-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="385a3-133">CommonParameters</span></span>
<span data-ttu-id="385a3-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="385a3-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="385a3-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="385a3-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="385a3-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="385a3-136">INPUTS</span></span>

### <span data-ttu-id="385a3-137">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="385a3-137">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>
<span data-ttu-id="385a3-138">Параметры: Workspace (ByValue)</span><span class="sxs-lookup"><span data-stu-id="385a3-138">Parameters: Workspace (ByValue)</span></span>

### <span data-ttu-id="385a3-139">System. String</span><span class="sxs-lookup"><span data-stu-id="385a3-139">System.String</span></span>

## <span data-ttu-id="385a3-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="385a3-140">OUTPUTS</span></span>

### <span data-ttu-id="385a3-141">System. void</span><span class="sxs-lookup"><span data-stu-id="385a3-141">System.Void</span></span>

## <span data-ttu-id="385a3-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="385a3-142">NOTES</span></span>

## <span data-ttu-id="385a3-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="385a3-143">RELATED LINKS</span></span>

[<span data-ttu-id="385a3-144">Командлеты оперативной аналитики Azure</span><span class="sxs-lookup"><span data-stu-id="385a3-144">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="385a3-145">Get-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="385a3-145">Get-AzureRmOperationalInsightsWorkspace</span></span>](./Get-AzureRmOperationalInsightsWorkspace.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 0C35E679-B991-49A8-890F-C8DAB68A8240
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: d02338c34584a68ece2ad3a90887a765f8142347
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98395468"
---
# <span data-ttu-id="f515c-101">Remove-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="f515c-101">Remove-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="f515c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f515c-102">SYNOPSIS</span></span>
<span data-ttu-id="f515c-103">Удаляет рабочее пространство.</span><span class="sxs-lookup"><span data-stu-id="f515c-103">Removes a workspace.</span></span>

## <span data-ttu-id="f515c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f515c-104">SYNTAX</span></span>

```
Remove-AzOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-ForceDelete] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f515c-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f515c-105">DESCRIPTION</span></span>
<span data-ttu-id="f515c-106">Командлет **Remove-AzOperationalInsightsWorkspace** удаляет существующую рабочее пространство.</span><span class="sxs-lookup"><span data-stu-id="f515c-106">The **Remove-AzOperationalInsightsWorkspace** cmdlet deletes an existing workspace.</span></span>
<span data-ttu-id="f515c-107">Если эта область была связана с существующей учетной записью с помощью параметра *CustomerId* во время создания, исходная учетная запись не удаляется на портале Operational Insights.</span><span class="sxs-lookup"><span data-stu-id="f515c-107">If this workspace was linked to an existing account via the *CustomerId* parameter at creation time the original account is not deleted in the Operational Insights portal.</span></span>

## <span data-ttu-id="f515c-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f515c-108">EXAMPLES</span></span>

### <span data-ttu-id="f515c-109">Пример 1. Удаление рабочей области по имени</span><span class="sxs-lookup"><span data-stu-id="f515c-109">Example 1: Remove a workspace by name</span></span>
```
PS C:\>Remove-AzOperationalInsightsWorkspace -ResourceGroupName "ContosResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="f515c-110">Эта команда удаляет из группы ресурсов ContosoResourceGroup рабочее пространство с именем MyWorkspace.</span><span class="sxs-lookup"><span data-stu-id="f515c-110">This command removes the workspace named MyWorkspace from the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="f515c-111">Пример 2. Удаление рабочей области с помощью конвейера без подтверждения</span><span class="sxs-lookup"><span data-stu-id="f515c-111">Example 2: Remove a workspace by using the pipeline and without confirmation</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosResourceGroup" -Name "MyWorkspace" | Remove-AzOperationalInsightsWorkspace -Force
```

<span data-ttu-id="f515c-112">Эта команда использует Get-AzOperationalInsightsWorkspace для получения рабочей области MyWorkspace и передает ее **командлету Remove-AzOperationalInsightsWorkspace** с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="f515c-112">This command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then passes it to the **Remove-AzOperationalInsightsWorkspace** cmdlet by using the pipeline operator to remove it.</span></span>
<span data-ttu-id="f515c-113">Так как *задан* параметр Force, команда не будет подсказок перед удалением рабочей области.</span><span class="sxs-lookup"><span data-stu-id="f515c-113">Since the *Force* parameter is specified, the command does not prompt you before removing the workspace.</span></span>

### <span data-ttu-id="f515c-114">Пример 3. Принудительное удаление рабочей области (восстановить невозможно)</span><span class="sxs-lookup"><span data-stu-id="f515c-114">Example 3: Force delete workspace (cannot be recovered)</span></span>
```
PS C:\> $workspace = New-AzOperationalInsightsWorkspace -ResourceGroupName $rgname -Name $wsname -Location $wslocation
PS C:\> $workspace | Remove-AzOperationalInsightsWorkspace -ForceDelete
```

<span data-ttu-id="f515c-115">Принудительное удаление рабочей области.</span><span class="sxs-lookup"><span data-stu-id="f515c-115">Force delete a workspace.</span></span>

## <span data-ttu-id="f515c-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f515c-116">PARAMETERS</span></span>

### <span data-ttu-id="f515c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f515c-117">-DefaultProfile</span></span>
<span data-ttu-id="f515c-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f515c-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f515c-119">-Force</span><span class="sxs-lookup"><span data-stu-id="f515c-119">-Force</span></span>
<span data-ttu-id="f515c-120">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="f515c-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f515c-121">-ForceDelete</span><span class="sxs-lookup"><span data-stu-id="f515c-121">-ForceDelete</span></span>
<span data-ttu-id="f515c-122">Принудительное удаление рабочей области.</span><span class="sxs-lookup"><span data-stu-id="f515c-122">Force delete workspace.</span></span>

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

### <span data-ttu-id="f515c-123">-Name</span><span class="sxs-lookup"><span data-stu-id="f515c-123">-Name</span></span>
<span data-ttu-id="f515c-124">Указывает имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="f515c-124">Specifies the name of the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f515c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f515c-125">-ResourceGroupName</span></span>
<span data-ttu-id="f515c-126">Имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="f515c-126">Specifies the name of an Azure resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f515c-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f515c-127">-Confirm</span></span>
<span data-ttu-id="f515c-128">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="f515c-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f515c-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f515c-129">-WhatIf</span></span>
<span data-ttu-id="f515c-130">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f515c-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f515c-131">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="f515c-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f515c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f515c-132">CommonParameters</span></span>
<span data-ttu-id="f515c-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f515c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f515c-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f515c-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f515c-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f515c-135">INPUTS</span></span>

### <span data-ttu-id="f515c-136">System.String</span><span class="sxs-lookup"><span data-stu-id="f515c-136">System.String</span></span>

## <span data-ttu-id="f515c-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f515c-137">OUTPUTS</span></span>

### <span data-ttu-id="f515c-138">System.Void</span><span class="sxs-lookup"><span data-stu-id="f515c-138">System.Void</span></span>

## <span data-ttu-id="f515c-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f515c-139">NOTES</span></span>

## <span data-ttu-id="f515c-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f515c-140">RELATED LINKS</span></span>

[<span data-ttu-id="f515c-141">Azure Operational Insights Cmdlets</span><span class="sxs-lookup"><span data-stu-id="f515c-141">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="f515c-142">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="f515c-142">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)



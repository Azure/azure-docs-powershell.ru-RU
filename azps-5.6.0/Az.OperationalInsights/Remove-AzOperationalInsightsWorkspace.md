---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 0C35E679-B991-49A8-890F-C8DAB68A8240
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/remove-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: 916e818b628608fcae7001797af298317ff96a4b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989761"
---
# <span data-ttu-id="699db-101">Remove-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="699db-101">Remove-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="699db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="699db-102">SYNOPSIS</span></span>
<span data-ttu-id="699db-103">Удаляет рабочее пространство.</span><span class="sxs-lookup"><span data-stu-id="699db-103">Removes a workspace.</span></span>

## <span data-ttu-id="699db-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="699db-104">SYNTAX</span></span>

```
Remove-AzOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-ForceDelete] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="699db-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="699db-105">DESCRIPTION</span></span>
<span data-ttu-id="699db-106">Командлет **Remove-AzOperationalInsightsWorkspace** удаляет существующую рабочее пространство.</span><span class="sxs-lookup"><span data-stu-id="699db-106">The **Remove-AzOperationalInsightsWorkspace** cmdlet deletes an existing workspace.</span></span>
<span data-ttu-id="699db-107">Если эта область была связана с существующей учетной записью с помощью параметра *CustomerId* во время создания, исходная учетная запись не удаляется на портале Operational Insights.</span><span class="sxs-lookup"><span data-stu-id="699db-107">If this workspace was linked to an existing account via the *CustomerId* parameter at creation time the original account is not deleted in the Operational Insights portal.</span></span>

## <span data-ttu-id="699db-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="699db-108">EXAMPLES</span></span>

### <span data-ttu-id="699db-109">Пример 1. Удаление рабочей области по имени</span><span class="sxs-lookup"><span data-stu-id="699db-109">Example 1: Remove a workspace by name</span></span>
```
PS C:\>Remove-AzOperationalInsightsWorkspace -ResourceGroupName "ContosResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="699db-110">Эта команда удаляет из группы ресурсов ContosoResourceGroup рабочее пространство с именем MyWorkspace.</span><span class="sxs-lookup"><span data-stu-id="699db-110">This command removes the workspace named MyWorkspace from the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="699db-111">Пример 2. Удаление рабочей области с помощью конвейера без подтверждения</span><span class="sxs-lookup"><span data-stu-id="699db-111">Example 2: Remove a workspace by using the pipeline and without confirmation</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosResourceGroup" -Name "MyWorkspace" | Remove-AzOperationalInsightsWorkspace -Force
```

<span data-ttu-id="699db-112">Эта команда использует Get-AzOperationalInsightsWorkspace для получения рабочей области MyWorkspace и передает ее **командлету Remove-AzOperationalInsightsWorkspace** с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="699db-112">This command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then passes it to the **Remove-AzOperationalInsightsWorkspace** cmdlet by using the pipeline operator to remove it.</span></span>
<span data-ttu-id="699db-113">Так как *задан* параметр Force, команда не будет подсказок перед удалением рабочей области.</span><span class="sxs-lookup"><span data-stu-id="699db-113">Since the *Force* parameter is specified, the command does not prompt you before removing the workspace.</span></span>

### <span data-ttu-id="699db-114">Пример 3. Принудительное удаление рабочей области (восстановить невозможно)</span><span class="sxs-lookup"><span data-stu-id="699db-114">Example 3: Force delete workspace (cannot be recovered)</span></span>
```
PS C:\> $workspace = New-AzOperationalInsightsWorkspace -ResourceGroupName $rgname -Name $wsname -Location $wslocation
PS C:\> $workspace | Remove-AzOperationalInsightsWorkspace -ForceDelete
```

<span data-ttu-id="699db-115">Принудительное удаление рабочей области.</span><span class="sxs-lookup"><span data-stu-id="699db-115">Force delete a workspace.</span></span>

## <span data-ttu-id="699db-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="699db-116">PARAMETERS</span></span>

### <span data-ttu-id="699db-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="699db-117">-DefaultProfile</span></span>
<span data-ttu-id="699db-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="699db-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="699db-119">-Force</span><span class="sxs-lookup"><span data-stu-id="699db-119">-Force</span></span>
<span data-ttu-id="699db-120">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="699db-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="699db-121">-ForceDelete</span><span class="sxs-lookup"><span data-stu-id="699db-121">-ForceDelete</span></span>
<span data-ttu-id="699db-122">Принудительное удаление рабочей области.</span><span class="sxs-lookup"><span data-stu-id="699db-122">Force delete workspace.</span></span>

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

### <span data-ttu-id="699db-123">-Name</span><span class="sxs-lookup"><span data-stu-id="699db-123">-Name</span></span>
<span data-ttu-id="699db-124">Указывает имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="699db-124">Specifies the name of the workspace.</span></span>

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

### <span data-ttu-id="699db-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="699db-125">-ResourceGroupName</span></span>
<span data-ttu-id="699db-126">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="699db-126">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="699db-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="699db-127">-Confirm</span></span>
<span data-ttu-id="699db-128">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="699db-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="699db-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="699db-129">-WhatIf</span></span>
<span data-ttu-id="699db-130">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="699db-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="699db-131">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="699db-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="699db-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="699db-132">CommonParameters</span></span>
<span data-ttu-id="699db-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="699db-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="699db-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="699db-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="699db-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="699db-135">INPUTS</span></span>

### <span data-ttu-id="699db-136">System.String</span><span class="sxs-lookup"><span data-stu-id="699db-136">System.String</span></span>

## <span data-ttu-id="699db-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="699db-137">OUTPUTS</span></span>

### <span data-ttu-id="699db-138">System.Void</span><span class="sxs-lookup"><span data-stu-id="699db-138">System.Void</span></span>

## <span data-ttu-id="699db-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="699db-139">NOTES</span></span>

## <span data-ttu-id="699db-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="699db-140">RELATED LINKS</span></span>

[<span data-ttu-id="699db-141">Azure Operational Insights Cmdlets</span><span class="sxs-lookup"><span data-stu-id="699db-141">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="699db-142">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="699db-142">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)



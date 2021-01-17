---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: A837077C-0A79-431C-93D2-799B2134EE69
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzAlertRule.md
ms.openlocfilehash: f515d7db58e75cc916478e07edb4e34233201a4d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98393460"
---
# <span data-ttu-id="56acd-101">Get-AzAlertRule</span><span class="sxs-lookup"><span data-stu-id="56acd-101">Get-AzAlertRule</span></span>

## <span data-ttu-id="56acd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56acd-102">SYNOPSIS</span></span>
<span data-ttu-id="56acd-103">Получает правила оповещения.</span><span class="sxs-lookup"><span data-stu-id="56acd-103">Gets alert rules.</span></span>

## <span data-ttu-id="56acd-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="56acd-104">SYNTAX</span></span>

### <span data-ttu-id="56acd-105">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="56acd-105">GetByResourceGroup</span></span>
```
Get-AzAlertRule -ResourceGroupName <String> [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="56acd-106">GetByName</span><span class="sxs-lookup"><span data-stu-id="56acd-106">GetByName</span></span>
```
Get-AzAlertRule -ResourceGroupName <String> -Name <String> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="56acd-107">GetByResourceUri</span><span class="sxs-lookup"><span data-stu-id="56acd-107">GetByResourceUri</span></span>
```
Get-AzAlertRule -ResourceGroupName <String> -TargetResourceId <String> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="56acd-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="56acd-108">DESCRIPTION</span></span>
<span data-ttu-id="56acd-109">С **помощью cmdlet Get-AzAlertRule** можно получить правило оповещения по имени, URI или всем правилам оповещения из указанной группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="56acd-109">The **Get-AzAlertRule** cmdlet gets an alert rule by its name or URI, or all alert rules from a specified resource group.</span></span>

## <span data-ttu-id="56acd-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="56acd-110">EXAMPLES</span></span>

### <span data-ttu-id="56acd-111">Пример 1. Получите правила оповещения для группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="56acd-111">Example 1: Get alert rules for a resource group</span></span>
```
PS C:\>Get-AzAlertRule -ResourceGroup "Default-Web-CentralUS"
```

<span data-ttu-id="56acd-112">Эта команда получает все правила оповещения для группы ресурсов Default-Web-CentralUS.</span><span class="sxs-lookup"><span data-stu-id="56acd-112">This command gets all of the alert rules for the resource group named Default-Web-CentralUS.</span></span>
<span data-ttu-id="56acd-113">Выходные данные не содержат подробных сведений о правилах, так как параметр *DetailedOutput* не указан.</span><span class="sxs-lookup"><span data-stu-id="56acd-113">The output does not contain details about the rules because the *DetailedOutput* parameter is not specified.</span></span>

### <span data-ttu-id="56acd-114">Пример 2. Получите правило оповещения по имени</span><span class="sxs-lookup"><span data-stu-id="56acd-114">Example 2: Get an alert rule by name</span></span>
```
PS C:\>Get-AzAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8"
```

<span data-ttu-id="56acd-115">Эта команда получает правило оповещения myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span><span class="sxs-lookup"><span data-stu-id="56acd-115">This command gets the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span></span>
<span data-ttu-id="56acd-116">Так как *параметр DetailedOutput* не указан, выходные данные содержат только основные сведения о правиле оповещения.</span><span class="sxs-lookup"><span data-stu-id="56acd-116">Because the *DetailedOutput* parameter is not specified, the output contains only basic information about the alert rule.</span></span>

### <span data-ttu-id="56acd-117">Пример 3. Получите правило оповещения по имени с подробными выходными сведениями</span><span class="sxs-lookup"><span data-stu-id="56acd-117">Example 3: Get an alert rule by name with detailed output</span></span>
```
PS C:\>Get-AzAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8" -DetailedOutput
```

<span data-ttu-id="56acd-118">Эта команда получает правило оповещения myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span><span class="sxs-lookup"><span data-stu-id="56acd-118">This command gets the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span></span>
<span data-ttu-id="56acd-119">Параметр *DetailedOutput* задан, поэтому выходные данные должны быть подробны.</span><span class="sxs-lookup"><span data-stu-id="56acd-119">The *DetailedOutput* parameter is specified, so the output is detailed.</span></span>

## <span data-ttu-id="56acd-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="56acd-120">PARAMETERS</span></span>

### <span data-ttu-id="56acd-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56acd-121">-DefaultProfile</span></span>
<span data-ttu-id="56acd-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="56acd-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="56acd-123">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="56acd-123">-DetailedOutput</span></span>
<span data-ttu-id="56acd-124">Отображение полных сведений в выходных данных.</span><span class="sxs-lookup"><span data-stu-id="56acd-124">Displays full details in the output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56acd-125">-Name</span><span class="sxs-lookup"><span data-stu-id="56acd-125">-Name</span></span>
<span data-ttu-id="56acd-126">Имя правила оповещения, которое нужно получить.</span><span class="sxs-lookup"><span data-stu-id="56acd-126">Specifies the name of the alert rule to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56acd-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56acd-127">-ResourceGroupName</span></span>
<span data-ttu-id="56acd-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="56acd-128">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56acd-129">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="56acd-129">-TargetResourceId</span></span>
<span data-ttu-id="56acd-130">Определяет ИД целевого ресурса.</span><span class="sxs-lookup"><span data-stu-id="56acd-130">Specifies the ID of the target resource.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56acd-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56acd-131">CommonParameters</span></span>
<span data-ttu-id="56acd-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56acd-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56acd-133">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="56acd-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56acd-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="56acd-134">INPUTS</span></span>

### <span data-ttu-id="56acd-135">System.String</span><span class="sxs-lookup"><span data-stu-id="56acd-135">System.String</span></span>

### <span data-ttu-id="56acd-136">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="56acd-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="56acd-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="56acd-137">OUTPUTS</span></span>

### <span data-ttu-id="56acd-138">Microsoft.Azure.Commands.Insights.OutputClasses.PSAlertRule</span><span class="sxs-lookup"><span data-stu-id="56acd-138">Microsoft.Azure.Commands.Insights.OutputClasses.PSAlertRule</span></span>

## <span data-ttu-id="56acd-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="56acd-139">NOTES</span></span>

## <span data-ttu-id="56acd-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="56acd-140">RELATED LINKS</span></span>

[<span data-ttu-id="56acd-141">Add-AzLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="56acd-141">Add-AzLogAlertRule</span></span>](./Add-AzLogAlertRule.md)

[<span data-ttu-id="56acd-142">Add-AzMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="56acd-142">Add-AzMetricAlertRule</span></span>](./Add-AzMetricAlertRule.md)

[<span data-ttu-id="56acd-143">Add-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="56acd-143">Add-AzWebtestAlertRule</span></span>](./Add-AzWebtestAlertRule.md)

[<span data-ttu-id="56acd-144">Get-AzAlertHistory</span><span class="sxs-lookup"><span data-stu-id="56acd-144">Get-AzAlertHistory</span></span>](./Get-AzAlertHistory.md)

[<span data-ttu-id="56acd-145">Remove-AzAlertRule</span><span class="sxs-lookup"><span data-stu-id="56acd-145">Remove-AzAlertRule</span></span>](./Remove-AzAlertRule.md)



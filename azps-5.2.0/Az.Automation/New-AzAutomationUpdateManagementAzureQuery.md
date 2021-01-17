---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationupdatemanagementazurequery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationUpdateManagementAzureQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationUpdateManagementAzureQuery.md
ms.openlocfilehash: 68139ff184df62583b3077a38fbc2e26fd5eae09
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98418460"
---
# <span data-ttu-id="4fb0a-101">New-AzAutomationUpdateManagementAzureQuery</span><span class="sxs-lookup"><span data-stu-id="4fb0a-101">New-AzAutomationUpdateManagementAzureQuery</span></span>

## <span data-ttu-id="4fb0a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4fb0a-102">SYNOPSIS</span></span>
<span data-ttu-id="4fb0a-103">Создание объекта запроса azure Automation Software Update Configuration Azure.</span><span class="sxs-lookup"><span data-stu-id="4fb0a-103">Creates azure automation software update configuration azure query object.</span></span>

## <span data-ttu-id="4fb0a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4fb0a-104">SYNTAX</span></span>

```
New-AzAutomationUpdateManagementAzureQuery -Scope <String[]> [-Location <String[]>] [-Tag <Hashtable>]
 [-FilterOperator <TagOperators>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4fb0a-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4fb0a-105">DESCRIPTION</span></span>
<span data-ttu-id="4fb0a-106">Создает объект запросов Azure для обновления программного обеспечения, который будет использоваться для создания конфигурации обновления программного обеспечения, которая будет работать по расписанию для обновления списка динамически урегулированного списка виртуальных машин Azure.</span><span class="sxs-lookup"><span data-stu-id="4fb0a-106">Creates a software update configuration azure queries object that will be used to create a software update configuration which will runs on a schedule to update a list of dynamically resolved list of azure virtual machines.</span></span>

## <span data-ttu-id="4fb0a-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4fb0a-107">EXAMPLES</span></span>

### <span data-ttu-id="4fb0a-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4fb0a-108">Example 1</span></span>
```powershell
PS C:\>$query1Scope = @(        
"/subscriptions/22e2445a-0984-4fa5-86a4-0280d76c4b2c/resourceGroups/resourceGroupName",
"/subscriptions/32e2445a-0984-4fa5-86a4-0280d76c4b2d/"
    )
PS C:\>$query1Location =@("Japan East", "UK South")
PS C:\>$query1FilterOperator = "All"
PS C:\>$tag1 = @{"tag1"= @("tag1Value1", "tag1Value2")}
PS C:\>$tag1.add("tag2", "tag2Value")
PS C:\>$azq = New-AzAutomationUpdateManagementAzureQuery -ResourceGroupName "mygroup" `
                                       -AutomationAccountName "myaccount" `
                                       -Scope $query1Scope `
                                       -Location $query1Location `
                                       -Tag $tag1
PS C:\>$AzureQueries = @($azq)
PS C:\> $startTime = [DateTimeOffset]"2018-09-13T21:00"

PS C:\> $duration = New-TimeSpan -Hours 2
PS C:\> $schedule = New-AzAutomationSchedule -ResourceGroupName "mygroup" `
                                                  -AutomationAccountName "myaccount" `
                                                  -Name MyWeeklySchedule `
                                                  -StartTime $startTime `
                                                  -DaysOfWeek Saturday `
                                                  -WeekInterval 1 `
                                                  -ForUpdateConfiguration

New-AzAutomationSoftwareUpdateConfiguration -ResourceGroupName "mygroup" `
                                                 -AutomationAccountName "myaccount" `
                                                 -Schedule $schedule `
                                                 -Windows `                                                 
                                                 -AzureQuery $AzureQueries `
                                                 -IncludedUpdateClassification Critical `
                                                 -Duration $duration

UpdateConfiguration   : Microsoft.Azure.Commands.Automation.Model.UpdateManagement.UpdateConfiguration
ScheduleConfiguration : Microsoft.Azure.Commands.Automation.Model.Schedule
ProvisioningState     : Provisioning
ErrorInfo             :
ResourceGroupName     : mygroup
AutomationAccountName : myaccount
Name                  : MyWeeklySchedule
CreationTime          : 9/14/2018 3:53:27 AM +00:00
LastModifiedTime      : 9/14/2018 3:53:27 AM +00:00
Description           :

```

## <span data-ttu-id="4fb0a-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4fb0a-109">PARAMETERS</span></span>

### <span data-ttu-id="4fb0a-110">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="4fb0a-110">-AutomationAccountName</span></span>
<span data-ttu-id="4fb0a-111">Имя учетной записи автоматизации.</span><span class="sxs-lookup"><span data-stu-id="4fb0a-111">The automation account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fb0a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fb0a-112">-DefaultProfile</span></span>
<span data-ttu-id="4fb0a-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4fb0a-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fb0a-114">-FilterOperator</span><span class="sxs-lookup"><span data-stu-id="4fb0a-114">-FilterOperator</span></span>
<span data-ttu-id="4fb0a-115">Оператор фильтра тегов.</span><span class="sxs-lookup"><span data-stu-id="4fb0a-115">Tag filter operator.</span></span>

```yaml
Type: TagOperators
Parameter Sets: (All)
Aliases:
Accepted values: All, Any

Required: False
Position: Named
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="4fb0a-116">-Location</span><span class="sxs-lookup"><span data-stu-id="4fb0a-116">-Location</span></span>
<span data-ttu-id="4fb0a-117">Список мест для виртуальных машин Azure.</span><span class="sxs-lookup"><span data-stu-id="4fb0a-117">List of locations for azure virtual machines.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="4fb0a-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4fb0a-118">-ResourceGroupName</span></span>
<span data-ttu-id="4fb0a-119">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4fb0a-119">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fb0a-120">-Scope</span><span class="sxs-lookup"><span data-stu-id="4fb0a-120">-Scope</span></span>
<span data-ttu-id="4fb0a-121">ИД ресурсов для виртуальных машин Azure.</span><span class="sxs-lookup"><span data-stu-id="4fb0a-121">Resource Ids for azure virtual machines.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="4fb0a-122">-Tag</span><span class="sxs-lookup"><span data-stu-id="4fb0a-122">-Tag</span></span>
<span data-ttu-id="4fb0a-123">Тег для виртуальных машин Azure.</span><span class="sxs-lookup"><span data-stu-id="4fb0a-123">Tag for azure virtual machines.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="4fb0a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fb0a-124">CommonParameters</span></span>
<span data-ttu-id="4fb0a-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4fb0a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="4fb0a-126">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4fb0a-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fb0a-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4fb0a-127">INPUTS</span></span>

### <span data-ttu-id="4fb0a-128">System.String[]</span><span class="sxs-lookup"><span data-stu-id="4fb0a-128">System.String[]</span></span>

### <span data-ttu-id="4fb0a-129">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="4fb0a-129">System.Collections.Hashtable</span></span>

### <span data-ttu-id="4fb0a-130">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.TagOperators</span><span class="sxs-lookup"><span data-stu-id="4fb0a-130">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.TagOperators</span></span>

### <span data-ttu-id="4fb0a-131">System.String</span><span class="sxs-lookup"><span data-stu-id="4fb0a-131">System.String</span></span>

## <span data-ttu-id="4fb0a-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4fb0a-132">OUTPUTS</span></span>

### <span data-ttu-id="4fb0a-133">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.AzureQueryProperties</span><span class="sxs-lookup"><span data-stu-id="4fb0a-133">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.AzureQueryProperties</span></span>

## <span data-ttu-id="4fb0a-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4fb0a-134">NOTES</span></span>

## <span data-ttu-id="4fb0a-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4fb0a-135">RELATED LINKS</span></span>

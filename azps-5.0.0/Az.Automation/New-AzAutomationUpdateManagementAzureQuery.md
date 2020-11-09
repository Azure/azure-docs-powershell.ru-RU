---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationupdatemanagementazurequery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationUpdateManagementAzureQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationUpdateManagementAzureQuery.md
ms.openlocfilehash: 68139ff184df62583b3077a38fbc2e26fd5eae09
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94315284"
---
# <span data-ttu-id="56063-101">New-AzAutomationUpdateManagementAzureQuery</span><span class="sxs-lookup"><span data-stu-id="56063-101">New-AzAutomationUpdateManagementAzureQuery</span></span>

## <span data-ttu-id="56063-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="56063-102">SYNOPSIS</span></span>
<span data-ttu-id="56063-103">Создает объект запроса конфигурации обновления программного обеспечения Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="56063-103">Creates azure automation software update configuration azure query object.</span></span>

## <span data-ttu-id="56063-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="56063-104">SYNTAX</span></span>

```
New-AzAutomationUpdateManagementAzureQuery -Scope <String[]> [-Location <String[]>] [-Tag <Hashtable>]
 [-FilterOperator <TagOperators>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="56063-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="56063-105">DESCRIPTION</span></span>
<span data-ttu-id="56063-106">Создание объекта запросов на настройку обновления программного обеспечения Azure, который будет использоваться для создания конфигурации обновления программного обеспечения, которая будет выполняться по расписанию для обновления списка динамически разрешенного списка виртуальных машин Azure.</span><span class="sxs-lookup"><span data-stu-id="56063-106">Creates a software update configuration azure queries object that will be used to create a software update configuration which will runs on a schedule to update a list of dynamically resolved list of azure virtual machines.</span></span>

## <span data-ttu-id="56063-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="56063-107">EXAMPLES</span></span>

### <span data-ttu-id="56063-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="56063-108">Example 1</span></span>
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

## <span data-ttu-id="56063-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="56063-109">PARAMETERS</span></span>

### <span data-ttu-id="56063-110">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="56063-110">-AutomationAccountName</span></span>
<span data-ttu-id="56063-111">Имя учетной записи службы автоматизации.</span><span class="sxs-lookup"><span data-stu-id="56063-111">The automation account name.</span></span>

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

### <span data-ttu-id="56063-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56063-112">-DefaultProfile</span></span>
<span data-ttu-id="56063-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="56063-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56063-114">-FilterOperator</span><span class="sxs-lookup"><span data-stu-id="56063-114">-FilterOperator</span></span>
<span data-ttu-id="56063-115">Оператор фильтра тегов.</span><span class="sxs-lookup"><span data-stu-id="56063-115">Tag filter operator.</span></span>

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

### <span data-ttu-id="56063-116">-Location</span><span class="sxs-lookup"><span data-stu-id="56063-116">-Location</span></span>
<span data-ttu-id="56063-117">Список местоположений для виртуальных машин Azure.</span><span class="sxs-lookup"><span data-stu-id="56063-117">List of locations for azure virtual machines.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="56063-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56063-118">-ResourceGroupName</span></span>
<span data-ttu-id="56063-119">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="56063-119">The resource group name.</span></span>

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

### <span data-ttu-id="56063-120">-Scope</span><span class="sxs-lookup"><span data-stu-id="56063-120">-Scope</span></span>
<span data-ttu-id="56063-121">Идентификаторы ресурсов для виртуальных машин Azure.</span><span class="sxs-lookup"><span data-stu-id="56063-121">Resource Ids for azure virtual machines.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="56063-122">-Тег</span><span class="sxs-lookup"><span data-stu-id="56063-122">-Tag</span></span>
<span data-ttu-id="56063-123">Тег для виртуальных машин Azure.</span><span class="sxs-lookup"><span data-stu-id="56063-123">Tag for azure virtual machines.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="56063-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56063-124">CommonParameters</span></span>
<span data-ttu-id="56063-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="56063-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="56063-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56063-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56063-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="56063-127">INPUTS</span></span>

### <span data-ttu-id="56063-128">System. String []</span><span class="sxs-lookup"><span data-stu-id="56063-128">System.String[]</span></span>

### <span data-ttu-id="56063-129">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="56063-129">System.Collections.Hashtable</span></span>

### <span data-ttu-id="56063-130">Microsoft. Azure. Commands. Automation. Model. UpdateManagement. TagOperators</span><span class="sxs-lookup"><span data-stu-id="56063-130">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.TagOperators</span></span>

### <span data-ttu-id="56063-131">System. String</span><span class="sxs-lookup"><span data-stu-id="56063-131">System.String</span></span>

## <span data-ttu-id="56063-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="56063-132">OUTPUTS</span></span>

### <span data-ttu-id="56063-133">Microsoft. Azure. Commands. Automation. Model. UpdateManagement. AzureQueryProperties</span><span class="sxs-lookup"><span data-stu-id="56063-133">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.AzureQueryProperties</span></span>

## <span data-ttu-id="56063-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="56063-134">NOTES</span></span>

## <span data-ttu-id="56063-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="56063-135">RELATED LINKS</span></span>

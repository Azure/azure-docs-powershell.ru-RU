---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: F271BCB1-6D43-48E5-BB51-00288F57BFFB
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azlogicapprunhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunHistory.md
ms.openlocfilehash: 1e847131a67e55fa7a9c520c6ce5a5d96f0475f3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98409959"
---
# <span data-ttu-id="2446f-101">Get-AzLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="2446f-101">Get-AzLogicAppRunHistory</span></span>

## <span data-ttu-id="2446f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2446f-102">SYNOPSIS</span></span>
<span data-ttu-id="2446f-103">Получает историю запуска приложения логики.</span><span class="sxs-lookup"><span data-stu-id="2446f-103">Gets the run history of a logic app.</span></span>

## <span data-ttu-id="2446f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2446f-104">SYNTAX</span></span>

```
Get-AzLogicAppRunHistory -ResourceGroupName <String> -Name <String> [-RunName <String>] [-FollowNextPageLink]
 [-MaximumFollowNextPageLink <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2446f-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2446f-105">DESCRIPTION</span></span>
<span data-ttu-id="2446f-106">С **помощью cmdlet get-AzLogicAppRunHistory** можно получить историю запуска приложения логики.</span><span class="sxs-lookup"><span data-stu-id="2446f-106">The **Get-AzLogicAppRunHistory** cmdlet gets the run history of a logic app.</span></span>
<span data-ttu-id="2446f-107">Этот cmdlet возвращает коллекцию объектов **WorkflowRun.**</span><span class="sxs-lookup"><span data-stu-id="2446f-107">This cmdlet returns a collection of **WorkflowRun** objects.</span></span>
<span data-ttu-id="2446f-108">Укажите приложение и группу ресурсов для логики.</span><span class="sxs-lookup"><span data-stu-id="2446f-108">Specify the logic app and resource group.</span></span>
<span data-ttu-id="2446f-109">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="2446f-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="2446f-110">Чтобы использовать динамический параметр, введите его в команду.</span><span class="sxs-lookup"><span data-stu-id="2446f-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="2446f-111">Чтобы найти имена динамических параметров, введите дефис (-) после имени cmdlet, а затем нажимая клавишу TAB для циклическиго перебора доступных параметров.</span><span class="sxs-lookup"><span data-stu-id="2446f-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="2446f-112">Если параметр обязательного шаблона не задан, будет выдан запрос на его значение.</span><span class="sxs-lookup"><span data-stu-id="2446f-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="2446f-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2446f-113">EXAMPLES</span></span>

### <span data-ttu-id="2446f-114">Пример 1. Просмотр истории запуска приложения логики</span><span class="sxs-lookup"><span data-stu-id="2446f-114">Example 1: Get the run history of a logic app</span></span>
```powershell
PS C:\>Get-AzLogicAppRunHistory -ResourceGroupName "Resourcegroup11" -Name "LogicApp03"
CorrelationId    : 55830326-9042-404d-a4c3-fab198106a57
EndTime          : 1/13/2016 2:46:55 PM
Error            : {code, message}
Name             : 08587489104702792076
Outputs          : {}
StartTime        : 1/13/2016 2:46:55 PM
Status           : Failed
TriggerName      : 
LogicAppName     : LogicApp03
LogicAppVersion  : 08587489107859952540

CorrelationId    : d3ddc917-9aaa-47b3-8814-c621c2ae530b
EndTime          : 1/13/2016 2:42:56 PM
Error            : {code, message}
Name             : 08587489107100664541
Outputs          : {}
StartTime        : 1/13/2016 2:42:55 PM
Status           : Failed
TriggerName      : httpTrigger
LogicAppName     : LogicApp03
LogicAppVersion  : 08587489107859952120
```

<span data-ttu-id="2446f-115">Эта команда получает историю запуска приложения logic с именем LogicApp03.</span><span class="sxs-lookup"><span data-stu-id="2446f-115">This command gets the run history of a logic app named LogicApp03.</span></span>

### <span data-ttu-id="2446f-116">Пример 2. Запуск логического приложения</span><span class="sxs-lookup"><span data-stu-id="2446f-116">Example 2: Get a logic app run</span></span>
```powershell
PS C:\>Get-AzLogicAppRunHistory -ResourceGroupName "Resourcegroup11" -Name "LogicApp03" -RunName "08587489104702792076"
CorrelationId    : 55830326-9042-404d-a4c3-fab198106a57
EndTime          : 1/13/2016 2:46:55 PM
Error            : {code, message}
Name             : 08587489104702792076
Outputs          : {}
StartTime        : 1/13/2016 2:46:55 PM
Status           : Failed
TriggerName      : 
LogicAppName     : LogicApp03
LogicAppVersion  : 08587489107859952120
```

<span data-ttu-id="2446f-117">Эта команда получает запускать определенное приложение логики для приложения LogicApp03.</span><span class="sxs-lookup"><span data-stu-id="2446f-117">This command gets a specific logic app run for the logic app named LogicApp03.</span></span>

### <span data-ttu-id="2446f-118">Пример 3</span><span class="sxs-lookup"><span data-stu-id="2446f-118">Example 3</span></span>

```powershell
Get-AzLogicAppRunHistory -Name 'LogicApp03' -ResourceGroupName MyResourceGroup -FollowNextPageLink
```

<span data-ttu-id="2446f-119">Эта команда получает весь история запуска логического приложения LogicApp03 с помощью nextPageLink.</span><span class="sxs-lookup"><span data-stu-id="2446f-119">This command gets the entire run history of a logic app named LogicApp03 by following the NextPageLink.</span></span>

### <span data-ttu-id="2446f-120">Пример 4</span><span class="sxs-lookup"><span data-stu-id="2446f-120">Example 4</span></span>

```powershell
Get-AzLogicAppRunHistory -Name 'LogicApp03' -ResourceGroupName MyResourceGroup -FollowNextPageLink -MaximumFollowNextPageLink 1
```

<span data-ttu-id="2446f-121">Эта команда получает первые две страницы истории запуска логического приложения LogicApp03, следуя следующей команде NextPageLink и ограничив размер результатов двумя страницами.</span><span class="sxs-lookup"><span data-stu-id="2446f-121">This command gets the first two pages of run history of a logic app named LogicApp03 by following the NextPageLink and limiting the result size to two pages.</span></span>
<span data-ttu-id="2446f-122">На каждой странице есть 30 результатов.</span><span class="sxs-lookup"><span data-stu-id="2446f-122">Each page contains thirty results.</span></span>

## <span data-ttu-id="2446f-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2446f-123">PARAMETERS</span></span>

### <span data-ttu-id="2446f-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2446f-124">-DefaultProfile</span></span>
<span data-ttu-id="2446f-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="2446f-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2446f-126">-FollowNextPageLink</span><span class="sxs-lookup"><span data-stu-id="2446f-126">-FollowNextPageLink</span></span>
<span data-ttu-id="2446f-127">Указывает на то, что для cmdlet должны следовать ссылки на следующую страницу.</span><span class="sxs-lookup"><span data-stu-id="2446f-127">Indicates the cmdlet should follow next page links.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: FL

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2446f-128">-MaximumFollowNextPageLink</span><span class="sxs-lookup"><span data-stu-id="2446f-128">-MaximumFollowNextPageLink</span></span>
<span data-ttu-id="2446f-129">Количество ссылок на следующую страницу, если используется FollowNextPageLink.</span><span class="sxs-lookup"><span data-stu-id="2446f-129">Specifies how many times to follow next page links if FollowNextPageLink is used.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: ML

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2446f-130">-Name</span><span class="sxs-lookup"><span data-stu-id="2446f-130">-Name</span></span>
<span data-ttu-id="2446f-131">Имя приложения логики, для которого этот cmdlet получает историю запуска.</span><span class="sxs-lookup"><span data-stu-id="2446f-131">Specifies the name of the logic app for which this cmdlet gets run history.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2446f-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2446f-132">-ResourceGroupName</span></span>
<span data-ttu-id="2446f-133">Имя группы ресурсов, которая содержит приложение логики.</span><span class="sxs-lookup"><span data-stu-id="2446f-133">Specifies the name of a resource group that contains the logic app.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2446f-134">-RunName</span><span class="sxs-lookup"><span data-stu-id="2446f-134">-RunName</span></span>
<span data-ttu-id="2446f-135">Указывает имя запуска приложения логики.</span><span class="sxs-lookup"><span data-stu-id="2446f-135">Specifies the run name of a logic app.</span></span>
<span data-ttu-id="2446f-136">Этот cmdlet возвращает запуск рабочего процесса, который указан этим этим cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2446f-136">This cmdlet gets the workflow run that this cmdlet specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2446f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2446f-137">CommonParameters</span></span>
<span data-ttu-id="2446f-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2446f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2446f-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2446f-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2446f-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2446f-140">INPUTS</span></span>

### <span data-ttu-id="2446f-141">System.String</span><span class="sxs-lookup"><span data-stu-id="2446f-141">System.String</span></span>

## <span data-ttu-id="2446f-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2446f-142">OUTPUTS</span></span>

### <span data-ttu-id="2446f-143">Microsoft.Azure.Management.Logic.Models.WorkflowRun</span><span class="sxs-lookup"><span data-stu-id="2446f-143">Microsoft.Azure.Management.Logic.Models.WorkflowRun</span></span>

## <span data-ttu-id="2446f-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2446f-144">NOTES</span></span>

## <span data-ttu-id="2446f-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2446f-145">RELATED LINKS</span></span>

[<span data-ttu-id="2446f-146">Get-AzLogicAppRunaction</span><span class="sxs-lookup"><span data-stu-id="2446f-146">Get-AzLogicAppRunAction</span></span>](./Get-AzLogicAppRunAction.md)

[<span data-ttu-id="2446f-147">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="2446f-147">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)

[<span data-ttu-id="2446f-148">Stop-AzLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="2446f-148">Stop-AzLogicAppRun</span></span>](./Stop-AzLogicAppRun.md)



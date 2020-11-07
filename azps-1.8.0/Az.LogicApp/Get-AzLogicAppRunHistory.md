---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: F271BCB1-6D43-48E5-BB51-00288F57BFFB
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azlogicapprunhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunHistory.md
ms.openlocfilehash: cff5113c37580b375bbaaea24850d5b55cd110ef
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93899958"
---
# <span data-ttu-id="68526-101">Get-AzLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="68526-101">Get-AzLogicAppRunHistory</span></span>

## <span data-ttu-id="68526-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="68526-102">SYNOPSIS</span></span>
<span data-ttu-id="68526-103">Возвращает историю выполнения приложения логики.</span><span class="sxs-lookup"><span data-stu-id="68526-103">Gets the run history of a logic app.</span></span>

## <span data-ttu-id="68526-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="68526-104">SYNTAX</span></span>

```
Get-AzLogicAppRunHistory -ResourceGroupName <String> -Name <String> [-RunName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="68526-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="68526-105">DESCRIPTION</span></span>
<span data-ttu-id="68526-106">Командлет **Get-AzLogicAppRunHistory** получает историю выполнения приложения логики.</span><span class="sxs-lookup"><span data-stu-id="68526-106">The **Get-AzLogicAppRunHistory** cmdlet gets the run history of a logic app.</span></span>
<span data-ttu-id="68526-107">Этот командлет возвращает коллекцию объектов **WorkflowRun** .</span><span class="sxs-lookup"><span data-stu-id="68526-107">This cmdlet returns a collection of **WorkflowRun** objects.</span></span>
<span data-ttu-id="68526-108">Укажите приложение логики и группу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="68526-108">Specify the logic app and resource group.</span></span>
<span data-ttu-id="68526-109">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="68526-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="68526-110">Чтобы использовать динамический параметр, введите его в командную команду.</span><span class="sxs-lookup"><span data-stu-id="68526-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="68526-111">Чтобы найти имена динамических параметров, введите дефис (-) после имени командлета, а затем несколько раз нажмите клавишу TAB, чтобы просмотреть все доступные параметры.</span><span class="sxs-lookup"><span data-stu-id="68526-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="68526-112">Если вы не пропустите требуемый параметр шаблона, командлет предложит вам указать значение.</span><span class="sxs-lookup"><span data-stu-id="68526-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="68526-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="68526-113">EXAMPLES</span></span>

### <span data-ttu-id="68526-114">Пример 1: получение истории выполнения для логики приложения</span><span class="sxs-lookup"><span data-stu-id="68526-114">Example 1: Get the run history of a logic app</span></span>
```
PS C:\>Get-AzLogicAppActionRunHistory -ResourceGroupName "Resourcegroup11" -Name "LogicApp03"
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

<span data-ttu-id="68526-115">Эта команда получает историю выполнения логического приложения с именем LogicApp03.</span><span class="sxs-lookup"><span data-stu-id="68526-115">This command gets the run history of a logic app named LogicApp03.</span></span>

### <span data-ttu-id="68526-116">Пример 2: запуск приложения логики</span><span class="sxs-lookup"><span data-stu-id="68526-116">Example 2: Get a logic app run</span></span>
```
PS C:\>Get-AzLogicAppActionRunHistory -ResourceGroupName "Resourcegroup11" -Name "LogicApp03" -RunName "08587489104702792076"
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

<span data-ttu-id="68526-117">Эта команда получает конкретное логическое приложение, запущенное для приложения Logic с именем LogicApp03.</span><span class="sxs-lookup"><span data-stu-id="68526-117">This command gets a specific logic app run for the logic app named LogicApp03.</span></span>

## <span data-ttu-id="68526-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="68526-118">PARAMETERS</span></span>

### <span data-ttu-id="68526-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68526-119">-DefaultProfile</span></span>
<span data-ttu-id="68526-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="68526-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="68526-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="68526-121">-Name</span></span>
<span data-ttu-id="68526-122">Указывает имя логического приложения, для которого этот командлет получает журнал выполнения.</span><span class="sxs-lookup"><span data-stu-id="68526-122">Specifies the name of the logic app for which this cmdlet gets run history.</span></span>

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

### <span data-ttu-id="68526-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68526-123">-ResourceGroupName</span></span>
<span data-ttu-id="68526-124">Указывает имя группы ресурсов, которая содержит логическое приложение.</span><span class="sxs-lookup"><span data-stu-id="68526-124">Specifies the name of a resource group that contains the logic app.</span></span>

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

### <span data-ttu-id="68526-125">-RunName</span><span class="sxs-lookup"><span data-stu-id="68526-125">-RunName</span></span>
<span data-ttu-id="68526-126">Указывает имя запуска для логики приложения.</span><span class="sxs-lookup"><span data-stu-id="68526-126">Specifies the run name of a logic app.</span></span>
<span data-ttu-id="68526-127">Этот командлет получает рабочий процесс, который указывает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="68526-127">This cmdlet gets the workflow run that this cmdlet specifies.</span></span>

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

### <span data-ttu-id="68526-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68526-128">CommonParameters</span></span>
<span data-ttu-id="68526-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="68526-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68526-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68526-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68526-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="68526-131">INPUTS</span></span>

### <span data-ttu-id="68526-132">System. String</span><span class="sxs-lookup"><span data-stu-id="68526-132">System.String</span></span>

## <span data-ttu-id="68526-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="68526-133">OUTPUTS</span></span>

### <span data-ttu-id="68526-134">Microsoft. Azure. Management. Logic. Models. WorkflowRun</span><span class="sxs-lookup"><span data-stu-id="68526-134">Microsoft.Azure.Management.Logic.Models.WorkflowRun</span></span>

## <span data-ttu-id="68526-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="68526-135">NOTES</span></span>

## <span data-ttu-id="68526-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="68526-136">RELATED LINKS</span></span>

[<span data-ttu-id="68526-137">Get-AzLogicAppRunAction</span><span class="sxs-lookup"><span data-stu-id="68526-137">Get-AzLogicAppRunAction</span></span>](./Get-AzLogicAppRunAction.md)

[<span data-ttu-id="68526-138">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="68526-138">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)

[<span data-ttu-id="68526-139">Остановить-AzLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="68526-139">Stop-AzLogicAppRun</span></span>](./Stop-AzLogicAppRun.md)



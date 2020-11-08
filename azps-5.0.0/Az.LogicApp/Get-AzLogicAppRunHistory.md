---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: F271BCB1-6D43-48E5-BB51-00288F57BFFB
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azlogicapprunhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunHistory.md
ms.openlocfilehash: de1c40dc7c9f8fefb1a275394b066e8af96de211
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247710"
---
# <span data-ttu-id="285ed-101">Get-AzLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="285ed-101">Get-AzLogicAppRunHistory</span></span>

## <span data-ttu-id="285ed-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="285ed-102">SYNOPSIS</span></span>
<span data-ttu-id="285ed-103">Возвращает историю выполнения приложения логики.</span><span class="sxs-lookup"><span data-stu-id="285ed-103">Gets the run history of a logic app.</span></span>

## <span data-ttu-id="285ed-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="285ed-104">SYNTAX</span></span>

```
Get-AzLogicAppRunHistory -ResourceGroupName <String> -Name <String> [-RunName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="285ed-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="285ed-105">DESCRIPTION</span></span>
<span data-ttu-id="285ed-106">Командлет **Get-AzLogicAppRunHistory** получает историю выполнения приложения логики.</span><span class="sxs-lookup"><span data-stu-id="285ed-106">The **Get-AzLogicAppRunHistory** cmdlet gets the run history of a logic app.</span></span>
<span data-ttu-id="285ed-107">Этот командлет возвращает коллекцию объектов **WorkflowRun** .</span><span class="sxs-lookup"><span data-stu-id="285ed-107">This cmdlet returns a collection of **WorkflowRun** objects.</span></span>
<span data-ttu-id="285ed-108">Укажите приложение логики и группу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="285ed-108">Specify the logic app and resource group.</span></span>
<span data-ttu-id="285ed-109">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="285ed-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="285ed-110">Чтобы использовать динамический параметр, введите его в командную команду.</span><span class="sxs-lookup"><span data-stu-id="285ed-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="285ed-111">Чтобы найти имена динамических параметров, введите дефис (-) после имени командлета, а затем несколько раз нажмите клавишу TAB, чтобы просмотреть все доступные параметры.</span><span class="sxs-lookup"><span data-stu-id="285ed-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="285ed-112">Если вы не пропустите требуемый параметр шаблона, командлет предложит вам указать значение.</span><span class="sxs-lookup"><span data-stu-id="285ed-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="285ed-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="285ed-113">EXAMPLES</span></span>

### <span data-ttu-id="285ed-114">Пример 1: получение истории выполнения для логики приложения</span><span class="sxs-lookup"><span data-stu-id="285ed-114">Example 1: Get the run history of a logic app</span></span>
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

<span data-ttu-id="285ed-115">Эта команда получает историю выполнения логического приложения с именем LogicApp03.</span><span class="sxs-lookup"><span data-stu-id="285ed-115">This command gets the run history of a logic app named LogicApp03.</span></span>

### <span data-ttu-id="285ed-116">Пример 2: запуск приложения логики</span><span class="sxs-lookup"><span data-stu-id="285ed-116">Example 2: Get a logic app run</span></span>
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

<span data-ttu-id="285ed-117">Эта команда получает конкретное логическое приложение, запущенное для приложения Logic с именем LogicApp03.</span><span class="sxs-lookup"><span data-stu-id="285ed-117">This command gets a specific logic app run for the logic app named LogicApp03.</span></span>

### <span data-ttu-id="285ed-118">Пример 3</span><span class="sxs-lookup"><span data-stu-id="285ed-118">Example 3</span></span>

<span data-ttu-id="285ed-119">Эта команда получает историю выполнения логического приложения с именем LogicApp03.</span><span class="sxs-lookup"><span data-stu-id="285ed-119">This command gets the run history of a logic app named LogicApp03.</span></span> <span data-ttu-id="285ed-120">(автоматически сформированные)</span><span class="sxs-lookup"><span data-stu-id="285ed-120">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Get-AzLogicAppRunHistory -Name 'IntegrationAccount31' -ResourceGroupName MyResourceGroup
```

## <span data-ttu-id="285ed-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="285ed-121">PARAMETERS</span></span>

### <span data-ttu-id="285ed-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="285ed-122">-DefaultProfile</span></span>
<span data-ttu-id="285ed-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="285ed-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="285ed-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="285ed-124">-Name</span></span>
<span data-ttu-id="285ed-125">Указывает имя логического приложения, для которого этот командлет получает журнал выполнения.</span><span class="sxs-lookup"><span data-stu-id="285ed-125">Specifies the name of the logic app for which this cmdlet gets run history.</span></span>

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

### <span data-ttu-id="285ed-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="285ed-126">-ResourceGroupName</span></span>
<span data-ttu-id="285ed-127">Указывает имя группы ресурсов, которая содержит логическое приложение.</span><span class="sxs-lookup"><span data-stu-id="285ed-127">Specifies the name of a resource group that contains the logic app.</span></span>

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

### <span data-ttu-id="285ed-128">-RunName</span><span class="sxs-lookup"><span data-stu-id="285ed-128">-RunName</span></span>
<span data-ttu-id="285ed-129">Указывает имя запуска для логики приложения.</span><span class="sxs-lookup"><span data-stu-id="285ed-129">Specifies the run name of a logic app.</span></span>
<span data-ttu-id="285ed-130">Этот командлет получает рабочий процесс, который указывает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="285ed-130">This cmdlet gets the workflow run that this cmdlet specifies.</span></span>

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

### <span data-ttu-id="285ed-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="285ed-131">CommonParameters</span></span>
<span data-ttu-id="285ed-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="285ed-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="285ed-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="285ed-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="285ed-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="285ed-134">INPUTS</span></span>

### <span data-ttu-id="285ed-135">System. String</span><span class="sxs-lookup"><span data-stu-id="285ed-135">System.String</span></span>

## <span data-ttu-id="285ed-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="285ed-136">OUTPUTS</span></span>

### <span data-ttu-id="285ed-137">Microsoft. Azure. Management. Logic. Models. WorkflowRun</span><span class="sxs-lookup"><span data-stu-id="285ed-137">Microsoft.Azure.Management.Logic.Models.WorkflowRun</span></span>

## <span data-ttu-id="285ed-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="285ed-138">NOTES</span></span>

## <span data-ttu-id="285ed-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="285ed-139">RELATED LINKS</span></span>

[<span data-ttu-id="285ed-140">Get-AzLogicAppRunAction</span><span class="sxs-lookup"><span data-stu-id="285ed-140">Get-AzLogicAppRunAction</span></span>](./Get-AzLogicAppRunAction.md)

[<span data-ttu-id="285ed-141">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="285ed-141">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)

[<span data-ttu-id="285ed-142">Остановить-AzLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="285ed-142">Stop-AzLogicAppRun</span></span>](./Stop-AzLogicAppRun.md)



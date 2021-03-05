---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 5307F1F1-E84C-4949-A557-99EF0012C3DF
online version: https://docs.microsoft.com/powershell/module/az.logicapp/get-azlogicapptrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppTrigger.md
ms.openlocfilehash: 28a7cd76f03dd3b6d2fc79e5d0b8d4d963a7f55c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008931"
---
# <span data-ttu-id="18b3e-101">Get-AzLogicAppTrigger</span><span class="sxs-lookup"><span data-stu-id="18b3e-101">Get-AzLogicAppTrigger</span></span>

## <span data-ttu-id="18b3e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18b3e-102">SYNOPSIS</span></span>
<span data-ttu-id="18b3e-103">Получает триггеры приложения логики.</span><span class="sxs-lookup"><span data-stu-id="18b3e-103">Gets the triggers of a logic app.</span></span>

## <span data-ttu-id="18b3e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="18b3e-104">SYNTAX</span></span>

```
Get-AzLogicAppTrigger -ResourceGroupName <String> -Name <String> [-TriggerName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="18b3e-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="18b3e-105">DESCRIPTION</span></span>
<span data-ttu-id="18b3e-106">Из приложения логики триггер **Get-AzLogicAppTrigger** получает триггеры.</span><span class="sxs-lookup"><span data-stu-id="18b3e-106">The **Get-AzLogicAppTrigger** cmdlet gets triggers from a logic app.</span></span>
<span data-ttu-id="18b3e-107">Этот cmdlet возвращает объект **WorkflowTrigger.**</span><span class="sxs-lookup"><span data-stu-id="18b3e-107">This cmdlet returns a **WorkflowTrigger** object.</span></span>
<span data-ttu-id="18b3e-108">Укажите рабочий процесс, группу ресурсов и триггер.</span><span class="sxs-lookup"><span data-stu-id="18b3e-108">Specify the workflow, resource group, and trigger.</span></span>
<span data-ttu-id="18b3e-109">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="18b3e-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="18b3e-110">Чтобы использовать динамический параметр, введите его в команду.</span><span class="sxs-lookup"><span data-stu-id="18b3e-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="18b3e-111">Чтобы найти имена динамических параметров, введите дефис (-) после имени cmdlet, а затем нажимая клавишу TAB для циклическиго перебора доступных параметров.</span><span class="sxs-lookup"><span data-stu-id="18b3e-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="18b3e-112">Если параметр обязательного шаблона не задан, будет выдан запрос на его значение.</span><span class="sxs-lookup"><span data-stu-id="18b3e-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="18b3e-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="18b3e-113">EXAMPLES</span></span>

### <span data-ttu-id="18b3e-114">Пример 1. Запуск триггера приложения логики</span><span class="sxs-lookup"><span data-stu-id="18b3e-114">Example 1: Get a trigger of a logic app</span></span>
```
PS C:\>Get-AzLogicAppTrigger -ResourceGroupName "ResourceGroup11" -Name "LogicApp05" -TriggerName "Trigger01"
ChangedTime         : 1/14/2016 11:45:07 AM
CreatedTime         : 1/13/2016 2:42:26 PM
LastExecutionTime   : 1/14/2016 11:45:07 AM
Name                : Trigger01
NextExecutionTime   : 1/14/2016 12:45:07 PM
RecurrenceFrequency : Minute
RecurrenceInterval  : 60
Status              : Waiting
Type                : Microsoft.Logic/workflows/triggers
LogicAppName        : LogicApp05
LogicAppVersion     : 08587489107406290826
```

<span data-ttu-id="18b3e-115">Эта команда получает триггер Trigger01 из приложения logicApp05.</span><span class="sxs-lookup"><span data-stu-id="18b3e-115">This command gets the trigger named Trigger01 from the logic app named LogicApp05.</span></span>

### <span data-ttu-id="18b3e-116">Пример 2. Все триггеры приложения логики</span><span class="sxs-lookup"><span data-stu-id="18b3e-116">Example 2: Get all triggers of a logic app</span></span>
```
PS C:\>Get-AzLogicAppTrigger -ResourceGroupName "ResourceGroup11" -Name "LogicApp07"
ChangedTime         : 1/14/2016 11:45:07 AM
CreatedTime         : 1/13/2016 2:42:26 PM
LastExecutionTime   : 1/14/2016 11:45:07 AM
Name                : Trigger02
NextExecutionTime   : 1/14/2016 12:45:07 PM
RecurrenceFrequency : Minute
RecurrenceInterval  : 60
Status              : Waiting
Type                : Microsoft.Logic/workflows/triggers
LogicAppName        : LogicApp07
LogicAppVersion     : 08587489107406290826
```

<span data-ttu-id="18b3e-117">Эта команда получает триггеры приложения логики LogicApp07.</span><span class="sxs-lookup"><span data-stu-id="18b3e-117">This command gets the triggers of the logic app named LogicApp07.</span></span>

## <span data-ttu-id="18b3e-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="18b3e-118">PARAMETERS</span></span>

### <span data-ttu-id="18b3e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18b3e-119">-DefaultProfile</span></span>
<span data-ttu-id="18b3e-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="18b3e-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="18b3e-121">-Name</span><span class="sxs-lookup"><span data-stu-id="18b3e-121">-Name</span></span>
<span data-ttu-id="18b3e-122">Указывает имя приложения логики, из которого этот cmdlet получает триггер.</span><span class="sxs-lookup"><span data-stu-id="18b3e-122">Specifies the name of the logic app from which this cmdlet gets a trigger.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18b3e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18b3e-123">-ResourceGroupName</span></span>
<span data-ttu-id="18b3e-124">Определяет имя группы ресурсов, для которой этот cmdlet получает триггер.</span><span class="sxs-lookup"><span data-stu-id="18b3e-124">Specifies the name of a resource group in which this cmdlet gets a trigger.</span></span>

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

### <span data-ttu-id="18b3e-125">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="18b3e-125">-TriggerName</span></span>
<span data-ttu-id="18b3e-126">Указывает имя триггера, который получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="18b3e-126">Specifies the name of the trigger that this cmdlet gets.</span></span>

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

### <span data-ttu-id="18b3e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18b3e-127">CommonParameters</span></span>
<span data-ttu-id="18b3e-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18b3e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18b3e-129">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18b3e-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18b3e-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="18b3e-130">INPUTS</span></span>

### <span data-ttu-id="18b3e-131">System.String</span><span class="sxs-lookup"><span data-stu-id="18b3e-131">System.String</span></span>

## <span data-ttu-id="18b3e-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="18b3e-132">OUTPUTS</span></span>

### <span data-ttu-id="18b3e-133">Microsoft.Azure.Management.Logic.Models.WorkflowTrigger</span><span class="sxs-lookup"><span data-stu-id="18b3e-133">Microsoft.Azure.Management.Logic.Models.WorkflowTrigger</span></span>

## <span data-ttu-id="18b3e-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="18b3e-134">NOTES</span></span>

## <span data-ttu-id="18b3e-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="18b3e-135">RELATED LINKS</span></span>

[<span data-ttu-id="18b3e-136">Get-AzLogicAppTriggerHistory</span><span class="sxs-lookup"><span data-stu-id="18b3e-136">Get-AzLogicAppTriggerHistory</span></span>](./Get-AzLogicAppTriggerHistory.md)

[<span data-ttu-id="18b3e-137">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="18b3e-137">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)



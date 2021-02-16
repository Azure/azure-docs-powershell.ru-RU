---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 5307F1F1-E84C-4949-A557-99EF0012C3DF
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azlogicapptrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppTrigger.md
ms.openlocfilehash: 7061d70ca1f4bc38c9ac8cc12ad75f01a3fed8b7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100219273"
---
# <span data-ttu-id="8096b-101">Get-AzLogicAppTrigger</span><span class="sxs-lookup"><span data-stu-id="8096b-101">Get-AzLogicAppTrigger</span></span>

## <span data-ttu-id="8096b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8096b-102">SYNOPSIS</span></span>
<span data-ttu-id="8096b-103">Получает триггеры приложения логики.</span><span class="sxs-lookup"><span data-stu-id="8096b-103">Gets the triggers of a logic app.</span></span>

## <span data-ttu-id="8096b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8096b-104">SYNTAX</span></span>

```
Get-AzLogicAppTrigger -ResourceGroupName <String> -Name <String> [-TriggerName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8096b-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8096b-105">DESCRIPTION</span></span>
<span data-ttu-id="8096b-106">Из приложения логики триггер **Get-AzLogicAppTrigger** получает триггеры.</span><span class="sxs-lookup"><span data-stu-id="8096b-106">The **Get-AzLogicAppTrigger** cmdlet gets triggers from a logic app.</span></span>
<span data-ttu-id="8096b-107">Этот cmdlet возвращает объект **WorkflowTrigger.**</span><span class="sxs-lookup"><span data-stu-id="8096b-107">This cmdlet returns a **WorkflowTrigger** object.</span></span>
<span data-ttu-id="8096b-108">Укажите рабочий процесс, группу ресурсов и триггер.</span><span class="sxs-lookup"><span data-stu-id="8096b-108">Specify the workflow, resource group, and trigger.</span></span>
<span data-ttu-id="8096b-109">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="8096b-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="8096b-110">Чтобы использовать динамический параметр, введите его в команду.</span><span class="sxs-lookup"><span data-stu-id="8096b-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="8096b-111">Чтобы найти имена динамических параметров, введите дефис (-) после имени cmdlet, а затем нажимая клавишу TAB для циклическиго перебора доступных параметров.</span><span class="sxs-lookup"><span data-stu-id="8096b-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="8096b-112">Если параметр обязательного шаблона не задан, будет выдан запрос на его значение.</span><span class="sxs-lookup"><span data-stu-id="8096b-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="8096b-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8096b-113">EXAMPLES</span></span>

### <span data-ttu-id="8096b-114">Пример 1. Запуск триггера приложения логики</span><span class="sxs-lookup"><span data-stu-id="8096b-114">Example 1: Get a trigger of a logic app</span></span>
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

<span data-ttu-id="8096b-115">Эта команда получает триггер Trigger01 из приложения logicApp05.</span><span class="sxs-lookup"><span data-stu-id="8096b-115">This command gets the trigger named Trigger01 from the logic app named LogicApp05.</span></span>

### <span data-ttu-id="8096b-116">Пример 2. Все триггеры приложения логики</span><span class="sxs-lookup"><span data-stu-id="8096b-116">Example 2: Get all triggers of a logic app</span></span>
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

<span data-ttu-id="8096b-117">Эта команда получает триггеры приложения logicApp07.</span><span class="sxs-lookup"><span data-stu-id="8096b-117">This command gets the triggers of the logic app named LogicApp07.</span></span>

## <span data-ttu-id="8096b-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8096b-118">PARAMETERS</span></span>

### <span data-ttu-id="8096b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8096b-119">-DefaultProfile</span></span>
<span data-ttu-id="8096b-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="8096b-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8096b-121">-Name</span><span class="sxs-lookup"><span data-stu-id="8096b-121">-Name</span></span>
<span data-ttu-id="8096b-122">Указывает имя приложения логики, из которого этот cmdlet получает триггер.</span><span class="sxs-lookup"><span data-stu-id="8096b-122">Specifies the name of the logic app from which this cmdlet gets a trigger.</span></span>

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

### <span data-ttu-id="8096b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8096b-123">-ResourceGroupName</span></span>
<span data-ttu-id="8096b-124">Определяет имя группы ресурсов, для которой этот cmdlet получает триггер.</span><span class="sxs-lookup"><span data-stu-id="8096b-124">Specifies the name of a resource group in which this cmdlet gets a trigger.</span></span>

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

### <span data-ttu-id="8096b-125">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="8096b-125">-TriggerName</span></span>
<span data-ttu-id="8096b-126">Указывает имя триггера, который получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8096b-126">Specifies the name of the trigger that this cmdlet gets.</span></span>

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

### <span data-ttu-id="8096b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8096b-127">CommonParameters</span></span>
<span data-ttu-id="8096b-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8096b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8096b-129">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8096b-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8096b-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8096b-130">INPUTS</span></span>

### <span data-ttu-id="8096b-131">System.String</span><span class="sxs-lookup"><span data-stu-id="8096b-131">System.String</span></span>

## <span data-ttu-id="8096b-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8096b-132">OUTPUTS</span></span>

### <span data-ttu-id="8096b-133">Microsoft.Azure.Management.Logic.Models.WorkflowTrigger</span><span class="sxs-lookup"><span data-stu-id="8096b-133">Microsoft.Azure.Management.Logic.Models.WorkflowTrigger</span></span>

## <span data-ttu-id="8096b-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8096b-134">NOTES</span></span>

## <span data-ttu-id="8096b-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8096b-135">RELATED LINKS</span></span>

[<span data-ttu-id="8096b-136">Get-AzLogicAppTriggerHistory</span><span class="sxs-lookup"><span data-stu-id="8096b-136">Get-AzLogicAppTriggerHistory</span></span>](./Get-AzLogicAppTriggerHistory.md)

[<span data-ttu-id="8096b-137">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="8096b-137">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)



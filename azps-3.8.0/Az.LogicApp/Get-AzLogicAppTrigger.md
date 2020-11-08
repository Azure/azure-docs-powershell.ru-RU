---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 5307F1F1-E84C-4949-A557-99EF0012C3DF
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azlogicapptrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppTrigger.md
ms.openlocfilehash: 7061d70ca1f4bc38c9ac8cc12ad75f01a3fed8b7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074357"
---
# <span data-ttu-id="a31be-101">Get-AzLogicAppTrigger</span><span class="sxs-lookup"><span data-stu-id="a31be-101">Get-AzLogicAppTrigger</span></span>

## <span data-ttu-id="a31be-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a31be-102">SYNOPSIS</span></span>
<span data-ttu-id="a31be-103">Возвращает триггеры для приложения логики.</span><span class="sxs-lookup"><span data-stu-id="a31be-103">Gets the triggers of a logic app.</span></span>

## <span data-ttu-id="a31be-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a31be-104">SYNTAX</span></span>

```
Get-AzLogicAppTrigger -ResourceGroupName <String> -Name <String> [-TriggerName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a31be-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a31be-105">DESCRIPTION</span></span>
<span data-ttu-id="a31be-106">Командлет **Get-AzLogicAppTrigger** получает триггеры из приложения логики.</span><span class="sxs-lookup"><span data-stu-id="a31be-106">The **Get-AzLogicAppTrigger** cmdlet gets triggers from a logic app.</span></span>
<span data-ttu-id="a31be-107">Этот командлет возвращает объект **WorkflowTrigger** .</span><span class="sxs-lookup"><span data-stu-id="a31be-107">This cmdlet returns a **WorkflowTrigger** object.</span></span>
<span data-ttu-id="a31be-108">Укажите рабочий процесс, группу ресурсов и триггер.</span><span class="sxs-lookup"><span data-stu-id="a31be-108">Specify the workflow, resource group, and trigger.</span></span>
<span data-ttu-id="a31be-109">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="a31be-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="a31be-110">Чтобы использовать динамический параметр, введите его в командную команду.</span><span class="sxs-lookup"><span data-stu-id="a31be-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="a31be-111">Чтобы найти имена динамических параметров, введите дефис (-) после имени командлета, а затем несколько раз нажмите клавишу TAB, чтобы просмотреть все доступные параметры.</span><span class="sxs-lookup"><span data-stu-id="a31be-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="a31be-112">Если вы не пропустите требуемый параметр шаблона, командлет предложит вам указать значение.</span><span class="sxs-lookup"><span data-stu-id="a31be-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="a31be-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a31be-113">EXAMPLES</span></span>

### <span data-ttu-id="a31be-114">Пример 1: получение триггера для приложения логики</span><span class="sxs-lookup"><span data-stu-id="a31be-114">Example 1: Get a trigger of a logic app</span></span>
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

<span data-ttu-id="a31be-115">Эта команда получает триггер с именем Trigger01 из приложения Logic с именем LogicApp05.</span><span class="sxs-lookup"><span data-stu-id="a31be-115">This command gets the trigger named Trigger01 from the logic app named LogicApp05.</span></span>

### <span data-ttu-id="a31be-116">Пример 2: получение всех триггеров для логики приложения</span><span class="sxs-lookup"><span data-stu-id="a31be-116">Example 2: Get all triggers of a logic app</span></span>
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

<span data-ttu-id="a31be-117">Эта команда получает триггеры приложения логики с именем LogicApp07.</span><span class="sxs-lookup"><span data-stu-id="a31be-117">This command gets the triggers of the logic app named LogicApp07.</span></span>

## <span data-ttu-id="a31be-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a31be-118">PARAMETERS</span></span>

### <span data-ttu-id="a31be-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a31be-119">-DefaultProfile</span></span>
<span data-ttu-id="a31be-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="a31be-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a31be-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a31be-121">-Name</span></span>
<span data-ttu-id="a31be-122">Указывает имя приложения логики, из которого этот командлет получает триггер.</span><span class="sxs-lookup"><span data-stu-id="a31be-122">Specifies the name of the logic app from which this cmdlet gets a trigger.</span></span>

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

### <span data-ttu-id="a31be-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a31be-123">-ResourceGroupName</span></span>
<span data-ttu-id="a31be-124">Указывает имя группы ресурсов, в которой этот командлет получает триггер.</span><span class="sxs-lookup"><span data-stu-id="a31be-124">Specifies the name of a resource group in which this cmdlet gets a trigger.</span></span>

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

### <span data-ttu-id="a31be-125">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="a31be-125">-TriggerName</span></span>
<span data-ttu-id="a31be-126">Указывает имя триггера, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="a31be-126">Specifies the name of the trigger that this cmdlet gets.</span></span>

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

### <span data-ttu-id="a31be-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a31be-127">CommonParameters</span></span>
<span data-ttu-id="a31be-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a31be-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a31be-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a31be-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a31be-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a31be-130">INPUTS</span></span>

### <span data-ttu-id="a31be-131">System. String</span><span class="sxs-lookup"><span data-stu-id="a31be-131">System.String</span></span>

## <span data-ttu-id="a31be-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a31be-132">OUTPUTS</span></span>

### <span data-ttu-id="a31be-133">Microsoft. Azure. Management. Logic. Models. WorkflowTrigger</span><span class="sxs-lookup"><span data-stu-id="a31be-133">Microsoft.Azure.Management.Logic.Models.WorkflowTrigger</span></span>

## <span data-ttu-id="a31be-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="a31be-134">NOTES</span></span>

## <span data-ttu-id="a31be-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a31be-135">RELATED LINKS</span></span>

[<span data-ttu-id="a31be-136">Get-AzLogicAppTriggerHistory</span><span class="sxs-lookup"><span data-stu-id="a31be-136">Get-AzLogicAppTriggerHistory</span></span>](./Get-AzLogicAppTriggerHistory.md)

[<span data-ttu-id="a31be-137">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="a31be-137">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)



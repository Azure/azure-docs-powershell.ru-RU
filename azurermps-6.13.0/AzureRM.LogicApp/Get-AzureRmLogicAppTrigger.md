---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 5307F1F1-E84C-4949-A557-99EF0012C3DF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/get-azurermlogicapptrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicAppTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicAppTrigger.md
ms.openlocfilehash: 6066a08774be9f5e3fa67a07b0d868947384f518
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568513"
---
# <span data-ttu-id="1ea39-101">Get-AzureRmLogicAppTrigger</span><span class="sxs-lookup"><span data-stu-id="1ea39-101">Get-AzureRmLogicAppTrigger</span></span>

## <span data-ttu-id="1ea39-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1ea39-102">SYNOPSIS</span></span>
<span data-ttu-id="1ea39-103">Возвращает триггеры для приложения логики.</span><span class="sxs-lookup"><span data-stu-id="1ea39-103">Gets the triggers of a logic app.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1ea39-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1ea39-104">SYNTAX</span></span>

```
Get-AzureRmLogicAppTrigger -ResourceGroupName <String> -Name <String> [-TriggerName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1ea39-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1ea39-105">DESCRIPTION</span></span>
<span data-ttu-id="1ea39-106">Командлет **Get-AzureRmLogicAppTrigger** получает триггеры из приложения логики.</span><span class="sxs-lookup"><span data-stu-id="1ea39-106">The **Get-AzureRmLogicAppTrigger** cmdlet gets triggers from a logic app.</span></span>
<span data-ttu-id="1ea39-107">Этот командлет возвращает объект **WorkflowTrigger** .</span><span class="sxs-lookup"><span data-stu-id="1ea39-107">This cmdlet returns a **WorkflowTrigger** object.</span></span>
<span data-ttu-id="1ea39-108">Укажите рабочий процесс, группу ресурсов и триггер.</span><span class="sxs-lookup"><span data-stu-id="1ea39-108">Specify the workflow, resource group, and trigger.</span></span>
<span data-ttu-id="1ea39-109">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="1ea39-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="1ea39-110">Чтобы использовать динамический параметр, введите его в командную команду.</span><span class="sxs-lookup"><span data-stu-id="1ea39-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="1ea39-111">Чтобы найти имена динамических параметров, введите дефис (-) после имени командлета, а затем несколько раз нажмите клавишу TAB, чтобы просмотреть все доступные параметры.</span><span class="sxs-lookup"><span data-stu-id="1ea39-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="1ea39-112">Если вы не пропустите требуемый параметр шаблона, командлет предложит вам указать значение.</span><span class="sxs-lookup"><span data-stu-id="1ea39-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="1ea39-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1ea39-113">EXAMPLES</span></span>

### <span data-ttu-id="1ea39-114">Пример 1: получение триггера для приложения логики</span><span class="sxs-lookup"><span data-stu-id="1ea39-114">Example 1: Get a trigger of a logic app</span></span>
```
PS C:\>Get-AzureRmLogicAppTrigger -ResourceGroupName "ResourceGroup11" -Name "LogicApp05" -TriggerName "Trigger01"
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

<span data-ttu-id="1ea39-115">Эта команда получает триггер с именем Trigger01 из приложения Logic с именем LogicApp05.</span><span class="sxs-lookup"><span data-stu-id="1ea39-115">This command gets the trigger named Trigger01 from the logic app named LogicApp05.</span></span>

### <span data-ttu-id="1ea39-116">Пример 2: получение всех триггеров для логики приложения</span><span class="sxs-lookup"><span data-stu-id="1ea39-116">Example 2: Get all triggers of a logic app</span></span>
```
PS C:\>Get-AzureRmLogicAppTrigger -ResourceGroupName "ResourceGroup11" -Name "LogicApp07"
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

<span data-ttu-id="1ea39-117">Эта команда получает триггеры приложения логики с именем LogicApp07.</span><span class="sxs-lookup"><span data-stu-id="1ea39-117">This command gets the triggers of the logic app named LogicApp07.</span></span>

## <span data-ttu-id="1ea39-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1ea39-118">PARAMETERS</span></span>

### <span data-ttu-id="1ea39-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ea39-119">-DefaultProfile</span></span>
<span data-ttu-id="1ea39-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="1ea39-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ea39-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1ea39-121">-Name</span></span>
<span data-ttu-id="1ea39-122">Указывает имя приложения логики, из которого этот командлет получает триггер.</span><span class="sxs-lookup"><span data-stu-id="1ea39-122">Specifies the name of the logic app from which this cmdlet gets a trigger.</span></span>

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

### <span data-ttu-id="1ea39-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ea39-123">-ResourceGroupName</span></span>
<span data-ttu-id="1ea39-124">Указывает имя группы ресурсов, в которой этот командлет получает триггер.</span><span class="sxs-lookup"><span data-stu-id="1ea39-124">Specifies the name of a resource group in which this cmdlet gets a trigger.</span></span>

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

### <span data-ttu-id="1ea39-125">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="1ea39-125">-TriggerName</span></span>
<span data-ttu-id="1ea39-126">Указывает имя триггера, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="1ea39-126">Specifies the name of the trigger that this cmdlet gets.</span></span>

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

### <span data-ttu-id="1ea39-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ea39-127">CommonParameters</span></span>
<span data-ttu-id="1ea39-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1ea39-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ea39-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ea39-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ea39-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1ea39-130">INPUTS</span></span>

### <span data-ttu-id="1ea39-131">System. String</span><span class="sxs-lookup"><span data-stu-id="1ea39-131">System.String</span></span>

## <span data-ttu-id="1ea39-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1ea39-132">OUTPUTS</span></span>

### <span data-ttu-id="1ea39-133">Microsoft. Azure. Management. Logic. Models. WorkflowTrigger</span><span class="sxs-lookup"><span data-stu-id="1ea39-133">Microsoft.Azure.Management.Logic.Models.WorkflowTrigger</span></span>

## <span data-ttu-id="1ea39-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="1ea39-134">NOTES</span></span>

## <span data-ttu-id="1ea39-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1ea39-135">RELATED LINKS</span></span>

[<span data-ttu-id="1ea39-136">Get-AzureRmLogicAppTriggerHistory</span><span class="sxs-lookup"><span data-stu-id="1ea39-136">Get-AzureRmLogicAppTriggerHistory</span></span>](./Get-AzureRmLogicAppTriggerHistory.md)

[<span data-ttu-id="1ea39-137">Start-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="1ea39-137">Start-AzureRmLogicApp</span></span>](./Start-AzureRmLogicApp.md)



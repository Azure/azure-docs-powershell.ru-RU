---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 2EA28B90-4BAE-45DF-BD2E-60C74F53FB7B
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azlogicapprunaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunAction.md
ms.openlocfilehash: 8aae52b52edbdbb456e9332fa96d1f1f78dac266
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912215"
---
# <span data-ttu-id="e30e1-101">Get-AzLogicAppRunAction</span><span class="sxs-lookup"><span data-stu-id="e30e1-101">Get-AzLogicAppRunAction</span></span>

## <span data-ttu-id="e30e1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e30e1-102">SYNOPSIS</span></span>
<span data-ttu-id="e30e1-103">Возвращает действие, выполняемое логическим приложением.</span><span class="sxs-lookup"><span data-stu-id="e30e1-103">Gets an action from a logic app run.</span></span>

## <span data-ttu-id="e30e1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e30e1-104">SYNTAX</span></span>

```
Get-AzLogicAppRunAction -ResourceGroupName <String> -Name <String> -RunName <String> [-ActionName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e30e1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e30e1-105">DESCRIPTION</span></span>
<span data-ttu-id="e30e1-106">Командлет **Get-AzLogicAppRunAction** Возвращает действие, выполняемое логическим приложением.</span><span class="sxs-lookup"><span data-stu-id="e30e1-106">The **Get-AzLogicAppRunAction** cmdlet gets an action from a logic app run.</span></span>
<span data-ttu-id="e30e1-107">Этот командлет возвращает объекты **WorkflowRunAction** .</span><span class="sxs-lookup"><span data-stu-id="e30e1-107">This cmdlet returns a **WorkflowRunAction** objects.</span></span>
<span data-ttu-id="e30e1-108">Укажите логическое приложение, группу ресурсов и запуск.</span><span class="sxs-lookup"><span data-stu-id="e30e1-108">Specify the logic app, resource group, and run.</span></span>
<span data-ttu-id="e30e1-109">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="e30e1-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="e30e1-110">Чтобы использовать динамический параметр, введите его в командную команду.</span><span class="sxs-lookup"><span data-stu-id="e30e1-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="e30e1-111">Чтобы найти имена динамических параметров, введите дефис (-) после имени командлета, а затем несколько раз нажмите клавишу TAB, чтобы просмотреть все доступные параметры.</span><span class="sxs-lookup"><span data-stu-id="e30e1-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="e30e1-112">Если вы не пропустите требуемый параметр шаблона, командлет предложит вам указать значение.</span><span class="sxs-lookup"><span data-stu-id="e30e1-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="e30e1-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e30e1-113">EXAMPLES</span></span>

### <span data-ttu-id="e30e1-114">Пример 1: получение действия из приложения логики выполнение</span><span class="sxs-lookup"><span data-stu-id="e30e1-114">Example 1: Get an action from a Logic App run</span></span>
```
PS C:\>Get-AzLogicAppActionRun -ResourceGroupName "ResourceGroup11" -Name "LogicApp05" -RunName "LogicAppRun56" -ActionName "LogicAppAction01"
Code        : NotFound
EndTime     : 1/13/2016 2:42:56 PM
Error       : 
InputsLink  : Microsoft.Azure.Management.Logic.Models.ContentLink
Name        : LogicAppAction01
OutputsLink : Microsoft.Azure.Management.Logic.Models.ContentLink
StartTime   : 1/13/2016 2:42:55 PM
Status      : Failed
TrackingId  : 
Type        :
```

<span data-ttu-id="e30e1-115">Эта команда получает определенное логическое действие приложения из приложения Logic с именем LogicApp05 для запуска с именем LogicAppRun56.</span><span class="sxs-lookup"><span data-stu-id="e30e1-115">This command gets a specific Logic App action from the logic app named LogicApp05 for the run named LogicAppRun56.</span></span>

### <span data-ttu-id="e30e1-116">Пример 2: получение всех действий из приложения логики выполнение</span><span class="sxs-lookup"><span data-stu-id="e30e1-116">Example 2: Get all the actions from a Logic App run</span></span>
```
PS C:\>Get-AzLogicAppActionRun -ResourceGroupName "ResourceGroup11" -Name "LogicApp05" -RunName "LogicAppRun56"
Code        : NotFound
EndTime     : 1/13/2016 2:42:56 PM
Error       : 
InputsLink  : Microsoft.Azure.Management.Logic.Models.ContentLink
Name        : LogicAppAction1
OutputsLink : Microsoft.Azure.Management.Logic.Models.ContentLink
StartTime   : 1/13/2016 2:42:55 PM
Status      : Failed
TrackingId  : 
Type        :
```

<span data-ttu-id="e30e1-117">Эта команда получает все логические действия приложения из запуска с именем LogicAppRun56 из приложения Logic с именем LogicApp05.</span><span class="sxs-lookup"><span data-stu-id="e30e1-117">This command gets all Logic App actions from a run named LogicAppRun56 of a logic app named LogicApp05.</span></span>

## <span data-ttu-id="e30e1-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e30e1-118">PARAMETERS</span></span>

### <span data-ttu-id="e30e1-119">-Имямакрокоманды</span><span class="sxs-lookup"><span data-stu-id="e30e1-119">-ActionName</span></span>
<span data-ttu-id="e30e1-120">Указывает имя действия в логическом запуске приложения.</span><span class="sxs-lookup"><span data-stu-id="e30e1-120">Specifies the name of an action in a logic app run.</span></span>
<span data-ttu-id="e30e1-121">Этот командлет получает действие, которое указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="e30e1-121">This cmdlet gets the action that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e30e1-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e30e1-122">-DefaultProfile</span></span>
<span data-ttu-id="e30e1-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="e30e1-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e30e1-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e30e1-124">-Name</span></span>
<span data-ttu-id="e30e1-125">Указывает имя приложения логики, для которого этот командлет получает действие.</span><span class="sxs-lookup"><span data-stu-id="e30e1-125">Specifies the name of a logic app for which this cmdlet gets an action.</span></span>

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

### <span data-ttu-id="e30e1-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e30e1-126">-ResourceGroupName</span></span>
<span data-ttu-id="e30e1-127">Указывает имя группы ресурсов, в которой этот командлет получает действие.</span><span class="sxs-lookup"><span data-stu-id="e30e1-127">Specifies the name of a resource group in which this cmdlet gets an action.</span></span>

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

### <span data-ttu-id="e30e1-128">-RunName</span><span class="sxs-lookup"><span data-stu-id="e30e1-128">-RunName</span></span>
<span data-ttu-id="e30e1-129">Указывает имя запуска логики приложения.</span><span class="sxs-lookup"><span data-stu-id="e30e1-129">Specifies the name of a run of a logic app.</span></span>
<span data-ttu-id="e30e1-130">Этот командлет получает действие для выполнения, которое указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="e30e1-130">This cmdlet gets an action for the run that this parameter specifies.</span></span>

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

### <span data-ttu-id="e30e1-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e30e1-131">CommonParameters</span></span>
<span data-ttu-id="e30e1-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e30e1-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e30e1-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e30e1-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e30e1-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e30e1-134">INPUTS</span></span>

### <span data-ttu-id="e30e1-135">System. String</span><span class="sxs-lookup"><span data-stu-id="e30e1-135">System.String</span></span>

## <span data-ttu-id="e30e1-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e30e1-136">OUTPUTS</span></span>

### <span data-ttu-id="e30e1-137">Microsoft. Azure. Management. Logic. Models. WorkflowRunAction</span><span class="sxs-lookup"><span data-stu-id="e30e1-137">Microsoft.Azure.Management.Logic.Models.WorkflowRunAction</span></span>

## <span data-ttu-id="e30e1-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="e30e1-138">NOTES</span></span>

## <span data-ttu-id="e30e1-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e30e1-139">RELATED LINKS</span></span>

[<span data-ttu-id="e30e1-140">Get-AzLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="e30e1-140">Get-AzLogicAppRunHistory</span></span>](./Get-AzLogicAppRunHistory.md)

[<span data-ttu-id="e30e1-141">Остановить-AzLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="e30e1-141">Stop-AzLogicAppRun</span></span>](./Stop-AzLogicAppRun.md)



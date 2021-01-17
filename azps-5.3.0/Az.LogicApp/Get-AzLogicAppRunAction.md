---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 2EA28B90-4BAE-45DF-BD2E-60C74F53FB7B
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azlogicapprunaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunAction.md
ms.openlocfilehash: c382b4bb9a02150beaa6880fd88d8f7b376b7c34
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98425780"
---
# <span data-ttu-id="c4899-101">Get-AzLogicAppRunAction</span><span class="sxs-lookup"><span data-stu-id="c4899-101">Get-AzLogicAppRunAction</span></span>

## <span data-ttu-id="c4899-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4899-102">SYNOPSIS</span></span>
<span data-ttu-id="c4899-103">Получает действие из логического приложения.</span><span class="sxs-lookup"><span data-stu-id="c4899-103">Gets an action from a logic app run.</span></span>

## <span data-ttu-id="c4899-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c4899-104">SYNTAX</span></span>

```
Get-AzLogicAppRunAction -ResourceGroupName <String> -Name <String> -RunName <String> [-ActionName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c4899-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c4899-105">DESCRIPTION</span></span>
<span data-ttu-id="c4899-106">Из логики запуска приложения можно получить действие с помощью cmdlet **Get-AzLogicAppRunAction.**</span><span class="sxs-lookup"><span data-stu-id="c4899-106">The **Get-AzLogicAppRunAction** cmdlet gets an action from a logic app run.</span></span>
<span data-ttu-id="c4899-107">Этот cmdlet возвращает **объекты WorkflowRunAction.**</span><span class="sxs-lookup"><span data-stu-id="c4899-107">This cmdlet returns a **WorkflowRunAction** objects.</span></span>
<span data-ttu-id="c4899-108">Укажите приложение логики, группу ресурсов и запустите его.</span><span class="sxs-lookup"><span data-stu-id="c4899-108">Specify the logic app, resource group, and run.</span></span>
<span data-ttu-id="c4899-109">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="c4899-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="c4899-110">Чтобы использовать динамический параметр, введите его в команду.</span><span class="sxs-lookup"><span data-stu-id="c4899-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="c4899-111">Чтобы найти имена динамических параметров, введите дефис (-) после имени cmdlet, а затем нажимая клавишу TAB для циклическиго перебора доступных параметров.</span><span class="sxs-lookup"><span data-stu-id="c4899-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="c4899-112">Если параметр обязательного шаблона не задан, будет выдан запрос на его значение.</span><span class="sxs-lookup"><span data-stu-id="c4899-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="c4899-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c4899-113">EXAMPLES</span></span>

### <span data-ttu-id="c4899-114">Пример 1. Получите действие из запуска приложения Logic</span><span class="sxs-lookup"><span data-stu-id="c4899-114">Example 1: Get an action from a Logic App run</span></span>
```powershell
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

<span data-ttu-id="c4899-115">Эта команда получает определенное действие Logic App в приложении LogicApp05 для запуска LogicAppRun56.</span><span class="sxs-lookup"><span data-stu-id="c4899-115">This command gets a specific Logic App action from the logic app named LogicApp05 for the run named LogicAppRun56.</span></span>

### <span data-ttu-id="c4899-116">Пример 2. Все действия из приложения Logic</span><span class="sxs-lookup"><span data-stu-id="c4899-116">Example 2: Get all the actions from a Logic App run</span></span>
```powershell
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

<span data-ttu-id="c4899-117">Эта команда получает все действия приложения Logic из запуска LogicAppRun56 логического приложения LogicApp05.</span><span class="sxs-lookup"><span data-stu-id="c4899-117">This command gets all Logic App actions from a run named LogicAppRun56 of a logic app named LogicApp05.</span></span>

### <span data-ttu-id="c4899-118">Пример 3</span><span class="sxs-lookup"><span data-stu-id="c4899-118">Example 3</span></span>

<span data-ttu-id="c4899-119">Эта команда получает все действия приложения Logic из запуска LogicAppRun56 логического приложения LogicApp05.</span><span class="sxs-lookup"><span data-stu-id="c4899-119">This command gets all Logic App actions from a run named LogicAppRun56 of a logic app named LogicApp05.</span></span> <span data-ttu-id="c4899-120">(autogenerated)</span><span class="sxs-lookup"><span data-stu-id="c4899-120">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Get-AzLogicAppRunAction -Name 'IntegrationAccount31' -ResourceGroupName MyResourceGroup -RunName '08587489104702792076'
```

## <span data-ttu-id="c4899-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c4899-121">PARAMETERS</span></span>

### <span data-ttu-id="c4899-122">-ActionName</span><span class="sxs-lookup"><span data-stu-id="c4899-122">-ActionName</span></span>
<span data-ttu-id="c4899-123">Указывает имя действия в запуске логического приложения.</span><span class="sxs-lookup"><span data-stu-id="c4899-123">Specifies the name of an action in a logic app run.</span></span>
<span data-ttu-id="c4899-124">Этот cmdlet получает действие, указанное этим параметром.</span><span class="sxs-lookup"><span data-stu-id="c4899-124">This cmdlet gets the action that this parameter specifies.</span></span>

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

### <span data-ttu-id="c4899-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4899-125">-DefaultProfile</span></span>
<span data-ttu-id="c4899-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="c4899-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c4899-127">-Name</span><span class="sxs-lookup"><span data-stu-id="c4899-127">-Name</span></span>
<span data-ttu-id="c4899-128">Указывает имя приложения-логики, для которого этот cmdlet получает действие.</span><span class="sxs-lookup"><span data-stu-id="c4899-128">Specifies the name of a logic app for which this cmdlet gets an action.</span></span>

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

### <span data-ttu-id="c4899-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4899-129">-ResourceGroupName</span></span>
<span data-ttu-id="c4899-130">Указывает имя группы ресурсов, в которой этот cmdlet получает действие.</span><span class="sxs-lookup"><span data-stu-id="c4899-130">Specifies the name of a resource group in which this cmdlet gets an action.</span></span>

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

### <span data-ttu-id="c4899-131">-RunName</span><span class="sxs-lookup"><span data-stu-id="c4899-131">-RunName</span></span>
<span data-ttu-id="c4899-132">Указывает имя запуска приложения логики.</span><span class="sxs-lookup"><span data-stu-id="c4899-132">Specifies the name of a run of a logic app.</span></span>
<span data-ttu-id="c4899-133">Этот cmdlet получает действие для запуска, указанное этим параметром.</span><span class="sxs-lookup"><span data-stu-id="c4899-133">This cmdlet gets an action for the run that this parameter specifies.</span></span>

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

### <span data-ttu-id="c4899-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4899-134">CommonParameters</span></span>
<span data-ttu-id="c4899-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4899-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4899-136">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4899-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4899-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c4899-137">INPUTS</span></span>

### <span data-ttu-id="c4899-138">System.String</span><span class="sxs-lookup"><span data-stu-id="c4899-138">System.String</span></span>

## <span data-ttu-id="c4899-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c4899-139">OUTPUTS</span></span>

### <span data-ttu-id="c4899-140">Microsoft.Azure.Management.Logic.Models.WorkflowRunAction</span><span class="sxs-lookup"><span data-stu-id="c4899-140">Microsoft.Azure.Management.Logic.Models.WorkflowRunAction</span></span>

## <span data-ttu-id="c4899-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c4899-141">NOTES</span></span>

## <span data-ttu-id="c4899-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c4899-142">RELATED LINKS</span></span>

[<span data-ttu-id="c4899-143">Get-AzLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="c4899-143">Get-AzLogicAppRunHistory</span></span>](./Get-AzLogicAppRunHistory.md)

[<span data-ttu-id="c4899-144">Stop-AzLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="c4899-144">Stop-AzLogicAppRun</span></span>](./Stop-AzLogicAppRun.md)



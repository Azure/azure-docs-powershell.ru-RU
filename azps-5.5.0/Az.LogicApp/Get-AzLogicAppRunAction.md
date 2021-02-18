---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 2EA28B90-4BAE-45DF-BD2E-60C74F53FB7B
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azlogicapprunaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunAction.md
ms.openlocfilehash: 175667480977e55cc93486f252a8f84080c64b5e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100214436"
---
# <span data-ttu-id="7291d-101">Get-AzLogicAppRunAction</span><span class="sxs-lookup"><span data-stu-id="7291d-101">Get-AzLogicAppRunAction</span></span>

## <span data-ttu-id="7291d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7291d-102">SYNOPSIS</span></span>

<span data-ttu-id="7291d-103">Получает действие из запуска логического приложения.</span><span class="sxs-lookup"><span data-stu-id="7291d-103">Gets an action from a logic app run.</span></span>

## <span data-ttu-id="7291d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7291d-104">SYNTAX</span></span>

```powershell
Get-AzLogicAppRunAction -ResourceGroupName <String> -Name <String> -RunName <String> [-ActionName <String>]
 [-FollowNextPageLink] [-MaximumFollowNextPageLink <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7291d-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7291d-105">DESCRIPTION</span></span>

<span data-ttu-id="7291d-106">Из логики запуска приложения можно получить действие с помощью cmdlet **Get-AzLogicAppRunAction.**</span><span class="sxs-lookup"><span data-stu-id="7291d-106">The **Get-AzLogicAppRunAction** cmdlet gets an action from a logic app run.</span></span>
<span data-ttu-id="7291d-107">Этот cmdlet возвращает **объекты WorkflowRunAction.**</span><span class="sxs-lookup"><span data-stu-id="7291d-107">This cmdlet returns a **WorkflowRunAction** objects.</span></span>
<span data-ttu-id="7291d-108">Укажите приложение логики, группу ресурсов и запустите его.</span><span class="sxs-lookup"><span data-stu-id="7291d-108">Specify the logic app, resource group, and run.</span></span>
<span data-ttu-id="7291d-109">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="7291d-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="7291d-110">Чтобы использовать динамический параметр, введите его в команду.</span><span class="sxs-lookup"><span data-stu-id="7291d-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="7291d-111">Чтобы найти имена динамических параметров, введите дефис (-) после имени cmdlet, а затем нажимая клавишу TAB для циклическиго перебора доступных параметров.</span><span class="sxs-lookup"><span data-stu-id="7291d-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="7291d-112">Если не задан параметр обязательного шаблона, будет выдан запрос на его значение.</span><span class="sxs-lookup"><span data-stu-id="7291d-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="7291d-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7291d-113">EXAMPLES</span></span>

### <span data-ttu-id="7291d-114">Пример 1. Получите действие из запуска приложения Logic</span><span class="sxs-lookup"><span data-stu-id="7291d-114">Example 1: Get an action from a Logic App run</span></span>

```powershell
PS C:\>Get-AzLogicAppRunAction -ResourceGroupName "ResourceGroup11" -Name "LogicApp05" -RunName "08585925184423369718380498702CU26" -ActionName "LogicAppAction01"
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

<span data-ttu-id="7291d-115">Эта команда получает определенное действие Logic App из приложения LogicApp05 для запуска с идентификатором 0858592518423369718380498702CU26.</span><span class="sxs-lookup"><span data-stu-id="7291d-115">This command gets a specific Logic App action from the logic app named LogicApp05 for the run with identifier 08585925184423369718380498702CU26.</span></span>

### <span data-ttu-id="7291d-116">Пример 2. Все действия из приложения Logic</span><span class="sxs-lookup"><span data-stu-id="7291d-116">Example 2: Get all the actions from a Logic App run</span></span>

```powershell
PS C:\>Get-AzLogicAppRunAction -ResourceGroupName "ResourceGroup11" -Name "LogicApp05" -RunName "08585925184423369718380498702CU26" -FollowNextPageLink
```

<span data-ttu-id="7291d-117">Эта команда получает все действия приложения Logic из запуска с идентификатором 0858592518423369718380498702CU26 логического приложения LogicApp05.</span><span class="sxs-lookup"><span data-stu-id="7291d-117">This command gets all Logic App actions from a run with identifier 08585925184423369718380498702CU26 of a logic app named LogicApp05.</span></span>

## <span data-ttu-id="7291d-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7291d-118">PARAMETERS</span></span>

### <span data-ttu-id="7291d-119">-ActionName</span><span class="sxs-lookup"><span data-stu-id="7291d-119">-ActionName</span></span>

<span data-ttu-id="7291d-120">Указывает имя действия в запуске логического приложения.</span><span class="sxs-lookup"><span data-stu-id="7291d-120">Specifies the name of an action in a logic app run.</span></span>
<span data-ttu-id="7291d-121">Этот cmdlet получает действие, указанное этим параметром.</span><span class="sxs-lookup"><span data-stu-id="7291d-121">This cmdlet gets the action that this parameter specifies.</span></span>

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

### <span data-ttu-id="7291d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7291d-122">-DefaultProfile</span></span>

<span data-ttu-id="7291d-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="7291d-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7291d-124">-FollowNextPageLink</span><span class="sxs-lookup"><span data-stu-id="7291d-124">-FollowNextPageLink</span></span>

<span data-ttu-id="7291d-125">Указывает на то, что для cmdlet следует использовать ссылки на следующую страницу.</span><span class="sxs-lookup"><span data-stu-id="7291d-125">Indicates the cmdlet should follow next page links.</span></span>

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

### <span data-ttu-id="7291d-126">-MaximumFollowNextPageLink</span><span class="sxs-lookup"><span data-stu-id="7291d-126">-MaximumFollowNextPageLink</span></span>

<span data-ttu-id="7291d-127">Количество ссылок на следующую страницу, если используется FollowNextPageLink.</span><span class="sxs-lookup"><span data-stu-id="7291d-127">Specifies how many times to follow next page links if FollowNextPageLink is used.</span></span>

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

### <span data-ttu-id="7291d-128">-Name</span><span class="sxs-lookup"><span data-stu-id="7291d-128">-Name</span></span>

<span data-ttu-id="7291d-129">Указывает имя приложения логики, для которого этот cmdlet получает действие.</span><span class="sxs-lookup"><span data-stu-id="7291d-129">Specifies the name of a logic app for which this cmdlet gets an action.</span></span>

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

### <span data-ttu-id="7291d-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7291d-130">-ResourceGroupName</span></span>

<span data-ttu-id="7291d-131">Указывает имя группы ресурсов, в которой этот cmdlet получает действие.</span><span class="sxs-lookup"><span data-stu-id="7291d-131">Specifies the name of a resource group in which this cmdlet gets an action.</span></span>

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

### <span data-ttu-id="7291d-132">-RunName</span><span class="sxs-lookup"><span data-stu-id="7291d-132">-RunName</span></span>

<span data-ttu-id="7291d-133">Указывает имя запуска приложения логики.</span><span class="sxs-lookup"><span data-stu-id="7291d-133">Specifies the name of a run of a logic app.</span></span>
<span data-ttu-id="7291d-134">Этот cmdlet получает действие для запуска, указанное этим параметром.</span><span class="sxs-lookup"><span data-stu-id="7291d-134">This cmdlet gets an action for the run that this parameter specifies.</span></span>

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

### <span data-ttu-id="7291d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7291d-135">CommonParameters</span></span>

<span data-ttu-id="7291d-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7291d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7291d-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7291d-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7291d-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7291d-138">INPUTS</span></span>

### <span data-ttu-id="7291d-139">System.String</span><span class="sxs-lookup"><span data-stu-id="7291d-139">System.String</span></span>

## <span data-ttu-id="7291d-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7291d-140">OUTPUTS</span></span>

### <span data-ttu-id="7291d-141">Microsoft.Azure.Management.Logic.Models.WorkflowRunAction</span><span class="sxs-lookup"><span data-stu-id="7291d-141">Microsoft.Azure.Management.Logic.Models.WorkflowRunAction</span></span>

## <span data-ttu-id="7291d-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7291d-142">NOTES</span></span>

## <span data-ttu-id="7291d-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7291d-143">RELATED LINKS</span></span>

[<span data-ttu-id="7291d-144">Get-AzLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="7291d-144">Get-AzLogicAppRunHistory</span></span>](./Get-AzLogicAppRunHistory.md)

[<span data-ttu-id="7291d-145">Stop-AzLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="7291d-145">Stop-AzLogicAppRun</span></span>](./Stop-AzLogicAppRun.md)

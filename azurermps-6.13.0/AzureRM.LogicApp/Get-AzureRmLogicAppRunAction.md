---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 2EA28B90-4BAE-45DF-BD2E-60C74F53FB7B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/get-azurermlogicapprunaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicAppRunAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicAppRunAction.md
ms.openlocfilehash: 4aa135adf8db8cc1044eba761b33f570abd0396b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732246"
---
# <span data-ttu-id="d36eb-101">Get-AzureRmLogicAppRunAction</span><span class="sxs-lookup"><span data-stu-id="d36eb-101">Get-AzureRmLogicAppRunAction</span></span>

## <span data-ttu-id="d36eb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d36eb-102">SYNOPSIS</span></span>
<span data-ttu-id="d36eb-103">Возвращает действие, выполняемое логическим приложением.</span><span class="sxs-lookup"><span data-stu-id="d36eb-103">Gets an action from a logic app run.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d36eb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d36eb-104">SYNTAX</span></span>

```
Get-AzureRmLogicAppRunAction -ResourceGroupName <String> -Name <String> -RunName <String>
 [-ActionName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d36eb-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d36eb-105">DESCRIPTION</span></span>
<span data-ttu-id="d36eb-106">Командлет **Get-AzureRmLogicAppRunAction** Возвращает действие, выполняемое логическим приложением.</span><span class="sxs-lookup"><span data-stu-id="d36eb-106">The **Get-AzureRmLogicAppRunAction** cmdlet gets an action from a logic app run.</span></span>
<span data-ttu-id="d36eb-107">Этот командлет возвращает объекты **WorkflowRunAction** .</span><span class="sxs-lookup"><span data-stu-id="d36eb-107">This cmdlet returns a **WorkflowRunAction** objects.</span></span>
<span data-ttu-id="d36eb-108">Укажите логическое приложение, группу ресурсов и запуск.</span><span class="sxs-lookup"><span data-stu-id="d36eb-108">Specify the logic app, resource group, and run.</span></span>
<span data-ttu-id="d36eb-109">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="d36eb-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="d36eb-110">Чтобы использовать динамический параметр, введите его в командную команду.</span><span class="sxs-lookup"><span data-stu-id="d36eb-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="d36eb-111">Чтобы найти имена динамических параметров, введите дефис (-) после имени командлета, а затем несколько раз нажмите клавишу TAB, чтобы просмотреть все доступные параметры.</span><span class="sxs-lookup"><span data-stu-id="d36eb-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="d36eb-112">Если вы не пропустите требуемый параметр шаблона, командлет предложит вам указать значение.</span><span class="sxs-lookup"><span data-stu-id="d36eb-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="d36eb-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d36eb-113">EXAMPLES</span></span>

### <span data-ttu-id="d36eb-114">Пример 1: получение действия из приложения логики выполнение</span><span class="sxs-lookup"><span data-stu-id="d36eb-114">Example 1: Get an action from a Logic App run</span></span>
```
PS C:\>Get-AzureRmLogicAppActionRun -ResourceGroupName "ResourceGroup11" -Name "LogicApp05" -RunName "LogicAppRun56" -ActionName "LogicAppAction01"
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

<span data-ttu-id="d36eb-115">Эта команда получает определенное логическое действие приложения из приложения Logic с именем LogicApp05 для запуска с именем LogicAppRun56.</span><span class="sxs-lookup"><span data-stu-id="d36eb-115">This command gets a specific Logic App action from the logic app named LogicApp05 for the run named LogicAppRun56.</span></span>

### <span data-ttu-id="d36eb-116">Пример 2: получение всех действий из приложения логики выполнение</span><span class="sxs-lookup"><span data-stu-id="d36eb-116">Example 2: Get all the actions from a Logic App run</span></span>
```
PS C:\>Get-AzureRmLogicAppActionRun -ResourceGroupName "ResourceGroup11" -Name "LogicApp05" -RunName "LogicAppRun56"
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

<span data-ttu-id="d36eb-117">Эта команда получает все логические действия приложения из запуска с именем LogicAppRun56 из приложения Logic с именем LogicApp05.</span><span class="sxs-lookup"><span data-stu-id="d36eb-117">This command gets all Logic App actions from a run named LogicAppRun56 of a logic app named LogicApp05.</span></span>

## <span data-ttu-id="d36eb-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d36eb-118">PARAMETERS</span></span>

### <span data-ttu-id="d36eb-119">-Имямакрокоманды</span><span class="sxs-lookup"><span data-stu-id="d36eb-119">-ActionName</span></span>
<span data-ttu-id="d36eb-120">Указывает имя действия в логическом запуске приложения.</span><span class="sxs-lookup"><span data-stu-id="d36eb-120">Specifies the name of an action in a logic app run.</span></span>
<span data-ttu-id="d36eb-121">Этот командлет получает действие, которое указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="d36eb-121">This cmdlet gets the action that this parameter specifies.</span></span>

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

### <span data-ttu-id="d36eb-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d36eb-122">-DefaultProfile</span></span>
<span data-ttu-id="d36eb-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="d36eb-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d36eb-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d36eb-124">-Name</span></span>
<span data-ttu-id="d36eb-125">Указывает имя приложения логики, для которого этот командлет получает действие.</span><span class="sxs-lookup"><span data-stu-id="d36eb-125">Specifies the name of a logic app for which this cmdlet gets an action.</span></span>

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

### <span data-ttu-id="d36eb-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d36eb-126">-ResourceGroupName</span></span>
<span data-ttu-id="d36eb-127">Указывает имя группы ресурсов, в которой этот командлет получает действие.</span><span class="sxs-lookup"><span data-stu-id="d36eb-127">Specifies the name of a resource group in which this cmdlet gets an action.</span></span>

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

### <span data-ttu-id="d36eb-128">-RunName</span><span class="sxs-lookup"><span data-stu-id="d36eb-128">-RunName</span></span>
<span data-ttu-id="d36eb-129">Указывает имя запуска логики приложения.</span><span class="sxs-lookup"><span data-stu-id="d36eb-129">Specifies the name of a run of a logic app.</span></span>
<span data-ttu-id="d36eb-130">Этот командлет получает действие для выполнения, которое указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="d36eb-130">This cmdlet gets an action for the run that this parameter specifies.</span></span>

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

### <span data-ttu-id="d36eb-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d36eb-131">CommonParameters</span></span>
<span data-ttu-id="d36eb-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d36eb-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d36eb-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d36eb-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d36eb-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d36eb-134">INPUTS</span></span>

### <span data-ttu-id="d36eb-135">System. String</span><span class="sxs-lookup"><span data-stu-id="d36eb-135">System.String</span></span>

## <span data-ttu-id="d36eb-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d36eb-136">OUTPUTS</span></span>

### <span data-ttu-id="d36eb-137">Microsoft. Azure. Management. Logic. Models. WorkflowRunAction</span><span class="sxs-lookup"><span data-stu-id="d36eb-137">Microsoft.Azure.Management.Logic.Models.WorkflowRunAction</span></span>

## <span data-ttu-id="d36eb-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="d36eb-138">NOTES</span></span>

## <span data-ttu-id="d36eb-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d36eb-139">RELATED LINKS</span></span>

[<span data-ttu-id="d36eb-140">Get-AzureRmLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="d36eb-140">Get-AzureRmLogicAppRunHistory</span></span>](./Get-AzureRmLogicAppRunHistory.md)

[<span data-ttu-id="d36eb-141">Остановить-AzureRmLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="d36eb-141">Stop-AzureRmLogicAppRun</span></span>](./Stop-AzureRmLogicAppRun.md)



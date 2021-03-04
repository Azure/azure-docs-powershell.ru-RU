---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 50C359FC-D98C-4C2C-87EE-BE9A25C3EDC6
online version: https://docs.microsoft.com/powershell/module/az.logicapp/start-azlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Start-AzLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Start-AzLogicApp.md
ms.openlocfilehash: c109839692ea20f1fbbcced50df9c4167322b1b1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952456"
---
# <span data-ttu-id="ea6c3-101">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="ea6c3-101">Start-AzLogicApp</span></span>

## <span data-ttu-id="ea6c3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea6c3-102">SYNOPSIS</span></span>
<span data-ttu-id="ea6c3-103">Запуск приложения логики в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ea6c3-103">Runs a logic app in a resource group.</span></span>

## <span data-ttu-id="ea6c3-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ea6c3-104">SYNTAX</span></span>

```
Start-AzLogicApp -ResourceGroupName <String> -Name <String> [-Parameters <Object>] -TriggerName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea6c3-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ea6c3-105">DESCRIPTION</span></span>
<span data-ttu-id="ea6c3-106">Для **запуска приложения Start-AzLogicApp** используется функция "Логические приложения".</span><span class="sxs-lookup"><span data-stu-id="ea6c3-106">The **Start-AzLogicApp** cmdlet runs a logic app by using the Logic Apps feature.</span></span>
<span data-ttu-id="ea6c3-107">Укажите имя, группу ресурсов и триггер.</span><span class="sxs-lookup"><span data-stu-id="ea6c3-107">Specify a name, resource group, and trigger.</span></span>
<span data-ttu-id="ea6c3-108">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="ea6c3-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="ea6c3-109">Чтобы использовать динамический параметр, введите его в команду.</span><span class="sxs-lookup"><span data-stu-id="ea6c3-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="ea6c3-110">Чтобы найти имена динамических параметров, введите дефис (-) после имени cmdlet, а затем нажимая клавишу TAB для циклическиго перебора доступных параметров.</span><span class="sxs-lookup"><span data-stu-id="ea6c3-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="ea6c3-111">Если параметр обязательного шаблона не задан, будет выдан запрос на его значение.</span><span class="sxs-lookup"><span data-stu-id="ea6c3-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="ea6c3-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ea6c3-112">EXAMPLES</span></span>

### <span data-ttu-id="ea6c3-113">Пример 1. Запуск приложения логики</span><span class="sxs-lookup"><span data-stu-id="ea6c3-113">Example 1: Run a logic app</span></span>
```
PS C:\>Start-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -TriggerName "Trigger22"
```

<span data-ttu-id="ea6c3-114">Эта команда запускает приложение логики в группе ресурсов ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="ea6c3-114">This command runs the logic app in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="ea6c3-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ea6c3-115">PARAMETERS</span></span>

### <span data-ttu-id="ea6c3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea6c3-116">-DefaultProfile</span></span>
<span data-ttu-id="ea6c3-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="ea6c3-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ea6c3-118">-Name</span><span class="sxs-lookup"><span data-stu-id="ea6c3-118">-Name</span></span>
<span data-ttu-id="ea6c3-119">Указывает имя приложения логики, которое запускается этим cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea6c3-119">Specifies the name of the logic app that this cmdlet starts.</span></span>

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

### <span data-ttu-id="ea6c3-120">-Parameters</span><span class="sxs-lookup"><span data-stu-id="ea6c3-120">-Parameters</span></span>
<span data-ttu-id="ea6c3-121">Определяет объект коллекции параметров приложения logic.</span><span class="sxs-lookup"><span data-stu-id="ea6c3-121">Specifies a parameters collection object of the logic app.</span></span>
<span data-ttu-id="ea6c3-122">Укажите hash table, Dictionary \<string\> или Dictionary \<string, WorkflowParameter\> (Словарь).</span><span class="sxs-lookup"><span data-stu-id="ea6c3-122">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea6c3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea6c3-123">-ResourceGroupName</span></span>
<span data-ttu-id="ea6c3-124">Имя группы ресурсов, которая содержит приложение логики, которое запускается этим cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea6c3-124">Specifies the name of the resource group that contains the logic app that this cmdlet starts.</span></span>

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

### <span data-ttu-id="ea6c3-125">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="ea6c3-125">-TriggerName</span></span>
<span data-ttu-id="ea6c3-126">Указывает имя триггера приложения логики, которое запускается этим cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea6c3-126">Specifies the name of the trigger of the logic app that this cmdlet starts.</span></span>

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

### <span data-ttu-id="ea6c3-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ea6c3-127">-Confirm</span></span>
<span data-ttu-id="ea6c3-128">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="ea6c3-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea6c3-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea6c3-129">-WhatIf</span></span>
<span data-ttu-id="ea6c3-130">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea6c3-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea6c3-131">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ea6c3-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea6c3-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea6c3-132">CommonParameters</span></span>
<span data-ttu-id="ea6c3-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea6c3-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea6c3-134">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea6c3-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea6c3-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ea6c3-135">INPUTS</span></span>

### <span data-ttu-id="ea6c3-136">System.String</span><span class="sxs-lookup"><span data-stu-id="ea6c3-136">System.String</span></span>

## <span data-ttu-id="ea6c3-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ea6c3-137">OUTPUTS</span></span>

### <span data-ttu-id="ea6c3-138">System.Void</span><span class="sxs-lookup"><span data-stu-id="ea6c3-138">System.Void</span></span>

## <span data-ttu-id="ea6c3-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ea6c3-139">NOTES</span></span>

## <span data-ttu-id="ea6c3-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ea6c3-140">RELATED LINKS</span></span>

[<span data-ttu-id="ea6c3-141">Get-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="ea6c3-141">Get-AzLogicApp</span></span>](./Get-AzLogicApp.md)

[<span data-ttu-id="ea6c3-142">Get-AzLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="ea6c3-142">Get-AzLogicAppRunHistory</span></span>](./Get-AzLogicAppRunHistory.md)

[<span data-ttu-id="ea6c3-143">New-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="ea6c3-143">New-AzLogicApp</span></span>](./New-AzLogicApp.md)

[<span data-ttu-id="ea6c3-144">Remove-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="ea6c3-144">Remove-AzLogicApp</span></span>](./Remove-AzLogicApp.md)

[<span data-ttu-id="ea6c3-145">Set-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="ea6c3-145">Set-AzLogicApp</span></span>](./Set-AzLogicApp.md)

[<span data-ttu-id="ea6c3-146">Stop-AzLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="ea6c3-146">Stop-AzLogicAppRun</span></span>](./Stop-AzLogicAppRun.md)



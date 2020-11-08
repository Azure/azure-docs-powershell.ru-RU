---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 50C359FC-D98C-4C2C-87EE-BE9A25C3EDC6
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/start-azlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Start-AzLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Start-AzLogicApp.md
ms.openlocfilehash: e93efdaf8ec55c3b7c8fb0793a24e062553545ff
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248950"
---
# <span data-ttu-id="3d10a-101">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="3d10a-101">Start-AzLogicApp</span></span>

## <span data-ttu-id="3d10a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3d10a-102">SYNOPSIS</span></span>
<span data-ttu-id="3d10a-103">Запускает логическое приложение в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3d10a-103">Runs a logic app in a resource group.</span></span>

## <span data-ttu-id="3d10a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3d10a-104">SYNTAX</span></span>

```
Start-AzLogicApp -ResourceGroupName <String> -Name <String> [-Parameters <Object>] -TriggerName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d10a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3d10a-105">DESCRIPTION</span></span>
<span data-ttu-id="3d10a-106">Командлет **Start-AzLogicApp** запускает логическое приложение с помощью функции "приложения логики".</span><span class="sxs-lookup"><span data-stu-id="3d10a-106">The **Start-AzLogicApp** cmdlet runs a logic app by using the Logic Apps feature.</span></span>
<span data-ttu-id="3d10a-107">Укажите имя, группу ресурсов и триггер.</span><span class="sxs-lookup"><span data-stu-id="3d10a-107">Specify a name, resource group, and trigger.</span></span>
<span data-ttu-id="3d10a-108">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="3d10a-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="3d10a-109">Чтобы использовать динамический параметр, введите его в командную команду.</span><span class="sxs-lookup"><span data-stu-id="3d10a-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="3d10a-110">Чтобы найти имена динамических параметров, введите дефис (-) после имени командлета, а затем несколько раз нажмите клавишу TAB, чтобы просмотреть все доступные параметры.</span><span class="sxs-lookup"><span data-stu-id="3d10a-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="3d10a-111">Если вы не пропустите требуемый параметр шаблона, командлет предложит вам указать значение.</span><span class="sxs-lookup"><span data-stu-id="3d10a-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="3d10a-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3d10a-112">EXAMPLES</span></span>

### <span data-ttu-id="3d10a-113">Пример 1: запуск приложения логики</span><span class="sxs-lookup"><span data-stu-id="3d10a-113">Example 1: Run a logic app</span></span>
```
PS C:\>Start-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -TriggerName "Trigger22"
```

<span data-ttu-id="3d10a-114">Эта команда запускает приложение Logic в группе ресурсов с именем ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="3d10a-114">This command runs the logic app in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="3d10a-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3d10a-115">PARAMETERS</span></span>

### <span data-ttu-id="3d10a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d10a-116">-DefaultProfile</span></span>
<span data-ttu-id="3d10a-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="3d10a-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3d10a-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3d10a-118">-Name</span></span>
<span data-ttu-id="3d10a-119">Указывает имя приложения логики, с которого начинается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="3d10a-119">Specifies the name of the logic app that this cmdlet starts.</span></span>

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

### <span data-ttu-id="3d10a-120">-Parameters</span><span class="sxs-lookup"><span data-stu-id="3d10a-120">-Parameters</span></span>
<span data-ttu-id="3d10a-121">Указывает объект коллекции Parameters для приложения логики.</span><span class="sxs-lookup"><span data-stu-id="3d10a-121">Specifies a parameters collection object of the logic app.</span></span>
<span data-ttu-id="3d10a-122">Укажите хэш-таблицу, словарь \<string\> или словарь \<string, WorkflowParameter\> .</span><span class="sxs-lookup"><span data-stu-id="3d10a-122">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

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

### <span data-ttu-id="3d10a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d10a-123">-ResourceGroupName</span></span>
<span data-ttu-id="3d10a-124">Указывает имя группы ресурсов, которая содержит логическое приложение, которое запускает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="3d10a-124">Specifies the name of the resource group that contains the logic app that this cmdlet starts.</span></span>

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

### <span data-ttu-id="3d10a-125">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="3d10a-125">-TriggerName</span></span>
<span data-ttu-id="3d10a-126">Задает имя триггера приложения логики, с которого начинается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="3d10a-126">Specifies the name of the trigger of the logic app that this cmdlet starts.</span></span>

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

### <span data-ttu-id="3d10a-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3d10a-127">-Confirm</span></span>
<span data-ttu-id="3d10a-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3d10a-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d10a-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d10a-129">-WhatIf</span></span>
<span data-ttu-id="3d10a-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3d10a-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d10a-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3d10a-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d10a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d10a-132">CommonParameters</span></span>
<span data-ttu-id="3d10a-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3d10a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d10a-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d10a-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d10a-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3d10a-135">INPUTS</span></span>

### <span data-ttu-id="3d10a-136">System. String</span><span class="sxs-lookup"><span data-stu-id="3d10a-136">System.String</span></span>

## <span data-ttu-id="3d10a-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3d10a-137">OUTPUTS</span></span>

### <span data-ttu-id="3d10a-138">System. void</span><span class="sxs-lookup"><span data-stu-id="3d10a-138">System.Void</span></span>

## <span data-ttu-id="3d10a-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="3d10a-139">NOTES</span></span>

## <span data-ttu-id="3d10a-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3d10a-140">RELATED LINKS</span></span>

[<span data-ttu-id="3d10a-141">Get-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="3d10a-141">Get-AzLogicApp</span></span>](./Get-AzLogicApp.md)

[<span data-ttu-id="3d10a-142">Get-AzLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="3d10a-142">Get-AzLogicAppRunHistory</span></span>](./Get-AzLogicAppRunHistory.md)

[<span data-ttu-id="3d10a-143">New-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="3d10a-143">New-AzLogicApp</span></span>](./New-AzLogicApp.md)

[<span data-ttu-id="3d10a-144">Remove-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="3d10a-144">Remove-AzLogicApp</span></span>](./Remove-AzLogicApp.md)

[<span data-ttu-id="3d10a-145">Set-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="3d10a-145">Set-AzLogicApp</span></span>](./Set-AzLogicApp.md)

[<span data-ttu-id="3d10a-146">Остановить-AzLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="3d10a-146">Stop-AzLogicAppRun</span></span>](./Stop-AzLogicAppRun.md)



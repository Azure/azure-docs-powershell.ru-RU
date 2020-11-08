---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 3308F901-4C9F-424D-8BEB-877A6038B246
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/stop-azlogicapprun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Stop-AzLogicAppRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Stop-AzLogicAppRun.md
ms.openlocfilehash: 9a437d3b8e1803865aedf7e46d0bf879cfcdeab8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243547"
---
# <span data-ttu-id="bc6cb-101">Stop-AzLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="bc6cb-101">Stop-AzLogicAppRun</span></span>

## <span data-ttu-id="bc6cb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bc6cb-102">SYNOPSIS</span></span>
<span data-ttu-id="bc6cb-103">Отменяет выполнение логики приложения.</span><span class="sxs-lookup"><span data-stu-id="bc6cb-103">Cancels a run of a logic app.</span></span>

## <span data-ttu-id="bc6cb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bc6cb-104">SYNTAX</span></span>

```
Stop-AzLogicAppRun -ResourceGroupName <String> -Name <String> -RunName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc6cb-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bc6cb-105">DESCRIPTION</span></span>
<span data-ttu-id="bc6cb-106">Командлет **Stop-AzLogicAppRun** отменяет выполнение логического приложения.</span><span class="sxs-lookup"><span data-stu-id="bc6cb-106">The **Stop-AzLogicAppRun** cmdlet cancels a run of a logic app.</span></span>
<span data-ttu-id="bc6cb-107">Укажите логическое приложение, группу ресурсов и запуск.</span><span class="sxs-lookup"><span data-stu-id="bc6cb-107">Specify the logic app, resource group, and run.</span></span>
<span data-ttu-id="bc6cb-108">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="bc6cb-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="bc6cb-109">Чтобы использовать динамический параметр, введите его в командную команду.</span><span class="sxs-lookup"><span data-stu-id="bc6cb-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="bc6cb-110">Чтобы найти имена динамических параметров, введите дефис (-) после имени командлета, а затем несколько раз нажмите клавишу TAB, чтобы просмотреть все доступные параметры.</span><span class="sxs-lookup"><span data-stu-id="bc6cb-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="bc6cb-111">Если вы не пропустите требуемый параметр шаблона, командлет предложит вам указать значение.</span><span class="sxs-lookup"><span data-stu-id="bc6cb-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="bc6cb-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bc6cb-112">EXAMPLES</span></span>

### <span data-ttu-id="bc6cb-113">Пример 1: Отмена выполнения приложения логики</span><span class="sxs-lookup"><span data-stu-id="bc6cb-113">Example 1: Cancel a run of a logic app</span></span>
```
PS C:\>Stop-AzLogicAppRun -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -RunName "08587489104702792076" -Force
```

<span data-ttu-id="bc6cb-114">Эта команда отменяет выполнение логического приложения с именем LogicApp03.</span><span class="sxs-lookup"><span data-stu-id="bc6cb-114">This command cancels a run of the logic app named LogicApp03.</span></span>

## <span data-ttu-id="bc6cb-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bc6cb-115">PARAMETERS</span></span>

### <span data-ttu-id="bc6cb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc6cb-116">-DefaultProfile</span></span>
<span data-ttu-id="bc6cb-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="bc6cb-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bc6cb-118">-Force</span><span class="sxs-lookup"><span data-stu-id="bc6cb-118">-Force</span></span>
<span data-ttu-id="bc6cb-119">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="bc6cb-119">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc6cb-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="bc6cb-120">-Name</span></span>
<span data-ttu-id="bc6cb-121">Указывает имя логического приложения, для которого этот командлет отменяет выполнение.</span><span class="sxs-lookup"><span data-stu-id="bc6cb-121">Specifies the name of a logic app for which this cmdlet cancels a run.</span></span>

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

### <span data-ttu-id="bc6cb-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc6cb-122">-ResourceGroupName</span></span>
<span data-ttu-id="bc6cb-123">Указывает имя группы ресурсов, в которой этот командлет отменяет выполнение.</span><span class="sxs-lookup"><span data-stu-id="bc6cb-123">Specifies the name for a resource group in which this cmdlet cancels a run.</span></span>

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

### <span data-ttu-id="bc6cb-124">-RunName</span><span class="sxs-lookup"><span data-stu-id="bc6cb-124">-RunName</span></span>
<span data-ttu-id="bc6cb-125">Указывает имя приложения логики, которое отменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="bc6cb-125">Specifies the name of a logic app run that this cmdlet cancels.</span></span>

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

### <span data-ttu-id="bc6cb-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bc6cb-126">-Confirm</span></span>
<span data-ttu-id="bc6cb-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="bc6cb-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc6cb-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc6cb-128">-WhatIf</span></span>
<span data-ttu-id="bc6cb-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="bc6cb-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc6cb-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="bc6cb-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc6cb-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc6cb-131">CommonParameters</span></span>
<span data-ttu-id="bc6cb-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bc6cb-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc6cb-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc6cb-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc6cb-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bc6cb-134">INPUTS</span></span>

### <span data-ttu-id="bc6cb-135">System. String</span><span class="sxs-lookup"><span data-stu-id="bc6cb-135">System.String</span></span>

## <span data-ttu-id="bc6cb-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bc6cb-136">OUTPUTS</span></span>

### <span data-ttu-id="bc6cb-137">System. void</span><span class="sxs-lookup"><span data-stu-id="bc6cb-137">System.Void</span></span>

## <span data-ttu-id="bc6cb-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="bc6cb-138">NOTES</span></span>

## <span data-ttu-id="bc6cb-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bc6cb-139">RELATED LINKS</span></span>

[<span data-ttu-id="bc6cb-140">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="bc6cb-140">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)



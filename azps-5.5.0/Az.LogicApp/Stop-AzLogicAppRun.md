---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 3308F901-4C9F-424D-8BEB-877A6038B246
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/stop-azlogicapprun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Stop-AzLogicAppRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Stop-AzLogicAppRun.md
ms.openlocfilehash: 9a437d3b8e1803865aedf7e46d0bf879cfcdeab8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100228249"
---
# <span data-ttu-id="241b8-101">Stop-AzLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="241b8-101">Stop-AzLogicAppRun</span></span>

## <span data-ttu-id="241b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="241b8-102">SYNOPSIS</span></span>
<span data-ttu-id="241b8-103">Отмена запуска приложения логики.</span><span class="sxs-lookup"><span data-stu-id="241b8-103">Cancels a run of a logic app.</span></span>

## <span data-ttu-id="241b8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="241b8-104">SYNTAX</span></span>

```
Stop-AzLogicAppRun -ResourceGroupName <String> -Name <String> -RunName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="241b8-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="241b8-105">DESCRIPTION</span></span>
<span data-ttu-id="241b8-106">С **помощью cmdlet Stop-AzLogicAppRun** можно отменить запуск приложения логики.</span><span class="sxs-lookup"><span data-stu-id="241b8-106">The **Stop-AzLogicAppRun** cmdlet cancels a run of a logic app.</span></span>
<span data-ttu-id="241b8-107">Укажите приложение логики, группу ресурсов и запустите его.</span><span class="sxs-lookup"><span data-stu-id="241b8-107">Specify the logic app, resource group, and run.</span></span>
<span data-ttu-id="241b8-108">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="241b8-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="241b8-109">Чтобы использовать динамический параметр, введите его в команду.</span><span class="sxs-lookup"><span data-stu-id="241b8-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="241b8-110">Чтобы найти имена динамических параметров, введите дефис (-) после имени cmdlet, а затем нажимая клавишу TAB для циклическиго перебора доступных параметров.</span><span class="sxs-lookup"><span data-stu-id="241b8-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="241b8-111">Если не задан параметр обязательного шаблона, будет выдан запрос на его значение.</span><span class="sxs-lookup"><span data-stu-id="241b8-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="241b8-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="241b8-112">EXAMPLES</span></span>

### <span data-ttu-id="241b8-113">Пример 1. Отмена запуска приложения логики</span><span class="sxs-lookup"><span data-stu-id="241b8-113">Example 1: Cancel a run of a logic app</span></span>
```
PS C:\>Stop-AzLogicAppRun -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -RunName "08587489104702792076" -Force
```

<span data-ttu-id="241b8-114">Эта команда отменяет запуск логического приложения LogicApp03.</span><span class="sxs-lookup"><span data-stu-id="241b8-114">This command cancels a run of the logic app named LogicApp03.</span></span>

## <span data-ttu-id="241b8-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="241b8-115">PARAMETERS</span></span>

### <span data-ttu-id="241b8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="241b8-116">-DefaultProfile</span></span>
<span data-ttu-id="241b8-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="241b8-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="241b8-118">-Force</span><span class="sxs-lookup"><span data-stu-id="241b8-118">-Force</span></span>
<span data-ttu-id="241b8-119">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="241b8-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="241b8-120">-Name</span><span class="sxs-lookup"><span data-stu-id="241b8-120">-Name</span></span>
<span data-ttu-id="241b8-121">Указывает имя приложения логики, для которого этот cmdlet отменяет запуск.</span><span class="sxs-lookup"><span data-stu-id="241b8-121">Specifies the name of a logic app for which this cmdlet cancels a run.</span></span>

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

### <span data-ttu-id="241b8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="241b8-122">-ResourceGroupName</span></span>
<span data-ttu-id="241b8-123">Имя группы ресурсов, в которой этот cmdlet отменяет запуск.</span><span class="sxs-lookup"><span data-stu-id="241b8-123">Specifies the name for a resource group in which this cmdlet cancels a run.</span></span>

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

### <span data-ttu-id="241b8-124">-RunName</span><span class="sxs-lookup"><span data-stu-id="241b8-124">-RunName</span></span>
<span data-ttu-id="241b8-125">Указывает имя запуска логического приложения, отменяемого этим cmdletом.</span><span class="sxs-lookup"><span data-stu-id="241b8-125">Specifies the name of a logic app run that this cmdlet cancels.</span></span>

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

### <span data-ttu-id="241b8-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="241b8-126">-Confirm</span></span>
<span data-ttu-id="241b8-127">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="241b8-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="241b8-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="241b8-128">-WhatIf</span></span>
<span data-ttu-id="241b8-129">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="241b8-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="241b8-130">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="241b8-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="241b8-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="241b8-131">CommonParameters</span></span>
<span data-ttu-id="241b8-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="241b8-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="241b8-133">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="241b8-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="241b8-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="241b8-134">INPUTS</span></span>

### <span data-ttu-id="241b8-135">System.String</span><span class="sxs-lookup"><span data-stu-id="241b8-135">System.String</span></span>

## <span data-ttu-id="241b8-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="241b8-136">OUTPUTS</span></span>

### <span data-ttu-id="241b8-137">System.Void</span><span class="sxs-lookup"><span data-stu-id="241b8-137">System.Void</span></span>

## <span data-ttu-id="241b8-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="241b8-138">NOTES</span></span>

## <span data-ttu-id="241b8-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="241b8-139">RELATED LINKS</span></span>

[<span data-ttu-id="241b8-140">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="241b8-140">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)



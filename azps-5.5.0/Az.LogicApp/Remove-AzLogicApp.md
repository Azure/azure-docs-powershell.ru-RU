---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 39D1576D-7042-4A62-AB41-0B5131C150D5
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzLogicApp.md
ms.openlocfilehash: 573ebbef14eef64d0dc1dd5a6e193eaac2deec0a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100214425"
---
# <span data-ttu-id="1c3bb-101">Remove-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="1c3bb-101">Remove-AzLogicApp</span></span>

## <span data-ttu-id="1c3bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1c3bb-102">SYNOPSIS</span></span>
<span data-ttu-id="1c3bb-103">Удаляет приложение логики из группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1c3bb-103">Removes a logic app from a resource group.</span></span>

## <span data-ttu-id="1c3bb-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1c3bb-104">SYNTAX</span></span>

```
Remove-AzLogicApp -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c3bb-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1c3bb-105">DESCRIPTION</span></span>
<span data-ttu-id="1c3bb-106">С **помощью функции "Логические приложения"** можно удалить приложение логики из группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1c3bb-106">The **Remove-AzLogicApp** cmdlet removes a logic app from a resource group by using the Logic Apps feature.</span></span>
<span data-ttu-id="1c3bb-107">Укажите приложение и группу ресурсов для логики.</span><span class="sxs-lookup"><span data-stu-id="1c3bb-107">Specify the logic app and resource group.</span></span>
<span data-ttu-id="1c3bb-108">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="1c3bb-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="1c3bb-109">Чтобы использовать динамический параметр, введите его в команду.</span><span class="sxs-lookup"><span data-stu-id="1c3bb-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="1c3bb-110">Чтобы найти имена динамических параметров, введите дефис (-) после имени cmdlet, а затем нажимая клавишу TAB для циклическиго перебора доступных параметров.</span><span class="sxs-lookup"><span data-stu-id="1c3bb-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="1c3bb-111">Если не задан параметр обязательного шаблона, будет выдан запрос на его значение.</span><span class="sxs-lookup"><span data-stu-id="1c3bb-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="1c3bb-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1c3bb-112">EXAMPLES</span></span>

### <span data-ttu-id="1c3bb-113">Пример 1. Удаление приложения логики</span><span class="sxs-lookup"><span data-stu-id="1c3bb-113">Example 1: Remove a logic app</span></span>
```
PS C:\>Remove-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -Force
```

<span data-ttu-id="1c3bb-114">Эта команда удаляет приложение-логику из группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1c3bb-114">This command removes a logic app from a resource group.</span></span>
<span data-ttu-id="1c3bb-115">Команда включает параметр *Force,* который не позволяет получить подтверждение.</span><span class="sxs-lookup"><span data-stu-id="1c3bb-115">The command includes the *Force* parameter, which prevents the command from prompting you for confirmation.</span></span>

## <span data-ttu-id="1c3bb-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1c3bb-116">PARAMETERS</span></span>

### <span data-ttu-id="1c3bb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c3bb-117">-DefaultProfile</span></span>
<span data-ttu-id="1c3bb-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="1c3bb-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1c3bb-119">-Force</span><span class="sxs-lookup"><span data-stu-id="1c3bb-119">-Force</span></span>
<span data-ttu-id="1c3bb-120">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="1c3bb-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1c3bb-121">-Name</span><span class="sxs-lookup"><span data-stu-id="1c3bb-121">-Name</span></span>
<span data-ttu-id="1c3bb-122">Указывает имя приложения логики, которое удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1c3bb-122">Specifies the name of the logic app that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c3bb-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c3bb-123">-ResourceGroupName</span></span>
<span data-ttu-id="1c3bb-124">Имя группы ресурсов, которая содержит приложение логики, которое удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1c3bb-124">Specifies the name of the resource group that contains the logic app that this cmdlet removes.</span></span>

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

### <span data-ttu-id="1c3bb-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1c3bb-125">-Confirm</span></span>
<span data-ttu-id="1c3bb-126">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1c3bb-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c3bb-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c3bb-127">-WhatIf</span></span>
<span data-ttu-id="1c3bb-128">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1c3bb-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c3bb-129">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="1c3bb-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c3bb-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c3bb-130">CommonParameters</span></span>
<span data-ttu-id="1c3bb-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c3bb-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c3bb-132">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c3bb-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c3bb-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1c3bb-133">INPUTS</span></span>

### <span data-ttu-id="1c3bb-134">System.String</span><span class="sxs-lookup"><span data-stu-id="1c3bb-134">System.String</span></span>

## <span data-ttu-id="1c3bb-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1c3bb-135">OUTPUTS</span></span>

### <span data-ttu-id="1c3bb-136">System.Void</span><span class="sxs-lookup"><span data-stu-id="1c3bb-136">System.Void</span></span>

## <span data-ttu-id="1c3bb-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1c3bb-137">NOTES</span></span>

## <span data-ttu-id="1c3bb-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1c3bb-138">RELATED LINKS</span></span>

[<span data-ttu-id="1c3bb-139">Get-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="1c3bb-139">Get-AzLogicApp</span></span>](./Get-AzLogicApp.md)

[<span data-ttu-id="1c3bb-140">New-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="1c3bb-140">New-AzLogicApp</span></span>](./New-AzLogicApp.md)

[<span data-ttu-id="1c3bb-141">Set-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="1c3bb-141">Set-AzLogicApp</span></span>](./Set-AzLogicApp.md)

[<span data-ttu-id="1c3bb-142">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="1c3bb-142">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 39D1576D-7042-4A62-AB41-0B5131C150D5
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzLogicApp.md
ms.openlocfilehash: 3458eef92b18ea5407724a2ad1b0cb2e10024233
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93899857"
---
# <span data-ttu-id="ba323-101">Remove-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="ba323-101">Remove-AzLogicApp</span></span>

## <span data-ttu-id="ba323-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ba323-102">SYNOPSIS</span></span>
<span data-ttu-id="ba323-103">Удаляет логическое приложение из группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ba323-103">Removes a logic app from a resource group.</span></span>

## <span data-ttu-id="ba323-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ba323-104">SYNTAX</span></span>

```
Remove-AzLogicApp -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba323-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ba323-105">DESCRIPTION</span></span>
<span data-ttu-id="ba323-106">Командлет **Remove-AzLogicApp** удаляет логическое приложение из группы ресурсов с помощью функции приложения логики.</span><span class="sxs-lookup"><span data-stu-id="ba323-106">The **Remove-AzLogicApp** cmdlet removes a logic app from a resource group by using the Logic Apps feature.</span></span>
<span data-ttu-id="ba323-107">Укажите приложение логики и группу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ba323-107">Specify the logic app and resource group.</span></span>
<span data-ttu-id="ba323-108">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="ba323-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="ba323-109">Чтобы использовать динамический параметр, введите его в командную команду.</span><span class="sxs-lookup"><span data-stu-id="ba323-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="ba323-110">Чтобы найти имена динамических параметров, введите дефис (-) после имени командлета, а затем несколько раз нажмите клавишу TAB, чтобы просмотреть все доступные параметры.</span><span class="sxs-lookup"><span data-stu-id="ba323-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="ba323-111">Если вы не пропустите требуемый параметр шаблона, командлет предложит вам указать значение.</span><span class="sxs-lookup"><span data-stu-id="ba323-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="ba323-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ba323-112">EXAMPLES</span></span>

### <span data-ttu-id="ba323-113">Пример 1: Удаление логики приложения</span><span class="sxs-lookup"><span data-stu-id="ba323-113">Example 1: Remove a logic app</span></span>
```
PS C:\>Remove-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -Force
```

<span data-ttu-id="ba323-114">Эта команда удаляет логическое приложение из группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ba323-114">This command removes a logic app from a resource group.</span></span>
<span data-ttu-id="ba323-115">В команду входит параметр *Force* , который не позволяет команде выдать запрос на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="ba323-115">The command includes the *Force* parameter, which prevents the command from prompting you for confirmation.</span></span>

## <span data-ttu-id="ba323-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ba323-116">PARAMETERS</span></span>

### <span data-ttu-id="ba323-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba323-117">-DefaultProfile</span></span>
<span data-ttu-id="ba323-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="ba323-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ba323-119">-Force</span><span class="sxs-lookup"><span data-stu-id="ba323-119">-Force</span></span>
<span data-ttu-id="ba323-120">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="ba323-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ba323-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ba323-121">-Name</span></span>
<span data-ttu-id="ba323-122">Указывает имя приложения логики, которое удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="ba323-122">Specifies the name of the logic app that this cmdlet removes.</span></span>

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

### <span data-ttu-id="ba323-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba323-123">-ResourceGroupName</span></span>
<span data-ttu-id="ba323-124">Указывает имя группы ресурсов, которая содержит логическое приложение, которое удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="ba323-124">Specifies the name of the resource group that contains the logic app that this cmdlet removes.</span></span>

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

### <span data-ttu-id="ba323-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ba323-125">-Confirm</span></span>
<span data-ttu-id="ba323-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ba323-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba323-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba323-127">-WhatIf</span></span>
<span data-ttu-id="ba323-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ba323-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba323-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ba323-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba323-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba323-130">CommonParameters</span></span>
<span data-ttu-id="ba323-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ba323-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba323-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba323-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba323-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ba323-133">INPUTS</span></span>

### <span data-ttu-id="ba323-134">System. String</span><span class="sxs-lookup"><span data-stu-id="ba323-134">System.String</span></span>

## <span data-ttu-id="ba323-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ba323-135">OUTPUTS</span></span>

### <span data-ttu-id="ba323-136">System. void</span><span class="sxs-lookup"><span data-stu-id="ba323-136">System.Void</span></span>

## <span data-ttu-id="ba323-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="ba323-137">NOTES</span></span>

## <span data-ttu-id="ba323-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ba323-138">RELATED LINKS</span></span>

[<span data-ttu-id="ba323-139">Get-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="ba323-139">Get-AzLogicApp</span></span>](./Get-AzLogicApp.md)

[<span data-ttu-id="ba323-140">New-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="ba323-140">New-AzLogicApp</span></span>](./New-AzLogicApp.md)

[<span data-ttu-id="ba323-141">Set-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="ba323-141">Set-AzLogicApp</span></span>](./Set-AzLogicApp.md)

[<span data-ttu-id="ba323-142">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="ba323-142">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)



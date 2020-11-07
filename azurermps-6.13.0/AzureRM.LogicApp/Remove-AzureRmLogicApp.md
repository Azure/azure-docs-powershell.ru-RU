---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 39D1576D-7042-4A62-AB41-0B5131C150D5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/remove-azurermlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmLogicApp.md
ms.openlocfilehash: 46515fc76d246ffdb4207afb0300613b52cae0a5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734372"
---
# <span data-ttu-id="6b2d8-101">Remove-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="6b2d8-101">Remove-AzureRmLogicApp</span></span>

## <span data-ttu-id="6b2d8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6b2d8-102">SYNOPSIS</span></span>
<span data-ttu-id="6b2d8-103">Удаляет логическое приложение из группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6b2d8-103">Removes a logic app from a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6b2d8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6b2d8-104">SYNTAX</span></span>

```
Remove-AzureRmLogicApp -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b2d8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6b2d8-105">DESCRIPTION</span></span>
<span data-ttu-id="6b2d8-106">Командлет **Remove-AzureRmLogicApp** удаляет логическое приложение из группы ресурсов с помощью функции приложения логики.</span><span class="sxs-lookup"><span data-stu-id="6b2d8-106">The **Remove-AzureRmLogicApp** cmdlet removes a logic app from a resource group by using the Logic Apps feature.</span></span>
<span data-ttu-id="6b2d8-107">Укажите приложение логики и группу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6b2d8-107">Specify the logic app and resource group.</span></span>
<span data-ttu-id="6b2d8-108">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="6b2d8-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="6b2d8-109">Чтобы использовать динамический параметр, введите его в командную команду.</span><span class="sxs-lookup"><span data-stu-id="6b2d8-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="6b2d8-110">Чтобы найти имена динамических параметров, введите дефис (-) после имени командлета, а затем несколько раз нажмите клавишу TAB, чтобы просмотреть все доступные параметры.</span><span class="sxs-lookup"><span data-stu-id="6b2d8-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="6b2d8-111">Если вы не пропустите требуемый параметр шаблона, командлет предложит вам указать значение.</span><span class="sxs-lookup"><span data-stu-id="6b2d8-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="6b2d8-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6b2d8-112">EXAMPLES</span></span>

### <span data-ttu-id="6b2d8-113">Пример 1: Удаление логики приложения</span><span class="sxs-lookup"><span data-stu-id="6b2d8-113">Example 1: Remove a logic app</span></span>
```
PS C:\>Remove-AzureRmLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -Force
```

<span data-ttu-id="6b2d8-114">Эта команда удаляет логическое приложение из группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6b2d8-114">This command removes a logic app from a resource group.</span></span>
<span data-ttu-id="6b2d8-115">В команду входит параметр *Force* , который не позволяет команде выдать запрос на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="6b2d8-115">The command includes the *Force* parameter, which prevents the command from prompting you for confirmation.</span></span>

## <span data-ttu-id="6b2d8-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6b2d8-116">PARAMETERS</span></span>

### <span data-ttu-id="6b2d8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b2d8-117">-DefaultProfile</span></span>
<span data-ttu-id="6b2d8-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="6b2d8-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6b2d8-119">-Force</span><span class="sxs-lookup"><span data-stu-id="6b2d8-119">-Force</span></span>
<span data-ttu-id="6b2d8-120">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="6b2d8-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6b2d8-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6b2d8-121">-Name</span></span>
<span data-ttu-id="6b2d8-122">Указывает имя приложения логики, которое удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="6b2d8-122">Specifies the name of the logic app that this cmdlet removes.</span></span>

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

### <span data-ttu-id="6b2d8-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b2d8-123">-ResourceGroupName</span></span>
<span data-ttu-id="6b2d8-124">Указывает имя группы ресурсов, которая содержит логическое приложение, которое удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="6b2d8-124">Specifies the name of the resource group that contains the logic app that this cmdlet removes.</span></span>

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

### <span data-ttu-id="6b2d8-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6b2d8-125">-Confirm</span></span>
<span data-ttu-id="6b2d8-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6b2d8-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b2d8-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b2d8-127">-WhatIf</span></span>
<span data-ttu-id="6b2d8-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6b2d8-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b2d8-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6b2d8-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b2d8-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b2d8-130">CommonParameters</span></span>
<span data-ttu-id="6b2d8-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6b2d8-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b2d8-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b2d8-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b2d8-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6b2d8-133">INPUTS</span></span>

### <span data-ttu-id="6b2d8-134">System. String</span><span class="sxs-lookup"><span data-stu-id="6b2d8-134">System.String</span></span>

## <span data-ttu-id="6b2d8-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6b2d8-135">OUTPUTS</span></span>

### <span data-ttu-id="6b2d8-136">System. void</span><span class="sxs-lookup"><span data-stu-id="6b2d8-136">System.Void</span></span>

## <span data-ttu-id="6b2d8-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="6b2d8-137">NOTES</span></span>

## <span data-ttu-id="6b2d8-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6b2d8-138">RELATED LINKS</span></span>

[<span data-ttu-id="6b2d8-139">Get-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="6b2d8-139">Get-AzureRmLogicApp</span></span>](./Get-AzureRmLogicApp.md)

[<span data-ttu-id="6b2d8-140">New-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="6b2d8-140">New-AzureRmLogicApp</span></span>](./New-AzureRmLogicApp.md)

[<span data-ttu-id="6b2d8-141">Set-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="6b2d8-141">Set-AzureRmLogicApp</span></span>](./Set-AzureRmLogicApp.md)

[<span data-ttu-id="6b2d8-142">Start-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="6b2d8-142">Start-AzureRmLogicApp</span></span>](./Start-AzureRmLogicApp.md)



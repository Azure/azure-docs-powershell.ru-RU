---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 7AAF2ACC-84ED-449C-B1E8-F074463F44EB
online version: https://docs.microsoft.com/powershell/module/az.logicapp/remove-azintegrationaccountmap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountMap.md
ms.openlocfilehash: b74b0f21abcac3441b44ce167982bcca7c178dab
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992673"
---
# <span data-ttu-id="e42a2-101">Remove-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="e42a2-101">Remove-AzIntegrationAccountMap</span></span>

## <span data-ttu-id="e42a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e42a2-102">SYNOPSIS</span></span>
<span data-ttu-id="e42a2-103">Удаляет интеграцию с картой учетной записи.</span><span class="sxs-lookup"><span data-stu-id="e42a2-103">Removes an integration account map.</span></span>

## <span data-ttu-id="e42a2-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e42a2-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccountMap -ResourceGroupName <String> -Name <String> -MapName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e42a2-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e42a2-105">DESCRIPTION</span></span>
<span data-ttu-id="e42a2-106">При **этом из группы** ресурсов удаляется карта учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="e42a2-106">The **Remove-AzIntegrationAccountMap** cmdlet removes an integration account map from a resource group.</span></span>
<span data-ttu-id="e42a2-107">Укажите имя учетной записи интеграции, имя группы ресурсов и имя карты.</span><span class="sxs-lookup"><span data-stu-id="e42a2-107">Specify the integration account name, resource group name, and map name.</span></span>
<span data-ttu-id="e42a2-108">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="e42a2-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="e42a2-109">Чтобы использовать динамический параметр, введите его в команду.</span><span class="sxs-lookup"><span data-stu-id="e42a2-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="e42a2-110">Чтобы найти имена динамических параметров, введите дефис (-) после имени cmdlet, а затем нажимая клавишу TAB для циклическиго перебора доступных параметров.</span><span class="sxs-lookup"><span data-stu-id="e42a2-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="e42a2-111">Если параметр обязательного шаблона не задан, будет выдан запрос на его значение.</span><span class="sxs-lookup"><span data-stu-id="e42a2-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="e42a2-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e42a2-112">EXAMPLES</span></span>

### <span data-ttu-id="e42a2-113">Пример 1. Удаление карты учетной записи интеграции</span><span class="sxs-lookup"><span data-stu-id="e42a2-113">Example 1: Remove an integration account map</span></span>
```
PS C:\>Remove-AzIntegrationAccountMap -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -MapName "IntegrationAccountMap47"
```

<span data-ttu-id="e42a2-114">Эта команда удаляет карту учетной записи интеграции с именем IntegrationAccountMap47.</span><span class="sxs-lookup"><span data-stu-id="e42a2-114">This command removes the integration account map named IntegrationAccountMap47.</span></span>

## <span data-ttu-id="e42a2-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e42a2-115">PARAMETERS</span></span>

### <span data-ttu-id="e42a2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e42a2-116">-DefaultProfile</span></span>
<span data-ttu-id="e42a2-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="e42a2-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e42a2-118">-Force</span><span class="sxs-lookup"><span data-stu-id="e42a2-118">-Force</span></span>
<span data-ttu-id="e42a2-119">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="e42a2-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e42a2-120">-MapName</span><span class="sxs-lookup"><span data-stu-id="e42a2-120">-MapName</span></span>
<span data-ttu-id="e42a2-121">Указывает имя карты учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="e42a2-121">Specifies the name of the integration account map.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e42a2-122">-Name</span><span class="sxs-lookup"><span data-stu-id="e42a2-122">-Name</span></span>
<span data-ttu-id="e42a2-123">Указывает имя учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="e42a2-123">Specifies the name of the integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e42a2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e42a2-124">-ResourceGroupName</span></span>
<span data-ttu-id="e42a2-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e42a2-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="e42a2-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e42a2-126">-Confirm</span></span>
<span data-ttu-id="e42a2-127">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="e42a2-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e42a2-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e42a2-128">-WhatIf</span></span>
<span data-ttu-id="e42a2-129">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e42a2-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e42a2-130">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="e42a2-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e42a2-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e42a2-131">CommonParameters</span></span>
<span data-ttu-id="e42a2-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e42a2-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e42a2-133">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e42a2-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e42a2-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e42a2-134">INPUTS</span></span>

### <span data-ttu-id="e42a2-135">System.String</span><span class="sxs-lookup"><span data-stu-id="e42a2-135">System.String</span></span>

## <span data-ttu-id="e42a2-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e42a2-136">OUTPUTS</span></span>

### <span data-ttu-id="e42a2-137">System.Void</span><span class="sxs-lookup"><span data-stu-id="e42a2-137">System.Void</span></span>

## <span data-ttu-id="e42a2-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e42a2-138">NOTES</span></span>

## <span data-ttu-id="e42a2-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e42a2-139">RELATED LINKS</span></span>

[<span data-ttu-id="e42a2-140">Get-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="e42a2-140">Get-AzIntegrationAccountMap</span></span>](./Get-AzIntegrationAccountMap.md)

[<span data-ttu-id="e42a2-141">New-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="e42a2-141">New-AzIntegrationAccountMap</span></span>](./New-AzIntegrationAccountMap.md)

[<span data-ttu-id="e42a2-142">Set-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="e42a2-142">Set-AzIntegrationAccountMap</span></span>](./Set-AzIntegrationAccountMap.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 56550997-21D9-4F85-B23A-677625482547
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountSchema.md
ms.openlocfilehash: 50eab845d20d9bf95c20e94f6309be2a302f413c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98328582"
---
# <span data-ttu-id="b836e-101">Remove-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="b836e-101">Remove-AzIntegrationAccountSchema</span></span>

## <span data-ttu-id="b836e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b836e-102">SYNOPSIS</span></span>
<span data-ttu-id="b836e-103">Удаляет схему интеграции учетной записи.</span><span class="sxs-lookup"><span data-stu-id="b836e-103">Removes an integration account schema.</span></span>

## <span data-ttu-id="b836e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b836e-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccountSchema -ResourceGroupName <String> -Name <String> -SchemaName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b836e-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b836e-105">DESCRIPTION</span></span>
<span data-ttu-id="b836e-106">При **этом из группы** ресурсов удаляется схема учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="b836e-106">The **Remove-AzIntegrationAccountSchema** cmdlet removes an integration account schema from a resource group.</span></span>
<span data-ttu-id="b836e-107">Укажите имя учетной записи интеграции, имя группы ресурсов и имя схемы.</span><span class="sxs-lookup"><span data-stu-id="b836e-107">Specifying the integration account name, resource group name, and schema name.</span></span>
<span data-ttu-id="b836e-108">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="b836e-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="b836e-109">Чтобы использовать динамический параметр, введите его в команду.</span><span class="sxs-lookup"><span data-stu-id="b836e-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="b836e-110">Чтобы найти имена динамических параметров, введите дефис (-) после имени cmdlet, а затем нажимая клавишу TAB для циклическиго перебора доступных параметров.</span><span class="sxs-lookup"><span data-stu-id="b836e-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="b836e-111">Если параметр обязательного шаблона не задан, будет выдан запрос на его значение.</span><span class="sxs-lookup"><span data-stu-id="b836e-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="b836e-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b836e-112">EXAMPLES</span></span>

### <span data-ttu-id="b836e-113">Пример 1. Удаление схемы учетной записи интеграции</span><span class="sxs-lookup"><span data-stu-id="b836e-113">Example 1: Remove an integration account schema</span></span>
```
PS C:\>Remove-AzIntegrationAccountSchema -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -SchemaName "IntegrationAccountSchema43"
```

<span data-ttu-id="b836e-114">Эта команда удаляет схему интеграции учетной записи IntegrationAccountSchema43.</span><span class="sxs-lookup"><span data-stu-id="b836e-114">This command removes an integration account schema named IntegrationAccountSchema43.</span></span>

## <span data-ttu-id="b836e-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b836e-115">PARAMETERS</span></span>

### <span data-ttu-id="b836e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b836e-116">-DefaultProfile</span></span>
<span data-ttu-id="b836e-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="b836e-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b836e-118">-Force</span><span class="sxs-lookup"><span data-stu-id="b836e-118">-Force</span></span>
<span data-ttu-id="b836e-119">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="b836e-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b836e-120">-Name</span><span class="sxs-lookup"><span data-stu-id="b836e-120">-Name</span></span>
<span data-ttu-id="b836e-121">Указывает имя учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="b836e-121">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="b836e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b836e-122">-ResourceGroupName</span></span>
<span data-ttu-id="b836e-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b836e-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="b836e-124">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="b836e-124">-SchemaName</span></span>
<span data-ttu-id="b836e-125">Имя схемы учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="b836e-125">Specifies the name of an integration account schema.</span></span>

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

### <span data-ttu-id="b836e-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b836e-126">-Confirm</span></span>
<span data-ttu-id="b836e-127">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="b836e-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b836e-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b836e-128">-WhatIf</span></span>
<span data-ttu-id="b836e-129">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b836e-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b836e-130">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="b836e-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b836e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b836e-131">CommonParameters</span></span>
<span data-ttu-id="b836e-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b836e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b836e-133">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b836e-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b836e-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b836e-134">INPUTS</span></span>

### <span data-ttu-id="b836e-135">System.String</span><span class="sxs-lookup"><span data-stu-id="b836e-135">System.String</span></span>

## <span data-ttu-id="b836e-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b836e-136">OUTPUTS</span></span>

### <span data-ttu-id="b836e-137">System.Void</span><span class="sxs-lookup"><span data-stu-id="b836e-137">System.Void</span></span>

## <span data-ttu-id="b836e-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b836e-138">NOTES</span></span>

## <span data-ttu-id="b836e-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b836e-139">RELATED LINKS</span></span>

[<span data-ttu-id="b836e-140">Get-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="b836e-140">Get-AzIntegrationAccountSchema</span></span>](./Get-AzIntegrationAccountSchema.md)

[<span data-ttu-id="b836e-141">New-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="b836e-141">New-AzIntegrationAccountSchema</span></span>](./New-AzIntegrationAccountSchema.md)

[<span data-ttu-id="b836e-142">Set-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="b836e-142">Set-AzIntegrationAccountSchema</span></span>](./Set-AzIntegrationAccountSchema.md)



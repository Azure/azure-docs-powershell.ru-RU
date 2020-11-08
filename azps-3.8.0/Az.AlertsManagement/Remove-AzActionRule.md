---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/remove-azactionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Remove-AzActionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Remove-AzActionRule.md
ms.openlocfilehash: 1cdea9a2d5deb9fbe93da0a090070f7ed1b07653
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065667"
---
# <span data-ttu-id="1c208-101">Remove-AzActionRule</span><span class="sxs-lookup"><span data-stu-id="1c208-101">Remove-AzActionRule</span></span>

## <span data-ttu-id="1c208-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1c208-102">SYNOPSIS</span></span>
<span data-ttu-id="1c208-103">Удаление правила действия</span><span class="sxs-lookup"><span data-stu-id="1c208-103">Deletes a action rule</span></span>

## <span data-ttu-id="1c208-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1c208-104">SYNTAX</span></span>

### <span data-ttu-id="1c208-105">ByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1c208-105">ByName (Default)</span></span>
```
Remove-AzActionRule -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c208-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="1c208-106">ByResourceId</span></span>
```
Remove-AzActionRule -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c208-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="1c208-107">ByInputObject</span></span>
```
Remove-AzActionRule -InputObject <PSActionRule> [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c208-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1c208-108">DESCRIPTION</span></span>
<span data-ttu-id="1c208-109">Командлет **Remove-AzActionRule** удаляет правило действия.</span><span class="sxs-lookup"><span data-stu-id="1c208-109">**Remove-AzActionRule** cmdlet deletes a action rule.</span></span>

## <span data-ttu-id="1c208-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1c208-110">EXAMPLES</span></span>

### <span data-ttu-id="1c208-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1c208-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzActionRule -ResourceGroupName "test-rg" -Name "ActionRuleName"
```

<span data-ttu-id="1c208-112">Этот командлет удаляет правило действия с именем ActionRuleName в группе ресурсов Test-RG</span><span class="sxs-lookup"><span data-stu-id="1c208-112">This cmdlet deletes the action rule with name ActionRuleName in resource group test-rg</span></span>

## <span data-ttu-id="1c208-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1c208-113">PARAMETERS</span></span>

### <span data-ttu-id="1c208-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c208-114">-DefaultProfile</span></span>
<span data-ttu-id="1c208-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1c208-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c208-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1c208-116">-InputObject</span></span>
<span data-ttu-id="1c208-117">Ресурс правила действий</span><span class="sxs-lookup"><span data-stu-id="1c208-117">The action rule resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1c208-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1c208-118">-Name</span></span>
<span data-ttu-id="1c208-119">Имя правила действия</span><span class="sxs-lookup"><span data-stu-id="1c208-119">Name of action rule</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c208-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1c208-120">-PassThru</span></span>
<span data-ttu-id="1c208-121">Функция PassThru возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="1c208-121">PassThru returns an object representing the item with which you are working.</span></span> <span data-ttu-id="1c208-122">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="1c208-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="1c208-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c208-123">-ResourceGroupName</span></span>
<span data-ttu-id="1c208-124">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="1c208-124">Resource Group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c208-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1c208-125">-ResourceId</span></span>
<span data-ttu-id="1c208-126">Получить правило действия по идентификатору изображение.</span><span class="sxs-lookup"><span data-stu-id="1c208-126">Get Action rule by resoure id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c208-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1c208-127">-Confirm</span></span>
<span data-ttu-id="1c208-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1c208-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c208-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c208-129">-WhatIf</span></span>
<span data-ttu-id="1c208-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1c208-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c208-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1c208-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c208-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c208-132">CommonParameters</span></span>
<span data-ttu-id="1c208-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1c208-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c208-134">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1c208-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c208-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1c208-135">INPUTS</span></span>

### <span data-ttu-id="1c208-136">Microsoft. Azure. Commands. AlertsManagement. OutputModels. PSActionRule</span><span class="sxs-lookup"><span data-stu-id="1c208-136">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="1c208-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1c208-137">OUTPUTS</span></span>

### <span data-ttu-id="1c208-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1c208-138">System.Boolean</span></span>

## <span data-ttu-id="1c208-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="1c208-139">NOTES</span></span>

## <span data-ttu-id="1c208-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1c208-140">RELATED LINKS</span></span>

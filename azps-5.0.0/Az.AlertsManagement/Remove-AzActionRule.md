---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/remove-azactionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Remove-AzActionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Remove-AzActionRule.md
ms.openlocfilehash: 4462434bcda1045afcc8478bbd9c4b7a1718d478
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247947"
---
# <span data-ttu-id="dc555-101">Remove-AzActionRule</span><span class="sxs-lookup"><span data-stu-id="dc555-101">Remove-AzActionRule</span></span>

## <span data-ttu-id="dc555-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dc555-102">SYNOPSIS</span></span>
<span data-ttu-id="dc555-103">Удаление правила действия</span><span class="sxs-lookup"><span data-stu-id="dc555-103">Deletes a action rule</span></span>

## <span data-ttu-id="dc555-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dc555-104">SYNTAX</span></span>

### <span data-ttu-id="dc555-105">ByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="dc555-105">ByName (Default)</span></span>
```
Remove-AzActionRule -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc555-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="dc555-106">ByResourceId</span></span>
```
Remove-AzActionRule -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc555-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="dc555-107">ByInputObject</span></span>
```
Remove-AzActionRule -InputObject <PSActionRule> [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dc555-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dc555-108">DESCRIPTION</span></span>
<span data-ttu-id="dc555-109">Командлет **Remove-AzActionRule** удаляет правило действия.</span><span class="sxs-lookup"><span data-stu-id="dc555-109">**Remove-AzActionRule** cmdlet deletes a action rule.</span></span>

## <span data-ttu-id="dc555-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dc555-110">EXAMPLES</span></span>

### <span data-ttu-id="dc555-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="dc555-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzActionRule -ResourceGroupName "test-rg" -Name "ActionRuleName"
```

<span data-ttu-id="dc555-112">Этот командлет удаляет правило действия с именем ActionRuleName в группе ресурсов Test-RG</span><span class="sxs-lookup"><span data-stu-id="dc555-112">This cmdlet deletes the action rule with name ActionRuleName in resource group test-rg</span></span>

## <span data-ttu-id="dc555-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dc555-113">PARAMETERS</span></span>

### <span data-ttu-id="dc555-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc555-114">-DefaultProfile</span></span>
<span data-ttu-id="dc555-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dc555-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc555-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dc555-116">-InputObject</span></span>
<span data-ttu-id="dc555-117">Ресурс правила действий</span><span class="sxs-lookup"><span data-stu-id="dc555-117">The action rule resource</span></span>

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

### <span data-ttu-id="dc555-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="dc555-118">-Name</span></span>
<span data-ttu-id="dc555-119">Имя правила действия</span><span class="sxs-lookup"><span data-stu-id="dc555-119">Name of action rule</span></span>

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

### <span data-ttu-id="dc555-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dc555-120">-PassThru</span></span>
<span data-ttu-id="dc555-121">Функция PassThru возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="dc555-121">PassThru returns an object representing the item with which you are working.</span></span> <span data-ttu-id="dc555-122">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="dc555-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="dc555-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc555-123">-ResourceGroupName</span></span>
<span data-ttu-id="dc555-124">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="dc555-124">Resource Group name</span></span>

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

### <span data-ttu-id="dc555-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dc555-125">-ResourceId</span></span>
<span data-ttu-id="dc555-126">Получить правило действия по идентификатору ресурса.</span><span class="sxs-lookup"><span data-stu-id="dc555-126">Get Action rule by resource id.</span></span>

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

### <span data-ttu-id="dc555-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dc555-127">-Confirm</span></span>
<span data-ttu-id="dc555-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="dc555-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc555-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc555-129">-WhatIf</span></span>
<span data-ttu-id="dc555-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="dc555-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc555-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="dc555-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc555-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc555-132">CommonParameters</span></span>
<span data-ttu-id="dc555-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dc555-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc555-134">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dc555-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc555-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dc555-135">INPUTS</span></span>

### <span data-ttu-id="dc555-136">Microsoft. Azure. Commands. AlertsManagement. OutputModels. PSActionRule</span><span class="sxs-lookup"><span data-stu-id="dc555-136">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="dc555-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dc555-137">OUTPUTS</span></span>

### <span data-ttu-id="dc555-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="dc555-138">System.Boolean</span></span>

## <span data-ttu-id="dc555-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="dc555-139">NOTES</span></span>

## <span data-ttu-id="dc555-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dc555-140">RELATED LINKS</span></span>

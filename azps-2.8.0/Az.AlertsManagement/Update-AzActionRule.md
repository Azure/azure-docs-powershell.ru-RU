---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/update-azactionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzActionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzActionRule.md
ms.openlocfilehash: 9991829a70029366086a58020aa53f839db8b6c3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93728180"
---
# <span data-ttu-id="0db06-101">Update-AzActionRule</span><span class="sxs-lookup"><span data-stu-id="0db06-101">Update-AzActionRule</span></span>

## <span data-ttu-id="0db06-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0db06-102">SYNOPSIS</span></span>
<span data-ttu-id="0db06-103">Обновляет свойства правила действия.</span><span class="sxs-lookup"><span data-stu-id="0db06-103">Updates action rule properties.</span></span>

## <span data-ttu-id="0db06-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0db06-104">SYNTAX</span></span>

### <span data-ttu-id="0db06-105">ByNameSimplifiedPatch (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0db06-105">ByNameSimplifiedPatch (Default)</span></span>
```
Update-AzActionRule -Name <String> -ResourceGroupName <String> [-Status <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0db06-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="0db06-106">ByResourceId</span></span>
```
Update-AzActionRule -ResourceId <String> [-Status <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0db06-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="0db06-107">ByInputObject</span></span>
```
Update-AzActionRule -InputObject <PSActionRule> [-Status <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0db06-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0db06-108">DESCRIPTION</span></span>
<span data-ttu-id="0db06-109">Командлет **Update-AzActionRule** обновляет свойства правила действия — status и Tags.</span><span class="sxs-lookup"><span data-stu-id="0db06-109">**Update-AzActionRule** cmdlet updates action rule properties - status and tags.</span></span>

## <span data-ttu-id="0db06-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0db06-110">EXAMPLES</span></span>

### <span data-ttu-id="0db06-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0db06-111">Example 1</span></span>
```powershell
PS C:\> Update-AzActionRule -ResourceGroupName "test-rg" -Name "Test-ActionRule" -Status "Disabled"
```

<span data-ttu-id="0db06-112">Этот командлет отключает правило действия.</span><span class="sxs-lookup"><span data-stu-id="0db06-112">This cmdlet disables the action rule.</span></span> 

## <span data-ttu-id="0db06-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0db06-113">PARAMETERS</span></span>

### <span data-ttu-id="0db06-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0db06-114">-DefaultProfile</span></span>
<span data-ttu-id="0db06-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0db06-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0db06-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0db06-116">-InputObject</span></span>
<span data-ttu-id="0db06-117">Ресурс правила действий</span><span class="sxs-lookup"><span data-stu-id="0db06-117">The action rule resource</span></span>

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

### <span data-ttu-id="0db06-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0db06-118">-Name</span></span>
<span data-ttu-id="0db06-119">Имя правила действия</span><span class="sxs-lookup"><span data-stu-id="0db06-119">Action rule name</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameSimplifiedPatch
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0db06-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0db06-120">-ResourceGroupName</span></span>
<span data-ttu-id="0db06-121">Имя правила действия</span><span class="sxs-lookup"><span data-stu-id="0db06-121">Action rule name</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameSimplifiedPatch
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0db06-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0db06-122">-ResourceId</span></span>
<span data-ttu-id="0db06-123">Идентификатор ресурса для правила действия</span><span class="sxs-lookup"><span data-stu-id="0db06-123">The resource id of action rule</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0db06-124">-Status (состояние)</span><span class="sxs-lookup"><span data-stu-id="0db06-124">-Status</span></span>
<span data-ttu-id="0db06-125">Состояние правила действия</span><span class="sxs-lookup"><span data-stu-id="0db06-125">Action rule status</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0db06-126">-Тег</span><span class="sxs-lookup"><span data-stu-id="0db06-126">-Tag</span></span>
<span data-ttu-id="0db06-127">Теги правила действия</span><span class="sxs-lookup"><span data-stu-id="0db06-127">Action rule tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0db06-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0db06-128">-Confirm</span></span>
<span data-ttu-id="0db06-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0db06-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0db06-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0db06-130">-WhatIf</span></span>
<span data-ttu-id="0db06-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0db06-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0db06-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0db06-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0db06-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0db06-133">CommonParameters</span></span>
<span data-ttu-id="0db06-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0db06-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0db06-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0db06-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0db06-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0db06-136">INPUTS</span></span>

### <span data-ttu-id="0db06-137">System. String</span><span class="sxs-lookup"><span data-stu-id="0db06-137">System.String</span></span>

### <span data-ttu-id="0db06-138">Microsoft. Azure. Commands. AlertsManagement. OutputModels. PSActionRule</span><span class="sxs-lookup"><span data-stu-id="0db06-138">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="0db06-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0db06-139">OUTPUTS</span></span>

### <span data-ttu-id="0db06-140">Microsoft. Azure. Commands. AlertsManagement. OutputModels. PSActionRule</span><span class="sxs-lookup"><span data-stu-id="0db06-140">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="0db06-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="0db06-141">NOTES</span></span>

## <span data-ttu-id="0db06-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0db06-142">RELATED LINKS</span></span>

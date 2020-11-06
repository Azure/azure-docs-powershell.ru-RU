---
external help file: Microsoft.Azure.Commands.Consumption.dll-Help.xml
Module Name: AzureRM.Consumption
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.consumption/remove-azurermconsumptionbudget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Consumption/Commands.Consumption/help/Remove-AzureRmConsumptionBudget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Consumption/Commands.Consumption/help/Remove-AzureRmConsumptionBudget.md
ms.openlocfilehash: b14afecc7f31f878b4ce1598f8b135265ff72249
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567788"
---
# <span data-ttu-id="13fcc-101">Remove-AzureRmConsumptionBudget</span><span class="sxs-lookup"><span data-stu-id="13fcc-101">Remove-AzureRmConsumptionBudget</span></span>

## <span data-ttu-id="13fcc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="13fcc-102">SYNOPSIS</span></span>
<span data-ttu-id="13fcc-103">Удаление бюджета либо в подписке, либо в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="13fcc-103">Remove a budget in either a subscription or a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="13fcc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="13fcc-104">SYNTAX</span></span>

### <span data-ttu-id="13fcc-105">Подписка (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="13fcc-105">Subscription (Default)</span></span>
```
Remove-AzureRmConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String>
 [-ResourceGroupName <String>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13fcc-106">Трубодержателей</span><span class="sxs-lookup"><span data-stu-id="13fcc-106">Piping</span></span>
```
Remove-AzureRmConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -InputObject <PSBudget> [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13fcc-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="13fcc-107">DESCRIPTION</span></span>
<span data-ttu-id="13fcc-108">Командлет Remove-AzureRmConsumptionBudget удаляет бюджет либо в подписке, либо в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="13fcc-108">The Remove-AzureRmConsumptionBudget cmdlet removes a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="13fcc-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="13fcc-109">EXAMPLES</span></span>

### <span data-ttu-id="13fcc-110">Пример 1: удаление бюджета с именем бюджета на уровне подписки</span><span class="sxs-lookup"><span data-stu-id="13fcc-110">Example 1: Remove a budget with a budget name at subscription level</span></span>
```powershell
PS C:\> Remove-AzureRmConsumptionBudget -Name PSBudget -PassThru
True
```

### <span data-ttu-id="13fcc-111">Пример 2: удаление бюджета с именем бюджета на уровне группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="13fcc-111">Example 2: Remove a budget with a budget name at resource group level</span></span>
```powershell
PS C:\> Remove-AzureRmConsumptionBudget -ResourceGroupName RGBudgets -Name PSBudgetRG -PassThru
True
```

### <span data-ttu-id="13fcc-112">Пример 3: удаление бюджета с помощью трубопроводов на уровне подписки</span><span class="sxs-lookup"><span data-stu-id="13fcc-112">Example 3: Remove a budget through piping at subscription level</span></span>
```powershell
PS C:\> Get-AzureRmConsumptionBudget -Name PSBudget | Remove-AzureRmConsumptionBudget -PassThru
True
```

## <span data-ttu-id="13fcc-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="13fcc-113">PARAMETERS</span></span>

### <span data-ttu-id="13fcc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13fcc-114">-DefaultProfile</span></span>
<span data-ttu-id="13fcc-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="13fcc-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13fcc-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="13fcc-116">-InputObject</span></span>
<span data-ttu-id="13fcc-117">Объект бюджета.</span><span class="sxs-lookup"><span data-stu-id="13fcc-117">Budget object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Consumption.Models.PSBudget
Parameter Sets: Piping
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="13fcc-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="13fcc-118">-Name</span></span>
<span data-ttu-id="13fcc-119">Название бюджета.</span><span class="sxs-lookup"><span data-stu-id="13fcc-119">Name of a budget.</span></span>

```yaml
Type: System.String
Parameter Sets: Subscription
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13fcc-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="13fcc-120">-PassThru</span></span>
<span data-ttu-id="13fcc-121">Командлет возвращает значение true, если бюджет был успешно удален.</span><span class="sxs-lookup"><span data-stu-id="13fcc-121">The Cmdlet returns true if a budget was successfully removed.</span></span>

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

### <span data-ttu-id="13fcc-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13fcc-122">-ResourceGroupName</span></span>
<span data-ttu-id="13fcc-123">Группа ресурсов бюджета.</span><span class="sxs-lookup"><span data-stu-id="13fcc-123">Resource Group of a budget.</span></span>

```yaml
Type: System.String
Parameter Sets: Subscription
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13fcc-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="13fcc-124">-Confirm</span></span>
<span data-ttu-id="13fcc-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="13fcc-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13fcc-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13fcc-126">-WhatIf</span></span>
<span data-ttu-id="13fcc-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="13fcc-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13fcc-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="13fcc-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13fcc-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13fcc-129">CommonParameters</span></span>
<span data-ttu-id="13fcc-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="13fcc-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13fcc-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13fcc-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13fcc-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="13fcc-132">INPUTS</span></span>

### <span data-ttu-id="13fcc-133">Microsoft. Azure. Commands. потребление. Models. PSBudget</span><span class="sxs-lookup"><span data-stu-id="13fcc-133">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>
<span data-ttu-id="13fcc-134">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="13fcc-134">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="13fcc-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="13fcc-135">OUTPUTS</span></span>

### <span data-ttu-id="13fcc-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="13fcc-136">System.Boolean</span></span>

## <span data-ttu-id="13fcc-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="13fcc-137">NOTES</span></span>

## <span data-ttu-id="13fcc-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="13fcc-138">RELATED LINKS</span></span>

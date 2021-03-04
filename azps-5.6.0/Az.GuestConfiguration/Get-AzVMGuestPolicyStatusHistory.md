---
external help file: Microsoft.Azure.PowerShell.Cmdlets.GuestConfiguration.dll-Help.xml
Module Name: Az.GuestConfiguration
online version: https://docs.microsoft.com/powershell/module/az.guestconfiguration/get-azvmguestpolicystatushistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatusHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatusHistory.md
ms.openlocfilehash: 9161b3c9c55c1014b64419a3644bf7ec80af8648
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990198"
---
# <span data-ttu-id="49700-101">Get-AzVMGuestPolicyStatusHistory</span><span class="sxs-lookup"><span data-stu-id="49700-101">Get-AzVMGuestPolicyStatusHistory</span></span>

## <span data-ttu-id="49700-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49700-102">SYNOPSIS</span></span>
<span data-ttu-id="49700-103">Возвращает историю состояния соответствия политики гостевой конфигурации инициативе типа "Гостевая конфигурация", которая назначена VM.</span><span class="sxs-lookup"><span data-stu-id="49700-103">Gets guest configuration policy compliance status history for an initiative of type "Guest Configuration" that is assigned to a VM.</span></span>
<span data-ttu-id="49700-104">Инициатива — это политика определения типа "Инициатива".</span><span class="sxs-lookup"><span data-stu-id="49700-104">An initiative is a policy of definition type "Initiative".</span></span>

## <span data-ttu-id="49700-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="49700-105">SYNTAX</span></span>

### <span data-ttu-id="49700-106">InitiativeNameScope (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="49700-106">InitiativeNameScope (Default)</span></span>
```
Get-AzVMGuestPolicyStatusHistory [-ResourceGroupName] <String> [-VMName] <String> [-InitiativeName] <String>
 [-ShowOnlyChange] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="49700-107">InitiativeIdScope</span><span class="sxs-lookup"><span data-stu-id="49700-107">InitiativeIdScope</span></span>
```
Get-AzVMGuestPolicyStatusHistory [-ResourceGroupName] <String> [-VMName] <String> [[-InitiativeId] <String>]
 [-ShowOnlyChange] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="49700-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="49700-108">DESCRIPTION</span></span>
<span data-ttu-id="49700-109">Этот Get-AzVMGuestPolicyStatusHistory получает историю состояния соответствия политик гостевой конфигурации инициативе типа "Гостевая конфигурация", которая назначена VM-устройству.</span><span class="sxs-lookup"><span data-stu-id="49700-109">The Get-AzVMGuestPolicyStatusHistory cmdlet gets compliance status history of guest configuration policies for an initiative of type "Guest Configuration" that is assigned to a VM.</span></span>
<span data-ttu-id="49700-110">Инициатива — это политика типа определения "Инициатива".</span><span class="sxs-lookup"><span data-stu-id="49700-110">An initiative is a policy of definition type "Initiative".</span></span>
<span data-ttu-id="49700-111">Используйте Get-AzVMGuestPolicyStatus для получения сведений об одном состоянии соответствия требованиям с помощью ReportId, которые можно найти в результатах Get-AzVMGuestPolicyStatusHistory выполнения.</span><span class="sxs-lookup"><span data-stu-id="49700-111">Use Get-AzVMGuestPolicyStatus cmdlet to get details of a single compliance status using ReportId that can be found in output of Get-AzVMGuestPolicyStatusHistory cmdlet.</span></span>

## <span data-ttu-id="49700-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="49700-112">EXAMPLES</span></span>

### <span data-ttu-id="49700-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="49700-113">Example 1</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeId "/providers/Microsoft.Authorization/policySetDefinitions/3fa7cbf5-c0a4-4a59-85a5-cca4d996d5af" -ShowOnlyChange
```

<span data-ttu-id="49700-114">Возвращает историю состояния соответствия по ИД инициатив. Переключатель ShowOnlyChange показывает только исторические изменения состояния.</span><span class="sxs-lookup"><span data-stu-id="49700-114">Gets compliance status history by initiative Id. ShowOnlyChange switch shows only historical status changes.</span></span>
<span data-ttu-id="49700-115">Пропускает состояния, которые не изменялись при двух проверках соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="49700-115">Skips statuses that have not changed between two compliance checks.</span></span>

### <span data-ttu-id="49700-116">Пример 2</span><span class="sxs-lookup"><span data-stu-id="49700-116">Example 2</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeName "b5a822e0-ba98-4e54-9278-5d9833aa9b17" -ShowOnlyChange
```

<span data-ttu-id="49700-117">Возвращает историю состояния соответствия по имени инициатив.</span><span class="sxs-lookup"><span data-stu-id="49700-117">Gets compliance status history by initiative name.</span></span>
<span data-ttu-id="49700-118">Переключатель ShowOnlyChange отображает только исторические изменения.</span><span class="sxs-lookup"><span data-stu-id="49700-118">ShowOnlyChange switch shows only historical status changes.</span></span>
<span data-ttu-id="49700-119">Пропускает состояния, которые не изменялись при двух проверках соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="49700-119">Skips statuses that have not changed between two compliance checks.</span></span>

### <span data-ttu-id="49700-120">Пример 3</span><span class="sxs-lookup"><span data-stu-id="49700-120">Example 3</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -ShowOnlyChange
```

<span data-ttu-id="49700-121">Возвращает историю состояния соответствия всем политикам настройки гостей, которые назначены VM.</span><span class="sxs-lookup"><span data-stu-id="49700-121">Gets compliance status history for all guest configuration policies assigned to the VM.</span></span>
<span data-ttu-id="49700-122">Переключатель ShowOnlyChange отображает только исторические изменения.</span><span class="sxs-lookup"><span data-stu-id="49700-122">ShowOnlyChange switch shows only historical status changes.</span></span>
<span data-ttu-id="49700-123">Пропускает состояния, которые не изменялись при двух проверках соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="49700-123">Skips statuses that have not changed between two compliance checks.</span></span>

### <span data-ttu-id="49700-124">Пример 4</span><span class="sxs-lookup"><span data-stu-id="49700-124">Example 4</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeId "/providers/Microsoft.Authorization/policySetDefinitions/3fa7cbf5-c0a4-4a59-85a5-cca4d996d5af"
```

<span data-ttu-id="49700-125">Возвращает историю состояния соответствия по ИД инициатив.</span><span class="sxs-lookup"><span data-stu-id="49700-125">Gets compliance status history by initiative Id.</span></span>

### <span data-ttu-id="49700-126">Пример 5</span><span class="sxs-lookup"><span data-stu-id="49700-126">Example 5</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeName "b5a822e0-ba98-4e54-9278-5d9833aa9b17"
```

<span data-ttu-id="49700-127">Возвращает историю состояния соответствия по имени инициатив.</span><span class="sxs-lookup"><span data-stu-id="49700-127">Gets compliance status history by initiative name.</span></span>

### <span data-ttu-id="49700-128">Пример 6</span><span class="sxs-lookup"><span data-stu-id="49700-128">Example 6</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName"
```
<span data-ttu-id="49700-129">Возвращает историю состояния соответствия всем политикам настройки гостей, которые назначены VM.</span><span class="sxs-lookup"><span data-stu-id="49700-129">Gets compliance status history for all guest configuration policies assigned to the VM.</span></span>

### <span data-ttu-id="49700-130">Пример 7</span><span class="sxs-lookup"><span data-stu-id="49700-130">Example 7</span></span>
```powershell
PS C:\>$x = Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName"
PS C:\>$x[10].ReportId
/subscriptions/4e6c6ed2-0bf6-41d7-9d21-a452c2cc7920/resourceGroups/MyResourceGroupName/providers/Microsoft.Compute/virtualMachines/MyVMName/providers/Microsoft.GuestConfiguration/guestConfigurationAssignments/MaximumPasswordAge/reports/c271f845-2c0a-4456-a441-e48fc332d0ac
PS C:\> Get-AzVMGuestPolicyStatus -ReportId $x[10].ReportId
```

<span data-ttu-id="49700-131">Получите состояние политики настройки гостей по ReportId.</span><span class="sxs-lookup"><span data-stu-id="49700-131">Get guest configuration policy status by ReportId.</span></span>
<span data-ttu-id="49700-132">ReportId — это свойство ReportId, которое можно найти в результатах get-AzVMGuestPolicyStatusHistory.</span><span class="sxs-lookup"><span data-stu-id="49700-132">The ReportId is the ReportId property that can be found in the results of Get-AzVMGuestPolicyStatusHistory.</span></span> <span data-ttu-id="49700-133">(обратитесь к другим примерам)</span><span class="sxs-lookup"><span data-stu-id="49700-133">(please refer other examples)</span></span>

## <span data-ttu-id="49700-134">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="49700-134">PARAMETERS</span></span>

### <span data-ttu-id="49700-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49700-135">-DefaultProfile</span></span>
<span data-ttu-id="49700-136">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="49700-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49700-137">-InitiativeId</span><span class="sxs-lookup"><span data-stu-id="49700-137">-InitiativeId</span></span>
<span data-ttu-id="49700-138">Определение ИД политики, в которой тип определения — Initiative, а категория — Guest Configuration</span><span class="sxs-lookup"><span data-stu-id="49700-138">Definition Id of a policy where definition type is Initiative and category is Guest Configuration</span></span>

```yaml
Type: System.String
Parameter Sets: InitiativeIdScope
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49700-139">-InitiativeName</span><span class="sxs-lookup"><span data-stu-id="49700-139">-InitiativeName</span></span>
<span data-ttu-id="49700-140">Имя политики, для которой тип определения — Initiative, а категория — Guest Configuration</span><span class="sxs-lookup"><span data-stu-id="49700-140">Name of a policy where definition type is Initiative and category is Guest Configuration</span></span>

```yaml
Type: System.String
Parameter Sets: InitiativeNameScope
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49700-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49700-141">-ResourceGroupName</span></span>
<span data-ttu-id="49700-142">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="49700-142">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49700-143">-ShowOnlyChange</span><span class="sxs-lookup"><span data-stu-id="49700-143">-ShowOnlyChange</span></span>
<span data-ttu-id="49700-144">Отображает исторические изменения состояния только для политик настройки гостей.</span><span class="sxs-lookup"><span data-stu-id="49700-144">Shows historical status changes only for guest configuration policies.</span></span>
<span data-ttu-id="49700-145">Пропускает состояния, которые не изменились между двумя аудитами состояния соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="49700-145">Skips statuses that have not changed between two compliance status audit runs.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49700-146">-VMName</span><span class="sxs-lookup"><span data-stu-id="49700-146">-VMName</span></span>
<span data-ttu-id="49700-147">Имя VM.</span><span class="sxs-lookup"><span data-stu-id="49700-147">VM name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49700-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49700-148">CommonParameters</span></span>
<span data-ttu-id="49700-149">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49700-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49700-150">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49700-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49700-151">INPUTS</span><span class="sxs-lookup"><span data-stu-id="49700-151">INPUTS</span></span>

### <span data-ttu-id="49700-152">Нет</span><span class="sxs-lookup"><span data-stu-id="49700-152">None</span></span>
## <span data-ttu-id="49700-153">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="49700-153">OUTPUTS</span></span>

### <span data-ttu-id="49700-154">Microsoft.Azure.Commands.GuestConfiguration.Models.PolicyStatus</span><span class="sxs-lookup"><span data-stu-id="49700-154">Microsoft.Azure.Commands.GuestConfiguration.Models.PolicyStatus</span></span>
## <span data-ttu-id="49700-155">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="49700-155">NOTES</span></span>

## <span data-ttu-id="49700-156">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="49700-156">RELATED LINKS</span></span>

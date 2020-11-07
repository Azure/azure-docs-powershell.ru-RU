---
external help file: Microsoft.Azure.PowerShell.Cmdlets.GuestConfiguration.dll-Help.xml
Module Name: Az.GuestConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.guestconfiguration/get-azvmguestpolicystatushistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatusHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatusHistory.md
ms.openlocfilehash: 2e2474b784d66c3c3c34bc9ea9abc2b0959ea500
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720859"
---
# <span data-ttu-id="6a9a6-101">Get-AzVMGuestPolicyStatusHistory</span><span class="sxs-lookup"><span data-stu-id="6a9a6-101">Get-AzVMGuestPolicyStatusHistory</span></span>

## <span data-ttu-id="6a9a6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6a9a6-102">SYNOPSIS</span></span>
<span data-ttu-id="6a9a6-103">Получение журнала состояния соответствия политике настройки гостевой конфигурации для инициативы типа "Гостевая конфигурация", назначенной ВМ.</span><span class="sxs-lookup"><span data-stu-id="6a9a6-103">Gets guest configuration policy compliance status history for an initiative of type "Guest Configuration" that is assigned to a VM.</span></span>
<span data-ttu-id="6a9a6-104">Инициатива — это политика типа определения "инициатива".</span><span class="sxs-lookup"><span data-stu-id="6a9a6-104">An initiative is a policy of definition type "Initiative".</span></span>

## <span data-ttu-id="6a9a6-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6a9a6-105">SYNTAX</span></span>

### <span data-ttu-id="6a9a6-106">InitiativeNameScope (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6a9a6-106">InitiativeNameScope (Default)</span></span>
```
Get-AzVMGuestPolicyStatusHistory [-ResourceGroupName] <String> [-VMName] <String> [-InitiativeName] <String>
 [-ShowOnlyChange] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6a9a6-107">InitiativeIdScope</span><span class="sxs-lookup"><span data-stu-id="6a9a6-107">InitiativeIdScope</span></span>
```
Get-AzVMGuestPolicyStatusHistory [-ResourceGroupName] <String> [-VMName] <String> [[-InitiativeId] <String>]
 [-ShowOnlyChange] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6a9a6-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6a9a6-108">DESCRIPTION</span></span>
<span data-ttu-id="6a9a6-109">Командлет Get-AzVMGuestPolicyStatusHistory получает историю состояния соответствия политик настройки гостевой конфигурации для инициативы типа "Гостевая конфигурация", назначенной виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="6a9a6-109">The Get-AzVMGuestPolicyStatusHistory cmdlet gets compliance status history of guest configuration policies for an initiative of type "Guest Configuration" that is assigned to a VM.</span></span>
<span data-ttu-id="6a9a6-110">Инициатива — это политика типа определения "инициатива".</span><span class="sxs-lookup"><span data-stu-id="6a9a6-110">An initiative is a policy of definition type "Initiative".</span></span>
<span data-ttu-id="6a9a6-111">Используйте Get-AzVMGuestPolicyStatusный командлет, чтобы получить сведения о состоянии одного соответствия с помощью ReportId, которое можно найти в выходных данных командлета Get-AzVMGuestPolicyStatusHistory.</span><span class="sxs-lookup"><span data-stu-id="6a9a6-111">Use Get-AzVMGuestPolicyStatus cmdlet to get details of a single compliance status using ReportId that can be found in output of Get-AzVMGuestPolicyStatusHistory cmdlet.</span></span>

## <span data-ttu-id="6a9a6-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6a9a6-112">EXAMPLES</span></span>

### <span data-ttu-id="6a9a6-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6a9a6-113">Example 1</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeId "/providers/Microsoft.Authorization/policySetDefinitions/3fa7cbf5-c0a4-4a59-85a5-cca4d996d5af" -ShowOnlyChange
```

<span data-ttu-id="6a9a6-114">Возвращает историю состояния соответствия по инициативе ID. ShowOnlyChange — отображаются только исторические изменения состояния.</span><span class="sxs-lookup"><span data-stu-id="6a9a6-114">Gets compliance status history by initiative Id. ShowOnlyChange switch shows only historical status changes.</span></span>
<span data-ttu-id="6a9a6-115">Пропускает состояние, которое не изменилось между двумя проверками соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="6a9a6-115">Skips statuses that have not changed between two compliance checks.</span></span>

### <span data-ttu-id="6a9a6-116">Пример 2</span><span class="sxs-lookup"><span data-stu-id="6a9a6-116">Example 2</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeName "b5a822e0-ba98-4e54-9278-5d9833aa9b17" -ShowOnlyChange
```

<span data-ttu-id="6a9a6-117">Возвращает историю состояния соответствия по названию инициативы.</span><span class="sxs-lookup"><span data-stu-id="6a9a6-117">Gets compliance status history by initiative name.</span></span>
<span data-ttu-id="6a9a6-118">В ShowOnlyChange Switch отображаются только исторические изменения состояния.</span><span class="sxs-lookup"><span data-stu-id="6a9a6-118">ShowOnlyChange switch shows only historical status changes.</span></span>
<span data-ttu-id="6a9a6-119">Пропускает состояние, которое не изменилось между двумя проверками соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="6a9a6-119">Skips statuses that have not changed between two compliance checks.</span></span>

### <span data-ttu-id="6a9a6-120">Пример 3</span><span class="sxs-lookup"><span data-stu-id="6a9a6-120">Example 3</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -ShowOnlyChange
```

<span data-ttu-id="6a9a6-121">Возвращает историю состояния соответствия для всех политик настройки гостевой конфигурации, назначенных виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="6a9a6-121">Gets compliance status history for all guest configuration policies assigned to the VM.</span></span>
<span data-ttu-id="6a9a6-122">В ShowOnlyChange Switch отображаются только исторические изменения состояния.</span><span class="sxs-lookup"><span data-stu-id="6a9a6-122">ShowOnlyChange switch shows only historical status changes.</span></span>
<span data-ttu-id="6a9a6-123">Пропускает состояние, которое не изменилось между двумя проверками соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="6a9a6-123">Skips statuses that have not changed between two compliance checks.</span></span>

### <span data-ttu-id="6a9a6-124">Пример 4</span><span class="sxs-lookup"><span data-stu-id="6a9a6-124">Example 4</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeId "/providers/Microsoft.Authorization/policySetDefinitions/3fa7cbf5-c0a4-4a59-85a5-cca4d996d5af"
```

<span data-ttu-id="6a9a6-125">Возвращает историю состояния соответствия по идентификатору инициативы.</span><span class="sxs-lookup"><span data-stu-id="6a9a6-125">Gets compliance status history by initiative Id.</span></span>

### <span data-ttu-id="6a9a6-126">Пример 5</span><span class="sxs-lookup"><span data-stu-id="6a9a6-126">Example 5</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeName "b5a822e0-ba98-4e54-9278-5d9833aa9b17"
```

<span data-ttu-id="6a9a6-127">Возвращает историю состояния соответствия по названию инициативы.</span><span class="sxs-lookup"><span data-stu-id="6a9a6-127">Gets compliance status history by initiative name.</span></span>

### <span data-ttu-id="6a9a6-128">Пример 6</span><span class="sxs-lookup"><span data-stu-id="6a9a6-128">Example 6</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName"
```
<span data-ttu-id="6a9a6-129">Возвращает историю состояния соответствия для всех политик настройки гостевой конфигурации, назначенных виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="6a9a6-129">Gets compliance status history for all guest configuration policies assigned to the VM.</span></span>

### <span data-ttu-id="6a9a6-130">Пример 7</span><span class="sxs-lookup"><span data-stu-id="6a9a6-130">Example 7</span></span>
```powershell
PS C:\>$x = Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName"
PS C:\>$x[10].ReportId
/subscriptions/4e6c6ed2-0bf6-41d7-9d21-a452c2cc7920/resourceGroups/MyResourceGroupName/providers/Microsoft.Compute/virtualMachines/MyVMName/providers/Microsoft.GuestConfiguration/guestConfigurationAssignments/MaximumPasswordAge/reports/c271f845-2c0a-4456-a441-e48fc332d0ac
PS C:\> Get-AzVMGuestPolicyStatus -ReportId $x[10].ReportId
```

<span data-ttu-id="6a9a6-131">Получение состояния политики гостевой настройки по ReportId.</span><span class="sxs-lookup"><span data-stu-id="6a9a6-131">Get guest configuration policy status by ReportId.</span></span>
<span data-ttu-id="6a9a6-132">ReportId — это свойство ReportId, которое можно найти в результатах Get-AzVMGuestPolicyStatusHistory.</span><span class="sxs-lookup"><span data-stu-id="6a9a6-132">The ReportId is the ReportId property that can be found in the results of Get-AzVMGuestPolicyStatusHistory.</span></span> <span data-ttu-id="6a9a6-133">(ознакомьтесь со всеми другими примерами)</span><span class="sxs-lookup"><span data-stu-id="6a9a6-133">(please refer other examples)</span></span>

## <span data-ttu-id="6a9a6-134">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6a9a6-134">PARAMETERS</span></span>

### <span data-ttu-id="6a9a6-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a9a6-135">-DefaultProfile</span></span>
<span data-ttu-id="6a9a6-136">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6a9a6-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a9a6-137">-InitiativeId</span><span class="sxs-lookup"><span data-stu-id="6a9a6-137">-InitiativeId</span></span>
<span data-ttu-id="6a9a6-138">Идентификатор определения политики, в которой тип определения — инициатива, а категория — конфигурация гостя.</span><span class="sxs-lookup"><span data-stu-id="6a9a6-138">Definition Id of a policy where definition type is Initiative and category is Guest Configuration</span></span>

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

### <span data-ttu-id="6a9a6-139">-InitiativeName</span><span class="sxs-lookup"><span data-stu-id="6a9a6-139">-InitiativeName</span></span>
<span data-ttu-id="6a9a6-140">Имя политики, в которой тип определения — инициатива, а категория — конфигурация гостя</span><span class="sxs-lookup"><span data-stu-id="6a9a6-140">Name of a policy where definition type is Initiative and category is Guest Configuration</span></span>

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

### <span data-ttu-id="6a9a6-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a9a6-141">-ResourceGroupName</span></span>
<span data-ttu-id="6a9a6-142">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6a9a6-142">Resource group name.</span></span>

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

### <span data-ttu-id="6a9a6-143">-ShowOnlyChange</span><span class="sxs-lookup"><span data-stu-id="6a9a6-143">-ShowOnlyChange</span></span>
<span data-ttu-id="6a9a6-144">Показывает хронологию изменений состояния только для политик настройки гостевой системы.</span><span class="sxs-lookup"><span data-stu-id="6a9a6-144">Shows historical status changes only for guest configuration policies.</span></span>
<span data-ttu-id="6a9a6-145">Пропускает состояние, которое не изменилось между двумя запущенными аудитом состояния соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="6a9a6-145">Skips statuses that have not changed between two compliance status audit runs.</span></span>

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

### <span data-ttu-id="6a9a6-146">-VMName</span><span class="sxs-lookup"><span data-stu-id="6a9a6-146">-VMName</span></span>
<span data-ttu-id="6a9a6-147">Имя ВМ.</span><span class="sxs-lookup"><span data-stu-id="6a9a6-147">VM name.</span></span>

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

### <span data-ttu-id="6a9a6-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a9a6-148">CommonParameters</span></span>
<span data-ttu-id="6a9a6-149">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6a9a6-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a9a6-150">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a9a6-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a9a6-151">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6a9a6-151">INPUTS</span></span>

### <span data-ttu-id="6a9a6-152">Ничего</span><span class="sxs-lookup"><span data-stu-id="6a9a6-152">None</span></span>
## <span data-ttu-id="6a9a6-153">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6a9a6-153">OUTPUTS</span></span>

### <span data-ttu-id="6a9a6-154">Microsoft. Azure. Commands. GuestConfiguration. Models. PolicyStatus</span><span class="sxs-lookup"><span data-stu-id="6a9a6-154">Microsoft.Azure.Commands.GuestConfiguration.Models.PolicyStatus</span></span>
## <span data-ttu-id="6a9a6-155">Пуск</span><span class="sxs-lookup"><span data-stu-id="6a9a6-155">NOTES</span></span>

## <span data-ttu-id="6a9a6-156">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6a9a6-156">RELATED LINKS</span></span>

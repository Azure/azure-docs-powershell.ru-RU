---
external help file: Microsoft.Azure.PowerShell.Cmdlets.GuestConfiguration.dll-Help.xml
Module Name: Az.GuestConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.guestconfiguration/get-AzVMGuestPolicyStatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatus.md
ms.openlocfilehash: 49148f1c62b71436e48b2b92a4591a7cdb36cccf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078266"
---
# <span data-ttu-id="46ff7-101">Get-AzVMGuestPolicyStatus</span><span class="sxs-lookup"><span data-stu-id="46ff7-101">Get-AzVMGuestPolicyStatus</span></span>

## <span data-ttu-id="46ff7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="46ff7-102">SYNOPSIS</span></span>
<span data-ttu-id="46ff7-103">Возвращает состояние политики гостевой настройки (подробно) для инициативы с типом "Гостевая конфигурация", назначенной ВМ.</span><span class="sxs-lookup"><span data-stu-id="46ff7-103">Gets guest configuration policy statuses (detailed) for an initiative of type "Guest Configuration" that is assigned to a VM.</span></span>
<span data-ttu-id="46ff7-104">Инициатива — это политика типа определения "инициатива".</span><span class="sxs-lookup"><span data-stu-id="46ff7-104">An initiative is a policy of definition type "Initiative".</span></span>

## <span data-ttu-id="46ff7-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="46ff7-105">SYNTAX</span></span>

### <span data-ttu-id="46ff7-106">VmScope (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="46ff7-106">VmScope (Default)</span></span>
```
Get-AzVMGuestPolicyStatus [-ResourceGroupName] <String> [-VMName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="46ff7-107">InitiativeIdScope</span><span class="sxs-lookup"><span data-stu-id="46ff7-107">InitiativeIdScope</span></span>
```
Get-AzVMGuestPolicyStatus [-ResourceGroupName] <String> [-VMName] <String> [-InitiativeId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="46ff7-108">InitiativeNameScope</span><span class="sxs-lookup"><span data-stu-id="46ff7-108">InitiativeNameScope</span></span>
```
Get-AzVMGuestPolicyStatus [-ResourceGroupName] <String> [-VMName] <String> [-InitiativeName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="46ff7-109">ReportIdScope</span><span class="sxs-lookup"><span data-stu-id="46ff7-109">ReportIdScope</span></span>
```
Get-AzVMGuestPolicyStatus [-ReportId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="46ff7-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="46ff7-110">DESCRIPTION</span></span>
<span data-ttu-id="46ff7-111">Командлет Get-AzVMGuestPolicyStatus получает статусы политики гостевой конфигурации для инициативы типа "Гостевая конфигурация", назначенной ВМ.</span><span class="sxs-lookup"><span data-stu-id="46ff7-111">The Get-AzVMGuestPolicyStatus cmdlet gets guest configuration policy statuses for an initiative of type "Guest Configuration" that is assigned to a VM.</span></span>
<span data-ttu-id="46ff7-112">Инициатива — это политика типа определения "инициатива".</span><span class="sxs-lookup"><span data-stu-id="46ff7-112">An initiative is a policy of definition type "Initiative".</span></span>
<span data-ttu-id="46ff7-113">Этот командлет получает состояние соответствия требованиям виртуальной машины и причины, по которым она не соответствует требованиям отдельных политик в инициативе.</span><span class="sxs-lookup"><span data-stu-id="46ff7-113">This cmdlet gets compliance statuses of the VM and reasons why it is non-compliant for the individual policies in the initiative.</span></span>

## <span data-ttu-id="46ff7-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="46ff7-114">EXAMPLES</span></span>

### <span data-ttu-id="46ff7-115">Пример 1</span><span class="sxs-lookup"><span data-stu-id="46ff7-115">Example 1</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName"
```

<span data-ttu-id="46ff7-116">Получение всех последних состояний политики настройки гостевой конфигурации для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="46ff7-116">Get all latest guest configuration policy statuses for a VM.</span></span>
<span data-ttu-id="46ff7-117">Этот статус включает состояние соответствия виртуальной машине для каждой политики во всех инициативах типа "Конфигурация гостя", причины соответствия требованиям, время проверки соответствия требованиям, сведения о ресурсе, которые были проверены на соответствие требованиям.</span><span class="sxs-lookup"><span data-stu-id="46ff7-117">The status includes compliance status of the VM for each policy in all initiatives of type "Guest Configuration", compliance reasons, time of the compliance check, resource information which was checked for compliance.</span></span>
<span data-ttu-id="46ff7-118">Результаты включают последние статусы и не включают предыдущие исторические статусы.</span><span class="sxs-lookup"><span data-stu-id="46ff7-118">The results include latest statuses, does not include previous historical statuses.</span></span>

### <span data-ttu-id="46ff7-119">Пример 2</span><span class="sxs-lookup"><span data-stu-id="46ff7-119">Example 2</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeId "/providers/Microsoft.Authorization/policySetDefinitions/3fa7cbf5-c0a4-4a59-85a5-cca4d996d5af"
```

<span data-ttu-id="46ff7-120">Получение последних состояний политики настройки гостевой конфигурации по идентификатору инициативы. Состояние соответствия требованиям виртуальной машины для каждой политики в инициативе, причины соответствия требованиям, время проверки соответствия требованиям, сведения о ресурсе, которые были проверены на соответствие требованиям.</span><span class="sxs-lookup"><span data-stu-id="46ff7-120">Get the latest guest configuration policy statuses by initiative Id. The status includes compliance status of the VM for each policy in the initiative, compliance reasons, time of the compliance check, resource information which was checked for compliance.</span></span>
<span data-ttu-id="46ff7-121">Результаты не включают в себя предыдущие состояния, они просто содержат Последнее состояние для каждой политики в инициативе.</span><span class="sxs-lookup"><span data-stu-id="46ff7-121">The results does not include previous statuses generated, it just includes latest status for each policy in the initiative.</span></span>

### <span data-ttu-id="46ff7-122">Пример 3</span><span class="sxs-lookup"><span data-stu-id="46ff7-122">Example 3</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeName "b5a822e0-ba98-4e54-9278-5d9833aa9b17"
```

<span data-ttu-id="46ff7-123">Получение последних состояний политики настройки гостевой конфигурации по названию инициативы.</span><span class="sxs-lookup"><span data-stu-id="46ff7-123">Get the latest guest configuration policy statuses by initiative name.</span></span>
<span data-ttu-id="46ff7-124">Состояние соответствия требованиям виртуальной машины для каждой политики в инициативе, причины соответствия требованиям, время проверки соответствия требованиям, сведения о ресурсе, которые были проверены на соответствие требованиям.</span><span class="sxs-lookup"><span data-stu-id="46ff7-124">The status includes compliance status of the VM for each policy in the initiative, compliance reasons, time of the compliance check, resource information which was checked for compliance.</span></span>
<span data-ttu-id="46ff7-125">Результаты не включают в себя предыдущие состояния, они просто содержат Последнее состояние для каждой политики в инициативе.</span><span class="sxs-lookup"><span data-stu-id="46ff7-125">The results does not include previous statuses generated, it just includes latest status for each policy in the initiative.</span></span>

### <span data-ttu-id="46ff7-126">Пример 4</span><span class="sxs-lookup"><span data-stu-id="46ff7-126">Example 4</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ReportId "/subscriptions/4e6c6ed2-0bf6-41d7-9d21-a452c2cc7920/resourceGroups/MyResourceGroupName/providers/Microsoft.Compute/virtualMachines/MyVMName/providers/Microsoft.GuestConfiguration/guestConfigurationAssignments/MaximumPasswordAge/reports/c271f845-2c0a-4456-a441-e48fc332d0ac"
```

<span data-ttu-id="46ff7-127">Получение состояния политики гостевой настройки по ReportId.</span><span class="sxs-lookup"><span data-stu-id="46ff7-127">Get guest configuration policy status by ReportId.</span></span>
<span data-ttu-id="46ff7-128">ReportId — это свойство ReportId, которое можно найти в результатах Get-AzVMGuestPolicyStatus по имени initiativeId или инициативы (пожалуйста, ознакомьтесь с другими примерами).</span><span class="sxs-lookup"><span data-stu-id="46ff7-128">The ReportId is the ReportId property that can be found in the results of Get-AzVMGuestPolicyStatus by initiativeId or Initiative name (please refer other examples)</span></span>

## <span data-ttu-id="46ff7-129">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="46ff7-129">PARAMETERS</span></span>

### <span data-ttu-id="46ff7-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46ff7-130">-DefaultProfile</span></span>
<span data-ttu-id="46ff7-131">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="46ff7-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46ff7-132">-InitiativeId</span><span class="sxs-lookup"><span data-stu-id="46ff7-132">-InitiativeId</span></span>
<span data-ttu-id="46ff7-133">Идентификатор определения политики, в которой тип определения — инициатива, а категория — конфигурация гостя.</span><span class="sxs-lookup"><span data-stu-id="46ff7-133">Definition Id of a policy where definition type is Initiative and category is Guest Configuration</span></span>

```yaml
Type: System.String
Parameter Sets: InitiativeIdScope
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46ff7-134">-InitiativeName</span><span class="sxs-lookup"><span data-stu-id="46ff7-134">-InitiativeName</span></span>
<span data-ttu-id="46ff7-135">Имя политики, в которой тип определения — инициатива, а категория — конфигурация гостя</span><span class="sxs-lookup"><span data-stu-id="46ff7-135">Name of a policy where definition type is Initiative and category is Guest Configuration</span></span>

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

### <span data-ttu-id="46ff7-136">-ReportId</span><span class="sxs-lookup"><span data-stu-id="46ff7-136">-ReportId</span></span>
<span data-ttu-id="46ff7-137">Идентификатор состояния политики гостевой конфигурации.</span><span class="sxs-lookup"><span data-stu-id="46ff7-137">Id of a Guest Configuration policy status.</span></span>
<span data-ttu-id="46ff7-138">Политика, в которой тип определения — инициатива, и категория является Гостевой конфигурацией, должна быть назначена области для получения сведений о состоянии.</span><span class="sxs-lookup"><span data-stu-id="46ff7-138">A policy where definition type is Initiative and category is Guest Configuration must be assigned to a scope to get statuses.</span></span>

```yaml
Type: System.String
Parameter Sets: ReportIdScope
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46ff7-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46ff7-139">-ResourceGroupName</span></span>
<span data-ttu-id="46ff7-140">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="46ff7-140">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: VmScope, InitiativeIdScope, InitiativeNameScope
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46ff7-141">-VMName</span><span class="sxs-lookup"><span data-stu-id="46ff7-141">-VMName</span></span>
<span data-ttu-id="46ff7-142">Имя ВМ.</span><span class="sxs-lookup"><span data-stu-id="46ff7-142">VM name.</span></span>

```yaml
Type: System.String
Parameter Sets: VmScope, InitiativeIdScope, InitiativeNameScope
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46ff7-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46ff7-143">CommonParameters</span></span>
<span data-ttu-id="46ff7-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="46ff7-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46ff7-145">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46ff7-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46ff7-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="46ff7-146">INPUTS</span></span>

### <span data-ttu-id="46ff7-147">Ничего</span><span class="sxs-lookup"><span data-stu-id="46ff7-147">None</span></span>
## <span data-ttu-id="46ff7-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="46ff7-148">OUTPUTS</span></span>

### <span data-ttu-id="46ff7-149">Microsoft. Azure. Commands. GuestConfiguration. Models. PolicyStatusDetailed</span><span class="sxs-lookup"><span data-stu-id="46ff7-149">Microsoft.Azure.Commands.GuestConfiguration.Models.PolicyStatusDetailed</span></span>
## <span data-ttu-id="46ff7-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="46ff7-150">NOTES</span></span>

## <span data-ttu-id="46ff7-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="46ff7-151">RELATED LINKS</span></span>

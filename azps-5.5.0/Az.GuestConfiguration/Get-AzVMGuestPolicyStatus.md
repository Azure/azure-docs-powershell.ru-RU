---
external help file: Microsoft.Azure.PowerShell.Cmdlets.GuestConfiguration.dll-Help.xml
Module Name: Az.GuestConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.guestconfiguration/get-AzVMGuestPolicyStatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatus.md
ms.openlocfilehash: 49148f1c62b71436e48b2b92a4591a7cdb36cccf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100221729"
---
# <span data-ttu-id="11187-101">Get-AzVMGuestPolicyStatus</span><span class="sxs-lookup"><span data-stu-id="11187-101">Get-AzVMGuestPolicyStatus</span></span>

## <span data-ttu-id="11187-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11187-102">SYNOPSIS</span></span>
<span data-ttu-id="11187-103">Получает статусы политики настройки гостей (подробный) для инициативы типа "Гостевая конфигурация", которая назначена VM.</span><span class="sxs-lookup"><span data-stu-id="11187-103">Gets guest configuration policy statuses (detailed) for an initiative of type "Guest Configuration" that is assigned to a VM.</span></span>
<span data-ttu-id="11187-104">Инициатива — это политика определения типа "Инициатива".</span><span class="sxs-lookup"><span data-stu-id="11187-104">An initiative is a policy of definition type "Initiative".</span></span>

## <span data-ttu-id="11187-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="11187-105">SYNTAX</span></span>

### <span data-ttu-id="11187-106">VmScope (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="11187-106">VmScope (Default)</span></span>
```
Get-AzVMGuestPolicyStatus [-ResourceGroupName] <String> [-VMName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="11187-107">InitiativeIdScope</span><span class="sxs-lookup"><span data-stu-id="11187-107">InitiativeIdScope</span></span>
```
Get-AzVMGuestPolicyStatus [-ResourceGroupName] <String> [-VMName] <String> [-InitiativeId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="11187-108">InitiativeNameScope</span><span class="sxs-lookup"><span data-stu-id="11187-108">InitiativeNameScope</span></span>
```
Get-AzVMGuestPolicyStatus [-ResourceGroupName] <String> [-VMName] <String> [-InitiativeName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="11187-109">ReportIdScope</span><span class="sxs-lookup"><span data-stu-id="11187-109">ReportIdScope</span></span>
```
Get-AzVMGuestPolicyStatus [-ReportId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="11187-110">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="11187-110">DESCRIPTION</span></span>
<span data-ttu-id="11187-111">Этот Get-AzVMGuestPolicyStatus получает состояние политики настройки гостей для инициативы типа "Гостевая конфигурация", которая назначена VM.</span><span class="sxs-lookup"><span data-stu-id="11187-111">The Get-AzVMGuestPolicyStatus cmdlet gets guest configuration policy statuses for an initiative of type "Guest Configuration" that is assigned to a VM.</span></span>
<span data-ttu-id="11187-112">Инициатива — это политика определения типа "Инициатива".</span><span class="sxs-lookup"><span data-stu-id="11187-112">An initiative is a policy of definition type "Initiative".</span></span>
<span data-ttu-id="11187-113">Этот cmdlet получает статус соответствия требованиям для VM-управления и причины, по которым он не соответствует отдельным политикам в инициативе.</span><span class="sxs-lookup"><span data-stu-id="11187-113">This cmdlet gets compliance statuses of the VM and reasons why it is non-compliant for the individual policies in the initiative.</span></span>

## <span data-ttu-id="11187-114">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="11187-114">EXAMPLES</span></span>

### <span data-ttu-id="11187-115">Пример 1</span><span class="sxs-lookup"><span data-stu-id="11187-115">Example 1</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName"
```

<span data-ttu-id="11187-116">Получите все последние состояния политики настройки гостей для VM.</span><span class="sxs-lookup"><span data-stu-id="11187-116">Get all latest guest configuration policy statuses for a VM.</span></span>
<span data-ttu-id="11187-117">Состояние включает состояние соответствия VM для каждой политики всем инициативам типа "Гостевая конфигурация", причины соответствия требованиям, время проверки соответствия, сведения о ресурсах, которые проверялись на соответствие требованиям.</span><span class="sxs-lookup"><span data-stu-id="11187-117">The status includes compliance status of the VM for each policy in all initiatives of type "Guest Configuration", compliance reasons, time of the compliance check, resource information which was checked for compliance.</span></span>
<span data-ttu-id="11187-118">Результаты включают последние состояния, но не включают предыдущие исторические состояния.</span><span class="sxs-lookup"><span data-stu-id="11187-118">The results include latest statuses, does not include previous historical statuses.</span></span>

### <span data-ttu-id="11187-119">Пример 2</span><span class="sxs-lookup"><span data-stu-id="11187-119">Example 2</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeId "/providers/Microsoft.Authorization/policySetDefinitions/3fa7cbf5-c0a4-4a59-85a5-cca4d996d5af"
```

<span data-ttu-id="11187-120">Получите последние состояния политики гостевой конфигурации по ид инициативной конфигурации. Состояние включает состояние соответствия VM для каждой политики в инициативе, причины соответствия требованиям, время проверки соответствия, сведения о ресурсах, которые были проверены на соответствие требованиям.</span><span class="sxs-lookup"><span data-stu-id="11187-120">Get the latest guest configuration policy statuses by initiative Id. The status includes compliance status of the VM for each policy in the initiative, compliance reasons, time of the compliance check, resource information which was checked for compliance.</span></span>
<span data-ttu-id="11187-121">В результатах не содержатся ранее созданные состояния, а только последние состояния каждой политики в инициативе.</span><span class="sxs-lookup"><span data-stu-id="11187-121">The results does not include previous statuses generated, it just includes latest status for each policy in the initiative.</span></span>

### <span data-ttu-id="11187-122">Пример 3</span><span class="sxs-lookup"><span data-stu-id="11187-122">Example 3</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeName "b5a822e0-ba98-4e54-9278-5d9833aa9b17"
```

<span data-ttu-id="11187-123">По названиям инициатив вы получаете последние состояния политики настройки гостей.</span><span class="sxs-lookup"><span data-stu-id="11187-123">Get the latest guest configuration policy statuses by initiative name.</span></span>
<span data-ttu-id="11187-124">Состояние включает состояние соответствия VM для каждой политики в инициативе, причины соответствия требованиям, время проверки соответствия, сведения о ресурсах, которые были проверены на соответствие требованиям.</span><span class="sxs-lookup"><span data-stu-id="11187-124">The status includes compliance status of the VM for each policy in the initiative, compliance reasons, time of the compliance check, resource information which was checked for compliance.</span></span>
<span data-ttu-id="11187-125">В результатах не содержатся ранее созданные состояния, а только последние состояния каждой политики в инициативе.</span><span class="sxs-lookup"><span data-stu-id="11187-125">The results does not include previous statuses generated, it just includes latest status for each policy in the initiative.</span></span>

### <span data-ttu-id="11187-126">Пример 4</span><span class="sxs-lookup"><span data-stu-id="11187-126">Example 4</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ReportId "/subscriptions/4e6c6ed2-0bf6-41d7-9d21-a452c2cc7920/resourceGroups/MyResourceGroupName/providers/Microsoft.Compute/virtualMachines/MyVMName/providers/Microsoft.GuestConfiguration/guestConfigurationAssignments/MaximumPasswordAge/reports/c271f845-2c0a-4456-a441-e48fc332d0ac"
```

<span data-ttu-id="11187-127">Получите состояние политики настройки гостей по ReportId.</span><span class="sxs-lookup"><span data-stu-id="11187-127">Get guest configuration policy status by ReportId.</span></span>
<span data-ttu-id="11187-128">ReportId — это свойство ReportId, которое можно найти в результатах поиска по Get-AzVMGuestPolicyStatus initiativeId или initiative name (см. другие примеры).</span><span class="sxs-lookup"><span data-stu-id="11187-128">The ReportId is the ReportId property that can be found in the results of Get-AzVMGuestPolicyStatus by initiativeId or Initiative name (please refer other examples)</span></span>

## <span data-ttu-id="11187-129">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="11187-129">PARAMETERS</span></span>

### <span data-ttu-id="11187-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11187-130">-DefaultProfile</span></span>
<span data-ttu-id="11187-131">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="11187-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11187-132">-InitiativeId</span><span class="sxs-lookup"><span data-stu-id="11187-132">-InitiativeId</span></span>
<span data-ttu-id="11187-133">Определение ИД политики, в которой тип определения — Initiative, а категория — Guest Configuration</span><span class="sxs-lookup"><span data-stu-id="11187-133">Definition Id of a policy where definition type is Initiative and category is Guest Configuration</span></span>

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

### <span data-ttu-id="11187-134">-InitiativeName</span><span class="sxs-lookup"><span data-stu-id="11187-134">-InitiativeName</span></span>
<span data-ttu-id="11187-135">Имя политики, для которой тип определения — Initiative, а категория — Guest Configuration</span><span class="sxs-lookup"><span data-stu-id="11187-135">Name of a policy where definition type is Initiative and category is Guest Configuration</span></span>

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

### <span data-ttu-id="11187-136">-ReportId</span><span class="sxs-lookup"><span data-stu-id="11187-136">-ReportId</span></span>
<span data-ttu-id="11187-137">ИД состояния политики "Гостевая конфигурация".</span><span class="sxs-lookup"><span data-stu-id="11187-137">Id of a Guest Configuration policy status.</span></span>
<span data-ttu-id="11187-138">Политика, в которой тип определения — Initiative, а категория — Guest Configuration, должна быть назначена области для получения состояния.</span><span class="sxs-lookup"><span data-stu-id="11187-138">A policy where definition type is Initiative and category is Guest Configuration must be assigned to a scope to get statuses.</span></span>

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

### <span data-ttu-id="11187-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11187-139">-ResourceGroupName</span></span>
<span data-ttu-id="11187-140">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="11187-140">Resource group name.</span></span>

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

### <span data-ttu-id="11187-141">-VMName</span><span class="sxs-lookup"><span data-stu-id="11187-141">-VMName</span></span>
<span data-ttu-id="11187-142">Имя VM.</span><span class="sxs-lookup"><span data-stu-id="11187-142">VM name.</span></span>

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

### <span data-ttu-id="11187-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11187-143">CommonParameters</span></span>
<span data-ttu-id="11187-144">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11187-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11187-145">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11187-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11187-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="11187-146">INPUTS</span></span>

### <span data-ttu-id="11187-147">Нет</span><span class="sxs-lookup"><span data-stu-id="11187-147">None</span></span>
## <span data-ttu-id="11187-148">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="11187-148">OUTPUTS</span></span>

### <span data-ttu-id="11187-149">Microsoft.Azure.Commands.GuestConfiguration.Models.PolicyStatusDetailed</span><span class="sxs-lookup"><span data-stu-id="11187-149">Microsoft.Azure.Commands.GuestConfiguration.Models.PolicyStatusDetailed</span></span>
## <span data-ttu-id="11187-150">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="11187-150">NOTES</span></span>

## <span data-ttu-id="11187-151">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="11187-151">RELATED LINKS</span></span>

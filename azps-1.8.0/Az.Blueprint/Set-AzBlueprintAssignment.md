---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/set-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintAssignment.md
ms.openlocfilehash: 795f1a7c4a002b7a8a141460b3b5e403ef8dc168
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93901481"
---
# <span data-ttu-id="2f2f9-101">Set-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="2f2f9-101">Set-AzBlueprintAssignment</span></span>

## <span data-ttu-id="2f2f9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2f2f9-102">SYNOPSIS</span></span>
<span data-ttu-id="2f2f9-103">Обновление существующего задания в виде чертежей.</span><span class="sxs-lookup"><span data-stu-id="2f2f9-103">Update an existing blueprint assignment.</span></span>

## <span data-ttu-id="2f2f9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2f2f9-104">SYNTAX</span></span>

```
Set-AzBlueprintAssignment -Name <String> -Blueprint <PSBlueprintBase> [-SubscriptionId <String[]>]
 -Location <String> [-ResourceGroupParameter <Hashtable>] [-Parameter <Hashtable>] [-SystemAssignedIdentity]
 [-UserAssignedIdentity <String>] [-Lock <PSLockMode>] [-SecureStringParameter <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f2f9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2f2f9-105">DESCRIPTION</span></span>
<span data-ttu-id="2f2f9-106">Обновление существующего задания в виде чертежей.</span><span class="sxs-lookup"><span data-stu-id="2f2f9-106">Update an existing blueprint assignment.</span></span>

## <span data-ttu-id="2f2f9-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2f2f9-107">EXAMPLES</span></span>

### <span data-ttu-id="2f2f9-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2f2f9-108">Example 1</span></span>
```powershell
PS C:\> $rg = @{ResourceGroup=@{name='storage_rg';location='eastus'}}
PS C:\> $params = @{applytaganditsdefaultvalue_tagName="Department_Cost_Center"; applytaganditsdefaultvalue_tagValue="Contoso/HR/Dev/0001"}
PS C:\> $blueprintObject =  Get-AzBlueprint -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myBlueprintName"
PS C:\> Set-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId "00000000-1111-0000-1111-000000000000" -Location "West US" -Parameter $params -ResourceGroupParameter $rg -SystemAssignedIdentity

Name              : myAssignment
Id                : /subscriptions/00000000-1111-0000-1111-000000000000/providers/Microsoft.Blueprint/blueprintAssignments/Assignment-PS-BlueprintDefinition
Scope             : /subscriptions/00000000-1111-0000-1111-000000000000
LastModified      : 2019-01-08
LockMode          : None
ProvisioningState : Creating
Parameters        : {applytaganditsdefaultvalue_tagName, applytaganditsdefaultvalue_tagValue}
ResourceGroups    : ResourceGroup
```

<span data-ttu-id="2f2f9-109">Обновите существующее назначение для определения плана `$blueprintObject` в указанной подписке, обновив параметры.</span><span class="sxs-lookup"><span data-stu-id="2f2f9-109">Update an existing blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription, updating the parameters.</span></span> <span data-ttu-id="2f2f9-110">Использует присвоенное системой удостоверение.</span><span class="sxs-lookup"><span data-stu-id="2f2f9-110">Uses system-assigned identity.</span></span> <span data-ttu-id="2f2f9-111">Расположение определяет регион для создания управляемого удостоверения.</span><span class="sxs-lookup"><span data-stu-id="2f2f9-111">The location defines the region for creating the managed identity.</span></span>

## <span data-ttu-id="2f2f9-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2f2f9-112">PARAMETERS</span></span>

### <span data-ttu-id="2f2f9-113">-Чертеж</span><span class="sxs-lookup"><span data-stu-id="2f2f9-113">-Blueprint</span></span>
<span data-ttu-id="2f2f9-114">Объект чертежа.</span><span class="sxs-lookup"><span data-stu-id="2f2f9-114">Blueprint object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2f2f9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f2f9-115">-DefaultProfile</span></span>
<span data-ttu-id="2f2f9-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2f2f9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f2f9-117">-Location</span><span class="sxs-lookup"><span data-stu-id="2f2f9-117">-Location</span></span>
<span data-ttu-id="2f2f9-118">Регион для создания управляемого удостоверения.</span><span class="sxs-lookup"><span data-stu-id="2f2f9-118">Region for managed identity to be created in.</span></span>
<span data-ttu-id="2f2f9-119">Дополнительные сведения по адресу aka.ms/blueprintmsi</span><span class="sxs-lookup"><span data-stu-id="2f2f9-119">Learn more at aka.ms/blueprintmsi</span></span>

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

### <span data-ttu-id="2f2f9-120">-Lock</span><span class="sxs-lookup"><span data-stu-id="2f2f9-120">-Lock</span></span>
<span data-ttu-id="2f2f9-121">Блокировка ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2f2f9-121">Lock resources.</span></span>
<span data-ttu-id="2f2f9-122">Дополнительные сведения по адресу aka.ms/blueprintlocks</span><span class="sxs-lookup"><span data-stu-id="2f2f9-122">Learn more at aka.ms/blueprintlocks</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Blueprint.Models.PSLockMode]
Parameter Sets: (All)
Aliases:
Accepted values: None, AllResourcesReadOnly, AllResourcesDoNotDelete

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f2f9-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2f2f9-123">-Name</span></span>
<span data-ttu-id="2f2f9-124">Имя назначения для схемы.</span><span class="sxs-lookup"><span data-stu-id="2f2f9-124">Blueprint assignment name.</span></span>

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

### <span data-ttu-id="2f2f9-125">-Параметр</span><span class="sxs-lookup"><span data-stu-id="2f2f9-125">-Parameter</span></span>
<span data-ttu-id="2f2f9-126">Параметр артефакта.</span><span class="sxs-lookup"><span data-stu-id="2f2f9-126">Artifact parameter.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f2f9-127">-ResourceGroupParameter</span><span class="sxs-lookup"><span data-stu-id="2f2f9-127">-ResourceGroupParameter</span></span>
<span data-ttu-id="2f2f9-128">{{Fill ResourceGroupParameter Description}}</span><span class="sxs-lookup"><span data-stu-id="2f2f9-128">{{Fill ResourceGroupParameter Description}}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f2f9-129">-SecureStringParameter</span><span class="sxs-lookup"><span data-stu-id="2f2f9-129">-SecureStringParameter</span></span>
<span data-ttu-id="2f2f9-130">Параметр Secure String для идентификатора ресурса KeyVault, имени и версии.</span><span class="sxs-lookup"><span data-stu-id="2f2f9-130">Secure string parameter for KeyVault resource id, name and version.</span></span>

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

### <span data-ttu-id="2f2f9-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2f2f9-131">-SubscriptionId</span></span>
<span data-ttu-id="2f2f9-132">SubscriptionId, чтобы назначить проект.</span><span class="sxs-lookup"><span data-stu-id="2f2f9-132">SubscriptionId to assign the Blueprint.</span></span>
<span data-ttu-id="2f2f9-133">Может быть списком из строк subscriptionId, разделенных запятыми.</span><span class="sxs-lookup"><span data-stu-id="2f2f9-133">Can be a comma delimited list of subscriptionId strings.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f2f9-134">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="2f2f9-134">-SystemAssignedIdentity</span></span>
<span data-ttu-id="2f2f9-135">Система присвоила идентификатор (MSI) для развертывания артефактов.</span><span class="sxs-lookup"><span data-stu-id="2f2f9-135">System assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="2f2f9-136">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="2f2f9-136">-UserAssignedIdentity</span></span>
<span data-ttu-id="2f2f9-137">Идентификатор (MSI), назначенный пользователю для развертывания артефактов.</span><span class="sxs-lookup"><span data-stu-id="2f2f9-137">User assigned identity(MSI) to deploy the artifacts.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f2f9-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2f2f9-138">-Confirm</span></span>
<span data-ttu-id="2f2f9-139">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2f2f9-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f2f9-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f2f9-140">-WhatIf</span></span>
<span data-ttu-id="2f2f9-141">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2f2f9-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f2f9-142">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2f2f9-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f2f9-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f2f9-143">CommonParameters</span></span>
<span data-ttu-id="2f2f9-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2f2f9-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f2f9-145">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f2f9-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f2f9-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2f2f9-146">INPUTS</span></span>

### <span data-ttu-id="2f2f9-147">System. String</span><span class="sxs-lookup"><span data-stu-id="2f2f9-147">System.String</span></span>

### <span data-ttu-id="2f2f9-148">Microsoft. Azure. Commands. чертеж. Models. PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="2f2f9-148">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="2f2f9-149">System. String []</span><span class="sxs-lookup"><span data-stu-id="2f2f9-149">System.String[]</span></span>

### <span data-ttu-id="2f2f9-150">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="2f2f9-150">System.Collections.Hashtable</span></span>

## <span data-ttu-id="2f2f9-151">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2f2f9-151">OUTPUTS</span></span>

### <span data-ttu-id="2f2f9-152">System. Object</span><span class="sxs-lookup"><span data-stu-id="2f2f9-152">System.Object</span></span>
## <span data-ttu-id="2f2f9-153">Пуск</span><span class="sxs-lookup"><span data-stu-id="2f2f9-153">NOTES</span></span>

## <span data-ttu-id="2f2f9-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2f2f9-154">RELATED LINKS</span></span>

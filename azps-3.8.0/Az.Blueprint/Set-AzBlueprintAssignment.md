---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/set-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintAssignment.md
ms.openlocfilehash: 418bb8a9ba8362e799d619705eccdc60e5418fc9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065456"
---
# <span data-ttu-id="87684-101">Set-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="87684-101">Set-AzBlueprintAssignment</span></span>

## <span data-ttu-id="87684-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="87684-102">SYNOPSIS</span></span>
<span data-ttu-id="87684-103">Обновление существующего задания в виде чертежей.</span><span class="sxs-lookup"><span data-stu-id="87684-103">Update an existing blueprint assignment.</span></span>

## <span data-ttu-id="87684-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="87684-104">SYNTAX</span></span>

### <span data-ttu-id="87684-105">UpdateBlueprintAssignment (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="87684-105">UpdateBlueprintAssignment (Default)</span></span>
```
Set-AzBlueprintAssignment -Name <String> -Blueprint <PSBlueprintBase> -Location <String>
 [-SystemAssignedIdentity] [-UserAssignedIdentity <String>] [-Lock <PSLockMode>]
 [-SecureStringParameter <Hashtable>] [-ResourceGroupParameter <Hashtable>] [-Parameter <Hashtable>]
 [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="87684-106">UpdateBlueprintAssignmentByFile</span><span class="sxs-lookup"><span data-stu-id="87684-106">UpdateBlueprintAssignmentByFile</span></span>
```
Set-AzBlueprintAssignment -Name <String> -Blueprint <PSBlueprintBase> [-AssignmentFile <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="87684-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="87684-107">DESCRIPTION</span></span>
<span data-ttu-id="87684-108">Обновление существующего задания в виде чертежей.</span><span class="sxs-lookup"><span data-stu-id="87684-108">Update an existing blueprint assignment.</span></span>

## <span data-ttu-id="87684-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="87684-109">EXAMPLES</span></span>

### <span data-ttu-id="87684-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="87684-110">Example 1</span></span>
```powershell
PS C:\> $rg = @{ResourceGroup=@{name='storage_rg';location='eastus'}}
PS C:\> $params = @{applytaganditsdefaultvalue_tagName="Department_Cost_Center"; applytaganditsdefaultvalue_tagValue="Contoso/HR/Dev/0001"}
PS C:\> $blueprintObject =  Get-AzBlueprint -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myBlueprintName"
PS C:\> Set-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId "00000000-1111-0000-1111-000000000000" -Location "West US" -Parameter $params -ResourceGroupParameter $rg -SystemAssignedIdentity

Name              : myAssignment
Id                : /subscriptions/00000000-1111-0000-1111-000000000000/providers/Microsoft.Blueprint/blueprintAssignments/myAssignment
Scope             : /subscriptions/00000000-1111-0000-1111-000000000000
LastModified      : 2019-01-08
LockMode          : None
ProvisioningState : Creating
Parameters        : {applytaganditsdefaultvalue_tagName, applytaganditsdefaultvalue_tagValue}
ResourceGroups    : ResourceGroup
```

<span data-ttu-id="87684-111">Обновите существующее назначение для определения плана `$blueprintObject` в указанной подписке, обновив параметры.</span><span class="sxs-lookup"><span data-stu-id="87684-111">Update an existing blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription, updating the parameters.</span></span> <span data-ttu-id="87684-112">Использует присвоенное системой удостоверение.</span><span class="sxs-lookup"><span data-stu-id="87684-112">Uses system-assigned identity.</span></span> <span data-ttu-id="87684-113">Расположение определяет регион для создания управляемого удостоверения.</span><span class="sxs-lookup"><span data-stu-id="87684-113">The location defines the region for creating the managed identity.</span></span>

### <span data-ttu-id="87684-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="87684-114">Example 2</span></span>
```powershell
PS C:\> $blueprintObject =  Get-AzBlueprint -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myBlueprintName"
PS C:\> Set-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId "00000000-1111-0000-1111-000000000000" -AssignmentFile C:\myAssignmentfile.json

Name              : myAssignment
Id                : /subscriptions/00000000-1111-0000-1111-000000000000/providers/Microsoft.Blueprint/blueprintAssignments/myAssignment
Scope             : /subscriptions/00000000-1111-0000-1111-000000000000
LastModified      : 2019-01-08
LockMode          : None
ProvisioningState : Creating
Parameters        : {applytaganditsdefaultvalue_tagName, applytaganditsdefaultvalue_tagValue}
ResourceGroups    : ResourceGroup
```

<span data-ttu-id="87684-115">Обновление существующего задания из схемы с помощью файла подборки.</span><span class="sxs-lookup"><span data-stu-id="87684-115">Update an existing blueprint assignment through an assignment file.</span></span> <span data-ttu-id="87684-116">Формат файла подборки можно найти в образцах запросов и ответов по адресу: https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span><span class="sxs-lookup"><span data-stu-id="87684-116">The format of the assignment file can be found in the request/response samples at: https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span></span>

## <span data-ttu-id="87684-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="87684-117">PARAMETERS</span></span>

### <span data-ttu-id="87684-118">-Чертеж</span><span class="sxs-lookup"><span data-stu-id="87684-118">-Blueprint</span></span>
<span data-ttu-id="87684-119">Объект чертежа.</span><span class="sxs-lookup"><span data-stu-id="87684-119">Blueprint object.</span></span>

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

### <span data-ttu-id="87684-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87684-120">-DefaultProfile</span></span>
<span data-ttu-id="87684-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="87684-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="87684-122">-Location</span><span class="sxs-lookup"><span data-stu-id="87684-122">-Location</span></span>
<span data-ttu-id="87684-123">Регион для создания управляемого удостоверения.</span><span class="sxs-lookup"><span data-stu-id="87684-123">Region for managed identity to be created in.</span></span>
<span data-ttu-id="87684-124">Дополнительные сведения по адресу aka.ms/blueprintmsi</span><span class="sxs-lookup"><span data-stu-id="87684-124">Learn more at aka.ms/blueprintmsi</span></span>

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

### <span data-ttu-id="87684-125">-Lock</span><span class="sxs-lookup"><span data-stu-id="87684-125">-Lock</span></span>
<span data-ttu-id="87684-126">Блокировка ресурсов.</span><span class="sxs-lookup"><span data-stu-id="87684-126">Lock resources.</span></span>
<span data-ttu-id="87684-127">Дополнительные сведения по адресу aka.ms/blueprintlocks</span><span class="sxs-lookup"><span data-stu-id="87684-127">Learn more at aka.ms/blueprintlocks</span></span>

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

### <span data-ttu-id="87684-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="87684-128">-Name</span></span>
<span data-ttu-id="87684-129">Имя назначения для схемы.</span><span class="sxs-lookup"><span data-stu-id="87684-129">Blueprint assignment name.</span></span>

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

### <span data-ttu-id="87684-130">-Параметр</span><span class="sxs-lookup"><span data-stu-id="87684-130">-Parameter</span></span>
<span data-ttu-id="87684-131">Параметр артефакта.</span><span class="sxs-lookup"><span data-stu-id="87684-131">Artifact parameter.</span></span>

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

### <span data-ttu-id="87684-132">-ResourceGroupParameter</span><span class="sxs-lookup"><span data-stu-id="87684-132">-ResourceGroupParameter</span></span>
<span data-ttu-id="87684-133">{{Fill ResourceGroupParameter Description}}</span><span class="sxs-lookup"><span data-stu-id="87684-133">{{Fill ResourceGroupParameter Description}}</span></span>

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

### <span data-ttu-id="87684-134">-SecureStringParameter</span><span class="sxs-lookup"><span data-stu-id="87684-134">-SecureStringParameter</span></span>
<span data-ttu-id="87684-135">Параметр Secure String для идентификатора ресурса KeyVault, имени и версии.</span><span class="sxs-lookup"><span data-stu-id="87684-135">Secure string parameter for KeyVault resource id, name and version.</span></span>

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

### <span data-ttu-id="87684-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="87684-136">-SubscriptionId</span></span>
<span data-ttu-id="87684-137">SubscriptionId, чтобы назначить проект.</span><span class="sxs-lookup"><span data-stu-id="87684-137">SubscriptionId to assign the Blueprint.</span></span>
<span data-ttu-id="87684-138">Может быть списком из строк subscriptionId, разделенных запятыми.</span><span class="sxs-lookup"><span data-stu-id="87684-138">Can be a comma delimited list of subscriptionId strings.</span></span>

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

### <span data-ttu-id="87684-139">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="87684-139">-SystemAssignedIdentity</span></span>
<span data-ttu-id="87684-140">Система присвоила идентификатор (MSI) для развертывания артефактов.</span><span class="sxs-lookup"><span data-stu-id="87684-140">System assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="87684-141">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="87684-141">-UserAssignedIdentity</span></span>
<span data-ttu-id="87684-142">Идентификатор (MSI), назначенный пользователю для развертывания артефактов.</span><span class="sxs-lookup"><span data-stu-id="87684-142">User assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="87684-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="87684-143">-Confirm</span></span>
<span data-ttu-id="87684-144">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="87684-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87684-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87684-145">-WhatIf</span></span>
<span data-ttu-id="87684-146">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="87684-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87684-147">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="87684-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87684-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87684-148">CommonParameters</span></span>
<span data-ttu-id="87684-149">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="87684-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87684-150">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87684-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87684-151">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="87684-151">INPUTS</span></span>

### <span data-ttu-id="87684-152">System. String</span><span class="sxs-lookup"><span data-stu-id="87684-152">System.String</span></span>

### <span data-ttu-id="87684-153">Microsoft. Azure. Commands. чертеж. Models. PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="87684-153">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="87684-154">System. String []</span><span class="sxs-lookup"><span data-stu-id="87684-154">System.String[]</span></span>

### <span data-ttu-id="87684-155">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="87684-155">System.Collections.Hashtable</span></span>

## <span data-ttu-id="87684-156">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="87684-156">OUTPUTS</span></span>

### <span data-ttu-id="87684-157">System. Object</span><span class="sxs-lookup"><span data-stu-id="87684-157">System.Object</span></span>
## <span data-ttu-id="87684-158">Пуск</span><span class="sxs-lookup"><span data-stu-id="87684-158">NOTES</span></span>

## <span data-ttu-id="87684-159">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="87684-159">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedservices/remove-azmanagedservicesassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Remove-AzManagedServicesAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Remove-AzManagedServicesAssignment.md
ms.openlocfilehash: a3a39db5f110f247ab58f2b4c6afcdb4536f4f50
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247333"
---
# <span data-ttu-id="8416e-101">Remove-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="8416e-101">Remove-AzManagedServicesAssignment</span></span>

## <span data-ttu-id="8416e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8416e-102">SYNOPSIS</span></span>
<span data-ttu-id="8416e-103">Удаление назначения регистрации.</span><span class="sxs-lookup"><span data-stu-id="8416e-103">Deletes a registration assignment.</span></span>

## <span data-ttu-id="8416e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8416e-104">SYNTAX</span></span>

### <span data-ttu-id="8416e-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8416e-105">Default (Default)</span></span>
```
Remove-AzManagedServicesAssignment [-Scope <String>] -Name <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8416e-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="8416e-106">ByInputObject</span></span>
```
Remove-AzManagedServicesAssignment -InputObject <PSRegistrationAssignment> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8416e-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8416e-107">DESCRIPTION</span></span>
<span data-ttu-id="8416e-108">Удаление назначения регистрации.</span><span class="sxs-lookup"><span data-stu-id="8416e-108">Deletes a registration assignment.</span></span>

## <span data-ttu-id="8416e-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8416e-109">EXAMPLES</span></span>

### <span data-ttu-id="8416e-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8416e-110">Example 1</span></span>
```
PS C:\> Remove-AzManagedServicesAssignment -Name 0413e647-6915-45e3-944d-79a587e57f80
PS C:\>
```

<span data-ttu-id="8416e-111">Удаляет назначение регистрации по имени в области по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8416e-111">Deletes the registration assignment by name at the default scope.</span></span>

### <span data-ttu-id="8416e-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="8416e-112">Example 2</span></span>
```
PS C:\> New-AzManagedServicesAssignment -RegistrationDefinitionId /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/55a89269-0347-4a9c-a778-c3f37b9f8672 -Name 12b05f0f-3426-48da-9e67-738e1dbf775f

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
12b05f0f-3426-48da-9e67-738e1dbf775f /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/12b05f0f-3426-48da-9e67-738e1dbf775f Succeeded


PS C:\> $assignment = Get-AzManagedServicesAssignment -Name 12b05f0f-3426-48da-9e67-738e1dbf775f
PS C:\> Remove-AzManagedServicesAssignment -InputObject $assignment
PS C:\>
```

<span data-ttu-id="8416e-113">Удаляет назначение регистрации, используя предоставленный объект ввода.</span><span class="sxs-lookup"><span data-stu-id="8416e-113">Deletes the registration assignment using the input object provided.</span></span>

### <span data-ttu-id="8416e-114">Пример 3</span><span class="sxs-lookup"><span data-stu-id="8416e-114">Example 3</span></span>
```
PS C:\> $auths = @(
>>   [Microsoft.Azure.Management.ManagedServices.Models.Authorization]@{RoleDefinitionId = "acdd72a7-3385-48ef-bd42-f606fba81ae7"; PrincipalId = "714160ec-87d5-42bb-8b17-287c0dd7417d" }
>>  );
PS C:\> $definition = New-AzManagedServicesDefinition -DisplayName "MyTestDefinition" -ManagedByTenantId 72f9acbf-86f1-41af-91ab-2d7ef011db47 -Authorization $auths
PS C:\> $definition

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
55a89269-0347-4a9c-a778-c3f37b9f8672 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/55a89269-0347-4a9c-a778-c3f37b9f8672 Succeeded


PS C:\> New-AzManagedServicesAssignment -RegistrationDefinition $definition

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
b279ec53-b42f-4952-bd62-cd49982e9572 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/b279ec53-b42f-4952-bd62-cd49982e9572 Succeeded


PS C:\> Remove-AzManagedServicesAssignment -Name b279ec53-b42f-4952-bd62-cd49982e9572 -Scope /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8
PS C:\>
```

<span data-ttu-id="8416e-115">Удаляет регистрацию назначения по имени в заданной области.</span><span class="sxs-lookup"><span data-stu-id="8416e-115">Deletes the registration assignment by name at the given scope.</span></span>

## <span data-ttu-id="8416e-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8416e-116">PARAMETERS</span></span>

### <span data-ttu-id="8416e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8416e-117">-DefaultProfile</span></span>
<span data-ttu-id="8416e-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8416e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8416e-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8416e-119">-InputObject</span></span>
<span data-ttu-id="8416e-120">Объект назначения регистрации.</span><span class="sxs-lookup"><span data-stu-id="8416e-120">The registration assignment object.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationAssignment
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8416e-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8416e-121">-Name</span></span>
<span data-ttu-id="8416e-122">Уникальное имя назначения регистрации.</span><span class="sxs-lookup"><span data-stu-id="8416e-122">The unique name of the Registration Assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8416e-123">-Scope</span><span class="sxs-lookup"><span data-stu-id="8416e-123">-Scope</span></span>
<span data-ttu-id="8416e-124">Область назначения регистрации.</span><span class="sxs-lookup"><span data-stu-id="8416e-124">The scope of the registration assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8416e-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8416e-125">-AsJob</span></span>
<span data-ttu-id="8416e-126">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="8416e-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8416e-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8416e-127">-Confirm</span></span>
<span data-ttu-id="8416e-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8416e-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8416e-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8416e-129">-WhatIf</span></span>
<span data-ttu-id="8416e-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8416e-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8416e-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8416e-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8416e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8416e-132">CommonParameters</span></span>
<span data-ttu-id="8416e-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8416e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8416e-134">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8416e-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8416e-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8416e-135">INPUTS</span></span>

### <span data-ttu-id="8416e-136">Microsoft. Azure. PowerShell. командлеты. ManagedServices. Models. PSRegistrationAssignment</span><span class="sxs-lookup"><span data-stu-id="8416e-136">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationAssignment</span></span>
## <span data-ttu-id="8416e-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8416e-137">OUTPUTS</span></span>

### <span data-ttu-id="8416e-138">System. void</span><span class="sxs-lookup"><span data-stu-id="8416e-138">System.Void</span></span>
## <span data-ttu-id="8416e-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="8416e-139">NOTES</span></span>

## <span data-ttu-id="8416e-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8416e-140">RELATED LINKS</span></span>

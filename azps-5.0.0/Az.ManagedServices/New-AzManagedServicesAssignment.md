---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedservices/new-azmanagedservicesassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/New-AzManagedServicesAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/New-AzManagedServicesAssignment.md
ms.openlocfilehash: 8023dde9253ccb4a1f7ff223c4dfdddf773a4728
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247334"
---
# <span data-ttu-id="b410c-101">New-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="b410c-101">New-AzManagedServicesAssignment</span></span>

## <span data-ttu-id="b410c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b410c-102">SYNOPSIS</span></span>
<span data-ttu-id="b410c-103">Создание или обновление назначения регистрации.</span><span class="sxs-lookup"><span data-stu-id="b410c-103">Creates or updates a registration assignment.</span></span>

## <span data-ttu-id="b410c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b410c-104">SYNTAX</span></span>

### <span data-ttu-id="b410c-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b410c-105">Default (Default)</span></span>
```
New-AzManagedServicesAssignment [-Name <String>] [-Scope <String>] -RegistrationDefinitionId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b410c-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="b410c-106">ByInputObject</span></span>
```
New-AzManagedServicesAssignment [-Name <String>] [-Scope <String>]
 -RegistrationDefinition <PSRegistrationDefinition> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b410c-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b410c-107">DESCRIPTION</span></span>
<span data-ttu-id="b410c-108">Создание или обновление назначения регистрации.</span><span class="sxs-lookup"><span data-stu-id="b410c-108">Creates or updates a registration assignment.</span></span>

## <span data-ttu-id="b410c-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b410c-109">EXAMPLES</span></span>

### <span data-ttu-id="b410c-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b410c-110">Example 1</span></span>
```
PS C:\> $definition = Get-AzManagedServicesDefinition
PS C:\> $definition

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
55a89269-0347-4a9c-a778-c3f37b9f8672 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/55a89269-0347-4a9c-a778-c3f37b9f8672 Succeeded

PS C:\> New-AzManagedServicesAssignment -RegistrationDefinitionId /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/55a89269-0347-4a9c-a778-c3f37b9f8672

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
12b05f0f-3426-48da-9e67-738e1dbf775f /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/12b05f0f-3426-48da-9e67-738e1dbf775f Succeeded


PS C:\>
```

<span data-ttu-id="b410c-111">Создает назначение регистрации в области по умолчанию, используя идентификатор определения регистрации.</span><span class="sxs-lookup"><span data-stu-id="b410c-111">Creates a registration assignment at the default scope using the registration definition identifier.</span></span>

### <span data-ttu-id="b410c-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="b410c-112">Example 2</span></span>
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


PS C:\>
```

<span data-ttu-id="b410c-113">Создает назначение регистрации с объектом определения регистрации в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="b410c-113">Creates a registration assignment with a registration definition object as input.</span></span>

### <span data-ttu-id="b410c-114">Пример 3</span><span class="sxs-lookup"><span data-stu-id="b410c-114">Example 3</span></span>
```
PS C:\> New-AzManagedServicesAssignment -RegistrationDefinitionId /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/55a89269-0347-4a9c-a778-c3f37b9f8672

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
12b05f0f-3426-48da-9e67-738e1dbf775f /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/12b05f0f-3426-48da-9e67-738e1dbf775f Succeeded


PS C:\> New-AzManagedServicesAssignment -RegistrationDefinitionId /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/55a89269-0347-4a9c-a778-c3f37b9f8672 -Name 12b05f0f-3426-48da-9e67-738e1dbf775f

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
12b05f0f-3426-48da-9e67-738e1dbf775f /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/12b05f0f-3426-48da-9e67-738e1dbf775f Succeeded

PS C:\>
```

<span data-ttu-id="b410c-115">Обновляет назначение регистрации с помощью идентификатора определения регистрации и имени.</span><span class="sxs-lookup"><span data-stu-id="b410c-115">Updates a registration assignment with a registration definition identifier and name.</span></span>


## <span data-ttu-id="b410c-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b410c-116">PARAMETERS</span></span>

### <span data-ttu-id="b410c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b410c-117">-DefaultProfile</span></span>
<span data-ttu-id="b410c-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b410c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b410c-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b410c-119">-Name</span></span>
<span data-ttu-id="b410c-120">Уникальное имя назначения регистрации.</span><span class="sxs-lookup"><span data-stu-id="b410c-120">The unique name of the Registration Assignment.</span></span>

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

### <span data-ttu-id="b410c-121">-RegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="b410c-121">-RegistrationDefinition</span></span>
<span data-ttu-id="b410c-122">Входной объект определения регистрации.</span><span class="sxs-lookup"><span data-stu-id="b410c-122">The registration definition input object.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b410c-123">-RegistrationDefinitionId</span><span class="sxs-lookup"><span data-stu-id="b410c-123">-RegistrationDefinitionId</span></span>
<span data-ttu-id="b410c-124">Полный идентификатор ресурса для определения регистрации.</span><span class="sxs-lookup"><span data-stu-id="b410c-124">The fully qualified resource id of the registration definition.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b410c-125">-Scope</span><span class="sxs-lookup"><span data-stu-id="b410c-125">-Scope</span></span>
<span data-ttu-id="b410c-126">Область, в которой должно быть создано назначение регистрации.</span><span class="sxs-lookup"><span data-stu-id="b410c-126">The scope where the registration assignment should be created.</span></span>

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

### <span data-ttu-id="b410c-127">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b410c-127">-AsJob</span></span>
<span data-ttu-id="b410c-128">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="b410c-128">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b410c-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b410c-129">-Confirm</span></span>
<span data-ttu-id="b410c-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b410c-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b410c-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b410c-131">-WhatIf</span></span>
<span data-ttu-id="b410c-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b410c-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b410c-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b410c-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b410c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b410c-134">CommonParameters</span></span>
<span data-ttu-id="b410c-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b410c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b410c-136">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b410c-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b410c-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b410c-137">INPUTS</span></span>

### <span data-ttu-id="b410c-138">Microsoft. Azure. PowerShell. командлеты. ManagedServices. Models. PSRegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="b410c-138">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition</span></span>
### <span data-ttu-id="b410c-139">System. String</span><span class="sxs-lookup"><span data-stu-id="b410c-139">System.String</span></span>
## <span data-ttu-id="b410c-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b410c-140">OUTPUTS</span></span>

### <span data-ttu-id="b410c-141">Microsoft. Azure. PowerShell. командлеты. ManagedServices. Models. PSRegistrationAssignment</span><span class="sxs-lookup"><span data-stu-id="b410c-141">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationAssignment</span></span>
## <span data-ttu-id="b410c-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="b410c-142">NOTES</span></span>

## <span data-ttu-id="b410c-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b410c-143">RELATED LINKS</span></span>
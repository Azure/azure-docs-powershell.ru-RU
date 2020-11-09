---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedservices/remove-azmanagedservicesassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Remove-AzManagedServicesAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Remove-AzManagedServicesAssignment.md
ms.openlocfilehash: 5f2328ba75a0142a61238665eef41e32bf1fbba6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243524"
---
# <span data-ttu-id="65c63-101">Remove-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="65c63-101">Remove-AzManagedServicesAssignment</span></span>

## <span data-ttu-id="65c63-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="65c63-102">SYNOPSIS</span></span>
<span data-ttu-id="65c63-103">Удаление назначения регистрации.</span><span class="sxs-lookup"><span data-stu-id="65c63-103">Deletes a registration assignment.</span></span>

## <span data-ttu-id="65c63-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="65c63-104">SYNTAX</span></span>

### <span data-ttu-id="65c63-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="65c63-105">Default (Default)</span></span>
```
Remove-AzManagedServicesAssignment [[-Scope] <String>] -Id <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65c63-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="65c63-106">ByResourceId</span></span>
```
Remove-AzManagedServicesAssignment -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65c63-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="65c63-107">ByInputObject</span></span>
```
Remove-AzManagedServicesAssignment -InputObject <PSRegistrationAssignment> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65c63-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="65c63-108">DESCRIPTION</span></span>
<span data-ttu-id="65c63-109">Удаление назначения регистрации.</span><span class="sxs-lookup"><span data-stu-id="65c63-109">Deletes a registration assignment.</span></span>

## <span data-ttu-id="65c63-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="65c63-110">EXAMPLES</span></span>

### <span data-ttu-id="65c63-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="65c63-111">Example 1</span></span>
```powershell
PS C:\Remove-AzManagedServicesAssignment -Id b037e73c-815e-4472-868f-59e51b49b949

Name                                 RegistrationDefinitionId
----                                 ------------------------
b037e73c-815e-4472-868f-59e51b49b949 /subscriptions/38bd4bef-41ff-45b5-b3af-d03e55a4ca15/providers/Microsoft.ManagedServices/registrationDefinitions/be2f72e6-93e0-4d3f-ac50-9a756ed4ffa7
```

<span data-ttu-id="65c63-112">Удаление назначения регистрации в области по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="65c63-112">Deletes the registration assignment under the default scope.</span></span>

### <span data-ttu-id="65c63-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="65c63-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzManagedServicesAssignment -ResourceId /subscriptions/38bd4bef-41ff-45b5-b3af-d03e55a4ca15/providers/Microsoft.ManagedServices/registrationAssignments/88ba878b-9a3c-40c3-80da-015cbe488a2f

Name                                 RegistrationDefinitionId
----                                 ------------------------
88ba878b-9a3c-40c3-80da-015cbe488a2f /subscriptions/38bd4bef-41ff-45b5-b3af-d03e55a4ca15/providers/Microsoft.ManagedServices/registrationDefinitions/40be0299-6573-4391-be2f-b41dd4aaf4f9
```

<span data-ttu-id="65c63-114">Удаляет назначение регистрации с учетом полного ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="65c63-114">Deletes the registration assignment given the fully qualified resource id.</span></span>

### <span data-ttu-id="65c63-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="65c63-115">Example 3</span></span>
```powershell
PS C:\> $assignment = New-AzManagedServicesAssignment -RegistrationDefinitionId /subscriptions/38bd4bef-41ff-45b5-b3af-d03e55a4ca15/providers/Microsoft.ManagedServices/registrationDefinitions/33974646-9bce-461d-89eb-331f20fca33c
PS C:\> Remove-AzManagedServicesAssignment -InputObject $assignment
```

<span data-ttu-id="65c63-116">Удаляет назначение регистрации, используя предоставленный объект ввода.</span><span class="sxs-lookup"><span data-stu-id="65c63-116">Deletes the registration assignment using the input object provided.</span></span>

## <span data-ttu-id="65c63-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="65c63-117">PARAMETERS</span></span>

### <span data-ttu-id="65c63-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="65c63-118">-AsJob</span></span>
<span data-ttu-id="65c63-119">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="65c63-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="65c63-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65c63-120">-DefaultProfile</span></span>
<span data-ttu-id="65c63-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="65c63-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65c63-122">-ID</span><span class="sxs-lookup"><span data-stu-id="65c63-122">-Id</span></span>
<span data-ttu-id="65c63-123">GUID назначения регистрации (например, b0c052e5-c437-4771-a476-8b1201158a57);</span><span class="sxs-lookup"><span data-stu-id="65c63-123">The registration assignment GUID (for example, b0c052e5-c437-4771-a476-8b1201158a57)</span></span>
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

### <span data-ttu-id="65c63-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="65c63-124">-InputObject</span></span>
<span data-ttu-id="65c63-125">Объект назначения регистрации.</span><span class="sxs-lookup"><span data-stu-id="65c63-125">The registration assignment object.</span></span>

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

### <span data-ttu-id="65c63-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="65c63-126">-ResourceId</span></span>
<span data-ttu-id="65c63-127">Полный идентификатор ресурса для задания регистрации (например,/subscriptions/bb6d49b2-603d-489f-b6ca-ca4dc497c749/providers/Microsoft.ManagedServices/registrationAssignments/b0c052e5-c437-4771-a476-8b1201158a57).</span><span class="sxs-lookup"><span data-stu-id="65c63-127">The fully qualified resource id of the registration assignment (for example, /subscriptions/bb6d49b2-603d-489f-b6ca-ca4dc497c749/providers/Microsoft.ManagedServices/registrationAssignments/b0c052e5-c437-4771-a476-8b1201158a57).</span></span>

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

### <span data-ttu-id="65c63-128">-Scope</span><span class="sxs-lookup"><span data-stu-id="65c63-128">-Scope</span></span>
<span data-ttu-id="65c63-129">Область, в которой должно быть создано назначение регистрации.</span><span class="sxs-lookup"><span data-stu-id="65c63-129">The scope where the registration assignment should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65c63-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="65c63-130">-Confirm</span></span>
<span data-ttu-id="65c63-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="65c63-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65c63-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65c63-132">-WhatIf</span></span>
<span data-ttu-id="65c63-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="65c63-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65c63-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="65c63-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65c63-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65c63-135">CommonParameters</span></span>
<span data-ttu-id="65c63-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="65c63-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65c63-137">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="65c63-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65c63-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="65c63-138">INPUTS</span></span>

### <span data-ttu-id="65c63-139">System. String</span><span class="sxs-lookup"><span data-stu-id="65c63-139">System.String</span></span>

### <span data-ttu-id="65c63-140">Microsoft. Azure. PowerShell. командлеты. ManagedServices. Models. PSRegistrationAssignment</span><span class="sxs-lookup"><span data-stu-id="65c63-140">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationAssignment</span></span>

## <span data-ttu-id="65c63-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="65c63-141">OUTPUTS</span></span>

### <span data-ttu-id="65c63-142">Microsoft. Azure. PowerShell. командлеты. ManagedServices. Models. PSRegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="65c63-142">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition</span></span>

## <span data-ttu-id="65c63-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="65c63-143">NOTES</span></span>

## <span data-ttu-id="65c63-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="65c63-144">RELATED LINKS</span></span>
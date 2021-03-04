---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/powershell/module/az.managedservices/remove-azmanagedservicesdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Remove-AzManagedServicesDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Remove-AzManagedServicesDefinition.md
ms.openlocfilehash: 20c025399197f780331f6281c05f243744544c41
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957080"
---
# <span data-ttu-id="ec07b-101">Remove-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="ec07b-101">Remove-AzManagedServicesDefinition</span></span>

## <span data-ttu-id="ec07b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec07b-102">SYNOPSIS</span></span>
<span data-ttu-id="ec07b-103">Удаляет определение регистрации.</span><span class="sxs-lookup"><span data-stu-id="ec07b-103">Deletes the registration definition.</span></span>

## <span data-ttu-id="ec07b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ec07b-104">SYNTAX</span></span>

### <span data-ttu-id="ec07b-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ec07b-105">Default (Default)</span></span>
```
Remove-AzManagedServicesDefinition [-Scope <String>] -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec07b-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="ec07b-106">ByInputObject</span></span>
```
Remove-AzManagedServicesDefinition -InputObject <PSRegistrationDefinition>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ec07b-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ec07b-107">DESCRIPTION</span></span>
<span data-ttu-id="ec07b-108">Удаляет определение регистрации.</span><span class="sxs-lookup"><span data-stu-id="ec07b-108">Deletes the registration definition.</span></span>

## <span data-ttu-id="ec07b-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ec07b-109">EXAMPLES</span></span>

### <span data-ttu-id="ec07b-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ec07b-110">Example 1</span></span>
```
PS C:\> Remove-AzManagedServicesDefinition -Name 0c146106-c927-4098-a7ca-30bbcf44a502
PS C:\>
```

<span data-ttu-id="ec07b-111">Удаляет определение регистрации по имени из области по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ec07b-111">Removes the registration definition by name at the default scope.</span></span>

### <span data-ttu-id="ec07b-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="ec07b-112">Example 2</span></span>
```
PS C:\> $definition = New-AzManagedServicesDefinition -DisplayName "MyTestDefinition" -ManagedByTenantId 72f9acbf-86f1-41af-91ab-2d7ef011db47 -RoleDefinitionId acdd72a7-3385-48ef-bd42-f606fba81ae7 -PrincipalId 714160ec-87d5-42bb-8b17-287c0dd7417d
PS C:\> Remove-AzManagedServicesDefinition -InputObject $definition
PS C:\>
```

<span data-ttu-id="ec07b-113">Удаляет определение регистрации с учетом входного объекта.</span><span class="sxs-lookup"><span data-stu-id="ec07b-113">Deletes the registration definition given the input object.</span></span>

## <span data-ttu-id="ec07b-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ec07b-114">PARAMETERS</span></span>

### <span data-ttu-id="ec07b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec07b-115">-DefaultProfile</span></span>
<span data-ttu-id="ec07b-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ec07b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec07b-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ec07b-117">-InputObject</span></span>
<span data-ttu-id="ec07b-118">Объект определения регистрации.</span><span class="sxs-lookup"><span data-stu-id="ec07b-118">The registration definition object.</span></span>

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

### <span data-ttu-id="ec07b-119">-Name</span><span class="sxs-lookup"><span data-stu-id="ec07b-119">-Name</span></span>
<span data-ttu-id="ec07b-120">Уникальное имя определения регистрации.</span><span class="sxs-lookup"><span data-stu-id="ec07b-120">The unique name of the Registration Definition.</span></span>

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

### <span data-ttu-id="ec07b-121">-Scope</span><span class="sxs-lookup"><span data-stu-id="ec07b-121">-Scope</span></span>
<span data-ttu-id="ec07b-122">Область создания определения регистрации.</span><span class="sxs-lookup"><span data-stu-id="ec07b-122">The scope where the registration definition created.</span></span>

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

### <span data-ttu-id="ec07b-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ec07b-123">-Confirm</span></span>
<span data-ttu-id="ec07b-124">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ec07b-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec07b-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec07b-125">-WhatIf</span></span>
<span data-ttu-id="ec07b-126">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ec07b-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec07b-127">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ec07b-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec07b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec07b-128">CommonParameters</span></span>
<span data-ttu-id="ec07b-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec07b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec07b-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ec07b-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec07b-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ec07b-131">INPUTS</span></span>

### <span data-ttu-id="ec07b-132">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="ec07b-132">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition</span></span>
## <span data-ttu-id="ec07b-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ec07b-133">OUTPUTS</span></span>

### <span data-ttu-id="ec07b-134">System.Void</span><span class="sxs-lookup"><span data-stu-id="ec07b-134">System.Void</span></span>
## <span data-ttu-id="ec07b-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ec07b-135">NOTES</span></span>

## <span data-ttu-id="ec07b-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ec07b-136">RELATED LINKS</span></span>

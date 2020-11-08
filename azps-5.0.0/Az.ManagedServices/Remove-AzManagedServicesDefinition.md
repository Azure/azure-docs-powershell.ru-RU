---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedservices/remove-azmanagedservicesdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Remove-AzManagedServicesDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Remove-AzManagedServicesDefinition.md
ms.openlocfilehash: 2b81a1983bb89af48115ead85c3392cc3d762734
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247332"
---
# <span data-ttu-id="eb179-101">Remove-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="eb179-101">Remove-AzManagedServicesDefinition</span></span>

## <span data-ttu-id="eb179-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="eb179-102">SYNOPSIS</span></span>
<span data-ttu-id="eb179-103">Удаляет определение регистрации.</span><span class="sxs-lookup"><span data-stu-id="eb179-103">Deletes the registration definition.</span></span>

## <span data-ttu-id="eb179-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="eb179-104">SYNTAX</span></span>

### <span data-ttu-id="eb179-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="eb179-105">Default (Default)</span></span>
```
Remove-AzManagedServicesDefinition [-Scope <String>] -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb179-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="eb179-106">ByInputObject</span></span>
```
Remove-AzManagedServicesDefinition -InputObject <PSRegistrationDefinition>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eb179-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="eb179-107">DESCRIPTION</span></span>
<span data-ttu-id="eb179-108">Удаляет определение регистрации.</span><span class="sxs-lookup"><span data-stu-id="eb179-108">Deletes the registration definition.</span></span>

## <span data-ttu-id="eb179-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="eb179-109">EXAMPLES</span></span>

### <span data-ttu-id="eb179-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="eb179-110">Example 1</span></span>
```
PS C:\> Remove-AzManagedServicesDefinition -Name 0c146106-c927-4098-a7ca-30bbcf44a502
PS C:\>
```

<span data-ttu-id="eb179-111">Удаляет определение регистрации по имени в области по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="eb179-111">Removes the registration definition by name at the default scope.</span></span>

### <span data-ttu-id="eb179-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="eb179-112">Example 2</span></span>
```
PS C:\> $definition = New-AzManagedServicesDefinition -DisplayName "MyTestDefinition" -ManagedByTenantId 72f9acbf-86f1-41af-91ab-2d7ef011db47 -RoleDefinitionId acdd72a7-3385-48ef-bd42-f606fba81ae7 -PrincipalId 714160ec-87d5-42bb-8b17-287c0dd7417d
PS C:\> Remove-AzManagedServicesDefinition -InputObject $definition
PS C:\>
```

<span data-ttu-id="eb179-113">Удаляет определение регистрации, полученное от объекта ввода.</span><span class="sxs-lookup"><span data-stu-id="eb179-113">Deletes the registration definition given the input object.</span></span>

## <span data-ttu-id="eb179-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="eb179-114">PARAMETERS</span></span>

### <span data-ttu-id="eb179-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb179-115">-DefaultProfile</span></span>
<span data-ttu-id="eb179-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="eb179-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eb179-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eb179-117">-InputObject</span></span>
<span data-ttu-id="eb179-118">Объект определения регистрации.</span><span class="sxs-lookup"><span data-stu-id="eb179-118">The registration definition object.</span></span>

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

### <span data-ttu-id="eb179-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="eb179-119">-Name</span></span>
<span data-ttu-id="eb179-120">Уникальное имя определения регистрации.</span><span class="sxs-lookup"><span data-stu-id="eb179-120">The unique name of the Registration Definition.</span></span>

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

### <span data-ttu-id="eb179-121">-Scope</span><span class="sxs-lookup"><span data-stu-id="eb179-121">-Scope</span></span>
<span data-ttu-id="eb179-122">Область, в которой создано определение регистрации.</span><span class="sxs-lookup"><span data-stu-id="eb179-122">The scope where the registration definition created.</span></span>

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

### <span data-ttu-id="eb179-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eb179-123">-Confirm</span></span>
<span data-ttu-id="eb179-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="eb179-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb179-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb179-125">-WhatIf</span></span>
<span data-ttu-id="eb179-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="eb179-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eb179-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="eb179-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb179-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb179-128">CommonParameters</span></span>
<span data-ttu-id="eb179-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="eb179-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb179-130">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eb179-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb179-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="eb179-131">INPUTS</span></span>

### <span data-ttu-id="eb179-132">Microsoft. Azure. PowerShell. командлеты. ManagedServices. Models. PSRegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="eb179-132">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition</span></span>
## <span data-ttu-id="eb179-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="eb179-133">OUTPUTS</span></span>

### <span data-ttu-id="eb179-134">System. void</span><span class="sxs-lookup"><span data-stu-id="eb179-134">System.Void</span></span>
## <span data-ttu-id="eb179-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="eb179-135">NOTES</span></span>

## <span data-ttu-id="eb179-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="eb179-136">RELATED LINKS</span></span>

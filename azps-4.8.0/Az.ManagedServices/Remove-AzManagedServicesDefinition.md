---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedservices/remove-azmanagedservicesdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Remove-AzManagedServicesDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Remove-AzManagedServicesDefinition.md
ms.openlocfilehash: ffebb4e3fca417c896939bb54ed1c0af1c42f7fc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236103"
---
# <span data-ttu-id="65f81-101">Remove-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="65f81-101">Remove-AzManagedServicesDefinition</span></span>

## <span data-ttu-id="65f81-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="65f81-102">SYNOPSIS</span></span>
<span data-ttu-id="65f81-103">Удаляет определение регистрации.</span><span class="sxs-lookup"><span data-stu-id="65f81-103">Deletes the registration definition.</span></span>

## <span data-ttu-id="65f81-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="65f81-104">SYNTAX</span></span>

### <span data-ttu-id="65f81-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="65f81-105">Default (Default)</span></span>
```
Remove-AzManagedServicesDefinition -Id <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65f81-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="65f81-106">ByResourceId</span></span>
```
Remove-AzManagedServicesDefinition -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65f81-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="65f81-107">ByInputObject</span></span>
```
Remove-AzManagedServicesDefinition -InputObject <PSRegistrationDefinition> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65f81-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="65f81-108">DESCRIPTION</span></span>
<span data-ttu-id="65f81-109">Удаляет определение регистрации.</span><span class="sxs-lookup"><span data-stu-id="65f81-109">Deletes the registration definition.</span></span>

## <span data-ttu-id="65f81-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="65f81-110">EXAMPLES</span></span>

### <span data-ttu-id="65f81-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="65f81-111">Example 1</span></span>
```powershell
PS C:\> Remove-RegistrationDefinition -Id 0513b566-cab0-4fef-9b53-a285cd33389f
```

<span data-ttu-id="65f81-112">Удаляет определение регистрации, заданное идентификатором.</span><span class="sxs-lookup"><span data-stu-id="65f81-112">Removes the registration definition given it identifier.</span></span>

### <span data-ttu-id="65f81-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="65f81-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzManagedServicesDefinition -ResourceId /subscriptions/38bd4bef-41ff-45b5-b3af-d03e55a4ca15/providers/Microsoft.ManagedServices/registrationDefinitions/11b7c937-c5c1-4dd1-9a77-204591f93fcd

Name                                 ManagedByTenantId                    PrincipalId                          RoleDefinitionId
----                                 -----------------                    -----------                          ----------------
11b7c937-c5c1-4dd1-9a77-204591f93fcd bab3375b-6197-4a15-a44b-16c41faa91d7 d6f6c88a-5b7a-455e-ba40-ce146d4d3671 acdd72a7-3385-48ef-bd42-f606fba81ae7
```

<span data-ttu-id="65f81-114">Удаляет определение регистрации по полному идентификатору ресурса.</span><span class="sxs-lookup"><span data-stu-id="65f81-114">Removes the registration definition given the fully qualified resource id.</span></span> 

### <span data-ttu-id="65f81-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="65f81-115">Example 3</span></span>
```powershell
PS C:\> $def = New-AzManagedServicesDefinition -RegistrationDefinitionName 572e1807-b80b-4401-9128-1968f432a5ad -ManagedByTenantId "bab3375b-6197-4a15-a44b-16c41faa91d7" -PrincipalId "d6f6c88a-5b7a-455e-ba40-ce146d4d3671" -RoleDefinitionId "acdd72a7-3385-48ef-bd42-f606fba81ae7"
PS C:\> Remove-AzManagedServicesDefinition -InputObject $def

Name                                 ManagedByTenantId                    PrincipalId                          RoleDefinitionId
----                                 -----------------                    -----------                          ----------------
eee59839-119f-453f-adec-4a72a8687125 bab3375b-6197-4a15-a44b-16c41faa91d7 d6f6c88a-5b7a-455e-ba40-ce146d4d3671 acdd72a7-3385-48ef-bd42-f606fba81ae7
```

<span data-ttu-id="65f81-116">Удаляет определение регистрации, полученное от объекта.</span><span class="sxs-lookup"><span data-stu-id="65f81-116">Deletes the registration definition given the object.</span></span>

## <span data-ttu-id="65f81-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="65f81-117">PARAMETERS</span></span>

### <span data-ttu-id="65f81-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="65f81-118">-AsJob</span></span>
<span data-ttu-id="65f81-119">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="65f81-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="65f81-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65f81-120">-DefaultProfile</span></span>
<span data-ttu-id="65f81-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="65f81-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65f81-122">-ID</span><span class="sxs-lookup"><span data-stu-id="65f81-122">-Id</span></span>
<span data-ttu-id="65f81-123">Идентификатор определения регистрации.</span><span class="sxs-lookup"><span data-stu-id="65f81-123">The registration definition identifier.</span></span>

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

### <span data-ttu-id="65f81-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="65f81-124">-InputObject</span></span>
<span data-ttu-id="65f81-125">Объект определения регистрации.</span><span class="sxs-lookup"><span data-stu-id="65f81-125">The registration definition object.</span></span>

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

### <span data-ttu-id="65f81-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="65f81-126">-ResourceId</span></span>
<span data-ttu-id="65f81-127">ResourceId (ИД) определения регистрации</span><span class="sxs-lookup"><span data-stu-id="65f81-127">ResourceId of the registration definition</span></span>

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

### <span data-ttu-id="65f81-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="65f81-128">-Confirm</span></span>
<span data-ttu-id="65f81-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="65f81-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65f81-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65f81-130">-WhatIf</span></span>
<span data-ttu-id="65f81-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="65f81-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65f81-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="65f81-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65f81-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65f81-133">CommonParameters</span></span>
<span data-ttu-id="65f81-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="65f81-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65f81-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="65f81-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65f81-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="65f81-136">INPUTS</span></span>

### <span data-ttu-id="65f81-137">Ничего</span><span class="sxs-lookup"><span data-stu-id="65f81-137">None</span></span>

## <span data-ttu-id="65f81-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="65f81-138">OUTPUTS</span></span>

### <span data-ttu-id="65f81-139">Microsoft. Azure. PowerShell. командлеты. ManagedServices. Models. PSRegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="65f81-139">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition</span></span>

## <span data-ttu-id="65f81-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="65f81-140">NOTES</span></span>

## <span data-ttu-id="65f81-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="65f81-141">RELATED LINKS</span></span>
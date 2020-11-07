---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedservices/new-azmanagedservicesdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/New-AzManagedServicesDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/New-AzManagedServicesDefinition.md
ms.openlocfilehash: 8bcf260156584ddf7c8c2ac0ec347a59214f20c3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720405"
---
# <span data-ttu-id="d08bd-101">New-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="d08bd-101">New-AzManagedServicesDefinition</span></span>

## <span data-ttu-id="d08bd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d08bd-102">SYNOPSIS</span></span>
<span data-ttu-id="d08bd-103">Создание или обновление определения регистрации.</span><span class="sxs-lookup"><span data-stu-id="d08bd-103">Creates or updates a registration definition.</span></span>

## <span data-ttu-id="d08bd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d08bd-104">SYNTAX</span></span>

### <span data-ttu-id="d08bd-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d08bd-105">Default (Default)</span></span>
```
New-AzManagedServicesDefinition -Name <String> -ManagedByTenantId <String>
 -PrincipalId <String> -RoleDefinitionId <String> [-Description <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d08bd-106">ByPlan</span><span class="sxs-lookup"><span data-stu-id="d08bd-106">ByPlan</span></span>
```
New-AzManagedServicesDefinition -Name <String> -ManagedByTenantId <String>
 -PrincipalId <String> -RoleDefinitionId <String> [-Description <String>] -PlanName <String>
 -PlanPublisher <String> -PlanProduct <String> -PlanVersion <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d08bd-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d08bd-107">DESCRIPTION</span></span>
<span data-ttu-id="d08bd-108">Создание или обновление определения регистрации.</span><span class="sxs-lookup"><span data-stu-id="d08bd-108">Creates or updates a registration definition.</span></span>

## <span data-ttu-id="d08bd-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d08bd-109">EXAMPLES</span></span>

### <span data-ttu-id="d08bd-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d08bd-110">Example 1</span></span>
```powershell
PS C:\> PS C:\> New-AzManagedServicesDefinition -Name name -ManagedByTenantId bab3375b-6197-4a15-a44b-16c41faa91d7 -PrincipalId d6f6c88a-5b7a-455e-ba40-ce146d4d3671 -RoleDefinitionId acdd72a7-3385-48ef-bd42-f606fba81ae7 -Description mydef

Name                                 ManagedByTenantId                    PrincipalId                          RoleDefinitionId
----                                 -----------------                    -----------                          ----------------
fdad02a1-a715-4352-844f-2923233590da bab3375b-6197-4a15-a44b-16c41faa91d7 d6f6c88a-5b7a-455e-ba40-ce146d4d3671 acdd72a7-3385-48ef-bd42-f606fba81ae7
```

<span data-ttu-id="d08bd-111">Создает или обновляет определение регистрации с учетом необходимых параметров.</span><span class="sxs-lookup"><span data-stu-id="d08bd-111">Creates or updates a registration definition given the required parameters.</span></span>

### <span data-ttu-id="d08bd-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="d08bd-112">Example 2</span></span>
```powershell
PS C> New-AzManagedServicesDefinition -Name asd -ManagedByTenantId "bab3375b-6197-4a15-a44b-16c41faa91d7" -PrincipalId "d6f6c88a-5b7a-455e-ba40-ce146d4d3671" -RoleDefinitionId "acdd72a7-3385-48ef-bd42-f606fba81ae7" -PlanName plan -PlanPublisher publisher -PlanProduct product -PlanVersion 0.1

Name                                 ManagedByTenantId                    PrincipalId                          RoleDefinitionId
----                                 -----------------                    -----------                          ----------------
8cde7c19-1750-468e-973e-b711549edc35 bab3375b-6197-4a15-a44b-16c41faa91d7 d6f6c88a-5b7a-455e-ba40-ce146d4d3671 acdd72a7-3385-48ef-bd42-f606fba81ae7
```

<span data-ttu-id="d08bd-113">Создание или обновление определения регистрации с учетом сведений о плане.</span><span class="sxs-lookup"><span data-stu-id="d08bd-113">Creates or updates a registration definition with the plan details.</span></span>

## <span data-ttu-id="d08bd-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d08bd-114">PARAMETERS</span></span>

### <span data-ttu-id="d08bd-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d08bd-115">-AsJob</span></span>
<span data-ttu-id="d08bd-116">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="d08bd-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d08bd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d08bd-117">-DefaultProfile</span></span>
<span data-ttu-id="d08bd-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d08bd-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d08bd-119">-Описание</span><span class="sxs-lookup"><span data-stu-id="d08bd-119">-Description</span></span>
<span data-ttu-id="d08bd-120">Описание определения регистрации.</span><span class="sxs-lookup"><span data-stu-id="d08bd-120">The description of the Registration Definition.</span></span>

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

### <span data-ttu-id="d08bd-121">-ManagedByTenantId</span><span class="sxs-lookup"><span data-stu-id="d08bd-121">-ManagedByTenantId</span></span>
<span data-ttu-id="d08bd-122">Идентификатор клиента ManagedBy.</span><span class="sxs-lookup"><span data-stu-id="d08bd-122">The ManagedBy Tenant Identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d08bd-123">-PlanName</span><span class="sxs-lookup"><span data-stu-id="d08bd-123">-PlanName</span></span>
<span data-ttu-id="d08bd-124">Название плана.</span><span class="sxs-lookup"><span data-stu-id="d08bd-124">The name of the plan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPlan
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d08bd-125">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="d08bd-125">-PlanProduct</span></span>
<span data-ttu-id="d08bd-126">Название продукта.</span><span class="sxs-lookup"><span data-stu-id="d08bd-126">The name of the Product.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPlan
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d08bd-127">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="d08bd-127">-PlanPublisher</span></span>
<span data-ttu-id="d08bd-128">Имя издателя.</span><span class="sxs-lookup"><span data-stu-id="d08bd-128">The name of the Publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPlan
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d08bd-129">-PlanVersion</span><span class="sxs-lookup"><span data-stu-id="d08bd-129">-PlanVersion</span></span>
<span data-ttu-id="d08bd-130">Номер версии плана.</span><span class="sxs-lookup"><span data-stu-id="d08bd-130">The version number of the plan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPlan
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d08bd-131">-PrincipalId</span><span class="sxs-lookup"><span data-stu-id="d08bd-131">-PrincipalId</span></span>
<span data-ttu-id="d08bd-132">Идентификатор участника ManagedBy.</span><span class="sxs-lookup"><span data-stu-id="d08bd-132">The ManagedBy Principal Identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d08bd-133">-RegistrationDefinitionName</span><span class="sxs-lookup"><span data-stu-id="d08bd-133">-RegistrationDefinitionName</span></span>
<span data-ttu-id="d08bd-134">Имя определения регистрации.</span><span class="sxs-lookup"><span data-stu-id="d08bd-134">The name of the Registration Definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d08bd-135">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="d08bd-135">-RoleDefinitionId</span></span>
<span data-ttu-id="d08bd-136">Идентификатор роли поставщика управляемых служб.</span><span class="sxs-lookup"><span data-stu-id="d08bd-136">The Managed Service Provider's Role Identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d08bd-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d08bd-137">-Confirm</span></span>
<span data-ttu-id="d08bd-138">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d08bd-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d08bd-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d08bd-139">-WhatIf</span></span>
<span data-ttu-id="d08bd-140">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d08bd-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d08bd-141">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d08bd-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d08bd-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d08bd-142">CommonParameters</span></span>
<span data-ttu-id="d08bd-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d08bd-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d08bd-144">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d08bd-144">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d08bd-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d08bd-145">INPUTS</span></span>

### <span data-ttu-id="d08bd-146">Ничего</span><span class="sxs-lookup"><span data-stu-id="d08bd-146">None</span></span>

## <span data-ttu-id="d08bd-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d08bd-147">OUTPUTS</span></span>

### <span data-ttu-id="d08bd-148">Microsoft. Azure. PowerShell. командлеты. ManagedServices. Models. PSRegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="d08bd-148">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition</span></span>

## <span data-ttu-id="d08bd-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="d08bd-149">NOTES</span></span>

## <span data-ttu-id="d08bd-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d08bd-150">RELATED LINKS</span></span>

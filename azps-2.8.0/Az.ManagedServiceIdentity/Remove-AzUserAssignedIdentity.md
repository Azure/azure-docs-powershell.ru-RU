---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServiceIdentity.dll-Help.xml
Module Name: Az.ManagedServiceIdentity
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedserviceidentity/remove-azuserassignedidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServiceIdentity/ManagedServiceIdentity/help/Remove-AzUserAssignedIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServiceIdentity/ManagedServiceIdentity/help/Remove-AzUserAssignedIdentity.md
ms.openlocfilehash: 7b3a231af55bfc16584426fe16c5cedcec50b8b0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720415"
---
# <span data-ttu-id="ddd1e-101">Remove-AzUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="ddd1e-101">Remove-AzUserAssignedIdentity</span></span>

## <span data-ttu-id="ddd1e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ddd1e-102">SYNOPSIS</span></span>
<span data-ttu-id="ddd1e-103">Удаляет пользователя, которому назначено удостоверение.</span><span class="sxs-lookup"><span data-stu-id="ddd1e-103">Removes a User Assigned Identity.</span></span>

## <span data-ttu-id="ddd1e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ddd1e-104">SYNTAX</span></span>

### <span data-ttu-id="ddd1e-105">ResourceGroupAndNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ddd1e-105">ResourceGroupAndNameParameterSet (Default)</span></span>
```
Remove-AzUserAssignedIdentity [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ddd1e-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ddd1e-106">InputObjectParameterSet</span></span>
```
Remove-AzUserAssignedIdentity -InputObject <PsUserAssignedIdentity> [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ddd1e-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ddd1e-107">ResourceIdParameterSet</span></span>
```
Remove-AzUserAssignedIdentity -ResourceId <String> [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ddd1e-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ddd1e-108">DESCRIPTION</span></span>
<span data-ttu-id="ddd1e-109">Средство **Remove-AzUserAssignedIdentity** Удаляет указанного пользователя, которому назначено удостоверение.</span><span class="sxs-lookup"><span data-stu-id="ddd1e-109">The **Remove-AzUserAssignedIdentity** deletes the specified User Assigned Identity.</span></span>

## <span data-ttu-id="ddd1e-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ddd1e-110">EXAMPLES</span></span>

### <span data-ttu-id="ddd1e-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ddd1e-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzUserAssignedIdentity -ResourceGroupName PSRG -Name ID1
```

<span data-ttu-id="ddd1e-112">В этом примере командлет удаляет удостоверение **id1** в разделе "Группа ресурсов" **PSRG**.</span><span class="sxs-lookup"><span data-stu-id="ddd1e-112">This example cmdlet deletes the identity **ID1** under resource group **PSRG**.</span></span>
<span data-ttu-id="ddd1e-113">Задан</span><span class="sxs-lookup"><span data-stu-id="ddd1e-113">True</span></span>

## <span data-ttu-id="ddd1e-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ddd1e-114">PARAMETERS</span></span>

### <span data-ttu-id="ddd1e-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ddd1e-115">-AsJob</span></span>
<span data-ttu-id="ddd1e-116">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="ddd1e-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ddd1e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddd1e-117">-DefaultProfile</span></span>
<span data-ttu-id="ddd1e-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ddd1e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ddd1e-119">-Force</span><span class="sxs-lookup"><span data-stu-id="ddd1e-119">-Force</span></span>
<span data-ttu-id="ddd1e-120">{Определение принудительной заливки}}</span><span class="sxs-lookup"><span data-stu-id="ddd1e-120">{{Fill Force Description}}</span></span>

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

### <span data-ttu-id="ddd1e-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ddd1e-121">-InputObject</span></span>
<span data-ttu-id="ddd1e-122">Объект Identity.</span><span class="sxs-lookup"><span data-stu-id="ddd1e-122">The Identity object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ManagedServiceIdentity.Models.PsUserAssignedIdentity
Parameter Sets: InputObjectParameterSet
Aliases: Identity

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ddd1e-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ddd1e-123">-Name</span></span>
<span data-ttu-id="ddd1e-124">Имя удостоверения.</span><span class="sxs-lookup"><span data-stu-id="ddd1e-124">The Identity name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupAndNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddd1e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ddd1e-125">-ResourceGroupName</span></span>
<span data-ttu-id="ddd1e-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ddd1e-126">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupAndNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddd1e-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ddd1e-127">-ResourceId</span></span>
<span data-ttu-id="ddd1e-128">Идентификатор ресурса удостоверения.</span><span class="sxs-lookup"><span data-stu-id="ddd1e-128">The Identity's resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddd1e-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ddd1e-129">-Confirm</span></span>
<span data-ttu-id="ddd1e-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ddd1e-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ddd1e-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ddd1e-131">-WhatIf</span></span>
<span data-ttu-id="ddd1e-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ddd1e-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ddd1e-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ddd1e-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ddd1e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddd1e-134">CommonParameters</span></span>
<span data-ttu-id="ddd1e-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ddd1e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddd1e-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ddd1e-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddd1e-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ddd1e-137">INPUTS</span></span>

### <span data-ttu-id="ddd1e-138">Microsoft. Azure. Commands. ManagedServiceIdentity. Models. PsUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="ddd1e-138">Microsoft.Azure.Commands.ManagedServiceIdentity.Models.PsUserAssignedIdentity</span></span>

### <span data-ttu-id="ddd1e-139">System. String</span><span class="sxs-lookup"><span data-stu-id="ddd1e-139">System.String</span></span>

## <span data-ttu-id="ddd1e-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ddd1e-140">OUTPUTS</span></span>

### <span data-ttu-id="ddd1e-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ddd1e-141">System.Boolean</span></span>

## <span data-ttu-id="ddd1e-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="ddd1e-142">NOTES</span></span>

## <span data-ttu-id="ddd1e-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ddd1e-143">RELATED LINKS</span></span>

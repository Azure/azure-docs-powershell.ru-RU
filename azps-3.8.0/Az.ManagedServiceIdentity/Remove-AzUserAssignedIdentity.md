---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServiceIdentity.dll-Help.xml
Module Name: Az.ManagedServiceIdentity
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedserviceidentity/remove-azuserassignedidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServiceIdentity/ManagedServiceIdentity/help/Remove-AzUserAssignedIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServiceIdentity/ManagedServiceIdentity/help/Remove-AzUserAssignedIdentity.md
ms.openlocfilehash: 4e133ef82e61d34e4e2915a37cc3f0e0d1e61382
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074204"
---
# <span data-ttu-id="7b49a-101">Remove-AzUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="7b49a-101">Remove-AzUserAssignedIdentity</span></span>

## <span data-ttu-id="7b49a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7b49a-102">SYNOPSIS</span></span>
<span data-ttu-id="7b49a-103">Удаляет пользователя, которому назначено удостоверение.</span><span class="sxs-lookup"><span data-stu-id="7b49a-103">Removes a User Assigned Identity.</span></span>

## <span data-ttu-id="7b49a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7b49a-104">SYNTAX</span></span>

### <span data-ttu-id="7b49a-105">ResourceGroupAndNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7b49a-105">ResourceGroupAndNameParameterSet (Default)</span></span>
```
Remove-AzUserAssignedIdentity [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b49a-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7b49a-106">InputObjectParameterSet</span></span>
```
Remove-AzUserAssignedIdentity -InputObject <PsUserAssignedIdentity> [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b49a-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7b49a-107">ResourceIdParameterSet</span></span>
```
Remove-AzUserAssignedIdentity -ResourceId <String> [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7b49a-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7b49a-108">DESCRIPTION</span></span>
<span data-ttu-id="7b49a-109">Средство **Remove-AzUserAssignedIdentity** Удаляет указанного пользователя, которому назначено удостоверение.</span><span class="sxs-lookup"><span data-stu-id="7b49a-109">The **Remove-AzUserAssignedIdentity** deletes the specified User Assigned Identity.</span></span>

## <span data-ttu-id="7b49a-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7b49a-110">EXAMPLES</span></span>

### <span data-ttu-id="7b49a-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7b49a-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzUserAssignedIdentity -ResourceGroupName PSRG -Name ID1
```

<span data-ttu-id="7b49a-112">В этом примере командлет удаляет удостоверение **id1** в разделе "Группа ресурсов" **PSRG**.</span><span class="sxs-lookup"><span data-stu-id="7b49a-112">This example cmdlet deletes the identity **ID1** under resource group **PSRG**.</span></span>
<span data-ttu-id="7b49a-113">Задан</span><span class="sxs-lookup"><span data-stu-id="7b49a-113">True</span></span>

## <span data-ttu-id="7b49a-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7b49a-114">PARAMETERS</span></span>

### <span data-ttu-id="7b49a-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7b49a-115">-AsJob</span></span>
<span data-ttu-id="7b49a-116">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="7b49a-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7b49a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b49a-117">-DefaultProfile</span></span>
<span data-ttu-id="7b49a-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7b49a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7b49a-119">-Force</span><span class="sxs-lookup"><span data-stu-id="7b49a-119">-Force</span></span>
<span data-ttu-id="7b49a-120">{Определение принудительной заливки}}</span><span class="sxs-lookup"><span data-stu-id="7b49a-120">{{Fill Force Description}}</span></span>

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

### <span data-ttu-id="7b49a-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7b49a-121">-InputObject</span></span>
<span data-ttu-id="7b49a-122">Объект Identity.</span><span class="sxs-lookup"><span data-stu-id="7b49a-122">The Identity object.</span></span>

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

### <span data-ttu-id="7b49a-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7b49a-123">-Name</span></span>
<span data-ttu-id="7b49a-124">Имя удостоверения.</span><span class="sxs-lookup"><span data-stu-id="7b49a-124">The Identity name.</span></span>

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

### <span data-ttu-id="7b49a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b49a-125">-ResourceGroupName</span></span>
<span data-ttu-id="7b49a-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7b49a-126">The resource group name.</span></span>

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

### <span data-ttu-id="7b49a-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7b49a-127">-ResourceId</span></span>
<span data-ttu-id="7b49a-128">Идентификатор ресурса удостоверения.</span><span class="sxs-lookup"><span data-stu-id="7b49a-128">The Identity's resource id.</span></span>

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

### <span data-ttu-id="7b49a-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7b49a-129">-Confirm</span></span>
<span data-ttu-id="7b49a-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7b49a-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b49a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b49a-131">-WhatIf</span></span>
<span data-ttu-id="7b49a-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7b49a-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7b49a-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7b49a-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b49a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b49a-134">CommonParameters</span></span>
<span data-ttu-id="7b49a-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7b49a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b49a-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b49a-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b49a-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7b49a-137">INPUTS</span></span>

### <span data-ttu-id="7b49a-138">Microsoft. Azure. Commands. ManagedServiceIdentity. Models. PsUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="7b49a-138">Microsoft.Azure.Commands.ManagedServiceIdentity.Models.PsUserAssignedIdentity</span></span>

### <span data-ttu-id="7b49a-139">System. String</span><span class="sxs-lookup"><span data-stu-id="7b49a-139">System.String</span></span>

## <span data-ttu-id="7b49a-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7b49a-140">OUTPUTS</span></span>

### <span data-ttu-id="7b49a-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7b49a-141">System.Boolean</span></span>

## <span data-ttu-id="7b49a-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="7b49a-142">NOTES</span></span>

## <span data-ttu-id="7b49a-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7b49a-143">RELATED LINKS</span></span>

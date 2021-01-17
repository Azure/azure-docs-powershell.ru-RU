---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServiceIdentity.dll-Help.xml
Module Name: Az.ManagedServiceIdentity
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedserviceidentity/remove-azuserassignedidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServiceIdentity/ManagedServiceIdentity/help/Remove-AzUserAssignedIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServiceIdentity/ManagedServiceIdentity/help/Remove-AzUserAssignedIdentity.md
ms.openlocfilehash: 4e133ef82e61d34e4e2915a37cc3f0e0d1e61382
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98415495"
---
# <span data-ttu-id="c46f5-101">Remove-AzUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="c46f5-101">Remove-AzUserAssignedIdentity</span></span>

## <span data-ttu-id="c46f5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c46f5-102">SYNOPSIS</span></span>
<span data-ttu-id="c46f5-103">Удаляет назначенное пользователю удостоверение.</span><span class="sxs-lookup"><span data-stu-id="c46f5-103">Removes a User Assigned Identity.</span></span>

## <span data-ttu-id="c46f5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c46f5-104">SYNTAX</span></span>

### <span data-ttu-id="c46f5-105">ResourceGroupAndNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c46f5-105">ResourceGroupAndNameParameterSet (Default)</span></span>
```
Remove-AzUserAssignedIdentity [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c46f5-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c46f5-106">InputObjectParameterSet</span></span>
```
Remove-AzUserAssignedIdentity -InputObject <PsUserAssignedIdentity> [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c46f5-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c46f5-107">ResourceIdParameterSet</span></span>
```
Remove-AzUserAssignedIdentity -ResourceId <String> [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c46f5-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c46f5-108">DESCRIPTION</span></span>
<span data-ttu-id="c46f5-109">Объект **Remove-AzUserAssignedIdentity** удаляет указанное удостоверение, назначенное пользователю.</span><span class="sxs-lookup"><span data-stu-id="c46f5-109">The **Remove-AzUserAssignedIdentity** deletes the specified User Assigned Identity.</span></span>

## <span data-ttu-id="c46f5-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c46f5-110">EXAMPLES</span></span>

### <span data-ttu-id="c46f5-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c46f5-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzUserAssignedIdentity -ResourceGroupName PSRG -Name ID1
```

<span data-ttu-id="c46f5-112">В этом примере cmdlet удаляет идентификатор **идентификатора 1** в группе **ресурсов PSRG.**</span><span class="sxs-lookup"><span data-stu-id="c46f5-112">This example cmdlet deletes the identity **ID1** under resource group **PSRG**.</span></span>
<span data-ttu-id="c46f5-113">True</span><span class="sxs-lookup"><span data-stu-id="c46f5-113">True</span></span>

## <span data-ttu-id="c46f5-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c46f5-114">PARAMETERS</span></span>

### <span data-ttu-id="c46f5-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c46f5-115">-AsJob</span></span>
<span data-ttu-id="c46f5-116">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="c46f5-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c46f5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c46f5-117">-DefaultProfile</span></span>
<span data-ttu-id="c46f5-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c46f5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c46f5-119">-Force</span><span class="sxs-lookup"><span data-stu-id="c46f5-119">-Force</span></span>
<span data-ttu-id="c46f5-120">{{Fill Force Description}}</span><span class="sxs-lookup"><span data-stu-id="c46f5-120">{{Fill Force Description}}</span></span>

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

### <span data-ttu-id="c46f5-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c46f5-121">-InputObject</span></span>
<span data-ttu-id="c46f5-122">Объект Identity.</span><span class="sxs-lookup"><span data-stu-id="c46f5-122">The Identity object.</span></span>

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

### <span data-ttu-id="c46f5-123">-Name</span><span class="sxs-lookup"><span data-stu-id="c46f5-123">-Name</span></span>
<span data-ttu-id="c46f5-124">Имя удостоверения.</span><span class="sxs-lookup"><span data-stu-id="c46f5-124">The Identity name.</span></span>

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

### <span data-ttu-id="c46f5-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c46f5-125">-ResourceGroupName</span></span>
<span data-ttu-id="c46f5-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c46f5-126">The resource group name.</span></span>

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

### <span data-ttu-id="c46f5-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c46f5-127">-ResourceId</span></span>
<span data-ttu-id="c46f5-128">Идентификатор ресурса удостоверения.</span><span class="sxs-lookup"><span data-stu-id="c46f5-128">The Identity's resource id.</span></span>

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

### <span data-ttu-id="c46f5-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c46f5-129">-Confirm</span></span>
<span data-ttu-id="c46f5-130">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="c46f5-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c46f5-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c46f5-131">-WhatIf</span></span>
<span data-ttu-id="c46f5-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c46f5-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c46f5-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="c46f5-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c46f5-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c46f5-134">CommonParameters</span></span>
<span data-ttu-id="c46f5-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c46f5-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c46f5-136">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c46f5-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c46f5-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c46f5-137">INPUTS</span></span>

### <span data-ttu-id="c46f5-138">Microsoft.Azure.Commands.ManagedServiceIdentity.Models.PsUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="c46f5-138">Microsoft.Azure.Commands.ManagedServiceIdentity.Models.PsUserAssignedIdentity</span></span>

### <span data-ttu-id="c46f5-139">System.String</span><span class="sxs-lookup"><span data-stu-id="c46f5-139">System.String</span></span>

## <span data-ttu-id="c46f5-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c46f5-140">OUTPUTS</span></span>

### <span data-ttu-id="c46f5-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c46f5-141">System.Boolean</span></span>

## <span data-ttu-id="c46f5-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c46f5-142">NOTES</span></span>

## <span data-ttu-id="c46f5-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c46f5-143">RELATED LINKS</span></span>

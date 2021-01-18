---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServiceIdentity.dll-Help.xml
Module Name: Az.ManagedServiceIdentity
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedserviceidentity/new-azuserassignedidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServiceIdentity/ManagedServiceIdentity/help/New-AzUserAssignedIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServiceIdentity/ManagedServiceIdentity/help/New-AzUserAssignedIdentity.md
ms.openlocfilehash: 1f165177871a2d8b425829dddaef6d1f0298cfb4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98508226"
---
# <span data-ttu-id="4a424-101">New-AzUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="4a424-101">New-AzUserAssignedIdentity</span></span>

## <span data-ttu-id="4a424-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a424-102">SYNOPSIS</span></span>
<span data-ttu-id="4a424-103">Создает новое удостоверение, назначенное пользователю, или обновляет существующее удостоверение.</span><span class="sxs-lookup"><span data-stu-id="4a424-103">Creates a new User Assigned Identity or updates an existing User Assigned Identity.</span></span>

## <span data-ttu-id="4a424-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4a424-104">SYNTAX</span></span>

```
New-AzUserAssignedIdentity [-ResourceGroupName] <String> [-Name] <String> [-Location <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-Tag <Hashtable>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4a424-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4a424-105">DESCRIPTION</span></span>
<span data-ttu-id="4a424-106">Для **создания нового идентификатора User AssignedIdentity new-AzUserAssignedIdentity** будет создаваться новое удостоверение, назначенное пользователю.</span><span class="sxs-lookup"><span data-stu-id="4a424-106">The **New-AzUserAssignedIdentity** cmdlet creates a new User Assigned Identity.</span></span> <span data-ttu-id="4a424-107">При его использования с уже существующим удостоверением оно обновлялось.</span><span class="sxs-lookup"><span data-stu-id="4a424-107">When used with an already existing identity, it updated the identity.</span></span>
<span data-ttu-id="4a424-108">Чтобы добавить теги Диспетчера ресурсов Azure в удостоверение, воспользуйтесь Set-AzResource командлетом.</span><span class="sxs-lookup"><span data-stu-id="4a424-108">To add Azure Resource Manager tags to the identity, please use the Set-AzResource cmdlet.</span></span>

## <span data-ttu-id="4a424-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4a424-109">EXAMPLES</span></span>

### <span data-ttu-id="4a424-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4a424-110">Example 1</span></span>
<span data-ttu-id="4a424-111">В этом примере создается новое назначенное пользователем удостоверение с именем **ID1** в группе **ресурсов PSRG** в расположении группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4a424-111">This example cmdlet creates a new User Assigned Identity with name **ID1** under resource group **PSRG** in the location of the ResourceGroup.</span></span>

```powershell
PS C:\> New-AzUserAssignedIdentity -ResourceGroupName PSRG -Name ID1

Id                : /subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID1

ResourceGroupName : PSRG

Name              : ID1

Location          : centralus

TenantId          : 493b860d-2741-480b-8b34-7b1d76e33c50

PrincipalId       : e34192f9-7831-4a02-bfe2-4c6d2fb4360d

ClientId          : a5e650a2-fdfe-4652-bb3b-109b64617cfd

ClientSecretUrl   : https://control-westus.identity.azure.net/subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG1/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID1/credentials?tid=493b860d-2741-480b-8b34-7b1d76e33c50&oid=e34192f9-7831-4a02-bfe2-4c6d2fb4360d&aid=a5e650a2-fdfe-4652-bb3b-109b64617cfd

Type              : Microsoft.ManagedIdentity/userAssignedIdentities
```

### <span data-ttu-id="4a424-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="4a424-112">Example 2</span></span>
<span data-ttu-id="4a424-113">В этом примере создается новое назначенное удостоверение пользователя с **ИД1** в группе **ресурсов PSRG** в западной части региона.</span><span class="sxs-lookup"><span data-stu-id="4a424-113">This example cmdlet creates a new User Assigned Identity with name **ID1** under the resource group **PSRG** in the westus region.</span></span>

```powershell
PS C:\> New-AzUserAssignedIdentity -ResourceGroupName PSRG -Name ID1 -Location westus

Id                : /subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID1

ResourceGroupName : PSRG

Name              : ID1

Location          : westus

TenantId          : 493b860d-2741-480b-8b34-7b1d76e33c50

PrincipalId       : e34192f9-7831-4a02-bfe2-4c6d2fb4360d

ClientId          : a5e650a2-fdfe-4652-bb3b-109b64617cfd

ClientSecretUrl   : https://control-westus.identity.azure.net/subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID1/credentials?tid=493b860d-2741-480b-8b34-7b1d76e33c50&oid=e34192f9-7831-4a02-bfe2-4c6d2fb4360d&aid=a5e650a2-fdfe-4652-bb3b-109b64617cfd

Type              : Microsoft.ManagedIdentity/userAssignedIdentities
```

## <span data-ttu-id="4a424-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4a424-114">PARAMETERS</span></span>

### <span data-ttu-id="4a424-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4a424-115">-AsJob</span></span>
<span data-ttu-id="4a424-116">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="4a424-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4a424-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a424-117">-DefaultProfile</span></span>
<span data-ttu-id="4a424-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4a424-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a424-119">-Location</span><span class="sxs-lookup"><span data-stu-id="4a424-119">-Location</span></span>
<span data-ttu-id="4a424-120">Имя региона Azure, в котором нужно создать удостоверение.</span><span class="sxs-lookup"><span data-stu-id="4a424-120">The Azure region name where the Identity should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a424-121">-Name</span><span class="sxs-lookup"><span data-stu-id="4a424-121">-Name</span></span>
<span data-ttu-id="4a424-122">Имя удостоверения.</span><span class="sxs-lookup"><span data-stu-id="4a424-122">The Identity name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a424-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a424-123">-ResourceGroupName</span></span>
<span data-ttu-id="4a424-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4a424-124">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a424-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="4a424-125">-Tag</span></span>
<span data-ttu-id="4a424-126">Теги Диспетчера ресурсов Azure, связанные с удостоверением.</span><span class="sxs-lookup"><span data-stu-id="4a424-126">The Azure Resource Manager tags associated with the identity.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a424-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4a424-127">-Confirm</span></span>
<span data-ttu-id="4a424-128">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="4a424-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a424-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a424-129">-WhatIf</span></span>
<span data-ttu-id="4a424-130">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4a424-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4a424-131">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="4a424-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a424-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a424-132">CommonParameters</span></span>
<span data-ttu-id="4a424-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a424-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a424-134">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a424-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a424-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4a424-135">INPUTS</span></span>

### <span data-ttu-id="4a424-136">System.String</span><span class="sxs-lookup"><span data-stu-id="4a424-136">System.String</span></span>

### <span data-ttu-id="4a424-137">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="4a424-137">System.Collections.Hashtable</span></span>

## <span data-ttu-id="4a424-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4a424-138">OUTPUTS</span></span>

### <span data-ttu-id="4a424-139">Microsoft.Azure.Commands.ManagedServiceIdentity.Models.PsUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="4a424-139">Microsoft.Azure.Commands.ManagedServiceIdentity.Models.PsUserAssignedIdentity</span></span>

## <span data-ttu-id="4a424-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4a424-140">NOTES</span></span>

## <span data-ttu-id="4a424-141">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4a424-141">RELATED LINKS</span></span>

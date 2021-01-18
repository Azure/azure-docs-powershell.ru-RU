---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServiceIdentity.dll-Help.xml
Module Name: Az.ManagedServiceIdentity
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedserviceidentity/get-azuserassignedidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServiceIdentity/ManagedServiceIdentity/help/Get-AzUserAssignedIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServiceIdentity/ManagedServiceIdentity/help/Get-AzUserAssignedIdentity.md
ms.openlocfilehash: 293c7c54147c254f7cf2f34ffdb2ffbe1f865b09
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506253"
---
# <span data-ttu-id="b1658-101">Get-AzUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="b1658-101">Get-AzUserAssignedIdentity</span></span>

## <span data-ttu-id="b1658-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1658-102">SYNOPSIS</span></span>
<span data-ttu-id="b1658-103">Возвращает идентификаторы и удостоверения, которые назначены пользователям.</span><span class="sxs-lookup"><span data-stu-id="b1658-103">Gets User Assigned Identity/identities.</span></span>

## <span data-ttu-id="b1658-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b1658-104">SYNTAX</span></span>

### <span data-ttu-id="b1658-105">SuscriptionParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b1658-105">SuscriptionParameterSet (Default)</span></span>
```
Get-AzUserAssignedIdentity [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b1658-106">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1658-106">ResourceGroupParameterSet</span></span>
```
Get-AzUserAssignedIdentity -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b1658-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b1658-107">DESCRIPTION</span></span>
<span data-ttu-id="b1658-108">Сущность **Get-AzUserAssignedIdentity** получает существующие удостоверения, которые назначены пользователям.</span><span class="sxs-lookup"><span data-stu-id="b1658-108">The **Get-AzUserAssignedIdentity** gets existing user assigned identities.</span></span>

## <span data-ttu-id="b1658-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b1658-109">EXAMPLES</span></span>

### <span data-ttu-id="b1658-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b1658-110">Example 1</span></span>
<span data-ttu-id="b1658-111">В этом примере для группы ресурсов **PSRG** возвращается назначенное пользователю удостоверение с именем **ID1.**</span><span class="sxs-lookup"><span data-stu-id="b1658-111">This example cmdlet gets the User Assigned Identity with name **ID1** under the resource group **PSRG**</span></span>

```powershell
PS C:\> Get-AzUserAssignedIdentity -ResourceGroupName PSRG -Name ID1

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

### <span data-ttu-id="b1658-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="b1658-112">Example 2</span></span>
<span data-ttu-id="b1658-113">В этом примере в группе ресурсов PSRG находятся все удостоверения пользователей, которые назначены **пользователям.**</span><span class="sxs-lookup"><span data-stu-id="b1658-113">This example cmdlet gets all the User Assigned Identities under the resource group **PSRG**</span></span>

```powershell
PS C:\> Get-AzUserAssignedIdentity -ResourceGroupName PSRG

Id                : /subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID1

ResourceGroupName : PSRG

Name              : ID1

Location          : westus

TenantId          : 493b860d-2741-480b-8b34-7b1d76e33c50

PrincipalId       : e34192f9-7831-4a02-bfe2-4c6d2fb4360d

ClientId          : a5e650a2-fdfe-4652-bb3b-109b64617cfd

ClientSecretUrl   : https://control-westus.identity.azure.net/subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID1/credentials?tid=493b860d-2741-480b-8b34-7b1d76e33c50&oid=e34192f9-7831-4a02-bfe2-4c6d2fb4360d&aid=a5e650a2-fdfe-4652-bb3b-109b64617cfd

Type              : Microsoft.ManagedIdentity/userAssignedIdentities


Id                : /subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID2

ResourceGroupName : PSRG

Name              : ID2

Location          : westus

TenantId          : 493b860d-2741-480b-8b34-7b1d76e33c50

PrincipalId       : e34192f9-7831-4a02-bfe2-4c6d2fb4360d

ClientId          : a5e650a2-fdfe-4652-bb3b-109b64617cfd

ClientSecretUrl   : https://control-westus.identity.azure.net/subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID2/credentials?tid=493b860d-2741-480b-8b34-7b1d76e33c50&oid=e34192f9-7831-4a02-bfe2-4c6d2fb4360d&aid=a5e650a2-fdfe-4652-bb3b-109b64617cfd

Type              : Microsoft.ManagedIdentity/userAssignedIdentities
```

### <span data-ttu-id="b1658-114">Пример 3</span><span class="sxs-lookup"><span data-stu-id="b1658-114">Example 3</span></span>
<span data-ttu-id="b1658-115">В этом примере с его учетными данными в рамках подписки получаются все удостоверения пользователей, которые назначены пользователям.</span><span class="sxs-lookup"><span data-stu-id="b1658-115">This example cmdlet gets all the User Assigned Identities under the subscription.</span></span>

```powershell
PS C:\> Get-AzUserAssignedIdentity

Id                : /subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID1

ResourceGroupName : PSRG

Name              : ID1

Location          : westus

TenantId          : 493b860d-2741-480b-8b34-7b1d76e33c50

PrincipalId       : e34192f9-7831-4a02-bfe2-4c6d2fb4360d

ClientId          : a5e650a2-fdfe-4652-bb3b-109b64617cfd

ClientSecretUrl   : https://control-westus.identity.azure.net/subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID1/credentials?tid=493b860d-2741-480b-8b34-7b1d76e33c50&oid=e34192f9-7831-4a02-bfe2-4c6d2fb4360d&aid=a5e650a2-fdfe-4652-bb3b-109b64617cfd

Type              : Microsoft.ManagedIdentity/userAssignedIdentities


Id                : /subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID2

ResourceGroupName : PSRG

Name              : ID2

Location          : westus

TenantId          : 493b860d-2741-480b-8b34-7b1d76e33c50

PrincipalId       : e34192f9-7831-4a02-bfe2-4c6d2fb4360d

ClientId          : a5e650a2-fdfe-4652-bb3b-109b64617cfd

ClientSecretUrl   : https://control-westus.identity.azure.net/subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID2/credentials?tid=493b860d-2741-480b-8b34-7b1d76e33c50&oid=e34192f9-7831-4a02-bfe2-4c6d2fb4360d&aid=a5e650a2-fdfe-4652-bb3b-109b64617cfd

Type              : Microsoft.ManagedIdentity/userAssignedIdentities


Id                : /subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG2/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID1

ResourceGroupName : PSRG2

Name              : ID1

Location          : westus

TenantId          : 493b860d-2741-480b-8b34-7b1d76e33c50

PrincipalId       : e34192f9-7831-4a02-bfe2-4c6d2fb4360d

ClientId          : a5e650a2-fdfe-4652-bb3b-109b64617cfd

ClientSecretUrl   : https://control-westus.identity.azure.net/subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG2/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID1/credentials?tid=493b860d-2741-480b-8b34-7b1d76e33c50&oid=e34192f9-7831-4a02-bfe2-4c6d2fb4360d&aid=a5e650a2-fdfe-4652-bb3b-109b64617cfd

Type              : Microsoft.ManagedIdentity/userAssignedIdentities
```

## <span data-ttu-id="b1658-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b1658-116">PARAMETERS</span></span>

### <span data-ttu-id="b1658-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1658-117">-DefaultProfile</span></span>
<span data-ttu-id="b1658-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b1658-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1658-119">-Name</span><span class="sxs-lookup"><span data-stu-id="b1658-119">-Name</span></span>
<span data-ttu-id="b1658-120">Имя удостоверения.</span><span class="sxs-lookup"><span data-stu-id="b1658-120">The Identity name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1658-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1658-121">-ResourceGroupName</span></span>
<span data-ttu-id="b1658-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b1658-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1658-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1658-123">CommonParameters</span></span>
<span data-ttu-id="b1658-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1658-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1658-125">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1658-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1658-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b1658-126">INPUTS</span></span>

### <span data-ttu-id="b1658-127">System.String</span><span class="sxs-lookup"><span data-stu-id="b1658-127">System.String</span></span>

## <span data-ttu-id="b1658-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b1658-128">OUTPUTS</span></span>

### <span data-ttu-id="b1658-129">Microsoft.Azure.Commands.ManagedServiceIdentity.Models.PsUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="b1658-129">Microsoft.Azure.Commands.ManagedServiceIdentity.Models.PsUserAssignedIdentity</span></span>

## <span data-ttu-id="b1658-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b1658-130">NOTES</span></span>

## <span data-ttu-id="b1658-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b1658-131">RELATED LINKS</span></span>

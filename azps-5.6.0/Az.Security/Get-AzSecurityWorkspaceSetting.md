---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzSecurityWorkspaceSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityWorkspaceSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityWorkspaceSetting.md
ms.openlocfilehash: f0de174ac85fb4247ac8af55f8a8ab9cb64d6446
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973507"
---
# <span data-ttu-id="cd827-101">Get-AzSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="cd827-101">Get-AzSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="cd827-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd827-102">SYNOPSIS</span></span>
<span data-ttu-id="cd827-103">Настраивает параметры рабочей области безопасности для подписки.</span><span class="sxs-lookup"><span data-stu-id="cd827-103">Gets the configured security workspace settings on a subscription.</span></span>

## <span data-ttu-id="cd827-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="cd827-104">SYNTAX</span></span>

### <span data-ttu-id="cd827-105">SubscriptionScope (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cd827-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityWorkspaceSetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd827-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="cd827-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityWorkspaceSetting -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd827-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="cd827-107">ResourceId</span></span>
```
Get-AzSecurityWorkspaceSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cd827-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cd827-108">DESCRIPTION</span></span>
<span data-ttu-id="cd827-109">Этот cmdlet позволяет найти настроенную рабочее пространство, в которое будут вмещаться данные безопасности, собранные агентом безопасности, установленным в VMs в этой подписке.</span><span class="sxs-lookup"><span data-stu-id="cd827-109">This cmdlet lets you discover the configured workspace that will hold the security data that was collected by the security agent that is installed in VMs inside this subscription.</span></span>

## <span data-ttu-id="cd827-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="cd827-110">EXAMPLES</span></span>

### <span data-ttu-id="cd827-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="cd827-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityWorkspaceSetting

Id                                                                                                         Name    WorkspaceId                                                                                                                               
--                                                                                                         ----    -----------                                                                                                                               
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/workspaceSettings/default default /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/mainws/providers/microsoft.operationalinsights/workspaces/securityus...
```

<span data-ttu-id="cd827-112">Получает параметры рабочей области для подписки.</span><span class="sxs-lookup"><span data-stu-id="cd827-112">Gets the workspace settings for a subscription.</span></span>

## <span data-ttu-id="cd827-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cd827-113">PARAMETERS</span></span>

### <span data-ttu-id="cd827-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd827-114">-DefaultProfile</span></span>
<span data-ttu-id="cd827-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cd827-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd827-116">-Name</span><span class="sxs-lookup"><span data-stu-id="cd827-116">-Name</span></span>
<span data-ttu-id="cd827-117">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="cd827-117">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd827-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cd827-118">-ResourceId</span></span>
<span data-ttu-id="cd827-119">ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="cd827-119">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd827-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd827-120">CommonParameters</span></span>
<span data-ttu-id="cd827-121">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd827-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd827-122">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cd827-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd827-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cd827-123">INPUTS</span></span>

### <span data-ttu-id="cd827-124">System.String</span><span class="sxs-lookup"><span data-stu-id="cd827-124">System.String</span></span>

## <span data-ttu-id="cd827-125">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="cd827-125">OUTPUTS</span></span>

### <span data-ttu-id="cd827-126">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="cd827-126">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="cd827-127">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="cd827-127">NOTES</span></span>

## <span data-ttu-id="cd827-128">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cd827-128">RELATED LINKS</span></span>

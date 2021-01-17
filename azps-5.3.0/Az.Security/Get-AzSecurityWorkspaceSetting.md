---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityWorkspaceSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityWorkspaceSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityWorkspaceSetting.md
ms.openlocfilehash: ca4f0d39b0023d641e2f95ceb4eddf90f19a51f1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98420932"
---
# <span data-ttu-id="1a262-101">Get-AzSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="1a262-101">Get-AzSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="1a262-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a262-102">SYNOPSIS</span></span>
<span data-ttu-id="1a262-103">Настраивает параметры рабочей области безопасности для подписки.</span><span class="sxs-lookup"><span data-stu-id="1a262-103">Gets the configured security workspace settings on a subscription.</span></span>

## <span data-ttu-id="1a262-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1a262-104">SYNTAX</span></span>

### <span data-ttu-id="1a262-105">SubscriptionScope (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1a262-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityWorkspaceSetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1a262-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="1a262-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityWorkspaceSetting -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1a262-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="1a262-107">ResourceId</span></span>
```
Get-AzSecurityWorkspaceSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1a262-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1a262-108">DESCRIPTION</span></span>
<span data-ttu-id="1a262-109">Этот cmdlet позволяет найти настроенную область, в которую будут вмещаться данные безопасности, собранные агентом безопасности, установленным в VMs в этой подписке.</span><span class="sxs-lookup"><span data-stu-id="1a262-109">This cmdlet lets you discover the configured workspace that will hold the security data that was collected by the security agent that is installed in VMs inside this subscription.</span></span>

## <span data-ttu-id="1a262-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1a262-110">EXAMPLES</span></span>

### <span data-ttu-id="1a262-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1a262-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityWorkspaceSetting

Id                                                                                                         Name    WorkspaceId                                                                                                                               
--                                                                                                         ----    -----------                                                                                                                               
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/workspaceSettings/default default /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/mainws/providers/microsoft.operationalinsights/workspaces/securityus...
```

<span data-ttu-id="1a262-112">Получает параметры рабочей области для подписки.</span><span class="sxs-lookup"><span data-stu-id="1a262-112">Gets the workspace settings for a subscription.</span></span>

## <span data-ttu-id="1a262-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1a262-113">PARAMETERS</span></span>

### <span data-ttu-id="1a262-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a262-114">-DefaultProfile</span></span>
<span data-ttu-id="1a262-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1a262-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a262-116">-Name</span><span class="sxs-lookup"><span data-stu-id="1a262-116">-Name</span></span>
<span data-ttu-id="1a262-117">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="1a262-117">Resource name.</span></span>

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

### <span data-ttu-id="1a262-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1a262-118">-ResourceId</span></span>
<span data-ttu-id="1a262-119">ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="1a262-119">Resource ID.</span></span>

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

### <span data-ttu-id="1a262-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a262-120">CommonParameters</span></span>
<span data-ttu-id="1a262-121">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a262-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a262-122">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1a262-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a262-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1a262-123">INPUTS</span></span>

### <span data-ttu-id="1a262-124">System.String</span><span class="sxs-lookup"><span data-stu-id="1a262-124">System.String</span></span>

## <span data-ttu-id="1a262-125">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1a262-125">OUTPUTS</span></span>

### <span data-ttu-id="1a262-126">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="1a262-126">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="1a262-127">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1a262-127">NOTES</span></span>

## <span data-ttu-id="1a262-128">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1a262-128">RELATED LINKS</span></span>

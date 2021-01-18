---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityWorkspaceSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityWorkspaceSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityWorkspaceSetting.md
ms.openlocfilehash: 23d35a0bce62aa2a3a5c922ea0e25e35cb619b09
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98517622"
---
# <span data-ttu-id="f385e-101">Set-AzSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="f385e-101">Set-AzSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="f385e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f385e-102">SYNOPSIS</span></span>
<span data-ttu-id="f385e-103">Обновляет параметры рабочей области для подписки.</span><span class="sxs-lookup"><span data-stu-id="f385e-103">Updates the workspace settings for the subscription.</span></span>

## <span data-ttu-id="f385e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f385e-104">SYNTAX</span></span>

```
Set-AzSecurityWorkspaceSetting -Name <String> -Scope <String> -WorkspaceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f385e-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f385e-105">DESCRIPTION</span></span>
<span data-ttu-id="f385e-106">Обновляет параметры рабочей области для подписки.</span><span class="sxs-lookup"><span data-stu-id="f385e-106">Updates the workspace settings for the subscription.</span></span>
<span data-ttu-id="f385e-107">В настроенной рабочей области будут удержаны данные безопасности, собранные агентом агента аналитики журналов Azure, который установлен в VMs в этой подписке.</span><span class="sxs-lookup"><span data-stu-id="f385e-107">The configured workspace will hold the security data that was collected by the Azure Log Analytics agent agent that is installed in VMs inside this subscription.</span></span>

## <span data-ttu-id="f385e-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f385e-108">EXAMPLES</span></span>

### <span data-ttu-id="f385e-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f385e-109">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityWorkspaceSetting -Name "default" -Scope "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869" -WorkspaceId  "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/mainws/providers/microsoft.operationalinsights/workspaces/securityuserws"

Id                                                                                                         Name    WorkspaceId 
--                                                                                                         ----    ----
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/workspaceSettings/default default /...
```

<span data-ttu-id="f385e-110">Задает для рабочей области MyWorkspace все данные безопасности, собранные агентом аналитики журналов Azure.</span><span class="sxs-lookup"><span data-stu-id="f385e-110">Sets the "myWorkspace" workspace to hold all the security data that was collected by the Azure Log Analytics agent.</span></span>

## <span data-ttu-id="f385e-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f385e-111">PARAMETERS</span></span>

### <span data-ttu-id="f385e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f385e-112">-DefaultProfile</span></span>
<span data-ttu-id="f385e-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f385e-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f385e-114">-Name</span><span class="sxs-lookup"><span data-stu-id="f385e-114">-Name</span></span>
<span data-ttu-id="f385e-115">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="f385e-115">Resource name.</span></span>

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

### <span data-ttu-id="f385e-116">-Scope</span><span class="sxs-lookup"><span data-stu-id="f385e-116">-Scope</span></span>
<span data-ttu-id="f385e-117">Область.</span><span class="sxs-lookup"><span data-stu-id="f385e-117">Scope.</span></span>

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

### <span data-ttu-id="f385e-118">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="f385e-118">-WorkspaceId</span></span>
<span data-ttu-id="f385e-119">ИД рабочей области.</span><span class="sxs-lookup"><span data-stu-id="f385e-119">Workspace ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f385e-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f385e-120">-Confirm</span></span>
<span data-ttu-id="f385e-121">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="f385e-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f385e-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f385e-122">-WhatIf</span></span>
<span data-ttu-id="f385e-123">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f385e-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f385e-124">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="f385e-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f385e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f385e-125">CommonParameters</span></span>
<span data-ttu-id="f385e-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f385e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f385e-127">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f385e-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f385e-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f385e-128">INPUTS</span></span>

### <span data-ttu-id="f385e-129">System.String</span><span class="sxs-lookup"><span data-stu-id="f385e-129">System.String</span></span>

## <span data-ttu-id="f385e-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f385e-130">OUTPUTS</span></span>

### <span data-ttu-id="f385e-131">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="f385e-131">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="f385e-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f385e-132">NOTES</span></span>

## <span data-ttu-id="f385e-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f385e-133">RELATED LINKS</span></span>

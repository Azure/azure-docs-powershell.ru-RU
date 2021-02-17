---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityWorkspaceSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityWorkspaceSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityWorkspaceSetting.md
ms.openlocfilehash: a02d2685987844db5f88fafaf12d0c9aed4a3234
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100235857"
---
# <span data-ttu-id="39f68-101">Set-AzSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="39f68-101">Set-AzSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="39f68-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39f68-102">SYNOPSIS</span></span>
<span data-ttu-id="39f68-103">Обновляет параметры рабочей области для подписки.</span><span class="sxs-lookup"><span data-stu-id="39f68-103">Updates the workspace settings for the subscription.</span></span>

## <span data-ttu-id="39f68-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="39f68-104">SYNTAX</span></span>

```
Set-AzSecurityWorkspaceSetting -Name <String> -Scope <String> -WorkspaceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="39f68-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="39f68-105">DESCRIPTION</span></span>
<span data-ttu-id="39f68-106">Обновляет параметры рабочей области для подписки.</span><span class="sxs-lookup"><span data-stu-id="39f68-106">Updates the workspace settings for the subscription.</span></span>
<span data-ttu-id="39f68-107">В настроенной рабочей области будут удержаны данные безопасности, собранные агентом агента аналитики журналов Azure, который установлен в VMs в этой подписке.</span><span class="sxs-lookup"><span data-stu-id="39f68-107">The configured workspace will hold the security data that was collected by the Azure Log Analytics agent agent that is installed in VMs inside this subscription.</span></span>

## <span data-ttu-id="39f68-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="39f68-108">EXAMPLES</span></span>

### <span data-ttu-id="39f68-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="39f68-109">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityWorkspaceSetting -Name "default" -Scope "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869" -WorkspaceId  "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/mainws/providers/microsoft.operationalinsights/workspaces/securityuserws"

Id                                                                                                         Name    WorkspaceId 
--                                                                                                         ----    ----
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/workspaceSettings/default default /...
```

<span data-ttu-id="39f68-110">Задает в рабочей области securityuserws все данные безопасности, собранные агентом аналитики журналов Azure.</span><span class="sxs-lookup"><span data-stu-id="39f68-110">Sets the "securityuserws" workspace to hold all the security data that was collected by the Azure Log Analytics agent.</span></span>

## <span data-ttu-id="39f68-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="39f68-111">PARAMETERS</span></span>

### <span data-ttu-id="39f68-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39f68-112">-DefaultProfile</span></span>
<span data-ttu-id="39f68-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="39f68-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39f68-114">-Name</span><span class="sxs-lookup"><span data-stu-id="39f68-114">-Name</span></span>
<span data-ttu-id="39f68-115">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="39f68-115">Resource name.</span></span>

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

### <span data-ttu-id="39f68-116">-Scope</span><span class="sxs-lookup"><span data-stu-id="39f68-116">-Scope</span></span>
<span data-ttu-id="39f68-117">Область.</span><span class="sxs-lookup"><span data-stu-id="39f68-117">Scope.</span></span>

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

### <span data-ttu-id="39f68-118">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="39f68-118">-WorkspaceId</span></span>
<span data-ttu-id="39f68-119">ИД рабочей области.</span><span class="sxs-lookup"><span data-stu-id="39f68-119">Workspace ID.</span></span>

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

### <span data-ttu-id="39f68-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="39f68-120">-Confirm</span></span>
<span data-ttu-id="39f68-121">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="39f68-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39f68-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39f68-122">-WhatIf</span></span>
<span data-ttu-id="39f68-123">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="39f68-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="39f68-124">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="39f68-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39f68-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39f68-125">CommonParameters</span></span>
<span data-ttu-id="39f68-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39f68-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39f68-127">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="39f68-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39f68-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="39f68-128">INPUTS</span></span>

### <span data-ttu-id="39f68-129">System.String</span><span class="sxs-lookup"><span data-stu-id="39f68-129">System.String</span></span>

## <span data-ttu-id="39f68-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="39f68-130">OUTPUTS</span></span>

### <span data-ttu-id="39f68-131">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="39f68-131">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="39f68-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="39f68-132">NOTES</span></span>

## <span data-ttu-id="39f68-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="39f68-133">RELATED LINKS</span></span>

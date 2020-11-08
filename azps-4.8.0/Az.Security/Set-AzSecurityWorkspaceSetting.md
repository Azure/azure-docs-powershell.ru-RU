---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityWorkspaceSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityWorkspaceSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityWorkspaceSetting.md
ms.openlocfilehash: 23d35a0bce62aa2a3a5c922ea0e25e35cb619b09
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235345"
---
# <span data-ttu-id="ac443-101">Set-AzSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="ac443-101">Set-AzSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="ac443-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ac443-102">SYNOPSIS</span></span>
<span data-ttu-id="ac443-103">Обновляет параметры рабочей области для подписки.</span><span class="sxs-lookup"><span data-stu-id="ac443-103">Updates the workspace settings for the subscription.</span></span>

## <span data-ttu-id="ac443-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ac443-104">SYNTAX</span></span>

```
Set-AzSecurityWorkspaceSetting -Name <String> -Scope <String> -WorkspaceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ac443-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ac443-105">DESCRIPTION</span></span>
<span data-ttu-id="ac443-106">Обновляет параметры рабочей области для подписки.</span><span class="sxs-lookup"><span data-stu-id="ac443-106">Updates the workspace settings for the subscription.</span></span>
<span data-ttu-id="ac443-107">Настроенная рабочая область будет хранить данные безопасности, собранные агентом агента службы аналитики журналов Azure, который установлен в виртуальных машинах в этой подписке.</span><span class="sxs-lookup"><span data-stu-id="ac443-107">The configured workspace will hold the security data that was collected by the Azure Log Analytics agent agent that is installed in VMs inside this subscription.</span></span>

## <span data-ttu-id="ac443-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ac443-108">EXAMPLES</span></span>

### <span data-ttu-id="ac443-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ac443-109">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityWorkspaceSetting -Name "default" -Scope "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869" -WorkspaceId  "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/mainws/providers/microsoft.operationalinsights/workspaces/securityuserws"

Id                                                                                                         Name    WorkspaceId 
--                                                                                                         ----    ----
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/workspaceSettings/default default /...
```

<span data-ttu-id="ac443-110">Задает рабочую область "myWorkspace", в которой хранятся все данные безопасности, собранные агентом аналитики журналов Azure.</span><span class="sxs-lookup"><span data-stu-id="ac443-110">Sets the "myWorkspace" workspace to hold all the security data that was collected by the Azure Log Analytics agent.</span></span>

## <span data-ttu-id="ac443-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ac443-111">PARAMETERS</span></span>

### <span data-ttu-id="ac443-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac443-112">-DefaultProfile</span></span>
<span data-ttu-id="ac443-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ac443-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac443-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ac443-114">-Name</span></span>
<span data-ttu-id="ac443-115">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="ac443-115">Resource name.</span></span>

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

### <span data-ttu-id="ac443-116">-Scope</span><span class="sxs-lookup"><span data-stu-id="ac443-116">-Scope</span></span>
<span data-ttu-id="ac443-117">Област.</span><span class="sxs-lookup"><span data-stu-id="ac443-117">Scope.</span></span>

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

### <span data-ttu-id="ac443-118">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="ac443-118">-WorkspaceId</span></span>
<span data-ttu-id="ac443-119">ИДЕНТИФИКАТОР рабочей области.</span><span class="sxs-lookup"><span data-stu-id="ac443-119">Workspace ID.</span></span>

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

### <span data-ttu-id="ac443-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ac443-120">-Confirm</span></span>
<span data-ttu-id="ac443-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ac443-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac443-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac443-122">-WhatIf</span></span>
<span data-ttu-id="ac443-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ac443-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ac443-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ac443-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac443-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac443-125">CommonParameters</span></span>
<span data-ttu-id="ac443-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ac443-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac443-127">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ac443-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac443-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ac443-128">INPUTS</span></span>

### <span data-ttu-id="ac443-129">System. String</span><span class="sxs-lookup"><span data-stu-id="ac443-129">System.String</span></span>

## <span data-ttu-id="ac443-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ac443-130">OUTPUTS</span></span>

### <span data-ttu-id="ac443-131">Microsoft. Azure. Commands. Security. Models. WorkspaceSettings. PSSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="ac443-131">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="ac443-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="ac443-132">NOTES</span></span>

## <span data-ttu-id="ac443-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ac443-133">RELATED LINKS</span></span>

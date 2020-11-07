---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityWorkspaceSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityWorkspaceSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityWorkspaceSetting.md
ms.openlocfilehash: 679b1458b3e749b2ccfca3863f745edd562ffc2f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729221"
---
# <span data-ttu-id="04f6d-101">Set-AzSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="04f6d-101">Set-AzSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="04f6d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="04f6d-102">SYNOPSIS</span></span>
<span data-ttu-id="04f6d-103">Обновляет параметры рабочей области для подписки.</span><span class="sxs-lookup"><span data-stu-id="04f6d-103">Updates the workspace settings for the subscription.</span></span>

## <span data-ttu-id="04f6d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="04f6d-104">SYNTAX</span></span>

```
Set-AzSecurityWorkspaceSetting -Name <String> -Scope <String> -WorkspaceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04f6d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="04f6d-105">DESCRIPTION</span></span>
<span data-ttu-id="04f6d-106">Обновляет параметры рабочей области для подписки.</span><span class="sxs-lookup"><span data-stu-id="04f6d-106">Updates the workspace settings for the subscription.</span></span>
<span data-ttu-id="04f6d-107">Настроенная рабочая область будет хранить данные безопасности, собранные агентом безопасности, установленным в виртуальных машинах в этой подписке.</span><span class="sxs-lookup"><span data-stu-id="04f6d-107">The configured workspace will hold the security data that was collected by the security agent that is installed in VMs inside this subscription.</span></span>

## <span data-ttu-id="04f6d-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="04f6d-108">EXAMPLES</span></span>

### <span data-ttu-id="04f6d-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="04f6d-109">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityWorkspaceSetting -Name "default" -Scope "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869" -WorkspaceId  "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/mainws/providers/microsoft.operationalinsights/workspaces/securityuserws"

Id                                                                                                         Name    WorkspaceId 
--                                                                                                         ----    ----
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/workspaceSettings/default default /...
```

<span data-ttu-id="04f6d-110">Задает рабочую область "myWorkspace", в которой хранятся все данные безопасности, собранные агентами безопасности.</span><span class="sxs-lookup"><span data-stu-id="04f6d-110">Sets the "myWorkspace" workspace to hold all the security data that was collected by the security agents.</span></span>

## <span data-ttu-id="04f6d-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="04f6d-111">PARAMETERS</span></span>

### <span data-ttu-id="04f6d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04f6d-112">-DefaultProfile</span></span>
<span data-ttu-id="04f6d-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="04f6d-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04f6d-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="04f6d-114">-Name</span></span>
<span data-ttu-id="04f6d-115">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="04f6d-115">Resource name.</span></span>

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

### <span data-ttu-id="04f6d-116">-Scope</span><span class="sxs-lookup"><span data-stu-id="04f6d-116">-Scope</span></span>
<span data-ttu-id="04f6d-117">Област.</span><span class="sxs-lookup"><span data-stu-id="04f6d-117">Scope.</span></span>

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

### <span data-ttu-id="04f6d-118">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="04f6d-118">-WorkspaceId</span></span>
<span data-ttu-id="04f6d-119">ИДЕНТИФИКАТОР рабочей области.</span><span class="sxs-lookup"><span data-stu-id="04f6d-119">Workspace ID.</span></span>

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

### <span data-ttu-id="04f6d-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="04f6d-120">-Confirm</span></span>
<span data-ttu-id="04f6d-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="04f6d-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04f6d-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04f6d-122">-WhatIf</span></span>
<span data-ttu-id="04f6d-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="04f6d-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="04f6d-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="04f6d-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04f6d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04f6d-125">CommonParameters</span></span>
<span data-ttu-id="04f6d-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="04f6d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04f6d-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04f6d-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04f6d-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="04f6d-128">INPUTS</span></span>

### <span data-ttu-id="04f6d-129">System. String</span><span class="sxs-lookup"><span data-stu-id="04f6d-129">System.String</span></span>

## <span data-ttu-id="04f6d-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="04f6d-130">OUTPUTS</span></span>

### <span data-ttu-id="04f6d-131">Microsoft. Azure. Commands. Security. Models. WorkspaceSettings. PSSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="04f6d-131">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="04f6d-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="04f6d-132">NOTES</span></span>

## <span data-ttu-id="04f6d-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="04f6d-133">RELATED LINKS</span></span>

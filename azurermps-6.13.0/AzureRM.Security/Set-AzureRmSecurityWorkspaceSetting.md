---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityWorkspaceSetting.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityWorkspaceSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityWorkspaceSetting.md
ms.openlocfilehash: 3d2fdd8b6a1763aea97da3967fb2696857e7fd75
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566411"
---
# <span data-ttu-id="3e036-101">Set-AzureRmSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="3e036-101">Set-AzureRmSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="3e036-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3e036-102">SYNOPSIS</span></span>
<span data-ttu-id="3e036-103">Обновляет параметры рабочей области для подписки.</span><span class="sxs-lookup"><span data-stu-id="3e036-103">Updates the workspace settings for the subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3e036-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3e036-104">SYNTAX</span></span>

```
Set-AzureRmSecurityWorkspaceSetting -Name <String> -Scope <String> -WorkspaceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e036-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3e036-105">DESCRIPTION</span></span>
<span data-ttu-id="3e036-106">Обновляет параметры рабочей области для подписки.</span><span class="sxs-lookup"><span data-stu-id="3e036-106">Updates the workspace settings for the subscription.</span></span>
<span data-ttu-id="3e036-107">Настроенная рабочая область будет хранить данные безопасности, собранные агентом безопасности, установленным в виртуальных машинах в этой подписке.</span><span class="sxs-lookup"><span data-stu-id="3e036-107">The configured workspace will hold the security data that was collected by the security agent that is installed in VMs inside this subscription.</span></span>

## <span data-ttu-id="3e036-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3e036-108">EXAMPLES</span></span>

### <span data-ttu-id="3e036-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3e036-109">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmSecurityWorkspaceSetting -Name "default" -Scope "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869" -WorkspaceId  "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/mainws/providers/microsoft.operationalinsights/workspaces/securityuserws"

Id                                                                                                         Name    WorkspaceId 
--                                                                                                         ----    ----
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/workspaceSettings/default default /...
```

<span data-ttu-id="3e036-110">Задает рабочую область "myWorkspace", в которой хранятся все данные безопасности, собранные агентами безопасности.</span><span class="sxs-lookup"><span data-stu-id="3e036-110">Sets the "myWorkspace" workspace to hold all the security data that was collected by the security agents.</span></span>

## <span data-ttu-id="3e036-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3e036-111">PARAMETERS</span></span>

### <span data-ttu-id="3e036-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e036-112">-DefaultProfile</span></span>
<span data-ttu-id="3e036-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3e036-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e036-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3e036-114">-Name</span></span>
<span data-ttu-id="3e036-115">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="3e036-115">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e036-116">-Scope</span><span class="sxs-lookup"><span data-stu-id="3e036-116">-Scope</span></span>
<span data-ttu-id="3e036-117">Област.</span><span class="sxs-lookup"><span data-stu-id="3e036-117">Scope.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e036-118">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="3e036-118">-WorkspaceId</span></span>
<span data-ttu-id="3e036-119">ИДЕНТИФИКАТОР рабочей области.</span><span class="sxs-lookup"><span data-stu-id="3e036-119">Workspace ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e036-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3e036-120">-Confirm</span></span>
<span data-ttu-id="3e036-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3e036-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e036-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e036-122">-WhatIf</span></span>
<span data-ttu-id="3e036-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3e036-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3e036-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3e036-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e036-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e036-125">CommonParameters</span></span>
<span data-ttu-id="3e036-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3e036-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e036-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e036-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e036-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3e036-128">INPUTS</span></span>

### <span data-ttu-id="3e036-129">System. String</span><span class="sxs-lookup"><span data-stu-id="3e036-129">System.String</span></span>

## <span data-ttu-id="3e036-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3e036-130">OUTPUTS</span></span>

### <span data-ttu-id="3e036-131">Microsoft. Azure. Commands. Security. Models. WorkspaceSettings. PSSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="3e036-131">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="3e036-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="3e036-132">NOTES</span></span>

## <span data-ttu-id="3e036-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3e036-133">RELATED LINKS</span></span>

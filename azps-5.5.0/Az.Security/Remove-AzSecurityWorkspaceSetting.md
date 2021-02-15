---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzSecurityWorkspaceSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityWorkspaceSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityWorkspaceSetting.md
ms.openlocfilehash: 75e68cfac55c8fb7086f02d5e70dc466f335d1de
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100217652"
---
# <span data-ttu-id="4e0cd-101">Remove-AzSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="4e0cd-101">Remove-AzSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="4e0cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4e0cd-102">SYNOPSIS</span></span>
<span data-ttu-id="4e0cd-103">Удаляет параметр рабочей области безопасности для этой подписки.</span><span class="sxs-lookup"><span data-stu-id="4e0cd-103">Deletes the security workspace setting for this subscription.</span></span>

## <span data-ttu-id="4e0cd-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4e0cd-104">SYNTAX</span></span>

### <span data-ttu-id="4e0cd-105">SubscriptionLevelResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4e0cd-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzSecurityWorkspaceSetting -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e0cd-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="4e0cd-106">ResourceId</span></span>
```
Remove-AzSecurityWorkspaceSetting -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e0cd-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="4e0cd-107">InputObject</span></span>
```
Remove-AzSecurityWorkspaceSetting -InputObject <PSSecurityWorkspaceSetting> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e0cd-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4e0cd-108">DESCRIPTION</span></span>
<span data-ttu-id="4e0cd-109">Удаляет параметр рабочей области безопасности для этой подписки.</span><span class="sxs-lookup"><span data-stu-id="4e0cd-109">Deletes the security workspace setting for this subscription.</span></span>
<span data-ttu-id="4e0cd-110">Это действие позволит новым установленным агентам безопасности сообщать о них в стандартную область данной подписки.</span><span class="sxs-lookup"><span data-stu-id="4e0cd-110">This action will make the newly installed security agents to report to the default workspace of this subscription.</span></span>

## <span data-ttu-id="4e0cd-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4e0cd-111">EXAMPLES</span></span>

### <span data-ttu-id="4e0cd-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4e0cd-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSecurityWorkspaceSetting -Name "default"
```

<span data-ttu-id="4e0cd-113">Удаляет параметр рабочей области безопасности для этой подписки.</span><span class="sxs-lookup"><span data-stu-id="4e0cd-113">Deletes the security workspace setting for this subscription.</span></span>

## <span data-ttu-id="4e0cd-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4e0cd-114">PARAMETERS</span></span>

### <span data-ttu-id="4e0cd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e0cd-115">-DefaultProfile</span></span>
<span data-ttu-id="4e0cd-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4e0cd-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e0cd-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4e0cd-117">-InputObject</span></span>
<span data-ttu-id="4e0cd-118">Объект ввода.</span><span class="sxs-lookup"><span data-stu-id="4e0cd-118">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4e0cd-119">-Name</span><span class="sxs-lookup"><span data-stu-id="4e0cd-119">-Name</span></span>
<span data-ttu-id="4e0cd-120">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="4e0cd-120">Resource name.</span></span>

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

### <span data-ttu-id="4e0cd-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4e0cd-121">-PassThru</span></span>
<span data-ttu-id="4e0cd-122">Возвращает, была ли операция успешной.</span><span class="sxs-lookup"><span data-stu-id="4e0cd-122">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="4e0cd-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4e0cd-123">-ResourceId</span></span>
<span data-ttu-id="4e0cd-124">ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="4e0cd-124">Resource ID.</span></span>

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

### <span data-ttu-id="4e0cd-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4e0cd-125">-Confirm</span></span>
<span data-ttu-id="4e0cd-126">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="4e0cd-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e0cd-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e0cd-127">-WhatIf</span></span>
<span data-ttu-id="4e0cd-128">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4e0cd-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4e0cd-129">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="4e0cd-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e0cd-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e0cd-130">CommonParameters</span></span>
<span data-ttu-id="4e0cd-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e0cd-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e0cd-132">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4e0cd-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e0cd-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4e0cd-133">INPUTS</span></span>

### <span data-ttu-id="4e0cd-134">System.String</span><span class="sxs-lookup"><span data-stu-id="4e0cd-134">System.String</span></span>

### <span data-ttu-id="4e0cd-135">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="4e0cd-135">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="4e0cd-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4e0cd-136">OUTPUTS</span></span>

### <span data-ttu-id="4e0cd-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4e0cd-137">System.Boolean</span></span>

## <span data-ttu-id="4e0cd-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4e0cd-138">NOTES</span></span>

## <span data-ttu-id="4e0cd-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4e0cd-139">RELATED LINKS</span></span>

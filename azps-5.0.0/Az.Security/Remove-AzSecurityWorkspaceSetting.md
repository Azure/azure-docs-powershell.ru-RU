---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzSecurityWorkspaceSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityWorkspaceSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityWorkspaceSetting.md
ms.openlocfilehash: 75e68cfac55c8fb7086f02d5e70dc466f335d1de
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248010"
---
# <span data-ttu-id="56d5c-101">Remove-AzSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="56d5c-101">Remove-AzSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="56d5c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="56d5c-102">SYNOPSIS</span></span>
<span data-ttu-id="56d5c-103">Удаление параметра рабочей области безопасности для этой подписки.</span><span class="sxs-lookup"><span data-stu-id="56d5c-103">Deletes the security workspace setting for this subscription.</span></span>

## <span data-ttu-id="56d5c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="56d5c-104">SYNTAX</span></span>

### <span data-ttu-id="56d5c-105">SubscriptionLevelResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="56d5c-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzSecurityWorkspaceSetting -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56d5c-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="56d5c-106">ResourceId</span></span>
```
Remove-AzSecurityWorkspaceSetting -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56d5c-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="56d5c-107">InputObject</span></span>
```
Remove-AzSecurityWorkspaceSetting -InputObject <PSSecurityWorkspaceSetting> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56d5c-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="56d5c-108">DESCRIPTION</span></span>
<span data-ttu-id="56d5c-109">Удаление параметра рабочей области безопасности для этой подписки.</span><span class="sxs-lookup"><span data-stu-id="56d5c-109">Deletes the security workspace setting for this subscription.</span></span>
<span data-ttu-id="56d5c-110">С помощью этого действия новые установленные агенты безопасности будут сообщать о рабочей области по умолчанию для этой подписки.</span><span class="sxs-lookup"><span data-stu-id="56d5c-110">This action will make the newly installed security agents to report to the default workspace of this subscription.</span></span>

## <span data-ttu-id="56d5c-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="56d5c-111">EXAMPLES</span></span>

### <span data-ttu-id="56d5c-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="56d5c-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSecurityWorkspaceSetting -Name "default"
```

<span data-ttu-id="56d5c-113">Удаление параметра рабочей области безопасности для этой подписки.</span><span class="sxs-lookup"><span data-stu-id="56d5c-113">Deletes the security workspace setting for this subscription.</span></span>

## <span data-ttu-id="56d5c-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="56d5c-114">PARAMETERS</span></span>

### <span data-ttu-id="56d5c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56d5c-115">-DefaultProfile</span></span>
<span data-ttu-id="56d5c-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="56d5c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56d5c-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="56d5c-117">-InputObject</span></span>
<span data-ttu-id="56d5c-118">Объект input.</span><span class="sxs-lookup"><span data-stu-id="56d5c-118">Input Object.</span></span>

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

### <span data-ttu-id="56d5c-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="56d5c-119">-Name</span></span>
<span data-ttu-id="56d5c-120">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="56d5c-120">Resource name.</span></span>

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

### <span data-ttu-id="56d5c-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="56d5c-121">-PassThru</span></span>
<span data-ttu-id="56d5c-122">Возвращает значение, указывающее, была ли операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="56d5c-122">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="56d5c-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="56d5c-123">-ResourceId</span></span>
<span data-ttu-id="56d5c-124">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="56d5c-124">Resource ID.</span></span>

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

### <span data-ttu-id="56d5c-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="56d5c-125">-Confirm</span></span>
<span data-ttu-id="56d5c-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="56d5c-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56d5c-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56d5c-127">-WhatIf</span></span>
<span data-ttu-id="56d5c-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="56d5c-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="56d5c-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="56d5c-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56d5c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56d5c-130">CommonParameters</span></span>
<span data-ttu-id="56d5c-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="56d5c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56d5c-132">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="56d5c-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56d5c-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="56d5c-133">INPUTS</span></span>

### <span data-ttu-id="56d5c-134">System. String</span><span class="sxs-lookup"><span data-stu-id="56d5c-134">System.String</span></span>

### <span data-ttu-id="56d5c-135">Microsoft. Azure. Commands. Security. Models. WorkspaceSettings. PSSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="56d5c-135">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="56d5c-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="56d5c-136">OUTPUTS</span></span>

### <span data-ttu-id="56d5c-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="56d5c-137">System.Boolean</span></span>

## <span data-ttu-id="56d5c-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="56d5c-138">NOTES</span></span>

## <span data-ttu-id="56d5c-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="56d5c-139">RELATED LINKS</span></span>

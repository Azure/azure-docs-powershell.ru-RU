---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Set-AzSecurityAlert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAlert.md
ms.openlocfilehash: 889e4a0651c9aa3ccbe91227db803958fcb3c7bc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986572"
---
# <span data-ttu-id="b900a-101">Set-AzSecurityAlert</span><span class="sxs-lookup"><span data-stu-id="b900a-101">Set-AzSecurityAlert</span></span>

## <span data-ttu-id="b900a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b900a-102">SYNOPSIS</span></span>
<span data-ttu-id="b900a-103">Обновляет состояние оповещения системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="b900a-103">Updates a security alert state.</span></span>

## <span data-ttu-id="b900a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b900a-104">SYNTAX</span></span>

### <span data-ttu-id="b900a-105">SubscriptionLevelResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b900a-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzSecurityAlert -Location <String> -Name <String> -ActionType <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b900a-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="b900a-106">ResourceGroupLevelResource</span></span>
```
Set-AzSecurityAlert -ResourceGroupName <String> -Location <String> -Name <String> -ActionType <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b900a-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="b900a-107">ResourceId</span></span>
```
Set-AzSecurityAlert -ActionType <String> -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b900a-108">InputObject</span><span class="sxs-lookup"><span data-stu-id="b900a-108">InputObject</span></span>
```
Set-AzSecurityAlert [-ActionType <String>] -InputObject <PSSecurityAlert> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b900a-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b900a-109">DESCRIPTION</span></span>
<span data-ttu-id="b900a-110">Настраивает состояние оповещения системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="b900a-110">Sets a security alert state.</span></span>

## <span data-ttu-id="b900a-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b900a-111">EXAMPLES</span></span>

### <span data-ttu-id="b900a-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b900a-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityAlert -Location "centralus" -ResourceGroupName "RSG" -Name "2518710774294070750_FFF23C70-80EF-4A8B-9122-507B0EA8DFFF" -ActionType Dismiss
```

<span data-ttu-id="b900a-113">Отклонено оповещение системы безопасности, которое было сдвещено.</span><span class="sxs-lookup"><span data-stu-id="b900a-113">Dismisses a security alert that was raised.</span></span>

## <span data-ttu-id="b900a-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b900a-114">PARAMETERS</span></span>

### <span data-ttu-id="b900a-115">-ActionType</span><span class="sxs-lookup"><span data-stu-id="b900a-115">-ActionType</span></span>
<span data-ttu-id="b900a-116">Тип действия.</span><span class="sxs-lookup"><span data-stu-id="b900a-116">Action Type.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource, ResourceGroupLevelResource, ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b900a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b900a-117">-DefaultProfile</span></span>
<span data-ttu-id="b900a-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b900a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b900a-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b900a-119">-InputObject</span></span>
<span data-ttu-id="b900a-120">Объект ввода.</span><span class="sxs-lookup"><span data-stu-id="b900a-120">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.Alerts.PSSecurityAlert
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b900a-121">-Location</span><span class="sxs-lookup"><span data-stu-id="b900a-121">-Location</span></span>
<span data-ttu-id="b900a-122">"Расположение".</span><span class="sxs-lookup"><span data-stu-id="b900a-122">Location.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource, ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b900a-123">-Name</span><span class="sxs-lookup"><span data-stu-id="b900a-123">-Name</span></span>
<span data-ttu-id="b900a-124">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="b900a-124">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource, ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b900a-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b900a-125">-PassThru</span></span>
<span data-ttu-id="b900a-126">Возвращает, была ли операция успешной.</span><span class="sxs-lookup"><span data-stu-id="b900a-126">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="b900a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b900a-127">-ResourceGroupName</span></span>
<span data-ttu-id="b900a-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b900a-128">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b900a-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b900a-129">-ResourceId</span></span>
<span data-ttu-id="b900a-130">ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="b900a-130">Resource ID.</span></span>

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

### <span data-ttu-id="b900a-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b900a-131">-Confirm</span></span>
<span data-ttu-id="b900a-132">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b900a-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b900a-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b900a-133">-WhatIf</span></span>
<span data-ttu-id="b900a-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b900a-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b900a-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="b900a-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b900a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b900a-136">CommonParameters</span></span>
<span data-ttu-id="b900a-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b900a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b900a-138">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b900a-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b900a-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b900a-139">INPUTS</span></span>

### <span data-ttu-id="b900a-140">System.String</span><span class="sxs-lookup"><span data-stu-id="b900a-140">System.String</span></span>

### <span data-ttu-id="b900a-141">Microsoft.Azure.Commands.Security.Models.Alerts.PSSecurityAlert</span><span class="sxs-lookup"><span data-stu-id="b900a-141">Microsoft.Azure.Commands.Security.Models.Alerts.PSSecurityAlert</span></span>

## <span data-ttu-id="b900a-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b900a-142">OUTPUTS</span></span>

### <span data-ttu-id="b900a-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b900a-143">System.Boolean</span></span>

## <span data-ttu-id="b900a-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b900a-144">NOTES</span></span>

## <span data-ttu-id="b900a-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b900a-145">RELATED LINKS</span></span>

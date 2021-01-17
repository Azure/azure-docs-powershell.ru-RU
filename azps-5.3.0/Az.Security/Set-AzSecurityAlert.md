---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityAlert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAlert.md
ms.openlocfilehash: 0555b86b6e5240adfc43bc52153bf14d7612be1b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98423660"
---
# <span data-ttu-id="8ed66-101">Set-AzSecurityAlert</span><span class="sxs-lookup"><span data-stu-id="8ed66-101">Set-AzSecurityAlert</span></span>

## <span data-ttu-id="8ed66-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ed66-102">SYNOPSIS</span></span>
<span data-ttu-id="8ed66-103">Обновляет состояние оповещения системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="8ed66-103">Updates a security alert state.</span></span>

## <span data-ttu-id="8ed66-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8ed66-104">SYNTAX</span></span>

### <span data-ttu-id="8ed66-105">SubscriptionLevelResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8ed66-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzSecurityAlert -Location <String> -Name <String> -ActionType <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ed66-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="8ed66-106">ResourceGroupLevelResource</span></span>
```
Set-AzSecurityAlert -ResourceGroupName <String> -Location <String> -Name <String> -ActionType <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ed66-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="8ed66-107">ResourceId</span></span>
```
Set-AzSecurityAlert -ActionType <String> -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ed66-108">InputObject</span><span class="sxs-lookup"><span data-stu-id="8ed66-108">InputObject</span></span>
```
Set-AzSecurityAlert [-ActionType <String>] -InputObject <PSSecurityAlert> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ed66-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8ed66-109">DESCRIPTION</span></span>
<span data-ttu-id="8ed66-110">Настраивает состояние оповещения системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="8ed66-110">Sets a security alert state.</span></span>

## <span data-ttu-id="8ed66-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8ed66-111">EXAMPLES</span></span>

### <span data-ttu-id="8ed66-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8ed66-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityAlert -Location "centralus" -ResourceGroupName "RSG" -Name "2518710774294070750_FFF23C70-80EF-4A8B-9122-507B0EA8DFFF" -ActionType Dismiss
```

<span data-ttu-id="8ed66-113">Отклонено оповещение системы безопасности, которое было сдвещено.</span><span class="sxs-lookup"><span data-stu-id="8ed66-113">Dismisses a security alert that was raised.</span></span>

## <span data-ttu-id="8ed66-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8ed66-114">PARAMETERS</span></span>

### <span data-ttu-id="8ed66-115">-ActionType</span><span class="sxs-lookup"><span data-stu-id="8ed66-115">-ActionType</span></span>
<span data-ttu-id="8ed66-116">Тип действия.</span><span class="sxs-lookup"><span data-stu-id="8ed66-116">Action Type.</span></span>

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

### <span data-ttu-id="8ed66-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ed66-117">-DefaultProfile</span></span>
<span data-ttu-id="8ed66-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8ed66-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8ed66-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8ed66-119">-InputObject</span></span>
<span data-ttu-id="8ed66-120">Объект ввода.</span><span class="sxs-lookup"><span data-stu-id="8ed66-120">Input Object.</span></span>

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

### <span data-ttu-id="8ed66-121">-Location</span><span class="sxs-lookup"><span data-stu-id="8ed66-121">-Location</span></span>
<span data-ttu-id="8ed66-122">"Расположение".</span><span class="sxs-lookup"><span data-stu-id="8ed66-122">Location.</span></span>

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

### <span data-ttu-id="8ed66-123">-Name</span><span class="sxs-lookup"><span data-stu-id="8ed66-123">-Name</span></span>
<span data-ttu-id="8ed66-124">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="8ed66-124">Resource name.</span></span>

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

### <span data-ttu-id="8ed66-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8ed66-125">-PassThru</span></span>
<span data-ttu-id="8ed66-126">Возвращает, была ли операция успешной.</span><span class="sxs-lookup"><span data-stu-id="8ed66-126">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="8ed66-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ed66-127">-ResourceGroupName</span></span>
<span data-ttu-id="8ed66-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8ed66-128">Resource group name.</span></span>

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

### <span data-ttu-id="8ed66-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8ed66-129">-ResourceId</span></span>
<span data-ttu-id="8ed66-130">ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="8ed66-130">Resource ID.</span></span>

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

### <span data-ttu-id="8ed66-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8ed66-131">-Confirm</span></span>
<span data-ttu-id="8ed66-132">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="8ed66-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ed66-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ed66-133">-WhatIf</span></span>
<span data-ttu-id="8ed66-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ed66-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8ed66-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="8ed66-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ed66-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ed66-136">CommonParameters</span></span>
<span data-ttu-id="8ed66-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ed66-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ed66-138">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8ed66-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ed66-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8ed66-139">INPUTS</span></span>

### <span data-ttu-id="8ed66-140">System.String</span><span class="sxs-lookup"><span data-stu-id="8ed66-140">System.String</span></span>

### <span data-ttu-id="8ed66-141">Microsoft.Azure.Commands.Security.Models.Alerts.PSSecurityAlert</span><span class="sxs-lookup"><span data-stu-id="8ed66-141">Microsoft.Azure.Commands.Security.Models.Alerts.PSSecurityAlert</span></span>

## <span data-ttu-id="8ed66-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8ed66-142">OUTPUTS</span></span>

### <span data-ttu-id="8ed66-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8ed66-143">System.Boolean</span></span>

## <span data-ttu-id="8ed66-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8ed66-144">NOTES</span></span>

## <span data-ttu-id="8ed66-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8ed66-145">RELATED LINKS</span></span>

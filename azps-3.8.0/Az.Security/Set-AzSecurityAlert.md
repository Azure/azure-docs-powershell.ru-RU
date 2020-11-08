---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityAlert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAlert.md
ms.openlocfilehash: 9618720b234f00700100e14b4e973e3a57f22705
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073775"
---
# <span data-ttu-id="11e82-101">Set-AzSecurityAlert</span><span class="sxs-lookup"><span data-stu-id="11e82-101">Set-AzSecurityAlert</span></span>

## <span data-ttu-id="11e82-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="11e82-102">SYNOPSIS</span></span>
<span data-ttu-id="11e82-103">Обновляет состояние оповещения системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="11e82-103">Updates a security alert state.</span></span>

## <span data-ttu-id="11e82-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="11e82-104">SYNTAX</span></span>

### <span data-ttu-id="11e82-105">SubscriptionLevelResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="11e82-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzSecurityAlert -Location <String> -Name <String> -ActionType <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11e82-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="11e82-106">ResourceGroupLevelResource</span></span>
```
Set-AzSecurityAlert -ResourceGroupName <String> -Location <String> -Name <String> -ActionType <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11e82-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="11e82-107">ResourceId</span></span>
```
Set-AzSecurityAlert -ActionType <String> -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11e82-108">InputObject</span><span class="sxs-lookup"><span data-stu-id="11e82-108">InputObject</span></span>
```
Set-AzSecurityAlert [-ActionType <String>] -InputObject <PSSecurityAlert> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11e82-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="11e82-109">DESCRIPTION</span></span>
<span data-ttu-id="11e82-110">Задает состояние оповещения системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="11e82-110">Sets a security alert state.</span></span>

## <span data-ttu-id="11e82-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="11e82-111">EXAMPLES</span></span>

### <span data-ttu-id="11e82-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="11e82-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityAlert -Location "centralus" -ResourceGroupName "RSG" -Name "2518710774294070750_FFF23C70-80EF-4A8B-9122-507B0EA8DFFF" -ActionType Dismiss
```

<span data-ttu-id="11e82-113">Закрывает возникшее оповещение системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="11e82-113">Dismisses a security alert that was raised.</span></span>

## <span data-ttu-id="11e82-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="11e82-114">PARAMETERS</span></span>

### <span data-ttu-id="11e82-115">-Себя</span><span class="sxs-lookup"><span data-stu-id="11e82-115">-ActionType</span></span>
<span data-ttu-id="11e82-116">Тип действия.</span><span class="sxs-lookup"><span data-stu-id="11e82-116">Action Type.</span></span>

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

### <span data-ttu-id="11e82-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11e82-117">-DefaultProfile</span></span>
<span data-ttu-id="11e82-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="11e82-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11e82-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="11e82-119">-InputObject</span></span>
<span data-ttu-id="11e82-120">Объект input.</span><span class="sxs-lookup"><span data-stu-id="11e82-120">Input Object.</span></span>

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

### <span data-ttu-id="11e82-121">-Location</span><span class="sxs-lookup"><span data-stu-id="11e82-121">-Location</span></span>
<span data-ttu-id="11e82-122">Поиска.</span><span class="sxs-lookup"><span data-stu-id="11e82-122">Location.</span></span>

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

### <span data-ttu-id="11e82-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="11e82-123">-Name</span></span>
<span data-ttu-id="11e82-124">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="11e82-124">Resource name.</span></span>

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

### <span data-ttu-id="11e82-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="11e82-125">-PassThru</span></span>
<span data-ttu-id="11e82-126">Возвращает значение, указывающее, была ли операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="11e82-126">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="11e82-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11e82-127">-ResourceGroupName</span></span>
<span data-ttu-id="11e82-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="11e82-128">Resource group name.</span></span>

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

### <span data-ttu-id="11e82-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="11e82-129">-ResourceId</span></span>
<span data-ttu-id="11e82-130">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="11e82-130">Resource ID.</span></span>

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

### <span data-ttu-id="11e82-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="11e82-131">-Confirm</span></span>
<span data-ttu-id="11e82-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="11e82-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11e82-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11e82-133">-WhatIf</span></span>
<span data-ttu-id="11e82-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="11e82-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="11e82-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="11e82-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11e82-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11e82-136">CommonParameters</span></span>
<span data-ttu-id="11e82-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="11e82-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11e82-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11e82-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11e82-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="11e82-139">INPUTS</span></span>

### <span data-ttu-id="11e82-140">System. String</span><span class="sxs-lookup"><span data-stu-id="11e82-140">System.String</span></span>

### <span data-ttu-id="11e82-141">Microsoft. Azure. Commands. Security. Models. Alerts. PSSecurityAlert</span><span class="sxs-lookup"><span data-stu-id="11e82-141">Microsoft.Azure.Commands.Security.Models.Alerts.PSSecurityAlert</span></span>

## <span data-ttu-id="11e82-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="11e82-142">OUTPUTS</span></span>

### <span data-ttu-id="11e82-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="11e82-143">System.Boolean</span></span>

## <span data-ttu-id="11e82-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="11e82-144">NOTES</span></span>

## <span data-ttu-id="11e82-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="11e82-145">RELATED LINKS</span></span>

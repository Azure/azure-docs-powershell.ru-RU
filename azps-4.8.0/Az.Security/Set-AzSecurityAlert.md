---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityAlert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAlert.md
ms.openlocfilehash: 0555b86b6e5240adfc43bc52153bf14d7612be1b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235358"
---
# <span data-ttu-id="5883e-101">Set-AzSecurityAlert</span><span class="sxs-lookup"><span data-stu-id="5883e-101">Set-AzSecurityAlert</span></span>

## <span data-ttu-id="5883e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5883e-102">SYNOPSIS</span></span>
<span data-ttu-id="5883e-103">Обновляет состояние оповещения системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="5883e-103">Updates a security alert state.</span></span>

## <span data-ttu-id="5883e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5883e-104">SYNTAX</span></span>

### <span data-ttu-id="5883e-105">SubscriptionLevelResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5883e-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzSecurityAlert -Location <String> -Name <String> -ActionType <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5883e-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="5883e-106">ResourceGroupLevelResource</span></span>
```
Set-AzSecurityAlert -ResourceGroupName <String> -Location <String> -Name <String> -ActionType <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5883e-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="5883e-107">ResourceId</span></span>
```
Set-AzSecurityAlert -ActionType <String> -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5883e-108">InputObject</span><span class="sxs-lookup"><span data-stu-id="5883e-108">InputObject</span></span>
```
Set-AzSecurityAlert [-ActionType <String>] -InputObject <PSSecurityAlert> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5883e-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5883e-109">DESCRIPTION</span></span>
<span data-ttu-id="5883e-110">Задает состояние оповещения системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="5883e-110">Sets a security alert state.</span></span>

## <span data-ttu-id="5883e-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5883e-111">EXAMPLES</span></span>

### <span data-ttu-id="5883e-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5883e-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityAlert -Location "centralus" -ResourceGroupName "RSG" -Name "2518710774294070750_FFF23C70-80EF-4A8B-9122-507B0EA8DFFF" -ActionType Dismiss
```

<span data-ttu-id="5883e-113">Закрывает возникшее оповещение системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="5883e-113">Dismisses a security alert that was raised.</span></span>

## <span data-ttu-id="5883e-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5883e-114">PARAMETERS</span></span>

### <span data-ttu-id="5883e-115">-Себя</span><span class="sxs-lookup"><span data-stu-id="5883e-115">-ActionType</span></span>
<span data-ttu-id="5883e-116">Тип действия.</span><span class="sxs-lookup"><span data-stu-id="5883e-116">Action Type.</span></span>

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

### <span data-ttu-id="5883e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5883e-117">-DefaultProfile</span></span>
<span data-ttu-id="5883e-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5883e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5883e-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5883e-119">-InputObject</span></span>
<span data-ttu-id="5883e-120">Объект input.</span><span class="sxs-lookup"><span data-stu-id="5883e-120">Input Object.</span></span>

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

### <span data-ttu-id="5883e-121">-Location</span><span class="sxs-lookup"><span data-stu-id="5883e-121">-Location</span></span>
<span data-ttu-id="5883e-122">Поиска.</span><span class="sxs-lookup"><span data-stu-id="5883e-122">Location.</span></span>

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

### <span data-ttu-id="5883e-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5883e-123">-Name</span></span>
<span data-ttu-id="5883e-124">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="5883e-124">Resource name.</span></span>

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

### <span data-ttu-id="5883e-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5883e-125">-PassThru</span></span>
<span data-ttu-id="5883e-126">Возвращает значение, указывающее, была ли операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="5883e-126">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="5883e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5883e-127">-ResourceGroupName</span></span>
<span data-ttu-id="5883e-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5883e-128">Resource group name.</span></span>

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

### <span data-ttu-id="5883e-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5883e-129">-ResourceId</span></span>
<span data-ttu-id="5883e-130">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="5883e-130">Resource ID.</span></span>

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

### <span data-ttu-id="5883e-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5883e-131">-Confirm</span></span>
<span data-ttu-id="5883e-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5883e-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5883e-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5883e-133">-WhatIf</span></span>
<span data-ttu-id="5883e-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5883e-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5883e-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5883e-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5883e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5883e-136">CommonParameters</span></span>
<span data-ttu-id="5883e-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5883e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5883e-138">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5883e-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5883e-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5883e-139">INPUTS</span></span>

### <span data-ttu-id="5883e-140">System. String</span><span class="sxs-lookup"><span data-stu-id="5883e-140">System.String</span></span>

### <span data-ttu-id="5883e-141">Microsoft. Azure. Commands. Security. Models. Alerts. PSSecurityAlert</span><span class="sxs-lookup"><span data-stu-id="5883e-141">Microsoft.Azure.Commands.Security.Models.Alerts.PSSecurityAlert</span></span>

## <span data-ttu-id="5883e-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5883e-142">OUTPUTS</span></span>

### <span data-ttu-id="5883e-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5883e-143">System.Boolean</span></span>

## <span data-ttu-id="5883e-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="5883e-144">NOTES</span></span>

## <span data-ttu-id="5883e-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5883e-145">RELATED LINKS</span></span>

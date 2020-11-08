---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/update-azalertstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzAlertState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzAlertState.md
ms.openlocfilehash: 4ba238f75fa1e39daf2309a1ceda1aed323ff47d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249135"
---
# <span data-ttu-id="033b5-101">Update-AzAlertState</span><span class="sxs-lookup"><span data-stu-id="033b5-101">Update-AzAlertState</span></span>

## <span data-ttu-id="033b5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="033b5-102">SYNOPSIS</span></span>
<span data-ttu-id="033b5-103">Обновление состояния оповещения</span><span class="sxs-lookup"><span data-stu-id="033b5-103">Updates alert state</span></span>

## <span data-ttu-id="033b5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="033b5-104">SYNTAX</span></span>

### <span data-ttu-id="033b5-105">ByAlertId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="033b5-105">ByAlertId (Default)</span></span>
```
Update-AzAlertState -AlertId <String> -State <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="033b5-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="033b5-106">ByInputObject</span></span>
```
Update-AzAlertState -State <String> -InputObject <PSAlert> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="033b5-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="033b5-107">DESCRIPTION</span></span>
<span data-ttu-id="033b5-108">**Update-AzAlertState** . состояние предупреждения обновления командлетов.</span><span class="sxs-lookup"><span data-stu-id="033b5-108">**Update-AzAlertState** cmdlet updates alert state.</span></span>

## <span data-ttu-id="033b5-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="033b5-109">EXAMPLES</span></span>

### <span data-ttu-id="033b5-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="033b5-110">Example 1</span></span>
```powershell
PS C:\> Update-AzAlertState -AlertId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529" -State "Closed"
```

<span data-ttu-id="033b5-111">Этот командлет обновляет состояние предупреждения на Closed.</span><span class="sxs-lookup"><span data-stu-id="033b5-111">This cmdlet updates the alert state to Closed.</span></span>

## <span data-ttu-id="033b5-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="033b5-112">PARAMETERS</span></span>

### <span data-ttu-id="033b5-113">-AlertId</span><span class="sxs-lookup"><span data-stu-id="033b5-113">-AlertId</span></span>
<span data-ttu-id="033b5-114">Уникальный идентификатор оповещения/ResourceId для оповещения.</span><span class="sxs-lookup"><span data-stu-id="033b5-114">Unique Identifier of Alert / ResourceId of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAlertId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="033b5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="033b5-115">-DefaultProfile</span></span>
<span data-ttu-id="033b5-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="033b5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="033b5-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="033b5-117">-InputObject</span></span>
<span data-ttu-id="033b5-118">Объект ввода из конвейера.</span><span class="sxs-lookup"><span data-stu-id="033b5-118">Input object from pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlert
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="033b5-119">-State</span><span class="sxs-lookup"><span data-stu-id="033b5-119">-State</span></span>
<span data-ttu-id="033b5-120">Обновленное состояние оповещения</span><span class="sxs-lookup"><span data-stu-id="033b5-120">Updated Alert State</span></span>

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

### <span data-ttu-id="033b5-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="033b5-121">-Confirm</span></span>
<span data-ttu-id="033b5-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="033b5-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="033b5-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="033b5-123">-WhatIf</span></span>
<span data-ttu-id="033b5-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="033b5-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="033b5-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="033b5-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="033b5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="033b5-126">CommonParameters</span></span>
<span data-ttu-id="033b5-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="033b5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="033b5-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="033b5-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="033b5-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="033b5-129">INPUTS</span></span>

### <span data-ttu-id="033b5-130">Ничего</span><span class="sxs-lookup"><span data-stu-id="033b5-130">None</span></span>

## <span data-ttu-id="033b5-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="033b5-131">OUTPUTS</span></span>

### <span data-ttu-id="033b5-132">Microsoft. Azure. Commands. AlertsManagement. OutputModels. PSAlert</span><span class="sxs-lookup"><span data-stu-id="033b5-132">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlert</span></span>

## <span data-ttu-id="033b5-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="033b5-133">NOTES</span></span>

## <span data-ttu-id="033b5-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="033b5-134">RELATED LINKS</span></span>

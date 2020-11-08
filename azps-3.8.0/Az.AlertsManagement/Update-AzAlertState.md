---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/update-azalertstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzAlertState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzAlertState.md
ms.openlocfilehash: 4ba238f75fa1e39daf2309a1ceda1aed323ff47d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065660"
---
# <span data-ttu-id="d7918-101">Update-AzAlertState</span><span class="sxs-lookup"><span data-stu-id="d7918-101">Update-AzAlertState</span></span>

## <span data-ttu-id="d7918-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d7918-102">SYNOPSIS</span></span>
<span data-ttu-id="d7918-103">Обновление состояния оповещения</span><span class="sxs-lookup"><span data-stu-id="d7918-103">Updates alert state</span></span>

## <span data-ttu-id="d7918-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d7918-104">SYNTAX</span></span>

### <span data-ttu-id="d7918-105">ByAlertId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d7918-105">ByAlertId (Default)</span></span>
```
Update-AzAlertState -AlertId <String> -State <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7918-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="d7918-106">ByInputObject</span></span>
```
Update-AzAlertState -State <String> -InputObject <PSAlert> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7918-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d7918-107">DESCRIPTION</span></span>
<span data-ttu-id="d7918-108">**Update-AzAlertState** . состояние предупреждения обновления командлетов.</span><span class="sxs-lookup"><span data-stu-id="d7918-108">**Update-AzAlertState** cmdlet updates alert state.</span></span>

## <span data-ttu-id="d7918-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d7918-109">EXAMPLES</span></span>

### <span data-ttu-id="d7918-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d7918-110">Example 1</span></span>
```powershell
PS C:\> Update-AzAlertState -AlertId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529" -State "Closed"
```

<span data-ttu-id="d7918-111">Этот командлет обновляет состояние предупреждения на Closed.</span><span class="sxs-lookup"><span data-stu-id="d7918-111">This cmdlet updates the alert state to Closed.</span></span>

## <span data-ttu-id="d7918-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d7918-112">PARAMETERS</span></span>

### <span data-ttu-id="d7918-113">-AlertId</span><span class="sxs-lookup"><span data-stu-id="d7918-113">-AlertId</span></span>
<span data-ttu-id="d7918-114">Уникальный идентификатор оповещения/ResourceId для оповещения.</span><span class="sxs-lookup"><span data-stu-id="d7918-114">Unique Identifier of Alert / ResourceId of alert.</span></span>

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

### <span data-ttu-id="d7918-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7918-115">-DefaultProfile</span></span>
<span data-ttu-id="d7918-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d7918-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7918-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d7918-117">-InputObject</span></span>
<span data-ttu-id="d7918-118">Объект ввода из конвейера.</span><span class="sxs-lookup"><span data-stu-id="d7918-118">Input object from pipeline.</span></span>

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

### <span data-ttu-id="d7918-119">-State</span><span class="sxs-lookup"><span data-stu-id="d7918-119">-State</span></span>
<span data-ttu-id="d7918-120">Обновленное состояние оповещения</span><span class="sxs-lookup"><span data-stu-id="d7918-120">Updated Alert State</span></span>

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

### <span data-ttu-id="d7918-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d7918-121">-Confirm</span></span>
<span data-ttu-id="d7918-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d7918-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7918-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7918-123">-WhatIf</span></span>
<span data-ttu-id="d7918-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d7918-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7918-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d7918-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7918-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7918-126">CommonParameters</span></span>
<span data-ttu-id="d7918-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d7918-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7918-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d7918-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7918-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d7918-129">INPUTS</span></span>

### <span data-ttu-id="d7918-130">Ничего</span><span class="sxs-lookup"><span data-stu-id="d7918-130">None</span></span>

## <span data-ttu-id="d7918-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d7918-131">OUTPUTS</span></span>

### <span data-ttu-id="d7918-132">Microsoft. Azure. Commands. AlertsManagement. OutputModels. PSAlert</span><span class="sxs-lookup"><span data-stu-id="d7918-132">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlert</span></span>

## <span data-ttu-id="d7918-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="d7918-133">NOTES</span></span>

## <span data-ttu-id="d7918-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d7918-134">RELATED LINKS</span></span>

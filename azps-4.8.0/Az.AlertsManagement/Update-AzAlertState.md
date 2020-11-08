---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/update-azalertstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzAlertState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzAlertState.md
ms.openlocfilehash: 4ba238f75fa1e39daf2309a1ceda1aed323ff47d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078030"
---
# <span data-ttu-id="f6060-101">Update-AzAlertState</span><span class="sxs-lookup"><span data-stu-id="f6060-101">Update-AzAlertState</span></span>

## <span data-ttu-id="f6060-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f6060-102">SYNOPSIS</span></span>
<span data-ttu-id="f6060-103">Обновление состояния оповещения</span><span class="sxs-lookup"><span data-stu-id="f6060-103">Updates alert state</span></span>

## <span data-ttu-id="f6060-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f6060-104">SYNTAX</span></span>

### <span data-ttu-id="f6060-105">ByAlertId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f6060-105">ByAlertId (Default)</span></span>
```
Update-AzAlertState -AlertId <String> -State <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6060-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="f6060-106">ByInputObject</span></span>
```
Update-AzAlertState -State <String> -InputObject <PSAlert> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6060-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f6060-107">DESCRIPTION</span></span>
<span data-ttu-id="f6060-108">**Update-AzAlertState** . состояние предупреждения обновления командлетов.</span><span class="sxs-lookup"><span data-stu-id="f6060-108">**Update-AzAlertState** cmdlet updates alert state.</span></span>

## <span data-ttu-id="f6060-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f6060-109">EXAMPLES</span></span>

### <span data-ttu-id="f6060-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f6060-110">Example 1</span></span>
```powershell
PS C:\> Update-AzAlertState -AlertId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529" -State "Closed"
```

<span data-ttu-id="f6060-111">Этот командлет обновляет состояние предупреждения на Closed.</span><span class="sxs-lookup"><span data-stu-id="f6060-111">This cmdlet updates the alert state to Closed.</span></span>

## <span data-ttu-id="f6060-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f6060-112">PARAMETERS</span></span>

### <span data-ttu-id="f6060-113">-AlertId</span><span class="sxs-lookup"><span data-stu-id="f6060-113">-AlertId</span></span>
<span data-ttu-id="f6060-114">Уникальный идентификатор оповещения/ResourceId для оповещения.</span><span class="sxs-lookup"><span data-stu-id="f6060-114">Unique Identifier of Alert / ResourceId of alert.</span></span>

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

### <span data-ttu-id="f6060-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6060-115">-DefaultProfile</span></span>
<span data-ttu-id="f6060-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f6060-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6060-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f6060-117">-InputObject</span></span>
<span data-ttu-id="f6060-118">Объект ввода из конвейера.</span><span class="sxs-lookup"><span data-stu-id="f6060-118">Input object from pipeline.</span></span>

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

### <span data-ttu-id="f6060-119">-State</span><span class="sxs-lookup"><span data-stu-id="f6060-119">-State</span></span>
<span data-ttu-id="f6060-120">Обновленное состояние оповещения</span><span class="sxs-lookup"><span data-stu-id="f6060-120">Updated Alert State</span></span>

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

### <span data-ttu-id="f6060-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f6060-121">-Confirm</span></span>
<span data-ttu-id="f6060-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f6060-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6060-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6060-123">-WhatIf</span></span>
<span data-ttu-id="f6060-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f6060-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6060-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f6060-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6060-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6060-126">CommonParameters</span></span>
<span data-ttu-id="f6060-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f6060-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6060-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f6060-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6060-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f6060-129">INPUTS</span></span>

### <span data-ttu-id="f6060-130">Ничего</span><span class="sxs-lookup"><span data-stu-id="f6060-130">None</span></span>

## <span data-ttu-id="f6060-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f6060-131">OUTPUTS</span></span>

### <span data-ttu-id="f6060-132">Microsoft. Azure. Commands. AlertsManagement. OutputModels. PSAlert</span><span class="sxs-lookup"><span data-stu-id="f6060-132">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlert</span></span>

## <span data-ttu-id="f6060-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="f6060-133">NOTES</span></span>

## <span data-ttu-id="f6060-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f6060-134">RELATED LINKS</span></span>

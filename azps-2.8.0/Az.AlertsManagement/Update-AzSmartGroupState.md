---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/update-azsmartgroupstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzSmartGroupState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzSmartGroupState.md
ms.openlocfilehash: 42ad9bf07a76bba0a3b8456691c34038e3b9372d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93728174"
---
# <span data-ttu-id="b720d-101">Update-AzSmartGroupState</span><span class="sxs-lookup"><span data-stu-id="b720d-101">Update-AzSmartGroupState</span></span>

## <span data-ttu-id="b720d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b720d-102">SYNOPSIS</span></span>
<span data-ttu-id="b720d-103">Обновляет состояние Smart Group</span><span class="sxs-lookup"><span data-stu-id="b720d-103">Updates smart group state</span></span>

## <span data-ttu-id="b720d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b720d-104">SYNTAX</span></span>

### <span data-ttu-id="b720d-105">BySmartGroupId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b720d-105">BySmartGroupId (Default)</span></span>
```
Update-AzSmartGroupState -SmartGroupId <String> -State <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b720d-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="b720d-106">ByInputObject</span></span>
```
Update-AzSmartGroupState -State <String> -InputObject <PSSmartGroup> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b720d-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b720d-107">DESCRIPTION</span></span>
<span data-ttu-id="b720d-108">Командлет **Update-AzSmartGroupState** обновляет состояние Smart Group.</span><span class="sxs-lookup"><span data-stu-id="b720d-108">**Update-AzSmartGroupState** cmdlet updates smart group state.</span></span>

## <span data-ttu-id="b720d-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b720d-109">EXAMPLES</span></span>

### <span data-ttu-id="b720d-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b720d-110">Example 1</span></span>
```powershell
PS C:\> Update-AzSmartGroupState -SmartGroupId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529" -State "Acknowledged"
```

<span data-ttu-id="b720d-111">Этот командлет обновляет состояние Smart Group до acknowleged.</span><span class="sxs-lookup"><span data-stu-id="b720d-111">This cmdlet updates the smart group state to Acknowleged.</span></span>

## <span data-ttu-id="b720d-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b720d-112">PARAMETERS</span></span>

### <span data-ttu-id="b720d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b720d-113">-DefaultProfile</span></span>
<span data-ttu-id="b720d-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b720d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b720d-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b720d-115">-InputObject</span></span>
<span data-ttu-id="b720d-116">Объект ввода из конвейера.</span><span class="sxs-lookup"><span data-stu-id="b720d-116">Input object from pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroup
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b720d-117">-SmartGroupId</span><span class="sxs-lookup"><span data-stu-id="b720d-117">-SmartGroupId</span></span>
<span data-ttu-id="b720d-118">Уникальный идентификатор Smart Group/ResourceId для Smart Group.</span><span class="sxs-lookup"><span data-stu-id="b720d-118">Unique Identifier of Smart Group / ResourceId of smart group.</span></span>

```yaml
Type: System.String
Parameter Sets: BySmartGroupId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b720d-119">-State</span><span class="sxs-lookup"><span data-stu-id="b720d-119">-State</span></span>
<span data-ttu-id="b720d-120">Обновлено состояние Smart Group</span><span class="sxs-lookup"><span data-stu-id="b720d-120">Updated Smart group State</span></span>

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

### <span data-ttu-id="b720d-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b720d-121">-Confirm</span></span>
<span data-ttu-id="b720d-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b720d-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b720d-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b720d-123">-WhatIf</span></span>
<span data-ttu-id="b720d-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b720d-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b720d-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b720d-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b720d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b720d-126">CommonParameters</span></span>
<span data-ttu-id="b720d-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b720d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b720d-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b720d-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b720d-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b720d-129">INPUTS</span></span>

### <span data-ttu-id="b720d-130">Ничего</span><span class="sxs-lookup"><span data-stu-id="b720d-130">None</span></span>

## <span data-ttu-id="b720d-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b720d-131">OUTPUTS</span></span>

### <span data-ttu-id="b720d-132">Microsoft. Azure. Commands. AlertsManagement. OutputModels. PSSmartGroup</span><span class="sxs-lookup"><span data-stu-id="b720d-132">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroup</span></span>

## <span data-ttu-id="b720d-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="b720d-133">NOTES</span></span>

## <span data-ttu-id="b720d-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b720d-134">RELATED LINKS</span></span>

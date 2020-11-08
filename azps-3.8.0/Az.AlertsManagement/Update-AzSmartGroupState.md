---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/update-azsmartgroupstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzSmartGroupState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzSmartGroupState.md
ms.openlocfilehash: 6c0b67bb70a364de45a88f80ca99bdec5e1d7188
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065658"
---
# <span data-ttu-id="48b23-101">Update-AzSmartGroupState</span><span class="sxs-lookup"><span data-stu-id="48b23-101">Update-AzSmartGroupState</span></span>

## <span data-ttu-id="48b23-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="48b23-102">SYNOPSIS</span></span>
<span data-ttu-id="48b23-103">Обновляет состояние Smart Group</span><span class="sxs-lookup"><span data-stu-id="48b23-103">Updates smart group state</span></span>

## <span data-ttu-id="48b23-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="48b23-104">SYNTAX</span></span>

### <span data-ttu-id="48b23-105">BySmartGroupId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="48b23-105">BySmartGroupId (Default)</span></span>
```
Update-AzSmartGroupState -SmartGroupId <String> -State <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48b23-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="48b23-106">ByInputObject</span></span>
```
Update-AzSmartGroupState -State <String> -InputObject <PSSmartGroup> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48b23-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="48b23-107">DESCRIPTION</span></span>
<span data-ttu-id="48b23-108">Командлет **Update-AzSmartGroupState** обновляет состояние Smart Group.</span><span class="sxs-lookup"><span data-stu-id="48b23-108">**Update-AzSmartGroupState** cmdlet updates smart group state.</span></span>

## <span data-ttu-id="48b23-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="48b23-109">EXAMPLES</span></span>

### <span data-ttu-id="48b23-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="48b23-110">Example 1</span></span>
```powershell
PS C:\> Update-AzSmartGroupState -SmartGroupId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529" -State "Acknowledged"
```

<span data-ttu-id="48b23-111">Этот командлет обновляет состояние Smart Group до acknowleged.</span><span class="sxs-lookup"><span data-stu-id="48b23-111">This cmdlet updates the smart group state to Acknowleged.</span></span>

## <span data-ttu-id="48b23-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="48b23-112">PARAMETERS</span></span>

### <span data-ttu-id="48b23-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48b23-113">-DefaultProfile</span></span>
<span data-ttu-id="48b23-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="48b23-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48b23-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="48b23-115">-InputObject</span></span>
<span data-ttu-id="48b23-116">Объект ввода из конвейера.</span><span class="sxs-lookup"><span data-stu-id="48b23-116">Input object from pipeline.</span></span>

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

### <span data-ttu-id="48b23-117">-SmartGroupId</span><span class="sxs-lookup"><span data-stu-id="48b23-117">-SmartGroupId</span></span>
<span data-ttu-id="48b23-118">Уникальный идентификатор Smart Group/ResourceId для Smart Group.</span><span class="sxs-lookup"><span data-stu-id="48b23-118">Unique Identifier of Smart Group / ResourceId of smart group.</span></span>

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

### <span data-ttu-id="48b23-119">-State</span><span class="sxs-lookup"><span data-stu-id="48b23-119">-State</span></span>
<span data-ttu-id="48b23-120">Обновлено состояние Smart Group</span><span class="sxs-lookup"><span data-stu-id="48b23-120">Updated Smart group State</span></span>

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

### <span data-ttu-id="48b23-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="48b23-121">-Confirm</span></span>
<span data-ttu-id="48b23-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="48b23-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48b23-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48b23-123">-WhatIf</span></span>
<span data-ttu-id="48b23-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="48b23-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="48b23-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="48b23-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48b23-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48b23-126">CommonParameters</span></span>
<span data-ttu-id="48b23-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="48b23-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48b23-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="48b23-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48b23-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="48b23-129">INPUTS</span></span>

### <span data-ttu-id="48b23-130">Ничего</span><span class="sxs-lookup"><span data-stu-id="48b23-130">None</span></span>

## <span data-ttu-id="48b23-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="48b23-131">OUTPUTS</span></span>

### <span data-ttu-id="48b23-132">Microsoft. Azure. Commands. AlertsManagement. OutputModels. PSSmartGroup</span><span class="sxs-lookup"><span data-stu-id="48b23-132">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroup</span></span>

## <span data-ttu-id="48b23-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="48b23-133">NOTES</span></span>

## <span data-ttu-id="48b23-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="48b23-134">RELATED LINKS</span></span>

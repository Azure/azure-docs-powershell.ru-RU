---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/update-azsmartgroupstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzSmartGroupState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzSmartGroupState.md
ms.openlocfilehash: 6c0b67bb70a364de45a88f80ca99bdec5e1d7188
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078024"
---
# <span data-ttu-id="0793b-101">Update-AzSmartGroupState</span><span class="sxs-lookup"><span data-stu-id="0793b-101">Update-AzSmartGroupState</span></span>

## <span data-ttu-id="0793b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0793b-102">SYNOPSIS</span></span>
<span data-ttu-id="0793b-103">Обновляет состояние Smart Group</span><span class="sxs-lookup"><span data-stu-id="0793b-103">Updates smart group state</span></span>

## <span data-ttu-id="0793b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0793b-104">SYNTAX</span></span>

### <span data-ttu-id="0793b-105">BySmartGroupId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0793b-105">BySmartGroupId (Default)</span></span>
```
Update-AzSmartGroupState -SmartGroupId <String> -State <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0793b-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="0793b-106">ByInputObject</span></span>
```
Update-AzSmartGroupState -State <String> -InputObject <PSSmartGroup> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0793b-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0793b-107">DESCRIPTION</span></span>
<span data-ttu-id="0793b-108">Командлет **Update-AzSmartGroupState** обновляет состояние Smart Group.</span><span class="sxs-lookup"><span data-stu-id="0793b-108">**Update-AzSmartGroupState** cmdlet updates smart group state.</span></span>

## <span data-ttu-id="0793b-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0793b-109">EXAMPLES</span></span>

### <span data-ttu-id="0793b-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0793b-110">Example 1</span></span>
```powershell
PS C:\> Update-AzSmartGroupState -SmartGroupId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529" -State "Acknowledged"
```

<span data-ttu-id="0793b-111">Этот командлет обновляет состояние Smart Group до acknowleged.</span><span class="sxs-lookup"><span data-stu-id="0793b-111">This cmdlet updates the smart group state to Acknowleged.</span></span>

## <span data-ttu-id="0793b-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0793b-112">PARAMETERS</span></span>

### <span data-ttu-id="0793b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0793b-113">-DefaultProfile</span></span>
<span data-ttu-id="0793b-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0793b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0793b-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0793b-115">-InputObject</span></span>
<span data-ttu-id="0793b-116">Объект ввода из конвейера.</span><span class="sxs-lookup"><span data-stu-id="0793b-116">Input object from pipeline.</span></span>

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

### <span data-ttu-id="0793b-117">-SmartGroupId</span><span class="sxs-lookup"><span data-stu-id="0793b-117">-SmartGroupId</span></span>
<span data-ttu-id="0793b-118">Уникальный идентификатор Smart Group/ResourceId для Smart Group.</span><span class="sxs-lookup"><span data-stu-id="0793b-118">Unique Identifier of Smart Group / ResourceId of smart group.</span></span>

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

### <span data-ttu-id="0793b-119">-State</span><span class="sxs-lookup"><span data-stu-id="0793b-119">-State</span></span>
<span data-ttu-id="0793b-120">Обновлено состояние Smart Group</span><span class="sxs-lookup"><span data-stu-id="0793b-120">Updated Smart group State</span></span>

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

### <span data-ttu-id="0793b-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0793b-121">-Confirm</span></span>
<span data-ttu-id="0793b-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0793b-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0793b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0793b-123">-WhatIf</span></span>
<span data-ttu-id="0793b-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0793b-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0793b-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0793b-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0793b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0793b-126">CommonParameters</span></span>
<span data-ttu-id="0793b-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0793b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0793b-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0793b-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0793b-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0793b-129">INPUTS</span></span>

### <span data-ttu-id="0793b-130">Ничего</span><span class="sxs-lookup"><span data-stu-id="0793b-130">None</span></span>

## <span data-ttu-id="0793b-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0793b-131">OUTPUTS</span></span>

### <span data-ttu-id="0793b-132">Microsoft. Azure. Commands. AlertsManagement. OutputModels. PSSmartGroup</span><span class="sxs-lookup"><span data-stu-id="0793b-132">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroup</span></span>

## <span data-ttu-id="0793b-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="0793b-133">NOTES</span></span>

## <span data-ttu-id="0793b-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0793b-134">RELATED LINKS</span></span>

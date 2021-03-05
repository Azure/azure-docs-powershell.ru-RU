---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/powershell/module/az.alertsmanagement/update-azsmartgroupstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzSmartGroupState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzSmartGroupState.md
ms.openlocfilehash: 5f7e0f26461780b30dbe2b80c79bad8231590e7d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015576"
---
# <span data-ttu-id="7b5e8-101">Update-AzSmartGroupState</span><span class="sxs-lookup"><span data-stu-id="7b5e8-101">Update-AzSmartGroupState</span></span>

## <span data-ttu-id="7b5e8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7b5e8-102">SYNOPSIS</span></span>
<span data-ttu-id="7b5e8-103">Обновления состояния смарт-группы</span><span class="sxs-lookup"><span data-stu-id="7b5e8-103">Updates smart group state</span></span>

## <span data-ttu-id="7b5e8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7b5e8-104">SYNTAX</span></span>

### <span data-ttu-id="7b5e8-105">BySmartGroupId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7b5e8-105">BySmartGroupId (Default)</span></span>
```
Update-AzSmartGroupState -SmartGroupId <String> -State <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b5e8-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="7b5e8-106">ByInputObject</span></span>
```
Update-AzSmartGroupState -State <String> -InputObject <PSSmartGroup> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7b5e8-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7b5e8-107">DESCRIPTION</span></span>
<span data-ttu-id="7b5e8-108">**Состояние смарт-группы update-AzSmartGroupState** обновляется.</span><span class="sxs-lookup"><span data-stu-id="7b5e8-108">**Update-AzSmartGroupState** cmdlet updates smart group state.</span></span>

## <span data-ttu-id="7b5e8-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7b5e8-109">EXAMPLES</span></span>

### <span data-ttu-id="7b5e8-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7b5e8-110">Example 1</span></span>
```powershell
PS C:\> Update-AzSmartGroupState -SmartGroupId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529" -State "Acknowledged"
```

<span data-ttu-id="7b5e8-111">Этот cmdlet updates the smart group state to Acknowleged.</span><span class="sxs-lookup"><span data-stu-id="7b5e8-111">This cmdlet updates the smart group state to Acknowleged.</span></span>

## <span data-ttu-id="7b5e8-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7b5e8-112">PARAMETERS</span></span>

### <span data-ttu-id="7b5e8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b5e8-113">-DefaultProfile</span></span>
<span data-ttu-id="7b5e8-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7b5e8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7b5e8-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7b5e8-115">-InputObject</span></span>
<span data-ttu-id="7b5e8-116">Входной объект из конвейера.</span><span class="sxs-lookup"><span data-stu-id="7b5e8-116">Input object from pipeline.</span></span>

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

### <span data-ttu-id="7b5e8-117">-SmartGroupId</span><span class="sxs-lookup"><span data-stu-id="7b5e8-117">-SmartGroupId</span></span>
<span data-ttu-id="7b5e8-118">Уникальный идентификатор интеллектуальной группы и идентификатора ресурса интеллектуальной группы.</span><span class="sxs-lookup"><span data-stu-id="7b5e8-118">Unique Identifier of Smart Group / ResourceId of smart group.</span></span>

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

### <span data-ttu-id="7b5e8-119">-State</span><span class="sxs-lookup"><span data-stu-id="7b5e8-119">-State</span></span>
<span data-ttu-id="7b5e8-120">Обновлено состояние группы Smart</span><span class="sxs-lookup"><span data-stu-id="7b5e8-120">Updated Smart group State</span></span>

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

### <span data-ttu-id="7b5e8-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7b5e8-121">-Confirm</span></span>
<span data-ttu-id="7b5e8-122">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7b5e8-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b5e8-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b5e8-123">-WhatIf</span></span>
<span data-ttu-id="7b5e8-124">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7b5e8-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7b5e8-125">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="7b5e8-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b5e8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b5e8-126">CommonParameters</span></span>
<span data-ttu-id="7b5e8-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b5e8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b5e8-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7b5e8-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b5e8-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7b5e8-129">INPUTS</span></span>

### <span data-ttu-id="7b5e8-130">Нет</span><span class="sxs-lookup"><span data-stu-id="7b5e8-130">None</span></span>

## <span data-ttu-id="7b5e8-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7b5e8-131">OUTPUTS</span></span>

### <span data-ttu-id="7b5e8-132">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroup</span><span class="sxs-lookup"><span data-stu-id="7b5e8-132">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroup</span></span>

## <span data-ttu-id="7b5e8-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7b5e8-133">NOTES</span></span>

## <span data-ttu-id="7b5e8-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7b5e8-134">RELATED LINKS</span></span>

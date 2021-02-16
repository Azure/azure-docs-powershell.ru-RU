---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/update-azsmartgroupstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzSmartGroupState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzSmartGroupState.md
ms.openlocfilehash: 6c0b67bb70a364de45a88f80ca99bdec5e1d7188
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100233844"
---
# <span data-ttu-id="ad687-101">Update-AzSmartGroupState</span><span class="sxs-lookup"><span data-stu-id="ad687-101">Update-AzSmartGroupState</span></span>

## <span data-ttu-id="ad687-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad687-102">SYNOPSIS</span></span>
<span data-ttu-id="ad687-103">Обновления состояния группы Smart Group</span><span class="sxs-lookup"><span data-stu-id="ad687-103">Updates smart group state</span></span>

## <span data-ttu-id="ad687-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ad687-104">SYNTAX</span></span>

### <span data-ttu-id="ad687-105">BySmartGroupId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ad687-105">BySmartGroupId (Default)</span></span>
```
Update-AzSmartGroupState -SmartGroupId <String> -State <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad687-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="ad687-106">ByInputObject</span></span>
```
Update-AzSmartGroupState -State <String> -InputObject <PSSmartGroup> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad687-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ad687-107">DESCRIPTION</span></span>
<span data-ttu-id="ad687-108">**Состояние смарт-группы update-AzSmartGroupState** обновляется.</span><span class="sxs-lookup"><span data-stu-id="ad687-108">**Update-AzSmartGroupState** cmdlet updates smart group state.</span></span>

## <span data-ttu-id="ad687-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ad687-109">EXAMPLES</span></span>

### <span data-ttu-id="ad687-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ad687-110">Example 1</span></span>
```powershell
PS C:\> Update-AzSmartGroupState -SmartGroupId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529" -State "Acknowledged"
```

<span data-ttu-id="ad687-111">Этот cmdlet updates the smart group state to Acknowleged.</span><span class="sxs-lookup"><span data-stu-id="ad687-111">This cmdlet updates the smart group state to Acknowleged.</span></span>

## <span data-ttu-id="ad687-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ad687-112">PARAMETERS</span></span>

### <span data-ttu-id="ad687-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad687-113">-DefaultProfile</span></span>
<span data-ttu-id="ad687-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ad687-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad687-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ad687-115">-InputObject</span></span>
<span data-ttu-id="ad687-116">Входной объект из конвейера.</span><span class="sxs-lookup"><span data-stu-id="ad687-116">Input object from pipeline.</span></span>

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

### <span data-ttu-id="ad687-117">-SmartGroupId</span><span class="sxs-lookup"><span data-stu-id="ad687-117">-SmartGroupId</span></span>
<span data-ttu-id="ad687-118">Уникальный идентификатор интеллектуальной группы и идентификатора ресурса интеллектуальной группы.</span><span class="sxs-lookup"><span data-stu-id="ad687-118">Unique Identifier of Smart Group / ResourceId of smart group.</span></span>

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

### <span data-ttu-id="ad687-119">-State</span><span class="sxs-lookup"><span data-stu-id="ad687-119">-State</span></span>
<span data-ttu-id="ad687-120">Обновлено состояние группы Smart</span><span class="sxs-lookup"><span data-stu-id="ad687-120">Updated Smart group State</span></span>

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

### <span data-ttu-id="ad687-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ad687-121">-Confirm</span></span>
<span data-ttu-id="ad687-122">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad687-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad687-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad687-123">-WhatIf</span></span>
<span data-ttu-id="ad687-124">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad687-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad687-125">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ad687-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad687-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad687-126">CommonParameters</span></span>
<span data-ttu-id="ad687-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad687-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad687-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ad687-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad687-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ad687-129">INPUTS</span></span>

### <span data-ttu-id="ad687-130">Нет</span><span class="sxs-lookup"><span data-stu-id="ad687-130">None</span></span>

## <span data-ttu-id="ad687-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ad687-131">OUTPUTS</span></span>

### <span data-ttu-id="ad687-132">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroup</span><span class="sxs-lookup"><span data-stu-id="ad687-132">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroup</span></span>

## <span data-ttu-id="ad687-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ad687-133">NOTES</span></span>

## <span data-ttu-id="ad687-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ad687-134">RELATED LINKS</span></span>

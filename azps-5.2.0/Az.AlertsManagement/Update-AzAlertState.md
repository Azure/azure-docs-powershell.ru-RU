---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/update-azalertstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzAlertState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzAlertState.md
ms.openlocfilehash: 4ba238f75fa1e39daf2309a1ceda1aed323ff47d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98327798"
---
# <span data-ttu-id="23abc-101">Update-AzAlertState</span><span class="sxs-lookup"><span data-stu-id="23abc-101">Update-AzAlertState</span></span>

## <span data-ttu-id="23abc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23abc-102">SYNOPSIS</span></span>
<span data-ttu-id="23abc-103">Состояние оповещений об обновлениях</span><span class="sxs-lookup"><span data-stu-id="23abc-103">Updates alert state</span></span>

## <span data-ttu-id="23abc-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="23abc-104">SYNTAX</span></span>

### <span data-ttu-id="23abc-105">ByAlertId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="23abc-105">ByAlertId (Default)</span></span>
```
Update-AzAlertState -AlertId <String> -State <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23abc-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="23abc-106">ByInputObject</span></span>
```
Update-AzAlertState -State <String> -InputObject <PSAlert> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23abc-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="23abc-107">DESCRIPTION</span></span>
<span data-ttu-id="23abc-108">**Update-AzAlertState** обновляет состояние оповещений.</span><span class="sxs-lookup"><span data-stu-id="23abc-108">**Update-AzAlertState** cmdlet updates alert state.</span></span>

## <span data-ttu-id="23abc-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="23abc-109">EXAMPLES</span></span>

### <span data-ttu-id="23abc-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="23abc-110">Example 1</span></span>
```powershell
PS C:\> Update-AzAlertState -AlertId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529" -State "Closed"
```

<span data-ttu-id="23abc-111">Этот cmdlet обновляет состояние оповещения на "Закрыто".</span><span class="sxs-lookup"><span data-stu-id="23abc-111">This cmdlet updates the alert state to Closed.</span></span>

## <span data-ttu-id="23abc-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="23abc-112">PARAMETERS</span></span>

### <span data-ttu-id="23abc-113">-AlertId</span><span class="sxs-lookup"><span data-stu-id="23abc-113">-AlertId</span></span>
<span data-ttu-id="23abc-114">Уникальный идентификатор оповещения и идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="23abc-114">Unique Identifier of Alert / ResourceId of alert.</span></span>

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

### <span data-ttu-id="23abc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23abc-115">-DefaultProfile</span></span>
<span data-ttu-id="23abc-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="23abc-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23abc-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="23abc-117">-InputObject</span></span>
<span data-ttu-id="23abc-118">Входной объект из конвейера.</span><span class="sxs-lookup"><span data-stu-id="23abc-118">Input object from pipeline.</span></span>

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

### <span data-ttu-id="23abc-119">-State</span><span class="sxs-lookup"><span data-stu-id="23abc-119">-State</span></span>
<span data-ttu-id="23abc-120">Обновлено состояние оповещения</span><span class="sxs-lookup"><span data-stu-id="23abc-120">Updated Alert State</span></span>

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

### <span data-ttu-id="23abc-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="23abc-121">-Confirm</span></span>
<span data-ttu-id="23abc-122">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23abc-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23abc-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23abc-123">-WhatIf</span></span>
<span data-ttu-id="23abc-124">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23abc-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23abc-125">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="23abc-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23abc-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23abc-126">CommonParameters</span></span>
<span data-ttu-id="23abc-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23abc-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23abc-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="23abc-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23abc-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="23abc-129">INPUTS</span></span>

### <span data-ttu-id="23abc-130">Нет</span><span class="sxs-lookup"><span data-stu-id="23abc-130">None</span></span>

## <span data-ttu-id="23abc-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="23abc-131">OUTPUTS</span></span>

### <span data-ttu-id="23abc-132">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlert</span><span class="sxs-lookup"><span data-stu-id="23abc-132">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlert</span></span>

## <span data-ttu-id="23abc-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="23abc-133">NOTES</span></span>

## <span data-ttu-id="23abc-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="23abc-134">RELATED LINKS</span></span>

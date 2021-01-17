---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: C7EC21C7-1C7E-49B2-9B33-486532FCDAEC
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzAlertRule.md
ms.openlocfilehash: 23b4c81e7c999301ccb535435911a9413ae4ef16
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98425455"
---
# <span data-ttu-id="b5a81-101">Remove-AzAlertRule</span><span class="sxs-lookup"><span data-stu-id="b5a81-101">Remove-AzAlertRule</span></span>

## <span data-ttu-id="b5a81-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5a81-102">SYNOPSIS</span></span>
<span data-ttu-id="b5a81-103">Удаляет правило оповещения.</span><span class="sxs-lookup"><span data-stu-id="b5a81-103">Removes an alert rule.</span></span>

## <span data-ttu-id="b5a81-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b5a81-104">SYNTAX</span></span>

```
Remove-AzAlertRule -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5a81-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b5a81-105">DESCRIPTION</span></span>
<span data-ttu-id="b5a81-106">Для **удаления правила оповещения удаляется cmdlet Remove-AzAlertRule.**</span><span class="sxs-lookup"><span data-stu-id="b5a81-106">The **Remove-AzAlertRule** cmdlet removes an alert rule.</span></span>
<span data-ttu-id="b5a81-107">Необходимо указать имя правила оповещения и группу ресурсов, которой оно назначено.</span><span class="sxs-lookup"><span data-stu-id="b5a81-107">You must specify the name of the alert rule and the resource group to which it is assigned.</span></span>
<span data-ttu-id="b5a81-108">Этот cmdlet реализует шаблон ShouldProcess, то есть может запросить подтверждение у пользователя перед фактическим созданием, изменением или удалением ресурса.</span><span class="sxs-lookup"><span data-stu-id="b5a81-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="b5a81-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b5a81-109">EXAMPLES</span></span>

### <span data-ttu-id="b5a81-110">Пример 1. Удаление правила оповещения</span><span class="sxs-lookup"><span data-stu-id="b5a81-110">Example 1: Remove an alert rule</span></span>
```
PS C:\>Remove-AzAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

<span data-ttu-id="b5a81-111">Эта команда удаляет правило оповещения myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8 в группе ресурсов Default-Web-CentralUS.</span><span class="sxs-lookup"><span data-stu-id="b5a81-111">This command removes the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8 in the resource group Default-Web-CentralUS.</span></span>

## <span data-ttu-id="b5a81-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b5a81-112">PARAMETERS</span></span>

### <span data-ttu-id="b5a81-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5a81-113">-DefaultProfile</span></span>
<span data-ttu-id="b5a81-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="b5a81-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b5a81-115">-Name</span><span class="sxs-lookup"><span data-stu-id="b5a81-115">-Name</span></span>
<span data-ttu-id="b5a81-116">Указывает имя правила оповещения, которое нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="b5a81-116">Specifies the name of the alert rule to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5a81-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5a81-117">-ResourceGroupName</span></span>
<span data-ttu-id="b5a81-118">Имя группы ресурсов для правила оповещения.</span><span class="sxs-lookup"><span data-stu-id="b5a81-118">Specifies the name of the resource group for the alert rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5a81-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b5a81-119">-Confirm</span></span>
<span data-ttu-id="b5a81-120">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b5a81-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5a81-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5a81-121">-WhatIf</span></span>
<span data-ttu-id="b5a81-122">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b5a81-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b5a81-123">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="b5a81-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5a81-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5a81-124">CommonParameters</span></span>
<span data-ttu-id="b5a81-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5a81-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5a81-126">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b5a81-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5a81-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b5a81-127">INPUTS</span></span>

### <span data-ttu-id="b5a81-128">System.String</span><span class="sxs-lookup"><span data-stu-id="b5a81-128">System.String</span></span>

## <span data-ttu-id="b5a81-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b5a81-129">OUTPUTS</span></span>

### <span data-ttu-id="b5a81-130">Microsoft.Azure.AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="b5a81-130">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="b5a81-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b5a81-131">NOTES</span></span>

## <span data-ttu-id="b5a81-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b5a81-132">RELATED LINKS</span></span>

[<span data-ttu-id="b5a81-133">Add-AzMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="b5a81-133">Add-AzMetricAlertRule</span></span>](./Add-AzMetricAlertRule.md)

[<span data-ttu-id="b5a81-134">Add-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="b5a81-134">Add-AzWebtestAlertRule</span></span>](./Add-AzWebtestAlertRule.md)

[<span data-ttu-id="b5a81-135">Get-AzAlertHistory</span><span class="sxs-lookup"><span data-stu-id="b5a81-135">Get-AzAlertHistory</span></span>](./Get-AzAlertHistory.md)

[<span data-ttu-id="b5a81-136">Get-AzAlertRule</span><span class="sxs-lookup"><span data-stu-id="b5a81-136">Get-AzAlertRule</span></span>](./Get-AzAlertRule.md)



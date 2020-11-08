---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: C7EC21C7-1C7E-49B2-9B33-486532FCDAEC
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzAlertRule.md
ms.openlocfilehash: 23b4c81e7c999301ccb535435911a9413ae4ef16
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078982"
---
# <span data-ttu-id="b9dce-101">Remove-AzAlertRule</span><span class="sxs-lookup"><span data-stu-id="b9dce-101">Remove-AzAlertRule</span></span>

## <span data-ttu-id="b9dce-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b9dce-102">SYNOPSIS</span></span>
<span data-ttu-id="b9dce-103">Удаление правила оповещения.</span><span class="sxs-lookup"><span data-stu-id="b9dce-103">Removes an alert rule.</span></span>

## <span data-ttu-id="b9dce-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b9dce-104">SYNTAX</span></span>

```
Remove-AzAlertRule -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9dce-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b9dce-105">DESCRIPTION</span></span>
<span data-ttu-id="b9dce-106">Командлет **Remove-AzAlertRule** удаляет правило оповещения.</span><span class="sxs-lookup"><span data-stu-id="b9dce-106">The **Remove-AzAlertRule** cmdlet removes an alert rule.</span></span>
<span data-ttu-id="b9dce-107">Вы должны указать имя правила оповещения и группу ресурсов, которому она назначена.</span><span class="sxs-lookup"><span data-stu-id="b9dce-107">You must specify the name of the alert rule and the resource group to which it is assigned.</span></span>
<span data-ttu-id="b9dce-108">Этот командлет реализует шаблон ShouldProcess, т. е. может запросить подтверждение от пользователя, прежде чем действительно создать, изменить или удалить ресурс.</span><span class="sxs-lookup"><span data-stu-id="b9dce-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="b9dce-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b9dce-109">EXAMPLES</span></span>

### <span data-ttu-id="b9dce-110">Пример 1: Удаление правила оповещения</span><span class="sxs-lookup"><span data-stu-id="b9dce-110">Example 1: Remove an alert rule</span></span>
```
PS C:\>Remove-AzAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

<span data-ttu-id="b9dce-111">Эта команда удаляет правило оповещения с именем myAlert-7da64548-214d-42ca-b12b-b245bb8f0ac8 в группе ресурсов Default-Web-CentralUS.</span><span class="sxs-lookup"><span data-stu-id="b9dce-111">This command removes the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8 in the resource group Default-Web-CentralUS.</span></span>

## <span data-ttu-id="b9dce-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b9dce-112">PARAMETERS</span></span>

### <span data-ttu-id="b9dce-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9dce-113">-DefaultProfile</span></span>
<span data-ttu-id="b9dce-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="b9dce-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b9dce-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b9dce-115">-Name</span></span>
<span data-ttu-id="b9dce-116">Указывает имя удаляемого правила оповещения.</span><span class="sxs-lookup"><span data-stu-id="b9dce-116">Specifies the name of the alert rule to remove.</span></span>

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

### <span data-ttu-id="b9dce-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9dce-117">-ResourceGroupName</span></span>
<span data-ttu-id="b9dce-118">Указывает имя группы ресурсов для правила оповещения.</span><span class="sxs-lookup"><span data-stu-id="b9dce-118">Specifies the name of the resource group for the alert rule.</span></span>

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

### <span data-ttu-id="b9dce-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b9dce-119">-Confirm</span></span>
<span data-ttu-id="b9dce-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b9dce-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9dce-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9dce-121">-WhatIf</span></span>
<span data-ttu-id="b9dce-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b9dce-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b9dce-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b9dce-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9dce-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9dce-124">CommonParameters</span></span>
<span data-ttu-id="b9dce-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b9dce-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9dce-126">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b9dce-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9dce-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b9dce-127">INPUTS</span></span>

### <span data-ttu-id="b9dce-128">System. String</span><span class="sxs-lookup"><span data-stu-id="b9dce-128">System.String</span></span>

## <span data-ttu-id="b9dce-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b9dce-129">OUTPUTS</span></span>

### <span data-ttu-id="b9dce-130">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="b9dce-130">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="b9dce-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="b9dce-131">NOTES</span></span>

## <span data-ttu-id="b9dce-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b9dce-132">RELATED LINKS</span></span>

[<span data-ttu-id="b9dce-133">Add-AzMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="b9dce-133">Add-AzMetricAlertRule</span></span>](./Add-AzMetricAlertRule.md)

[<span data-ttu-id="b9dce-134">Add-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="b9dce-134">Add-AzWebtestAlertRule</span></span>](./Add-AzWebtestAlertRule.md)

[<span data-ttu-id="b9dce-135">Get-AzAlertHistory</span><span class="sxs-lookup"><span data-stu-id="b9dce-135">Get-AzAlertHistory</span></span>](./Get-AzAlertHistory.md)

[<span data-ttu-id="b9dce-136">Get-AzAlertRule</span><span class="sxs-lookup"><span data-stu-id="b9dce-136">Get-AzAlertRule</span></span>](./Get-AzAlertRule.md)



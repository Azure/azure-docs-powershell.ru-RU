---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 0C35E679-B991-49A8-890F-C8DAB68A8240
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: 9758c0dda8d392100e57909edca310f14d3746af
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/13/2020
ms.locfileid: "93731925"
---
# <span data-ttu-id="47f5a-101">Remove-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="47f5a-101">Remove-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="47f5a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="47f5a-102">SYNOPSIS</span></span>
<span data-ttu-id="47f5a-103">Удаление рабочей области.</span><span class="sxs-lookup"><span data-stu-id="47f5a-103">Removes a workspace.</span></span>

## <span data-ttu-id="47f5a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="47f5a-104">SYNTAX</span></span>

```
Remove-AzOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47f5a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="47f5a-105">DESCRIPTION</span></span>
<span data-ttu-id="47f5a-106">Командлет **Remove-AzOperationalInsightsWorkspace** удаляет существующую рабочую область.</span><span class="sxs-lookup"><span data-stu-id="47f5a-106">The **Remove-AzOperationalInsightsWorkspace** cmdlet deletes an existing workspace.</span></span>
<span data-ttu-id="47f5a-107">Если эта Рабочая область была связана с существующей учетной записью с помощью параметра *CustomerID* на этапе создания, исходная учетная запись не будет удалена на портале оперативной аналитики.</span><span class="sxs-lookup"><span data-stu-id="47f5a-107">If this workspace was linked to an existing account via the *CustomerId* parameter at creation time the original account is not deleted in the Operational Insights portal.</span></span>

## <span data-ttu-id="47f5a-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="47f5a-108">EXAMPLES</span></span>

### <span data-ttu-id="47f5a-109">Пример 1: Удаление рабочей области по имени</span><span class="sxs-lookup"><span data-stu-id="47f5a-109">Example 1: Remove a workspace by name</span></span>
```
PS C:\>Remove-AzOperationalInsightsWorkspace -ResourceGroupName "ContosResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="47f5a-110">Эта команда удаляет рабочую область с именем MyWorkspace из группы ресурсов с именем ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="47f5a-110">This command removes the workspace named MyWorkspace from the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="47f5a-111">Пример 2: Удаление рабочей области с помощью конвейера и без подтверждения</span><span class="sxs-lookup"><span data-stu-id="47f5a-111">Example 2: Remove a workspace by using the pipeline and without confirmation</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosResourceGroup" -Name "MyWorkspace" | Remove-AzOperationalInsightsWorkspace -Force
```

<span data-ttu-id="47f5a-112">Эта команда использует командлет Get-AzOperationalInsightsWorkspace, чтобы получить рабочую область с именем MyWorkspace, а затем передает ее командлету **Remove-AzOperationalInsightsWorkspace** с помощью оператора конвейера, чтобы удалить его.</span><span class="sxs-lookup"><span data-stu-id="47f5a-112">This command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then passes it to the **Remove-AzOperationalInsightsWorkspace** cmdlet by using the pipeline operator to remove it.</span></span>
<span data-ttu-id="47f5a-113">Так как параметр *Force* задан, команда не выдает запрос перед удалением рабочей области.</span><span class="sxs-lookup"><span data-stu-id="47f5a-113">Since the *Force* parameter is specified, the command does not prompt you before removing the workspace.</span></span>

## <span data-ttu-id="47f5a-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="47f5a-114">PARAMETERS</span></span>

### <span data-ttu-id="47f5a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47f5a-115">-DefaultProfile</span></span>
<span data-ttu-id="47f5a-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="47f5a-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="47f5a-117">-Force</span><span class="sxs-lookup"><span data-stu-id="47f5a-117">-Force</span></span>
<span data-ttu-id="47f5a-118">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="47f5a-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47f5a-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="47f5a-119">-Name</span></span>
<span data-ttu-id="47f5a-120">Указывает имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="47f5a-120">Specifies the name of the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47f5a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47f5a-121">-ResourceGroupName</span></span>
<span data-ttu-id="47f5a-122">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="47f5a-122">Specifies the name of an Azure resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47f5a-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="47f5a-123">-Confirm</span></span>
<span data-ttu-id="47f5a-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="47f5a-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47f5a-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47f5a-125">-WhatIf</span></span>
<span data-ttu-id="47f5a-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="47f5a-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47f5a-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="47f5a-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47f5a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47f5a-128">CommonParameters</span></span>
<span data-ttu-id="47f5a-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="47f5a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47f5a-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47f5a-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47f5a-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="47f5a-131">INPUTS</span></span>

### <span data-ttu-id="47f5a-132">System. String</span><span class="sxs-lookup"><span data-stu-id="47f5a-132">System.String</span></span>

## <span data-ttu-id="47f5a-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="47f5a-133">OUTPUTS</span></span>

### <span data-ttu-id="47f5a-134">System. void</span><span class="sxs-lookup"><span data-stu-id="47f5a-134">System.Void</span></span>

## <span data-ttu-id="47f5a-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="47f5a-135">NOTES</span></span>

## <span data-ttu-id="47f5a-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="47f5a-136">RELATED LINKS</span></span>

[<span data-ttu-id="47f5a-137">Командлеты оперативной аналитики Azure</span><span class="sxs-lookup"><span data-stu-id="47f5a-137">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)

[<span data-ttu-id="47f5a-138">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="47f5a-138">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)



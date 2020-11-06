---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 0C35E679-B991-49A8-890F-C8DAB68A8240
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/remove-azurermoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsWorkspace.md
ms.openlocfilehash: 5a222b404aa931cec468ee5dfc66963f48b23ada
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558391"
---
# <span data-ttu-id="05a4b-101">Remove-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="05a4b-101">Remove-AzureRmOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="05a4b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="05a4b-102">SYNOPSIS</span></span>
<span data-ttu-id="05a4b-103">Удаление рабочей области.</span><span class="sxs-lookup"><span data-stu-id="05a4b-103">Removes a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="05a4b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="05a4b-104">SYNTAX</span></span>

```
Remove-AzureRmOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05a4b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="05a4b-105">DESCRIPTION</span></span>
<span data-ttu-id="05a4b-106">Командлет **Remove-AzureRmOperationalInsightsWorkspace** удаляет существующую рабочую область.</span><span class="sxs-lookup"><span data-stu-id="05a4b-106">The **Remove-AzureRmOperationalInsightsWorkspace** cmdlet deletes an existing workspace.</span></span>
<span data-ttu-id="05a4b-107">Если эта Рабочая область была связана с существующей учетной записью с помощью параметра *CustomerID* на этапе создания, исходная учетная запись не будет удалена на портале оперативной аналитики.</span><span class="sxs-lookup"><span data-stu-id="05a4b-107">If this workspace was linked to an existing account via the *CustomerId* parameter at creation time the original account is not deleted in the Operational Insights portal.</span></span>

## <span data-ttu-id="05a4b-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="05a4b-108">EXAMPLES</span></span>

### <span data-ttu-id="05a4b-109">Пример 1: Удаление рабочей области по имени</span><span class="sxs-lookup"><span data-stu-id="05a4b-109">Example 1: Remove a workspace by name</span></span>
```
PS C:\>Remove-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="05a4b-110">Эта команда удаляет рабочую область с именем MyWorkspace из группы ресурсов с именем ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="05a4b-110">This command removes the workspace named MyWorkspace from the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="05a4b-111">Пример 2: Удаление рабочей области с помощью конвейера и без подтверждения</span><span class="sxs-lookup"><span data-stu-id="05a4b-111">Example 2: Remove a workspace by using the pipeline and without confirmation</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosResourceGroup" -Name "MyWorkspace" | Remove-AzureRmOperationalInsightsWorkspace -Force
```

<span data-ttu-id="05a4b-112">Эта команда использует командлет Get-AzureRmOperationalInsightsWorkspace, чтобы получить рабочую область с именем MyWorkspace, а затем передает ее командлету **Remove-AzureRmOperationalInsightsWorkspace** с помощью оператора конвейера, чтобы удалить его.</span><span class="sxs-lookup"><span data-stu-id="05a4b-112">This command uses the Get-AzureRmOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then passes it to the **Remove-AzureRmOperationalInsightsWorkspace** cmdlet by using the pipeline operator to remove it.</span></span>
<span data-ttu-id="05a4b-113">Так как параметр *Force* задан, команда не выдает запрос перед удалением рабочей области.</span><span class="sxs-lookup"><span data-stu-id="05a4b-113">Since the *Force* parameter is specified, the command does not prompt you before removing the workspace.</span></span>

## <span data-ttu-id="05a4b-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="05a4b-114">PARAMETERS</span></span>

### <span data-ttu-id="05a4b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05a4b-115">-DefaultProfile</span></span>
<span data-ttu-id="05a4b-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="05a4b-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05a4b-117">-Force</span><span class="sxs-lookup"><span data-stu-id="05a4b-117">-Force</span></span>
<span data-ttu-id="05a4b-118">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="05a4b-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="05a4b-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="05a4b-119">-Name</span></span>
<span data-ttu-id="05a4b-120">Указывает имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="05a4b-120">Specifies the name of the workspace.</span></span>

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

### <span data-ttu-id="05a4b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05a4b-121">-ResourceGroupName</span></span>
<span data-ttu-id="05a4b-122">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="05a4b-122">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="05a4b-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="05a4b-123">-Confirm</span></span>
<span data-ttu-id="05a4b-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="05a4b-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05a4b-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05a4b-125">-WhatIf</span></span>
<span data-ttu-id="05a4b-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="05a4b-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05a4b-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="05a4b-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05a4b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05a4b-128">CommonParameters</span></span>
<span data-ttu-id="05a4b-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="05a4b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05a4b-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05a4b-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05a4b-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="05a4b-131">INPUTS</span></span>

### <span data-ttu-id="05a4b-132">System. String</span><span class="sxs-lookup"><span data-stu-id="05a4b-132">System.String</span></span>

## <span data-ttu-id="05a4b-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="05a4b-133">OUTPUTS</span></span>

### <span data-ttu-id="05a4b-134">System. void</span><span class="sxs-lookup"><span data-stu-id="05a4b-134">System.Void</span></span>

## <span data-ttu-id="05a4b-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="05a4b-135">NOTES</span></span>

## <span data-ttu-id="05a4b-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="05a4b-136">RELATED LINKS</span></span>

[<span data-ttu-id="05a4b-137">Командлеты оперативной аналитики Azure</span><span class="sxs-lookup"><span data-stu-id="05a4b-137">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="05a4b-138">Get-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="05a4b-138">Get-AzureRmOperationalInsightsWorkspace</span></span>](./Get-AzureRmOperationalInsightsWorkspace.md)



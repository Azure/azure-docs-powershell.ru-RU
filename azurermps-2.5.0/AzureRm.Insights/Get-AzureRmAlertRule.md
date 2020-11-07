---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: A837077C-0A79-431C-93D2-799B2134EE69
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermalertrule
schema: 2.0.0
ms.openlocfilehash: fe763bcf6ff4aeeeedb3ff0dcb0c2ebd5c4b45cc
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93915294"
---
# <span data-ttu-id="4ac55-101">Get-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="4ac55-101">Get-AzureRmAlertRule</span></span>

## <span data-ttu-id="4ac55-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4ac55-102">SYNOPSIS</span></span>
<span data-ttu-id="4ac55-103">Возвращает правила оповещения.</span><span class="sxs-lookup"><span data-stu-id="4ac55-103">Gets alert rules.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4ac55-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4ac55-104">SYNTAX</span></span>

### <span data-ttu-id="4ac55-105">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4ac55-105">GetByResourceGroup</span></span>
```
Get-AzureRmAlertRule -ResourceGroupName <String> [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4ac55-106">GetByName</span><span class="sxs-lookup"><span data-stu-id="4ac55-106">GetByName</span></span>
```
Get-AzureRmAlertRule -ResourceGroupName <String> -Name <String> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4ac55-107">GetByResourceUri</span><span class="sxs-lookup"><span data-stu-id="4ac55-107">GetByResourceUri</span></span>
```
Get-AzureRmAlertRule -ResourceGroupName <String> -TargetResourceId <String> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ac55-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4ac55-108">DESCRIPTION</span></span>
<span data-ttu-id="4ac55-109">Командлет **Get-AzureRmAlertRule** получает правило оповещения по имени или URI-адресу или ко всем правилам оповещений из определенной группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4ac55-109">The **Get-AzureRmAlertRule** cmdlet gets an alert rule by its name or URI, or all alert rules from a specified resource group.</span></span>

## <span data-ttu-id="4ac55-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4ac55-110">EXAMPLES</span></span>

### <span data-ttu-id="4ac55-111">Пример 1: получение правил оповещения для группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="4ac55-111">Example 1: Get alert rules for a resource group</span></span>
```
PS C:\>Get-AzureRmAlertRule -ResourceGroup "Default-Web-CentralUS"
```

<span data-ttu-id="4ac55-112">Эта команда получает все правила оповещения для группы ресурсов по умолчанию — Web-CentralUS.</span><span class="sxs-lookup"><span data-stu-id="4ac55-112">This command gets all of the alert rules for the resource group named Default-Web-CentralUS.</span></span>
<span data-ttu-id="4ac55-113">Выходные данные не содержат сведений о правилах, так как параметр *DetailedOutput* не указан.</span><span class="sxs-lookup"><span data-stu-id="4ac55-113">The output does not contain details about the rules because the *DetailedOutput* parameter is not specified.</span></span>

### <span data-ttu-id="4ac55-114">Пример 2: получение правила оповещения по имени</span><span class="sxs-lookup"><span data-stu-id="4ac55-114">Example 2: Get an alert rule by name</span></span>
```
PS C:\>Get-AzureRmAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8"
```

<span data-ttu-id="4ac55-115">Эта команда возвращает правило оповещения с именем myAlert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span><span class="sxs-lookup"><span data-stu-id="4ac55-115">This command gets the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span></span>
<span data-ttu-id="4ac55-116">Так как параметр *DetailedOutput* не указан, в выходных данных содержатся только основные сведения о правиле оповещения.</span><span class="sxs-lookup"><span data-stu-id="4ac55-116">Because the *DetailedOutput* parameter is not specified, the output contains only basic information about the alert rule.</span></span>

### <span data-ttu-id="4ac55-117">Пример 3: получение правила оповещения по имени с подробным выводом</span><span class="sxs-lookup"><span data-stu-id="4ac55-117">Example 3: Get an alert rule by name with detailed output</span></span>
```
PS C:\>Get-AzureRmAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8" -DetailedOutput
```

<span data-ttu-id="4ac55-118">Эта команда возвращает правило оповещения с именем myAlert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span><span class="sxs-lookup"><span data-stu-id="4ac55-118">This command gets the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span></span>
<span data-ttu-id="4ac55-119">Указан параметр *DetailedOutput* , поэтому выходные данные подробно описаны.</span><span class="sxs-lookup"><span data-stu-id="4ac55-119">The *DetailedOutput* parameter is specified, so the output is detailed.</span></span>

## <span data-ttu-id="4ac55-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4ac55-120">PARAMETERS</span></span>

### <span data-ttu-id="4ac55-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ac55-121">-DefaultProfile</span></span>
<span data-ttu-id="4ac55-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="4ac55-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4ac55-123">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="4ac55-123">-DetailedOutput</span></span>
<span data-ttu-id="4ac55-124">Отображение подробных сведений в выходных данных.</span><span class="sxs-lookup"><span data-stu-id="4ac55-124">Displays full details in the output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ac55-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4ac55-125">-Name</span></span>
<span data-ttu-id="4ac55-126">Указывает имя правила оповещения, которое требуется получить.</span><span class="sxs-lookup"><span data-stu-id="4ac55-126">Specifies the name of the alert rule to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ac55-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ac55-127">-ResourceGroupName</span></span>
<span data-ttu-id="4ac55-128">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4ac55-128">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="4ac55-129">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="4ac55-129">-TargetResourceId</span></span>
<span data-ttu-id="4ac55-130">Указывает идентификатор целевого ресурса.</span><span class="sxs-lookup"><span data-stu-id="4ac55-130">Specifies the ID of the target resource.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ac55-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ac55-131">CommonParameters</span></span>
<span data-ttu-id="4ac55-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4ac55-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ac55-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ac55-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ac55-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4ac55-134">INPUTS</span></span>

### <span data-ttu-id="4ac55-135">System. String</span><span class="sxs-lookup"><span data-stu-id="4ac55-135">System.String</span></span>

### <span data-ttu-id="4ac55-136">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="4ac55-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="4ac55-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4ac55-137">OUTPUTS</span></span>

### <span data-ttu-id="4ac55-138">Microsoft. Azure. Commands. Insights. OutputClasses. PSAlertRule</span><span class="sxs-lookup"><span data-stu-id="4ac55-138">Microsoft.Azure.Commands.Insights.OutputClasses.PSAlertRule</span></span>

## <span data-ttu-id="4ac55-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="4ac55-139">NOTES</span></span>

## <span data-ttu-id="4ac55-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4ac55-140">RELATED LINKS</span></span>



[<span data-ttu-id="4ac55-141">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="4ac55-141">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="4ac55-142">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="4ac55-142">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="4ac55-143">Get-AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="4ac55-143">Get-AzureRmAlertHistory</span></span>](./Get-AzureRmAlertHistory.md)

[<span data-ttu-id="4ac55-144">Remove-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="4ac55-144">Remove-AzureRmAlertRule</span></span>](./Remove-AzureRmAlertRule.md)



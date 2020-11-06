---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: A837077C-0A79-431C-93D2-799B2134EE69
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmAlertRule.md
ms.openlocfilehash: 65c5bc7a2767fd00497b487783c4e6f0ce6d6723
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569396"
---
# <span data-ttu-id="b980d-101">Get-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="b980d-101">Get-AzureRmAlertRule</span></span>

## <span data-ttu-id="b980d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b980d-102">SYNOPSIS</span></span>
<span data-ttu-id="b980d-103">Возвращает правила оповещения.</span><span class="sxs-lookup"><span data-stu-id="b980d-103">Gets alert rules.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b980d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b980d-104">SYNTAX</span></span>

### <span data-ttu-id="b980d-105">Параметры для Get-AzureRmAlertRule командлета</span><span class="sxs-lookup"><span data-stu-id="b980d-105">Parameters for Get-AzureRmAlertRule cmdlet</span></span>
```
Get-AzureRmAlertRule -ResourceGroup <String> [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b980d-106">Параметры командлета Get-AzureRmAlertRule с помощью имени</span><span class="sxs-lookup"><span data-stu-id="b980d-106">Parameters for Get-AzureRmAlertRule cmdlet using name</span></span>
```
Get-AzureRmAlertRule -ResourceGroup <String> -Name <String> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b980d-107">Параметры командлета Get-AzureRmAlertRule с помощью URI целевого ресурса</span><span class="sxs-lookup"><span data-stu-id="b980d-107">Parameters for Get-AzureRmAlertRule cmdlet using target resource uri</span></span>
```
Get-AzureRmAlertRule -ResourceGroup <String> -TargetResourceId <String> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b980d-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b980d-108">DESCRIPTION</span></span>
<span data-ttu-id="b980d-109">Командлет **Get-AzureRmAlertRule** получает правило оповещения по имени или URI-адресу или ко всем правилам оповещений из определенной группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b980d-109">The **Get-AzureRmAlertRule** cmdlet gets an alert rule by its name or URI, or all alert rules from a specified resource group.</span></span>

## <span data-ttu-id="b980d-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b980d-110">EXAMPLES</span></span>

### <span data-ttu-id="b980d-111">Пример 1: получение правил оповещения для группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="b980d-111">Example 1: Get alert rules for a resource group</span></span>
```
PS C:\>Get-AzureRmAlertRule -ResourceGroup "Default-Web-CentralUS"
```

<span data-ttu-id="b980d-112">Эта команда получает все правила оповещения для группы ресурсов по умолчанию — Web-CentralUS.</span><span class="sxs-lookup"><span data-stu-id="b980d-112">This command gets all of the alert rules for the resource group named Default-Web-CentralUS.</span></span>
<span data-ttu-id="b980d-113">Выходные данные не содержат сведений о правилах, так как параметр *DetailedOutput* не указан.</span><span class="sxs-lookup"><span data-stu-id="b980d-113">The output does not contain details about the rules because the *DetailedOutput* parameter is not specified.</span></span>

### <span data-ttu-id="b980d-114">Пример 2: получение правила оповещения по имени</span><span class="sxs-lookup"><span data-stu-id="b980d-114">Example 2: Get an alert rule by name</span></span>
```
PS C:\>Get-AzureRmAlertRule -ResourcGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8"
```

<span data-ttu-id="b980d-115">Эта команда возвращает правило оповещения с именем myAlert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span><span class="sxs-lookup"><span data-stu-id="b980d-115">This command gets the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span></span>
<span data-ttu-id="b980d-116">Так как параметр *DetailedOutput* не указан, в выходных данных содержатся только основные сведения о правиле оповещения.</span><span class="sxs-lookup"><span data-stu-id="b980d-116">Because the *DetailedOutput* parameter is not specified, the output contains only basic information about the alert rule.</span></span>

### <span data-ttu-id="b980d-117">Пример 3: получение правила оповещения по имени с подробным выводом</span><span class="sxs-lookup"><span data-stu-id="b980d-117">Example 3: Get an alert rule by name with detailed output</span></span>
```
PS C:\>Get-AzureRmAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8" -DetailedOutput
```

<span data-ttu-id="b980d-118">Эта команда возвращает правило оповещения с именем myAlert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span><span class="sxs-lookup"><span data-stu-id="b980d-118">This command gets the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span></span>
<span data-ttu-id="b980d-119">Указан параметр *DetailedOutput* , поэтому выходные данные подробно описаны.</span><span class="sxs-lookup"><span data-stu-id="b980d-119">The *DetailedOutput* parameter is specified, so the output is detailed.</span></span>

## <span data-ttu-id="b980d-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b980d-120">PARAMETERS</span></span>

### <span data-ttu-id="b980d-121">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="b980d-121">-DetailedOutput</span></span>
<span data-ttu-id="b980d-122">Отображение подробных сведений в выходных данных.</span><span class="sxs-lookup"><span data-stu-id="b980d-122">Displays full details in the output.</span></span>

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

### <span data-ttu-id="b980d-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b980d-123">-Name</span></span>
<span data-ttu-id="b980d-124">Указывает имя правила оповещения, которое требуется получить.</span><span class="sxs-lookup"><span data-stu-id="b980d-124">Specifies the name of the alert rule to get.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameters for Get-AzureRmAlertRule cmdlet using name
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b980d-125">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b980d-125">-ResourceGroup</span></span>
<span data-ttu-id="b980d-126">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b980d-126">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="b980d-127">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="b980d-127">-TargetResourceId</span></span>
<span data-ttu-id="b980d-128">Указывает идентификатор целевого ресурса.</span><span class="sxs-lookup"><span data-stu-id="b980d-128">Specifies the ID of the target resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameters for Get-AzureRmAlertRule cmdlet using target resource uri
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b980d-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b980d-129">-DefaultProfile</span></span>
<span data-ttu-id="b980d-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b980d-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b980d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b980d-131">CommonParameters</span></span>
<span data-ttu-id="b980d-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b980d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b980d-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b980d-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b980d-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b980d-134">INPUTS</span></span>

## <span data-ttu-id="b980d-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b980d-135">OUTPUTS</span></span>

### <span data-ttu-id="b980d-136">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. Insights. OutputClasses. PSManagementItemDescriptor]</span><span class="sxs-lookup"><span data-stu-id="b980d-136">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSManagementItemDescriptor]</span></span>

## <span data-ttu-id="b980d-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="b980d-137">NOTES</span></span>

## <span data-ttu-id="b980d-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b980d-138">RELATED LINKS</span></span>

[<span data-ttu-id="b980d-139">Add-AzureRmLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="b980d-139">Add-AzureRmLogAlertRule</span></span>](./Add-AzureRmLogAlertRule.md)

[<span data-ttu-id="b980d-140">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="b980d-140">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="b980d-141">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="b980d-141">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="b980d-142">Get-AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="b980d-142">Get-AzureRmAlertHistory</span></span>](./Get-AzureRmAlertHistory.md)

[<span data-ttu-id="b980d-143">Remove-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="b980d-143">Remove-AzureRmAlertRule</span></span>](./Remove-AzureRmAlertRule.md)



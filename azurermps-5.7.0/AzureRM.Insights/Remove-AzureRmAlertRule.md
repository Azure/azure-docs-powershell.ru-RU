---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: C7EC21C7-1C7E-49B2-9B33-486532FCDAEC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/remove-azurermalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmAlertRule.md
ms.openlocfilehash: eaa7cfa9f58bb9bb5affa7a035d194910bcf0006
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561799"
---
# <span data-ttu-id="b4858-101">Remove-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="b4858-101">Remove-AzureRmAlertRule</span></span>

## <span data-ttu-id="b4858-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b4858-102">SYNOPSIS</span></span>
<span data-ttu-id="b4858-103">Удаление правила оповещения.</span><span class="sxs-lookup"><span data-stu-id="b4858-103">Removes an alert rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b4858-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b4858-104">SYNTAX</span></span>

```
Remove-AzureRmAlertRule -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b4858-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b4858-105">DESCRIPTION</span></span>
<span data-ttu-id="b4858-106">Командлет **Remove-AzureRmAlertRule** удаляет правило оповещения.</span><span class="sxs-lookup"><span data-stu-id="b4858-106">The **Remove-AzureRmAlertRule** cmdlet removes an alert rule.</span></span>
<span data-ttu-id="b4858-107">Вы должны указать имя правила оповещения и группу ресурсов, которому она назначена.</span><span class="sxs-lookup"><span data-stu-id="b4858-107">You must specify the name of the alert rule and the resource group to which it is assigned.</span></span>

<span data-ttu-id="b4858-108">Этот командлет реализует шаблон ShouldProcess, т. е. может запросить подтверждение от пользователя, прежде чем действительно создать, изменить или удалить ресурс.</span><span class="sxs-lookup"><span data-stu-id="b4858-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="b4858-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b4858-109">EXAMPLES</span></span>

### <span data-ttu-id="b4858-110">Пример 1: Удаление правила оповещения</span><span class="sxs-lookup"><span data-stu-id="b4858-110">Example 1: Remove an alert rule</span></span>
```
PS C:\>Remove-AzureRmAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

<span data-ttu-id="b4858-111">Эта команда удаляет правило оповещения с именем myAlert-7da64548-214d-42ca-b12b-b245bb8f0ac8 в группе ресурсов Default-Web-CentralUS.</span><span class="sxs-lookup"><span data-stu-id="b4858-111">This command removes the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8 in the resource group Default-Web-CentralUS.</span></span>

## <span data-ttu-id="b4858-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b4858-112">PARAMETERS</span></span>

### <span data-ttu-id="b4858-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4858-113">-DefaultProfile</span></span>
<span data-ttu-id="b4858-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="b4858-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4858-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b4858-115">-Name</span></span>
<span data-ttu-id="b4858-116">Указывает имя удаляемого правила оповещения.</span><span class="sxs-lookup"><span data-stu-id="b4858-116">Specifies the name of the alert rule to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4858-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4858-117">-ResourceGroupName</span></span>
<span data-ttu-id="b4858-118">Указывает имя группы ресурсов для правила оповещения.</span><span class="sxs-lookup"><span data-stu-id="b4858-118">Specifies the name of the resource group for the alert rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4858-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4858-119">CommonParameters</span></span>
<span data-ttu-id="b4858-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b4858-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4858-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4858-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4858-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b4858-122">INPUTS</span></span>

### <span data-ttu-id="b4858-123">Ничего</span><span class="sxs-lookup"><span data-stu-id="b4858-123">None</span></span>
<span data-ttu-id="b4858-124">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="b4858-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b4858-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b4858-125">OUTPUTS</span></span>

### <span data-ttu-id="b4858-126">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="b4858-126">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="b4858-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="b4858-127">NOTES</span></span>

## <span data-ttu-id="b4858-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b4858-128">RELATED LINKS</span></span>

[<span data-ttu-id="b4858-129">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="b4858-129">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="b4858-130">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="b4858-130">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="b4858-131">Get-AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="b4858-131">Get-AzureRmAlertHistory</span></span>](./Get-AzureRmAlertHistory.md)

[<span data-ttu-id="b4858-132">Get-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="b4858-132">Get-AzureRmAlertRule</span></span>](./Get-AzureRmAlertRule.md)



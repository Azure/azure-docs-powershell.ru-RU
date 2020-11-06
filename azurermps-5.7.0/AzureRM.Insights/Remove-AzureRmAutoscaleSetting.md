---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 6140E973-D7AB-4A28-A4FA-818E08129372
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/remove-azurermautoscalesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmAutoscaleSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmAutoscaleSetting.md
ms.openlocfilehash: 4d6c2f748915847038ef4029dc024763375ef99e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561796"
---
# <span data-ttu-id="828d6-101">Remove-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="828d6-101">Remove-AzureRmAutoscaleSetting</span></span>

## <span data-ttu-id="828d6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="828d6-102">SYNOPSIS</span></span>
<span data-ttu-id="828d6-103">Удаление параметра автомасштабирования.</span><span class="sxs-lookup"><span data-stu-id="828d6-103">Removes an Autoscale setting.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="828d6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="828d6-104">SYNTAX</span></span>

```
Remove-AzureRmAutoscaleSetting -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="828d6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="828d6-105">DESCRIPTION</span></span>
<span data-ttu-id="828d6-106">Командлет **Remove-AzureRmAutoscaleSetting** удаляет параметр автомасштабирования.</span><span class="sxs-lookup"><span data-stu-id="828d6-106">The **Remove-AzureRmAutoscaleSetting** cmdlet removes an Autoscale setting.</span></span>
<span data-ttu-id="828d6-107">Вы должны указать имя параметра и имя группы ресурсов, которому она назначена.</span><span class="sxs-lookup"><span data-stu-id="828d6-107">You must specify the name of the setting and the name of the resource group to which it is assigned.</span></span>

<span data-ttu-id="828d6-108">Этот командлет реализует шаблон ShouldProcess, т. е. может запросить подтверждение от пользователя, прежде чем действительно создать, изменить или удалить ресурс.</span><span class="sxs-lookup"><span data-stu-id="828d6-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="828d6-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="828d6-109">EXAMPLES</span></span>

## <span data-ttu-id="828d6-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="828d6-110">PARAMETERS</span></span>

### <span data-ttu-id="828d6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="828d6-111">-DefaultProfile</span></span>
<span data-ttu-id="828d6-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="828d6-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="828d6-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="828d6-113">-Name</span></span>
<span data-ttu-id="828d6-114">Задает имя параметра автомасштабирования, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="828d6-114">Specifies the name of the Autoscale setting to remove.</span></span>

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

### <span data-ttu-id="828d6-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="828d6-115">-ResourceGroupName</span></span>
<span data-ttu-id="828d6-116">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="828d6-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="828d6-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="828d6-117">CommonParameters</span></span>
<span data-ttu-id="828d6-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="828d6-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="828d6-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="828d6-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="828d6-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="828d6-120">INPUTS</span></span>

### <span data-ttu-id="828d6-121">Ничего</span><span class="sxs-lookup"><span data-stu-id="828d6-121">None</span></span>
<span data-ttu-id="828d6-122">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="828d6-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="828d6-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="828d6-123">OUTPUTS</span></span>

### <span data-ttu-id="828d6-124">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="828d6-124">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="828d6-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="828d6-125">NOTES</span></span>

## <span data-ttu-id="828d6-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="828d6-126">RELATED LINKS</span></span>

[<span data-ttu-id="828d6-127">Add-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="828d6-127">Add-AzureRmAutoscaleSetting</span></span>](./Add-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="828d6-128">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="828d6-128">Get-AzureRmAutoscaleSetting</span></span>](./Get-AzureRmAutoscaleSetting.md)



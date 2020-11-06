---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 6140E973-D7AB-4A28-A4FA-818E08129372
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmAutoscaleSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmAutoscaleSetting.md
ms.openlocfilehash: cd853184e06403f3c0d516ee1b0790c724adacb4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567623"
---
# <span data-ttu-id="3f9f3-101">Remove-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="3f9f3-101">Remove-AzureRmAutoscaleSetting</span></span>

## <span data-ttu-id="3f9f3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3f9f3-102">SYNOPSIS</span></span>
<span data-ttu-id="3f9f3-103">Удаление параметра автомасштабирования.</span><span class="sxs-lookup"><span data-stu-id="3f9f3-103">Removes an Autoscale setting.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3f9f3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3f9f3-104">SYNTAX</span></span>

```
Remove-AzureRmAutoscaleSetting -ResourceGroup <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3f9f3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3f9f3-105">DESCRIPTION</span></span>
<span data-ttu-id="3f9f3-106">Командлет **Remove-AzureRmAutoscaleSetting** удаляет параметр автомасштабирования.</span><span class="sxs-lookup"><span data-stu-id="3f9f3-106">The **Remove-AzureRmAutoscaleSetting** cmdlet removes an Autoscale setting.</span></span>
<span data-ttu-id="3f9f3-107">Вы должны указать имя параметра и имя группы ресурсов, которому она назначена.</span><span class="sxs-lookup"><span data-stu-id="3f9f3-107">You must specify the name of the setting and the name of the resource group to which it is assigned.</span></span>

## <span data-ttu-id="3f9f3-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3f9f3-108">EXAMPLES</span></span>

## <span data-ttu-id="3f9f3-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3f9f3-109">PARAMETERS</span></span>

### <span data-ttu-id="3f9f3-110">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3f9f3-110">-Name</span></span>
<span data-ttu-id="3f9f3-111">Задает имя параметра автомасштабирования, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="3f9f3-111">Specifies the name of the Autoscale setting to remove.</span></span>

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

### <span data-ttu-id="3f9f3-112">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="3f9f3-112">-ResourceGroup</span></span>
<span data-ttu-id="3f9f3-113">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3f9f3-113">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="3f9f3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f9f3-114">-DefaultProfile</span></span>
<span data-ttu-id="3f9f3-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3f9f3-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3f9f3-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f9f3-116">CommonParameters</span></span>
<span data-ttu-id="3f9f3-117">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3f9f3-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f9f3-118">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f9f3-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f9f3-119">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3f9f3-119">INPUTS</span></span>

## <span data-ttu-id="3f9f3-120">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3f9f3-120">OUTPUTS</span></span>

### <span data-ttu-id="3f9f3-121">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="3f9f3-121">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="3f9f3-122">Пуск</span><span class="sxs-lookup"><span data-stu-id="3f9f3-122">NOTES</span></span>

## <span data-ttu-id="3f9f3-123">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3f9f3-123">RELATED LINKS</span></span>

[<span data-ttu-id="3f9f3-124">Add-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="3f9f3-124">Add-AzureRmAutoscaleSetting</span></span>](./Add-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="3f9f3-125">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="3f9f3-125">Get-AzureRmAutoscaleSetting</span></span>](./Get-AzureRmAutoscaleSetting.md)



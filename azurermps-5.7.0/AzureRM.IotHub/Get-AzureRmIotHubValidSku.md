---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/get-azurermiothubvalidsku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubValidSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubValidSku.md
ms.openlocfilehash: 23c51ff85ba061d23745974e34bcf89135edcee3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734455"
---
# <span data-ttu-id="72de1-101">Get-AzureRmIotHubValidSku</span><span class="sxs-lookup"><span data-stu-id="72de1-101">Get-AzureRmIotHubValidSku</span></span>

## <span data-ttu-id="72de1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="72de1-102">SYNOPSIS</span></span>
<span data-ttu-id="72de1-103">Возвращает все допустимые SKU, в которые может переходить этот IotHub.</span><span class="sxs-lookup"><span data-stu-id="72de1-103">Gets all valid skus that this IotHub can transition to.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="72de1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="72de1-104">SYNTAX</span></span>

```
Get-AzureRmIotHubValidSku [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="72de1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="72de1-105">DESCRIPTION</span></span>
<span data-ttu-id="72de1-106">Получает все допустимые SKU, в которые может переходить этот IotHub.</span><span class="sxs-lookup"><span data-stu-id="72de1-106">Gets all the valid skus that this IotHub can transition to.</span></span>
<span data-ttu-id="72de1-107">IotHub не может переходить между бесплатной и платной SKU и наоборот.</span><span class="sxs-lookup"><span data-stu-id="72de1-107">An IotHub cannot transition between free and the paid skus and vice versa.</span></span> <span data-ttu-id="72de1-108">Если вы хотите добиться этого, вам нужно будет удалить и повторно создать iothub.</span><span class="sxs-lookup"><span data-stu-id="72de1-108">You will have to delete and recreate the iothub if you want to achieve this.</span></span>

## <span data-ttu-id="72de1-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="72de1-109">EXAMPLES</span></span>

### <span data-ttu-id="72de1-110">Пример 1 Получение допустимых SKU</span><span class="sxs-lookup"><span data-stu-id="72de1-110">Example 1 Get the valid skus</span></span>
```
PS C:\> Get-AzureRmIotHubValidSku -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="72de1-111">Получает список всех SKU для IotHub с именем "myiothub"</span><span class="sxs-lookup"><span data-stu-id="72de1-111">Gets a list of all skus for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="72de1-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="72de1-112">PARAMETERS</span></span>

### <span data-ttu-id="72de1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72de1-113">-DefaultProfile</span></span>
<span data-ttu-id="72de1-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="72de1-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="72de1-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="72de1-115">-Name</span></span>
<span data-ttu-id="72de1-116">Имя центра Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="72de1-116">Name of the IoT hub.</span></span> 

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72de1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72de1-117">-ResourceGroupName</span></span>
<span data-ttu-id="72de1-118">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="72de1-118">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72de1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72de1-119">CommonParameters</span></span>
<span data-ttu-id="72de1-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="72de1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72de1-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72de1-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72de1-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="72de1-122">INPUTS</span></span>

### <span data-ttu-id="72de1-123">System. String</span><span class="sxs-lookup"><span data-stu-id="72de1-123">System.String</span></span>

## <span data-ttu-id="72de1-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="72de1-124">OUTPUTS</span></span>

### <span data-ttu-id="72de1-125">System. Collections. Generic. IList ' 1 [[Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHubSkuDescription, Microsoft. Azure. Commands. IotHub, Version = 1.0.0.0, Culture = "нейтрально", PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="72de1-125">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSkuDescription, Microsoft.Azure.Commands.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="72de1-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="72de1-126">NOTES</span></span>

## <span data-ttu-id="72de1-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="72de1-127">RELATED LINKS</span></span>


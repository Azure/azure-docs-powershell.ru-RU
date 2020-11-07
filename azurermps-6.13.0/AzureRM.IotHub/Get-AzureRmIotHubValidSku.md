---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/get-azurermiothubvalidsku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubValidSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubValidSku.md
ms.openlocfilehash: d1c52cef6548f8762f972789a1fd9d47e8cc92aa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734386"
---
# <span data-ttu-id="32679-101">Get-AzureRmIotHubValidSku</span><span class="sxs-lookup"><span data-stu-id="32679-101">Get-AzureRmIotHubValidSku</span></span>

## <span data-ttu-id="32679-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="32679-102">SYNOPSIS</span></span>
<span data-ttu-id="32679-103">Возвращает все допустимые SKU, в которые может переходить этот IotHub.</span><span class="sxs-lookup"><span data-stu-id="32679-103">Gets all valid skus that this IotHub can transition to.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="32679-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="32679-104">SYNTAX</span></span>

```
Get-AzureRmIotHubValidSku [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="32679-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="32679-105">DESCRIPTION</span></span>
<span data-ttu-id="32679-106">Получает все допустимые SKU, в которые может переходить этот IotHub.</span><span class="sxs-lookup"><span data-stu-id="32679-106">Gets all the valid skus that this IotHub can transition to.</span></span>
<span data-ttu-id="32679-107">IotHub не может переходить между бесплатной и платной SKU и наоборот.</span><span class="sxs-lookup"><span data-stu-id="32679-107">An IotHub cannot transition between free and the paid skus and vice versa.</span></span> <span data-ttu-id="32679-108">Если вы хотите добиться этого, вам нужно будет удалить и повторно создать iothub.</span><span class="sxs-lookup"><span data-stu-id="32679-108">You will have to delete and recreate the iothub if you want to achieve this.</span></span>

## <span data-ttu-id="32679-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="32679-109">EXAMPLES</span></span>

### <span data-ttu-id="32679-110">Пример 1 Получение допустимых SKU</span><span class="sxs-lookup"><span data-stu-id="32679-110">Example 1 Get the valid skus</span></span>
```
PS C:\> Get-AzureRmIotHubValidSku -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="32679-111">Получает список всех SKU для IotHub с именем "myiothub"</span><span class="sxs-lookup"><span data-stu-id="32679-111">Gets a list of all skus for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="32679-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="32679-112">PARAMETERS</span></span>

### <span data-ttu-id="32679-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32679-113">-DefaultProfile</span></span>
<span data-ttu-id="32679-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="32679-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="32679-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="32679-115">-Name</span></span>
<span data-ttu-id="32679-116">Имя центра Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="32679-116">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="32679-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32679-117">-ResourceGroupName</span></span>
<span data-ttu-id="32679-118">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="32679-118">Resource Group Name</span></span>

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

### <span data-ttu-id="32679-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32679-119">CommonParameters</span></span>
<span data-ttu-id="32679-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="32679-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32679-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32679-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32679-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="32679-122">INPUTS</span></span>

### <span data-ttu-id="32679-123">System. String</span><span class="sxs-lookup"><span data-stu-id="32679-123">System.String</span></span>

## <span data-ttu-id="32679-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="32679-124">OUTPUTS</span></span>

### <span data-ttu-id="32679-125">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHubSkuDescription</span><span class="sxs-lookup"><span data-stu-id="32679-125">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSkuDescription</span></span>

## <span data-ttu-id="32679-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="32679-126">NOTES</span></span>

## <span data-ttu-id="32679-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="32679-127">RELATED LINKS</span></span>

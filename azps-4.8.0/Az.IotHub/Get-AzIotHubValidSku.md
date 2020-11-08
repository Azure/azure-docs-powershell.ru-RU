---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubvalidsku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubValidSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubValidSku.md
ms.openlocfilehash: e0f178c10fa74d8fa230472397d7bcc835f98bf4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94242740"
---
# <span data-ttu-id="6cebf-101">Get-AzIotHubValidSku</span><span class="sxs-lookup"><span data-stu-id="6cebf-101">Get-AzIotHubValidSku</span></span>

## <span data-ttu-id="6cebf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6cebf-102">SYNOPSIS</span></span>
<span data-ttu-id="6cebf-103">Возвращает все допустимые SKU, в которые может переходить этот IotHub.</span><span class="sxs-lookup"><span data-stu-id="6cebf-103">Gets all valid skus that this IotHub can transition to.</span></span>

## <span data-ttu-id="6cebf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6cebf-104">SYNTAX</span></span>

```
Get-AzIotHubValidSku [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6cebf-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6cebf-105">DESCRIPTION</span></span>
<span data-ttu-id="6cebf-106">Получает все допустимые SKU, в которые может переходить этот IotHub.</span><span class="sxs-lookup"><span data-stu-id="6cebf-106">Gets all the valid skus that this IotHub can transition to.</span></span>
<span data-ttu-id="6cebf-107">IotHub не может переходить между бесплатной и платной SKU и наоборот.</span><span class="sxs-lookup"><span data-stu-id="6cebf-107">An IotHub cannot transition between free and the paid skus and vice versa.</span></span> <span data-ttu-id="6cebf-108">Если вы хотите добиться этого, вам нужно будет удалить и повторно создать iothub.</span><span class="sxs-lookup"><span data-stu-id="6cebf-108">You will have to delete and recreate the iothub if you want to achieve this.</span></span>

## <span data-ttu-id="6cebf-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6cebf-109">EXAMPLES</span></span>

### <span data-ttu-id="6cebf-110">Пример 1 Получение допустимых SKU</span><span class="sxs-lookup"><span data-stu-id="6cebf-110">Example 1 Get the valid skus</span></span>
```
PS C:\> Get-AzIotHubValidSku -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="6cebf-111">Получает список всех SKU для IotHub с именем "myiothub"</span><span class="sxs-lookup"><span data-stu-id="6cebf-111">Gets a list of all skus for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="6cebf-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6cebf-112">PARAMETERS</span></span>

### <span data-ttu-id="6cebf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cebf-113">-DefaultProfile</span></span>
<span data-ttu-id="6cebf-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="6cebf-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6cebf-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6cebf-115">-Name</span></span>
<span data-ttu-id="6cebf-116">Имя центра Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="6cebf-116">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="6cebf-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6cebf-117">-ResourceGroupName</span></span>
<span data-ttu-id="6cebf-118">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="6cebf-118">Resource Group Name</span></span>

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

### <span data-ttu-id="6cebf-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cebf-119">CommonParameters</span></span>
<span data-ttu-id="6cebf-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6cebf-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cebf-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6cebf-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cebf-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6cebf-122">INPUTS</span></span>

### <span data-ttu-id="6cebf-123">System. String</span><span class="sxs-lookup"><span data-stu-id="6cebf-123">System.String</span></span>

## <span data-ttu-id="6cebf-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6cebf-124">OUTPUTS</span></span>

### <span data-ttu-id="6cebf-125">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHubSkuDescription</span><span class="sxs-lookup"><span data-stu-id="6cebf-125">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSkuDescription</span></span>

## <span data-ttu-id="6cebf-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="6cebf-126">NOTES</span></span>

## <span data-ttu-id="6cebf-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6cebf-127">RELATED LINKS</span></span>

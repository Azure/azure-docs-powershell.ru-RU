---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 48C33FAF-83C1-4725-AD2A-CF48D0718182
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewaysku
schema: 2.0.0
ms.openlocfilehash: cda4281b1bf52b9f0b94926bc66590d1bd741c44
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913611"
---
# <span data-ttu-id="53545-101">New-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="53545-101">New-AzureRmApplicationGatewaySku</span></span>

## <span data-ttu-id="53545-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="53545-102">SYNOPSIS</span></span>
<span data-ttu-id="53545-103">Создает SKU для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="53545-103">Creates a SKU for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="53545-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="53545-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewaySku -Name <String> -Tier <String> -Capacity <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="53545-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="53545-105">DESCRIPTION</span></span>
<span data-ttu-id="53545-106">Командлет **New-AzureRmApplicationGatewaySku** создает единицу хранения (SKU) для шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="53545-106">The **New-AzureRmApplicationGatewaySku** cmdlet creates a stock keeping unit (SKU) for an Azure application gateway.</span></span>

## <span data-ttu-id="53545-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="53545-107">EXAMPLES</span></span>

### <span data-ttu-id="53545-108">Пример 1: создание SKU для шлюза приложений Azure</span><span class="sxs-lookup"><span data-stu-id="53545-108">Example 1: Create a SKU for an Azure application gateway</span></span>
```
PS C:\>$SKU = New-AzureRmApplicationGatewaySku -Name "Standard_Small" -Tier "Standard" -Capacity 2
```

<span data-ttu-id="53545-109">Эта команда создает SKU с именем Standard_Small для шлюза приложений Azure и сохраняет результат в переменной с именем $SKU.</span><span class="sxs-lookup"><span data-stu-id="53545-109">This command creates a SKU named Standard_Small for an Azure application gateway and stores the result in the variable named $SKU.</span></span>

## <span data-ttu-id="53545-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="53545-110">PARAMETERS</span></span>

### <span data-ttu-id="53545-111">-Capacity</span><span class="sxs-lookup"><span data-stu-id="53545-111">-Capacity</span></span>
<span data-ttu-id="53545-112">Задает количество экземпляров шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="53545-112">Specifies the number of instances of an application gateway.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53545-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53545-113">-DefaultProfile</span></span>
<span data-ttu-id="53545-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="53545-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="53545-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="53545-115">-Name</span></span>
<span data-ttu-id="53545-116">Указывает имя SKU.</span><span class="sxs-lookup"><span data-stu-id="53545-116">Specifies the name of the SKU.</span></span>

<span data-ttu-id="53545-117">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="53545-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="53545-118">Standard_Small</span><span class="sxs-lookup"><span data-stu-id="53545-118">Standard_Small</span></span>
- <span data-ttu-id="53545-119">Standard_Medium</span><span class="sxs-lookup"><span data-stu-id="53545-119">Standard_Medium</span></span>
- <span data-ttu-id="53545-120">Standard_Large</span><span class="sxs-lookup"><span data-stu-id="53545-120">Standard_Large</span></span>
- <span data-ttu-id="53545-121">WAF_Medium</span><span class="sxs-lookup"><span data-stu-id="53545-121">WAF_Medium</span></span>
- <span data-ttu-id="53545-122">WAF_Large</span><span class="sxs-lookup"><span data-stu-id="53545-122">WAF_Large</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Standard_Small, Standard_Medium, Standard_Large, WAF_Medium, WAF_Large

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53545-123">Уровень</span><span class="sxs-lookup"><span data-stu-id="53545-123">-Tier</span></span>
<span data-ttu-id="53545-124">Указывает уровень SKU.</span><span class="sxs-lookup"><span data-stu-id="53545-124">Specifies the tier of the SKU.</span></span>
<span data-ttu-id="53545-125">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="53545-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="53545-126">Стандартная</span><span class="sxs-lookup"><span data-stu-id="53545-126">Standard</span></span>
- <span data-ttu-id="53545-127">WAF</span><span class="sxs-lookup"><span data-stu-id="53545-127">WAF</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Standard, WAF

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53545-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53545-128">CommonParameters</span></span>
<span data-ttu-id="53545-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="53545-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53545-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53545-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53545-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="53545-131">INPUTS</span></span>

### <span data-ttu-id="53545-132">System. String</span><span class="sxs-lookup"><span data-stu-id="53545-132">System.String</span></span>

## <span data-ttu-id="53545-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="53545-133">OUTPUTS</span></span>

### <span data-ttu-id="53545-134">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="53545-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

## <span data-ttu-id="53545-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="53545-135">NOTES</span></span>

## <span data-ttu-id="53545-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="53545-136">RELATED LINKS</span></span>

[<span data-ttu-id="53545-137">Get-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="53545-137">Get-AzureRmApplicationGatewaySku</span></span>](./Get-AzureRmApplicationGatewaySku.md)

[<span data-ttu-id="53545-138">Set-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="53545-138">Set-AzureRmApplicationGatewaySku</span></span>](./Set-AzureRmApplicationGatewaySku.md)



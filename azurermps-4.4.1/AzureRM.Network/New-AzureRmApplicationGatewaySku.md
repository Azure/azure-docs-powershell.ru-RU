---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 48C33FAF-83C1-4725-AD2A-CF48D0718182
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewaySku.md
ms.openlocfilehash: eb1f0dadd905ff4b57a58c46f763f3c2dd51f256
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568032"
---
# <span data-ttu-id="f4106-101">New-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="f4106-101">New-AzureRmApplicationGatewaySku</span></span>

## <span data-ttu-id="f4106-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f4106-102">SYNOPSIS</span></span>
<span data-ttu-id="f4106-103">Создает SKU для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="f4106-103">Creates a SKU for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f4106-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f4106-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewaySku -Name <String> -Tier <String> -Capacity <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f4106-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f4106-105">DESCRIPTION</span></span>
<span data-ttu-id="f4106-106">Командлет **New-AzureRmApplicationGatewaySku** создает единицу хранения (SKU) для шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="f4106-106">The **New-AzureRmApplicationGatewaySku** cmdlet creates a stock keeping unit (SKU) for an Azure application gateway.</span></span>

## <span data-ttu-id="f4106-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f4106-107">EXAMPLES</span></span>

### <span data-ttu-id="f4106-108">Пример 1: создание SKU для шлюза приложений Azure</span><span class="sxs-lookup"><span data-stu-id="f4106-108">Example 1: Create a SKU for an Azure application gateway</span></span>
```
PS C:\>$SKU = New-AzureRmApplicationGatewaySku -Name "Standard_Small" -Tier "Standard" -Capacity 2
```

<span data-ttu-id="f4106-109">Эта команда создает SKU с именем Standard_Small для шлюза приложений Azure и сохраняет результат в переменной с именем $SKU.</span><span class="sxs-lookup"><span data-stu-id="f4106-109">This command creates a SKU named Standard_Small for an Azure application gateway and stores the result in the variable named $SKU.</span></span>

## <span data-ttu-id="f4106-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f4106-110">PARAMETERS</span></span>

### <span data-ttu-id="f4106-111">-Capacity</span><span class="sxs-lookup"><span data-stu-id="f4106-111">-Capacity</span></span>
<span data-ttu-id="f4106-112">Задает количество экземпляров шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="f4106-112">Specifies the number of instances of an application gateway.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4106-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f4106-113">-Name</span></span>
<span data-ttu-id="f4106-114">Указывает имя SKU.</span><span class="sxs-lookup"><span data-stu-id="f4106-114">Specifies the name of the SKU.</span></span>

<span data-ttu-id="f4106-115">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="f4106-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f4106-116">Standard_Small</span><span class="sxs-lookup"><span data-stu-id="f4106-116">Standard_Small</span></span>
- <span data-ttu-id="f4106-117">Standard_Medium</span><span class="sxs-lookup"><span data-stu-id="f4106-117">Standard_Medium</span></span>
- <span data-ttu-id="f4106-118">Standard_Large</span><span class="sxs-lookup"><span data-stu-id="f4106-118">Standard_Large</span></span>
- <span data-ttu-id="f4106-119">WAF_Medium</span><span class="sxs-lookup"><span data-stu-id="f4106-119">WAF_Medium</span></span>
- <span data-ttu-id="f4106-120">WAF_Large</span><span class="sxs-lookup"><span data-stu-id="f4106-120">WAF_Large</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Standard_Small, Standard_Medium, Standard_Large, WAF_Medium, WAF_Large

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4106-121">Уровень</span><span class="sxs-lookup"><span data-stu-id="f4106-121">-Tier</span></span>
<span data-ttu-id="f4106-122">Указывает уровень SKU.</span><span class="sxs-lookup"><span data-stu-id="f4106-122">Specifies the tier of the SKU.</span></span>
<span data-ttu-id="f4106-123">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="f4106-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f4106-124">Стандартная</span><span class="sxs-lookup"><span data-stu-id="f4106-124">Standard</span></span>
- <span data-ttu-id="f4106-125">WAF</span><span class="sxs-lookup"><span data-stu-id="f4106-125">WAF</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Standard, WAF

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4106-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4106-126">-DefaultProfile</span></span>
<span data-ttu-id="f4106-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f4106-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4106-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4106-128">CommonParameters</span></span>
<span data-ttu-id="f4106-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f4106-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4106-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4106-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4106-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f4106-131">INPUTS</span></span>

### <span data-ttu-id="f4106-132">System. String</span><span class="sxs-lookup"><span data-stu-id="f4106-132">System.String</span></span>

## <span data-ttu-id="f4106-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f4106-133">OUTPUTS</span></span>

### <span data-ttu-id="f4106-134">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="f4106-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

## <span data-ttu-id="f4106-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="f4106-135">NOTES</span></span>

## <span data-ttu-id="f4106-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f4106-136">RELATED LINKS</span></span>

[<span data-ttu-id="f4106-137">Get-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="f4106-137">Get-AzureRmApplicationGatewaySku</span></span>](./Get-AzureRmApplicationGatewaySku.md)

[<span data-ttu-id="f4106-138">Set-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="f4106-138">Set-AzureRmApplicationGatewaySku</span></span>](./Set-AzureRmApplicationGatewaySku.md)



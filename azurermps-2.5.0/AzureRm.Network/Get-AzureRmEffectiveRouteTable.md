---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 84FDB0F7-E6DE-4E1B-BD71-89535EDC6AA1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermeffectiveroutetable
schema: 2.0.0
ms.openlocfilehash: 403a3d37418e022032988d5d7fccb40a1e79f449
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913635"
---
# <span data-ttu-id="2a259-101">Get-AzureRmEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="2a259-101">Get-AzureRmEffectiveRouteTable</span></span>

## <span data-ttu-id="2a259-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2a259-102">SYNOPSIS</span></span>
<span data-ttu-id="2a259-103">Возвращает эффективную таблицу маршрутов сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="2a259-103">Gets the effective route table of a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2a259-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2a259-104">SYNTAX</span></span>

```
Get-AzureRmEffectiveRouteTable -NetworkInterfaceName <String> [-ResourceGroupName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2a259-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2a259-105">DESCRIPTION</span></span>
<span data-ttu-id="2a259-106">Командлет **Get-AzureRmEffectiveRouteTable** Возвращает действующую таблицу маршрутов, которая применяется к сетевому интерфейсу.</span><span class="sxs-lookup"><span data-stu-id="2a259-106">The **Get-AzureRmEffectiveRouteTable** cmdlet returns the effective route table that is applied on a network interface.</span></span>

## <span data-ttu-id="2a259-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2a259-107">EXAMPLES</span></span>

### <span data-ttu-id="2a259-108">Пример 1: получение действующей таблицы маршрутов на сетевом интерфейсе</span><span class="sxs-lookup"><span data-stu-id="2a259-108">Example 1: Get the effective route table on a network interface</span></span>
```
PS C:\>Get-AzureRmEffectiveRouteTable -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="2a259-109">Эта команда получает действующую таблицу маршрутов, связанную с сетевым интерфейсом MyNetworkInterface в группе ресурсов с именем MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="2a259-109">This command gets the effective route table associated with network interface named MyNetworkInterface in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="2a259-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2a259-110">PARAMETERS</span></span>

### <span data-ttu-id="2a259-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2a259-111">-AsJob</span></span>
<span data-ttu-id="2a259-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="2a259-112">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a259-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a259-113">-DefaultProfile</span></span>
<span data-ttu-id="2a259-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2a259-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2a259-115">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="2a259-115">-NetworkInterfaceName</span></span>
<span data-ttu-id="2a259-116">Указывает имя сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="2a259-116">Specified the name of a network interface.</span></span>

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

### <span data-ttu-id="2a259-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a259-117">-ResourceGroupName</span></span>
<span data-ttu-id="2a259-118">Указывает группу ресурсов сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="2a259-118">Specifies the resource group of a network interface.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a259-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a259-119">CommonParameters</span></span>
<span data-ttu-id="2a259-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2a259-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a259-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a259-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a259-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2a259-122">INPUTS</span></span>

## <span data-ttu-id="2a259-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2a259-123">OUTPUTS</span></span>

### <span data-ttu-id="2a259-124">Microsoft. Azure. Commands. Network. Models. PSEffectiveRoute</span><span class="sxs-lookup"><span data-stu-id="2a259-124">Microsoft.Azure.Commands.Network.Models.PSEffectiveRoute</span></span>

## <span data-ttu-id="2a259-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="2a259-125">NOTES</span></span>

## <span data-ttu-id="2a259-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2a259-126">RELATED LINKS</span></span>

[<span data-ttu-id="2a259-127">Get-AzureRmEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="2a259-127">Get-AzureRmEffectiveNetworkSecurityGroup</span></span>](./Get-AzureRmEffectiveNetworkSecurityGroup.md)



---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 84FDB0F7-E6DE-4E1B-BD71-89535EDC6AA1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermeffectiveroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmEffectiveRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmEffectiveRouteTable.md
ms.openlocfilehash: 7826dad8b9f19e3fc289ec4b08efa98b8b1ed8a5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733016"
---
# <span data-ttu-id="fd948-101">Get-AzureRmEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="fd948-101">Get-AzureRmEffectiveRouteTable</span></span>

## <span data-ttu-id="fd948-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fd948-102">SYNOPSIS</span></span>
<span data-ttu-id="fd948-103">Возвращает эффективную таблицу маршрутов сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="fd948-103">Gets the effective route table of a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fd948-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fd948-104">SYNTAX</span></span>

```
Get-AzureRmEffectiveRouteTable -NetworkInterfaceName <String> [-ResourceGroupName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fd948-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fd948-105">DESCRIPTION</span></span>
<span data-ttu-id="fd948-106">Командлет **Get-AzureRmEffectiveRouteTable** Возвращает действующую таблицу маршрутов, которая применяется к сетевому интерфейсу.</span><span class="sxs-lookup"><span data-stu-id="fd948-106">The **Get-AzureRmEffectiveRouteTable** cmdlet returns the effective route table that is applied on a network interface.</span></span>

## <span data-ttu-id="fd948-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fd948-107">EXAMPLES</span></span>

### <span data-ttu-id="fd948-108">Пример 1: получение действующей таблицы маршрутов на сетевом интерфейсе</span><span class="sxs-lookup"><span data-stu-id="fd948-108">Example 1: Get the effective route table on a network interface</span></span>
```
PS C:\>Get-AzureRmEffectiveRouteTable -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="fd948-109">Эта команда получает действующую таблицу маршрутов, связанную с сетевым интерфейсом MyNetworkInterface в группе ресурсов с именем MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="fd948-109">This command gets the effective route table associated with network interface named MyNetworkInterface in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="fd948-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fd948-110">PARAMETERS</span></span>

### <span data-ttu-id="fd948-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fd948-111">-AsJob</span></span>
<span data-ttu-id="fd948-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="fd948-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fd948-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd948-113">-DefaultProfile</span></span>
<span data-ttu-id="fd948-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fd948-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fd948-115">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="fd948-115">-NetworkInterfaceName</span></span>
<span data-ttu-id="fd948-116">Указывает имя сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="fd948-116">Specified the name of a network interface.</span></span>

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

### <span data-ttu-id="fd948-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd948-117">-ResourceGroupName</span></span>
<span data-ttu-id="fd948-118">Указывает группу ресурсов сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="fd948-118">Specifies the resource group of a network interface.</span></span>

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

### <span data-ttu-id="fd948-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd948-119">CommonParameters</span></span>
<span data-ttu-id="fd948-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fd948-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd948-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd948-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd948-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fd948-122">INPUTS</span></span>

### <span data-ttu-id="fd948-123">Ничего</span><span class="sxs-lookup"><span data-stu-id="fd948-123">None</span></span>
<span data-ttu-id="fd948-124">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="fd948-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fd948-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fd948-125">OUTPUTS</span></span>

### <span data-ttu-id="fd948-126">Microsoft. Azure. Commands. Network. Models. PSEffectiveRoute</span><span class="sxs-lookup"><span data-stu-id="fd948-126">Microsoft.Azure.Commands.Network.Models.PSEffectiveRoute</span></span>

## <span data-ttu-id="fd948-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="fd948-127">NOTES</span></span>

## <span data-ttu-id="fd948-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fd948-128">RELATED LINKS</span></span>

[<span data-ttu-id="fd948-129">Get-AzureRmEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="fd948-129">Get-AzureRmEffectiveNetworkSecurityGroup</span></span>](./Get-AzureRmEffectiveNetworkSecurityGroup.md)



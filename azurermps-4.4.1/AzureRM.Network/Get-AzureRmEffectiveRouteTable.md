---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 84FDB0F7-E6DE-4E1B-BD71-89535EDC6AA1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmEffectiveRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmEffectiveRouteTable.md
ms.openlocfilehash: f42e378bb0bb5202f9f955dea1b844e343a0e037
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565615"
---
# <span data-ttu-id="0b55c-101">Get-AzureRmEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="0b55c-101">Get-AzureRmEffectiveRouteTable</span></span>

## <span data-ttu-id="0b55c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0b55c-102">SYNOPSIS</span></span>
<span data-ttu-id="0b55c-103">Возвращает эффективную таблицу маршрутов сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="0b55c-103">Gets the effective route table of a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0b55c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0b55c-104">SYNTAX</span></span>

```
Get-AzureRmEffectiveRouteTable -NetworkInterfaceName <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0b55c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0b55c-105">DESCRIPTION</span></span>
<span data-ttu-id="0b55c-106">Командлет **Get-AzureRmEffectiveRouteTable** Возвращает действующую таблицу маршрутов, которая применяется к сетевому интерфейсу.</span><span class="sxs-lookup"><span data-stu-id="0b55c-106">The **Get-AzureRmEffectiveRouteTable** cmdlet returns the effective route table that is applied on a network interface.</span></span>

## <span data-ttu-id="0b55c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0b55c-107">EXAMPLES</span></span>

### <span data-ttu-id="0b55c-108">Пример 1: получение действующей таблицы маршрутов на сетевом интерфейсе</span><span class="sxs-lookup"><span data-stu-id="0b55c-108">Example 1: Get the effective route table on a network interface</span></span>
```
PS C:\>Get-AzureRmEffectiveRouteTable -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="0b55c-109">Эта команда получает действующую таблицу маршрутов, связанную с сетевым интерфейсом MyNetworkInterface в группе ресурсов с именем MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="0b55c-109">This command gets the effective route table associated with network interface named MyNetworkInterface in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="0b55c-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0b55c-110">PARAMETERS</span></span>

### <span data-ttu-id="0b55c-111">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="0b55c-111">-NetworkInterfaceName</span></span>
<span data-ttu-id="0b55c-112">Указывает имя сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="0b55c-112">Specified the name of a network interface.</span></span>

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

### <span data-ttu-id="0b55c-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b55c-113">-ResourceGroupName</span></span>
<span data-ttu-id="0b55c-114">Указывает группу ресурсов сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="0b55c-114">Specifies the resource group of a network interface.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b55c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b55c-115">-DefaultProfile</span></span>
<span data-ttu-id="0b55c-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0b55c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0b55c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b55c-117">CommonParameters</span></span>
<span data-ttu-id="0b55c-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0b55c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b55c-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b55c-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b55c-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0b55c-120">INPUTS</span></span>

## <span data-ttu-id="0b55c-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0b55c-121">OUTPUTS</span></span>

### <span data-ttu-id="0b55c-122">Microsoft. Azure. Commands. Network. Models. PSEffectiveRoute</span><span class="sxs-lookup"><span data-stu-id="0b55c-122">Microsoft.Azure.Commands.Network.Models.PSEffectiveRoute</span></span>

## <span data-ttu-id="0b55c-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="0b55c-123">NOTES</span></span>

## <span data-ttu-id="0b55c-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0b55c-124">RELATED LINKS</span></span>

[<span data-ttu-id="0b55c-125">Get-AzureRmEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="0b55c-125">Get-AzureRmEffectiveNetworkSecurityGroup</span></span>](./Get-AzureRmEffectiveNetworkSecurityGroup.md)



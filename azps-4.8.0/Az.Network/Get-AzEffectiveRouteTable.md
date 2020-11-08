---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 84FDB0F7-E6DE-4E1B-BD71-89535EDC6AA1
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azeffectiveroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzEffectiveRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzEffectiveRouteTable.md
ms.openlocfilehash: e7d65e7797fb606306f0f0cc1e7c394fcf3d1d3d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235053"
---
# <span data-ttu-id="5be62-101">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="5be62-101">Get-AzEffectiveRouteTable</span></span>

## <span data-ttu-id="5be62-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5be62-102">SYNOPSIS</span></span>
<span data-ttu-id="5be62-103">Возвращает эффективную таблицу маршрутов сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="5be62-103">Gets the effective route table of a network interface.</span></span>

## <span data-ttu-id="5be62-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5be62-104">SYNTAX</span></span>

```
Get-AzEffectiveRouteTable -NetworkInterfaceName <String> [-ResourceGroupName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5be62-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5be62-105">DESCRIPTION</span></span>
<span data-ttu-id="5be62-106">Командлет **Get-AzEffectiveRouteTable** Возвращает действующую таблицу маршрутов, которая применяется к сетевому интерфейсу.</span><span class="sxs-lookup"><span data-stu-id="5be62-106">The **Get-AzEffectiveRouteTable** cmdlet returns the effective route table that is applied on a network interface.</span></span>

## <span data-ttu-id="5be62-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5be62-107">EXAMPLES</span></span>

### <span data-ttu-id="5be62-108">Пример 1: получение действующей таблицы маршрутов на сетевом интерфейсе</span><span class="sxs-lookup"><span data-stu-id="5be62-108">Example 1: Get the effective route table on a network interface</span></span>
```
PS C:\>Get-AzEffectiveRouteTable -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="5be62-109">Эта команда получает действующую таблицу маршрутов, связанную с сетевым интерфейсом MyNetworkInterface в группе ресурсов с именем MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="5be62-109">This command gets the effective route table associated with network interface named MyNetworkInterface in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="5be62-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5be62-110">PARAMETERS</span></span>

### <span data-ttu-id="5be62-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5be62-111">-AsJob</span></span>
<span data-ttu-id="5be62-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="5be62-112">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5be62-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5be62-113">-DefaultProfile</span></span>
<span data-ttu-id="5be62-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5be62-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5be62-115">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="5be62-115">-NetworkInterfaceName</span></span>
<span data-ttu-id="5be62-116">Указывает имя сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="5be62-116">Specified the name of a network interface.</span></span>

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

### <span data-ttu-id="5be62-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5be62-117">-ResourceGroupName</span></span>
<span data-ttu-id="5be62-118">Указывает группу ресурсов сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="5be62-118">Specifies the resource group of a network interface.</span></span>

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

### <span data-ttu-id="5be62-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5be62-119">CommonParameters</span></span>
<span data-ttu-id="5be62-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5be62-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5be62-121">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5be62-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5be62-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5be62-122">INPUTS</span></span>

### <span data-ttu-id="5be62-123">System. String</span><span class="sxs-lookup"><span data-stu-id="5be62-123">System.String</span></span>

## <span data-ttu-id="5be62-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5be62-124">OUTPUTS</span></span>

### <span data-ttu-id="5be62-125">Microsoft. Azure. Commands. Network. Models. PSEffectiveRoute</span><span class="sxs-lookup"><span data-stu-id="5be62-125">Microsoft.Azure.Commands.Network.Models.PSEffectiveRoute</span></span>

## <span data-ttu-id="5be62-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="5be62-126">NOTES</span></span>

## <span data-ttu-id="5be62-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5be62-127">RELATED LINKS</span></span>

[<span data-ttu-id="5be62-128">Get-AzEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="5be62-128">Get-AzEffectiveNetworkSecurityGroup</span></span>](./Get-AzEffectiveNetworkSecurityGroup.md)



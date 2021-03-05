---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 84FDB0F7-E6DE-4E1B-BD71-89535EDC6AA1
online version: https://docs.microsoft.com/powershell/module/az.network/get-azeffectiveroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzEffectiveRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzEffectiveRouteTable.md
ms.openlocfilehash: 28ec38b9f2dfbb658203aa46fe0d8225aca08a5e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967912"
---
# <span data-ttu-id="d04d7-101">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="d04d7-101">Get-AzEffectiveRouteTable</span></span>

## <span data-ttu-id="d04d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d04d7-102">SYNOPSIS</span></span>
<span data-ttu-id="d04d7-103">Получает эффективную таблицу маршрутов в сетевом интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="d04d7-103">Gets the effective route table of a network interface.</span></span>

## <span data-ttu-id="d04d7-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d04d7-104">SYNTAX</span></span>

```
Get-AzEffectiveRouteTable -NetworkInterfaceName <String> [-ResourceGroupName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d04d7-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d04d7-105">DESCRIPTION</span></span>
<span data-ttu-id="d04d7-106">С **помощью cmdlet get-AzEffectiveRouteTable** возвращается эффективная таблица маршрутов, примененная в сетевом интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="d04d7-106">The **Get-AzEffectiveRouteTable** cmdlet returns the effective route table that is applied on a network interface.</span></span>

## <span data-ttu-id="d04d7-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d04d7-107">EXAMPLES</span></span>

### <span data-ttu-id="d04d7-108">Пример 1. Получить эффективную таблицу маршрутов в сетевом интерфейсе</span><span class="sxs-lookup"><span data-stu-id="d04d7-108">Example 1: Get the effective route table on a network interface</span></span>
```
PS C:\>Get-AzEffectiveRouteTable -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="d04d7-109">Эта команда возвращает эффективную таблицу маршрутов, связанную с сетевым интерфейсом MyNetworkInterface в группе ресурсов MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="d04d7-109">This command gets the effective route table associated with network interface named MyNetworkInterface in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="d04d7-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d04d7-110">PARAMETERS</span></span>

### <span data-ttu-id="d04d7-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d04d7-111">-AsJob</span></span>
<span data-ttu-id="d04d7-112">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="d04d7-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d04d7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d04d7-113">-DefaultProfile</span></span>
<span data-ttu-id="d04d7-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d04d7-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d04d7-115">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="d04d7-115">-NetworkInterfaceName</span></span>
<span data-ttu-id="d04d7-116">Имя сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="d04d7-116">Specified the name of a network interface.</span></span>

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

### <span data-ttu-id="d04d7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d04d7-117">-ResourceGroupName</span></span>
<span data-ttu-id="d04d7-118">Определяет группу ресурсов в сетевом интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="d04d7-118">Specifies the resource group of a network interface.</span></span>

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

### <span data-ttu-id="d04d7-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d04d7-119">CommonParameters</span></span>
<span data-ttu-id="d04d7-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d04d7-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d04d7-121">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d04d7-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d04d7-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d04d7-122">INPUTS</span></span>

### <span data-ttu-id="d04d7-123">System.String</span><span class="sxs-lookup"><span data-stu-id="d04d7-123">System.String</span></span>

## <span data-ttu-id="d04d7-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d04d7-124">OUTPUTS</span></span>

### <span data-ttu-id="d04d7-125">Microsoft.Azure.Commands.Network.Models.PSEffectiveRoute</span><span class="sxs-lookup"><span data-stu-id="d04d7-125">Microsoft.Azure.Commands.Network.Models.PSEffectiveRoute</span></span>

## <span data-ttu-id="d04d7-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d04d7-126">NOTES</span></span>

## <span data-ttu-id="d04d7-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d04d7-127">RELATED LINKS</span></span>

[<span data-ttu-id="d04d7-128">Get-AzEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="d04d7-128">Get-AzEffectiveNetworkSecurityGroup</span></span>](./Get-AzEffectiveNetworkSecurityGroup.md)



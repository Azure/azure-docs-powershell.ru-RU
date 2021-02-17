---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 84FDB0F7-E6DE-4E1B-BD71-89535EDC6AA1
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azeffectiveroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzEffectiveRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzEffectiveRouteTable.md
ms.openlocfilehash: e7d65e7797fb606306f0f0cc1e7c394fcf3d1d3d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100226033"
---
# <span data-ttu-id="43971-101">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="43971-101">Get-AzEffectiveRouteTable</span></span>

## <span data-ttu-id="43971-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43971-102">SYNOPSIS</span></span>
<span data-ttu-id="43971-103">Получает эффективную таблицу маршрутов сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="43971-103">Gets the effective route table of a network interface.</span></span>

## <span data-ttu-id="43971-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="43971-104">SYNTAX</span></span>

```
Get-AzEffectiveRouteTable -NetworkInterfaceName <String> [-ResourceGroupName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="43971-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="43971-105">DESCRIPTION</span></span>
<span data-ttu-id="43971-106">С **помощью cmdlet get-AzEffectiveRouteTable** возвращается эффективная таблица маршрутов, примененная в сетевом интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="43971-106">The **Get-AzEffectiveRouteTable** cmdlet returns the effective route table that is applied on a network interface.</span></span>

## <span data-ttu-id="43971-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="43971-107">EXAMPLES</span></span>

### <span data-ttu-id="43971-108">Пример 1. Получить эффективную таблицу маршрутов в сетевом интерфейсе</span><span class="sxs-lookup"><span data-stu-id="43971-108">Example 1: Get the effective route table on a network interface</span></span>
```
PS C:\>Get-AzEffectiveRouteTable -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="43971-109">Эта команда возвращает эффективную таблицу маршрутов, связанную с сетевым интерфейсом MyNetworkInterface в группе ресурсов MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="43971-109">This command gets the effective route table associated with network interface named MyNetworkInterface in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="43971-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="43971-110">PARAMETERS</span></span>

### <span data-ttu-id="43971-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="43971-111">-AsJob</span></span>
<span data-ttu-id="43971-112">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="43971-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="43971-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43971-113">-DefaultProfile</span></span>
<span data-ttu-id="43971-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="43971-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="43971-115">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="43971-115">-NetworkInterfaceName</span></span>
<span data-ttu-id="43971-116">Имя сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="43971-116">Specified the name of a network interface.</span></span>

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

### <span data-ttu-id="43971-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43971-117">-ResourceGroupName</span></span>
<span data-ttu-id="43971-118">Группа ресурсов в сетевом интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="43971-118">Specifies the resource group of a network interface.</span></span>

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

### <span data-ttu-id="43971-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43971-119">CommonParameters</span></span>
<span data-ttu-id="43971-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43971-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43971-121">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="43971-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43971-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="43971-122">INPUTS</span></span>

### <span data-ttu-id="43971-123">System.String</span><span class="sxs-lookup"><span data-stu-id="43971-123">System.String</span></span>

## <span data-ttu-id="43971-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="43971-124">OUTPUTS</span></span>

### <span data-ttu-id="43971-125">Microsoft.Azure.Commands.Network.Models.PSEffectiveRoute</span><span class="sxs-lookup"><span data-stu-id="43971-125">Microsoft.Azure.Commands.Network.Models.PSEffectiveRoute</span></span>

## <span data-ttu-id="43971-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="43971-126">NOTES</span></span>

## <span data-ttu-id="43971-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="43971-127">RELATED LINKS</span></span>

[<span data-ttu-id="43971-128">Get-AzEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="43971-128">Get-AzEffectiveNetworkSecurityGroup</span></span>](./Get-AzEffectiveNetworkSecurityGroup.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B9409AD6-F761-4B80-8E08-DBB2356F567D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azeffectivenetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzEffectiveNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzEffectiveNetworkSecurityGroup.md
ms.openlocfilehash: c0f7d2692472316d018d4a11b6843264c8666fe2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078939"
---
# <span data-ttu-id="62531-101">Get-AzEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="62531-101">Get-AzEffectiveNetworkSecurityGroup</span></span>

## <span data-ttu-id="62531-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="62531-102">SYNOPSIS</span></span>
<span data-ttu-id="62531-103">Возвращает эффективную сетевую группу безопасности сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="62531-103">Gets the effective network security group of a network interface.</span></span>

## <span data-ttu-id="62531-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="62531-104">SYNTAX</span></span>

```
Get-AzEffectiveNetworkSecurityGroup -NetworkInterfaceName <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="62531-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="62531-105">DESCRIPTION</span></span>
<span data-ttu-id="62531-106">Командлет **Get-AzEffectiveNetworkSecurityGroup** Возвращает действующую группу безопасности сети, которая применяется к сетевому интерфейсу.</span><span class="sxs-lookup"><span data-stu-id="62531-106">The **Get-AzEffectiveNetworkSecurityGroup** cmdlet returns the effective network security group that is applied on a network interface.</span></span>

## <span data-ttu-id="62531-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="62531-107">EXAMPLES</span></span>

### <span data-ttu-id="62531-108">Пример 1: получение эффективной сетевой группы безопасности на сетевом интерфейсе</span><span class="sxs-lookup"><span data-stu-id="62531-108">Example 1: Get the effective network security group on a network interface</span></span>
```
PS C:\>Get-AzEffectiveNetworkSecurityGroup -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="62531-109">Эта команда получает все действующие правила сетевой безопасности, связанные с сетевым интерфейсом MyNetworkInterface в группе ресурсов с именем myResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="62531-109">This command gets all of the effective network security rules associated with the network interface named MyNetworkInterface in the resource group named myResourceGroup.</span></span>

## <span data-ttu-id="62531-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="62531-110">PARAMETERS</span></span>

### <span data-ttu-id="62531-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62531-111">-DefaultProfile</span></span>
<span data-ttu-id="62531-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="62531-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="62531-113">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="62531-113">-NetworkInterfaceName</span></span>
<span data-ttu-id="62531-114">Указывает имя сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="62531-114">Specified the name of a network interface.</span></span>

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

### <span data-ttu-id="62531-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62531-115">-ResourceGroupName</span></span>
<span data-ttu-id="62531-116">Указывает группу ресурсов сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="62531-116">Specifies the resource group of a network interface.</span></span>

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

### <span data-ttu-id="62531-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62531-117">CommonParameters</span></span>
<span data-ttu-id="62531-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="62531-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62531-119">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="62531-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62531-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="62531-120">INPUTS</span></span>

### <span data-ttu-id="62531-121">System. String</span><span class="sxs-lookup"><span data-stu-id="62531-121">System.String</span></span>

## <span data-ttu-id="62531-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="62531-122">OUTPUTS</span></span>

### <span data-ttu-id="62531-123">Microsoft. Azure. Commands. Network. Models. PSEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="62531-123">Microsoft.Azure.Commands.Network.Models.PSEffectiveNetworkSecurityGroup</span></span>

## <span data-ttu-id="62531-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="62531-124">NOTES</span></span>

## <span data-ttu-id="62531-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="62531-125">RELATED LINKS</span></span>

[<span data-ttu-id="62531-126">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="62531-126">Get-AzEffectiveRouteTable</span></span>](./Get-AzEffectiveRouteTable.md)



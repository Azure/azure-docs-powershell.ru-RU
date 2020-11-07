---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: B9409AD6-F761-4B80-8E08-DBB2356F567D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermeffectivenetworksecuritygroup
schema: 2.0.0
ms.openlocfilehash: 214ab7f91791fa05453e2f4ef4238440d9c78a3d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913636"
---
# <span data-ttu-id="f05c0-101">Get-AzureRmEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="f05c0-101">Get-AzureRmEffectiveNetworkSecurityGroup</span></span>

## <span data-ttu-id="f05c0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f05c0-102">SYNOPSIS</span></span>
<span data-ttu-id="f05c0-103">Возвращает эффективную сетевую группу безопасности сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="f05c0-103">Gets the effective network security group of a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f05c0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f05c0-104">SYNTAX</span></span>

```
Get-AzureRmEffectiveNetworkSecurityGroup -NetworkInterfaceName <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f05c0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f05c0-105">DESCRIPTION</span></span>
<span data-ttu-id="f05c0-106">Командлет **Get-AzureRmEffectiveNetworkSecurityGroup** Возвращает действующую группу безопасности сети, которая применяется к сетевому интерфейсу.</span><span class="sxs-lookup"><span data-stu-id="f05c0-106">The **Get-AzureRmEffectiveNetworkSecurityGroup** cmdlet returns the effective network security group that is applied on a network interface.</span></span>

## <span data-ttu-id="f05c0-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f05c0-107">EXAMPLES</span></span>

### <span data-ttu-id="f05c0-108">Пример 1: получение эффективной сетевой группы безопасности на сетевом интерфейсе</span><span class="sxs-lookup"><span data-stu-id="f05c0-108">Example 1: Get the effective network security group on a network interface</span></span>
```
PS C:\>Get-AzureRmEffectiveNetworkSecurityGroup -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="f05c0-109">Эта команда получает все действующие правила сетевой безопасности, связанные с сетевым интерфейсом MyNetworkInterface в группе ресурсов с именем myResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="f05c0-109">This command gets all of the effective network security rules associated with the network interface named MyNetworkInterface in the resource group named myResourceGroup.</span></span>

## <span data-ttu-id="f05c0-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f05c0-110">PARAMETERS</span></span>

### <span data-ttu-id="f05c0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f05c0-111">-DefaultProfile</span></span>
<span data-ttu-id="f05c0-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f05c0-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f05c0-113">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="f05c0-113">-NetworkInterfaceName</span></span>
<span data-ttu-id="f05c0-114">Указывает имя сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="f05c0-114">Specified the name of a network interface.</span></span>

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

### <span data-ttu-id="f05c0-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f05c0-115">-ResourceGroupName</span></span>
<span data-ttu-id="f05c0-116">Указывает группу ресурсов сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="f05c0-116">Specifies the resource group of a network interface.</span></span>

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

### <span data-ttu-id="f05c0-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f05c0-117">CommonParameters</span></span>
<span data-ttu-id="f05c0-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f05c0-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f05c0-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f05c0-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f05c0-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f05c0-120">INPUTS</span></span>

## <span data-ttu-id="f05c0-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f05c0-121">OUTPUTS</span></span>

### <span data-ttu-id="f05c0-122">Microsoft. Azure. Commands. Network. Models. PSEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="f05c0-122">Microsoft.Azure.Commands.Network.Models.PSEffectiveNetworkSecurityGroup</span></span>

## <span data-ttu-id="f05c0-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="f05c0-123">NOTES</span></span>

## <span data-ttu-id="f05c0-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f05c0-124">RELATED LINKS</span></span>

[<span data-ttu-id="f05c0-125">Get-AzureRmEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="f05c0-125">Get-AzureRmEffectiveRouteTable</span></span>](./Get-AzureRmEffectiveRouteTable.md)



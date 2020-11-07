---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: B9409AD6-F761-4B80-8E08-DBB2356F567D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermeffectivenetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmEffectiveNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmEffectiveNetworkSecurityGroup.md
ms.openlocfilehash: a7c131db8ce5a3489bc2a869e31b0ef7ab89f3c2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733014"
---
# <span data-ttu-id="5a016-101">Get-AzureRmEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="5a016-101">Get-AzureRmEffectiveNetworkSecurityGroup</span></span>

## <span data-ttu-id="5a016-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5a016-102">SYNOPSIS</span></span>
<span data-ttu-id="5a016-103">Возвращает эффективную сетевую группу безопасности сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="5a016-103">Gets the effective network security group of a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5a016-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5a016-104">SYNTAX</span></span>

```
Get-AzureRmEffectiveNetworkSecurityGroup -NetworkInterfaceName <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5a016-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5a016-105">DESCRIPTION</span></span>
<span data-ttu-id="5a016-106">Командлет **Get-AzureRmEffectiveNetworkSecurityGroup** Возвращает действующую группу безопасности сети, которая применяется к сетевому интерфейсу.</span><span class="sxs-lookup"><span data-stu-id="5a016-106">The **Get-AzureRmEffectiveNetworkSecurityGroup** cmdlet returns the effective network security group that is applied on a network interface.</span></span>

## <span data-ttu-id="5a016-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5a016-107">EXAMPLES</span></span>

### <span data-ttu-id="5a016-108">Пример 1: получение эффективной сетевой группы безопасности на сетевом интерфейсе</span><span class="sxs-lookup"><span data-stu-id="5a016-108">Example 1: Get the effective network security group on a network interface</span></span>
```
PS C:\>Get-AzureRmEffectiveNetworkSecurityGroup -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="5a016-109">Эта команда получает все действующие правила сетевой безопасности, связанные с сетевым интерфейсом MyNetworkInterface в группе ресурсов с именем myResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="5a016-109">This command gets all of the effective network security rules associated with the network interface named MyNetworkInterface in the resource group named myResourceGroup.</span></span>

## <span data-ttu-id="5a016-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5a016-110">PARAMETERS</span></span>

### <span data-ttu-id="5a016-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a016-111">-DefaultProfile</span></span>
<span data-ttu-id="5a016-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5a016-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5a016-113">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="5a016-113">-NetworkInterfaceName</span></span>
<span data-ttu-id="5a016-114">Указывает имя сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="5a016-114">Specified the name of a network interface.</span></span>

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

### <span data-ttu-id="5a016-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a016-115">-ResourceGroupName</span></span>
<span data-ttu-id="5a016-116">Указывает группу ресурсов сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="5a016-116">Specifies the resource group of a network interface.</span></span>

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

### <span data-ttu-id="5a016-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a016-117">CommonParameters</span></span>
<span data-ttu-id="5a016-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5a016-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a016-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a016-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a016-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5a016-120">INPUTS</span></span>

### <span data-ttu-id="5a016-121">Ничего</span><span class="sxs-lookup"><span data-stu-id="5a016-121">None</span></span>
<span data-ttu-id="5a016-122">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="5a016-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5a016-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5a016-123">OUTPUTS</span></span>

### <span data-ttu-id="5a016-124">Microsoft. Azure. Commands. Network. Models. PSEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="5a016-124">Microsoft.Azure.Commands.Network.Models.PSEffectiveNetworkSecurityGroup</span></span>

## <span data-ttu-id="5a016-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="5a016-125">NOTES</span></span>

## <span data-ttu-id="5a016-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5a016-126">RELATED LINKS</span></span>

[<span data-ttu-id="5a016-127">Get-AzureRmEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="5a016-127">Get-AzureRmEffectiveRouteTable</span></span>](./Get-AzureRmEffectiveRouteTable.md)



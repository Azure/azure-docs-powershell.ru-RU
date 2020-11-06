---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: B9409AD6-F761-4B80-8E08-DBB2356F567D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermeffectivenetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmEffectiveNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmEffectiveNetworkSecurityGroup.md
ms.openlocfilehash: 565d0748104e537f448a40116a48f0cd34ebf16b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560088"
---
# <span data-ttu-id="9da89-101">Get-AzureRmEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="9da89-101">Get-AzureRmEffectiveNetworkSecurityGroup</span></span>

## <span data-ttu-id="9da89-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9da89-102">SYNOPSIS</span></span>
<span data-ttu-id="9da89-103">Возвращает эффективную сетевую группу безопасности сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="9da89-103">Gets the effective network security group of a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9da89-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9da89-104">SYNTAX</span></span>

```
Get-AzureRmEffectiveNetworkSecurityGroup -NetworkInterfaceName <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9da89-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9da89-105">DESCRIPTION</span></span>
<span data-ttu-id="9da89-106">Командлет **Get-AzureRmEffectiveNetworkSecurityGroup** Возвращает действующую группу безопасности сети, которая применяется к сетевому интерфейсу.</span><span class="sxs-lookup"><span data-stu-id="9da89-106">The **Get-AzureRmEffectiveNetworkSecurityGroup** cmdlet returns the effective network security group that is applied on a network interface.</span></span>

## <span data-ttu-id="9da89-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9da89-107">EXAMPLES</span></span>

### <span data-ttu-id="9da89-108">Пример 1: получение эффективной сетевой группы безопасности на сетевом интерфейсе</span><span class="sxs-lookup"><span data-stu-id="9da89-108">Example 1: Get the effective network security group on a network interface</span></span>
```
PS C:\>Get-AzureRmEffectiveNetworkSecurityGroup -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="9da89-109">Эта команда получает все действующие правила сетевой безопасности, связанные с сетевым интерфейсом MyNetworkInterface в группе ресурсов с именем myResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="9da89-109">This command gets all of the effective network security rules associated with the network interface named MyNetworkInterface in the resource group named myResourceGroup.</span></span>

## <span data-ttu-id="9da89-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9da89-110">PARAMETERS</span></span>

### <span data-ttu-id="9da89-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9da89-111">-DefaultProfile</span></span>
<span data-ttu-id="9da89-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9da89-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9da89-113">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="9da89-113">-NetworkInterfaceName</span></span>
<span data-ttu-id="9da89-114">Указывает имя сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="9da89-114">Specified the name of a network interface.</span></span>

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

### <span data-ttu-id="9da89-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9da89-115">-ResourceGroupName</span></span>
<span data-ttu-id="9da89-116">Указывает группу ресурсов сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="9da89-116">Specifies the resource group of a network interface.</span></span>

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

### <span data-ttu-id="9da89-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9da89-117">CommonParameters</span></span>
<span data-ttu-id="9da89-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9da89-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9da89-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9da89-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9da89-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9da89-120">INPUTS</span></span>

### <span data-ttu-id="9da89-121">System. String</span><span class="sxs-lookup"><span data-stu-id="9da89-121">System.String</span></span>

## <span data-ttu-id="9da89-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9da89-122">OUTPUTS</span></span>

### <span data-ttu-id="9da89-123">Microsoft. Azure. Commands. Network. Models. PSEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="9da89-123">Microsoft.Azure.Commands.Network.Models.PSEffectiveNetworkSecurityGroup</span></span>

## <span data-ttu-id="9da89-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="9da89-124">NOTES</span></span>

## <span data-ttu-id="9da89-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9da89-125">RELATED LINKS</span></span>

[<span data-ttu-id="9da89-126">Get-AzureRmEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="9da89-126">Get-AzureRmEffectiveRouteTable</span></span>](./Get-AzureRmEffectiveRouteTable.md)



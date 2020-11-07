---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B9409AD6-F761-4B80-8E08-DBB2356F567D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azeffectivenetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzEffectiveNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzEffectiveNetworkSecurityGroup.md
ms.openlocfilehash: a960d5b2f6daf19fc4e46eb253b596eb88e6bd71
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910030"
---
# <span data-ttu-id="dc9ab-101">Get-AzEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="dc9ab-101">Get-AzEffectiveNetworkSecurityGroup</span></span>

## <span data-ttu-id="dc9ab-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dc9ab-102">SYNOPSIS</span></span>
<span data-ttu-id="dc9ab-103">Возвращает эффективную сетевую группу безопасности сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="dc9ab-103">Gets the effective network security group of a network interface.</span></span>

## <span data-ttu-id="dc9ab-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dc9ab-104">SYNTAX</span></span>

```
Get-AzEffectiveNetworkSecurityGroup -NetworkInterfaceName <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dc9ab-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dc9ab-105">DESCRIPTION</span></span>
<span data-ttu-id="dc9ab-106">Командлет **Get-AzEffectiveNetworkSecurityGroup** Возвращает действующую группу безопасности сети, которая применяется к сетевому интерфейсу.</span><span class="sxs-lookup"><span data-stu-id="dc9ab-106">The **Get-AzEffectiveNetworkSecurityGroup** cmdlet returns the effective network security group that is applied on a network interface.</span></span>

## <span data-ttu-id="dc9ab-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dc9ab-107">EXAMPLES</span></span>

### <span data-ttu-id="dc9ab-108">Пример 1: получение эффективной сетевой группы безопасности на сетевом интерфейсе</span><span class="sxs-lookup"><span data-stu-id="dc9ab-108">Example 1: Get the effective network security group on a network interface</span></span>
```
PS C:\>Get-AzEffectiveNetworkSecurityGroup -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="dc9ab-109">Эта команда получает все действующие правила сетевой безопасности, связанные с сетевым интерфейсом MyNetworkInterface в группе ресурсов с именем myResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="dc9ab-109">This command gets all of the effective network security rules associated with the network interface named MyNetworkInterface in the resource group named myResourceGroup.</span></span>

## <span data-ttu-id="dc9ab-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dc9ab-110">PARAMETERS</span></span>

### <span data-ttu-id="dc9ab-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc9ab-111">-DefaultProfile</span></span>
<span data-ttu-id="dc9ab-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dc9ab-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dc9ab-113">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="dc9ab-113">-NetworkInterfaceName</span></span>
<span data-ttu-id="dc9ab-114">Указывает имя сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="dc9ab-114">Specified the name of a network interface.</span></span>

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

### <span data-ttu-id="dc9ab-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc9ab-115">-ResourceGroupName</span></span>
<span data-ttu-id="dc9ab-116">Указывает группу ресурсов сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="dc9ab-116">Specifies the resource group of a network interface.</span></span>

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

### <span data-ttu-id="dc9ab-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc9ab-117">CommonParameters</span></span>
<span data-ttu-id="dc9ab-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dc9ab-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc9ab-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc9ab-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc9ab-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dc9ab-120">INPUTS</span></span>

## <span data-ttu-id="dc9ab-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dc9ab-121">OUTPUTS</span></span>

### <span data-ttu-id="dc9ab-122">Microsoft. Azure. Commands. Network. Models. PSEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="dc9ab-122">Microsoft.Azure.Commands.Network.Models.PSEffectiveNetworkSecurityGroup</span></span>

## <span data-ttu-id="dc9ab-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="dc9ab-123">NOTES</span></span>

## <span data-ttu-id="dc9ab-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dc9ab-124">RELATED LINKS</span></span>

[<span data-ttu-id="dc9ab-125">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="dc9ab-125">Get-AzEffectiveRouteTable</span></span>](./Get-AzEffectiveRouteTable.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5AECCBD7-1FDE-4217-9F59-36328062E669
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkSecurityGroup.md
ms.openlocfilehash: beb2b723a0b72f7ab485846f6f55fabd4e6ef9aa
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93909949"
---
# <span data-ttu-id="96077-101">Get-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="96077-101">Get-AzNetworkSecurityGroup</span></span>

## <span data-ttu-id="96077-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="96077-102">SYNOPSIS</span></span>
<span data-ttu-id="96077-103">Получает сетевую группу безопасности.</span><span class="sxs-lookup"><span data-stu-id="96077-103">Gets a network security group.</span></span>

## <span data-ttu-id="96077-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="96077-104">SYNTAX</span></span>

### <span data-ttu-id="96077-105">NOEXPAND</span><span class="sxs-lookup"><span data-stu-id="96077-105">NoExpand</span></span>
```
Get-AzNetworkSecurityGroup [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="96077-106">Кройте</span><span class="sxs-lookup"><span data-stu-id="96077-106">Expand</span></span>
```
Get-AzNetworkSecurityGroup -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="96077-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="96077-107">DESCRIPTION</span></span>
<span data-ttu-id="96077-108">Командлет **Get-AzNetworkSecurityGroup** получает сетевую группу безопасности Azure.</span><span class="sxs-lookup"><span data-stu-id="96077-108">The **Get-AzNetworkSecurityGroup** cmdlet gets an Azure network security group.</span></span>

## <span data-ttu-id="96077-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="96077-109">EXAMPLES</span></span>

### <span data-ttu-id="96077-110">1. получение существующей группы безопасности сети</span><span class="sxs-lookup"><span data-stu-id="96077-110">1: Retrieve an existing network security group</span></span>
```
Get-AzNetworkSecurityGroup -Name  nsg1 -ResourceGroupName "rg1"
```

<span data-ttu-id="96077-111">Эта команда возвращает содержимое группы безопасности сети Azure "nsg1" в группе ресурсов "Rg1"</span><span class="sxs-lookup"><span data-stu-id="96077-111">This command returns contents of Azure network security group "nsg1" in resource group "rg1"</span></span>

## <span data-ttu-id="96077-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="96077-112">PARAMETERS</span></span>

### <span data-ttu-id="96077-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96077-113">-DefaultProfile</span></span>
<span data-ttu-id="96077-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="96077-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="96077-115">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="96077-115">-ExpandResource</span></span>
```yaml
Type: String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96077-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="96077-116">-Name</span></span>
<span data-ttu-id="96077-117">Указывает имя сетевой группы безопасности, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="96077-117">Specifies the name of the network security group that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96077-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96077-118">-ResourceGroupName</span></span>
<span data-ttu-id="96077-119">Указывает имя группы ресурсов, к которой принадлежит Сетевая группа безопасности.</span><span class="sxs-lookup"><span data-stu-id="96077-119">Specifies the name of the resource group that the network security group belongs to.</span></span>

```yaml
Type: String
Parameter Sets: NoExpand
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96077-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96077-120">CommonParameters</span></span>
<span data-ttu-id="96077-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="96077-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96077-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96077-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96077-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="96077-123">INPUTS</span></span>

## <span data-ttu-id="96077-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="96077-124">OUTPUTS</span></span>

### <span data-ttu-id="96077-125">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="96077-125">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="96077-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="96077-126">NOTES</span></span>

## <span data-ttu-id="96077-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="96077-127">RELATED LINKS</span></span>

[<span data-ttu-id="96077-128">New-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="96077-128">New-AzNetworkSecurityGroup</span></span>](./New-AzNetworkSecurityGroup.md)

[<span data-ttu-id="96077-129">Remove-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="96077-129">Remove-AzNetworkSecurityGroup</span></span>](./Remove-AzNetworkSecurityGroup.md)

[<span data-ttu-id="96077-130">Set-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="96077-130">Set-AzNetworkSecurityGroup</span></span>](./Set-AzNetworkSecurityGroup.md)



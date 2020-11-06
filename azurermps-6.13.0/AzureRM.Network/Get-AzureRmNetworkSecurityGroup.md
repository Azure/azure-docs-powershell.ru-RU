---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5AECCBD7-1FDE-4217-9F59-36328062E669
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkSecurityGroup.md
ms.openlocfilehash: 32bcc3b83ad34a0f60b01048212d402745934317
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93570216"
---
# <span data-ttu-id="8710e-101">Get-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="8710e-101">Get-AzureRmNetworkSecurityGroup</span></span>

## <span data-ttu-id="8710e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8710e-102">SYNOPSIS</span></span>
<span data-ttu-id="8710e-103">Получает сетевую группу безопасности.</span><span class="sxs-lookup"><span data-stu-id="8710e-103">Gets a network security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8710e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8710e-104">SYNTAX</span></span>

### <span data-ttu-id="8710e-105">NOEXPAND</span><span class="sxs-lookup"><span data-stu-id="8710e-105">NoExpand</span></span>
```
Get-AzureRmNetworkSecurityGroup [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8710e-106">Кройте</span><span class="sxs-lookup"><span data-stu-id="8710e-106">Expand</span></span>
```
Get-AzureRmNetworkSecurityGroup -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8710e-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8710e-107">DESCRIPTION</span></span>
<span data-ttu-id="8710e-108">Командлет **Get-AzureRmNetworkSecurityGroup** получает сетевую группу безопасности Azure.</span><span class="sxs-lookup"><span data-stu-id="8710e-108">The **Get-AzureRmNetworkSecurityGroup** cmdlet gets an Azure network security group.</span></span>

## <span data-ttu-id="8710e-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8710e-109">EXAMPLES</span></span>

### <span data-ttu-id="8710e-110">1. получение существующей группы безопасности сети</span><span class="sxs-lookup"><span data-stu-id="8710e-110">1: Retrieve an existing network security group</span></span>
```
Get-AzureRmNetworkSecurityGroup -Name  nsg1 -ResourceGroupName "rg1"
```

<span data-ttu-id="8710e-111">Эта команда возвращает содержимое группы безопасности сети Azure "nsg1" в группе ресурсов "Rg1"</span><span class="sxs-lookup"><span data-stu-id="8710e-111">This command returns contents of Azure network security group "nsg1" in resource group "rg1"</span></span>

## <span data-ttu-id="8710e-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8710e-112">PARAMETERS</span></span>

### <span data-ttu-id="8710e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8710e-113">-DefaultProfile</span></span>
<span data-ttu-id="8710e-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8710e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8710e-115">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="8710e-115">-ExpandResource</span></span>
```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8710e-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8710e-116">-Name</span></span>
<span data-ttu-id="8710e-117">Указывает имя сетевой группы безопасности, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="8710e-117">Specifies the name of the network security group that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8710e-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8710e-118">-ResourceGroupName</span></span>
<span data-ttu-id="8710e-119">Указывает имя группы ресурсов, к которой принадлежит Сетевая группа безопасности.</span><span class="sxs-lookup"><span data-stu-id="8710e-119">Specifies the name of the resource group that the network security group belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8710e-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8710e-120">CommonParameters</span></span>
<span data-ttu-id="8710e-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8710e-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8710e-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8710e-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8710e-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8710e-123">INPUTS</span></span>

### <span data-ttu-id="8710e-124">System. String</span><span class="sxs-lookup"><span data-stu-id="8710e-124">System.String</span></span>

## <span data-ttu-id="8710e-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8710e-125">OUTPUTS</span></span>

### <span data-ttu-id="8710e-126">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="8710e-126">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="8710e-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="8710e-127">NOTES</span></span>

## <span data-ttu-id="8710e-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8710e-128">RELATED LINKS</span></span>

[<span data-ttu-id="8710e-129">New-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="8710e-129">New-AzureRmNetworkSecurityGroup</span></span>](./New-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="8710e-130">Remove-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="8710e-130">Remove-AzureRmNetworkSecurityGroup</span></span>](./Remove-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="8710e-131">Set-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="8710e-131">Set-AzureRmNetworkSecurityGroup</span></span>](./Set-AzureRmNetworkSecurityGroup.md)



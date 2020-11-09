---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallPolicy.md
ms.openlocfilehash: f53733976d946b61fc143e0a2b2e9be71017b7f6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94318617"
---
# <span data-ttu-id="ca3fe-101">Get-AzFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="ca3fe-101">Get-AzFirewallPolicy</span></span>

## <span data-ttu-id="ca3fe-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ca3fe-102">SYNOPSIS</span></span>
<span data-ttu-id="ca3fe-103">Получение политики брандмауэра Azure</span><span class="sxs-lookup"><span data-stu-id="ca3fe-103">Gets a Azure Firewall Policy</span></span>

## <span data-ttu-id="ca3fe-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ca3fe-104">SYNTAX</span></span>

### <span data-ttu-id="ca3fe-105">GetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ca3fe-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzFirewallPolicy -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ca3fe-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ca3fe-106">GetByResourceIdParameterSet</span></span>
```
Get-AzFirewallPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ca3fe-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ca3fe-107">DESCRIPTION</span></span>
<span data-ttu-id="ca3fe-108">Командлет **Get-AzFirewallPolicy** получает один или несколько брандмауэров в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ca3fe-108">The **Get-AzFirewallPolicy** cmdlet gets one or more Firewalls in a resource group</span></span>

## <span data-ttu-id="ca3fe-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ca3fe-109">EXAMPLES</span></span>

### <span data-ttu-id="ca3fe-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ca3fe-110">Example 1</span></span>
```powershell
PS C:\> Get-AzFirewallPolicy -Name firwallPolicy -ResourceGroupName TestRg
```

<span data-ttu-id="ca3fe-111">В этом примере выполняется получение политики брандмауэра с именем "firewallPolicy" в группе ресурсов "TestRg"</span><span class="sxs-lookup"><span data-stu-id="ca3fe-111">This example get a firewall policy named "firewallPolicy" in the resource group "TestRg"</span></span>

## <span data-ttu-id="ca3fe-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ca3fe-112">PARAMETERS</span></span>

### <span data-ttu-id="ca3fe-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca3fe-113">-DefaultProfile</span></span>
<span data-ttu-id="ca3fe-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ca3fe-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca3fe-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ca3fe-115">-Name</span></span>
<span data-ttu-id="ca3fe-116">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="ca3fe-116">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca3fe-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca3fe-117">-ResourceGroupName</span></span>
<span data-ttu-id="ca3fe-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ca3fe-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca3fe-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ca3fe-119">-ResourceId</span></span>
<span data-ttu-id="ca3fe-120">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="ca3fe-120">The resource Id.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca3fe-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca3fe-121">CommonParameters</span></span>
<span data-ttu-id="ca3fe-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ca3fe-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca3fe-123">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ca3fe-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca3fe-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ca3fe-124">INPUTS</span></span>

### <span data-ttu-id="ca3fe-125">System. String</span><span class="sxs-lookup"><span data-stu-id="ca3fe-125">System.String</span></span>

## <span data-ttu-id="ca3fe-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ca3fe-126">OUTPUTS</span></span>

### <span data-ttu-id="ca3fe-127">Microsoft. Azure. Commands. Network. Models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="ca3fe-127">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

### <span data-ttu-id="ca3fe-128">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. Network.. PSAzureFirewall, Microsoft. Azure. PowerShell. командлеты. Network, Version = 1.12.0.0, культура = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="ca3fe-128">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSAzureFirewall, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=1.12.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="ca3fe-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="ca3fe-129">NOTES</span></span>

## <span data-ttu-id="ca3fe-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ca3fe-130">RELATED LINKS</span></span>
